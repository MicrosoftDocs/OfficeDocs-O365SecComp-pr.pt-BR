---
title: Gerenciar listas de remetentes confiáveis para mailers em massa
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: 'Se quiser usar listas de remetentes seguros, você deve saber que o Exchange Online Protection (EOP) e o processamento do Outlook lidam de forma diferente. O serviço respeita os remetentes e domínios seguros inspecionando o endereço RFC 5321. MailFrom e o endereço RFC 5322. from, enquanto o Outlook adiciona o endereço RFC 5322. from à lista de remetentes seguros de um usuário. (Observação: o serviço inspeciona o endereço 5321. MailFrom e o endereço 5322. from para os remetentes e domínios bloqueados.)'
ms.openlocfilehash: 27d635ec93dd04df8ebf22d5d3d8f8ead4b7bcf8
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276131"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>Gerenciar listas de remetentes confiáveis para mailers em massa

Se quiser usar listas de remetentes seguros, você deve saber que o Exchange Online Protection (EOP) e o processamento do Outlook lidam de forma diferente. O serviço respeita os remetentes e domínios seguros inspecionando o endereço RFC 5321. MailFrom e o endereço RFC 5322. from, enquanto o Outlook adiciona o endereço RFC 5322. from à lista de remetentes seguros de um usuário. (Observação: o serviço inspeciona o endereço 5321. MailFrom e o endereço 5322. from para os remetentes e domínios bloqueados.)
  
O endereço de email SMTP, caso contrário, conhecido como o endereço RFC 5321. MailFrom, é o endereço de email usado para executar verificações de SPF e, se o email não puder ser entregue, o caminho para o qual a mensagem devolvida será entregue. Esse endereço de email é colocado no caminho de retorno nos cabeçalhos de mensagem por padrão, embora seja possível para o remetente designar um endereço de caminho de retorno diferente.
  
O endereço de: nos cabeçalhos da mensagem, caso contrário, conhecido como o endereço RFC 5322. from, é o endereço de email que é exibido no cliente de email, como o Outlook.
  
Na maioria das vezes, os endereços 5321. MailFrom e 5322. from são os mesmos. Isso é típico para comunicação pessoa a pessoa. No enTanto, quando o email é enviado em nome de outra pessoa, os endereços são frequentemente diferentes. Isso geralmente acontece com mais frequência para mensagens de email em massa.
  
Por exemplo, suponha que as companhias aéreas de Yonder azul de aviação tenham contratado a viagem da Margie para enviar seu anúncio de email. Você recebe uma mensagem em sua caixa de entrada do remetente blueyonder@news.blueyonderairlines.com. Nesse caso, o endereço 5321. MailFrom é blueyonder.airlines@margiestravel.com e blueyonder@news.blueyonderairlines.com é o endereço 5322. from que é aquele que você vê no Outlook. Como o serviço respeita o endereço RFC 5322. from, para evitar que esta mensagem seja filtrada, você pode simplesmente adicionar o RFC 5322. from address como um remetente seguro no Outlook.
  

