---
title: Remover um usuário do portal de usuários restritos após o envio de email de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: c775887ecfa136bd638d0b76050c7882a6219ae4
ms.sourcegitcommit: f86383dcb9c52352661d51b22617f1809445beaa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/14/2019
ms.locfileid: "30573515"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="f0737-103">Remover um usuário do portal de usuários restritos após o envio de email de spam</span><span class="sxs-lookup"><span data-stu-id="f0737-103">Removing a user from the restricted users portal after sending spam email</span></span>

<span data-ttu-id="f0737-104">Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="f0737-104">If a user continuously sends emails from Office 365 that are classified as spam, they will be restricted from sending any more messages outbound.</span></span> <span data-ttu-id="f0737-105">O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:</span><span class="sxs-lookup"><span data-stu-id="f0737-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="f0737-106">Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido.</span><span class="sxs-lookup"><span data-stu-id="f0737-106">Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="f0737-107">O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não é mais permitido enviar mensagens fora da sua organização.</span><span class="sxs-lookup"><span data-stu-id="f0737-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization.</span></span> <span data-ttu-id="f0737-108">Entre em contato com seu administrador de email para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="f0737-108">Contact your email admin for assistance.</span></span> <span data-ttu-id="f0737-109">O servidor remoto retornou ' 550 5.1.8 acesso negado, remetente de saída inválido '</span><span class="sxs-lookup"><span data-stu-id="f0737-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f0737-110">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="f0737-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="f0737-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f0737-111"></span></span>

<span data-ttu-id="f0737-112">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="f0737-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="f0737-113">Para executar este procedimento ou estes procedimentos, você precisa receber permissões.</span><span class="sxs-lookup"><span data-stu-id="f0737-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="f0737-114">Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0737-114">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="f0737-115">O procedimento a seguir também pode ser realizado pelo PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="f0737-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="f0737-116">Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição.</span><span class="sxs-lookup"><span data-stu-id="f0737-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="f0737-117">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="f0737-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="f0737-118">Remover restrições para uma conta de email bloqueada do Office 365</span><span class="sxs-lookup"><span data-stu-id="f0737-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="f0737-119">Você conclui essa tarefa no centro de conformidade do & de segurança do Office 365 (SCC).</span><span class="sxs-lookup"><span data-stu-id="f0737-119">You complete this task in the Office 365 Security & Compliance Center (SCC).</span></span> <span data-ttu-id="f0737-120">[Vá para o centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC.</span><span class="sxs-lookup"><span data-stu-id="f0737-120">[Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="f0737-121">Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções.</span><span class="sxs-lookup"><span data-stu-id="f0737-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="f0737-122">[Vá até permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.</span><span class="sxs-lookup"><span data-stu-id="f0737-122">[Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="f0737-123">Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.</span><span class="sxs-lookup"><span data-stu-id="f0737-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f0737-124">Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="f0737-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="f0737-125">Esta página conterá a lista de usuários que foram impedidos de enviar emails para fora da sua organização.</span><span class="sxs-lookup"><span data-stu-id="f0737-125">This page will contain the list of users that have been blocked from sending mail to outside of your organization.</span></span>  <span data-ttu-id="f0737-126">Localize o usuário para o qual deseja remover as restrições e clique em **desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="f0737-126">Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="f0737-127">Um surgimento entrará nos detalhes sobre a conta cujo envio é restrito.</span><span class="sxs-lookup"><span data-stu-id="f0737-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="f0737-128">Você deve percorrer as recomendações para garantir que você esteja tomando as ações adequadas caso a conta seja realmente comprometida.</span><span class="sxs-lookup"><span data-stu-id="f0737-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="f0737-129">Clique em **Avançar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="f0737-129">Click **Next** when done.</span></span>

4. <span data-ttu-id="f0737-130">A próxima tela tem recomendações para ajudar a evitar o comprometimento futuro.</span><span class="sxs-lookup"><span data-stu-id="f0737-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="f0737-131">Habilitar a MFA (autenticação multifator) e alterar as senhas é uma boa defesa.</span><span class="sxs-lookup"><span data-stu-id="f0737-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="f0737-132">Clique em **desbloquear usuário** quando concluído.</span><span class="sxs-lookup"><span data-stu-id="f0737-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="f0737-133">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="f0737-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0737-134">Pode levar até 30 minutos para que as restrições sejam removidas.</span><span class="sxs-lookup"><span data-stu-id="f0737-134">It may take up to 30 minutes before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="f0737-135">Garantir que os administradores sejam alertados quando isso acontecer</span><span class="sxs-lookup"><span data-stu-id="f0737-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="f0737-136">Os administradores de locatários também receberão um alerta informando que o usuário foi impedido de enviar mais mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="f0737-136">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span> <span data-ttu-id="f0737-137">É um alerta padrão que é fornecido para todos os locatários e está listado na página políticas de alerta SCC, intitulado "usuário restrito a enviar email".</span><span class="sxs-lookup"><span data-stu-id="f0737-137">It is a default alert that is provided for all tenants and is listed in the SCC Alert policies page, titled "User restricted from sending email".</span></span> <span data-ttu-id="f0737-138">Vá para [políticas de alerta no centro de conformidade do & de segurança do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) para obter mais informações sobre o alerta.</span><span class="sxs-lookup"><span data-stu-id="f0737-138">Go to [Alert policies in the Office 365 Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) for more information on the alert.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="f0737-139">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="f0737-139">For more information</span></span>

[<span data-ttu-id="f0737-140">Respondendo a uma conta de email comprometida</span><span class="sxs-lookup"><span data-stu-id="f0737-140">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="f0737-141">Noções básicas sobre o usuário impedido de enviar alerta de email</span><span class="sxs-lookup"><span data-stu-id="f0737-141">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[<span data-ttu-id="f0737-142">Pool de entrega de alto risco para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="f0737-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="f0737-143">Permissões no centro de conformidade do & de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="f0737-143">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
