---
title: Gerenciar a Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Depois de concluir a configuração de backup do Office 365 Message Encryption (OME), você pode personalizar a configuração da sua implantação em um número de formas. Por exemplo, você pode configurar se deseja habilitar as senhas de uma única vez, exibir o botão de Protect no Outlook na web e muito mais. As tarefas neste artigo descrevem como.
ms.openlocfilehash: ddc86bdf0d0ce5480587862a4ed438b6c138987f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523793"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="2b886-105">Gerenciar a Criptografia de Mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b886-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="2b886-p102">Depois de concluir a configuração de backup do Office 365 Message Encryption (OME), você pode personalizar a configuração da sua implantação em um número de formas. Por exemplo, você pode configurar se deseja habilitar as senhas de uma única vez, exibir o botão de **Protect** no Outlook na web e muito mais. As tarefas neste artigo descrevem como.</span><span class="sxs-lookup"><span data-stu-id="2b886-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span> 
  
||
|:-----|
|<span data-ttu-id="2b886-p103">Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Este artigo destina-se aos administradores e profissionais de TI. Se você apenas estiver procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos no [Office 365 Message Encryption (OME)](ome.md) e localize o artigo que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="2b886-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and IT Pros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="2b886-112">Gerenciando se destinatários Google, Yahoo e Account da Microsoft podem usar essas contas para entrar no portal do Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="2b886-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="2b886-113"><a name="PermitSocialID"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-113"></span></span>

<span data-ttu-id="2b886-p104">Por padrão, quando você configura os novos recursos do Office 365 Message Encryption, usuários em sua organização podem enviar mensagens para destinatários que estão fora da sua organização do Office 365. Se o destinatário usa uma *ID social* como uma conta do Google, Yahoo conta ou conta da Microsoft, o destinatário pode entrar no portal do OME usando o ID de social. Se desejar, você pode optar por não permitir que os destinatários usar IDs sociais para entrar no portal OME.</span><span class="sxs-lookup"><span data-stu-id="2b886-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a  *social ID*  such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span> 
  
 <span data-ttu-id="2b886-117">**Para gerenciar se deseja ou não permitir que os destinatários usar IDs sociais para entrar no portal OME**</span><span class="sxs-lookup"><span data-stu-id="2b886-117">**To manage whether or not to allow recipients to use social IDs to sign in to the OME portal**</span></span>
  
1. <span data-ttu-id="2b886-118">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-118">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-119">Execute o cmdlet Set-OMEConfiguration com o parâmetro SocialIdSignIn da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-119">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    <span data-ttu-id="2b886-120">Por exemplo, para desativar as IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="2b886-120">For example, to disable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    <span data-ttu-id="2b886-121">Para permitir que IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="2b886-121">To enable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="2b886-122">Gerenciando o uso de senhas únicas para entrar no portal do Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="2b886-122">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="2b886-123"><a name="GenerateOTPC"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-123"></span></span>

<span data-ttu-id="2b886-p105">Por padrão, se o destinatário de uma mensagem criptografada por OME não usa o Outlook, independentemente da conta usada pelo destinatário, o destinatário receberá um link de modo de exibição da web de tempo limitado que permite que eles ler a mensagem. Isso inclui uma senha de uma única vez. Como administrador, você pode gerenciar senhas ocasional podem ser usadas para entrar no portal OME ou não.</span><span class="sxs-lookup"><span data-stu-id="2b886-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
 <span data-ttu-id="2b886-127">**Para gerenciar os senhas uma única vez ou não são geradas para OME**</span><span class="sxs-lookup"><span data-stu-id="2b886-127">**To manage whether or not one-time pass codes are generated for OME**</span></span>
  
1. <span data-ttu-id="2b886-128">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-128">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-129">Execute o cmdlet Set-OMEConfiguration com o parâmetro OTPEnabled da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-129">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    <span data-ttu-id="2b886-130">Por exemplo, para desabilitar as senhas de uma única vez:</span><span class="sxs-lookup"><span data-stu-id="2b886-130">For example, to disable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    <span data-ttu-id="2b886-131">Para permitir que as senhas de uma única vez:</span><span class="sxs-lookup"><span data-stu-id="2b886-131">To enable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="2b886-132">Gerenciar a exibição do botão Protect no Outlook na web</span><span class="sxs-lookup"><span data-stu-id="2b886-132">Managing the display of the Protect button in Outlook on the web</span></span>
<span data-ttu-id="2b886-133"><a name="DisplayProtectButton"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-133"></span></span>

