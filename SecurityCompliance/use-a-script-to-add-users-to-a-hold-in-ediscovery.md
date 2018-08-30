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
- MET150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Executar um script para adicionar rapidamente caixas de correio e sites do OneDrive for Business para uma nova isenção que está associado a um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade.
ms.openlocfilehash: eb53f01b4f1b7245e1411ac470db629115eb1ef5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523974"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="ac6a5-103">Usar um script para adicionar usuários a uma isenção um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="ac6a5-103">Use a script to add users to a hold in an eDiscovery case in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="ac6a5-p101">A segurança do Office 365 &amp; Centro de conformidade fornece muitos dos cmdlets do Windows PowerShell que permitem que você automatizam tarefas demoradas relacionadas à criação e gerenciamento de casos de eDiscovery. Atualmente, usando a ferramenta de casos de eDiscovery na segurança &amp; Centro de conformidade para colocar um grande número de locais de conteúdo dos responsáveis em espera leva tempo e preparação. Por exemplo, antes de criar uma isenção, você precisa coletar a URL para cada OneDrive para site de negócios que você deseja colocar em espera. Em seguida, para cada usuário que você deseja colocar em espera, você precisará adicionar suas caixas de correio e seu OneDrive para o site de negócios à isenção. Em futuras versões da segurança &amp; Centro de conformidade, isso receberá mais fácil fazer. Enquanto isso, você pode usar o script neste artigo para automatizar esse processo.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p101">The Office 365 Security &amp; Compliance Center provides lots of Windows PowerShell cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases. Currently, using the eDiscovery case tool in the Security &amp; Compliance Center to place a large number of custodian content locations on hold takes time and preparation. For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold. Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold. In future releases of the Security &amp; Compliance Center, this will get easier to do. Until then, you can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="ac6a5-p102">O script solicita o nome do domínio de meusite da sua organização (por exemplo, **contoso** na URL https://contoso-my.sharepoint.com), o nome de um caso de descoberta eletrônica existente, o nome da nova isenção que associados com o caso, uma lista de endereços de email dos usuários que você deseja para colocar em espera e uma consulta de pesquisa a ser usado se você deseja criar uma pausa baseado em consulta. O script então obtém a URL do OneDrive para site de negócios para cada usuário na lista, cria um nova isenção e, em seguida, adiciona a caixa de correio e OneDrive para site de negócios para cada usuário na lista à isenção. O script também gera arquivos de log que contêm informações sobre a nova isenção.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p102">The script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold. The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold. The script also generates log files that contain information about the new hold.</span></span> 
  
<span data-ttu-id="ac6a5-113">Aqui estão as etapas para fazer isso acontecer:</span><span class="sxs-lookup"><span data-stu-id="ac6a5-113">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="ac6a5-114">Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ac6a5-114">Step 1: Install the SharePoint Online Management Shell</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[<span data-ttu-id="ac6a5-115">Etapa 2: Gerar uma lista de usuários</span><span class="sxs-lookup"><span data-stu-id="ac6a5-115">Step 2: Generate a list of users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[<span data-ttu-id="ac6a5-116">Etapa 3: Executar o script para criar uma pausa e adicionar usuários</span><span class="sxs-lookup"><span data-stu-id="ac6a5-116">Step 3: Run the script to create a hold and add users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a><span data-ttu-id="ac6a5-117">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="ac6a5-117">Before you begin</span></span>

- <span data-ttu-id="ac6a5-p103">Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade e um administrador global do SharePoint Online para executar o script na etapa 3. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="ac6a5-p104">Um máximo de 1.000 caixas de correio e 100 sites pode ser adicionado a uma isenção que está associado a um caso de eDiscovery na segurança &amp; Centro de conformidade. Supondo que cada usuário que você deseja colocar em espera tenha um OneDrive para o site de negócios, você pode adicionar um máximo de 100 usuários a uma isenção usando o script neste artigo.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p104">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security &amp; Compliance Center. Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span> 
    
- <span data-ttu-id="ac6a5-p105">Certifique-se de salvar a lista de usuários que você criar na etapa 2 e o script na etapa 3 para a mesma pasta. Será que tornam mais fácil executar o script.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p105">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="ac6a5-p106">O script adiciona a lista de usuários a uma isenção nova que está associada um caso existente. Certifique-se de que o caso em que você deseja associar a suspensão com é criado antes de executar o script.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p106">The script adds the list of users to a new hold that is associated with an existing case. Be sure the case that you want to associate the hold with is created before you run the script.</span></span>
    
- <span data-ttu-id="ac6a5-p107">O script inclui o tratamento de erros mínimas. Seu objetivo principal é modo rápido e fácil colocar a caixa de correio e OneDrive para site de negócios de cada usuário em espera.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p107">The script includes minimal error handling. Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>
    
- <span data-ttu-id="ac6a5-p108">Os scripts de exemplo fornecidos neste tópico não são suportados em qualquer serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos que se encontra, sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho dos scripts de amostra e documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p108">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="ac6a5-133">Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ac6a5-133">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="ac6a5-p109">A primeira etapa é instalar o Shell de gerenciamento do SharePoint Online, caso ele ainda não esteja instalado no computador local. Você não precisa usar o shell neste procedimento, mas você precisa instalá-lo, pois ele contém pré-requisitos necessários para o script que você pode executar na etapa 3. Esses pré-requisitos permitem que o script para se comunicar com o SharePoint Online para obter as URLs para o OneDrive for sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p109">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="ac6a5-137">Vá para [Configurar o ambiente do SharePoint Online Management Shell do Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) e executar a etapa 1 e a etapa 2 para instalar o Shell de gerenciamento do SharePoint Online no computador local.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-137">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span> 

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="ac6a5-138">Etapa 2: Gerar uma lista de usuários</span><span class="sxs-lookup"><span data-stu-id="ac6a5-138">Step 2: Generate a list of users</span></span>
<span data-ttu-id="ac6a5-139"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="ac6a5-139"></span></span>

<span data-ttu-id="ac6a5-p110">O script na etapa 3 criará uma isenção associado a um caso de eDiscovery e adicionar caixas de correio e OneDrive para sites de negócios de uma lista de usuários à isenção. Você pode apenas digitar os endereços de email em um arquivo de texto, ou você pode executar um comando do Windows PowerShell para obter uma lista de endereços de email e salvá-los em um arquivo (localizado na mesma pasta que você vai salvar o script na etapa 3).</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p110">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="ac6a5-142">Aqui está um comando do PowerShell (isto é executado usando o PowerShell remoto conectado à sua organização do Exchange Online) obter uma lista de endereços de email de todos os usuários em sua organização e salvá-lo em um arquivo de texto denominada HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-142">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="ac6a5-p111">Depois de executar esse comando, abra o arquivo de texto e remover o cabeçalho que contém o nome da propriedade, `PrimarySmtpAddress`. Remova todos os endereços de email, exceto aqueles para os usuários que você deseja adicionar à isenção que você vai criar na etapa 3. Verifique não se que há nenhuma linha em branco antes ou depois da lista de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p111">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`. Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="ac6a5-146">Etapa 3: Executar o script para criar uma pausa e adicionar usuários</span><span class="sxs-lookup"><span data-stu-id="ac6a5-146">Step 3: Run the script to create a hold and add users</span></span>
<span data-ttu-id="ac6a5-147"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="ac6a5-147"></span></span>

<span data-ttu-id="ac6a5-p112">Quando você executar o script nesta etapa, ele solicitará para as informações a seguir. Certifique-se de ter essas informações prontas antes de executar o script.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p112">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="ac6a5-p113">**Suas credenciais de usuário** - o script usarão suas credenciais para se conectar à segurança &amp; Centro de conformidade com o PowerShell remoto. Além disso, ele usará essas credenciais para acessar o SharePoint Online para obter o OneDrive para Business URLs para a lista de usuários.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p113">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center with remote PowerShell. It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>
    
- <span data-ttu-id="ac6a5-p114">**Nome do seu domínio meusite** - meusite o domínio é o domínio que contém todos os OneDrive para sites corporativos em sua organização. Por exemplo, se a URL do seu domínio meusite for **https://contoso-my.sharepoint.com**, e em seguida, você digitaria `contoso` quando o script solicita o nome do seu domínio do meu site.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p114">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="ac6a5-p115">**Nome do caso** - o nome de um caso existente. O script criará uma nova isenção que está associada esse caso.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p115">**Name of the case** - The name of an existing case. The script will create a new hold that is associated with this case.</span></span>
    
- <span data-ttu-id="ac6a5-156">**Nome da isenção** - o nome da isenção o script criará e associar o caso especificado.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-156">**Name of the hold** - The name of the hold the script will create and associate with the specified case.</span></span>
    
- <span data-ttu-id="ac6a5-p116">**Mantenha a consulta de pesquisa para um baseado em consulta** - você pode criar uma isenção baseado em consulta para que apenas o conteúdo que satisfaz os critérios de pesquisa especificado é colocado em espera. Para colocar todo o conteúdo em espera, basta pressione **Enter** quando você for solicitado para uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p116">**Search query for a query-based hold** - You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold. To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span> 
    
- <span data-ttu-id="ac6a5-p117">**Se deseja ou não ativar a suspensão** - você pode ter o script ativem o bloqueio depois que ele é criado ou você pode ter o script criar isenção sem ativá-lo. Se você não tiver o script ativem o bloqueio, você pode ativá-la mais tarde na segurança &amp; Centro de conformidade ou executando os seguintes comandos do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p117">**Whether or not to turn the hold on** - You can have the script turn the hold on after it's created or you can have the script create the hold without enabling it. If you don't have the script turn on the hold, you can turn it on later in the Security &amp; Compliance Center or by running the following PowerShell commands:</span></span> 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="ac6a5-p118">**Nome do arquivo de texto com a lista de usuários** - o nome do arquivo de texto da etapa 2 que contém a lista de usuários para adicionar à isenção. Se esse arquivo está localizado na mesma pasta que o script, basta digite o nome do arquivo (por exemplo, HoldUsers.txt). Se o arquivo de texto está em outra pasta, digite o nome do caminho completo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p118">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold. If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt). If the text file is in another folder, type the full pathname of the file.</span></span>
    
