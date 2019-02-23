---
title: Como o Office 365 usa o Sender Policy Framework (SPF) para evitar a falsificação
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/15/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
description: 'Resumo: Este artigo descreve como o Office 365 usa o registro TXT SPF (Sender Policy Framework) no DNS para garantir que os sistemas de email de destino confiem em mensagens enviadas do seu domínio personalizado. Isso se aplica a mensagens de saída enviadas do Office 365. As mensagens enviadas do Office 365 para um destinatário no Office 365 sempre passarão a SPF.'
ms.openlocfilehash: b4898bf8b607e7ad600455c915f99baaab21f6f6
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223560"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a><span data-ttu-id="e2e2c-105">Como o Office 365 usa o Sender Policy Framework (SPF) para evitar a falsificação</span><span class="sxs-lookup"><span data-stu-id="e2e2c-105">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>

 <span data-ttu-id="e2e2c-p102">**Resumo:** Este artigo descreve como o Office 365 usa o registro TXT SPF (Sender Policy Framework) no DNS para garantir que os sistemas de email de destino confiem em mensagens enviadas do seu domínio personalizado. Isso se aplica a mensagens de saída enviadas do Office 365. As mensagens enviadas do Office 365 para um destinatário no Office 365 sempre passarão a SPF.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p102">**Summary:** This article describes how Office 365 uses the Sender Policy Framework (SPF) TXT record in DNS to ensure that destination email systems trust messages sent from your custom domain. This applies to outbound mail sent from Office 365. Messages sent from Office 365 to a recipient within Office 365 will always pass SPF.</span></span> 
  
<span data-ttu-id="e2e2c-p103">Um registro TXT SPF é um registro DNS que ajuda a evitar falsificação e phishing, verificando o nome de domínio do qual as mensagens de email são enviadas. O SPF valida a origem das mensagens de email, verificando o endereço IP do remetente em relação ao suposto proprietário do domínio de envio.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p103">An SPF TXT record is a DNS record that helps prevent spoofing and phishing by verifying the domain name from which email messages are sent. SPF validates the origin of email messages by verifying the IP address of the sender against the alleged owner of the sending domain.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e2e2c-p104">Os tipos de registro SPF tornaram-se obsoletos pela IETF (Internet Engineering Task Force) em 2014. Em vez disso, use os registros TXT no DNS para publicar as informações da sua SPF. O restante deste artigo usa o termo registro TXT SPF para maior clareza.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p104">SPF record types were deprecated by the Internet Engineering Task Force (IETF) in 2014. Instead, ensure that you use TXT records in DNS to publish your SPF information. The rest of this article uses the term SPF TXT record for clarity.</span></span> 
  
