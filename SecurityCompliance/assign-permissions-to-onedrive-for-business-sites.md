---
title: Atribuir permissões de Descoberta Eletrônica a sites do OneDrive for Business
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Você pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar todas as OneDrive para sites corporativos em sua organização para determinadas palavras-chave, informações confidenciais e outros critérios de pesquisa. Cada usuário na sua organização é o proprietário de sua OneDrive para o site de negócios, que está localizado no conjunto de sites denominado https://domain-my.sharepoint.com. Por padrão, um administrador global do Office 365 ou um Gerenciador de conformidade não pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar qualquer OneDrive para sites corporativos. Para pesquisar um OneDrive for Business site, administradores ou gerentes de conformidade deve ser um administrador de conjunto de sites que onedrive para o site de negócios.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524077"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a>Atribuir permissões de Descoberta Eletrônica a sites do OneDrive for Business

Você pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar todas as OneDrive para sites corporativos em sua organização para determinadas palavras-chave, informações confidenciais e outros critérios de pesquisa. Cada usuário na sua organização é o proprietário de sua OneDrive para o site de negócios, que está localizado no conjunto de sites denominado https://domain-my.sharepoint.com. Por padrão, um administrador global do Office 365 ou um Gerenciador de conformidade não pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar qualquer OneDrive para sites corporativos. Para pesquisar um OneDrive for Business site, administradores ou gerentes de conformidade deve ser um administrador de conjunto de sites que onedrive para o site de negócios. 
  
Este artigo o orienta pelas etapas para tornar um administrador ou conformidade Gerenciador de um administrador de conjunto de sites para cada OneDrive para o site de negócios em sua organização. 
  
