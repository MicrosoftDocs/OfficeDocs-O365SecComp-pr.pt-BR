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
ms.openlocfilehash: 460ac0bba4d10fe8bef896a23a20f74527f031b2
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750050"
---
# <a name="manage-office-365-message-encryption"></a>Gerenciar a Criptografia de Mensagens do Office 365

Depois de concluir a configuração de backup do Office 365 Message Encryption (OME), você pode personalizar a configuração da sua implantação em um número de formas. Por exemplo, você pode configurar se deseja habilitar as senhas de uma única vez, exibir o botão de **Protect** no Outlook na web e muito mais. As tarefas neste artigo descrevem como. 
  
||
|:-----|
|Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Este artigo destina-se aos administradores e profissionais de TI. Se você apenas estiver procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos no [Office 365 Message Encryption (OME)](ome.md) e localize o artigo que atenda às suas necessidades. |

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Gerenciando se destinatários Google, Yahoo e Account da Microsoft podem usar essas contas para entrar no portal do Office 365 Message Encryption

Por padrão, quando você configura os novos recursos do Office 365 Message Encryption, usuários em sua organização podem enviar mensagens para destinatários que estão fora da sua organização do Office 365. Se o destinatário usa uma *ID social* como uma conta do Google, Yahoo conta ou conta da Microsoft, o destinatário pode entrar no portal do OME usando o ID de social. Se desejar, você pode optar por não permitir que os destinatários usar IDs sociais para entrar no portal OME. 
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>Para gerenciar se deseja ou não permitir que os destinatários usar IDs sociais para entrar no portal OME
  
