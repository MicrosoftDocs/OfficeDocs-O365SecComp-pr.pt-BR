---
title: Projetar um site de equipe do SharePoint Online isolado
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Resumo: Percorra o processo de design para sites de equipe isolados do SharePoint Online.'
ms.openlocfilehash: 09748fcc22a4a48efc4346ff75a225db612a0ef4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216151"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="eb86d-103">Projetar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="eb86d-103">Design an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="eb86d-104">**Resumo:** Percorra o processo de design para sites de equipe isolados do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="eb86d-104">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="eb86d-105">Este artigo orienta as principais decisões de design que você deve fazer antes de criar um site de equipe do SharePoint Online isolado.</span><span class="sxs-lookup"><span data-stu-id="eb86d-105">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="eb86d-106">Fase 1: determinar seus grupos e níveis de permissão do SharePoint</span><span class="sxs-lookup"><span data-stu-id="eb86d-106">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="eb86d-107">Todos os sites de equipe do SharePoint Online por padrão são criados com os seguintes grupos do SharePoint:</span><span class="sxs-lookup"><span data-stu-id="eb86d-107">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>
  
- <span data-ttu-id="eb86d-108">\<Membros name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-108">\<site name> Members</span></span>
    
- <span data-ttu-id="eb86d-109">\<Visitantes do site name></span><span class="sxs-lookup"><span data-stu-id="eb86d-109">\<site name> Visitors</span></span>
    
- <span data-ttu-id="eb86d-110">\<Proprietários de name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-110">\<site name> Owners</span></span>
    
<span data-ttu-id="eb86d-111">Esses grupos são separados dos grupos do Office 365 e do Azure Active Directory (AD) e são a base para atribuir permissões para os recursos do site.</span><span class="sxs-lookup"><span data-stu-id="eb86d-111">These groups are separate from Office 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>
  
<span data-ttu-id="eb86d-p101">O conjunto de permissões específicas que determina o que um membro de um grupo do SharePoint pode fazer em um site é um nível de permissão. Há três níveis de permissão por padrão para um site de equipe do SharePoint Online: editar, ler e controle total. A tabela a seguir mostra a correlação padrão de grupos do SharePoint e níveis de permissão atribuídos:</span><span class="sxs-lookup"><span data-stu-id="eb86d-p101">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level. There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control. The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>
  
|<span data-ttu-id="eb86d-115">**Grupo do SharePoint**</span><span class="sxs-lookup"><span data-stu-id="eb86d-115">**SharePoint group**</span></span>|<span data-ttu-id="eb86d-116">**Nível de permissão**</span><span class="sxs-lookup"><span data-stu-id="eb86d-116">**Permission level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb86d-117">\<Membros name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-117">\<site name> Members</span></span>  <br/> |<span data-ttu-id="eb86d-118">Editar</span><span class="sxs-lookup"><span data-stu-id="eb86d-118">Edit</span></span>  <br/> |
|<span data-ttu-id="eb86d-119">\<Visitantes do site name></span><span class="sxs-lookup"><span data-stu-id="eb86d-119">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="eb86d-120">Ler</span><span class="sxs-lookup"><span data-stu-id="eb86d-120">Read</span></span>  <br/> |
|<span data-ttu-id="eb86d-121">\<Proprietários de name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-121">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="eb86d-122">Controle total</span><span class="sxs-lookup"><span data-stu-id="eb86d-122">Full control</span></span>  <br/> |
   
 <span data-ttu-id="eb86d-p102">Práticas **recomendadas:** Você pode criar grupos adicionais do SharePoint e níveis de permissão. No enTanto, recomendamos o uso dos grupos e níveis de permissão padrão do SharePoint para seu site isolado do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p102">**Best practice:** You can create additional SharePoint groups and permission levels. However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>
  
<span data-ttu-id="eb86d-125">Estes são os grupos e os níveis de permissão padrão do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="eb86d-125">Here are the default SharePoint groups and permission levels.</span></span>
  
