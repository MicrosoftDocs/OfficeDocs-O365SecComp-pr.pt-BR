---
title: Examinar e tomar medidas em alertas no Office 365 Cloud app Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Use a página alertas no Office 365 Cloud app Security para exibir possíveis problemas e tomar ações. Você pode descartar ou resolver alertas e, se necessário, suspender uma conta de usuário.
ms.openlocfilehash: ddef10293fca7b722a13babdca5c05bbe2398cb3
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000034"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="9bdad-104">Examinar e tomar medidas em alertas no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9bdad-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="9bdad-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9bdad-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9bdad-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9bdad-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9bdad-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9bdad-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9bdad-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9bdad-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9bdad-109">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="9bdad-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9bdad-110">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="9bdad-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="9bdad-111">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="9bdad-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="9bdad-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="9bdad-112">You are here!</span></span>  <br/> [<span data-ttu-id="9bdad-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9bdad-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="9bdad-114">Você pode usar a página alertas no Office 365 Cloud app Security para exibir possíveis problemas e, se necessário, tomar medidas.</span><span class="sxs-lookup"><span data-stu-id="9bdad-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9bdad-115">Você deve ser um administrador global ou administrador de segurança para executar as tarefas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="9bdad-115">You must be a global administrator or security administrator to perform the tasks in this article.</span></span> <span data-ttu-id="9bdad-116">Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9bdad-116">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="9bdad-117">Como acessar a página alertas</span><span class="sxs-lookup"><span data-stu-id="9bdad-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="9bdad-118">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="9bdad-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="9bdad-119">Na barra de navegação na parte superior da tela, escolha **alertas**.</span><span class="sxs-lookup"><span data-stu-id="9bdad-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="9bdad-120">![Na página alertas, você pode ver os alertas que foram disparados e as ações realizadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="9bdad-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
 
> [!NOTE]
> <span data-ttu-id="9bdad-121">Os alertas de segurança do Cloud app também estão visíveis no centro de conformidade do & de segurança (vá para **alertas** > ,**exibir alertas**.</span><span class="sxs-lookup"><span data-stu-id="9bdad-121">Cloud App Security alerts are also visible in the Security & Compliance Center (go to **Alerts** > **View alerts**.</span></span> <span data-ttu-id="9bdad-122">No momento, no entanto, você deve resolver esses alertas no portal do Cloud app Security e no centro de conformidade do & de segurança.</span><span class="sxs-lookup"><span data-stu-id="9bdad-122">Currently, however, you must resolve these alerts in both the Cloud App Security portal and the Security & Compliance Center.</span></span> <span data-ttu-id="9bdad-123">Para saber mais, consulte [viewIng Cloud app Security Alerts](alert-policies.md#viewing-cloud-app-security-alerts).)</span><span class="sxs-lookup"><span data-stu-id="9bdad-123">To learn more, see [Viewing Cloud App Security alerts](alert-policies.md#viewing-cloud-app-security-alerts).)</span></span> 
 
## <a name="review-and-handle-alerts"></a><span data-ttu-id="9bdad-124">Examinar e lidar com alertas</span><span class="sxs-lookup"><span data-stu-id="9bdad-124">Review and handle alerts</span></span>

<span data-ttu-id="9bdad-125">Os alertas ajudam a identificar atividades no seu ambiente de nuvem do Office 365 que você pode querer investigar.</span><span class="sxs-lookup"><span data-stu-id="9bdad-125">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further.</span></span> <span data-ttu-id="9bdad-126">Você também pode optar por criar novas políticas ou editar políticas existentes com base nos alertas exibidos.</span><span class="sxs-lookup"><span data-stu-id="9bdad-126">You might also decide to create new policies or edit existing policies based on the alerts you see.</span></span> <span data-ttu-id="9bdad-127">Por exemplo, se você vir um administrador fazendo logon a partir de um local estranho, poderá decidir configurar uma política que impede que os administradores entrem no Office 365 de determinados locais.</span><span class="sxs-lookup"><span data-stu-id="9bdad-127">For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="9bdad-128">Você pode filtrar os alertas por **categoria** ou por **gravidade** para que possa gerenciar o mais importante primeiro.</span><span class="sxs-lookup"><span data-stu-id="9bdad-128">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="9bdad-129">Para cada alerta, examine o que causou o resultado para que você possa decidir qual ação executar.</span><span class="sxs-lookup"><span data-stu-id="9bdad-129">For each alert, look into what caused it so you can decide what action to take.</span></span> <span data-ttu-id="9bdad-130">Para ver mais detalhes sobre um alerta e realizar ações, como resolver o alerta ou suspender uma conta de usuário, escolha o alerta para abrir uma página de detalhes.</span><span class="sxs-lookup"><span data-stu-id="9bdad-130">To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page.</span></span> <span data-ttu-id="9bdad-131">Na página detalhes, você pode revisar o log de atividades, contas e usuários relacionados ao alerta e realizar ações como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="9bdad-131">On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="9bdad-132">**Ignorar** Se o alerta for falso positivo, ignore-o.</span><span class="sxs-lookup"><span data-stu-id="9bdad-132">**Dismiss** If the alert was a false positive, dismiss it.</span></span> <span data-ttu-id="9bdad-133">Opcionalmente, você pode adicionar um comentário explicando por que você o descartau.</span><span class="sxs-lookup"><span data-stu-id="9bdad-133">You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="9bdad-134">**Resolver alerta** Se o alerta foi disparado por uma atividade que você sabe que não é uma ameaça, resolva-o.</span><span class="sxs-lookup"><span data-stu-id="9bdad-134">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it.</span></span> <span data-ttu-id="9bdad-135">Opcionalmente, você pode adicionar um comentário explicando por que você o resolveu.</span><span class="sxs-lookup"><span data-stu-id="9bdad-135">You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="9bdad-136">**Suspender** Se você suspeitar de entradas não autorizadas em uma conta, por exemplo, alguém entrando de outro país quando você sabe que a pessoa está fisicamente em um escritório local, você pode [suspender a conta](suspend-or-restore-an-account-in-ocas.md) enquanto investiga o que está acontecendo.</span><span class="sxs-lookup"><span data-stu-id="9bdad-136">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="9bdad-137">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9bdad-137">Next steps</span></span>

- [<span data-ttu-id="9bdad-138">Investigar uma atividade</span><span class="sxs-lookup"><span data-stu-id="9bdad-138">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="9bdad-139">Suspender ou restaurar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="9bdad-139">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="9bdad-140">Exibir uma lista de [logs de tráfego da Web e fontes de dados](web-traffic-logs-and-data-sources-for-ocas.md) suportados</span><span class="sxs-lookup"><span data-stu-id="9bdad-140">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="9bdad-141">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="9bdad-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

