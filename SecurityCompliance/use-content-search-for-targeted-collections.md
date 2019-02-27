---
title: Usar a pesquisa de conteúdo no Office 365 para coleções direcionadas
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Use a pesquisa de conteúdo no centro de &amp; conformidade de segurança do Office 365 para realizar coleções direcionadas. Uma coleção direcionada significa que você tem certeza de que os itens que respondem a um caso ou itens privilegiados estão localizados em uma caixa de correio ou pasta de site específica. Use o script neste artigo para obter a ID da pasta ou o caminho das pastas de caixa de correio ou de site específicas que você deseja pesquisar.
ms.openlocfilehash: c6e837e2f95b4f2ae3e32344f966f096407e360e
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296924"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="48c93-105">Usar a pesquisa de conteúdo no Office 365 para coleções direcionadas</span><span class="sxs-lookup"><span data-stu-id="48c93-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="48c93-p102">O recurso de pesquisa de conteúdo no centro de &amp; conformidade de segurança do Office 365 não oferece uma maneira direta na interface de usuário pesquisar pastas específicas em caixas de correio do Exchange ou sites do SharePoint e do onedrive for Business. No enTanto, é possível pesquisar pastas específicas (chamadas de *coleção direcionadas*) ESPECIFICANDO a ID da pasta ou o caminho na sintaxe de consulta de pesquisa real. O uso da pesquisa de conteúdo para executar uma coleção direcionada é útil quando você tem certeza de que os itens que respondem a um caso ou itens privilegiados estão localizados em uma caixa de correio ou pasta de site específica. Você pode usar o script neste artigo para obter a ID de pasta para pastas de caixa de correio ou o caminho para pastas em um site do SharePoint e do OneDrive for Business. Em seguida, você pode usar a ID de pasta ou o caminho em uma consulta de pesquisa para retornar itens localizados na pasta.</span><span class="sxs-lookup"><span data-stu-id="48c93-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="48c93-111">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="48c93-111">Before you begin</span></span>

