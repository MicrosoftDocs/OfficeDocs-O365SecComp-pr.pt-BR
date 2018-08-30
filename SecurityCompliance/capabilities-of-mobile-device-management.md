---
title: Recursos de Gerenciamento de Dispositivos Móveis internos para o Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.DevicePolicySupportedDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: a1da44e5-7475-4992-be91-9ccec25905b0
description: Gerenciamento de dispositivos móveis para o Office 365 pode ajudá-lo a proteger e gerenciar dispositivos móveis, como iPhones, iPads, Androids e Windows Phones utilizados na organização. Crie políticas de gerenciamento de dispositivo móvel com as configurações que podem ajudar a controlar o acesso a email do Office 365 e documentos para dispositivos móveis suportados e aplicativos de sua organização e permitem que você apagar um dispositivo remotamente, se ele for roubado.
ms.openlocfilehash: b7200eee3b50c2fc6d3e0ea0920236d71837a88b
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272596"
---
# <a name="capabilities-of-built-in-mobile-device-management-for-office-365"></a>Recursos de Gerenciamento de Dispositivos Móveis internos para o Office 365

Gerenciamento de dispositivos móveis para o Office 365 pode ajudá-lo a proteger e gerenciar dispositivos móveis, como iPhones, iPads, Androids e Windows Phones utilizado pelos usuários licenciados do Office 365 em sua organização. Você pode criar políticas de gerenciamento de dispositivo móvel com configurações que podem ajudar a controlar o acesso a documentos para aplicativos e dispositivos móveis suportados e email do Office 365 da sua organização. Se um dispositivo é perdido ou roubado, você pode apagar remotamente o dispositivo para remover informações organizacionais confidenciais.
    
Precisa de mais funcionalidades que está incluído no MDM para o Office 365? Se o Microsoft Intune tem o que você precisa: [escolher entre MDM para Office 365 e Microsoft Intune](choose-between-mdm-and-intune.md).
  
## <a name="supported-devices"></a>Dispositivos suportados

Você pode usar o MDM para o Office 365 para proteger e gerenciar os seguintes tipos de dispositivos.
  
- Windows Phone 8.1 +
    
- iOS 7.1 ou versões posteriores
    
- Android 4 ou versões posteriores
    
- Windows 8.1\*
    
- Windows 8.1 RT\*
    
- Windows 10\*\*
    
- Windows 10 Mobile\*\*
    
\*Controle de acesso para dispositivos Windows 8.1 e Windows 8.1 RT é limitado ao Exchange ActiveSync.
  
\*\*Requer o dispositivo ser ingressou no Windows Azure Active Directory e ser registrados no serviço de gerenciamento de dispositivo móvel de sua organização.
  
Se as pessoas na sua organização usar dispositivos móveis que não são suportados pelo gerenciamento de dispositivos móveis para o Office 365, você talvez queira bloquear o acesso de app do Exchange ActiveSync para email do Office 365 para esses dispositivos, para ajudar a tornar os dados da sua organização mais seguro. Etapas para bloquear o Exchange ActiveSync: consulte [Gerenciar configurações de acesso de dispositivo](manage-device-access-settings.md).
  
## <a name="access-control-for-office-365-email-and-documents"></a>Controle de acesso aos emails e documentos do Office 365

Aplicativos suportados para os diferentes tipos de dispositivos móveis na tabela a seguir sugerem a registrar-se no MDM para o Office 365 onde houver uma nova política de gerenciamento de dispositivos móveis que se aplica a um dispositivo do usuário e o usuário não tiver anteriormente inscritos no dispositivo. Se um dispositivo do usuário não estiver em conformidade com uma política, dependendo de como configurar a diretiva, um usuário poderá ser bloqueado acessem recursos do Office 365 nesses aplicativos, ou eles podem ter acesso mas Office 365 informará uma violação de política.
  
