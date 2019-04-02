---
title: Detecção próxima duplicação
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
ms.openlocfilehash: 941809193a3342d8c7b9de991370848aee4af070
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31029845"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="a2c38-102">Detecção próxima duplicação</span><span class="sxs-lookup"><span data-stu-id="a2c38-102">Near duplicate detection</span></span>

<span data-ttu-id="a2c38-103">Considere um conjunto de documentos para ser revisado no qual um subconjunto é baseado no mesmo modelo e tem principalmente o mesmo idioma clichê, com algumas diferenças aqui e ali.</span><span class="sxs-lookup"><span data-stu-id="a2c38-103">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there.</span></span> <span data-ttu-id="a2c38-104">Se um revisor pudesse identificar esse subconjunto, revise um deles cuidadosamente e revise as diferenças para o resto, eles não teriam informações exclusivas e, ao mesmo tempo, levaria apenas uma fração de tempo que teria levado em vista para ler todos os documentos na capa.</span><span class="sxs-lookup"><span data-stu-id="a2c38-104">If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover.</span></span> <span data-ttu-id="a2c38-105">Um grupo de detecção de duplicidades próximo agrupa documentos semelhantes para ajudá-lo a tornar seu processo de revisão mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="a2c38-105">Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="a2c38-106">Como funciona?</span><span class="sxs-lookup"><span data-stu-id="a2c38-106">How does it work?</span></span>

<span data-ttu-id="a2c38-107">Quando a detecção próxima duplicação é executada, o sistema analisa todos os documentos com texto.</span><span class="sxs-lookup"><span data-stu-id="a2c38-107">When near duplicate detection is run, the system parses every document with text.</span></span> <span data-ttu-id="a2c38-108">Em seguida, ele compara todos os documentos entre si para determinar se sua similaridade é maior do que o limite definido.</span><span class="sxs-lookup"><span data-stu-id="a2c38-108">Then, it compares every document against each other to determine whether their similarity is greater than the set threshold.</span></span> <span data-ttu-id="a2c38-109">Se for, os documentos serão agrupados.</span><span class="sxs-lookup"><span data-stu-id="a2c38-109">If it is, the documents are grouped together.</span></span> <span data-ttu-id="a2c38-110">Depois que todos os documentos forem comparados e agrupados, um documento de cada grupo será marcado como "pivô"; ao revisar seus documentos, você pode revisar uma tabela dinâmica primeiro e revisar os outros documentos no mesmo conjunto próximo duplicado, concentrando-se na diferença entre a tabela dinâmica e o documento que está em revisão.</span><span class="sxs-lookup"><span data-stu-id="a2c38-110">Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>