<span data-ttu-id="2b886-p106">Por padrão, o botão **Protect** no Outlook na web não está habilitado quando você configura OME. Como administrador, você pode gerenciar se deseja ou não exibir este botão aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="2b886-p106">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span> 
  
 <span data-ttu-id="2b886-136">**Para gerenciar ou não o botão Protect aparece no Outlook na web**</span><span class="sxs-lookup"><span data-stu-id="2b886-136">**To manage whether or not the Protect button appears in Outlook on the web**</span></span>
  
1. <span data-ttu-id="2b886-137">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-137">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-138">Execute o cmdlet Set-IRMConfiguration com o parâmetro - SimplifiedClientAccessEnabled da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-138">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    <span data-ttu-id="2b886-139">Por exemplo, para desabilitar o botão **Protect** :</span><span class="sxs-lookup"><span data-stu-id="2b886-139">For example, to disable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    <span data-ttu-id="2b886-140">Para habilitar o botão **Protect** :</span><span class="sxs-lookup"><span data-stu-id="2b886-140">To enable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="2b886-141">Habilitar a descriptografia do lado do serviço de mensagens de email para usuários de aplicativo de email iOS</span><span class="sxs-lookup"><span data-stu-id="2b886-141">Enable service-side decryption of email messages for iOS mail app users</span></span>
<span data-ttu-id="2b886-142"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-142"></span></span>

