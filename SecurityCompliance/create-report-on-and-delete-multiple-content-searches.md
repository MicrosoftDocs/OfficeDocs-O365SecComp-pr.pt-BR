---
title: Criar, gerar relatórios e excluir várias Pesquisas de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Saiba como automatizar tarefas de pesquisa de conteúdo, como criar pesquisas e executar relatórios por meio de scripts do PowerShell no Office 365 Security &amp; Centro de conformidade.
ms.openlocfilehash: 2baa569c28ed5324e6674addeac688b854a65ed8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523707"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Criar, gerar relatórios e excluir várias Pesquisas de Conteúdo

 Criando rapidez e relatar as pesquisas de descoberta geralmente é uma etapa importante no eDiscovery e investigações quando você está tentando Saiba mais sobre os dados subjacentes e a riqueza e a qualidade das pesquisas. Para ajudá-lo a fazer isso, a segurança &amp; Centro de conformidade oferece um conjunto de cmdlets do Windows PowerShell para automatizar tarefas demoradas de pesquisa de conteúdo. Esses scripts fornecem uma maneira rápida e fácil para criar um número de pesquisas e, em seguida, executar relatórios dos resultados da pesquisa estimados que podem ajudá-lo a determinar a quantidade de dados em questão. Você também pode usar os scripts para criar versões diferentes de pesquisas para comparar os resultados de que cada um produz. Esses scripts podem ajudá-lo a identificar e analisar os dados rápida e eficiente. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar os scripts que são descritos neste tópico. 
    
- Para coletar uma lista das URLs do OneDrive para sites corporativos em sua organização que você pode adicionar o arquivo CSV na etapa 1, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Certifique-se de salvar todos os arquivos que você criar neste tópico na mesma pasta. Será que tornam mais fácil executar os scripts.
    
- Os scripts incluem o tratamento de erros mínimas. Sua finalidade principal é criar rapidamente, relatar e excluir várias pesquisas de conteúdo.
    
- Os scripts de exemplo fornecidos neste tópico não são suportados em qualquer serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos que se encontra, sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho dos scripts de amostra e documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Etapa 1: Criar um arquivo CSV que contém informações sobre as pesquisas que você deseja executar

O arquivo (CSV) de valores separados por vírgulas que você criar nesta etapa contém uma linha para cada usuário que deseja pesquisar. Você pode pesquisar o Exchange Online de correio do usuário (que inclui a caixa de correio de arquivo morto, se ele estiver habilitado) e seu OneDrive para o site de negócios. Ou você pode pesquisar apenas a caixa de correio ou OneDrive para o site de negócios. Você também pode pesquisar qualquer site na sua organização do SharePoint Online. O script que você pode executar na etapa 3 criará uma pesquisa separado para cada linha no arquivo CSV. 
  
1. Copie e cole o seguinte texto em um arquivo. txt usando o bloco de notas. Salve o arquivo para uma pasta no computador local. Você poupará os outros scripts para essa pasta também.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    A primeira linha ou a linha de cabeçalho do arquivo lista os parâmetros que serão usados pelo cmdlet **New-ComplianceSearch** (no script na etapa 3) para criar um novo pesquisas de conteúdo. O nome de cada parâmetro é separado por uma vírgula. Certificar-se de que não existem espaços na linha de cabeçalho. Cada linha sob a linha de cabeçalho representa os valores de parâmetro para cada pesquisa. Certifique-se de substituir os dados de espaço reservado no arquivo CSV com seus dados reais. 
    
