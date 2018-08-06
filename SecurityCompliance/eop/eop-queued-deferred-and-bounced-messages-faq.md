---
title: Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Este tópico fornece respostas para perguntas frequentes sobre mensagens que foram enfileiradas, adiadas ou retornadas durante o processo de filtragem do Microsoft Proteção do Exchange Online (EOP).
ms.openlocfilehash: 17e5955195c4e38299712fb9161822984b2a643a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026218"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="6f8dd-103">Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP</span><span class="sxs-lookup"><span data-stu-id="6f8dd-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="6f8dd-104">Este tópico fornece respostas para perguntas frequentes sobre mensagens que foram enfileiradas, adiadas ou retornadas durante o processo de filtragem do Microsoft Proteção do Exchange Online (EOP).</span><span class="sxs-lookup"><span data-stu-id="6f8dd-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="6f8dd-105">**P. Por que o email é enfileirado?**</span><span class="sxs-lookup"><span data-stu-id="6f8dd-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="6f8dd-p101">R. As mensagens são enfileiradas ou adiadas se o serviço não conseguir criar uma conexão com o servidor do destinatário para entrega. Ele não adiará mensagens se estiver retornando um erro de série 500 a partir da rede do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6f8dd-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="6f8dd-109">**P. Como uma mensagem é adiada?**</span><span class="sxs-lookup"><span data-stu-id="6f8dd-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="6f8dd-p102">R. As mensagens serão mantidas quando uma conexão não puder ser feita com o servidor do destinatário e o servidor do destinatário estiver retornando uma "falha temporária" como um tempo limite de conexão, conexão recusada ou um erro de série 400. Se houver uma falha permanente, como um erro de série 500, a mensagem será retornada ao remetente.</span><span class="sxs-lookup"><span data-stu-id="6f8dd-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="6f8dd-113">**P. Quanto tempo uma mensagem permanece em adiamento e qual é o intervalo de repetição?**</span><span class="sxs-lookup"><span data-stu-id="6f8dd-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="6f8dd-p103">R. As mensagens em adiamento permanecerão nas filas por 2 dias. As tentativas de repetição de mensagens baseiam-se no tipo de erro recebido do sistema de mensagens do destinatário. Em média, as mensagens passam por uma nova tentativa a cada 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="6f8dd-p103">A. Messages in deferral will remain in our queues for 2 days. Message retry attempts are based on the error we get back from the recipient's mail system. On average, messages are retried every 5 minutes.</span></span>
  
 <span data-ttu-id="6f8dd-118">**P. Após a restauração do servidor de email, como mensagens enfileiradas são distribuídas?**</span><span class="sxs-lookup"><span data-stu-id="6f8dd-118">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="6f8dd-p104">R. Após a restauração de seu servidor de email, todas as mensagens enfileiradas são automaticamente processadas na ordem em que foram recebidas e enfileiradas quando o servidor ficou indisponível.</span><span class="sxs-lookup"><span data-stu-id="6f8dd-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

