---
title: Baixar trabalhos de exportação
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
ms.openlocfilehash: 904bc5f8a6d6cef937d55336e8f383957713769a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251875"
---
# <a name="download-export-jobs"></a><span data-ttu-id="f1677-102">Baixar trabalhos de exportação</span><span class="sxs-lookup"><span data-stu-id="f1677-102">Download export jobs</span></span>

<span data-ttu-id="f1677-103">Todos os dados exportados são adicionados a um blob do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1677-103">All exported data is added to a Microsoft Azure blob.</span></span> <span data-ttu-id="f1677-104">Isso fornece várias opções para lidar com a downstream dos dados.</span><span class="sxs-lookup"><span data-stu-id="f1677-104">This provides multiple options to handle the data downstream.</span></span> <span data-ttu-id="f1677-105">Há várias maneiras de acessar um blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1677-105">There are several ways to access an Azure blob.</span></span> <span data-ttu-id="f1677-106">Um método é usar o Gerenciador de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1677-106">One method is to use Azure Storage Explorer.</span></span> <span data-ttu-id="f1677-107">Este método oferece suporte a conexão simples, navegação e download.</span><span class="sxs-lookup"><span data-stu-id="f1677-107">This method supports simple connection, browsing and downloading.</span></span> <span data-ttu-id="f1677-108">Para obter mais informações, visite<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span><span class="sxs-lookup"><span data-stu-id="f1677-108">For more information, visit <https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span></span>

1.  <span data-ttu-id="f1677-109">Para baixar o conteúdo após a conclusão de um trabalho de exportação, vá para a guia exportar e selecione um trabalho de exportação.</span><span class="sxs-lookup"><span data-stu-id="f1677-109">To download content after an export job is complete, go to the Exports tab and select an export job.</span></span>

2.  <span data-ttu-id="f1677-110">Copie o texto na seção "locais" do submenu.</span><span class="sxs-lookup"><span data-stu-id="f1677-110">Copy the text in the “Locations” section of the flyout.</span></span>

![](../media/eDiscoExportJob.png)

3.  <span data-ttu-id="f1677-111">Abra o Azure Storage Explorer e clique no botão "conectar"</span><span class="sxs-lookup"><span data-stu-id="f1677-111">Open Azure Storage Explorer and click the “Connect” button</span></span>

![](../media/AzureStorageConnect.png)

4.  <span data-ttu-id="f1677-112">Selecione "usar um URI de assinatura de acesso compartilhado" e clique em avançar</span><span class="sxs-lookup"><span data-stu-id="f1677-112">Select “Use a shared access signature URI” and click next</span></span>

![](../media/AzureStorageConnect2.png)

5.  <span data-ttu-id="f1677-113">Cole o texto do local na caixa de texto URI e clique em avançar</span><span class="sxs-lookup"><span data-stu-id="f1677-113">Paste the Location text in the URI text box and click next</span></span>

![](../media/AzureStorageConnect3.png)

6.  <span data-ttu-id="f1677-114">Clique em conectar</span><span class="sxs-lookup"><span data-stu-id="f1677-114">Click Connect</span></span>

![](../media/AzureStorageConnect4.png)

<span data-ttu-id="f1677-115">Isso adicionará a exportação como um objeto nos contêineres de contas de armazenamento/serviços anexados por SAS/BLOB.</span><span class="sxs-lookup"><span data-stu-id="f1677-115">This will add the export as an object in Storage Accounts/SAS-Attached Services/Blob Containers.</span></span> <span data-ttu-id="f1677-116">Você poderá explorar a exportação e baixar todos ou partes da exportação.</span><span class="sxs-lookup"><span data-stu-id="f1677-116">You will be able to explore the export and download all or portions of the export.</span></span>

![](../media/AzureStorageConnect5.png)