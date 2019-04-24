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
# <a name="download-export-jobs"></a>Baixar trabalhos de exportação

Todos os dados exportados são adicionados a um blob do Microsoft Azure. Isso fornece várias opções para lidar com a downstream dos dados. Há várias maneiras de acessar um blob do Azure. Um método é usar o Gerenciador de armazenamento do Azure. Este método oferece suporte a conexão simples, navegação e download. Para obter mais informações, visite<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  Para baixar o conteúdo após a conclusão de um trabalho de exportação, vá para a guia exportar e selecione um trabalho de exportação.

2.  Copie o texto na seção "locais" do submenu.

![](../media/eDiscoExportJob.png)

3.  Abra o Azure Storage Explorer e clique no botão "conectar"

![](../media/AzureStorageConnect.png)

4.  Selecione "usar um URI de assinatura de acesso compartilhado" e clique em avançar

![](../media/AzureStorageConnect2.png)

5.  Cole o texto do local na caixa de texto URI e clique em avançar

![](../media/AzureStorageConnect3.png)

6.  Clique em conectar

![](../media/AzureStorageConnect4.png)

Isso adicionará a exportação como um objeto nos contêineres de contas de armazenamento/serviços anexados por SAS/BLOB. Você poderá explorar a exportação e baixar todos ou partes da exportação.

![](../media/AzureStorageConnect5.png)