---
title: Políticas de atividades e alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definir políticas de atividade com o Office 365 Cloud app Security para configurar alertas a serem acionados quando atividades específicas acontecem ou acontecem com muita frequência. Configurando políticas para acionar alertas, você pode ser notificado sobre e monitorar atividades específicas.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219761"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="c2dea-104">Políticas de atividades e alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c2dea-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="c2dea-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c2dea-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="c2dea-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c2dea-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="c2dea-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c2dea-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="c2dea-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c2dea-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="c2dea-109">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="c2dea-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="c2dea-110">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="c2dea-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="c2dea-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="c2dea-111">You are here!</span></span>  <br/> [<span data-ttu-id="c2dea-112">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="c2dea-112">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="c2dea-113">Começar a usar</span><span class="sxs-lookup"><span data-stu-id="c2dea-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="c2dea-p102">Com o Office 365 Cloud app Security, as políticas avançadas de gerenciamento de nuvem disparam alertas para atividades específicas que acontecem ou acontecem com muito frequência. Por exemplo, suponha que um usuário tente entrar no Office 365 e falhe 70 vezes em um minuto. Suponha que outro usuário Baixe 7.000 arquivos ou que esteja conectado do Canadá, quando esse usuário deve estar em outro local. Ou pior, suponha que a conta de alguém tenha sido comprometida e um invasor esteja usando essa conta para acessar os aplicativos de nuvem e dados confidenciais da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="c2dea-p103">Se você for um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), os alertas de atividade o notificarão quando eventos como esses ocorrerem. Você pode então tomar ações específicas, como suspender uma conta de usuário até que você possa investigar o que aconteceu.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c2dea-p104">As políticas de segurança do aplicativo Cloud do Office 365 são diferentes das [políticas de alerta &amp; no centro de conformidade de segurança do Office 365](alert-policies.md). As políticas de atividade descritas neste artigo são definidas no portal do Office 365 Cloud app Security e podem ajudá-lo a gerenciar melhor o ambiente de nuvem da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="c2dea-122">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="c2dea-122">Before you begin</span></span>

<span data-ttu-id="c2dea-123">Verifique se:</span><span class="sxs-lookup"><span data-stu-id="c2dea-123">Make sure that:</span></span>
  
- <span data-ttu-id="c2dea-124">Sua organização tem o [Office 365 Cloud app Security](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="c2dea-124">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="c2dea-125">O [registro em log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2dea-125">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="c2dea-126">Você é um administrador global ou administrador de segurança do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2dea-126">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="c2dea-127">Criar uma nova política de atividade</span><span class="sxs-lookup"><span data-stu-id="c2dea-127">Create a new activity policy</span></span>

1. <span data-ttu-id="c2dea-128">Como administrador global ou administrador de segurança, vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="c2dea-128">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="c2dea-129">Isso leva você à página de políticas de segurança do aplicativo nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2dea-129">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="c2dea-130">![Ao acessar o portal do Office 365 Cloud app Security, comece com a página políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="c2dea-130">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="c2dea-131">Clique em **criar política**e selecione **política de atividade**.</span><span class="sxs-lookup"><span data-stu-id="c2dea-131">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="c2dea-132">![Ao criar uma política no O365 CAS, você pode escolher entre políticas de atividade e políticas de detecção de anomalias.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="c2dea-132">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="c2dea-p105">Na página **criar política de atividade** , especifique o **nome** e a **Descrição**da política. Para basear sua política em um modelo padrão, escolha uma na lista **modelo de política** ou crie sua própria política sem usar um modelo.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="c2dea-135">![Você pode criar políticas de atividade com o Office 365 Cloud app Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="c2dea-135">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="c2dea-p106">Escolha uma **severidade de política** (baixa, média ou alta) que mede o grau de seriedade para você se essa política disparar um alerta. Isso ajudará você a filtrar alertas quando estiver examinando mais tarde.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="c2dea-p107">Escolha uma **categoria** para esta política. Isso ajudará você a filtrar e classificar alertas que foram disparados ou a políticas de grupo quando estiver revisando a fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="c2dea-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="c2dea-140">Escolha **filtros de atividade** para configurar outras ações ou métricas que irão disparar um alerta baseado nessa política.</span><span class="sxs-lookup"><span data-stu-id="c2dea-140">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="c2dea-141">Em **parâmetros de correspondência de atividade**, especifique se uma violação de política será disparada quando uma única atividade corresponder aos filtros ou se um número especificado de atividades repetidas for necessário antes de os gatilhos de alerta.</span><span class="sxs-lookup"><span data-stu-id="c2dea-141">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="c2dea-142">Se você selecionar **atividade repetida**, especifique o número de atividades, o período de tempo e se uma violação será contabilizada para um usuário dentro de um aplicativo específico ou para o mesmo usuário com qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2dea-142">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="c2dea-143">Opcionalmente, você pode selecionar **criar alerta** para criar alertas adicionais para receber notificações dessa política (por email, mensagem de texto ou ambos).</span><span class="sxs-lookup"><span data-stu-id="c2dea-143">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="c2dea-144">\*\*Certifique-se de que seu provedor de email não bloqueie `no-reply@cloudappsecurity.com`emails enviados \*\*.</span><span class="sxs-lookup"><span data-stu-id="c2dea-144">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="c2dea-145">Escolha as **ações** que devem ser executadas quando um alerta é disparado para suspender o usuário ou solicitar que o usuário entre novamente nos aplicativos do Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2dea-145">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="c2dea-146">Escolha **criar** para concluir a criação da política.</span><span class="sxs-lookup"><span data-stu-id="c2dea-146">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="c2dea-147">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c2dea-147">Next steps</span></span>

- [<span data-ttu-id="c2dea-148">Políticas de detecção de anomalias</span><span class="sxs-lookup"><span data-stu-id="c2dea-148">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="c2dea-149">Integrar seu servidor SIEM</span><span class="sxs-lookup"><span data-stu-id="c2dea-149">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="c2dea-150">ReVisar e executar ação em alertas</span><span class="sxs-lookup"><span data-stu-id="c2dea-150">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="c2dea-151">Agrupar seus endereços IP para simplificar o gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c2dea-151">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

