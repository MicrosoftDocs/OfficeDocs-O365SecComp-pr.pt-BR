---
title: Gerenciar grupos no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Você pode usar o Exchange Online Protection (EOP) para criar grupos habilitados para email para uma organização do Exchange. Você também pode usar o EOP para definir ou atualizar as propriedades do grupo que especificam a associação, endereços de email e outros aspectos dos grupos.
ms.openlocfilehash: 744a28d2003496650e7350108797cc5cc4eaad4f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026338"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="b1084-104">Gerenciar grupos no EOP</span><span class="sxs-lookup"><span data-stu-id="b1084-104">Manage groups in EOP</span></span>

 <span data-ttu-id="b1084-p102">Você pode usar o Proteção do Exchange Online (EOP) para criar grupos habilitados para email para uma organização do Exchange. Você também pode usar o EOP para definir ou atualizar propriedades de grupo que especificam associação, endereços de email e outros aspectos de grupos. Você pode criar grupos de distribuição e grupos de segurança, dependendo das suas necessidades. Esses grupos podem ser criados usando o Centro de administração do Exchange (EAC) ou pelo Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="b1084-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span> 
  
## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="b1084-109">Tipos de grupos habilitados para email</span><span class="sxs-lookup"><span data-stu-id="b1084-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="b1084-110">Você pode criar dois tipos de grupos para sua organização do Exchange:</span><span class="sxs-lookup"><span data-stu-id="b1084-110">You can create two types of groups for your Exchange organization:</span></span>
  
- <span data-ttu-id="b1084-p103">[Criar um grupo no EAC](manage-groups-in-eop.md) (também conhecidos como grupos de distribuição) são coleções de usuários de email, como uma equipe ou outro grupo ad hoc, que precisam receber ou enviar emails sobre uma área comum de interesse. Os grupos de distribuição destinam-se exclusivamente à distribuição de mensagens de email. No EOP, um grupo de distribuição refere-se a qualquer grupo habilitado para email, esteja ou não em um contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="b1084-p103">[Create a group in the EAC](manage-groups-in-eop.md) (also known as distribution groups) are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest. Distribution groups are exclusively for distributing email messages. In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>
    
- <span data-ttu-id="b1084-p104">[Editar ou remover um grupo no EAC](manage-groups-in-eop.md) (também conhecidos como grupos de segurança) são coleções de usuários de email que precisam de permissões de acesso para funções de Administrador. Por exemplo, talvez você queira fornecer permissões de função de administrador a um grupo específico de usuários para que eles possam definir configurações antispam e antimalware.</span><span class="sxs-lookup"><span data-stu-id="b1084-p104">[Edit or remove a group in the EAC](manage-groups-in-eop.md) (also known as security groups) are collections of email users who need access permissions for Admin roles. For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b1084-p105">Por padrão, todos os novos grupos de segurança habilitados para email exigem que todos os remetentes sejam autenticados. Isso evita que remetentes externos enviem mensagens para grupos de segurança habilitados para email.</span><span class="sxs-lookup"><span data-stu-id="b1084-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="b1084-118">Antes de você começar</span><span class="sxs-lookup"><span data-stu-id="b1084-118">Before you begin</span></span>

- <span data-ttu-id="b1084-p106">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Grupos de Distribuição e Grupos de Segurança" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b1084-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="b1084-121">Lembre-se de que quando estiver criando e gerenciando grupos usando cmdlets do PowerShell remoto, você pode encontrar limitações.</span><span class="sxs-lookup"><span data-stu-id="b1084-121">Be aware that when creating and managing groups by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="b1084-122">Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis.</span><span class="sxs-lookup"><span data-stu-id="b1084-122">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="b1084-123">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Conectar-se ao Exchange Online Protection usando o PowerShell Remoto](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1084-123">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
- <span data-ttu-id="b1084-124">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="b1084-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="b1084-p107">Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="b1084-p107">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="b1084-128">Criar um grupo no EAC</span><span class="sxs-lookup"><span data-stu-id="b1084-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="b1084-129">No Centro de administração do Exchange (EAC), vá para **Destinatários** \> **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="b1084-129">In the Exchange admin center (EAC), go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="b1084-p108">Clique em **Novo**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.png) e em **Grupo de distribuição**, ou em **Grupo de segurança**, dependendo das suas necessidades. Consulte [Tipos de grupos habilitados para email](manage-groups-in-eop.md) para ver a diferença.</span><span class="sxs-lookup"><span data-stu-id="b1084-p108">Click **New**![Add Icon](../media/ITPro-EAC-AddIcon.png), and then click **Distribution group** or **Security group**, depending on your needs. See [Types of mail-enabled groups](manage-groups-in-eop.md) for the distinction.</span></span> 
    
