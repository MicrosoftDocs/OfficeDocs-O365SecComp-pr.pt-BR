---
title: Mnsagens backscatter e EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada. O DNSBL de Remetente de Backscatterer é uma lista de endereços IP que enviam mensagens backscatter. Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL de Remetentes de Backscatter.
ms.openlocfilehash: 7581255ce4e68f6eb661df280ecb0cb94b7515ef
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693360"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="69078-105">Mnsagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="69078-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="69078-106">As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada.</span><span class="sxs-lookup"><span data-stu-id="69078-106">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam.</span></span> <span data-ttu-id="69078-107">Porque o Exchange Online Protection (EOP) é um serviço de filtro de spam, mensagens de email enviadas a destinatários inexistentes e para outros destinos suspeitos são rejeitadas por nosso serviço.</span><span class="sxs-lookup"><span data-stu-id="69078-107">Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service.</span></span> <span data-ttu-id="69078-108">Quando isso acontece, EOP gera uma mensagem do relatório de não-entregas (NDR) e a devolve ao "remetente".</span><span class="sxs-lookup"><span data-stu-id="69078-108">When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender."</span></span> <span data-ttu-id="69078-109">Porque remetentes de spam frequentemente usam um endereço "De" falsificados ou inválidos nas suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem backscatter.</span><span class="sxs-lookup"><span data-stu-id="69078-109">Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message.</span></span> <span data-ttu-id="69078-110">Quando isso acontece, servidores de saída que são associados à rede EOP podem ser listados na Lista de Bloqueio DNS de Remetente de Backscatter (DNSBL).</span><span class="sxs-lookup"><span data-stu-id="69078-110">When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL).</span></span> <span data-ttu-id="69078-111">O DNSBL de Remetente de Backscatterer é uma lista de endereços IP que enviam mensagens backscatter.</span><span class="sxs-lookup"><span data-stu-id="69078-111">The Backscatterer DNSBL is a list of IP addresses that send backscatter messages.</span></span> <span data-ttu-id="69078-112">Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL de Remetentes de Backscatter.</span><span class="sxs-lookup"><span data-stu-id="69078-112">It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="69078-p103">De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="69078-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="69078-116">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="69078-116">For more information</span></span>

[<span data-ttu-id="69078-117">A lista de IPs do Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="69078-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="69078-118">Consulte a entrada "inspersão de NDR" em [Opções avançadas de filtragem de spam](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="69078-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

