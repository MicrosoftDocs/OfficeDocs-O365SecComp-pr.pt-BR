---
title: Carregar dados do Office 365 em um conjunto de trabalho
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
ms.openlocfilehash: 427b4c8c9dfffe351827a6869ae26a5356d646d8
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607346"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="25a8e-102">Carregar dados do Office 365 em um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="25a8e-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="25a8e-p101">Nem todos os documentos que você talvez precise analisar com eDiscovery avançadas do Office 365 residirá no Office 365. Com o conteúdo não-Office 365 importe recurso no eDiscovery avançado, que você pode carregar documentos que não live no Office 365 em um conjunto de trabalho para que ele é analisado com eDiscovery avançado. Esse procedimento mostra como trazer seus documentos do Office 365 para descoberta eletrônica avançada para análise.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="25a8e-p102">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá Inscrever-se para uma avaliação do Office 365 Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="25a8e-108">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="25a8e-108">Before you begin</span></span>
<span data-ttu-id="25a8e-109">Usando o recurso de upload Non-Office 365, conforme descrito neste procedimento requer que você tenha:</span><span class="sxs-lookup"><span data-stu-id="25a8e-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
* <span data-ttu-id="25a8e-110">Um Office 365 E3 com inscrição de E5 ou complemento de conformidade avançadas</span><span class="sxs-lookup"><span data-stu-id="25a8e-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
* <span data-ttu-id="25a8e-111">Todos os responsáveis cujo conteúdo não - Office 365 será carregado devem ter E3 com licenças de E5 ou complemento de conformidade avançadas</span><span class="sxs-lookup"><span data-stu-id="25a8e-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
* <span data-ttu-id="25a8e-112">Uma ocorrência de descoberta eletrônica existente</span><span class="sxs-lookup"><span data-stu-id="25a8e-112">An existing eDiscovery case</span></span>
* <span data-ttu-id="25a8e-p103">Todos os arquivos para carregar coletadas em pastas onde houver uma pasta por dos responsáveis e nome das pastas se situa este formato *alias@domainname* . O *alias@domainname* deve ser o domínio e alias de usuário Office 365. Você pode coletar todas as pastas de *alias@domainname* em uma pasta raiz. A pasta raiz pode conter apenas as pastas *alias@domainname* , não deve haver nenhum arquivo afastado na pasta raiz</span><span class="sxs-lookup"><span data-stu-id="25a8e-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder</span></span>
* <span data-ttu-id="25a8e-117">Uma conta que é uma gerente de descoberta eletrônica ou eDiscovery administrador Microsoft Azure armazenamento ferramentas instalado em um computador que tenha acesso na estrutura de pasta de conteúdo do Office 365.</span><span class="sxs-lookup"><span data-stu-id="25a8e-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>
* <span data-ttu-id="25a8e-118">Instalar AzCopy, você poderá fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="25a8e-118">Install AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="25a8e-119">Carregar o conteúdo do Office 365 em eDiscovery avançado</span><span class="sxs-lookup"><span data-stu-id="25a8e-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>
1. <span data-ttu-id="25a8e-p104">Como um gerente de descoberta eletrônica ou eDiscovery administrador, abra o eDiscovery avançada, em seguida, o caso em que os dados não - Office 365 serão carregados.  Clique na guia **conjuntos de trabalho** e selecione o conjunto de trabalho que você deseja carregar os dados não-Office 365.  Se você já não tiver criado um conjunto de trabalho, você poderá fazer isso agora.  Finalmente, clique em **Gerenciar funcionamento definido** e **carregamentos de modo de exibição** , na seção de dados não-Office 365</span><span class="sxs-lookup"><span data-stu-id="25a8e-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="25a8e-124">Clique no botão **carregar arquivos** para iniciar o Assistente de importação de dados não-Office 365.</span><span class="sxs-lookup"><span data-stu-id="25a8e-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Carregar arquivos](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="25a8e-p105">A primeira etapa do assistente simplesmente prepara um blob Azure seguro para os arquivos sejam carregados.  Após a preparação é compelted, clique no **próximo: carregar arquivos** botão.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Não-Office 365 importar - preparar](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="25a8e-p106">Na etapa **carregar arquivos** , especifique o **caminho para o local dos arquivos**, isso é onde os dados não-Office 365 que você planeja importando estão localizados.  Definir o local correto garante a AzCopy comando é atualizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="25a8e-131">Se você ainda não tiver instalado AzCopy, você pode fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="25a8e-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="25a8e-p107">Copie o comando predefinido clicando no link de **cópia para área de transferência** . Inicie um prompt de comando do windows, cole o comando e pressione enter.  Os arquivos serão carregados para o armazenamento de blob Azure segura para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Importação de não-Office 365 - carregar arquivos](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importação de não-Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="25a8e-p108">Finalmente, retorne à conformidade de & de segurança e clique no **próximo: processar arquivos** botão.  Isso iniciará o processamento, extração de texto e indexação dos arquivos carregados.  Você pode controlar o andamento do processamento aqui ou na guia **Jobs** .  Depois de concluído, os novos arquivos estarão disponíveis no conjunto de trabalho.  Depois que o processamento estiver concluído, você pode recusar o assistente.</span><span class="sxs-lookup"><span data-stu-id="25a8e-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Importação de não-Office 365 - processar arquivos](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

