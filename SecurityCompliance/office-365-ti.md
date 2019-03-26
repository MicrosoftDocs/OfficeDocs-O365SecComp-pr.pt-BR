---
title: Investigação e resposta contra ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Descubra como os recursos de inteligência de ameaças no Office 365 proteção avançada contra ameaças pode ajudá-lo a Pesquisar ameaças em sua organização, responder a malware, phishing e outros ataques que o Office 365 detectou em seu nome e Pesquisar ameaças indicadores.
ms.openlocfilehash: 6f7e6e0a49bb4035458af2e9d7e45fd954a1f9fc
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732264"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="2edac-103">Investigação e resposta contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="2edac-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="2edac-104">Os recursos de investigação e resposta contra ameaças no [office 365 proteção avançada contra ameaças](office-365-atp.md) ajudam os analistas e administradores de segurança a proteger os usuários do Office 365 da sua organização:</span><span class="sxs-lookup"><span data-stu-id="2edac-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="2edac-105">Facilitando a identificação, o monitoramento e a compreensão de ataques</span><span class="sxs-lookup"><span data-stu-id="2edac-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="2edac-106">Ajudando a resolver rapidamente as ameaças no Exchange Online, no SharePoint Online, no OneDrive for Business e no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2edac-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="2edac-107">Fornecer informações e conhecimento para ajudar a evitar ataques contra sua organização</span><span class="sxs-lookup"><span data-stu-id="2edac-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="2edac-108">Investigação e resposta automatizadas para ameaças críticas baseadas em email</span><span class="sxs-lookup"><span data-stu-id="2edac-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="2edac-109">O **office 365 proteção avançada contra ameaças e investigação e resposta contra ameaças (anteriormente conhecido como Office 365 Threat Intelligence) são agora o office 365 Advanced Threat Protection Plan 2**, juntamente com outros recursos de proteção contra ameaças incluídos no determinadas assinaturas, como [o Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), a [Microsoft 365 Business, o](https://www.microsoft.com/microsoft-365/business)Office 365 Enterprise E5, o Office 365 Education a5, etc. Se sua organização tem uma assinatura que não inclui o Office 365 ATP, você pode potencialmente comprar ATP como um complemento.</span><span class="sxs-lookup"><span data-stu-id="2edac-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="2edac-110">Confira mais informações em [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="2edac-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="2edac-111">O que está mudando?</span><span class="sxs-lookup"><span data-stu-id="2edac-111">What's changing?</span></span>

<span data-ttu-id="2edac-112">Antes, o Office 365 Threat Intelligence foi incluído em assinaturas, como o Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="2edac-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="2edac-113">Esse ainda é o caso, já que os recursos de investigação e resposta contra ameaças agora fazem parte do plano de proteção avançada contra ameaças do Office 365 (e isso está incluído no Office 365 Enterprise E5).</span><span class="sxs-lookup"><span data-stu-id="2edac-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="2edac-114">Além disso, o Office 365 Threat Intelligence estava disponível para compra como um complemento para o Office 365 para clientes de negócios.</span><span class="sxs-lookup"><span data-stu-id="2edac-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="2edac-115">Agora, esses recursos estão incluídos no Office 365 Advanced Threat Protection Plan 2 (juntamente com todos os recursos do Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="2edac-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="2edac-116">Para saber mais, confira [planos e preços avançados de proteção contra ameaças do Office 365](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="2edac-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="2edac-117">Veja o que isso significa:</span><span class="sxs-lookup"><span data-stu-id="2edac-117">Here's what all this means:</span></span>

- <span data-ttu-id="2edac-118">**Se sua organização já tem o Office 365 Enterprise E5**, você já tem o plano de proteção avançada contra ameaças 2, e isso inclui recursos de investigação e resposta contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="2edac-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="2edac-119">**Se sua organização já tinha o office 365 Threat Intelligence (mas não a proteção avançada contra ameaças do office 365) como um complemento** a outra assinatura do Office 365, agora você terá o Office 365 Advanced Threat Protection Plan 2, e isso inclui recursos de investigação e resposta de ameaças.</span><span class="sxs-lookup"><span data-stu-id="2edac-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="2edac-120">**Se sua organização já teve a proteção avançada contra ameaças do office 365 (mas não o office 365 Threat Intelligence) como um complemento** a outra assinatura do Office 365, agora você terá o Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="2edac-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="2edac-121">Isso inclui o plano de proteção avançada contra ameaças do Office 365, mas não os recursos de investigação e resposta de ameaças.</span><span class="sxs-lookup"><span data-stu-id="2edac-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="2edac-122">Confira mais informações em [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="2edac-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="2edac-123">Introdução aos recursos de investigação e resposta contra ameaças</span><span class="sxs-lookup"><span data-stu-id="2edac-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="2edac-124">Use os seguintes recursos para saber mais sobre os recursos de investigação de ameaças e de resposta no Office 365 e como você pode usá-lo para manter as pessoas em sua organização mais seguras.</span><span class="sxs-lookup"><span data-stu-id="2edac-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="2edac-125">[Introdução à investigação e à resposta de ameaças](get-started-with-ti.md) (isso inclui informações sobre as funções necessárias)</span><span class="sxs-lookup"><span data-stu-id="2edac-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="2edac-126">Saiba mais sobre os rastreadores de ameaças-novidade e digno de sessão</span><span class="sxs-lookup"><span data-stu-id="2edac-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="2edac-127">Investigação e resposta automatizadas (AIR) com inteligência contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="2edac-127">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="2edac-128">Usar o explorador de ameaças no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="2edac-128">Use Threat Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
    
- [<span data-ttu-id="2edac-129">Encontre e investigue emails mal-intencionados que foram entregues</span><span class="sxs-lookup"><span data-stu-id="2edac-129">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="2edac-130">Usar o simulador de ataque</span><span class="sxs-lookup"><span data-stu-id="2edac-130">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="2edac-131">Integre a investigação e a resposta de ameaças com a proteção avançada contra ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="2edac-131">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="2edac-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2edac-132">Related topics</span></span>

[<span data-ttu-id="2edac-133">Modos de exibição do Gerenciador de ameaças</span><span class="sxs-lookup"><span data-stu-id="2edac-133">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="2edac-134">Proteção contra ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="2edac-134">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="2edac-135">Proteção Avançada contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="2edac-135">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="2edac-136">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="2edac-136">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
