---
title: Visão geral do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
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
ms.openlocfilehash: b146512c22cbe86ce3aef95c5916de6959341578
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706395"
---
# <a name="overview-of-office-365-cloud-app-security"></a><span data-ttu-id="c6704-103">Visão geral do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-103">Overview of Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="c6704-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c6704-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="c6704-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c6704-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="c6704-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c6704-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="c6704-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c6704-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6704-108">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="c6704-108">You are here!</span></span>  <br/> [<span data-ttu-id="c6704-109">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="c6704-109">Next step</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="c6704-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="c6704-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="c6704-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="c6704-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="c6704-112">Iniciar a utilização</span><span class="sxs-lookup"><span data-stu-id="c6704-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="c6704-p101">Segurança de aplicativo de nuvem do Office 365 está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a segurança de aplicativo de nuvem do Office 365 pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="c6704-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="c6704-p102">Segurança de aplicativo de nuvem do Office 365 oferece percepção atividades suspeitas no Office 365 para que você possa investigar situações em que são potencialmente problemáticas e, se necessário, execute uma ação para solucionar problemas de segurança. Com a segurança de aplicativo de nuvem do Office 365, você pode receber notificações de alertas disparadas para atividades atípicos ou suspeitas, consulte como os dados da sua organização no Office 365 são acessados e usados, suspender apresentando atividades suspeitas de contas de usuário e exigem usuários façam logon novamente para aplicativos do Office 365 depois que tiver sido disparado um alerta. Leia este artigo para obter uma visão geral dos recursos de segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6704-p102">Office 365 Cloud App Security gives you insight into suspicious activity in Office 365 so you can investigate situations that are potentially problematic and, if needed, take action to address security issues. With Office 365 Cloud App Security, you can receive notifications of triggered alerts for atypical or suspicious activities, see how your organization's data in Office 365 is accessed and used, suspend user accounts exhibiting suspicious activity, and require users to log back in to Office 365 apps after an alert has been triggered. Read this article to get an overview of Office 365 Cloud App Security features and capabilities.</span></span>
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="c6704-119">Como localizar o portal de segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="c6704-119">How to find the Office 365 Cloud App Security portal</span></span>

> [!NOTE]
> <span data-ttu-id="c6704-p103">Para acessar o portal de segurança de aplicativo de nuvem do Office 365, você deve ser um administrador global, administrador de segurança ou leitor de segurança. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c6704-p103">To access the Office 365 Cloud App Security portal, you must be a global administrator, security administrator, or security reader. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
<span data-ttu-id="c6704-p104">Você pode obter o portal de segurança de aplicativo de nuvem do Office 365 através de segurança do Office 365 &amp; Centro de conformidade. Aqui está uma boa maneira de fazê-la:</span><span class="sxs-lookup"><span data-stu-id="c6704-p104">You can get to the Office 365 Cloud App Security portal through the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>
  
