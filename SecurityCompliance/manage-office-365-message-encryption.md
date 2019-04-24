---
title: Gerenciar a Criptografia de Mensagens do Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- M365-security-compliance
description: Depois de concluir a configuração do Office 365 Message Encryption (OME), você pode personalizar a configuração da implantação de várias maneiras. Por exemplo, você pode configurar se deseja habilitar códigos de passagem única, exibir o botão proteger no Outlook na Web e muito mais. As tarefas deste artigo descrevem como.
ms.openlocfilehash: 7b5297ae42d3efa071408540863c6ff7dbdee407
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259809"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="0da2c-105">Gerenciar a Criptografia de Mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="0da2c-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="0da2c-106">Depois de concluir a configuração do Office 365 Message Encryption (OME), você pode personalizar a configuração da implantação de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="0da2c-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways.</span></span> <span data-ttu-id="0da2c-107">Por exemplo, você pode configurar se deseja habilitar códigos de passagem única, exibir o botão **proteger** no Outlook na Web e muito mais.</span><span class="sxs-lookup"><span data-stu-id="0da2c-107">For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more.</span></span> <span data-ttu-id="0da2c-108">As tarefas deste artigo descrevem como.</span><span class="sxs-lookup"><span data-stu-id="0da2c-108">The tasks in this article describe how.</span></span>
  
