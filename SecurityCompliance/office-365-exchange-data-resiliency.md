---
title: Resiliência de dados do Exchange Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Uma explicação dos vários aspectos de resiliência de dados dentro do Exchange Online e o Office 365.
ms.openlocfilehash: 8d0448a95f010b766faf852a374513a1c2da61fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523949"
---
# <a name="exchange-online-data-resiliency-in-office-365"></a>Resiliência de dados on-line do Exchange no Office 365

## <a name="introduction"></a>Introdução
Existem dois tipos de corrupção que podem afetar a um banco de dados do Exchange: corrupção física, que é geralmente causada por problemas de hardware (em particular, hardware de armazenamento), e corrupção lógica, que ocorre devido aos outros fatores. Geralmente, há dois tipos de corrupção lógica que podem ocorrer em um banco de dados do Exchange: 
- **Corrupção lógica do banco de dados** - as correspondências de soma de verificação de página de banco de dados, mas os dados na página logicamente está errado. Isso pode ocorrer quando o mecanismo de banco de dados (o Extensible Storage Engine (ESE)) tenta escrever uma página de banco de dados e o mesmo que o sistema operacional retorna uma mensagem de êxito, os dados são seja nunca gravados no disco ou ele está escrito para o lugar errado. Isso é conhecido como um *perdido flush*. ESE inclui vários recursos e proteções que foram projetadas para evitar corrupção física de um banco de dados e outros cenários de perda de dados. Para impedir que liberações perdidas perda de dados, o ESE inclui um mecanismo de detecção de liberação perdidas no banco de dados, juntamente com um recurso (restauração de página única) para corrigi-la. 
- **Corrupção lógica do repositório** - dados é adicionado, excluído ou manipulado de forma que o usuário não esperar. Nesses casos são geralmente causados por aplicativos de terceiros. Geralmente, é só corrupção no sentido de que o usuário visualiza como corrupção. O armazenamento do Exchange considera a transação que produzidos corrupção lógica para ser uma série de operações de MAPI válidas. Os recursos de [Retenção In-loco](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) no Exchange Online oferece proteção contra corrupção lógica do repositório (porque ele impede que o conteúdo sendo excluído permanentemente por um usuário ou um aplicativo). 

O Exchange Online realiza várias verificações de consistência em arquivos de log replicados durante inspeção de log e a reprodução de log. Essas verificações de consistência objetivo de impedir danos físicos sejam replicados pelo sistema. Por exemplo, durante a inspeção de log, há uma verificação de integridade física que verifica o arquivo de log e valida se a soma de verificação gravada no arquivo de log corresponde a soma de verificação gerada na memória. Além disso, o cabeçalho do arquivo de log é examinado para certificar-se de que a assinatura do arquivo de log registrada no cabeçalho log corresponde do arquivo de log. Durante a reprodução de log, o arquivo de log passa por ainda mais exames detalhados. Por exemplo, o cabeçalho de banco de dados também contém a assinatura de log que é comparada com a assinatura do arquivo de log para garantir que elas correspondam. 

Proteção contra corrupção de dados de caixa de correio no Exchange Online é obtida usando a proteção de dados nativa do Exchange, uma estratégia de resiliência que aproveita a replicação de nível de aplicativo em vários servidores e diversos datacenters, juntamente com outros recursos que ajudam a proteger os dados sejam perdidas devido a corrupção ou outros motivos. Esses recursos incluem recursos nativos que são gerenciados pela Microsoft ou Exchange Online próprio aplicativo, tais como:

