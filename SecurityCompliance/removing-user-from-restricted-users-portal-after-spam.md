---
title: Remoção de um usuário do portal de Usuários Restritos após o envio de email de spam
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/10/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: 40d63bb452392041401fd1af6d0d6d4af67e5d2b
ms.sourcegitcommit: 986f40a00ab454093b21e724d58594b8b8b4a9ba
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2019
ms.locfileid: "35613649"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="f92c9-103">Remoção de um usuário do portal de Usuários Restritos após o envio de email de spam</span><span class="sxs-lookup"><span data-stu-id="f92c9-103">Removing a user from the Restricted Users portal after sending spam email</span></span>

<span data-ttu-id="f92c9-104">Se um usuário enviar continuamente emails classificados como spam do Office 365, eles serão impedidos de enviar emails, mas ainda poderão recebê-lo.</span><span class="sxs-lookup"><span data-stu-id="f92c9-104">If a user continuously sends emails that are classified as spam from Office 365, they will be restricted from sending email, but will still be able to receive it.</span></span> <span data-ttu-id="f92c9-105">O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:</span><span class="sxs-lookup"><span data-stu-id="f92c9-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

> <span data-ttu-id="f92c9-106">"Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido.</span><span class="sxs-lookup"><span data-stu-id="f92c9-106">"Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="f92c9-107">O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não tem mais permissão para enviar emails.</span><span class="sxs-lookup"><span data-stu-id="f92c9-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send email.</span></span>  <span data-ttu-id="f92c9-108">Entre em contato com seu administrador de email para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="f92c9-108">Contact  your email admin for assistance.</span></span> <span data-ttu-id="f92c9-109">O servidor remoto retornou ' 550 5.1.8 acesso negado, emissor de saída incorreto. "</span><span class="sxs-lookup"><span data-stu-id="f92c9-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender."</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f92c9-110">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="f92c9-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="f92c9-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f92c9-111"></span></span>

