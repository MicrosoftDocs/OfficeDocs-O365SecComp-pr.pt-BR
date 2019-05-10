---
title: Configurar detecção de privilégio de cliente de advogado na descoberta eletrônica avançada
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835061"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="5414f-102">Configurar a detecção de privilégio de cliente de advogado (visualização) na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="5414f-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="5414f-103">Um aspecto importante e dispendioso da parte de revisão de qualquer processo de descoberta é a análise de conteúdo privilegiado.</span><span class="sxs-lookup"><span data-stu-id="5414f-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="5414f-104">A descoberta eletrônica avançada fornece uma detecção baseada em AI de conteúdo privilegiado no seu caso, para que você possa tornar esse processo mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="5414f-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="5414f-105">Como este recurso está atualmente na versão beta, um administrador de descoberta eletrônica precisa optar pelo recurso para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5414f-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="5414f-106">Como funciona?</span><span class="sxs-lookup"><span data-stu-id="5414f-106">How does it work?</span></span>

<span data-ttu-id="5414f-107">Com o recurso ativado, quando você analisa um conjunto de revisão em um caso, todos os documentos são executados por meio do modelo de detecção de privilégio de cliente advogado.</span><span class="sxs-lookup"><span data-stu-id="5414f-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="5414f-108">O modelo examina duas coisas:</span><span class="sxs-lookup"><span data-stu-id="5414f-108">The model looks at two things:</span></span>

- <span data-ttu-id="5414f-109">Conteúdo: o modelo ML determina a probabilidade de que o conteúdo do documento seja legal por natureza.</span><span class="sxs-lookup"><span data-stu-id="5414f-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="5414f-110">Participantes: se houver uma lista de advogados para o locatário, o modelo compara os participantes do documento com a lista para determinar se o documento tem pelo menos um participante advogado.</span><span class="sxs-lookup"><span data-stu-id="5414f-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="5414f-111">O modelo produz três valores para todos os documentos, que poderão ser pesquisados em um conjunto de revisão:</span><span class="sxs-lookup"><span data-stu-id="5414f-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="5414f-112">Pontuação de conteúdo: a probabilidade de o documento ser legal por natureza (Pontuação entre 0 e 1)</span><span class="sxs-lookup"><span data-stu-id="5414f-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="5414f-113">O advogado é verdadeiro se um dos participantes for encontrado na lista advogado carregado, caso contrário, false ou se não houver nenhuma lista de advogados.</span><span class="sxs-lookup"><span data-stu-id="5414f-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="5414f-114">Possivelmente privilegiado: true se a pontuação de conteúdo estiver acima do limite ou tiver um participante advogado; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="5414f-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="5414f-115">Optando por detecção de privilégio de cliente advogado</span><span class="sxs-lookup"><span data-stu-id="5414f-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="5414f-116">Etapa 1: optar pela detecção de privilégio de cliente do advogado (administrador de descoberta eletrônica)</span><span class="sxs-lookup"><span data-stu-id="5414f-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="5414f-117">Como a detecção de privilégio de cliente do advogado é um recurso de visualização, o administrador de descoberta eletrônica precisa optar por permitir que o recurso fique disponível em seus casos.</span><span class="sxs-lookup"><span data-stu-id="5414f-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="5414f-118">Vá para "configurar recursos experimentais" da página de descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="5414f-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="5414f-119">Clique em "gerenciar detecção de privilégio de cliente do advogado".</span><span class="sxs-lookup"><span data-stu-id="5414f-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="5414f-120">Clique no botão de alternância para ativar o recurso.</span><span class="sxs-lookup"><span data-stu-id="5414f-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="5414f-121">Etapa 2: carregar uma lista de advogados (opcional)</span><span class="sxs-lookup"><span data-stu-id="5414f-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="5414f-122">Para aproveitar ao máximo a detecção de privilégio de cliente de advogado, recomendamos fornecer uma lista de endereços de email de advogados ou pessoas jurídicas que trabalham na empresa.</span><span class="sxs-lookup"><span data-stu-id="5414f-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="5414f-123">A lista deve ser um CSV sem cabeçalho, com um endereço de email por linha.</span><span class="sxs-lookup"><span data-stu-id="5414f-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="5414f-124">Aproveitamento da detecção de privilégio de cliente do advogado</span><span class="sxs-lookup"><span data-stu-id="5414f-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="5414f-125">Etapa 1: analisar um conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="5414f-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="5414f-126">Quando você analisa o conjunto de análise, a detecção de privilégio de cliente também será executada.</span><span class="sxs-lookup"><span data-stu-id="5414f-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="5414f-127">Para saber mais sobre a análise de dados no conjunto de revisão, consulte [analisar dados em uma revisão definida em descoberta eletrônica avançada](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="5414f-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="5414f-128">Etapa 2: criar um grupo de marcas inteligentes com modelo de detecção de privilégio de cliente advogado</span><span class="sxs-lookup"><span data-stu-id="5414f-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="5414f-129">Uma das principais maneiras de consumir os resultados da detecção de privilégio de cliente de advogados no processo de revisão é usar um grupo de marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5414f-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="5414f-130">Os grupos de marcas inteligentes usam os resultados de um modelo de ML e mostram os resultados do modelo em linha ao lado das marcas, para que você possa consumir facilmente os resultados do modelo, quando for relevante, e usar as marcas no processo de revisão, como faria com qualquer outra marca no painel de marcação.</span><span class="sxs-lookup"><span data-stu-id="5414f-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span>

- <span data-ttu-id="5414f-131">Em "gerenciar marcas", clique em "Adicionar seção de marca inteligente".</span><span class="sxs-lookup"><span data-stu-id="5414f-131">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="5414f-132">Selecione "detecção de privilégio de cliente advogado".</span><span class="sxs-lookup"><span data-stu-id="5414f-132">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="5414f-133">Você verá que um grupo de marcas e duas marcas, correspondendo aos possíveis resultados do modelo, foram criados.</span><span class="sxs-lookup"><span data-stu-id="5414f-133">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="5414f-134">Renomeie o grupo de marcas e as marcas conforme você vê o ajuste para sua análise.</span><span class="sxs-lookup"><span data-stu-id="5414f-134">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="5414f-135">Etapa 3: usar o grupo de marcas inteligentes para revisão de privilégio</span><span class="sxs-lookup"><span data-stu-id="5414f-135">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="5414f-136">Quando você revisar um documento, se o modelo tiver determinado que o documento é potencialmente privilegiado, a marca inteligente correspondente exibirá o resultado:</span><span class="sxs-lookup"><span data-stu-id="5414f-136">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="5414f-137">Se o documento tiver conteúdo que possa ser legal, um rótulo de "conteúdo legal" será exibido ao lado da marca inteligente correspondente.</span><span class="sxs-lookup"><span data-stu-id="5414f-137">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="5414f-138">Se o documento tiver um participante encontrado na lista de advogados carregados, um rótulo "advogado" será exibido ao lado da marca inteligente correspondente.</span><span class="sxs-lookup"><span data-stu-id="5414f-138">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>