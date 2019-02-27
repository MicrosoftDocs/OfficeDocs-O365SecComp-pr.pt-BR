---
title: Visão geral da descoberta eletrônica avançada (visualização) no Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo descreve a nova versão da descoberta eletrônica avançada (prévia) no Microsoft 365.
ms.openlocfilehash: e2d89c2b8499c8818bececc4414182a6db689fb6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297014"
---
# <a name="overview-of-advanced-ediscovery-preview-in-microsoft-365"></a>Visão geral da descoberta eletrônica avançada (visualização) no Microsoft 365

A Microsoft acabou de lançar uma versão de visualização da ferramenta de descoberta eletrônica avançada atualizada que se baseia nos recursos de descoberta eletrônica existentes no Office 365. Esta versão prévia, chamada de *descoberta eletrônica avançada (visualização)*, fornece um fluxo de trabalho de ponta a ponta para preservar, coletar, analisar, analisar e exportar conteúdo que responde às investigações internas e externas da sua organização. 

## <a name="alignment-with-edrm"></a>Alinhamento com EDRM

O fluxo de trabalho interno da descoberta eletrônica avançada (visualização) se alinha com o processo de descoberta eletrônica descrito pelo modelo de referência de descoberta eletrônica (EDRM). 

![O modelo de referência de descoberta eletrônica (EDRM)](../media/EDRMv1.png)

(Imagem de origem cortesia de edrm.net. A imagem de origem foi disponibilizada sob a licença do Creative Commons 3,0 Unported License.)

Em um nível alto, veja como a descoberta eletrônica avançada (visualização) oferece suporte ao fluxo de trabalho do EDRM:

- **Identificação** – depois de identificar as possíveis pessoas de interesse em uma investigação, você pode adicioná-las como responsáveis (também chamados de *responsáveis por dados*, porque eles podem ter informações relevantes para a investigação) a um avançado caso de descoberta eletrônica (visualização). Depois que os usuários são adicionados como responsáveis, é fácil preservar, coletar e revisar documentos de responsáveis.

- **Preservação** -para preservar e proteger os dados relevantes para uma investigação, a descoberta eletrônica avançada (visualização) permite que você coloque um controle legal nas fontes de dados associadas aos responsáveis em um caso. Você também pode colocar dados não custodial em espera. Além disso, a descoberta eletrônica avançada (prévia) tem um fluxo de trabalho de comunicações interno para que você possa enviar notificações de retenção legal para os responsáveis e controlar suas confirmações.

