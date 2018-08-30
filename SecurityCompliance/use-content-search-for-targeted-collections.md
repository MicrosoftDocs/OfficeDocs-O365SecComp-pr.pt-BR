---
title: Usar a pesquisa de conteúdo no Office 365 para conjuntos de destino
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para executar os conjuntos de destino. Uma coleção direcionada significa que você está confiante de que os itens respondendo de forma a um caso ou itens privilegiados estão localizados em uma pasta de caixa de correio ou de site específica. Use o script neste artigo para obter o ID da pasta ou o caminho para as pastas de caixa de correio ou de site específicos que você deseja pesquisar.
ms.openlocfilehash: 3ff0ca00915bce53e9e932316c5ab47884f346b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523578"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Usar a pesquisa de conteúdo no Office 365 para conjuntos de destino

O recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade não ofereça uma maneira direta na interface de usuário para pesquisar pastas específicas em caixas de correio do Exchange ou o SharePoint e o OneDrive sites corporativos. No entanto, é possível pesquisar pastas específicas (chamadas de um conjunto de destino), especificando o ID da pasta ou o caminho na sintaxe da consulta de pesquisa real. Uso de pesquisa de conteúdo para executar um conjunto de destino é útil quando você estiver confiante de que os itens respondendo de forma a um caso ou itens privilegiados estão localizados em uma pasta de caixa de correio ou de site específica. Você pode usar o script neste artigo para obter o ID de pasta para pastas de caixa de correio ou o caminho para pastas em um SharePoint e OneDrive para o site de negócios. Em seguida, você pode usar o ID da pasta ou o caminho em uma consulta de pesquisa para retornar a itens localizados na pasta.
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script na etapa 1. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
    
    Além disso, você precisa ser atribuído à função de destinatários de email na sua organização do Exchange Online. Isso é necessário para executar o cmdlet **Get-MailboxFolderStatistics** , que está incluído no script na etapa 1. Por padrão, a função de destinatários de email é atribuída aos grupos de função de gerenciamento de organização e gerenciamento de destinatário no Exchange Online. Para obter mais informações sobre como atribuir permissões no Exchange Online, consulte [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). Você pode também criar um grupo de função personalizada, atribua a função destinatários de email a ela e, em seguida, adicionar os membros que precisam para executar o script na etapa 1. Para obter mais informações, consulte [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).
    