Consulte a seção de [informações adicionais](#more-information) para obter dicas sobre como usar o script neste artigo, incluindo examinando o script na etapa 3 para remover um usuário como um administrador de conjunto de sites do OneDrive para sites corporativos. 
  
## <a name="before-you-begin"></a>Antes de começar

- Instale o Shell de gerenciamento Online do SharePoint. Para obter informações, consulte [Configurar o ambiente do SharePoint Online Management Shell do Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318).
    
- Execute o script na etapa 3 em cada vez que você deseja atribuir a um usuário como um administrador de conjunto de sites a qualquer OneDrive para sites corporativos em sua organização. 
    
    > [!IMPORTANT]
    > Um administrador ou conformidade gerente que é um administrador de conjunto de sites do OneDrive para sites corporativos podem abrir OneDrive dos usuários para bibliotecas de documentos de negócios e executar as mesmas tarefas que o proprietário. É importante para controlar e monitorar que tenha sido atribuído permissões de descoberta eletrônica para o OneDrive para sites corporativos em sua organização. 
  
- O exemplo de script fornecido neste artigo não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega do script será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar o script de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a>Etapa 1: Coletar uma lista de todos os OneDrive para sites corporativos

A primeira etapa é criar uma lista de todos os OneDrive para sites corporativos em sua organização. Para obter instruções, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Esse script neste artigo cria um arquivo de texto que contém uma lista de todos os sites de OneDrive. O script que você pode executar na etapa 3 atribui um usuário especificado como um administrador de conjunto de sites para cada OneDrive para site de negócios listado no arquivo de texto que é criado nesta etapa. O texto a seguir fornece um exemplo de como a lista de sites neste arquivo deve ser formatada. Você pode remover sites desse arquivo, se necessário.

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a>Etapa 2: Conectar o Shell de gerenciamento do SharePoint Online para a sua organização

1. No seu computador local, abra o Shell de Gerenciamento do SharePoint Online e execute o seguinte comando:

    ```
    $credentials = Get-Credential
    ```

2. Na caixa de diálogo **Solicitação de Credenciais do Windows PowerShell**, digite o nome de usuário e senha da sua conta de administrador global do Office 365 e clique em **OK**.
    
3. Execute o seguinte comando para conectar o Shell à sua organização do SharePoint Online:
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. Para verificar se você está conectado à sua organização do SharePoint Online, execute o seguinte comando para obter uma lista de todos os sites da sua organização:
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a>Etapa 3: Atribuir um usuário como um administrador de conjunto de sites para sites do OneDrive for Business

A próxima etapa é executar um script que atribui a um usuário especificado como um administrador de conjunto de sites em cada OneDrive para site de negócios em sua organização. Esse script usa a lista de OneDrive para sites corporativos que você criou na etapa 1. Conforme indicado anteriormente, você precisará executar esse script cada vez que você deseja atribuir a um usuário como um administrador de conjunto de sites para o OneDrive para sites corporativos.
  
1. Salve o texto a seguir em um arquivo de texto. Por exemplo, você poderá salvá-lo em um arquivo chamado OD4BAssignSCA.txt.

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. Edite as variáveis a seguir no início do arquivo de script e usar informações específicas para a sua organização. Os exemplos seguintes assumem que o nome de domínio da sua organização é contoso.onmicrosoft.com. Certifique-se ao redor os valores para as variáveis com aspas duplas ("").
    
    - **$AdminURI** - Especifica o URI para o serviço de administração do SharePoint Online, por exemplo, `"https://contoso-admin.sharepoint.com"`.
    
    - **$AdminAccount** - Especifica uma conta de administrador global na sua organização do Office 365, por exemplo, `"admin@contoso.onmicrosoft.com"`.
    
    - **$eDiscoveryUser** - Especifica a conta de usuário de um administrador ou Gerenciador de conformidade que será atribuído como um administrador de conjunto de sites para cada OneDrive para site de negócios em sua organização, por exemplo, `"annb@contoso.onmicrosoft.com"`.
    
      > [!NOTE]
      > Alterar a conta de usuário especificada pela variável **$eDiscoveryUser** e execute novamente o script para atribuir um usuário diferente como um administrador de conjunto de sites para o OneDrive for sites corporativos especificadas pela variável **$MySiteListFile** . 
  
    - **$MySitePrefix** Especifica a URL para o domínio de meusite da sua organização. Este é o domínio que contém todos os OneDrive para sites corporativos em sua organização, por exemplo, `"https://contoso-my.sharepoint.com"`.
    
    - **$MySiteListFile** Especifica o caminho completo do arquivo de texto que você criou na etapa 1. Esse arquivo contém uma lista de OneDrive para sites corporativos em sua organização, por exemplo, `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Certifique-se ao redor o valor dessa variável com aspas (' '). Observe que você deve especificar o local que você salvou o arquivo de texto na etapa 1.
    
3. Salve o arquivo de texto como um arquivo de script do PowerShell alterando o sufixo de nome de arquivo para .ps1. Por exemplo, salve o arquivo OD4BAssignSCA.txt como OD4BAssignSCA.ps1.
    
4. No Shell de Gerenciamento do SharePoint Online, vá para a pasta que contém o script do PowerShell criado na etapa anterior e execute-o; por exemplo:
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    Você será solicitado a inserir a senha para a conta de administrador que você especificou no script. Se o script é executado com êxito, a mensagem `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` é exibido para cada OneDrive para site de negócios que está listado no arquivo de entrada especificado pelo **$MySiteListFile**.

## <a name="more-information"></a>Mais informações

- O script que você executou na etapa 3 usa o cmdlet **Set-SPOUser** para atribuir o usuário especificado como um administrador de conjunto de sites para cada OneDrive for Business que está listado no arquivo especificado pela variável **$MySiteListFile** . Se você tiver uma organização muito grande com milhares de usuários, considere o seguinte para facilitar a gerenciar a atribuição de permissões de descoberta eletrônica. 
    
  - Edite o arquivo que você criou na etapa 1 que contém a lista de OneDrive para sites corporativos para que ele inclua somente os sites para os usuários estão que estão envolvidos nos casos jurídicos ativos.
    
  - Atribua permissões a 2.500 não ultrapassa OneDrive para sites corporativos por dia. Por exemplo, digamos que você tenha 10.000 OneDrive para sites corporativos em sua organização. Você pode criar a lista na etapa 1 para coletar todos os sites. Em seguida, você poderia usar esse arquivo para criar arquivos de quatro que contém os 2.500 usuários. No primeiro dia, você pode executar o script na etapa 3 para atribuir permissões a 2.500 primeiro OneDrive para sites corporativos. No segundo dia, execute o script do lado 2.500 OneDrive para sites corporativos e assim por diante.
    
- Manter um registro de OneDrive para sites corporativos que foram atribuídas permissões de descoberta eletrônica e de usuário que é atribuído como o administrador do conjunto de sites. Por exemplo, depois de atribuir permissões, você pode salvar o arquivo de texto que contém a lista de OneDrive para sites corporativos e adicionar uma linha a ela que identifica o usuário que é atribuído como o administrador do conjunto de sites.
    
- Usuários podem exibir a lista de administradores do conjunto de sites para seu OneDrive para o site de negócios. Como os usuários são de administrador do conjunto de sites para sua próprias OneDrive para o site de negócios, eles podem remover administradores de conjunto de sites. Considere o seguinte para reduzir a chance de usuários a remoção do usuário que é atribuído permissões de descoberta eletrônica a OneDrive para sites corporativos.
    
  - Comunicar-se aos usuários que para fins de conformidade e eDiscovery, um responsável pela conformidade tenha sido atribuída como um administrador de conjunto de sites para o OneDrive para sites corporativos em sua organização.
    
  - Execute novamente o script na etapa 3, se necessário, para atribuir a um usuário novamente como o administrador do conjunto de sites do OneDrive para sites corporativos.
    
- Você também pode usar o script que você executou na etapa 3 para remover um usuário como o administrador do conjunto de sites do OneDrive para sites corporativos. Para remover um usuário como um administrador de conjunto de sites, você precisará alterar o seguinte comando (próximo ao final do script) de: 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    para:
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    Você também pode alterar a seguinte linha no script de:

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    para:
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    Depois de fazer essas alterações, salve o script com um nome diferente, como OD4BRemoveSCA.ps1 e depois usá-lo para remover um usuário como um administrador de conjunto de sites de um grupo do OneDrive para sites corporativos.