- [Grupos de disponibilidade de dados](https://docs.microsoft.com/exchange/back-up-email)
- Correção de Bit único 
- Banco de dados online verificação 
- Detecção de liberação perdida 
- Restauração de página única 
- Serviço de replicação de caixa de correio 
- Verificações de arquivo de log 
- Implantação no sistema de arquivos resiliente 

Para obter mais informações sobre os recursos nativos listados acima, clique em hiperlinks acima e veja abaixo para obter informações adicionais e para obter detalhes sobre os itens sem hiperlinks. Além desses recursos nativos, o Exchange Online também inclui recursos de resiliência de dados que os clientes podem gerenciar, tais como: 
- [Recuperação de Item único (habilitado por padrão)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Bloqueio In-loco e Retenção de Litígio](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Retenção de Item de excluído e caixas de correio de Soft-Deleted (ambos ativados por padrão)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Grupos de Disponibilidade de Banco de Dados 
Cada banco de dados de caixa de correio no Office 365 é hospedado em um [grupo de disponibilidade do banco de dados (DAG)](https://docs.microsoft.com/exchange/back-up-email) e replicado em centros de dados geograficamente separados com a mesma região. A configuração mais comum é quatro cópias de banco de dados em quatro datacenters; No entanto, algumas regiões tem menos de centros de dados (bancos de dados são replicados para três centros de dados na Índia e dois datacenters na Austrália e Japão). Mas em todos os casos, cada banco de dados de caixa de correio tem quatro cópias distribuídas em vários datacenters, garantindo assim que os dados de caixa de correio estão protegidos contra falhas de datacenter até mesmo, hardware e software. 

Sem essas quatro cópias, três deles são configurados como altamente disponível. A cópia do quarta é configurada como um [atraso de cópia de banco de dados](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies). A cópia do banco de dados com retardamento não se destina a recuperação de caixa de correio individual ou recuperação de item de caixa de correio. Seu objetivo é fornecer um mecanismo de recuperação para o evento raro de todo o sistema, uma catástrofe corrupção lógica. 

Cópias de banco de dados com atraso no Exchange Online são configuradas com um tempo de retardo de repetição de arquivo de log de sete dias. Além disso, o Gerenciador de retardo de repetição do Exchange está habilitado para fornecer log dinâmico arquivo descarte de cópias com retardamento permitir que cópias de banco de dados com retardamento reparo automático e gerenciar o crescimento do arquivo de log. Embora o atraso cópias são usadas no Exchange Online do banco de dados, é importante entender que não são um backup garantido no momento. Cópias de banco de dados com atraso no Exchange Online, que tem um limite de disponibilidade, normalmente aproximadamente 90%, devido aos períodos em que o disco que contém uma cópia com atraso é perdido devido à falha de disco, a cópia com atraso se tornando uma altamente disponível copiar (devido à automática de descarte), também como os períodos onde a cópia do banco de dados com retardamento está criando novamente o log de repetição fila. 

## <a name="transport-resilience"></a>Resiliência de transporte 
O Exchange Online inclui dois recursos de resiliência de transporte primário: Safety Net e redundância de sombra. Redundância de sombra mantém uma cópia redundante de uma mensagem enquanto ela está em trânsito. Safety Net mantém uma cópia redundante de uma mensagem depois que a mensagem é entregue com êxito. 

Com a redundância de sombra, cada servidor de transporte Exchange Online faz uma cópia de cada mensagem recebida antes que ele reconhece com êxito recebendo a mensagem para o servidor de envio. Isso faz com que todas as mensagens no pipeline de transporte redundantes em trânsito. Se o Exchange Online determina que a mensagem original foi perdida em trânsito, uma cópia redundante da mensagem é entregue novamente. 

Rede de segurança é uma fila de transporte que está associada com o serviço de transporte em um servidor de caixa de correio. Essa fila armazena cópias das mensagens que foram processadas com êxito pelo servidor. Quando uma falha de banco de dados ou o servidor de caixa de correio requer Ativando uma cópia desatualizada do banco de dados de caixa de correio, as mensagens na fila Safety Net automaticamente são reenviadas para a nova cópia ativa do banco de dados de caixa de correio. Safety Net também são redundante, eliminando o transporte como um único ponto de falha. Ele usa o conceito de uma rede de segurança principal e uma sombra Safety Net no qual se o Safety Net principal não está disponível por mais de 12 horas, reenviar solicitações se tornam as solicitações de reenvio de sombra e as mensagens são entregues novamente da sombra Safety Net.

Reenvios mensagens da Safety Net são iniciados automaticamente pelo componente Gerenciador ativo do serviço de replicação do Microsoft Exchange que gerencia a caixa de correio e DAGs cópias de banco de dados. Nenhuma ação manual é necessárias para reenviar mensagens da Safety Net. 

## <a name="single-bit-correction"></a>Correção de Bit único 
ESE inclui um mecanismo para detectar e resolver erros de CRC de bit único (também conhecido como bit único inverte) que são o resultado de erros de hardware (e, como tal, representam corrupção física). Quando esses erros ocorrem, ESE corrige-las automaticamente e registra um evento no log de eventos. 

## <a name="online-database-scanning"></a>Banco de dados online verificação 
Banco de dados online verificação (também conhecida como a *soma de banco de dados*) é o processo onde um ESE usa um verificador de consistência do banco de dados para cada página de leitura e verificar para corrupção de página. A principal finalidade é detectar corrupção física e liberações perdidas que podem não ser obtendo detectadas pelas operações transacionais. Verificação de banco de dados também executa a falha de pós-armazenamento de operações. Espaço pode ser vazado devido a falhas e verificação de banco de dados online localiza e recupera espaço perdido. O sistema foi projetado com a expectativa que cada banco de dados sejam verificado totalmente uma vez a cada sete dias. 

## <a name="lost-flush-detection"></a>Detecção de liberação perdida 
Um flush perdido ocorre quando uma operação de gravação do banco de dados que o sistema/operacional subsistema do disco retornado como concluída, na verdade, não pôde ser gravada para disco ou foi escrito no local errado. Perdido liberação de incidentes pode resultado na corrupção lógica do banco de dados, portanto para impedir que liberações perdidas resulta em perda de dados, ESE inclui um mecanismo de detecção de liberação perdidas. Como as páginas de banco de dados são gravadas cópias passivas, uma verificação é executada por liberações perdidas na cópia ativa. Se for detectado um flush perdida, ESE pode reparar o processo usando uma página no processo de aplicação de patch. 

## <a name="single-page-restore"></a>Restauração de página única 
Restauração de página única, também conhecido como *correção de página*, é um processo automático onde as páginas do banco de dados corrompido são substituídas por cópias íntegras de uma réplica íntegra. O processo de reparo para uma página corrompido depende se a cópia do banco de dados está ativo ou passivo. Quando uma cópia do banco de dados ativo encontra uma página corrompida, ele pode copiar uma página de uma das suas réplicas, desde que a página copia é completamente atualizada. Isso é feito colocando-se uma solicitação para a página em um fluxo de log, que é a base da replicação de banco de dados de caixa de correio. Assim que uma réplica encontra a solicitação de página responderá enviando uma cópia da página para a cópia do banco de dados solicitante. Restauração de página única também oferece um mecanismo de comunicação assíncrona para ativa solicitar uma página de réplicas, mesmo se as réplicas estiverem offline. 

No caso de danos em uma cópia passiva do banco de dados, incluindo uma cópia do banco de dados com retardamento, pois essas cópias são sempre por trás de sua cópia ativa, é sempre seguro copiar qualquer página da cópia ativa para uma cópia passiva. Uma cópia passiva do banco de dados é por natureza altamente disponível e, portanto durante a processo de aplicação de patches de página, o log reproduzindo é suspenso, mas a cópia de log continuará. A cópia passiva do banco de dados recupera uma cópia da página corrompida da cópia ativa, aguardará até que o arquivo de log que atende aos requisitos de geração de log exigidos máximo é copiado inspecionado e, em seguida, patches a página corrompida. Depois que a página tiver sido corrigida, retoma a reprodução de log. O processo é o mesmo para a cópia do banco de dados com retardamento, exceto pelo fato do banco de dados com retardamento primeiro repete todos os arquivos de log que são necessários para alcançar um estado de patches. 

## <a name="mailbox-replication-service"></a>Serviço de replicação de caixa de correio 
Mover caixas de correio é uma parte importante do gerenciamento de um serviço de email em grande escala. Sempre são atualizadas tecnologias e atualizações de hardware e a versão para lidar com, para ter uma robusta acelerado sistema que permite que nossos engenheiros realizar isso funcione enquanto mantém a caixa de correio move transparente para os usuários (, certificando-se de que eles permanecem on-line ao longo do processo) é a chave e certificando-se de que o processo dimensiona normalmente como obtém de caixas de correio maiores. 

O serviço de replicação de caixa de correio do Exchange (MRS) é responsável por mover caixas de correio entre bancos de dados. Durante a movimentação, MRS executa uma verificação de consistência em todos os itens dentro da caixa de correio. Se for encontrado um problema de consistência, MRS irá corrigir o problema, ou ignorar os itens corrompidos, removendo assim a corrupção da caixa de correio. 

Como MRS é um componente do Exchange Online, podemos pode fazer alterações em seu código endereço novos formulários de corrupção que forem detectados no futuro. Por exemplo, se podemos detectar um problema de consistência MRS não é possível corrigir, podemos analisar a corrupção, altere o código do MRS e corrigir a inconsistência (se conseguimos compreender como). 

## <a name="log-file-checks"></a>Verificações de arquivo de log 
Todos os arquivos de log de transação gerados por um banco de dados do Exchange são submetidos a diversas formas de verificações de consistência. Quando um arquivo de log é criado, a primeira coisa concluído é um padrão de bit é gravado e, em seguida, uma série de gravações de log é executada. Isso permite que o Exchange Online executar uma série de verificações (flush perdida, CRC e outras verificações) para validar cada arquivo de log, conforme ele está escrito e outra quando ele é replicado. 

## <a name="deployment-on-resilient-file-system"></a>Implantação no sistema de arquivos resiliente 
Para ajudar a evitar corrupção ocorra no nível do sistema de arquivos, o Exchange Online está sendo implantado nas partições de sistema de arquivos resiliente (ReFS) para fornecer recursos aprimorados de recuperação. ReFS é um sistema de arquivos no Windows Server 2012 e posterior é projetado para ser mais resiliente contra corrupção de dados, maximizando assim, integridade e disponibilidade de dados. Especificamente, ReFS traz aprimoramentos da maneira que metadados é atualizado que oferece melhor proteção de dados e reduz casos de corrupção de dados. Ele também usa somas de verificação para verificar a integridade dos dados de arquivo e garantir que corrupção de dados de metadados está facilmente encontrado e reparado. 

O Exchange Online aproveita vários benefícios ReFS: 
- Mais resiliência em integridade dos dados significa menos incidentes de corrupção de dados. Redução do número de incidentes de corrupção significa menos repropagações de desnecessários do banco de dados. 
- Soma de verificação em execução em metadados habilitando detecções de casos de corrupção mais cedo e forma mais determinista, permitindo-nos corrigir os dados do cliente corrupção antes de cinza falhas nos volumes de dados.
- Projetado para funcionar bem com conjuntos de dados muito grandes — petabytes e maior — sem impacto no desempenho
- Suporte para outros recursos usados pelo Exchange Online, como criptografia de disco BitLocker. 

O Exchange Online também se beneficia de outros recursos ReFS: 
- **Integridade (fluxos de integridade)** - ReFS armazena dados de forma que protege de muitos dos erros comuns que normalmente podem causar perda de dados. Pesquisa do Office 365 usa fluxos de integridade para ajudá-lo com detecção de corrupção de disco antecipada e somas de verificação de conteúdo do arquivo. Esse recurso também reduz incidentes de corrupção causadas por "Rasgado grava" (quando uma operação de gravação não for concluída devido à falta de energia, etc.). 
- **Disponibilidade (residual)** - ReFS prioriza a disponibilidade dos dados. Historicamente, sistemas de arquivos com frequência eram suscetíveis a corrupção de dados que exigiria a ficar offline para reparo do sistema. Embora seja rara, se ocorrer corrupção, implementa ReFS resgatar, um recurso que remove os dados corrompidos do namespace em um volume ao vivo e garante que os dados bons não são afetados negativamente por dados corrompidos não pode ser reparado. Aplicando o recurso residual e isolando corrupção de dados para o Exchange Online volumes de banco de dados significam que podemos pode manter os bancos de dados não é afetado em um volume corrompido Íntegro entre o momento de ação de corrupção e reparar. Isso aumenta a disponibilidade dos bancos de dados que normalmente seriam afetados por esses problemas de corrupção do disco. 