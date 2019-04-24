---
title: Carregar dados do Office 365 em um conjunto de trabalho
ms.author: markjjo
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
ms.openlocfilehash: 2ac12cf8c447e3341724d9e853da0f32b7c232fb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242908"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="b3fb8-102">Carregar dados do Office 365 em um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="b3fb8-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="b3fb8-103">Nem todos os documentos que você pode precisar analisar com a descoberta eletrônica avançada do Office 365 residirão no Office 365.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="b3fb8-104">Com o recurso de importação de conteúdo não-Office 365 na descoberta eletrônica avançada, é possível carregar documentos que não residem no Office 365 em um conjunto de trabalho para que seja analisado com a descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="b3fb8-105">Este procedimento mostra como trazer documentos não-Office 365 para a descoberta eletrônica avançada para análise.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="b3fb8-106">A descoberta eletrônica avançada requer um Office 365 E3 com o complemento de conformidade avançada ou uma assinatura E5 para sua organização.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="b3fb8-107">Se você não tiver esse plano e quiser tentar a descoberta eletrônica avançada, poderá se inscrever para uma avaliação do Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b3fb8-108">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="b3fb8-108">Before you begin</span></span>
<span data-ttu-id="b3fb8-109">O uso do recurso de upload que não é do Office 365 conforme descrito neste procedimento exige que você tenha:</span><span class="sxs-lookup"><span data-stu-id="b3fb8-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="b3fb8-110">Um Office 365 E3 com um complemento de conformidade avançada ou uma assinatura e5.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="b3fb8-111">Todos os responsáveis cujo conteúdo que não seja do Office 365 será carregado precisarão ter E3 com o complemento de conformidade avançada ou com licenças e5.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="b3fb8-112">Uma ocorrência de descoberta eletrônica existente.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="b3fb8-113">Todos os arquivos para carregamento são coletados em pastas onde há uma pasta por responsáveis e o nome das pastas está neste formato *alias @ nome_do_domínio* .</span><span class="sxs-lookup"><span data-stu-id="b3fb8-113">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* .</span></span> <span data-ttu-id="b3fb8-114">O *alias @ nome_do_domínio* deve ser Users Office 365 alias and Domain.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-114">The *alias@domainname* must be users Office 365 alias and domain.</span></span> <span data-ttu-id="b3fb8-115">Você pode coletar todas as pastas *alias @* DomainName em uma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-115">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="b3fb8-116">A pasta raiz pode conter apenas as pastas *alias @* DomainName, não deve haver arquivos soltos na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-116">The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

   <span data-ttu-id="b3fb8-117">A estrutura de pastas para os dados que não são do Office 365 que você planeja carregar deve ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3fb8-117">The folder structure for the non-Office 365 data you plan to upload should look something like the following:</span></span>

   - <span data-ttu-id="b3fb8-118">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b3fb8-118">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="b3fb8-119">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b3fb8-119">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="b3fb8-120">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b3fb8-120">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="b3fb8-121">Onde abraham.mcmahon@contoso.com, jewell.gordon@contoso.com e staci.gonzalez@contoso.com são endereços SMTP dos responsáveis no caso.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-121">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are SMTP addresses of custodians in the case.</span></span>

![Estrutura de pastas de carregamento de dados não-Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="b3fb8-123">Uma conta que seja um Gerenciador de descoberta eletrônica ou ferramentas de armazenamento do Microsoft Azure administrador instaladas em um computador que tenha acesso à estrutura de pasta de conteúdo não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-123">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="b3fb8-124">Instale o AzCopy, que pode ser feito aqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="b3fb8-124">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="b3fb8-125">Carregar conteúdo que não seja do Office 365 na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="b3fb8-125">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="b3fb8-126">Como um gerente de descoberta eletrônica ou administrador de descoberta eletrônica, abra a descoberta eletrônica avançada e, em seguida, o caso em que os dados que não sejam do Office 365 serão carregados.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-126">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="b3fb8-127">Clique na guia **conjuntos de trabalho** e selecione o conjunto de trabalho para o qual você deseja carregar os dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-127">Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="b3fb8-128">Se você ainda não criou um conjunto de trabalho, você pode fazer isso agora.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-128">If you have not already created a working set, you can do so now.</span></span>  <span data-ttu-id="b3fb8-129">Por fim, clique em **gerenciar conjunto de trabalho** e, em seguida, **exiba** os carregamentos na seção dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-129">Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section.</span></span>

2. <span data-ttu-id="b3fb8-130">Clique no botão **carregar arquivos** para iniciar o assistente de importação de dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-130">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Carregar arquivos](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="b3fb8-132">A primeira etapa no assistente simplesmente prepara um blob do Azure seguro para os arquivos a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-132">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="b3fb8-133">Após a conclusão da preparação, clique no botão **próximo: carregar arquivos** .</span><span class="sxs-lookup"><span data-stu-id="b3fb8-133">Once preparation is completed, click the **Next: Upload files** button.</span></span>

![Não-Office 365 Import-Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="b3fb8-135">Na etapa **carregar arquivos** , especifique o **caminho para o local dos arquivos**, onde os dados não-Office 365 que você planeja importar estão localizados.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-135">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="b3fb8-136">Definir o local correto garante que o comando AzCopy seja atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-136">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="b3fb8-137">Se você ainda não tiver instalado o AzCopy, poderá fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="b3fb8-137">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="b3fb8-138">Copie o comando predefinido clicando no link **copiar para a área de transferência** .</span><span class="sxs-lookup"><span data-stu-id="b3fb8-138">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="b3fb8-139">Inicie um prompt de comando do Windows, Cole o comando e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-139">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="b3fb8-140">Os arquivos serão carregados para o armazenamento de blob do Azure seguro para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-140">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Arquivos não-Office 365 Import-upload](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importação de AzCopy não-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

> [!NOTE]
> <span data-ttu-id="b3fb8-143">Se o comando AzCopy fornecido falhar, consulte [solucionar problemas de AzCopy na descoberta eletrônica avançada (versão prévia)](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="b3fb8-143">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="b3fb8-144">Por fim, volte para a conformidade do & de segurança e clique no botão **próximo: processar arquivos** .</span><span class="sxs-lookup"><span data-stu-id="b3fb8-144">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="b3fb8-145">Isso iniciará o processamento, a extração de texto e a indexação de arquivos carregados.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-145">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="b3fb8-146">Você pode acompanhar o progresso do processamento aqui ou na guia **trabalhos** .  Depois de concluído, os novos arquivos estarão disponíveis no conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-146">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.</span></span>  <span data-ttu-id="b3fb8-147">Quando o processamento estiver concluído, você poderá ignorar o assistente.</span><span class="sxs-lookup"><span data-stu-id="b3fb8-147">Once processing is complete, you can dismiss the wizard.</span></span>

![Arquivos de processo de importação e não-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

