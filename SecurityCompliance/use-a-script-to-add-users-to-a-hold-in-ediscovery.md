---
title: Usar um script para adicionar usuários a uma isenção um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Executar um script para adicionar rapidamente caixas de correio e sites do OneDrive for Business para uma nova isenção que está associado a um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade.
ms.openlocfilehash: 2c93deb14bc8c1f89dab7bb054d2e94db06cfbd5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038254"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Usar um script para adicionar usuários a uma isenção um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade

A segurança do Office 365 &amp; Centro de conformidade fornece muitos dos cmdlets do Windows PowerShell que permitem que você automatizam tarefas demoradas relacionadas à criação e gerenciamento de casos de eDiscovery. Atualmente, usando a ferramenta de casos de eDiscovery na segurança &amp; Centro de conformidade para colocar um grande número de locais de conteúdo dos responsáveis em espera leva tempo e preparação. Por exemplo, antes de criar uma isenção, você precisa coletar a URL para cada OneDrive para site de negócios que você deseja colocar em espera. Em seguida, para cada usuário que você deseja colocar em espera, você precisará adicionar suas caixas de correio e seu OneDrive para o site de negócios à isenção. Em futuras versões da segurança &amp; Centro de conformidade, isso receberá mais fácil fazer. Enquanto isso, você pode usar o script neste artigo para automatizar esse processo.
  
