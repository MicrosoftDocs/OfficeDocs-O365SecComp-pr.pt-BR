---
title: Implantar um site de equipe do SharePoint Online isolado
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 3033614b-e23b-4f68-9701-f62525eafaab
description: 'Resumo: Implante um novo isolado SharePoint Online site de equipe com estas instruções passo a passo.'
ms.openlocfilehash: d233ec46b1e7257a92451c781afd6c61312f44b8
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345973"
---
# <a name="deploy-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="a47fb-103">Implantar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="a47fb-103">Deploy an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="a47fb-104">**Resumo:** Implante um novo isolado SharePoint Online site de equipe com estas instruções passo a passo.</span><span class="sxs-lookup"><span data-stu-id="a47fb-104">**Summary:** Deploy a new isolated SharePoint Online team site with these step-by-step instructions.</span></span>
  
<span data-ttu-id="a47fb-p101">Este artigo é um guia passo a passo de implantação para criar e configurar um site de equipe do SharePoint Online isolado em Microsoft Office 365. Essas etapas pressupõem o uso dos três grupos padrão do SharePoint e níveis de permissão correspondente, com um grupo único de acesso baseado no AD do Windows Azure Active Directory para cada nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p101">This article is a step-by-step deployment guide for creating and configuring an isolated SharePoint Online team site in Microsoft Office 365. These steps assume the use of the three default SharePoint groups and corresponding permission levels, with a single Azure Active Directory (AD)-based access group for each level of access.</span></span>
  
## <a name="phase-1-create-and-populate-the-team-site-access-groups"></a><span data-ttu-id="a47fb-107">Fase 1: Crie e preencha os grupos de acesso do site de equipe</span><span class="sxs-lookup"><span data-stu-id="a47fb-107">Phase 1: Create and populate the team site access groups</span></span>

<span data-ttu-id="a47fb-108">Nesta fase, você cria os três grupos Azure acesso baseado em AD para os grupos padrão de três do SharePoint e preenchê-los com as contas de usuário apropriada.</span><span class="sxs-lookup"><span data-stu-id="a47fb-108">In this phase, you create the three Azure AD-based access groups for the three default SharePoint groups and populate them with the appropriate user accounts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a47fb-p102">As etapas a seguir pressupõem que todas as contas de usuário necessários já existirem e recebem as licenças apropriadas. Caso contrário, adicione-os e atribuir licenças antes de prosseguir para a etapa 1.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p102">The following steps assume that all necessary user accounts already exist and are assigned the appropriate licenses. If not, please add them and assign licenses before proceeding to step 1.</span></span> 
  
### <a name="step-1-list-the-sharepoint-online-admins-for-the-site"></a><span data-ttu-id="a47fb-111">Etapa 1: Listar os administradores do SharePoint Online para o site</span><span class="sxs-lookup"><span data-stu-id="a47fb-111">Step 1: List the SharePoint Online admins for the site</span></span>

<span data-ttu-id="a47fb-112">Determine que o conjunto de usuário contas correspondente ao grupo de administradores do SharePoint Online para o site de equipe isolado.</span><span class="sxs-lookup"><span data-stu-id="a47fb-112">Determine the set of user accounts corresponding to the SharePoint Online admins for the isolated team site.</span></span>
  
