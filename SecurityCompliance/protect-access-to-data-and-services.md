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
# <a name="protect-access-to-data-and-services-in-office-365"></a>Proteja o acesso a dados e serviços no Office 365

Proteger o acesso aos dados e serviços do Office 365 é crucial para se defender contra ataques de cyberismo e proteger contra a perda de dados. As mesmas proteções podem ser aplicadas a outros aplicativos SaaS em seu ambiente e até mesmo para aplicativos locais publicados com o proxy de aplicativo do Active Directory do Azure.
  
## <a name="step-1-review-recommendations"></a>Etapa 1: analisar as recomendações

Recursos recomendados para proteger identidades e dispositivos que acessam o Office 365, outros serviços SaaS e aplicativos locais publicados com o Proxy de Aplicativo do Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Mais idiomas](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Etapa 2: configurar a MFA

Use estes recursos para se orientar na MFA, decidir qual versão é adequada para você e, em seguida, planejar e implantar a MFA para seu ambiente.
  
- [O que é a autenticação multifator do Azure?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Escolha a solução de autenticação multifator do Azure para você](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Como obter a autenticação multifator do Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Planejar a autenticação multifator para implantações do Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurar a autenticação multifator para usuários do Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planejar onde implantar a MFA, a nuvem ou o local](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Definir as configurações de autenticação multifator do Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Etapa 3: impor a MFA com as regras de acesso condicional do Azure AD

Se você estiver usando o Azure AD MFA, crie uma regra de acesso condicional para exigir a MFA para acesso ao Office 365 e outros aplicativos SaaS em seu ambiente.
  
- [Acesso condicional no Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Etapa 4: configurar o gerenciamento de acesso privilegiado

O gerenciamento de acesso privilegiado permite o controle de acesso granular sobre tarefas administrativas privilegiadas no Office 365.  Ele pode ajudar a proteger sua organização contra violações que podem usar contas de administrador privilegiadas existentes com acesso à dados confidenciais ou acesso a definições de configuração crítica.

- [Visão geral do gerenciamento de acesso privilegiado](privileged-access-management-overview.md)
- [Configurar gerenciamento de acesso privilegiado](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Etapa 5: configurar as políticas de acesso do dispositivo do SharePoint

As políticas de acesso do dispositivo para o SharePoint Online e o OneDrive for Business são recomendadas para proteger dados confidenciais, classificados e regulamentados. Em breve, é a capacidade de aplicar políticas de acesso do dispositivo a sites de equipe individuais.
  
- [Controlar o acesso de dispositivos não gerenciados](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Etapa 6: configurar a proteção de aplicativos e dados para dispositivos

Você pode gerenciar aplicativos em dispositivos móveis independentemente se os dispositivos estão registrados para gerenciamento de dispositivos móveis. Isso protege contra vazamento acidental de dados no Office 365, incluindo emails e arquivos.
  
- Para iOS e Android: [proteger dados de aplicativo usando políticas de proteção de aplicativo com o Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Para o Windows 10, configure a proteção de informações do Windows (WIP) para evitar vazamentos de dados acidentais.
  
- Para dispositivos gerenciados: [criar uma proteção de informações do Windows (WIP) com a política de registro usando o portal do Azure para o Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Para dispositivos não gerenciados: [criar e implantar a política de proteção de aplicativos WIP (proteção de informações do Windows) com o Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Etapa 7: gerenciar dispositivos com o Intune

O gerenciamento de dispositivos permite que você verifique se eles estão íntegros e em conformidade antes de permitir o acesso aos recursos em seu ambiente. As regras de acesso condicional baseadas em dispositivos ajudam a garantir que os invasores não tenham acesso a seus recursos de dispositivos não gerenciados.
  
- [Registrar dispositivos para gerenciamento no Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Etapa 8: configurar políticas adicionais do Intune e regras de acesso condicional para seu ambiente

Use estas configurações recomendadas como ponto de partida para cenários de segurança de acesso sofisticado ou de escala empresarial.
  
- [Configurações e políticas de email seguro](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

