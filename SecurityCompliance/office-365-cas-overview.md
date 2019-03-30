---
title: Overview of Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'O Office 365 Cloud app Security fornece informações sobre atividades suspeitas no Office 365 para que você possa investigar situações que são potencialmente problemáticas e, se necessário, tomar medidas para resolver problemas de segurança. '
ms.openlocfilehash: 960e4c75a4da13e1a0365f75d290cd18587abd58
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001204"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Overview of Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|Você está aqui!  <br/> [Próxima etapa](get-ready-for-office-365-cas.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> O Office 365 Cloud app Security está disponível no Office 365 Enterprise e5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, o Office 365 Cloud app Security pode ser adquirido como um complemento. (como administrador global, no centro de administração do Microsoft 365, escolha **cobrança** \> **adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço da plataforma do office 365 &amp; : centro de conformidade de segurança](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) do Office 365 e [comprar ou editar um complemento para o Office 365 for Business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on). 
  
Office 365 Cloud app Security fornece informações sobre atividades suspeitas no Office 365 para que você possa investigar situações que são potencialmente problemáticas e, se necessário, tomar medidas para resolver problemas de segurança. Com o Office 365 Cloud app Security, você pode receber notificações de alertas disparados para atividades suspeitas ou atypical, Confira como os dados da sua organização no Office 365 são acessados e usados, suspender contas de usuário que apresentam atividades suspeitas e exigir os usuários façam logon novamente nos aplicativos do Office 365 depois que um alerta tiver sido acionado. Leia este artigo para obter uma visão geral dos recursos e funcionalidades do Office 365 Cloud app Security.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Como localizar o portal do Office 365 Cloud app Security

> [!NOTE]
> Para acessar o portal do Office 365 Cloud app Security, você deve ser um administrador global do Office 365, um administrador de segurança ou um leitor de segurança. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
Você pode acessar o portal do Office 365 Cloud app Security entrando no [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) e entrando. 

Você também pode chegar lá no centro de conformidade de &amp; segurança do Office 365. Veja uma boa maneira de fazer isso:
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365. (Isso leva você para o centro &amp; de conformidade de segurança.)
    
2. No centro de &amp; conformidade de segurança, escolha **alertas** \> **Gerenciar alertas avançados**. <br/>![Escolha Gerenciar alertas avançados para ir para o Office 365 Cloud app Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Se o Office 365 Cloud app Security ainda não estiver habilitado e você for um administrador global, [ative o Office 365 Cloud app Security](turn-on-office-365-cas.md).)
    
3. Escolha **ir para o Office 365 Cloud app Security**. 
    
## <a name="policies"></a>Políticas

O Office 365 Cloud app Security funciona com as políticas definidas para sua organização. Com o Office 365 Cloud app Security, sua organização obtém muitas políticas predefinidas de detecção de anomalias e vários modelos para políticas de atividade. Essas políticas foram projetadas para detectar anomalias gerais, identificar os usuários que fazem logon a partir de um endereço IP arriscado, detectar atividades de ransomware, detectar atividades de administrador de endereços IP não corporativos e muito mais.
  
![No portal CAS, escolha modelos de \> controle para exibir ou criar modelos de política](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
para exibir/usar modelos de política, no portal do Office 365 Cloud App Security, vá para **modelos**de **controle** \> . 
  
![No portal do O365 CAS, escolha controle](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Para saber mais sobre políticas, confira os seguintes recursos:
  
- [Políticas e alertas de atividades no Office 365 Cloud app Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud app Security](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Alertas

Quando as políticas são definidas, os alertas notificam você sobre atividades suspeitas ou atypical que foram detectadas. Para exibir os alertas da sua organização, escolha **alertas** na barra de navegação na parte superior da tela. 
  
![Na página alertas, você pode ver os alertas que foram disparados e as ações realizadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
À medida que os alertas são disparados, você pode examiná-los para saber mais sobre o que está acontecendo. Em seguida, se a atividade ainda for suspeita, você poderá executar uma ação. Por exemplo, você pode notificar um usuário sobre um problema, suspender um usuário de entrar no Office 365 ou exigir que um usuário entre no Office 365 aplicativos.
  
Para saber mais sobre alertas, confira os seguintes recursos:
  
- [Políticas e alertas de atividades no Office 365 Cloud app Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud app Security](anomaly-detection-policies-in-ocas.md)
    
- [Examinar e adotar medidas nos alertas do Office 365 Cloud app Security](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Logs de atividade

Exibir informações sobre as atividades do usuário na página log de atividades no Office 365 Cloud app Security.
  
![No portal do O365 CAS, escolha investigar \> log de atividade](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
para acessar essa página, no portal do Office 365 Cloud App Security, vá para **investigar** \> **log de atividade**. 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Você pode usar os logs de tráfego da Web com o Office 365 Cloud app Security também. Quanto mais detalhes são incluídos nesses arquivos de log, melhor visibilidade que você terá na atividade do usuário. É possível usar arquivos de log de Barracuda, revestimento azul, ponto de verificação, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, websence, Zscaler e muito mais.
  
[Saiba mais sobre logs de tráfego da Web e fontes de dados para o Office 365 Cloud app Security](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>Aplicativos OAuth

Com o Office 365 Cloud app Security, você pode permitir ou impedir que as pessoas em sua organização usem aplicativos de terceiros que acessam dados no Office 365.
  
![Nas autoridades de certificação do O365, você pode acessar a página Gerenciar aplicativos OAuth no menu investigar.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Para acessar essa página, vá para **investigar** \> **aplicativos OAuth**. 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Gerenciar aplicativos OAuth usando o Office 365 Cloud app Security](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Painel de descoberta de nuvem

O **painel de descoberta de nuvem**, também chamado de **descoberta de aplicativos de produtividade**, mostra informações sobre o uso do aplicativo em nuvem em sua organização. Você pode exibir informações sobre aplicativos, usuários, tráfego, transações e muito mais usando este painel. O painel de descoberta de nuvem se assemelha à imagem a seguir: 
  
![No portal CAS do Office 365, escolha descobrir \> painel de descoberta de nuvem](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
para acessar esse painel, no portal do Office 365 Cloud App Security, vá para **descobrir** \> **painel de descoberta de nuvem**. 
  
![No portal CAS do Office 365, escolha descobrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Examinar as descobertas de descoberta de aplicativos no Office 365 Cloud app Security](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Próximas etapas

- Obter o [Guia de uso e casos de uso do Office 365 Cloud app Security](https://aka.ms/O365CASGuide)
    
- [Prepare-se para o Office 365 Cloud app Security](get-ready-for-office-365-cas.md)
    

