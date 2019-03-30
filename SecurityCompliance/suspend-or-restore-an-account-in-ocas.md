---
title: Suspender ou restaurar uma conta de usuário no Office 365 Cloud app Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Com o Office 365 Cloud app Security, as ações de governança que você pode executar são suspender ou cancelar a suspensão de uma conta de usuário. '
ms.openlocfilehash: d162be9d4e5382c6c03c63ae1b30043edbf0295b
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998864"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="69ab3-103">Suspender ou restaurar uma conta de usuário no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="69ab3-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="69ab3-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="69ab3-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="69ab3-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="69ab3-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="69ab3-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="69ab3-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="69ab3-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="69ab3-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="69ab3-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="69ab3-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="69ab3-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="69ab3-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="69ab3-110">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="69ab3-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="69ab3-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="69ab3-111">You are here!</span></span>  <br/> [<span data-ttu-id="69ab3-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="69ab3-112">Next steps</span></span>](#next-steps)<br/> |
   
<span data-ttu-id="69ab3-113">Suponha que você receba um alerta de que uma das contas de usuário da sua organização para o Office 365 foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="69ab3-113">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised.</span></span> <span data-ttu-id="69ab3-114">Ou, suponha que você recebeu um alerta que indica que algo está errado com uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="69ab3-114">Or, suppose that you've received an alert that indicates something is wrong with a user account.</span></span> <span data-ttu-id="69ab3-115">Com o Office 365 Cloud app Security, você pode suspender uma conta de usuário e restaurá-la posteriormente após investigar os alertas recebidos.</span><span class="sxs-lookup"><span data-stu-id="69ab3-115">With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="69ab3-116">O Office 365 Cloud app Security está disponível no Office 365 Enterprise e5.</span><span class="sxs-lookup"><span data-stu-id="69ab3-116">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="69ab3-117">Se sua organização estiver usando outra assinatura do Office 365 Enterprise, o Office 365 Cloud app Security pode ser adquirido como um complemento.</span><span class="sxs-lookup"><span data-stu-id="69ab3-117">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="69ab3-118">(como administrador global, no centro de administração do Microsoft 365, escolha **cobrança** \> **adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço da plataforma do office 365 &amp; : centro de conformidade de segurança](https://technet.microsoft.com/en-us/library/dn933793.aspx) do Office 365 e [comprar ou editar um complemento para o Office 365 for Business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="69ab3-118">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="69ab3-119">Para suspender uma conta de usuário no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="69ab3-119">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="69ab3-120">Ao suspender uma conta de usuário, você impede o usuário de entrar novamente.</span><span class="sxs-lookup"><span data-stu-id="69ab3-120">When you suspend a user account, you prevent the user from signing in again.</span></span> <span data-ttu-id="69ab3-121">É o mesmo que editar a conta de usuário diretamente no Office 365 para definir o status de entrada para **entrar em bloqueio**.</span><span class="sxs-lookup"><span data-stu-id="69ab3-121">It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="69ab3-122">Se você impedir que um usuário entre no Office 365, suspenda-o ou editando seu status de entrada, lembre-se de que pode levar uma hora ou, assim, entrar em todos os dispositivos e clientes do usuário ([Editar ou alterar um usuário no Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span><span class="sxs-lookup"><span data-stu-id="69ab3-122">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span></span> <span data-ttu-id="69ab3-123">Se o usuário estiver conectado ao Office 365, o bloco entrará em vigor sempre que o Office 365 exigir que eles entrem novamente.</span><span class="sxs-lookup"><span data-stu-id="69ab3-123">If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="69ab3-124">Como [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), acesse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="69ab3-124">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> <span data-ttu-id="69ab3-125">(Isso leva você para o centro &amp; de conformidade de segurança.)</span><span class="sxs-lookup"><span data-stu-id="69ab3-125">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="69ab3-126">No centro de &amp; conformidade de segurança, escolha **alertas** \> **Gerenciar alertas avançados**.</span><span class="sxs-lookup"><span data-stu-id="69ab3-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="69ab3-127">Escolha **ir para o Office 365 Cloud app Security**.</span><span class="sxs-lookup"><span data-stu-id="69ab3-127">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="69ab3-128">![No centro de &amp; conformidade de segurança, escolha Gerenciar alertas avançados para acessar o Office 365 Cloud app Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="69ab3-128">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="69ab3-129">Na barra de navegação na parte superior da tela, escolha **alertas**.</span><span class="sxs-lookup"><span data-stu-id="69ab3-129">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="69ab3-130">Na coluna **alerta** , clique duas vezes em um alerta que pertença a uma conta de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="69ab3-130">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="69ab3-131">Em **contas**, na coluna **status** , escolha o ícone ![](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> de configurações de **suspensão do usuário**.</span><span class="sxs-lookup"><span data-stu-id="69ab3-131">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="69ab3-132">Para restaurar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="69ab3-132">To restore a user account</span></span>

<span data-ttu-id="69ab3-133">Consulte [restaurar um usuário no Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="69ab3-133">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="69ab3-134">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="69ab3-134">Next steps</span></span>

- [<span data-ttu-id="69ab3-135">Examinar e tomar medidas em alertas no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="69ab3-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="69ab3-136">Gerenciar aplicativos OAuth usando o Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="69ab3-136">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="69ab3-137">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="69ab3-137">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

