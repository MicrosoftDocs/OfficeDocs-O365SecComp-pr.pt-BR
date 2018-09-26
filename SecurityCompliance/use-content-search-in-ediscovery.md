---
title: Usar a pesquisa de conteúdo no seu fluxo de trabalho de descoberta eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Usar um script do PowerShell para criar uma pesquisa de descoberta eletrônica In-loco no Exchange Online com base em uma pesquisa criada no Office 365 Security &amp; Centro de conformidade. '
ms.openlocfilehash: 42af94ce850736dede52e619c240bb9e0a6f7031
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038064"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="ea90e-103">Usar a pesquisa de conteúdo no seu fluxo de trabalho de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="ea90e-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="ea90e-p101">O recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade permite pesquisar todas as caixas de correio em sua organização. Ao contrário de descoberta eletrônica in-loco no Exchange Online (onde você pode pesquisar até 10.000 caixas de correio), não há nenhum limite para o número de caixas de correio de destino em uma única pesquisa. Para cenários que exigem que você realizar pesquisas de toda a organização, você pode usar a pesquisa de conteúdo para todas as caixas de pesquisa. Em seguida, você pode usar os recursos de fluxo de trabalho de descoberta eletrônica In-loco para executar outras tarefas relacionadas a descoberta eletrônica, como colocação de caixas de correio em espera e resultados de pesquisa de exportação. Por exemplo, digamos que você tenha que pesquisar todas as caixas de correio para identificar os responsáveis específicos que estão respondendo de forma a um caso jurídico. Você pode usar a pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar todas as caixas de correio em sua organização para identificar daquelas que estão respondendo de forma ao caso. Em seguida, você pode usar essa lista de caixas de correio dos responsáveis como as caixas de correio de origem para uma pesquisa de descoberta eletrônica In-loco no Exchange Online. Usando In-Place eDiscovery também permite que você colocar um bloqueio nessas caixas de correio de origem, copie os resultados da pesquisa para uma caixa de correio de descoberta e exportar os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="ea90e-p102">Este tópico inclui um script que pode ser executado para criar uma pesquisa de descoberta eletrônica In-loco no Exchange Online usando a lista de caixas de correio de origem e de consulta de pesquisa de uma pesquisa criada na segurança &amp; Centro de conformidade. Aqui está uma visão geral do processo:</span><span class="sxs-lookup"><span data-stu-id="ea90e-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="ea90e-114">Etapa 1: Criar uma Pesquisa de Conteúdo para pesquisar todas as caixas de correio em sua organização</span><span class="sxs-lookup"><span data-stu-id="ea90e-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="ea90e-115">Etapa 2: Conectar-se à segurança &amp; Centro de conformidade e o Exchange Online em uma única sessão do PowerShell remota</span><span class="sxs-lookup"><span data-stu-id="ea90e-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="ea90e-116">Etapa 3: Execute o script para criar uma pesquisa de Descoberta Eletrônica In-loco na Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea90e-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="ea90e-117">Etapa 4: Iniciar a pesquisa de Descoberta Eletrônica In-loco</span><span class="sxs-lookup"><span data-stu-id="ea90e-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="ea90e-118">Etapa 1: Criar uma Pesquisa de Conteúdo para pesquisar todas as caixas de correio em sua organização</span><span class="sxs-lookup"><span data-stu-id="ea90e-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="ea90e-p103">A primeira etapa é usar a segurança &amp; Centro de conformidade (ou segurança & PowerShell do Centro de conformidade) para criar uma pesquisa de conteúdo que procura por todas as caixas de correio em sua organização. Não há nenhum limite para o número de caixas de correio para uma única pesquisa de conteúdo. Especifique uma consulta de palavra-chave apropriada (ou uma consulta para tipos de informações confidenciais) para que a pesquisa retornar somente as caixas de fonte que são relevantes para a investigação. Se necessário, refine a consulta de pesquisa para restringir o escopo dos resultados da pesquisa e caixas de correio de origem que são retornadas.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ea90e-p104">Se a pesquisa de conteúdo de origem não retornar qualquer resultado, a Descoberta Eletrônica In-loco não será criada quando você executar o script na Etapa 3. Talvez seja necessário revisar a consulta de pesquisa e executar novamente a pesquisa de conteúdo para retornar os resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="ea90e-125">Usar a segurança &amp; Centro de conformidade para pesquisar todas as caixas de correio</span><span class="sxs-lookup"><span data-stu-id="ea90e-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="ea90e-126">[Ir para a segurança do Office 365 &amp; Centro de conformidade](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="ea90e-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="ea90e-127">Clique em **pesquisa &amp; investigação**, clique em **pesquisa de conteúdo**e, em seguida, clique em **novo** ![ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="ea90e-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="ea90e-128">Na página **Nova pesquisa**, digite um nome para a pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ea90e-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="ea90e-129">Em **Onde você deseja que procuremos?**, clique em **Pesquisar todas as caixas de correio** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="ea90e-p105">Na caixa em **que você deseja fazer conosco para procurar?**, digite uma consulta de pesquisa na caixa. Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que utilizam um operador booleano, como AND, OR, não ou próximo ou, você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) nas mensagens. Para obter mais informações sobre como criar consultas de pesquisa, consulte [consultas de palavra-chave de pesquisa de conteúdo](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="ea90e-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="ea90e-134">Clique em **Pesquisar** para salvar as configurações da pesquisa e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="ea90e-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="ea90e-p106">Após algum tempo, uma estimativa dos resultados da pesquisa são exibidos no painel de detalhes. A estimativa inclui o tamanho total e o número de itens para os resultados da pesquisa. Uma vez concluída a pesquisa, você pode visualizar os resultados da pesquisa. Se necessário, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="ea90e-139">Se for necessário, refine a consulta de pesquisa para restringir o escopo dos resultados da pesquisa e reinicie a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="ea90e-140">Usar o PowerShell do Centro de conformidade & segurança para pesquisar todas as caixas de correio</span><span class="sxs-lookup"><span data-stu-id="ea90e-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="ea90e-p107">Você também pode usar o cmdlet **New-ComplianceSearch** para pesquisar todas as caixas de correio em sua organização. A primeira etapa é [conectar a segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="ea90e-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="ea90e-p108">Aqui está um exemplo de como usar o PowerShell para pesquisar todas as caixas de correio em sua organização. A consulta de pesquisa retorna todas as mensagens enviadas entre 1º de janeiro de 2015 e 30 de junho de 2015 e que contenham a frase "relatório financeiro" na linha de assunto. O primeiro comando cria a pesquisa e o segundo comando executa a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="ea90e-146">Para obter mais informações, consulte [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="ea90e-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="ea90e-147">Verifique o número de caixas de correio de origem na pesquisa de conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea90e-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="ea90e-p109">Uma pesquisa de conteúdo retorna um máximo de 1.000 caixas de correio de origem que contêm os resultados da pesquisa. Se houver mais de 1.000 caixas de correio que contém conteúdo que corresponde à consulta de pesquisa, somente as caixas de correio de cima 1.000 com a maioria dos resultados de pesquisa estão incluídas na pesquisa de conteúdo que você criou na etapa anterior. Isso se mais de 1.000 caixas de correio contêm os resultados da pesquisa, algumas dessas caixas de correio não serão incluídas na lista de caixas de correio de origem copiado para a nova pesquisa de descoberta eletrônica In-loco criada na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="ea90e-151">Para ajudá-lo a criar uma pesquisa de conteúdo com não mais de caixas de correio de origem 1.000, siga estas etapas para executar um script que exibe o número de caixas de correio de origem (que contenham os resultados da pesquisa) retornado pela pesquisa de conteúdo que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="ea90e-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="ea90e-p110">Salve o seguinte texto em um arquivo de script do PowerShell usando um sufixo de nome de arquivo de. ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `SourceMailboxes.ps1`.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
                  "Please wait until the search finishes.";
                  break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
                  "The Content Search " + $SearchName + " didn't return any useful results.";
                  break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  "Number of mailboxes that have search hits: " + $mailboxes.Count
  ```

2. <span data-ttu-id="ea90e-154">Na & PowerShell do Centro de conformidade de segurança, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ea90e-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="ea90e-155">Quando receber a solicitação pelo script, digite o nome da pesquisa de conteúdo criada na Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="ea90e-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="ea90e-156">O script exibe o número de caixas de correio de origem que contêm os resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="ea90e-p111">Se houver mais de 1.000 caixas de correio de origem, tente criar pesquisas de conteúdo duas (ou mais). Por exemplo, pesquise metade das caixas de correio da sua organização em uma pesquisa de conteúdo e a outra metade na pesquisa de conteúdo de outro. Você também pode alterar os critérios de pesquisa para reduzir o número de caixas de correio que contêm os resultados da pesquisa. Por exemplo, você pode incluir um intervalo de datas ou refinar a consulta de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="ea90e-161">Etapa 2: Conectar-se à segurança &amp; Centro de conformidade e o Exchange Online em uma única sessão do PowerShell remota</span><span class="sxs-lookup"><span data-stu-id="ea90e-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="ea90e-p112">A próxima etapa é conectar o Windows PowerShell para ambos os a segurança &amp; Centro de conformidade e para sua organização do Exchange Online. Isso é necessário porque o script que você pode executar na etapa 3 requer acesso para os cmdlets de pesquisa de conteúdo na segurança &amp; Centro de conformidade e os cmdlets de descoberta eletrônica In-loco no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="ea90e-p113">Salve o seguinte texto em um arquivo de script do Windows PowerShell, usando um sufixo de nome de arquivo de. ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `ConnectEXO-CC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="ea90e-166">No computador local, abra o Windows PowerShell, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ea90e-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="ea90e-p114">Como verifico se isso funcionou? Depois de executar o script, os cmdlets de segurança &amp; Centro de conformidade e o Exchange Online são importados para a sua sessão local do PowerShell. Se você não receber algum erro, você conectado com êxito. Um teste rápido é executada uma segurança &amp; cmdlet do Centro de conformidade — por exemplo, **Install-UnifiedCompliancePrerequisite** — e um cmdlet do Exchange Online, como **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="ea90e-171">Etapa 3: Execute o script para criar uma pesquisa de Descoberta Eletrônica In-loco na Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="ea90e-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="ea90e-p115">Depois de criar a sessão do PowerShell dual na etapa 2, a próxima etapa é executar um script que irá converter uma pesquisa de conteúdo existente para uma pesquisa de descoberta eletrônica In-loco. Aqui está o que significa o script:</span><span class="sxs-lookup"><span data-stu-id="ea90e-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="ea90e-174">Solicita o nome da pesquisa de conteúdo para a conversão.</span><span class="sxs-lookup"><span data-stu-id="ea90e-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="ea90e-p116">Verifica se a pesquisa de conteúdo foi concluída. Se a pesquisa de conteúdo não retornar resultados, e a Descoberta Eletrônica In-loco não for criada.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="ea90e-177">Salva uma lista das caixas de correio de origem da pesquisa de conteúdo que contêm os resultados de pesquisa para uma variável.</span><span class="sxs-lookup"><span data-stu-id="ea90e-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="ea90e-p117">Cria uma nova pesquisa de Descoberta Eletrônica In-loco, com as seguintes propriedades. Observe que a nova pesquisa não foi iniciada. Você poderá iniciá-la na Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="ea90e-p118">**Nome** - o nome da nova pesquisa usa este formato: \<nome de pesquisa de conteúdo\>_MBSearch1. Se você executar o script novamente e usar a mesma fonte de conteúdo de pesquisa, a pesquisa será denominada \<nome de pesquisa de conteúdo\>_MBSearch2.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="ea90e-183">**Caixas de correio de origem** - todas as caixas de pesquisa o conteúdo que contêm os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="ea90e-p119">**Consulta de pesquisa** - a nova pesquisa usa a consulta de pesquisa da pesquisa de conteúdo. Se a pesquisa de conteúdo inclui todo o conteúdo (onde a consulta de pesquisa está em branco) a nova pesquisa também terão uma consulta de pesquisa em branco e incluirá todo o conteúdo encontrado nas caixas de correio de origem.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="ea90e-p120">**Estimar a pesquisa somente** - a nova pesquisa está marcado como uma pesquisa somente estimativa. Ele não copiar os resultados da pesquisa para uma caixa de correio de descoberta depois de você iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="ea90e-p121">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `CreateMBSearchFromComplianceSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName,
      [switch]$original,
      [switch]$restoreOriginal
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
    "Please wait until the search finishes";
    break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
    "The Content Search " + $SearchName + " didn't return any useful results";
    "A mailbox search object wasn't created";
    break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  $msPrefix = $SearchName + "_MBSearch";
  $I = 1;
  $mbSearches = Get-MailboxSearch;
  while ($true)
  {
      $found = $false;
      $mbsName = "$msPrefix$I";
      foreach ($mbs in $mbSearches)
      {
          if ($mbs.Name -eq $mbsName)
          {
              $found = $true;
              break;
          }
      }
      if (!$found)
      {
          break;
      }
      $I++;
  }
  $query = $search.KeywordQuery;
  if ([string]::IsNullOrWhiteSpace($query))
  {
      $query = $search.ContentMatchQuery;
  }
  if ([string]::IsNullOrWhiteSpace($query))
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -EstimateOnly;
  }
  else
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -SearchQuery $query -EstimateOnly;
  }
  
  ```

2. <span data-ttu-id="ea90e-190">Na sessão do Windows PowerShell que você criou na etapa 2, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ea90e-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="ea90e-191">Quando solicitado pelo script, digite o nome da pesquisa de conteúdo que você deseja converter para uma pesquisa de descoberta eletrônica In-loco (por exemplo, a pesquisa que você criou na etapa 1) e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="ea90e-p122">Se o script for bem-sucedida, uma nova pesquisa de descoberta eletrônica In-loco é criada com um status de **NotStarted**. Execute o comando `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` para exibir as propriedades da nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="ea90e-194">Etapa 4: Iniciar a pesquisa de Descoberta Eletrônica In-loco</span><span class="sxs-lookup"><span data-stu-id="ea90e-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="ea90e-p123">O script executado na Etapa 3 cria uma nova pesquisa de Descoberta Eletrônica In-loco, mas não a inicia. A próxima etapa é iniciar a pesquisa para que você possa obter uma estimativa dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="ea90e-197">No Centro de administração do Exchange (EAC), vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="ea90e-198">No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco que você criou na Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ea90e-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="ea90e-199">Clique em **Pesquisar** ![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **resultados da pesquisa de estimativa** para iniciar a pesquisa e retornar uma estimativa do tamanho total e o número de itens retornados pela pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="ea90e-p124">As estimativas são exibidas no painel de detalhes. Clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações exibidas no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="ea90e-202">Para visualizar os resultados após a conclusão da pesquisa, clique em **Visualizar resultados da pesquisa** no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="ea90e-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="ea90e-203">Próximas etapas após a criação e execução da pesquisa de Descoberta Eletrônica In-loco</span><span class="sxs-lookup"><span data-stu-id="ea90e-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="ea90e-204">Depois de criar e iniciar a pesquisa de Descoberta Eletrônica In-loco criada pelo script na Etapa 3, você pode usar o fluxo de trabalho normal de Descoberta Eletrônica In-loco para executar ações de Descoberta Eletrônica diferentes nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="ea90e-205">Criar um Bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="ea90e-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="ea90e-206">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="ea90e-207">Na exibição de lista, selecione a pesquisa de descoberta eletrônica In-loco que você criou na etapa 3 e clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="ea90e-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="ea90e-208">Na página **Bloqueio In-loco**, marque a caixa de seleção **Colocar conteúdo correspondente à consulta de pesquisa nas caixas de correio selecionadas em bloqueio** e selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="ea90e-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="ea90e-p125">**Reter indefinidamente** - escolher esta opção para colocar os itens retornados pela pesquisa em um bloqueio indefinido. Itens em espera serão preservadas até que você remova a caixa de correio de pesquisa ou remover a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="ea90e-p126">**Especificar o número de dias para reter itens em relação à sua data de recebimento** - escolher esta opção para reter itens por um período específico. A duração é calculada a partir da data de um item de caixa de correio é recebido ou criado.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="ea90e-213">Clique em **Salvar** para criar o Bloqueio In-loco e reiniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="ea90e-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="ea90e-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="ea90e-215">Copiar os resultados da pesquisa</span><span class="sxs-lookup"><span data-stu-id="ea90e-215">Copy the search results</span></span>

1. <span data-ttu-id="ea90e-216">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="ea90e-217">No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco que você criou na Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ea90e-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="ea90e-218">Clique em **Pesquisar** ![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)e clique em **resultados da pesquisa de cópia** da lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="ea90e-219">Em **Copiar Resultados da Pesquisa**, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="ea90e-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="ea90e-220">**Incluir itens não pesquisáveis** - marque essa caixa de seleção para incluir os itens de caixa de correio que não puderam ser pesquisados (por exemplo, mensagens com anexos de tipos de arquivo que não puderam ser indexados pela pesquisa do Exchange).</span><span class="sxs-lookup"><span data-stu-id="ea90e-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="ea90e-p127">**Habilitar Desfazer duplicação** - marque essa caixa de seleção para excluir mensagens duplicadas. Somente uma única instância de uma mensagem será copiada para a caixa de correio de descoberta.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="ea90e-223">**Habilitar o log completo** - marque essa caixa de seleção para incluir um log completo nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="ea90e-224">**Envie uma mensagem quando a cópia for concluída** - marque essa caixa de seleção para obter uma notificação por e-mail quando a pesquisa é concluída.</span><span class="sxs-lookup"><span data-stu-id="ea90e-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="ea90e-225">**Copiar os resultados para esta caixa de correio de descoberta** - clique em **Procurar** para selecionar a caixa de correio de descoberta onde deseja que os resultados da pesquisa copiado para.</span><span class="sxs-lookup"><span data-stu-id="ea90e-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="ea90e-226">Clique em **Copiar** para iniciar o processo de cópia dos resultados da pesquisa para a caixa de correio de descoberta especificada.</span><span class="sxs-lookup"><span data-stu-id="ea90e-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="ea90e-227">Clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações sobre o status de cópia que é exibido no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="ea90e-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="ea90e-228">Após a conclusão da cópia, clique em **Abrir** para abrir a caixa de correio de descoberta e exibir os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea90e-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="ea90e-229">Exportar os resultados da pesquisa</span><span class="sxs-lookup"><span data-stu-id="ea90e-229">Export the search results</span></span>

1. <span data-ttu-id="ea90e-230">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="ea90e-231">No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco criada na Etapa 3 e clique em **Exportar para um arquivo PST**.</span><span class="sxs-lookup"><span data-stu-id="ea90e-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="ea90e-232">Na janela **Ferramenta de Exportação de PST de Descoberta Eletrônica**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea90e-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="ea90e-233">Clique em **Procurar** para especificar o local para o qual você deseja baixar o arquivo PST.</span><span class="sxs-lookup"><span data-stu-id="ea90e-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="ea90e-p128">Clique na caixa de seleção **Habilitar deduplicação** para excluir as mensagens duplicadas. Somente uma única instância de uma mensagem será incluída no arquivo PST.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="ea90e-p129">Clique na caixa de seleção **Incluir itens não pesquisáveis** para incluir itens da caixa de correio que não puderam ser pesquisados (por exemplo, mensagens com anexos dos tipos de arquivo que não puderam ser indexadas pela Pesquisa do Exchange). Os itens não pesquisáveis são exportados para um arquivo PST separado.</span><span class="sxs-lookup"><span data-stu-id="ea90e-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="ea90e-238">Clique em **Iniciar** para exportar os resultados da pesquisa para um arquivo PST.</span><span class="sxs-lookup"><span data-stu-id="ea90e-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="ea90e-239">Uma janela é exibida contendo as informações do status sobre o processo de exportação.</span><span class="sxs-lookup"><span data-stu-id="ea90e-239">A window is displayed that contains status information about the export process.</span></span>
