---
title: Funcionamento da DLP entre a segurança &amp; Centro de conformidade e Centro de administração do Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Saiba como DLP na segurança &amp; Centro de conformidade funciona com DLP e regras de transporte no Centro de administração do Exchange.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524332"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>Funcionamento da DLP entre a segurança &amp; Centro de conformidade e Centro de administração do Exchange

No Office 365, você pode criar uma política de prevention (DLP) de perda de dados em dois centros de admin diferentes:
  
- No **segurança &amp; Centro de conformidade**, você pode criar uma única política DLP para ajudar a proteger o conteúdo no SharePoint, OneDrive e Exchange. Quando possível, recomendamos que você crie uma política de DLP. Para obter mais informações, consulte [DLP na segurança &amp; Centro de conformidade](data-loss-prevention-policies.md).
    
- No **Centro de administração do Exchange**, você pode criar uma política de DLP para ajudar a proteger conteúdo apenas no Exchange. Essa diretiva pode usar regras de transporte do Exchange, para que ele tenha mais opções específicas para a manipulação de email. Para obter mais informações, consulte [DLP no Centro de administração do Exchange](https://go.microsoft.com/fwlink/?linkid=852311).
    
Políticas de DLP criado nesses admin centrais funcionam lado a lado - este tópico explica como.
  
![Páginas DLP no Centro de conformidade e segurança e o Centro de administração do Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>Como DLP na segurança &amp; Centro de conformidade funciona com DLP e regras de transporte no Centro de administração do Exchange

Depois de criar uma política de DLP na segurança &amp; Centro de conformidade, a política é implantado em todos os locais incluídos na política. Se a política inclui o Exchange Online, a política sincronizados lá e impostas no exatamente da mesma maneira que uma política de DLP criada no Centro de administração do Exchange. 
  
Se você tiver criado políticas de DLP no Centro de administração do Exchange, essas diretivas continuará inserido lado a lado com quaisquer políticas de email que você criar na segurança &amp; Centro de conformidade. Mas, observe que as regras criadas no Centro de administração do Exchange prevalecem. Todas as regras de transporte do Exchange são processadas primeiro e, em seguida, a DLP regras da segurança &amp; Centro de conformidade são processadas.
  
Isso significa que:
  
- Mensagens que estão bloqueadas por regras de transporte do Exchange não obter verificadas por regras DLP, criadas na segurança &amp; Centro de conformidade.
    
- Se uma regra de transporte do Exchange modifica uma mensagem de uma forma que faz com que ela corresponda a uma política de DLP na segurança &amp; Centro de conformidade - como a adição de usuários externos - e em seguida, as regras DLP detectará isso e aplicar a política conforme necessário.
    
Também Observe que regras de transporte do Exchange que usam a ação de "parar o processamento" não afetam o processamento de DLP regras na segurança &amp; Centro de conformidade - elas ainda serão processadas.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>Dicas de política na segurança &amp; Centro de conformidade versus Exchange Admin Center

Dicas de política podem trabalhar com políticas de DLP e criadas no Centro de administração do Exchange, ou com diretivas DLP, criadas na segurança de regras de fluxo de email &amp; Centro de conformidade, mas não ambos. Isso ocorre porque essas diretivas são armazenadas em locais diferentes, mas as dicas de política podem desenhar apenas de um único local.
  
Se você configurou dicas de política no Centro de administração do Exchange, quaisquer dicas de política que você definir na segurança &amp; Centro de conformidade não aparecerá aos usuários do Outlook na web e o Outlook 2013 e posterior, até que você desative as dicas no Centro de administração do Exchange. Isso garante que as regras de transporte do Exchange atuais continuará funcionando até que você escolher alternar para a segurança &amp; Centro de conformidade.
  
Observe que as notificações de email enquanto dicas de política podem desenhar apenas a partir de um único local, sempre são enviadas, mesmo se você estiver usando políticas de DLP em ambos os a segurança &amp; Centro de conformidade e o Centro de administração do Exchange.
  

