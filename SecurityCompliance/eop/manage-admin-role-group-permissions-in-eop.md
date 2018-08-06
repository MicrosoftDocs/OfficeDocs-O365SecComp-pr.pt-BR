---
title: Gerenciar permissões do grupo de funções de administrador no EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: No Microsoft Proteção do Exchange Online (EOP), é possível usar o Centro de administração do Exchange (EAC) para tornar um usuário membro de um grupo ou de grupos de funções a fim de atribuir a ele permissões de execução de tarefas administrativas específicas. Também é possível remover um usuário de um grupo ou grupo de funções usando o EAC.
ms.openlocfilehash: 5d50c77c97f2c345aa3994e7fa3ecd2eea93a13a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026658"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="d97d6-104">Gerenciar permissões do grupo de funções de administrador no EOP</span><span class="sxs-lookup"><span data-stu-id="d97d6-104">Manage admin role group permissions in EOP</span></span>
  
<span data-ttu-id="d97d6-p102">No Microsoft Proteção do Exchange Online (EOP), é possível usar o Centro de administração do Exchange (EAC) para tornar um usuário membro de um grupo ou de grupos de funções a fim de atribuir a ele permissões de execução de tarefas administrativas específicas. Também é possível remover um usuário de um grupo ou grupo de funções usando o EAC.</span><span class="sxs-lookup"><span data-stu-id="d97d6-p102">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d97d6-107">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="d97d6-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d97d6-108">Tempo estimado para conclusão: 5 a 10 minutos</span><span class="sxs-lookup"><span data-stu-id="d97d6-108">Estimated time to complete: 5-10 minutes</span></span>
    
- <span data-ttu-id="d97d6-p103">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e funções de grupo" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="d97d6-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="d97d6-p104">Determinadas permissões no Office 365 mapeiam para as permissões do grupo de funções de administração do EOP. Para obter mais informações, consulte a coluna "Função no Exchange Online" na seção "Para quais serviços minhas permissões do Office 365 se estendem?" em [Atribuição de funções de administração](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span><span class="sxs-lookup"><span data-stu-id="d97d6-p104">Certain permissions in Office 365 map to EOP admin role group permissions. For more information, see the "Role in Exchange Online" column in the "Which services do my Office 365 permissions extend to?" section in [Assigning Admin Roles](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span></span>
    
- <span data-ttu-id="d97d6-114">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="d97d6-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="d97d6-p105">Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="d97d6-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="what-do-you-want-to-do"></a><span data-ttu-id="d97d6-118">O que você deseja fazer?</span><span class="sxs-lookup"><span data-stu-id="d97d6-118">What do you want to do?</span></span>

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="d97d6-119">Usar o EAC para atribuir membros a grupos de funções de administração</span><span class="sxs-lookup"><span data-stu-id="d97d6-119">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="d97d6-120">No EAC, navegue até **Permissões** \> **Funções de Administração**, clique no grupo de funções ao qual você deseja adicionar o usuário ou usuários e clique em **Editar**![Ícone de edição](../media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="d97d6-120">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to add the user or users to, and then click **Edit**![Edit icon](../media/ITPro-EAC-EditIcon.png).</span></span>
    
2. <span data-ttu-id="d97d6-p106">Em Membros, clique em **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.png). A janela Selecionar Membros será exibida.</span><span class="sxs-lookup"><span data-stu-id="d97d6-p106">Under Members, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.png). The Select Members window will appear.</span></span>
    
3. <span data-ttu-id="d97d6-123">Procure o usuário ou usuários que você deseja adicionar ou selecione-os na lista.</span><span class="sxs-lookup"><span data-stu-id="d97d6-123">Search for the user or users that you wish to add, or select them from the list.</span></span>
    
4. <span data-ttu-id="d97d6-p107">Depois de selecionar o usuário ou usuários que você deseja adicionar, clique em **Adicionar** e clique em **OK**. A janela Selecionar Membros será fechada.</span><span class="sxs-lookup"><span data-stu-id="d97d6-p107">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>
    
5. <span data-ttu-id="d97d6-p108">Você verá que o usuário foi adicionado ao painel **Membros**. Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d97d6-p108">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d97d6-128">Os usuários precisam sair e entrar novamente para ver a alteração em seus diretos administrativos após a adição ou remoção de membros do grupo de funções.</span><span class="sxs-lookup"><span data-stu-id="d97d6-128">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="d97d6-129">Usar o EAC para remover membros de grupos de funções de administração</span><span class="sxs-lookup"><span data-stu-id="d97d6-129">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="d97d6-130">No EAC, navegue até **Permissões** \> **Funções de Administração**, clique no grupo de funções do qual você deseja remover o usuário ou usuários e clique em **Editar**![Ícone de edição](../media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="d97d6-130">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit**![Edit icon](../media/ITPro-EAC-EditIcon.png).</span></span>
    
2. <span data-ttu-id="d97d6-131">Em Membros, selecione o usuário ou usuários que você deseja remover e clique em **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.png).</span><span class="sxs-lookup"><span data-stu-id="d97d6-131">Under Members, select the user or users that you want to remove and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.png).</span></span>
    
3. <span data-ttu-id="d97d6-p109">Clique em **Salvar** para salvar a alteração no grupo e retornar à página **Funções de Administração**. Para verificar se você removeu o usuário do grupo de funções de administrador, verifique se o membro não está mais sendo exibido em Membros no painel de detalhes do grupo de funções selecionado.</span><span class="sxs-lookup"><span data-stu-id="d97d6-p109">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="d97d6-134">Os usuários precisam sair e entrar novamente para ver a alteração em seus diretos administrativos após a adição ou remoção de membros do grupo de funções.</span><span class="sxs-lookup"><span data-stu-id="d97d6-134">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="d97d6-135">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="d97d6-135">For more information</span></span>

[<span data-ttu-id="d97d6-136">Permissões de recurso no EOP</span><span class="sxs-lookup"><span data-stu-id="d97d6-136">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
  