1. [Conecte-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Execute o cmdlet Set-OMEConfiguration com o parâmetro SocialIdSignIn da seguinte maneira:

  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
  ```

  Por exemplo, para desativar as IDs sociais:
  
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

  Para permitir que IDs sociais:

  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Gerenciando o uso de senhas únicas para entrar no portal do Office 365 Message Encryption

Por padrão, se o destinatário de uma mensagem criptografada por OME não usa o Outlook, independentemente da conta usada pelo destinatário, o destinatário receberá um link de modo de exibição da web de tempo limitado que permite que eles ler a mensagem. Isso inclui uma senha de uma única vez. Como administrador, você pode gerenciar senhas ocasional podem ser usadas para entrar no portal OME ou não.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>Para gerenciar os senhas uma única vez ou não são geradas para OME
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-OMEConfiguration com o parâmetro OTPEnabled:

   ```Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>```

   Por exemplo, para desabilitar as senhas de uma única vez:

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false```

   Para permitir que as senhas de uma única vez:

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Gerenciar a exibição do botão Protect no Outlook na web

Por padrão, o botão **Protect** no Outlook na web não está habilitado quando você configura OME. Como administrador, você pode gerenciar se deseja ou não exibir este botão aos usuários finais. 
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>Para gerenciar ou não o botão Protect aparece no Outlook na web
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-IRMConfiguration com o parâmetro - SimplifiedClientAccessEnabled:

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>```

   Por exemplo, para desabilitar o botão **Protect** :

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

   Para habilitar o botão **Protect** :

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $true```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Habilitar a descriptografia do lado do serviço de mensagens de email para usuários de aplicativo de email iOS

O aplicativo de email iOS não é possível descriptografar mensagens protegidas com criptografia de mensagem do Office 365. Como um administrador do Office 365, você pode aplicar a descriptografia no lado do serviço de mensagens entregues para o aplicativo de email iOS. Quando você optar por fazer isso, o serviço envia uma cópia descriptografada da mensagem ao dispositivo iOS. A mensagem é armazenada descriptografados no dispositivo do cliente. A mensagem também mantém informações sobre os direitos de uso, mesmo que o aplicativo de email iOS não se aplica a direitos de uso do cliente para o usuário. Isso significa que o usuário pode copiar ou imprimir a mensagem, mesmo se eles não tivesse originalmente os direitos de fazê-lo. No entanto, se o usuário tentar concluir uma ação que requer o servidor de email do Office 365, como encaminhamento da mensagem, o servidor não permitirá que a ação se o usuário não tivesse originalmente o direito de uso de fazê-lo. No entanto, os usuários finais podem dar uma solução alternativa não encaminhar as restrições de uso pelo encaminhamento da mensagem de uma conta diferente no seu email de iOS App. independentemente se você configurar descriptografia do lado do serviço de email, quaisquer direitos e anexos criptografados protegido por email não podem ser exibidos no aplicativo de email iOS.
  
Se você optar por não permitir descriptografadas mensagens sejam enviadas aos usuários do aplicativo de email de iOS, os usuários recebem uma mensagem informando que não têm os direitos para exibir a mensagem. Por padrão, a descriptografia do lado do serviço de mensagens de email não está habilitada.
  
Para obter mais informações e para um modo de exibição da experiência do cliente, consulte a seção "[ler mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)de" em [visualizar mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>Para gerenciar usuários de aplicativo de email do iOS ou não pode exibir mensagens protegidas pelo Office 365 Message Encryption
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-ActiveSyncOrganizations com o parâmetro AllowRMSSupportForUnenlightenedApps:

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>```

   Por exemplo, para configurar o serviço para descriptografar mensagens antes de serem enviadas aos aplicativos unenlightened como o iOS mensagens app:

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true```

   Ou, para configurar o serviço não para enviar mensagens descriptografadas aos aplicativos unenlightened:

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Habilitar a descriptografia do lado do serviço de anexos de email para clientes de email do navegador da web

Normalmente, quando você usa criptografia de mensagem do Office 365, anexos serão criptografados automaticamente. Como um administrador do Office 365, você pode aplicar a descriptografia do lado do serviço anexos de email que os usuários fazer download de um navegador da web. 
  
Quando você optar por fazer isso, o serviço envia uma cópia descriptografada do arquivo para o dispositivo. A mensagem ainda é criptografada. O anexo de email também mantém informações sobre os direitos de uso, mesmo que o navegador não se aplica a direitos de uso do cliente para o usuário. Isso significa que o usuário pode copiar ou imprimir o anexo de email, mesmo se eles não tivesse originalmente os direitos de fazê-lo. No entanto, se o usuário tentar concluir uma ação que requer que o servidor de email do Office 365, como encaminhamento o anexo, o servidor não permitirá que a ação se o usuário não tivesse originalmente o direito de uso de fazê-lo.
  
Independentemente se você configurar a descriptografia no lado do serviço de anexos, todos os anexos para criptografados e direitos de email protegido não pode ser exibido no aplicativo de email iOS.
  
Se você optar por não permitir anexos de email descriptografada, que é o padrão, os usuários recebem uma mensagem informando que não têm os direitos para exibir o anexo.
  
Para obter mais informações sobre como o Office 365 implementa a criptografia para emails e anexos com a opção somente criptografar, consulte [opção somente criptografar para e-mails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>Para gerenciar os anexos de email ou não sejam descriptografados no download de um navegador da web
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-IRMConfiguration com o parâmetro DecryptAttachmentFromPortal:

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>```

   Por exemplo configurar o serviço para descriptografar os anexos de email quando um usuário faz o download de um navegador da web:

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $true```

   Para configurar o serviço para deixar anexos de email criptografadas como eles estão após o download:

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $false```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Personalizando a aparência das mensagens de email e o portal OME

Para obter informações detalhadas sobre como você pode personalizar OME para sua organização, consulte [Adicionar a marca da sua organização a suas mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>Desabilitando os novos recursos para o OME

Esperamos que ela não vir a ele, mas se você precisa, desabilitando os novos recursos para o OME é muito simples. Primeiro, você precisará remover qualquer mail flow regras que você criou que usam os novos recursos OME. Para obter informações sobre como remover regras de fluxo de correio, consulte [Gerenciar regras de fluxo de email](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Em seguida, conclua estas etapas no Exchange Online PowerShell.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>Para desabilitar os novos recursos para o OME
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Se você habilitou o botão **Protect** no Outlook na web, desabilitá-lo executando o cmdlet Set-IRMConfiguration com o parâmetro SimplifiedClientAccessEnabled. Caso contrário, ignore esta etapa.

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

3. Desabilite os novos recursos para o OME executando o cmdlet Set-IRMConfiguration com o parâmetro AzureRMSLicensingEnabled definido como false:

   ```Set-IRMConfiguration -AzureRMSLicensingEnabled $false```
