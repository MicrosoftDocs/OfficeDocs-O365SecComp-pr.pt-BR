---
title: Coletar dados para um caso de eDiscovery avançado (Preview)
ms.author: esclee
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
description: ''
ms.openlocfilehash: 11e2c336512c91d65bd046c3022d5375ebecde4a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695047"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="afd45-102">Coletar dados para um caso de eDiscovery avançado (Preview)</span><span class="sxs-lookup"><span data-stu-id="afd45-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="afd45-p101">Depois de ter identificado responsáveis e fontes de dados de interesse para seu caso, é hora para identificar o conjunto de documentos para abordar. Você pode usar a ferramenta de pesquisa no eDiscovery avançado (Preview) para identificar esses de custódia e não custódia locais no Office 365.</span><span class="sxs-lookup"><span data-stu-id="afd45-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="afd45-p102">Após executar uma pesquisa, você poderá exibir estatísticas sobre os itens recuperados como os locais que tinha a maioria dos itens que correspondem à consulta de pesquisa. Você também pode visualizar um subconjunto dos resultados. Quando você identificou o conjunto de documentos que deseja examinar mais detalhadamente, você pode adicionar os resultados da pesquisa para um conjunto de trabalho para coletar e processar.</span><span class="sxs-lookup"><span data-stu-id="afd45-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="afd45-108">Criar uma pesquisa</span><span class="sxs-lookup"><span data-stu-id="afd45-108">Create a search</span></span>

<span data-ttu-id="afd45-p103">Clicando em **nova pesquisa** na guia **pesquisas** iniciará um assistente que orienta a criação de uma pesquisa. Para obter informações detalhadas sobre como criar uma pesquisa, consulte [criar uma pesquisa para coletar dados](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="afd45-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="afd45-p104">Depois que uma pesquisa é criada, é exibida uma página de submenu com detalhes. Observe que os botões de **estatísticas** e **visualização** inicialmente aparecem acinzentados porque a pesquisa ainda não foi concluída. Você pode ficar atento o progresso da pesquisa na guia **pesquisas** .</span><span class="sxs-lookup"><span data-stu-id="afd45-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="afd45-114">Exibir resultados da pesquisa e estatísticas</span><span class="sxs-lookup"><span data-stu-id="afd45-114">View search results and statistics</span></span>
<span data-ttu-id="afd45-p105">Existem dois componentes de uma pesquisa de conteúdo: estatísticas (estimativas) e visualização. Como cada um desses componentes concluídos, você verá o status exibido nas colunas correspondentes na guia **pesquisas** mudar de **submetido** para **em andamento** como **concluído**.</span><span class="sxs-lookup"><span data-stu-id="afd45-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="afd45-p106">Depois que a estimativa de pesquisa for concluída, clique em pesquisa para exibir a página de submenu, que exibirá algumas estatísticas de alto nível sobre os resultados da pesquisa. Neste ponto, o botão de **estatísticas** ficará ativo. Você pode clicar nele para ver as estatísticas da pesquisa, tais como:</span><span class="sxs-lookup"><span data-stu-id="afd45-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="afd45-120">Resumo</span><span class="sxs-lookup"><span data-stu-id="afd45-120">Summary</span></span>
- <span data-ttu-id="afd45-121">Locais principais</span><span class="sxs-lookup"><span data-stu-id="afd45-121">Top locations</span></span>
- <span data-ttu-id="afd45-122">Consultas</span><span class="sxs-lookup"><span data-stu-id="afd45-122">Queries</span></span>
- <span data-ttu-id="afd45-123">Refinadores</span><span class="sxs-lookup"><span data-stu-id="afd45-123">Refiners</span></span>

<span data-ttu-id="afd45-124">Para obter mais informações sobre estatísticas da pesquisa, consulte [estatísticas da pesquisa](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="afd45-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="afd45-p107">Depois de visualização for concluída, o botão **Visualizar** ficará ativo. Clique para visualizar um subconjunto de amostra dos resultados.</span><span class="sxs-lookup"><span data-stu-id="afd45-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="afd45-127">Adicionar resultados de pesquisa para um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="afd45-127">Adding search results to a working set</span></span>

<span data-ttu-id="afd45-p108">Quando você estiver pronto para coletar e processar os resultados inteiros de uma pesquisa, você pode fazer isso pelo adicioná-lo a um conjunto de trabalho. Para obter detalhes, consulte [Adicionar dados para um conjunto de trabalho](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="afd45-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 