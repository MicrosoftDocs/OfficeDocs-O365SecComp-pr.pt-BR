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
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Você pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar todas as OneDrive para sites corporativos em sua organização para determinadas palavras-chave, informações confidenciais e outros critérios de pesquisa. Cada usuário na sua organização é o proprietário de sua OneDrive para o site de negócios, que está localizado no conjunto de sites denominado https://domain-my.sharepoint.com. Por padrão, um administrador global do Office 365 ou um Gerenciador de conformidade não pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar qualquer OneDrive para sites corporativos. Para pesquisar um OneDrive for Business site, administradores ou gerentes de conformidade deve ser um administrador de conjunto de sites que onedrive para o site de negócios.
ms.openlocfilehash: 61f068a03bcce599d9f1b7eb62d7b317b7feab68
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038084"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a><span data-ttu-id="fd38b-106">Atribuir permissões de Descoberta Eletrônica a sites do OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="fd38b-106">Assign eDiscovery permissions to OneDrive for Business sites</span></span>

<span data-ttu-id="fd38b-p102">Você pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar todas as OneDrive para sites corporativos em sua organização para determinadas palavras-chave, informações confidenciais e outros critérios de pesquisa. Cada usuário na sua organização é o proprietário de sua OneDrive para o site de negócios, que está localizado no conjunto de sites denominado https://domain-my.sharepoint.com. Por padrão, um administrador global do Office 365 ou um Gerenciador de conformidade não pode usar o Centro de descoberta eletrônica no SharePoint Online para pesquisar qualquer OneDrive para sites corporativos. Para pesquisar um OneDrive for Business site, administradores ou gerentes de conformidade deve ser um administrador de conjunto de sites que onedrive para o site de negócios.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p102">You can use the eDiscovery Center in SharePoint Online to search all OneDrive for Business sites in your organization for certain keywords, sensitive information, and other search criteria. Each user in your organization is the owner of their OneDrive for Business site, which is located in the site collection named https://domain-my.sharepoint.com. By default, an Office 365 global administrator or compliance manager can't use the eDiscovery Center in SharePoint Online to search any OneDrive for Business sites. To search a OneDrive for Business site, administrators or compliance managers must be a site collection administrator for that OneDrive for Business site.</span></span> 
  
<span data-ttu-id="fd38b-111">Este artigo o orienta pelas etapas para tornar um administrador ou conformidade Gerenciador de um administrador de conjunto de sites para cada OneDrive para o site de negócios em sua organização.</span><span class="sxs-lookup"><span data-stu-id="fd38b-111">This article guides you through the steps to make an administrator or compliance manager a site collection administrator for every OneDrive for Business site in your organization.</span></span> 
  
