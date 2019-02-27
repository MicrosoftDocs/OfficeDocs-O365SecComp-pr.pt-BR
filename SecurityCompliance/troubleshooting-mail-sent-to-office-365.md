---
title: Solução de problemas de email enviados para o Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: Este artigo fornece informações de solução de problemas para remetentes que estão enfrentando problemas ao tentar enviar emails para caixas de entrada no Office 365 e práticas recomendadas para envio de email em massa para clientes do Office 365.
ms.openlocfilehash: cfb3901b930b63ef8a33391c673a32a73eaa1b07
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276291"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a><span data-ttu-id="e0d14-103">Solução de problemas de email enviados para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-103">Troubleshooting mail sent to Office 365</span></span>

<span data-ttu-id="e0d14-104">Este artigo fornece informações de solução de problemas para remetentes que estão enfrentando problemas ao tentar enviar emails para caixas de entrada no Office 365 e práticas recomendadas para envio de email em massa para clientes do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e0d14-104">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Office 365 and best practices for bulk mailing to Office 365 customers.</span></span>
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a><span data-ttu-id="e0d14-105">Solucionando problemas comuns com a entrega de emails para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-105">Troubleshooting common problems with mail delivery to Office 365</span></span>

<span data-ttu-id="e0d14-106">Escolha um desses problemas normalmente encontrados.</span><span class="sxs-lookup"><span data-stu-id="e0d14-106">Choose from one of these commonly encountered issues.</span></span>
  
