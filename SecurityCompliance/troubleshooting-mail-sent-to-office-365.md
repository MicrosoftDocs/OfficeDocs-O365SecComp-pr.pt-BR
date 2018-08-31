---
title: Solução de problemas de email enviados para o Office 365
ms.author: krowley
author: kccross
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
description: Este artigo fornece informações de solução de problemas para os remetentes que estão enfrentando problemas ao tentar enviar email para caixas de entrada no Office 365 e práticas recomendadas para mala direta para os clientes do Office 365.
ms.openlocfilehash: 3d8c0a05d096da87b9f686222055d76a6ae96ff2
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003200"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a><span data-ttu-id="633aa-103">Solução de problemas de email enviados para o Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-103">Troubleshooting mail sent to Office 365</span></span>

<span data-ttu-id="633aa-104">Este artigo fornece informações de solução de problemas para os remetentes que estão enfrentando problemas ao tentar enviar email para caixas de entrada no Office 365 e práticas recomendadas para mala direta para os clientes do Office 365.</span><span class="sxs-lookup"><span data-stu-id="633aa-104">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Office 365 and best practices for bulk mailing to Office 365 customers.</span></span>
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a><span data-ttu-id="633aa-105">Solução de problemas comuns com a entrega de email para o Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-105">Troubleshooting common problems with mail delivery to Office 365</span></span>

<span data-ttu-id="633aa-106">Escolha um desses problemas comumente encontrados.</span><span class="sxs-lookup"><span data-stu-id="633aa-106">Choose from one of these commonly encountered issues.</span></span>
  