<span data-ttu-id="fd38b-112">Consulte a seção de [informações adicionais](#more-information) para obter dicas sobre como usar o script neste artigo, incluindo examinando o script na etapa 3 para remover um usuário como um administrador de conjunto de sites do OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-112">See the [More information](#more-information) section for tips about using the script in this article, including revising the script in Step 3 to remove a user as a site collection administrator from OneDrive for Business sites.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="fd38b-113">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="fd38b-113">Before you begin</span></span>

- <span data-ttu-id="fd38b-p103">Instale o Shell de gerenciamento Online do SharePoint. Para obter informações, consulte [Configurar o ambiente do SharePoint Online Management Shell do Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span><span class="sxs-lookup"><span data-stu-id="fd38b-p103">Install the SharePoint Online Management Shell. For information, see [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span></span>
    
- <span data-ttu-id="fd38b-116">Execute o script na etapa 3 em cada vez que você deseja atribuir a um usuário como um administrador de conjunto de sites a qualquer OneDrive para sites corporativos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="fd38b-116">Run the script in Step 3 each time you want to assign a user as a site collection administrator to any OneDrive for Business sites in your organization.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="fd38b-p104">Um administrador ou conformidade gerente que é um administrador de conjunto de sites do OneDrive para sites corporativos podem abrir OneDrive dos usuários para bibliotecas de documentos de negócios e executar as mesmas tarefas que o proprietário. É importante para controlar e monitorar que tenha sido atribuído permissões de descoberta eletrônica para o OneDrive para sites corporativos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p104">An administrator or compliance manager who is a site collection administrator for OneDrive for Business sites can open users' OneDrive for Business document libraries and perform the same tasks as the owner. It's important to control and monitor who has been assigned eDiscovery permissions to OneDrive for Business sites in your organization.</span></span> 
  
- <span data-ttu-id="fd38b-p105">O exemplo de script fornecido neste artigo não é suportado em qualquer serviço ou programa de suporte padrão da Microsoft. O script de exemplo é fornecido que se encontra sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do script de exemplo e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega do script será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar o script de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p105">The sample script provided in this article isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a><span data-ttu-id="fd38b-124">Etapa 1: Coletar uma lista de todos os OneDrive para sites corporativos</span><span class="sxs-lookup"><span data-stu-id="fd38b-124">Step 1: Collect a list of all OneDrive for Business sites</span></span>

<span data-ttu-id="fd38b-p106">A primeira etapa é criar uma lista de todos os OneDrive para sites corporativos em sua organização. Para obter instruções, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Esse script neste artigo cria um arquivo de texto que contém uma lista de todos os sites de OneDrive. O script que você pode executar na etapa 3 atribui um usuário especificado como um administrador de conjunto de sites para cada OneDrive para site de negócios listado no arquivo de texto que é criado nesta etapa. O texto a seguir fornece um exemplo de como a lista de sites neste arquivo deve ser formatada. Você pode remover sites desse arquivo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p106">The first step is to create a list of all OneDrive for Business sites in your organization. For instructions, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. The script that you run in Step 3 assigns a specified user as a site collection administrator to each OneDrive for Business site listed in the text file that's created in this step. The following text provides an example of how the list of sites in this file should be formatted. You can remove sites from this file if necessary.</span></span>

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a><span data-ttu-id="fd38b-131">Etapa 2: Conectar o Shell de gerenciamento do SharePoint Online para a sua organização</span><span class="sxs-lookup"><span data-stu-id="fd38b-131">Step 2: Connect SharePoint Online Management Shell to your organization</span></span>

1. <span data-ttu-id="fd38b-132">No seu computador local, abra o Shell de Gerenciamento do SharePoint Online e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="fd38b-132">On your local computer, open the SharePoint Online Management Shell, and run the following command:</span></span>

    ```
    $credentials = Get-Credential
    ```

2. <span data-ttu-id="fd38b-133">Na caixa de diálogo **Solicitação de Credenciais do Windows PowerShell**, digite o nome de usuário e senha da sua conta de administrador global do Office 365 e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd38b-133">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global administrator account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="fd38b-134">Execute o seguinte comando para conectar o Shell à sua organização do SharePoint Online:</span><span class="sxs-lookup"><span data-stu-id="fd38b-134">Run the following command to connect the Shell to your SharePoint Online organization:</span></span>
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. <span data-ttu-id="fd38b-135">Para verificar se você está conectado à sua organização do SharePoint Online, execute o seguinte comando para obter uma lista de todos os sites da sua organização:</span><span class="sxs-lookup"><span data-stu-id="fd38b-135">To verify that you are connected to your SharePoint Online organization, run the following command to get a list of all the sites in your organization:</span></span>
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a><span data-ttu-id="fd38b-136">Etapa 3: Atribuir um usuário como um administrador de conjunto de sites para sites do OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="fd38b-136">Step 3: Assign a user as a site collection administrator to OneDrive for Business sites</span></span>

<span data-ttu-id="fd38b-p107">A próxima etapa é executar um script que atribui a um usuário especificado como um administrador de conjunto de sites em cada OneDrive para site de negócios em sua organização. Esse script usa a lista de OneDrive para sites corporativos que você criou na etapa 1. Conforme indicado anteriormente, você precisará executar esse script cada vez que você deseja atribuir a um usuário como um administrador de conjunto de sites para o OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p107">The next step is to run a script that assigns a specified user as a site collection administrator in every OneDrive for Business site in your organization. This script uses the list of OneDrive for Business sites that you created in Step 1. As previously stated, you have to run this script each time that you want to assign a user as a site collection administrator to OneDrive for Business sites.</span></span>
  
1. <span data-ttu-id="fd38b-p108">Salve o texto a seguir em um arquivo de texto. Por exemplo, você poderá salvá-lo em um arquivo chamado OD4BAssignSCA.txt.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p108">Save the following text to a text file. For example, you could save it to a file named OD4BAssignSCA.txt.</span></span>

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

2. <span data-ttu-id="fd38b-p109">Edite as variáveis a seguir no início do arquivo de script e usar informações específicas para a sua organização. Os exemplos seguintes assumem que o nome de domínio da sua organização é contoso.onmicrosoft.com. Certifique-se ao redor os valores para as variáveis com aspas duplas ("").</span><span class="sxs-lookup"><span data-stu-id="fd38b-p109">Edit the following variables in the beginning of the script file, and use information that's specific to your organization. The following examples assume that the domain name of your organization is contoso.onmicrosoft.com. Be sure to surround the values for the variables with double-quotation marks (" ").</span></span>
    
    - <span data-ttu-id="fd38b-145">**$AdminURI** - Especifica o URI para o serviço de administração do SharePoint Online, por exemplo, `"https://contoso-admin.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="fd38b-145">**$AdminURI** - This specifies the URI for your SharePoint Online admin service, for example,  `"https://contoso-admin.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="fd38b-146">**$AdminAccount** - Especifica uma conta de administrador global na sua organização do Office 365, por exemplo, `"admin@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="fd38b-146">**$AdminAccount** - This specifies a global administrator account in your Office 365 organization, for example,  `"admin@contoso.onmicrosoft.com"`.</span></span>
    
    - <span data-ttu-id="fd38b-147">**$eDiscoveryUser** - Especifica a conta de usuário de um administrador ou Gerenciador de conformidade que será atribuído como um administrador de conjunto de sites para cada OneDrive para site de negócios em sua organização, por exemplo, `"annb@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="fd38b-147">**$eDiscoveryUser** - This specifies the user account of an administrator or compliance manager who will be assigned as a site collection administrator for every OneDrive for Business site in your organization, for example,  `"annb@contoso.onmicrosoft.com"`.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="fd38b-148">Alterar a conta de usuário especificada pela variável **$eDiscoveryUser** e execute novamente o script para atribuir um usuário diferente como um administrador de conjunto de sites para o OneDrive for sites corporativos especificadas pela variável **$MySiteListFile** .</span><span class="sxs-lookup"><span data-stu-id="fd38b-148">Change the user account specified by the **$eDiscoveryUser** variable and re-run the script to assign a different user as a site collection administrator to the OneDrive for Business sites that are specified by the **$MySiteListFile** variable.</span></span> 
  
    - <span data-ttu-id="fd38b-p110">**$MySitePrefix** Especifica a URL para o domínio de meusite da sua organização. Este é o domínio que contém todos os OneDrive para sites corporativos em sua organização, por exemplo, `"https://contoso-my.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p110">**$MySitePrefix**This specifies the URL for your organization's MySite domain. This is the domain that contains all the OneDrive for Business sites in your organization, for example,  `"https://contoso-my.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="fd38b-p111">**$MySiteListFile** Especifica o caminho completo do arquivo de texto que você criou na etapa 1. Esse arquivo contém uma lista de OneDrive para sites corporativos em sua organização, por exemplo, `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Certifique-se ao redor o valor dessa variável com aspas (' '). Observe que você deve especificar o local que você salvou o arquivo de texto na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p111">**$MySiteListFile**This specifies the full path of the text file that you created in Step 1. This file contains a list of OneDrive for Business sites in your organization, for example,  `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Be sure to surround the value for this variable with single-quotation marks (' '). Note that you should specify the location that you saved the text file to in Step 1.</span></span>
    
3. <span data-ttu-id="fd38b-p112">Salve o arquivo de texto como um arquivo de script do PowerShell alterando o sufixo de nome de arquivo para .ps1. Por exemplo, salve o arquivo OD4BAssignSCA.txt como OD4BAssignSCA.ps1.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p112">Save the text file as a PowerShell script file by changing the file name suffix to .ps1. For example, save the file OD4BAssignSCA.txt as OD4BAssignSCA.ps1.</span></span>
    
4. <span data-ttu-id="fd38b-157">No Shell de Gerenciamento do SharePoint Online, vá para a pasta que contém o script do PowerShell criado na etapa anterior e execute-o; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fd38b-157">In SharePoint Online Management Shell, go to the folder that contains the PowerShell script that you created in the previous step, and then run the script, for example:</span></span>
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    <span data-ttu-id="fd38b-p113">Você será solicitado a inserir a senha para a conta de administrador que você especificou no script. Se o script é executado com êxito, a mensagem `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` é exibido para cada OneDrive para site de negócios que está listado no arquivo de entrada especificado pelo **$MySiteListFile**.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p113">You will be prompted to enter the password for the administrator account that you specified in the script. If the script runs successfully, the message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` is displayed for each OneDrive for Business site that's listed in the input file specified by **$MySiteListFile**.</span></span>

## <a name="more-information"></a><span data-ttu-id="fd38b-160">Mais informações</span><span class="sxs-lookup"><span data-stu-id="fd38b-160">More information</span></span>

- <span data-ttu-id="fd38b-p114">O script que você executou na etapa 3 usa o cmdlet **Set-SPOUser** para atribuir o usuário especificado como um administrador de conjunto de sites para cada OneDrive for Business que está listado no arquivo especificado pela variável **$MySiteListFile** . Se você tiver uma organização muito grande com milhares de usuários, considere o seguinte para facilitar a gerenciar a atribuição de permissões de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p114">The script that you ran in Step 3 uses the **Set-SPOUser** cmdlet to assign the specified user as a site collection administrator to every OneDrive for Business that's listed in the file specified by the **$MySiteListFile** variable. If you have a very large organization with thousands of users, consider doing the following to make it easier to manage assigning eDiscovery permissions.</span></span> 
    
  - <span data-ttu-id="fd38b-163">Edite o arquivo que você criou na etapa 1 que contém a lista de OneDrive para sites corporativos para que ele inclua somente os sites para os usuários estão que estão envolvidos nos casos jurídicos ativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-163">Edit the file that you created in Step 1 that contains the list of OneDrive for Business sites so that it includes only the sites for users are that are involved in active legal cases.</span></span>
    
  - <span data-ttu-id="fd38b-p115">Atribua permissões a 2.500 não ultrapassa OneDrive para sites corporativos por dia. Por exemplo, digamos que você tenha 10.000 OneDrive para sites corporativos em sua organização. Você pode criar a lista na etapa 1 para coletar todos os sites. Em seguida, você poderia usar esse arquivo para criar arquivos de quatro que contém os 2.500 usuários. No primeiro dia, você pode executar o script na etapa 3 para atribuir permissões a 2.500 primeiro OneDrive para sites corporativos. No segundo dia, execute o script do lado 2.500 OneDrive para sites corporativos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p115">Assign permissions to no more than 2,500 OneDrive for Business sites per day. For example, let's say you have 10,000 OneDrive for Business sites in your organization. You could create the list in Step 1 to collect all the sites. Then you could use that file to create four files that each contain 2,500 users. On the first day, you would run the script in Step 3 to assign permissions to the first 2,500 OneDrive for Business sites. On the second day, you would run the script for the next 2,500 OneDrive for Business sites, and so on.</span></span>
    
- <span data-ttu-id="fd38b-p116">Manter um registro de OneDrive para sites corporativos que foram atribuídas permissões de descoberta eletrônica e de usuário que é atribuído como o administrador do conjunto de sites. Por exemplo, depois de atribuir permissões, você pode salvar o arquivo de texto que contém a lista de OneDrive para sites corporativos e adicionar uma linha a ela que identifica o usuário que é atribuído como o administrador do conjunto de sites.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p116">Keep a record of the OneDrive for Business sites that were assigned eDiscovery permissions and the user who is assigned as the site collection administrator. For example, after you assign permissions, you can save the text file that contains the list of OneDrive for Business sites and add a line to it that identifies the user who is assigned as the site collection administrator.</span></span>
    
- <span data-ttu-id="fd38b-p117">Usuários podem exibir a lista de administradores do conjunto de sites para seu OneDrive para o site de negócios. Como os usuários são de administrador do conjunto de sites para sua próprias OneDrive para o site de negócios, eles podem remover administradores de conjunto de sites. Considere o seguinte para reduzir a chance de usuários a remoção do usuário que é atribuído permissões de descoberta eletrônica a OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-p117">Users can view the list of site collection administators for their OneDrive for Business site. Because users are site collection administrator for their own OneDrive for Business site, they can remove site collection administrators. Consider doing the following to mitigate the chance of users removing the user who is assigned eDiscovery permissions to OneDrive for Business sites.</span></span>
    
  - <span data-ttu-id="fd38b-175">Comunicar-se aos usuários que para fins de conformidade e eDiscovery, um responsável pela conformidade tenha sido atribuída como um administrador de conjunto de sites para o OneDrive para sites corporativos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="fd38b-175">Communicate to users that for eDiscovery and compliance purposes, a compliance officer has been assigned as a site collection administrator to OneDrive for Business sites in your organization.</span></span>
    
  - <span data-ttu-id="fd38b-176">Execute novamente o script na etapa 3, se necessário, para atribuir a um usuário novamente como o administrador do conjunto de sites do OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-176">Re-run the script in Step 3, if necessary, to re-assign a user as the site collection administrator for OneDrive for Business sites.</span></span>
    
- <span data-ttu-id="fd38b-p118">Você também pode usar o script que você executou na etapa 3 para remover um usuário como o administrador do conjunto de sites do OneDrive para sites corporativos. Para remover um usuário como um administrador de conjunto de sites, você precisará alterar o seguinte comando (próximo ao final do script) de:</span><span class="sxs-lookup"><span data-stu-id="fd38b-p118">You can also use the script that you ran in Step 3 to remove a user as the site collection administrator from OneDrive for Business sites. To remove a user as a site collection administrator, you have to change the following command (near the end of the script) from:</span></span> 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    <span data-ttu-id="fd38b-179">para:</span><span class="sxs-lookup"><span data-stu-id="fd38b-179">to:</span></span>
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    <span data-ttu-id="fd38b-180">Você também pode alterar a seguinte linha no script de:</span><span class="sxs-lookup"><span data-stu-id="fd38b-180">You can also change the following line in the script from:</span></span>

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    <span data-ttu-id="fd38b-181">para:</span><span class="sxs-lookup"><span data-stu-id="fd38b-181">to:</span></span>
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    <span data-ttu-id="fd38b-182">Depois de fazer essas alterações, salve o script com um nome diferente, como OD4BRemoveSCA.ps1 e depois usá-lo para remover um usuário como um administrador de conjunto de sites de um grupo do OneDrive para sites corporativos.</span><span class="sxs-lookup"><span data-stu-id="fd38b-182">After you make these changes, save the script with a different name, such as OD4BRemoveSCA.ps1, and then use it to remove a user as a site collection administrator from a group of OneDrive for Business sites.</span></span>
