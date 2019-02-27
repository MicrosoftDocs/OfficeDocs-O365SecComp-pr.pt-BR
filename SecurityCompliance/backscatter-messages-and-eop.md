---
title: Mnsagens backscatter e EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada. O DNSBL dispersão é uma lista de endereços IP que enviam mensagens de dispersão. Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL dispersão.
ms.openlocfilehash: 73f8631c50bcfb8a023b2b6007b7ccf48038e16e
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275291"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="ba364-105">Mnsagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="ba364-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="ba364-p102">As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada. Como o Exchange Online Protection (EOP) é um serviço de filtragem de spam, as mensagens de email enviadas a destinatários inexistentes e a outros destinos suspeitos são rejeitadas pelo nosso serviço. Quando isso acontece, EOP gera uma mensagem de notificação de falha na entrega (NDR) e a entrega de volta para o "remetente". Como os spammers freqüentemente usam um endereço "de" forjado ou inválido em suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem de inspersão. Quando isso acontece, os servidores de saída associados à rede do EOP podem ser listados na lista de bloqueios de DNS (DNSBL) do dispersão. O DNSBL dispersão é uma lista de endereços IP que enviam mensagens de dispersão. Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL dispersão.</span><span class="sxs-lookup"><span data-stu-id="ba364-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ba364-p103">De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="ba364-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="ba364-116">Para obter mais informações, consulte</span><span class="sxs-lookup"><span data-stu-id="ba364-116">For more information</span></span>

[<span data-ttu-id="ba364-117">A lista de IPs do Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="ba364-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="ba364-118">Consulte a entrada "inspersão de NDR" em [Opções avançadas de filtragem de spam](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="ba364-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

