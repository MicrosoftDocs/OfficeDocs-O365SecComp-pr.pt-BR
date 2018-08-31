---
title: Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Revise o funcionamento do documento semelhança valor, o nível mínimo de semelhança para dois arquivos a serem considerados perto duplicatas no eDiscovery avançadas do Office 365. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523885"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a><span data-ttu-id="44aac-103">Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="44aac-103">Understand document similarity in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="44aac-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="44aac-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="44aac-106">No eDiscovery avançado, semelhança de documento é o nível mínimo de semelhança necessário para dois documentos a serem considerados como perto duplicatas.</span><span class="sxs-lookup"><span data-stu-id="44aac-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="44aac-p102">Para a maioria dos aplicativos de negócios, é recomendável usar um valor de semelhança de 60% - 75%. Para material de reconhecimento óptico de caracteres (OCR) de péssima qualidade, valores de semelhança menores podem ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="44aac-p102">For most business applications, it is recommended to use a Similarity value of 60%-75%. For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44aac-109">Depois que ele tiver sido definida e executar para um determinado caso, o valor de semelhança não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="44aac-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="44aac-p103">Em um conjunto de duplicados Near (fim), pode haver documentos com um nível de semelhança abaixo do limiar de semelhança. Para um documento ingressar em um conjunto de término, deve haver pelo menos um documento no término definidas com um nível de semelhança excedendo a semelhança.</span><span class="sxs-lookup"><span data-stu-id="44aac-p103">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold. For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="44aac-112">Por exemplo, suponha a semelhança estiver definida como 80%, F1 do documento se parece com o documento F2 em um nível de 85% e documento F2 se parece com o documento F3 em um nível de 90%.</span><span class="sxs-lookup"><span data-stu-id="44aac-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="44aac-p104">No entanto, documento F1 pode se parecer com o documento F3 em um nível de apenas 70%, que está abaixo do limiar. No entanto, neste exemplo, documentos F1, F2 e F3 todos serão exibidos no término de um definido. Da mesma forma, usando um valor de semelhança de 80%, talvez criamos dois conjuntos, EquiSet-1 e EquiSet-2. EquiSet-1 contém documentos E1 e E2. Equiset-2 contém documentos F1, F2 e F3.</span><span class="sxs-lookup"><span data-stu-id="44aac-p104">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold. Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set. Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2. EquiSet-1 contains documents E1 and E2. Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="44aac-118">Os níveis de semelhança são ilustrados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="44aac-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Similaridade de documentos](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="44aac-p105">Suponha que a outro documento, X1, agora é inserido. A semelhança entre X1 e E3 é 87%. Da mesma forma, a semelhança entre X1 e F1 é 92%. Como resultado, o EquiSet -1, EquiSet -2 e X1 agora são combinados em um término definido.</span><span class="sxs-lookup"><span data-stu-id="44aac-p105">Assume that another document, X1, is now inserted. The resemblance between X1 and E3 is 87%. Similarly, the resemblance between X1 and F1 is 92%. As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Similaridade de documentos](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="44aac-125">Se qualquer dois documentos são atribuídos a um conjunto de término, eles permanecerão juntos no mesmo conjunto de término, mesmo se adicionais os documentos são adicionados ao conjunto ou se os conjuntos são mesclados.</span><span class="sxs-lookup"><span data-stu-id="44aac-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="44aac-126">Depois que forem mesclados conjuntos, o documento Pivot pode alterar quando novos documentos forem adicionados a um conjunto.</span><span class="sxs-lookup"><span data-stu-id="44aac-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44aac-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="44aac-127">See also</span></span>

[<span data-ttu-id="44aac-128">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="44aac-128">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="44aac-129">Definindo opções de analisar</span><span class="sxs-lookup"><span data-stu-id="44aac-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="44aac-130">Configuração Ignorar texto</span><span class="sxs-lookup"><span data-stu-id="44aac-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="44aac-131">Analisar configuração configurações avançada</span><span class="sxs-lookup"><span data-stu-id="44aac-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="44aac-132">Exibindo os resultados da análise</span><span class="sxs-lookup"><span data-stu-id="44aac-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

