---
title: Repetir uma pesquisa de conteúdo para resolver um erro de local do conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Use o botão de repetição para resolver pesquisas de conteúdo que possuem erros de localização do conteúdo.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210174"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="ea70c-103">Repetir uma pesquisa de conteúdo para resolver um erro de local do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea70c-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="ea70c-104">Quando você usa a pesquisa de conteúdo no Centro de conformidade & segurança do Office 365 para pesquisar um número muito grande de caixas de correio (por exemplo, a pesquisa de caixas de 100.000 correio ou mais em uma única pesquisa de conteúdo), você pode obter erros de pesquisa que são semelhantes ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea70c-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="ea70c-p101">Esses erros (com códigos de erro de CS008-009 e CS012-002) indicam que a pesquisa de conteúdo não pôde ser pesquisar em locais específicos de conteúdo; Neste exemplo, duas caixas de correio não foram pesquisadas. Esses erros são exibidos na página status detalhes submenu da pesquisa conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="ea70c-107">Causa de erros de localização do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea70c-107">Cause of content location errors</span></span>

<span data-ttu-id="ea70c-p102">Quando um grande número de caixas de correio de recursos de pesquisa, a pesquisa é distribuída entre milhares de servidores em um datacenter da Microsoft. A qualquer momento, os servidores específicos poderia ser em estado de reinicialização ou no processo de failover para cópias redundantes. Em qualquer um desses casos, a solicitação de pesquisa de conteúdo para recuperar dados atinja o tempo limite. No exemplo anterior, os erros para as caixas de correio que falharam eram o resultado do cronograma do pesquisa check-out.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="ea70c-112">Resolvendo erros de localização do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea70c-112">Resolving content location errors</span></span>

<span data-ttu-id="ea70c-p103">Reiniciando a pesquisa frequentemente resultará em erros semelhantes em servidores diferentes. Em vez de reiniciar a pesquisa, clique no botão **de repetição** é exibido na parte superior da página de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Clique no botão de repetição para resolver erros do local do conteúdo](media/retrycontentsearch3.png)

<span data-ttu-id="ea70c-p104">Isso resultará no repetindo a pesquisa somente para as caixas de correio que falharam. Quando você tentar novamente a pesquisa, os resultados foram retornados com êxito serão mantidos.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="ea70c-118">Dicas para evitar erros de localização do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea70c-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="ea70c-119">Aqui estão algumas causas de adição de erros de localização do conteúdo e algumas dicas para ajudá-lo a evitá-los ao pesquisar grandes números de caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="ea70c-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="ea70c-p105">A caixa de correio que estão sendo pesquisada pode estar ocupada devido à atividade do usuário. Nesse caso, o serviço de pesquisa pode acelerar próprio para impedir que a caixa de correio ficar indisponível. Para evitar esse problema, tente executar pesquisas durante o horário não comercial.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="ea70c-p106">A consulta de pesquisa pode ser muito conteúdo recuperação da caixa de correio. Se possível, tente restringir o escopo da pesquisa usando palavras-chave, intervalos de data e condições de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="ea70c-p107">Muitas palavras-chave ou frases de palavra-chave quando você cria uma consulta de pesquisa usando a [lista de palavras-chave](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Quando você executa uma consulta de pesquisa que usa a lista de palavras-chave, o serviço executa essencialmente uma pesquisa separado para cada linha na lista de palavra-chave, para que as estatísticas podem ser geradas. Se você estiver usando a lista de palavras-chave em consultas de pesquisa, minimizar o número de linhas na lista de palavra-chave ou dividir as palavras-chave números em listas menores e criar uma pesquisa de diferente para cada lista de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ea70c-128">Para ajudar a reduzir problemas causados por palavra-chave grandes listas, agora você está limitado a um máximo de 20 linhas na lista de palavra-chave de uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea70c-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="ea70c-p108">Número excessivo de pesquisas estão sendo executadas na mesma caixa de correio ao mesmo tempo. Se possível, tente executar uma pesquisa por vez em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="ea70c-p109">Pesquisando o excesso de caixas de correio em uma única pesquisa. A probabilidade de erros de localização do conteúdo aumenta ao pesquisar um número muito grande de caixas de correio. Se possível, tente executar várias pesquisas de forma que cada pesquisa inclui um subconjunto de caixas de correio em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="ea70c-p110">Manutenção necessária está sendo executada na caixa de correio. Embora essa causa provavelmente ocorre raramente, espere um pouco enquanto depois de receber o erro de local de conteúdo e tente novamente a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea70c-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
