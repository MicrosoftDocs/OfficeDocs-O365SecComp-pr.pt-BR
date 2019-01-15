---
title: Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Com segurança de aplicativo de nuvem do Office 365, as ações de governança que podem ser realizadas são suspender ou cancelar a suspensão de uma conta de usuário. '
ms.openlocfilehash: 09d6ae870aa1a6b0a619ccf20f8cc19b392e23a8
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014843"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="43896-103">Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="43896-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="43896-104">Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="43896-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="43896-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="43896-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="43896-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="43896-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="43896-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="43896-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="43896-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="43896-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="43896-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="43896-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="43896-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="43896-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="43896-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="43896-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="43896-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="43896-112">You are here!</span></span>  <br/> [<span data-ttu-id="43896-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="43896-113">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="43896-p101">Suponha que você recebe um alerta que uma das contas de usuário da sua organização para o Office 365 foi comprometida. Ou então, suponha que você tiver recebido um alerta indicando que algo está errado com uma conta de usuário. Com a segurança de aplicativo de nuvem do Office 365, você pode suspender uma conta de usuário e restaurá-lo mais tarde após você ter investigados os alertas que você recebe.</span><span class="sxs-lookup"><span data-stu-id="43896-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="43896-p102">Segurança de aplicativo de nuvem do Office 365 está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a segurança de aplicativo de nuvem do Office 365 pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="43896-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="43896-120">Para suspender uma conta de usuário na segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="43896-120">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="43896-p103">Quando você suspende uma conta de usuário, você impede que o usuário entrar novamente. É o mesmo editando a conta de usuário diretamente no Office 365 para definir o status de entrada para **entrar bloqueados**.</span><span class="sxs-lookup"><span data-stu-id="43896-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="43896-p104">Se você bloquear um usuário entrar no Office 365, suspendendo-los ou editando seus status de entrada, lembre-se de que ele pode levar uma hora ou isso entre em vigor em todos os dispositivos e clientes ([Editar ou alterar um usuário no Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) do usuário. Se o usuário está conectado ao Office 365, o bloco entrará em vigor sempre que o Office 365 exige que eles entrar novamente.</span><span class="sxs-lookup"><span data-stu-id="43896-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="43896-p105">Como um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola. (Isso leva você para a segurança &amp; Centro de conformidade.)</span><span class="sxs-lookup"><span data-stu-id="43896-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="43896-127">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="43896-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="43896-128">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="43896-128">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="43896-129">![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="43896-129">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="43896-130">Na barra de navegação na parte superior da tela, escolha **alertas**.</span><span class="sxs-lookup"><span data-stu-id="43896-130">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="43896-131">Na coluna de **alerta** , clique duas vezes em um alerta que pertence a uma conta de usuário específico.</span><span class="sxs-lookup"><span data-stu-id="43896-131">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="43896-132">Em **contas**, na coluna **Status** , escolha configurações ![ícone configurações](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **usuário Suspend**.</span><span class="sxs-lookup"><span data-stu-id="43896-132">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="43896-133">Para restaurar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="43896-133">To restore a user account</span></span>

<span data-ttu-id="43896-134">Consulte a [restauração de um usuário no Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="43896-134">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="43896-135">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="43896-135">Next steps</span></span>

- [<span data-ttu-id="43896-136">Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="43896-136">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="43896-137">Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="43896-137">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="43896-138">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="43896-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

