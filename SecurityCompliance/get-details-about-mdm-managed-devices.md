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
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="4c7b6-103">Obter detalhes sobre os dispositivos gerenciados pelo Mobile Device Management (MDM) para o Office 365</span><span class="sxs-lookup"><span data-stu-id="4c7b6-103">Get details about devices managed by Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="4c7b6-104">Este artigo mostra como usar o Windows PowerShell para obter detalhes sobre os dispositivos em sua organização que você definiu para gerenciamento de dispositivos móveis para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Mobile Device Management for Office 365.</span></span> 
  
## <a name="what-device-details-can-i-get"></a><span data-ttu-id="4c7b6-105">Os detalhes do dispositivo que pode fazer?</span><span class="sxs-lookup"><span data-stu-id="4c7b6-105">What device details can I get?</span></span>

<span data-ttu-id="4c7b6-106">Aqui está uma divisão.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-106">Here's a breakdown.</span></span>
  
|<span data-ttu-id="4c7b6-107">**Detalhes**</span><span class="sxs-lookup"><span data-stu-id="4c7b6-107">**Detail**</span></span>|<span data-ttu-id="4c7b6-108">**O que procurar no PowerShell**</span><span class="sxs-lookup"><span data-stu-id="4c7b6-108">**What to look for in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c7b6-109">O dispositivo está [inscrito no MDM para o Office 365](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="4c7b6-109">Device is [enrolled in MDM for Office 365](enroll-your-mobile-device.md)</span></span> <br/> |<span data-ttu-id="4c7b6-110">O valor do parâmetro *isManaged* é:</span><span class="sxs-lookup"><span data-stu-id="4c7b6-110">The value of the  *isManaged*  parameter is:</span></span>  <br/> <span data-ttu-id="4c7b6-111">**True** = dispositivo está inscrito.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-111">**True** = device is enrolled.</span></span>  <br/> <span data-ttu-id="4c7b6-112">**False** = dispositivo não está inscrito.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-112">**False** = device is not enrolled.</span></span>  <br/> |
|<span data-ttu-id="4c7b6-113">O dispositivo está em conformidade com suas [políticas de segurança de dispositivo](https://go.microsoft.com/fwlink/?linkid=615144)</span><span class="sxs-lookup"><span data-stu-id="4c7b6-113">Device is compliant with your [device security policies](https://go.microsoft.com/fwlink/?linkid=615144)</span></span> <br/> |<span data-ttu-id="4c7b6-114">O valor do parâmetro *isCompliant* é:</span><span class="sxs-lookup"><span data-stu-id="4c7b6-114">The value of the  *isCompliant*  parameter is:</span></span>  <br/> <span data-ttu-id="4c7b6-115">**True** = dispositivo está em conformidade com políticas.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-115">**True** = device is compliant with policies.</span></span>  <br/> <span data-ttu-id="4c7b6-116">**False** = dispositivo não é compatível com políticas.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-116">**False** = device is not compliant with policies.</span></span>  <br/> |
   
![Fluxo mostrando valores de param de AAD Shell para se os dispositivos serão inscritos e reclamações](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> <span data-ttu-id="4c7b6-118">Os comandos e scripts neste artigo também retornará detalhes sobre todos os dispositivos que são gerenciados pelo [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="4c7b6-118">The commands and scripts in this article will also return details about any devices that are managed by [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="4c7b6-119">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="4c7b6-119">Before you begin</span></span>

<span data-ttu-id="4c7b6-120">Há algumas coisas que você precisará configurado para executar os comandos e scripts descritos neste artigo.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-120">There are a few things you'll need to set up to run the commands and scripts described in this article.</span></span>
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="4c7b6-121">Etapa 1: Baixar e instalar o Windows Azure Active Directory módulo para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c7b6-121">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="4c7b6-122">Para obter mais informações sobre essas etapas, consulte [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="4c7b6-122">For more info on these steps, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>
  
1. <span data-ttu-id="4c7b6-123">Vá para o [Assistente Microsoft Online Services entrar para RTWl de profissionais de TI](https://www.microsoft.com/en-us/download/details.aspx?id=41950) e clique em **Download** para o Assistente de entrada do Microsoft Online Services.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-123">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) and click **Download** for Microsoft Online Services Sign-in Assistant.</span></span> 
    
2. <span data-ttu-id="4c7b6-124">Instale o Módulo Microsoft Azure Active Directory para Windows PowerShell seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="4c7b6-124">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>
    
    1. <span data-ttu-id="4c7b6-125">Abra um prompt de comando do PowerShell do nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-125">Open an administrator-level PowerShell command prompt.</span></span>
        
    2. <span data-ttu-id="4c7b6-126">Execute o `Install-Module MSOnline` comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-126">Run the `Install-Module MSOnline` command.</span></span>
        
    3. <span data-ttu-id="4c7b6-127">Se solicitado a instalar o provedor NuGet, digite `Y` e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-127">If prompted to install the NuGet provider, type `Y` and press ENTER.</span></span>
        
    4. <span data-ttu-id="4c7b6-128">Se solicitado a instalar o módulo de PSGallery, digite `Y` e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-128">If prompted to install the module from PSGallery, type `Y` and press ENTER.</span></span>
        
    5. <span data-ttu-id="4c7b6-129">Após a instalação, feche a janela de comando do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-129">After installation, close the PowerShell command window.</span></span>
    
### <a name="step-2-connect-to-your-office-365-subscription"></a><span data-ttu-id="4c7b6-130">Etapa 2: conectar-se à sua assinatura do Office 365</span><span class="sxs-lookup"><span data-stu-id="4c7b6-130">Step 2: Connect to your Office 365 subscription</span></span>

1. <span data-ttu-id="4c7b6-131">Em que o Windows Azure Active Directory módulo para Windows PowerShell, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-131">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span></br>  
  `$UserCredential = Get-Credential`

2. <span data-ttu-id="4c7b6-132">Na caixa de diálogo **Solicitação de credencial do Windows PowerShell** , digite o nome de usuário e a senha da sua conta de administrador global do Office 365 e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-132">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="4c7b6-133">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-133">Run the following command.</span></span></br>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="4c7b6-134">Etapa 3: Verifique se que você está possibilidade de executar scripts do PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c7b6-134">Step 3: Make sure you're able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="4c7b6-135">Você pode ignorar esta etapa se você já estiver configurado para executar scripts do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-135">You can skip this step if you're already set up to run PowerShell scripts.</span></span> 
  
<span data-ttu-id="4c7b6-136">Para executar o script **Get-MsolUserDeviceComplianceStatus.ps1** , você precisa habilitar a execução de scripts do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-136">To run the **Get-MsolUserDeviceComplianceStatus.ps1** script, you need to enable the running of PowerShell scripts.</span></span> 
  
1. <span data-ttu-id="4c7b6-p101">Da sua área de trabalho do Windows, clique em **Iniciar**e, em seguida, digite o Windows PowerShell. Clique com botão direito **Do Windows PowerShell**e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p101">From your Windows Desktop, click **Start**, and then type Windows PowerShell. Right click **Windows PowerShell**, and then click **Run as administrator**.</span></span>
    
2. <span data-ttu-id="4c7b6-139">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-139">Run the following command.</span></span></br>
  `Set-ExecutionPolicy RemoteSigned`

3. <span data-ttu-id="4c7b6-140">Quando solicitado, digite `Y` e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-140">When prompted, type `Y` and then press Enter.</span></span> 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="4c7b6-141">Execute o cmdlet Get-MsolDevice para exibir os detalhes para todos os dispositivos em sua organização</span><span class="sxs-lookup"><span data-stu-id="4c7b6-141">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="4c7b6-142">Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-142">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="4c7b6-143">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-143">Run the following command.</span></span></br>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

<span data-ttu-id="4c7b6-144">Para obter mais exemplos, consulte [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span><span class="sxs-lookup"><span data-stu-id="4c7b6-144">For more examples, see [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span></span>
  
## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="4c7b6-145">Executar um script para obter detalhes do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4c7b6-145">Run a script to get device details</span></span>

### <a name="first-save-the-script-to-your-computer"></a><span data-ttu-id="4c7b6-146">Primeiro, salve o script em seu computador</span><span class="sxs-lookup"><span data-stu-id="4c7b6-146">First, save the script to your computer</span></span>

1. <span data-ttu-id="4c7b6-147">Copie e cole o seguinte texto no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-147">Copy and paste the following text into Notepad.</span></span></br> 
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

2. <span data-ttu-id="4c7b6-148">Salve-o como um arquivo de script do Windows PowerShell, usando a extensão de arquivo **. ps1**.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-148">Save it as a Windows PowerShell script file by using the file extension **.ps1**.</span></span> </br><span data-ttu-id="4c7b6-149">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="4c7b6-149">Example:</span></span></br> <span data-ttu-id="4c7b6-150">`Get-MsolUserDeviceComplianceStatus.ps1`.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-150"></span></span>
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="4c7b6-151">Execute o script para obter informações do dispositivo para uma conta de usuário único</span><span class="sxs-lookup"><span data-stu-id="4c7b6-151">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="4c7b6-152">Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-152">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="4c7b6-p102">Navegue até a pasta onde você salvou o script. Por exemplo, se você salvou às C:\PS-Scripts, você faria execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p102">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
    `cd C:\PS-Scripts`

3. <span data-ttu-id="4c7b6-p103">Execute o seguinte comando para identificar o usuário que você deseja obter os detalhes do dispositivo para. Este exemplo obtém detalhes para bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p103">Run the following command to identify the user you want to get device details for. This example gets details for bar@example.com.</span></span></br>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. <span data-ttu-id="4c7b6-157">Execute o seguinte comando para iniciar o script.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-157">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="4c7b6-p104">As informações são exportadas para sua área de trabalho do Windows como um arquivo CSV. Você pode usar os parâmetros adicionais para especificar o nome do arquivo e caminho do CSV.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p104">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="4c7b6-160">Execute o script para obter informações do dispositivo para um grupo de usuários</span><span class="sxs-lookup"><span data-stu-id="4c7b6-160">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="4c7b6-161">Abra o Módulo Microsoft Azure Active Directory para Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-161">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="4c7b6-p105">Navegue até a pasta onde você salvou o script. Por exemplo, se você salvou às C:\PS-Scripts, você faria execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p105">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
  `cd C:\PS-Scripts`

3. <span data-ttu-id="4c7b6-p106">Execute o seguinte comando para identificar o grupo que você deseja obter os detalhes do dispositivo para. Este exemplo obtém detalhes para os usuários no grupo FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p106">Run the following command to identify the group you want to get device details for. This example gets details for users in the FinanceStaff group.</span></span></br>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. <span data-ttu-id="4c7b6-166">Execute o seguinte comando para iniciar o script.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-166">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="4c7b6-p107">As informações são exportadas para sua área de trabalho do Windows como um arquivo CSV. Você pode usar os parâmetros adicionais para especificar o nome do arquivo e caminho do CSV.</span><span class="sxs-lookup"><span data-stu-id="4c7b6-p107">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
## <a name="more-info"></a><span data-ttu-id="4c7b6-169">Mais informações</span><span class="sxs-lookup"><span data-stu-id="4c7b6-169">More info</span></span>

[<span data-ttu-id="4c7b6-170">Visão geral do MDM para o Office 365</span><span class="sxs-lookup"><span data-stu-id="4c7b6-170">Overview of MDM for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="4c7b6-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="4c7b6-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=841721)
  

