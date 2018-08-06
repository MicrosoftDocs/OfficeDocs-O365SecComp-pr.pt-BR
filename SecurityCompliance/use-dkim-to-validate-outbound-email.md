---
title: Usar DKIM para validar emails enviados de seu domínio personalizado no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/19/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.custom: TN2DMC
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
description: 'Resumo: este artigo descreve como usar o DomainKeys Identified Mail (DKIM) com o Office 365 para garantir que os sistemas de email de destino confiem em mensagens enviadas de seu domínio personalizado.'
ms.openlocfilehash: 0626a2c7bc33df3dc77d3aec8be6dbec5a96472b
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026158"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="85fb6-103">Usar DKIM para validar emails enviados de seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-103">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="85fb6-104">**Resumo:** este artigo descreve como usar o DomainKeys Identified Mail (DKIM) com o Office 365 para garantir que os sistemas de email de destino confiem em mensagens enviadas de seu domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="85fb6-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent from your custom domain.</span></span> 
  
<span data-ttu-id="85fb6-p101">Você deve usar o DKIM, além da SPF e do DMARC, para ajudar a evitar que spoofers enviem mensagens que pareçam que são provenientes de seu domínio. O DKIM possibilita adicionar uma assinatura digital a mensagens de email no cabeçalho da mensagem. Parece complicado, mas não é. Quando você configura o DKIM, autoriza seu domínio a associar, ou assinar, o nome dele a uma mensagem de email usando a autenticação de criptografia. Sistemas de email que recebem emails de seu domínio podem usar essa assinatura digital para ajudar a determinar se os emails recebidos são legítimos.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p101">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain. DKIM lets you add a digital signature to email messages in the message header. Sounds complicated, but it's really not. When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication. Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="85fb6-p102">Basicamente, você usa uma chave privada para criptografar o cabeçalho no email de saída do seu domínio. Publique uma chave pública nos registros DNS do seu domínio que os servidores de recebimento possam então usar para decodificar a assinatura. Eles usam a chave pública para confirmar que as mensagens realmente vêm de você e não de alguém que está falsificando seu domínio.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p102">Basically, you use a private key to encrypt the header in your domain's outgoing email. You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature. They use the public key to verify that the messages are really coming from you and not coming from someone spoofing your domain.</span></span>
  
