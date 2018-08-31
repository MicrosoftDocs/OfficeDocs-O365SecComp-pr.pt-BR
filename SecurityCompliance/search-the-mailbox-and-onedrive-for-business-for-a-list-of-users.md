---
title: Usar a Pesquisa de Conteúdo para pesquisar na caixa de correio e no site do OneDrive for Business para obter uma lista de usuários
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Use a pesquisa de conteúdo e o script neste artigo para procurar as caixas de correio e OneDrive sites corporativos para um grupo de usuários.
ms.openlocfilehash: cc88f8e81a9883b8d392965db14994691878748d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523912"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Usar a Pesquisa de Conteúdo para pesquisar na caixa de correio e no site do OneDrive for Business para obter uma lista de usuários

A segurança do Office 365 &amp; Centro de conformidade fornece uma série de cmdlets do Windows PowerShell que permitem automatizar demoradas tarefas relacionadas a descoberta eletrônica. Atualmente, criando uma pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar um grande número de locais de conteúdo dos responsáveis leva tempo e preparação. Antes de criar uma pesquisa, você precisa coletar a URL para cada OneDrive for sites corporativos e adicione cada caixa de correio e O neDrive para o site de negócios para a pesquisa. Em futuras versões, esse será mais fácil fazer na segurança &amp; Centro de conformidade. Enquanto isso, você pode usar o script neste artigo para automatizar esse processo. Esse script solicita o nome do domínio de meusite da sua organização (por exemplo, **contoso** na URL https://contoso-my.sharepoint.com), endereços de uma lista de email do usuário, o nome da nova pesquisa de conteúdo e consulta de pesquisa para usar. O script obtém o OneDrive para Business URL para cada usuário na lista e, em seguida, ele cria e inicia uma pesquisa de conteúdo que a caixa de correio de pesquisa e OneDrive para o site de negócios para cada usuário na lista, usando a consulta de pesquisa que você fornecer. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade e um administrador global do SharePoint Online para executar o script na etapa 3.
    
- Certifique-se de salvar a lista de usuários que você criar na etapa 2 e o script na etapa 3 para a mesma pasta. Será que tornam mais fácil executar o script.
    
- O script inclui o tratamento de erros mínimas. Sua finalidade principal é rapidez e facilidade de pesquisa a caixa de correio e OneDrive para site de negócios de cada usuário.
    
- Os scripts de exemplo fornecidos neste tópico não são suportados em qualquer serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos que se encontra, sem qualquer garantia. Microsoft também se isenta todos i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied implícitas, sem limitação, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho dos scripts de amostra e documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Etapa 1: Instalar o Shell de gerenciamento do SharePoint Online
<a name="step1"> </a>

A primeira etapa é instalar o Shell de gerenciamento do SharePoint Online. Você não precisa usar o shell neste procedimento, mas você precisa instalá-lo, pois ele contém pré-requisitos necessários para o script que você pode executar na etapa 3. Esses pré-requisitos permitem que o script para se comunicar com o SharePoint Online para obter as URLs para o OneDrive for sites corporativos.
  
Vá para [Configurar o ambiente do SharePoint Online Management Shell do Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) e executar a etapa 1 e a etapa 2 para instalar o Shell de gerenciamento do SharePoint Online.
  
## <a name="step-2-generate-a-list-of-users"></a>Etapa 2: Gerar uma lista de usuários
<a name="step2"> </a>

O script na etapa 3 criará uma pesquisa de conteúdo para pesquisar as caixas de correio e as contas de OneDrive para obter uma lista de usuários. Você pode apenas digitar os endereços de email em um arquivo de texto, ou você pode executar um comando do Windows PowerShell para obter uma lista de endereços de email e salvá-los em um arquivo (localizado na mesma pasta que você vai salvar o script na etapa 3).
  
Aqui está um comando do [PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=517283) que você pode runt para obter uma lista de endereços de email para todos os usuários em sua organização e salvá-lo em um arquivo de texto chamado `Users.txt`. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

Depois de executar este comando, não se esqueça de abrir o arquivo e remover o cabeçalho que contém o nome da propriedade, `PrimarySmtpAddress`. O arquivo de texto deve conter apenas uma lista de endereços de email e nada mais. Verifique não se que há nenhuma linha em branco antes ou depois da lista de endereços de email.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Etapa 3: Executar o script para criar e iniciar a pesquisa

Quando você executar o script nesta etapa, ele solicitará para as informações a seguir. Certifique-se de ter essas informações prontas antes de executar o script.
  
- **Suas credenciais de usuário** - o script usarão suas credenciais para acessar o SharePoint Online para obter o OneDrive para Business URLs e se conectem à segurança &amp; Centro de conformidade com o PowerShell remoto. 
    
- **Nome do seu domínio meusite** - meusite o domínio é o domínio que contém todos os OneDrive para sites corporativos em sua organização. Por exemplo, se a URL do seu domínio meusite for **https://contoso-my.sharepoint.com**, e em seguida, você digitaria `contoso` quando o script solicita o nome do seu domínio do meu site. 
    
- **Nome do caminho do arquivo de texto da etapa 2** - o nome do caminho do arquivo de texto que você criou na etapa 2. Se o arquivo de texto e o script estiverem localizados na mesma pasta, em seguida, digite o nome do arquivo de texto. Caso contrário, insira o caminho completo para o arquivo de texto. 
    
- **Nome da pesquisa conteúdo** - o nome da pesquisa conteúdo que será criado pelo script. 
    
- **Consulta de pesquisa** - a consulta de pesquisa que será usada com a pesquisa de conteúdo é criado e executado. Para obter mais informações sobre as consultas de pesquisa, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).


**Para executar o script:**
    
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `SearchEXOOD4B.ps1`. Salve o arquivo na mesma pasta onde você salvou a lista de usuários na etapa 2.
    
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

2. Abra o Windows PowerShell e vá para a pasta onde você salvou o script e a lista de usuários da etapa 2.
    
3. Inicie o script; Por exemplo:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Quando solicitado a fornecer suas credenciais, digite seu endereço de email e senha e clique em **Okey**. 
    
5. Insira a seguinte informações quando solicitado pelo script. Digite cada parte da informação e pressione **Enter**.
    
    - O nome do seu domínio do meu site. 
    
    - O nome do caminho do arquivo de texto que contém a lista de usuários.
    
    - Um nome para a pesquisa de conteúdo.
    
    - A consulta de pesquisa (deixe em branco para retornar todos os itens em locais de conteúdo).
    
    O script obtém as URLs para cada OneDrive para o site de negócios e, em seguida, cria e inicia a pesquisa. Você pode executar o cmdlet **Get-ComplianceSearch** no PowerShell do Centro de conformidade & segurança para exibir as estatísticas de pesquisa e resultados, ou você pode ir para a página de **pesquisa de conteúdo** na segurança &amp; Centro de conformidade para exibir informações sobre a pesquisa. 
