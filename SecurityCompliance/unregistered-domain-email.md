---
title: Email de domínio não registrado
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Se você enviar um alto volume de emails de domínio não registrados, correrá o risco de que seu email fique bloqueado. Leia este artigo para saber mais.
ms.openlocfilehash: 21c403c8072902565f63048782b06c531cdbceb0
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670536"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="7d0b9-104">Email de domínio não registrado: o que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="7d0b9-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="7d0b9-105">O Office 365 permite que os locatários transmitam algumas mensagens por meio do Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="7d0b9-105">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP).</span></span> <span data-ttu-id="7d0b9-106">Um exemplo com suporte é quando os usuários têm uma caixa de correio do Office 365 e alguém externo envia esses emails, mas o encaminhamento de emails é configurado para que ele volte para a caixa de correio externa do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-106">One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox.</span></span> <span data-ttu-id="7d0b9-107">Isso é mais comum em ambientes educacionais em que os alunos querem aproveitar sua interface de email pessoal, mas ainda receber emails relacionados à escola.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-107">This is most common in education environments where students want to leverage their personal email interface but still get emails related to school.</span></span> <span data-ttu-id="7d0b9-108">Outro exemplo é quando os clientes estão em um cenário híbrido e têm servidores locais que enviam emails do EOP.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-108">Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="7d0b9-109">Problemas com domínios não registrados</span><span class="sxs-lookup"><span data-stu-id="7d0b9-109">Problems with unregistered domains</span></span>

<span data-ttu-id="7d0b9-110">O problema ocorre quando os servidores locais são comprometidos e acabam retransmitindo um grande volume de spam do EOP.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-110">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP.</span></span> <span data-ttu-id="7d0b9-111">Em quase todos os casos, os conectores corretos são configurados, mas o email é enviado de domínios não registrados, também conhecidos como desprovisionados,.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-111">In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains.</span></span> <span data-ttu-id="7d0b9-112">O Office 365 permite uma quantidade razoável de emails provenientes de domínios não registrados, mas um domínio aceito deve ser configurado no centro de administração para cada domínio em que você pretende enviar.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-112">Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="7d0b9-113">Após o comprometimento, os locatários serão impedidos de enviar emails de saída para domínios não registrados.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-113">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains.</span></span> <span data-ttu-id="7d0b9-114">Os usuários receberão uma NDR (notificação de falha na entrega) que diz:</span><span class="sxs-lookup"><span data-stu-id="7d0b9-114">Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="7d0b9-115">550 o serviço 5.7.750 não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-115">550 5.7.750 Service unavailable.</span></span> <span data-ttu-id="7d0b9-116">Cliente impedido de enviar de domínios não registrados</span><span class="sxs-lookup"><span data-stu-id="7d0b9-116">Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="7d0b9-117">Desbloqueando o locatário para enviar novamente</span><span class="sxs-lookup"><span data-stu-id="7d0b9-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="7d0b9-118">Há várias coisas que você precisa fazer se você estiver bloqueado para envio de domínios não registrados:</span><span class="sxs-lookup"><span data-stu-id="7d0b9-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="7d0b9-119">Certifique-se de registrar todos os seus domínios no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-119">Make sure that you register all of your domains in Microsoft 365 admin center.</span></span> <span data-ttu-id="7d0b9-120">Mais informações podem ser encontradas [aqui](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="7d0b9-120">More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="7d0b9-121">Procure por conectores incomuns.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-121">Look for unusual connectors.</span></span> <span data-ttu-id="7d0b9-122">Os atores mal-intencionados geralmente criarão novos conectores de entrada em seu locatário do Office 365 para enviar spam.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-122">Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam.</span></span> <span data-ttu-id="7d0b9-123">Você pode encontrar mais informações sobre como verificar seus conectores [aqui](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="7d0b9-123">More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="7d0b9-124">Bloqueie seus servidores locais e certifique-se de que eles não estão comprometidos.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="7d0b9-125">Há muitos fatores envolvidos aqui, especialmente se forem servidores de terceiros.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-125">There are many factors involved here, especially if these are third-party servers.</span></span> <span data-ttu-id="7d0b9-126">Independentemente disso, você precisará confirmar que todos os emails que deixam seus servidores são legítimos.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-126">Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="7d0b9-127">Após concluir, você precisará ligar para o suporte da Microsoft e solicitar que o locatário seja desbloqueado para envio de domínios não registrados.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-127">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.</span></span>  <span data-ttu-id="7d0b9-128">Fornecer o código de erro é útil, mas você precisará provar que seu ambiente está protegido e que o spam não será enviado novamente.</span><span class="sxs-lookup"><span data-stu-id="7d0b9-128">Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again.</span></span> <span data-ttu-id="7d0b9-129">É possível encontrar mais informações sobre como abrir um caso de suporte [aqui](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="7d0b9-129">More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="7d0b9-130">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="7d0b9-130">For more information</span></span>

[<span data-ttu-id="7d0b9-131">Office 365 email anti-spam protection</span><span class="sxs-lookup"><span data-stu-id="7d0b9-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="7d0b9-132">Notificações de falha na entrega de email no Office 365</span><span class="sxs-lookup"><span data-stu-id="7d0b9-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="7d0b9-133">Configurar o encaminhamento de email para uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="7d0b9-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="7d0b9-134">Como configurar um dispositivo multifuncional ou aplicativo para enviar email usando o Office 365</span><span class="sxs-lookup"><span data-stu-id="7d0b9-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="7d0b9-135">[Gerenciar domínios aceitos no Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="7d0b9-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
