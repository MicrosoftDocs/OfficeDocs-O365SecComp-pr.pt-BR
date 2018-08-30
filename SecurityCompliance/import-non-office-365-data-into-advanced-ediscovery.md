---
title: Importar conteúdo não relacionado ao Office 365 para Descoberta Eletrônica Avançada
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Como às etapas para importar o conteúdo que não está armazenado no O365 em um Windows Azure blob para que ele pode ser analisado com AeD
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524719"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="6fb2e-103">Importar conteúdo não relacionado ao Office 365 para Descoberta Eletrônica Avançada</span><span class="sxs-lookup"><span data-stu-id="6fb2e-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="6fb2e-p101">Nem todos os documentos que você talvez precise analisar com eDiscovery avançadas do Office 365 residirá no Office 365. Com o conteúdo não-Office 365 importe recurso no eDiscovery avançado, que você pode carregar documentos que não live no Office 365 (exceto os arquivos. PST) em um blob maiusculas armazenamento Azure vinculados e analisá-los com eDiscovery avançado. Esse procedimento mostra como trazer seus documentos do Office 365 para descoberta eletrônica avançada para análise.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6fb2e-p102">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6fb2e-p103">Você pode adquirir uma assinatura eDiscovery avançadas do Office 365 de complemento de armazenamento dados para o seu conteúdo do Office 365. Isso é exclusivamente disponível para o conteúdo que deve ser analisada com eDiscovery avançado. Siga as etapas em [comprar ou editar e Add-on do Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) e comprar o complemento de armazenamento de descoberta eletrônica avançadas do Office 365.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p103">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content. This is exclusively available for content that is to be analyzed with Advanced eDiscovery. Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6fb2e-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="6fb2e-112">Before you begin</span></span>

<span data-ttu-id="6fb2e-113">Usando o recurso de upload Non-Office 365, conforme descrito neste procedimento requer que você tenha:</span><span class="sxs-lookup"><span data-stu-id="6fb2e-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="6fb2e-114">Um Office 365 E3 com inscrição de E5 ou complemento de conformidade avançadas</span><span class="sxs-lookup"><span data-stu-id="6fb2e-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="6fb2e-115">Todos os responsáveis cujo conteúdo não - Office 365 será carregado devem ter E3 com licenças de E5 ou complemento de conformidade avançadas</span><span class="sxs-lookup"><span data-stu-id="6fb2e-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="6fb2e-116">Uma ocorrência de descoberta eletrônica existente</span><span class="sxs-lookup"><span data-stu-id="6fb2e-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="6fb2e-p104">Todos os arquivos para carregar coletadas em pastas onde houver uma pasta por dos responsáveis e nome das pastas se situa este formato *alias@domainname* . O *alias@domainname* deve ser o domínio e alias de usuário Office 365. Você pode coletar todas as pastas de *alias@domainname* em uma pasta raiz. A pasta raiz pode conter apenas as pastas *alias@domainname* , não deve haver nenhum arquivo afastado na pasta raiz</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p104">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  . The  *alias@domainname*  must be users Office 365 alias and domain. You can collect all the  *alias@domainname*  folders into a root folder. The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="6fb2e-121">Uma conta que seja um gerente de descoberta eletrônica ou um administrador de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="6fb2e-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="6fb2e-122">[Ferramentas de armazenamento do Microsoft Azure](https://aka.ms/downloadazcopy) instalado em um computador que tenha acesso na estrutura de pasta de conteúdo do Office 365.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="6fb2e-123">Carregar o conteúdo do Office 365 em eDiscovery avançado</span><span class="sxs-lookup"><span data-stu-id="6fb2e-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="6fb2e-p105">Como um gerente de descoberta eletrônica ou eDiscovery administrador, abra o **eDiscovery**e, em seguida, abra o caso em que os dados não - Office 365 serão carregados. Se você precisar criar um caso, consulte [gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](manage-ediscovery-cases.md)</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p105">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to. If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="6fb2e-126">Clique em **Alternar para descoberta eletrônica avançada**</span><span class="sxs-lookup"><span data-stu-id="6fb2e-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="6fb2e-127">Em **tipo de fonte** , selecione **os dados não-Office 365**.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="6fb2e-p106">Clique em **Adicionar contêiner**. Nomeie o contêiner e adicionar uma descrição.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p106">Click **Add container**. Name the container and add a description.</span></span>
    
5. <span data-ttu-id="6fb2e-130">Selecione o contêiner recém-adicionado na lista do contêiner e copie a URL que aparece no painel de detalhes do contêiner e, em seguida, feche o painel</span><span class="sxs-lookup"><span data-stu-id="6fb2e-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="6fb2e-131">Abra um prompt de comando como administrador e altere o diretório para a pasta onde você tinha AzCopy instalado..</span><span class="sxs-lookup"><span data-stu-id="6fb2e-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="6fb2e-132">Construa a linha de comando AzCopy para carregar os arquivos semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="6fb2e-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="6fb2e-p107">AzCopy /Source: " *o caminho completo para a pasta raiz na máquina local* " /Dest: " *URL contêiner até, mas não incluindo o?* " /DestSAS: " *restante da url de contêiner a? até o final* "/ S.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p107">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*  " /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="6fb2e-135">Por exemplo, usando estes valores:</span><span class="sxs-lookup"><span data-stu-id="6fb2e-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="6fb2e-136">pasta raiz - C:\Collected dados</span><span class="sxs-lookup"><span data-stu-id="6fb2e-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="6fb2e-137">url de contêiner - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;si = NonOfficeData15 %7 C 0&amp;sig = % Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA 3D</span><span class="sxs-lookup"><span data-stu-id="6fb2e-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="6fb2e-138">a sintaxe de linha de comando AzCopy seria:</span><span class="sxs-lookup"><span data-stu-id="6fb2e-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="6fb2e-139">Para obter mais informações sobre Azcopy sintaxe consulte, [transferir dados com o AzCopy no Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span><span class="sxs-lookup"><span data-stu-id="6fb2e-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6fb2e-140">Deve haver uma pasta de raiz por usuário e o nome da pasta deve estar no formato *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="6fb2e-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="6fb2e-p108">Depois que as pastas terminar de carregar, volte para a descoberta eletrônica avançada. O conteúdo nas pastas que você carregou está pronto para ser processado no eDiscovery avançado. Selecione o contêiner e clique no botão de processo. Para obter mais detalhes sobre o eDiscovery avançado processamento ver, [execute o módulo de processo e carregar dados no eDiscovery avançadas do Office 365](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p108">Once the folders have finished uploading, switch back to Advanced eDiscovery. The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery. Select the container and click the Process button. For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6fb2e-p109">Depois que o contêiner é processado com êxito no eDiscovery avançado, você não mais poderá adicionar novo conteúdo para o armazenamento SAS no Windows Azure. Se você coletar conteúdo adicional e deseja adicioná-lo ao caso para análise de descoberta eletrônica avançado, você deve criar um novo contêiner de **dados de não-Office 365** e repita esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-p109">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure. If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="6fb2e-147">Se o contêiner *não processará com êxito devido a problemas de nomenclatura de pasta* e, em seguida, corrigir os problemas, você ainda precisará criar um novo contêiner e reconecte e carregar novamente usando os procedimentos neste artigo.</span><span class="sxs-lookup"><span data-stu-id="6fb2e-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span> 
  

