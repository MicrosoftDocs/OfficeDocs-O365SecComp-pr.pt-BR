---
title: Adicionar dados de um conjunto de revisão para outro conjunto de revisão
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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527099"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="ae1a6-102">Adicionar dados a um conjunto de revisão de outro conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="ae1a6-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="ae1a6-103">Em alguns casos, pode ser necessário distribuir uma parte dos documentos de um conjunto de análise e trabalhar com eles individualmente em outro conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="ae1a6-104">Isso é especialmente útil se você tiver escolhido conteúdo em um conjunto de revisão e quiser executar a análise no subconjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="ae1a6-105">Use o fluxo de trabalho a seguir para adicionar conteúdo de uma análise definida para outra.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-105">Use the following workflow to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ae1a6-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="ae1a6-106">Before you begin</span></span>

<span data-ttu-id="ae1a6-107">Antes de começar, você precisará criar uma nova revisão configurada para adicionar os dados a.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="ae1a6-108">Um novo conjunto de revisão pode ser adicionado à guia **conjuntos de revisão** da ocorrência.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="ae1a6-109">Para obter mais informações, consulte [Manage Review sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="ae1a6-109">For more information, see [Manage review sets](managing-review-sets.md).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="ae1a6-110">Etapa 1: identificar o conteúdo a ser adicionado a outro conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="ae1a6-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="ae1a6-111">Você pode adicionar conteúdo a um conjunto de revisão selecionando emails e documentos na grade do documento ou todos os itens em um resultado de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-111">You can add content to a review set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="ae1a6-112">Se escolher Adicionar itens selecionados, selecione os itens, clique em **ação**e, em seguida, clique em **Adicionar a outro conjunto de revisão**.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-112">If choosing to add selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Adicionar a outro conjunto de revisão](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="ae1a6-114">Etapa 2: especificar as opções para adicionar a outro conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="ae1a6-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="ae1a6-115">Na página **Adicionar a outro conjunto de revisão** , escolha o conjunto de revisão ao qual você deseja adicionar os itens.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-115">In the **Add to another review set** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="ae1a6-116">Escolha se deseja adicionar **todos os resultados de pesquisa** ou os **itens selecionados**.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="ae1a6-117">Informações adicionais fornecem opções para incluir todos os metadados dos itens e, por fim, se as marcas de documento devem ou não ser incluídas no novo conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="ae1a6-117">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new review set.</span></span>  <span data-ttu-id="ae1a6-118">Após clicar em **OK** , um novo trabalho será criado para adicionar o conteúdo a um conjunto de revisão; Você pode monitorar o andamento desse trabalho na guia **trabalho** . Para obter mais informações, consulte [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="ae1a6-118">After clicking **Ok** a new job will be created to add the content to a review set; you can monitor the progress of that job on the **Job** tab. For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>

![Adicionar a outro conjunto de revisão](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
