---
title: Configurar marcas inteligentes para detecção de privilégio de cliente de advogado na descoberta eletrônica avançada
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153963"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="fdb4f-102">Configurar marcas inteligentes para revisão assistida por ML na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="fdb4f-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="fdb4f-103">Os recursos de aprendizado de máquina em descoberta eletrônica avançada têm como objetivo ajudar a tornar o processo de decisão sobre os documentos de forma mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="fdb4f-104">Marcas inteligentes é uma maneira de trazer os recursos de aprendizado de máquina para onde as decisões são registradas: marcas e grupos de marcas.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="fdb4f-105">Quando você cria um grupo de marcas inteligentes, as decisões do modelo ML mapeados para o grupo serão mostradas em linha com as marcas no grupo para ajudá-lo a ver as informações em linha, onde fazem a maioria dos sentidos de forma contextual.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="fdb4f-106">Como configurar um grupo de marcas inteligentes</span><span class="sxs-lookup"><span data-stu-id="fdb4f-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="fdb4f-107">Em um conjunto de revisão, vá para **gerenciar análise configurar** -> **gerenciar marcas**.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="fdb4f-108">Clique na lista suspensa ao lado de **Adicionar grupo de marcas** e selecione **Adicionar grupo de marcas inteligentes**.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="fdb4f-109">Selecione o modelo que você deseja mapear para este grupo.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="fdb4f-110">Isso criará uma seção de marca e N marcas filhas, onde N é o número de saídas possíveis do modelo.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="fdb4f-111">Por exemplo, o modelo de detecção de privilégio de cliente de advogados tem dois possíveis resultados-privilegiados e não privilegiados; selecionar esse modelo criará duas marcas filhas no conjunto de revisão, cada uma delas correspondente a uma das possíveis saídas.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="fdb4f-112">Renomeie o grupo de marcas e as marcas conforme você vê ajustar.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="fdb4f-113">Como usar um grupo de marcas inteligentes</span><span class="sxs-lookup"><span data-stu-id="fdb4f-113">How to use a smart tag group</span></span>

<span data-ttu-id="fdb4f-114">Ao revisar um documento, os resultados do modelo serão expostos ao lado do valor de marca apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="fdb4f-115">Por exemplo, se você tiver um grupo de marcas inteligentes para detecção de privilégio de cliente de advogados e revisar um documento que o modelo decidiu ser potencialmente privilegiado, você verá o motivo para isso ao lado da marca apropriada.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="fdb4f-116">É importante observar que a marca não é aplicada automaticamente; para todos os efeitos e finalidades, as marcas dentro de um grupo de marcas inteligentes atuam exatamente como marcas normais, exceto pelo fato de que elas expõem os resultados do modelo ao lado, quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdb4f-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>