||**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|
|:-----|:-----|:-----|:-----|
|**Exchange** <br/> Exchange ActiveSync inclui eletrônico interno e aplicativos de terceiros, como TouchDown, que usam a versão do Exchange ActiveSync 14,1 ou posterior.  <br/> |![Ícone do Exchange ActiveSync](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Ícone móvel do Exchange Mail](media/5b5312b4-3bfb-4fc7-84ff-d7ab21227c10.png)Email do Exchange  <br/> |![Ícone do Exchange ActiveSync](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Ícone móvel do Email para o iPhone](media/888bdc7a-8354-4013-a0b2-0d4432a9a92e.png)Email  <br/> |![Ícone do Exchange ActiveSync](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Ícone de email do Android](media/20b48492-4adc-40ce-99cf-1b47bd2b389d.png)Email  <br/> |
|**Office** e **OneDrive for Business** <br/> |Não há aplicativos com suporte  <br/> |![Ícone móvel do Outlook para iPhone](media/6c63112d-c10c-4040-85cc-feeccc3dd424.png)Outlook  <br/> ![Ícone móvel do OneDrive para iPhone](media/560ec187-82d9-4793-b72f-7ba595972bdc.png)OneDrive  <br/> ![Ícone móvel do Word para iPhone](media/63a3a749-1f98-402f-b211-e46b9224b655.png)Word  <br/> ![Ícone móvel do Excel para iPhone](media/5b8f62c0-96aa-4602-9ed8-f837bbf5fa9e.png)Excel  <br/> ![Ícone móvel do PowerPoint para iPhone](media/17c02dca-f60a-4d13-a610-00d576a40943.png)PowerPoint  <br/> |**Em smartphones e tablets:** <br/> ![Android ícone de telefone e tablet Outlook mobile](media/ed2a813d-f481-46e0-acc9-6422f0d16072.png)Outlook  <br/> ![Ícone do telefone Android OneDrive mobile](media/64855d02-1684-4795-b4c5-863860f18722.png)OneDrive  <br/> ![Ícone de móveis Android do Word](media/f618fe83-b163-4680-b924-fcedc06ab4ba.png)Word  <br/> ![Ícone de móveis Android do Excel](media/659c7a5f-5797-4b47-a776-4a0c8f784c89.png)Excel  <br/> ![Ícone de móveis Android do PowerPoint](media/35b98bce-d7cb-40ce-87e3-07b9764207b1.png)PowerPoint  <br/> **Apenas para telefones:** <br/> ![Ícone de móvel móveis do Office](media/1aa9e978-6eb2-40aa-82da-62fb79cee313.png)Office Mobile  <br/> |
   
> [!NOTE]
>  Suporte para iOS 7.1 e versões posteriores inclui iPhone e iPad devices. > Gerenciamento de dispositivos BlackBerry não é suportado pelo gerenciamento de dispositivos móveis para o Office 365. Use o BlackBerry Business Cloud Services (BBCS) do BlackBerry para gerenciar dispositivos BlackBerry. > Usuários não serão avisados para registrar e não ser bloqueados ou relatado por violação de política se eles usarem o navegador móvel para acessar sites do Office 365 SharePoint, documentos no Office Online ou email no Outlook Web App. 
  
O diagrama a seguir mostra o que acontece quando um usuário com um novo dispositivo entra um aplicativo que suporta controle com MDM de acesso para o Office 365. O usuário é impedido de acessar os recursos do Office 365 no aplicativo até que se inscrever seus dispositivos.
  
![Mostra o processo de registro para um novo dispositivo.](media/O365-MDM-Capabilities-EnrollmentExample.png)
  