2. Abra o arquivo. txt no Excel e, em seguida, use as informações na tabela a seguir para editar o arquivo com informações para cada pesquisa. 
    
    |**Parameter**|**Descrição**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |O endereço SMTP da caixa de correio do usuário.  <br/> |
    | `SharePointLocation` <br/> |A URL de OneDrive do usuário para o site de negócios ou a URL de qualquer site na sua organização. Para a URL do OneDrive for sites corporativos, use o seguinte formato: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Por exemplo, `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.<br/> |
    | `ContentMatchQuery` <br/> |A consulta de pesquisa para a pesquisa. Para obter mais informações sobre como criar uma consulta de pesquisa, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).<br/> |
    | `StartDate` <br/> |Para email, a data em ou após uma mensagem foi recebida por um destinatário ou enviada pelo remetente. Para documentos no SharePoint ou OneDrive para sites corporativos, a data em ou após um documento última modificação.  <br/> |
    | `EndDate` <br/> |Para email, a data em ou antes de uma mensagem foi enviada pelo enviados pelo usuário. Para documentos no SharePoint ou OneDrive para sites corporativos, a data em ou antes de um documento de última modificação.  <br/> |
   
3. Salve o arquivo do Excel como um arquivo CSV para uma pasta no computador local. O script que você criar na etapa 3 usará as informações neste arquivo CSV para criar as pesquisas. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Etapa 2: Conectar ao PowerShell do Centro de conformidade & segurança

A próxima etapa é conectar o Windows PowerShell para a segurança &amp; Centro de conformidade para sua organização.
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `ConnectSCC.ps1`. Salve o arquivo na mesma pasta que você salvou o arquivo CSV na etapa 1.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. No computador local, abra o Windows PowerShell, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Etapa 3: Executar o script para criar e iniciar as pesquisas

O script nesta etapa criará uma pesquisa de conteúdo separado para cada linha no arquivo CSV que você criou na etapa 1. Quando você executar esse script, você será solicitado para dois valores:
  
- **ID do grupo de busca** - esse nome fornece uma maneira fácil de organizar as pesquisas criados a partir do arquivo CSV. Cada pesquisa que é criada é chamada com a ID do grupo de pesquisa e, em seguida, um número foi acrescentado ao nome de pesquisa. Por exemplo, se você inserir **ContosoCase** para a ID do grupo de pesquisa, as pesquisas são nomeadas **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**e assim por diante. Observe que o nome que você digita diferencia maiusculas de minúsculas. Quando você usa a ID do grupo de busca na etapa 4 e etapa 5, você precisará usar o mesmo caso como fez quando criá-la. 
    
- **Arquivo CSV** - o nome do arquivo CSV que você criou na etapa 1. Certifique-se de incluir a usar o nome de arquivo completo, inclua a extensão de arquivo. csv; Por exemplo, `ContosoCase.csv`.
    
Para executar o script:

1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `CreateSearches.ps1`. Salve o arquivo na mesma pasta onde você salvou os outros arquivos.
    
  ```
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\CreateSearches.ps1
    ```

3. No prompt do **ID do grupo de busca** , digite o nome de um grupo de pesquisa e pressione **Enter**. Por exemplo, `ContosoCase`. Lembre-se de que esse nome diferencia maiusculas de minúsculas, portanto você terá que digitar ele da mesma maneira nas etapas posteriores.
    
4. No prompt do **arquivo CSV de origem** , digite o nome do arquivo CSV, incluindo a extensão de arquivo. csv; Por exemplo, `ContosoCase.csv`.
    
5. Pressione **Enter** para continuar a execução do script. 
    
    O script exibe o progresso da criação e execução das pesquisas. Quando o script for concluído, ele retorna ao prompt. 
    
    ![Exemplo de saída da execução do script para criar várias pesquisas de conformidade](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Etapa 4: Executar o script a ser relatado a pesquisa estima

Depois de criar as pesquisas, a próxima etapa é executar um script que exibe um relatório simples do número de ocorrências de pesquisa para cada pesquisa que foi criada na etapa 3. O relatório também inclui o tamanho dos resultados para cada pesquisa e o número total de acertos e o tamanho total de todas as pesquisas. Quando você executa o script de relatórios, você será solicitado para a ID do grupo de pesquisa e um nome de arquivo CSV se você deseja salvar o relatório para um arquivo CSV.
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `SearchReport.ps1`. Salve o arquivo na mesma pasta onde você salvou os outros arquivos.
    
  ```
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\SearchReport.ps1
    ```

3. No prompt do **ID do grupo de busca** , digite o nome de um grupo de pesquisa e pressione **Enter**. Por exemplo `ContosoCase`. Lembre-se de que esse nome diferencia maiusculas de minúsculas, portanto você terá que digitá-lo da mesma maneira fez quando executou o script na etapa 3.
    
4. No prompt do **caminho do arquivo para salvar o relatório para um arquivo CSV (deixe em branco para exibir apenas o relatório)** , digite um nome de arquivo do caminho completo do nome de arquivo (incluindo a extensão de arquivo. csv) se você deseja salvar o relatório para um arquivo CSV. nome do arquivo CSV, incluindo a extensão de arquivo. csv. Por exemplo, você pode digitar `ContosoCaseReport.csv` para salvá-lo no diretório atual, ou você pode digitar `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` salvá-lo em uma pasta diferente. Você também pode deixar o prompt em branco para exibir o relatório, mas não salve-o em um arquivo. 
    
5. Pressione **Enter**.
    
    O script exibe o progresso da criação e execução das pesquisas. Quando o script for concluído, o relatório é exibido. 
    
    ![Executar o relatório de pesquisa para exibir as estimativas para o grupo de pesquisa](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Se a mesma caixa de correio ou site é especificado como um local de conteúdo em mais de uma pesquisa em um grupo de busca, a estimativa de resultados totais no relatório (para o número de itens e o tamanho total) pode incluir resultados para os mesmos itens. Isso ocorre porque a mesma mensagem de email ou o documento será contado mais de uma vez se ela corresponde à consulta de pesquisas diferentes no grupo de pesquisa. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Etapa 5: Executar o script para excluir as pesquisas

Porque você pode estar criando uma grande quantidade de pesquisas, esse último script apenas facilita excluir rapidamente as pesquisas que você criou na etapa 3. Como os scripts, este também solicita a identificação do grupo de busca. Todas as pesquisas com a ID do grupo de busca no nome da pesquisa serão excluídas quando você executar esse script. 
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `DeleteSearches.ps1`. Salve o arquivo na mesma pasta onde você salvou os outros arquivos.
    
  ```
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\DeleteSearches.ps1
    ```

3. No prompt do **ID do grupo de busca** , digite um nome de grupo de pesquisa para as pesquisas que você deseja excluir e pressione **Enter**. Por exemplo, `ContosoCase`. Lembre-se de que esse nome diferencia maiusculas de minúsculas, portanto você terá que digitá-lo da mesma maneira fez quando executou o script na etapa 3.
    
    O script exibe o nome de cada pesquisa que é excluído.
    
    ![Executar o script para excluir as pesquisas no grupo de pesquisa](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
