---
title: Correção de erro durante o processamento de dados
ms.author: markjjo
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
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607376"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="8aa72-102">Correção de erro durante o processamento de dados</span><span class="sxs-lookup"><span data-stu-id="8aa72-102">Error remediation when processing data</span></span>

<span data-ttu-id="8aa72-p101">Correção de erro permite que administradores de descoberta eletrônica a capacidade corrigir problemas de dados que impedir a corretamente o conteúdo de processamento do eDiscovery avançado (Preview). Por exemplo, arquivos que são protegidas por senha não podem ser processados, desde que os arquivos estão bloqueados ou criptografados. Usando a correção de erro, os administradores de descoberta eletrônica podem fazer o download de arquivos com esses erros, remover a proteção por senha e carregar os arquivos remediados por teste.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="8aa72-106">Use o seguinte fluxo de trabalho para remediar arquivos com erros em casos de eDiscovery avançado (Preview).</span><span class="sxs-lookup"><span data-stu-id="8aa72-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="8aa72-107">Criando uma sessão de correção de erro para remediar arquivos com erros de processamento</span><span class="sxs-lookup"><span data-stu-id="8aa72-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="8aa72-108">Se o Assistente de correção de erro é fechado a qualquer momento durante o procedimento a seguir, é possível retornar para a sessão de correção de erro a partir da guia **processamento** selecionando **correções de erro** no menu suspenso **modo de exibição** .</span><span class="sxs-lookup"><span data-stu-id="8aa72-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="8aa72-109">Na guia **processamento** em um caso de eDiscovery avançado (Preview), selecione **erros** no menu suspenso **modo de exibição** .</span><span class="sxs-lookup"><span data-stu-id="8aa72-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="8aa72-p102">Selecione os erros que você deseja remediar clicando no botão de opção ao lado do tipo de erro ou um tipo de arquivo.  No exemplo a seguir, podemos estiver correção um arquivo de protegido por senha.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="8aa72-112">Clique em **+ novo correção de erro**.</span><span class="sxs-lookup"><span data-stu-id="8aa72-112">Click **+ New error remediation**.</span></span>

    ![Correção de erro](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="8aa72-114">A sessão de correção de erro será iniciada, começando com um estágio de preparação onde os arquivos ou com erros são movidos para um local seguro de Azure sejam baixados.</span><span class="sxs-lookup"><span data-stu-id="8aa72-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Preparando a correção de erro](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="8aa72-116">Após a preparação for concluída, clique em **próximo: baixar arquivos** para prosseguir com o download.</span><span class="sxs-lookup"><span data-stu-id="8aa72-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Baixar arquivos](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="8aa72-p103">Para baixar arquivos, especifique o **caminho de destino para download**; Este é um caminho no computador local onde o arquivo deve ser baixado.  O caminho padrão, % USERPROFILE%\Downloads\errors, aponta para a pasta de downloads do usuário registrado no; Isso pode ser alterado conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="8aa72-120">Recomendamos que você use um caminho de arquivo local, em vez de um caminho de rede remoto para um desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="8aa72-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8aa72-121">Se você não instalou AzCopy, você pode instalá-lo a partir daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="8aa72-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="8aa72-p104">Copie o comando predefinido, clicando em **Copiar para a área de transferência**. Inicie um prompt de comando do windows, cole o comando e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="8aa72-124">Os arquivos serão baixados.</span><span class="sxs-lookup"><span data-stu-id="8aa72-124">The files will be downloaded.</span></span>

    ![Preparando a correção de erro](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="8aa72-126">Se você tiver problemas ao executar esse comando, consulte https://go.microsoft.com/fwlink/?linkid=2038117 para dicas de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="8aa72-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="8aa72-p105">Depois de baixar os arquivos, você pode remediá-los com uma ferramenta adequada. Arquivos protegidos por senha, há um número de ferramentas que você pode usar para quebrar senhas. Se você souber as senhas para os arquivos, você pode abri-los e remover a proteção por senha.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="8aa72-p106">IT é importante que você mantenha os nomes de arquivo e a estrutura de diretório dos arquivos remediados por teste intacto.  Todas as convenções de nomenclatura usada nos arquivos baixados e pastas tornam possível associar os arquivos remdiated original.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="8aa72-p107">Agora, volte à eDiscovery avançado (Preview) e clique em **próximo: carregar arquivos**.  Isso moverá para a próxima etapa onde você agora pode carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![Carregar arquivos](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="8aa72-135">Especifique o local dos arquivos remediados por teste na caixa de texto **caminho para o local dos arquivos** , clique em **Copiar para clibpboard**.</span><span class="sxs-lookup"><span data-stu-id="8aa72-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="8aa72-136">Cole o comando em um Prompt de comando do Windows e pressione **Enter** para carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="8aa72-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="8aa72-138">Finalmente, volte à eDiscovery avançado (Preview) e clique em **próximo: processar arquivos**.</span><span class="sxs-lookup"><span data-stu-id="8aa72-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="8aa72-p108">Quando o processamento é concluído.  Você pode retornar ao conjunto de trabalho e consulte o arquivo remediados por teste.</span><span class="sxs-lookup"><span data-stu-id="8aa72-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="8aa72-141">O que acontece quando os arquivos são remediados</span><span class="sxs-lookup"><span data-stu-id="8aa72-141">What happens when files are remediated</span></span>

<span data-ttu-id="8aa72-142">Quando remediados por teste arquivos são carregados, os metadados original é preservado, com exceção dos seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="8aa72-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="8aa72-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="8aa72-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="8aa72-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="8aa72-144">ExtractedTextSize</span></span>
- <span data-ttu-id="8aa72-145">HasText</span><span class="sxs-lookup"><span data-stu-id="8aa72-145">HasText</span></span>
- <span data-ttu-id="8aa72-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="8aa72-146">IsErrorRemediate</span></span>
- <span data-ttu-id="8aa72-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="8aa72-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="8aa72-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="8aa72-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="8aa72-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="8aa72-149">LoadId</span></span>
- <span data-ttu-id="8aa72-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="8aa72-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="8aa72-151">Processamento</span><span class="sxs-lookup"><span data-stu-id="8aa72-151">ProcessingStatus</span></span>
- <span data-ttu-id="8aa72-152">Texto</span><span class="sxs-lookup"><span data-stu-id="8aa72-152">Text</span></span>
- <span data-ttu-id="8aa72-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="8aa72-153">WordCount</span></span>
- <span data-ttu-id="8aa72-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="8aa72-154">WorkingsetId</span></span>

<span data-ttu-id="8aa72-155">Para uma definição de todos os campos de metadados de documento no eDiscovery avançado (Preview), consulte [os campos de metadados de documento](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="8aa72-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>