<span data-ttu-id="f92c9-112">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="f92c9-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="f92c9-113">Para executar este procedimento ou estes procedimentos, você precisa receber permissões.</span><span class="sxs-lookup"><span data-stu-id="f92c9-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="f92c9-114">Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f92c9-114">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="f92c9-115">O procedimento a seguir também pode ser realizado pelo PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="f92c9-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="f92c9-116">Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição.</span><span class="sxs-lookup"><span data-stu-id="f92c9-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="f92c9-117">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="f92c9-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="f92c9-118">Remover restrições para uma conta de email bloqueada do Office 365</span><span class="sxs-lookup"><span data-stu-id="f92c9-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="f92c9-119">Você conclui essa tarefa no centro de conformidade & segurança (SCC).</span><span class="sxs-lookup"><span data-stu-id="f92c9-119">You complete this task in the Security & Compliance Center (SCC).</span></span> <span data-ttu-id="f92c9-120">[Vá para o centro de conformidade & segurança](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC.</span><span class="sxs-lookup"><span data-stu-id="f92c9-120">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="f92c9-121">Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções.</span><span class="sxs-lookup"><span data-stu-id="f92c9-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="f92c9-122">[Vá até permissões no centro de conformidade & segurança](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.</span><span class="sxs-lookup"><span data-stu-id="f92c9-122">[Go to Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="f92c9-123">Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.</span><span class="sxs-lookup"><span data-stu-id="f92c9-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f92c9-124">Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="f92c9-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="f92c9-125">Esta página conterá a lista de usuários que foram impedidos de enviar emails.</span><span class="sxs-lookup"><span data-stu-id="f92c9-125">This page will contain the list of users that have been blocked from sending email.</span></span>  <span data-ttu-id="f92c9-126">Localize o usuário para o qual você deseja remover as restrições e selecione **desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="f92c9-126">Find the user you wish to remove restrictions from, and select **Unblock**.</span></span>

3. <span data-ttu-id="f92c9-127">Um surgimento entrará nos detalhes sobre a conta cujo envio é restrito.</span><span class="sxs-lookup"><span data-stu-id="f92c9-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="f92c9-128">Você deve percorrer as recomendações para garantir que você esteja tomando as ações adequadas caso a conta seja realmente comprometida.</span><span class="sxs-lookup"><span data-stu-id="f92c9-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="f92c9-129">Clique em **Avançar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="f92c9-129">Click **Next** when done.</span></span>

4. <span data-ttu-id="f92c9-130">A próxima tela tem recomendações para ajudar a evitar o comprometimento futuro.</span><span class="sxs-lookup"><span data-stu-id="f92c9-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="f92c9-131">Habilitar a MFA (autenticação multifator) e alterar as senhas é uma boa defesa.</span><span class="sxs-lookup"><span data-stu-id="f92c9-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="f92c9-132">Clique em **desbloquear usuário** quando concluído.</span><span class="sxs-lookup"><span data-stu-id="f92c9-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="f92c9-133">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="f92c9-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f92c9-134">Pode levar 30 minutos ou mais antes de as restrições serem removidas.</span><span class="sxs-lookup"><span data-stu-id="f92c9-134">It may take 30 minutes or more before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="f92c9-135">Garantir que os administradores sejam alertados quando isso acontecer</span><span class="sxs-lookup"><span data-stu-id="f92c9-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="f92c9-136">Um alerta "usuário restrito a enviar emails" está disponível como uma política na página políticas de alerta de conformidade do Office 365 Security &.</span><span class="sxs-lookup"><span data-stu-id="f92c9-136">A "User restricted from sending email" alert is available as a policy under the Office 365 Security & Compliance Alert policies page.</span></span> <span data-ttu-id="f92c9-137">Isso era anteriormente a política de spam de saída, mas agora é nativa para a plataforma de alerta do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f92c9-137">This was formerly the outbound spam policy but is now native to the Office 365 alerting platform.</span></span> <span data-ttu-id="f92c9-138">Vá para [políticas de alerta no centro de conformidade & segurança](alert-policies.md) para obter mais informações sobre alertas.</span><span class="sxs-lookup"><span data-stu-id="f92c9-138">Go to [Alert policies in the Security & Compliance Center](alert-policies.md) for more information on alerts.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f92c9-139">Para que os alertas funcionem, a pesquisa de log de auditoria deve ser ativada.</span><span class="sxs-lookup"><span data-stu-id="f92c9-139">For alerts to work, audit log search must to be turned on.</span></span> <span data-ttu-id="f92c9-140">Confira como [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f92c9-140">See how to [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md) for more information.</span></span>

<span data-ttu-id="f92c9-141">A política para este alerta é um padrão e vem com cada locatário do Office 365 e não precisa ser configurada.</span><span class="sxs-lookup"><span data-stu-id="f92c9-141">The policy for this alert is a default one and comes with every Office 365 tenant and does not need to be set up.</span></span> <span data-ttu-id="f92c9-142">É considerado um alerta de alta gravidade e enviará um email para o grupo TenantAdmins configurado quando o alerta for acionado sempre que um usuário tiver sido restringido do envio de email.</span><span class="sxs-lookup"><span data-stu-id="f92c9-142">It is considered a High severity alert and will email the configured TenantAdmins group when the alert is fired whenever a user has been restricted from sending mail.</span></span> <span data-ttu-id="f92c9-143">Os administradores podem atualizar o grupo notificado quando esse alerta acontecer indo para o alerta sob o portal SCC > alertas > políticas de alerta > usuários restritos a enviar emails.</span><span class="sxs-lookup"><span data-stu-id="f92c9-143">Admins can update the group notified when this alert happens by going to the alert under the SCC portal > Alerts > Alert policies > Users restricted from sending email.</span></span>

<span data-ttu-id="f92c9-144">Você poderá editar o alerta para:</span><span class="sxs-lookup"><span data-stu-id="f92c9-144">You will be able to Edit the alert to:</span></span>
- <span data-ttu-id="f92c9-145">Ativar/desativar notificações por email</span><span class="sxs-lookup"><span data-stu-id="f92c9-145">Turn email notifications On/Off</span></span>
- <span data-ttu-id="f92c9-146">Enviar por email os destinatários necessários</span><span class="sxs-lookup"><span data-stu-id="f92c9-146">Email the required recipients</span></span>
- <span data-ttu-id="f92c9-147">Limitar as notificações obtidas por dia</span><span class="sxs-lookup"><span data-stu-id="f92c9-147">Limit the notifications you get per day</span></span>

## <a name="checking-for-and-removing-restrictions-using-powershell"></a><span data-ttu-id="f92c9-148">Verificando e removendo restrições usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f92c9-148">Checking for and removing restrictions using PowerShell</span></span>
<span data-ttu-id="f92c9-149">Os comandos do PowerShell para usuários restritos são:</span><span class="sxs-lookup"><span data-stu-id="f92c9-149">The PowerShell commands for Restricted Users are:</span></span>
- <span data-ttu-id="f92c9-150">`Get-BlockedSenderAddress`: Executar para recuperar a lista de usuários que não têm permissão para enviar emails</span><span class="sxs-lookup"><span data-stu-id="f92c9-150">`Get-BlockedSenderAddress`: Run to retreive the list of users that are restricted from sending email</span></span>
- <span data-ttu-id="f92c9-151">`Remove-BlockedSenderAddress`: Executar para remover usuário (s) de ser restringida</span><span class="sxs-lookup"><span data-stu-id="f92c9-151">`Remove-BlockedSenderAddress`: Run to remove user(s) from being restricted</span></span>

## <a name="for-more-information"></a><span data-ttu-id="f92c9-152">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="f92c9-152">For more information</span></span>

[<span data-ttu-id="f92c9-153">Respondendo a uma conta de email comprometida</span><span class="sxs-lookup"><span data-stu-id="f92c9-153">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="f92c9-154">Noções básicas sobre o usuário impedido de enviar alerta de email</span><span class="sxs-lookup"><span data-stu-id="f92c9-154">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[<span data-ttu-id="f92c9-155">Pool de entrega de alto risco para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="f92c9-155">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="f92c9-156">Permissões no centro de conformidade & segurança</span><span class="sxs-lookup"><span data-stu-id="f92c9-156">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

[<span data-ttu-id="f92c9-157">Políticas de alerta no centro de conformidade & segurança</span><span class="sxs-lookup"><span data-stu-id="f92c9-157">Alert policies in the Security & Compliance Center</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)
