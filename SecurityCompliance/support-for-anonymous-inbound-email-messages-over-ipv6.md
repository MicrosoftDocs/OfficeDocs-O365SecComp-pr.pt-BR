---
title: Suporte para mensagens de email de entrada anônimas por IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Saiba como configurar o suporte para mensagens anônimas de origens de IPv6 para o Exchange Online Protection e o Exchange Online.
ms.openlocfilehash: 0d324ce6e0ff0ff9104ef597176b09a5a319abc7
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255806"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="ced16-103">Suporte para mensagens de email de entrada anônimas por IPv6</span><span class="sxs-lookup"><span data-stu-id="ced16-103">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="ced16-p101">Exchange Online Protection (EOP) e o Exchange Online suportam o recebimento de mensagens de email de entrada anônimas sobre IPv6 comunicações de remetentes que não enviem mensagens sobre segurança de camada de transporte (TLS). Você pode opt-in para receber mensagens sobre IPv6, solicitando essa funcionalidade do Microsoft Support abrindo o Centro de administração do Office 365 em [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicando em **suporte**e, em seguida, clicando em **nova solicitação de serviço**). Se você não opt-in para IPv6, você vai continuar a receber mensagens via IPv4.</span><span class="sxs-lookup"><span data-stu-id="ced16-p101">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS). You can opt-in to receive messages over IPv6 by requesting this functionality from Microsoft Support by opening the Office 365 admin center at [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicking **Support**, and then clicking **New service request**). If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="ced16-107">Remetentes que transmitem mensagens para serviço sobre IPv6 devem cumprir com os dois requisitos a seguir:</span><span class="sxs-lookup"><span data-stu-id="ced16-107">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="ced16-108">O endereço de IPv6 remetente deve ter um registro PTR válido ([registro DNS inverso](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) do endereço IPv6 remetente).</span><span class="sxs-lookup"><span data-stu-id="ced16-108">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="ced16-109">O remetente deve passar por verificação SPF (definida na [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou [verificação DKIM](http://dkim.org/) (definida na [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="ced16-109">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="ced16-p102">Esses requisitos de reunião é obrigatória, a configuração antes da autorização de IPv6. Se ambos os requisitos sejam atendidos, a mensagem serão efetuadas normal email fornecido pelo serviço de filtragem de mensagens. Se um ou outro não for atendido, a mensagem será rejeitada com uma das seguintes 450 respostas:</span><span class="sxs-lookup"><span data-stu-id="ced16-p102">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6. If both requirements are met, the message will go through normal email message filtering provided by the service. If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="ced16-113">Se você não tiver a opção de receber mensagens sobre IPv6 e o remetente tentar forçar uma mensagem sobre IPv6 manualmente conectando-se ao servidor de email, a mensagem será rejeitada com uma resposta 550 parecida com a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ced16-113">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="ced16-114">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="ced16-114">For more information</span></span>

[<span data-ttu-id="ced16-115">Suporte para validação de mensagens assinadas por DKIM</span><span class="sxs-lookup"><span data-stu-id="ced16-115">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

