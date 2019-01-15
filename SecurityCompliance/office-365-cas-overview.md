---
title: Visão geral do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Segurança de aplicativo de nuvem do Office 365 oferece ideias sobre atividades suspeitas no Office 365 para que você possa investigar situações em que são potencialmente problemáticas e, se necessário, execute uma ação para solucionar problemas de segurança. '
ms.openlocfilehash: 62b1dc1d9285e60f30c1d5e541973640bb47ae35
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014923"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Visão geral do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|Você está aqui!  <br/> [Próxima etapa](get-ready-for-office-365-cas.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |[Iniciar a utilização](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Segurança de aplicativo de nuvem do Office 365 está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a segurança de aplicativo de nuvem do Office 365 pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
Segurança de aplicativo de nuvem do Office 365 oferece percepção atividades suspeitas no Office 365 para que você possa investigar situações em que são potencialmente problemáticas e, se necessário, execute uma ação para solucionar problemas de segurança. Com a segurança de aplicativo de nuvem do Office 365, você pode receber notificações de alertas disparadas para atividades atípicos ou suspeitas, consulte como os dados da sua organização no Office 365 são acessados e usados, suspender apresentando atividades suspeitas de contas de usuário e exigem usuários façam logon novamente para aplicativos do Office 365 depois que tiver sido disparado um alerta. Leia este artigo para obter uma visão geral dos recursos de segurança de aplicativo de nuvem do Office 365.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Como localizar o portal de segurança de aplicativo de nuvem do Office 365

> [!NOTE]
> Para acessar o portal de segurança de aplicativo de nuvem do Office 365, você deve ser um administrador global, administrador de segurança ou leitor de segurança. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
Você pode obter o portal de segurança de aplicativo de nuvem do Office 365 através de segurança do Office 365 &amp; Centro de conformidade. Aqui está uma boa maneira de fazê-la:
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.) 
    
2. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**. <br/>![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Se a segurança de aplicativo de nuvem do Office 365 ainda não estiver habilitada, e você é um administrador global, [Ative a segurança de aplicativo do Office 365 nuvem](turn-on-office-365-cas.md).)
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**. 
    
## <a name="policies"></a>Diretivas

O Office 365 segurança de aplicativo de nuvem trabalha com as políticas definidas para sua organização. Com a segurança de aplicativo de nuvem do Office 365, sua organização obtém muitos políticas de detecção de anomalia predefinidos e vários modelos de políticas de atividade. Essas diretivas são projetadas para detectar problemas gerais, identificar usuários de log de um endereço IP riscado, detectar ransomware atividades, detectar atividades de administrador de não-corporativos endereços IP e muito mais.
  
![No portal do CAS, selecione controle \> modelos para exibir ou criar modelos de política](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
Para exibir/uso modelos de política, no portal de segurança de aplicativo de nuvem do Office 365, vá para o **controle** \> **modelos**. 
  
![No portal do CAS O365, selecione o controle](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Para saber mais sobre políticas, consulte os seguintes recursos:
  
- [Políticas de atividades e alertas no Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Alertas

Quando as diretivas são definidas, alertas notificação-lo sobre atividades suspeitas ou atípicos detectados. Para exibir alertas para sua organização, escolha **alertas** na barra de navegação na parte superior da tela. 
  
![Na página alertas, você pode ver os alertas que foram acionados e quaisquer ações tomadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
Como os alertas são acionados, você poderá analisá-los para saber mais sobre o que está acontecendo. Em seguida, se a atividade for ainda suspeita, você pode executar a ação. Por exemplo, você pode notificar o usuário sobre um problema, suspender a um usuário faça logon para o Office 365 ou exigem um usuário entrar novamente para aplicativos do Office 365.
  
Para saber mais sobre os alertas, consulte os seguintes recursos:
  
- [Políticas de atividades e alertas no Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Revise e agir em alertas de segurança de aplicativo de nuvem do Office 365](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Logs de atividade

Exibir informações sobre as atividades do usuário em sua página de log da atividade na segurança de aplicativo de nuvem do Office 365.
  
![No portal do O365 CAS, escolha investigar \> log de atividade](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
Para obter a esta página, no portal de segurança de aplicativo de nuvem do Office 365, vá para **investigar** \> **log da atividade**. 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Você pode usar os logs de tráfego da web com segurança de aplicativo de nuvem do Office 365, muito. Os detalhes mais incluídos em que os arquivos de log, a melhor visibilidade que você vai ter em atividade do usuário. Você pode usar os arquivos de log de Barracuda, pelo azul, ponto de verificação, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, lula, Websence, Zscaler e muito mais.
  
[Saiba mais sobre as fontes de dados e logs de tráfego da web para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>Aplicativos do OAuth

Com a segurança de aplicativo de nuvem do Office 365, você pode permitir ou impedir que as pessoas na sua organização para usar aplicativos de terceiros que acessam dados no Office 365.
  
![O365 CAS, você pode acessar a página de aplicativos gerenciar OAuth no menu investigar.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Para acessar esta página, vá para **investigar** \> **OAuth apps**. 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Painel de descoberta de nuvem

O **Painel de descoberta de nuvem**, também conhecida como a **Descoberta de aplicativos de produtividade**, mostra informações sobre o uso do aplicativo de nuvem dentro da sua organização. Você pode exibir informações sobre aplicativos, usuários, tráfego, transações e muito mais usando este painel. O painel de descoberta de nuvem é semelhante à seguinte imagem: 
  
![No portal do Office 365 CAS, escolha descobrir \> painel de descoberta de nuvem](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Para obter a este painel, no portal de segurança de aplicativo de nuvem do Office 365, vá para **descobrir** \> **Painel de descoberta de nuvem**. 
  
![No portal do Office 365 CAS, escolha Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Analisar descobertas de aplicativos do Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Próximas etapas

- Obtenha o [guia de uso e casos de uso de segurança de aplicativo do Office 365 nuvem](https://aka.ms/O365CASGuide)
    
- [Introdução ao Office 365 Cloud App Security](get-ready-for-office-365-cas.md)
    

