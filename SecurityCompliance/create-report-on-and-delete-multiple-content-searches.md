---
title: Criar, relatar e excluir várias pesquisas de conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Saiba como automatizar tarefas de pesquisa de conteúdo, como criar pesquisas e executar relatórios por meio de scripts do PowerShell &amp; no centro de conformidade de segurança do Office 365.
ms.openlocfilehash: 740f3384e5d4f26e09512cc846ad8779bcbc31ef
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670656"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="43c78-103">Criar, relatar e excluir várias pesquisas de conteúdo</span><span class="sxs-lookup"><span data-stu-id="43c78-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="43c78-104">Criar e relatar rapidamente pesquisas de descoberta é geralmente uma etapa importante na descoberta eletrônica e investigações quando você está tentando saber mais sobre os dados subjacentes, e a riqueza e a qualidade das pesquisas.</span><span class="sxs-lookup"><span data-stu-id="43c78-104">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches.</span></span> <span data-ttu-id="43c78-105">Para ajudá-lo a fazer isso, &amp; o centro de conformidade de segurança oferece um conjunto de cmdlets do Windows PowerShell para automatizar tarefas de pesquisa de conteúdo demoradas.</span><span class="sxs-lookup"><span data-stu-id="43c78-105">To help you do this, the Security &amp; Compliance Center offers a set of Windows PowerShell cmdlets to automate time-consuming Content Search tasks.</span></span> <span data-ttu-id="43c78-106">Esses scripts fornecem uma maneira rápida e fácil de criar várias pesquisas e, em seguida, executar relatórios dos resultados estimados da pesquisa que podem ajudá-lo a determinar a quantidade de dados em questão.</span><span class="sxs-lookup"><span data-stu-id="43c78-106">These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question.</span></span> <span data-ttu-id="43c78-107">Você também pode usar os scripts para criar versões diferentes de pesquisas para comparar os resultados que cada um produz.</span><span class="sxs-lookup"><span data-stu-id="43c78-107">You can also use the scripts to create different versions of searches to compare the results each one produces.</span></span> <span data-ttu-id="43c78-108">Esses scripts podem ajudá-lo a identificar e analisar os dados de forma rápida e eficiente.</span><span class="sxs-lookup"><span data-stu-id="43c78-108">These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="43c78-109">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="43c78-109">Before you begin</span></span>

