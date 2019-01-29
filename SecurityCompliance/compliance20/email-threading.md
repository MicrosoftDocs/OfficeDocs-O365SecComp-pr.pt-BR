---
title: Email threading
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
ms.openlocfilehash: 2340128f508a3be389afce86596f7e6395a0bb7e
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607353"
---
# <a name="email-threading"></a><span data-ttu-id="29394-102">Email threading</span><span class="sxs-lookup"><span data-stu-id="29394-102">Email threading</span></span>
<span data-ttu-id="29394-p101">Considere a possibilidade de uma conversa de email acontecendo por algum tempo. Na maioria dos casos, o último email no thread incluirá o conteúdo de todos os emails anteriores; analisar o último email fornecerá um contexto completo da conversa que ocorreram no segmento. Email threading identifica tais emails para que os revisores podem revisar uma fração de documentos coletados sem perder nenhum contexto.</span><span class="sxs-lookup"><span data-stu-id="29394-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="29394-106">O que faz threading de email?</span><span class="sxs-lookup"><span data-stu-id="29394-106">What does email threading do?</span></span>
<span data-ttu-id="29394-p102">Email threading analisa cada email e desconstructs-la para mensagens individuais; cada email é uma cadeia de mensagens individuais. Em seguida, ele analisa todos os emails no conjunto de trabalho para determinar se um email tem conteúdo exclusivo ou se a cadeia está totalmente contida em um email diferente. No final emails são divididos em quatro categorias:</span><span class="sxs-lookup"><span data-stu-id="29394-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>
- <span data-ttu-id="29394-110">Inclusives: a última mensagem no email tem conteúdo exclusivo e o email tem todos os anexos que foram incluídos em outras emails dos quais o conteúdo está totalmente contido neste email.</span><span class="sxs-lookup"><span data-stu-id="29394-110">Inclusives: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="29394-111">Inclusive menos: a última mensagem no email tem conteúdo exclusivo, mas o email não contém alguns dos anexos que foram incluídos em outras emails dos quais o conteúdo está totalmente contido neste email.</span><span class="sxs-lookup"><span data-stu-id="29394-111">Inclusive minus: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="29394-112">Inclusive cópia: uma cópia exata de um inclusive/inclusive menos email</span><span class="sxs-lookup"><span data-stu-id="29394-112">Inclusive copy: an exact copy of an inclusive/inclusive minus email</span></span>
- <span data-ttu-id="29394-113">NONE: O conteúdo deste e-mail está totalmente contido em pelo menos um email que está marcado como inclusive inclusive subtração.</span><span class="sxs-lookup"><span data-stu-id="29394-113">None: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="29394-114">Como ele é diferente do conversas no Outlook?</span><span class="sxs-lookup"><span data-stu-id="29394-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="29394-p103">Em um relance, isso sons bastante similar às agrupamentos de conversa no Outlook. No entanto, há algumas distinções importantes. Considere a possibilidade de uma conversa de email que receber bifurcada em dois conversa; Por exemplo, alguém respondeu a um email que não seja as informações mais recentes na conversa para que os duas últimas emails na conversa que ambos tenham o conteúdo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="29394-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="29394-p104">Outlook ainda seria agrupar os e-mails em uma única conversa; ler somente o último email significaria faltando o contexto do segundo recente e-mail, que também contém conteúdo exclusivo. Porque o email threading analisa check-out de cada email em componentes individuais e os compara, email threading seria marcar ambas os duas últimas emails como inclusives, garantindo que você não perca nenhum contexto desde que você leia todos os e-mails marcados como inclusive.</span><span class="sxs-lookup"><span data-stu-id="29394-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>