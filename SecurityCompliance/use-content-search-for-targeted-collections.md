---
title: Usar a pesquisa de conteúdo no Office 365 para conjuntos de destino
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para executar os conjuntos de destino. Uma coleção direcionada significa que você está confiante de que os itens respondendo de forma a um caso ou itens privilegiados estão localizados em uma pasta de caixa de correio ou de site específica. Use o script neste artigo para obter o ID da pasta ou o caminho para as pastas de caixa de correio ou de site específicos que você deseja pesquisar.
ms.openlocfilehash: 094fa4de4b8de9782a9bafb2eb8fb6ef3c52b46b
ms.sourcegitcommit: 06ae71741875f604bcc7a4e01b0b62cc768cbe97
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/13/2018
ms.locfileid: "27245058"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="e486c-105">Usar a pesquisa de conteúdo no Office 365 para conjuntos de destino</span><span class="sxs-lookup"><span data-stu-id="e486c-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="e486c-p102">O recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade não ofereça uma maneira direta na interface de usuário para pesquisar pastas específicas em caixas de correio do Exchange ou o SharePoint e o OneDrive sites corporativos. No entanto, é possível pesquisar pastas específicas (chamadas um *destinadas a coleção*), especificando o ID da pasta ou o caminho na sintaxe da consulta de pesquisa real. Uso de pesquisa de conteúdo para executar um conjunto de destino é útil quando você estiver confiante de que os itens respondendo de forma a um caso ou itens privilegiados estão localizados em uma pasta de caixa de correio ou de site específica. Você pode usar o script neste artigo para obter o ID de pasta para pastas de caixa de correio ou o caminho para pastas em um SharePoint e OneDrive para o site de negócios. Em seguida, você pode usar o ID da pasta ou o caminho em uma consulta de pesquisa para retornar a itens localizados na pasta.</span><span class="sxs-lookup"><span data-stu-id="e486c-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="e486c-111">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="e486c-111">Before you begin</span></span>

