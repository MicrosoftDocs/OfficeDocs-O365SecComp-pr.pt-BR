---
title: Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Este tópico fornece respostas para perguntas frequentes sobre mensagens que foram enfileiradas, adiadas ou retornadas durante o processo de filtragem do Microsoft Proteção do Exchange Online (EOP).
ms.openlocfilehash: 4b2c902adacd6e72e587aadaceecd22dd0084d85
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686421"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP

Este tópico fornece respostas para perguntas frequentes sobre mensagens que foram enfileiradas, adiadas ou retornadas durante o processo de filtragem do Microsoft Proteção do Exchange Online (EOP).
  
 **P. Por que o email é enfileirado?**
  
R. As mensagens são enfileiradas ou adiadas se o serviço não conseguir criar uma conexão com o servidor do destinatário para entrega. Ele não adiará mensagens se estiver retornando um erro de série 500 a partir da rede do destinatário.
  
 **P. Como uma mensagem é adiada?**
  
R. As mensagens serão mantidas quando uma conexão não puder ser feita com o servidor do destinatário e o servidor do destinatário estiver retornando uma "falha temporária" como um tempo limite de conexão, conexão recusada ou um erro de série 400. Se houver uma falha permanente, como um erro de série 500, a mensagem será retornada ao remetente.
  
 **P. Quanto tempo uma mensagem permanece em adiamento e qual é o intervalo de repetição?**
  
R. mensagens de no adiamento permanecerá em nossas filas por 2 dias. Tentativas de repetição de mensagem se baseiam no erro que recebemos de volta do sistema de email do destinatário. Os primeiro adiamentos alguns são 15 minutos ou menos, com tentativas subsequentes (via as próximas dezenas de meia mais ou menos) aumentar o intervalo sobre várias tentativas para um máximo de 60 minutos. A expansão de duração do intervalo é dinâmica, levando em consideração vários variáveis, como tamanhos de fila e a prioridade da mensagem interna. Basic, é 15 minutos (ou menos) para iniciar, expandindo a partir daí sobre as próximas algumas horas para 60 min max.
  
 **P. Após a restauração do servidor de email, como mensagens enfileiradas são distribuídas?**
  
R. Após a restauração de seu servidor de email, todas as mensagens enfileiradas são automaticamente processadas na ordem em que foram recebidas e enfileiradas quando o servidor ficou indisponível. 
  

