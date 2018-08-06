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
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
description: Mnsagens são as mensagens de rejeição automatizada que são enviadas pelos servidores de email, geralmente como resultado de spam de entrada. O DNSBLHTTP:// Backscatterer é uma lista de endereços IP que enviam mensagens backscatter. Não é uma lista de remetente de spam e não tentaremos remova nossos servidores o DNSBLHTTP:// Backscatterer.
ms.openlocfilehash: 8f8a60715f9fb12ca53ffddc6d4fca6e9fab2ede
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028168"
---
# <a name="backscatter-messages-and-eop"></a>Mnsagens backscatter e EOP

Mnsagens são as mensagens de rejeição automatizada que são enviadas pelos servidores de email, geralmente como resultado de spam de entrada. Como o Exchange Online Protection (EOP) é um serviço de filtragem de spam, mensagens de email enviadas a destinatários inexistentes e para outros destinos suspeitos são rejeitadas pelo nosso serviço. Quando isso acontece, EOP gera uma mensagem de relatório de falha na entrega (NDR) e entrega volta para o "remetente". Como os remetentes de spam frequentemente usam um endereço falsificado ou inválido "From" em suas mensagens, o endereço do remetente ao qual o NDR é enviado pode resultar em uma mensagem backscatter. Quando isso acontece, servidores de saída que estão associados a rede EOP podem estar listados na lista de bloqueio de DNS para Backscatterer (DNSBLHTTP://). O DNSBLHTTP:// Backscatterer é uma lista de endereços IP que enviam mensagens backscatter. Não é uma lista de remetente de spam e não tentaremos remova nossos servidores o DNSBLHTTP:// Backscatterer. 
  
> [!TIP]
> De acordo com as instruções no site da web Backscatterer, o uso do modo rejeitar para todo email de entrada não é uma configuração recomendada ou uso desse serviço. Ao invés disso, ele deve ser usado no modo de segurança. Para obter mais informações sobre a implementação da configuração correta de backscatter, visite o site da web [Backscatterer.org](http://www.backscatterer.org/?target=usage). 
  
## <a name="for-more-information"></a>Para obter mais informações, consulte

[A lista de IPs do Backscatterer.org](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
Consulte a entrada "backscatter NDR" em [Opções de filtragem de spam avançadas](advanced-spam-filtering-asf-options.md)
  