- <span data-ttu-id="43c78-110">Você precisa ser membro do grupo de função Gerenciador de descoberta eletrônica no centro de &amp; conformidade de segurança para executar os scripts descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="43c78-110">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="43c78-111">Para coletar uma lista das URLs para os sites do OneDrive for Business em sua organização que você pode adicionar ao arquivo CSV na etapa 1, consulte [criar uma lista de todos os locais do onedrive em sua organização](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span><span class="sxs-lookup"><span data-stu-id="43c78-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="43c78-112">Certifique-se de salvar todos os arquivos que você criou neste tópico para a mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="43c78-112">Be sure to save all the files that you create in this topic to the same folder.</span></span> <span data-ttu-id="43c78-113">Isso facilitará a execução dos scripts.</span><span class="sxs-lookup"><span data-stu-id="43c78-113">That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="43c78-114">Os scripts incluem um tratamento de erros mínimo.</span><span class="sxs-lookup"><span data-stu-id="43c78-114">The scripts include minimal error handling.</span></span> <span data-ttu-id="43c78-115">Seu objetivo principal é criar, relatar e excluir rapidamente várias pesquisas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="43c78-115">Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="43c78-p104">Os scripts de exemplo fornecidos neste tópico não são compatíveis com nenhum serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos COMO ESTÃO sem qualquer tipo de garantia. A Microsoft também se isenta de todas as garantias implícitas, incluindo sem limitações quaisquer garantias aplicáveis de padrões de comercialização ou de adequação a uma finalidade específica. Todos os riscos decorrentes do uso ou da execução da documentação ou scripts de exemplo serão de sua responsabilidade. De modo algum a Microsoft, seus autores ou qualquer outra pessoa envolvida na criação, produção ou veiculação dos scripts serão considerados responsáveis por quaisquer danos (incluindo sem limitações danos por perda de lucros comerciais, interrupção de negócios, perda de informações comerciais ou outras perdas pecuniárias) resultantes do uso ou da incapacidade de uso da documentação ou scripts de exemplo, mesmo que a Microsoft tenha sido alertada sobre a possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="43c78-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="43c78-121">Etapa 1: criar um arquivo CSV que contenha informações sobre as pesquisas que você deseja executar</span><span class="sxs-lookup"><span data-stu-id="43c78-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="43c78-122">O arquivo de valor separado por vírgula (CSV) que você criou nesta etapa contém uma linha para cada usuário que deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="43c78-122">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search.</span></span> <span data-ttu-id="43c78-123">Você pode pesquisar a caixa de correio do Exchange Online do usuário (que inclui a caixa de correio de arquivo morto, se ela estiver habilitada) e seu site do OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="43c78-123">You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site.</span></span> <span data-ttu-id="43c78-124">Ou você pode pesquisar apenas a caixa de correio ou o site do OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="43c78-124">Or you can search just the mailbox or the OneDrive for Business site.</span></span> <span data-ttu-id="43c78-125">Você também pode pesquisar qualquer site em sua organização do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="43c78-125">You can also search any site in your SharePoint Online organization.</span></span> <span data-ttu-id="43c78-126">O script executado na etapa 3 criará uma pesquisa separada para cada linha no arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="43c78-126">The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="43c78-127">Copie e cole o texto a seguir em um arquivo. txt usando o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="43c78-127">Copy and paste the following text into a .txt file using NotePad.</span></span> <span data-ttu-id="43c78-128">Salve esse arquivo em uma pasta no computador local.</span><span class="sxs-lookup"><span data-stu-id="43c78-128">Save this file to a folder on your local computer.</span></span> <span data-ttu-id="43c78-129">Você também salvará outros scripts nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="43c78-129">You'll save the other scripts to this folder as well.</span></span>
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="43c78-130">A primeira linha, ou linha de cabeçalho, do arquivo lista os parâmetros que serão usados pelo cmdlet **New-ComplianceSearch** (no script na etapa 3) para criar novas pesquisas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="43c78-130">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches.</span></span> <span data-ttu-id="43c78-131">Os nomes dos parâmetros são separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="43c78-131">Each parameter name is separated by a comma.</span></span> <span data-ttu-id="43c78-132">Certifique-se de que não haja espaços na linha de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="43c78-132">Make sure there aren't any spaces in the header row.</span></span> <span data-ttu-id="43c78-133">Cada linha sob a linha de cabeçalho representa os valores de parâmetro de cada pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-133">Each row under the header row represents the parameter values for each search.</span></span> <span data-ttu-id="43c78-134">Certifique-se de substituir os dados de espaço reservado no arquivo CSV pelos dados reais.</span><span class="sxs-lookup"><span data-stu-id="43c78-134">Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="43c78-135">Abra o arquivo. txt no Excel e use as informações da tabela a seguir para editar o arquivo com as informações de cada pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="43c78-136">**Parâmetro**</span><span class="sxs-lookup"><span data-stu-id="43c78-136">**Parameter**</span></span>|<span data-ttu-id="43c78-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43c78-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="43c78-138">O endereço SMTP da caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="43c78-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="43c78-139">A URL do site do OneDrive for Business do usuário ou a URL de qualquer site em sua organização.</span><span class="sxs-lookup"><span data-stu-id="43c78-139">The URL for the user's OneDrive for Business site or the URL for any site in your organization.</span></span> <span data-ttu-id="43c78-140">Para a URL dos sites do OneDrive for Business, use este formato ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `:.</span><span class="sxs-lookup"><span data-stu-id="43c78-140">For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `.</span></span> <span data-ttu-id="43c78-141">Por exemplo,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="43c78-141">For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span></span>  <br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="43c78-142">A consulta de pesquisa para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-142">The search query for the search.</span></span> <span data-ttu-id="43c78-143">Para obter mais informações sobre como criar uma consulta de pesquisa, consulte [keyword queries and Search Conditions for Content Search](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="43c78-143">For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>  <br/> |
    | `StartDate` <br/> |<span data-ttu-id="43c78-144">Para email, a data de ou após uma mensagem foi recebida por um destinatário ou enviada pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="43c78-144">For email, the date on or after a message was received by a recipient or sent by the sender.</span></span> <span data-ttu-id="43c78-145">Para documentos em sites do SharePoint ou do OneDrive for Business, a data da última modificação de um documento.</span><span class="sxs-lookup"><span data-stu-id="43c78-145">For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="43c78-146">Para email, a data de ou antes de uma mensagem foi enviada por um enviado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="43c78-146">For email, the date on or before a message was sent by a sent by the user.</span></span> <span data-ttu-id="43c78-147">Para documentos em sites do SharePoint ou do OneDrive for Business, a data em ou antes da última modificação de um documento.</span><span class="sxs-lookup"><span data-stu-id="43c78-147">For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="43c78-148">Salve o arquivo do Excel como um arquivo CSV em uma pasta no computador local.</span><span class="sxs-lookup"><span data-stu-id="43c78-148">Save the Excel file as a CSV file to a folder on your local computer.</span></span> <span data-ttu-id="43c78-149">O script criado na etapa 3 usará as informações neste arquivo CSV para criar as pesquisas.</span><span class="sxs-lookup"><span data-stu-id="43c78-149">The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="43c78-150">Etapa 2: conectar-se ao Security & central de conformidade do PowerShell</span><span class="sxs-lookup"><span data-stu-id="43c78-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="43c78-151">A próxima etapa é conectar o Windows PowerShell ao centro de &amp; conformidade de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="43c78-151">The next step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="43c78-152">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="43c78-152">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> <span data-ttu-id="43c78-153">Salve o arquivo na mesma pasta em que você salvou o arquivo CSV na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="43c78-153">Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="43c78-154">No computador local, abra o Windows PowerShell, vá para a pasta onde o script criado na etapa anterior está localizado e, em seguida, execute o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="43c78-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="43c78-155">Etapa 3: executar o script para criar e iniciar as pesquisas</span><span class="sxs-lookup"><span data-stu-id="43c78-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="43c78-156">O script nesta etapa criará uma pesquisa de conteúdo separada para cada linha no arquivo CSV que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="43c78-156">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1.</span></span> <span data-ttu-id="43c78-157">Ao executar esse script, você será solicitado a fornecer dois valores:</span><span class="sxs-lookup"><span data-stu-id="43c78-157">When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="43c78-158">**ID do grupo de pesquisa** -este nome oferece uma maneira fácil de organizar as pesquisas criadas a partir do arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="43c78-158">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file.</span></span> <span data-ttu-id="43c78-159">Cada pesquisa criada é nomeada com a ID do grupo de pesquisa e, em seguida, um número é acrescentado ao nome da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-159">Each search that's created is named with the Search Group ID, and then a number is appended to the search name.</span></span> <span data-ttu-id="43c78-160">Por exemplo, se você inserir **ContosoCase** para a ID do grupo de pesquisa, as pesquisas serão nomeadas como **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="43c78-160">For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on.</span></span> <span data-ttu-id="43c78-161">Observe que o nome digitado diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="43c78-161">Note that the name you type is case sensitive.</span></span> <span data-ttu-id="43c78-162">Quando você usa a ID do grupo de pesquisa na etapa 4 e a etapa 5, é necessário usar o mesmo caso que você fez ao criá-la.</span><span class="sxs-lookup"><span data-stu-id="43c78-162">When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="43c78-163">**Arquivo CSV** -o nome do arquivo CSV que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="43c78-163">**CSV file** - The name of the CSV file that you created in Step 1.</span></span> <span data-ttu-id="43c78-164">Certifique-se de incluir o uso do nome de arquivo completo, inclua a extensão de arquivo. csv; por exemplo, `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="43c78-164">Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="43c78-165">Para executar o script:</span><span class="sxs-lookup"><span data-stu-id="43c78-165">To run the script:</span></span>

1. <span data-ttu-id="43c78-166">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `CreateSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="43c78-166">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`.</span></span> <span data-ttu-id="43c78-167">Salve o arquivo na mesma pasta onde você salvou os outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="43c78-167">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
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

2. <span data-ttu-id="43c78-168">No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e execute o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="43c78-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="43c78-169">No prompt **ID do grupo de pesquisa** , digite um nome de grupo de pesquisa e pressione **Enter**. por exemplo, `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="43c78-169">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="43c78-170">Lembre-se de que esse nome diferencia maiúsculas de minúsculas, portanto, você terá que digitá-lo da mesma maneira nas etapas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="43c78-170">Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="43c78-171">No prompt de **arquivo CSV de origem** , digite o nome do arquivo CSV, incluindo a extensão de arquivo. csv; por exemplo, `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="43c78-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="43c78-172">Pressione **Enter** para continuar executando o script.</span><span class="sxs-lookup"><span data-stu-id="43c78-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="43c78-173">O script exibe o progresso da criação e execução das pesquisas.</span><span class="sxs-lookup"><span data-stu-id="43c78-173">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="43c78-174">Quando o script é concluído, ele retorna ao prompt.</span><span class="sxs-lookup"><span data-stu-id="43c78-174">When the script is complete, it returns to the prompt.</span></span> 
    
    ![Exemplo de saída da execução do script para criar várias pesquisas de conformidade](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="43c78-176">Etapa 4: executar o script para relatar as estimativas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="43c78-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="43c78-177">Após criar as pesquisas, a próxima etapa é executar um script que exibe um relatório simples do número de visitas de pesquisa para cada pesquisa criada na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="43c78-177">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3.</span></span> <span data-ttu-id="43c78-178">O relatório também inclui o tamanho dos resultados de cada pesquisa e o número total de acertos e o tamanho total de todas as pesquisas.</span><span class="sxs-lookup"><span data-stu-id="43c78-178">The report also includes the size of results for each search, and the total number of hits and total size of all searches.</span></span> <span data-ttu-id="43c78-179">Ao executar o script de relatório, você será solicitado a solicitar o ID do grupo de pesquisa e um nome de arquivo CSV se quiser salvar o relatório em um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="43c78-179">When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="43c78-180">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `SearchReport.ps1`.</span><span class="sxs-lookup"><span data-stu-id="43c78-180">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`.</span></span> <span data-ttu-id="43c78-181">Salve o arquivo na mesma pasta onde você salvou os outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="43c78-181">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
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

2. <span data-ttu-id="43c78-182">No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e execute o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="43c78-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="43c78-183">No prompt **ID do grupo de pesquisa** , digite um nome de grupo de pesquisa e pressione **Enter**. por exemplo `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="43c78-183">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`.</span></span> <span data-ttu-id="43c78-184">Lembre-se de que esse nome diferencia maiúsculas de minúsculas, portanto, você terá que digitá-la da mesma maneira que fez ao executar o script na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="43c78-184">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="43c78-185">No **caminho do arquivo para salvar o relatório em um arquivo CSV (deixe em branco para exibir o relatório)** , digite um nome de arquivo completo para o caminho de arquivo (incluindo a extensão de arquivo. csv) se quiser salvar o relatório em um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="43c78-185">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file.</span></span> <span data-ttu-id="43c78-186">nome do arquivo CSV, incluindo a extensão de arquivo. csv.</span><span class="sxs-lookup"><span data-stu-id="43c78-186">name of the CSV file, including the .csv file extension.</span></span> <span data-ttu-id="43c78-187">Por exemplo, você poderia digitar `ContosoCaseReport.csv` para salvá-lo no diretório atual ou poderia digitar `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` para salvá-lo em uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="43c78-187">For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder.</span></span> <span data-ttu-id="43c78-188">Você também pode deixar o prompt em branco para exibir o relatório, mas não salvá-lo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="43c78-188">You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="43c78-189">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="43c78-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="43c78-190">O script exibe o progresso da criação e execução das pesquisas.</span><span class="sxs-lookup"><span data-stu-id="43c78-190">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="43c78-191">Quando o script estiver concluído, o relatório será exibido.</span><span class="sxs-lookup"><span data-stu-id="43c78-191">When the script is complete, the report is displayed.</span></span> 
    
    ![Executar o relatório de pesquisa para exibir as estimativas para o grupo de pesquisa](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="43c78-193">Se a mesma caixa de correio ou site for especificado como um local de conteúdo em mais de uma pesquisa em um grupo de pesquisa, a estimativa de resultados total no relatório (para o número de itens e o tamanho total) poderá incluir resultados para os mesmos itens.</span><span class="sxs-lookup"><span data-stu-id="43c78-193">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items.</span></span> <span data-ttu-id="43c78-194">Isso ocorre porque o mesmo documento ou mensagem de email será contado mais de uma vez se corresponder à consulta de pesquisas diferentes no grupo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-194">That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="43c78-195">Etapa 5: executar o script para excluir as pesquisas</span><span class="sxs-lookup"><span data-stu-id="43c78-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="43c78-196">Como você pode estar criando muitas pesquisas, esse último script simplesmente facilita a exclusão rápida das pesquisas que você criou na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="43c78-196">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3.</span></span> <span data-ttu-id="43c78-197">Assim como os outros scripts, isso também solicita a ID do grupo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="43c78-197">Like the other scripts, this one also prompts you for the Search Group ID.</span></span> <span data-ttu-id="43c78-198">Todas as pesquisas com a ID do grupo de pesquisa no nome da pesquisa serão excluídas quando você executar esse script.</span><span class="sxs-lookup"><span data-stu-id="43c78-198">All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="43c78-199">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo. ps1; por exemplo, `DeleteSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="43c78-199">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`.</span></span> <span data-ttu-id="43c78-200">Salve o arquivo na mesma pasta onde você salvou os outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="43c78-200">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
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

2. <span data-ttu-id="43c78-201">No Windows PowerShell, vá para a pasta onde você salvou o script na etapa anterior e execute o script; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="43c78-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="43c78-202">No prompt **ID do grupo de pesquisa** , digite um nome de grupo de pesquisa para as pesquisas que você deseja excluir e pressione **Enter**. por exemplo, `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="43c78-202">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="43c78-203">Lembre-se de que esse nome diferencia maiúsculas de minúsculas, portanto, você terá que digitá-la da mesma maneira que fez ao executar o script na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="43c78-203">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="43c78-204">O script exibe o nome de cada pesquisa que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="43c78-204">The script displays the name of each search that's deleted.</span></span>
    
    ![Executar o script para excluir as pesquisas no grupo de pesquisa](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
