---
title: Carregar dados que não sejam do Office 365 em um conjunto de revisão
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Importe dados que não sejam do Office 365 para uma análise definida em uma ocorrência de descoberta eletrônica avançada.
ms.openlocfilehash: 37f8c2a5c97452845152e2a12578b9d243ab6711
ms.sourcegitcommit: 82ee560bf3ac84079764cbb4a2d858c321f65145
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2019
ms.locfileid: "35840828"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="2b6ef-103">Carregar dados que não sejam do Office 365 em um conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="2b6ef-103">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="2b6ef-104">Nem todos os documentos que você precisa analisar na descoberta eletrônica avançada estão localizados no Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-104">Not all documents that you need to analyze in Advanced eDiscovery are located in Office 365.</span></span> <span data-ttu-id="2b6ef-105">Com o recurso de importação de dados não-Office 365 na descoberta eletrônica avançada, você pode carregar documentos que não estão localizados no Office 365 para um conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-105">With the non-Office 365 data import feature in Advanced eDiscovery, you can upload documents that aren't located in Office 365 to a review set.</span></span> <span data-ttu-id="2b6ef-106">Este artigo mostra como trazer documentos não-Office 365 para a descoberta eletrônica avançada para análise.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-106">This article shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="2b6ef-107">A descoberta eletrônica avançada requer uma assinatura do Microsoft 365 ou do Office 365 E5 para sua organização ou uma assinatura E3 com a assinatura de complemento de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-107">Advanced eDiscovery requires an Microsoft 365 or Office 365 E5 subscription for your organization or an E3 subscription with the Advanced Compliance add-on subscription.</span></span> <span data-ttu-id="2b6ef-108">Se você não tiver esse plano e quiser tentar a descoberta eletrônica avançada, poderá se inscrever para uma avaliação do Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-108">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2b6ef-109">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="2b6ef-109">Before you begin</span></span>

<span data-ttu-id="2b6ef-110">O uso do recurso de upload que não é do Office 365 descrito neste artigo requer que você tenha o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2b6ef-110">Using the upload non-Office 365 feature described in this article requires that you have the following:</span></span>

- <span data-ttu-id="2b6ef-111">Todos os responsáveis que você deseja associar o conteúdo não-Office 365 deve ser atribuído a uma licença E5 ou uma licença E3 com uma licença avançada de complemento de conformidade.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-111">All custodians that you want to associate non-Office 365 content to must be assigned an E5 license, or an E3 license with an Advanced Compliance add-on license.</span></span>

- <span data-ttu-id="2b6ef-112">Uma ocorrência de descoberta eletrônica avançada existente.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="2b6ef-113">Os responsáveis devem ser adicionados ao caso antes que você possa carregar e associar os dados não-Office 365 a eles.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-113">Custodians must be added to the case before you can upload and associate the non-Office 365 data to them.</span></span>

- <span data-ttu-id="2b6ef-114">Dados não-Office 365 devem ser um tipo de arquivo com suporte da descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-114">Non-Office 365 data must be a file type that's supported by Advanced eDiscovery.</span></span> <span data-ttu-id="2b6ef-115">Para saber mais, confira [tipos de arquivo com suporte na descoberta eletrônica avançada](supported-filetypes-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="2b6ef-115">For more information, see [Supported file types in Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span></span>

