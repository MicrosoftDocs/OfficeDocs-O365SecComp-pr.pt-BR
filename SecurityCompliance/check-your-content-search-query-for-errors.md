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
# <a name="check-your-content-search-query-for-errors"></a>Verificar sua consulta de Pesquisa de Conteúdo para erros

Ao criar ou editar uma pesquisa de conteúdo, você pode fazer com que o Office 365 Verifique sua consulta em busca de caracteres não suportados e operadores booleanos que podem não estar em maiúsculas. Como? Basta clicar em **verificar erros de digitação** na página consulta de uma pesquisa de conteúdo. 
  
![Clique em "verificar erros de ortografia" para verificar se há caracteres não suportados na consulta de pesquisa.](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
Aqui está uma lista de caracteres não suportados que verificamos. Os caracteres sem suporte são geralmente ocultos e geralmente causam um erro de pesquisa ou retornam resultados indesejados.
  
- **** Aspas inglesas-não há suporte para aspas inglesas e duplas (também chamadas de aspas inglesas). Somente aspas normais podem ser usadas em uma consulta de pesquisa. 
    
- **Caracteres não imprimíveis e de controle** -caracteres não imprimíveis e de controle não representam um símbolo escrito, como um caractere alfanumérico. Exemplos de caracteres não imprimíveis e de controle incluem caracteres que formatam texto ou linhas separadas de texto. 
    
- **Marcas da esquerda para a direita e da direita para a esquerda** -estes são caracteres de controle usados para indicar a direção do texto para idiomas da esquerda para a direita (como Inglês e espanhol) e idiomas da direita para a esquerda (como árabe e Hebraico).
    
- **Operadores booleanOs minúsculos** -se você usar um operador Boolean, como **e**, **ou**, e **não** em uma consulta de pesquisa, ele deverá estar em letras maiúsculas. Quando verificamos uma consulta em busca de erros de digitação, a sintaxe da consulta geralmente indica que um operador booliano está sendo usado, mesmo que operadores minúsculos possam ser usados; por exemplo, `(WordA or WordB) and (WordC or WordD)`.
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a>O que acontece se uma consulta tiver um caractere sem suporte?

Se forem encontrados caracteres sem suporte na consulta, será exibida uma mensagem de aviso que diz que os caracteres não suportados foram encontrados e um sugere uma alternativa. Em seguida, você tem a opção de manter a consulta original ou substituí-la pela consulta revisada sugerida. Veja um exemplo da mensagem de aviso exibida depois que você clica em **verificar se há erros de ortografia** para a consulta de pesquisa na captura de tela anterior. Observe que a consulta original contém aspas inteligentes e operadores booleanos minúsculos. 
  
![Uma mensagem de aviso é exibida com uma revisão sugerida para a consulta](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a>Como impedir que caracteres não suportados em suas consultas de pesquisa

Os caracteres sem suporte são normalmente adicionados a uma consulta quando você copia a consulta ou partes da consulta de outros aplicativos (como o Microsoft Word ou Microsoft Excel) e as copia para a caixa de palavra-chave na página de consulta de uma pesquisa de conteúdo. A melhor maneira de evitar que os caracteres não suportados seja simplesmente digitar a consulta na caixa palavra-chave. Como alternativa, você pode copiar uma consulta do Word ou Excel e colá-la no arquivo em um editor de texto sem formatação, como o bloco de notas da Microsoft. Em seguida, salve o arquivo de texto e selecione **ANSI** na lista suspensa **codificação** . Isso removerá qualquer formatação e caractere sem suporte. Em seguida, você pode copiar e colar a consulta do arquivo de texto para a caixa de consulta de palavra-chave. 
