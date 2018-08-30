---
title: Exportar um relatório da Pesquisa de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/25/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Em vez de exportar os resultados reais de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, você pode exportar apenas um relatório de resultados de pesquisa. O relatório contém um resumo dos resultados da pesquisa e um documento com informações detalhadas sobre cada item que deve ser exportado.
ms.openlocfilehash: 45415f25754b4549a919e4ce56853a6ae09a9bdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523462"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="6d47a-104">Exportar um relatório da Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="6d47a-104">Export a Content Search report</span></span>

<span data-ttu-id="6d47a-105">Em vez de exportar o conjunto completo de pesquisa resultados de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade (e a partir de uma pesquisa de conteúdo que está associado a um caso de descoberta eletrônica), você pode exportar apenas os mesmos relatórios que são gerados quando você exporte resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d47a-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="6d47a-p102">Quando você exporta um relatório, ele será baixado para uma pasta que tem o mesmo nome que a pesquisa de conteúdo, mas que foi acrescentado com *_ReportsOnly* . Por exemplo, se a pesquisa de conteúdo é denominada *ContosoCase0815* , o relatório é baixado para uma pasta denominada *ContosoCase0815_ReportsOnly* . Para obter uma lista de documentos que estão incluídos no relatório, consulte [o que está incluído no relatório](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="6d47a-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="6d47a-109">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="6d47a-109">Before you begin</span></span>

- <span data-ttu-id="6d47a-p103">Para exportar um relatório de pesquisa de conteúdo, você precisa ter a função de gerenciamento de conformidade de pesquisa no Office 365 Security &amp; Centro de conformidade. Essa função é atribuída aos grupos de função de gerente e o gerenciamento da organização do eDiscovery internas. Ele não é atribuído por padrão ao grupo de funções de gerenciamento da organização. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="6d47a-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="6d47a-p104">Quando você exporta um relatório, os dados são armazenados temporariamente em uma área de armazenamento do Windows Azure exclusiva em nuvem da Microsoft antes de ele será baixado para o computador local. Certifique-se de que sua organização pode se conectar ao ponto de extremidade no Windows Azure, que é \*\* \*. blob.core.windows.net\*\* (o caractere curinga representa um identificador exclusivo para a exportação). Os dados dos resultados de pesquisa são excluídos da área de armazenamento do Azure duas semanas após sua criação.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="6d47a-117">O computador que você usa para exportar os resultados da pesquisa devem atender aos seguintes requisitos de sistema:</span><span class="sxs-lookup"><span data-stu-id="6d47a-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="6d47a-118">Versões de 32 e 64 bits do Windows 7 e versões posteriores


</span><span class="sxs-lookup"><span data-stu-id="6d47a-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="6d47a-119">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="6d47a-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="6d47a-120">Um navegador com suporte:</span><span class="sxs-lookup"><span data-stu-id="6d47a-120">A supported browser:</span></span>
    
    - <span data-ttu-id="6d47a-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6d47a-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="6d47a-122">ou</span><span class="sxs-lookup"><span data-stu-id="6d47a-122">or</span></span>
    
    - <span data-ttu-id="6d47a-123">Microsoft Internet Explorer 10 e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="6d47a-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="6d47a-p105">**Observação:** A Microsoft não fabrica extensões de terceiros ou complementos para aplicativos ClickOnce. Exportar resultados de pesquisa usando um navegador sem suporte com extensões de terceiros ou complementos não é suportado.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
    
## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="6d47a-126">Gerar e faça o download de um relatório de pesquisa de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6d47a-126">Generate and download a Content Search report</span></span>

<span data-ttu-id="6d47a-127">As etapas para gerar e faça o download de um relatório de pesquisa de conteúdo serão bastante similares às realmente exportar os resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d47a-127">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="6d47a-128">Etapa 1: Gerar o relatório para exportação</span><span class="sxs-lookup"><span data-stu-id="6d47a-128">Step 1: Generate the report for export</span></span>

<span data-ttu-id="6d47a-p106">A primeira etapa é preparar o relatório para baixar para seu computador exportando. Quando você o relatório, o relatório de documentos são carregados para uma área de armazenamento do Azure na Microsoft em nuvem.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p106">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="6d47a-131">Vá para [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="6d47a-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="6d47a-132">Entrar no Office 365 usando sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="6d47a-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="6d47a-133">No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisa&amp; investigação** \> **Pesquisa de Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-133">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="6d47a-134">Na página de **pesquisa de conteúdo** , selecione uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d47a-134">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="6d47a-135">No painel de detalhes, em **Exportar relatório em um computador**, clique em **Gerar relatório**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-135">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6d47a-p107">Se os resultados para uma pesquisa mais de 7 dias, você precisará atualizar os resultados da pesquisa. Se isso acontecer, cancelar a exportação, clique em **resultados da pesquisa de atualização** no painel de detalhes para a pesquisa selecionado e inicie a exportação de relatório novamente depois que os resultados são atualizados.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p107">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="6d47a-138">Na página **Exportar um relatório** , em **incluir estes itens da pesquisa**, escolha uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="6d47a-138">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="6d47a-139">Exportar somente itens indexados</span><span class="sxs-lookup"><span data-stu-id="6d47a-139">Export only indexed items</span></span>
    
    - <span data-ttu-id="6d47a-140">Exportar itens indexados e não indexados</span><span class="sxs-lookup"><span data-stu-id="6d47a-140">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="6d47a-141">Exportar somente itens não indexados</span><span class="sxs-lookup"><span data-stu-id="6d47a-141">Export only unindexed items</span></span>
    
    <span data-ttu-id="6d47a-142">Para obter mais informações sobre os itens não indexadas, consulte [parcialmente indexados itens na pesquisa de conteúdo](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="6d47a-142">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="6d47a-p108">Optar por incluir as estatísticas da pesquisa para todas as versões de documentos do SharePoint. Essa opção aparecerá somente se as fontes de conteúdo da pesquisa inclui SharePoint ou OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p108">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="6d47a-145">Clique em **Gerar relatório**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-145">Click **Generate report**.</span></span>
    
    <span data-ttu-id="6d47a-p109">O relatório de resultados de pesquisa está preparado para download, o que significa que os documentos de relatório serão carregados para a área de armazenamento do Azure na nuvem da Microsoft. Quando o relatório está pronto para download, no link **baixar relatório** é exibido em **Exportar relatório em um computador** no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p109">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6d47a-p110">Você também pode exportar um relatório para uma pesquisa de conteúdo que está associado a um caso de eDiscovery. Para fazer isso, vá para **pesquisa &amp; investigação** \> **eDiscovery**, selecione um caso e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Na página de **pesquisa** , selecione uma pesquisa e, em seguida, clique em **Exportar** ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exportar um relatório**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p110">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="6d47a-151">Etapa 2: Baixar o relatório</span><span class="sxs-lookup"><span data-stu-id="6d47a-151">Step 2: Download the report</span></span>

<span data-ttu-id="6d47a-152">A próxima etapa é baixar o relatório a partir da área de armazenamento do Azure ao computador local.</span><span class="sxs-lookup"><span data-stu-id="6d47a-152">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="6d47a-153">No painel de detalhes para a pesquisa que você gerou o relatório, em **Exportar relatório em um computador**, clique em **baixar relatório**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-153">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="6d47a-154">A página de **Download de relatório** é exibida e contém as seguintes informações sobre o relatório até ser baixado para seu computador.</span><span class="sxs-lookup"><span data-stu-id="6d47a-154">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="6d47a-155">O número de itens que serão baixados.</span><span class="sxs-lookup"><span data-stu-id="6d47a-155">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="6d47a-156">O tamanho total estimado dos itens que serão baixados.</span><span class="sxs-lookup"><span data-stu-id="6d47a-156">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="6d47a-p111">Se indexados ou não indexados serão exportados. Itens indexados são itens que têm um formato reconhecido, são criptografados ou não foram indexados por outros motivos.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p111">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="6d47a-159">Se serão baixadas ou não versões dos documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6d47a-159">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="6d47a-p112">O status do processo de exportação de relatório. Você pode iniciar o download do relatório, mesmo se a preparação do relatório não for concluída.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p112">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="6d47a-p113">Em **Exportar chave**, clique em **Copiar para a área de transferência**. Você usará essa chave na etapa 5 para baixar o relatório.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p113">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6d47a-164">Porque qualquer pessoa pode instalar e iniciar a ferramenta de exportação de descoberta eletrônica e, em seguida, use essa chave para baixar o relatório de pesquisa, certifique-se de que tome precauções para proteger essa chave exatamente como você faria proteger senhas ou outras informações relacionadas à segurança.</span><span class="sxs-lookup"><span data-stu-id="6d47a-164">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="6d47a-165">Clique em **baixar relatório**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-165">Click **Download report**.</span></span>
    
4. <span data-ttu-id="6d47a-166">Se você for solicitado a instalar o **eDiscovery MicrosoftOffice 365 Tool exportar**, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="6d47a-166">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="6d47a-167">Na **Ferramenta de Exportação de Descoberta Eletrônica**, cole a chave de exportação que você copiou na etapa 2 na caixa apropriada.</span><span class="sxs-lookup"><span data-stu-id="6d47a-167">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="6d47a-168">Clique em **Procurar** para especificar o local onde você deseja baixar o relatório.</span><span class="sxs-lookup"><span data-stu-id="6d47a-168">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="6d47a-169">Clique em **Iniciar** para baixar os resultados da pesquisa em seu computador.</span><span class="sxs-lookup"><span data-stu-id="6d47a-169">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="6d47a-p114">A **ferramenta de exportação de descoberta eletrônica** exibe informações de status sobre o processo de exportação, incluindo uma estimativa do número (e tamanho) dos itens restantes a serem baixados. Quando o processo de exportação estiver concluído, você pode acessar os arquivos no local onde elas são baixadas.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p114">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6d47a-p115">Você pode baixar o relatório para uma pesquisa de conteúdo que está associado a um caso de eDiscovery. Para fazer isso, vá para **pesquisa &amp; investigação** \> **eDiscovery**, selecione um caso e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Na página **exportações** , selecione Exportar um relatório e clique em **baixar relatório** no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p115">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="6d47a-175">O que está incluído no relatório</span><span class="sxs-lookup"><span data-stu-id="6d47a-175">What's included in the report</span></span>

<span data-ttu-id="6d47a-176">Quando você gera e exporta um relatório sobre os resultados de uma pesquisa de conteúdo, os documentos a seguir são baixados:</span><span class="sxs-lookup"><span data-stu-id="6d47a-176">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="6d47a-p116">**Exportar resumo** - documento do Excel de uma contém um resumo da exportação. Isso inclui informações como o número de fontes de conteúdo que foram pesquisadas, o número de resultados de pesquisa de cada local do conteúdo, o número estimado de itens, o número real de itens que seria ser exportados e o tamanho estimado e real dos itens que poderia ser exportado.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p116">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6d47a-p117">Se você incluir itens indexados ao exportar o relatório, o número de itens indexados é incluído no número total de resultados de pesquisa estimados e no número total de resultados da pesquisa baixado (se fosse exportar os resultados da pesquisa) que estão listados no Exporte o relatório de resumo. Em outras palavras, o número total de itens que seria ser baixado é igual ao número total de resultados estimados e o número total de itens indexados.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p117">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="6d47a-181">**Manifesto** - um arquivo de manifesto (no formato XML) que contém informações sobre cada item incluído nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d47a-181">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="6d47a-p118">**Resultados** - documento An Excel que contém uma linha com informações sobre cada item indexado que seria ser exportado com os resultados da pesquisa. Para email, o log de resultado contém informações sobre cada mensagem, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6d47a-p118">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="6d47a-184">O local da mensagem na caixa de correio de origem (inclusive se a mensagem está na caixa de correio principal ou de arquivo morto).</span><span class="sxs-lookup"><span data-stu-id="6d47a-184">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="6d47a-185">A data na qual a mensagem foi enviada ou recebida.</span><span class="sxs-lookup"><span data-stu-id="6d47a-185">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="6d47a-186">A linha de assunto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d47a-186">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="6d47a-187">O remetente e os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d47a-187">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="6d47a-188">Para documentos do SharePoint e do OneDrive para sites corporativos, o log de resultados contém informações sobre cada documento, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6d47a-188">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="6d47a-189">A URL para o documento.</span><span class="sxs-lookup"><span data-stu-id="6d47a-189">The URL for the document.</span></span>
    
  - <span data-ttu-id="6d47a-190">A URL para o conjunto de sites onde o documento está localizado.</span><span class="sxs-lookup"><span data-stu-id="6d47a-190">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="6d47a-191">A data em que o documento foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6d47a-191">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="6d47a-192">O nome do documento (que está localizado na coluna Assunto no log de resultados).</span><span class="sxs-lookup"><span data-stu-id="6d47a-192">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6d47a-193">O número de linhas no relatório de **resultados** deve ser igual ao número total de resultados de pesquisa que seria ser baixados menos o número total de itens listados no relatório de **Itens indexados** .</span><span class="sxs-lookup"><span data-stu-id="6d47a-193">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="6d47a-p119">**Itens indexados** - documento do Excel de uma que contém informações sobre todos os itens indexados seriam incluídos nos resultados da pesquisa. Se você não incluir itens indexados quando você gera o relatório de resultados de pesquisa, ainda será baixado este relatório, mas estará vazio.</span><span class="sxs-lookup"><span data-stu-id="6d47a-p119">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