<span data-ttu-id="2b886-p107">O aplicativo de email iOS não é possível descriptografar mensagens protegidas com criptografia de mensagem do Office 365. Como um administrador do Office 365, você pode aplicar a descriptografia no lado do serviço de mensagens entregues para o aplicativo de email iOS. Quando você optar por fazer isso, o serviço envia uma cópia descriptografada da mensagem ao dispositivo iOS. A mensagem é armazenada descriptografados no dispositivo do cliente. A mensagem também mantém informações sobre os direitos de uso, mesmo que o aplicativo de email iOS não se aplica a direitos de uso do cliente para o usuário. Isso significa que o usuário pode copiar ou imprimir a mensagem, mesmo se eles não tivesse originalmente os direitos de fazê-lo. No entanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhamento da mensagem, o servidor não permitirá que a ação se o usuário não tivesse originalmente o direito de uso de fazê-lo. No entanto, os usuários finais podem dar uma solução alternativa não encaminhar as restrições de uso pelo encaminhamento da mensagem de uma conta diferente no seu email de iOS App. independentemente se você configurar descriptografia do lado do serviço de email, quaisquer direitos e anexos criptografados protegido por email não podem ser exibidos no aplicativo de email iOS.</span><span class="sxs-lookup"><span data-stu-id="2b886-p107">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="2b886-p108">Se você optar por não permitir descriptografadas mensagens sejam enviadas aos usuários do aplicativo de email de iOS, os usuários recebem uma mensagem informando que não têm os direitos para exibir a mensagem. Por padrão, a descriptografia do lado do serviço de mensagens de email não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2b886-p108">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="2b886-154">Para obter mais informações e para um modo de exibição da experiência do cliente, consulte a seção "[ler mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)de" em [visualizar mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="2b886-154">For more information, and for a view of the client experience, see the section, "[View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
 <span data-ttu-id="2b886-155">**Para gerenciar usuários de aplicativo de email do iOS ou não pode exibir mensagens protegidas pelo Office 365 Message Encryption**</span><span class="sxs-lookup"><span data-stu-id="2b886-155">**To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption**</span></span>
  
1. <span data-ttu-id="2b886-156">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-156">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-157">Execute o cmdlet Set-ActiveSyncOrganizations com o parâmetro AllowRMSSupportForUnenlightenedApps da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-157">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter as follows:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    <span data-ttu-id="2b886-158">Por exemplo, para configurar o serviço para descriptografar mensagens antes de serem enviadas aos aplicativos unenlightened como o iOS mensagens app:</span><span class="sxs-lookup"><span data-stu-id="2b886-158">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    <span data-ttu-id="2b886-159">Por exemplo, para configurar o serviço não para enviar mensagens descriptografadas aos aplicativos unenlightened:</span><span class="sxs-lookup"><span data-stu-id="2b886-159">For example, to configure the service not to send decrypted messages to unenlightened apps:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="2b886-160">Habilitar a descriptografia do lado do serviço de anexos de email para clientes de email do navegador da web</span><span class="sxs-lookup"><span data-stu-id="2b886-160">Enable service-side decryption of email attachments for web browser mail clients</span></span>
<span data-ttu-id="2b886-161"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-161"></span></span>

<span data-ttu-id="2b886-p109">Normalmente, quando você usa criptografia de mensagem do Office 365, anexos serão criptografados automaticamente. Como um administrador do Office 365, você pode aplicar a descriptografia do lado do serviço anexos de email que os usuários fazer download de um navegador da web.</span><span class="sxs-lookup"><span data-stu-id="2b886-p109">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span> 
  
<span data-ttu-id="2b886-p110">Quando você optar por fazer isso, o serviço envia uma cópia descriptografada do arquivo para o dispositivo. A mensagem ainda é criptografada. O anexo de email também mantém informações sobre os direitos de uso, mesmo que o navegador não se aplica a direitos de uso do cliente para o usuário. Isso significa que o usuário pode copiar ou imprimir o anexo de email, mesmo se eles não tivesse originalmente os direitos de fazê-lo. No entanto, se o usuário tentar concluir uma ação que requer que o servidor de email do Office 365, como encaminhamento o anexo, o servidor não permitirá que a ação se o usuário não tivesse originalmente o direito de uso de fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="2b886-p110">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="2b886-169">Independentemente se você configurar a descriptografia no lado do serviço de anexos, todos os anexos para criptografados e direitos de email protegido não pode ser exibido no aplicativo de email iOS.</span><span class="sxs-lookup"><span data-stu-id="2b886-169">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="2b886-p111">Se você optar por não permitir anexos de email descriptografada, que é o padrão, os usuários recebem uma mensagem informando que não têm os direitos para exibir o anexo. \* \* \* Inserir imagem?</span><span class="sxs-lookup"><span data-stu-id="2b886-p111">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment. \*\*\* insert picture?</span></span>
  
<span data-ttu-id="2b886-172">Para obter mais informações sobre como o Office 365 implementa a criptografia para emails e anexos com a opção somente criptografar, consulte [opção somente criptografar para e-mails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="2b886-172">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
 <span data-ttu-id="2b886-173">**Para gerenciar os anexos de email ou não sejam descriptografados no download de um navegador da web**</span><span class="sxs-lookup"><span data-stu-id="2b886-173">**To manage whether or not email attachments are decrypted on download from a web browser**</span></span>
  
1. <span data-ttu-id="2b886-174">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-174">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-175">Execute o cmdlet Set-IRMConfiguration com o parâmetro DecryptAttachmentFromPortal da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-175">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    <span data-ttu-id="2b886-176">Por exemplo configurar o serviço para descriptografar os anexos de email quando um usuário faz o download de um navegador da web:</span><span class="sxs-lookup"><span data-stu-id="2b886-176">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    <span data-ttu-id="2b886-177">Para configurar o serviço para deixar anexos de email criptografadas como eles estão após o download:</span><span class="sxs-lookup"><span data-stu-id="2b886-177">To configure the service to leave encrypted email attachments as they are upon download:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="2b886-178">Personalizando a aparência das mensagens de email e o portal OME</span><span class="sxs-lookup"><span data-stu-id="2b886-178">Customizing the appearance of email messages and the OME portal</span></span>
<span data-ttu-id="2b886-179"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-179"></span></span>

<span data-ttu-id="2b886-180">Para obter informações detalhadas sobre como você pode personalizar OME para sua organização, consulte [Adicionar a marca da sua organização a suas mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2b886-180">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="2b886-181">Desabilitando os novos recursos para o OME</span><span class="sxs-lookup"><span data-stu-id="2b886-181">Disabling the new capabilities for OME</span></span>
<span data-ttu-id="2b886-182"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="2b886-182"></span></span>

<span data-ttu-id="2b886-p112">Esperamos que ela não vir a ele, mas se você precisa, desabilitando os novos recursos para o OME é muito simples. Primeiro, você precisará remover qualquer mail flow regras que você criou que usam os novos recursos OME. Para obter informações sobre como remover regras de fluxo de correio, consulte [Gerenciar regras de fluxo de email](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Em seguida, conclua estas etapas no Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b886-p112">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
 <span data-ttu-id="2b886-187">**Para desabilitar os novos recursos para o OME**</span><span class="sxs-lookup"><span data-stu-id="2b886-187">**To disable the new capabilities for OME**</span></span>
  
1. <span data-ttu-id="2b886-188">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b886-188">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="2b886-189">Se você habilitou o botão Protect no Outlook na web, desabilitá-lo executando o cmdlet Set-IRMConfiguration com o parâmetro SimplifiedClientAccessEnabled da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-189">If you enabled the Protect button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. <span data-ttu-id="2b886-190">Execute o cmdlet Set-IRMConfiguration com o parâmetro AzureRMSLicensingEnabled da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b886-190">Run the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


