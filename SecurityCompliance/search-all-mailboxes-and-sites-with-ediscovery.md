---
title: Pesquisar todas as caixas de correio e sites usando o Centro de Descoberta Eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: Na Central de descoberta eletrônica no Office 365, você pode pesquisar todas as caixas de correio do Exchange Online, sites do SharePoint Online e OneDrive para sites corporativos em uma pesquisa de descoberta eletrônica único. Para pesquisar todas as fontes de conteúdo na organização, um gerente de descoberta eletrônica deve ter as permissões de descoberta eletrônica apropriado para cada fonte de conteúdo.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523896"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a><span data-ttu-id="d4876-104">Pesquisar todas as caixas de correio e sites usando o Centro de Descoberta Eletrônica</span><span class="sxs-lookup"><span data-stu-id="d4876-104">Search all mailboxes and sites using the eDiscovery Center</span></span>

<span data-ttu-id="d4876-p102">Na Central de descoberta eletrônica no Office 365, você pode pesquisar todas as caixas de correio do Exchange Online, sites do SharePoint Online e OneDrive para sites corporativos em uma pesquisa de descoberta eletrônica único. Para pesquisar todas as fontes de conteúdo na organização, um gerente de descoberta eletrônica deve ter as permissões de descoberta eletrônica apropriado para cada fonte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d4876-p102">In the eDiscovery Center in Office 365, you can search all Exchange Online mailboxes, SharePoint Online sites, and OneDrive for Business sites in a single eDiscovery search. To search all content sources in the organization, an eDiscovery manager must be assigned the appropriate eDiscovery permissions for each content source.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="d4876-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="d4876-107">Before you begin</span></span>

