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
# <a name="backscatter-messages-and-eop"></a>Mnsagens backscatter e EOP

As mensagens de dispersão são as mensagens de retorno automatizadas que são enviadas por servidores de email, geralmente como resultado de um spam de entrada. Como o Exchange Online Protection (EOP) é um serviço de filtragem de spam, as mensagens de email enviadas a destinatários inexistentes e a outros destinos suspeitos são rejeitadas pelo nosso serviço. Quando isso acontece, EOP gera uma mensagem de notificação de falha na entrega (NDR) e a entrega de volta para o "remetente". Como os spammers freqüentemente usam um endereço "de" forjado ou inválido em suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem de inspersão. Quando isso acontece, os servidores de saída associados à rede do EOP podem ser listados na lista de bloqueios de DNS (DNSBL) do dispersão. O DNSBL dispersão é uma lista de endereços IP que enviam mensagens de dispersão. Não é uma lista de remetentes de spam e não tentamos remover nossos servidores da DNSBL dispersão. 
  
> [!TIP]
> De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage). 
  
## <a name="for-more-information"></a>Para obter mais informações, consulte

[A lista de IPs do Backscatterer.org](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
Consulte a entrada "inspersão de NDR" em [Opções avançadas de filtragem de spam](advanced-spam-filtering-asf-options.md)
  

