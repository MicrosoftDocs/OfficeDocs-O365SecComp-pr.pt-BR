---
title: Investigar uma atividade no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Com a segurança de aplicativo de nuvem do Office 365, você pode ver o que está acontecendo no seu ambiente do Office 365 consultando e investigando atividades e contas. '
ms.openlocfilehash: d988a86c5ceaa2ec46bc27f1aaff540fa3e0b3b4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014893"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="16fb4-103">Investigar uma atividade no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="16fb4-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="16fb4-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="16fb4-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="16fb4-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="16fb4-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="16fb4-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="16fb4-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="16fb4-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="16fb4-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="16fb4-108">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="16fb4-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="16fb4-109">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="16fb4-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="16fb4-110">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="16fb4-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="16fb4-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="16fb4-111">You are here!</span></span>  <br/> [<span data-ttu-id="16fb4-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="16fb4-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="16fb4-p101">O Office 365 segurança de aplicativo de nuvem funciona com o [log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md). Com a segurança de aplicativo de nuvem do Office 365, como um administrador global ou administrador de segurança, você pode usar a página de log da atividade para ver os possíveis problemas em como sua organização estiver usando o Office 365.</span><span class="sxs-lookup"><span data-stu-id="16fb4-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="16fb4-115">Como chegar à página de log de atividade</span><span class="sxs-lookup"><span data-stu-id="16fb4-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="16fb4-p102">Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola. (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="16fb4-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="16fb4-118">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="16fb4-118">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="16fb4-119">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="16fb4-119">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="16fb4-120">![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="16fb4-120">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="16fb4-121">Na barra de navegação na parte superior da tela, escolha **investigar** \> **log da atividade**.</span><span class="sxs-lookup"><span data-stu-id="16fb4-121">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="16fb4-122">![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="16fb4-122">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="16fb4-123">Revise e investigar atividades</span><span class="sxs-lookup"><span data-stu-id="16fb4-123">Review and investigate activities</span></span>

<span data-ttu-id="16fb4-p103">Na página log de atividade, você pode ver uma lista de várias atividades que estão ocorrendo dentro da sua organização que usam o Office 365. Você pode usar filtros na parte superior da tela para focalizar em um tipo específico de atividade ou um usuário específico. Por exemplo, a imagem a seguir mostra informações sobre a alteração de senha da conta de administração do Office 365 da organização:</span><span class="sxs-lookup"><span data-stu-id="16fb4-p103">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Na segurança de aplicativo de nuvem do Office 365, escolha investigar \> log da atividade.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="16fb4-p104">Ao olhar para cada item no registro de atividades, você pode clicar nas reticências para localizar outras atividades relacionadas. Por exemplo, você pode exibir outras atividades do mesmo tipo, a partir do mesmo endereço IP ou o mesmo país/região.</span><span class="sxs-lookup"><span data-stu-id="16fb4-p104">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="16fb4-p105">Você pode exibir informações sobre muitos outros tipos de atividades, muito. Por exemplo, aqui estão algumas das atividades que você pode exibir no registro de atividades:</span><span class="sxs-lookup"><span data-stu-id="16fb4-p105">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="16fb4-132">Membros adicionados ou removidos de grupos</span><span class="sxs-lookup"><span data-stu-id="16fb4-132">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="16fb4-133">Alterações no licenças de usuário</span><span class="sxs-lookup"><span data-stu-id="16fb4-133">Changes in user licenses</span></span>
    
- <span data-ttu-id="16fb4-134">Arquivos ou pastas compartilhadas interna ou externamente</span><span class="sxs-lookup"><span data-stu-id="16fb4-134">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="16fb4-135">Sites criadas ou excluídas ou conjuntos de sites</span><span class="sxs-lookup"><span data-stu-id="16fb4-135">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="16fb4-136">As regras de encaminhamento de email</span><span class="sxs-lookup"><span data-stu-id="16fb4-136">Email forwarding rules</span></span>
    
<span data-ttu-id="16fb4-137">Use a página de log da atividade para se familiarizar com como pessoas da sua organização estiver usando o Office 365 e o que problemas eles pode estar tendo ao longo do percurso.</span><span class="sxs-lookup"><span data-stu-id="16fb4-137">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="16fb4-138">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="16fb4-138">Next steps</span></span>

- [<span data-ttu-id="16fb4-139">Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="16fb4-139">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="16fb4-140">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="16fb4-140">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