- <span data-ttu-id="2b6ef-116">Todos os arquivos carregados em um conjunto de revisão devem estar localizados em pastas, onde cada pasta é associada a um determinado local.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-116">All files that are uploaded to a review set must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="2b6ef-117">Os nomes dessas pastas devem usar o seguinte formato de nomenclatura: *alias @ nome_do_domínio*.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-117">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="2b6ef-118">O *alias @ nome_do_domínio* deve ser o alias e o domínio do Office 365 do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-118">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="2b6ef-119">Você pode coletar todas as pastas *alias @* DomainName em uma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-119">You can collect all the *alias@domainname* folders in a root folder.</span></span> <span data-ttu-id="2b6ef-120">A pasta raiz só pode conter as pastas *alias @* DomainName.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-120">The root folder can only contain the *alias@domainname* folders.</span></span> <span data-ttu-id="2b6ef-121">Não há suporte para arquivos soltos na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-121">Loose files in the root folder aren't supported.</span></span>

   <span data-ttu-id="2b6ef-122">A estrutura de pastas para os dados que não são do Office 365 que você deseja carregar seria semelhante ao exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="2b6ef-122">The folder structure for the non-Office 365 data that you want to upload would be similar to the following example:</span></span>

   - <span data-ttu-id="2b6ef-123">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b6ef-123">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="2b6ef-124">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b6ef-124">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="2b6ef-125">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b6ef-125">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="2b6ef-126">Onde abraham.mcmahon@contoso.com, jewell.gordon@contoso.com e staci.gonzalez@contoso.com são os endereços SMTP dos responsáveis no caso.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-126">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Estrutura de pastas de carregamento de dados não-Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="2b6ef-128">Uma conta atribuída ao grupo de função Gerenciador de descoberta eletrônica (e adicionada como administrador de descoberta eletrônica).</span><span class="sxs-lookup"><span data-stu-id="2b6ef-128">An account that is assigned to the eDiscovery Manager role group (and added as eDiscovery Administrator).</span></span>

- <span data-ttu-id="2b6ef-129">Ferramentas de armazenamento do Microsoft Azure instaladas em um computador que tem acesso à estrutura de pasta de conteúdo não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-129">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span> <span data-ttu-id="2b6ef-130">Para instalar o AzCopy, confira [introdução ao AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="2b6ef-130">To install AzCopy, see [Get started with AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span> <span data-ttu-id="2b6ef-131">Certifique-se de instalar o AzCopy no local padrão, que é **% ProgramFiles (x86)% \ Microsoft SDKs\Azure\AzCopy**.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-131">Be sure to install AzCopy in the default location, which is **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span></span>


## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="2b6ef-132">Carregar conteúdo que não seja do Office 365 na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="2b6ef-132">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="2b6ef-133">Como um gerente de descoberta eletrônica ou administrador de descoberta eletrônica, abra a descoberta eletrônica avançada e, em seguida, o caso em que os dados que não sejam do Office 365 serão carregados.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-133">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  

2. <span data-ttu-id="2b6ef-134">Clique em revisar **conjuntos**e selecione o conjunto de revisão para carregar os dados que não são do Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-134">Click **Review sets**, and then select the review set to upload the non-Office 365 data to.</span></span>  <span data-ttu-id="2b6ef-135">Se você não tiver um conjunto de revisão, você pode criar um.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-135">If you don't have a review set, you can create one.</span></span> 
 
3. <span data-ttu-id="2b6ef-136">No conjunto de revisão, clique em **gerenciar o conjunto de revisão**e, em seguida, clique em **Exibir carregamentos** no bloco de **dados não-Office 365** .</span><span class="sxs-lookup"><span data-stu-id="2b6ef-136">In the review set, click **Manage review set**, and then click **View uploads** on the **Non-Office 365 data** tile.</span></span>

