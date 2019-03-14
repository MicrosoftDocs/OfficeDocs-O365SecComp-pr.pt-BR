---
title: Políticas de alerta no centro de conformidade &amp; de segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Criar políticas de alerta no centro de conformidade &amp; de segurança do Office 365 para monitorar possíveis ameaças, perda de dados e problemas de permissões. Em seguida, você pode exibir e gerenciar os alertas gerados quando os usuários realizam atividades que correspondam às condições de uma política de alerta.
ms.openlocfilehash: 639cd893b39505b002cbe8a72cde6f3c9f9643fa
ms.sourcegitcommit: 8b36bf7949f1769f1418d740293637d60e403f87
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30339449"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Políticas de alerta no centro de conformidade &amp; de segurança do Office 365

Você pode usar a nova política de alerta e as ferramentas de painel de alerta no &amp; centro de conformidade de segurança do Office 365 para criar políticas de alerta e, em seguida, exibir os alertas gerados quando os usuários realizam atividades que correspondem às condições de uma política de alerta. As políticas de alerta criam e expandem a funcionalidade dos alertas de atividade, permitindo que você categorize a política de alerta, aplique a política a todos os usuários em sua organização, defina um nível de limite para quando um alerta for disparado e decida se deseja ou não receber emails por. Há também uma página **exibir alertas** no centro de conformidade &amp; de segurança, onde você pode exibir e filtrar alertas, definir um status de alerta para ajudá-lo a gerenciar alertas e, em seguida, ignorar alertas após ter resolvido ou resolvido o incidente subjacente. Também expandimos o tipo de eventos para os quais você pode criar alertas. Por exemplo, você pode criar políticas de alerta para acompanhar incidentes de perda de dados e atividade de malware. Por fim, também incluímos diversas políticas de alerta padrão que ajudam a monitorar a atribuição de privilégios de administrador no Exchange Online, nos ataques de malware e em níveis incomuns de exclusões de arquivos e compartilhamento externo. 
  
> [!NOTE]
> As políticas de alerta estão disponíveis para organizações que possuem uma assinatura do Office 365 Enterprise ou do Office 365 governo dos EUA, E3/G3 ou E5/G5. No enTanto, algumas funcionalidades avançadas só estão disponíveis para organizações com uma assinatura do E5/G5 ou para organizações que possuem uma assinatura E1/G1 ou E3/G3 e uma assinatura do complemento do Office 365 Threat Intelligence ou do Office 365 Advanced Compliance. A funcionalidade que requer uma assinatura do E5/G5 ou complemento é realçada neste tópico. Observe também que as políticas de alerta estão disponíveis nos ambientes do Office 365 GCC, GCC High e DoD US governamentais.
  
## <a name="how-alert-policies-work"></a>Como funcionam as políticas de alerta

Veja aqui uma rápida visão geral de como as políticas de alerta funcionam e os alertas que são disparados quando as atividades de usuário ou de administrador correspondem às condições de uma política de alerta.
  
