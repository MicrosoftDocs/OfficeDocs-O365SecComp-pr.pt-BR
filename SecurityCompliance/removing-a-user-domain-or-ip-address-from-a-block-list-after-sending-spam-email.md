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
description: Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614395"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="51668-103">Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam</span><span class="sxs-lookup"><span data-stu-id="51668-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="51668-p101">Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. O usuário será listado no serviço como um remetente de saída inválido e receberá um não-entrega relatório (NDR) declarando:</span><span class="sxs-lookup"><span data-stu-id="51668-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="51668-p102">Sua mensagem não pôde ser entregue porque você não foram reconhecido como um remetente válido. O motivo mais comum para que isso é que o seu endereço de email é suspeito de envio de spam e ele não tem permissão para enviar mensagens fora da sua organização. Para obter assistência, entre em contato com seu administrador de email.  Servidor remoto retornou '550 5.1.8 acesso negado, remetente saída ruim'</span><span class="sxs-lookup"><span data-stu-id="51668-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="51668-110">Os administradores de Inquilino também receberá um alerta indicando que o usuário tiver sido protegido enviem todas as mensagens de saída mais.</span><span class="sxs-lookup"><span data-stu-id="51668-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="51668-111">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="51668-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="51668-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="51668-112"></span></span>

<span data-ttu-id="51668-113">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="51668-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="51668-p103">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a "entrada de antispam no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="51668-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="51668-p104">O procedimento a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e Remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="51668-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="51668-119">Remova as restrições de uma conta de email do Office 365 bloqueada</span><span class="sxs-lookup"><span data-stu-id="51668-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="51668-p105">Conclusão da tarefa no Centro de conformidade (SCC) do & de segurança do Office 365. Para obter mais detalhes sobre SCC, [vá para o Centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) . Você precisa estar no **Gerenciamento da organização** ou grupo de funções de **Segurança de administrador** para executar essas funções. [Vá para permissões no Centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre os grupos de função SCC.</span><span class="sxs-lookup"><span data-stu-id="51668-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="51668-124">Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365, inscreva-se no Centro de conformidade e segurança do Office 365 e na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **restrito Os usuários**.</span><span class="sxs-lookup"><span data-stu-id="51668-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="51668-125">Para ir diretamente para a página **Usuários restritos** (anteriormente conhecida como o Centro de ação) na segurança &amp; Centro de conformidade, use esta URL: gt _[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="51668-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="51668-p106">Esta página conterá a lista de usuários que foram bloqueados de envio de e-mail para fora da sua organização.  Encontre o usuário que você deseja remover restrições em e clique em **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="51668-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="51668-128">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="51668-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="51668-p107">Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Você precisará contatar o suporte para desbloquear o usuário.</span><span class="sxs-lookup"><span data-stu-id="51668-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span></br></br> <span data-ttu-id="51668-131">Pode levar até 1 hora antes que o usuário seja desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="51668-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="51668-132">Listas de bloqueio de terceiros</span><span class="sxs-lookup"><span data-stu-id="51668-132">Third-party block lists</span></span>

<span data-ttu-id="51668-p108">Exchange Online Protection também usa a listas de bloqueio de terceiros para ajudar a tomar decisões na filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para que aparecem em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de softwares de terceiros se eles pertencem a você.</span><span class="sxs-lookup"><span data-stu-id="51668-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="51668-p109">Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ficar em lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar removem-se usando o [portal de autoatendimento de retirada da lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span><span class="sxs-lookup"><span data-stu-id="51668-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="51668-138">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="51668-138">For more information</span></span>

[<span data-ttu-id="51668-139">Respondendo a uma conta de email comprometido</span><span class="sxs-lookup"><span data-stu-id="51668-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="51668-140">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="51668-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="51668-141">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="51668-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="51668-142">Permissões no Centro de conformidade de & de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="51668-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

