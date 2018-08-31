---
title: Verificar sua consulta de Pesquisa de Conteúdo para erros
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Verifique sua consulta de palavra-chave de pesquisa de conteúdo para erros e erros de digitação, como os caracteres não suportados e minúsculos operadores booleanos, antes de executar a pesquisa. Se conseguimos encontrar um erro, vai sugerimos uma consulta revisada.
ms.openlocfilehash: 0d2119ceef4ce3777d3967a56357551e235e426c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524045"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="ee3ab-104">Verificar sua consulta de Pesquisa de Conteúdo para erros</span><span class="sxs-lookup"><span data-stu-id="ee3ab-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="ee3ab-p102">Quando você cria ou editar uma pesquisa de conteúdo, você pode ter o Office 365 verificar sua consulta para caracteres não suportados e operadores booleanos que não podem estar em letras maiusculas. Como? Basta clicar em **Verificar a consulta para erros de digitação** na página consulta de uma pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Clique em "Verificação de consulta para erros de digitação" para verificar a consulta de pesquisa para caracteres não suportados](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="ee3ab-p103">Aqui está uma lista dos caracteres não suportados que verificamos. Não há suporte para caracteres geralmente estão ocultos e geralmente causar um erro de pesquisa ou retornar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="ee3ab-p104">**Aspas inglesas** - single e double aspas inglesas (também chamadas de aspas inglesas) não são suportados. Somente as aspas normais pode ser usadas em uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="ee3ab-p105">**Caracteres não imprimíveis e controle** - não imprimíveis e caracteres de controle não representam um símbolo escrito, como um caractere alfanumérico. Exemplos de não-imprimíveis e caracteres de controle incluem caracteres que formatar texto ou em linhas separadas de texto.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="ee3ab-115">**Marca da esquerda para a direita e da direita para a esquerda** - esses são usados para indicar a direção do texto para a esquerda para a direita (por exemplo, inglês e espanhol) e idiomas da direita para a esquerda (por exemplo, árabe e hebraico) de caracteres de controle.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="ee3ab-p106">**Operadores booleanos minúsculo** - se você usar um operador booleano, como **e**, **ou**e **não** em uma consulta de pesquisa, ela deve ser letras maiusculas. Quando verificamos uma consulta para erros de digitação, a sintaxe de consulta frequentemente indicará que um operador booleano está sendo usado, mesmo que poderiam ser usadas operadores minúsculas; Por exemplo, `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="ee3ab-118">O que acontece se uma consulta tiver um caractere sem suporte?</span><span class="sxs-lookup"><span data-stu-id="ee3ab-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="ee3ab-p107">Se não há suporte para caracteres forem encontradas em sua consulta, aviso será exibida uma mensagem que informa que não há suporte para caracteres encontrados e um sugere uma alternativa. Em seguida, em seguida, você tem a opção mantenha a consulta original ou substituí-la com a consulta revisada sugerida. Aqui está um exemplo de mensagem de aviso é exibido após você clicar em **Verificar a consulta para erros de digitação** para a consulta de pesquisa a captura de tela anterior. Observe que a consulta original contém aspas inglesas e operadores booleanos minúsculos.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Uma mensagem de aviso é exibida com uma revisão sugerida para a sua consulta](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="ee3ab-124">Como impedir que os caracteres não suportados em suas consultas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="ee3ab-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="ee3ab-p108">Não há suporte para caracteres normalmente são adicionados a uma consulta quando você copia a consulta ou partes da consulta de outros aplicativos (por exemplo, Microsoft Word ou Microsoft Excel) e copiá-los para a caixa de palavra-chave na página consulta de uma pesquisa de conteúdo. Basta digitar a consulta na caixa de palavra-chave é a melhor maneira de impedir que os caracteres não suportados. Como alternativa, você pode copiar uma consulta do Word ou Excel e colá-lo no arquivo em um editor de texto sem formatação, como o Microsoft Notepad. Em seguida, salve o arquivo de texto e selecione **ANSI** na lista suspensa **codificação** . Isto irá remover quaisquer caracteres não suportados e formatação. Você pode, em seguida, copie e cole a consulta do arquivo de texto para a caixa de consulta de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
