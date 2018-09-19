---
title: Proteger o acesso a dados e serviços no Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: página de aterrissagem de proteção de acesso a dados do O365 e serviços
ms.openlocfilehash: 6ea617b1a7a7a34492689908d4816a851d58e776
ms.sourcegitcommit: 0ce722533d72fa8dcc1d8a58d3c649cb345b938d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/19/2018
ms.locfileid: "24009097"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="d1c94-103">Proteger o acesso a dados e serviços no Office 365</span><span class="sxs-lookup"><span data-stu-id="d1c94-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="d1c94-p101">Protegendo o acesso aos seus serviços e dados do Office 365 é crucial para a defesa contra ataques de virtuais e proteção contra perda de dados. As mesmas proteções podem ser aplicadas a outros aplicativos SaaS em seu ambiente e publicados pares aos aplicativos de local com Proxy de aplicativo do Windows Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1c94-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="d1c94-106">Etapa 1: Recomendações de revisão</span><span class="sxs-lookup"><span data-stu-id="d1c94-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="d1c94-107">Recursos recomendados para proteger identidades e dispositivos que acessam o Office 365, outros serviços SaaS e aplicativos locais publicados com o Proxy de Aplicativo do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d1c94-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="d1c94-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Mais idiomas](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="d1c94-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="d1c94-109">Etapa 2: Configurar MFA</span><span class="sxs-lookup"><span data-stu-id="d1c94-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="d1c94-110">Use esses recursos para orientar você mesmo para MFA, decida qual versão é o certo para você e, em seguida, planejar e implantar MFA para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="d1c94-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="d1c94-111">Qual é a autenticação multifator Azure?</span><span class="sxs-lookup"><span data-stu-id="d1c94-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="d1c94-112">Escolha a solução do Azure a autenticação multifator para você</span><span class="sxs-lookup"><span data-stu-id="d1c94-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="d1c94-113">Como obter o Azure a autenticação multifator</span><span class="sxs-lookup"><span data-stu-id="d1c94-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="d1c94-114">Planejar a autenticação multifator para implantações do Office 365</span><span class="sxs-lookup"><span data-stu-id="d1c94-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="d1c94-115">Configurar a autenticação multifator para usuários do Office 365</span><span class="sxs-lookup"><span data-stu-id="d1c94-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="d1c94-116">Planejar onde implantar MFA, nuvem ou no local</span><span class="sxs-lookup"><span data-stu-id="d1c94-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="d1c94-117">Definir configurações de autenticação de vários fatores Azure</span><span class="sxs-lookup"><span data-stu-id="d1c94-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="d1c94-118">Etapa 3: Impor MFA com as regras de acesso condicional Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d1c94-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="d1c94-119">Se você estiver usando o Windows Azure AD MFA, crie uma regra de acesso condicional para exigir MFA para acesso ao Office 365 e outros aplicativos SaaS em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="d1c94-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="d1c94-120">Acesso condicional no Windows Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d1c94-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="d1c94-121">Etapa 4: Configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="d1c94-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="d1c94-p102">Privilegiado acesso gerenciamento permite que o controle de acesso granular sobre tarefas de administração com privilégios no Office 365.  Ele pode ajudar a proteger sua organização contra violações que possam usar contas de administração com privilégios existentes com acesso a posição a dados confidenciais ou acesso às definições de configuração crítico.</span><span class="sxs-lookup"><span data-stu-id="d1c94-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="d1c94-124">Visão geral dos privilégios gerenciamento de acesso</span><span class="sxs-lookup"><span data-stu-id="d1c94-124">Overview of privileged access management</span></span>](privileged-access-managment-overview.md)
- [<span data-ttu-id="d1c94-125">Configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="d1c94-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="d1c94-126">Etapa 5: Configurar políticas de acesso de dispositivo do SharePoint</span><span class="sxs-lookup"><span data-stu-id="d1c94-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="d1c94-p103">Políticas de acesso de dispositivo para o SharePoint Online e o OneDrive for Business são recomendadas para proteger dados confidenciais, classificados e regulamentados. Em breve é a capacidade de aplicar políticas de acesso de dispositivo para sites de equipe individuais.</span><span class="sxs-lookup"><span data-stu-id="d1c94-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="d1c94-129">Controlar o acesso de dispositivos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="d1c94-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="d1c94-130">Etapa 6: Configurar o aplicativo e proteção de dados para dispositivos</span><span class="sxs-lookup"><span data-stu-id="d1c94-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="d1c94-p104">Você pode gerenciar aplicativos em dispositivos móveis, independentemente se os dispositivos serão inscritos para gerenciamento de dispositivos móveis. Isso protege contra vazamento acidental de dados no Office 365, incluindo email e arquivos.</span><span class="sxs-lookup"><span data-stu-id="d1c94-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="d1c94-133">Para iOS e Android: [proteger dados de aplicativo usando políticas de proteção de aplicativos com o Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="d1c94-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="d1c94-134">Para Windows 10, configure a proteção de informações do Windows (WIP) para impedir o vazamento acidental de dados.</span><span class="sxs-lookup"><span data-stu-id="d1c94-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="d1c94-135">Para dispositivos gerenciados: [criar uma proteção de informações de Windows (WIP) com a diretiva de inscrição usando o portal do Windows Azure para Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="d1c94-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="d1c94-136">Para dispositivos não gerenciados: [criar e implantar diretivas de proteção de aplicativos de proteção de informações do Windows (WIP) com Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="d1c94-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="d1c94-137">Etapa 7: Gerencia dispositivos com Intune</span><span class="sxs-lookup"><span data-stu-id="d1c94-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="d1c94-p105">Gerenciando dispositivos permite verificar se estão íntegro e em conformidade antes de permitir o acesso aos recursos em seu ambiente. Dispositivo baseado acesso condicional regras de ajudam a garantir que os invasores não podem acessar seus recursos de dispositivos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="d1c94-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="d1c94-140">Inscrever-se os dispositivos de gerenciamento no Intune</span><span class="sxs-lookup"><span data-stu-id="d1c94-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="d1c94-141">Etapa 8: Configurar regras de acesso condicional para o seu ambiente e políticas de Intune adicionais</span><span class="sxs-lookup"><span data-stu-id="d1c94-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="d1c94-142">Use essas configurações recomendadas como ponto de partida para cenários de segurança de acesso sofisticados ou de escala corporativa.</span><span class="sxs-lookup"><span data-stu-id="d1c94-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="d1c94-143">Configurações e políticas de email seguro</span><span class="sxs-lookup"><span data-stu-id="d1c94-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

