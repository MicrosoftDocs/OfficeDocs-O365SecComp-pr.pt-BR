---
title: Introdução ao Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Começar a usar a segurança de aplicativo de nuvem do Office 365
ms.openlocfilehash: 1d1ae464278a5d9aafa5a176298f03174b6a37dc
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603692"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Introdução ao Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |Você está aqui!  <br/> [Próxima etapa](turn-on-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |[Iniciar a utilização](utilization-activities-for-ocas.md) <br/> |
   
Como se preparar para ativar e implementar a segurança de aplicativo do Office 365 nuvem (anteriormente conhecido como gerenciamento avançado de segurança) para sua organização, há algumas coisas levar em conta. Use este artigo como guia para planejar a segurança de aplicativo de nuvem do Office 365.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>Etapa 1: Identificar e proteger suas contas de administrador globais e segurança

Os administradores globais, os administradores de segurança e leitores de segurança podem acessar o portal de segurança de aplicativo de nuvem do Office 365 para visualizar políticas, examine os alertas e usar os relatórios. Os administradores globais e segurança pode definir políticas e realizar outras ações para proteger a sua organização. (Para obter mais informações, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).) Revise as contas de usuário da sua organização tem permissões elevadas como precaução. 
  
 **[Contas de administrador global de proteger seu Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>Etapa 2: Ativar o log de auditoria para sua organização

Em ordem para segurança de aplicativo do Office 365 nuvem trabalhem correto, os logs de auditoria devem ser ativado. Normalmente, isso é feito por um administrador do Exchange Online ou um administrador global.
  
 **[Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md)**. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>Etapa 3: Ir para o portal de segurança de aplicativo de nuvem do Office 365

Você pode obter o portal de segurança de aplicativo de nuvem do Office 365 indo para [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) e entrando. 

Você também pode chegar lá da segurança do Office 365 &amp; Centro de conformidade. Aqui está uma boa maneira de fazê-la:

1. Vá para [https://protection.office.com](https://protection.office.com) e sign in (isso leva você para a segurança &amp; Centro de conformidade.)
    
2. Vá para **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo de nuvem do Office 365** para ir para o portal de segurança de aplicativo de nuvem do Office 365.<br> ![Escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>Quando você vai para o portal de segurança de aplicativo de nuvem do Office 365, a primeira página que você vê é a página de políticas, que é semelhante à seguinte imagem:<br>![Quando você vai para o portal de segurança de aplicativo de nuvem do Office 365, você iniciar com a página de políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)<br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>Etapa 4: Definir políticas e configurar alertas &amp; ações

Os administradores globais e segurança definir políticas na segurança de aplicativo de nuvem do Office 365. Durante o processo de definição de políticas, os alertas e ações também são definidas. Um alerta é uma notificação com base em critérios que aparece em uma exibição ou é enviada via email. 
  
Existem dois tipos de alertas na segurança de aplicativo de nuvem do Office 365: alertas de detecção de anomalia que detectam atividades suspeitas e alertas de atividade, que são definidas para atividades que podem ser atípicos para sua organização. Alertas notificam os administradores globais e segurança quando há uma atividade em seu ambiente do Office 365 que é incomum para sua organização.
  
Consulte os seguintes recursos para saber mais:
  
- [Políticas de atividades e alertas no Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Revise e agir em alertas de segurança de aplicativo de nuvem do Office 365](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a>Etapa 5: Saiba mais sobre o uso de nuvem da sua organização

Como um administrador global, administrador de segurança ou leitor de segurança, você pode aprender sobre o uso de nuvem da sua organização por meio de relatórios e um painel de descoberta de nuvem (também chamado de descoberta de aplicativos de produtividade). Este painel mostra informações sobre usuários, aplicativos, o tráfego da web e níveis de risco.
  
![No portal do Office 365 CAS, escolha descobrir \> painel de descoberta de nuvem](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Para ir para o painel de descoberta de aplicativos de produtividade, no portal de segurança de aplicativo de nuvem do Office 365, escolha **descobrir** \> **Painel de descoberta de nuvem**.
  
![No portal do Office 365 CAS, escolha Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
Para preencher relatórios com as informações que necessárias, carregar seus arquivos de log de firewalls e proxies de sua organização. Para saber mais, consulte os seguintes recursos:
  
- [Criar relatórios de descoberta de aplicativo na segurança de aplicativo de nuvem do Office 365](create-app-discovery-reports-in-ocas.md)
    
- [Analisar descobertas de aplicativos do Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a>Etapa 6: Gerenciar aplicativos que sua organização estiver usando o Access Office 365

Como um administrador global ou administrador de segurança, você pode gerenciar aplicativos, como aplicativos personalizados ou aplicativos de terceiros, que pessoas da sua organização estão usando em seus dispositivos com o Office 365. Por exemplo, suponha que alguém tenha baixado um aplicativo personalizado que queiram usar com o Office 365. Você pode analisar os aplicativos pessoas estão usando, proibir aplicativos não confiáveis ou marcar aplicativos como aprovados para fins de acompanhamento. [Aplicativos de gerenciar OAuth usando a segurança de aplicativo de nuvem do Office 365](manage-app-permissions-in-ocas.md).
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a>Etapa 7: Use seu servidor SIEM com segurança de aplicativo de nuvem do Office 365

É a sua organização usando um servidor de gerenciamento (SIEM) de eventos e informações de segurança? O Office 365 a segurança de aplicativo de nuvem agora pode integrar com seu servidor SIEM para habilitar o monitoramento centralizado de alertas. Integrando com um serviço SIEM permite que você proteja melhor seus aplicativos em nuvem, mantendo o seu fluxo de trabalho de segurança usual, automatizando os procedimentos de segurança e correlacionando entre baseado em nuvem e eventos no local. O agente SIEM é executado em seu servidor, recebe alertas de segurança de aplicativo de nuvem do Office 365 e transmite esses alertas em seu servidor SIEM. Consulte [SIEM integração com a segurança de aplicativo de nuvem do Office 365](integrate-your-siem-server-with-office-365-cas.md).
  
## <a name="next-steps"></a>Próximas etapas

- [Ativar o Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
- Tente nosso [Guia de laboratório de teste](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) para uma experiência interativa de onde você pode demonstrar os recursos avançados de segurança de aplicativo de nuvem do Office 365 e criar uma prova de conceito. 
    

