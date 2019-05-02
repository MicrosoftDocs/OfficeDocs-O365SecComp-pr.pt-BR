---
title: Adicionar resultados de pesquisa a um conjunto de revisão
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
description: ''
ms.openlocfilehash: fc32836026d1a2c449e73a28eafc2f5a631a1705
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527103"
---
# <a name="add-search-results-to-a-review-set"></a>Adicionar resultados de pesquisa a um conjunto de revisão

Quando estiver satisfeito com os resultados de uma pesquisa e estiver pronto para revisar e analisar os resultados da pesquisa, você poderá adicioná-los a uma análise definida no caso. Copiar os dados originais para o conjunto de revisão também facilita o processo de revisão e análise fornecendo ferramentas avançadas de análise, como detecção de temas, detecção de duplicidade próxima e identificação de thread de email. Também é possível adicionar dados de fontes de dados que não sejam do Office 365 a um conjunto de revisão para que você possa revisar os dados além dos dados coletados do Office 365.

Quando você adiciona os resultados de uma pesquisa a um conjunto de revisão (os conjuntos de revisão estão localizados na guia **conjuntos de revisão** do caso), ocorrem as duas ações a seguir:

- Todos os itens nos resultados da pesquisa são copiados da fonte de dados original nos serviços do Live Office 365 e copiados para um local seguro de armazenamento do Azure na nuvem da Microsoft.

- Todos os itens (incluindo o conteúdo e os metadados) são reindexados para que todos os dados no conjunto de revisão sejam totalmente pesquisáveis durante a revisão dos dados de caso. A indexação dos resultados dos dados em pesquisas abrangentes e muito rápidas quando você pesquisa os dados na revisão definida durante a investigação do caso.

Para adicionar dados a um conjunto de revisão, clique em uma pesquisa na guia **pesquisas** e, em seguida, clique em **Adicionar resultados para revisão definida** na página do menu suspenso.

![Adicionando dados a um conjunto de revisão](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

Observe que você pode adicionar a um conjunto de revisão existente ou criar um novo conjunto de revisão.  Se estiver adicionando a um novo conjunto de revisão, especifique o nome e clique em **Adicionar**.

![Selecione um conjunto de revisão](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

A adição de dados a um conjunto de revisão é um processo de execução demorada. Esse processo inclui a coleta de itens das fontes de dados originais no Office 365 (por exemplo, de caixas de correio e sites), copiando-os para o local de armazenamento do Azure (esse processo de cópia também é chamado de *inclusão*) e, em seguida, indexando novamente os itens. Você pode acompanhar o progresso na guia **trabalhos** ou na guia **pesquisas** monitorando o status na coluna **Adicionar dados para revisão** . Depois que o processamento do conjunto de revisão estiver concluído, clique na guia revisar **conjuntos** no caso e, em seguida, clique no conjunto de revisão para iniciar a filtragem do processo, a revisão, a marcação e a exportação de dados no conjunto de revisão.

## <a name="add-a-sample-to-a-review-set"></a>Adicionar um exemplo a um conjunto de revisão

Se você quiser validar os resultados de uma pesquisa com mais detalhes antes de adicionar todos eles a um conjunto de revisão, você pode adicionar um exemplo dos resultados da pesquisa a um conjunto de revisão, em vez de adicionar tudo.

Para adicionar um exemplo a um conjunto de revisão, clique em uma pesquisa na guia **pesquisas** e clique em **amostra** na página do menu suspenso. Na página **parâmetros de amostragem** , escolha uma das seguintes opções:

- O **nível de confiança%** e o **intervalo de confiança%** -os itens adicionados ao conjunto de revisão serão determinados pelos parâmetros estatísticos definidos. Se você costuma usar um nível de confiança e um intervalo ao obter resultados de amostragem, especifique-os nas caixas suspensas. Caso contrário, basta usar as configurações padrão.

- **Amostra aleatória%** -os itens adicionados ao conjunto de revisão são baseados em uma seleção aleatória do percentual especificado do número total de itens retornados pela pesquisa.

Após selecionar e configurar uma das opções anteriores, escolha um conjunto de revisão existente para adicionar o exemplo e clique em **Enviar**. Novamente, você pode acompanhar o progresso na guia **trabalhos** ou na guia **pesquisas** monitorando o status na coluna **Adicionar dados para revisão** .