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
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="fd3fb-103">Evite caracteres inválidos em suas regras de filtro de spam e política de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="fd3fb-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="fd3fb-p101">Anteriormente, os administradores do Office 365 configurar e definidas as regras de filtro de spam e a política de filtro de spam por meio do Centro de administração do Exchange (EAC). Agora, você pode usar a segurança &amp; Centro de conformidade para gerenciar a sua configuração de antispam. Os caracteres a seguir foram suportados no EAC, mas não há suporte para uso na segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fd3fb-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="fd3fb-107">**Caracteres inválidos:**</span><span class="sxs-lookup"><span data-stu-id="fd3fb-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="fd3fb-108">Se suas regras de filtro de spam ou sua política de filtro de spam contém qualquer um dos caracteres inválidos, você pode encontrar um ou todos esses problemas:</span><span class="sxs-lookup"><span data-stu-id="fd3fb-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="fd3fb-109">Você talvez não consiga encontrar a política ou regras na segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fd3fb-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="fd3fb-110">Você pode receber erros ao tentar obter as regras ou a política usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd3fb-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="fd3fb-111">Você pode achar que a diretiva ou configurações não executar ou executar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="fd3fb-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="fd3fb-112">Remova os caracteres inválidos da política de filtro de spam e regras</span><span class="sxs-lookup"><span data-stu-id="fd3fb-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="fd3fb-113">Depois de identificar a política e regras que contêm caracteres inválidos, você pode alterar os nomes usando os cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd3fb-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="fd3fb-114">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="fd3fb-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="fd3fb-115">Para alterar o nome da política de filtro de spam, execute o cmdlet Set-HostedContentFilterPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fd3fb-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="fd3fb-116">Para alterar o nome de uma regra de filtro de spam, execute o cmdlet Set-HostedContentFilterRule da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fd3fb-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="fd3fb-117">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="fd3fb-117">For more information</span></span>

[<span data-ttu-id="fd3fb-118">Gerenciamento de segurança de ameaça &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="fd3fb-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="fd3fb-119">Set-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="fd3fb-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="fd3fb-120">Set-HostedContentFilterRule</span><span class="sxs-lookup"><span data-stu-id="fd3fb-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