||
|:-----|
|<span data-ttu-id="0da2c-109">Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0da2c-109">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="0da2c-110">Este artigo destina-se a administradores e ITPros.</span><span class="sxs-lookup"><span data-stu-id="0da2c-110">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="0da2c-111">Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="0da2c-111">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="0da2c-112">Gerenciando se o Google, Yahoo e destinatários de contas da Microsoft podem usar essas contas para entrar no portal de criptografia de mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="0da2c-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="0da2c-113">Por padrão, quando você configura os novos recursos de criptografia de mensagem do Office 365, os usuários em sua organização podem enviar mensagens para destinatários fora da sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0da2c-113">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="0da2c-114">Se o destinatário usar uma *ID social* , como uma conta do Google, uma conta do Yahoo ou uma conta da Microsoft, o destinatário poderá entrar no portal do ome usando a ID social.</span><span class="sxs-lookup"><span data-stu-id="0da2c-114">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID.</span></span> <span data-ttu-id="0da2c-115">Se quiser, você pode optar por não permitir que os destinatários usem IDs sociais para entrar no portal do OME.</span><span class="sxs-lookup"><span data-stu-id="0da2c-115">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="0da2c-116">Para gerenciar o fato de permitir ou não que os destinatários usem IDs sociais para entrar no portal do OME</span><span class="sxs-lookup"><span data-stu-id="0da2c-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="0da2c-117">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0da2c-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="0da2c-118">Execute o cmdlet Set-OMEConfiguration com o parâmetro SocialIdSignIn da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0da2c-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   <span data-ttu-id="0da2c-119">Por exemplo, para desabilitar as IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="0da2c-119">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="0da2c-120">Para habilitar as IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="0da2c-120">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="0da2c-121">Gerenciando o uso de códigos de passagem única para entrar no portal de criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="0da2c-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="0da2c-122">Por padrão, se o destinatário de uma mensagem criptografada por OME não usa o Outlook, independentemente da conta usada pelo destinatário, o destinatário recebe um link de exibição da Web de tempo limitado que permite que ele leia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0da2c-122">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="0da2c-123">Isso inclui um código de passagem única.</span><span class="sxs-lookup"><span data-stu-id="0da2c-123">This includes a one-time pass code.</span></span> <span data-ttu-id="0da2c-124">Como administrador, você pode gerenciar se os códigos de passagem única podem ser usados para entrar no portal do OME.</span><span class="sxs-lookup"><span data-stu-id="0da2c-124">As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="0da2c-125">Para gerenciar se os códigos de passagem única são gerados ou não para OME</span><span class="sxs-lookup"><span data-stu-id="0da2c-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="0da2c-126">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-126">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="0da2c-127">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="0da2c-127">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="0da2c-128">Execute o cmdlet Set-OMEConfiguration com o parâmetro OTPEnabled:</span><span class="sxs-lookup"><span data-stu-id="0da2c-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="0da2c-129">Por exemplo, para desabilitar códigos de passagem única:</span><span class="sxs-lookup"><span data-stu-id="0da2c-129">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="0da2c-130">Para habilitar códigos de passagem única:</span><span class="sxs-lookup"><span data-stu-id="0da2c-130">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="0da2c-131">Gerenciando a exibição do botão proteger no Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="0da2c-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="0da2c-132">Por padrão, o botão **proteger** no Outlook na Web não é habilitado quando você configura o ome.</span><span class="sxs-lookup"><span data-stu-id="0da2c-132">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME.</span></span> <span data-ttu-id="0da2c-133">Como administrador, você pode gerenciar se este botão deve ou não ser exibido para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="0da2c-133">As an administrator, you can manage whether or not to display this button to end users.</span></span>
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="0da2c-134">Para gerenciar se o botão proteger aparece ou não no Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="0da2c-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="0da2c-135">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-135">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="0da2c-136">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="0da2c-136">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="0da2c-137">Execute o cmdlet Set-IRMConfiguration com o parâmetro-SimplifiedClientAccessEnabled:</span><span class="sxs-lookup"><span data-stu-id="0da2c-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="0da2c-138">Por exemplo, para desabilitar o botão **proteger** :</span><span class="sxs-lookup"><span data-stu-id="0da2c-138">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="0da2c-139">Para habilitar o botão **proteger** :</span><span class="sxs-lookup"><span data-stu-id="0da2c-139">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="0da2c-140">Habilitar a descriptografia do lado do serviço de mensagens de email para usuários do aplicativo iOS mail</span><span class="sxs-lookup"><span data-stu-id="0da2c-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="0da2c-141">O aplicativo de email iOS não pode descriptografar mensagens protegidas com a criptografia de mensagem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0da2c-141">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="0da2c-142">Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para mensagens entregues ao aplicativo de email iOS.</span><span class="sxs-lookup"><span data-stu-id="0da2c-142">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="0da2c-143">Quando você optar por fazer isso, o serviço enviará uma cópia descriptografada da mensagem para o dispositivo iOS.</span><span class="sxs-lookup"><span data-stu-id="0da2c-143">When you choose to do this, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="0da2c-144">A mensagem é armazenada descriptografada no dispositivo cliente.</span><span class="sxs-lookup"><span data-stu-id="0da2c-144">The message is stored decrypted on the client device.</span></span> <span data-ttu-id="0da2c-145">A mensagem também mantém informações sobre direitos de uso, mesmo que o aplicativo de email iOS não aplique direitos de uso do lado do cliente ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0da2c-145">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="0da2c-146">Isso significa que o usuário pode copiar ou imprimir a mensagem, mesmo que não tenha originalmente os direitos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="0da2c-146">This means that the user can copy or print the message even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="0da2c-147">No enTanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar a mensagem, o servidor não permitirá a ação se o usuário não tiver originalmente o direito de uso para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="0da2c-147">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so.</span></span> <span data-ttu-id="0da2c-148">No enTanto, os usuários finais podem trabalhar em torno não para enCaminhar a restrição de uso ao encaminhar a mensagem de uma conta diferente no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="0da2c-148">However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app.</span></span> <span data-ttu-id="0da2c-149">Independentemente de você configurar a descriptografia do lado do serviço de email, todos os anexos a mensagens criptografadas e de direitos protegidos não podem ser exibidos no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="0da2c-149">Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="0da2c-150">Se você optar por não permitir que as mensagens descriptografadas sejam enviadas aos usuários do aplicativo de email iOS, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0da2c-150">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="0da2c-151">Por padrão, a descriptografia do lado do serviço de mensagens de email não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0da2c-151">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="0da2c-152">Para obter mais informações e para uma visão da experiência do cliente, consulte [Exibir mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="0da2c-152">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="0da2c-153">Para gerenciar se os usuários de aplicativos de email iOS podem ou não exibir mensagens protegidas pela criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="0da2c-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="0da2c-154">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-154">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="0da2c-155">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="0da2c-155">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="0da2c-156">Execute o cmdlet Set-ActiveSyncOrganizations com o parâmetro AllowRMSSupportForUnenlightenedApps:</span><span class="sxs-lookup"><span data-stu-id="0da2c-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="0da2c-157">Por exemplo, para configurar o serviço para descriptografar mensagens antes que elas sejam enviadas para aplicativos não habilitados, como o aplicativo de email iOS:</span><span class="sxs-lookup"><span data-stu-id="0da2c-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="0da2c-158">Ou, para configurar o serviço para não enviar mensagens descriptografadas a aplicativos não habilitados:</span><span class="sxs-lookup"><span data-stu-id="0da2c-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="0da2c-159">Habilitar a descriptografia do lado do serviço de anexos de email para clientes de email de navegador da Web</span><span class="sxs-lookup"><span data-stu-id="0da2c-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="0da2c-160">Normalmente, quando você usa a criptografia de mensagem do Office 365, os anexos são criptografados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0da2c-160">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="0da2c-161">Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para os anexos de email que os usuários baixem de um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="0da2c-161">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="0da2c-162">Quando você optar por fazer isso, o serviço enviará uma cópia descriptografada do arquivo ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0da2c-162">When you choose to do this, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="0da2c-163">A mensagem ainda está criptografada.</span><span class="sxs-lookup"><span data-stu-id="0da2c-163">The message is still encrypted.</span></span> <span data-ttu-id="0da2c-164">O anexo de email também mantém informações sobre direitos de uso, embora o navegador não aplique direitos de uso do lado do cliente ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0da2c-164">The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user.</span></span> <span data-ttu-id="0da2c-165">Isso significa que o usuário pode copiar ou imprimir o anexo de email, mesmo que não tenha originalmente os direitos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="0da2c-165">This means that the user can copy or print the email attachment even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="0da2c-166">No enTanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar o anexo, o servidor não permitirá a ação se o usuário não tiver originalmente o direito de uso para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="0da2c-166">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="0da2c-167">Independentemente de você configurar a descriptografia do lado do serviço de anexos, todos os anexos a mensagens criptografadas e de direitos protegidos não podem ser exibidos no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="0da2c-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="0da2c-168">Se você optar por não permitir anexos de email descriptografados, que é o padrão, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir o anexo.</span><span class="sxs-lookup"><span data-stu-id="0da2c-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="0da2c-169">Para obter mais informações sobre como o Office 365 implementa a criptografia de emails e anexos de email com a opção somente criptografia, consulte [opção somente criptografia para emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="0da2c-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="0da2c-170">Para gerenciar se os anexos de email serão descriptografados no download a partir de um navegador da Web</span><span class="sxs-lookup"><span data-stu-id="0da2c-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="0da2c-171">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-171">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="0da2c-172">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="0da2c-172">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="0da2c-173">Execute o cmdlet Set-IRMConfiguration com o parâmetro DecryptAttachmentFromPortal:</span><span class="sxs-lookup"><span data-stu-id="0da2c-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="0da2c-174">Por exemplo, para configurar o serviço para descriptografar anexos de email quando um usuário o baixa de um navegador da Web:</span><span class="sxs-lookup"><span data-stu-id="0da2c-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="0da2c-175">Para configurar o serviço para deixar anexos de email criptografados como estão no download:</span><span class="sxs-lookup"><span data-stu-id="0da2c-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="0da2c-176">Personalizando a aparência de mensagens de email e o portal do OME</span><span class="sxs-lookup"><span data-stu-id="0da2c-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="0da2c-177">Para obter informações detalhadas sobre como você pode personalizar o OME para sua organização, confira [Adicionar a marca da sua organização às mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0da2c-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="0da2c-178">Desabilitando os novos recursos do OME</span><span class="sxs-lookup"><span data-stu-id="0da2c-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="0da2c-179">Esperamos que ele não venha, mas se você precisar, desabilitar os novos recursos do OME é muito simples.</span><span class="sxs-lookup"><span data-stu-id="0da2c-179">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="0da2c-180">Primeiro, você precisará remover as regras de fluxo de emails que criou que usam os novos recursos do OME.</span><span class="sxs-lookup"><span data-stu-id="0da2c-180">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="0da2c-181">Para obter informações sobre como remover regras de fluxo de email, consulte [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0da2c-181">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="0da2c-182">Em seguida, conclua estas etapas no PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-182">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="0da2c-183">Para desabilitar os novos recursos do OME</span><span class="sxs-lookup"><span data-stu-id="0da2c-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="0da2c-184">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0da2c-184">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="0da2c-185">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="0da2c-185">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="0da2c-186">Se você habilitou o botão **proteger** no Outlook na Web, desabilite-o executando o cmdlet Set-IRMConfiguration com o parâmetro SimplifiedClientAccessEnabled.</span><span class="sxs-lookup"><span data-stu-id="0da2c-186">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="0da2c-187">Caso contrário, pule esta etapa.</span><span class="sxs-lookup"><span data-stu-id="0da2c-187">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="0da2c-188">DesAbilite os novos recursos do OME executando o cmdlet Set-IRMConfiguration com o parâmetro AzureRMSLicensingEnabled definido como false:</span><span class="sxs-lookup"><span data-stu-id="0da2c-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
