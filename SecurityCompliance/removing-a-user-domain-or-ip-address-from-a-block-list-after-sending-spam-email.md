---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: Se um usuário envia continuamente mensagens de email do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: 3ffd8b65d6994699093237e9f9a0a3aaa802f5e2
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223080"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="52db6-103">Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam</span><span class="sxs-lookup"><span data-stu-id="52db6-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="52db6-p101">Se um usuário envia continuamente mensagens de email do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens. O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:</span><span class="sxs-lookup"><span data-stu-id="52db6-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="52db6-p102">Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido. O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não é mais permitido enviar mensagens fora da sua organização. Entre em contato com seu administrador de email para obter assistência.  O servidor remoto retornou ' 550 5.1.8 acesso negado, remetente de saída inválido '</span><span class="sxs-lookup"><span data-stu-id="52db6-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="52db6-110">Os administradores de locatários também receberão um alerta informando que o usuário foi impedido de enviar mais mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="52db6-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="52db6-111">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="52db6-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="52db6-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="52db6-112"></span></span>

<span data-ttu-id="52db6-113">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="52db6-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="52db6-p103">Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="52db6-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="52db6-p104">O procedimento a seguir também pode ser executado por meio do PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="52db6-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="52db6-119">Remover restrições para uma conta de email bloqueada do Office 365</span><span class="sxs-lookup"><span data-stu-id="52db6-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="52db6-p105">Você conclui essa tarefa no centro de conformidade do & de segurança do Office 365 (SCC). [Vá para o centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC. Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções. [Vá até permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.</span><span class="sxs-lookup"><span data-stu-id="52db6-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="52db6-124">Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.</span><span class="sxs-lookup"><span data-stu-id="52db6-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="52db6-125">Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="52db6-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="52db6-p106">Esta página conterá a lista de usuários que foram impedidos de enviar emails para fora da sua organização.  Localize o usuário para o qual deseja remover as restrições e clique em **desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="52db6-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="52db6-128">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="52db6-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="52db6-p107">Há um limite para o número de vezes que uma conta pode ser desbloqueada pelo administrador de locatários. Se o limite de um usuário foi excedido, uma mensagem de erro será exibida. Em seguida, será necessário entrar em contato com o suporte para desbloquear o usuário.</span><span class="sxs-lookup"><span data-stu-id="52db6-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span><br/><br/> <span data-ttu-id="52db6-131">Pode levar até 1 hora para que o usuário seja desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="52db6-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="52db6-132">Listas de bloqueio de terceiros</span><span class="sxs-lookup"><span data-stu-id="52db6-132">Third-party block lists</span></span>

<span data-ttu-id="52db6-p108">O Exchange Online Protection também usa listas de bloqueio de terceiros para ajudar a tomar decisões sobre filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para aparecer em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de terceiros se eles pertencem a você.</span><span class="sxs-lookup"><span data-stu-id="52db6-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="52db6-p109">Se alguém fora do Office 365 não puder enviar mensagens para a sua conta do Office 365, sua conta poderá estar na lista de remetentes bloqueados externos. Os usuários fora do Office 365 podem tentar remover a si próprios usando o [portal de Can-lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="52db6-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="52db6-138">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="52db6-138">For more information</span></span>

[<span data-ttu-id="52db6-139">Respondendo a uma conta de email comprometida</span><span class="sxs-lookup"><span data-stu-id="52db6-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="52db6-140">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="52db6-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="52db6-141">Pool de entrega de alto risco para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="52db6-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="52db6-142">Permissões no centro de conformidade do & de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="52db6-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

