---
title: Correção de erros durante o processamento de dados
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
description: ''
ms.openlocfilehash: efcee812b6082a7f7ee36e6aea0ecb7ed0243077
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36168119"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="3f375-102">Correção de erros durante o processamento de dados</span><span class="sxs-lookup"><span data-stu-id="3f375-102">Error remediation when processing data</span></span>

<span data-ttu-id="3f375-103">A correção de erros permite que os administradores de descoberta eletrônica corrijam problemas de dados que impedem a descoberta eletrônica avançada do processamento adequado do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3f375-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="3f375-104">Por exemplo, os arquivos protegidos por senha não podem ser processados, já que os arquivos são bloqueados ou criptografados.</span><span class="sxs-lookup"><span data-stu-id="3f375-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="3f375-105">Usando a correção de erros, os administradores de descoberta eletrônica podem baixar arquivos com esses erros, remover a proteção por senha e carregar os arquivos corrigidos.</span><span class="sxs-lookup"><span data-stu-id="3f375-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="3f375-106">Use o fluxo de trabalho a seguir para corrigir arquivos com erros em casos de descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="3f375-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="3f375-107">Criar uma sessão de correção de erro para corrigir arquivos com erros de processamento</span><span class="sxs-lookup"><span data-stu-id="3f375-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="3f375-108">Se o assistente de correção de erros for fechado a qualquer momento durante o procedimento a seguir, você poderá retornar à sessão de correção de erro na guia **processamento** selecionando as correções de **erro** no menu suspenso **Exibir** .</span><span class="sxs-lookup"><span data-stu-id="3f375-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="3f375-109">Na guia **processamento** em um caso de descoberta eletrônica avançada, selecione **erros** no menu suspenso **Exibir** .</span><span class="sxs-lookup"><span data-stu-id="3f375-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="3f375-110">Selecione os erros que você deseja corrigir clicando no botão de opção ao lado do tipo de erro ou tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3f375-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="3f375-111">No exemplo a seguir, estamos corrigindo um arquivo protegido por senha.</span><span class="sxs-lookup"><span data-stu-id="3f375-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="3f375-112">Clique em **nova correção de erro**.</span><span class="sxs-lookup"><span data-stu-id="3f375-112">Click **New error remediation**.</span></span>

    ![Correção de erro](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="3f375-114">A sessão de correção de erro começa com um estágio de preparação onde os arquivos com erros são copiados para um local de armazenamento do Azure fornecido pela Microsoft para que você possa baixá-los para o computador local para correção.</span><span class="sxs-lookup"><span data-stu-id="3f375-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Preparando correção de erro](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="3f375-116">Após a conclusão da preparação, clique em **Avançar: baixar arquivos** para continuar com o download.</span><span class="sxs-lookup"><span data-stu-id="3f375-116">After the preparation is complete, click **Next: Download files** to proceed with download.</span></span>

    ![Baixar arquivos](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="3f375-118">Para baixar arquivos, especifique o **caminho de destino para download**.</span><span class="sxs-lookup"><span data-stu-id="3f375-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="3f375-119">Este é um caminho no computador local onde o arquivo é baixado.</span><span class="sxs-lookup"><span data-stu-id="3f375-119">This is a path on your local computer where the file is downloaded.</span></span>  <span data-ttu-id="3f375-120">O caminho padrão,%USERPROFILE%\Downloads\errors, aponta para a pasta downloads do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="3f375-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="3f375-121">Você pode alterar esse caminho, se necessário.</span><span class="sxs-lookup"><span data-stu-id="3f375-121">You can change this path if necessary.</span></span> <span data-ttu-id="3f375-122">Se você alterar, recomendamos que você use um caminho de arquivo local para o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="3f375-122">If you do change it, we recommend that you use a local file path for the best performance.</span></span> <span data-ttu-id="3f375-123">Não use um caminho de rede remoto.</span><span class="sxs-lookup"><span data-stu-id="3f375-123">Don't use a remote network path.</span></span>

6. <span data-ttu-id="3f375-124">Copie o comando predefinido clicando em **copiar para área de transferência**.</span><span class="sxs-lookup"><span data-stu-id="3f375-124">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="3f375-125">Inicie um prompt de comando do Windows, Cole o comando e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="3f375-125">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="3f375-126">Os arquivos são baixados.</span><span class="sxs-lookup"><span data-stu-id="3f375-126">The files are downloaded.</span></span>

    ![Preparar para correção de erros](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="3f375-128">Você deve usar o AzCopy v 8.1 para usar com êxito o comando fornecido na página **baixar arquivos** .</span><span class="sxs-lookup"><span data-stu-id="3f375-128">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="3f375-129">Você também deve usar o AzCopy v 8.1 para carregar os arquivos na etapa 10 abaixo.</span><span class="sxs-lookup"><span data-stu-id="3f375-129">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="3f375-130">Para instalar esta versão do AzCopy, confira [transferir dados com o AzCopy v 8.1 no Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="3f375-130">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="3f375-131">Se o comando AzCopy fornecido falhar, confira [solucionar problemas de AzCopy na descoberta eletrônica avançada](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="3f375-131">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="3f375-132">Depois de baixar os arquivos, você pode corrigi-los com uma ferramenta apropriada.</span><span class="sxs-lookup"><span data-stu-id="3f375-132">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="3f375-133">Para arquivos protegidos por senha, várias ferramentas de quebra de senha podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="3f375-133">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="3f375-134">Se você souber as senhas dos arquivos, poderá abri-las e remover a proteção por senha.</span><span class="sxs-lookup"><span data-stu-id="3f375-134">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="3f375-135">É importante manter a estrutura de diretório e os nomes de arquivo dos arquivos corrigidos no tact.</span><span class="sxs-lookup"><span data-stu-id="3f375-135">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="3f375-136">Todas as convenções de nomenclatura usadas nas pastas e arquivos baixados tornam possível associar os arquivos do remdiated de volta ao original.</span><span class="sxs-lookup"><span data-stu-id="3f375-136">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="3f375-137">Agora, retorne à descoberta eletrônica avançada e clique em **Avançar: carregar arquivos**.</span><span class="sxs-lookup"><span data-stu-id="3f375-137">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="3f375-138">Isso passará para a próxima etapa, onde você pode agora carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="3f375-138">This will move to the next step where you can now upload the files.</span></span>

    ![Carregar arquivos](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="3f375-140">Especifique o local dos arquivos corrigidos na caixa de texto **caminho para o local de arquivos** e clique em **copiar para área de transferência**.</span><span class="sxs-lookup"><span data-stu-id="3f375-140">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="3f375-141">Cole o comando em um prompt de comando do Windows e pressione **Enter** para carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="3f375-141">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="3f375-143">Retorne à descoberta eletrônica avançada e clique em **Avançar: processar arquivos**.</span><span class="sxs-lookup"><span data-stu-id="3f375-143">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="3f375-144">Quando o processamento estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="3f375-144">When processing is complete.</span></span> <span data-ttu-id="3f375-145">Você pode retornar ao conjunto de revisão e ver o arquivo corrigido.</span><span class="sxs-lookup"><span data-stu-id="3f375-145">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="3f375-146">O que acontece quando os arquivos são corrigidos</span><span class="sxs-lookup"><span data-stu-id="3f375-146">What happens when files are remediated</span></span>

<span data-ttu-id="3f375-147">Quando os arquivos corrigidos são carregados, os metadados originais são preservados, exceto os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="3f375-147">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="3f375-148">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="3f375-148">ExtractedTextSize</span></span>
- <span data-ttu-id="3f375-149">HasText</span><span class="sxs-lookup"><span data-stu-id="3f375-149">HasText</span></span>
- <span data-ttu-id="3f375-150">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="3f375-150">IsErrorRemediate</span></span>
- <span data-ttu-id="3f375-151">Loadid</span><span class="sxs-lookup"><span data-stu-id="3f375-151">LoadId</span></span>
- <span data-ttu-id="3f375-152">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="3f375-152">ProcessingErrorMessage</span></span>
- <span data-ttu-id="3f375-153">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="3f375-153">ProcessingStatus</span></span>
- <span data-ttu-id="3f375-154">Texto</span><span class="sxs-lookup"><span data-stu-id="3f375-154">Text</span></span>
- <span data-ttu-id="3f375-155">WordCount</span><span class="sxs-lookup"><span data-stu-id="3f375-155">WordCount</span></span>
- <span data-ttu-id="3f375-156">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="3f375-156">WorkingsetId</span></span>

<span data-ttu-id="3f375-157">Para obter uma definição de todos os campos de metadados na descoberta eletrônica avançada, confira [campos de metadados do documento](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="3f375-157">For a definition of all metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
