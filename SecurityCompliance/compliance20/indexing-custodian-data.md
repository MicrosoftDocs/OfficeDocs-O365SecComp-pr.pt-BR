---
title: Indexação avançada de dados de responsáveis
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218661"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="dacf3-102">Indexação avançada de dados de responsáveis</span><span class="sxs-lookup"><span data-stu-id="dacf3-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="dacf3-p101">Quando um qualificador é adicionado a um caso de descoberta eletrônica avançada (visualização), qualquer conteúdo no Office 365 que foi considerado parcialmente indexado é reprocessado para torná-lo totalmente pesquisável.  Esse processo é chamado de *indexAção avançada*. O conteúdo pode ser parcialmente indexado por vários motivos, incluindo a existência de imagens, tipos de arquivos não suportados ou quando são encontrados limites de tamanho de arquivo de indexação.  Para saber mais sobre itens parcialmente indexados, confira [itens parcialmente indexados na pesquisa de conteúdo no Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="dacf3-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="dacf3-107">Exibindo resultados avançados de indexação</span><span class="sxs-lookup"><span data-stu-id="dacf3-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="dacf3-p102">Após a conclusão do processo de indexação avançada, você pode entender a eficácia da reprocessamento.  No modo de exibição de indexação de responsáveis, o gráfico lista todos os itens adicionados ao *índice híbrido*.  O índice híbrido é onde a descoberta eletrônica avançada (visualização) armazena o conteúdo reprocessado.</span><span class="sxs-lookup"><span data-stu-id="dacf3-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="dacf3-p103">O gráfico também inclui o número de itens que exigem correção e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [Error remediation When Processing data](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="dacf3-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="dacf3-113">Atualizando índices avançados para os responsáveis</span><span class="sxs-lookup"><span data-stu-id="dacf3-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="dacf3-p104">Quando um responsáveis é adicionado a uma descoberta eletrônica avançada (visualização), todos os itens parcialmente indexados são processados novamente. No enTanto, à medida que o tempo passa, os itens mais parcialmente indexados podem ser adicionados à caixa de correio de um usuário ou a uma conta do OneDrive.  Quando necessário, você pode atualizar os índices.</span><span class="sxs-lookup"><span data-stu-id="dacf3-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="dacf3-p105">Atualizar os índices dos responsáveis é um processo de execução longa. É recomendável que você não atualize os índices mais de uma vez por dia em um caso.</span><span class="sxs-lookup"><span data-stu-id="dacf3-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
