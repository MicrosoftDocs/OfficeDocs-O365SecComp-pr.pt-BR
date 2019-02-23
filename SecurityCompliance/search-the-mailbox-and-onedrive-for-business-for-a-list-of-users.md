---
title: Usar a Pesquisa de Conteúdo para pesquisar na caixa de correio e no site do OneDrive for Business para obter uma lista de usuários
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Use a pesquisa de conteúdo e o script neste artigo para pesquisar as caixas de correio e os sites do OneDrive for Business para um grupo de usuários.
ms.openlocfilehash: 758c9b9e756f6830f207b76392ad808fc14f0caa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218881"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="d8e17-103">Usar a Pesquisa de Conteúdo para pesquisar na caixa de correio e no site do OneDrive for Business para obter uma lista de usuários</span><span class="sxs-lookup"><span data-stu-id="d8e17-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="d8e17-p101">O centro de conformidade &amp; de segurança do Office 365 fornece vários cmdlets do Windows PowerShell que permitem automatizar tarefas relacionadas a descoberta eletrônica demoradas. Atualmente, criar uma pesquisa de conteúdo no centro &amp; de conformidade de segurança para pesquisar um grande número de locais de conteúdo dos responsáveis leva tempo e preparação. Antes de criar uma pesquisa, você precisa coletar a URL de cada site do OneDrive for Business e, em seguida, adicionar cada caixa de correio e O neDrive para o site de negócios à pesquisa. Em versões futuras, isso será mais fácil de fazer no centro de &amp; conformidade de segurança. Até lá, você pode usar o script neste artigo para automatizar esse processo. Esse script solicita o nome do domínio meusite da sua organização (por exemplo, **contoso** na URL https://contoso-my.sharepoint.com), uma lista de endereços de email do usuário, o nome da nova pesquisa de conteúdo e a consulta de pesquisa a ser usada. O script Obtém a URL do OneDrive for Business para cada usuário na lista e, em seguida, cria e inicia uma pesquisa de conteúdo que pesquisa a caixa de correio e o site do OneDrive for Business para cada usuário na lista, usando a consulta de pesquisa que você fornece.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p101">The Office 365 Security &amp; Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks. Currently, creating a Content Search in the Security &amp; Compliance Center to search a large number of custodian content locations takes time and preparation. Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and O neDrive for Business site to the search. In future releases, this will be easier to do in the Security &amp; Compliance Center. Until then, you can use the script in this article to automate this process. This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), a list of user email addresses, the name of the new Content Search, and the search query to use. The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="d8e17-111">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="d8e17-111">Before you begin</span></span>

- <span data-ttu-id="d8e17-112">Você precisa ser membro do grupo de função Gerenciador de descoberta eletrônica no centro de &amp; conformidade de segurança e um administrador global do SharePoint Online para executar o script na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="d8e17-112">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>
    
- <span data-ttu-id="d8e17-p102">Certifique-se de salvar a lista de usuários que você criou na etapa 2 e o script na etapa 3 para a mesma pasta. Isso facilitará a execução do script.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p102">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="d8e17-p103">O script inclui o tratamento de erros mínimo. O objetivo principal é Pesquisar rápida e facilmente a caixa de correio e o site do OneDrive for Business de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p103">The script includes minimal error handling. It's primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>
    
- <span data-ttu-id="d8e17-p104">Os scripts de exemplo fornecidos neste tópico não são suportados em nenhum programa ou serviço de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos como estão sem garantia de qualquer tipo. A Microsoft se isenta de[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)todas as garantias mplied, incluindo, sem limitação, quaisquer garantias implícitas de comercialização ou ADEQÜAÇÃO para um propósito específico. Todo o risco resultante do uso ou do desempenho dos scripts de exemplo e da documentação permanece com você. Em hipótese alguma a Microsoft, seus autores ou qualquer outra pessoa envolvida na criação, produção ou entrega dos scripts serão responsáveis por qualquer dano (incluindo, sem limitação, danos à perda de lucros de negócios, interrupção de negócios, perda de informações comerciais ou outras perdas de pecuniary) resultantes do uso ou da incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido avisada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="d8e17-122">Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d8e17-122">Step 1: Install the SharePoint Online Management Shell</span></span>
<span data-ttu-id="d8e17-123"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="d8e17-123"></span></span>

<span data-ttu-id="d8e17-p105">A primeira etapa é instalar o Shell de gerenciamento do SharePoint Online. Não é necessário usar o Shell neste procedimento, mas você precisa instalá-lo porque ele contém pré-requisitos necessários para o script executado na etapa 3. Esses pré-requisitos permitem que o script se comunique com o SharePoint Online para obter as URLs para os sites do OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p105">The first step is to install the SharePoint Online Management Shell. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="d8e17-127">Vá para [Configurar o ambiente do Windows PowerShell do Shell de gerenciamento do SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkID=286318) e execute a etapa 1 e a etapa 2 para instalar o Shell de gerenciamento do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="d8e17-127">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="d8e17-128">Etapa 2: gerar uma lista de usuários</span><span class="sxs-lookup"><span data-stu-id="d8e17-128">Step 2: Generate a list of users</span></span>
<span data-ttu-id="d8e17-129"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="d8e17-129"></span></span>

<span data-ttu-id="d8e17-p106">O script na etapa 3 criará uma pesquisa de conteúdo para pesquisar as caixas de correio e as contas do OneDrive para uma lista de usuários. Você pode simplesmente digitar os endereços de email em um arquivo de texto ou pode executar um comando no Windows PowerShell para obter uma lista de endereços de email e salvá-los em um arquivo (localizado na mesma pasta em que você salvará o script na etapa 3).</span><span class="sxs-lookup"><span data-stu-id="d8e17-p106">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="d8e17-132">Este é um comando do [PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=517283) que você pode fazer com o Runt para obter uma lista de endereços de email para todos os usuários em sua organização e `Users.txt`salvá-lo em um arquivo de texto chamado.</span><span class="sxs-lookup"><span data-stu-id="d8e17-132">Here's an [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="d8e17-p107">Depois de executar esse comando, certifique-se de abrir o arquivo e remover o cabeçalho que contém o nome da `PrimarySmtpAddress`propriedade. O arquivo de texto deve conter apenas uma lista de endereços de email e nada mais. Certifique-se de que não haja linhas em branco antes ou depois da lista de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p107">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`. The text file should just contain a list of email addresses, and nothing else. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="d8e17-136">Etapa 3: executar o script para criar e iniciar a pesquisa</span><span class="sxs-lookup"><span data-stu-id="d8e17-136">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="d8e17-p108">Quando você executar o script nesta etapa, ele solicitará as seguintes informações. Certifique-se de ter essas informações prontas antes de executar o script.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p108">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="d8e17-139">**Suas credenciais de usuário** -o script usará suas credenciais para acessar o SharePoint Online para obter as URLs do onedrive for Business e se conectar &amp; ao centro de conformidade de segurança com o PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="d8e17-139">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security &amp; Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="d8e17-p109">**Nome do seu domínio meusite** -o domínio MeuSite é o domínio que contém todos os sites do onedrive for Business em sua organização. Por exemplo, se a URL do seu domínio meusite for **https://contoso-my.sharepoint.com**, você deve inserir `contoso` quando o script solicitar o nome do seu domínio meusite.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p109">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="d8e17-p110">**Nome do caminho do arquivo de texto da etapa 2** -o nome do caminho do arquivo de texto que você criou na etapa 2. Se o arquivo de texto e o script estiverem localizados na mesma pasta, insira o nome do arquivo de texto. Caso contrário, insira o nome de caminho completo para o arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p110">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2. If the text file and the script are located in the same folder, then enter the name of the text file. Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="d8e17-145">**Nome da pesquisa de conteúdo** -o nome da pesquisa de conteúdo que será criado pelo script.</span><span class="sxs-lookup"><span data-stu-id="d8e17-145">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="d8e17-p111">**Consulta de pesquisa** -a consulta de pesquisa que será usada com a pesquisa de conteúdo é criada e executada. Para obter mais informações sobre consultas de pesquisa, consulte [keyword queries and Search Conditions for Content Search](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="d8e17-p111">**Search query** - The search query that will be used with the Content Search is created and run. For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="d8e17-148">**Para executar o script:**</span><span class="sxs-lookup"><span data-stu-id="d8e17-148">**To run the script:**</span></span>
    
1. <span data-ttu-id="d8e17-p112">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `SearchEXOOD4B.ps1`. Salve o arquivo na mesma pasta onde você salvou a lista de usuários na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p112">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`. Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
  ```
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
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
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
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
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. <span data-ttu-id="d8e17-151">Abra o Windows PowerShell e vá para a pasta onde você salvou o script e a lista de usuários da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d8e17-151">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="d8e17-152">Inicie o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8e17-152">Start the script; for example:</span></span>
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="d8e17-153">Quando solicitar suas credenciais, insira seu endereço de email e senha e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8e17-153">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="d8e17-p113">Insira as informações a seguir quando solicitado pelo script. Digite cada informação e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p113">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="d8e17-156">O nome do seu domínio meusite.</span><span class="sxs-lookup"><span data-stu-id="d8e17-156">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="d8e17-157">O nome do caminho do arquivo de texto que contém a lista de usuários.</span><span class="sxs-lookup"><span data-stu-id="d8e17-157">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="d8e17-158">Um nome para a pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d8e17-158">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="d8e17-159">A consulta de pesquisa (deixe em branco para retornar todos os itens nos locais de conteúdo).</span><span class="sxs-lookup"><span data-stu-id="d8e17-159">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="d8e17-p114">O script Obtém as URLs para cada site do OneDrive for Business e, em seguida, cria e inicia a pesquisa. Você pode executar o cmdlet **Get-ComplianceSearch** no centro de segurança _AMP_ de conformidade do PowerShell para exibir as estatísticas e resultados da pesquisa ou pode ir para a página de **pesquisa** de conteúdo &amp; no centro de conformidade de segurança para exibir informações sobre a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d8e17-p114">The script gets the URLs for each OneDrive for Business site and then creates and starts the search. You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security &amp; Compliance Center to view information about the search.</span></span> 
