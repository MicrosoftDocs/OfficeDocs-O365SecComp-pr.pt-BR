---
title: Atividades de utilização após a implantação do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Depois que você definiu e distribuiu segurança de aplicativo de nuvem do Office 365, você vai querer realizar certas tarefas para certificar-se de que sua configuração está correta e que você está preparado para revisões regulares.
ms.openlocfilehash: 71b6793f2e325fcba3431ba5157640b29814ad30
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603702"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="b7ba7-103">Atividades de utilização após a implantação do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b7ba7-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="b7ba7-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ba7-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b7ba7-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ba7-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b7ba7-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ba7-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b7ba7-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b7ba7-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b7ba7-108">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="b7ba7-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b7ba7-109">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="b7ba7-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="b7ba7-110">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="b7ba7-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="b7ba7-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="b7ba7-111">You are here!</span></span>  <br/> [<span data-ttu-id="b7ba7-112">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="b7ba7-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="b7ba7-p101">Segurança de aplicativo de nuvem do Office 365 está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a segurança de aplicativo de nuvem do Office 365 pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="b7ba7-116">Depois que você configurar e configurou a segurança de aplicativo de nuvem do Office 365, você vai querer realizar certas tarefas de utilização como um administrador global do Office 365 ou um administrador de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="b7ba7-p102">Ao executar essas tarefas, você vai ajudar a garantir que segurança de aplicativo de nuvem do Office 365 está configurada corretamente, suas políticas estão atualizadas e sua organização percebe o valor do Office 365. Use este artigo como guia para ajudá-lo a planejar para essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b7ba7-p103">Você deve ser um administrador global ou administrador de segurança para executar as tarefas descritas neste artigo. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="b7ba7-121">Atividades após a configuração inicial e a distribuição de segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="b7ba7-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="b7ba7-122">Depois de segurança de aplicativo de nuvem do Office 365 está configurada e distribuiu, como um administrador global ou administradores de segurança, você terá várias coisas a considerar:</span><span class="sxs-lookup"><span data-stu-id="b7ba7-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="b7ba7-123">Tarefas que precisam ser adicionados ao calendário do departamento de IT?</span><span class="sxs-lookup"><span data-stu-id="b7ba7-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="b7ba7-124">Como você pode verificar se a que segurança de aplicativo de nuvem do Office 365 está configurada para usar o conjunto de políticas certo ao longo do tempo?</span><span class="sxs-lookup"><span data-stu-id="b7ba7-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="b7ba7-125">Quais tipos de informações de resumo você enviar a cadeia de gerenciamento de IT</span><span class="sxs-lookup"><span data-stu-id="b7ba7-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="b7ba7-126">A tabela a seguir resume brevemente as tarefas em andamento, que você vai querer executar e a tarefas periódicas, que você deve considerar a inclusão ao calendário do seu departamento de TI.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="b7ba7-127">**Tarefas em andamento**</span><span class="sxs-lookup"><span data-stu-id="b7ba7-127">**Ongoing tasks**</span></span>|<span data-ttu-id="b7ba7-128">**Tarefas periódicas**</span><span class="sxs-lookup"><span data-stu-id="b7ba7-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b7ba7-129">Monitorar as contas de email para o qual você está enviando mensagens de alerta</span><span class="sxs-lookup"><span data-stu-id="b7ba7-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="b7ba7-130">Monitorar os feeds de notícias do setor cybersecurity para obter as informações mais recentes sobre novos ataques virtuais</span><span class="sxs-lookup"><span data-stu-id="b7ba7-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="b7ba7-131">Desenvolver os alertas de segurança para identificar e abordar os riscos e incidentes de segurança</span><span class="sxs-lookup"><span data-stu-id="b7ba7-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="b7ba7-132">Resumir cada incidente de segurança e a resolução em um log central</span><span class="sxs-lookup"><span data-stu-id="b7ba7-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="b7ba7-133">Executar as revisões mensais ou trimestrais de alertas de segurança de aplicativo de nuvem do Office 365 para problemas especiais e analisar as tendências</span><span class="sxs-lookup"><span data-stu-id="b7ba7-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="b7ba7-134">Executar as revisões mensais ou trimestrais das suas políticas de segurança de aplicativo de nuvem do Office 365 existentes para incluir melhorias na segurança de aplicativo de nuvem do Office 365 e o endereço cyberattacks novas e as tendências nas cybersecurity</span><span class="sxs-lookup"><span data-stu-id="b7ba7-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="b7ba7-135">Dependendo do tamanho e o interesse em monitoramento e manutenção de um stature de segurança da sua organização, você pode compilar um resumo mensal para sua cadeia de gerenciamento de TI que inclui:</span><span class="sxs-lookup"><span data-stu-id="b7ba7-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="b7ba7-136">Os diferentes tipos de incidentes de segurança identificados com segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="b7ba7-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="b7ba7-137">Informações de resumo de sua central log dos incidentes de segurança, como o número de incidentes detectado</span><span class="sxs-lookup"><span data-stu-id="b7ba7-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="b7ba7-138">Tendências de alertas e como eles foram abordados</span><span class="sxs-lookup"><span data-stu-id="b7ba7-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="b7ba7-139">As tendências de cybersecurity mais recentes</span><span class="sxs-lookup"><span data-stu-id="b7ba7-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="b7ba7-140">Recomendações para alterações de diretiva de segurança de aplicativo de nuvem do Office 365 e o impacto sobre os usuários finais</span><span class="sxs-lookup"><span data-stu-id="b7ba7-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="b7ba7-141">Atividades após o tempo decorrido desde a aplicação do segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="b7ba7-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="b7ba7-142">Se um protracted período de tempo decorrido desde que você inicialmente configurado ou mantido suas políticas de segurança de aplicativo de nuvem do Office 365, siga as seguintes etapas para retornar para uma configuração que reflita as metas de segurança da sua organização e os recursos atuais de segurança de aplicativo de nuvem do Office 365:</span><span class="sxs-lookup"><span data-stu-id="b7ba7-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="b7ba7-143">Determine a data da última alteração de configuração de segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="b7ba7-p104">Entender a configuração atual da segurança de aplicativo de nuvem do Office 365 e ajustar essas diretivas, conforme necessário. Por exemplo, verifique se que você sabe onde os alertas estão sendo enviadas por email.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="b7ba7-146">Consulte [What's new na segurança de aplicativo de nuvem do Office 365](new-in-office-365-cas.md) para que as alterações de produto, desde que você configurou última segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="b7ba7-147">Realize uma análise de alertas de segurança de aplicativo de nuvem do Office 365 e logs anomalias especiais e analisar tendências.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="b7ba7-148">Verifique as tendências do setor cybersecurity fique ciente as ameaças de segurança mais recentes.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="b7ba7-p105">Execute uma análise das alterações que precisam ser realizadas no conjunto atual de diretivas de segurança de aplicativo de nuvem do Office 365. Incorpore alterações de recursos, anomalias atuais e tendências de cybersecurity segurança de aplicativo de nuvem do Office 365. Recomende alterações políticas existentes ou a criação de novas políticas.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="b7ba7-p106">Faça um plano para implementar as alterações da diretiva. Se comunicar (se socializar) as consequências das alterações propostas com seus usuários finais, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="b7ba7-154">Implemente as alterações da diretiva de segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="b7ba7-155">Monitore os alertas de segurança de aplicativo de nuvem do Office 365 e comentários do usuário final e ajuste políticas ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ba7-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="b7ba7-156">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b7ba7-156">Next steps</span></span>

- [<span data-ttu-id="b7ba7-157">Investigar uma atividade</span><span class="sxs-lookup"><span data-stu-id="b7ba7-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="b7ba7-158">Suspender ou restaurar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="b7ba7-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="b7ba7-159">Gerenciar aplicativos de OAuth</span><span class="sxs-lookup"><span data-stu-id="b7ba7-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="b7ba7-160">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b7ba7-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="b7ba7-161">Exibir uma lista de suportadas [fontes de dados e logs de tráfego da Web](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="b7ba7-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