<span data-ttu-id="a47fb-113">Se você está gerenciando contas de usuários e grupos por meio do Office 365 e deseja usar o Windows PowerShell, faça uma lista dos seus usuários nomes principais (UPNs) (exemplo UPN: belindan@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a47fb-113">If you are managing user accounts and groups through Office 365 and want to use Windows PowerShell, make a list of their user principal names (UPNs) (example UPN: belindan@contoso.com).</span></span>
  
### <a name="step-2-list-the-members-for-the-site"></a><span data-ttu-id="a47fb-114">Etapa 2: Listam os membros do site</span><span class="sxs-lookup"><span data-stu-id="a47fb-114">Step 2: List the members for the site</span></span>

<span data-ttu-id="a47fb-115">Determine o conjunto de contas de usuário correspondente aos membros para o site de equipe isolado, aqueles que vai ser colaborando em recursos armazenados dentro do site.</span><span class="sxs-lookup"><span data-stu-id="a47fb-115">Determine the set of user accounts corresponding to the members for the isolated team site, those who will be collaborating on resources stored within the site.</span></span>
  
<span data-ttu-id="a47fb-p103">Se você está gerenciando contas de usuários e grupos por meio do Office 365 e deseja usar o PowerShell, faça uma lista de seus UPNs. Se houver muitos membros do site, você pode armazenar a lista de UPNs em um arquivo de texto e adicioná-los a todos com um único comando do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p103">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs. If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
### <a name="step-3-list-the-viewers-for-the-site"></a><span data-ttu-id="a47fb-118">Etapa 3: Listar os visualizadores para o site</span><span class="sxs-lookup"><span data-stu-id="a47fb-118">Step 3: List the viewers for the site</span></span>

<span data-ttu-id="a47fb-119">Determine o conjunto de contas de usuário correspondente para os visualizadores do site da equipe isolado, aqueles que pode exibir os recursos armazenados no site, mas não modificá-los ou colaborar diretamente em seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a47fb-119">Determine the set of user accounts corresponding to the viewers of the isolated team site, those who can view the resources stored in the site but not modify them or directly collaborate on their contents.</span></span>
  
<span data-ttu-id="a47fb-p104">Se você está gerenciando contas de usuários e grupos por meio do Office 365 e deseja usar o PowerShell, faça uma lista de seus UPNs. Se houver muitos membros do site, você pode armazenar a lista de UPNs em um arquivo de texto e adicioná-los a todos com um único comando do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p104">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs. If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
<span data-ttu-id="a47fb-122">Visualizadores para o site podem incluir a gerência executiva, assessores jurídicos ou inter-departmental participantes.</span><span class="sxs-lookup"><span data-stu-id="a47fb-122">Viewers for the site might include executive management, legal counsel, or inter-departmental stakeholders.</span></span>
  
### <a name="step-4-create-the-three-access-groups-for-the-site-in-azure-ad"></a><span data-ttu-id="a47fb-123">Etapa 4: Criar os grupos de três do access para o site no Windows Azure AD</span><span class="sxs-lookup"><span data-stu-id="a47fb-123">Step 4: Create the three access groups for the site in Azure AD</span></span>

<span data-ttu-id="a47fb-124">Você precisa criar os seguintes grupos de acesso no Azure AD:</span><span class="sxs-lookup"><span data-stu-id="a47fb-124">You need to create the following access groups in Azure AD:</span></span>
  
- <span data-ttu-id="a47fb-125">Administradores de site (que conterão a lista da etapa 1)</span><span class="sxs-lookup"><span data-stu-id="a47fb-125">Site admins (which will contain the list from step 1)</span></span>
    
- <span data-ttu-id="a47fb-126">Membros do site (que conterão a lista da etapa 2)</span><span class="sxs-lookup"><span data-stu-id="a47fb-126">Site members (which will contain the list from step 2)</span></span>
    
- <span data-ttu-id="a47fb-127">Visitantes do site (que conterão a lista da etapa 3)</span><span class="sxs-lookup"><span data-stu-id="a47fb-127">Site viewers (which will contain the list from step 3)</span></span>
    
1. <span data-ttu-id="a47fb-128">No seu navegador, vá para o portal do Windows Azure em [https://portal.azure.com](https://portal.azure.com) e entre com as credenciais de uma conta que tenha sido atribuída com função de administrador de gerenciamento de usuários ou administrador da empresa.</span><span class="sxs-lookup"><span data-stu-id="a47fb-128">In your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com) and sign in with the credentials of an account that has been assigned with User Management Admin or Company Administrator role.</span></span>
    
2. <span data-ttu-id="a47fb-129">No Portal do Azure, clique em **Azure Active Directory > Grupos**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-129">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="a47fb-130">Na folha **Grupos – Todos os grupos**, clique em **+ Novo grupo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-130">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="a47fb-131">Na folha **Grupo**:</span><span class="sxs-lookup"><span data-stu-id="a47fb-131">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="a47fb-132">Escolha **Office 365** em **Tipo de Grupo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-132">Select **Office 365** in **Group type**.</span></span>
    
  - <span data-ttu-id="a47fb-133">Digite o nome do grupo no **nome**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-133">Type the group name in **Name**.</span></span>
    
  - <span data-ttu-id="a47fb-134">Digite uma descrição do grupo na **Descrição do grupo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-134">Type a description of the group in **Group description**.</span></span>
    
  - <span data-ttu-id="a47fb-135">Escolha **Atribuído** em **Tipo de Associação**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-135">Select **Assigned** in **Membership type**.</span></span>
    
5. <span data-ttu-id="a47fb-136">Clique em **Criar** e, em seguida, feche a folha **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-136">Click **Create**, and then close the **Group** blade.</span></span>
    
6. <span data-ttu-id="a47fb-137">Repita as etapas 3 a 5 para os grupos adicionais.</span><span class="sxs-lookup"><span data-stu-id="a47fb-137">Repeat steps 3-5 for your additional groups.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a47fb-p105">Você precisará usar o portal do Windows Azure para criar os grupos para que eles tenham os recursos do Office habilitados. Se um site do SharePoint Online isolado posteriormente é configurado como um site altamente confidenciais com um rótulo de proteção de informações do Windows Azure (AIP) para criptografar arquivos e atribuir permissões a grupos específicos, os grupos permitidos devem ter sido criados com os recursos do Office habilitado. Você não pode alterar a configuração de recursos do Office de um grupo do Windows Azure AD após ele ter sido criado.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p105">You need to use the Azure portal to create the groups so that they have Office features enabled. If a SharePoint Online isolated site is later configured as a Highly Confidential site with an Azure Information Protection (AIP) label to encrypt files and assign permission to specific groups, the permitted groups must have been created with Office features enabled. You cannot change the Office features setting of an Azure AD group after it has been created.</span></span> 
  
<span data-ttu-id="a47fb-141">Aqui está a configuração resultante com os grupos de acesso de três do site.</span><span class="sxs-lookup"><span data-stu-id="a47fb-141">Here is your resulting configuration with the three site access groups.</span></span>
  
![Os três grupos de acesso para sua implantação de um site isolado do SharePoint Online.](media/c2557f61-478b-4494-95e9-d79fe5909e8b.png)
  
### <a name="step-5-add-the-user-accounts-to-the-access-groups"></a><span data-ttu-id="a47fb-p106">Etapa 5. Adicione as contas de usuário para os grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="a47fb-p106">Step 5. Add the user accounts to the access groups</span></span>

<span data-ttu-id="a47fb-145">Nesta etapa, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a47fb-145">In this step, do the following:</span></span>
  
1. <span data-ttu-id="a47fb-146">Adicionar a lista de usuários da etapa 1 ao grupo de acesso de administradores de site</span><span class="sxs-lookup"><span data-stu-id="a47fb-146">Add the list of users from step 1 to the site admins access group</span></span>
    
2. <span data-ttu-id="a47fb-147">Adicionar a lista de usuários da etapa 2 para o grupo de acesso de membros do site</span><span class="sxs-lookup"><span data-stu-id="a47fb-147">Add the list of users from step 2 to the site members access group</span></span>
    
3. <span data-ttu-id="a47fb-148">Adicionar a lista de usuários da etapa 3, ao grupo de acesso do site visualizadores</span><span class="sxs-lookup"><span data-stu-id="a47fb-148">Add the list of users from step 3 to the site viewers access group</span></span>
    
<span data-ttu-id="a47fb-149">Se você está gerenciando contas de usuários e grupos por meio do Windows Server AD, adicione usuários aos grupos de acesso apropriado usando seu usuário normal do Windows Server AD e procedimentos de gerenciamento de grupo e aguarde a sincronização com sua assinatura do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a47fb-149">If you are managing user accounts and groups through Windows Server AD, add users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="a47fb-p107">Se você estiver gerenciando contas de usuários e grupos por meio do Office 365, você pode usar o Centro de administração do Office ou do PowerShell. Se você tiver os nomes de grupo duplicado para qualquer um dos grupos de acesso, você deve usar o Centro de administração do Office.</span><span class="sxs-lookup"><span data-stu-id="a47fb-p107">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell. If you have duplicate group names for any of the access groups, you should use the Office Admin center.</span></span>
  
<span data-ttu-id="a47fb-152">Para o Centro de administração do Office, entrar com uma conta de usuário que tenha sido atribuída a função de administrador da conta de usuário ou administrador da empresa e use grupos para adicionar as contas de usuário apropriados e para os grupos de acesso apropriado.</span><span class="sxs-lookup"><span data-stu-id="a47fb-152">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate user accounts and groups to the appropriate access groups.</span></span>
  
<span data-ttu-id="a47fb-153">Para o PowerShell, primeiro [conectar com o módulo do Azure Active Directory V2 PowerShell](https://go.microsoft.com/fwlink/?linkid=842218).</span><span class="sxs-lookup"><span data-stu-id="a47fb-153">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218).</span></span>
  
<span data-ttu-id="a47fb-154">Em seguida, use o seguinte bloco de comando para adicionar uma conta de usuário individual para um grupo de acesso:</span><span class="sxs-lookup"><span data-stu-id="a47fb-154">Next, use the following command block to add an individual user account to an access group:</span></span>
  
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="a47fb-155">Para um arquivo de texto que contém todos os comandos do PowerShell e um Excel planilha de configuração que gera os comandos do PowerShell com base no seu grupo e usuário nomes de conta, baixe o [Isolado SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span><span class="sxs-lookup"><span data-stu-id="a47fb-155">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 
  
<span data-ttu-id="a47fb-156">Se você armazenou os UPNs das contas de usuário para qualquer um dos grupos de acesso em um arquivo de texto, você pode usar o seguinte bloco de comando do PowerShell para adicioná-los todos ao mesmo tempo:</span><span class="sxs-lookup"><span data-stu-id="a47fb-156">If you stored the UPNs of user accounts for any of the access groups in a text file, you can use the following PowerShell command block to add them all at one time:</span></span>
  
```
$grpName="<display name of the access group>"
$fileName="<path and name of the file containing the list of account UPNs>"
$grpID=(Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
Get-Content $fileName | ForEach { $userUPN=$_; Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID $grpID }
```

<span data-ttu-id="a47fb-157">Para PowerShell, use o seguinte bloco de comando para adicionar um grupo individual para um grupo de acesso:</span><span class="sxs-lookup"><span data-stu-id="a47fb-157">For PowerShell, use the following command block to add an individual group to an access group:</span></span>
  
```
$nestedGrpName="<display name of the group to add to the access group>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $nestedGrpName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID

```

<span data-ttu-id="a47fb-158">Os resultados devem ser o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a47fb-158">The results should be the following:</span></span>
  
- <span data-ttu-id="a47fb-159">Grupo do Azure AD de administradores de site contém as contas de usuário do administrador de site ou grupos</span><span class="sxs-lookup"><span data-stu-id="a47fb-159">The site admins Azure AD group contains the site admin user accounts or groups</span></span>
    
- <span data-ttu-id="a47fb-160">Grupo do Azure AD de membros do site contém as contas de usuário do site membro ou grupos</span><span class="sxs-lookup"><span data-stu-id="a47fb-160">The site members Azure AD group contains the site member user accounts or groups</span></span>
    
- <span data-ttu-id="a47fb-161">Grupo de visualizadores Azure AD de site contém as contas de usuário ou grupos que só podem visualizar o conteúdo do site</span><span class="sxs-lookup"><span data-stu-id="a47fb-161">The site viewers Azure AD group contains the user accounts or groups that can only view the site contents</span></span>
    
<span data-ttu-id="a47fb-162">Valide a lista de membros de grupo para cada grupo de acesso com o Centro de administração do Office ou com o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a47fb-162">Validate the list of group members for each access group with the Office Admin center or with the following PowerShell command block:</span></span>
  
```
$grpName="<display name of the access group>"
Get-AzureADGroupMember -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID | Sort UserPrincipalName | Select UserPrincipalName,DisplayName,UserType
```

<span data-ttu-id="a47fb-163">Aqui está a configuração resultante com os grupos de acesso do três site preenchida com as contas de usuário ou grupos.</span><span class="sxs-lookup"><span data-stu-id="a47fb-163">Here is your resulting configuration with the three site access groups populated with user accounts or groups.</span></span>
  
![Os três grupos de acesso preenchidos com contas de usuário.](media/2320107c-dad6-4c8f-94e5-f6427c125e71.png)
  
## <a name="phase-2-create-and-configure-the-isolated-team-site"></a><span data-ttu-id="a47fb-165">Fase 2: Criar e configurar o site de equipe isolado</span><span class="sxs-lookup"><span data-stu-id="a47fb-165">Phase 2: Create and configure the isolated team site</span></span>

<span data-ttu-id="a47fb-166">Nesta fase, você cria o site do SharePoint Online isolado e configurar as permissões para os níveis de permissão padrão do SharePoint Online usar os novos grupos do Azure acesso baseado em AD.</span><span class="sxs-lookup"><span data-stu-id="a47fb-166">In this phase, you create the isolated SharePoint Online site and configure the permissions for the default SharePoint Online permission levels to use your new Azure AD-based access groups.</span></span>
  
<span data-ttu-id="a47fb-167">Primeiro, crie o site da equipe do SharePoint Online com estas etapas.</span><span class="sxs-lookup"><span data-stu-id="a47fb-167">First, create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="a47fb-p108">Entre no Portal do Office 365 com uma conta que também será usada para administrar o site de equipe do SharePoint Online (um administrador do SharePoint Online). Para obter ajuda, consulte [Onde entrar no Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="a47fb-p108">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="a47fb-170">Na lista de blocos, clique em **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-170">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="a47fb-171">Na nova guia **SharePoint** do navegador, clique em **+ Criar site**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-171">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="a47fb-172">Na página **Criar um site**, clique em **Site de equipe**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-172">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="a47fb-173">Em **nome do Site**, digite um nome para o site de equipe.</span><span class="sxs-lookup"><span data-stu-id="a47fb-173">In **Site name**, type a name for the team site.</span></span> 
    
6. <span data-ttu-id="a47fb-174">Na **Descrição do site de equipe,** digite uma descrição opcional da finalidade do site.</span><span class="sxs-lookup"><span data-stu-id="a47fb-174">In **Team site description,** type an optional description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="a47fb-175">Em **Configurações de privacidade**, escolha **Privado – somente membros podem acessar esse site** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-175">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="a47fb-176">No painel **Quem você deseja adicionar?**, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-176">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="a47fb-177">Em seguida, do novo site de equipe do SharePoint Online, configure permissões.</span><span class="sxs-lookup"><span data-stu-id="a47fb-177">Next, from the new SharePoint Online team site, configure permissions.</span></span>
  
1. <span data-ttu-id="a47fb-178">Na barra de ferramentas, clique no ícone Configurações e, em seguida, clique em **Permissões do site**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-178">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
2. <span data-ttu-id="a47fb-179">No painel **Permissões do site**, clique em **Configurações de permissões avançadas**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-179">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
3. <span data-ttu-id="a47fb-180">Na nova guia **Permissões** do navegador, clique em **Configurações de Solicitação de Acesso**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-180">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
4. <span data-ttu-id="a47fb-181">Na caixa de diálogo **Configurações de solicitações de acesso** , desmarque **Permitir membro para compartilhar o site e arquivos e pastas individuais** e **solicitações de acesso permitir** (de forma que todas as três caixas de seleção estiver desmarcadas) e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-181">In the **Access Requests Settings** dialog box, clear **Allow member to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
5. <span data-ttu-id="a47fb-182">Na guia **permissões** do seu navegador, clique em \*\* \<nome do site > membros\*\* na lista.</span><span class="sxs-lookup"><span data-stu-id="a47fb-182">On the **Permissions** tab of your browser, click **\<site name> Members** in the list.</span></span>
    
6. <span data-ttu-id="a47fb-183">Em **Pessoas e Grupos**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-183">In **People and Groups**, click **New**.</span></span>
    
7. <span data-ttu-id="a47fb-184">Na caixa de diálogo **compartilhar** , digite o nome do grupo de acesso de membros do site, selecione-o e, em seguida, clique em **compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-184">In the **Share** dialog box, type the name of the site members access group, select it, and then click **Share**.</span></span>
    
8. <span data-ttu-id="a47fb-185">Clique no botão voltar de seu navegador.</span><span class="sxs-lookup"><span data-stu-id="a47fb-185">Click the back button on your browser.</span></span>
    
9. <span data-ttu-id="a47fb-186">Clique em \*\* \<nome do site > proprietários\*\* na lista.</span><span class="sxs-lookup"><span data-stu-id="a47fb-186">Click **\<site name> Owners** in the list.</span></span>
    
10. <span data-ttu-id="a47fb-187">Em **Pessoas e Grupos**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-187">In **People and Groups**, click **New**.</span></span>
    
11. <span data-ttu-id="a47fb-188">Na caixa de diálogo **compartilhamento** , digite o nome do grupo de acesso de administradores do site, selecioná-la e, em seguida, clique em **compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-188">In the **Share** dialog box, type the name of the site admins access group, select it, and then click **Share**.</span></span>
    
12. <span data-ttu-id="a47fb-189">Clique no botão voltar de seu navegador.</span><span class="sxs-lookup"><span data-stu-id="a47fb-189">Click the back button on your browser.</span></span>
    
13. <span data-ttu-id="a47fb-190">Clique em \*\* \<nome do site > visitantes\*\* na lista.</span><span class="sxs-lookup"><span data-stu-id="a47fb-190">Click **\<site name> Visitors** in the list.</span></span>
    
14. <span data-ttu-id="a47fb-191">Em **Pessoas e Grupos**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-191">In **People and Groups**, click **New**.</span></span>
    
15. <span data-ttu-id="a47fb-192">Na caixa de diálogo **compartilhamento** , digite o nome do grupo de acesso ao site visualizadores, selecioná-la e, em seguida, clique em **compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="a47fb-192">In the **Share** dialog box, type the name of the site viewers access group, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="a47fb-193">Feche a guia **Permissões** do navegador.</span><span class="sxs-lookup"><span data-stu-id="a47fb-193">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="a47fb-194">Os resultados dessas configurações de permissão são:</span><span class="sxs-lookup"><span data-stu-id="a47fb-194">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="a47fb-195">O \*\* \<nome do site > proprietários\*\* grupo do SharePoint contém o grupo de acesso de administradores de site, no quais todos os membros têm o nível de permissão **controle total** .</span><span class="sxs-lookup"><span data-stu-id="a47fb-195">The **\<site name> Owners** SharePoint group contains the site admins access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="a47fb-196">O \*\* \<nome do site > membros\*\* grupo do SharePoint contém o grupo de acesso de membros do site, em que todos os membros têm o nível de permissão **Editar** .</span><span class="sxs-lookup"><span data-stu-id="a47fb-196">The **\<site name> Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="a47fb-197">O \*\* \<nome do site > visitantes\*\* grupo do SharePoint contém o site grupo visualizadores de acesso, no quais todos os membros têm o nível de permissão de **leitura** .</span><span class="sxs-lookup"><span data-stu-id="a47fb-197">The **\<site name> Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="a47fb-198">A capacidade de membros convidar outros membros ou de membros solicitar acesso está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a47fb-198">The ability for members to invite other members or for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="a47fb-199">Aqui está a configuração resultante com os três grupos do SharePoint para o site configurado para usar os três grupos de acesso, que são preenchidos com contas de usuário ou grupos do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a47fb-199">Here is your resulting configuration with the three SharePoint groups for the site configured to use the three access groups, which are populated with user accounts or Azure AD groups.</span></span>
  
![A configuração final do seu site isolado do SharePoint Online com contas de usuário e grupos de acesso.](media/e7618971-06ab-447b-90ff-d8be3790fe63.png)
  
<span data-ttu-id="a47fb-201">Você e os membros do site, por meio de associação de grupo em um dos grupos de acesso, agora podem colaborar usando os recursos do site.</span><span class="sxs-lookup"><span data-stu-id="a47fb-201">You and the members of the site, through group membership in one of the access groups, can now collaborate using the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="a47fb-202">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="a47fb-202">Next step</span></span>

<span data-ttu-id="a47fb-203">Quando você precisar alterar a associação de grupo de acesso do site ou criar uma pasta de documentos com permissões personalizadas, consulte [Gerenciar um site de equipe do SharePoint Online isolado](manage-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="a47fb-203">When you need to change site access group membership or create a document folder with custom permissions, see [Manage an isolated SharePoint Online team site](manage-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a47fb-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="a47fb-204">See Also</span></span>

[<span data-ttu-id="a47fb-205">Sites de equipe do SharePoint Online isolados</span><span class="sxs-lookup"><span data-stu-id="a47fb-205">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="a47fb-206">Projetar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="a47fb-206">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)
  
[<span data-ttu-id="a47fb-207">Gerenciar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="a47fb-207">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)
  



