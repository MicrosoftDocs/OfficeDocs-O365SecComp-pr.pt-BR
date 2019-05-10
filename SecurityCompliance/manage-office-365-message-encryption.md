---
title: Gerenciar a Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 5/8/2019
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Após concluir a configuração do Office 365 Message Encryption (OME), você pode personalizar a configuração de sua implantação de várias maneiras. Por exemplo, você pode configurar se deseja habilitar códigos de passagem única, exibir o botão proteger no Outlook na Web e muito mais. As tarefas deste artigo descrevem como.
ms.openlocfilehash: 1afaaea3cd744878630598acd3f02dc7dc70e9cb
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834920"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="e28c5-105">Gerenciar a Criptografia de Mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="e28c5-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="e28c5-106">Após concluir a configuração do Office 365 Message Encryption (OME), você pode personalizar a configuração de sua implantação de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="e28c5-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in several ways.</span></span> <span data-ttu-id="e28c5-107">Por exemplo, você pode configurar se deseja habilitar códigos de passagem única, exibir o botão **proteger** no Outlook na Web e muito mais.</span><span class="sxs-lookup"><span data-stu-id="e28c5-107">For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more.</span></span> <span data-ttu-id="e28c5-108">As tarefas deste artigo descrevem como.</span><span class="sxs-lookup"><span data-stu-id="e28c5-108">The tasks in this article describe how.</span></span>

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="e28c5-109">Gerenciar se o Google, Yahoo e destinatários de contas da Microsoft podem usar essas contas para entrar no portal de criptografia de mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="e28c5-109">Manage whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="e28c5-110">Ao configurar os novos recursos de criptografia de mensagens do Office 365, os usuários em sua organização podem enviar mensagens para destinatários fora da sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e28c5-110">When you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="e28c5-111">Se o destinatário usar uma *ID social* , como uma conta do Google, uma conta do Yahoo ou uma conta da Microsoft, o destinatário poderá entrar no portal do ome com uma ID social.</span><span class="sxs-lookup"><span data-stu-id="e28c5-111">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal with a social ID.</span></span> <span data-ttu-id="e28c5-112">Se quiser, você pode optar por não permitir que os destinatários usem IDs sociais para entrar no portal do OME.</span><span class="sxs-lookup"><span data-stu-id="e28c5-112">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="e28c5-113">Para gerenciar se os destinatários podem usar IDs sociais para entrar no portal do OME</span><span class="sxs-lookup"><span data-stu-id="e28c5-113">To manage whether recipients can use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="e28c5-114">[Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e28c5-114">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="e28c5-115">Execute o cmdlet Set-OMEConfiguration com o parâmetro SocialIdSignIn da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e28c5-115">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   <span data-ttu-id="e28c5-116">Por exemplo, para desabilitar as IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="e28c5-116">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="e28c5-117">Para habilitar as IDs sociais:</span><span class="sxs-lookup"><span data-stu-id="e28c5-117">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a><span data-ttu-id="e28c5-118">Gerenciar o uso de códigos de passagem única para o portal de criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="e28c5-118">Manage the use of one-time pass codes for the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="e28c5-119">Se o destinatário de uma mensagem criptografada pelo OME não usar o Outlook, independentemente da conta usada pelo destinatário, o destinatário receberá um link de exibição da Web de tempo limitado que permite que ele leia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e28c5-119">If the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="e28c5-120">Este link inclui um código de passagem única.</span><span class="sxs-lookup"><span data-stu-id="e28c5-120">This link includes a one-time pass code.</span></span> <span data-ttu-id="e28c5-121">Como administrador, você pode decidir se os destinatários podem usar códigos de passagem única para entrar no portal do OME.</span><span class="sxs-lookup"><span data-stu-id="e28c5-121">As an administrator, you can decide if recipients can use one-time pass codes to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a><span data-ttu-id="e28c5-122">Para gerenciar se o OME gera códigos de passagem única</span><span class="sxs-lookup"><span data-stu-id="e28c5-122">To manage whether OME generates one-time pass codes</span></span>
  
