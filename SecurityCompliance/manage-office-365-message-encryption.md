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
# <a name="manage-office-365-message-encryption"></a>Gerenciar a Criptografia de Mensagens do Office 365

Depois de concluir a configuração do Office 365 Message Encryption (OME), você pode personalizar a configuração da implantação de várias maneiras. Por exemplo, você pode configurar se deseja habilitar códigos de passagem única, exibir o botão **proteger** no Outlook na Web e muito mais. As tarefas deste artigo descrevem como.
  
||
|:-----|
|Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo destina-se a administradores e ITPros. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Gerenciando se o Google, Yahoo e destinatários de contas da Microsoft podem usar essas contas para entrar no portal de criptografia de mensagens do Office 365

Por padrão, quando você configura os novos recursos de criptografia de mensagem do Office 365, os usuários em sua organização podem enviar mensagens para destinatários fora da sua organização do Office 365. Se o destinatário usar uma *ID social* , como uma conta do Google, uma conta do Yahoo ou uma conta da Microsoft, o destinatário poderá entrar no portal do ome usando a ID social. Se quiser, você pode optar por não permitir que os destinatários usem IDs sociais para entrar no portal do OME.
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>Para gerenciar o fato de permitir ou não que os destinatários usem IDs sociais para entrar no portal do OME
  
1. [Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Execute o cmdlet Set-OMEConfiguration com o parâmetro SocialIdSignIn da seguinte maneira:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   Por exemplo, para desabilitar as IDs sociais:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   Para habilitar as IDs sociais:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Gerenciando o uso de códigos de passagem única para entrar no portal de criptografia de mensagem do Office 365

Por padrão, se o destinatário de uma mensagem criptografada por OME não usa o Outlook, independentemente da conta usada pelo destinatário, o destinatário recebe um link de exibição da Web de tempo limitado que permite que ele leia a mensagem. Isso inclui um código de passagem única. Como administrador, você pode gerenciar se os códigos de passagem única podem ser usados para entrar no portal do OME.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>Para gerenciar se os códigos de passagem única são gerados ou não para OME
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-OMEConfiguration com o parâmetro OTPEnabled:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   Por exemplo, para desabilitar códigos de passagem única:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   Para habilitar códigos de passagem única:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Gerenciando a exibição do botão proteger no Outlook na Web

Por padrão, o botão **proteger** no Outlook na Web não é habilitado quando você configura o ome. Como administrador, você pode gerenciar se este botão deve ou não ser exibido para os usuários finais.
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>Para gerenciar se o botão proteger aparece ou não no Outlook na Web
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-IRMConfiguration com o parâmetro-SimplifiedClientAccessEnabled:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   Por exemplo, para desabilitar o botão **proteger** :

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   Para habilitar o botão **proteger** :

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Habilitar a descriptografia do lado do serviço de mensagens de email para usuários do aplicativo iOS mail

O aplicativo de email iOS não pode descriptografar mensagens protegidas com a criptografia de mensagem do Office 365. Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para mensagens entregues ao aplicativo de email iOS. Quando você optar por fazer isso, o serviço enviará uma cópia descriptografada da mensagem para o dispositivo iOS. A mensagem é armazenada descriptografada no dispositivo cliente. A mensagem também mantém informações sobre direitos de uso, mesmo que o aplicativo de email iOS não aplique direitos de uso do lado do cliente ao usuário. Isso significa que o usuário pode copiar ou imprimir a mensagem, mesmo que não tenha originalmente os direitos para fazer isso. No enTanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar a mensagem, o servidor não permitirá a ação se o usuário não tiver originalmente o direito de uso para fazer isso. No enTanto, os usuários finais podem trabalhar em torno não para enCaminhar a restrição de uso ao encaminhar a mensagem de uma conta diferente no aplicativo de email do iOS. Independentemente de você configurar a descriptografia do lado do serviço de email, todos os anexos a mensagens criptografadas e de direitos protegidos não podem ser exibidos no aplicativo de email do iOS.
  
Se você optar por não permitir que as mensagens descriptografadas sejam enviadas aos usuários do aplicativo de email iOS, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir a mensagem. Por padrão, a descriptografia do lado do serviço de mensagens de email não está habilitada.
  
Para obter mais informações e para uma visão da experiência do cliente, consulte [Exibir mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>Para gerenciar se os usuários de aplicativos de email iOS podem ou não exibir mensagens protegidas pela criptografia de mensagem do Office 365
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-ActiveSyncOrganizations com o parâmetro AllowRMSSupportForUnenlightenedApps:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   Por exemplo, para configurar o serviço para descriptografar mensagens antes que elas sejam enviadas para aplicativos não habilitados, como o aplicativo de email iOS:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   Ou, para configurar o serviço para não enviar mensagens descriptografadas a aplicativos não habilitados:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Habilitar a descriptografia do lado do serviço de anexos de email para clientes de email de navegador da Web

Normalmente, quando você usa a criptografia de mensagem do Office 365, os anexos são criptografados automaticamente. Como administrador do Office 365, você pode aplicar a descriptografia do lado do serviço para os anexos de email que os usuários baixem de um navegador da Web.
  
Quando você optar por fazer isso, o serviço enviará uma cópia descriptografada do arquivo ao dispositivo. A mensagem ainda está criptografada. O anexo de email também mantém informações sobre direitos de uso, embora o navegador não aplique direitos de uso do lado do cliente ao usuário. Isso significa que o usuário pode copiar ou imprimir o anexo de email, mesmo que não tenha originalmente os direitos para fazer isso. No enTanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhar o anexo, o servidor não permitirá a ação se o usuário não tiver originalmente o direito de uso para fazer isso.
  
Independentemente de você configurar a descriptografia do lado do serviço de anexos, todos os anexos a mensagens criptografadas e de direitos protegidos não podem ser exibidos no aplicativo de email do iOS.
  
Se você optar por não permitir anexos de email descriptografados, que é o padrão, os usuários receberão uma mensagem afirmando que eles não têm direitos para exibir o anexo.
  
Para obter mais informações sobre como o Office 365 implementa a criptografia de emails e anexos de email com a opção somente criptografia, consulte [opção somente criptografia para emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>Para gerenciar se os anexos de email serão descriptografados no download a partir de um navegador da Web
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-IRMConfiguration com o parâmetro DecryptAttachmentFromPortal:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   Por exemplo, para configurar o serviço para descriptografar anexos de email quando um usuário o baixa de um navegador da Web:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   Para configurar o serviço para deixar anexos de email criptografados como estão no download:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Personalizando a aparência de mensagens de email e o portal do OME

Para obter informações detalhadas sobre como você pode personalizar o OME para sua organização, confira [Adicionar a marca da sua organização às mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>Desabilitando os novos recursos do OME

Esperamos que ele não venha, mas se você precisar, desabilitar os novos recursos do OME é muito simples. Primeiro, você precisará remover as regras de fluxo de emails que criou que usam os novos recursos do OME. Para obter informações sobre como remover regras de fluxo de email, consulte [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Em seguida, conclua estas etapas no PowerShell do Exchange Online.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>Para desabilitar os novos recursos do OME
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Se você habilitou o botão **proteger** no Outlook na Web, desabilite-o executando o cmdlet Set-IRMConfiguration com o parâmetro SimplifiedClientAccessEnabled. Caso contrário, pule esta etapa.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. DesAbilite os novos recursos do OME executando o cmdlet Set-IRMConfiguration com o parâmetro AzureRMSLicensingEnabled definido como false:

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
