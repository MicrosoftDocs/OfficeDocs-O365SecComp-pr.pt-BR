---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026328"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="876d7-103">Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam</span><span class="sxs-lookup"><span data-stu-id="876d7-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="876d7-104">Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.</span><span class="sxs-lookup"><span data-stu-id="876d7-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="876d7-105">Quando um remetente for bloqueado enviem mensagens de emails, eles recebem um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.</span><span class="sxs-lookup"><span data-stu-id="876d7-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="876d7-p101">Não só poderão ser bloqueados usuários individuais aos domínios de serviço, mas a sites específicos, e endereços IP também podem ser bloqueados. Em alguns casos, sites ou domínios podem ser adicionados a uma lista de bloqueios só porque eles aparecem em uma mensagem de spam. Como o administrador do Office 365, você pode tentar obter usuários, sites, domínios e endereços IP removidos das listas de bloqueio de terceiros. Use os links na tabela na parte inferior deste tópico entrar em contato com cada terceiros e siga as instruções. Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ter terminado na lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar remover sozinhos da lista de remetentes bloqueados usando o [portal de autoatendimento de retirada da lista](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="876d7-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="876d7-p102">Você pode definir configurações de spam de saída para que você obtenha anotification quando um usuário do Office 365 é impedido de envio de email que é classificada como spam. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.</span><span class="sxs-lookup"><span data-stu-id="876d7-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="876d7-114">Desbloquear uma conta de email do Office 365</span><span class="sxs-lookup"><span data-stu-id="876d7-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="876d7-p103">Conclusão da tarefa no Centro de administração do Exchange (EAC). Confira [do Exchange admin center no Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) para obter detalhes sobre o EAC.</span><span class="sxs-lookup"><span data-stu-id="876d7-p103">You complete this task in the Exchange admin center (EAC). Check out [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) for details about the EAC.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="876d7-117">Você não verá a Central de ações, a menos que esteja no EAC para Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="876d7-117">You won't see the action center unless you're in the EAC for Exchange Online.</span></span> 
  
1. <span data-ttu-id="876d7-118">No EAC, navegue até **proteção** \> **Central de ações**.</span><span class="sxs-lookup"><span data-stu-id="876d7-118">In the EAC, navigate to **protection** \> **action center**.</span></span>
    
    ![Navegar até a central de ações no Centro de administração do Exchange](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. <span data-ttu-id="876d7-120">Selecione o ícone de **pesquisa** e, em seguida, insira o endereço SMTP do usuário bloqueado.</span><span class="sxs-lookup"><span data-stu-id="876d7-120">Select the **Search** icon, and then enter the SMTP address of the blocked user.</span></span> 
    
    ![Pesquisar um usuário bloqueado na central de ações](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. <span data-ttu-id="876d7-122">Clique em **Desbloquear conta** do painel de descrição.</span><span class="sxs-lookup"><span data-stu-id="876d7-122">Click **Unblock Account** in the description pane.</span></span> 
    
    ![Desbloquear um usuário na central de ações](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. <span data-ttu-id="876d7-124">Clique em **Sim** para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="876d7-124">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="876d7-p104">Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Contate o suporte para desbloquear o usuário.</span><span class="sxs-lookup"><span data-stu-id="876d7-p104">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. Contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="876d7-127">Listas de bloqueio de terceiros</span><span class="sxs-lookup"><span data-stu-id="876d7-127">Third-party block lists</span></span>

|<span data-ttu-id="876d7-128">**Nome da Lista **</span><span class="sxs-lookup"><span data-stu-id="876d7-128">**List Name**</span></span>|<span data-ttu-id="876d7-129">**Portal para Retirada da Lista**</span><span class="sxs-lookup"><span data-stu-id="876d7-129">**Delisting Portal**</span></span>|<span data-ttu-id="876d7-130">**Para saber mais**</span><span class="sxs-lookup"><span data-stu-id="876d7-130">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="876d7-131">URIBL</span><span class="sxs-lookup"><span data-stu-id="876d7-131">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="876d7-132">Site URIBL</span><span class="sxs-lookup"><span data-stu-id="876d7-132"> URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="876d7-133">SURBL</span><span class="sxs-lookup"><span data-stu-id="876d7-133">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="876d7-134">Apresentando os dados de reputação de URI de SURBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="876d7-134">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="876d7-135">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="876d7-135">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="876d7-136">Entendendo a filtragem DNSBLHTTP://</span><span class="sxs-lookup"><span data-stu-id="876d7-136">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="876d7-137">invaluement</span><span class="sxs-lookup"><span data-stu-id="876d7-137">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="876d7-138">lista de anti-spam de lista</span><span class="sxs-lookup"><span data-stu-id="876d7-138">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="876d7-139">Phishtank</span><span class="sxs-lookup"><span data-stu-id="876d7-139">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="876d7-140">PhishTank perguntas Frequentes</span><span class="sxs-lookup"><span data-stu-id="876d7-140">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="876d7-141">Exchange Online Protection também usa a listas de bloqueio de terceiros para filtragem de spam.</span><span class="sxs-lookup"><span data-stu-id="876d7-141">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="876d7-142">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="876d7-142">For more information</span></span>

[<span data-ttu-id="876d7-143">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="876d7-143">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="876d7-144">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="876d7-144">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="876d7-145">Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365</span><span class="sxs-lookup"><span data-stu-id="876d7-145">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

