---
title: Indexação dos dados dos responsáveis avançada
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
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607306"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="3957f-102">Indexação dos dados dos responsáveis avançada</span><span class="sxs-lookup"><span data-stu-id="3957f-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="3957f-p101">Quando um funcionário encarregado é adicionado a um caso de eDiscovery avançado (Preview), qualquer conteúdo no Office 365 foi considerada como parcialmente indexado é re-processado para torná-la totalmente pesquisável.  Esse processo é chamado de *indexação avançada*. O conteúdo pode ser indexado parcialmente para vários motivos, inclusive a existência de imagens, tipos de arquivo incompatíveis ou quando os limites de tamanho de arquivo indexação forem encontrados.  Para saber mais sobre itens indexados parcialmente, consulte [parcialmente indexados itens na pesquisa de conteúdo no Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="3957f-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="3957f-107">Exibição de resultados avançados de indexação</span><span class="sxs-lookup"><span data-stu-id="3957f-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="3957f-p102">Quando o processo de indexação avançado for concluído, você pode obter uma compreensão da eficácia do processamento novamente.  Na exibição de indexação dos responsáveis, o gráfico lista todos os itens adicionados ao *índice híbrida*.  O índice de híbrido é onde o eDiscovery avançado (Preview) armazena o conteúdo de re-processado.</span><span class="sxs-lookup"><span data-stu-id="3957f-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="3957f-p103">O gráfico também inclui o número de itens que exigem remediação e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [correção de erro durante o processamento de dados](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="3957f-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="3957f-113">Atualização de índices avançadas para responsáveis</span><span class="sxs-lookup"><span data-stu-id="3957f-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="3957f-p104">Quando um funcionário encarregado é adicionado a um caso de eDiscovery avançado (Preview), todos os itens indexados parcialmente são processados novamente. No entanto, como passar do tempo, itens indexados mais parcialmente podem ser adicionados à caixa de correio de um usuário ou conta de OneDrive.  Quando necessário, você poderá atualizar os índices.</span><span class="sxs-lookup"><span data-stu-id="3957f-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="3957f-p105">Atualização de índices dos responsáveis é um processo em tempo de execução. É recomendável que você não atualizar índices mais de uma vez por dia em um caso.</span><span class="sxs-lookup"><span data-stu-id="3957f-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