O script solicita o nome do domínio de meusite da sua organização (por exemplo, **contoso** na URL https://contoso-my.sharepoint.com), o nome de um caso de descoberta eletrônica existente, o nome da nova isenção que associados com o caso, uma lista de endereços de email dos usuários que você deseja para colocar em espera e uma consulta de pesquisa a ser usado se você deseja criar uma pausa baseado em consulta. O script então obtém a URL do OneDrive para site de negócios para cada usuário na lista, cria um nova isenção e, em seguida, adiciona a caixa de correio e OneDrive para site de negócios para cada usuário na lista à isenção. O script também gera arquivos de log que contêm informações sobre a nova isenção. 
  
Aqui estão as etapas para fazer isso acontecer:
  
[Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[Etapa 2: Gerar uma lista de usuários](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Etapa 3: Executar o script para criar uma pausa e adicionar usuários](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade e um administrador global do SharePoint Online para executar o script na etapa 3. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
    
- Um máximo de 1.000 caixas de correio e 100 sites pode ser adicionado a uma isenção que está associado a um caso de eDiscovery na segurança &amp; Centro de conformidade. Supondo que cada usuário que você deseja colocar em espera tenha um OneDrive para o site de negócios, você pode adicionar um máximo de 100 usuários a uma isenção usando o script neste artigo. 
    
- Certifique-se de salvar a lista de usuários que você criar na etapa 2 e o script na etapa 3 para a mesma pasta. Será que tornam mais fácil executar o script.
    
- O script adiciona a lista de usuários a uma isenção nova que está associada um caso existente. Certifique-se de que o caso em que você deseja associar a suspensão com é criado antes de executar o script.
    
- O script inclui o tratamento de erros mínimas. Seu objetivo principal é modo rápido e fácil colocar a caixa de correio e OneDrive para site de negócios de cada usuário em espera.
    
- Os scripts de exemplo fornecidos neste tópico não são compatíveis com nenhum serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos COMO ESTÃO sem qualquer tipo de garantia. A Microsoft também se isenta de todas as garantias implícitas, incluindo sem limitações quaisquer garantias aplicáveis de padrões de comercialização ou de adequação a uma finalidade específica. Todos os riscos decorrentes do uso ou da execução da documentação ou scripts de exemplo serão de sua responsabilidade. De modo algum a Microsoft, seus autores ou qualquer outra pessoa envolvida na criação, produção ou veiculação dos scripts serão considerados responsáveis por quaisquer danos (incluindo sem limitações danos por perda de lucros comerciais, interrupção de negócios, perda de informações comerciais ou outras perdas pecuniárias) resultantes do uso ou da incapacidade de uso da documentação ou scripts de exemplo, mesmo que a Microsoft tenha sido alertada sobre a possibilidade de tais danos.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online

A primeira etapa é instalar o Shell de gerenciamento do SharePoint Online, caso ele ainda não esteja instalado no computador local. Você não precisa usar o shell neste procedimento, mas você precisa instalá-lo, pois ele contém pré-requisitos necessários para o script que você pode executar na etapa 3. Esses pré-requisitos permitem que o script para se comunicar com o SharePoint Online para obter as URLs para o OneDrive for sites corporativos.
  
Vá para [Configurar o ambiente do SharePoint Online Management Shell do Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) e executar a etapa 1 e a etapa 2 para instalar o Shell de gerenciamento do SharePoint Online no computador local. 

## <a name="step-2-generate-a-list-of-users"></a>Etapa 2: Gerar uma lista de usuários
<a name="step2"> </a>

O script na etapa 3 criará uma isenção associado a um caso de eDiscovery e adicionar caixas de correio e OneDrive para sites de negócios de uma lista de usuários à isenção. Você pode apenas digitar os endereços de email em um arquivo de texto, ou você pode executar um comando do Windows PowerShell para obter uma lista de endereços de email e salvá-los em um arquivo (localizado na mesma pasta que você vai salvar o script na etapa 3).
  
Aqui está um comando do PowerShell (isto é executado usando o PowerShell remoto conectado à sua organização do Exchange Online) obter uma lista de endereços de email de todos os usuários em sua organização e salvá-lo em um arquivo de texto denominada HoldUsers.txt.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

Depois de executar esse comando, abra o arquivo de texto e remover o cabeçalho que contém o nome da propriedade, `PrimarySmtpAddress`. Remova todos os endereços de email, exceto aqueles para os usuários que você deseja adicionar à isenção que você vai criar na etapa 3. Verifique não se que há nenhuma linha em branco antes ou depois da lista de endereços de email.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Etapa 3: Executar o script para criar uma pausa e adicionar usuários
<a name="step3"> </a>

Quando você executar o script nesta etapa, ele solicitará para as informações a seguir. Certifique-se de ter essas informações prontas antes de executar o script.
  
- **Suas credenciais de usuário** - o script usarão suas credenciais para se conectar à segurança &amp; Centro de conformidade com o PowerShell remoto. Além disso, ele usará essas credenciais para acessar o SharePoint Online para obter o OneDrive para Business URLs para a lista de usuários.
    
- **Nome do seu domínio meusite** - meusite o domínio é o domínio que contém todos os OneDrive para sites corporativos em sua organização. Por exemplo, se a URL do seu domínio meusite for **https://contoso-my.sharepoint.com**, e em seguida, você digitaria `contoso` quando o script solicita o nome do seu domínio do meu site. 
    
- **Nome do caso** - o nome de um caso existente. O script criará uma nova isenção que está associada esse caso.
    
- **Nome da isenção** - o nome da isenção o script criará e associar o caso especificado.
    
- **Mantenha a consulta de pesquisa para um baseado em consulta** - você pode criar uma isenção baseado em consulta para que apenas o conteúdo que satisfaz os critérios de pesquisa especificado é colocado em espera. Para colocar todo o conteúdo em espera, basta pressione **Enter** quando você for solicitado para uma consulta de pesquisa. 
    
- **Se deseja ou não ativar a suspensão** - você pode ter o script ativem o bloqueio depois que ele é criado ou você pode ter o script criar isenção sem ativá-lo. Se você não tiver o script ativem o bloqueio, você pode ativá-la mais tarde na segurança &amp; Centro de conformidade ou executando os seguintes comandos do PowerShell: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **Nome do arquivo de texto com a lista de usuários** - o nome do arquivo de texto da etapa 2 que contém a lista de usuários para adicionar à isenção. Se esse arquivo está localizado na mesma pasta que o script, basta digite o nome do arquivo (por exemplo, HoldUsers.txt). Se o arquivo de texto está em outra pasta, digite o nome do caminho completo do arquivo.
    
Depois que você coletou as informações que o script solicitará que você forneça, a etapa final é executar o script para criar a nova isenção e adicionar usuários a ele.
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `AddUsersToHold.ps1`.
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Office 365 Security &amp; Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Office 365 Security &amp; Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
      }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to http://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.
    
3. Executar o script; Por exemplo:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Insira as informações que o script solicita.
    
    O script conecta-se à segurança & PowerShell do Centro de conformidade e cria um nova isenção no caso de descoberta eletrônica e adiciona a caixas de correio e o OneDrive for Business para os usuários na lista. Você pode ir para o caso, na página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade para exibir a nova isenção. 
    
Depois que o script é concluído em execução, ele cria os seguintes arquivos de log e salva-los na pasta onde o script está localizado.
  
- **LocationsOnHold.txt** - contém uma lista de caixas de correio e OneDrive para sites de negócios que o script com êxito colocado em espera.
    
- **LocationsNotOnHold.txt** - contém uma lista de caixas de correio e OneDrive para sites de negócios que o script não colocou em espera. Se um usuário tem uma caixa de correio, mas não uma OneDrive para o site de negócios, o usuário seria incluído na lista de OneDrive para sites corporativos que não foram colocados em espera.
    
- **GetCaseHoldPolicy.txt** - contém a saída do cmdlet **Get-CaseHoldPolicy** para a nova isenção, o script foi executado após a criação de nova isenção. As informações retornadas por esse cmdlet incluem uma lista de usuários cujas caixas de correio e OneDrive para sites corporativos foram colocados em espera e a retenção habilitada ou desabilitada. 
    
- **GetCaseHoldRule.txt** - contém a saída do cmdlet **Get-CaseHoldRule** para a nova isenção, o script foi executado após a criação de nova isenção. As informações retornadas por esse cmdlet incluem a consulta de pesquisa, se você tiver usado o script para criar uma pausa baseado em consulta. 
