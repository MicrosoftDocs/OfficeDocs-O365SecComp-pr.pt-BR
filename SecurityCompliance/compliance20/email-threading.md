---
title: Encadeamento de email
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3c4f940c34a9c51bf58107d10e04d0ed60f28a8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213421"
---
# <a name="email-threading"></a><span data-ttu-id="68482-102">Encadeamento de email</span><span class="sxs-lookup"><span data-stu-id="68482-102">Email threading</span></span>

<span data-ttu-id="68482-p101">Considere uma conversa por email que está acontecendo por algum tempo. Na maioria dos casos, o último email no thread incluirá o conteúdo de todos os emails anteriores; a revisão do último email fornecerá um contexto completo da conversa que aconteceu no thread. O encadeamento de emails identifica esses emails para que os Revisores possam revisar uma fração de documentos coletados sem perder nenhum contexto.</span><span class="sxs-lookup"><span data-stu-id="68482-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="68482-106">O que o thread de email faz?</span><span class="sxs-lookup"><span data-stu-id="68482-106">What does email threading do?</span></span>

<span data-ttu-id="68482-p102">O encadeamento de emails analisa cada email e o desconstructs para mensagens individuais; cada email é uma cadeia de mensagens individuais. Em seguida, ele analisa todos os emails no conjunto de trabalho para determinar se um email tem conteúdo exclusivo ou se a cadeia está totalmente contida em um email diferente. Nos emails finais estão divididos em quatro categorias:</span><span class="sxs-lookup"><span data-stu-id="68482-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="68482-110">**Inclusive**: a última mensagem no email tem conteúdo exclusivo e o email tem todos os anexos que foram incluídos em outros emails dos quais o conteúdo está totalmente contido neste email.</span><span class="sxs-lookup"><span data-stu-id="68482-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="68482-111">**Inclusive menos**: a última mensagem no email tem conteúdo exclusivo, mas o email não contém alguns dos anexos que foram incluídos em outros emails dos quais o conteúdo está totalmente contido neste email.</span><span class="sxs-lookup"><span data-stu-id="68482-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="68482-112">**Cópia inclusiva**: uma cópia exata de um email incluindo menos de um</span><span class="sxs-lookup"><span data-stu-id="68482-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="68482-113">**Nenhum**: o conteúdo desse email está totalmente contido em pelo menos um email marcado como incluindo, inclusive, o menos.</span><span class="sxs-lookup"><span data-stu-id="68482-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="68482-114">Qual é a diferença entre conversas no Outlook?</span><span class="sxs-lookup"><span data-stu-id="68482-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="68482-p103">Em resumo, isso parece muito semelhante aos agrupamentos de conversa no Outlook. No enTanto, há algumas diferenças importantes. Considere uma conversa de email que foi bifurcada em duas conversas; por exemplo, alguém respondeu a um email que não é o mais recente na conversa para que os dois últimos emails da conversa tenham conteúdo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="68482-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="68482-p104">O Outlook ainda agruparia os emails em uma única conversa; somente leitura o último email significaria ter o contexto do segundo email, que também contém conteúdo exclusivo. Como o encadeamento de emails analisa todos os emails em componentes individuais e os compara, o encadeamento de emails marcaria os dois últimos emails como inclusivos, garantindo que você não perderá nenhum contexto, desde que Leia todos os emails marcados como inclusive.</span><span class="sxs-lookup"><span data-stu-id="68482-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>