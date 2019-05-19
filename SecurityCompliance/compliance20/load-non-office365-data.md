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
description: ''
ms.openlocfilehash: 86d858994f95176ea4d415405c4043f7e7c5308e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155003"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="95f55-102">Carregar dados que não sejam do Office 365 em um conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="95f55-102">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="95f55-103">Nem todos os documentos que você pode precisar analisar com a descoberta eletrônica avançada do Office 365 residirão no Office 365.</span><span class="sxs-lookup"><span data-stu-id="95f55-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="95f55-104">Com o recurso de importação de conteúdo não-Office 365 na descoberta eletrônica avançada, é possível carregar documentos que não residem no Office 365 em um conjunto de revisão para que seja analisado com a descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="95f55-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a review set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="95f55-105">Este procedimento mostra como trazer documentos não-Office 365 para a descoberta eletrônica avançada para análise.</span><span class="sxs-lookup"><span data-stu-id="95f55-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="95f55-106">A descoberta eletrônica avançada requer um Office 365 E3 com o complemento de conformidade avançada ou uma assinatura E5 para sua organização.</span><span class="sxs-lookup"><span data-stu-id="95f55-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="95f55-107">Se você não tiver esse plano e quiser tentar a descoberta eletrônica avançada, poderá se inscrever para uma avaliação do Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="95f55-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="95f55-108">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="95f55-108">Before you begin</span></span>

<span data-ttu-id="95f55-109">O uso do recurso de upload que não é do Office 365 conforme descrito neste artigo requer que você tenha o seguinte:</span><span class="sxs-lookup"><span data-stu-id="95f55-109">Using the upload Non-Office 365 feature as described in this article requires that you have the following:</span></span>

- <span data-ttu-id="95f55-110">Uma assinatura do Office 365 ou do Microsoft 365 E5 ou uma assinatura E3 com a assinatura de complemento de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="95f55-110">An Office 365 or Microsoft 365 E5 subscription or an E3 subscription with the Advanced Compliance add-on subscription.</span></span>

- <span data-ttu-id="95f55-111">Todos os responsáveis cujo conteúdo que não seja do Office 365 será carregado deverá ter a licença E3 com uma licença de complemento de conformidade avançada ou ter uma licença e5.</span><span class="sxs-lookup"><span data-stu-id="95f55-111">All custodians whose non-Office 365 content will be uploaded must have E3 license with an Advanced Compliance add-on license or have an E5 license.</span></span>

- <span data-ttu-id="95f55-112">Uma ocorrência de descoberta eletrônica avançada existente.</span><span class="sxs-lookup"><span data-stu-id="95f55-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="95f55-113">Os responsáveis devem ser adicionados à ocorrência antes de você carregar os dados que não são do Office 365 associados a eles.</span><span class="sxs-lookup"><span data-stu-id="95f55-113">Custodians must be added to the case before you upload the non-Office 365 data that's associated to them.</span></span>

- <span data-ttu-id="95f55-114">Todos os arquivos que serão carregados devem estar localizados em pastas, onde cada pasta é associada a um determinado local.</span><span class="sxs-lookup"><span data-stu-id="95f55-114">All files that will be uploaded must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="95f55-115">Os nomes dessas pastas devem usar o seguinte formato de nomenclatura: *alias @ nome_do_domínio*.</span><span class="sxs-lookup"><span data-stu-id="95f55-115">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="95f55-116">O *alias @ nome_do_domínio* deve ser o alias e o domínio do Office 365 do usuário.</span><span class="sxs-lookup"><span data-stu-id="95f55-116">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="95f55-117">Você pode coletar todas as pastas *alias @* DomainName em uma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="95f55-117">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="95f55-118">A pasta raiz pode conter apenas as pastas *alias @* DomainName; arquivos soltos não são permitidos na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="95f55-118">The root folder can only contain the *alias@domainname* folders; loose files aren't allowed in the root folder.</span></span>

   <span data-ttu-id="95f55-119">Por exemplo, a estrutura de pastas dos dados não-Office 365 que você deseja carregar seria semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="95f55-119">For example, the folder structure for the non-Office 365 data that you want to upload would be similar to the following:</span></span>

   - <span data-ttu-id="95f55-120">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="95f55-120">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="95f55-121">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="95f55-121">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="95f55-122">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="95f55-122">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="95f55-123">Onde abraham.mcmahon@contoso.com, jewell.gordon@contoso.com e staci.gonzalez@contoso.com são os endereços SMTP dos responsáveis no caso.</span><span class="sxs-lookup"><span data-stu-id="95f55-123">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Estrutura de pastas de carregamento de dados não-Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="95f55-125">Uma conta que seja um Gerenciador de descoberta eletrônica ou administrador de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="95f55-125">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>

