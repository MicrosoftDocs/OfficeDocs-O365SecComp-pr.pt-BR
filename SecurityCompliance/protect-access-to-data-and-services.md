---
title: Proteja o acesso a dados e serviços no Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: página de aterrissagem para proteger o acesso a dados e serviços do O365
ms.openlocfilehash: 95933c5a7bc95f9fd70e8f3470055b57193971d4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213531"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="5de72-103">Proteja o acesso a dados e serviços no Office 365</span><span class="sxs-lookup"><span data-stu-id="5de72-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="5de72-p101">Proteger o acesso aos dados e serviços do Office 365 é crucial para se defender contra ataques de cyberismo e proteger contra a perda de dados. As mesmas proteções podem ser aplicadas a outros aplicativos SaaS em seu ambiente e até mesmo para aplicativos locais publicados com o proxy de aplicativo do Active Directory do Azure.</span><span class="sxs-lookup"><span data-stu-id="5de72-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="5de72-106">Etapa 1: analisar as recomendações</span><span class="sxs-lookup"><span data-stu-id="5de72-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="5de72-107">Recursos recomendados para proteger identidades e dispositivos que acessam o Office 365, outros serviços SaaS e aplicativos locais publicados com o Proxy de Aplicativo do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5de72-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="5de72-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Mais idiomas](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="5de72-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="5de72-109">Etapa 2: configurar a MFA</span><span class="sxs-lookup"><span data-stu-id="5de72-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="5de72-110">Use estes recursos para se orientar na MFA, decidir qual versão é adequada para você e, em seguida, planejar e implantar a MFA para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="5de72-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="5de72-111">O que é a autenticação multifator do Azure?</span><span class="sxs-lookup"><span data-stu-id="5de72-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="5de72-112">Escolha a solução de autenticação multifator do Azure para você</span><span class="sxs-lookup"><span data-stu-id="5de72-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="5de72-113">Como obter a autenticação multifator do Azure</span><span class="sxs-lookup"><span data-stu-id="5de72-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="5de72-114">Planejar a autenticação multifator para implantações do Office 365</span><span class="sxs-lookup"><span data-stu-id="5de72-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="5de72-115">Configurar a autenticação multifator para usuários do Office 365</span><span class="sxs-lookup"><span data-stu-id="5de72-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="5de72-116">Planejar onde implantar a MFA, a nuvem ou o local</span><span class="sxs-lookup"><span data-stu-id="5de72-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="5de72-117">Definir as configurações de autenticação multifator do Azure</span><span class="sxs-lookup"><span data-stu-id="5de72-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="5de72-118">Etapa 3: impor a MFA com as regras de acesso condicional do Azure AD</span><span class="sxs-lookup"><span data-stu-id="5de72-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="5de72-119">Se você estiver usando o Azure AD MFA, crie uma regra de acesso condicional para exigir a MFA para acesso ao Office 365 e outros aplicativos SaaS em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="5de72-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="5de72-120">Acesso condicional no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5de72-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="5de72-121">Etapa 4: configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="5de72-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="5de72-p102">O gerenciamento de acesso privilegiado permite o controle de acesso granular sobre tarefas administrativas privilegiadas no Office 365.  Ele pode ajudar a proteger sua organização contra violações que podem usar contas de administrador privilegiadas existentes com acesso à dados confidenciais ou acesso a definições de configuração crítica.</span><span class="sxs-lookup"><span data-stu-id="5de72-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="5de72-124">Visão geral do gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="5de72-124">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="5de72-125">Configurar gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="5de72-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="5de72-126">Etapa 5: configurar as políticas de acesso do dispositivo do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5de72-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="5de72-p103">As políticas de acesso do dispositivo para o SharePoint Online e o OneDrive for Business são recomendadas para proteger dados confidenciais, classificados e regulamentados. Em breve, é a capacidade de aplicar políticas de acesso do dispositivo a sites de equipe individuais.</span><span class="sxs-lookup"><span data-stu-id="5de72-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="5de72-129">Controlar o acesso de dispositivos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="5de72-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="5de72-130">Etapa 6: configurar a proteção de aplicativos e dados para dispositivos</span><span class="sxs-lookup"><span data-stu-id="5de72-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="5de72-p104">Você pode gerenciar aplicativos em dispositivos móveis independentemente se os dispositivos estão registrados para gerenciamento de dispositivos móveis. Isso protege contra vazamento acidental de dados no Office 365, incluindo emails e arquivos.</span><span class="sxs-lookup"><span data-stu-id="5de72-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="5de72-133">Para iOS e Android: [proteger dados de aplicativo usando políticas de proteção de aplicativo com o Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="5de72-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="5de72-134">Para o Windows 10, configure a proteção de informações do Windows (WIP) para evitar vazamentos de dados acidentais.</span><span class="sxs-lookup"><span data-stu-id="5de72-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="5de72-135">Para dispositivos gerenciados: [criar uma proteção de informações do Windows (WIP) com a política de registro usando o portal do Azure para o Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="5de72-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="5de72-136">Para dispositivos não gerenciados: [criar e implantar a política de proteção de aplicativos WIP (proteção de informações do Windows) com o Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="5de72-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="5de72-137">Etapa 7: gerenciar dispositivos com o Intune</span><span class="sxs-lookup"><span data-stu-id="5de72-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="5de72-p105">O gerenciamento de dispositivos permite que você verifique se eles estão íntegros e em conformidade antes de permitir o acesso aos recursos em seu ambiente. As regras de acesso condicional baseadas em dispositivos ajudam a garantir que os invasores não tenham acesso a seus recursos de dispositivos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="5de72-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="5de72-140">Registrar dispositivos para gerenciamento no Intune</span><span class="sxs-lookup"><span data-stu-id="5de72-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="5de72-141">Etapa 8: configurar políticas adicionais do Intune e regras de acesso condicional para seu ambiente</span><span class="sxs-lookup"><span data-stu-id="5de72-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="5de72-142">Use estas configurações recomendadas como ponto de partida para cenários de segurança de acesso sofisticado ou de escala empresarial.</span><span class="sxs-lookup"><span data-stu-id="5de72-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="5de72-143">Configurações e políticas de email seguro</span><span class="sxs-lookup"><span data-stu-id="5de72-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

