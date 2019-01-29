---
title: Construindo consultas de pesquisa
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
ms.openlocfilehash: 119cdd9d932b6c1be847c406988efa80b8534795
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607350"
---
# <a name="building-search-queries"></a><span data-ttu-id="9ba93-102">Construindo consultas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="9ba93-102">Building search queries</span></span>
<span data-ttu-id="9ba93-103">No edifício sua consulta, você pode usar várias palavras-chave e condições para definir quais itens a serem localizados.</span><span class="sxs-lookup"><span data-stu-id="9ba93-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="9ba93-104">Pesquisas de palavra-chave</span><span class="sxs-lookup"><span data-stu-id="9ba93-104">Keyword searches</span></span>
<span data-ttu-id="9ba93-p101">Digite uma consulta de pesquisa na caixa **palavras-chave** . Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que usam um operador booleano, como **AND**, **ou**, **não**e **NEAR**. Você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) em documentos ou procurar documentos que foram compartilhados externamente. Se você deixar a caixa de palavra-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificados será incluído nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ba93-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="9ba93-p102">Como alternativa, você pode clicar na caixa de seleção **Mostrar lista de palavra-chave** e o tipo de uma palavra-chave em cada linha. Se você fizer isso, as palavras-chave em cada linha são conectadas por um operador lógico ( **c:s**) que é semelhante em funcionalidade ao operador **OR** na consulta de pesquisa que é criado.</span><span class="sxs-lookup"><span data-stu-id="9ba93-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="9ba93-p103">Por que usar a lista de palavra-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave é mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas da pesquisa, consulte [estatística de pesquisa](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="9ba93-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="9ba93-117">Condições</span><span class="sxs-lookup"><span data-stu-id="9ba93-117">Conditions</span></span>    
<span data-ttu-id="9ba93-p104">Você pode adicionar condições para limitar a pesquisa e retornar um conjunto mais refinado de resultados de pesquisa. Cada condição adiciona uma cláusula a consulta de pesquisa que é criado e executados quando você iniciar a pesquisa. Uma condição logicamente é conectada a consulta de palavra-chave (especificada na caixa de palavra-chave) por um operador lógico (**c:c**) que é semelhante em funcionalidade ao operador **e** . Isso significa que os itens têm que satisfazer a consulta de palavra-chave e uma ou mais condições a serem incluídos nos resultados. Isso é como ajudam a condições para restringir os resultados. Para obter uma lista e descrição das condições que podem ser usados em uma consulta de pesquisa, consulte a seção "Critérios de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="9ba93-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


