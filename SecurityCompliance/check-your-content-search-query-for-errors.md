---
title: Verificar sua consulta de Pesquisa de Conteúdo para erros
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Verifique a pesquisa de palavras-chave em busca de erros e erros de digitação, como caracteres não suportados e operadores booleanos minúsculos, antes de executar a pesquisa. Se encontrarmos um erro, sugeriremos uma consulta revisada.
ms.openlocfilehash: 00612116f345e2a01471d5c83df77f4bc8db9ce5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215931"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="1d34c-104">Verificar sua consulta de Pesquisa de Conteúdo para erros</span><span class="sxs-lookup"><span data-stu-id="1d34c-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="1d34c-p102">Ao criar ou editar uma pesquisa de conteúdo, você pode fazer com que o Office 365 Verifique sua consulta em busca de caracteres não suportados e operadores booleanos que podem não estar em maiúsculas. Como? Basta clicar em **verificar erros de digitação** na página consulta de uma pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Clique em "verificar erros de ortografia" para verificar se há caracteres não suportados na consulta de pesquisa.](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="1d34c-p103">Aqui está uma lista de caracteres não suportados que verificamos. Os caracteres sem suporte são geralmente ocultos e geralmente causam um erro de pesquisa ou retornam resultados indesejados.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="1d34c-p104">\*\*\*\* Aspas inglesas-não há suporte para aspas inglesas e duplas (também chamadas de aspas inglesas). Somente aspas normais podem ser usadas em uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="1d34c-p105">**Caracteres não imprimíveis e de controle** -caracteres não imprimíveis e de controle não representam um símbolo escrito, como um caractere alfanumérico. Exemplos de caracteres não imprimíveis e de controle incluem caracteres que formatam texto ou linhas separadas de texto.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="1d34c-115">**Marcas da esquerda para a direita e da direita para a esquerda** -estes são caracteres de controle usados para indicar a direção do texto para idiomas da esquerda para a direita (como Inglês e espanhol) e idiomas da direita para a esquerda (como árabe e Hebraico).</span><span class="sxs-lookup"><span data-stu-id="1d34c-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="1d34c-p106">**Operadores booleanOs minúsculos** -se você usar um operador Boolean, como **e**, **ou**, e **não** em uma consulta de pesquisa, ele deverá estar em letras maiúsculas. Quando verificamos uma consulta em busca de erros de digitação, a sintaxe da consulta geralmente indica que um operador booliano está sendo usado, mesmo que operadores minúsculos possam ser usados; por exemplo, `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="1d34c-118">O que acontece se uma consulta tiver um caractere sem suporte?</span><span class="sxs-lookup"><span data-stu-id="1d34c-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="1d34c-p107">Se forem encontrados caracteres sem suporte na consulta, será exibida uma mensagem de aviso que diz que os caracteres não suportados foram encontrados e um sugere uma alternativa. Em seguida, você tem a opção de manter a consulta original ou substituí-la pela consulta revisada sugerida. Veja um exemplo da mensagem de aviso exibida depois que você clica em **verificar se há erros de ortografia** para a consulta de pesquisa na captura de tela anterior. Observe que a consulta original contém aspas inteligentes e operadores booleanos minúsculos.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Uma mensagem de aviso é exibida com uma revisão sugerida para a consulta](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="1d34c-124">Como impedir que caracteres não suportados em suas consultas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1d34c-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="1d34c-p108">Os caracteres sem suporte são normalmente adicionados a uma consulta quando você copia a consulta ou partes da consulta de outros aplicativos (como o Microsoft Word ou Microsoft Excel) e as copia para a caixa de palavra-chave na página de consulta de uma pesquisa de conteúdo. A melhor maneira de evitar que os caracteres não suportados seja simplesmente digitar a consulta na caixa palavra-chave. Como alternativa, você pode copiar uma consulta do Word ou Excel e colá-la no arquivo em um editor de texto sem formatação, como o bloco de notas da Microsoft. Em seguida, salve o arquivo de texto e selecione **ANSI** na lista suspensa **codificação** . Isso removerá qualquer formatação e caractere sem suporte. Em seguida, você pode copiar e colar a consulta do arquivo de texto para a caixa de consulta de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="1d34c-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
