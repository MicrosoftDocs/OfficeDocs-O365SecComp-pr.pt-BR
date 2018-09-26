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
# <a name="use-content-search-in-your-ediscovery-workflow"></a>Usar a pesquisa de conteúdo no seu fluxo de trabalho de descoberta eletrônica

O recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade permite pesquisar todas as caixas de correio em sua organização. Ao contrário de descoberta eletrônica in-loco no Exchange Online (onde você pode pesquisar até 10.000 caixas de correio), não há nenhum limite para o número de caixas de correio de destino em uma única pesquisa. Para cenários que exigem que você realizar pesquisas de toda a organização, você pode usar a pesquisa de conteúdo para todas as caixas de pesquisa. Em seguida, você pode usar os recursos de fluxo de trabalho de descoberta eletrônica In-loco para executar outras tarefas relacionadas a descoberta eletrônica, como colocação de caixas de correio em espera e resultados de pesquisa de exportação. Por exemplo, digamos que você tenha que pesquisar todas as caixas de correio para identificar os responsáveis específicos que estão respondendo de forma a um caso jurídico. Você pode usar a pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar todas as caixas de correio em sua organização para identificar daquelas que estão respondendo de forma ao caso. Em seguida, você pode usar essa lista de caixas de correio dos responsáveis como as caixas de correio de origem para uma pesquisa de descoberta eletrônica In-loco no Exchange Online. Usando In-Place eDiscovery também permite que você colocar um bloqueio nessas caixas de correio de origem, copie os resultados da pesquisa para uma caixa de correio de descoberta e exportar os resultados da pesquisa.
  
Este tópico inclui um script que pode ser executado para criar uma pesquisa de descoberta eletrônica In-loco no Exchange Online usando a lista de caixas de correio de origem e de consulta de pesquisa de uma pesquisa criada na segurança &amp; Centro de conformidade. Aqui está uma visão geral do processo:
  