- [<span data-ttu-id="e0d14-107">Você está gerenciando sua reputação de envio de IP e de domínio?</span><span class="sxs-lookup"><span data-stu-id="e0d14-107">Are you managing your IP and domain's sending reputation?</span></span>](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [<span data-ttu-id="e0d14-108">Você está enviando emails de novos endereços IP?</span><span class="sxs-lookup"><span data-stu-id="e0d14-108">Are you sending email from new IP addresses?</span></span>](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [<span data-ttu-id="e0d14-109">Confirmar se o DNS está configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="e0d14-109">Confirm that your DNS is set up correctly</span></span>](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [<span data-ttu-id="e0d14-110">Não se anuncie como um IP não roteável</span><span class="sxs-lookup"><span data-stu-id="e0d14-110">Ensure that you do not advertise yourself as a non-routable IP</span></span>](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [<span data-ttu-id="e0d14-111">Você recebeu uma notificação de falha na entrega (NDR) ao enviar emails para um usuário no Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-111">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [<span data-ttu-id="e0d14-112">Meu email Redirecionado na pasta lixo eletrônico do destinatário no EOP</span><span class="sxs-lookup"><span data-stu-id="e0d14-112">My email landed in the recipient's junk folder in EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [<span data-ttu-id="e0d14-113">O tráfego do meu endereço IP é limitado por EOP</span><span class="sxs-lookup"><span data-stu-id="e0d14-113">Traffic from my IP address is throttled by EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="e0d14-114">Você está gerenciando sua reputação de envio de IP e de domínio?</span><span class="sxs-lookup"><span data-stu-id="e0d14-114">Are you managing your IP and domain's sending reputation?</span></span>
<span data-ttu-id="e0d14-115"><a name="ManageRep"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-115"></span></span>

<span data-ttu-id="e0d14-p101">As tecnologias de filtragem do EOP são projetadas para fornecer proteções antispam para o Microsoft Office 365, bem como outros produtos da Microsoft, como o Exchange Server, o Microsoft Office Outlook e o Windows Live mail. Também aproveitamos o SPF, DKIM e DMARC; tecnologias de autenticação de email que ajudam a resolver o problema de falsificação e phishing, verificando se o domínio que envia o email está autorizado a fazer isso. A filtragem EOP é influenciada por vários fatores relacionados ao IP de envio, domínio, autenticação, precisão da lista, taxas de reclamação, conteúdo e muito mais. Desses, um dos principais fatores para a condução da reputação de um remetente e sua capacidade de entregar emails é a taxa de reclamação de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p101">EOP filtering technologies are designed to provide anti-spam protections for Microsoft Office 365 as well as other Microsoft products like Exchange Server, Microsoft Office Outlook, and Windows Live Mail. We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so. EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more. Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span> 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="e0d14-120">Você está enviando emails de novos endereços IP?</span><span class="sxs-lookup"><span data-stu-id="e0d14-120">Are you sending email from new IP addresses?</span></span>
<span data-ttu-id="e0d14-121"><a name="NewIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-121"></span></span>

<span data-ttu-id="e0d14-p102">Os endereços IP não usados anteriormente para enviar emails normalmente não têm nenhuma reputação criada em nossos sistemas. Como resultado, os emails de novos IPs têm maior probabilidade de sofrer problemas de entrega. Depois que o IP tiver criado uma reputação de não enviar spam, o EOP geralmente permitirá uma melhor experiência de entrega de email.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p102">IP addresses not previously used to send email typically don't have any reputation built up in our systems. As a result, emails from new IPs are more likely to experience delivery issues. Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>
  
<span data-ttu-id="e0d14-p103">Os novos IPs que são adicionados para domínios autenticados em registros SPF existentes normalmente apresentam a vantagem adicional de herdar alguns dos domínios de envio do domínio. Se seu domínio tem uma boa reputação de envio, novos IPs podem ter um tempo de crescimento mais rápido. Um novo IP pode esperar ser totalmente enescalado dentro de algumas semanas ou antes, dependendo do volume, da precisão da lista e das taxas de reclamação de emails de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p103">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation. If your domain has a good sending reputation new IPs may experience a faster ramp up time. A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="e0d14-128">Confirmar se o DNS está configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="e0d14-128">Confirm that your DNS is set up correctly</span></span>
<span data-ttu-id="e0d14-129"><a name="ConfirmDNSsetup"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-129"></span></span>

<span data-ttu-id="e0d14-130">Para obter instruções sobre como criar e manter registros DNS, incluindo o registro MX exigido para roteamento de email, você precisará entrar em contato com o provedor de hospedagem DNS.</span><span class="sxs-lookup"><span data-stu-id="e0d14-130">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="e0d14-131">Não se anuncie como um IP não roteável</span><span class="sxs-lookup"><span data-stu-id="e0d14-131">Ensure that you do not advertise yourself as a non-routable IP</span></span>
<span data-ttu-id="e0d14-132"><a name="NoReverseDNS"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-132"></span></span>

<span data-ttu-id="e0d14-p104">Podemos não aceitar emails de remetentes que falham em uma pesquisa de DNS reverso. Em alguns casos, os remetentes legítimos se anunciam incorretamente como um IP que não é roteável pela Internet ao tentar abrir uma conexão com o EOP. Os endereços IP reservados para redes privadas (não roteáveis) incluem:</span><span class="sxs-lookup"><span data-stu-id="e0d14-p104">We may not accept email from senders who fail a reverse-DNS lookup. In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP. IP addresses that are reserved for private (non-routable) networking include:</span></span>
  
- <span data-ttu-id="e0d14-136">192.168.0.0/16 (ou 192.168.0.0-192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="e0d14-136">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>
    
- <span data-ttu-id="e0d14-137">10.0.0.0/8 (ou 10.0.0.0-10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="e0d14-137">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>
    
- <span data-ttu-id="e0d14-138">172.16.0.0/11 (ou 172.16.0.0-172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="e0d14-138">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="e0d14-139">Você recebeu uma notificação de falha na entrega (NDR) ao enviar emails para um usuário no Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-139">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>
<span data-ttu-id="e0d14-140"><a name="NDRInbound"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-140"></span></span>

<span data-ttu-id="e0d14-p105">Alguns problemas de entrega são o resultado do endereço IP do remetente sendo bloqueado pela Microsoft ou porque a conta do usuário é identificada como remetente proibido devido à atividade de spam anterior. Se você achar que recebeu a notificação por erro, primeiro siga as instruções na mensagem de notificação de falha na entrega para resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p105">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity. If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span> 
  
<span data-ttu-id="e0d14-143">Para obter mais informações sobre o erro recebido, consulte a lista completa de códigos de erro SMTP em [DSNs e NDRs no Exchange 2013 local e no Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0d14-143">For more information about the error you received, see the complete list of SMTP error codes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span></span>
  
 <span data-ttu-id="e0d14-144">Por exemplo, se você receber a seguinte notificação de falha na entrega, ela indicará que o endereço IP de envio foi bloqueado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e0d14-144">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft.</span></span> 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
<span data-ttu-id="e0d14-145">Para solicitar a remoção dessa lista, você pode [usar o portal de deslista para se remover da lista de remetentes bloqueados do Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span><span class="sxs-lookup"><span data-stu-id="e0d14-145">To request removal from this list, you can [Use the delist portal to remove yourself from the Office 365 blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a><span data-ttu-id="e0d14-146">Meu email Redirecionado na pasta lixo eletrônico do destinatário no EOP</span><span class="sxs-lookup"><span data-stu-id="e0d14-146">My email landed in the recipient's junk folder in EOP</span></span>
<span data-ttu-id="e0d14-147"><a name="JunkMailBox"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-147"></span></span>

<span data-ttu-id="e0d14-p106">Se uma mensagem foi identificada incorretamente como spam pelo EOP, você poderá trabalhar com o destinatário para enviar essa mensagem falsa positiva para a equipe de análise de spam da Microsoft, que avaliará e analisará a mensagem. Dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir a mensagem. Você usa email para enviar mensagens para a Microsoft que não devem ser classificadas como spam. Ao fazer isso, certifique-se de usar as etapas do procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p106">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through. You use email to submit messages to Microsoft that should not be classified as spam. When doing so, be sure to use the steps in the following procedure.</span></span>
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a><span data-ttu-id="e0d14-152">Para usar o email para enviar mensagens de falso positivo para a equipe de análise de spam da Microsoft</span><span class="sxs-lookup"><span data-stu-id="e0d14-152">To use email to submit false positive messages to the Microsoft Spam Analysis Team</span></span>

1. <span data-ttu-id="e0d14-153">Salve a mensagem que você deseja enviar como não spam.</span><span class="sxs-lookup"><span data-stu-id="e0d14-153">Save the message you want to submit as non-spam.</span></span>
    
2. <span data-ttu-id="e0d14-154">Crie uma nova mensagem em branco e anexe a ela a mensagem que não é spam.</span><span class="sxs-lookup"><span data-stu-id="e0d14-154">Create a new, blank message and attach the non-spam message to it.</span></span>
    
    <span data-ttu-id="e0d14-155">Você pode anexar várias mensagens que não são spam, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e0d14-155">You can attach multiple non-spam messages if needed.</span></span>
    
3. <span data-ttu-id="e0d14-156">Copie e cole a linha de assunto da mensagem original na linha de assunto da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0d14-156">Copy and paste the original message subject line into the new message subject line.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="e0d14-157">Deixe o corpo da nova mensagem vazio.</span><span class="sxs-lookup"><span data-stu-id="e0d14-157">Leave the body of the new message empty.</span></span> 
  
4. <span data-ttu-id="e0d14-158">Envie a mensagem para [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e0d14-158">Send your new message to [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span></span>
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="e0d14-159">O tráfego do meu endereço IP é limitado por EOP</span><span class="sxs-lookup"><span data-stu-id="e0d14-159">Traffic from my IP address is throttled by EOP</span></span>
<span data-ttu-id="e0d14-160"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-160"></span></span>

<span data-ttu-id="e0d14-161">Se você receber uma notificação de falha na EOP que indica que seu endereço IP está sendo limitado por EOP, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e0d14-161">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
<span data-ttu-id="e0d14-p107">Você recebeu a notificação de falha na entrega porque a atividade suspeita foi detectada no endereço IP e foi temporariamente restringida enquanto está sendo avaliada. Se a suspeita for limpa através da avaliação, essa restrição será levantada em breve.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p107">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated. If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a><span data-ttu-id="e0d14-164">Não consigo receber emails de remetentes no Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-164">I can't receive email from senders in Office 365</span></span>
<span data-ttu-id="e0d14-165"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-165"></span></span>

 <span data-ttu-id="e0d14-p108">Para receber mensagens de nossos usuários, certifique-se de que a sua rede permite conexões dos endereços IP que o EOP usa em nossos data centers. Confira mais informações em [endereços IP do Exchange Online Protection](eop/exchange-online-protection-ip-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="e0d14-p108">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters. For more information, see [Exchange Online Protection IP addresses](eop/exchange-online-protection-ip-addresses.md).</span></span> 
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a><span data-ttu-id="e0d14-168">Práticas recomendadas para envio de email em massa para usuários do Office 365</span><span class="sxs-lookup"><span data-stu-id="e0d14-168">Best practices for bulk emailing to Office 365 users</span></span>
<span data-ttu-id="e0d14-169"><a name="BulkMailer"> </a></span><span class="sxs-lookup"><span data-stu-id="e0d14-169"></span></span>

<span data-ttu-id="e0d14-170">Se você costuma conduzir campanhas de email em massa para os usuários do Office 365 e quiser garantir que seus emails cheguem de forma segura e oportuna, siga as dicas desta seção.</span><span class="sxs-lookup"><span data-stu-id="e0d14-170">If you often conduct bulk email campaigns to Office 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="e0d14-171">Verifique se o nome de: reflete quem está enviando a mensagem</span><span class="sxs-lookup"><span data-stu-id="e0d14-171">Ensure that the From: name reflects who is sending the message</span></span>

<span data-ttu-id="e0d14-p109">O assunto deve ser um breve resumo do que a mensagem está sobre, e o corpo da mensagem deve indicar claramente e sucintamente o que a oferta, serviço ou produto está. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e0d14-p109">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about. For example:</span></span>
  
<span data-ttu-id="e0d14-174">Maneira</span><span class="sxs-lookup"><span data-stu-id="e0d14-174">Correct</span></span>
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
<span data-ttu-id="e0d14-175">Correcta</span><span class="sxs-lookup"><span data-stu-id="e0d14-175">Incorrect</span></span>
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
<span data-ttu-id="e0d14-176">Quanto mais fácil você fizer isso para que as pessoas saibam quem é e o que você está fazendo, menos dificuldade você terá de fornecer pela maioria dos filtros de spam.</span><span class="sxs-lookup"><span data-stu-id="e0d14-176">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="e0d14-177">Sempre incluir uma opção de cancelamento de assinatura em emails de campanha</span><span class="sxs-lookup"><span data-stu-id="e0d14-177">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="e0d14-p110">Os emails de marketing, especialmente boletins informativos, devem sempre incluir uma forma de inscrever-se em emails futuros. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e0d14-p110">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails. For example:</span></span>
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
<span data-ttu-id="e0d14-p111">Alguns remetentes incluem essa opção exigindo que os destinatários enviem um email para um determinado alias com "unsubscribe" no assunto. Isso não é preferível ao exemplo de um clique acima. Se você optar por exigir que os destinatários enviem um email, certifique-se de que ao clicar no link, todos os campos obrigatórios sejam preenchidos previamente.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p111">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject. This is not preferable to the one-click example above. If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="e0d14-183">Use a opção de consentimento duplo para o email de marketing ou o registro de boletim informativo</span><span class="sxs-lookup"><span data-stu-id="e0d14-183">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="e0d14-p112">Essa prática recomendada do setor é recomendada se sua empresa requer ou incentiva os usuários a registrar suas informações de contato para acessar seu produto ou serviço. Algumas empresas fazem dele uma prática inscrever automaticamente seus usuários para emails de marketing ou boletins eletrônicos durante o processo de registro, mas isso é considerado uma prática de marketing questionável no mundo da filtragem de email.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p112">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services. Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>
  
<span data-ttu-id="e0d14-186">Durante o processo de registro, se a caixa de seleção "Sim, envie-me seu boletim informativo" ou "Sim, enviar ofertas especiais" estiver selecionada por padrão, os usuários que não pagarão mais atenção podem inadvertidamente involuntariamente inscrever-se no email de marketing ou boletins informativos de que não deseja receber.</span><span class="sxs-lookup"><span data-stu-id="e0d14-186">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>
  
 <span data-ttu-id="e0d14-p113">Recomendamos a opção de consentimento duplo em vez disso, o que significa que a caixa de seleção para os emails de marketing ou boletins informativos está desmarcada por padrão. Além disso, após o formulário de registro ter sido enviado, um email de verificação é enviado para o usuário com uma URL que permite confirmar sua decisão de receber emails de marketing.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p113">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default. Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span> 
  
 <span data-ttu-id="e0d14-189">Isso ajuda a garantir que apenas os usuários que desejam receber emails de marketing estão inscritos para os emails, subseqüentemente limpando a empresa de envio de qualquer prática de marketing de email questionável.</span><span class="sxs-lookup"><span data-stu-id="e0d14-189">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span> 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="e0d14-190">Garantir que o conteúdo da mensagem de email seja transparente e rastreável</span><span class="sxs-lookup"><span data-stu-id="e0d14-190">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="e0d14-p114">Tão importante quanto a forma como os emails são enviados é o conteúdo que eles contêm. Ao criar conteúdo de email, use as práticas recomendadas a seguir para garantir que seus emails não sejam sinalizados por serviços de filtragem de email:</span><span class="sxs-lookup"><span data-stu-id="e0d14-p114">Just as important as the way the emails are sent is the content they contain. When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>
  
- <span data-ttu-id="e0d14-193">Quando a mensagem de email solicita que os destinatários adicionem o remetente ao catálogo de endereços, deve indicar claramente que essa ação não é uma garantia de entrega.</span><span class="sxs-lookup"><span data-stu-id="e0d14-193">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>
    
- <span data-ttu-id="e0d14-p115">Redirecionamentos incluídos no corpo da mensagem devem ser semelhantes e consistentes, e não múltiplos e variados. Um redirecionamento neste contexto é qualquer coisa que aponte para longe da mensagem, como links e documentos. Se você tiver muitos links de propaganda ou cancelamento de assinatura ou atualizar os links de perfil, todos eles apontarão para o mesmo domínio. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e0d14-p115">Redirects included in the body of the message should be similar and consistent, and not multiple and varied. A redirect in this context is anything that points away from the message, such as links and documents. If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain. For example:</span></span>
    
    <span data-ttu-id="e0d14-198">Maneira</span><span class="sxs-lookup"><span data-stu-id="e0d14-198">Correct</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    <span data-ttu-id="e0d14-199">Correcta</span><span class="sxs-lookup"><span data-stu-id="e0d14-199">Incorrect</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- <span data-ttu-id="e0d14-200">Evite conteúdo com imagens e anexos grandes ou mensagens que são exclusivamente compostas por uma imagem.</span><span class="sxs-lookup"><span data-stu-id="e0d14-200">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>
    
- <span data-ttu-id="e0d14-201">Suas configurações de privacidade pública ou P3P devem indicar claramente a presença de pixels de rastreamento (Web bugs ou beacons).</span><span class="sxs-lookup"><span data-stu-id="e0d14-201">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="e0d14-202">Remover aliases de email incorretos dos bancos de dados</span><span class="sxs-lookup"><span data-stu-id="e0d14-202">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="e0d14-p116">Qualquer alias de email em seu banco de dados que cria um repercussão é desnecessário e coloca seus emails de saída em risco para mais investigações por serviços de filtragem de email. Verifique se o banco de dados de email está atualizado.</span><span class="sxs-lookup"><span data-stu-id="e0d14-p116">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services. Ensure that your email database is up-to-date.</span></span>
  

