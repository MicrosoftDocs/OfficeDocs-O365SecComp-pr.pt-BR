---
title: Suporte para validação de mensagens assinadas por DKIM
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: Saiba mais sobre a validação de mensagens assinadas do DKIM no Exchange Online Protection e no Exchange Online
ms.openlocfilehash: 0538158d052afb632dc0adbb14a88aa9766e6322
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156443"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Suporte para validação de mensagens assinadas por DKIM

O Exchange Online Protection (EOP) e o Exchange Online suportam validação de entrada de mensagens de Email Identificado por Chaves de Domínio ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)). DKIM é um método para validar que uma mensagem foi enviada do domínio que ela diz ter originado e que não foi falsificada por qualquer outra pessoa. Ele liga uma mensagem de email ao responsável da organização por enviá-la. A verificação DKIM é usada automaticamente para todas as mensagens enviadas em comunicações IPv6. (Para saber mais sobre o suporte a IPv6, veja [Suporte para mensagens de email de entrada anônimas por IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).).
  
DKIM valida uma mensagem assinada digitalmente que aparece no cabeçalho DKIM-Assinatura nos cabeçalhos de mensagens. Os resultados de uma validação DKIM-Assinatura ficam carimbados no cabeçalho Resultados-de-Autenticação que está de acordo com RFC 7001 ([Campo do cabeçalho de mensagens para indicar status de autenticação de mensagens](https://www.rfc-editor.org/rfc/rfc7001.txt)). O texto do cabeçalho de mensagens tem aparência semelhante à seguinte (em que contoso.com é o remetente):
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Os administradores podem criar [regras de fluxo](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) de emails do Exchange (também conhecidas como regras de transporte) nos resultados de uma validação de DKIM para filtrar ou rotear mensagens, conforme necessário. 
  

