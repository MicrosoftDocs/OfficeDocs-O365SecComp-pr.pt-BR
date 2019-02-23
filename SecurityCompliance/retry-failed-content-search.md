---
title: Repetir uma pesquisa de conteúdo para resolver um erro de localização de conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Use o botão repetir para resolver pesquisas de conteúdo que têm erros de local de conteúdo.
ms.openlocfilehash: 032d93ef0990ed1dd7c1ea7bf2ba16653b3a862f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218851"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="11d21-103">Repetir uma pesquisa de conteúdo para resolver um erro de localização de conteúdo</span><span class="sxs-lookup"><span data-stu-id="11d21-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="11d21-104">Ao usar a pesquisa de conteúdo no centro de conformidade do & de segurança do Office 365 para pesquisar um número muito grande de caixas de correio (por exemplo, Pesquisar em 100.000 caixas de correio ou mais em uma única pesquisa de conteúdo), você pode receber erros de pesquisa semelhantes aos seguintes:</span><span class="sxs-lookup"><span data-stu-id="11d21-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="11d21-p101">Esses erros (com códigos de erro de CS008-009 e CS012-002) indicam que a pesquisa de conteúdo falhou ao pesquisar locais de conteúdo específicos; Neste exemplo, duas caixas de correio não foram pesquisadas. Esses erros são exibidos na página do menu de detalhes de status da pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="11d21-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="11d21-107">Causa de erros de localização de conteúdo</span><span class="sxs-lookup"><span data-stu-id="11d21-107">Cause of content location errors</span></span>

<span data-ttu-id="11d21-p102">Ao pesquisar um grande número de caixas de correio, a pesquisa é distribuída entre milhares de servidores em um datacenter da Microsoft. A qualquer momento, os servidores específicos podem estar no estado de reinicialização ou no processo de failover para cópias redundantes. Em qualquer um desses casos, a solicitação de pesquisa de conteúdo para recuperar dados irá expirar. No exemplo anterior, os erros para as caixas de correio que falharam foram o resultado da pesquisa com tempo limite.</span><span class="sxs-lookup"><span data-stu-id="11d21-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="11d21-112">Resolvendo erros de localização de conteúdo</span><span class="sxs-lookup"><span data-stu-id="11d21-112">Resolving content location errors</span></span>

<span data-ttu-id="11d21-p103">A reinicialização da pesquisa geralmente resultará em erros semelhantes em servidores diferentes. Em vez de reiniciar a pesquisa, clique no botão **repetir** que é exibido na parte superior da página de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="11d21-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Clique no botão repetir para resolver erros de localização de conteúdo](media/retrycontentsearch3.png)

<span data-ttu-id="11d21-p104">Isso resultará na repetição da pesquisa apenas para as caixas de correio que falharam. Quando você repetir a pesquisa, os outros resultados retornados com êxito serão mantidos.</span><span class="sxs-lookup"><span data-stu-id="11d21-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="11d21-118">Dicas para evitar erros de localização de conteúdo</span><span class="sxs-lookup"><span data-stu-id="11d21-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="11d21-119">Aqui estão algumas causas de adição de erros de local de conteúdo e algumas dicas para ajudá-lo a evitá-los ao pesquisar grandes números de caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="11d21-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="11d21-p105">A caixa de correio que está sendo pesquisada pode estar ocupada devido à atividade do usuário. Nesse caso, o serviço de pesquisa pode se limitar a impedir que a caixa de correio fique indisponível. Para evitar isso, tente executar pesquisas fora do horário comercial.</span><span class="sxs-lookup"><span data-stu-id="11d21-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="11d21-p106">A consulta de pesquisa pode recuperar muito conteúdo da caixa de correio. Se possível, tente restringir o escopo da pesquisa usando palavras-chave, intervalos de datas e condições de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="11d21-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="11d21-p107">Excesso de palavras-chave ou frases de palavra-chave quando você cria uma consulta de pesquisa usando a [lista de palavras-chave](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Quando você executa uma consulta de pesquisa que usa a lista de palavras-chave, o serviço essencialmente executa uma pesquisa separada para cada linha na lista de palavras-chave para que as estatísticas possam ser geradas. Se você estiver usando a lista de palavras-chave em consultas de pesquisa, minimize o número de linhas na lista de palavras-chave ou divida as palavras-chave do número em listas menores e crie uma pesquisa diferente para cada lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="11d21-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="11d21-128">Para ajudar a reduzir os problemas causados por listas de palavras-chave grandes, agora você está limitado a um máximo de 20 linhas na lista de palavras-chave de uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="11d21-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="11d21-p108">Muitas pesquisas estão sendo realizadas na mesma caixa de correio ao mesmo tempo. Se possível, tente executar uma pesquisa de cada vez em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="11d21-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="11d21-p109">Pesquisar muitas caixas de correio em uma única pesquisa. A probabilidade de erros de localização de conteúdo aumenta ao pesquisar um número muito grande de caixas de correio. Se possível, tente executar várias pesquisas para que cada pesquisa inclua um subconjunto de caixas de correio em sua organização.</span><span class="sxs-lookup"><span data-stu-id="11d21-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="11d21-p110">A manutenção necessária está sendo executada na caixa de correio. Embora essa causa provavelmente ocorra com frequência, espere um pouco antes de receber o erro de localização do conteúdo e repita a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="11d21-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