> [!NOTE]
> Políticas e regras de acesso criadas no MDM para Office 365 substituirão políticas de caixa de correio de dispositivo móvel do Exchange ActiveSync e regras de acesso de dispositivo criadas no Centro de administração do Exchange. Depois que um dispositivo está inscrito no MDM para o Office 365, qualquer política de caixa de correio de dispositivo móvel do Exchange ActiveSync ou aplicada ao dispositivo da regra de acesso de dispositivo será ignorada. Para saber mais sobre o Exchange ActiveSync, consulte [Exchange ActiveSync no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="policy-settings-for-mobile-devices"></a>Configurações de política para dispositivos móveis

Se você criar uma política para bloquear o acesso com determinadas configurações ativadas, os usuários serão bloqueados de acessar os recursos do Office 365 ao usar um aplicativo com suporte que está listado no [controle de acesso de email do Office 365 e documentos](#access-control-for-office-365-email-and-documents). As configurações que podem impedir que os usuários acessem os recursos do Office 365 são nestas seções:
  
- Segurança
    
- Criptografia
    
- Desbloqueado
    
- Perfil de email gerenciado
    
Por exemplo, o diagrama a seguir mostra o que acontece quando um usuário com um dispositivo registrado não é compatível com uma configuração de segurança em uma política de gerenciamento de dispositivos móveis que se aplica ao seu dispositivo. O usuário entra um aplicativo que suporta controle com MDM de acesso para o Office 365. Eles estão impedidos de acessar os recursos do Office 365 no aplicativo até que seu dispositivo está de acordo com a configuração de segurança.
  
![Mostra que o usuário está bloqueado quando o dispositivo não é compatível.](media/O365-MDM-Capabilities-ComplianceExample.png)
  
As seções a seguir listam as configurações de política que você pode usar para proteger e gerenciar dispositivos móveis que se conectam aos recursos do Office 365 da sua organização. 
  
### <a name="security-settings"></a>Configurações de segurança

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exigir uma senha  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Impedir senha simples  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Exigir uma senha alfanumérica  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Tamanho mínimo da senha  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Número de falhas de entrada antes de o dispositivo ser apagado  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Minutos de inatividade antes de o dispositivo ser bloqueado  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Vencimento da senha (dias)  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Lembrar histórico de senhas e impedir reutilização  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="encryption-settings"></a>Configurações de criptografia

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exigir criptografia de dados em dispositivos  <br/> |O Windows Phone 8.1 já é criptografado e não pode ser descriptografado  <br/> |✖  <br/> |✔  <br/> |✔\*  <br/> |
   
\*Com Samsung Knox, você também pode exigir criptografia em cartões de armazenamento.
  
### <a name="jail-broken-setting"></a>Configuração de desbloqueio

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|O dispositivo não pode ser desbloqueado ou modificado  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="managed-email-profile-option"></a>Opção de perfil de email gerenciado

A seguinte opção pode impedir que os usuários acessem seus emails do Office 365 se elas estão usando um perfil de email criada manualmente. Usuários em dispositivos iOS devem excluir seu perfil de email criada manualmente, para que possam acessar seus emails. Depois que eles excluir o perfil, um novo perfil será criado automaticamente no dispositivo.
  
|**Nome da Configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|O perfil de email é gerenciado  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="cloud-settings"></a>Configurações de nuvem

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exige backup criptografado  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquear cópia de segurança na nuvem  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquear sincronização de documento  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquear sincronização de fotos  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Permitir que o backup do Google  <br/> |N/D  <br/> |N/D  <br/> |✖  <br/> |✔  <br/> |
|Permitir sincronização de automática de conta do Google  <br/> |N/D  <br/> |N/D  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="system-settings"></a>Configurações do sistema

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquear captura de tela  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Bloquear o envio de dados de diagnóstico do dispositivo  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="application-settings"></a>Configurações de aplicativo

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquear videoconferências no dispositivo  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquear o acesso à loja de aplicativos  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Exigir senha ao acessar a loja de aplicativos  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="device-capabilities-settings"></a>Configurações de recursos do dispositivo

|**Nome da configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquear a conexão com armazenamento removível  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|Bloquear conexão Bluetooth  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="additional-settings"></a>Configurações adicionais

Você pode definir as seguintes configurações de diretiva adicional usando cmdlets do PowerShell. Para obter mais informações, consulte [a segurança do Office 365 &amp; cmdlets do Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkId=827804).
  
|**Nome da Configuração**|**Windows Phone 8.1 +**|**iOS 7.1 ou posterior**|**Android 4 + (incluindo Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|CameraEnabled  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|RegionRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MoviesRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|TVShowsRating  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AppsRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceDialing  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceAssistant  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowAssistantWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowPassbookWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MaxPasswordGracePeriod  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|PasswordQuality  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|SystemSecurityTLS  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|WLANEnabled  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="settings-supported-by-windows"></a>Configurações com suporte do Windows

Você pode gerenciar dispositivos Windows 8.1 e Windows 10 inscrevendo-las como dispositivos móveis. Depois que uma diretiva aplicável for implantada, os usuários com dispositivos Windows 8.1 RT e Windows 10 RT precisará registrar-se no MDM para o Office 365 na primeira vez que usam o aplicativo de email internas para acessar seus emails do Office 365. 
  
As configurações a seguir são suportadas para dispositivos Windows 8.1 e Windows 10 registrados como dispositivos móveis. Essas configurações não impedir que os usuários acessem os recursos do Office 365.
  
 **Configurações de segurança**
  
- Exigir uma senha alfanumérica
    
- Tamanho mínimo da senha
    
- Número de falhas de entrada antes de o dispositivo ser apagado
    
- Minutos de inatividade antes de o dispositivo ser bloqueado
    
- Vencimento da senha (dias)
    
- Lembrar histórico de senhas e impedir reutilização
    
 **Configurações do sistema**
  
Bloquear o envio de dados de diagnóstico do dispositivo
  
 **Configurações adicionais**
  
Você pode definir as seguintes configurações de política adicionais usando cmdlets do PowerShell:
  
- AllowConvenienceLogon
    
- UserAccountControlStatus
    
- FirewallStatus
    
- AutoUpdateStatus
    
- AntiVirusStatus
    
- AntiVirusSignatureStatus
    
- SmartScreenEnabled
    
- WorkFoldersSyncUrl
    
## <a name="remotely-wipe-a-mobile-device"></a>Apagar remotamente um dispositivo móvel

 Se um dispositivo é perdido ou roubado, você pode remover dados organizacionais confidenciais e ajudar a impedir o acesso aos recursos do Office 365 da sua organização, fazendo uma limpeza de segurança de ** &amp; Centro de conformidade\>prevenção de perda de dados\>dispositivo gerenciamento**. Você pode fazer uma limpeza seletiva para remover apenas dados organizacionais ou uma limpeza completa para excluir todas as informações de um dispositivo e restaurá-lo para suas configurações de fábrica.
  
Para obter mais informações, consulte [Apagar um dispositivo móvel no Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518157).
  
## <a name="see-also"></a>Confira também

[Visão geral do Gerenciamento de Dispositivos Móveis para o Office 365](overview-of-mdm.md)
  
[Criar e implantar políticas de segurança de dispositivo](create-device-security-policies.md)

