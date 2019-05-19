---
title: Criar consultas de pesquisa
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
ms.openlocfilehash: a33ecb6e1a2549b6bdc3bde9897b8a75e742b482
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151923"
---
# <a name="build-search-queries"></a>Criar consultas de pesquisa

Ao criar sua consulta, você pode usar várias palavras-chave e condições para definir quais itens localizar.

## <a name="keyword-searches"></a>Pesquisas de palavra-chave

Digite uma consulta de pesquisa na caixa **palavras-chave** . Você pode especificar palavras-chave, propriedades de mensagem, como datas de envio e recebimento, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterado pela última vez. Você pode usar consultas mais complexas que usam um operador Boolean, como **e**, **ou**, e **não**, e **Near**. Você também pode pesquisar informações confidenciais (como números de seguridade social) em documentos ou pesquisar documentos que foram compartilhados externamente. Se você deixar a caixa de palavras-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificado será incluído nos resultados da pesquisa.
    
Como alternativa, você pode clicar na caixa de seleção **Mostrar lista de palavras-chave** e a palavra-chave tipo a em cada linha. Se você fizer isso, as palavras-chave em cada linha serão conectadas por um operador lógico ( **c:s**) que é semelhante em funcionalidade ao operador **or** na consulta de pesquisa criada. 
    
Por que usar a lista de palavras-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave são mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas de pesquisa, consulte estatísticas de [pesquisa](search-statistics.md).

## <a name="conditions"></a>Condições
    
Você pode adicionar condições de pesquisa para restringir uma pesquisa e retornar um conjunto de resultados mais refinado. Cada condição adiciona uma cláusula à consulta de pesquisa criada e executada quando você inicia a pesquisa. Uma condição é conectada logicamente à consulta de palavra-chave (especificada na caixa palavra-chave) por um operador lógico (**c:c**) que é semelhante em funcionalidade ao operador **and** . Isso significa que os itens precisam satisfazer a consulta de palavra-chave e uma ou mais condições a serem incluídas nos resultados. É assim que as condições ajudam a restringir os resultados. Para obter uma lista e uma descrição das condições que você pode usar em uma consulta de pesquisa, consulte a seção "condições de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](../keyword-queries-and-search-conditions.md#search-conditions).


