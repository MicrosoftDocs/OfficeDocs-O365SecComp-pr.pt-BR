---
title: Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Use a página alertas na segurança de aplicativo de nuvem do Office 365 para exibir possíveis problemas e executar ação. Você pode descartar ou resolver alertas e, se necessário, suspender uma conta de usuário.
ms.openlocfilehash: 2665f4ebc9c5c24b95da64954a606dfc0df99082
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014823"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="c1766-104">Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c1766-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="c1766-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c1766-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="c1766-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c1766-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="c1766-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c1766-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="c1766-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c1766-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="c1766-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="c1766-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="c1766-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="c1766-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="c1766-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="c1766-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="c1766-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="c1766-112">You are here!</span></span>  <br/> [<span data-ttu-id="c1766-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c1766-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="c1766-114">Você pode usar a página alertas na segurança de aplicativo de nuvem do Office 365 para exibir possíveis problemas e, se necessário, executar a ação.</span><span class="sxs-lookup"><span data-stu-id="c1766-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c1766-p102">Você deve ser um administrador global ou administrador de segurança para executar as tarefas neste artigo. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c1766-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="c1766-117">Como chegar à página de alertas</span><span class="sxs-lookup"><span data-stu-id="c1766-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="c1766-118">Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="c1766-118">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="c1766-119">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="c1766-119">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="c1766-120">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="c1766-120">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="c1766-121">![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="c1766-121">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="c1766-122">Na barra de navegação na parte superior da tela, escolha **alertas**.</span><span class="sxs-lookup"><span data-stu-id="c1766-122">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="c1766-123">![Na página alertas, você pode ver os alertas que foram acionados e quaisquer ações tomadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="c1766-123">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="c1766-124">Revisão e a alça de alertas</span><span class="sxs-lookup"><span data-stu-id="c1766-124">Review and handle alerts</span></span>

<span data-ttu-id="c1766-p103">Alertas ajudarão-lo a identificar atividades no seu ambiente de nuvem do Office 365 que você talvez queira investigar melhor. Você também pode decidir criar novas políticas ou editar políticas existentes, com base nos alertas que você vê. Por exemplo, se você vir um administrador de logon de um local estranho, você decidir definir uma política que impede que os administradores entrando para o Office 365 de determinados locais.</span><span class="sxs-lookup"><span data-stu-id="c1766-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="c1766-128">Você pode filtrar os alertas por **categoria** ou por **gravidade** para que você possa gerenciar os mais importantes primeiro.</span><span class="sxs-lookup"><span data-stu-id="c1766-128">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="c1766-p104">Para cada tipo de alerta, considere o que causou para decidir qual ação a ser executada. Para obter mais detalhes sobre um alerta e ações, como resolver o alerta ou suspendendo uma conta de usuários, escolha o alerta para abrir uma página de detalhes. Na página de detalhes, você pode examinar o log da atividade, contas e usuários que estão relacionados ao alerta e realizar ações como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1766-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="c1766-p105">**Descartar** Se o alerta era um falso positivo, descartá-lo. Opcionalmente, você pode adicionar um comentário que explica por que você descartado.</span><span class="sxs-lookup"><span data-stu-id="c1766-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="c1766-p106">**Resolver alerta** Se o alerta tiver sido disparado por uma atividade que você sabe que não é uma ameaça, resolvê-lo. Opcionalmente, você pode adicionar um comentário que explica por que você resolvido.</span><span class="sxs-lookup"><span data-stu-id="c1766-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="c1766-136">**Suspender** Se você suspeitar de entrada não autorizada ins em uma conta, por exemplo, alguém entrando de outro país quando você sabe que a pessoa está fisicamente em um escritório local, é possível [suspender a conta](suspend-or-restore-an-account-in-ocas.md) enquanto você investigar o que está acontecendo.</span><span class="sxs-lookup"><span data-stu-id="c1766-136">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="c1766-137">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c1766-137">Next steps</span></span>

- [<span data-ttu-id="c1766-138">Investigar uma atividade</span><span class="sxs-lookup"><span data-stu-id="c1766-138">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="c1766-139">Suspender ou restaurar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c1766-139">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="c1766-140">Exibir uma lista de suportadas [fontes de dados e logs de tráfego da Web](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="c1766-140">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="c1766-141">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="c1766-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

