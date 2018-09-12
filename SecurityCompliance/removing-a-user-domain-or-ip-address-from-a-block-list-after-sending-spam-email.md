---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: 8dcd6c8f55d867e1c2e249ec71a3a5c6b78ac76a
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955433"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="7cdbe-103">Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam</span><span class="sxs-lookup"><span data-stu-id="7cdbe-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="7cdbe-p101">Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. O usuário será listado no serviço como um remetente de saída inválido e receberá um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>

<span data-ttu-id="7cdbe-p102">Você pode configurar as configurações de política de spam de saída para que você receber uma notificação quando um usuário do Office 365 é impedido de envio de email. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p102">You can configure your outbound spam policy settings so that you get a notification when an Office 365 user is blocked from sending email. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="7cdbe-108">Desbloquear uma conta de email do Office 365</span><span class="sxs-lookup"><span data-stu-id="7cdbe-108">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="7cdbe-p103">Conclusão da tarefa no Centro de conformidade (SCC) & segurança do Office 365. [Vá para o Centro de conformidade & segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="7cdbe-111">Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365, inscreva-se no Centro de conformidade e segurança do Office 365 e na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **restrito Os usuários**.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-111">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="7cdbe-112">Para ir diretamente para a página **Usuários restritos** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="7cdbe-112">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="7cdbe-p104">Esta página conterá a lista de usuários que foram bloqueados de envio de e-mail para fora da sua organização.  Encontre o usuário que você deseja remover restrições em e clique em **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="7cdbe-115">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-115">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7cdbe-p105">Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Você precisará contatar o suporte para desbloquear o usuário.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="7cdbe-118">Listas de bloqueio de terceiros</span><span class="sxs-lookup"><span data-stu-id="7cdbe-118">Third-party block lists</span></span>

<span data-ttu-id="7cdbe-p106">Exchange Online Protection também usa a listas de bloqueio de terceiros para ajudar a tomar decisões na filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para que aparecem em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de softwares de terceiros se eles pertencem a você. Use os links a tabela a seguir para cada terceiros entre em contato e siga suas instruções.</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p106">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you. Use the links in the below table to contact each third party and then follow their instructions.</span></span>

|<span data-ttu-id="7cdbe-123">\*\*Nome da Lista \*\*</span><span class="sxs-lookup"><span data-stu-id="7cdbe-123">**List Name**</span></span>|<span data-ttu-id="7cdbe-124">**Portal para Retirada da Lista**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-124">**Delisting Portal**</span></span>|<span data-ttu-id="7cdbe-125">**Para saber mais**</span><span class="sxs-lookup"><span data-stu-id="7cdbe-125">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cdbe-126">URIBL</span><span class="sxs-lookup"><span data-stu-id="7cdbe-126">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="7cdbe-127">Site URIBL</span><span class="sxs-lookup"><span data-stu-id="7cdbe-127">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="7cdbe-128">SURBL</span><span class="sxs-lookup"><span data-stu-id="7cdbe-128">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="7cdbe-129">Apresentando os dados de reputação de URI de SURBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="7cdbe-129">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="7cdbe-130">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="7cdbe-130">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="7cdbe-131">Entendendo a filtragem DNSBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="7cdbe-131">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="7cdbe-132">invaluement</span><span class="sxs-lookup"><span data-stu-id="7cdbe-132">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="7cdbe-133">lista de anti-spam de lista</span><span class="sxs-lookup"><span data-stu-id="7cdbe-133">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="7cdbe-134">Phishtank</span><span class="sxs-lookup"><span data-stu-id="7cdbe-134">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="7cdbe-135">PhishTank perguntas Frequentes</span><span class="sxs-lookup"><span data-stu-id="7cdbe-135">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |

> [!NOTE]
> <span data-ttu-id="7cdbe-p107">Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ficar em lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar removem-se usando o [portal de autoatendimento de retirada da lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span><span class="sxs-lookup"><span data-stu-id="7cdbe-p107">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="7cdbe-138">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="7cdbe-138">For more information</span></span>

[<span data-ttu-id="7cdbe-139">Respondendo a uma conta de email comprometido</span><span class="sxs-lookup"><span data-stu-id="7cdbe-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="7cdbe-140">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="7cdbe-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="7cdbe-141">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="7cdbe-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

  

  

