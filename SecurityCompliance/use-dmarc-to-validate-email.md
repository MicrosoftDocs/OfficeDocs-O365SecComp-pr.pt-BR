---
title: Usar DMARC para validar emails no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: TN2DMC
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
description: Saiba como configurar a autenticação baseada em domínio de mensagem, relatórios e conformidade (DMARC) para validar as mensagens enviadas de sua organização do Office 365.
ms.openlocfilehash: 2f8e712028b5b5ee8950b48780083a20c7dce6ab
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750040"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a><span data-ttu-id="969d6-103">Usar DMARC para validar emails no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-103">Use DMARC to validate email in Office 365</span></span>

<span data-ttu-id="969d6-p101">Autenticação de mensagem, relatórios e conformidade ([DMARC](https://dmarc.org)) baseada em domínio funciona com o Framework de política do remetente (SPF) e email de identificado DomainKeys (DKIM) para autenticar remetentes de email e certifique-se de que os sistemas de email de destino deve confiar mensagens enviadas de seu domínio. Implementar DMARC com SPF e DKIM fornece proteção adicional contra email falsificação e phishing. Ajuda DMARC sistemas de recebimento de email determinam o que fazer com que as mensagens enviadas a partir de seu domínio SPF fail ou DKIM verifica.</span><span class="sxs-lookup"><span data-stu-id="969d6-p101">Domain-based Message Authentication, Reporting, and Conformance ([DMARC](https://dmarc.org)) works with Sender Policy Framework (SPF) and DomainKeys Identified Mail (DKIM) to authenticate mail senders and ensure that destination email systems trust messages sent from your domain. Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email. DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span>
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a><span data-ttu-id="969d6-107">Como o SPF e o DMARC trabalham juntos para proteger o email no Office 365?</span><span class="sxs-lookup"><span data-stu-id="969d6-107">How do SPF and DMARC work together to protect email in Office 365?</span></span>
<span data-ttu-id="969d6-108"><a name="SPFandDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-108"></span></span>

 <span data-ttu-id="969d6-p102">Uma mensagem de email pode conter vários endereços originadores ou de remetente. Esses endereços são usados com finalidades diferentes. Por exemplo, considere esses endereços:</span><span class="sxs-lookup"><span data-stu-id="969d6-p102">An email message may contain multiple originator, or sender, addresses. These addresses are used for different purposes. For example, consider these addresses:</span></span> 
  
- <span data-ttu-id="969d6-p103">**"Mail From" endereço**: identifique o remetente e especifica para onde enviar avisos de retorno, se houver problemas com a entrega da mensagem, como os avisos de falha na entrega. Isso é exibida na parte de envelope de uma mensagem de email e não é geralmente exibido pelo seu aplicativo de email. Às vezes, isso é chamado o endereço de 5321.MailFrom ou o endereço do caminho de ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="969d6-p103">**"Mail From" address**: Identifies the sender and specifies where to send return notices if any problems occur with the delivery of the message, such as non-delivery notices. This appears in the envelope portion of an email message and is not usually displayed by your email application. This is sometimes called the 5321.MailFrom address or the reverse-path address.</span></span>
    
- <span data-ttu-id="969d6-p104">**Endereço "De"**: O endereço exibido como o endereço de pelo seu aplicativo de email. Esse endereço identifica o autor do email. Ou seja, a caixa de correio da pessoa ou do sistema responsável pela elaboração a mensagem. Às vezes, isso é chamado de endereço de 5322.From.</span><span class="sxs-lookup"><span data-stu-id="969d6-p104">**"From" address**: The address displayed as the From address by your mail application. This address identifies the author of the email. That is, the mailbox of the person or system responsible for writing the message. This is sometimes called the 5322.From address.</span></span>
    
<span data-ttu-id="969d6-p105">O SPF usa um registro TXT DNS para fornecer uma lista de endereços IP de envio autorizados para um determinado domínio. Normalmente, só são executadas verificações de SPF contra o endereço 5321.MailFrom. Isso significa que o endereço 5322.From não é autenticado ao usar SPF por si só. Isso possibilita que exista um cenário em que um usuário recebe uma mensagem que passa por uma verificação de SPF mas tem um endereço de remetente 5322.From falso. Por exemplo, considere esta transcrição SMTP:</span><span class="sxs-lookup"><span data-stu-id="969d6-p105">SPF uses a DNS TXT record to provide a list of authorized sending IP addresses for a given domain. Normally, SPF checks are only performed against the 5321.MailFrom address. This means that the 5322.From address is not authenticated when you use SPF by itself. This allows for a scenario where a user can receive a message which passes an SPF check but has a spoofed 5322.From sender address. For example, consider this SMTP transcript:</span></span>
  
```
S: Helo woodgrovebank.com
S: Mail from: phish@phishing.contoso.com
S: Rcpt to: astobes@tailspintoys.com
S: data
S: To: "Andrew Stobes" <astobes@tailspintoys.com>
S: From: "Woodgrove Bank Security" <security@woodgrovebank.com>
S: Subject: Woodgrove Bank - Action required
S:
S: Greetings User,
S: 
S: We need to verify your banking details.
S: Please click the following link to verify that we have the right information for your account.
S: 
S: http://short.url/woodgrovebank/updateaccount/12-121.aspx
S:
S: Thank you,
S: Woodgrove Bank
S: .
```

<span data-ttu-id="969d6-124">Nesta transcrição, os endereços de remetente são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="969d6-124">In this transcript, the sender addresses are as follows:</span></span>
  
- <span data-ttu-id="969d6-125">Endereço MailFrom (5321.MailFrom): phish@phishing.contoso.com</span><span class="sxs-lookup"><span data-stu-id="969d6-125">Mail from address (5321.MailFrom): phish@phishing.contoso.com</span></span>
    
- <span data-ttu-id="969d6-126">Endereço De (5322.From): segurança@woodgrovebank.com</span><span class="sxs-lookup"><span data-stu-id="969d6-126">From address (5322.From): security@woodgrovebank.com</span></span>
    
<span data-ttu-id="969d6-p106">Se você configurou o SPF, o servidor de recebimento executa uma verificação do endereço MailFrom phish@phishing.contoso.com. Se a mensagem veio de uma fonte válida para o domínio phishing.contoso.com, ela passa na verificação de SPF. Como o cliente de email exibe apenas o endereço De, o usuário vê que essa mensagem é proveniente de segurança@woodgrovebank.com. Com o SPF sozinho, a validade de woodgrovebank.com nunca foi autenticada.</span><span class="sxs-lookup"><span data-stu-id="969d6-p106">If you configured SPF, then the receiving server performs a check against the Mail from address phish@phishing.contoso.com. If the message came from a valid source for the domain phishing.contoso.com then the SPF check passes. Since the email client only displays the From address, the user sees that this message came from security@woodgrovebank.com. With SPF alone, the validity of woodgrovebank.com was never authenticated.</span></span>
  
<span data-ttu-id="969d6-p107">Quando você usa o DMARC, o servidor de recebimento também executa uma verificação do endereço De. No exemplo acima, se houver um registro TXT do DMARC para woodgrovebank.com, a verificação do endereço De falha.</span><span class="sxs-lookup"><span data-stu-id="969d6-p107">When you use DMARC, the receiving server also performs a check against the From address. In the example above, if there is a DMARC TXT record in place for woodgrovebank.com, then the check against the From address fails.</span></span>
  
## <a name="what-is-a-dmarc-txt-record"></a><span data-ttu-id="969d6-133">O que é um registro TXT do DMARC?</span><span class="sxs-lookup"><span data-stu-id="969d6-133">What is a DMARC TXT record?</span></span>
<span data-ttu-id="969d6-134"><a name="WhatisDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-134"></span></span>

<span data-ttu-id="969d6-p108">Como os registros DNS para SPF, o registro do DMARC é um registro de texto (TXT) de DNS que ajuda a evitar os tipos de falsificação spoofing e phishing. Você publica registros TXT de DMARC no DNS. Os registros TXT de DMARC validam a origem das mensagens de email verificando o endereço IP do remetente em relação ao suposto proprietário do domínio de envio. O registro TXT do DMARC identifica os servidores de email de saída autorizados. Os sistemas de email de destino conseguem, então, verificar se as mensagens têm origem em servidores de email de saída autorizados.</span><span class="sxs-lookup"><span data-stu-id="969d6-p108">Like the DNS records for SPF, the record for DMARC is a DNS text (TXT) record that helps prevent spoofing and phishing. You publish DMARC TXT records in DNS. DMARC TXT records validate the origin of email messages by verifying the IP address of an email's author against the alleged owner of the sending domain. The DMARC TXT record identifies authorized outbound email servers. Destination email systems can then verify that messages they receive originate from authorized outbound email servers.</span></span>
  
<span data-ttu-id="969d6-140">O registro TXT DMARC da Microsoft tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="969d6-140">Microsoft's DMARC TXT record looks something like this:</span></span>
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

<span data-ttu-id="969d6-p109">A Microsoft envia seus relatórios de DMARC à [Agari](https://agari.com), uma terceirizada. A Agari coleta e analisa os relatórios de DMARC.</span><span class="sxs-lookup"><span data-stu-id="969d6-p109">Microsoft sends its DMARC reports to [Agari](https://agari.com), a 3rd party. Agari collects and analyzes DMARC reports.</span></span>
  
## <a name="implement-dmarc-for-inbound-mail"></a><span data-ttu-id="969d6-143">Implementar DMARC para email de entrada</span><span class="sxs-lookup"><span data-stu-id="969d6-143">Implement DMARC for inbound mail</span></span>
<span data-ttu-id="969d6-144"><a name="implementDMARCinbound"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-144"></span></span>

<span data-ttu-id="969d6-p110">Você não precisa fazer nada para configurar o DMARC para mensagens que receber no Office 365. Nós já cuidamos de tudo para você. Se você deseja saber o que acontece com as mensagens que não passam em nossas verificações de DMARC, confira [Como o Office 365 lida com emails de entrada que não passam na verificação do DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span><span class="sxs-lookup"><span data-stu-id="969d6-p110">You don't have to do a thing to set up DMARC for mail that you receive in Office 365. We've taken care of everything for you. If you want to learn what happens to mail that fails to pass our DMARC checks, see [How Office 365 handles inbound email that fails DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span></span>
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a><span data-ttu-id="969d6-148">Implementar DMARC para emails de saída do Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-148">Implement DMARC for outbound mail from Office 365</span></span>
<span data-ttu-id="969d6-149"><a name="implementDMARCoutbound"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-149"></span></span>

<span data-ttu-id="969d6-p111">Se você usa o Office 365, mas não está usando um domínio personalizado, ou seja, você usa o onmicrosoft.com, não é preciso fazer mais nada para configurar ou implementar o DMARC para a sua organização. O SPF já está configurado, e o Office 365 gera automaticamente uma assinatura do DKIM para o seu email de saída. Para saber mais sobre essa assinatura, confira [Comportamento padrão para o DKIM e o Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="969d6-p111">If you use Office 365 but you aren't using a custom domain, that is, you use onmicrosoft.com, you don't need to do anything else to configure or implement DMARC for your organization. SPF is already set up for you and Office 365 automatically generates a DKIM signature for your outgoing mail. For more information about this signature, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
 <span data-ttu-id="969d6-p112">Se tiver um domínio personalizado ou se estiver usando servidores do Exchange no local além do Office 365, você precisará implementar manualmente o DMARC para os seus emails de saída. Para implementar o DMARC no seu domínio personalizado, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="969d6-p112">If you have a custom domain or you are using on-premises Exchange servers in addition to Office 365, you need to manually implement DMARC for your outbound mail. Implementing DMARC for your custom domain includes these steps:</span></span> 
  
- [<span data-ttu-id="969d6-155">Etapa 1: Identificar fontes válidas de email para seu domínio</span><span class="sxs-lookup"><span data-stu-id="969d6-155">Step 1: Identify valid sources of mail for your domain</span></span>](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [<span data-ttu-id="969d6-156">Etapa 2: Definir o SPF para seu domínio no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-156">Step 2: Set up SPF for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [<span data-ttu-id="969d6-157">Etapa 3: Configurar o DKIM para o seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-157">Step 3: Set up DKIM for your custom domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [<span data-ttu-id="969d6-158">Etapa 4: Formar o registro TXT do DMARC para seu domínio no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-158">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a><span data-ttu-id="969d6-159">Etapa 1: Identificar fontes válidas de email para seu domínio</span><span class="sxs-lookup"><span data-stu-id="969d6-159">Step 1: Identify valid sources of mail for your domain</span></span>
<span data-ttu-id="969d6-160"><a name="IdentifyValidSources"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-160"></span></span>

<span data-ttu-id="969d6-p113">Se você já configurou o SPF, já executou esta etapa. Entretanto, para o DMARC, há outras considerações. Ao identificar fontes de email para seu domínio, há duas perguntas que você deve responder:</span><span class="sxs-lookup"><span data-stu-id="969d6-p113">If you have already set up SPF then you have already gone through this exercise. However, for DMARC, there are additional considerations. When identifying sources of mail for your domain there are two questions you need to answer:</span></span>
  
- <span data-ttu-id="969d6-164">Que endereços IP enviam mensagens do meu domínio?</span><span class="sxs-lookup"><span data-stu-id="969d6-164">What IP addresses send messages from my domain?</span></span>
    
- <span data-ttu-id="969d6-165">Para emails enviados de terceiros em meu nome, os domínios de 5321.MailFrom e 5322.From são iguais?</span><span class="sxs-lookup"><span data-stu-id="969d6-165">For mail sent from third parties on my behalf, will the 5321.MailFrom and 5322.From domains match?</span></span>
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a><span data-ttu-id="969d6-166">Etapa 2: Definir o SPF para seu domínio no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-166">Step 2: Set up SPF for your domain in Office 365</span></span>
<span data-ttu-id="969d6-167"><a name="ConfigSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-167"></span></span>

<span data-ttu-id="969d6-168">Agora que você tem uma lista de todos os seus remetentes válidos, pode seguir as etapas para [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="969d6-168">Now that you have a list of all your valid senders you can follow the steps to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>
  
<span data-ttu-id="969d6-169">Por exemplo, supondo que contoso.com envia emails do Exchange Online, um servidor Exchange local cujo endereço IP é 192.168.0.1 e um aplicativo Web cujo endereço IP é 192.168.100.100, o registro TXT do SPF teria a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="969d6-169">For example, assuming contoso.com sends mail from Exchange Online, an on-premises Exchange server whose IP address is 192.168.0.1, and a web application whose IP address is 192.168.100.100, the SPF TXT record would look like this:</span></span>
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

<span data-ttu-id="969d6-170">Como prática recomendada, certifique-se de que seu registro TXT do SPF leva em consideração contas de remetentes terceirizados.</span><span class="sxs-lookup"><span data-stu-id="969d6-170">As a best practice, ensure that your SPF TXT record takes into account third-party senders.</span></span>
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a><span data-ttu-id="969d6-171">Etapa 3: Configurar o DKIM para o seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-171">Step 3: Set up DKIM for your custom domain in Office 365</span></span>
<span data-ttu-id="969d6-172"><a name="ConfigDKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-172"></span></span>

<span data-ttu-id="969d6-p114">Quando já tiver definido o SPF, precisará configurar o DKIM. O DKIM possibilita adicionar uma assinatura digital a mensagens de email no cabeçalho da mensagem. Se você não configurar o DKIM e, ao invés disso, permitir que o Office 365 use as configurações padrão do DKIM para seu domínio, o DMARC poderá falhar. Isso ocorre porque a configuração padrão do DKIM usa seu domínio inicial onmicrosoft.com como o endereço 5322.From, e não o seu domínio personalizado. Isso causa uma incompatibilidade entre os endereços 5321.MailFrom e 5322.From em todos os emails enviados a partir do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="969d6-p114">Once you have set up SPF, you need to set up DKIM. DKIM lets you add a digital signature to email messages in the message header. If you do not set up DKIM and instead allow Office 365 to use the default DKIM configuration for your domain, DMARC may fail. This is because the default DKIM configuration uses your initial onmicrosoft.com domain as the 5322.From address, not your custom domain. This forces a mismatch between the 5321.MailFrom and the 5322.From addresses in all email sent from your domain.</span></span>
  
<span data-ttu-id="969d6-p115">Se você tem remetentes terceirizados que enviam emails em seu nome e o email que eles enviarem tiver endereços 5321.MailFrom e 5322.From incompatíveis, o DMARC falhará para aquele email. Para evitar isto, é preciso configurar especificamente o DKIM para seu domínio com o remetente terceirizado. Isso possibilita que o Office 365 autentique o email do serviço terceirizado. Também permite que outros serviços, como Yahoo, Gmail e Comcast, verifiquem o email enviado a eles pela parte terceirizada, como se o email tivesse sido enviado por você. Isso é benéfico porque permite que seus clientes confiem em seu domínio, independentemente de onde sua caixa de correio está localizada e, ao mesmo tempo, o Office 365 não marca a mensagem como spam devido a spoofing, porque ela passa nas verificações de autenticação para seu domínio.</span><span class="sxs-lookup"><span data-stu-id="969d6-p115">If you have third-party senders that send mail on your behalf and the mail they send has mismatched 5321.MailFrom and 5322.From addresses, DMARC will fail for that email. To avoid this, you need to set up DKIM for your domain specifically with that third-party sender. This allows Office 365 to authenticate email from this 3rd-party service. However, it also allows others, for example, Yahoo, Gmail, and Comcast, to verify email sent to them by the third-party as if it was email sent by you. This is beneficial because it allows your customers to build trust with your domain no matter where their mailbox is located, and at the same time Office 365 won't mark a message as spam due to spoofing because it passes authentication checks for your domain.</span></span>
  
<span data-ttu-id="969d6-183">Para obter instruções sobre como configurar o DKIM para seu domínio, incluindo como configurar o DKIM para remetentes terceirizados para que possam imitar o seu domínio, confira [Usar DKIM para validar emails enviados de seu domínio personalizado no Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="969d6-183">For instructions on setting up DKIM for your domain, including how to set up DKIM for third-party senders so they can spoof your domain, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a><span data-ttu-id="969d6-184">Etapa 4: Formar o registro TXT do DMARC para seu domínio no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-184">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>
<span data-ttu-id="969d6-185"><a name="CreateDMARCRecord"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-185"></span></span>

<span data-ttu-id="969d6-p116">Apesar de haver outras opções de sintaxe que não são mencionadas aqui, essas são as opções mais comumente usadas para o Office 365. Formar o registro TXT do DMARC para seu domínio no formato:</span><span class="sxs-lookup"><span data-stu-id="969d6-p116">Although there are other syntax options that are not mentioned here, these are the most commonly used options for Office 365. Form the DMARC TXT record for your domain in the format:</span></span>
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

<span data-ttu-id="969d6-188">em que:</span><span class="sxs-lookup"><span data-stu-id="969d6-188">where:</span></span>
  
- <span data-ttu-id="969d6-p117">*é o domínio que você queira proteger.* Por padrão, o registro protege o email do domínio e todos os subdomínios. Por exemplo, se você especificar \_dmarc.contoso.com, em seguida, DMARC protege o email do domínio e todos os subdomínios, como housewares.contoso.com ou plumbing.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="969d6-p117">*domain* is the domain you want to protect. By default, the record protects mail from the domain and all subdomains. For example, if you specify \_dmarc.contoso.com, then DMARC protects mail from the domain and all subdomains, such as housewares.contoso.com or plumbing.contoso.com.</span></span> 
    
- <span data-ttu-id="969d6-p118">*TTL* deve sempre ser o equivalente de uma hora. A unidade usada para o TTL, ambos horas (1 hora), minutos (60 minutos) ou segundos (3.600 segundos), irá variar dependendo do registrador para o seu domínio.</span><span class="sxs-lookup"><span data-stu-id="969d6-p118">*TTL* should always be the equivalent of one hour. The unit used for TTL, either hours (1 hour), minutes (60 minutes), or seconds (3600 seconds), will vary depending on the registrar for your domain.</span></span> 
    
- <span data-ttu-id="969d6-194">*pct = 100* indica que esta regra deve ser usada para 100% de email.</span><span class="sxs-lookup"><span data-stu-id="969d6-194">*pct=100* indicates that this rule should be used for 100% of email.</span></span>
    
- <span data-ttu-id="969d6-p119">*diretiva* Especifica qual diretiva você deseja que o servidor de recebimento a seguir se DMARC falhar. Você pode definir a política como nenhum, quarentena, ou rejeitar.</span><span class="sxs-lookup"><span data-stu-id="969d6-p119">*policy* specifies what policy you want the receiving server to follow if DMARC fails. You can set the policy to none, quarantine, or reject.</span></span> 
    
<span data-ttu-id="969d6-197">Para saber mais sobre quais opções usar, familiarize-se com os conceitos em [Práticas recomendadas para implementar o DMARC no Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span><span class="sxs-lookup"><span data-stu-id="969d6-197">For information about which options to use, become familiar with the concepts in [Best practices for implementing DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span></span>
  
<span data-ttu-id="969d6-198">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="969d6-198">Examples:</span></span>
  
- <span data-ttu-id="969d6-199">Política definida como none</span><span class="sxs-lookup"><span data-stu-id="969d6-199">Policy set to none</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- <span data-ttu-id="969d6-200">Política definida como quarantine</span><span class="sxs-lookup"><span data-stu-id="969d6-200">Policy set to quarantine</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- <span data-ttu-id="969d6-201">Política definida como reject</span><span class="sxs-lookup"><span data-stu-id="969d6-201">Policy set to reject</span></span>
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

<span data-ttu-id="969d6-p120">Após formar seu registro, é preciso atualizá-lo com seu registrador de domínio. Para saber mais sobre como adicionar o registro TXT do DMARC em seus registros de DNS para o Office 365, confira [Criar registros DNS para o Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span><span class="sxs-lookup"><span data-stu-id="969d6-p120">Once you have formed your record, you need to update the record at your domain registrar. For instructions on adding the DMARC TXT record to your DNS records for Office 365, see [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a><span data-ttu-id="969d6-204">Práticas recomendadas para implementar o DMARC no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-204">Best practices for implementing DMARC in Office 365</span></span>
<span data-ttu-id="969d6-205"><a name="DMARCbestpractices"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-205"></span></span>

<span data-ttu-id="969d6-p121">Você pode implementar o DMARC gradualmente sem causar impacto no restante de seu fluxo de emails. Crie e execute um plano de implementação que siga estas etapas. Realize cada uma dessas etapas primeiro em um subdomínio, depois em outros subdomínios e, por fim, com o domínio principal de sua organização antes de seguir para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="969d6-p121">You can implement DMARC gradually without impacting the rest of your mail flow. Create and implement a roll out plan that follows these steps. Do each of these steps first with a sub-domain, then other sub-domains, and finally with the top-level domain in your organization before moving on to the next step.</span></span>
  
1. <span data-ttu-id="969d6-209">Monitorar o impacto da implementação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-209">Monitor the impact of implementing DMARC</span></span>
    
    <span data-ttu-id="969d6-p122">Comece com um registro de modo de monitoramento simples para um subdomínio ou domínio que exija que os receptores do DMARC enviem a você estatísticas sobre mensagens que virem usando esse domínio. Um registro de modo de monitoramento é um registro TXT do DMARC que tem a política definida como none (p=none). Muitas empresas publicam um registro TXT do DMARC com p=none porque não têm certeza sobre quantos emails eles podem perder ao publicar uma política de DMARC mais restritiva.</span><span class="sxs-lookup"><span data-stu-id="969d6-p122">Start with a simple monitoring-mode record for a sub-domain or domain that requests that DMARC receivers send you statistics about messages that they see using that domain. A monitoring-mode record is a DMARC TXT record that has its policy set to none (p=none). Many companies publish a DMARC TXT record with p=none because they are unsure about how much email they may lose by publishing a more restrictive DMARC policy.</span></span> 
    
    <span data-ttu-id="969d6-p123">Você pode fazer isso até mesmo antes de ter implementado o SPF ou o DKIM em sua infraestrutura de mensagens. Entretanto, não será possível colocar em quarentena ou rejeitar eficazmente os emails usando o DMARC até que você também implemente o SPF e o DKIM. Conforme você introduz o SPF e o DKIM, os relatórios gerados pelo DMARC fornecem a quantidade e as fontes das mensagens que passam por essas verificações, e as que não passam. É possível ver facilmente quanto de seu tráfego legítimo é ou não abrangido por eles, e solucionar quaisquer problemas. Você também começará a ver quantas mensagens fraudulentas estão sendo enviadas, e de onde.</span><span class="sxs-lookup"><span data-stu-id="969d6-p123">You can do this even before you've implemented SPF or DKIM in your messaging infrastructure. However, you won't be able to effectively quarantine or reject mail by using DMARC until you also implement SPF and DKIM. As you introduce SPF and DKIM, the reports generated through DMARC will provide the numbers and sources of messages that pass these checks, and those that don't. You can easily see how much of your legitimate traffic is or isn't covered by them, and troubleshoot any problems. You'll also begin to see how many fraudulent messages are being sent, and from where.</span></span>
    
2. <span data-ttu-id="969d6-218">Solicitar que sistemas de email externos coloquem em quarentena as mensagens que não passam na verificação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-218">Request that external mail systems quarantine mail that fails DMARC</span></span>
    
    <span data-ttu-id="969d6-p124">Quando você acredita que todo o, ou a maior parte de, seu tráfego legítimo é protegido por SPF e DKIM, e quando compreende o impacto da implementação do DMARC, pode, então, implementar uma política de quarentena. Uma política de quarentena é um registro TXT do DMARC que tem sua política definida como quarantine (p=quarantine). Ao fazer isto, você pede que os receptores do DMARC coloquem as mensagens de seu domínio que falharem na verificação em um local equivalente a uma pasta de spam, ao invés de colocá-las nas caixas de entrada dos clientes.</span><span class="sxs-lookup"><span data-stu-id="969d6-p124">When you believe that all or most of your legitimate traffic is protected by SPF and DKIM, and you understand the impact of implementing DMARC, you can implement a quarantine policy. A quarantine policy is a DMARC TXT record that has its policy set to quarantine (p=quarantine). By doing this, you are asking DMARC receivers to put messages from your domain that fail DMARC into the local equivalent of a spam folder instead of your customers' inboxes.</span></span>
    
3. <span data-ttu-id="969d6-222">Solicitar que sistemas de email externos rejeitem as mensagens que não passam na verificação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-222">Request that external mail systems not accept messages that fail DMARC</span></span>
    
    <span data-ttu-id="969d6-p125">A etapa final é implementar uma política de rejeição. Uma política de rejeição é um registro TXT do DMARC que tem a política definida como reject (p=reject). Ao fazer isto, você pede aos receptores do DMARC que não aceitem as mensagens que falham na verificação.</span><span class="sxs-lookup"><span data-stu-id="969d6-p125">The final step is implementing a reject policy. A reject policy is a DMARC TXT record that has its policy set to reject (p=reject). When you do this, you're asking DMARC receivers not to accept messages that fail the DMARC checks.</span></span> 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a><span data-ttu-id="969d6-226">Como o Office 365 lida com emails de saída que não passam na verificação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-226">How Office 365 handles outbound email that fails DMARC</span></span>
<span data-ttu-id="969d6-227"><a name="outbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-227"></span></span>

<span data-ttu-id="969d6-p126">Se uma mensagem é a saída do Office 365 e falha DMARC e você tiver definido a política como p = quarentena ou p = reject, a mensagem é encaminhada pelo [pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md). Não há nenhuma substituição para emails de saída.</span><span class="sxs-lookup"><span data-stu-id="969d6-p126">If a message is outbound from Office 365 and fails DMARC, and you have set the policy to p=quarantine or p=reject, the message is routed through the [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md). There is no override for outbound email.</span></span>
  
<span data-ttu-id="969d6-p127">Se você publicar uma política de rejeição (p=reject) do DMARC, nenhum outro cliente no Office 365 poderá imitar (spoof) seu domínio, porque as mensagens não conseguirão passar pelas verificações de SPF ou DKIM para seu domínio durante a retransmissão de uma mensagem de saída pelo serviço. No entanto, se você publicar uma política de rejeição do DMARC, mas não tiver todos os seus emails autenticados pelo Office 365, algumas mensagens poderão ser marcadas como spam para emails de entrada (conforme descrito acima), ou poderão ser rejeitadas, caso você não publique o SPF e tente retransmiti-las pelo serviço. Isso acontece, por exemplo, se você esquecer de incluir alguns dos endereços IP para servidores e aplicativos que enviam emails em nome do seu domínio ao formar o registro TXT do DMARC.</span><span class="sxs-lookup"><span data-stu-id="969d6-p127">If you publish a DMARC reject policy (p=reject), no other customer in Office 365 can spoof your domain because messages will not be able to pass SPF or DKIM for your domain when relaying a message outbound through the service. However, if you do publish a DMARC reject policy but don't have all of your email authenticated through Office 365, some of it may be marked as spam for inbound email (as described above), or it will be rejected if you do not publish SPF and try to relay it outbound through the service. This happens, for example, if you forget to include some of the IP addresses for servers and apps that send mail on behalf of your domain when you form your DMARC TXT record.</span></span>
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a><span data-ttu-id="969d6-233">Como o Office 365 lida com emails de entrada que não passam na verificação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-233">How Office 365 handles inbound email that fails DMARC</span></span>
<span data-ttu-id="969d6-234"><a name="inbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-234"></span></span>

<span data-ttu-id="969d6-p128">Se a política do DMARC do servidor de envio for p=reject, o EOP marca a mensagem como spam ao invés de rejeitá-la. Em outras palavras, para emails de entrada, o Office 365 trata p=reject e p=quarantine da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="969d6-p128">If the DMARC policy of the sending server is p=reject, EOP marks the message as spam instead of rejecting it. In other words, for inbound email, Office 365 treats p=reject and p=quarantine the same way.</span></span>
  
<span data-ttu-id="969d6-p129">O Office 365 é configurado assim porque alguns emails legítimos podem falhar na verificação do DMARC. Por exemplo, uma mensagem pode não passar na verificação do DMARC se for enviada a uma lista de endereçamento que retransmite a mensagem a todos os participantes da lista. Se o Office 365 rejeitar essas mensagens, as pessoas podem perder emails legítimos e não têm como recuperá-los. Em vez disso, essas mensagens ainda falharão na verificação do DMARC, mas serão marcadas como spam e não rejeitadas. Se quiserem, os usuários ainda podem receber essas mensagens em suas caixas de entrada fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="969d6-p129">Office 365 is configured like this because some legitimate email may fail DMARC. For example, a message might fail DMARC if it is sent to a mailing list that then relays the message to all list participants. If Office 365 rejected these messages, people could lose legitimate email and have no way to retrieve it. Instead, these messages will still fail DMARC but they will be marked as spam and not rejected. If desired, users can still get these messages in their inbox through these methods:</span></span>
  
- <span data-ttu-id="969d6-242">Os usuários podem adicionar os remetentes seguros individualmente usando seus clientes de email</span><span class="sxs-lookup"><span data-stu-id="969d6-242">Users add safe senders individually by using their email client</span></span>
    
- <span data-ttu-id="969d6-243">Os administradores podem criar uma Regra de Transporte do Exchange (ETR) para todos os usuários que permitem mensagens desses remetentes específicos.</span><span class="sxs-lookup"><span data-stu-id="969d6-243">Administrators create an Exchange transport rule (ETR) for all users that allows messages for those particular senders.</span></span> 
    
## <a name="troubleshooting-your-dmarc-implementation"></a><span data-ttu-id="969d6-244">Solucionar problemas com sua implementação do DMARC</span><span class="sxs-lookup"><span data-stu-id="969d6-244">Troubleshooting your DMARC implementation</span></span>
<span data-ttu-id="969d6-245"><a name="dmarctroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-245"></span></span>

<span data-ttu-id="969d6-246">Se você tiver configurado os registros MX de seu domínio de forma que o EOP não é a primeira entrada, o DMARC não será aplicado ao seu domínio.</span><span class="sxs-lookup"><span data-stu-id="969d6-246">If you have configured your domain's MX records where EOP is not the first entry, DMARC failures will not be enforced for your domain.</span></span> 
  
<span data-ttu-id="969d6-p130">Se você é um cliente do Office 365 e o registro MX primário de seu domínio não aponta para o EOP, você não terá os benefícios do DMARC. Por exemplo, o DMARC não funcionará se você apontar o registro MX para seu servidor de email local e direcionar os emails para o EOP usando um conector. Neste cenário, o domínio receptor é um de seus Domínios Aceitos, mas o EOP não é o MX primário. Por exemplo, suponha que contoso.com aponta seu registro MX para si mesmo e usa o EOP como registro MX secundário. O registro MX de contoso.com tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="969d6-p130">If you're an Office 365 customer, and your domain's primary MX record does not point to EOP, you will not get the benefits of DMARC. For example, DMARC won't work if you point the MX record to your on-premises mail server and then route email to EOP by using a connector. In this scenario, the receiving domain is one of your Accepted-Domains but EOP is not the primary MX. For example, suppose contoso.com points its MX at itself and uses EOP as a secondary MX record, contoso.com's MX record looks like the following:</span></span>
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

<span data-ttu-id="969d6-p131">Maioria, ou todos os email primeiro será roteada para mail.contoso.com desde que é o principal MX, e, em seguida, email é roteado para o EOP. Em alguns casos, você talvez nem mesmo listar EOP como um registro MX em todas as e simplesmente ligar conectores façam o roteamento seu email. EOP não precisa ser a primeira entrada de validação de DMARC a ser feito. Apenas garante a validação, como podemos não terá certeza de que todos os servidores em-local/não-O365 fará DMARC verificações.  DMARC está qualificado para ser imposto para o domínio do cliente (não servidor) quando você configurar o registro TXT DMARC, mas é até o servidor de recebimento realmente fazer a imposição.  Se você configurar o EOP como o servidor de recebimento, EOP faz a imposição de DMARC.</span><span class="sxs-lookup"><span data-stu-id="969d6-p131">All, or most, email will first be routed to mail.contoso.com since it's the primary MX, and then mail will get routed to EOP. In some cases, you might not even list EOP as an MX record at all and simply hook up connectors to route your email. EOP does not have to be the first entry for DMARC validation to be done. It just ensures the validation, as we cannot be certain that all on-premise/non-O365 servers will do DMARC checks.  DMARC is eligible to be enforced for a customer’s domain (not server) when you set up the DMARC TXT record, but it is up to the receiving server to actually do the enforcement.  If you set up EOP as the receiving server, then EOP does the DMARC enforcement.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="969d6-257">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="969d6-257">For more information</span></span>
<span data-ttu-id="969d6-258"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-258"></span></span>

<span data-ttu-id="969d6-p132">Quer mais informações sobre o DMARC? Estes recursos podem ajudar.</span><span class="sxs-lookup"><span data-stu-id="969d6-p132">Want more information about DMARC? These resources can help.</span></span>
  
- <span data-ttu-id="969d6-261">[Cabeçalhos de mensagem antispam](anti-spam-message-headers.md) inclui a sintaxe e os campos de cabeçalho usados pelo Office 365 para verificações de DMARC.</span><span class="sxs-lookup"><span data-stu-id="969d6-261">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DMARC checks.</span></span> 
    
- <span data-ttu-id="969d6-262">Faça a [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) do M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span><span class="sxs-lookup"><span data-stu-id="969d6-262">Take the [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) from M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span></span>
    
- <span data-ttu-id="969d6-263">Use a lista de verificação em [dmarcian](https://space.dmarcian.com/deployment/).</span><span class="sxs-lookup"><span data-stu-id="969d6-263">Use the checklist at [dmarcian](https://space.dmarcian.com/deployment/).</span></span>
    
- <span data-ttu-id="969d6-264">Vá direto à fonte em [DMARC.org](https://dmarc.org).</span><span class="sxs-lookup"><span data-stu-id="969d6-264">Go directly to the source at [DMARC.org](https://dmarc.org).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="969d6-265">See also</span><span class="sxs-lookup"><span data-stu-id="969d6-265">See also</span></span>
<span data-ttu-id="969d6-266"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="969d6-266"></span></span>

[<span data-ttu-id="969d6-267">Como o Office 365 usa o Sender Policy Framework (SPF) para evitar a falsificação</span><span class="sxs-lookup"><span data-stu-id="969d6-267">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[<span data-ttu-id="969d6-268">Configurar o SPF no Office 365 para ajudar a evitar falsificações</span><span class="sxs-lookup"><span data-stu-id="969d6-268">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[<span data-ttu-id="969d6-269">Usar DKIM para validar emails enviados de seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="969d6-269">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md)

