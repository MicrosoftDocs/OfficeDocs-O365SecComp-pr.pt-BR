---
title: Investigar uma atividade no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Com o Office 365 Cloud app Security, você pode ver o que está acontecendo no seu ambiente do Office 365 examinando e investigando atividades e contas. '
ms.openlocfilehash: 0cc3860d953b40b0b0c247af6fb2b157d1abb235
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218961"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="1f75b-103">Investigar uma atividade no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="1f75b-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="1f75b-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="1f75b-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="1f75b-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="1f75b-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="1f75b-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="1f75b-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="1f75b-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1f75b-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="1f75b-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="1f75b-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="1f75b-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="1f75b-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="1f75b-110">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="1f75b-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="1f75b-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="1f75b-111">You are here!</span></span>  <br/> [<span data-ttu-id="1f75b-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1f75b-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="1f75b-p101">O Office 365 Cloud app Security funciona com seu [log de auditoria do office 365](detailed-properties-in-the-office-365-audit-log.md). Com o Office 365 Cloud app Security, como administrador global ou administrador de segurança, você pode usar a página de registro de atividades para ver possíveis problemas em como sua organização está usando o Office 365.</span><span class="sxs-lookup"><span data-stu-id="1f75b-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="1f75b-115">Como acessar a página de log de atividades</span><span class="sxs-lookup"><span data-stu-id="1f75b-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="1f75b-116">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="1f75b-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="1f75b-117">Na barra de navegação na parte superior da tela, escolha **investigar** \> **log de atividade**.</span><span class="sxs-lookup"><span data-stu-id="1f75b-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="1f75b-118">![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="1f75b-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="1f75b-119">Analisar e investigar atividades</span><span class="sxs-lookup"><span data-stu-id="1f75b-119">Review and investigate activities</span></span>

<span data-ttu-id="1f75b-p102">Na página registro de atividades, você pode ver uma lista de várias atividades que estão sendo realizadas na sua organização usando o Office 365. Você pode usar filtros na parte superior da tela para se concentrar em um tipo específico de atividade ou um usuário específico. Por exemplo, a imagem a seguir mostra informações sobre a alteração de senha da conta de administração do Office 365 de uma organização:</span><span class="sxs-lookup"><span data-stu-id="1f75b-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![No Office 365 Cloud app Security, escolha investigar \> log de atividade.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="1f75b-p103">Ao examinar cada item no log de atividades, você pode clicar nas reticências para localizar outras atividades relacionadas. Por exemplo, você pode exibir outras atividades do mesmo tipo, do mesmo endereço IP ou do mesmo país/região.</span><span class="sxs-lookup"><span data-stu-id="1f75b-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="1f75b-p104">Você também pode exibir informações sobre muitos outros tipos de atividades. Por exemplo, aqui estão algumas das atividades que você pode exibir no log de atividades:</span><span class="sxs-lookup"><span data-stu-id="1f75b-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="1f75b-128">Membros adicionados ou removidos de grupos</span><span class="sxs-lookup"><span data-stu-id="1f75b-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="1f75b-129">Alterações nas licenças de usuário</span><span class="sxs-lookup"><span data-stu-id="1f75b-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="1f75b-130">Arquivos ou pastas compartilhados interna ou externamente</span><span class="sxs-lookup"><span data-stu-id="1f75b-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="1f75b-131">Sites ou conjuntos de sites criados ou excluídos</span><span class="sxs-lookup"><span data-stu-id="1f75b-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="1f75b-132">Regras de encaminhamento de email</span><span class="sxs-lookup"><span data-stu-id="1f75b-132">Email forwarding rules</span></span>
    
<span data-ttu-id="1f75b-133">Use a página registro de atividades para familiarizar-se com o modo como as pessoas em sua organização estão usando o Office 365 e quais problemas eles podem ter ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="1f75b-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="1f75b-134">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1f75b-134">Next steps</span></span>

- [<span data-ttu-id="1f75b-135">Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="1f75b-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="1f75b-136">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="1f75b-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

