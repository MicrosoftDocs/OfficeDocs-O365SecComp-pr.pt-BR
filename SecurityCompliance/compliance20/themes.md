---
title: Temas
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
description: ''
ms.openlocfilehash: b26b031b767f23504294880f4424be5042350c71
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151433"
---
# <a name="themes"></a><span data-ttu-id="0e75c-102">Temas</span><span class="sxs-lookup"><span data-stu-id="0e75c-102">Themes</span></span>
<span data-ttu-id="0e75c-103">Como uma pessoa escreve um documento?</span><span class="sxs-lookup"><span data-stu-id="0e75c-103">How does a person write a document?</span></span> <span data-ttu-id="0e75c-104">Geralmente, elas começam com uma ou mais ideias que desejam transmitir no documento e compor usando palavras que se alinham com as ideias.</span><span class="sxs-lookup"><span data-stu-id="0e75c-104">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="0e75c-105">Quanto mais predominante uma ideia é, mais frequentes as palavras relacionadas a essa ideia tendem a ser.</span><span class="sxs-lookup"><span data-stu-id="0e75c-105">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="0e75c-106">Isso informa como as pessoas consomem documentos também; o importante para a leitura de um documento é a idéia de que o documento está tentando transmitir e quais ideias aparecem onde e quais são as relações entre as idéias.</span><span class="sxs-lookup"><span data-stu-id="0e75c-106">This informs how people consume documents as well; the important thing to get from reading a document is the ideas that the document is trying to convey, and which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="0e75c-107">Isso pode ser estendido para a forma como uma pessoa deseja consumir um conjunto de documentos.</span><span class="sxs-lookup"><span data-stu-id="0e75c-107">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="0e75c-108">Eles desejam ver quais ideias estão presentes nos conjuntos e quais documentos estão falando sobre essas ideias.</span><span class="sxs-lookup"><span data-stu-id="0e75c-108">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="0e75c-109">Além disso, caso encontrem um documento de interesse específico, eles desejam poder ver documentos que discutem ideias semelhantes.</span><span class="sxs-lookup"><span data-stu-id="0e75c-109">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="0e75c-110">O módulo temas tenta simular a razão dos seresns de documentos, analisando os "temas" que são discutidos em um conjunto de revisão e atribuindo-os a documentos.</span><span class="sxs-lookup"><span data-stu-id="0e75c-110">Themes module tries to mimic how humans reason about documents, by analyzing the "themes" that are discussed in a review set and assigning them to documents.</span></span> <span data-ttu-id="0e75c-111">Temas avançam um passo adiante e identificam por documento o "tema dominante"; ou seja, o tema que aparece mais.</span><span class="sxs-lookup"><span data-stu-id="0e75c-111">Themes goes one step further and identifies per document the "dominant theme"; i.e. the theme that appears the most.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="0e75c-112">Como os temas funcionam?</span><span class="sxs-lookup"><span data-stu-id="0e75c-112">How does Themes work?</span></span>
<span data-ttu-id="0e75c-113">Temas analisa documentos com texto em uma revisão definida para analisar temas comuns que aparecem nos documentos.</span><span class="sxs-lookup"><span data-stu-id="0e75c-113">Themes analyzes documents with text in a review set to parse out common themes that appear accross the documents.</span></span> <span data-ttu-id="0e75c-114">Em seguida, ele atribui esses temas aos documentos em que eles aparecem.</span><span class="sxs-lookup"><span data-stu-id="0e75c-114">Then, it assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="0e75c-115">Ele também rotula cada um com palavras usadas nos documentos representativos do tema.</span><span class="sxs-lookup"><span data-stu-id="0e75c-115">It also labels each with words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="0e75c-116">Como um documento pode ser sobre mais de um assunto, em muitos casos, um documento tem mais de um temas atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="0e75c-116">Since a document can be about more than one subject matter, in many cases a document has more than one themes assigned to it.</span></span> <span data-ttu-id="0e75c-117">O tema que aparece mais proeminentemente em um documento é designado como seu tema dominante.</span><span class="sxs-lookup"><span data-stu-id="0e75c-117">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>