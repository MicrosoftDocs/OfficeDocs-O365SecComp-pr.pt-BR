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
# <a name="building-search-queries"></a>Construindo consultas de pesquisa
No edifício sua consulta, você pode usar várias palavras-chave e condições para definir quais itens a serem localizados.

## <a name="keyword-searches"></a>Pesquisas de palavra-chave
Digite uma consulta de pesquisa na caixa **palavras-chave** . Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que usam um operador booleano, como **AND**, **ou**, **não**e **NEAR**. Você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) em documentos ou procurar documentos que foram compartilhados externamente. Se você deixar a caixa de palavra-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificados será incluído nos resultados da pesquisa.
    
Como alternativa, você pode clicar na caixa de seleção **Mostrar lista de palavra-chave** e o tipo de uma palavra-chave em cada linha. Se você fizer isso, as palavras-chave em cada linha são conectadas por um operador lógico ( **c:s**) que é semelhante em funcionalidade ao operador **OR** na consulta de pesquisa que é criado. 
    
Por que usar a lista de palavra-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave é mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas da pesquisa, consulte [estatística de pesquisa](search-statistics.md).

## <a name="conditions"></a>Condições    
Você pode adicionar condições para limitar a pesquisa e retornar um conjunto mais refinado de resultados de pesquisa. Cada condição adiciona uma cláusula a consulta de pesquisa que é criado e executados quando você iniciar a pesquisa. Uma condição logicamente é conectada a consulta de palavra-chave (especificada na caixa de palavra-chave) por um operador lógico (**c:c**) que é semelhante em funcionalidade ao operador **e** . Isso significa que os itens têm que satisfazer a consulta de palavra-chave e uma ou mais condições a serem incluídos nos resultados. Isso é como ajudam a condições para restringir os resultados. Para obter uma lista e descrição das condições que podem ser usados em uma consulta de pesquisa, consulte a seção "Critérios de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](../keyword-queries-and-search-conditions.md#search-conditions).


