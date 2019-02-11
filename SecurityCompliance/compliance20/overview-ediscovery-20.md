---
title: Visão geral do eDiscovery avançado (Preview) no Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo descreve a nova versão do eDiscovery avançado (Preview) no Microsoft 365.
ms.openlocfilehash: cb82541037983ca21cefbefb7f72fffa3b054373
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706152"
---
# <a name="overview-of-advanced-ediscovery-preview-in-microsoft-365"></a>Visão geral do eDiscovery avançado (Preview) no Microsoft 365

Microsoft lançou apenas uma versão de visualização da ferramenta atualizadas avançadas de eDiscovery que aproveita os recursos de descoberta eletrônica existente no Office 365. Esta versão de demonstração, chamada *eDiscovery avançado (Preview)*, fornece um fluxo de trabalho de ponta a ponta para preservar, coletar, revisar, analisar e exportar conteúdo que responde às investigações internos e externos de sua organização. 

## <a name="alignment-with-edrm"></a>Alinhamento com EDRM

O fluxo de trabalho interno de eDiscovery avançado (Preview) se alinha com o processo de descoberta eletrônica descrito pelo Electronic Discovery Reference Model (EDRM). 

![O modelo de referência de descoberta eletrônica (EDRM)](../media/EDRMv1.png)

(Origem da imagem cortesia edrm.net. A imagem de origem foi disponibilizada sob criativo comuns atribuição 3.0 Unported licença.)

Em um alto nível, o eDiscovery de aqui está como avançado (Preview) suporta o fluxo de trabalho EDRM:

- **Identificação** - depois de identificar potenciais pessoas de interesse em uma investigação, você poderá adicioná-los como responsáveis (também chamados *responsáveis de dados*, porque talvez possuem informações relevantes à investigação) para um avançado caso de descoberta eletrônica (Preview). Depois que os usuários são adicionados como responsáveis, é fácil preservar, coletar e examine os documentos dos responsáveis.

- **Preservação** - preservar e proteger dados que são relevantes para uma investigação, Avançado permite que o eDiscovery (Preview) você realiza uma retenção legal em fontes de dados que estão associadas as responsáveis em um caso. Você também pode colocar dados não-custódia em espera. Além disso, o eDiscovery avançado (Preview) tem um fluxo de trabalho de comunicações internas para poder enviar notificações de uma retenção legal aos responsáveis e controlar seus confirmações.

- **Coleção** - depois que você identificou (e preservadas) as fontes de dados relevantes à investigação, você pode usar a ferramenta de pesquisa internas no procurar eDiscovery avançado (Preview) e coletar dados ao vivo de fontes de dados custódia (e não custódia fontes de dados, se aplicável) que podem ser relevantes ao caso.

- **Processamento** - após você coletou todos os dados relevantes para o caso, a próxima etapa é processá-lo para análise e revisão posterior. No eDiscovery avançado (Preview), isso significa que os dados no local que você identificou na fase de conjunto são copiados para o local de armazenamento do Azure (chamado de um *conjunto de trabalho*), que proporciona uma exibição estática dos dados maiusculas. 
 
- Conjunto de **revisão** - depois dados tem sido adicionados a um trabalho, você pode exibir documentos específicos e executar consultas adicionais para  
 
- **Análise** - avançadas de descoberta eletrônica (Preview) fornece ferramentas de análise integrada ajudá-lo a analisar os dados do conjunto de trabalho que você determinar não forem relevantes à investigação. Além de reduzir o volume de dados relevantes, eDiscovery antecipada (Preview) também ajuda a reduzir custos de revisão legal, permitindo que você organizar conteúdo para tornar o processo de revisão mais fácil e eficiente.

- **Produção** e **apresentação** - quando você estiver pronto, você pode exportar documentos de um conjunto de trabalho para revisão legal. Você pode exportar documentos no formato nativo ou em um formato EDRM especificados para que eles podem ser importados para aplicativos de terceiros revisão.