4. <span data-ttu-id="2b6ef-137">Clique em **carregar arquivos** para iniciar o assistente de importação de dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-137">Click **Upload files** to start the Non-Office 365 data import wizard.</span></span>

   ![Carregar arquivos](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   <span data-ttu-id="2b6ef-139">A primeira etapa do assistente prepara um local de armazenamento do Azure seguro fornecido pela Microsoft para carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-139">The first step in the wizard prepares a secure Microsoft-provided Azure Storage location to upload the files to.</span></span>  <span data-ttu-id="2b6ef-140">Quando a preparação estiver concluída, o botão **Avançar: carregar arquivos** se tornará ativo.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-140">When the preparation is completed, the **Next: Upload files** button becomes active.</span></span>

   ![Importação não-Office 365: preparar](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. <span data-ttu-id="2b6ef-142">Clique em **Avançar: carregar arquivos**.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-142">Click **Next: Upload files**.</span></span>

6. <span data-ttu-id="2b6ef-143">Na página **carregar arquivos** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2b6ef-143">On the **Upload files** page, do the following:</span></span>

   ![Importação não-Office 365: carregar arquivos](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   <span data-ttu-id="2b6ef-145">a.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-145">a.</span></span> <span data-ttu-id="2b6ef-146">Na caixa **caminho para o local dos arquivos** , verifique ou digite o local da pasta raiz onde você armazenou os dados que não são do Office 365 que você deseja carregar.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-146">In the **Path to location of files** box, verify or type the location of the root folder where you've stored the non-Office 365 data you want to upload.</span></span> <span data-ttu-id="2b6ef-147">Por exemplo, para o local dos arquivos de exemplo mostrados na **seção antes de começar**, digite **%USERPROFILE\Downloads\nonO365**.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-147">For example, for the location of the example files shown in the **Before you begin section**, you would type **%USERPROFILE\Downloads\nonO365**.</span></span> <span data-ttu-id="2b6ef-148">Fornecer o local correto garante que o comando AzCopy exibido em caixa abaixo do caminho seja atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-148">Providing the correct location ensures the AzCopy command displayed in box under the path is properly updated.</span></span>

   <span data-ttu-id="2b6ef-149">b.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-149">b.</span></span> <span data-ttu-id="2b6ef-150">Clique em **copiar para área de transferência** para copiar o comando exibido na caixa.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-150">Click **Copy to clipboard** to copy the command that is displayed in the box.</span></span> <span data-ttu-id="2b6ef-151">Inicie um prompt de comando do Windows, Cole o comando e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-151">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="2b6ef-152">Os arquivos serão carregados para o armazenamento de blob do Azure seguro para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-152">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

7. <span data-ttu-id="2b6ef-153">Inicie um prompt de comando do Windows, Cole o comando copiado na etapa anterior e pressione **Enter** para iniciar o comando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-153">Start a Windows command prompt, paste the command that you copied in the previous step, and then press **Enter** to start the AzCopy command.</span></span>  <span data-ttu-id="2b6ef-154">Depois de iniciar o comando, os arquivos que não são do Office 365 serão carregados no local de armazenamento do Azure que foi preparado na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-154">After you start the command, the non-Office 365 files will be uploaded to the Azure Storage location that was prepared in step 4.</span></span>

   ![Importação não-Office 365: AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="2b6ef-156">Se o comando AzCopy fornecido falhar, consulte [solucionar problemas de AzCopy na descoberta eletrônica avançada](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="2b6ef-156">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

8. <span data-ttu-id="2b6ef-157">Volte para o centro de conformidade & segurança e clique em **Avançar: processar arquivos** no assistente.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-157">Go back to the Security & Compliance Center, and click **Next: Process files** in the wizard.</span></span>  <span data-ttu-id="2b6ef-158">Isso inicia o processamento, extração de texto e indexação de arquivos que não são do Office 365 que foram carregados no local de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-158">This initiates processing, text extraction, and indexing of the non-Office 365 files that were uploaded to the Azure Storage location.</span></span>  

9. <span data-ttu-id="2b6ef-159">Acompanhe o progresso do processamento de arquivos que não são do Office 365 na página **arquivos de processo** ou na guia **trabalhos** , exibindo um trabalho chamado **adicionando dados que não sejam 365 do Office a um conjunto de revisão**.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-159">Track the progress of processing the non-Office 365 files on the **Process files** page or on the **Jobs** tab by viewing a job named **Adding non-Office 365 data to a review set**.</span></span>  <span data-ttu-id="2b6ef-160">Depois que o trabalho for concluído, os novos arquivos estarão disponíveis no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-160">After the job is finished, the new files will be available in the review set.</span></span>

   ![Importação não-Office 365: processar arquivos](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. <span data-ttu-id="2b6ef-162">Depois que o processamento for concluído, você poderá fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="2b6ef-162">After the processing is finished, you can close the wizard.</span></span>