3. <span data-ttu-id="b1084-132">Na página **Novo grupo de distribuição** ou **Novo grupo de segurança**, preencha os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="b1084-132">On the **New distribution group** or **New security group** page, complete the following fields:</span></span> 
    
  - <span data-ttu-id="b1084-p109">**Nome para exibição** Digite um nome para exibição que seja exclusivo em sua organização e significativo para usuários do EOP. É necessário fornecer o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="b1084-p109">**Display name** Type a display name that's unique to your organization and meaningful to EOP users. The display name is required.</span></span> 
    
  - <span data-ttu-id="b1084-p110">**Alias** Digite um alias de grupo de até 64 caracteres que seja exclusivo em sua organização. Os usuários do EOP digitam o alias na linha Para: de uma mensagem de email; então ele é convertido para o nome para exibição do grupo. Se você alterar o alias, o endereço SMTP principal do grupo também será alterado e conterá o novo alias. O alias é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b1084-p110">**Alias** Type a group alias of up to 64 characters that's unique to your organization. EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name. If you change the alias, the primary SMTP address for the group also changes and will contain the new alias. The alias is required.</span></span> 
    
  - <span data-ttu-id="b1084-139">**Descrição** Digite uma descrição do grupo de forma que as pessoas saibam qual é a finalidade do grupo.</span><span class="sxs-lookup"><span data-stu-id="b1084-139">**Description** Type a description of the group so that people will know the purpose of the group.</span></span> 
    
  - <span data-ttu-id="b1084-p111">**Proprietários** Por padrão, a pessoa que cria um grupo é o proprietário. Você pode adicionar um proprietário escolhendo **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.png). Todos os grupos devem ter no mínimo um proprietário.</span><span class="sxs-lookup"><span data-stu-id="b1084-p111">**Owners** By default, the person who creates the group is the owner. You can add an owner by choosing **Add**![Add Icon](../media/ITPro-EAC-AddIcon.png). All groups must have at least one owner.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b1084-143">Os proprietários do grupo não precisam ser membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="b1084-143">Owners don't have to be members of the group.</span></span> 
  
  - <span data-ttu-id="b1084-p112">**Membros** Use esta seção para adicionar membros e especificar se é necessário obter aprovação para que as pessoas ingressem ou saiam do grupo. Para adicionar membros ao grupo, clique em **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.png).</span><span class="sxs-lookup"><span data-stu-id="b1084-p112">**Members** Use this section to add group members and to specify whether approval is required for people to join or leave the group. To add members to the group, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.png).</span></span>
    
4. <span data-ttu-id="b1084-146">Clique em **OK** para retornar à página original.</span><span class="sxs-lookup"><span data-stu-id="b1084-146">Click **OK** to return to the original page.</span></span> 
    
5. <span data-ttu-id="b1084-p113">Quando você tiver terminado, clique em **Salvar** para criar o grupo. O novo grupo deve aparecer na lista de grupos.</span><span class="sxs-lookup"><span data-stu-id="b1084-p113">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span> 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="b1084-149">Editar ou remover um grupo no EAC</span><span class="sxs-lookup"><span data-stu-id="b1084-149">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="b1084-150">No EAC, navegue até **Destinatários** \> **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="b1084-150">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="b1084-151">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="b1084-151">Do one of the following:</span></span>
    
  - <span data-ttu-id="b1084-p114">Para editar um grupo: Na lista de grupos, clique no grupo de distribuição ou no grupo de segurança que deseja exibir ou alterar e clique em **Editar**![Ícone de edição](../media/ITPro-EAC-EditIcon.png). Você pode atualizar configurações gerais, adicionar ou remover proprietários de grupo e adicionar ou remover membros de grupo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="b1084-p114">To edit a group: In the list of groups, click the distribution or security group that you want to view or change, and then click **Edit**![Edit icon](../media/ITPro-EAC-EditIcon.png). You can update general settings, add or remove group owners, and add or remove group members, as needed.</span></span>
    
  - <span data-ttu-id="b1084-154">Para remover um grupo: Selecione o grupo e clique em **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.png).</span><span class="sxs-lookup"><span data-stu-id="b1084-154">To remove a group: Select the group and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.png).</span></span>
    