- <span data-ttu-id="48c93-p103">Você precisa ser membro do grupo de função Gerenciador de descoberta eletrônica no centro de &amp; conformidade de segurança para executar o script na etapa 1. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no centro &amp; de conformidade de segurança do Office 365](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="48c93-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="48c93-p104">Além disso, você precisa receber a função de destinatários de email em sua organização do Exchange Online. Isso é necessário para executar o cmdlet **Get-MailboxFolderStatistics** , que está incluído no script na etapa 1. Por padrão, a função de destinatários de email é atribuída aos grupos de função de gerenciamento de organização e de gerenciamento de destinatários no Exchange Online. Para obter mais informações sobre como atribuir permissões no Exchange Online, consulte [Manage role Group Members](https://go.microsoft.com/fwlink/p/?linkid=692102). Você também pode criar um grupo de função personalizado, atribuir a ele a função de destinatários de email e, em seguida, adicionar os membros que precisam executar o script na etapa 1. Para obter mais informações, consulte [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="48c93-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="48c93-p105">Cada vez que você executa o script na etapa 1, uma nova sessão remota do PowerShell é criada. Portanto, você pode usar todas as sessões remotas do PowerShell disponíveis para você. Para evitar que isso aconteça, você pode executar o seguinte comando para desconectar suas sessões do PowerShell remotos ativas.</span><span class="sxs-lookup"><span data-stu-id="48c93-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="48c93-123">Para saber mais, confira [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="48c93-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="48c93-p106">O script inclui o tratamento de erros mínimo. O objetivo principal do script é exibir rapidamente uma lista de IDs de pasta de caixa de correio ou caminhos de site que podem ser usados na sintaxe de consulta de pesquisa de uma pesquisa de conteúdo para executar uma coleção direcionada.</span><span class="sxs-lookup"><span data-stu-id="48c93-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="48c93-p107">Não há suporte para o script de exemplo fornecido neste tópico em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido como está sem garantia de qualquer tipo. A Microsoft se isenta de todas as garantias implícitas, incluindo, sem limitação, quaisquer garantias implícitas de comercialização ou ADEQÜAÇÃO para um propósito específico. Todo o risco resultante do uso ou do desempenho do script de exemplo e da documentação permanece com você. Em hipótese alguma a Microsoft, seus autores ou qualquer outra pessoa envolvida na criação, produção ou entrega dos scripts serão responsáveis por qualquer dano (incluindo, sem limitação, danos à perda de lucros de negócios, interrupção de negócios, perda de informações comerciais ou outras perdas de pecuniary) resultantes do uso ou da incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido avisada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="48c93-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="48c93-131">Etapa 1: executar o script para obter uma lista de pastas para uma caixa de correio ou site</span><span class="sxs-lookup"><span data-stu-id="48c93-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="48c93-p108">O script executado nesta primeira etapa retornará uma lista de pastas de caixa de correio ou pastas do SharePoint ou do OneDrive for Business e a ID de pasta ou o caminho correspondente de cada pasta. Quando você executar esse script, ele solicitará as seguintes informações.</span><span class="sxs-lookup"><span data-stu-id="48c93-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="48c93-p109">**Endereço de email ou URL do site** Digite um endereço de email do responsáveis para retornar uma lista de pastas de caixa de correio do Exchange e IDs de pasta. Ou digite a URL de um site do SharePoint ou do OneDrive for Business para retornar uma lista de caminhos para o site especificado. Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="48c93-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="48c93-137">**Exchange** -stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="48c93-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="48c93-138">**Do** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="48c93-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="48c93-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="48c93-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="48c93-p110">**Suas credenciais de usuário** -o script usará suas credenciais para se conectar ao Exchange Online e &amp; ao centro de conformidade de segurança com o PowerShell remoto. Conforme explicado anteriormente, você precisa atribuir as permissões apropriadas para executar esse script com êxito.</span><span class="sxs-lookup"><span data-stu-id="48c93-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="48c93-142">Para exibir uma lista de pastas de caixa de correio ou nomes de caminho de site:</span><span class="sxs-lookup"><span data-stu-id="48c93-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="48c93-143">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="48c93-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
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

2. <span data-ttu-id="48c93-144">No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="48c93-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="48c93-145">Executar o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="48c93-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="48c93-146">Insira as informações que o script solicitará para você.</span><span class="sxs-lookup"><span data-stu-id="48c93-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="48c93-p111">O script exibe uma lista de pastas de caixa de correio ou pasta de site para o usuário especificado. Deixe essa janela aberta para que você possa copiar uma ID de pasta ou um nome de caminho e colá-lo em uma consulta de pesquisa na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="48c93-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="48c93-p112">Em vez de exibir uma lista de pastas na tela do computador, você pode redirecionar a saída do script para um arquivo de texto. Esse arquivo será salvo na pasta em que o script está localizado. Por exemplo, para redirecionar a saída do script para um arquivo de texto, execute o seguinte comando `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` na etapa 3: depois você pode copiar uma ID de pasta ou caminho do arquivo para usar em uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="48c93-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="48c93-152">Saída de script para pastas de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="48c93-152">Script output for mailbox folders</span></span>

<span data-ttu-id="48c93-p113">Se você estiver obtendo IDs de pasta de caixa de correio, o script se conecta ao Exchange Online usando o PowerShell remoto, executa o cmdlet **Get-MailboxFolderStatisics** e exibe a lista de pastas da caixa de correio especificada. Para cada pasta na caixa de correio, o script exibe o nome da pasta na coluna **FolderPath** e a ID da pasta na coluna **FolderQuery** . Além disso, o script adiciona o prefixo \*\*\*\* de FolderId (que é o nome da propriedade da caixa de correio) à ID da pasta. Como a \*\*\*\* Propriedade FolderId é uma propriedade pesquisável, você usará `folderid:<folderid>` uma consulta de pesquisa na etapa 2 para pesquisar essa pasta.</span><span class="sxs-lookup"><span data-stu-id="48c93-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="48c93-157">Veja um exemplo de saída retornada pelo script para pastas de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="48c93-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Exemplo da lista de pastas de caixa de correio e IDs de pasta retornada pelo script](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="48c93-159">O exemplo na etapa 2 mostra a consulta usada para pesquisar a subpasta de limpezas na pasta itens recuperáveis do usuário.</span><span class="sxs-lookup"><span data-stu-id="48c93-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="48c93-160">Saída de script para pastas de site</span><span class="sxs-lookup"><span data-stu-id="48c93-160">Script output for site folders</span></span>

<span data-ttu-id="48c93-p114">Se você estiver obtendo caminhos de sites do SharePoint ou do OneDrive for Business, o script se conecta &amp; ao centro de conformidade de segurança usando o PowerShell remoto, cria uma nova pesquisa de conteúdo que procura por pastas no site e, em seguida, exibe uma lista das pastas localizado no site especificado. O script exibe o nome de cada pasta e adiciona o prefixo de **caminho** (que é o nome da propriedade de site) à URL da pasta. Como a propriedade **path** é uma propriedade pesquisável, você usará `path:<path>` uma consulta de pesquisa na etapa 2 para pesquisar essa pasta.</span><span class="sxs-lookup"><span data-stu-id="48c93-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="48c93-164">Veja um exemplo de saída retornada pelo script para pastas de site.</span><span class="sxs-lookup"><span data-stu-id="48c93-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![Exemplo da lista de nomes de caminho para pastas de site retornadas pelo script](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="48c93-166">Etapa 2: usar uma ID de pasta ou um caminho para executar uma coleção de direcionamento</span><span class="sxs-lookup"><span data-stu-id="48c93-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="48c93-p115">Após executar o script para coletar uma lista de IDs de pasta ou caminhos para um usuário específico, a próxima etapa para acessar o centro de conformidade &amp; de segurança e criar uma nova pesquisa de conteúdo para pesquisar uma pasta específica. Você usará a `folderid:<folderid>` propriedade `path:<path>` ou na consulta de pesquisa que você configura na caixa palavra-chave de pesquisa de conteúdo (ou como o valor para o parâmetro *ContentMatchQuery* se você usar o cmdlet **New-ComplianceSearch** ). Você pode combinar a `folderid` propriedade `path` ou com outros parâmetros de pesquisa ou condições de pesquisa. Se você incluir apenas a `folderid` propriedade `path` ou na consulta, a pesquisa retornará todos os itens localizados na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="48c93-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="48c93-171">O uso `path` da propriedade para pesquisar os locais do onedrive não retornará arquivos de mídia, como arquivos. png,. TIFF ou. wav, nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="48c93-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="48c93-172">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="48c93-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="48c93-173">Entre no Office 365 usando a conta e as credenciais que você usou para executar o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="48c93-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="48c93-174">No painel esquerdo do centro de conformidade &amp; de segurança, clique em **pesquisa de conteúdo**de investigação \> de \*\* &amp; pesquisa\*\* e clique em](media/O365-MDM-CreatePolicy-AddIcon.gif) **novo** ![ícone de adição.</span><span class="sxs-lookup"><span data-stu-id="48c93-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="48c93-p116">Na página **Nova pesquisa**, digite um nome para a Pesquisa de Conteúdo. O nome deve ser exclusivo em sua organização.</span><span class="sxs-lookup"><span data-stu-id="48c93-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="48c93-177">Em **onde você deseja procurar**, faça um dos seguintes, dependendo de como você está pesquisando uma pasta de caixa de correio ou uma pasta de site:</span><span class="sxs-lookup"><span data-stu-id="48c93-177">Under **Where do you want us to look**, do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="48c93-178">Clique em **escolher caixas de correio específicas para pesquisar** e, em seguida, adicione a mesma caixa de correio que você especificou ao executar o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="48c93-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="48c93-179">Ou</span><span class="sxs-lookup"><span data-stu-id="48c93-179">Or</span></span>
    
    - <span data-ttu-id="48c93-180">Clique em **escolher sites específicos para pesquisar** e, em seguida, adicione a URL do site que você especificou ao executar o script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="48c93-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="48c93-181">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c93-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="48c93-182">Na caixa palavra-chave da página **o que você deseja procurar** , Cole o ou `folderid:<folderid>` `path:<path>` o valor retornado pelo script na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="48c93-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="48c93-183">Por exemplo, a consulta na captura de tela a seguir pesquisará qualquer item na subpasta de limpezas na pasta itens recuperáveis do usuário (o valor `folderid` da propriedade da subpasta de limpezas é mostrado na captura de tela na etapa 1):</span><span class="sxs-lookup"><span data-stu-id="48c93-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Cole o FolderId ou o caminho na caixa de palavra-chave da consulta de pesquisa](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="48c93-185">Clique em **Pesquisar** para iniciar a pesquisa de coleção direcionada.</span><span class="sxs-lookup"><span data-stu-id="48c93-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="48c93-186">Exemplos de consultas de pesquisa para coleções direcionadas</span><span class="sxs-lookup"><span data-stu-id="48c93-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="48c93-p117">Aqui estão alguns exemplos de como usar `folderid` as `path` Propriedades e em uma consulta de pesquisa para executar uma coleção direcionada. Observe que os espaços reservados são usados `folderid:<folderid>` para `path:<path>` o e economizar espaço.</span><span class="sxs-lookup"><span data-stu-id="48c93-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="48c93-p118">Este exemplo pesquisa três pastas de caixa de correio diferentes. Você pode usar sintaxe de consulta semelhante para pesquisar as pastas ocultas em uma pasta de itens recuperáveis de um usuário.</span><span class="sxs-lookup"><span data-stu-id="48c93-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="48c93-191">Este exemplo procura em uma pasta de caixa de correio itens que contenham uma frase exata.</span><span class="sxs-lookup"><span data-stu-id="48c93-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="48c93-192">Este exemplo pesquisa uma pasta de site (e todas as subpastas) para documentos que contenham as letras "NDA" no título.</span><span class="sxs-lookup"><span data-stu-id="48c93-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="48c93-193">Este exemplo pesquisa uma pasta de site (e qualquer subpasta) para documentos que foram alterados em um intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="48c93-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="48c93-194">Mais informações</span><span class="sxs-lookup"><span data-stu-id="48c93-194">More information</span></span>

<span data-ttu-id="48c93-195">Tenha em mente os seguintes pontos ao usar o script neste artigo para executar coleções direcionadas.</span><span class="sxs-lookup"><span data-stu-id="48c93-195">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>
  
- <span data-ttu-id="48c93-p119">O script não remove nenhuma pasta dos resultados. Portanto, algumas pastas listadas nos resultados podem não ser pesquisadas (ou retornar itens de zero) porque contêm conteúdo gerado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="48c93-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="48c93-p120">Este script retorna apenas as informações da pasta da caixa de correio principal do usuário. Ele não retorna informações sobre pastas na caixa de correio de arquivo morto do usuário.</span><span class="sxs-lookup"><span data-stu-id="48c93-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="48c93-p121">Ao pesquisar pastas de caixa de correio, somente a pasta especificada ( `folderid` identificado por sua propriedade) será pesquisada. As subpastas não serão pesquisadas. Para pesquisar subpastas, você precisa usar a ID de pasta para a subpasta que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="48c93-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  folder ID for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="48c93-203">Ao pesquisar pastas de site, a pasta (identificado por `path` sua propriedade) e todas as subpastas serão pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="48c93-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="48c93-p122">Conforme mencionado anteriormente, você não pode `path` usar a propriedade para pesquisar arquivos de mídia, como arquivos. png,. TIFF ou. wav, localizados em locais do onedrive. Use uma [propriedade de site](keyword-queries-and-search-conditions.md#searchable-site-properties) diferente para pesquisar arquivos de mídia em pastas do onedrive.</span><span class="sxs-lookup"><span data-stu-id="48c93-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 

- <span data-ttu-id="48c93-p123">Ao exportar os resultados de uma pesquisa na qual você só especificou `folderid` a propriedade na consulta de pesquisa, você pode escolher a primeira opção de exportação, "todos os itens, exceto aqueles que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos". Todos os itens na pasta sempre serão exportados, independentemente do status de indexação, porque a ID da pasta é sempre indexada.</span><span class="sxs-lookup"><span data-stu-id="48c93-p123">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons." All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