1. <span data-ttu-id="e28c5-123">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365 e inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-123">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-124">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-124">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-125">Execute o cmdlet Set-OMEConfiguration com o parâmetro OTPEnabled:</span><span class="sxs-lookup"><span data-stu-id="e28c5-125">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="e28c5-126">Por exemplo, para desabilitar códigos de passagem única:</span><span class="sxs-lookup"><span data-stu-id="e28c5-126">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="e28c5-127">Para habilitar códigos de passagem única:</span><span class="sxs-lookup"><span data-stu-id="e28c5-127">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="e28c5-128">Gerenciar a exibição do botão proteger no Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="e28c5-128">Manage the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="e28c5-129">O botão **proteger** no Outlook na Web é desabilitado quando você configura o ome.</span><span class="sxs-lookup"><span data-stu-id="e28c5-129">The **Protect** button in Outlook on the web is disabled when you set up OME.</span></span> <span data-ttu-id="e28c5-130">Como administrador, você pode gerenciar se deseja exibir este botão para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="e28c5-130">As an administrator, you can manage whether to display this button to end users.</span></span>
  
### <a name="to-manage-whether-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="e28c5-131">Para gerenciar se o botão proteger aparece no Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="e28c5-131">To manage whether the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="e28c5-132">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365 e inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-132">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-133">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-133">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-134">Execute o cmdlet Set-IRMConfiguration com o parâmetro-SimplifiedClientAccessEnabled:</span><span class="sxs-lookup"><span data-stu-id="e28c5-134">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="e28c5-135">Por exemplo, para desabilitar o botão **proteger** :</span><span class="sxs-lookup"><span data-stu-id="e28c5-135">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="e28c5-136">Para habilitar o botão **proteger** :</span><span class="sxs-lookup"><span data-stu-id="e28c5-136">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="e28c5-137">Habilitar a descriptografia do lado do serviço de mensagens de email para usuários do aplicativo iOS mail</span><span class="sxs-lookup"><span data-stu-id="e28c5-137">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="e28c5-138">O aplicativo de email iOS não pode descriptografar mensagens protegidas com a criptografia de mensagem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e28c5-138">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="e28c5-139">Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para mensagens entregues ao aplicativo de email iOS.</span><span class="sxs-lookup"><span data-stu-id="e28c5-139">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="e28c5-140">Quando você opta por usar a descriptografia do lado do serviço, o serviço envia uma cópia descriptografada da mensagem para o dispositivo iOS.</span><span class="sxs-lookup"><span data-stu-id="e28c5-140">When you choose to do use service-side decryption, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="e28c5-141">O dispositivo cliente armazena uma cópia descriptografada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e28c5-141">The client device stores a decrypted copy of the message.</span></span> <span data-ttu-id="e28c5-142">A mensagem também mantém informações sobre direitos de uso, mesmo que o aplicativo de email iOS não aplique direitos de uso do lado do cliente ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e28c5-142">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="e28c5-143">O usuário pode copiar ou imprimir a mensagem, mesmo que não tenha originalmente os direitos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e28c5-143">The user can copy or print the message even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="e28c5-144">No entanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar a mensagem, o servidor não permitirá a ação se o usuário não tiver originalmente o uso do direito de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e28c5-144">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span> <span data-ttu-id="e28c5-145">No entanto, os usuários finais podem contornar a restrição de uso "não encaminhar" encaminhando a mensagem de uma conta diferente no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="e28c5-145">However, end users can work around "Do Not Forward" usage restriction by forwarding the message from a different account within the iOS mail app.</span></span> <span data-ttu-id="e28c5-146">Independentemente de você configurar a descriptografia do lado do serviço de email, os anexos a mensagens criptografadas e protegidas por direitos não podem ser exibidos no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="e28c5-146">Regardless of whether you set up service-side decryption of mail, attachments to encrypted and rights protected mail can't be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="e28c5-147">Se você optar por não permitir que as mensagens descriptografadas sejam enviadas aos usuários do aplicativo de email iOS, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e28c5-147">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="e28c5-148">Por padrão, a descriptografia do lado do serviço de mensagens de email não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e28c5-148">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="e28c5-149">Para obter mais informações e para uma visão da experiência do cliente, consulte [Exibir mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="e28c5-149">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="e28c5-150">Para gerenciar se os usuários do aplicativo iOS podem exibir mensagens protegidas pela criptografia de mensagens do Office 365</span><span class="sxs-lookup"><span data-stu-id="e28c5-150">To manage whether iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="e28c5-151">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365 e inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-151">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-152">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-152">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-153">Execute o cmdlet Set-ActiveSyncOrganizations com o parâmetro AllowRMSSupportForUnenlightenedApps:</span><span class="sxs-lookup"><span data-stu-id="e28c5-153">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="e28c5-154">Por exemplo, para configurar o serviço para descriptografar mensagens antes que elas sejam enviadas para aplicativos não habilitados, como o aplicativo de email iOS:</span><span class="sxs-lookup"><span data-stu-id="e28c5-154">For example, to configure the service to decrypt messages before they're sent to unenlightened apps like the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="e28c5-155">Ou, para configurar o serviço para não enviar mensagens descriptografadas a aplicativos não habilitados:</span><span class="sxs-lookup"><span data-stu-id="e28c5-155">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="e28c5-156">Habilitar a descriptografia do lado do serviço de anexos de email para clientes de email de navegador da Web</span><span class="sxs-lookup"><span data-stu-id="e28c5-156">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="e28c5-157">Normalmente, quando você usa a criptografia de mensagem do Office 365, os anexos são criptografados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e28c5-157">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="e28c5-158">Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para os anexos de email que os usuários baixem de um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="e28c5-158">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="e28c5-159">Quando você usa a descriptografia do lado do serviço, o serviço envia uma cópia descriptografada do arquivo ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e28c5-159">When you use service-side decryption, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="e28c5-160">A mensagem ainda está criptografada.</span><span class="sxs-lookup"><span data-stu-id="e28c5-160">The message is still encrypted.</span></span> <span data-ttu-id="e28c5-161">O anexo de email também mantém informações sobre direitos de uso, embora o navegador não aplique direitos de uso do lado do cliente ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e28c5-161">The email attachment also keeps information about usage rights even though the browser doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="e28c5-162">O usuário pode copiar ou imprimir o anexo de email, mesmo que não tenha originalmente os direitos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e28c5-162">The user can copy or print the email attachment even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="e28c5-163">No entanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar o anexo, o servidor não permitirá a ação se o usuário não tiver originalmente o uso do direito de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e28c5-163">However, if the user tries to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span>
  
