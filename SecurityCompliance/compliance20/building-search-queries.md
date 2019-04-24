---
title: Criar consultas de pesquisa
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
ms.openlocfilehash: e62d486b102fa035ae21b379d30bb0657b82acc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242499"
---
# <a name="build-search-queries"></a><span data-ttu-id="56042-102">Criar consultas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="56042-102">Build search queries</span></span>

<span data-ttu-id="56042-103">Ao criar sua consulta, você pode usar várias palavras-chave e condições para definir quais itens localizar.</span><span class="sxs-lookup"><span data-stu-id="56042-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="56042-104">Pesquisas de palavra-chave</span><span class="sxs-lookup"><span data-stu-id="56042-104">Keyword searches</span></span>

<span data-ttu-id="56042-105">Digite uma consulta de pesquisa na caixa **palavras-chave** .</span><span class="sxs-lookup"><span data-stu-id="56042-105">Type a search query in **Keywords** box.</span></span> <span data-ttu-id="56042-106">Você pode especificar palavras-chave, propriedades de mensagem, como datas de envio e recebimento, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="56042-106">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="56042-107">Você pode usar consultas mais complexas que usam um operador Boolean, como **e**, **ou**, e **não**, e **Near**.</span><span class="sxs-lookup"><span data-stu-id="56042-107">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="56042-108">Você também pode pesquisar informações confidenciais (como números de seguridade social) em documentos ou pesquisar documentos que foram compartilhados externamente.</span><span class="sxs-lookup"><span data-stu-id="56042-108">You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally.</span></span> <span data-ttu-id="56042-109">Se você deixar a caixa de palavras-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificado será incluído nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="56042-109">If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="56042-110">Como alternativa, você pode clicar na caixa de seleção **Mostrar lista de palavras-chave** e a palavra-chave tipo a em cada linha.</span><span class="sxs-lookup"><span data-stu-id="56042-110">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row.</span></span> <span data-ttu-id="56042-111">Se você fizer isso, as palavras-chave em cada linha serão conectadas por um operador lógico ( **c:s**) que é semelhante em funcionalidade ao operador **or** na consulta de pesquisa criada.</span><span class="sxs-lookup"><span data-stu-id="56042-111">If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="56042-112">Por que usar a lista de palavras-chave?</span><span class="sxs-lookup"><span data-stu-id="56042-112">Why use the keyword list?</span></span> <span data-ttu-id="56042-113">Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="56042-113">You can get statistics that show how many items match each keyword.</span></span> <span data-ttu-id="56042-114">Isso pode ajudá-lo a identificar rapidamente quais palavras-chave são mais (e menos) eficientes.</span><span class="sxs-lookup"><span data-stu-id="56042-114">This can help you quickly identify which keywords are the most (and least) effective.</span></span> <span data-ttu-id="56042-115">Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha.</span><span class="sxs-lookup"><span data-stu-id="56042-115">You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span> <span data-ttu-id="56042-116">Para obter mais informações sobre estatísticas de pesquisa, consulte estatísticas de [pesquisa](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="56042-116">For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="56042-117">Condições</span><span class="sxs-lookup"><span data-stu-id="56042-117">Conditions</span></span>
    
<span data-ttu-id="56042-118">Você pode adicionar condições de pesquisa para restringir uma pesquisa e retornar um conjunto de resultados mais refinado.</span><span class="sxs-lookup"><span data-stu-id="56042-118">You can add search conditions to narrow a search and return a more refined set of results.</span></span> <span data-ttu-id="56042-119">Cada condição adiciona uma cláusula à consulta de pesquisa criada e executada quando você inicia a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="56042-119">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="56042-120">Uma condição é conectada logicamente à consulta de palavra-chave (especificada na caixa palavra-chave) por um operador lógico (**c:c**) que é semelhante em funcionalidade ao operador **and** .</span><span class="sxs-lookup"><span data-stu-id="56042-120">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="56042-121">Isso significa que os itens precisam satisfazer a consulta de palavra-chave e uma ou mais condições a serem incluídas nos resultados.</span><span class="sxs-lookup"><span data-stu-id="56042-121">That means that items have to satisfy both the keyword query and one or more conditions to be included in the results.</span></span> <span data-ttu-id="56042-122">É assim que as condições ajudam a restringir os resultados.</span><span class="sxs-lookup"><span data-stu-id="56042-122">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="56042-123">Para obter uma lista e uma descrição das condições que você pode usar em uma consulta de pesquisa, consulte a seção "condições de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="56042-123">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