<span data-ttu-id="e2e2c-p105">Administradores de domínio publicam informações do SPF em registros TXT no DNS. As informações do SPF identificam servidores de email de saída autorizados. Os sistemas de email de destino verificam se as mensagens têm origem em servidores de email de saída autorizados. Se você está acostumado com o SPF ou tem uma implantação simples e só precisa saber o que incluir no seu registro TXT SPF no DNS para o Office 365, acesse [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). Se você não tem uma implantação totalmente hospedada no Office 365 ou se deseja obter mais informações sobre como o SPF funciona ou como solucionar problemas do SPF para o Office 365, continue lendo este artigo.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p105">Domain administrators publish SPF information in TXT records in DNS. The SPF information identifies authorized outbound email servers. Destination email systems verify that messages originate from authorized outbound email servers. If you are already familiar with SPF, or you have a simple deployment, and just need to know what to include in your SPF TXT record in DNS for Office 365, you can go to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). If you do not have a deployment that is fully-hosted in Office 365, or you want more information about how SPF works or how to troubleshoot SPF for Office 365, keep reading.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e2e2c-p106">Antes, era necessário adicionar um registro TXT SPF diferente para seu domínio personalizado se você também usasse o SharePoint Online. Isso não é mais necessário. Essa alteração deve reduzir o risco de mensagens de notificação do SharePoint Online acabarem na pasta Lixo Eletrônico. Não é necessário fazer nenhuma alteração imediatamente, mas se você receber a mensagem de erro "muitas pesquisas", modifique seu registro TXT SPF conforme descrito em [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p106">Previously, you had to add a different SPF TXT record to your custom domain if you also used SharePoint Online. This is no longer required. This change should reduce the risk of SharePoint Online notification messages ending up in the Junk Email folder. You do not need to make any changes immediately, but if you receive the "too many lookups" error, modify your SPF TXT record as described in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> 
     
## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a><span data-ttu-id="e2e2c-123">Como o SPF funciona para evitar falsificação e phishing no Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-123">How SPF works to prevent spoofing and phishing in Office 365</span></span>
<span data-ttu-id="e2e2c-124"><a name="HowSPFWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-124"></span></span>

<span data-ttu-id="e2e2c-p107">O SPF determina se um remetente tem ou não permissão para enviar em nome de um domínio. Se o remetente não tiver permissão para fazer isso, ou seja, se o email falhar na verificação do SPF no servidor de recebimento, a política de spam configurada nesse servidor determinará o que fazer com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p107">SPF determines whether or not a sender is permitted to send on behalf of a domain. If the sender is not permitted to do so, that is, if the email fails the SPF check on the receiving server, the spam policy configured on that server determines what to do with the message.</span></span>
  
<span data-ttu-id="e2e2c-p108">Cada registro TXT SPF contém três partes: a instrução de que ele é um registro TXT SPF, os endereços IP que estão autorizados a enviar email proveniente do seu domínio e de domínios externos que podem fazer envios em nome do seu domínio e uma regra de aplicação. É preciso todos os três em um registro TXT SPF válido. Este artigo descreve como formular um registro TXT SPF e fornece as práticas recomendadas para trabalhar com os serviços no Office 365. Também são fornecidos links para instruções sobre como trabalhar com o registrador de domínios para publicar seu registro para o DNS.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p108">Each SPF TXT record contains three parts: the declaration that it is an SPF TXT record, the IP addresses that are allowed to send mail from your domain and the external domains that can send on your domain's behalf, and an enforcement rule. You need all three in a valid SPF TXT record. This article describes how you form your SPF TXT record and provides best practices for working with the services in Office 365. Links to instructions on working with your domain registrar to publish your record to DNS are also provided.</span></span>
  
### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a><span data-ttu-id="e2e2c-131">Noções básicas da SPF: endereços IP que podem enviar do seu domínio personalizado</span><span class="sxs-lookup"><span data-stu-id="e2e2c-131">SPF basics: IP addresses allowed to send from your custom domain</span></span>
<span data-ttu-id="e2e2c-132"><a name="SPFBasicsIPaddresses"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-132"></span></span>

<span data-ttu-id="e2e2c-133">Observe a sintaxe básica de uma regra de SPF:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-133">Take a look at the basic syntax for an SPF rule:</span></span>
  
<span data-ttu-id="e2e2c-134">v=spf1 \<IP\> \<regra de aplicação\></span><span class="sxs-lookup"><span data-stu-id="e2e2c-134">v=spf1 \<IP\> \<enforcement rule\></span></span>
  
<span data-ttu-id="e2e2c-135">Por exemplo, digamos que exista a seguinte regra de SPF para contoso.com:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-135">For example, let's say the following SPF rule exists for contoso.com:</span></span>
  
<span data-ttu-id="e2e2c-136">v=spf1 \<endereço IP 1\> \<endereço IP 2\> \<endereço IP 3\> \<regra de aplicação\></span><span class="sxs-lookup"><span data-stu-id="e2e2c-136">v=spf1 \<IP address #1\> \<IP address #2\> \<IP address #3\> \<enforcement rule\></span></span>
  
<span data-ttu-id="e2e2c-137">Neste exemplo, a regra de SPF instrui o servidor de email de recebimento a apenas aceitar emails desses endereços IP para o domínio contoso.com:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-137">In this example, the SPF rule instructs the receiving email server to only accept mail from these IP addresses for the domain contoso.com:</span></span>
  
- <span data-ttu-id="e2e2c-138">Endereço IP 1</span><span class="sxs-lookup"><span data-stu-id="e2e2c-138">IP address #1</span></span>
    
- <span data-ttu-id="e2e2c-139">Endereço IP 2</span><span class="sxs-lookup"><span data-stu-id="e2e2c-139">IP address #2</span></span>
    
- <span data-ttu-id="e2e2c-140">Endereço IP 3</span><span class="sxs-lookup"><span data-stu-id="e2e2c-140">IP address #3</span></span>
    
<span data-ttu-id="e2e2c-p109">Essa regra de SPF informa o servidor de email de recebimento que, se uma mensagem for proveniente de contoso.com, mas não de um desses três endereços IP, o servidor de recebimento deverá fazer valer a regra de aplicação à mensagem. A regra de aplicação é geralmente uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p109">This SPF rule tells the receiving email server that if a message comes from contoso.com, but not from one of these three IP addresses, the receiving server should apply the enforcement rule to the message. The enforcement rule is usually one of these options:</span></span>
  
- <span data-ttu-id="e2e2c-p110">**Falha irrecuperável.** Marca a mensagem com "falha irrecuperável" no envelope de mensagem e segue a política de spam configurada do servidor de recebimento para esse tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p110">**Hard fail.** Mark the message with 'hard fail' in the message envelope and then follow the receiving server's configured spam policy for this type of message.</span></span> 
    
- <span data-ttu-id="e2e2c-p111">**Falha recuperável.** Marca a mensagem com "falha recuperável" no envelope de mensagem. Normalmente, os servidores de email estão configurados para entregar essas mensagens de qualquer maneira. A maioria dos usuários finais não vê essa marca.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p111">**Soft fail.** Mark the message with 'soft fail' in the message envelope. Typically, email servers are configured to deliver these messages anyway. Most end users do not see this mark.</span></span> 
    
- <span data-ttu-id="e2e2c-p112">**Neutro.** Não faz nada, ou seja, não marca o envelope de mensagem. Isso é geralmente reservado para fins de teste e é raramente usado.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p112">**Neutral.** Do nothing, that is, do not mark the message envelope. This is usually reserved for testing purposes and is rarely used.</span></span> 
    
<span data-ttu-id="e2e2c-p113">Os exemplos a seguir mostram como o SPF funciona em diferentes situações. Nestes exemplos, contoso.com é o remetente e woodgrovebank.com é o destinatário.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p113">The following examples show how SPF works in different situations. In these examples, contoso.com is the sender and woodgrovebank.com is the receiver.</span></span>
  
### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a><span data-ttu-id="e2e2c-154">Exemplo 1: Autenticação de email de uma mensagem enviada diretamente do remetente para o destinatário</span><span class="sxs-lookup"><span data-stu-id="e2e2c-154">Example 1: Email authentication of a message sent directly from sender to receiver</span></span>
<span data-ttu-id="e2e2c-155"><a name="spfExample1"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-155"></span></span>

<span data-ttu-id="e2e2c-156">O SPF funciona melhor quando o caminho do remetente para o destinatário é direto, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-156">SPF works best when the path from sender to receiver is direct, for example:</span></span>
  
![Diagrama que mostra como o SPF autentica o email quando ele é enviado diretamente de um servidor para outro.](media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)
  
<span data-ttu-id="e2e2c-158">Quando woodgrovebank.com recebe a mensagem, se o endereço IP 1 está no registro TXT SPF para contoso.com, a mensagem passa na verificação do SPF e é autenticada.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-158">When woodgrovebank.com receives the message, if IP address #1 is in the SPF TXT record for contoso.com, the message passes the SPF check and is authenticated.</span></span>
  
### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a><span data-ttu-id="e2e2c-159">Exemplo 2: Endereço falsificado do remetente falha na verificação do SPF</span><span class="sxs-lookup"><span data-stu-id="e2e2c-159">Example 2: Spoofed sender address fails the SPF check</span></span>
<span data-ttu-id="e2e2c-160"><a name="spfExample2"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-160"></span></span>

<span data-ttu-id="e2e2c-161">Suponha que um agente de phishing encontre uma maneira de falsificar contoso.com:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-161">Suppose a phisher finds a way to spoof contoso.com:</span></span>
  
![Diagrama que mostra como o SPF autentica o email quando ele é enviado de um servidor falso.](media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)
  
<span data-ttu-id="e2e2c-163">Como o endereço IP 12 não está no registro TXT SPF de contoso.com, a mensagem falha na verificação do SPF, e o destinatário pode optar por marcá-la como spam.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-163">Since IP address #12 is not in contoso.com's SPF TXT record, the message fails the SPF check and the receiver may choose to mark it as spam.</span></span>
  
### <a name="example-3-spf-and-forwarded-messages"></a><span data-ttu-id="e2e2c-164">Exemplo 3: SPF e mensagens encaminhadas</span><span class="sxs-lookup"><span data-stu-id="e2e2c-164">Example 3: SPF and forwarded messages</span></span>
<span data-ttu-id="e2e2c-165"><a name="spfExample3"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-165"></span></span>

<span data-ttu-id="e2e2c-p114">Uma desvantagem do SPF é que ele não funciona quando um email é encaminhado. Por exemplo, suponha que o usuário em woodgrovebank.com configurou uma regra de encaminhamento para enviar todos os e-mails para uma conta do outlook.com:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p114">One drawback of SPF is that it doesn't work when an email has been forwarded. For example, suppose the user at woodgrovebank.com has set up a forwarding rule to send all email to an outlook.com account:</span></span>
  
![Diagrama que mostra como o SPF não consegue autenticar o email quando a mensagem é encaminhada.](media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)
  
<span data-ttu-id="e2e2c-p115">A mensagem passa originalmente na verificação do SPF em woodgrovebank.com, mas falha na verificação do SPF em outlook.com, pois o IP 25 não está no registro TXT SPF de contoso.com. O domínio outlook.com pode marcar a mensagem como spam. Para contornar esse problema, use o SPF em conjunto com outros métodos de autenticação de email, como DKIM e DMARC.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p115">The message originally passes the SPF check at woodgrovebank.com but it fails the SPF check at outlook.com because IP #25 is not in contoso.com's SPF TXT record. Outlook.com might then mark the message as spam. To work around this problem, use SPF in conjunction with other email authentication methods such as DKIM and DMARC.</span></span>
  
### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a><span data-ttu-id="e2e2c-172">Noções básicas do SPF: Inclusão de domínios de terceiros que podem enviar emails em nome do seu domínio</span><span class="sxs-lookup"><span data-stu-id="e2e2c-172">SPF basics: Including third-party domains that can send mail on behalf of your domain</span></span>
<span data-ttu-id="e2e2c-173"><a name="SPFBasicsIncludes"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-173"></span></span>

<span data-ttu-id="e2e2c-p116">Além de endereços IP, também é possível configurar seu registro TXT SPF para incluir domínios como remetentes. Eles são adicionados ao registro TXT SPF como instruções "incluir". Por exemplo, contoso.com pode querer incluir todos os endereços IP dos servidores de email de contoso.net e contoso.org que ele também possui. Para fazer isso, contoso.com publica um registro TXT SPF parecido com este:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p116">In addition to IP addresses, you can also configure your SPF TXT record to include domains as senders. These are added to the SPF TXT record as "include" statements. For example, contoso.com might want to include all of the IP addresses of the mail servers from contoso.net and contoso.org which it also owns. To do this, contoso.com publishes an SPF TXT record that looks like this:</span></span>
  
```
IN TXT "v=spf1 include:contoso.net include:contoso.org -all"
```

<span data-ttu-id="e2e2c-p117">Quando o servidor de recebimento visualiza esse registro no DNS, ele também realiza uma pesquisa de DNS no registro TXT SPF em busca de contoso.net e, em seguida, de contoso.org. Se ele encontrar uma instrução de inclusão adicional nos registros para contoso.net ou contoso.org, eles também serão incluídos. Para ajudar a evitar ataques de negação de serviço, o número máximo de pesquisas de DNS para uma única mensagem de email é 10. Cada instrução de inclusão representa uma pesquisa de DNS adicional. Se uma mensagem exceder o limite de 10, ela falhará no SPF. Quando uma mensagem atinge esse limite, dependendo da maneira como o servidor de recebimento está configurado, o remetente pode receber uma mensagem informando que a mensagem gerou "muitas pesquisas" ou que a "contagem máxima de saltos da mensagem foi excedida". Para dicas sobre como evitar isso, confira [Solução de problemas: práticas recomendadas para o SPF no Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p117">When the receiving server sees this record in DNS, it also performs a DNS lookup on the SPF TXT record for contoso.net and then for contoso.org. If it finds an additional include statement within the records for contoso.net or contoso.org, it will follow those too. In order to help prevent denial of service attacks, the maximum number of DNS lookups for a single email message is 10. Each include statement represents an additional DNS lookup. If a message exceeds the 10 limit, the message fails SPF. Once a message reaches this limit, depending on the way the receiving server is configured, the sender may receive a message that states that the message generated "too many lookups" or that the "maximum hop count for the message has been exceeded". For tips on how to avoid this, see [Troubleshooting: Best practices for SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span></span>
  
## <a name="requirements-for-your-spf-txt-record-and-office-365"></a><span data-ttu-id="e2e2c-184">Requisitos para o seu registro TXT SPF e o Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-184">Requirements for your SPF TXT record and Office 365</span></span>
<span data-ttu-id="e2e2c-185"><a name="SPFReqsinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-185"></span></span>

<span data-ttu-id="e2e2c-p118">Se você configurou o email ao configurar o Office 365, já criou um registro TXT SPF que identifica os servidores de mensagens da Microsoft como uma origem legítima de emails para o seu domínio. Esse registro provavelmente tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p118">If you set up mail when you set up Office 365, you already created an SPF TXT record that identifies the Microsoft messaging servers as a legitimate source of mail for your domain. This record probably looks like this:</span></span>
  
```
v=spf1 include:spf.protection.outlook.com -all
```

<span data-ttu-id="e2e2c-188">Se você é um cliente do Office 365 totalmente hospedado, ou seja, não tem servidores de email locais que enviam emails de saída, esse é o único registro TXT SPF que precisa ser publicado para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-188">If you're a fully-hosted Office 365 customer, that is, you have no on-premises mail servers that send outbound mail, this is the only SPF TXT record that you need to publish for Office 365.</span></span>
  
<span data-ttu-id="e2e2c-189">Se você tem uma implantação híbrida (ou seja, algumas caixas de correio locais e outras hospedadas no Office 365) ou se é um cliente independente da EOP (Proteção do Exchange Online), isto é, sua organização usa a EOP para proteger suas caixas de correio locais, adicione o endereço IP de saída para cada um dos seus servidores de email de borda locais ao registro TXT SPF no DNS.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-189">If you have a hybrid deployment (that is, you have some mailboxes on-premises and some hosted in Office 365), or if you're an Exchange Online Protection (EOP) standalone customer (that is, your organization uses EOP to protect your on-premises mailboxes), you should add the outbound IP address for each of your on-premises edge mail servers to the SPF TXT record in DNS.</span></span>
  
## <a name="form-your-spf-txt-record-for-office-365"></a><span data-ttu-id="e2e2c-190">Formular seu registro TXT SPF para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-190">Form your SPF TXT record for Office 365</span></span>
<span data-ttu-id="e2e2c-191"><a name="FormYourSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-191"></span></span>

<span data-ttu-id="e2e2c-p119">Use as informações de sintaxe neste artigo para formular o registro TXT SPF do seu domínio personalizado. Apesar de haver outras opções de sintaxe que não são mencionadas aqui, essas são as opções mais usadas. Após formular seu registro, atualize-o no seu registrador de domínios.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p119">Use the syntax information in this article to form the SPF TXT record for your custom domain. Although there are other syntax options that are not mentioned here, these are the most commonly used options. Once you have formed your record, you need to update the record at your domain registrar.</span></span>
  
<span data-ttu-id="e2e2c-p120">Para informações sobre os domínios que você precisará incluir para o Office 365, confira [Registros DNS externos necessários para o SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US). Use as [instruções passo a passo](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) para atualizar registros TXT SPF para o seu registrador de domínios. Se o seu registrador não estiver listado, entre em contato com ele separadamente para saber como atualizar seu registro.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p120">For information about the domains you will need to include for Office 365, see [External DNS records required for SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US). Use the [step-by-step instructions](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) for updating SPF (TXT) records for your domain registrar. If your registrar is not listed, you will need to contact them separately to learn how to update your record.</span></span> 
  
### <a name="spf-txt-record-syntax-for-office-365"></a><span data-ttu-id="e2e2c-198">Sintaxe do registro TXT SPF para Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-198">SPF TXT record syntax for Office 365</span></span>
<span data-ttu-id="e2e2c-199"><a name="SPFSyntaxO365"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-199"></span></span>

<span data-ttu-id="e2e2c-200">Um registro TXT SPF típico para Office 365 tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-200">A typical SPF TXT record for Office 365 has the following syntax:</span></span>
  
```
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

<span data-ttu-id="e2e2c-201">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-201">For example:</span></span>
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

<span data-ttu-id="e2e2c-202">em que:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-202">where:</span></span>
  
- <span data-ttu-id="e2e2c-p121">**v=spf1** é obrigatório. Isso define o registro TXT como um registro TXT SPF.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p121">**v=spf1** is required. This defines the TXT record as an SPF TXT record.</span></span> 
    
- <span data-ttu-id="e2e2c-p122">**ip4** indica que você está usando endereços IP versão 4. **ip6** indica que você está usando endereços IP versão 6. Se estiver usando endereços IP IPv6, substitua **ip4** por **ip6** nos exemplos deste artigo. Você também pode especificar intervalos de endereços IP usando a notação CIDR, por exemplo, **ip4:192.168.0.1/26**.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p122">**ip4** indicates that you are using IP version 4 addresses. **ip6** indicates that you are using IP version 6 addresses. If you are using IPv6 IP addresses, replace **ip4** with **ip6** in the examples in this article. You can also specify IP address ranges using CIDR notation, for example **ip4:192.168.0.1/26**.</span></span>
    
-  <span data-ttu-id="e2e2c-p123">_IP address_ é o endereço IP que você deseja adicionar ao registro TXT SPF. Geralmente, esse é o endereço IP do servidor de email de saída da sua organização. É possível listar vários servidores de email de saída. Para mais informações, confira [Exemplo: registro TXT SPF para vários servidores de email de saída locais no Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p123">_IP address_ is the IP address that you want to add to the SPF TXT record. Usually, this is the IP address of the outbound mail server for your organization. You can list multiple outbound mail servers. For more information, see [Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).</span></span>
    
-  <span data-ttu-id="e2e2c-p124">_domain name_ é o domínio que você deseja adicionar como remetente legítimo. Para uma lista de nomes de domínio que você deve incluir para o Office 365, confira [Registros DNS externos necessários para o SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p124">_domain name_ is the domain you want to add as a legitimate sender. For a list of domain names you should include for Office 365, see [External DNS records required for SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
    
- <span data-ttu-id="e2e2c-215">A regra de aplicação é geralmente uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-215">Enforcement rule is usually one of the following:</span></span>
    
  - <span data-ttu-id="e2e2c-216">-all</span><span class="sxs-lookup"><span data-stu-id="e2e2c-216">-all</span></span>
    
    <span data-ttu-id="e2e2c-p125">Indica falha irrecuperável. Se você conhece todos os endereços IP autorizados do seu domínio, liste-os no registro TXT SPF e use o qualificador -all (falha irrecuperável). Além disso, se estiver usando apenas o SPF, ou seja, se não estiver usando DMARC ou DKIM, você deverá usar o qualificador -all. Recomendamos que você sempre use esse qualificador.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p125">Indicates hard fail. If you know all of the authorized IP addresses for your domain, list them in the SPF TXT record and use the -all (hard fail) qualifier. Also, if you are only using SPF, that is, you are not using DMARC or DKIM, you should use the -all qualifier. We recommend that you use always this qualifier.</span></span>
    
  - <span data-ttu-id="e2e2c-221">~all</span><span class="sxs-lookup"><span data-stu-id="e2e2c-221">~all</span></span>
    
    <span data-ttu-id="e2e2c-p126">Indica falha recuperável. Se você não sabe se tem a lista completa de endereços IP, convém usar o qualificador ~all (falha recuperável). Além disso, se você estiver usando DMARC com p=quarantine ou p=reject, poderá usar ~all. Caso contrário, use -all.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p126">Indicates soft fail. If you're not sure that you have the complete list of IP addresses, then you should use the ~all (soft fail) qualifier. Also, if you are using DMARC with p=quarantine or p=reject, then you can use ~all. Otherwise, use -all.</span></span>
    
  - <span data-ttu-id="e2e2c-226">?all</span><span class="sxs-lookup"><span data-stu-id="e2e2c-226">?all</span></span>
    
    <span data-ttu-id="e2e2c-p127">Indica neutralidade. Usado ao testar o SPF. Não recomendamos o uso desse qualificador na sua implantação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p127">Indicates neutral. This is used when testing SPF. We do not recommend that you use this qualifier in your live deployment.</span></span>
    
### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a><span data-ttu-id="e2e2c-230">Exemplo: Registro TXT SPF a ser usado quando todos os seus emails são enviados pelo Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-230">Example: SPF TXT record to use when all of your mail is sent by Office 365</span></span>
<span data-ttu-id="e2e2c-231"><a name="ExampleSPFNoSP"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-231"></span></span>

<span data-ttu-id="e2e2c-232">Se todos os seus emails forem enviados pelo Office 365, use isso em seu registro TXT SPF:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-232">If all of your mail is sent by Office 365, use this in your SPF TXT record:</span></span>
  
```
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a><span data-ttu-id="e2e2c-233">Exemplo: Registro TXT SPF para um cenário híbrido com um Exchange Server local e o Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-233">Example: SPF TXT record for a hybrid scenario with one on-premises Exchange Server and Office 365</span></span>
<span data-ttu-id="e2e2c-234"><a name="ExampleSPFHybridOneExchangeServer"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-234"></span></span>

<span data-ttu-id="e2e2c-235">Em um ambiente híbrido, se o endereço IP do seu Exchange Server local for 192.168.0.1, para definir a regra de aplicação da SPF como falha irrecuperável, formule o registro TXT SPF da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-235">In a hybrid environment, if the IP address of your on-premises Exchange Server is 192.168.0.1, in order to set the SPF enforcement rule to hard fail, form the SPF TXT record as follows:</span></span>
  
```
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a><span data-ttu-id="e2e2c-236">Exemplo: registro TXT SPF para vários servidores de email de saída locais no Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-236">Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365</span></span>
<span data-ttu-id="e2e2c-237"><a name="ExampleSPFMultipleMailServerO365"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-237"></span></span>

<span data-ttu-id="e2e2c-p128">Se tiver vários servidores de saída de email, inclua o endereço IP de cada servidor de email no registro TXT SPF e separe cada endereço IP com um espaço seguido de um "ip4".declaração. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p128">If you have multiple outbound mail servers, include the IP address for each mail server in the SPF TXT record and separate each IP address with a space followed by an "ip4:" statement. For example:</span></span>
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a><span data-ttu-id="e2e2c-240">Próximas etapas: configurar o SPF para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-240">Next steps: Set up SPF for Office 365</span></span>
<span data-ttu-id="e2e2c-241"><a name="SPFNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-241"></span></span>

<span data-ttu-id="e2e2c-242">Depois que você tiver formulado seu registro SPF da TXT, siga as etapas em [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) para adicioná-lo ao seu domínio.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-242">Once you have formulated your SPF TXT record, follow the steps in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) to add it to your domain.</span></span> 
  
<span data-ttu-id="e2e2c-p129">Embora o SPF tenha sido projetado para ajudar a evitar falsificação, existem técnicas de falsificação contra as quais o SPF não pode oferecer proteção. Para proteger-se contra elas, depois de ter configurado o SPF, você também deve configurar o DKIM e o DMARC para o Office 365. Para começar, confira [Usar DKIM para validar emails enviados de seu domínio personalizado no Office 365](use-dkim-to-validate-outbound-email.md). Em seguida, confira [Usar DMARC para validar emails no Office 365](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p129">Although SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against. In order to protect against these, once you have set up SPF, you should also configure DKIM and DMARC for Office 365. To get started, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>
  
## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a><span data-ttu-id="e2e2c-247">Solução de problemas: práticas recomendadas para o SPF no Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-247">Troubleshooting: Best practices for SPF in Office 365</span></span>
<span data-ttu-id="e2e2c-248"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-248"></span></span>

<span data-ttu-id="e2e2c-p130">Você só pode criar um registro TXT SPF para o seu domínio personalizado. A criação de vários registros causa uma situação de round robin e a falha do SPF. Para evitar isso, crie registros separados para cada subdomínio. Por exemplo, crie um registro para contoso.com e outro para bulkmail.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p130">You can only create one SPF TXT record for your custom domain. Creating multiple records causes a round robin situation and SPF will fail. To avoid this, you can create separate records for each subdomain. For example, create one record for contoso.com and another record for bulkmail.contoso.com.</span></span>
  
<span data-ttu-id="e2e2c-p131">Se uma mensagem de email causar mais de 10 pesquisas de DNS antes de ser entregue, o servidor de email de recebimento responderá com um erro permanente, também chamado de  _permerror_, e fará com que a mensagem falhe na verificação do SPF. O servidor de recebimento também pode responder com uma NDR (notificação de falha na entrega) que contém um erro semelhante a estes:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p131">If an email message causes more than 10 DNS lookups before it is delivered, the receiving mail server will respond with a permanent error, also called a  _permerror_, and cause the message to fail the SPF check. The receiving server may also respond with a non-delivery report (NDR) that contains an error similar to these:</span></span>
  
- <span data-ttu-id="e2e2c-255">A mensagem excedeu a contagem de saltos.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-255">The message exceeded the hop count.</span></span>
    
- <span data-ttu-id="e2e2c-256">A mensagem exigiu muitas pesquisas.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-256">The message required too many lookups.</span></span>
    
## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a><span data-ttu-id="e2e2c-257">Evitando o erro "muitas pesquisas" quando você usa domínios de terceiros com o Office 365</span><span class="sxs-lookup"><span data-stu-id="e2e2c-257">Avoiding the "too many lookups" error when you use third-party domains with Office 365</span></span>
<span data-ttu-id="e2e2c-258"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-258"></span></span>

<span data-ttu-id="e2e2c-p132">Alguns registros TXT SPF de domínios de terceiros instruem o servidor de recebimento a realizar um grande número de pesquisas de DNS. Por exemplo, na ocasião da elaboração deste artigo, Salesforce.com contém cinco instruções de inclusão em seu registro:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p132">Some SPF TXT records for third-party domains direct the receiving server to perform a large number of DNS lookups. For example, at the time of this writing, Salesforce.com contains 5 include statements in its record:</span></span>
  
```
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

<span data-ttu-id="e2e2c-p133">Para evitar o erro, você pode implementar uma política na qual qualquer pessoa que enviar emails em massa, por exemplo, precisará usar um subdomínio especificamente para essa finalidade. Em seguida, você define um registro TXT SPF diferente para o subdomínio que inclui os emails em massa.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p133">To avoid the error, you can implement a policy where anyone sending bulk email, for example, has to use a subdomain specifically for this purpose. You then define a different SPF TXT record for the subdomain that includes the bulk email.</span></span>
  
 <span data-ttu-id="e2e2c-p134">Em alguns casos, como no exemplo salesforce.com, você precisa usar o domínio no seu registro TXT SPF, mas, em outros casos, terceiros podem já ter criado um subdomínio a ser usado para essa finalidade. Por exemplo, exacttarget.com criou um subdomínio que você precisa usar para o seu registro TXT SPF:</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p134">In some cases, like the salesforce.com example, you have to use the domain in your SPF TXT record, but in other cases, the third-party may have already created a subdomain for you to use for this purpose. For example, exacttarget.com has created a subdomain that you need to use for your SPF TXT record:</span></span> 
  
```
cust-spf.exacttarget.com
```

<span data-ttu-id="e2e2c-265">Quando você inclui domínios de terceiros no seu registro TXT SPF, precisa confirmar com eles qual domínio ou subdomínio deve ser usado para evitar o limite de 10 pesquisas.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-265">When you include third-party domains in your SPF TXT record, you need to confirm with the third-party which domain or subdomain to use in order to avoid running into the 10 lookup limit.</span></span>
  
## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a><span data-ttu-id="e2e2c-266">Como visualizar seu registro TXT SPF atual e determinar o número de pesquisas que ele exige</span><span class="sxs-lookup"><span data-stu-id="e2e2c-266">How to view your current SPF TXT record and determine the number of lookups that it requires</span></span>
<span data-ttu-id="e2e2c-267"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-267"></span></span>

<span data-ttu-id="e2e2c-p135">Você pode usar nslookup para visualizar seus registros DNS, incluindo seu registro TXT SPF. Ou, se preferir, há uma série de ferramentas online gratuitas disponíveis que você pode usar para visualizar o conteúdo do seu registro TXT SPF. Ao examinar seu registro TXT SPF e seguir a cadeia de redirecionamentos e instruções de inclusão, é possível determinar quantas pesquisas de DNS o registro exige. Algumas ferramentas online até mesmo contarão e exibirão essas pesquisas para você. Manter o controle desse número ajudará a evitar que mensagens enviadas da sua organização disparem um erro permanente, chamado de permerror, do servidor de recebimento.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p135">You can use nslookup to view your DNS records, including your SPF TXT record. Or, if you prefer, there are a number of free, online tools available that you can use to view the contents of your SPF TXT record. By looking at your SPF TXT record and following the chain of include statements and redirects, you can determine how many DNS lookups the record requires. Some online tools will even count and display these lookups for you. Keeping track of this number will help prevent messages sent from your organization from triggering a permanent error, called a permerror, from the receiving server.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="e2e2c-273">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="e2e2c-273">For more information</span></span>
<span data-ttu-id="e2e2c-274"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="e2e2c-274"></span></span>

<span data-ttu-id="e2e2c-p136">Precisa de ajuda para adicionar o registro TXT SPF? Estão disponíveis [instruções passo a passo](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) para atualizar registros TXT SPF em uma série de registradores de domínios conhecidos. [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md) inclui os campos de cabeçalho e sintaxe usados pelo Office 365 para verificações do SPF.</span><span class="sxs-lookup"><span data-stu-id="e2e2c-p136">Need help adding the SPF TXT record? [Step-by-step instructions](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) for updating SPF (TXT) records at a variety of popular domain registrars is available. [Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for SPF checks.</span></span> 
  

