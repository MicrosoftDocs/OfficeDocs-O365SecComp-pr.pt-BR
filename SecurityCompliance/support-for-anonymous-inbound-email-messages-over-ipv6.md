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
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Suporte para mensagens de email de entrada anônimas por IPv6

Exchange Online Protection (EOP) e o Exchange Online suportam o recebimento de mensagens de email de entrada anônimas sobre IPv6 comunicações de remetentes que não enviem mensagens sobre segurança de camada de transporte (TLS). Você pode opt-in para receber mensagens sobre IPv6, solicitando essa funcionalidade do Microsoft Support abrindo o Centro de administração do Office 365 em [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicando em **suporte**e, em seguida, clicando em **nova solicitação de serviço**). Se você não opt-in para IPv6, você vai continuar a receber mensagens via IPv4.
  
Remetentes que transmitem mensagens para serviço sobre IPv6 devem cumprir com os dois requisitos a seguir:
  
1. O endereço de IPv6 remetente deve ter um registro PTR válido ([registro DNS inverso](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) do endereço IPv6 remetente). 
    
2. O remetente deve passar por verificação SPF (definida na [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou [verificação DKIM](http://dkim.org/) (definida na [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).
    
Esses requisitos de reunião é obrigatória, a configuração antes da autorização de IPv6. Se ambos os requisitos sejam atendidos, a mensagem serão efetuadas normal email fornecido pelo serviço de filtragem de mensagens. Se um ou outro não for atendido, a mensagem será rejeitada com uma das seguintes 450 respostas:
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
Se você não tiver a opção de receber mensagens sobre IPv6 e o remetente tentar forçar uma mensagem sobre IPv6 manualmente conectando-se ao servidor de email, a mensagem será rejeitada com uma resposta 550 parecida com a seguinte:
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>Para obter mais informações

[Suporte para validação de mensagens assinadas por DKIM](support-for-validation-of-dkim-signed-messages.md)
  

