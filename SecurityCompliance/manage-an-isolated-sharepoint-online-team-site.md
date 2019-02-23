---
title: Gerenciar um site de equipe do SharePoint Online isolado
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: 'Resumo: Gerencie seu site de equipe do SharePoint Online isolado com estes procedimentos.'
ms.openlocfilehash: 81a6fcd80bb3e4950eb7b783d1ad964b9bc67cc5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214481"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="b8e32-103">Gerenciar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="b8e32-103">Manage an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="b8e32-104">**Resumo:** Gerencie seu site de equipe do SharePoint Online isolado com estes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="b8e32-104">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>
  
<span data-ttu-id="b8e32-105">Este artigo descreve as operações de gerenciamento comuns para um site de equipe do SharePoint Online isolado.</span><span class="sxs-lookup"><span data-stu-id="b8e32-105">This article describes common management operations for an isolated SharePoint Online team site.</span></span>
  
## <a name="add-a-new-user"></a><span data-ttu-id="b8e32-106">Adicionar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="b8e32-106">Add a new user</span></span>

<span data-ttu-id="b8e32-107">Quando alguém novo ingressar no site, você deverá decidir o nível de participação no site:</span><span class="sxs-lookup"><span data-stu-id="b8e32-107">When someone new joins the site, you must decide their level of participation in the site:</span></span>
  
- <span data-ttu-id="b8e32-108">Administração: adicionar a nova conta de usuário ao grupo de acesso de administradores de site</span><span class="sxs-lookup"><span data-stu-id="b8e32-108">Administration: Add the new user account to the site admins access group</span></span>
    
- <span data-ttu-id="b8e32-109">Colaboração ativa: adicionar a conta de usuário ao grupo de acesso de membros do site</span><span class="sxs-lookup"><span data-stu-id="b8e32-109">Active collaboration: Add the user account to the site members access group</span></span>
    
- <span data-ttu-id="b8e32-110">Exibindo: adicionar a conta de usuário ao grupo de acesso de visualizadores de sites</span><span class="sxs-lookup"><span data-stu-id="b8e32-110">Viewing: Add the user account to the site viewers access group</span></span>
    
<span data-ttu-id="b8e32-111">Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server Active Directory (AD), adicione os usuários apropriados aos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Assinatura do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b8e32-111">If you are managing user accounts and groups through Windows Server Active Directory (AD), add the appropriate users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="b8e32-112">Se você estiver gerenciando contas de usuário e grupos através do Office 365, poderá usar o centro de administração do Office ou o Microsoft PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-112">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or Microsoft PowerShell:</span></span>
  
- <span data-ttu-id="b8e32-113">Para o centro de administração do Office, entre com uma conta de usuário que tenha recebido a função Administrador de conta de usuário ou administrador da empresa e use grupos para adicionar os usuários apropriados aos grupos de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="b8e32-113">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>
    
