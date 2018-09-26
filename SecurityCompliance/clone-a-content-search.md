---
title: Como clonar uma pesquisa de conteúdo de segurança do Office 365 &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Use o script do Windows PowerShell neste artigo para clonar rapidamente uma pesquisa de conteúdo existente na segurança &amp; pesquisa Compliane Center. Quando um você clonar uma pesquisa, uma nova pesquisa (com um novo nome) é criada que contém as mesmas propriedades que a pesquisa original. Em seguida, você pode editar a nova pesquisa (alterando a consulta de palavra-chave ou o intervalo de datas) e, em seguida, executá-lo.
ms.openlocfilehash: fd2ea0d8fa812d23e7479b664b13c786a62d5a38
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038044"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="be75e-105">Como clonar uma pesquisa de conteúdo de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="be75e-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="be75e-p102">Criando uma pesquisa de conteúdo na segurança do Office 365 &amp; OneDrive para sites corporativos e Centro de conformidade que procura um monte de caixas de correio ou SharePoint podem levar algum tempo. Especificando para pesquisar os sites também pode ser propenso a erros se você vir a digitar uma URL. Para evitar esses problemas, você pode usar o script do Windows PowerShell neste artigo para clonar rapidamente uma pesquisa de conteúdo existente. Quando um você clonar uma pesquisa, uma nova pesquisa (com um nome diferente) é criada que contém as mesmas propriedades (por exemplo, os locais de conteúdo e consulta de pesquisa) que a pesquisa original. Você pode editar a nova pesquisa (alterando a consulta de palavra-chave ou o intervalo de datas) e executá-lo.</span><span class="sxs-lookup"><span data-stu-id="be75e-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="be75e-111">Por que clonar pesquisas de conteúdo?</span><span class="sxs-lookup"><span data-stu-id="be75e-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="be75e-112">Para comparar os resultados da palavra-chave diferente consultas de pesquisa execute na mesmos locais de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="be75e-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="be75e-113">Para evitar que seja necessário digitem novamente um grande número de locais de conteúdo quando você cria uma nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="be75e-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="be75e-114">Para diminuir o tamanho dos resultados da pesquisa; Por exemplo, se você tiver uma pesquisa que retorne resultados em excesso para exportar, você pode clonar a pesquisa e adicione um critério de pesquisa com base em um intervalo de datas para reduzir o número de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="be75e-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="be75e-115">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="be75e-115">Before you begin</span></span>

- <span data-ttu-id="be75e-116">Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="be75e-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="be75e-p103">O script inclui o tratamento de erros mínimas. A principal finalidade do script é clonar rapidamente uma pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="be75e-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="be75e-119">O script cria uma nova pesquisa de conteúdo, mas não iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="be75e-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="be75e-p104">Esse script leva em consideração se a pesquisa de conteúdo que está sendo clonada é associada a um caso de eDiscovery. Se a pesquisa estiver associada um caso, a nova pesquisa também serão associada com o mesmo caso. Se a pesquisa existente não estiver associada a um caso, a nova pesquisa será listada na página de **pesquisa de conteúdo** na segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="be75e-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="be75e-p105">O script de amostra fornecido neste tópico não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="be75e-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="be75e-128">Etapa 1: Execute o script para clonar uma pesquisa</span><span class="sxs-lookup"><span data-stu-id="be75e-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="be75e-p106">O script nesta etapa criará uma nova pesquisa de conteúdo pela clonagem de um existente. Quando você executar esse script, você precisará das seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="be75e-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="be75e-p107">**Suas credenciais de usuário** - o script usarão suas credenciais para se conectar à segurança &amp; Centro de conformidade para sua organização do Office 365 com o Windows PowerShell. Conforme anteriormente mencionado, você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script.</span><span class="sxs-lookup"><span data-stu-id="be75e-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="be75e-133">**O nome da pesquisa existente** - este é a pesquisa de conteúdo que você deseja clonar.</span><span class="sxs-lookup"><span data-stu-id="be75e-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="be75e-134">**O nome da nova pesquisa que será criado** - se esse valor for deixado em branco, o script criará um nome para a nova pesquisa que é baseado no nome da pesquisa clonada.</span><span class="sxs-lookup"><span data-stu-id="be75e-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="be75e-135">Para clonar uma pesquisa:</span><span class="sxs-lookup"><span data-stu-id="be75e-135">To clone a search:</span></span>
  
1. <span data-ttu-id="be75e-136">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="be75e-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. <span data-ttu-id="be75e-137">Abra o Windows PowerShell e vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="be75e-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="be75e-138">Executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="be75e-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="be75e-139">Quando solicitado a fornecer suas credenciais, digite seu endereço de email e senha e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="be75e-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="be75e-p108">Insira a seguinte informações quando solicitado pelo script. Digite cada parte da informação e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="be75e-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="be75e-142">O nome da pesquisa existente.</span><span class="sxs-lookup"><span data-stu-id="be75e-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="be75e-143">O nome da nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="be75e-143">The name of the new search.</span></span>
    
    <span data-ttu-id="be75e-p109">O script cria a nova pesquisa de conteúdo, mas não iniciá-lo. Isso oferece uma oportunidade para editar e executar a pesquisa na próxima etapa. Você pode exibir as propriedades da nova pesquisa executando o cmdlet **Get-ComplianceSearch** ou indo para a página de **pesquisa de conteúdo** ou de **Descoberta eletrônica** na segurança &amp; Centro de conformidade, dependendo se é ou não a nova pesquisa associados a um caso.</span><span class="sxs-lookup"><span data-stu-id="be75e-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="be75e-147">Etapa 2: Edite e execute a pesquisa clonada na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="be75e-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="be75e-p110">Depois da executar o script para clonar uma pesquisa de conteúdo existente, a próxima etapa é ir para a segurança &amp; Centro de conformidade para editar e executar a nova pesquisa. Conforme anteriormente mencionado, você pode editar uma pesquisa alterando a consulta de pesquisa de palavra-chave e adicionando ou removendo critérios de pesquisa. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="be75e-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="be75e-151">Pesquisa de conteúdo no Office 365</span><span class="sxs-lookup"><span data-stu-id="be75e-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="be75e-152">Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="be75e-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="be75e-153">casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="be75e-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
