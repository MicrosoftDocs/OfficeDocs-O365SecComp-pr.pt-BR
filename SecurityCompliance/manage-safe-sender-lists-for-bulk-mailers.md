---
title: Gerenciar listas de remetentes seguros para correspondências em massa
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
description: 'Se você quiser usar listas de remetentes confiáveis, você deve saber que Exchange Online Protection (EOP) e o Outlook manipular processamento de forma diferente. O serviço respeita remetentes e domínios inspecionando o endereço do RFC 5321.MailFrom e o endereço do RFC 5322.From, enquanto o Outlook adiciona o endereço de 5322.From do RFC à lista de remetentes seguros de um usuário. (Observação: O serviço inspeciona o endereço de 5321.MailFrom e o endereço de 5322.From para remetentes bloqueados e domínios.)'
ms.openlocfilehash: e5d6f8440281d527e7ea1846416b785beda25f1c
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026538"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>Gerenciar listas de remetentes seguros para correspondências em massa

Se você quiser usar listas de remetentes confiáveis, você deve saber que Exchange Online Protection (EOP) e o Outlook manipular processamento de forma diferente. O serviço respeita remetentes e domínios inspecionando o endereço do RFC 5321.MailFrom e o endereço do RFC 5322.From, enquanto o Outlook adiciona o endereço de 5322.From do RFC à lista de remetentes seguros de um usuário. (Observação: O serviço inspeciona o endereço de 5321.MailFrom e o endereço de 5322.From para remetentes bloqueados e domínios.)
  
O endereço SMTP MAIL FROM, também é conhecido como o endereço do RFC 5321.MailFrom, é o endereço de email que é usado para executar verificações de SPF, e se o email não pode ser entregue, o caminho para o qual a mensagem de devolução é entregue. É este endereço de email é colocado no caminho de retorno nos cabeçalhos da mensagem por padrão, embora ele esteja possível para o emissor designar um endereço de retorno-caminho diferente.
  
From: o endereço em cabeçalhos da mensagem, também é conhecido como o endereço do RFC 5322.From, é o endereço de email é exibido no cliente de email, como o Outlook.
  
Grande parte dos endereços de tempo, o 5321.MailFrom e 5322.From são os mesmos. Isso é normal para a comunicação entre duas pessoas. No entanto, quando o email é enviado em nome de outra pessoa, os endereços são frequentemente diferentes. Isso geralmente ocorre com mais frequência para mensagens de email em massa.
  
Por exemplo, suponha que a Blue Yonder Airlines companhias tem contratado check-out de viagens Margie enviar publicidade seu email. Em seguida, recebo uma mensagem na caixa de entrada do remetente blueyonder@news.blueyonderairlines.com. Nesse caso, o endereço de 5321.MailFrom é blueyonder.airlines@margiestravel.com e blueyonder@news.blueyonderairlines.com é o endereço de 5322.From que é exibido no Outlook. Porque o serviço respeita o endereço de 5322.From RFC, para impedir que essa mensagem obtendo filtrado, você pode simplesmente adicionar o endereço do RFC 5322.From como um remetente seguro no Outlook.
  

