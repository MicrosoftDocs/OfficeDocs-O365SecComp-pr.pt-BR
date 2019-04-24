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
ms.openlocfilehash: fb4b36841394576c44667f9677507c5655179e45
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242549"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="5cc54-102">Coletar dados para uma ocorrência na descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="5cc54-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="5cc54-103">Depois de identificar os responsáveis e as fontes de dados que são de interesse para o seu caso, é hora de identificar o conjunto de documentos para o qual você deseja se aprofundar.</span><span class="sxs-lookup"><span data-stu-id="5cc54-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="5cc54-104">Você pode usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para identificá-los de locais do custodial e do não custodial no Office 365.</span><span class="sxs-lookup"><span data-stu-id="5cc54-104">You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="5cc54-105">Após executar uma pesquisa, você poderá exibir estatísticas sobre os itens recuperados, como os locais que tinham a maioria dos itens que corresponderam à consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5cc54-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="5cc54-106">Você também pode visualizar um subconjunto dos resultados.</span><span class="sxs-lookup"><span data-stu-id="5cc54-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="5cc54-107">Quando você identificou o conjunto de documentos que deseja examinar mais, você pode adicionar os resultados da pesquisa a um conjunto de trabalho para coletar e processar.</span><span class="sxs-lookup"><span data-stu-id="5cc54-107">When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="5cc54-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="5cc54-108">Create a search</span></span>

<span data-ttu-id="5cc54-109">Clicar em **nova pesquisa** na guia **pesquisas** iniciará um assistente que orienta você durante a criação de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5cc54-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="5cc54-110">Para obter informações detalhadas sobre como criar uma pesquisa, consulte [criar uma pesquisa para coletar dados](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="5cc54-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="5cc54-111">Após a criação de uma pesquisa, uma página de submenu com detalhes é exibida.</span><span class="sxs-lookup"><span data-stu-id="5cc54-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="5cc54-112">Observe que os botões **estatísticas** e **Visualização** estão esmaecidos inicialmente porque a pesquisa ainda não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5cc54-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="5cc54-113">Você pode acompanhar o progresso da pesquisa na guia **pesquisas** .</span><span class="sxs-lookup"><span data-stu-id="5cc54-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="5cc54-114">Exibir resultados e estatísticas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5cc54-114">View search results and statistics</span></span>
<span data-ttu-id="5cc54-115">Há dois componentes de uma pesquisa de conteúdo: estatísticas (estimativas) e visualização.</span><span class="sxs-lookup"><span data-stu-id="5cc54-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="5cc54-116">Como cada um desses componentes é concluído, você verá o status exibido nas colunas correspondentes na guia **pesquisas** mudar de de **enviado** para **em andamento** para **concluído**.</span><span class="sxs-lookup"><span data-stu-id="5cc54-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="5cc54-117">Após a conclusão da pesquisa, clique na pesquisa para exibir a página do menu suspenso, que exibirá algumas estatísticas de alto nível sobre os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5cc54-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="5cc54-118">Neste ponto, o botão **estatísticas** estará ativo.</span><span class="sxs-lookup"><span data-stu-id="5cc54-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="5cc54-119">Você pode clicar nele para ver as estatísticas de pesquisa, como:</span><span class="sxs-lookup"><span data-stu-id="5cc54-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="5cc54-120">Resumo</span><span class="sxs-lookup"><span data-stu-id="5cc54-120">Summary</span></span>
- <span data-ttu-id="5cc54-121">Principais locais</span><span class="sxs-lookup"><span data-stu-id="5cc54-121">Top locations</span></span>
- <span data-ttu-id="5cc54-122">Consultas</span><span class="sxs-lookup"><span data-stu-id="5cc54-122">Queries</span></span>

<span data-ttu-id="5cc54-123">Para obter mais informações sobre estatísticas de pesquisa, confira [Estatísticas de pesquisa](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="5cc54-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="5cc54-124">Após a conclusão da visualização, o botão **Visualizar** estará ativo.</span><span class="sxs-lookup"><span data-stu-id="5cc54-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="5cc54-125">Clique nele para visualizar um subconjunto de amostra dos resultados.</span><span class="sxs-lookup"><span data-stu-id="5cc54-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="5cc54-126">Adicionando resultados de pesquisa a um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="5cc54-126">Adding search results to a working set</span></span>

<span data-ttu-id="5cc54-127">Quando estiver pronto para coletar e processar os resultados inteiros de uma pesquisa, você poderá adicioná-lo a um conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5cc54-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set.</span></span> <span data-ttu-id="5cc54-128">Para obter detalhes, consulte [Add data to a Working Set](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="5cc54-128">For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 