![Visão geral de como as políticas de alerta funcionam](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Um administrador na sua organização cria, configura e ativa uma política de alerta usando a página **políticas de alerta** no centro de conformidade do _AMP_ de segurança. Você também pode criar políticas de alerta usando o cmdlet **New-ProtectionAlert** no PowerShell. Para criar políticas de alerta, você precisa ter a função de configuração da organização ou a função Gerenciar alertas no centro de conformidade do & de segurança.
    
2. Um usuário realiza uma atividade que corresponde às condições de uma política de alerta. No caso de ataques de malware, as mensagens de email infectadas enviadas para os usuários em sua organização irão disparar um alerta.
    
3. O Office 365 gera um alerta que é exibido na página **exibir alertas** no centro de &amp; conformidade de segurança. Além disso, se as notificações por email estiverem habilitadas para a política de alerta, o Office 365 enviará uma notificação para uma lista de destinatários. Os alertas que um administrador ou outros usuários podem ver na página **exibir alertas** é determinado pelas funções atribuídas ao usuário. Para obter mais informações, consulte a seção [permissões RBAC necessárias para exibir alertas](#rbac-permissions-required-to-view-alerts) .
    
4. Um administrador gerencia alertas no centro de &amp; conformidade de segurança. O gerenciamento de alertas consiste em atribuir um status de alerta para ajudar a rastrear e gerenciar qualquer investigação.
    
## <a name="alert-policy-settings"></a>Configurações de política de alerta

Uma política de alerta consiste em um conjunto de regras e condições que definem o usuário ou a atividade de administrador que irá gerar um alerta, uma lista de usuários que irão disparar o alerta se eles executarem a atividade e o limite que define quantas vezes a atividade deve ocorrer antes de um n o alerta é disparado. Você também categoriza a política e a atribui a um nível de severidade. Essas duas configurações ajudam você a gerenciar políticas de alerta (e os alertas disparados quando as condições de política são correspondidas), pois você pode filtrar essas configurações ao gerenciar políticas e &amp; exibir alertas no centro de conformidade de segurança. Por exemplo, você pode exibir alertas que correspondam às condições da mesma categoria ou exibir alertas com o mesmo nível de severidade.
  
Para exibir e criar políticas de alerta, vá até **alertas** \> **políticas de alerta** no &amp; centro de conformidade de segurança. 
  
![No centro de &amp; Complinace de segurança, clique em alertas e, em seguida, clique em políticas de alerta para exibir e criar políticas de alerta](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Uma política de alerta consiste nas configurações e condições a seguir.
  
- **Atividade o alerta é o acompanhamento** -você cria uma política para controlar uma atividade ou, em alguns casos, algumas atividades relacionadas, como compartilhar um arquivo com um usuário externo compartilhando-o, atribuindo permissões de acesso ou criando um link anônimo. Quando um usuário realiza a atividade definida pela política, um alerta é acionado com base nas configurações de limite de alerta.
    
    > [!NOTE]
    > As atividades que você pode acompanhar dependem do plano do governo dos EUA da organização do Office 365 Enterprise ou do Office 365. Em geral, as atividades relacionadas a campanhas de malware e ataques de phishing exigem uma assinatura do E5/G5 ou uma assinatura E1/G1 ou E3/G3 com uma assinatura complementar de inteligência de ameaças. 
  
- **Condições de atividade** -para a maioria das atividades, você pode definir condições adicionais que devem ser atendidas para que um alerta seja disparado. As condições comuns incluem endereços IP (para que um alerta seja disparado quando o usuário executa a atividade em um computador com um endereço IP específico ou dentro de um intervalo de endereços IP), se um alerta é disparado se um usuário ou usuários específicos realizam essa atividade e se a atividade é executada em um nome de arquivo específico ou uma URL. Você também pode configurar uma condição que dispara um alerta quando a atividade é realizada por qualquer usuário em sua organização. Observe que as condições disponíveis dependem da atividade selecionada.
    
- **Quando o alerta é** disparado, você pode definir uma configuração que define a frequência com que uma atividade pode ocorrer antes de um alerta ser acionado. Isso permite que você configure uma política para gerar um alerta sempre que uma atividade corresponder às condições da política, quando um determinado limite for excedido ou quando a ocorrência da atividade que o alerta estiver rastreando se tornar incomum para nossa organização. 
    
    ![Configurar como os alertas são acionados, com base em quando a atividade ocorre, um limite ou atividade incomum para sua organização](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Se você selecionar a configuração com base em atividade incomum, o Office 365 estabelece um valor de linha de base que define a frequência normal para a atividade selecionada; leva até 7 dias para estabelecer essa linha de base, durante a qual os alertas não serão gerados. Depois que a linha de base é estabelecida, um alerta será disparado quando a frequência da atividade rastreada pela política de alerta exceder muito o valor da linha de base. Para atividades relacionadas à auditoria (como atividades de arquivo e pasta), você pode estabelecer uma linha de base com base em um único usuário ou com base em todos os usuários em sua organização; para atividades relacionadas a malware, você pode estabelecer uma linha de base com base em uma única família de malware, um único destinatário ou todas as mensagens em sua organização.
    
    > [!NOTE]
    > A capacidade de configurar políticas de alerta com base em um limite ou com base em atividade incomum requer uma assinatura do E5/G5 ou uma assinatura E1/G1 ou E3/G3 com uma assinatura de inteligência de ameaças ou de um complemento avançado de conformidade. As organizações com uma assinatura E1/G1 e E3/G3 só podem criar uma política de alerta onde um alerta é acionado toda vez que uma atividade ocorre. 
  
- **Categoria de alerta** – para ajudar no controle e gerenciamento dos alertas gerados por uma política, você pode atribuir uma das seguintes categorias a uma política.
    
  - Governança de dados
    
  - Prevenção contra perda de dados

  - Fluxo de mensagens
    
  - Permissões
    
  - Gerenciamento de ameaças
    
  - Outros
    
  Quando ocorre uma atividade que corresponde às condições da política de alerta, o alerta gerado é marcado com a categoria definida nesta configuração. Isso permite que você rastreie e gerencie alertas que tenham a mesma configuração de categoria na página **exibir alertas** no centro de conformidade do _AMP_ de segurança, pois é possível classificar e filtrar alertas com base na categoria. 
    
- **Severidade de alerta** -semelhante à categoria de alerta, você atribui um atributo de gravidade ( **baixo**, **médio**ou **alto**) a políticas de alerta. Como a categoria de alerta, quando ocorre uma atividade que corresponde às condições da política de alerta, o alerta gerado é marcado com o mesmo nível de gravidade definido para a política de alerta. Novamente, isso permite que você rastreie e gerencie alertas com a mesma configuração de gravidade na página **exibir alertas** . Por exemplo, você pode filtrar a lista de alertas para que apenas os alertas com uma severidade **alta** sejam exibidos. 
    
    > [!TIP]
    > Ao configurar uma política de alerta, considere atribuir uma severidade maior a atividades que podem resultar em conseqüências severamente negativas, como a detecção de malware após a entrega aos usuários, a exibição de dados confidenciais ou classificados, o compartilhamento de dados com usuários externos, ou outras atividades que podem resultar em perda de dados ou ameaças à segurança. Isso pode ajudar você a priorizar alertas e as ações tomadas para investigar e resolver as causas subjacentes. 
  
- **Notificações por email** -você pode configurar a política para que as notificações por email sejam enviadas (ou não enviadas) para uma lista de usuários quando um alerta é acionado. Você também pode definir um limite de notificação diária para que, depois que o número máximo de notificações tiver sido atingido, nenhuma notificação será enviada para o alerta durante esse dia. Adicionalmente às notificações por email, você ou outros administradores podem exibir os alertas que são disparados por uma política na página **exibir alertas** . Considere habilitar notificações por email para políticas de alerta de uma categoria específica ou que tenham uma configuração de severidade mais alta. 
  
## <a name="default-alert-policies"></a>Políticas de alerta padrão

O Office 365 fornece políticas de alerta internas que ajudam a identificar as permissões de administração do Exchange abuso, atividade de malware e riscos de governança de dados. Na página **políticas de alerta** , o nome dessas políticas internas está em negrito e o tipo de política é definido como **sistema**. Essas políticas são ativadas por padrão. Você pode desativar essas políticas (ou voltar novamente), configurar uma lista de destinatários para enviar notificações por email e definir um limite diário de notificação. As outras configurações dessas políticas não podem ser editadas.
  
A tabela a seguir lista e descreve as políticas de alerta padrão disponíveis e a categoria à qual cada política é atribuída. Observe que essa categoria é usada para determinar quais alertas um usuário pode exibir na página exibir alertas. Para obter mais informações, consulte a seção [permissões RBAC necessárias para exibir alertas](#rbac-permissions-required-to-view-alerts) .  

A tabela também indica os planos do governo dos EUA do Office 365 Enterprise e do Office 365 necessários para cada um. Observe que algumas políticas de alerta padrão estão disponíveis se sua organização tem a assinatura complementar apropriada, além de uma assinatura E1/G1 ou E3/G3. 
  
|**Política de alerta padrão**|**Descrição**|**Category**|**Assinatura do Office 365 Enterprise**|
|:-----|:-----|:-----|:-----|
|**Criação de regra de encaminhamento/redirecionamento** <br/> |Gera um alerta quando alguém em sua organização cria uma regra de caixa de entrada para a caixa de correio que encaminha ou redireciona mensagens para outra conta de email. Esta política controla apenas as regras de caixa de entrada que são criadas usando o Outlook na Web (anteriormente conhecido como Outlook Web App) ou o PowerShell do Exchange Online. Essa política tem uma configuração de **baixa** gravidade. Para obter mais informações sobre como usar regras de caixa de entrada para encaminhar e redirecionar emails no Outlook na Web, confira [usar regras no Outlook na Web para encaminhar automaticamente as mensagens para outra conta](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).  <br/> |Gerenciamento de ameaças <br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**pesquisa de descoberta eletrônica iniciada ou exportada** <br/> |Gera um alerta quando alguém usa a ferramenta de pesquisa de conteúdo no centro de conformidade do & de segurança. Um alerta é disparado quando as seguintes atividades de pesquisa de conteúdo são executadas: <br/><br/>• Uma pesquisa de conteúdo foi iniciada<br/>• Os resultados de uma pesquisa de conteúdo são exportados<br/>• Um relatório de pesquisa de conteúdo é exportado<br/><br/>Os alertas também são acionada quando as atividades de pesquisa de conteúdo anteriores são realizadas em associação a uma ocorrência de descoberta eletrônica. Essa política tem uma configuração de severidade **média** . Para obter mais informações sobre as atividades de pesquisa de conteúdo, consulte [Search for eDiscovery Activities no log de auditoria do Office 365](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities). <br/> |Gerenciamento de ameaças<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Elevação do privilégio de administrador do Exchange** <br/> |Gera um alerta quando alguém recebe permissões administrativas na sua organização do Exchange Online; por exemplo, se um usuário é adicionado ao grupo de função gerenciamento da organização no Exchange Online. Essa política tem uma configuração de **baixa** gravidade.  <br/> |Permissões <br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**As mensagens foram atrasadas** <br/> |Gera um alerta quando o Office 365 não consegue enviar mensagens de email para sua organização local ou para servidores parceiros usando um conector. Quando isso acontecer, a mensagem será enfileirada no Office 365. Este alerta é disparado quando há 2.000 mensagens ou mais que foram enfileiradas por mais de uma hora. Essa política tem uma configuração de **alta** gravidade.  <br/> |Fluxo de mensagens<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Campanha de malware detectada após a entrega** <br/> |Gera um alerta quando um número excepcionalmente grande de mensagens contendo malware é entregue às caixas de correio em sua organização. Se esse evento ocorrer, o Office 365 removerá as mensagens infectadas das caixas de correio do Exchange Online. Essa política tem uma configuração de **alta** gravidade.  <br/> |Gerenciamento de ameaças<br/> |Licença complementar de inteligência de ameaças do Office 365 ou E5/G5  <br/> |
|**Campanha de malware detectada e bloqueada** <br/> |Gera um alerta quando alguém tentava enviar um número excepcionalmente grande de mensagens de email contendo um determinado tipo de malware para os usuários em sua organização. Se esse evento ocorrer, as mensagens infectadas serão bloqueadas pelo Office 365 e não serão entregues às caixas de correio. Essa política tem uma configuração de **baixa** gravidade.  <br/> |Gerenciamento de ameaças<br/> |Licença complementar de inteligência de ameaças do Office 365 ou E5/G5  <br/> |
|**Campanha de malware detectada no SharePoint e no OneDrive** <br/> |Gera um alerta quando um volume excepcionalmente alto de malware ou vírus é detectado em arquivos localizados em sites do SharePoint ou em contas do OneDrive em sua organização. Essa política tem uma configuração de **alta** gravidade.  <br/> |Gerenciamento de ameaças<br/> |Licença complementar de inteligência de ameaças do Office 365 ou E5/G5  <br/> |
|**Atividade de arquivo de usuário externo incomum** <br/> |Gera um alerta quando um grande número de atividades geralmente é executado em arquivos no SharePoint ou no OneDrive por usuários fora da sua organização. Isso inclui atividades como acessar arquivos, baixar arquivos e excluir arquivos. Essa política tem uma configuração de **alta** gravidade.  <br/> |Governança de dados<br/> |E5/G5 ou o Office 365 Threat Intelligence ou a assinatura de complemento de conformidade avançada  <br/> |
|**Volume incomum de compartilhamento de arquivos externos** <br/> |Gera um alerta quando um número muito grande de arquivos no SharePoint ou no OneDrive são compartilhados com usuários fora da sua organização. Essa política tem uma configuração de severidade **média** .  <br/> |Governança de dados<br/> |E5/G5 ou o Office 365 Threat Intelligence ou a assinatura de complemento de conformidade avançada  <br/> |
|**Volume incomum de exclusão de arquivo** <br/> |Gera um alerta quando um número excepcionalmente grande de arquivos é excluído no SharePoint ou no OneDrive dentro de um curto período de tempo. Essa política tem uma configuração de severidade **média** .  <br/> |Governança de dados <br/> |E5/G5 ou o Office 365 Threat Intelligence ou a assinatura de complemento de conformidade avançada  <br/> |
|**Aumento incomum no email relatado como phishing** <br/> |Gera um alerta quando há um aumento significativo no número de pessoas em sua organização usando o suplemento de mensagem de relatório no Outlook para relatar mensagens como email de phishing. Essa política tem uma configuração de **alta** gravidade. Para obter mais informações sobre esse suplemento, confira [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).  <br/> |Gerenciamento de ameaças<br/> |Licença complementar de inteligência de ameaças do Office 365 ou E5/G5  <br/> |
|**Usuário impedido de enviar email** <br/> |Gera um alerta quando alguém em sua organização não tem permissão para enviar emails de saída. Isso geralmente ocorre quando uma conta é comprometida e o usuário é listado na página **usuários restritos** no centro de conformidade do _AMP_ de segurança. (Para acessar essa página, vá para **Gerenciamento de ameaça > revisar _GT_ usuários restritos**). Essa política tem uma configuração de **alta** gravidade. Para obter mais informações sobre usuários restritos, consulte [removendo um usuário, domínio ou endereço IP de uma lista de bloqueios após o envio de email de spam](https://docs.microsoft.com/office365/securitycompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email).  <br/> |Gerenciamento de ameaças<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|||||
   
Observe que a atividade incomum monitorada por algumas das políticas internas é baseada no mesmo processo da configuração de limite de alerta descrita anteriormente. O Office 365 estabelece um valor de linha de base que define a frequência normal da atividade "normal". Os alertas são disparados quando a frequência das atividades rastreadas pela política de alerta interna excede muito o valor da linha de base.
 
## <a name="viewing-alerts"></a>Exibir alertas

Quando uma atividade realizada pelos usuários em sua organização corresponde às configurações de uma política de alerta, um alerta é gerado e exibido na página **exibir alertas** no centro de &amp; conformidade de segurança. Dependendo das configurações de uma política de alerta, uma notificação por email também é enviada para uma lista de usuários especificados quando um alerta é disparado. Para cada alerta, o painel na página **exibir alertas** exibe o nome da política de alerta correspondente, a severidade e a categoria do alerta (definido na política de alerta) e o número de vezes que uma atividade ocorreu, que resultou no alerta ser gerado Esse valor é baseado na configuração de limite da política de alerta. O painel também mostra o status de cada alerta. Consulte a seção [Managing Alerts](#managing-alerts) para obter mais informações sobre como usar a propriedade status para gerenciar alertas. 
  
Para exibir alertas, vá para **alertas** \> **exibir alertas** no centro de &amp; conformidade de segurança. 
  
![No centro de &amp; Complinace de segurança, clique em alertas e em exibir alertas para exibir alertas](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Você pode usar os filtros a seguir para exibir um subconjunto de todos os alertas da página **exibir alertas** . 
  
- **Status** -Use este filtro para mostrar os alertas atribuídos a um status específico; o status padrão é **ativo**. Você ou outros administradores podem alterar o valor de status.
    
- **Política** – Use este filtro para mostrar os alertas que correspondem à configuração de uma ou mais políticas de alerta. Ou você pode simplesmente exibir todos os alertas para todas as políticas de alerta.
    
- **Intervalo de tempo** – Use este filtro para mostrar os alertas que foram gerados dentro de um intervalo de data e hora específico.
    
- **Severity** -Use este filtro para mostrar os alertas atribuídos a uma severidade específica.
    
- **Categoria** – Use este filtro para mostrar alertas de uma ou mais categorias de alerta.

- **Source** – Use este filtro para mostrar os alertas acionados pelas políticas de alerta no centro de conformidade do _AMP_ de segurança ou alertas disparados pelas políticas de segurança do aplicativo Cloud do Office 365 ou ambos. Para obter mais informações sobre os alertas do Office 365 Cloud app Security, consulte a seção exibindo os [alertas de segurança do Cloud app](#viewing-cloud-app-security-alerts) .

## <a name="rbac-permissions-required-to-view-alerts"></a>Permissões de RBAC necessárias para exibir alertas

> [!NOTE]
> A funcionalidade descrita nesta seção será implantada nas organizações que começam em 20 de fevereiro de 2019 e será concluída no mundo todo até o final de 2019 de março.

As permissões de controle de acesso de base de função (RBAC) atribuídas aos usuários em sua organização determinam quais alertas um usuário pode ver na página **exibir alertas** . Como isso é feito? As funções de gerenciamento atribuídas aos usuários (com base em sua associação em grupos de função no centro de conformidade do & de segurança) determinam quais categorias de alerta um usuário pode ver na página **exibir alertas** . Estes são alguns exemplos:

- Os membros do grupo de função gerenciamento de registros podem exibir apenas os alertas gerados por políticas de alerta atribuídas à categoria de **governança de dados** .

- Os membros do grupo de função Administrador de conformidade não podem exibir alertas gerados por políticas de alerta atribuídas à categoria **Gerenciamento de ameaças** . 

- Os membros do grupo de função Gerenciador de descoberta eletrônica não podem exibir nenhum alerta porque nenhuma das funções atribuídas fornece permissão para exibir alertas de qualquer categoria de alerta.

Esse design (baseado nas permissões RBAC) permite que você determine quais alertas podem ser exibidos (e gerenciados) por usuários em funções de trabalho específicas em sua organização. 

A tabela a seguir lista as funções necessárias para exibir alertas das 6 categorias de alerta diferentes. A primeira coluna nas tabelas lista todas as funções no centro de conformidade do & de segurança.  Uma marca de seleção indica que um usuário atribuído a essa função pode exibir alertas da categoria de alerta correspondente listada na linha superior.

Para ver a qual categoria uma política de alerta padrão é atribuída, confira a tabela na seção [políticas de alerta padrão](#default-alert-policies) .

|<br/>|Governança de dados|Prevenção contra perda de dados|Fluxo de mensagens|Permissões|Gerenciamento de ameaças|Outros | 
|:---------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|Logs de auditoria <br/> |         ||         |         |         |         |
|Gerenciamento de casos <br/>|         |         |         |         |         |         |
|Administrador de Conformidade<br/>|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Pesquisa de conformidade<br/>|         |         |         |         |         |         |
|Gerenciamento de dispositivos<br/>|         |         |         |         |         |         |
|Gerenciamento de descarte<br/>|         |         |         |         |         |         |
|Gerenciamento de conformidade de DLP<br/>|         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Exportar<br/>|         |         |         |         |         |         |
|Retenção<br/>|         |         |         |         |         |         |
|Gerenciar Alertas<br/>|         |         |         |         |         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Configuração da organização|         |         |         |         |         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Visualização <br/>|         |         |         |         |         |         |
|Gerenciamento de registros <br/>|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gerenciamento de retenção <br/>| ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Examinar <br/>|         |         |         |         |         |         |
|DesCriptografia do RMS<br/>|         |         |         |         |         |         |
|Gerenciamento de função<br/>|         |         |         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |
|Pesquisa e limpeza<br/>|         |         |         |         |         |         |
|Administrador de segurança<br/>||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Leitor de segurança<br/>|         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)
|Exibição da garantia de serviço<br/>|         |         |         |         |         |         |
|Administrador de análise de supervisão<br/>|         |         |         |         |         |         |
|Logs de auditoria somente para exibição<br/>|         |         |         |         |         |         |
|Gerenciamento de dispositivos somente exibição<br/>|         |         |         |         |         |         |
|Somente exibição Gerenciamento de conformidade DLP<br/>|         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Somente exibição Gerenciar alertas<br/>|         |         |         |         |         |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Destinatários Somente para Exibição<br/>|         |         |  ![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         ||         |
|Gerenciamento de registros somente de exibição<br/>|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gerenciamento de retenção somente para exibição<br/>|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|         |         |         |         |         |         |

**Dica:** Para exibir as funções atribuídas a cada um dos grupos de função padrão, execute os seguintes comandos no Security & Compliance Center PowerShell: 

```
$RoleGroups = Get-RoleGroup

$RoleGroups | foreach {Write-Output -InputObject `r`n,$_.Name,"-----------------------"; Get-RoleGroup $_.Identity | Select-Object -ExpandProperty Roles}
```
Você também pode exibir as funções atribuídas a um grupo de função no centro de conformidade do & de segurança. Vá até a página **permissões** e clique em um grupo de funções. As funções atribuídas estão listadas na página do menu de atalho.


## <a name="managing-alerts"></a>Gerenciar alertas

Após os alertas terem sido gerados e exibidos na página **exibir alertas** no centro de &amp; conformidade de segurança, você pode fazer a triagem, investigar e resolvê-los. Veja algumas tarefas que você pode executar para gerenciar alertas. 
  
- **Atribuir um status a alertas** -você pode atribuir um dos seguintes status a alertas: **ativo** (o valor padrão), investigando ****, **resolvido**ou **Descartado**. Em seguida, você pode filtrar essa configuração para exibir alertas com a mesma configuração de status. Essa configuração de status pode ajudar a acompanhar o processo de gerenciamento de alertas.
    
- **Exibir detalhes de alerta** -você pode clicar em um alerta para exibir uma página de submenu com detalhes sobre o alerta. As informações detalhadas dependem da política de alerta correspondente, mas normalmente incluem o seguinte: nome da operação real que disparou o alerta (como um cmdlet), uma descrição da atividade que disparou o alerta, o usuário (ou a lista de usuários) Quem disparou o alerta e o nome (e o link para) da política de alerta correspondente.
    
  - O nome da operação real que disparou o alerta, como um cmdlet ou uma operação de log de auditoria.
    
  - Uma descrição da atividade que disparou o alerta.
    
  - O usuário que disparou o alerta; Isso é incluído apenas para políticas de alerta que são configuradas para controlar um único usuário ou uma única atividade.
    
  - O número de vezes que a atividade rastreada pelo alerta foi executada. Observe que esse número pode não coincidir com o número real de alertas relacionados listados na página exibir alertas, pois os alertas adicionais podem ter sido disparados.
    
  - Um link para uma lista de atividades que inclui um item para cada atividade que foi executada que disparou o alerta. Cada entrada dessa lista identifica quando a atividade ocorreu, o nome da operação real (como "fileDeleted") e o usuário que realizou a atividade, o objeto (como um arquivo, uma ocorrência de descoberta eletrônica ou uma caixa de correio) em que a atividade foi executada e o IP Endereço do computador do usuário. Para alertas relacionados a malware, esses links para uma lista de mensagens.
    
  - O nome (e o link para) da política de alerta correspondente.
    
- **Suprimir notificações por email** -você pode desativar (ou suprimir) notificações por email da página de submenu de um alerta. Quando você suprimir notificações por email, o Office 365 não enviará notificações quando atividades ou eventos que corresponderem às condições da política de alerta. No enTanto, os alertas continuarão a ser acionados quando as atividades realizadas por usuários corresponderem às condições da política de alerta. Você também pode desativar as notificações por email editando a política de alerta.
    
- **Resolver alertas** -é possível marcar um alerta como resolvido na página de menu de um alerta (que define o status do alerta como **resolvido**). A menos que você altere o filtro, os alertas resolvidos não são exibidos na página **exibir alertas** . 
    
## <a name="viewing-cloud-app-security-alerts"></a>Exibindo alertas do Cloud app Security
  
Os alertas que são acionados pelas políticas de segurança do aplicativo Cloud do Office 365 agora são exibidos na página **exibir alertas** no centro de conformidade do _AMP_ de segurança. Isso inclui alertas disparados por políticas de atividade e alertas disparados por políticas de detecção de anomalias no Office 365 Cloud app Security. Isso significa que você pode exibir todos os alertas no centro de conformidade do & de segurança. Observe que a segurança do aplicativo de nuvem do Office 365 só está disponível para organizações com uma assinatura do Office 365 Enterprise E5 ou do Office 365 US governos do governo dos EUA. Para obter mais informações, consulte [Overview of Office 365 Cloud app Security](office-365-cas-overview.md).

Além disso, as organizações que têm o Microsoft Cloud app Security como parte de uma assinatura do Enterprise Mobility + Security E5 ou como um serviço autônomo também podem exibir os alertas de segurança do aplicativo na nuvem que estão relacionados aos aplicativos e serviços do Office 365 no & de segurança Centro de conformidade.

Para exibir apenas os alertas do Cloud app Security no centro de conformidade do & de segurança, use o filtro de **origem** e selecione **Cloud app Security**.

![Usar o filtro de origem para exibir somente os alertas de segurança do aplicativo na nuvem](media/FilterCASAlerts.png)

Semelhante a um alerta disparado por uma política de alerta do centro de conformidade do & de segurança, você pode clicar em um alerta de segurança do Cloud app para exibir uma página de submenu com detalhes sobre o alerta. O alerta inclui um link para exibir os detalhes e gerenciar o alerta no portal do Cloud app Security e um link para a política de segurança de aplicativo na nuvem correspondente que disparou o alerta. Consulte [revisar e executar ação em alertas no Office 365 Cloud app Security](review-office-365-cas-alerts.md).

![Detalhes do alerta contêm links para o portal do Cloud app Security](media/CASAlertDetail.png)

> [!IMPORTANT]
> Alterar o status de um alerta do Cloud app Security no centro de conformidade do & de segurança não atualizará o status de resolução para o mesmo alerta no portal do Cloud app Security. Por exemplo, se você marcar o status do alerta como **resolvido** no centro de conformidade do _AMP_ de segurança, o status do alerta no portal de segurança do aplicativo na nuvem não será alterado. Para resolver ou descartar um alerta de segurança do aplicativo na nuvem, gerencie o alerta no portal do Cloud app Security.
