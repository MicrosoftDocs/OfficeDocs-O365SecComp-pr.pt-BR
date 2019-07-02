---
title: Configurar marcas inteligentes na descoberta eletrônica avançada
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
description: As marcas inteligentes permitem que você aplique os recursos de aprendizado da máquina ao revisar o conteúdo em uma ocorrência de descoberta eletrônica avançada. Use grupos de marcas inteligentes para exibir os resultados dos modelos de detecção de aprendizagem de máquina, como o modelo de privilégio de cliente advogado.
ms.openlocfilehash: 68b558cc2282cc388387f8d61825b9ee569ff32a
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703824"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a><span data-ttu-id="d4e81-104">Configurar marcas inteligentes na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="d4e81-104">Set up smart tags in Advanced eDiscovery</span></span>

<span data-ttu-id="d4e81-105">Os recursos do Machine Learning (ML) na descoberta eletrônica avançada podem ajudá-lo a tornar o processo de decisão mais eficiente ao revisar os documentos de caso em um conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="d4e81-105">Machine learning (ML) capabilities in Advanced eDiscovery can help you make the decision process more efficient when reviewing case documents in a review set.</span></span> <span data-ttu-id="d4e81-106">As marcas inteligentes são uma maneira de trazer os recursos de ML para onde as decisões são registradas: ao marcar documentos durante a revisão.</span><span class="sxs-lookup"><span data-stu-id="d4e81-106">Smart tags are a way to bring the ML capabilities to where the decisions are recorded: when tagging documents during review.</span></span> <span data-ttu-id="d4e81-107">Quando você cria um grupo de marcas inteligentes, as decisões que são o resultado do modelo ML que você associou ao grupo de marcas inteligentes são exibidas em linha com as marcas no grupo de marcas.</span><span class="sxs-lookup"><span data-stu-id="d4e81-107">When you create a smart tag group, then the decisions that are the result of the ML model that you've associated with the smart tag group are displayed in-line with the tags in the tag group.</span></span> <span data-ttu-id="d4e81-108">Isso ajuda a ver as informações de resultados de ML em linha quando você está examinando documentos específicos.</span><span class="sxs-lookup"><span data-stu-id="d4e81-108">This helps see the ML results information in-line when you're reviewing specific documents.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="d4e81-109">Como configurar um grupo de marcas inteligentes</span><span class="sxs-lookup"><span data-stu-id="d4e81-109">How to set up a smart tag group</span></span>

1. <span data-ttu-id="d4e81-110">Em um conjunto de revisão, clique em **gerenciar análise definida** e, em seguida, clique em **gerenciar marcas**.</span><span class="sxs-lookup"><span data-stu-id="d4e81-110">In a review set, click **Manage review set** and then click **Manage tags**.</span></span>

2. <span data-ttu-id="d4e81-111">Clique em **Adicionar grupo de marcas** e selecione **Adicionar grupo de marcas inteligentes**.</span><span class="sxs-lookup"><span data-stu-id="d4e81-111">Click **Add tag group** and then select **Add smart tag group**.</span></span>

3. <span data-ttu-id="d4e81-112">Selecione o modelo ML que você deseja associar ao grupo de marcas.</span><span class="sxs-lookup"><span data-stu-id="d4e81-112">Select the ML model that you want to associate to the tag group.</span></span>
    
   <span data-ttu-id="d4e81-113">Isso cria um grupo de marcas e *n* marcas filhas, onde *N* é o número de saídas possíveis do modelo.</span><span class="sxs-lookup"><span data-stu-id="d4e81-113">This creates a tag group and *N* child tags, where *N* is the number of possible outputs of the model.</span></span> <span data-ttu-id="d4e81-114">Por exemplo, o [modelo de detecção de privilégio de cliente advogado](attorney-privilege-detection.md) tem duas saídas possíveis:</span><span class="sxs-lookup"><span data-stu-id="d4e81-114">For example, the [attorney-client privilege detection model](attorney-privilege-detection.md) has two possible outputs:</span></span> 

   - <span data-ttu-id="d4e81-115">**Positivo** – use para marcar documentos que contenham conteúdo privilegiado pelo cliente advogado.</span><span class="sxs-lookup"><span data-stu-id="d4e81-115">**Positive** – Use to tag documents that contain attorney-client privileged content.</span></span>
   
   - <span data-ttu-id="d4e81-116">**Negativo** – use para marcar documentos que não contenham conteúdo privilegiado pelo cliente advogado.</span><span class="sxs-lookup"><span data-stu-id="d4e81-116">**Negative** – Use to tag documents that don't contain attorney-client privileged content.</span></span>
    
    <span data-ttu-id="d4e81-117">Se você selecionar este modelo, um grupo de marcas com duas marcas filhas será criado (uma marca filha denominada **positiva** e a outra chamada **negativa**) para o conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="d4e81-117">If you select this model, a tag group with two child tags is created (one child tag named **Positive** and the other named **Negative**) for the review set.</span></span> <span data-ttu-id="d4e81-118">Neste exemplo, cada marca filha corresponde a uma das possíveis saídas do modelo de detecção de privilégio de cliente advogado.</span><span class="sxs-lookup"><span data-stu-id="d4e81-118">In this example, each child tag corresponds to one of the possible outputs from the attorney-client privilege detection model.</span></span>

4. <span data-ttu-id="d4e81-119">Opcionalmente, você pode renomear o grupo de marcas e as marcas filhas.</span><span class="sxs-lookup"><span data-stu-id="d4e81-119">Optionally, you can rename the tag group and the child tags.</span></span> <span data-ttu-id="d4e81-120">Por exemplo, você pode renomear a marca \*\*\*\* **positiva** como privilegiada e a marca **negativa** como **não privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="d4e81-120">For example, you could rename the **Positive** tag to **Privileged** and the **Negative** tag to **Not privileged**.</span></span>

## <a name="how-to-use-smart-tags"></a><span data-ttu-id="d4e81-121">Como usar marcas inteligentes</span><span class="sxs-lookup"><span data-stu-id="d4e81-121">How to use smart tags</span></span>

<span data-ttu-id="d4e81-122">Ao revisar um documento, os resultados do modelo são exibidos ao lado da marca filha apropriada.</span><span class="sxs-lookup"><span data-stu-id="d4e81-122">When reviewing a document, the model's results are displayed next to the appropriate child tag.</span></span> <span data-ttu-id="d4e81-123">Por exemplo, se você tiver um grupo de marcas inteligentes para detecção de privilégio de cliente de advogado e revisar um documento que é potencialmente privilegiado, o motivo para essa conclusão será exibido ao lado da marca apropriada.</span><span class="sxs-lookup"><span data-stu-id="d4e81-123">For example, if you have a smart tag group for attorney-client privilege detection and you review a document that is potentially privileged, the reason for that conclusion is displayed next to the appropriate tag.</span></span> <span data-ttu-id="d4e81-124">É importante observar que a marca não é automaticamente aplicada ao documento.</span><span class="sxs-lookup"><span data-stu-id="d4e81-124">It's important to note that the tag isn't automatically applied to the document.</span></span> <span data-ttu-id="d4e81-125">O revisor toma a decisão de como marcar o documento.</span><span class="sxs-lookup"><span data-stu-id="d4e81-125">The reviewer makes the decision about how to tag the document.</span></span>