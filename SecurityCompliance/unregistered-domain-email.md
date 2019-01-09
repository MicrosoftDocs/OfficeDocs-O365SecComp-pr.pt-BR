---
title: Email de domínio não registrados
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Se você enviar um grande volume de email do domínio não registrados, você correrá o risco de seu email obtendo bloqueado. Leia este artigo para saber mais.
ms.openlocfilehash: f632c5f7ab94a200a364828408b13c0026335869
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769775"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="a28df-104">Email de domínio não registrado: O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a28df-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="a28df-p102">O Office 365 permite inquilinos retransmitir algumas mensagens por meio de Exchange Online Protection (EOP). Um exemplo com suporte, isso seria quando os usuários têm uma caixa de correio do Office 365 e alguém externo envia email mas encaminhamento de email está configurado de forma que ele volta check-out para a caixa de correio externa do usuário. Isso é mais comum em ambientes de educação em alunos desejarem aproveitar seu interface email pessoal mas ainda têm emails relacionados à escola. Outro exemplo é quando estiver em um cenário híbrido clientes e servidores locais que enviam emails fora do EOP.</span><span class="sxs-lookup"><span data-stu-id="a28df-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="a28df-109">Problemas com domínios não registrados</span><span class="sxs-lookup"><span data-stu-id="a28df-109">Problems with unregistered domains</span></span>

<span data-ttu-id="a28df-p103">O problema é quando servidores locais estiver comprometidos e acabam retransmissão de um grande volume de spam fora do EOP. Em quase todos os casos, os conectores direita estiver configurados, mas email está sendo enviado do não registrados, também conhecido como desprovisionados, domínios. Office 365 permitem que uma quantidade razoável de emails provenientes de domínios não registrados, mas um domínio aceito deve ser configurado no Centro de administração para cada domínio que você planeja enviar ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="a28df-p103">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="a28df-p104">Depois que comprometida, inquilinos serão impedidos de enviar mensagens de saída para domínios não registrados. Os usuários receberão um não-entrega relatório (NDR) declarando:</span><span class="sxs-lookup"><span data-stu-id="a28df-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="a28df-p105">550 5.7.750 serviço indisponível. Cliente bloqueado para o envio de domínios não registrados</span><span class="sxs-lookup"><span data-stu-id="a28df-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="a28df-117">Desbloqueando locatário para enviar novamente</span><span class="sxs-lookup"><span data-stu-id="a28df-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="a28df-118">Há várias coisas que você precisa fazer se obter bloqueado para o envio de domínios não registrados:</span><span class="sxs-lookup"><span data-stu-id="a28df-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="a28df-p106">Certifique-se de que você registre todos os seus domínios no Centro de administração do Office 365. Mais informações podem ser encontradas [aqui](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="a28df-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="a28df-p107">Procure conectores incomuns. Atores mal-intencionado geralmente irá criar novos conectores de entrada no seu locatário do Office 365 para enviar spam. Para obter mais informações sobre a verificação da suas conectores podem ser encontradas [aqui](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="a28df-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="a28df-124">Bloquear os servidores no local e certifique-se de que eles não estão comprometidos.</span><span class="sxs-lookup"><span data-stu-id="a28df-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="a28df-p108">Há vários fatores envolvidos aqui, especialmente se esses são os servidores de terceiros. Seja como for, você precisará ser capaz de confirmar que todos os emails, deixando os servidores são legítimas.</span><span class="sxs-lookup"><span data-stu-id="a28df-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="a28df-p109">Depois de concluído, você precisará chamar o Microsoft Support e pede para obter seu locatário desbloqueado para enviar de domínios não registrados novamente.  Fornecer o código de erro é útil, mas você precisará provar que seu ambiente esteja protegido e que spam não será enviada novamente. Para obter mais informações sobre como abrir um caso de suporte podem ser encontradas [aqui](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="a28df-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="a28df-130">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="a28df-130">For more information</span></span>

[<span data-ttu-id="a28df-131">Proteção antispam de emails do Office 365</span><span class="sxs-lookup"><span data-stu-id="a28df-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="a28df-132">Notificações de falha na entrega de email no Office 365</span><span class="sxs-lookup"><span data-stu-id="a28df-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="a28df-133">Configurar o encaminhamento de email para uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a28df-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="a28df-134">Como configurar um dispositivo multifuncional ou aplicativo para enviar email usando o Office 365</span><span class="sxs-lookup"><span data-stu-id="a28df-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="a28df-135">[Gerenciar domínios aceitos no Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="a28df-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
