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
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="53f8c-103">Funcionamento da DLP entre a segurança &amp; Centro de conformidade e Centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="53f8c-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="53f8c-104">No Office 365, você pode criar uma política de prevention (DLP) de perda de dados em dois centros de admin diferentes:</span><span class="sxs-lookup"><span data-stu-id="53f8c-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="53f8c-p101">No **segurança &amp; Centro de conformidade**, você pode criar uma única política DLP para ajudar a proteger o conteúdo no SharePoint, OneDrive e Exchange. Quando possível, recomendamos que você crie uma política de DLP. Para obter mais informações, consulte [DLP na segurança &amp; Centro de conformidade](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="53f8c-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="53f8c-p102">No **Centro de administração do Exchange**, você pode criar uma política de DLP para ajudar a proteger conteúdo apenas no Exchange. Essa diretiva pode usar regras de transporte do Exchange, para que ele tenha mais opções específicas para a manipulação de email. Para obter mais informações, consulte [DLP no Centro de administração do Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="53f8c-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="53f8c-111">Políticas de DLP criado nesses admin centrais funcionam lado a lado - este tópico explica como.</span><span class="sxs-lookup"><span data-stu-id="53f8c-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Páginas DLP no Centro de conformidade e segurança e o Centro de administração do Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="53f8c-113">Como DLP na segurança &amp; Centro de conformidade funciona com DLP e regras de transporte no Centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="53f8c-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="53f8c-p103">Depois de criar uma política de DLP na segurança &amp; Centro de conformidade, a política é implantado em todos os locais incluídos na política. Se a política inclui o Exchange Online, a política sincronizados lá e impostas no exatamente da mesma maneira que uma política de DLP criada no Centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f8c-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="53f8c-p104">Se você tiver criado políticas de DLP no Centro de administração do Exchange, essas diretivas continuará inserido lado a lado com quaisquer políticas de email que você criar na segurança &amp; Centro de conformidade. Mas, observe que as regras criadas no Centro de administração do Exchange prevalecem. Todas as regras de transporte do Exchange são processadas primeiro e, em seguida, a DLP regras da segurança &amp; Centro de conformidade são processadas.</span><span class="sxs-lookup"><span data-stu-id="53f8c-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="53f8c-119">Isso significa que:</span><span class="sxs-lookup"><span data-stu-id="53f8c-119">This means that:</span></span>
  
- <span data-ttu-id="53f8c-120">Mensagens que estão bloqueadas por regras de transporte do Exchange não obter verificadas por regras DLP, criadas na segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="53f8c-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="53f8c-121">Se uma regra de transporte do Exchange modifica uma mensagem de uma forma que faz com que ela corresponda a uma política de DLP na segurança &amp; Centro de conformidade - como a adição de usuários externos - e em seguida, as regras DLP detectará isso e aplicar a política conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="53f8c-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="53f8c-122">Também Observe que regras de transporte do Exchange que usam a ação de "parar o processamento" não afetam o processamento de DLP regras na segurança &amp; Centro de conformidade - elas ainda serão processadas.</span><span class="sxs-lookup"><span data-stu-id="53f8c-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="53f8c-123">Dicas de política na segurança &amp; Centro de conformidade versus Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="53f8c-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="53f8c-p105">Dicas de política podem trabalhar com políticas de DLP e criadas no Centro de administração do Exchange, ou com diretivas DLP, criadas na segurança de regras de fluxo de email &amp; Centro de conformidade, mas não ambos. Isso ocorre porque essas diretivas são armazenadas em locais diferentes, mas as dicas de política podem desenhar apenas de um único local.</span><span class="sxs-lookup"><span data-stu-id="53f8c-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="53f8c-p106">Se você configurou dicas de política no Centro de administração do Exchange, quaisquer dicas de política que você definir na segurança &amp; Centro de conformidade não aparecerá aos usuários do Outlook na web e o Outlook 2013 e posterior, até que você desative as dicas no Centro de administração do Exchange. Isso garante que as regras de transporte do Exchange atuais continuará funcionando até que você escolher alternar para a segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="53f8c-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="53f8c-128">Observe que as notificações de email enquanto dicas de política podem desenhar apenas a partir de um único local, sempre são enviadas, mesmo se você estiver usando políticas de DLP em ambos os a segurança &amp; Centro de conformidade e o Centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f8c-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