<span data-ttu-id="85fb6-p103">O Office 365 configura automaticamente o DKIM para domínios iniciais. O domínio inicial é o domínio que o Office 365 criou quando você se inscreveu no serviço, por exemplo, contoso.onmicrosoft.com. Não é preciso fazer nada para configurar o DKIM para o seu domínio inicial. Para saber mais sobre domínios, confira [Perguntas frequentes sobre domínios](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p103">Office 365 automatically sets up DKIM for initial domains. The initial domain is the domain that Office 365 created for you when you signed up with the service, for example, contoso.onmicrosoft.com. You don't need to do anything to set up DKIM for your initial domain. For more information about domains, see [Domains FAQ](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
<span data-ttu-id="85fb6-p104">Você também pode optar por não fazer nada sobre o DKIM em relação ao seu domínio personalizado. Se você não configurar o DKIM para o seu domínio personalizado, o Office 365 criará um par de chaves privada e pública, habilitará a assinatura do DKIM e configurará a política padrão do Office 365 para o seu domínio personalizado. Embora isso seja abrangente o suficiente para a maioria dos clientes do Office 365, você deve configurar manualmente o DKIM para o seu domínio personalizado nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p104">You can choose to do nothing about DKIM for your custom domain too. If you do not set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain. While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="85fb6-120">Você tem mais de um domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-120">You have more than one custom domain in Office 365</span></span>
    
- <span data-ttu-id="85fb6-121">For configurar o DMARC também (recomendado)</span><span class="sxs-lookup"><span data-stu-id="85fb6-121">You're going to set up DMARC too (recommended)</span></span>
    
- <span data-ttu-id="85fb6-122">Quiser ter controle sobre sua chave privada</span><span class="sxs-lookup"><span data-stu-id="85fb6-122">You want control over your private key</span></span>
    
- <span data-ttu-id="85fb6-123">Quiser personalizar seus registros CNAME</span><span class="sxs-lookup"><span data-stu-id="85fb6-123">You want to customize your CNAME records</span></span>
    
- <span data-ttu-id="85fb6-124">Configure as chaves do DKIM para emails provenientes de um domínio de terceiros, por exemplo, se você usar um programa de email em massa terceirizado.</span><span class="sxs-lookup"><span data-stu-id="85fb6-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>
    
<span data-ttu-id="85fb6-125">Neste artigo:</span><span class="sxs-lookup"><span data-stu-id="85fb6-125">In this article:</span></span>
  
- [<span data-ttu-id="85fb6-126">Como o DKIM funciona melhor do que o SPF para evitar a falsificação maliciosa no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [<span data-ttu-id="85fb6-127">O que você precisa fazer para configurar manualmente o DKIM no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-127">What you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [<span data-ttu-id="85fb6-128">Para configurar o DKIM para mais de um domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-128">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [<span data-ttu-id="85fb6-129">Desabilitar a política de assinatura do DKIM para um domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-129">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [<span data-ttu-id="85fb6-130">Comportamento padrão para o DKIM e o Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-130">Default behavior for DKIM and Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [<span data-ttu-id="85fb6-131">Configurar o DKIM de forma que um serviço terceirizado possa enviar, ou fazer spoof de, emails em nome de seu domínio personalizado</span><span class="sxs-lookup"><span data-stu-id="85fb6-131">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [<span data-ttu-id="85fb6-132">Próximas etapas: depois de configurar o DKIM para o Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-132">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="85fb6-133">Como o DKIM funciona melhor do que o SPF para evitar a falsificação maliciosa no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-133">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="85fb6-134"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-134"></span></span>

<span data-ttu-id="85fb6-p105">A SPF adiciona informações a um envelope de mensagem, mas o DKIM realmente criptografa uma assinatura dentro do cabeçalho da mensagem. Ao encaminhar uma mensagem, partes de seu envelope podem ser removidas pelo servidor de encaminhamento. Como a assinatura digital permanece com a mensagem de email porque faz parte do cabeçalho do email, o DKIM funciona mesmo quando uma mensagem é encaminhada conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p105">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header. When you forward a message, portions of that message's envelope can be stripped away by the forwarding server. Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![Diagrama que mostra uma mensagem encaminhada passando pela autenticação DKIM onde a verificação de SPF falha](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="85fb6-p106">Neste exemplo, se você tivesse apenas publicado um registro TXT SPF do seu domínio, o servidor de email do destinatário poderia ter marcado seu email como spam e gerado um resultado positivo falso. A adição do DKIM neste cenário reduz o resultado positivo falso de spam. Como o DKIM depende de criptografia de chave pública para autenticar, e não apenas de endereços IP, é considerado uma forma muito mais forte de autenticação que o SPF. Recomendamos usar o SPF e o DKIM, bem como o DMARC, em sua implantação.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p106">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result. The addition of DKIM in this scenario reduces false positive spam reporting. Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF. We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="85fb6-p107">Detalhes fundamentais: o DKIM usa uma chave privada para inserir uma assinatura criptografada nos cabeçalhos das mensagens. A domínio que assina, ou domínio de saída, é inserido como o valor do campo **d=** no cabeçalho. O domínio que verifica, ou domínio do destinatário, usa esse campo **d=** para procurar a chave pública no DNS e autenticar a mensagem. Se a mensagem for verificada, passa na verificação do DKIM.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p107">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers. The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header. The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message. If the message is verified, the DKIM check passes.</span></span> 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="85fb6-147">O que você precisa fazer para configurar manualmente o DKIM no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-147">What you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="85fb6-148"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-148"></span></span>

<span data-ttu-id="85fb6-149">Para configurar o DKIM, execute estas etapas:</span><span class="sxs-lookup"><span data-stu-id="85fb6-149">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="85fb6-150">Publicar dois registros CNAME para o seu domínio personalizado no DNS</span><span class="sxs-lookup"><span data-stu-id="85fb6-150">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [<span data-ttu-id="85fb6-151">Habilitar a assinatura DKIM para o seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-151">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="85fb6-152">Publicar dois registros CNAME para o seu domínio personalizado no DNS</span><span class="sxs-lookup"><span data-stu-id="85fb6-152">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="85fb6-153"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-153"></span></span>

<span data-ttu-id="85fb6-p108">Para cada domínio para o qual você deseja adicionar uma assinatura de DKIM no DNS, é preciso publicar dois registros CNAME. Um registro CNAME é usado pelo DNS para especificar que o nome canônico de um domínio é um alias para outro nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p108">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records. A CNAME record is used by DNS to specify that the canonical name of a domain is an alias for another domain name.</span></span> 
  
 <span data-ttu-id="85fb6-p109">O Office 365 executa a rotação de chaves automática usando os dois registros estabelecidos. Se você provisionou domínios personalizados em adição ao domínio inicial no Office 365, deve publicar dois registros CNAME para cada domínio adicional. Portanto, se você tem dois domínios, deve publicar dois registros CNAME adicionais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p109">Office 365 performs automatic key rotation using the two records that you establish. If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain. So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span> 
  
<span data-ttu-id="85fb6-159">Use o seguinte formato para os registros CNAME:</span><span class="sxs-lookup"><span data-stu-id="85fb6-159">Use the following format for the CNAME records:</span></span>
  
```
Host name:          selector1._domainkey.<domain>
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
Host name:          selector2._domainkey.<domain>
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

```

<span data-ttu-id="85fb6-160">Em que:</span><span class="sxs-lookup"><span data-stu-id="85fb6-160">Where:</span></span>
  
-  <span data-ttu-id="85fb6-161">Para o Office 365, os seletores sempre serão "seletor1" ou "seletor2".</span><span class="sxs-lookup"><span data-stu-id="85fb6-161">For Office 365, the selectors will always be "selector1" or "selector2".</span></span> 
    
-  <span data-ttu-id="85fb6-p110">O  _domainGUID_ é igual ao  _domainGUID_ no registro MX personalizado para o seu domínio personalizado, que aparece antes de mail.protection.outlook.com. Por exemplo, no seguinte registro MX para o domínio contoso.com, o  _domainGUID_ é contoso-com:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p110">_domainGUID_ is the same as the  _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com. For example, in the following MX record for the domain contoso.com, the  _domainGUID_ is contoso-com:</span></span> 
    
  ```
  contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
  ```

-  <span data-ttu-id="85fb6-p111">_initialDomain_ é o domínio que você usou quando se inscreveu no Office 365. Para saber mais sobre como determinar seu domínio inicial, confira [Perguntas frequentes sobre domínios](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p111">_initialDomain_ is the domain that you used when you signed up for Office 365. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
    
<span data-ttu-id="85fb6-166">Por exemplo, se você tiver o domínio inicial cohovineyardandwinery.onmicrosoft.com e dois domínios personalizados, cohovineyard.com e cohowinery.com, precisará configurar dois registros CNAME para cada domínio adicional, totalizando quatro registros CNAME.</span><span class="sxs-lookup"><span data-stu-id="85fb6-166">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
```
Host name:          selector1._domainkey.cohovineyard.com  
Points to address or value: selector1-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600
Host name:          selector2._domainkey.cohovineyard.com  
Points to address or value: selector2-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600
Host name:          selector1._domainkey.cohowinery.com
Points to address or value: selector1-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey.cohowinery.com
Points to address or value: selector2-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="85fb6-167">Habilitar a assinatura DKIM para o seu domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-167">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="85fb6-168"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-168"></span></span>

<span data-ttu-id="85fb6-p112">Depois de publicar os registros CNAME no DNS, você estará pronto para habilitar a assinatura DKIM pelo Office 365. Para tanto, use o Centro de administração do Office 365 ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p112">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365. You can do this either through the Office 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-office-365-admin-center"></a><span data-ttu-id="85fb6-171">Para habilitar a assinatura DKIM para o seu domínio personalizado por meio do Centro de administração do Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-171">To enable DKIM signing for your custom domain through the Office 365 admin center</span></span>

1. <span data-ttu-id="85fb6-172">[Entre no Office 365](https://support.office.microsoft.com/article/Sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4) com sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="85fb6-172">[Sign in to Office 365](https://support.office.microsoft.com/article/Sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 
    
2. <span data-ttu-id="85fb6-173">Selecione o ícone do inicializador de aplicativos no canto superior esquerdo e escolha **Administrador**.</span><span class="sxs-lookup"><span data-stu-id="85fb6-173">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>
    
3. <span data-ttu-id="85fb6-174">No painel de navegação inferior à esquerda, expanda **Administrador** e escolha **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="85fb6-174">In the lower-left navigation, expand **Admin** and choose **Exchange**.</span></span>
    
4. <span data-ttu-id="85fb6-175">Vá para **Proteção** \> **DKIM**.</span><span class="sxs-lookup"><span data-stu-id="85fb6-175">Go to **Protection** \> **dkim**.</span></span>
    
5. <span data-ttu-id="85fb6-p113">Selecione o domínio para o qual você deseja habilitar o DKIM e, para **Assinar mensagens deste domínio com assinaturas DKIM**, escolha **Habilitar**. Repita essa etapa para cada domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p113">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**. Repeat this step for each custom domain.</span></span>
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="85fb6-178">Para habilitar a assinatura DKIM para o seu domínio personalizado usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="85fb6-178">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="85fb6-179">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85fb6-179">[Connect to Exchange Online using remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="85fb6-180">Execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="85fb6-180">Run the following cmdlet:</span></span>
    
  ```
  New-DkimSigningConfig -DomainName <domain> -Enabled $true
  ```

    <span data-ttu-id="85fb6-181">Em que  _domain_ é o nome do domínio personalizado para o qual você deseja habilitar a assinatura DKIM.</span><span class="sxs-lookup"><span data-stu-id="85fb6-181">Where  _domain_ is the name of the custom domain for which you want to enable DKIM signing.</span></span> 
    
    <span data-ttu-id="85fb6-182">Por exemplo, para o domínio contoso.com:</span><span class="sxs-lookup"><span data-stu-id="85fb6-182">For example, for the domain contoso.com:</span></span>
    
  ```
  New-DkimSigningConfig -DomainName contoso.com -Enabled $true
  ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="85fb6-183">Para confirmar que a assinatura de DKIM está configurada adequadamente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-183">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="85fb6-p114">Aguarde alguns minutos antes de prosseguir com essas etapas para confirmar que você configurou o DKIM corretamente. Isso permite que as informações do DKIM sobre o domínio sejam distribuídas por toda a rede.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p114">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM. This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="85fb6-186">Envie uma mensagem de uma conta do seu domínio do Office 365 habilitado com DKIM para outra conta de email, como outlook.com ou Hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="85fb6-186">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>
    
- <span data-ttu-id="85fb6-p115">Não use uma conta aol.com para fins de teste. A AOL pode ignorar a verificação de DKIM se a verificação de SPF passar. Isso anula o teste.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p115">Do not use an aol.com account for testing purposes. AOL may skip the DKIM check if the SPF check passes. This will nullify your test.</span></span>
    
- <span data-ttu-id="85fb6-p116">Abra a mensagem e examine o cabeçalho. Instruções para exibir o cabeçalho da mensagem variam dependendo do seu cliente de mensagens. Para instruções sobre como visualizar cabeçalhos de mensagens no Outlook, confira [Visualizar cabeçalhos de mensagens de email](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p116">Open the message and look at the header. Instructions for viewing the header for the message will vary depending on your messaging client. For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>
    
     <span data-ttu-id="85fb6-p117">A mensagem assinada com DKIM conterá o nome do host e o domínio definidos quando você publicou as entradas CNAME. A mensagem terá uma aparência similar à do exemplo:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p117">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries. The message will look something like this example:</span></span> 
    
  ```
  From: Example User <example@contoso.com> 
  DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
      s=selector1; d=contoso.com; t=1429912795; 
      h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
      bh=<body hash>; 
      b=<signed field>;
  
  ```

- <span data-ttu-id="85fb6-p118">Procure pelo cabeçalho Authentication-Results. Embora cada serviço receptor use um formato ligeiramente diferente para carimbar as mensagens recebidas, o resultado deve incluir algo parecido com **DKIM=pass** ou **DKIM=OK**.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p118">Look for the Authentication-Results header. While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span> 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="85fb6-197">Para configurar o DKIM para mais de um domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-197">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="85fb6-198"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-198"></span></span>

<span data-ttu-id="85fb6-p119">Se em algum momento no futuro você decidir adicionar outro domínio personalizado e quiser habilitar o DKIM para o novo domínio, deve executar as etapas deste artigo para cada domínio. Especificamente, execute todas as etapas em [O que você precisa fazer para configurar manualmente o DKIM no Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p119">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain. Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="85fb6-201">Desabilitar a política de assinatura do DKIM para um domínio personalizado no Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-201">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="85fb6-202"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-202"></span></span>

<span data-ttu-id="85fb6-p120">Desabilitar a política de assinatura não desabilita completamente o DKIM. Após um período de tempo, o Office 365 aplicará automaticamente a política padrão do Office 365 ao seu domínio. Para saber mais, confira [Comportamento padrão para o DKIM e o Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p120">Disabling the signing policy does not completely disable DKIM. After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain. For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="85fb6-206">Para desabilitar a política de assinatura do DKIM usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="85fb6-206">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="85fb6-207">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85fb6-207">[Connect to Exchange Online using remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="85fb6-208">Execute um dos seguintes comandos para cada domínio para o qual você deseja desabilitar a assinatura de DKIM.</span><span class="sxs-lookup"><span data-stu-id="85fb6-208">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
  ```
  $p=Get-DkimSigningConfig -identity <domain>
  $p[0] | set-DkimSigningConfig -enabled $false
  
  ```

    <span data-ttu-id="85fb6-209">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="85fb6-209">For example:</span></span>
    
  ```
  $p=Get-DkimSigningConfig -identity contoso.com
  $p[0] | set-DkimSigningConfig -enabled $false
  ```

    <span data-ttu-id="85fb6-210">Ou</span><span class="sxs-lookup"><span data-stu-id="85fb6-210">Or</span></span>
    
  ```
  Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
  
  ```

    <span data-ttu-id="85fb6-p121">Em que  _number_ é o índice da política. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p121">Where  _number_ is the index of the policy. For example:</span></span> 
    
  ```
  Set-DkimSigningConfig -identity $p[0].identity -enabled $false
  ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="85fb6-213">Comportamento padrão para o DKIM e o Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-213">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="85fb6-214"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-214"></span></span>

<span data-ttu-id="85fb6-p122">Se você não habilitar o DKIM, o Office 365 criará automaticamente uma chave pública DKIM de 1.024 bits para seu domínio personalizado e a chave privada associada que é armazenada internamente em nosso data center. Por padrão, o Office 365 usa uma configuração de assinatura padrão para domínios que não têm uma política aplicada. Isso significa que se você não configurar o DKIM por conta própria, o Office 365 usará a política e as chaves padrão que ele criar para habilitar o DKIM para o seu domínio.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p122">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your custom domain and the associated private key which we store internally in our datacenter. By default, Office 365 uses a default signing configuration for domains that do not have a policy in place. This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="85fb6-218">Além disso, se você desabilitar a assinatura DKIM após ativá-la, depois de um período de tempo o Office 365 aplicará automaticamente a política padrão do Office 365 para o seu domínio.</span><span class="sxs-lookup"><span data-stu-id="85fb6-218">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="85fb6-p123">No exemplo a seguir, suponha que o DKIM de fabrikam.com foi habilitado pelo Office 365, não pelo administrador do domínio. Isso significa que os CNAMEs necessários não existem no DNS. Assinaturas DKIM para email deste domínio terão uma aparência similar a esta:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p123">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain. This means that the required CNAMEs do not exist in DNS. DKIM signatures for email from this domain will look something like this:</span></span>
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;

```

<span data-ttu-id="85fb6-p124">Neste exemplo, o nome de host e o domínio contêm os valores para os quais o CNAME apontaria se a assinatura de DKIM para fabrikam.com tivesse sido ativada pelo administrador do domínio. Eventualmente, cada mensagem enviada do Office 365 será assinada com DKIM. Se você mesmo habilitar o DKIM, o domínio será o mesmo que o do campo de endereço De:, neste caso fabrikam.com. Caso contrário, os domínios não corresponderão entre si e, em vez disso, será usado o domínio inicial da sua organização. Para saber mais sobre como determinar seu domínio inicial, confira [Perguntas frequentes sobre domínios](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="85fb6-p124">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator. Eventually, every single message sent from Office 365 will be DKIM-signed. If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com. If you don't, it will not align and instead will use your organization's initial domain. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/en-us/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="85fb6-227">Configurar o DKIM de forma que um serviço terceirizado possa enviar, ou fazer spoof de, emails em nome de seu domínio personalizado</span><span class="sxs-lookup"><span data-stu-id="85fb6-227">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="85fb6-228"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-228"></span></span>

<span data-ttu-id="85fb6-p125">Alguns provedores de serviço de email em massa, ou provedores de software como serviço, permitem que você configure as chaves DKIM para o email originado de seu serviço. Isso exige a coordenação entre sua empresa e a empresa terceirizada para configurar os registros DNS necessários. Não há duas organizações que fazem isso exatamente da mesma maneira. Em vez disso, o processo depende totalmente da organização.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p125">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service. This requires coordination between yourself and the third-party in order to set up the necessary DNS records. No two organizations do it exactly the same way. Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="85fb6-233">Um exemplo de mensagem mostrando um DKIM configurado adequadamente para contoso.com e bulkemailprovider.com pode parecer com este:</span><span class="sxs-lookup"><span data-stu-id="85fb6-233">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="85fb6-234">Neste exemplo, para obter este resultado:</span><span class="sxs-lookup"><span data-stu-id="85fb6-234">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="85fb6-235">O provedor de email em massa deu à Contoso uma chave pública de DKIM.</span><span class="sxs-lookup"><span data-stu-id="85fb6-235">Bulk Email Provider gave Contoso a public DKIM key.</span></span>
    
2. <span data-ttu-id="85fb6-236">A Contoso publicou a chave de DKIM em seu registro DNS.</span><span class="sxs-lookup"><span data-stu-id="85fb6-236">Contoso published the DKIM key to its DNS record.</span></span>
    
3. <span data-ttu-id="85fb6-p126">Ao enviar emails, o Provedor de Email em Massa assina a chave com a chave privada correspondente. Ao fazer isso, o Provedor de Email em Massa anexa a assinatura DKIM ao cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p126">When sending email, Bulk Email Provider signs the key with the corresponding private key. By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>
    
4. <span data-ttu-id="85fb6-p127">Sistemas de recebimento de email executam uma verificação de DKIM autenticando o valor DKIM-Signature d=\<domínio\> em relação ao domínio no campo de endereço From: (5322.From) da mensagem. Neste exemplo, os valores são correspondentes:</span><span class="sxs-lookup"><span data-stu-id="85fb6-p127">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message. In this example, the values match:</span></span>
    
    <span data-ttu-id="85fb6-241">remetente@ **contoso.com**</span><span class="sxs-lookup"><span data-stu-id="85fb6-241">sender@ **contoso.com**</span></span>
    
    <span data-ttu-id="85fb6-242">d= **contoso.com**</span><span class="sxs-lookup"><span data-stu-id="85fb6-242">d= **contoso.com**</span></span>
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="85fb6-243">Próximas etapas: depois de configurar o DKIM para o Office 365</span><span class="sxs-lookup"><span data-stu-id="85fb6-243">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="85fb6-244"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="85fb6-244"></span></span>

<span data-ttu-id="85fb6-p128">Embora DKIM foi projetado para ajudar a impedir falsificação, DKIM funciona melhor com SPF e DMARC. Depois que você definiu DKIM, se você já não tiver configurado a SPF deve fazê-lo. Para obter uma introdução rápida SPF e instalá-la configurado rapidamente, consulte [Configurar SPF no Office 365 para ajudar a impedir a falsificação](set-up-spf-in-office-365-to-help-prevent-spoofing.md). Para ter uma compreensão mais detalhada de como o Office 365 usa SPF ou para implantações não-padrão ou de solução de problemas, por exemplo, híbrida, inicie com [como o Office 365 usa Framework de política do remetente (SPF) para evitar a falsificação](how-office-365-uses-spf-to-prevent-spoofing.md). Em seguida, consulte [DMARC de uso para validar emails no Office 365](use-dmarc-to-validate-email.md). [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md) inclui os campos de sintaxes e de cabeçalho usados pelo Office 365 para verificações de verificação.</span><span class="sxs-lookup"><span data-stu-id="85fb6-p128">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC. Once you have set up DKIM, if you have not already set up SPF you should do so. For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md). [Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span> 
  

