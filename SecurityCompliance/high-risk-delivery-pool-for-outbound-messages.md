---
title: Pool de alto risco de entrega para mensagens de saída
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
description: Quando o sistema de email do cliente foi comprometido por malware ou um ataque de spam mal-intencionado, e ele está enviando spam de saída através do serviço de filtragem hospedado, isso pode resultar nos endereços IP dos servidores de centro de dados do Office 365 seja listados no bloco de terceiros lista.
ms.openlocfilehash: 856db53b105379ea3e606e39bf3c2612afa803c3
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026618"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a><span data-ttu-id="64c01-103">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="64c01-103">High-risk delivery pool for outbound messages</span></span>

<span data-ttu-id="64c01-p101">Quando o sistema de email do cliente foi comprometido por malware ou um ataque de spam mal-intencionado, e ele está enviando spam de saída através do serviço de filtragem hospedado, isso pode resultar nos endereços IP dos servidores de centro de dados do Office 365 seja listados no bloco de terceiros lista. Servidores de destino que faça não usar o serviço de filtragem hospedado, mas use essas listas de bloqueio, rejeitar todos os emails enviados a partir de qualquer um dos endereços IP de filtragem hospedados que foram adicionados a essas listas. Para impedir isso, todas as mensagens de saída que excedem o limite de spam são enviadas por meio de um pool de entrega de alto risco. Este pool de emails de saída secundário é usado apenas para enviar mensagens que podem ser de baixa qualidade. Isso ajuda a proteger o restante da rede enviem mensagens que são mais prováveis resultar em que o endereço IP de envio estão sendo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="64c01-p101">When a customer's email system has been compromised by malware or a malicious spam attack, and it's sending outbound spam through the hosted filtering service, this can result in the IP addresses of the Office 365 data center servers being listed on third-party block lists. Destination servers that do not use the hosted filtering service, but do use these block lists, reject all email sent from any of the hosted filtering IP addresses that have been added to those lists. To prevent this, all outbound messages that exceed the spam threshold are sent through a high-risk delivery pool. This secondary outbound email pool is only used to send messages that may be of low quality. This helps to protect the rest of the network from sending messages that are more likely to result in the sending IP address being blocked.</span></span>
  
<span data-ttu-id="64c01-p102">O uso de um pool de entrega de alto risco dedicado ajuda a garantir que o pool de saída normal somente está enviando mensagens que são conhecidas para ser de alta qualidade. Usando este pool de IP secundário ajuda a reduzir a probabilidade de que o pool de saída-IP normal sejam adicionado a uma lista de bloqueios. A possibilidade de que o pool de entrega de alto risco ser colocada em uma lista de bloqueios permanece um risco. Isso ocorre por design.</span><span class="sxs-lookup"><span data-stu-id="64c01-p102">The use of a dedicated high-risk delivery pool helps ensure that the normal outbound pool is only sending messages that are known to be of a high-quality. Using this secondary IP pool helps to reduce the probability of the normal outbound-IP pool being added to a blocked list. The possibility of the high-risk delivery pool being placed on a blocked list remains a risk. This is by design.</span></span>
  
<span data-ttu-id="64c01-113">Mensagens onde o domínio de envio tem nenhum registro de endereço (um registro), que oferece a você o endereço IP do domínio, e nenhum registro MX, que ajuda a mala direta para os servidores que devem receber o email para um domínio específico no DNS, sempre são roteadas através do pool de entrega de alto risco independentemente de seu descarte de spam.</span><span class="sxs-lookup"><span data-stu-id="64c01-113">Messages where the sending domain has no address record (A record), which gives you the IP address of the domain, and no MX record, which helps direct mail to the servers that should receive the mail for a particular domain in the DNS, are always routed through the high-risk delivery pool regardless of their spam disposition.</span></span>
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a><span data-ttu-id="64c01-114">Noções básicas sobre mensagens de notificação de Status de entrega (DSN)</span><span class="sxs-lookup"><span data-stu-id="64c01-114">Understanding Delivery Status Notification (DSN) messages</span></span>

<span data-ttu-id="64c01-115">O pool de entrega de alto risco de saída gerencia a entrega de todas as mensagens (DSN) de "devolução" ou "falhas".</span><span class="sxs-lookup"><span data-stu-id="64c01-115">The outbound high-risk delivery pool manages the delivery for all "bounced" or "failed" (DSN) messages.</span></span>
  
<span data-ttu-id="64c01-116">As possíveis causas para um surto nas mensagens DSN incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="64c01-116">Possible causes for a surge in DSN messages include the following:</span></span>
  
- <span data-ttu-id="64c01-117">Uma campanha de falsificação que afete um dos clientes que utilizam o serviço</span><span class="sxs-lookup"><span data-stu-id="64c01-117">A spoofing campaign affecting one of the customers using the service</span></span>
    
- <span data-ttu-id="64c01-118">Um ataque de coleta de diretório</span><span class="sxs-lookup"><span data-stu-id="64c01-118">A directory harvest attack</span></span>
    
- <span data-ttu-id="64c01-119">Um ataque de spam</span><span class="sxs-lookup"><span data-stu-id="64c01-119">A spam attack</span></span>
    
- <span data-ttu-id="64c01-120">Um servidor SMTP invasor</span><span class="sxs-lookup"><span data-stu-id="64c01-120">A rogue SMTP server</span></span>
    
<span data-ttu-id="64c01-p103">Todos esses problemas podem resultar em um repentino aumento no número de mensagens DSN que estão sendo processadas pelo serviço. Muitas vezes, essas mensagens DSN parecem ser spams para outros servidores de email e serviços.</span><span class="sxs-lookup"><span data-stu-id="64c01-p103">All of these issues can result in a sudden increase in the number of DSN messages being processed by the service. Many times, these DSN messages appear to be spam to other email servers and services.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="64c01-123">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="64c01-123">For more information</span></span>

[<span data-ttu-id="64c01-124">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="64c01-124">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="64c01-125">Perguntas frequentes sobre a proteção antispam</span><span class="sxs-lookup"><span data-stu-id="64c01-125">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

