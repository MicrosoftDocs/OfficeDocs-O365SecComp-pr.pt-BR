---
title: Fornecer acesso aos usuários para a segurança do Office 365 &amp; Centro de conformidade
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Os usuários precisam ter permissões de segurança do Office 365 &amp; Centro de conformidade antes que eles possam gerenciar qualquer um dos seus recursos de segurança ou conformidade.
ms.openlocfilehash: c612c99f7d72b19d072d728eb4851532d4012414
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013795"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="042ca-103">Fornecer acesso aos usuários para a segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="042ca-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="042ca-p101">Os usuários precisam ter permissões de segurança do Office 365 &amp; Centro de conformidade antes que eles possam gerenciar qualquer um dos seus recursos de segurança ou conformidade. Como um administrador global do Office 365 ou um membro do grupo de função OrganizationManagement na segurança &amp; Centro de conformidade, você pode conceder essas permissões aos usuários. Os usuários somente poderão gerenciar os recursos de segurança ou conformidade que você conceda acesso a.</span><span class="sxs-lookup"><span data-stu-id="042ca-p101">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features. As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users. Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="042ca-107">Para obter mais informações sobre as permissões diferentes, você pode conceder aos usuários na segurança &amp; Centro de conformidade, check-out [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="042ca-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="042ca-108">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="042ca-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="042ca-109">Você precisa ser um administrador global do Office 365 ou um membro do grupo de funções OrganizationManagement na segurança &amp; Centro de conformidade, conclua as etapas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="042ca-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="042ca-110">Grupos de função para a segurança &amp; Centro de conformidade podem ter nomes semelhantes aos grupos de função no Exchange Online, mas eles não são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="042ca-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="042ca-111">Associações de grupo de função não são compartilhadas entre o Exchange Online e a segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="042ca-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="042ca-112">Use o Centro de administração do Office 365 para fornecer outro acesso de usuário de segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="042ca-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="042ca-113">[Entrar no Office 365 e vá para o Centro de administração](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="042ca-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
<span data-ttu-id="042ca-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="042ca-114"><<<<<<< HEAD</span></span>
2. <span data-ttu-id="042ca-115">No Centro de administração do Office 365, abra a **centrais de administração** e clique **segurança &amp; conformidade**.</span><span class="sxs-lookup"><span data-stu-id="042ca-115">In the Office 365 Admin Center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
=======
2. <span data-ttu-id="042ca-116">No Centro de administração do Office 365, abra a **centrais de administração** e clique **segurança &amp; conformidade**.</span><span class="sxs-lookup"><span data-stu-id="042ca-116">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
>>>>>>> <span data-ttu-id="042ca-117">mestre</span><span class="sxs-lookup"><span data-stu-id="042ca-117">master</span></span>
    
3. <span data-ttu-id="042ca-118">Na segurança &amp; Centro de conformidade, vá para **permissões**.</span><span class="sxs-lookup"><span data-stu-id="042ca-118">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="042ca-119">Na lista, escolha o grupo de função que você deseja adicionar o usuário e clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="042ca-119">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="042ca-120">Na página de propriedades do grupo de funções em **membros**, clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione o nome do usuário (ou usuários) para o qual você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="042ca-120">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="042ca-121">Quando você tiver selecionado todos os usuários que você deseja adicionar ao grupo de funções, clique em **Adicionar-\> ** e **Okey**.</span><span class="sxs-lookup"><span data-stu-id="042ca-121">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="042ca-122">Clique em **Salvar** para salvar as alterações feitas no grupo de funções.</span><span class="sxs-lookup"><span data-stu-id="042ca-122">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="042ca-123">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="042ca-123">How do you know this worked?</span></span>

1. <span data-ttu-id="042ca-124">Na segurança &amp; Centro de conformidade, vá para **permissões**.</span><span class="sxs-lookup"><span data-stu-id="042ca-124">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="042ca-125">Na lista, selecione o grupo de funções para exibir os membros.</span><span class="sxs-lookup"><span data-stu-id="042ca-125">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="042ca-126">À direita, nos detalhes do grupo de função, você pode exibir os membros do grupo de função.</span><span class="sxs-lookup"><span data-stu-id="042ca-126">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="042ca-127">Use o PowerShell para fornecer outro acesso de usuário de segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="042ca-127">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="042ca-128">[Conectar para a segurança do Office 365 &amp; usando o PowerShell remoto do Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="042ca-128">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
    
2. <span data-ttu-id="042ca-129">Use o comando **Add-RoleGroupMember** para adicionar um usuário à função de Gerenciamento de Organização, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="042ca-129">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="042ca-130">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="042ca-130">**Parameters**</span></span>
  
-  <span data-ttu-id="042ca-131">_-Identity_ é o grupo de funções ao qual adicionar um membro.</span><span class="sxs-lookup"><span data-stu-id="042ca-131">_-Identity_ is the role group to add a member to.</span></span> 
    
- - <span data-ttu-id="042ca-p102">_Membro_ é a caixa de correio, o grupo de segurança universal (USG) ou computador para adicionar ao grupo de funções. Você pode especificar somente um membro ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="042ca-p102">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group. You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="042ca-134">Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="042ca-134">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="042ca-135">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="042ca-135">How do you know this worked?</span></span>

<span data-ttu-id="042ca-136">Para verificar que você tiver concedido aos usuários acesso à segurança &amp; Centro de conformidade, use o cmdlet **Get-RoleGroupMember** para exibir os membros no grupo de função de gerenciamento da organização, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="042ca-136">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="042ca-137">Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="042ca-137">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  