<span data-ttu-id="ac6a5-164">Depois que você coletou as informações que o script solicitará que você forneça, a etapa final é executar o script para criar a nova isenção e adicionar usuários a ele.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-164">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="ac6a5-165">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `AddUsersToHold.ps1`.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-165">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `AddUsersToHold.ps1`.</span></span>
    
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

2. <span data-ttu-id="ac6a5-166">No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-166">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="ac6a5-167">Executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ac6a5-167">Run the script; for example:</span></span>
    
      ```
    .\AddUsersToHold.ps1
      ```

4. <span data-ttu-id="ac6a5-168">Insira as informações que o script solicita.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-168">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="ac6a5-p119">O script conecta-se à segurança & PowerShell do Centro de conformidade e cria um nova isenção no caso de descoberta eletrônica e adiciona a caixas de correio e o OneDrive for Business para os usuários na lista. Você pode ir para o caso, na página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade para exibir a nova isenção.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p119">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list. You can go to the case on the **eDiscovery** page in the Security &amp; Compliance Center to view the new hold.</span></span> 
    
<span data-ttu-id="ac6a5-171">Depois que o script é concluído em execução, ele cria os seguintes arquivos de log e salva-los na pasta onde o script está localizado.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-171">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="ac6a5-172">**LocationsOnHold.txt** - contém uma lista de caixas de correio e OneDrive para sites de negócios que o script com êxito colocado em espera.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-172">**LocationsOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>
    
