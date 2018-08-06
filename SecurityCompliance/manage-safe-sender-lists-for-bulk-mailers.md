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
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="19124-105">Gerenciar listas de remetentes seguros para correspondências em massa</span><span class="sxs-lookup"><span data-stu-id="19124-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="19124-p102">Se você quiser usar listas de remetentes confiáveis, você deve saber que Exchange Online Protection (EOP) e o Outlook manipular processamento de forma diferente. O serviço respeita remetentes e domínios inspecionando o endereço do RFC 5321.MailFrom e o endereço do RFC 5322.From, enquanto o Outlook adiciona o endereço de 5322.From do RFC à lista de remetentes seguros de um usuário. (Observação: O serviço inspeciona o endereço de 5321.MailFrom e o endereço de 5322.From para remetentes bloqueados e domínios.)</span><span class="sxs-lookup"><span data-stu-id="19124-p102">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently. The service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list. (Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="19124-p103">O endereço SMTP MAIL FROM, também é conhecido como o endereço do RFC 5321.MailFrom, é o endereço de email que é usado para executar verificações de SPF, e se o email não pode ser entregue, o caminho para o qual a mensagem de devolução é entregue. É este endereço de email é colocado no caminho de retorno nos cabeçalhos da mensagem por padrão, embora ele esteja possível para o emissor designar um endereço de retorno-caminho diferente.</span><span class="sxs-lookup"><span data-stu-id="19124-p103">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered. It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="19124-111">From: o endereço em cabeçalhos da mensagem, também é conhecido como o endereço do RFC 5322.From, é o endereço de email é exibido no cliente de email, como o Outlook.</span><span class="sxs-lookup"><span data-stu-id="19124-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="19124-p104">Grande parte dos endereços de tempo, o 5321.MailFrom e 5322.From são os mesmos. Isso é normal para a comunicação entre duas pessoas. No entanto, quando o email é enviado em nome de outra pessoa, os endereços são frequentemente diferentes. Isso geralmente ocorre com mais frequência para mensagens de email em massa.</span><span class="sxs-lookup"><span data-stu-id="19124-p104">Much of the time, the 5321.MailFrom and 5322.From addresses are the same. This is typical for person-to-person communication. However, when email is sent on behalf of someone else, the addresses are frequently different. This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="19124-p105">Por exemplo, suponha que a Blue Yonder Airlines companhias tem contratado check-out de viagens Margie enviar publicidade seu email. Em seguida, recebo uma mensagem na caixa de entrada do remetente blueyonder@news.blueyonderairlines.com. Nesse caso, o endereço de 5321.MailFrom é blueyonder.airlines@margiestravel.com e blueyonder@news.blueyonderairlines.com é o endereço de 5322.From que é exibido no Outlook. Porque o serviço respeita o endereço de 5322.From RFC, para impedir que essa mensagem obtendo filtrado, você pode simplesmente adicionar o endereço do RFC 5322.From como um remetente seguro no Outlook.</span><span class="sxs-lookup"><span data-stu-id="19124-p105">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising. You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com. In this case, the 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one you see in Outlook. Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can simply add the RFC 5322.From address as a safe sender in Outlook.</span></span>
  

