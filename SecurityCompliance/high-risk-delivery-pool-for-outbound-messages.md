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
# <a name="high-risk-delivery-pool-for-outbound-messages"></a>Pool de alto risco de entrega para mensagens de saída

Quando o sistema de email do cliente foi comprometido por malware ou um ataque de spam mal-intencionado, e ele está enviando spam de saída através do serviço de filtragem hospedado, isso pode resultar nos endereços IP dos servidores de centro de dados do Office 365 seja listados no bloco de terceiros lista. Servidores de destino que faça não usar o serviço de filtragem hospedado, mas use essas listas de bloqueio, rejeitar todos os emails enviados a partir de qualquer um dos endereços IP de filtragem hospedados que foram adicionados a essas listas. Para impedir isso, todas as mensagens de saída que excedem o limite de spam são enviadas por meio de um pool de entrega de alto risco. Este pool de emails de saída secundário é usado apenas para enviar mensagens que podem ser de baixa qualidade. Isso ajuda a proteger o restante da rede enviem mensagens que são mais prováveis resultar em que o endereço IP de envio estão sendo bloqueado.
  
O uso de um pool de entrega de alto risco dedicado ajuda a garantir que o pool de saída normal somente está enviando mensagens que são conhecidas para ser de alta qualidade. Usando este pool de IP secundário ajuda a reduzir a probabilidade de que o pool de saída-IP normal sejam adicionado a uma lista de bloqueios. A possibilidade de que o pool de entrega de alto risco ser colocada em uma lista de bloqueios permanece um risco. Isso ocorre por design.
  
Mensagens onde o domínio de envio tem nenhum registro de endereço (um registro), que oferece a você o endereço IP do domínio, e nenhum registro MX, que ajuda a mala direta para os servidores que devem receber o email para um domínio específico no DNS, sempre são roteadas através do pool de entrega de alto risco independentemente de seu descarte de spam.
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a>Noções básicas sobre mensagens de notificação de Status de entrega (DSN)

O pool de entrega de alto risco de saída gerencia a entrega de todas as mensagens (DSN) de "devolução" ou "falhas".
  
As possíveis causas para um surto nas mensagens DSN incluem o seguinte:
  
- Uma campanha de falsificação que afete um dos clientes que utilizam o serviço
    
- Um ataque de coleta de diretório
    
- Um ataque de spam
    
- Um servidor SMTP invasor
    
Todos esses problemas podem resultar em um repentino aumento no número de mensagens DSN que estão sendo processadas pelo serviço. Muitas vezes, essas mensagens DSN parecem ser spams para outros servidores de email e serviços.
  
## <a name="for-more-information"></a>Para saber mais

[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Perguntas frequentes sobre a proteção antispam](anti-spam-protection-faq.md)
  