- <span data-ttu-id="ac6a5-p120">**LocationsNotOnHold.txt** - contém uma lista de caixas de correio e OneDrive para sites de negócios que o script não colocou em espera. Se um usuário tem uma caixa de correio, mas não uma OneDrive para o site de negócios, o usuário seria incluído na lista de OneDrive para sites corporativos que não foram colocados em espera.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p120">**LocationsNotOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold. If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>
    
- <span data-ttu-id="ac6a5-p121">**GetCaseHoldPolicy.txt** - contém a saída do cmdlet **Get-CaseHoldPolicy** para a nova isenção, o script foi executado após a criação de nova isenção. As informações retornadas por esse cmdlet incluem uma lista de usuários cujas caixas de correio e OneDrive para sites corporativos foram colocados em espera e a retenção habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p121">**GetCaseHoldPolicy.txt** - Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 
    
- <span data-ttu-id="ac6a5-p122">**GetCaseHoldRule.txt** - contém a saída do cmdlet **Get-CaseHoldRule** para a nova isenção, o script foi executado após a criação de nova isenção. As informações retornadas por esse cmdlet incluem a consulta de pesquisa, se você tiver usado o script para criar uma pausa baseado em consulta.</span><span class="sxs-lookup"><span data-stu-id="ac6a5-p122">**GetCaseHoldRule.txt** - Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span> 