3. <span data-ttu-id="b1084-155">Ao terminar de fazer as alterações, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b1084-155">When you're finished making your changes, click **Save**.</span></span>
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="b1084-156">Criar, editar ou remover um grupo usando o Windows PowerShell remoto</span><span class="sxs-lookup"><span data-stu-id="b1084-156">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="b1084-p115">Esta seção fornece informações sobre a criação de grupos e alterações em suas propriedades usando o Windows PowerShell remoto. Também mostra como remover um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="b1084-p115">This section provides information about creating groups and changing their properties by using remote Windows PowerShell. It also shows how to remove an existing group.</span></span> 
  
 <span data-ttu-id="b1084-159">**Para criar um grupo usando o Windows PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="b1084-159">**To create a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="b1084-p116">Este exemplo usa o cmdlet [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) para criar um grupo de distribuição com um alias itadmin e o nome IT Administrators (Administradores de TI). Também adiciona usuários como membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="b1084-p116">This example uses the [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span> 
  
```
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

<span data-ttu-id="b1084-162">Para criar um grupo de segurança em vez de um grupo de distribuição, especifique  `-Type "Security"`.</span><span class="sxs-lookup"><span data-stu-id="b1084-162">To create a security group instead of a distribution group, specify  `-Type "Security"` instead.</span></span> 
  
<span data-ttu-id="b1084-163">Para verificar se você criou o grupo Administradores de TI com êxito, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) para exibir informações sobre o novo grupo:</span><span class="sxs-lookup"><span data-stu-id="b1084-163">To verify that you've successfully created the IT Administrators group, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to display information about the new group:</span></span> 
  
```
Get-Recipient "IT Administrators" | Format-List

```

<span data-ttu-id="b1084-164">Para obter uma lista dos membros no grupo, execute o cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b1084-164">To get a list of members in the group, run the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```
Get-DistributionGroupMember "IT Administrators"

```

<span data-ttu-id="b1084-165">Para obter uma lista completa de todos os seus grupos, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b1084-165">To get a full list of all your groups, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows:</span></span> 
  
```
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 <span data-ttu-id="b1084-166">**Para alterar as propriedades de um grupo usando o Windows PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="b1084-166">**To change the properties of a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="b1084-p117">Use os cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) e [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) para visualizar e alterar propriedades para grupos. Uma das vantagens de usar o PowerShell remoto, em vez do EAC, é a capacidade de alterar as propriedades de vários grupos.</span><span class="sxs-lookup"><span data-stu-id="b1084-p117">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlets to view and change properties for groups. An advantage of using remote PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span> 
  
<span data-ttu-id="b1084-169">Aqui estão alguns exemplos de uso do Windows PowerShell remoto para alterar as propriedades do grupo.</span><span class="sxs-lookup"><span data-stu-id="b1084-169">Here are some examples of using remote Windows PowerShell to change group properties.</span></span>
  
<span data-ttu-id="b1084-170">Esse exemplo usa o cmdlet [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) para alterar o endereço SMTP principal (também chamado de endereço de resposta) do grupo de Seattle Employees (Funcionários de Seattle) para sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="b1084-170">This example uses the [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet to change the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span> 
  
```
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

<span data-ttu-id="b1084-p118">Para verificar se você alterou com êxito as propriedades de um grupo, use o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx). Uma vantagem de usar o PowerShell remoto é que você pode exibir várias propriedades de vários grupos. No exemplo anterior, em que o endereço SMTP principal do grupo foi alterado, execute este comando para verificar o novo valor:</span><span class="sxs-lookup"><span data-stu-id="b1084-p118">To verify that you've successfully changed the properties for a group, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. One advantage of using remote PowerShell is that you can view multiple properties for multiple groups. In the previous example where the primary SMTP address group was changed, run the following command to verify the new value:</span></span> 
  
```
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

<span data-ttu-id="b1084-p119">Este exemplo usa o cmdlet [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) para atualizar todos os membros do grupo de Seattle Employees (Funcionários de Seattle). Use uma vírgula para separar todos os membros.</span><span class="sxs-lookup"><span data-stu-id="b1084-p119">This example uses the [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet to update all the members of the Seattle Employees group. Use a comma to separate all members.</span></span> 
  
```
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

<span data-ttu-id="b1084-176">Para obter a lista de todos os membros no grupo de Seattle Employees (Funcionários de Seattle), use o cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b1084-176">To get the list of all the members in the group Seattle Employees, use the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```
Get-DistributionGroupMember "Seattle Employees"

```

 <span data-ttu-id="b1084-177">**Para remover um grupo usando o Windows PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="b1084-177">**To remove a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="b1084-178">Este exemplo usa o cmdlet [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) para remover um grupo de distribuição chamado IT Administrators (Administradores de TI).</span><span class="sxs-lookup"><span data-stu-id="b1084-178">This example uses the [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet to remove a distribution group named IT Administrators.</span></span> 
  
```
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

<span data-ttu-id="b1084-179">Para verificar se o grupo foi removido, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira e confirme que o grupo (nesse caso "IT Administrators") foi excluído.</span><span class="sxs-lookup"><span data-stu-id="b1084-179">To verify that the group was removed, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows, and confirm that the group (in this case "It Administrators") was deleted.</span></span> 
  
```
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


