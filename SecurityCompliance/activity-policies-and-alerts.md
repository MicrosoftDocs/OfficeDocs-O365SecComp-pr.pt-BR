---
title: Políticas de atividades e alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Defina políticas de atividade com segurança de aplicativo do Office 365 nuvem para configurar alertas para disparar quando atividades específicas acontecem ou acontecer muito frequentemente. Configurando políticas para acionar os alertas, você pode ser notificado sobre e monitora atividades específicas.
ms.openlocfilehash: af364e7ff96f6d18b60d3267c5992d4c5533ea8c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29604088"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="dcef8-104">Políticas de atividades e alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="dcef8-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

<span data-ttu-id="dcef8-105">Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcef8-105">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="dcef8-106">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dcef8-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="dcef8-107">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dcef8-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="dcef8-108">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dcef8-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="dcef8-109">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcef8-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="dcef8-110">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="dcef8-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="dcef8-111">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="dcef8-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="dcef8-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="dcef8-112">You are here!</span></span>  <br/> [<span data-ttu-id="dcef8-113">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="dcef8-113">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="dcef8-114">Iniciar a utilização</span><span class="sxs-lookup"><span data-stu-id="dcef8-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="dcef8-p102">Com a segurança de aplicativo de nuvem do Office 365, políticas de gerenciamento avançado de nuvem disparam alertas para atividades específicas que acontecesse ou acontecer muito frequentemente. Por exemplo, suponha que um usuário tenta entrar no Office 365 e falha 70 vezes em um minuto. Suponha que outro usuário baixa 7.000 arquivos ou parece estar conectado no Canadá, quando o usuário deve para estar em outro local. Ou pior, suponha que a conta de alguém foi comprometida e um invasor esteja usando essa conta para acessar dados confidenciais e aplicativos de nuvem da sua organização.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="dcef8-p103">Se você for um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), os alertas de atividade notificam quando eventos, como estas ocorre. Em seguida, você pode tirar ações específicas, como suspendendo uma conta de usuário até que você possa investigar o que aconteceu.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dcef8-p104">Diretivas de segurança de aplicativo de nuvem do Office 365 são diferentes dos [políticas de segurança do Office 365 de alerta &amp; Centro de conformidade](alert-policies.md). A atividade políticas descritas neste artigo são definidas no portal de segurança de aplicativo de nuvem do Office 365 e poderá ajudá-lo gerenciar o ambiente de nuvem da sua organização.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="dcef8-123">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="dcef8-123">Before you begin</span></span>

<span data-ttu-id="dcef8-124">Verifique se:</span><span class="sxs-lookup"><span data-stu-id="dcef8-124">Make sure that:</span></span>
  
- <span data-ttu-id="dcef8-125">Sua organização tem [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="dcef8-125">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="dcef8-126">[Log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para o seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcef8-126">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="dcef8-127">Você é um administrador global ou administrador de segurança para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcef8-127">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="dcef8-128">Criar uma nova política de atividade</span><span class="sxs-lookup"><span data-stu-id="dcef8-128">Create a new activity policy</span></span>

1. <span data-ttu-id="dcef8-129">Como administrador global ou administrador de segurança, vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar.</span><span class="sxs-lookup"><span data-stu-id="dcef8-129">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="dcef8-130">Isso leva você para a página de diretivas de segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcef8-130">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="dcef8-131">![Quando você vai para o portal de segurança de aplicativo de nuvem do Office 365, você iniciar com a página de políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="dcef8-131">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="dcef8-132">Clique em **Criar política**e selecione **a política de atividade**.</span><span class="sxs-lookup"><span data-stu-id="dcef8-132">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="dcef8-133">![Quando você cria uma política no O365 CAS, você pode escolher entre as políticas de atividade e detecção de anomalias.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="dcef8-133">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="dcef8-p105">Na página **criar a política de atividade** , especifique o **nome da diretiva** e a **Descrição**. Para basear sua política em um modelo padrão, escolha uma opção na lista **modelo de política** ou criar sua própria política sem usar um modelo.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="dcef8-136">![Você pode criar políticas de atividade com segurança de aplicativo de nuvem do Office 365.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="dcef8-136">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="dcef8-p106">Escolha a **gravidade da política** (baixa, média ou alta) que mede como sérios é a você se essa diretiva dispara um alerta. Isso ajudará você filtrar alertas quando você estiver revisá-las mais tarde.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="dcef8-p107">Escolha uma **categoria** para esta diretiva. Isso ajudará você filtrar e classificar alertas que tiverem sido disparadas, ou quando você estiver revisá-las para fazer alterações de diretivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="dcef8-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="dcef8-141">Escolha **os filtros de atividade** para configurar outras ações ou métricas que acionarão um alerta com base nesta diretiva.</span><span class="sxs-lookup"><span data-stu-id="dcef8-141">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="dcef8-142">Em **atividade correspondem a parâmetros**, especifique se uma violação de política será acionada quando os filtros corresponde a uma única atividade, ou se um número especificado de atividades repetidas for necessária antes do alerta dispara.</span><span class="sxs-lookup"><span data-stu-id="dcef8-142">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="dcef8-143">Se você selecionar **repetida atividade**, especifique o número de atividades, o intervalo de tempo, e se uma violação contará para um usuário em um aplicativo específico ou para o mesmo usuário com qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcef8-143">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="dcef8-144">Opcionalmente, você pode selecionar **criar alerta** para criar alertas adicionais para receber notificações dessa diretiva (via email, mensagem de texto ou ambos).</span><span class="sxs-lookup"><span data-stu-id="dcef8-144">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="dcef8-145">\*\*Certificar-se de que o seu provedor de email não bloqueie emails enviados a partir `no-reply@cloudappsecurity.com` \*\*.</span><span class="sxs-lookup"><span data-stu-id="dcef8-145">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="dcef8-146">Escolha as **ações** que devem ser tomadas quando um alerta é acionado para suspender o usuário ou exigem que o usuário entrar novamente para aplicativos do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcef8-146">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="dcef8-147">Escolha **criar** para concluir a criação de sua política.</span><span class="sxs-lookup"><span data-stu-id="dcef8-147">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="dcef8-148">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="dcef8-148">Next steps</span></span>

- [<span data-ttu-id="dcef8-149">Políticas de detecção de anomalia</span><span class="sxs-lookup"><span data-stu-id="dcef8-149">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="dcef8-150">Integrar seu servidor SIEM</span><span class="sxs-lookup"><span data-stu-id="dcef8-150">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="dcef8-151">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="dcef8-151">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="dcef8-152">Seus endereços IP para simplificar o gerenciamento de grupo</span><span class="sxs-lookup"><span data-stu-id="dcef8-152">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