## <a name="advanced-ediscovery-preview-workflow"></a>Fluxo de trabalho do eDiscovery avançado (Preview)

As seções a seguir descrevem cada etapa do fluxo de trabalho internas no eDiscovery avançado (Preview). A captura de tela a seguir mostra na guia **página inicial** de um caso denominado *2019002 de responsabilidade do produto*. Observe que as guias de fluxo de trabalho na parte superior da página são sequenciadas para alinhar com o processo EDRM. 

Para obter mais informações sobre o fluxo de trabalho de ponta a ponta no eDiscovery avançado (Preview), consulte este [Microsoft mecânica vídeo](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Guias no eDiscovery avançado (Preview) siga o fluxo de trabalho EDRM](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Gerenciando responsáveis

Use a guia **responsáveis** para adicionar e gerenciar as pessoas que você identificou como pessoas de interesse no caso. Quando você adiciona responsáveis, você pode executar rapidamente as ações relacionadas a dos responsáveis como colocar um legal como fontes de dados dos responsáveis, como sua caixa de correio e a conta do OneDrive, responsáveis se comunicando e fontes de dados dos responsáveis para coletar o conteúdo de pesquisa que é relevante para o caso. Como o andamento de caso, é fácil adicionar novos responsáveis ou liberar responsáveis de caso. Para obter mais informações, consulte [trabalhar com responsáveis no eDiscovery avançado (Preview)](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Gerenciar notificações de retenção legal

Use a guia de **comunicações** para gerenciar o processo de comunicação com os responsáveis no caso. Um aviso de isenção legal instrui responsáveis para preservar qualquer conteúdo que pode ser relevante ao caso. As equipes jurídicas devem ser capazes de controlar que avisos foram recebidos, leia e reconhecidos pelo responsáveis. O fluxo de trabalho do communications no eDiscovery avançado (Preview) permite que você criar e enviar notificações iniciais, lembretes, avisos de lançamento e escalonamentos se responsáveis apresentar falha ao confirmar uma notificação de espera. Para obter mais informações, consulte [trabalhar com a comunicação no eDiscovery avançado (Preview)](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Gerenciando preservação de conteúdo

Quando você adiciona um funcionário encarregado a um caso, você tem a opção para fazer uma pausa nos dados custódia. Use a guia **contém** para gerenciar a retenção criada quando você adiciona responsáveis e gerenciar legais adicionais retém associada com o caso; Por exemplo, você pode identificar e fazer uma pausa em fontes de dados não-custódia. Você também pode editar qualquer espera no caso e torná-lo uma isenção baseado em consulta para que somente o conteúdo que corresponde à consulta é colocado em espera; Por exemplo, você pode adicionar um intervalo de datas à isenção para que somente o conteúdo que foi criado em uma data específica variou no preservadas. Você também pode obter estatísticas sobre o conteúdo que estiver em espera, remover a retenção após quando ele não está mais relevante para o caso ou excluí-lo. Para obter mais informações, consulte [gerenciar retenções no eDiscovery avançado (Preview)](managing-holds.md).

## <a name="indexing-custodian-data"></a>A indexação de dados dos responsáveis

Quando você adiciona dos responsáveis e as fontes de dados de custódia correspondente a um caso, qualquer item parcialmente indexado de uma fonte de dados dos responsáveis novamente é indexada (por um processo chamado *indexação avançada*). Isso permite que o conteúdo custódia como imagens, tipos de arquivo incompatíveis e outro conteúdo potencialmente não indexado para ser totalmente pesquisável quando você executa pesquisas para coletar dados relevantes ao caso. Use a guia de **processamento** para monitorar o status da indexação avançada e correção de processamento de erros (usando um calle do processo *correção de erro*). Para obter mais informações, consulte a [corrigir erros de processamento no eDiscovery avançado (Preview)](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Coleta de dados de maiusculas

Use a guia de **pesquisas** para criar pesquisas para pesquisar o in-loco custódia e fontes de dados não-custódia no Office 365 para conteúdo relevante ao caso. Você pode criar e executar pesquisas baseado em consulta (usando palavras-chave e condições) para identificar um mensagens de email do conjunto e documentos que são relevantes para o caso e o que você quer mais revisão e analisar nas etapas posteriores do fluxo de trabalho de descoberta eletrônica. Você pode criar uma ou mais pesquisas associadas à ocorrência. Além disso, você pode usar a ferramenta de pesquisa para visualizar documentos de amostra e exibir as estatísticas de pesquisa que podem ser úteis refinar e aprimorar os resultados da pesquisa. Quando você estiver satisfeito que os resultados da pesquisa contêm os todos os dados relevantes para o caso, se você adicionar os resultados da pesquisa a um conjunto de trabalho para revisão posterior, análise e se necessário, remoção. Para obter mais informações, consulte a [coletar dados para um caso de eDiscovery avançado (Preview)](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>Revisar e analisando dados maiusculas

Use a guia **conjuntos de trabalho** ou revisar e analisar o conteúdo que você tiver coletadas do sistema ao vivo e adicionado a um conjunto de trabalho. Um *conjunto de trabalho* é uma coleção estática (em outras palavras, uma cópia offline do dat) de dados custódia (e, se aplicável, dados não-custódia) que você coletou na fase anterior do fluxo de trabalho de descoberta eletrônica. Quando você adiciona os resultados da pesquisa para um conjunto de trabalho, um processo é disparado extrai arquivos de contêineres, que extrai metadados e extrai o texto. Quando este processo estiver concluído, o sistema cria um novo índice de todos os dados coletados dos responsáveis e adicionado ao conjunto de trabalho. Depois que os dados são adicionados ao conjunto de trabalho, você pode executar consultas adicionais para restringir os dados de maiusculas, exibir dados como texto ou em formato de arquivo nativo e anotar, redigir e defina de marcar documentos no trabalho. Além disso, você pode executar análises avançadas como identificar a duplicação de documento, envie um email threading e temas. Depois que você tiver removido os dados apenas o que é relevante para o caso, você pode baixar o download de documentos diretamente ou exportá-los junto com quaisquer marcas, anotações e metadados do arquivo. Para obter mais informações, consulte:

  - [Revisar dados de maiusculas no eDiscovery avançado (Preview)](reviewing-data-in-working-set.md)
  - [Analisar dados em um conjunto de trabalho no eDiscovery avançado (Preview)](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportando dados para revisão e apresentação

Depois de exportar os dados de um conjunto de trabalho, use a guia de **exportações** para gerenciar um trabalho de exportação e download de dados de um conjunto de trabalho. Ao exportar um conjunto de trabalho, os dados foi carregados em um local de armazenamento do Azure e, em seguida, está disponíveis para download em um computador local. Você pode obter o local e o armazenamento avaliar chave necessária para baixar os dados exportados na guia **exportações** . Para obter mais informações, consulte [Exportar dados de maiusculas no eDiscovery avançado (Preview)](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Gerenciando trabalhos

Use a guia **trabalhos** para monitorar os processos de longa execução de tarefas relacionadas ao caso que você tiver iniciado, pesquisas como reindexação, pesquisas e exportações. Por exemplo, você pode criar uma nova pesquisa na guia **pesquisas** que inclui um grande número de fontes de dados. O status desse processo de pesquisa é exibido na guia **Jobs** . Para obter mais informações, consulte [Manage jobs no eDiscovery avançado (Preview)](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Definindo configurações de maiusculas

Use a guia **configurações** para definir as configurações de todo o caso. Isso inclui adicionando membros a um caso de fechamento ou excluindo um caso e configurando o comportamento de pesquisa e análise. Para obter mais informações, consulte [Configure settings de maiusculas no eDiscovery avançado (Preview)](configuring-case-settings-ediscovery20.md).