- [<span data-ttu-id="633aa-107">Você está gerenciando seus IP e do domínio enviando reputação?</span><span class="sxs-lookup"><span data-stu-id="633aa-107">Are you managing your IP and domain's sending reputation?</span></span>](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [<span data-ttu-id="633aa-108">São enviar e-mails de novos endereços IP?</span><span class="sxs-lookup"><span data-stu-id="633aa-108">Are you sending email from new IP addresses?</span></span>](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [<span data-ttu-id="633aa-109">Confirme se o DNS está configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="633aa-109">Confirm that your DNS is set up correctly</span></span>](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [<span data-ttu-id="633aa-110">Certifique-se de que você não anuncie si mesmo como um IP não roteáveis</span><span class="sxs-lookup"><span data-stu-id="633aa-110">Ensure that you do not advertise yourself as a non-routable IP</span></span>](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [<span data-ttu-id="633aa-111">Você recebeu um relatório de falha na entrega (NDR) ao enviar email a um usuário no Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-111">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [<span data-ttu-id="633aa-112">Meu e-mail trouxe na pasta de lixo eletrônico do destinatário no EOP</span><span class="sxs-lookup"><span data-stu-id="633aa-112">My email landed in the recipient's junk folder in EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [<span data-ttu-id="633aa-113">Tráfego do meu endereço IP seja restringido pelo EOP</span><span class="sxs-lookup"><span data-stu-id="633aa-113">Traffic from my IP address is throttled by EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="633aa-114">Você está gerenciando seus IP e do domínio enviando reputação?</span><span class="sxs-lookup"><span data-stu-id="633aa-114">Are you managing your IP and domain's sending reputation?</span></span>
<span data-ttu-id="633aa-115"><a name="ManageRep"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-115"></span></span>

<span data-ttu-id="633aa-p101">Tecnologias de filtragem do EOP são projetadas para fornecer recursos anti-spam proteções para Microsoft Office 365, bem como outros produtos da Microsoft como Windows Live Mail, Microsoft Office Outlook e Exchange Server. Também podemos aproveitar SPF, DKIM e DMARC; email tecnologias de autenticação que ajudam a solucionar o problema de falsificação e phishing, confirmando que o domínio enviando email está autorizado a fazê-lo. Filtragem do EOP é influenciada por um número de fatores relacionados para o IP de envio, domínio, autenticação, precisão de lista, taxas de reclamações, conteúdo e muito mais. Desses, um da entidade de segurança os fatores que baixam reputação do remetente e sua capacidade de oferecer o email é seu taxa de compatível com de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="633aa-p101">EOP filtering technologies are designed to provide anti-spam protections for Microsoft Office 365 as well as other Microsoft products like Exchange Server, Microsoft Office Outlook, and Windows Live Mail. We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so. EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more. Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span> 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="633aa-120">São enviar e-mails de novos endereços IP?</span><span class="sxs-lookup"><span data-stu-id="633aa-120">Are you sending email from new IP addresses?</span></span>
<span data-ttu-id="633aa-121"><a name="NewIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-121"></span></span>

<span data-ttu-id="633aa-p102">Endereços IP não anteriormente usados para enviar email normalmente não têm qualquer reputação criada em nossos sistemas. Como resultado, emails do novo IPs são mais prováveis ter problemas de entrega. Depois que o IP tiver construído uma reputação por não enviem spam, normalmente permitirá EOP para uma melhor experiência de entrega de email.</span><span class="sxs-lookup"><span data-stu-id="633aa-p102">IP addresses not previously used to send email typically don't have any reputation built up in our systems. As a result, emails from new IPs are more likely to experience delivery issues. Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>
  
<span data-ttu-id="633aa-p103">Novo IPs que são adicionadas aos domínios que são autenticados em registros existentes de SPF geralmente experimentar o benefício adicional de herdando algumas das reputação do remetente do domínio. Se o domínio tiver uma boa reputação de envio IPs novo perceba uma tempo mais rápido de participação. Um novo IP pode esperar ser aumentada totalmente em algumas semanas ou mais cedo dependendo de volume, precisão de lista e taxas de reclamações de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="633aa-p103">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation. If your domain has a good sending reputation new IPs may experience a faster ramp up time. A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="633aa-128">Confirme se o DNS está configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="633aa-128">Confirm that your DNS is set up correctly</span></span>
<span data-ttu-id="633aa-129"><a name="ConfirmDNSsetup"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-129"></span></span>

<span data-ttu-id="633aa-130">Para obter instruções sobre como criar e manter registros DNS, incluindo o registro MX necessário para roteamento de email, você precisará entrar em contato com seu provedor de hospedagem de DNS.</span><span class="sxs-lookup"><span data-stu-id="633aa-130">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="633aa-131">Certifique-se de que você não anuncie si mesmo como um IP não roteáveis</span><span class="sxs-lookup"><span data-stu-id="633aa-131">Ensure that you do not advertise yourself as a non-routable IP</span></span>
<span data-ttu-id="633aa-132"><a name="NoReverseDNS"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-132"></span></span>

<span data-ttu-id="633aa-p104">Podemos pode não aceitar emails de remetentes que falham uma pesquisa de DNS reverso. Em alguns casos, remetentes legítimos anunciam-se incorretamente como um IP roteável de não-internet ao tentar abrir uma conexão para o EOP. Endereços IP que são reservados para uma rede privada (não roteáveis) incluem:</span><span class="sxs-lookup"><span data-stu-id="633aa-p104">We may not accept email from senders who fail a reverse-DNS lookup. In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP. IP addresses that are reserved for private (non-routable) networking include:</span></span>
  
- <span data-ttu-id="633aa-136">192.168.0.0/16 (ou 192.168.0.0 - 192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="633aa-136">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>
    
- <span data-ttu-id="633aa-137">10.0.0.0/8 (ou 10.0.0.0 - 10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="633aa-137">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>
    
- <span data-ttu-id="633aa-138">172.16.0.0/11 (ou 172.16.0.0 - 172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="633aa-138">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="633aa-139">Você recebeu um relatório de falha na entrega (NDR) ao enviar email a um usuário no Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-139">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>
<span data-ttu-id="633aa-140"><a name="NDRInbound"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-140"></span></span>

<span data-ttu-id="633aa-p105">Alguns problemas de entrega são o resultado de endereço IP do remetente estão sendo bloqueado pela Microsoft ou porque a conta de usuário é identificada como remetente proibido devido à atividade de spam anterior. Se você acredita que você recebeu o NDR em erro, primeiro siga as instruções na mensagem de notificação de falha para resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="633aa-p105">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity. If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span> 
  
<span data-ttu-id="633aa-143">Para obter mais informações sobre o erro que você recebeu, consulte a lista completa dos códigos de erro do SMTP no [DSNs e NDRs no Exchange 2013 no local e o Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span><span class="sxs-lookup"><span data-stu-id="633aa-143">For more information about the error you received, see the complete list of SMTP error codes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span></span>
  
 <span data-ttu-id="633aa-144">Por exemplo, se você receber os seguintes NDR, indica que o endereço IP de envio foi bloqueado pelo Microsoft.</span><span class="sxs-lookup"><span data-stu-id="633aa-144">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft.</span></span> 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
<span data-ttu-id="633aa-145">Para solicitar a remoção dessa lista, você pode [usar o portal delist para remover seu nome na lista de remetentes bloqueados do Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span><span class="sxs-lookup"><span data-stu-id="633aa-145">To request removal from this list, you can [Use the delist portal to remove yourself from the Office 365 blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a><span data-ttu-id="633aa-146">Meu e-mail trouxe na pasta de lixo eletrônico do destinatário no EOP</span><span class="sxs-lookup"><span data-stu-id="633aa-146">My email landed in the recipient's junk folder in EOP</span></span>
<span data-ttu-id="633aa-147"><a name="JunkMailBox"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-147"></span></span>

<span data-ttu-id="633aa-p106">Se uma mensagem foi incorretamente identificada como spam pelo EOP, você pode trabalhar com o destinatário para enviar essa mensagem de falsa positiva à equipe de análise do Spam da Microsoft, que irá avaliar e analisar a mensagem. Dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir que a mensagem pelo. Você usa o email para enviar mensagens para a Microsoft não devem ser classificadas como spam. Ao fazer isso, certifique-se de usar as etapas no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="633aa-p106">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through. You use email to submit messages to Microsoft that should not be classified as spam. When doing so, be sure to use the steps in the following procedure.</span></span>
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a><span data-ttu-id="633aa-152">Usar o e-mail para enviar mensagens de falso positivo à equipe de análise de Spam da Microsoft</span><span class="sxs-lookup"><span data-stu-id="633aa-152">To use email to submit false positive messages to the Microsoft Spam Analysis Team</span></span>

1. <span data-ttu-id="633aa-153">Salve a mensagem que deseja enviar como não spam.</span><span class="sxs-lookup"><span data-stu-id="633aa-153">Save the message you want to submit as non-spam.</span></span>
    
2. <span data-ttu-id="633aa-154">Crie uma nova mensagem em branco e anexe a ela a mensagem que não é spam.</span><span class="sxs-lookup"><span data-stu-id="633aa-154">Create a new, blank message and attach the non-spam message to it.</span></span>
    
    <span data-ttu-id="633aa-155">Se necessário, você pode anexar várias mensagens não spam.</span><span class="sxs-lookup"><span data-stu-id="633aa-155">You can attach multiple non-spam messages if needed.</span></span>
    
3. <span data-ttu-id="633aa-156">Copie e cole a linha de assunto da mensagem original na linha de assunto da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="633aa-156">Copy and paste the original message subject line into the new message subject line.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="633aa-157">Deixe o corpo da nova mensagem vazio.</span><span class="sxs-lookup"><span data-stu-id="633aa-157">Leave the body of the new message empty.</span></span> 
  
4. <span data-ttu-id="633aa-158">Envie a mensagem para [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="633aa-158">Send your new message to [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span></span>
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="633aa-159">Tráfego do meu endereço IP seja restringido pelo EOP</span><span class="sxs-lookup"><span data-stu-id="633aa-159">Traffic from my IP address is throttled by EOP</span></span>
<span data-ttu-id="633aa-160"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-160"></span></span>

<span data-ttu-id="633aa-161">Se você receber uma notificação de falha do EOP que indica que seu endereço IP está sendo limitado pelo EOP, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="633aa-161">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
<span data-ttu-id="633aa-p107">Você recebeu o NDR porque foi detectada atividade suspeita do endereço IP e se ele tiver sido restringido temporariamente enquanto ele está sendo avaliado ainda mais. Se o desconfiança estiver desmarcada por meio de avaliação, essa restrição será ser elevada em breve.</span><span class="sxs-lookup"><span data-stu-id="633aa-p107">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated. If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a><span data-ttu-id="633aa-164">Não consigo receber email dos remetentes no Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-164">I can't receive email from senders in Office 365</span></span>
<span data-ttu-id="633aa-165"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-165"></span></span>

 <span data-ttu-id="633aa-p108">Para receber mensagens de nossos usuários, certifique-se de que sua rede permite conexões de saída dos endereços IP que EOP usa em nossos centros de dados. Para obter mais informações, consulte [endereços IP do Exchange Online Protection](eop/exchange-online-protection-ip-addresses.md). Para um registro de IP de todos os endereços que foram adicionados, alterados ou preteridos no ano passado, consulte a [notificação de alteração de endereços IP do EOP](eop/change-notification-for-eop-ip-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="633aa-p108">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters. For more information, see [Exchange Online Protection IP addresses](eop/exchange-online-protection-ip-addresses.md). For a record of all IP addresses that have been added, changed, or deprecated in the past year, see [Change notification for EOP IP addresses](eop/change-notification-for-eop-ip-addresses.md).</span></span>
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a><span data-ttu-id="633aa-169">Práticas recomendadas para um email em massa, aos usuários do Office 365</span><span class="sxs-lookup"><span data-stu-id="633aa-169">Best practices for bulk emailing to Office 365 users</span></span>
<span data-ttu-id="633aa-170"><a name="BulkMailer"> </a></span><span class="sxs-lookup"><span data-stu-id="633aa-170"></span></span>

<span data-ttu-id="633aa-171">Se você geralmente conduzir campanhas de email em massa para usuários do Office 365 e para assegurar que seus emails chegarem na maneira segura e em tempo hábil, siga as dicas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="633aa-171">If you often conduct bulk email campaigns to Office 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="633aa-172">Certifique-se de que as From: nome reflete o que está enviando a mensagem</span><span class="sxs-lookup"><span data-stu-id="633aa-172">Ensure that the From: name reflects who is sending the message</span></span>

<span data-ttu-id="633aa-p109">O assunto deve ser um breve resumo dos qual a mensagem é sobre e o corpo da mensagem deve claramente e sucinta indicam o que é a oferta, serviço ou produto sobre. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="633aa-p109">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about. For example:</span></span>
  
<span data-ttu-id="633aa-175">Corrigir</span><span class="sxs-lookup"><span data-stu-id="633aa-175">Correct</span></span>
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
<span data-ttu-id="633aa-176">Incorreto</span><span class="sxs-lookup"><span data-stu-id="633aa-176">Incorrect</span></span>
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
<span data-ttu-id="633aa-177">Mais fácil torná-lo para as pessoas saibam quem você é e o que está fazendo, a menos dificuldade terá como entregar a maioria dos filtros de spam.</span><span class="sxs-lookup"><span data-stu-id="633aa-177">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="633aa-178">Sempre incluir uma opção de cancelamento da assinatura em emails de campanha</span><span class="sxs-lookup"><span data-stu-id="633aa-178">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="633aa-p110">Emails de marketing, especialmente boletins informativos, deve sempre incluir uma maneira de cancelar a assinatura de emails futuros. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="633aa-p110">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails. For example:</span></span>
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
<span data-ttu-id="633aa-p111">Alguns remetentes incluem essa opção, exigindo destinatários enviar um email para um determinado alias com "Cancelar inscrição" no assunto. Isso não é preferível o exemplo de um clique acima. Se você escolher exigir que os destinatários enviar um email, certifique-se de que, quando eles clicarem no link, todos os campos necessários são preenchidos previamente.</span><span class="sxs-lookup"><span data-stu-id="633aa-p111">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject. This is not preferable to the one-click example above. If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="633aa-184">Use a opção double opt-in para registro de email ou o boletim informativo de marketing</span><span class="sxs-lookup"><span data-stu-id="633aa-184">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="633aa-p112">Essa prática recomendada do setor recomenda-se sua empresa requer ou incentiva os usuários para registrar as informações de contato para acessar seus produtos ou serviços. Algumas empresas tornam uma prática Inscreva-se automaticamente se seus usuários para emails de marketing ou f boletins informativos durante o processo de registro, mas isso é considerado uma prática de marketing questionável no mundo da filtragem de email.</span><span class="sxs-lookup"><span data-stu-id="633aa-p112">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services. Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>
  
<span data-ttu-id="633aa-187">Durante o processo de registro, se o de "Sim, Oriente-me o boletim informativo" ou "Sim, Oriente-me ofertas especiais" caixa de seleção é marcada por padrão, os usuários que não preste atenção acidentalmente poderão desconectá para marketing de email ou boletins informativos que não tiverem deseja receber.</span><span class="sxs-lookup"><span data-stu-id="633aa-187">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>
  
 <span data-ttu-id="633aa-p113">É recomendável a opção double opt-in em vez disso, que significa que a caixa de seleção para emails de marketing ou boletins informativos está desmarcada por padrão. Além disso, depois que o formulário de registro tiver sido enviado, um email de verificação é enviado ao usuário com uma URL que permite que eles confirmar sua decisão para receber emails de marketing.</span><span class="sxs-lookup"><span data-stu-id="633aa-p113">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default. Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span> 
  
 <span data-ttu-id="633aa-190">Isso ajuda a garantir que somente os usuários que desejam receber email marketing são inscreveu para emails, subsequentemente desmarcar a empresa de envio de qualquer email questionável práticas de marketing.</span><span class="sxs-lookup"><span data-stu-id="633aa-190">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span> 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="633aa-191">Certifique-se de que o conteúdo da mensagem de email é transparente e rastreável</span><span class="sxs-lookup"><span data-stu-id="633aa-191">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="633aa-p114">Apenas tão importante quanto a maneira como os emails são enviados é o conteúdo que eles contêm. Ao criar o conteúdo de email, use as seguintes práticas recomendadas para garantir que seus emails não serão sinalizadas pelo serviços de filtragem de email:</span><span class="sxs-lookup"><span data-stu-id="633aa-p114">Just as important as the way the emails are sent is the content they contain. When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>
  
- <span data-ttu-id="633aa-194">Quando a mensagem de email solicita que os destinatários adicionem o remetente ao catálogo de endereços, ele deve indicar claramente que tal ação não é uma garantia de entrega.</span><span class="sxs-lookup"><span data-stu-id="633aa-194">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>
    
- <span data-ttu-id="633aa-p115">Redirecionamentos incluídos no corpo da mensagem devem ser semelhante e consistente e não vários e variados. Um redirecionamento nesse contexto é qualquer coisa que aponta para longe da mensagem, links e documentos. Se você tiver muitos anúncios ou links de cancelamento da assinatura ou atualizar os vínculos de perfil, eles devem apontar para o mesmo domínio. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="633aa-p115">Redirects included in the body of the message should be similar and consistent, and not multiple and varied. A redirect in this context is anything that points away from the message, such as links and documents. If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain. For example:</span></span>
    
    <span data-ttu-id="633aa-199">Corrigir</span><span class="sxs-lookup"><span data-stu-id="633aa-199">Correct</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    <span data-ttu-id="633aa-200">Incorreto</span><span class="sxs-lookup"><span data-stu-id="633aa-200">Incorrect</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- <span data-ttu-id="633aa-201">Evite conteúdo com imagens grandes e anexos ou mensagens que são compostas por apenas uma imagem.</span><span class="sxs-lookup"><span data-stu-id="633aa-201">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>
    
- <span data-ttu-id="633aa-202">Sua privacidade pública ou configurações P3P devem indicar claramente a presença de acompanhamento pixels (bugs da web ou avisos).</span><span class="sxs-lookup"><span data-stu-id="633aa-202">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="633aa-203">Remover os aliases de email incorreto de seus bancos de dados</span><span class="sxs-lookup"><span data-stu-id="633aa-203">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="633aa-p116">Qualquer alias de email em seu banco de dados que cria um retorno é desnecessário e coloca os seus emails de saída em risco para maiores investigações pelos serviços de filtragem de email. Certifique-se de que seu banco de dados de email seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="633aa-p116">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services. Ensure that your email database is up-to-date.</span></span>
  