- **Coleção** – depois de identificar (e preservar) as fontes de dados relevantes para a investigação, você pode usar a ferramenta de pesquisa interna na descoberta eletrônica avançada (visualização) pesquisa e coletar dados ao vivo das fontes de dados do custodial (e não do custodial fontes de dados, se aplicável, que podem ser relevantes para o caso.

- **Processamento** – após coletar todos os dados relevantes para o caso, a próxima etapa é processá-lo para revisão e análise mais detalhada. Na descoberta eletrônica avançada (visualização), isso significa que os dados no local que você identificou na fase de coleta são copiados para o local de armazenamento do Azure (chamado de *conjunto de trabalho*), que fornece a você uma exibição estática dos dados de caso. 
 
- **** Revisar-depois que os dados forem adicionados a um conjunto de trabalho, você poderá exibir documentos específicos e executar consultas adicionais para  
 
- **Análise** -descoberta eletrônica avançada (visualização) fornece ferramentas de análise integradas que ajudam a analisar os dados do conjunto de trabalho que você determina não é relevante para a investigação. Além de reduzir o volume de dados relevantes, a descoberta eletrônica avançada (visualização) também ajuda você a salvar custos de análise jurídica, permitindo que você organize o conteúdo para tornar o processo de revisão mais fácil e eficiente.

- **Produção** e **apresentação** -quando você estiver pronto, você pode exportar documentos de um conjunto de trabalho para análise jurídica. Você pode exportar documentos em seu formato nativo ou em um formato especificado pelo EDRM para que eles possam ser importados para aplicativos de revisão de terceiros.

## <a name="advanced-ediscovery-preview-workflow"></a>Fluxo de trabalho de descoberta eletrônica avançada (prévia)

As seções a seguir descrevem cada etapa no fluxo de trabalho interno da descoberta eletrônica avançada (visualização). A captura de tela a seguir mostra a guia **página inicial** de uma ocorrência chamada *responsabilidade do produto 2019002*. Observação as guias de fluxo de trabalho na parte superior da página são sequenciadas para alinhar-se com o processo EDRM. 

Para obter mais informações sobre o fluxo de trabalho de ponta a ponta na descoberta eletrônica avançada (visualização), consulte este [vídeo da Microsoft mecânica](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Guias na descoberta eletrônica avançada (visualização) seguem o fluxo de trabalho EDRM](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Gerenciando os responsáveis

Use a guia **responsáveis** para adicionar e gerenciar as pessoas que você identificou como pessoas de interesse no caso. Ao adicionar os responsáveis, você pode executar rapidamente ações relacionadas a responsáveis, como colocar uma ofício como as fontes de dados de responsáveis, como a sua caixa de correio e a conta do OneDrive, a comunicação com os responsáveis e a pesquisa de fontes de dados do mesmo para coletar conteúdo Isso é relevante para o caso. Como o andamento do caso, é fácil adicionar novos responsáveis ou liberar responsáveis pela ocorrência. Para obter mais informações, consulte [trabalhar com os responsáveis na descoberta eletrônica avançada (visualização)](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Gerenciando notificações de retenção legal

Use a guia **comunicações** para gerenciar o processo de comunicação com os responsáveis no caso. Um aviso de retenção legal instrui os responsáveis a preservar qualquer conteúdo que possa ser relevante para o caso. As equipes jurídicas devem poder rastrear que os avisos foram recebidos, lidos e confirmados pelos responsáveis. O fluxo de trabalho de comunicações em descoberta eletrônica avançada (visualização) permite criar e enviar notificações iniciais, lembretes, avisos de lançamento e escalonamentos se os responsáveis não conseguirem confirmar uma notificação de bloqueio. Para obter mais informações, consulte [trabalhar com comunicações na descoberta eletrônica avançada (visualização)](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Gerenciando preservação de conteúdo

Ao adicionar um membro a um caso, você tem a opção de colocar uma retenção em dados de custodial. Use a guia **isenções** para gerenciar a retenção criada quando você adiciona os responsáveis e gerencia as retenções legais adicionais associadas à ocorrência; por exemplo, você pode identificar e colocar uma retenção em fontes de dados não custodial. Você também pode editar qualquer bloqueio no caso e torná-lo um bloqueio baseado em consulta para que somente o conteúdo que corresponde à consulta seja colocado em espera; por exemplo, você pode adicionar um intervalo de datas à isenção para que somente o conteúdo que foi criado em uma data específica seja faixa em preservado. Você também pode obter estatísticas sobre o conteúdo que está em espera, remover a retenção após o momento em que ela não for mais relevante para o caso ou excluí-la. Para obter mais informações, consulte [gerenciar isenções na descoberta eletrônica avançada (visualização)](managing-holds.md).

## <a name="indexing-custodian-data"></a>Indexando dados de responsáveis

Quando você adiciona um Objecte as fontes de dados do custodial correspondentes a um caso, qualquer item parcialmente indexado de uma fonte de dados do responsáveis é re-indexado (por um processo chamado *indexAção avançada*). Isso permite que o conteúdo do custodial, como imagens, tipos de arquivo não suportados, e outro conteúdo potencialmente não indexado seja totalmente pesquisável quando você executar pesquisas para coletar dados relevantes ao caso. Use a guia **processamento** para monitorar o status de erros avançados de indexação e processamento de correção (usando um processo Calle *correção de erro*.) Para obter mais informações, consulte [corrigir erros de processamento em descoberta eletrônica avançada (versão prévia)](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Coletando dados de caso

Use a guia **pesquisas** para criar pesquisas para pesquisar as fontes de dados custodial e não-custodial no local no Office 365 para o conteúdo relevante para o caso. Você pode criar e executar pesquisas baseadas em consulta (usando palavras-chave e condições) para identificar um conjunto de mensagens e documentos de email que são relevantes para o caso e o que você deseja revisar mais e analisar em etapas subsequentes no fluxo de trabalho de descoberta eletrônica. Você pode criar uma ou mais pesquisas associadas à ocorrência. Além disso, você pode usar a ferramenta de pesquisa para visualizar documentos de amostra e exibir estatísticas de pesquisa que podem ajudar a aprimorar e aprimorar os resultados da pesquisa. Quando você estiver convencido de que os resultados da pesquisa contenham todos os dados relevantes para o caso, adicione os resultados da pesquisa a um conjunto de trabalho para revisão adicional, análise e, se necessário, de remoção. Para obter mais informações, consulte [coletar dados por um caso na descoberta eletrônica avançada (visualização)](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>ReVisando e analisando dados de caso

Use a guia **conjuntos de trabalho** ou revise e analise o conteúdo que você coletou do sistema em tempo real e adicionado a um conjunto de trabalho. Um *conjunto de trabalho* é uma coleção estática (em outras palavras, uma cópia offline do DAT) de dados do custodial (e, se aplicável, dados não custodial) que você coletou na fase anterior do fluxo de trabalho de descoberta eletrônica. Quando você adiciona resultados de pesquisa a um conjunto de trabalho, um processo é disparado que extrai arquivos de contêineres, extrai metadados e extrai texto. Quando esse processo é concluído, o sistema cria um novo índice de todos os dados coletados de responsáveis e adicionados ao conjunto de trabalho. Depois que os dados são adicionados ao conjunto de trabalho, você pode executar consultas adicionais para restringir os dados de caso, exibir dados como texto ou no formato de arquivo nativo e anotar, redigir e marcar documentos no conjunto de trabalho. Além disso, você pode executar análises avançadas, como identificar duplicação de documentos, encadeamento de emails e temas. Após a remoção dos dados para o que for relevante para o caso, você pode baixar documentos de download diretamente ou exportá-los junto com metadados, anotações e marcas de arquivo. Para obter mais informações, consulte:

  - [ReVisar dados de caso na descoberta eletrônica avançada (versão prévia)](reviewing-data-in-working-set.md)
  - [Analisar dados em um conjunto de trabalho em descoberta eletrônica avançada (visualização)](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>ExPortando dados para revisão e apresentação

Depois de exportar os dados de um conjunto de trabalho, use **** a guia exportações para gerenciar um trabalho de exportação e baixar dados de um conjunto de trabalho. Quando você exporta um conjunto de trabalho, os dados são carregados em um local de armazenamento do Azure e, em seguida, estão disponíveis para download em um computador local. Você pode obter a chave de avaliação de local e armazenamento necessária para baixar os dados exportados na guia exportações. **** Para obter mais informações, consulte [exportar dados de caso na descoberta eletrônica avançada (visualização)](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Gerenciando trabalhos

Use a guia **trabalhos** para monitorar processos de execução demorada para tarefas relacionadas a casos que você iniciou, pesquisa como reindexação, pesquisas e exportações. Por exemplo, você pode criar uma nova pesquisa na guia **pesquisas** que inclui um grande número de fontes de dados. O status desse processo de pesquisa é exibido na guia **trabalhos** . Para obter mais informações, consulte [gerenciar trabalhos na descoberta eletrônica avançada (visualização)](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>ConFigurando as configurações de caso

Use a guia **configurações** para configurar definições em todo o caso. Isso inclui adicionar membros a um caso, fechar ou excluir uma ocorrência e configurar o comportamento de pesquisa e análise. Para obter mais informações, consulte [Configure Case Settings in Advanced eDiscovery (Preview)](configuring-case-settings-ediscovery20.md).