1. <span data-ttu-id="c6704-p105">Vá para [https://security.microsoft.com](https://security.microsoft.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.)</span><span class="sxs-lookup"><span data-stu-id="c6704-p105">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="c6704-126">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="c6704-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span> <br/><span data-ttu-id="c6704-127">![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="c6704-127">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="c6704-128">(Se a segurança de aplicativo de nuvem do Office 365 ainda não estiver habilitada, e você é um administrador global, [Ative a segurança de aplicativo do Office 365 nuvem](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="c6704-128">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="c6704-129">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="c6704-129">Choose **Go to Office 365 Cloud App Security**.</span></span> 
    
## <a name="policies"></a><span data-ttu-id="c6704-130">Diretivas</span><span class="sxs-lookup"><span data-stu-id="c6704-130">Policies</span></span>

<span data-ttu-id="c6704-p106">O Office 365 segurança de aplicativo de nuvem trabalha com as políticas definidas para sua organização. Com a segurança de aplicativo de nuvem do Office 365, sua organização obtém 10 políticas de detecção de anomalia predefinidos e vários modelos de políticas de atividade. Essas diretivas são projetadas para detectar problemas gerais, identificar usuários de log de um endereço IP riscado, detectar ransomware atividades, detectar atividades de administrador de não-corporativos endereços IP e muito mais.</span><span class="sxs-lookup"><span data-stu-id="c6704-p106">Office 365 Cloud App Security works with the policies that are defined for your organization. With Office 365 Cloud App Security, your organization gets 10 predefined anomaly detection policies and several templates for activity policies. These policies are designed to detect general anomalies, identify users logging in from a risky IP address, detect ransomware activities, detect administrator activities from non-corporate IP addresses, and more.</span></span>
  
![No portal do CAS, selecione controle \> modelos para exibir ou criar modelos de política](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
<span data-ttu-id="c6704-135">Para exibir/uso modelos de política, no portal de segurança de aplicativo de nuvem do Office 365, vá para o **controle** \> **modelos**.</span><span class="sxs-lookup"><span data-stu-id="c6704-135">To view/use policy templates, in the Office 365 Cloud App Security portal, go to **Control** \> **Templates**.</span></span> 
  
![No portal do CAS O365, selecione o controle](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
<span data-ttu-id="c6704-137">Para saber mais sobre políticas, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="c6704-137">To learn more about policies, see the following resources:</span></span>
  
- [<span data-ttu-id="c6704-138">Políticas de atividades e alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-138">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="c6704-139">Políticas de detecção de anomalias no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-139">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a><span data-ttu-id="c6704-140">Alertas</span><span class="sxs-lookup"><span data-stu-id="c6704-140">Alerts</span></span>

<span data-ttu-id="c6704-p107">Quando as diretivas são definidas, alertas notificação-lo sobre atividades suspeitas ou atípicos detectados. Para exibir alertas para sua organização, escolha **alertas** na barra de navegação na parte superior da tela.</span><span class="sxs-lookup"><span data-stu-id="c6704-p107">When policies are defined, alerts notify you about suspicious or atypical activities that were detected. To view alerts for your organization, choose **Alerts** in the navigation bar across the top of the screen.</span></span> 
  
![Na página alertas, você pode ver os alertas que foram acionados e quaisquer ações tomadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
<span data-ttu-id="c6704-p108">Como os alertas são acionados, você poderá analisá-los para saber mais sobre o que está acontecendo. Em seguida, se a atividade for ainda suspeita, você pode executar a ação. Por exemplo, você pode notificar o usuário sobre um problema, suspender a um usuário faça logon para o Office 365 ou exigem um usuário entrar novamente para aplicativos do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6704-p108">As alerts are triggered you can review them to learn more about what is going on. Then, if the activity is still suspicious, you can take action. For example, you can notify a user about an issue, suspend a user from signing in to Office 365, or require a user to sign back in to Office 365 apps.</span></span>
  
<span data-ttu-id="c6704-147">Para saber mais sobre os alertas, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="c6704-147">To learn more about alerts, see the following resources:</span></span>
  
- [<span data-ttu-id="c6704-148">Políticas de atividades e alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-148">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="c6704-149">Políticas de detecção de anomalias no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-149">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="c6704-150">Revise e agir em alertas de segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="c6704-150">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a><span data-ttu-id="c6704-151">Logs de atividade</span><span class="sxs-lookup"><span data-stu-id="c6704-151">Activity logs</span></span>

<span data-ttu-id="c6704-152">Exibir informações sobre as atividades do usuário em sua página de log da atividade na segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6704-152">View information about user activities on your Activity log page in Office 365 Cloud App Security.</span></span>
  
![No portal do O365 CAS, escolha investigar \> log de atividade](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
<span data-ttu-id="c6704-154">Para obter a esta página, no portal de segurança de aplicativo de nuvem do Office 365, vá para **investigar** \> **log da atividade**.</span><span class="sxs-lookup"><span data-stu-id="c6704-154">To get to this page, in the Office 365 Cloud App Security portal, go to **Investigate** \> **Activity log**.</span></span> 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
<span data-ttu-id="c6704-p109">Você pode usar os logs de tráfego da web com segurança de aplicativo de nuvem do Office 365, muito. Os detalhes mais incluídos em que os arquivos de log, a melhor visibilidade que você vai ter em atividade do usuário. Você pode usar os arquivos de log de Barracuda, pelo azul, ponto de verificação, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, lula, Websence, Zscaler e muito mais.</span><span class="sxs-lookup"><span data-stu-id="c6704-p109">You can use your web traffic logs with Office 365 Cloud App Security, too. The more details that are included in those log files, the better visibility you'll have into user activity. You can use log files from Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, and more.</span></span>
  
[<span data-ttu-id="c6704-159">Saiba mais sobre as fontes de dados e logs de tráfego da web para segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="c6704-159">Learn about web traffic logs and data sources for Office 365 Cloud App Security</span></span>](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="app-permissions"></a><span data-ttu-id="c6704-160">Permissões de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6704-160">App permissions</span></span>

<span data-ttu-id="c6704-161">Com a segurança de aplicativo de nuvem do Office 365, você pode permitir ou impedir que as pessoas na sua organização para usar aplicativos de terceiros que acessam dados no Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6704-161">With Office 365 Cloud App Security, you can allow or prevent people in your organization to use third-party apps that access data in Office 365.</span></span>
  
![O CAS O365, você pode acessar a página Gerenciar permissões de aplicativo no menu investigar.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
<span data-ttu-id="c6704-163">Para acessar esta página, vá para **investigar** \> **permissões do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="c6704-163">To get to this page, go to **Investigate** \> **App permissions**.</span></span> 
  
![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[<span data-ttu-id="c6704-165">Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-165">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a><span data-ttu-id="c6704-166">Painel de descoberta de nuvem</span><span class="sxs-lookup"><span data-stu-id="c6704-166">Cloud Discovery Dashboard</span></span>

<span data-ttu-id="c6704-p110">O **Painel de descoberta de nuvem**, também conhecida como a **Descoberta de aplicativos de produtividade**, mostra informações sobre o uso do aplicativo de nuvem dentro da sua organização. Você pode exibir informações sobre aplicativos, usuários, tráfego, transações e muito mais usando este painel. O painel de descoberta de nuvem é semelhante à seguinte imagem:</span><span class="sxs-lookup"><span data-stu-id="c6704-p110">The **Cloud Discovery Dashboard**, also referred to as **Productivity App Discovery**, shows information about cloud app usage within your organization. You can view information about apps, users, traffic, transactions, and more using this dashboard. The Cloud Discovery Dashboard resembles the following image:</span></span> 
  
![No portal do Office 365 CAS, escolha descobrir \> painel de descoberta de nuvem](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="c6704-171">Para obter a este painel, no portal de segurança de aplicativo de nuvem do Office 365, vá para **descobrir** \> **Painel de descoberta de nuvem**.</span><span class="sxs-lookup"><span data-stu-id="c6704-171">To get to this dashboard, in the Office 365 Cloud App Security portal, go to **Discover** \> **Cloud Discovery dashboard**.</span></span> 
  
![No portal do Office 365 CAS, escolha Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[<span data-ttu-id="c6704-173">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-173">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a><span data-ttu-id="c6704-174">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c6704-174">Next steps</span></span>

- <span data-ttu-id="c6704-175">Obtenha o [guia de uso e casos de uso de segurança de aplicativo do Office 365 nuvem](https://aka.ms/O365CASGuide)</span><span class="sxs-lookup"><span data-stu-id="c6704-175">Get the [Office 365 Cloud App Security Use Cases and Usage Guide](https://aka.ms/O365CASGuide)</span></span>
    
- [<span data-ttu-id="c6704-176">Introdução ao Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c6704-176">Get ready for Office 365 Cloud App Security</span></span>](get-ready-for-office-365-cas.md)
    