- Cada vez que você executar o script na etapa 1, uma nova sessão do PowerShell remota é criada. Portanto, você poderia usar backup todas as PowerShell sessões remotas disponíveis para você. Para evitar que isso aconteça, você pode executar o seguinte comando para desconectar suas sessões ativas de PowerShell remotos.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    Para saber mais, confira [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- O script inclui o tratamento de erros mínimas. A principal finalidade do script é rapidamente exibir uma lista de IDs de pasta de caixa de correio ou de caminhos que podem ser usados para executar um conjunto de destino na sintaxe da consulta de pesquisa de uma pesquisa de conteúdo de site.
    
- O script de amostra fornecido neste tópico não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>Etapa 1: Execute o script para obter uma lista de pastas para uma caixa de correio ou de um site

O script que você execute nesta etapa primeiro vai retornar uma lista de pastas de caixa de correio ou SharePoint ou o OneDrive para pastas de negócios e o ID da pasta correspondente ou o caminho para cada pasta. Quando você executar esse script, ele solicitará para as informações a seguir.
  
- **URL do site ou o endereço de email** Digite um endereço de email do dos responsáveis para retornar uma lista de pastas de caixa de correio do Exchange e dobrar IDs. Ou então, digite a URL para um site do SharePoint ou um OneDrive para o site de negócios para retornar uma lista de caminhos do site especificado. Aqui estão alguns exemplos: 
    
  - **Exchange** - stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **Suas credenciais de usuário** - o script usarão suas credenciais para se conectar ao Exchange Online e a segurança &amp; Centro de conformidade com o PowerShell remoto. Conforme explicado anteriormente, você precisará atribua as permissões apropriadas para executar com êxito esse script.
    
Para exibir uma lista de pastas de caixa de correio ou nomes de caminho do site:
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `GetFolderSearchParameters.ps1`.
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appeneded to the folder ID or path ID to use in a Content Search.              #
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
  # Authenticate with Exchange Online and the Security &amp; Complaince Center (Exchange Online Protection - EOP)
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
      # Authenticate with the Security &amp; Complaince Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the the script was aborted, the search we created might not have been deleted.  Try to do so now.
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
          # Create a Complinace Search Action and wait for it to complete. The folders will be listed in the .Results parameter
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

2. No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.
    
3. Executar o script; Por exemplo:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. Insira as informações que o script solicita.
    
    O script exibe uma lista de pastas de caixa de correio ou pasta de site para o usuário especificado. Permitir que esta janela Abrir para que você pode copiar um nome de ID ou o caminho da pasta e colá-la para uma consulta de pesquisa na etapa 2.
    
    > [!TIP]
    > Em vez de exibir uma lista de pastas na tela do computador, você pode direcionar novamente a saída do script para um arquivo de texto. Este arquivo será salvo na pasta onde o script está localizado. Por exemplo, para redirecionar a saída para um arquivo de texto do script, execute o seguinte comando na etapa 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` e em seguida, você pode copiar uma ID da pasta ou um caminho de arquivo a ser usado em uma consulta de pesquisa.
  
### <a name="script-output-for-mailbox-folders"></a>Saída do script para pastas de caixa de correio

Se estiver recebendo IDs de pasta de caixa de correio, o script conecta-se ao Exchange Online usando o PowerShell remoto, executa o cmdlet **Get-MailboxFolderStatisics** e, em seguida, exibe a lista de pastas da caixa de correio especificada. Para cada pasta na caixa de correio, o script exibe o nome da pasta na coluna **FolderPath** e o ID de pasta na coluna **FolderQuery** . Além disso, o script adiciona o prefixo de **folderId** (que é o nome da propriedade da caixa de correio) à ID de pasta. Como a propriedade **folderid** é uma propriedade pesquisável, você usará `folderid:<folderid>` em uma consulta de pesquisa na etapa 2 para pesquisar dessa pasta. 
  
Aqui está um exemplo da saída retornado pelo script para pastas de caixa de correio.
  
![Exemplo da lista de pastas de caixa de correio e pasta IDs retornados pelo script.](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
O exemplo na etapa 2 mostra a consulta usada para pesquisar a subpasta limpezas na pasta de itens recuperáveis do usuário.
  
### <a name="script-output-for-site-folders"></a>Saída do script para pastas de site

Se estiver recebendo caminhos do SharePoint ou OneDrive para sites corporativos, o script conecta-se à segurança &amp; Centro de conformidade usando o PowerShell remoto, cria uma nova pesquisa de conteúdo que o site para pastas de pesquisa e, em seguida, exibe uma lista das pastas localizado no site especificado. O script exibe o nome de cada pasta e adiciona o prefixo do **caminho** (que é o nome da propriedade site) para a URL da pasta. Como a propriedade **path** é uma propriedade pesquisável, você usará `path:<path>` em uma consulta de pesquisa na etapa 2 para pesquisar dessa pasta. 
  
Aqui está um exemplo da saída retornado pelo script para pastas de site.
  
![Exemplo da lista de nomes de caminho para pastas de site retornados pelo script.](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a>Etapa 2: Usar uma ID da pasta ou um caminho para executar um conjunto de destino

Depois de executar o script para coletar a uma lista de IDs de pasta ou caminhos para um usuário específico, a próxima etapa para ir para a segurança &amp; Centro de conformidade e criar uma nova pesquisa de conteúdo para pesquisar uma pasta específica. Você usará o `folderid:<folderid>` ou `path:<path>` propriedade na consulta de pesquisa que você definir na caixa de palavra-chave de pesquisa de conteúdo (ou como o valor do parâmetro *ContentMatchQuery* se você usar o cmdlet **New-ComplianceSearch** ). Você pode combinar os `folderid` ou `path` propriedade com os outros parâmetros de pesquisa ou critérios de pesquisa. Se você incluir apenas o `folderid` ou `path` propriedade na consulta, a pesquisa retornará todos os itens localizados na pasta especificada. 
  
> [!NOTE]
> Usando o `path` propriedade pesquisar OneDrive locais não devolvem arquivos de mídia, como arquivos. png,. wav ou. TIFF, nos resultados da pesquisa. 
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando a conta e as credenciais usadas para executar o script na etapa 1.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **pesquisa de conteúdo**e, em seguida, clique em **novo** ![ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
4. Na página **Nova pesquisa**, digite um nome para a Pesquisa de Conteúdo. O nome deve ser exclusivo em sua organização. 
    
5. Em **onde você deseja com a aparência**, siga um destes procedimentos, com base em se sua pesquisa uma pasta de caixa de correio ou uma pasta do site:
    
    - Clique em **Escolher caixas de correio específicas para pesquisar** e adicione a mesma caixa de correio que você especificou quando executou o script na etapa 1. 
    
      Ou
    
    - Clique em **sites específicos de escolha Pesquisar** para pesquisar e, em seguida, adicionar a mesma URL do site que você especificou quando executou o script na etapa 1. 
    
6. Clique em **Avançar**.
    
7. Na caixa na página **que você deseja fazer conosco para procurar por** palavra-chave, cole o `folderid:<folderid>` ou `path:<path>` valor que foi retornado pelo script na etapa 1. 
    
    Por exemplo, a consulta na seguinte imagem pesquisará para qualquer item na subpasta limpezas na pasta de itens recuperáveis do usuário (o valor do `folderid` propriedade para a subpasta limpezas é mostrada na captura de tela na etapa 1):
    
    ![Cole o folderid ou o caminho na caixa palavras-chave da consulta de pesquisa](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. Clique em **pesquisa** para iniciar a pesquisa do conjunto de destino. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>Exemplos de consultas de pesquisa para conjuntos de destino

Aqui estão alguns exemplos de como usar o `folderid` e `path` propriedades em uma consulta de pesquisa para executar um conjunto de destino. Observe que os espaços reservados são usados para `folderid:<folderid>` e `path:<path>` para economizar espaço. 
  
- Este exemplo procura três pastas de caixa de correio diferente. Você poderia usar a sintaxe de consulta semelhante para pesquisar as pastas ocultas na pasta de itens recuperáveis do usuário.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- Este exemplo procura uma pasta de caixa de correio para itens que contenham uma frase exata.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- Este exemplo procura uma pasta do site (e todas as subpastas) para documentos que contêm as letras "Divulgação" do título.
    
  ```
  path:<path> AND filename:nda
  ```

- Este exemplo procura uma pasta do site (e qualquer subpasta) para documentos ali foram alterados dentro de um intervalo de datas.
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>Mais informações

Mantenha as seguintes coisas em mente ao usar o script neste artigo e executando voltadas conjuntos.
  
- O script não remove todas as pastas dos resultados. Para algumas pastas listados nos resultados podem ser não pesquisáveis (ou retornar zero itens) porque eles contêm conteúdo gerada pelo sistema.
    
- Esse script retorna apenas informações de pasta de caixa de correio principal do usuário. Ele não retorna informações sobre pastas na caixa de correio de arquivo morto do usuário.
    
- Ao pesquisar pastas de caixa de correio, somente a pasta especificada (identificado pelo seu `folderid` propriedade) devem ser pesquisadas. As subpastas não ser pesquisadas. Para Pesquisar subpastas, você precisará usar o `folderid` para a subpasta que você deseja pesquisar. 
    
- Ao pesquisar pastas do site, na pasta (identificado pelo seu `path` propriedade) e todas as subpastas devem ser pesquisadas. 
    
- Conforme indicado anteriormente, não é possível usar `path` propriedade para procurar arquivos de mídia,. png,. TIFF ou arquivos. wav, localizado em OneDrive locais. Use uma [propriedade do site](keyword-queries-and-search-conditions.md#searchable-site-properties) de diferentes para pesquisar os arquivos de mídia nas pastas de OneDrive. 
