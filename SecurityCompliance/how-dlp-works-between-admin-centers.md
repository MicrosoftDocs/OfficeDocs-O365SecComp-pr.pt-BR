---
title: Como a DLP funciona entre o &amp; centro de conformidade de segurança e o centro de administração do Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Saiba como a DLP no centro &amp; de conformidade de segurança funciona com as regras de transporte e DLP no centro de administração do Exchange.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215641"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="43f85-103">Como a DLP funciona entre o &amp; centro de conformidade de segurança e o centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="43f85-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="43f85-104">No Office 365, você pode criar uma política de prevenção de perda de dados (DLP) em dois centros de administração diferentes:</span><span class="sxs-lookup"><span data-stu-id="43f85-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="43f85-p101">No **centro de &amp; conformidade de segurança**, você pode criar uma única política de DLP para ajudar a proteger o conteúdo no SharePoint, no onedrive e no Exchange. Quando possível, recomendamos que você crie uma política de DLP aqui. Para obter mais informações, consulte [DLP no centro &amp; de conformidade de segurança](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="43f85-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="43f85-p102">No **centro de administração do Exchange**, você pode criar uma política de DLP para ajudar a proteger o conteúdo somente no Exchange. Essa política pode usar regras de transporte do Exchange, portanto, ela tem mais opções específicas para lidar com emails. Para obter mais informações, consulte [DLP no centro de administração do Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="43f85-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="43f85-111">As políticas de DLP criadas nesses centros de administração funcionam lado a lado – este tópico explica como.</span><span class="sxs-lookup"><span data-stu-id="43f85-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Páginas de DLP no centro de administração de segurança e conformidade do Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="43f85-113">Como a DLP no centro &amp; de conformidade de segurança funciona com as regras de transporte e DLP no centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="43f85-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="43f85-p103">Depois de criar uma política de DLP no centro &amp; de conformidade de segurança, a política é implantada em todos os locais incluídos na política. Se a política incluir o Exchange Online, a política será sincronizada e aplicada exatamente da mesma maneira que uma política de DLP criada no centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="43f85-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="43f85-p104">Se você tiver criado políticas de DLP no centro de administração do Exchange, essas políticas continuarão a funcionar lado a lado com todas as políticas de email que você cria &amp; no centro de conformidade de segurança. Mas Observe que as regras criadas no centro de administração do Exchange têm precedência. Todas as regras de transporte do Exchange são processadas primeiro e, em seguida, &amp; as regras de DLP do centro de conformidade de segurança são processadas.</span><span class="sxs-lookup"><span data-stu-id="43f85-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="43f85-119">Isso significa que:</span><span class="sxs-lookup"><span data-stu-id="43f85-119">This means that:</span></span>
  
- <span data-ttu-id="43f85-120">As mensagens bloqueadas pelas regras de transporte do Exchange não serão verificadas pelas regras de DLP criadas &amp; no centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="43f85-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="43f85-121">Se uma regra de transporte do Exchange modifica uma mensagem de uma maneira que faz com que ela coincida com uma política de &amp; DLP no centro de conformidade de segurança, como a adição de usuários externos, as regras de DLP detectarão isso e imporão a política, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="43f85-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="43f85-122">Observe também que as regras de transporte do Exchange que usam a ação "parar processamento" não afetam o processamento de regras de &amp; DLP no centro de conformidade de segurança, elas ainda serão processadas.</span><span class="sxs-lookup"><span data-stu-id="43f85-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="43f85-123">Dicas de política no centro &amp; de conformidade de segurança vs. o centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="43f85-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="43f85-p105">As dicas de política podem funcionar com políticas de DLP e regras de fluxo de email criadas no centro de administração do Exchange ou com políticas de &amp; DLP criadas no centro de conformidade de segurança, mas não em ambos. Isso ocorre porque essas políticas são armazenadas em locais diferentes, mas as dicas de política podem desenhar apenas de um único local.</span><span class="sxs-lookup"><span data-stu-id="43f85-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="43f85-p106">Se você configurou as dicas de política no centro de administração do Exchange, qualquer dica de política configurada no centro de conformidade de segurança &amp; não aparecerá para os usuários no Outlook na Web e no Outlook 2013 e posterior até que você desative as dicas no centro de administração do Exchange. Isso garante que as regras atuais de transporte do Exchange continuem a funcionar até que você opte por alternar para &amp; o centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="43f85-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="43f85-128">Observe que, embora as dicas de política possam desenhar apenas de um único local, as notificações por email são sempre enviadas, mesmo que você esteja usando políticas &amp; de DLP no centro de conformidade de segurança e no centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="43f85-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

