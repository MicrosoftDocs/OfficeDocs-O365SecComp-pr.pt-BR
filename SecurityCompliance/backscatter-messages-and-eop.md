---
title: Mnsagens backscatter e EOP
ms.author: krowley
author: kccross
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
description: Mnsagens são as mensagens de rejeição automatizada que são enviadas pelos servidores de email, geralmente como resultado de spam de entrada. O DNSBLHTTP:// Backscatterer é uma lista de endereços IP que enviam mensagens backscatter. Não é uma lista de remetente de spam e não tentaremos remova nossos servidores o DNSBLHTTP:// Backscatterer.
ms.openlocfilehash: 2ab5c6a3bec347446452acd3bdfd8c5d309994a9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002674"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="39433-105">Mnsagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="39433-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="39433-p102">Mnsagens são as mensagens de rejeição automatizada que são enviadas pelos servidores de email, geralmente como resultado de spam de entrada. Como o Exchange Online Protection (EOP) é um serviço de filtragem de spam, mensagens de email enviadas a destinatários inexistentes e para outros destinos suspeitos são rejeitadas pelo nosso serviço. Quando isso acontece, EOP gera uma mensagem de relatório de falha na entrega (NDR) e entrega volta para o "remetente". Como os remetentes de spam frequentemente usam um endereço falsificado ou inválido "From" em suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem backscatter. Quando isso acontece, servidores de saída que estão associados a rede EOP podem estar listados na lista de bloqueio de DNS para Backscatterer (DNSBLHTTP://). O DNSBLHTTP:// Backscatterer é uma lista de endereços IP que enviam mensagens backscatter. Não é uma lista de remetente de spam e não tentaremos remova nossos servidores o DNSBLHTTP:// Backscatterer.</span><span class="sxs-lookup"><span data-stu-id="39433-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="39433-p103">De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="39433-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="39433-116">Para obter mais informações, consulte</span><span class="sxs-lookup"><span data-stu-id="39433-116">For more information</span></span>

[<span data-ttu-id="39433-117">A lista de IPs do Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="39433-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="39433-118">Consulte a entrada "backscatter NDR" em [Opções de filtragem de spam avançadas](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="39433-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

