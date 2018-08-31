---
title: Obter detalhes sobre os dispositivos gerenciados pelo Mobile Device Management (MDM) para o Office 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MBS150
- MET150
ms.assetid: 5602963c-a1f2-4c21-afb9-f66cd7dca1f0
description: Este artigo mostra como usar o Windows PowerShell para obter detalhes sobre os dispositivos em sua organização que você definiu para gerenciamento de dispositivos móveis para o Office 365.
ms.openlocfilehash: 2e406d3583e7892531b7c74bef0db374672956c7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272526"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a>Obter detalhes sobre os dispositivos gerenciados pelo Mobile Device Management (MDM) para o Office 365

Este artigo mostra como usar o Windows PowerShell para obter detalhes sobre os dispositivos em sua organização que você definiu para gerenciamento de dispositivos móveis para o Office 365. 
  
## <a name="what-device-details-can-i-get"></a>Os detalhes do dispositivo que pode fazer?

Aqui está uma divisão.
  
|**Detalhes**|**O que procurar no PowerShell**|
|:-----|:-----|
|O dispositivo está [inscrito no MDM para o Office 365](enroll-your-mobile-device.md) <br/> |O valor do parâmetro *isManaged* é:  <br/> **True** = dispositivo está inscrito.  <br/> **False** = dispositivo não está inscrito.  <br/> |
|O dispositivo está em conformidade com suas [políticas de segurança de dispositivo](https://go.microsoft.com/fwlink/?linkid=615144) <br/> |O valor do parâmetro *isCompliant* é:  <br/> **True** = dispositivo está em conformidade com políticas.  <br/> **False** = dispositivo não é compatível com políticas.  <br/> |
   
![Fluxo mostrando valores de param de AAD Shell para se os dispositivos serão inscritos e reclamações](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> Os comandos e scripts neste artigo também retornará detalhes sobre todos os dispositivos que são gerenciados pelo [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune). 
  
## <a name="before-you-begin"></a>Antes de começar

Há algumas coisas que você precisará configurado para executar os comandos e scripts descritos neste artigo.
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a>Etapa 1: Baixar e instalar o Windows Azure Active Directory módulo para Windows PowerShell

Para obter mais informações sobre essas etapas, consulte [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).
  
1. Vá para o [Assistente Microsoft Online Services entrar para RTWl de profissionais de TI](https://www.microsoft.com/en-us/download/details.aspx?id=41950) e clique em **Download** para o Assistente de entrada do Microsoft Online Services. 
    
2. Instale o Módulo Microsoft Azure Active Directory para Windows PowerShell seguindo estas etapas:
    
    1. Abra um prompt de comando do PowerShell do nível de administrador.
        
    2. Execute o `Install-Module MSOnline` comando.
        
    3. Se solicitado a instalar o provedor NuGet, digite `Y` e pressione ENTER.
        
    4. Se solicitado a instalar o módulo de PSGallery, digite `Y` e pressione ENTER.
        
    5. Após a instalação, feche a janela de comando do PowerShell.
    
### <a name="step-2-connect-to-your-office-365-subscription"></a>Etapa 2: conectar-se à sua assinatura do Office 365

1. Em que o Windows Azure Active Directory módulo para Windows PowerShell, execute o seguinte comando.</br>  
  `$UserCredential = Get-Credential`

2. Na caixa de diálogo **Solicitação de credencial do Windows PowerShell** , digite o nome de usuário e a senha da sua conta de administrador global do Office 365 e clique em **Okey**.
    
3. Execute o seguinte comando.</br>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a>Etapa 3: Verifique se que você está possibilidade de executar scripts do PowerShell

> [!NOTE]
> Você pode ignorar esta etapa se você já estiver configurado para executar scripts do PowerShell. 
  
Para executar o script **Get-MsolUserDeviceComplianceStatus.ps1** , você precisa habilitar a execução de scripts do PowerShell. 
  
1. Da sua área de trabalho do Windows, clique em **Iniciar**e, em seguida, digite o Windows PowerShell. Clique com botão direito **Do Windows PowerShell**e clique em **Executar como administrador**.
    
2. Execute o seguinte comando.</br>
  `Set-ExecutionPolicy RemoteSigned`

3. Quando solicitado, digite `Y` e pressione Enter. 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a>Execute o cmdlet Get-MsolDevice para exibir os detalhes para todos os dispositivos em sua organização

1. Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.
    
2. Execute o seguinte comando.</br>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

Para obter mais exemplos, consulte [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).
  
## <a name="run-a-script-to-get-device-details"></a>Executar um script para obter detalhes do dispositivo

### <a name="first-save-the-script-to-your-computer"></a>Primeiro, salve o script em seu computador

1. Copie e cole o seguinte texto no bloco de notas.</br> 
  ```
  param (
      [PSObject[]]$users = @(),
      [Switch]$export,
      [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
      [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
  [System.Collections.IDictionary]$script:schema = @{
      
      DeviceId = ''
      DeviceOSType = ''
      DeviceOSVersion = ''
      DeviceTrustLevel = ''
      DisplayName = ''
      IsCompliant = ''
      IsManaged = ''
      ApproximateLastLogonTimestamp = ''
      DeviceObjectId = ''    
      RegisteredOwnerUpn = ''
      RegisteredOwnerObjectId = ''
      RegisteredOwnerDisplayName = ''
  }
  function createResultObject
  {
      [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
      return $resultObject
  }
  If ($users.Count -eq 0)
  {
      $users = Get-MsolUser
  }
  [PSObject[]]$result = foreach ($u in $users)
  {
      
      [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
      foreach ($d in $devices)
      {
          [PSObject]$deviceResult = createResultObject
          $deviceResult.DeviceId = $d.DeviceId 
          $deviceResult.DeviceOSType = $d.DeviceOSType 
          $deviceResult.DeviceOSVersion = $d.DeviceOSVersion 
          $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
          $deviceResult.DisplayName = $d.DisplayName
          $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
          $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
          $deviceResult.DeviceObjectId = $d.ObjectId
          $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
          $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
          $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
          $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
          $deviceResult
      }
  }
  If ($export)
  {
      $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
  }
  Else
  {
      $result
  }
  
  ```

2. Salve-o como um arquivo de script do Windows PowerShell, usando a extensão de arquivo **. ps1**. </br>Exemplo:</br> `Get-MsolUserDeviceComplianceStatus.ps1`.
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a>Execute o script para obter informações do dispositivo para uma conta de usuário único

1. Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.
    
2. Navegue até a pasta onde você salvou o script. Por exemplo, se você salvou às C:\PS-Scripts, você faria execute o seguinte comando.</br>
    `cd C:\PS-Scripts`

3. Execute o seguinte comando para identificar o usuário que você deseja obter os detalhes do dispositivo para. Este exemplo obtém detalhes para bar@example.com.</br>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. Execute o seguinte comando para iniciar o script.</br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

As informações são exportadas para sua área de trabalho do Windows como um arquivo CSV. Você pode usar os parâmetros adicionais para especificar o nome do arquivo e caminho do CSV.
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a>Execute o script para obter informações do dispositivo para um grupo de usuários

1. Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.
    
2. Navegue até a pasta onde você salvou o script. Por exemplo, se você salvou às C:\PS-Scripts, você faria execute o seguinte comando.</br>
  `cd C:\PS-Scripts`

3. Execute o seguinte comando para identificar o grupo que você deseja obter os detalhes do dispositivo para. Este exemplo obtém detalhes para os usuários no grupo FinanceStaff.</br>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. Execute o seguinte comando para iniciar o script.</br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

As informações são exportadas para sua área de trabalho do Windows como um arquivo CSV. Você pode usar os parâmetros adicionais para especificar o nome do arquivo e caminho do CSV.
  
## <a name="more-info"></a>Mais informações

[Visão geral do MDM para o Office 365](overview-of-mdm.md)
  
[Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)
  

