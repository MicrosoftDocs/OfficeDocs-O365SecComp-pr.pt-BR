---
title: Suporte para validação de mensagens assinadas por DKIM
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: O Exchange Online Protection (EOP) e o Exchange Online suportam validação de entrada de mensagens de Email Identificado por Chaves de Domínio (DKIM). DKIM é um método para validar que uma mensagem foi enviada do domínio que ela diz ter originado e que não foi falsificada por qualquer outra pessoa. Ele liga uma mensagem de email ao responsável da organização por enviá-la. A verificação DKIM é usada automaticamente para todas as mensagens enviadas em comunicações IPv6. (Para saber mais sobre o suporte a IPv6, veja Suporte para mensagens de email de entrada anônimas por IPv6.).
ms.openlocfilehash: 0fafc5a4754309f8f467a712f934fea3067b660d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026148"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="fa608-107">Suporte para validação de mensagens assinadas por DKIM</span><span class="sxs-lookup"><span data-stu-id="fa608-107">Support for validation of DKIM signed messages</span></span>

<span data-ttu-id="fa608-p102">O Exchange Online Protection (EOP) e o Exchange Online suportam validação de entrada de mensagens de Email Identificado por Chaves de Domínio ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)). DKIM é um método para validar que uma mensagem foi enviada do domínio que ela diz ter originado e que não foi falsificada por qualquer outra pessoa. Ele liga uma mensagem de email ao responsável da organização por enviá-la. A verificação DKIM é usada automaticamente para todas as mensagens enviadas em comunicações IPv6. (Para saber mais sobre o suporte a IPv6, veja [Suporte para mensagens de email de entrada anônimas por IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).).</span><span class="sxs-lookup"><span data-stu-id="fa608-p102">Exchange Online Protection (EOP) and Exchange Online support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages. DKIM is a method for validating that a message was sent from the domain it says it originated from and that it was not spoofed by someone else. It ties an email message to the organization responsible for sending it. DKIM verification is automatically used for all messages sent over IPv6 communications. (For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>
  
<span data-ttu-id="fa608-p103">DKIM valida uma mensagem assinada digitalmente que aparece no cabeçalho DKIM-Assinatura nos cabeçalhos de mensagens. Os resultados de uma validação DKIM-Assinatura ficam carimbados no cabeçalho Resultados-de-Autenticação que está de acordo com RFC 7001 ([Campo do cabeçalho de mensagens para indicar status de autenticação de mensagens](https://www.rfc-editor.org/rfc/rfc7001.txt)). O texto do cabeçalho de mensagens tem aparência semelhante à seguinte (em que contoso.com é o remetente):</span><span class="sxs-lookup"><span data-stu-id="fa608-p103">DKIM validates a digitally signed message that appears in the DKIM-Signature header in the message headers. The results of a DKIM-Signature validation is stamped in the Authentication-Results header which conforms with RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt)). The message header text appears similar to the following (where contoso.com is the sender):</span></span>
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
<span data-ttu-id="fa608-116">Administradores podem criar Exchange [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) nos resultados de uma validação DKIM para filtrar ou encaminhar mensagens conforme o necessário.</span><span class="sxs-lookup"><span data-stu-id="fa608-116">Admins can create Exchange [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) on the results of a DKIM validation to filter or route messages as needed.</span></span> 
  

