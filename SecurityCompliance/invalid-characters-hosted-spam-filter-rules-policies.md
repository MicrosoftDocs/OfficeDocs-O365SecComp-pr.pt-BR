---
title: Evite caracteres inválidos em suas regras de filtro de spam e a política de filtro de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Fornece ajuda para os administradores que possuem caracteres inválidos em suas configurações antispam e ter problemas ao tentar usar a segurança &amp; Centro de conformidade.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018730"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Evite caracteres inválidos em suas regras de filtro de spam e política de filtro de spam 

Anteriormente, os administradores do Office 365 configurar e definidas as regras de filtro de spam e a política de filtro de spam por meio do Centro de administração do Exchange (EAC). Agora, você pode usar a segurança &amp; Centro de conformidade para gerenciar a sua configuração de antispam. Os caracteres a seguir foram suportados no EAC, mas não há suporte para uso na segurança &amp; Centro de conformidade.  

**Caracteres inválidos:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Se suas regras de filtro de spam ou sua política de filtro de spam contém qualquer um dos caracteres inválidos, você pode encontrar um ou todos esses problemas:
- Você talvez não consiga encontrar a política ou regras na segurança &amp; Centro de conformidade.
- Você pode receber erros ao tentar obter as regras ou a política usando o Windows PowerShell.
- Você pode achar que a diretiva ou configurações não executar ou executar conforme o esperado.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Remova os caracteres inválidos da política de filtro de spam e regras

Depois de identificar a política e regras que contêm caracteres inválidos, você pode alterar os nomes usando os cmdlets do Windows PowerShell. 

1. [Conecte-se ao Exchange Online usando o PowerShell remoto](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Para alterar o nome da política de filtro de spam, execute o cmdlet Set-HostedContentFilterPolicy da seguinte maneira:
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Para alterar o nome de uma regra de filtro de spam, execute o cmdlet Set-HostedContentFilterRule da seguinte maneira:
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Para saber mais

[Gerenciamento de segurança de ameaça &amp; Centro de conformidade](threat-management.md)
  
[Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Set-HostedContentFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