- <span data-ttu-id="95f55-126">Ferramentas de armazenamento do Microsoft Azure instaladas em um computador que tem acesso à estrutura de pasta de conteúdo não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="95f55-126">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="95f55-127">Instale o AzCopy, que pode ser feito aqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="95f55-127">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="95f55-128">Carregar conteúdo que não seja do Office 365 na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="95f55-128">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="95f55-129">Como um gerente de descoberta eletrônica ou administrador de descoberta eletrônica, abra a descoberta eletrônica avançada e, em seguida, o caso em que os dados que não sejam do Office 365 serão carregados.</span><span class="sxs-lookup"><span data-stu-id="95f55-129">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="95f55-130">Clique na guia **conjuntos de revisão** e selecione o conjunto de revisão para o qual você deseja carregar os dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="95f55-130">Click the **review sets** tab, then select the review set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="95f55-131">Se você ainda não criou um conjunto de revisão, é possível fazer isso agora.</span><span class="sxs-lookup"><span data-stu-id="95f55-131">If you have not already created a review set, you can do so now.</span></span>  <span data-ttu-id="95f55-132">Por fim, clique em **gerenciar o conjunto de revisão** e, em seguida, clique em **Exibir carregamentos** no bloco de dados \* \* não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="95f55-132">Finally, click **Manage review set** and then click **View uploads** in the \*\*Non-Office 365 data tile.</span></span>

2. <span data-ttu-id="95f55-133">Clique no botão **carregar arquivos** para iniciar o assistente de importação de dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="95f55-133">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

   ![Carregar arquivos](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="95f55-135">A primeira etapa no assistente simplesmente prepara um blob do Azure seguro para os arquivos a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="95f55-135">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="95f55-136">Após a conclusão da preparação, clique no botão **próximo: carregar arquivos** .</span><span class="sxs-lookup"><span data-stu-id="95f55-136">Once preparation is completed, click the **Next: Upload files** button.</span></span>

   ![Não-Office 365 Import-Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="95f55-138">Na etapa **carregar arquivos** , especifique o **caminho para o local dos arquivos**, onde os dados não-Office 365 que você planeja importar estão localizados.</span><span class="sxs-lookup"><span data-stu-id="95f55-138">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="95f55-139">Definir o local correto garante que o comando AzCopy seja atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="95f55-139">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

   > [!NOTE]
   > <span data-ttu-id="95f55-140">Se você ainda não tiver instalado o AzCopy, poderá fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="95f55-140">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="95f55-141">Copie o comando predefinido clicando no link **copiar para a área de transferência** .</span><span class="sxs-lookup"><span data-stu-id="95f55-141">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="95f55-142">Inicie um prompt de comando do Windows, Cole o comando e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="95f55-142">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="95f55-143">Os arquivos serão carregados para o armazenamento de blob do Azure seguro para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="95f55-143">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

   ![Arquivos não-Office 365 Import-upload](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Importação de AzCopy não-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="95f55-146">Se o comando AzCopy fornecido falhar, consulte [solucionar problemas de AzCopy na descoberta eletrônica avançada](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="95f55-146">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="95f55-147">Por fim, volte para a conformidade do & de segurança e clique no botão **próximo: processar arquivos** .</span><span class="sxs-lookup"><span data-stu-id="95f55-147">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="95f55-148">Isso iniciará o processamento, a extração de texto e a indexação de arquivos carregados.</span><span class="sxs-lookup"><span data-stu-id="95f55-148">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="95f55-149">Você pode acompanhar o progresso do processamento aqui ou na guia **trabalhos** .  Depois de concluído, os novos arquivos estarão disponíveis no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="95f55-149">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the review set.</span></span>  <span data-ttu-id="95f55-150">Quando o processamento estiver concluído, você poderá ignorar o assistente.</span><span class="sxs-lookup"><span data-stu-id="95f55-150">Once processing is complete, you can dismiss the wizard.</span></span>

   ![Arquivos de processo de importação e não-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

