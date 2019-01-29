---
title: Perto de detecção de duplicatas
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
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607324"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="1baf9-102">Perto de detecção de duplicatas</span><span class="sxs-lookup"><span data-stu-id="1baf9-102">Near duplicate detection</span></span>

<span data-ttu-id="1baf9-p101">Considere a possibilidade de um conjunto de documentos seja revisada na qual um subconjunto baseia-se no mesmo modelo e tem principalmente o mesmo texto padronizado idioma, com algumas diferenças aqui e ali. Se um revisor pode identificar este subconjunto, revisar um deles inteiro e revise as diferenças para o restante, eles seriam não ter perdido quaisquer informações exclusivas enquanto aproveitando apenas uma fração do tempo que teria levado-los para ler todos os documentos na íntegra. Detecção de duplicatas quase agrupa documentos textualmente semelhantes juntos para ajudá-lo a tornar seu processo de revisão mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="1baf9-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="1baf9-106">Como funciona?</span><span class="sxs-lookup"><span data-stu-id="1baf9-106">How does it work?</span></span>

<span data-ttu-id="1baf9-p102">Quando perto de detecção de duplicatas é executado, o sistema analisa todos os documentos com texto. Em seguida, ele se compara todos os documentos contra uns aos outros para determinar se os seu semelhança é maior que o limite estabelecido. Se for, os documentos são agrupados. Depois que todos os documentos foram comparados e agrupados, um documento a partir de cada grupo está marcado como "pivot"; na revisão seus documentos, você pode revisar um pivô primeiro e revise os outros documentos na mesma quase duplicado set, concentrando-se a diferença entre o pivot e o documento que está em revisão.</span><span class="sxs-lookup"><span data-stu-id="1baf9-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>