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
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Use o script do Windows PowerShell neste artigo para clonar rapidamente uma pesquisa de conteúdo existente na segurança &amp; pesquisa Compliane Center. Quando um você clonar uma pesquisa, uma nova pesquisa (com um novo nome) é criada que contém as mesmas propriedades que a pesquisa original. Em seguida, você pode editar a nova pesquisa (alterando a consulta de palavra-chave ou o intervalo de datas) e, em seguida, executá-lo.
ms.openlocfilehash: a4f801e3de281e8caf8aeb7d1c2bd48f0facb77c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523927"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Como clonar uma pesquisa de conteúdo de segurança do Office 365 &amp; Centro de conformidade

Criando uma pesquisa de conteúdo na segurança do Office 365 &amp; OneDrive para sites corporativos e Centro de conformidade que procura um monte de caixas de correio ou SharePoint podem levar algum tempo. Especificando para pesquisar os sites também pode ser propenso a erros se você vir a digitar uma URL. Para evitar esses problemas, você pode usar o script do Windows PowerShell neste artigo para clonar rapidamente uma pesquisa de conteúdo existente. Quando um você clonar uma pesquisa, uma nova pesquisa (com um nome diferente) é criada que contém as mesmas propriedades (por exemplo, os locais de conteúdo e consulta de pesquisa) que a pesquisa original. Você pode editar a nova pesquisa (alterando a consulta de palavra-chave ou o intervalo de datas) e executá-lo.
  
Por que clonar pesquisas de conteúdo?
  
- Para comparar os resultados da palavra-chave diferente consultas de pesquisa execute na mesmos locais de conteúdo.
    
- Para evitar que seja necessário digitem novamente um grande número de locais de conteúdo quando você cria uma nova pesquisa.
    
- Para diminuir o tamanho dos resultados da pesquisa; Por exemplo, se você tiver uma pesquisa que retorne resultados em excesso para exportar, você pode clonar a pesquisa e adicione um critério de pesquisa com base em um intervalo de datas para reduzir o número de resultados de pesquisa.
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script descrito neste tópico.
    
- O script inclui o tratamento de erros mínimas. A principal finalidade do script é clonar rapidamente uma pesquisa de conteúdo.
    
- O script cria uma nova pesquisa de conteúdo, mas não iniciá-lo.
    
- Esse script leva em consideração se a pesquisa de conteúdo que está sendo clonada é associada a um caso de eDiscovery. Se a pesquisa estiver associada um caso, a nova pesquisa também serão associada com o mesmo caso. Se a pesquisa existente não estiver associada a um caso, a nova pesquisa será listada na página de **pesquisa de conteúdo** na segurança &amp; Centro de conformidade. 
    
- O script de amostra fornecido neste tópico não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>Etapa 1: Execute o script para clonar uma pesquisa

O script nesta etapa criará uma nova pesquisa de conteúdo pela clonagem de um existente. Quando você executar esse script, você precisará das seguintes informações:
  
- **Suas credenciais de usuário** - o script usarão suas credenciais para se conectar à segurança &amp; Centro de conformidade para sua organização do Office 365 com o Windows PowerShell. Conforme anteriormente mencionado, você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade para executar o script. 
    
- **O nome da pesquisa existente** - este é a pesquisa de conteúdo que você deseja clonar. 
    
- **O nome da nova pesquisa que será criado** - se esse valor for deixado em branco, o script criará um nome para a nova pesquisa que é baseado no nome da pesquisa clonada. 
    
Para clonar uma pesquisa:
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `CloneSearch.ps1`.
    
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

2. Abra o Windows PowerShell e vá para a pasta onde você salvou o script.
    
3. Executar o script; Por exemplo:
    
    ```
    .\CloneSearch.ps1
    ```

4. Quando solicitado a fornecer suas credenciais, digite seu endereço de email e senha e clique em **Okey**.
    
5. Insira a seguinte informações quando solicitado pelo script. Digite cada parte da informação e pressione **Enter**.
    
    - O nome da pesquisa existente.
    
    - O nome da nova pesquisa.
    
    O script cria a nova pesquisa de conteúdo, mas não iniciá-lo. Isso oferece uma oportunidade para editar e executar a pesquisa na próxima etapa. Você pode exibir as propriedades da nova pesquisa executando o cmdlet **Get-ComplianceSearch** ou indo para a página de **pesquisa de conteúdo** ou de **Descoberta eletrônica** na segurança &amp; Centro de conformidade, dependendo se é ou não a nova pesquisa associados a um caso. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a>Etapa 2: Edite e execute a pesquisa clonada na segurança &amp; Centro de conformidade

Depois da executar o script para clonar uma pesquisa de conteúdo existente, a próxima etapa é ir para a segurança &amp; Centro de conformidade para editar e executar a nova pesquisa. Conforme anteriormente mencionado, você pode editar uma pesquisa alterando a consulta de pesquisa de palavra-chave e adicionando ou removendo critérios de pesquisa. Para obter mais informações, consulte:
  
- [Pesquisa de conteúdo no Office 365](content-search.md)
    
- [Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md)
    
- [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md)