<span data-ttu-id="e28c5-164">Independentemente de você configurar a descriptografia do lado do serviço de anexos, os usuários não podem exibir nenhum anexo a emails protegidos e criptografados no aplicativo de email do iOS.</span><span class="sxs-lookup"><span data-stu-id="e28c5-164">Regardless of whether you set up service-side decryption of attachments, users can't view any attachments to encrypted and rights protected mail in the iOS mail app.</span></span>
  
<span data-ttu-id="e28c5-165">Se você optar por não permitir anexos de email descriptografados, que é o padrão, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir o anexo.</span><span class="sxs-lookup"><span data-stu-id="e28c5-165">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="e28c5-166">Para obter mais informações sobre como o Office 365 implementa a criptografia de emails e anexos de email com a opção somente criptografia, consulte [opção somente criptografia para emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="e28c5-166">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="e28c5-167">Para gerenciar se os anexos de email são descriptografados no download a partir de um navegador da Web</span><span class="sxs-lookup"><span data-stu-id="e28c5-167">To manage whether email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="e28c5-168">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365 e inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-168">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-169">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-169">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-170">Execute o cmdlet Set-IRMConfiguration com o parâmetro DecryptAttachmentFromPortal:</span><span class="sxs-lookup"><span data-stu-id="e28c5-170">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="e28c5-171">Por exemplo, para configurar o serviço para descriptografar anexos de email quando um usuário o baixa de um navegador da Web:</span><span class="sxs-lookup"><span data-stu-id="e28c5-171">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="e28c5-172">Para configurar o serviço para deixar anexos de email criptografados como estão no download:</span><span class="sxs-lookup"><span data-stu-id="e28c5-172">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a><span data-ttu-id="e28c5-173">Garantir que todos os destinatários externos usem o portal do OME para ler emails criptografados — somente criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="e28c5-173">Ensure all external recipients use the OME Portal to read encrypted mail — Office 365 Advanced Message Encryption only</span></span>

<span data-ttu-id="e28c5-174">Se você tiver a criptografia de mensagem avançada do Office 365, poderá usar modelos de identidade visual personalizados para forçar os destinatários a receber emails de conteúdo adicional que os direcionam a ler emails criptografados no portal do OME, em vez de usar o Outlook ou o Outlook na Web.</span><span class="sxs-lookup"><span data-stu-id="e28c5-174">If you have Office 365 Advanced Message Encryption, you can use custom branding templates to force recipients to receive a wrapper mail that directs them to read encrypted email in the OME Portal instead of using Outlook or Outlook on the web.</span></span> <span data-ttu-id="e28c5-175">Você pode querer fazer isso se você usar deseja ter maior controle sobre como os destinatários usam o email que eles recebem.</span><span class="sxs-lookup"><span data-stu-id="e28c5-175">You might want to do this if you use want greater control over how recipients use the mail they receive.</span></span> <span data-ttu-id="e28c5-176">Por exemplo, se os destinatários externos exibem email no portal da Web, você pode definir uma data de expiração para o email e pode revogar o email.</span><span class="sxs-lookup"><span data-stu-id="e28c5-176">For example, if external recipients view email in the web portal, you can set an expiration date for the email, and you can revoke the email.</span></span> <span data-ttu-id="e28c5-177">Esses recursos só são compatíveis com o portal do OME.</span><span class="sxs-lookup"><span data-stu-id="e28c5-177">These features are only supported through the OME Portal.</span></span> <span data-ttu-id="e28c5-178">Você pode usar a opção criptografar e a opção não encaminhar ao criar regras de fluxo de emails.</span><span class="sxs-lookup"><span data-stu-id="e28c5-178">You can use the Encrypt option and the Do Not Forward option when creating the mail flow rules.</span></span>

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a><span data-ttu-id="e28c5-179">Criar um modelo personalizado para forçar todos os destinatários externos a usar o portal do OME e para que os emails criptografados sejam revogávels e expirarem em 7 dias</span><span class="sxs-lookup"><span data-stu-id="e28c5-179">Create a custom template to force all external recipients to use the OME Portal and for encrypted email to be revocable and expire in 7 days</span></span>

1. <span data-ttu-id="e28c5-180">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365 e inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-180">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-181">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-181">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-182">Execute o cmdlet New-OMEConfiguration:</span><span class="sxs-lookup"><span data-stu-id="e28c5-182">Run the New-OMEConfiguration cmdlet:</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   <span data-ttu-id="e28c5-183">em `template name` que é o nome que você deseja usar para o modelo de identidade visual personalizada de criptografia de mensagem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e28c5-183">where `template name` is the name you want to use for the Office 365 Message Encryption custom branding template.</span></span> <span data-ttu-id="e28c5-184">For example,</span><span class="sxs-lookup"><span data-stu-id="e28c5-184">For example,</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. <span data-ttu-id="e28c5-185">Execute o cmdlet New-TransportRule:</span><span class="sxs-lookup"><span data-stu-id="e28c5-185">Run the New-TransportRule cmdlet:</span></span>

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    <span data-ttu-id="e28c5-186">em que:</span><span class="sxs-lookup"><span data-stu-id="e28c5-186">where:</span></span>

   - <span data-ttu-id="e28c5-187">`mail flow rule name`é o nome que você deseja usar para a nova regra de fluxo de emails.</span><span class="sxs-lookup"><span data-stu-id="e28c5-187">`mail flow rule name` is the name you want to use for the new mail flow rule.</span></span>

   - <span data-ttu-id="e28c5-188">`option name`é `Encrypt` ou `Do Not Forward`.</span><span class="sxs-lookup"><span data-stu-id="e28c5-188">`option name` is either `Encrypt` or `Do Not Forward`.</span></span>

   - <span data-ttu-id="e28c5-189">`template name`é o nome que você deu ao modelo de identidade visual personalizado, `One week expiration`por exemplo.</span><span class="sxs-lookup"><span data-stu-id="e28c5-189">`template name` is the name you gave the custom branding template, for example `One week expiration`.</span></span>

   <span data-ttu-id="e28c5-190">Para criptografar todos os emails externos com o modelo "expiração de uma semana" e aplicar a opção somente criptografia:</span><span class="sxs-lookup"><span data-stu-id="e28c5-190">To encrypt all external email with the "One week expiration" template and apply the Encrypt-Only option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   <span data-ttu-id="e28c5-191">Para criptografar todos os emails externos com o modelo "expiração de uma semana" e aplicar a opção não encaminhar:</span><span class="sxs-lookup"><span data-stu-id="e28c5-191">To encrypt all external email with the "One week expiration" template and apply the Do Not Forward option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="e28c5-192">Personalizar a aparência de mensagens de email e o portal do OME</span><span class="sxs-lookup"><span data-stu-id="e28c5-192">Customize the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="e28c5-193">Para obter informações detalhadas sobre como você pode personalizar o OME para sua organização, confira [Adicionar a marca da sua organização às mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e28c5-193">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disable-the-new-capabilities-for-ome"></a><span data-ttu-id="e28c5-194">Desabilitar os novos recursos do OME</span><span class="sxs-lookup"><span data-stu-id="e28c5-194">Disable the new capabilities for OME</span></span>

<span data-ttu-id="e28c5-195">Esperamos que ele não venha, mas se você precisar, desabilitar os novos recursos do OME é muito simples.</span><span class="sxs-lookup"><span data-stu-id="e28c5-195">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="e28c5-196">Primeiro, você precisará remover as regras de fluxo de emails que criou que usam os novos recursos do OME.</span><span class="sxs-lookup"><span data-stu-id="e28c5-196">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="e28c5-197">Para obter informações sobre como remover regras de fluxo de email, consulte [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e28c5-197">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="e28c5-198">Em seguida, conclua estas etapas no PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-198">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="e28c5-199">Para desabilitar os novos recursos do OME</span><span class="sxs-lookup"><span data-stu-id="e28c5-199">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="e28c5-200">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e28c5-200">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e28c5-201">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e28c5-201">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e28c5-202">Se você habilitou o botão **proteger** no Outlook na Web, desabilite-o executando o cmdlet Set-IRMConfiguration com o parâmetro SimplifiedClientAccessEnabled.</span><span class="sxs-lookup"><span data-stu-id="e28c5-202">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="e28c5-203">Caso contrário, pule esta etapa.</span><span class="sxs-lookup"><span data-stu-id="e28c5-203">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="e28c5-204">Desabilite os novos recursos do OME executando o cmdlet Set-IRMConfiguration com o parâmetro AzureRMSLicensingEnabled definido como false:</span><span class="sxs-lookup"><span data-stu-id="e28c5-204">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