- <span data-ttu-id="e486c-p103">Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script na etapa 1. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e486c-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="e486c-p104">Além disso, você precisa ser atribuído à função de destinatários de email na sua organização do Exchange Online. Isso é necessário para executar o cmdlet **Get-MailboxFolderStatistics** , que está incluído no script na etapa 1. Por padrão, a função de destinatários de email é atribuída aos grupos de função de gerenciamento de organização e gerenciamento de destinatário no Exchange Online. Para obter mais informações sobre como atribuir permissões no Exchange Online, consulte [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). Você pode também criar um grupo de função personalizada, atribua a função destinatários de email a ela e, em seguida, adicionar os membros que precisam para executar o script na etapa 1. Para obter mais informações, consulte [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="e486c-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="e486c-p105">Cada vez que você executar o script na etapa 1, uma nova sessão do PowerShell remota é criada. Portanto, você poderia usar backup todas as PowerShell sessões remotas disponíveis para você. Para evitar que isso aconteça, você pode executar o seguinte comando para desconectar suas sessões ativas de PowerShell remotos.</span><span class="sxs-lookup"><span data-stu-id="e486c-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="e486c-123">Para saber mais, confira [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="e486c-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="e486c-p106">O script inclui o tratamento de erros mínimas. A principal finalidade do script é rapidamente exibir uma lista de IDs de pasta de caixa de correio ou de caminhos que podem ser usados para executar um conjunto de destino na sintaxe da consulta de pesquisa de uma pesquisa de conteúdo de site.</span><span class="sxs-lookup"><span data-stu-id="e486c-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="e486c-p107">O script de amostra fornecido neste tópico não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="e486c-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="e486c-131">Etapa 1: Execute o script para obter uma lista de pastas para uma caixa de correio ou de um site</span><span class="sxs-lookup"><span data-stu-id="e486c-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="e486c-p108">O script que você execute nesta etapa primeiro vai retornar uma lista de pastas de caixa de correio ou SharePoint ou o OneDrive para pastas de negócios e o ID da pasta correspondente ou o caminho para cada pasta. Quando você executar esse script, ele solicitará para as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="e486c-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="e486c-p109">**URL do site ou o endereço de email** Digite um endereço de email do dos responsáveis para retornar uma lista de pastas de caixa de correio do Exchange e IDs de pasta. Ou então, digite a URL para um site do SharePoint ou um OneDrive para o site de negócios para retornar uma lista de caminhos do site especificado. Aqui estão alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="e486c-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="e486c-137">**Exchange** - stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="e486c-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="e486c-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="e486c-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="e486c-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="e486c-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="e486c-p110">**Suas credenciais de usuário** - o script usarão suas credenciais para se conectar ao Exchange Online e a segurança &amp; Centro de conformidade com o PowerShell remoto. Conforme explicado anteriormente, você precisará atribua as permissões apropriadas para executar com êxito esse script.</span><span class="sxs-lookup"><span data-stu-id="e486c-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="e486c-142">Para exibir uma lista de pastas de caixa de correio ou nomes de caminho do site:</span><span class="sxs-lookup"><span data-stu-id="e486c-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="e486c-143">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="e486c-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appended to the folder ID or path ID to use in a Content Search.               #
  # Notes:                                              #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the   #
  #      the current folder and all sub-folders are searched.                       #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                               #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.       #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security &amp; Compliance Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security &amp; Compliance Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Compliance Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "path:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. <span data-ttu-id="e486c-144">No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="e486c-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="e486c-145">Executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e486c-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="e486c-146">Insira as informações que o script solicita.</span><span class="sxs-lookup"><span data-stu-id="e486c-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="e486c-p111">O script exibe uma lista de pastas de caixa de correio ou pasta de site para o usuário especificado. Permitir que esta janela Abrir para que você pode copiar um nome de ID ou o caminho da pasta e colá-la para uma consulta de pesquisa na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="e486c-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="e486c-p112">Em vez de exibir uma lista de pastas na tela do computador, você pode direcionar novamente a saída do script para um arquivo de texto. Este arquivo será salvo na pasta onde o script está localizado. Por exemplo, para redirecionar a saída para um arquivo de texto do script, execute o seguinte comando na etapa 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` e em seguida, você pode copiar uma ID da pasta ou um caminho de arquivo a ser usado em uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e486c-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="e486c-152">Saída do script para pastas de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e486c-152">Script output for mailbox folders</span></span>

<span data-ttu-id="e486c-p113">Se estiver recebendo IDs de pasta de caixa de correio, o script conecta-se ao Exchange Online usando o PowerShell remoto, executa o cmdlet **Get-MailboxFolderStatisics** e, em seguida, exibe a lista de pastas da caixa de correio especificada. Para cada pasta na caixa de correio, o script exibe o nome da pasta na coluna **FolderPath** e o ID de pasta na coluna **FolderQuery** . Além disso, o script adiciona o prefixo de **folderId** (que é o nome da propriedade da caixa de correio) à ID de pasta. Como a propriedade **folderid** é uma propriedade pesquisável, você usará `folderid:<folderid>` em uma consulta de pesquisa na etapa 2 para pesquisar dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="e486c-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="e486c-157">Aqui está um exemplo da saída retornado pelo script para pastas de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="e486c-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Exemplo da lista de pastas de caixa de correio e pasta IDs retornados pelo script.](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="e486c-159">O exemplo na etapa 2 mostra a consulta usada para pesquisar a subpasta limpezas na pasta de itens recuperáveis do usuário.</span><span class="sxs-lookup"><span data-stu-id="e486c-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="e486c-160">Saída do script para pastas de site</span><span class="sxs-lookup"><span data-stu-id="e486c-160">Script output for site folders</span></span>

<span data-ttu-id="e486c-p114">Se estiver recebendo caminhos do SharePoint ou OneDrive para sites corporativos, o script conecta-se à segurança &amp; Centro de conformidade usando o PowerShell remoto, cria uma nova pesquisa de conteúdo que o site para pastas de pesquisa e, em seguida, exibe uma lista das pastas localizado no site especificado. O script exibe o nome de cada pasta e adiciona o prefixo do **caminho** (que é o nome da propriedade site) para a URL da pasta. Como a propriedade **path** é uma propriedade pesquisável, você usará `path:<path>` em uma consulta de pesquisa na etapa 2 para pesquisar dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="e486c-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="e486c-164">Aqui está um exemplo da saída retornado pelo script para pastas de site.</span><span class="sxs-lookup"><span data-stu-id="e486c-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![Exemplo da lista de nomes de caminho para pastas de site retornados pelo script.](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="e486c-166">Etapa 2: Usar uma ID da pasta ou um caminho para executar um conjunto de destino</span><span class="sxs-lookup"><span data-stu-id="e486c-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="e486c-p115">Depois de executar o script para coletar a uma lista de IDs de pasta ou caminhos para um usuário específico, a próxima etapa para ir para a segurança &amp; Centro de conformidade e criar uma nova pesquisa de conteúdo para pesquisar uma pasta específica. Você usará o `folderid:<folderid>` ou `path:<path>` propriedade na consulta de pesquisa que você definir na caixa de palavra-chave de pesquisa de conteúdo (ou como o valor do parâmetro *ContentMatchQuery* se você usar o cmdlet **New-ComplianceSearch** ). Você pode combinar os `folderid` ou `path` propriedade com os outros parâmetros de pesquisa ou critérios de pesquisa. Se você incluir apenas o `folderid` ou `path` propriedade na consulta, a pesquisa retornará todos os itens localizados na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e486c-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e486c-171">Usando o `path` propriedade pesquisar OneDrive locais não devolvem arquivos de mídia, como arquivos. png,. wav ou. TIFF, nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e486c-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="e486c-172">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="e486c-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="e486c-173">Entrar no Office 365 usando a conta e as credenciais usadas para executar o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="e486c-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="e486c-174">No painel à esquerda da segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **pesquisa de conteúdo**e, em seguida, clique em **novo** ![ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="e486c-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="e486c-p116">Na página **Nova pesquisa**, digite um nome para a Pesquisa de Conteúdo. O nome deve ser exclusivo em sua organização.</span><span class="sxs-lookup"><span data-stu-id="e486c-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="e486c-177">Em **onde você deseja com a aparência**, siga um destes procedimentos, com base na qual está pesquisando uma pasta de caixa de correio ou de uma pasta do site:</span><span class="sxs-lookup"><span data-stu-id="e486c-177">Under **Where do you want us to look**, do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="e486c-178">Clique em **Escolher caixas de correio específicas para pesquisar** e adicione a mesma caixa de correio que você especificou quando executou o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="e486c-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="e486c-179">Ou</span><span class="sxs-lookup"><span data-stu-id="e486c-179">Or</span></span>
    
    - <span data-ttu-id="e486c-180">Clique em **sites específicos de escolha Pesquisar** para pesquisar e, em seguida, adicionar a mesma URL do site que você especificou quando executou o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="e486c-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="e486c-181">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e486c-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="e486c-182">Na caixa na página **que você deseja fazer conosco para procurar por** palavra-chave, cole o `folderid:<folderid>` ou `path:<path>` valor que foi retornado pelo script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="e486c-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="e486c-183">Por exemplo, a consulta na seguinte imagem pesquisará para qualquer item na subpasta limpezas na pasta de itens recuperáveis do usuário (o valor do `folderid` propriedade para a subpasta limpezas é mostrada na captura de tela na etapa 1):</span><span class="sxs-lookup"><span data-stu-id="e486c-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Cole o folderid ou o caminho na caixa palavras-chave da consulta de pesquisa](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="e486c-185">Clique em **pesquisa** para iniciar a pesquisa do conjunto de destino.</span><span class="sxs-lookup"><span data-stu-id="e486c-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="e486c-186">Exemplos de consultas de pesquisa para conjuntos de destino</span><span class="sxs-lookup"><span data-stu-id="e486c-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="e486c-p117">Aqui estão alguns exemplos de como usar o `folderid` e `path` propriedades em uma consulta de pesquisa para executar um conjunto de destino. Observe que os espaços reservados são usados para `folderid:<folderid>` e `path:<path>` para economizar espaço.</span><span class="sxs-lookup"><span data-stu-id="e486c-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="e486c-p118">Este exemplo procura três pastas de caixa de correio diferente. Você poderia usar a sintaxe de consulta semelhante para pesquisar as pastas ocultas na pasta de itens recuperáveis do usuário.</span><span class="sxs-lookup"><span data-stu-id="e486c-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="e486c-191">Este exemplo procura uma pasta de caixa de correio para itens que contenham uma frase exata.</span><span class="sxs-lookup"><span data-stu-id="e486c-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="e486c-192">Este exemplo procura uma pasta do site (e todas as subpastas) para documentos que contêm as letras "Divulgação" do título.</span><span class="sxs-lookup"><span data-stu-id="e486c-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="e486c-193">Este exemplo procura uma pasta do site (e qualquer subpasta) para documentos ali foram alterados dentro de um intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="e486c-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="e486c-194">Mais informações</span><span class="sxs-lookup"><span data-stu-id="e486c-194">More information</span></span>

<span data-ttu-id="e486c-195">Mantenha as seguintes coisas em mente ao usar o script neste artigo para executar os conjuntos de destino.</span><span class="sxs-lookup"><span data-stu-id="e486c-195">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>
  
- <span data-ttu-id="e486c-p119">O script não remove todas as pastas dos resultados. Para algumas pastas listados nos resultados podem ser não pesquisáveis (ou retornar zero itens) porque eles contêm conteúdo gerada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e486c-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="e486c-p120">Esse script retorna apenas informações de pasta de caixa de correio principal do usuário. Ele não retorna informações sobre pastas na caixa de correio de arquivo morto do usuário.</span><span class="sxs-lookup"><span data-stu-id="e486c-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="e486c-p121">Ao pesquisar pastas de caixa de correio, somente a pasta especificada (identificado pelo seu `folderid` propriedade) devem ser pesquisadas. As subpastas não ser pesquisadas. Para Pesquisar subpastas, você precisará usar o ID da pasta para a subpasta que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="e486c-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  folder ID for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="e486c-203">Ao pesquisar pastas do site, na pasta (identificado pelo seu `path` propriedade) e todas as subpastas devem ser pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="e486c-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="e486c-p122">Conforme indicado anteriormente, não é possível usar `path` propriedade para procurar arquivos de mídia,. png,. TIFF ou arquivos. wav, localizado em OneDrive locais. Use uma [propriedade do site](keyword-queries-and-search-conditions.md#searchable-site-properties) de diferentes para pesquisar os arquivos de mídia nas pastas de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="e486c-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 

- <span data-ttu-id="e486c-p123">Ao exportar os resultados de uma pesquisa em que você especificou apenas o `folderid` propriedade na consulta de pesquisa, você pode escolher a exportação a primeira opção, "todos os itens, excluindo aquelas que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos." Todos os itens na pasta sempre serão exportados independente do status de indexação porque o ID da pasta sempre é indexado.</span><span class="sxs-lookup"><span data-stu-id="e486c-p123">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons." All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
