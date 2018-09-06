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
ms.openlocfilehash: 3f3130bec3cde4cdc1343a0140a9013deacfc519
ms.sourcegitcommit: d85fc77cba3a17d5ddf215e2f506f61b499e0cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839105"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="d152c-103">Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam</span><span class="sxs-lookup"><span data-stu-id="d152c-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="d152c-104">Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.</span><span class="sxs-lookup"><span data-stu-id="d152c-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="d152c-105">Quando um remetente for bloqueado enviem mensagens de emails, eles recebem um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.</span><span class="sxs-lookup"><span data-stu-id="d152c-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="d152c-p101">Não só poderão ser bloqueados usuários individuais aos domínios de serviço, mas a sites específicos, e endereços IP também podem ser bloqueados. Em alguns casos, sites ou domínios podem ser adicionados a uma lista de bloqueios só porque eles aparecem em uma mensagem de spam. Como o administrador do Office 365, você pode tentar obter usuários, sites, domínios e endereços IP removidos das listas de bloqueio de terceiros. Use os links na tabela na parte inferior deste tópico entrar em contato com cada terceiros e siga as instruções. Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ter terminado na lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar remover sozinhos da lista de remetentes bloqueados usando o [portal de autoatendimento de retirada da lista](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d152c-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="d152c-p102">Você pode definir configurações de spam de saída para que você obtenha anotification quando um usuário do Office 365 é impedido de envio de email que é classificada como spam. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.</span><span class="sxs-lookup"><span data-stu-id="d152c-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="d152c-114">Desbloquear uma conta de email do Office 365</span><span class="sxs-lookup"><span data-stu-id="d152c-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="d152c-p103">Conclusão da tarefa no Centro de conformidade (SCC) & segurança do Office 365. [Vá para o Centro de conformidade & segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC.</span><span class="sxs-lookup"><span data-stu-id="d152c-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="d152c-117">Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365, inscreva-se no Centro de conformidade e segurança do Office 365 e na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **restrito Os usuários**.</span><span class="sxs-lookup"><span data-stu-id="d152c-117">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d152c-118">Para ir diretamente para a página **Usuários restritos** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="d152c-118">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="d152c-p104">Esta página conterá a lista de usuários que foram bloqueados de envio de e-mail para fora da sua organização.  Encontre o (s) que você deseja remover restrições e clique em **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="d152c-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user(s) you wish to remove restrictions and then click on **Unblock**.</span></span>

3. <span data-ttu-id="d152c-121">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="d152c-121">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d152c-p105">Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Você precisará contatar o suporte para desbloquear o usuário.</span><span class="sxs-lookup"><span data-stu-id="d152c-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="d152c-124">Listas de bloqueio de terceiros</span><span class="sxs-lookup"><span data-stu-id="d152c-124">Third-party block lists</span></span>

|<span data-ttu-id="d152c-125">**Nome da Lista **</span><span class="sxs-lookup"><span data-stu-id="d152c-125">**List Name**</span></span>|<span data-ttu-id="d152c-126">**Portal para Retirada da Lista**</span><span class="sxs-lookup"><span data-stu-id="d152c-126">**Delisting Portal**</span></span>|<span data-ttu-id="d152c-127">**Para saber mais**</span><span class="sxs-lookup"><span data-stu-id="d152c-127">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d152c-128">URIBL</span><span class="sxs-lookup"><span data-stu-id="d152c-128">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="d152c-129">Site URIBL</span><span class="sxs-lookup"><span data-stu-id="d152c-129">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="d152c-130">SURBL</span><span class="sxs-lookup"><span data-stu-id="d152c-130">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="d152c-131">Apresentando os dados de reputação de URI de SURBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="d152c-131">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="d152c-132">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="d152c-132">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="d152c-133">Entendendo a filtragem DNSBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="d152c-133">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="d152c-134">invaluement</span><span class="sxs-lookup"><span data-stu-id="d152c-134">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="d152c-135">lista de anti-spam de lista</span><span class="sxs-lookup"><span data-stu-id="d152c-135">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="d152c-136">Phishtank</span><span class="sxs-lookup"><span data-stu-id="d152c-136">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="d152c-137">PhishTank perguntas Frequentes</span><span class="sxs-lookup"><span data-stu-id="d152c-137">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="d152c-138">Exchange Online Protection também usa a listas de bloqueio de terceiros para filtragem de spam.</span><span class="sxs-lookup"><span data-stu-id="d152c-138">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="d152c-139">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="d152c-139">For more information</span></span>

[<span data-ttu-id="d152c-140">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="d152c-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="d152c-141">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="d152c-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="d152c-142">Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365</span><span class="sxs-lookup"><span data-stu-id="d152c-142">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

