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
ms.openlocfilehash: 62dd86d91e89e4f3c966b2969d0d763595bb5dc3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243892"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="2ece3-105">Mensagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="2ece3-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="2ece3-106">As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada.</span><span class="sxs-lookup"><span data-stu-id="2ece3-106">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam.</span></span> <span data-ttu-id="2ece3-107">Porque o Exchange Online Protection (EOP) é um serviço de filtro de spam, mensagens de email enviadas a destinatários inexistentes e para outros destinos suspeitos são rejeitadas por nosso serviço.</span><span class="sxs-lookup"><span data-stu-id="2ece3-107">Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service.</span></span> <span data-ttu-id="2ece3-108">Quando isso acontece, EOP gera uma mensagem do relatório de não-entregas (NDR) e a devolve ao "remetente".</span><span class="sxs-lookup"><span data-stu-id="2ece3-108">When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender."</span></span> <span data-ttu-id="2ece3-109">Porque remetentes de spam frequentemente usam um endereço "De" falsificados ou inválidos nas suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem backscatter.</span><span class="sxs-lookup"><span data-stu-id="2ece3-109">Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message.</span></span> <span data-ttu-id="2ece3-110">Quando isso acontece, servidores de saída que são associados à rede EOP podem ser listados na Lista de Bloqueio DNS de Remetente de Backscatter (DNSBL).</span><span class="sxs-lookup"><span data-stu-id="2ece3-110">When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL).</span></span> <span data-ttu-id="2ece3-111">O DNSBL de Remetente de Backscatterer é uma lista de endereços IP que enviam mensagens backscatter.</span><span class="sxs-lookup"><span data-stu-id="2ece3-111">The Backscatterer DNSBL is a list of IP addresses that send backscatter messages.</span></span> <span data-ttu-id="2ece3-112">Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL de Remetentes de Backscatter.</span><span class="sxs-lookup"><span data-stu-id="2ece3-112">It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="2ece3-p103">De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="2ece3-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="2ece3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ece3-116">Related topics</span></span>
  
[<span data-ttu-id="2ece3-117">Opções avançadas de filtragem de spam</span><span class="sxs-lookup"><span data-stu-id="2ece3-117">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
  

