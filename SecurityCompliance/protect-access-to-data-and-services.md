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
# <a name="protect-access-to-data-and-services-in-office-365"></a>Proteger o acesso a dados e serviços no Office 365

Protegendo o acesso aos seus serviços e dados do Office 365 é crucial para a defesa contra ataques de virtuais e proteção contra perda de dados. As mesmas proteções podem ser aplicadas a outros aplicativos SaaS em seu ambiente e publicados pares aos aplicativos de local com Proxy de aplicativo do Windows Azure Active Directory.
  
## <a name="step-1-review-recommendations"></a>Etapa 1: Recomendações de revisão

Recursos recomendados para proteger identidades e dispositivos que acessam o Office 365, outros serviços SaaS e aplicativos locais publicados com o Proxy de Aplicativo do Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Mais idiomas](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Etapa 2: Configurar MFA

Use esses recursos para orientar você mesmo para MFA, decida qual versão é o certo para você e, em seguida, planejar e implantar MFA para seu ambiente.
  
- [Qual é a autenticação multifator Azure?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Escolha a solução do Azure a autenticação multifator para você](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Como obter o Azure a autenticação multifator](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Planejar a autenticação multifator para implantações do Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurar a autenticação multifator para usuários do Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planejar onde implantar MFA, nuvem ou no local](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Definir configurações de autenticação de vários fatores Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Etapa 3: Impor MFA com as regras de acesso condicional Azure AD.

Se você estiver usando o Windows Azure AD MFA, crie uma regra de acesso condicional para exigir MFA para acesso ao Office 365 e outros aplicativos SaaS em seu ambiente.
  
- [Acesso condicional no Windows Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Etapa 4: Configurar o gerenciamento de acesso privilegiado

Privilegiado acesso gerenciamento permite que o controle de acesso granular sobre tarefas de administração com privilégios no Office 365.  Ele pode ajudar a proteger sua organização contra violações que possam usar contas de administração com privilégios existentes com acesso a posição a dados confidenciais ou acesso às definições de configuração crítico.

- [Visão geral dos privilégios gerenciamento de acesso](privileged-access-managment-overview.md)
- [Configurar o gerenciamento de acesso privilegiado](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Etapa 5: Configurar políticas de acesso de dispositivo do SharePoint

Políticas de acesso de dispositivo para o SharePoint Online e o OneDrive for Business são recomendadas para proteger dados confidenciais, classificados e regulamentados. Em breve é a capacidade de aplicar políticas de acesso de dispositivo para sites de equipe individuais.
  
- [Controlar o acesso de dispositivos não gerenciados](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Etapa 6: Configurar o aplicativo e proteção de dados para dispositivos

Você pode gerenciar aplicativos em dispositivos móveis, independentemente se os dispositivos serão inscritos para gerenciamento de dispositivos móveis. Isso protege contra vazamento acidental de dados no Office 365, incluindo email e arquivos.
  
- Para iOS e Android: [proteger dados de aplicativo usando políticas de proteção de aplicativos com o Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Para Windows 10, configure a proteção de informações do Windows (WIP) para impedir o vazamento acidental de dados.
  
- Para dispositivos gerenciados: [criar uma proteção de informações de Windows (WIP) com a diretiva de inscrição usando o portal do Windows Azure para Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Para dispositivos não gerenciados: [criar e implantar diretivas de proteção de aplicativos de proteção de informações do Windows (WIP) com Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Etapa 7: Gerencia dispositivos com Intune

Gerenciando dispositivos permite verificar se estão íntegro e em conformidade antes de permitir o acesso aos recursos em seu ambiente. Dispositivo baseado acesso condicional regras de ajudam a garantir que os invasores não podem acessar seus recursos de dispositivos não gerenciados.
  
- [Inscrever-se os dispositivos de gerenciamento no Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Etapa 8: Configurar regras de acesso condicional para o seu ambiente e políticas de Intune adicionais

Use essas configurações recomendadas como ponto de partida para cenários de segurança de acesso sofisticados ou de escala corporativa.
  
- [Configurações e políticas de email seguro](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