- <span data-ttu-id="b8e32-p101">Para o PowerShell, primeiro [Conecte-se ao módulo PowerShell do Azure Active Directory v2](https://go.microsoft.com/fwlink/?linkid=842218). Para adicionar uma conta de usuário a um grupo de acesso com seu nome de usuário principal (UPN), use o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-p101">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="b8e32-116">Para um arquivo de texto que contém todos os comandos do PowerShell e uma planilha de configuração do Excel que gera comandos do PowerShell com base em seus nomes de conta de usuário e de grupo, baixe o [Kit de implantação de site de equipe do SharePoint Online isolado](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span><span class="sxs-lookup"><span data-stu-id="b8e32-116">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 

<span data-ttu-id="b8e32-117">Para adicionar uma conta de usuário a um grupo de acesso com seu nome de exibição, use o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-117">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="b8e32-118">Adicionar um novo grupo</span><span class="sxs-lookup"><span data-stu-id="b8e32-118">Add a new group</span></span>

<span data-ttu-id="b8e32-119">Para adicionar acesso a um grupo inteiro, você deve decidir o nível de participação de todos os membros do grupo no site:</span><span class="sxs-lookup"><span data-stu-id="b8e32-119">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>
  
- <span data-ttu-id="b8e32-120">Administração: Adicionar o grupo ao grupo de acesso de administradores de site</span><span class="sxs-lookup"><span data-stu-id="b8e32-120">Administration: Add the group to the site admins access group</span></span>
    
- <span data-ttu-id="b8e32-121">Colaboração ativa: Adicionar o grupo ao grupo de acesso de membros do site</span><span class="sxs-lookup"><span data-stu-id="b8e32-121">Active collaboration: Add the group to the site members access group</span></span>
    
- <span data-ttu-id="b8e32-122">Exibindo: Adicionar o grupo ao grupo de acesso visualizadores de sites</span><span class="sxs-lookup"><span data-stu-id="b8e32-122">Viewing: Add the group to the site viewers access group</span></span>
    
<span data-ttu-id="b8e32-123">Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server AD, adicione os grupos apropriados aos grupos apropriados usando seus procedimentos normais de gerenciamento de usuário e grupo do Windows Server AD e aguarde a sincronização com sua assinatura do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b8e32-123">If you are managing user accounts and groups through Windows Server AD, add the appropriate groups to the appropriate groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="b8e32-124">Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-124">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="b8e32-125">Para o centro de administração do Office, entre com uma conta de usuário que tenha recebido a função Administrador de conta de usuário ou administrador da empresa e use grupos para adicionar os grupos apropriados aos grupos de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="b8e32-125">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>
    
- <span data-ttu-id="b8e32-p102">Para o PowerShell, primeiro [Conecte-se ao módulo PowerShell do Azure Active Directory v2](https://go.microsoft.com/fwlink/?linkid=842218). Em seguida, use os seguintes comandos do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-p102">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). Then, use the following PowerShell commands:</span></span>
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="b8e32-128">Remover um usuário</span><span class="sxs-lookup"><span data-stu-id="b8e32-128">Remove a user</span></span>

<span data-ttu-id="b8e32-129">Quando o acesso de alguém precisa ser removido do site, você os remove do grupo de acesso para o qual eles são membros atualmente, com base na sua participação no site:</span><span class="sxs-lookup"><span data-stu-id="b8e32-129">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="b8e32-130">Administração: Remova a conta de usuário do grupo de acesso de administradores de site</span><span class="sxs-lookup"><span data-stu-id="b8e32-130">Administration: Remove the user account from the site admins access group</span></span>
    
- <span data-ttu-id="b8e32-131">Colaboração ativa: Remova a conta de usuário do grupo de acesso de membros do site</span><span class="sxs-lookup"><span data-stu-id="b8e32-131">Active collaboration: Remove the user account from the site members access group</span></span>
    
- <span data-ttu-id="b8e32-132">Exibição: remover a conta de usuário do grupo de acesso de visualizadores de sites</span><span class="sxs-lookup"><span data-stu-id="b8e32-132">Viewing: Remove the user account from the site viewers access group</span></span>
    
<span data-ttu-id="b8e32-133">Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server AD, remova os usuários apropriados dos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Office 365 scriçõe.</span><span class="sxs-lookup"><span data-stu-id="b8e32-133">If you are managing user accounts and groups through Windows Server AD, remove the appropriate users from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="b8e32-134">Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-134">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="b8e32-135">Para o centro de administração do Office, entre com uma conta de usuário que tenha atribuído a função Administrador de conta de usuário ou administrador da empresa e use grupos para remover os usuários apropriados dos grupos de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="b8e32-135">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>
    
- <span data-ttu-id="b8e32-p103">Para o PowerShell, primeiro [Conecte-se ao módulo PowerShell do Azure Active Directory v2](https://go.microsoft.com/fwlink/?linkid=842218). Para remover uma conta de usuário de um grupo de acesso com seu UPN, use o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-p103">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="b8e32-138">Para remover uma conta de usuário de um grupo de acesso com seu nome de exibição, use o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-138">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="b8e32-139">Remover um grupo</span><span class="sxs-lookup"><span data-stu-id="b8e32-139">Remove a group</span></span>

<span data-ttu-id="b8e32-140">Para remover o acesso de um grupo inteiro, remova o grupo do grupo de acesso para o qual eles são membros atualmente com base em sua participação no site:</span><span class="sxs-lookup"><span data-stu-id="b8e32-140">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="b8e32-141">Administração: remover o grupo do grupo de acesso de administradores de site</span><span class="sxs-lookup"><span data-stu-id="b8e32-141">Administration: Remove the group from the site admins access group</span></span>
    
- <span data-ttu-id="b8e32-142">Colaboração ativa: remover o grupo do grupo de acesso de membros do site</span><span class="sxs-lookup"><span data-stu-id="b8e32-142">Active collaboration: Remove the group from the site members access group</span></span>
    
- <span data-ttu-id="b8e32-143">Exibição: remover o grupo do grupo de acesso de visualizadores de sites</span><span class="sxs-lookup"><span data-stu-id="b8e32-143">Viewing: Remove the group from the site viewers access group</span></span>
    
<span data-ttu-id="b8e32-144">Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server Active Directory, remova os grupos apropriados dos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Assinatura do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b8e32-144">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="b8e32-145">Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-145">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="b8e32-146">Para o centro de administração do Office, entre com uma conta de usuário que tenha atribuído a função Administrador de conta de usuário ou administrador da empresa e use grupos para remover os grupos apropriados dos grupos de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="b8e32-146">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>
    
- <span data-ttu-id="b8e32-147">Para o PowerShell, primeiro [Conecte-se ao módulo PowerShell do Azure Active Directory v2](https://go.microsoft.com/fwlink/?linkid=842218).</span><span class="sxs-lookup"><span data-stu-id="b8e32-147">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218).</span></span>    
<span data-ttu-id="b8e32-148">Para remover um grupo de um grupo de acesso usando seus nomes de exibição, use o seguinte bloco de comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b8e32-148">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="b8e32-149">Criar uma subpasta documentos com permissões personalizadas</span><span class="sxs-lookup"><span data-stu-id="b8e32-149">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="b8e32-p104">Em alguns casos, um subconjunto das pessoas que trabalham dentro do site isolado precisa de um local mais privado para colaborar. Para sites do SharePoint Online, você pode criar uma subpasta na pasta documentos do site e atribuir permissões personalizadas. Aqueles sem permissões não verão a subpasta.</span><span class="sxs-lookup"><span data-stu-id="b8e32-p104">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>
  
<span data-ttu-id="b8e32-153">Para criar uma subpasta documentos com permissões personalizadas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b8e32-153">To create a documents subfolder with custom permissions, do the following:</span></span>
  
1. <span data-ttu-id="b8e32-p105">Entre no Office 365 com uma conta que seja membro do grupo de acesso de administradores para o site. Para obter ajuda, confira [onde entrar no Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="b8e32-p105">Sign in to Office 365 with an account that is a member of the admins access group for the site. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="b8e32-156">Vá para o site de equipe isolado e clique em **documentos**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-156">Go to the isolated team site and click **Documents**.</span></span>
    
3. <span data-ttu-id="b8e32-157">Navegue até a pasta na pasta documentos que conterá a subpasta com permissões personalizadas, crie a pasta e, em seguida, abra-a.</span><span class="sxs-lookup"><span data-stu-id="b8e32-157">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>
    
4. <span data-ttu-id="b8e32-158">Clique em **Compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-158">Click **Share**.</span></span>
    
5. <span data-ttu-id="b8e32-159">Clique em **compartilhado com o _GT_ avançado**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-159">Click **Shared with > Advanced**.</span></span>
    
6. <span data-ttu-id="b8e32-160">Clique em **parar de herdar permissões**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-160">Click **Stop inheriting permissions**, and then click **OK**.</span></span>
    
7. <span data-ttu-id="b8e32-161">Clique em **Compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-161">Click **Share**.</span></span>
    
8. <span data-ttu-id="b8e32-162">Clique em **compartilhado com o _GT_ avançado**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-162">Click **Shared with > Advanced**.</span></span>
    
9. <span data-ttu-id="b8e32-163">Clique em **conceder permissões _GT_ Shared com o _GT_ avançado**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-163">Click **Grant Permissions > Shared with > Advanced**.</span></span>
    
10. <span data-ttu-id="b8e32-164">Na página permissões, clique em \*\* \<membros do name> de site na lista\*\*.</span><span class="sxs-lookup"><span data-stu-id="b8e32-164">On the permissions page, click **\<site name> Members in the list**.</span></span>
    
11. <span data-ttu-id="b8e32-165">Na página \*\* \<membros do site name>\*\* , selecione a marca de seleção ao lado do grupo de acesso de membros do site, clique em **ações**, clique em **remover usuários do grupo**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-165">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>
    
12. <span data-ttu-id="b8e32-166">Para adicionar membros específicos a essa subpasta, clique em **novo _GT_ adicionar usuários**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-166">To add specific members to this subfolder, click **New > Add users**.</span></span>
    
13. <span data-ttu-id="b8e32-167">Na caixa de diálogo **compartilhar** , digite os nomes das contas de usuário que podem colaborar em arquivos na subpasta e, em seguida, clique em **compartilhar**.</span><span class="sxs-lookup"><span data-stu-id="b8e32-167">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>
    
14. <span data-ttu-id="b8e32-168">Atualize a página da Web para ver os novos resultados.</span><span class="sxs-lookup"><span data-stu-id="b8e32-168">Refresh the web page to see the new results.</span></span>
    
15. <span data-ttu-id="b8e32-169">em **grupos** no painel de navegação à esquerda, clique no grupo \*\* \<visitantes do name> do site\*\* e use as etapas 11-14 para especificar o conjunto de contas de usuário que podem exibir os arquivos na subpasta (conforme necessário).</span><span class="sxs-lookup"><span data-stu-id="b8e32-169">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>
    
16. <span data-ttu-id="b8e32-170">em **grupos** no painel de navegação à esquerda, clique no \*\* \<grupo proprietários do site name>\*\* e use as etapas 11-14 para especificar o conjunto de contas de usuário que podem administrar as permissões na subpasta (conforme necessário).</span><span class="sxs-lookup"><span data-stu-id="b8e32-170">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>
    
17. <span data-ttu-id="b8e32-171">Feche a guia **pessoas e grupos** no navegador.</span><span class="sxs-lookup"><span data-stu-id="b8e32-171">Close the **People and Groups** tab in your browser.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8e32-172">Confira também
</span><span class="sxs-lookup"><span data-stu-id="b8e32-172">See Also</span></span>

[<span data-ttu-id="b8e32-173">Sites de equipe do SharePoint Online isolados</span><span class="sxs-lookup"><span data-stu-id="b8e32-173">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="b8e32-174">Projetar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="b8e32-174">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="b8e32-175">Implantar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="b8e32-175">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