[Etapa 1: Criar uma Pesquisa de Conteúdo para pesquisar todas as caixas de correio em sua organização](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[Etapa 2: Conectar-se à segurança &amp; Centro de conformidade e o Exchange Online em uma única sessão do PowerShell remota](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[Etapa 3: Execute o script para criar uma pesquisa de Descoberta Eletrônica In-loco na Pesquisa de Conteúdo](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[Etapa 4: Iniciar a pesquisa de Descoberta Eletrônica In-loco](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a>Etapa 1: Criar uma Pesquisa de Conteúdo para pesquisar todas as caixas de correio em sua organização

A primeira etapa é usar a segurança &amp; Centro de conformidade (ou segurança & PowerShell do Centro de conformidade) para criar uma pesquisa de conteúdo que procura por todas as caixas de correio em sua organização. Não há nenhum limite para o número de caixas de correio para uma única pesquisa de conteúdo. Especifique uma consulta de palavra-chave apropriada (ou uma consulta para tipos de informações confidenciais) para que a pesquisa retornar somente as caixas de fonte que são relevantes para a investigação. Se necessário, refine a consulta de pesquisa para restringir o escopo dos resultados da pesquisa e caixas de correio de origem que são retornadas.
  
> [!NOTE]
> Se a pesquisa de conteúdo de origem não retornar qualquer resultado, a Descoberta Eletrônica In-loco não será criada quando você executar o script na Etapa 3. Talvez seja necessário revisar a consulta de pesquisa e executar novamente a pesquisa de conteúdo para retornar os resultados de pesquisa. 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a>Usar a segurança &amp; Centro de conformidade para pesquisar todas as caixas de correio

1. [Ir para a segurança do Office 365 &amp; Centro de conformidade](go-to-the-securitycompliance-center.md). 
    
2. Clique em **pesquisa &amp; investigação**, clique em **pesquisa de conteúdo**e, em seguida, clique em **novo** ![ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
3. Na página **Nova pesquisa**, digite um nome para a pesquisa de conteúdo. 
    
4. Em **Onde você deseja que procuremos?**, clique em **Pesquisar todas as caixas de correio** e clique em **Avançar**.
    
5. Na caixa em **que você deseja fazer conosco para procurar?**, digite uma consulta de pesquisa na caixa. Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que utilizam um operador booleano, como AND, OR, não ou próximo ou, você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) nas mensagens. Para obter mais informações sobre como criar consultas de pesquisa, consulte [consultas de palavra-chave de pesquisa de conteúdo](keyword-queries-and-search-conditions.md).
    
6. Clique em **Pesquisar** para salvar as configurações da pesquisa e iniciá-la. 
    
    Após algum tempo, uma estimativa dos resultados da pesquisa são exibidos no painel de detalhes. A estimativa inclui o tamanho total e o número de itens para os resultados da pesquisa. Uma vez concluída a pesquisa, você pode visualizar os resultados da pesquisa. Se necessário, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes. 
    
7.  Se for necessário, refine a consulta de pesquisa para restringir o escopo dos resultados da pesquisa e reinicie a pesquisa. 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a>Usar o PowerShell do Centro de conformidade & segurança para pesquisar todas as caixas de correio

Você também pode usar o cmdlet **New-ComplianceSearch** para pesquisar todas as caixas de correio em sua organização. A primeira etapa é [conectar a segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkID=627084).
  
Aqui está um exemplo de como usar o PowerShell para pesquisar todas as caixas de correio em sua organização. A consulta de pesquisa retorna todas as mensagens enviadas entre 1º de janeiro de 2015 e 30 de junho de 2015 e que contenham a frase "relatório financeiro" na linha de assunto. O primeiro comando cria a pesquisa e o segundo comando executa a pesquisa. 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

Para obter mais informações, consulte [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a>Verifique o número de caixas de correio de origem na pesquisa de conteúdo

Uma pesquisa de conteúdo retorna um máximo de 1.000 caixas de correio de origem que contêm os resultados da pesquisa. Se houver mais de 1.000 caixas de correio que contém conteúdo que corresponde à consulta de pesquisa, somente as caixas de correio de cima 1.000 com a maioria dos resultados de pesquisa estão incluídas na pesquisa de conteúdo que você criou na etapa anterior. Isso se mais de 1.000 caixas de correio contêm os resultados da pesquisa, algumas dessas caixas de correio não serão incluídas na lista de caixas de correio de origem copiado para a nova pesquisa de descoberta eletrônica In-loco criada na etapa 3. 
  
Para ajudá-lo a criar uma pesquisa de conteúdo com não mais de caixas de correio de origem 1.000, siga estas etapas para executar um script que exibe o número de caixas de correio de origem (que contenham os resultados da pesquisa) retornado pela pesquisa de conteúdo que você criou na etapa 1. 
  
1. Salve o seguinte texto em um arquivo de script do PowerShell usando um sufixo de nome de arquivo de. ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `SourceMailboxes.ps1`.
    
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

2. Na & PowerShell do Centro de conformidade de segurança, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\SourceMailboxes.ps1
    ```

3. Quando receber a solicitação pelo script, digite o nome da pesquisa de conteúdo criada na Etapa 1.
    
    O script exibe o número de caixas de correio de origem que contêm os resultados de pesquisa.
    
Se houver mais de 1.000 caixas de correio de origem, tente criar pesquisas de conteúdo duas (ou mais). Por exemplo, pesquise metade das caixas de correio da sua organização em uma pesquisa de conteúdo e a outra metade na pesquisa de conteúdo de outro. Você também pode alterar os critérios de pesquisa para reduzir o número de caixas de correio que contêm os resultados da pesquisa. Por exemplo, você pode incluir um intervalo de datas ou refinar a consulta de palavra-chave.
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Etapa 2: Conectar-se à segurança &amp; Centro de conformidade e o Exchange Online em uma única sessão do PowerShell remota

A próxima etapa é conectar o Windows PowerShell para ambos os a segurança &amp; Centro de conformidade e para sua organização do Exchange Online. Isso é necessário porque o script que você pode executar na etapa 3 requer acesso para os cmdlets de pesquisa de conteúdo na segurança &amp; Centro de conformidade e os cmdlets de descoberta eletrônica In-loco no Exchange Online.
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell, usando um sufixo de nome de arquivo de. ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `ConnectEXO-CC.ps1`.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. No computador local, abra o Windows PowerShell, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\ConnectEXO-CC.ps1
    ```

Como verifico se isso funcionou? Depois de executar o script, os cmdlets de segurança &amp; Centro de conformidade e o Exchange Online são importados para a sua sessão local do PowerShell. Se você não receber algum erro, você conectado com êxito. Um teste rápido é executada uma segurança &amp; cmdlet do Centro de conformidade — por exemplo, **Install-UnifiedCompliancePrerequisite** — e um cmdlet do Exchange Online, como **Get-Mailbox**. 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a>Etapa 3: Execute o script para criar uma pesquisa de Descoberta Eletrônica In-loco na Pesquisa de Conteúdo

Depois de criar a sessão do PowerShell dual na etapa 2, a próxima etapa é executar um script que irá converter uma pesquisa de conteúdo existente para uma pesquisa de descoberta eletrônica In-loco. Aqui está o que significa o script:
  
- Solicita o nome da pesquisa de conteúdo para a conversão.
    
- Verifica se a pesquisa de conteúdo foi concluída. Se a pesquisa de conteúdo não retornar resultados, e a Descoberta Eletrônica In-loco não for criada.
    
- Salva uma lista das caixas de correio de origem da pesquisa de conteúdo que contêm os resultados de pesquisa para uma variável.
    
- Cria uma nova pesquisa de Descoberta Eletrônica In-loco, com as seguintes propriedades. Observe que a nova pesquisa não foi iniciada. Você poderá iniciá-la na Etapa 4.
    
  - **Nome** - o nome da nova pesquisa usa este formato: \<nome de pesquisa de conteúdo\>_MBSearch1. Se você executar o script novamente e usar a mesma fonte de conteúdo de pesquisa, a pesquisa será denominada \<nome de pesquisa de conteúdo\>_MBSearch2.
    
  - **Caixas de correio de origem** - todas as caixas de pesquisa o conteúdo que contêm os resultados da pesquisa. 
    
  - **Consulta de pesquisa** - a nova pesquisa usa a consulta de pesquisa da pesquisa de conteúdo. Se a pesquisa de conteúdo inclui todo o conteúdo (onde a consulta de pesquisa está em branco) a nova pesquisa também terão uma consulta de pesquisa em branco e incluirá todo o conteúdo encontrado nas caixas de correio de origem. 
    
  - **Estimar a pesquisa somente** - a nova pesquisa está marcado como uma pesquisa somente estimativa. Ele não copiar os resultados da pesquisa para uma caixa de correio de descoberta depois de você iniciá-lo. 
    
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de ps1. Por exemplo, você poderia salvá-la para um arquivo chamado `CreateMBSearchFromComplianceSearch.ps1`.
    
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

2. Na sessão do Windows PowerShell que você criou na etapa 2, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, executar o script; Por exemplo:
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. Quando solicitado pelo script, digite o nome da pesquisa de conteúdo que você deseja converter para uma pesquisa de descoberta eletrônica In-loco (por exemplo, a pesquisa que você criou na etapa 1) e pressione **Enter**.
    
    Se o script for bem-sucedida, uma nova pesquisa de descoberta eletrônica In-loco é criada com um status de **NotStarted**. Execute o comando `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` para exibir as propriedades da nova pesquisa. 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a>Etapa 4: Iniciar a pesquisa de Descoberta Eletrônica In-loco

O script executado na Etapa 3 cria uma nova pesquisa de Descoberta Eletrônica In-loco, mas não a inicia. A próxima etapa é iniciar a pesquisa para que você possa obter uma estimativa dos resultados da pesquisa.
  
1. No Centro de administração do Exchange (EAC), vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
2. No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco que você criou na Etapa 3.
    
3. Clique em **Pesquisar** ![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **resultados da pesquisa de estimativa** para iniciar a pesquisa e retornar uma estimativa do tamanho total e o número de itens retornados pela pesquisa. 
    
    As estimativas são exibidas no painel de detalhes. Clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações exibidas no painel de detalhes. 
    
4. Para visualizar os resultados após a conclusão da pesquisa, clique em **Visualizar resultados da pesquisa** no painel de detalhes.
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a>Próximas etapas após a criação e execução da pesquisa de Descoberta Eletrônica In-loco

Depois de criar e iniciar a pesquisa de Descoberta Eletrônica In-loco criada pelo script na Etapa 3, você pode usar o fluxo de trabalho normal de Descoberta Eletrônica In-loco para executar ações de Descoberta Eletrônica diferentes nos resultados da pesquisa.
  
### <a name="create-an-in-place-hold"></a>Criar um Bloqueio In-loco

1. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
2. Na exibição de lista, selecione a pesquisa de descoberta eletrônica In-loco que você criou na etapa 3 e clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
3. Na página **Bloqueio In-loco**, marque a caixa de seleção **Colocar conteúdo correspondente à consulta de pesquisa nas caixas de correio selecionadas em bloqueio** e selecione uma das seguintes opções: 
    
  - **Reter indefinidamente** - escolher esta opção para colocar os itens retornados pela pesquisa em um bloqueio indefinido. Itens em espera serão preservadas até que você remova a caixa de correio de pesquisa ou remover a pesquisa. 
    
  - **Especificar o número de dias para reter itens em relação à sua data de recebimento** - escolher esta opção para reter itens por um período específico. A duração é calculada a partir da data de um item de caixa de correio é recebido ou criado. 
    
4. Clique em **Salvar** para criar o Bloqueio In-loco e reiniciar a pesquisa. 
    
[Return to top](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a>Copiar os resultados da pesquisa

1. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
2. No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco que você criou na Etapa 3.
    
3. Clique em **Pesquisar** ![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)e clique em **resultados da pesquisa de cópia** da lista suspensa. 
    
4. Em **Copiar Resultados da Pesquisa**, selecione uma das seguintes opções:
    
    - **Incluir itens não pesquisáveis** - marque essa caixa de seleção para incluir os itens de caixa de correio que não puderam ser pesquisados (por exemplo, mensagens com anexos de tipos de arquivo que não puderam ser indexados pela pesquisa do Exchange). 
    
    - **Habilitar Desfazer duplicação** - marque essa caixa de seleção para excluir mensagens duplicadas. Somente uma única instância de uma mensagem será copiada para a caixa de correio de descoberta. 
    
    - **Habilitar o log completo** - marque essa caixa de seleção para incluir um log completo nos resultados da pesquisa. 
    
    - **Envie uma mensagem quando a cópia for concluída** - marque essa caixa de seleção para obter uma notificação por e-mail quando a pesquisa é concluída. 
    
    - **Copiar os resultados para esta caixa de correio de descoberta** - clique em **Procurar** para selecionar a caixa de correio de descoberta onde deseja que os resultados da pesquisa copiado para. 
    
5. Clique em **Copiar** para iniciar o processo de cópia dos resultados da pesquisa para a caixa de correio de descoberta especificada. 
    
6. Clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações sobre o status de cópia que é exibido no painel de detalhes. 
    
7. Após a conclusão da cópia, clique em **Abrir** para abrir a caixa de correio de descoberta e exibir os resultados da pesquisa. 
  
### <a name="export-the-search-results"></a>Exportar os resultados da pesquisa

1. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
2. No modo de exibição de lista, selecione a pesquisa de Descoberta Eletrônica In-loco criada na Etapa 3 e clique em **Exportar para um arquivo PST**.
    
3. Na janela **Ferramenta de Exportação de PST de Descoberta Eletrônica**, faça o seguinte: 
    
    - Clique em **Procurar** para especificar o local para o qual você deseja baixar o arquivo PST. 
    
    - Clique na caixa de seleção **Habilitar deduplicação** para excluir as mensagens duplicadas. Somente uma única instância de uma mensagem será incluída no arquivo PST. 
    
    - Clique na caixa de seleção **Incluir itens não pesquisáveis** para incluir itens da caixa de correio que não puderam ser pesquisados (por exemplo, mensagens com anexos dos tipos de arquivo que não puderam ser indexadas pela Pesquisa do Exchange). Os itens não pesquisáveis são exportados para um arquivo PST separado. 
    
4. Clique em **Iniciar** para exportar os resultados da pesquisa para um arquivo PST. 
    
    Uma janela é exibida contendo as informações do status sobre o processo de exportação.