![Os grupos do SharePoint e níveis de permissão padrão de um site do SharePoint Online.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="eb86d-127">Fase 2: atribuir permissões a usuários com grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="eb86d-127">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="eb86d-p103">Você pode atribuir permissões aos usuários adicionando sua conta de usuário ou um grupo do Office 365 ou do Azure AD do qual a conta de usuário é membro, para os grupos do SharePoint. Depois de adicionada, as contas de usuário do Office 365, direta ou indiretamente, via Associação a um grupo do Office 365 ou do Azure AD, recebem o nível de permissão associado ao grupo do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p103">You can assign permissions to users by adding their user account, or an Office 365 or Azure AD group of which the user account is a member, to the SharePoint groups. Once added, the Office 365 user accounts, either directly or indirectly via membership in an Office 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>
  
<span data-ttu-id="eb86d-130">Usando os grupos padrão do SharePoint como exemplo:</span><span class="sxs-lookup"><span data-stu-id="eb86d-130">Using the default SharePoint groups as an example:</span></span>
  
- <span data-ttu-id="eb86d-131">Os membros do grupo \*\* \<site name> Members\*\* SharePoint, que podem incluir contas de usuário e grupos, recebem o nível de permissão **Editar**</span><span class="sxs-lookup"><span data-stu-id="eb86d-131">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>
    
- <span data-ttu-id="eb86d-132">Os membros do grupo \*\* \<site name> visitantes\*\* do SharePoint, que podem incluir contas de usuário e grupos, recebem o nível de permissão de **leitura**</span><span class="sxs-lookup"><span data-stu-id="eb86d-132">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>
    
- <span data-ttu-id="eb86d-133">Os membros do grupo \*\* \<sites name> proprietários do site\*\* , que podem incluir contas de usuário e grupos, recebem o nível de permissão **controle total**</span><span class="sxs-lookup"><span data-stu-id="eb86d-133">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>
    
 <span data-ttu-id="eb86d-p104">Práticas **recomendadas:** Embora você possa gerenciar permissões por meio de contas de usuário individuais, recomendamos usar um único grupo do Azure AD, conhecido como grupo de acesso, em vez disso. Isso simplifica o gerenciamento de permissões por meio da associação no grupo de acesso, em vez de gerenciar a lista de contas de usuário para cada grupo do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p104">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead. This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>
  
<span data-ttu-id="eb86d-p105">Os grupos do Azure AD para Office 365 são diferentes dos grupos do Office 365. Os grupos do Azure AD aparecem no centro de administração do Office com o **tipo** definido como **segurança** e não têm um endereço de email. Os grupos do Azure AD podem ser gerenciados em:</span><span class="sxs-lookup"><span data-stu-id="eb86d-p105">Azure AD groups for Office 365 are different than Office 365 groups. Azure AD groups appear in the Office Admin center with their **Type** set to **Security** and do not have an email address. Azure AD groups can be managed within:</span></span>
  
- <span data-ttu-id="eb86d-139">Windows Server Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="eb86d-139">Windows Server Active Directory (AD)</span></span>
    
    <span data-ttu-id="eb86d-p106">Estes são os grupos que foram criados em sua infraestrutura local do AD do Windows Server e estão sincronizados com a sua assinatura do Office 365. No centro de administração do Office, esses grupos têm \*\*\*\* um status **sincronizado com o Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p106">These are groups that have been created in your on-premises Windows Server AD infrastructure and synchronized to your Office 365 subscription. In the Office Admin center, these groups have a **Status** of **Synched with active directory**.</span></span>
    
- <span data-ttu-id="eb86d-142">Office 365</span><span class="sxs-lookup"><span data-stu-id="eb86d-142">Office 365</span></span>
    
    <span data-ttu-id="eb86d-p107">Estes são os grupos que foram criados usando o centro de administração do Office, o portal do Azure ou o Microsoft PowerShell. No centro de administração do Office, esses grupos têm um **status** de **nuvem**.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p107">These are groups that have been created using either the Office Admin center, the Azure portal, or Microsoft PowerShell. In the Office Admin center, these groups have a **Status** of **Cloud**.</span></span>
    
 <span data-ttu-id="eb86d-145">Práticas **recomendadas:** Se você estiver usando o Windows Server AD no local e estiver sincronizando com sua assinatura do Office 365, realize o gerenciamento de usuário e de grupo com o Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="eb86d-145">**Best practice:** If you are using Windows Server AD on-premises and synchronizing with your Office 365 subscription, perform your user and group management with Windows Server AD.</span></span>
  
<span data-ttu-id="eb86d-146">Para sites de equipe isolados do SharePoint Online, a estrutura de grupo recomendada é semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="eb86d-146">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>
  
|<span data-ttu-id="eb86d-147">**Grupo do SharePoint**</span><span class="sxs-lookup"><span data-stu-id="eb86d-147">**SharePoint group**</span></span>|<span data-ttu-id="eb86d-148">**Grupo de acesso baseado no AD do Azure**</span><span class="sxs-lookup"><span data-stu-id="eb86d-148">**Azure AD-based access group**</span></span>|<span data-ttu-id="eb86d-149">**Nível de permissão**</span><span class="sxs-lookup"><span data-stu-id="eb86d-149">**Permission level**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb86d-150">\<Membros name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-150">\<site name> Members</span></span>  <br/> |<span data-ttu-id="eb86d-151">\<Membros name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-151">\<site name> Members</span></span>  <br/> |<span data-ttu-id="eb86d-152">Editar</span><span class="sxs-lookup"><span data-stu-id="eb86d-152">Edit</span></span>  <br/> |
|<span data-ttu-id="eb86d-153">\<Visitantes do site name></span><span class="sxs-lookup"><span data-stu-id="eb86d-153">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="eb86d-154">\<Visualizadores de name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-154">\<site name> Viewers</span></span>  <br/> |<span data-ttu-id="eb86d-155">Ler</span><span class="sxs-lookup"><span data-stu-id="eb86d-155">Read</span></span>  <br/> |
|<span data-ttu-id="eb86d-156">\<Proprietários de name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-156">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="eb86d-157">\<Administradores de name> de site</span><span class="sxs-lookup"><span data-stu-id="eb86d-157">\<site name> Admins</span></span>  <br/> |<span data-ttu-id="eb86d-158">Controle total</span><span class="sxs-lookup"><span data-stu-id="eb86d-158">Full control</span></span>  <br/> |
   
 <span data-ttu-id="eb86d-p108">Práticas **recomendadas:** Embora você possa usar os grupos do Office 365 ou do Azure AD como membros de grupos do SharePoint, recomendamos usar os grupos do Azure AD. Os grupos do Azure AD, gerenciados pelo Windows Server AD ou pelo Office 365, oferecem mais flexibilidade para usar grupos aninhados para atribuir permissões.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p108">**Best practice:** Although you can use either Office 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups. Azure AD groups, managed either through Windows Server AD or Office 365, give you more flexibility to use nested groups to assign permissions.</span></span>
  
<span data-ttu-id="eb86d-161">Estes são os grupos padrão do SharePoint configurados para usar grupos de acesso baseados no Azure AD.</span><span class="sxs-lookup"><span data-stu-id="eb86d-161">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>
  
![Usando os grupos de acesso como membros de grupos de sites do SharePoint Online padrão.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
<span data-ttu-id="eb86d-163">Ao projetar os três grupos de acesso, tenha em mente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eb86d-163">When designing the three access groups, keep the following in mind:</span></span>
  
- <span data-ttu-id="eb86d-164">Deve haver apenas alguns membros no grupo de acesso de \*\* \<administradores do site name>\*\* , correspondente a um pequeno número de administradores do SharePoint Online que estão gerenciando o site de equipe.</span><span class="sxs-lookup"><span data-stu-id="eb86d-164">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>
    
- <span data-ttu-id="eb86d-p109">A maioria dos membros do site estão nos grupos de acesso de \*\* \<name> de site\*\* ou \*\* \<\*\* membros do site name> visualizadores. Como os membros do site no grupo de acesso de \*\* \<membros do site name>\*\* podem excluir ou modificar recursos no site, considere cuidadosamente sua associação. Quando estiver em dúvida, adicione o membro de site \*\* \<\*\* ao grupo de acesso name> visualizadores de site.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p109">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups. Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership. When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>
    
<span data-ttu-id="eb86d-168">Veja um exemplo de grupos do SharePoint e grupos de acesso para um site isolado chamado projeto x.</span><span class="sxs-lookup"><span data-stu-id="eb86d-168">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>
  
![Um exemplo de como usar os grupos de acesso em um site do SharePoint Online chamado ProjectX.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="eb86d-170">Fase 3: usar grupos aninhados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="eb86d-170">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="eb86d-p110">Para um projeto confinado a um pequeno número de pessoas, um único nível de grupos de acesso baseado no AD do Azure adicionado aos grupos do SharePoint do site se ajustará à maioria dos cenários. No enTanto, se você tiver um grande número de pessoas e essas pessoas já forem membros dos grupos do Azure AD estabelecidos, poderá atribuir permissões do SharePoint com mais facilidade usando grupos aninhados ou grupos que contenham outros grupos como membros.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p110">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios. However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>
  
<span data-ttu-id="eb86d-p111">Por exemplo, você deseja criar um site de equipe isolado do SharePoint Online para colaboração entre os executivos dos departamentos de vendas, marketing, engenharia, legal e de suporte e esses departamentos que já têm seus próprios grupos com conta de usuário executivo Academy. Em vez de criar um novo grupo para os novos membros do site e colocar todas as contas de usuário executivo individuais, coloque os grupos executivos existentes para cada departamento do novo grupo.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p111">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership. Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>
  
 <span data-ttu-id="eb86d-p112">Se você estiver compartilhando uma assinatura do Office 365 entre várias organizações, pode ser difícil gerenciar um único nível de associação de grupo para um site isolado para uma organização devido ao número enorme de contas de usuário. Nesse caso, você pode usar grupos aninhados do Azure AD para cada organização que contenha os grupos dentro de suas organizações para gerenciar as permissões.</span><span class="sxs-lookup"><span data-stu-id="eb86d-p112">If you are sharing an Office 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts. In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>
  
<span data-ttu-id="eb86d-177">Para usar grupos aninhados do Azure AD:</span><span class="sxs-lookup"><span data-stu-id="eb86d-177">To use nested Azure AD groups:</span></span>
  
1. <span data-ttu-id="eb86d-178">Identifique ou crie os grupos do Azure AD que conterá as contas de usuário e adicione as contas de usuário apropriadas como membros.</span><span class="sxs-lookup"><span data-stu-id="eb86d-178">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>
    
2. <span data-ttu-id="eb86d-179">Crie o grupo de acesso baseado em AD do Azure de contêiner que conterá os outros grupos do Azure AD e adicione esses grupos como membros.</span><span class="sxs-lookup"><span data-stu-id="eb86d-179">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>
    
3.  <span data-ttu-id="eb86d-180">Para o nível de acesso apropriado para o grupo de acesso de contêiner, identifique o grupo do SharePoint e o nível de permissão correspondente.</span><span class="sxs-lookup"><span data-stu-id="eb86d-180">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>
    
> [!NOTE]
> <span data-ttu-id="eb86d-181">Não é possível usar grupos aninhados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="eb86d-181">You cannot use nested Office 365 groups.</span></span> 
  
<span data-ttu-id="eb86d-182">Veja um exemplo de grupos aninhados do Azure AD para o grupo de acesso de membros do projeto x.</span><span class="sxs-lookup"><span data-stu-id="eb86d-182">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>
  
![Um exemplo de como usar grupos de acesso aninhados para o grupo de acesso de membros do site do ProjectX.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
<span data-ttu-id="eb86d-184">Como todas as contas de usuário nas equipes de pesquisa, engenharia e projetos líderes do projeto devem ser membros do site, é mais fácil adicionar seus grupos do Azure AD ao grupo de acesso de membros do projeto x.</span><span class="sxs-lookup"><span data-stu-id="eb86d-184">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="eb86d-185">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="eb86d-185">Next step</span></span>

<span data-ttu-id="eb86d-186">Quando estiver pronto para criar e configurar um site isolado em produção, consulte [implantar um site de equipe isolado do SharePoint Online](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="eb86d-186">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb86d-187">Confira também
</span><span class="sxs-lookup"><span data-stu-id="eb86d-187">See Also</span></span>

[<span data-ttu-id="eb86d-188">Sites de equipe do SharePoint Online isolados</span><span class="sxs-lookup"><span data-stu-id="eb86d-188">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="eb86d-189">Gerenciar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="eb86d-189">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="eb86d-190">Implantar um site de equipe do SharePoint Online isolado</span><span class="sxs-lookup"><span data-stu-id="eb86d-190">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



