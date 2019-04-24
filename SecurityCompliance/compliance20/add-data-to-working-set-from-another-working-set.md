---
title: Adicionar dados de um conjunto de trabalho a outro conjunto de trabalho
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
ms.openlocfilehash: e9e34d112cb84c27fec35e752eb2bfcbfe3136a3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243421"
---
# <a name="add-data-to-a-working-set-from-another-working-set"></a><span data-ttu-id="1dbfd-102">Adicionar dados a um conjunto de trabalho de outro conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="1dbfd-102">Add data to a working set from another working set</span></span>
<span data-ttu-id="1dbfd-103">Em alguns casos, pode ser necessário distribuir uma parte dos documentos de um conjunto de trabalho e trabalhar com eles individualmente em outro conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-103">In some cases, it may be necessary to carve out a portion of documents from one working set and work with them individually in another working set.</span></span>  <span data-ttu-id="1dbfd-104">Isso é especialmente útil se você tiver escolhido conteúdo em um conjunto de trabalho e quiser executar a análise no subconjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-104">This is especially useful if you've culled content in a working set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="1dbfd-105">Use o fluxo de trabalho a seguir para adicionar conteúdo de um conjunto de trabalho a outro.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-105">Use the following workflow to add content from one working set to another.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="1dbfd-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="1dbfd-106">Before you start</span></span>
<span data-ttu-id="1dbfd-107">Antes de começar, você precisará criar um novo conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-107">Before you start, you'll need to create a new working set.</span></span>  <span data-ttu-id="1dbfd-108">Um novo conjunto de trabalho pode ser adicionado por meio da guia *conjuntos de trabalho* [saiba mais](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span><span class="sxs-lookup"><span data-stu-id="1dbfd-108">A new working set can be added through the *Working sets* tab [Learn more](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span></span>

## <a name="step-1-identify-content-to-add-to-another-working-set"></a><span data-ttu-id="1dbfd-109">Etapa 1: identificar o conteúdo a ser adicionado a outro conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="1dbfd-109">Step 1: Identify content to add to another working set</span></span>
<span data-ttu-id="1dbfd-110">Você pode adicionar conteúdo a um conjunto de trabalho selecionando emails e documentos na grade do documento ou todos os itens em um resultado de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-110">You can add content to a working set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="1dbfd-111">Se escolher Adicionar itens selecionados, selecione os itens e clique na lista suspensa *ação* e, em seguida, *adicione a outro conjunto de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-111">If choosing to add selected items, select the items and click the *Action* drop down then *Add to another working set*.</span></span>

![Adicionar a outro conjunto de trabalho](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-workings-set"></a><span data-ttu-id="1dbfd-113">Etapa 2: especificar as opções para adicionar a outro conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="1dbfd-113">Step 2: Specify options for adding to another workings set</span></span>
<span data-ttu-id="1dbfd-114">No submenu *Adicionar a outro conjunto de trabalho opções* , primeiro escolha o conjunto de trabalho ao qual você deseja adicionar os itens.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-114">In the *Add to another working set options* flyout, first choose the working set you want to add the items to.</span></span>  <span data-ttu-id="1dbfd-115">Escolha se deseja adicionar todos os resultados de pesquisa ou os itens selecionados.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-115">Choose whether to add All search results or Selected items.</span></span>  <span data-ttu-id="1dbfd-116">Informações adicionais fornecem opções para incluir todos os metadados dos itens e, por fim, se as marcas de documento devem ou não ser incluídas no novo conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1dbfd-116">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new working set.</span></span>  <span data-ttu-id="1dbfd-117">Após clicar em *OK* , um novo trabalho será criado para adicionar o conteúdo a um conjunto de trabalho, você poderá monitorar o andamento desse trabalho na guia [trabalhos](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) . ![adicionar a outro conjunto de trabalho](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span><span class="sxs-lookup"><span data-stu-id="1dbfd-117">After clicking *OK* a new job will be created to add the content to a working set, you can monitor the progress of that job in the [Jobs](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) tab. ![Add to another working set](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span></span>
