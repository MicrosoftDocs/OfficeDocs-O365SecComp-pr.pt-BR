---
title: Coletar dados para uma ocorrência na descoberta eletrônica avançada (visualização)
ms.author: esclee
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
ms.openlocfilehash: bcc307cc08954dd3cc69e8905747393d79f97b04
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297094"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="343fe-102">Coletar dados para uma ocorrência na descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="343fe-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="343fe-p101">Depois de identificar os responsáveis e as fontes de dados que são de interesse para o seu caso, é hora de identificar o conjunto de documentos para o qual você deseja se aprofundar. Você pode usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para identificá-los de locais do custodial e do não custodial no Office 365.</span><span class="sxs-lookup"><span data-stu-id="343fe-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="343fe-p102">Após executar uma pesquisa, você poderá exibir estatísticas sobre os itens recuperados, como os locais que tinham a maioria dos itens que corresponderam à consulta de pesquisa. Você também pode visualizar um subconjunto dos resultados. Quando você identificou o conjunto de documentos que deseja examinar mais, você pode adicionar os resultados da pesquisa a um conjunto de trabalho para coletar e processar.</span><span class="sxs-lookup"><span data-stu-id="343fe-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="343fe-108">Criar uma pesquisa</span><span class="sxs-lookup"><span data-stu-id="343fe-108">Create a search</span></span>

<span data-ttu-id="343fe-p103">Clicar em **nova pesquisa** na guia **pesquisas** iniciará um assistente que orienta você durante a criação de uma pesquisa. Para obter informações detalhadas sobre como criar uma pesquisa, consulte [criar uma pesquisa para coletar dados](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="343fe-p104">Após a criação de uma pesquisa, uma página de submenu com detalhes é exibida. Observe que os botões **estatísticas** e **Visualização** estão esmaecidos inicialmente porque a pesquisa ainda não foi concluída. Você pode acompanhar o progresso da pesquisa na guia **pesquisas** .</span><span class="sxs-lookup"><span data-stu-id="343fe-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="343fe-114">Exibir resultados e estatísticas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="343fe-114">View search results and statistics</span></span>
<span data-ttu-id="343fe-p105">Há dois componentes de uma pesquisa de conteúdo: estatísticas (estimativas) e visualização. Como cada um desses componentes é concluído, você verá o status exibido nas colunas correspondentes na guia **pesquisas** mudar de de **enviado** para **em andamento** para **concluído**.</span><span class="sxs-lookup"><span data-stu-id="343fe-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="343fe-p106">Após a conclusão da pesquisa, clique na pesquisa para exibir a página do menu suspenso, que exibirá algumas estatísticas de alto nível sobre os resultados da pesquisa. Neste ponto, o botão **estatísticas** estará ativo. Você pode clicar nele para ver as estatísticas de pesquisa, como:</span><span class="sxs-lookup"><span data-stu-id="343fe-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="343fe-120">Resumo</span><span class="sxs-lookup"><span data-stu-id="343fe-120">Summary</span></span>
- <span data-ttu-id="343fe-121">Principais locais</span><span class="sxs-lookup"><span data-stu-id="343fe-121">Top locations</span></span>
- <span data-ttu-id="343fe-122">Repete</span><span class="sxs-lookup"><span data-stu-id="343fe-122">Queries</span></span>
- <span data-ttu-id="343fe-123">Refinadores</span><span class="sxs-lookup"><span data-stu-id="343fe-123">Refiners</span></span>

<span data-ttu-id="343fe-124">Para obter mais informações sobre estatísticas de pesquisa, confira [Estatísticas de pesquisa](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="343fe-p107">Após a conclusão da visualização, o botão **Visualizar** estará ativo. Clique nele para visualizar um subconjunto de amostra dos resultados.</span><span class="sxs-lookup"><span data-stu-id="343fe-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="343fe-127">Adicionando resultados de pesquisa a um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="343fe-127">Adding search results to a working set</span></span>

<span data-ttu-id="343fe-p108">Quando estiver pronto para coletar e processar os resultados inteiros de uma pesquisa, você poderá adicioná-lo a um conjunto de trabalho. Para obter detalhes, consulte [Add data to a Working Set](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 