- <span data-ttu-id="d4876-p103">Um gerente de Descoberta eletrônica deve ter as permissões apropriadas para pesquisar uma fonte de conteúdo. Para saber mais sobre como atribuir permissões de Descoberta eletrônica a sites e caixas de correio, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4876-p103">An eDiscovery manager must be assigned the appropriate permissions to search a content source. For more information about assigning eDiscovery permissions to mailboxes and sites, see the following:</span></span> 
    
  - [<span data-ttu-id="d4876-110">Atribuir permissões de descoberta eletrônica no Exchange</span><span class="sxs-lookup"><span data-stu-id="d4876-110">Assign eDiscovery permissions in Exchange</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [<span data-ttu-id="d4876-111">Atribuir permissões de Descoberta Eletrônica no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d4876-111">Assign eDiscovery permissions in SharePoint Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [<span data-ttu-id="d4876-112">Atribuir permissões de Descoberta eletrônica a sites do OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="d4876-112">Assign eDiscovery permissions to OneDrive for Business sites</span></span>](assign-permissions-to-onedrive-for-business-sites.md)
    
- <span data-ttu-id="d4876-p104">Você pode pesquisar um máximo de 10.000 caixas de correio e um número ilimitado de SharePoint Online e OneDrive para sites corporativos em uma consulta de pesquisa de descoberta eletrônica único. No entanto, se você especificar os sites específicos para pesquisar, o limite é de 100 sites.</span><span class="sxs-lookup"><span data-stu-id="d4876-p104">You can search a maximum of 10,000 mailboxes and an unlimited number of SharePoint Online and OneDrive for Business sites in a single eDiscovery search query. However, if you specify the specific sites to search, the limit is 100 sites.</span></span>
    
- <span data-ttu-id="d4876-115">Consulte a seção de [informações adicionais](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) para obter uma descrição dos limites ao visualizar os resultados ao pesquisar todas as caixas de correio e sites.</span><span class="sxs-lookup"><span data-stu-id="d4876-115">See the [More information](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) section for a description of the limits when viewing the results when searching all mailboxes and sites.</span></span> 
    
- <span data-ttu-id="d4876-116">Para obter mais informações sobre como criar consultas de pesquisa no Centro de descoberta eletrônica, consulte [criar e consultas do eDiscovery execução](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span><span class="sxs-lookup"><span data-stu-id="d4876-116">For more information about creating search queries in the eDiscovery Center, see [Create and run eDiscovery queries](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span></span>
    
## <a name="search-all-locations"></a><span data-ttu-id="d4876-117">Pesquisar todos os locais</span><span class="sxs-lookup"><span data-stu-id="d4876-117">Search all locations</span></span>

1. <span data-ttu-id="d4876-118">No Centro de Descoberta Eletrônica, abra a ocorrência de Descoberta eletrônica para a qual deseja executar a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d4876-118">In the eDiscovery Center, open the eDiscovery case that you want to run the search query for.</span></span>
    
2. <span data-ttu-id="d4876-119">Em **pesquisa e exportação**, clique em uma consulta existente ou clique em **novo item** para criar uma nova consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d4876-119">Under **Search and Export**, click an existing query or click **New item** to create a new search query.</span></span> 
    
3. <span data-ttu-id="d4876-120">Na página de consulta da pesquisa, na seção **Fontes**, clique em **Modificar Escopo de Consulta**.</span><span class="sxs-lookup"><span data-stu-id="d4876-120">On the search query page, in the **Sources** section, click **Modify Query Scope**.</span></span>
    
4. <span data-ttu-id="d4876-121">Na página **Modificar Escopo de Consulta**, clique em **Pesquisar tudo** e selecione os locais de conteúdo para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d4876-121">On the **Modify Query Scope** page, click **Search everything**, and select the content locations to search.</span></span>
    
  - <span data-ttu-id="d4876-122">Selecione a todas as caixas de pesquisa do **Exchange** .</span><span class="sxs-lookup"><span data-stu-id="d4876-122">Select **Exchange** to search all mailboxes.</span></span> 
    
  - <span data-ttu-id="d4876-123">Selecione **SharePoint** para procurar todos os SharePoint Online e OneDrive sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="d4876-123">Select **SharePoint** to search all SharePoint Online and OneDrive for Business sites.</span></span> 
    
  - <span data-ttu-id="d4876-124">Selecione **Exchange** e **SharePoint** para pesquisar todos os locais de conteúdo na sua organização.</span><span class="sxs-lookup"><span data-stu-id="d4876-124">Select both **Exchange** and **SharePoint** to search all content locations in your organization.</span></span> 
    
![Pesquisar todas as caixas de correio e sites](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. <span data-ttu-id="d4876-126">Clique em **OK** para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="d4876-126">Click **OK** to save the changes.</span></span> 
    
6. <span data-ttu-id="d4876-p105">Conclua ou revise outras informações na página de consulta da pesquisa, como a consulta de palavra-chave, o intervalo de datas ou a restrição dos tipos específicos de conteúdo a serem pesquisados. Quando você estiver pronto para executar a consulta, clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="d4876-p105">Complete or revise other information on the search query page, such as the keyword query, the date range, or narrowing the specific types of content to search for. When you're ready to run the query, click **Search**.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="d4876-129">Mais informações</span><span class="sxs-lookup"><span data-stu-id="d4876-129">More information</span></span>
<span data-ttu-id="d4876-130"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="d4876-130"></span></span>

- <span data-ttu-id="d4876-131">As primeiras 500 caixas de correio e 500 sites com o maior número de resultados listados em **Fontes** na página **Consulta**.</span><span class="sxs-lookup"><span data-stu-id="d4876-131">The top 500 mailboxes and the top 500 sites with the most results are listed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="d4876-132">O número total de itens encontrados em todas as fontes de conteúdo e o tamanho total combinado é exibido em **Fontes** na página **Consulta**. 
</span><span class="sxs-lookup"><span data-stu-id="d4876-132">The total number of items found in all content sources and their combined total size are displayed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="d4876-133">Você pode visualizar os 200 resultados de pesquisa mais recentes localizados nas caixas de correio do Exchange ou nos sites do SharePoint na página **Consulta**.</span><span class="sxs-lookup"><span data-stu-id="d4876-133">You can preview the 200 most recent search results located in Exchange mailboxes or SharePoint sites on the **Query** page.</span></span> 
    
    <span data-ttu-id="d4876-134">A captura de tela a seguir mostra um exemplo dos resultados da pesquisa exibidos na página **Consulta** quando você pesquisa todos os sites e caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="d4876-134">The following screenshot shows an example of the search results displayed on the **Query** page when you search all mailboxes and sites.</span></span> 
    
    ![Captura de tela dos resultados ao pesquisar todos os locais](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

