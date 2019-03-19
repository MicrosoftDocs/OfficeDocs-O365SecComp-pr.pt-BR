---
title: Gerenciar usuários de email no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: A definição de usuários de email é uma parte importante do gerenciamento do serviço Exchange Online Protection (EOP).
ms.openlocfilehash: 9ab4420dd9fcf6c056bc661b5f3646672a89a683
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670636"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="05b51-103">Gerenciar usuários de email no EOP</span><span class="sxs-lookup"><span data-stu-id="05b51-103">Manage mail users in EOP</span></span>

<span data-ttu-id="05b51-p101">A definição de usuários de email é uma parte importante do gerenciamento do serviço Exchange Online Protection (EOP). Existem várias maneiras possíveis de gerenciar usuários no EOP:</span><span class="sxs-lookup"><span data-stu-id="05b51-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="05b51-106">Utilizar a sincronização de diretórios para gerenciar usuários de email: se sua empresa possui contas de usuário existentes em um ambiente do Active Directory local, é possível sincronizar essas contas com o Azure Active Directory (AD), onde uma cópia dessas contas fica armazenada na nuvem.</span><span class="sxs-lookup"><span data-stu-id="05b51-106">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud.</span></span> <span data-ttu-id="05b51-107">Ao sincronizar suas contas de usuário existentes com o Azure Active Directory, será possível exibir esses usuários no painel **Destinatários** do Centro de administração do Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="05b51-107">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC).</span></span> <span data-ttu-id="05b51-108">Recomendamos usar a sincronização de diretório.</span><span class="sxs-lookup"><span data-stu-id="05b51-108">Using directory synchronization is recommended.</span></span> 
    
- <span data-ttu-id="05b51-109">Usar o EAC para gerenciar usuários de email: adicione e gerencie usuários de email diretamente no EAC.</span><span class="sxs-lookup"><span data-stu-id="05b51-109">Use the EAC to manage mail users: Add and manage mail users directly in the EAC.</span></span> <span data-ttu-id="05b51-110">Esse é o modo mais fácil de adicionar usuários de email e é útil para adicionar um usuário por vez.</span><span class="sxs-lookup"><span data-stu-id="05b51-110">This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>
    
- <span data-ttu-id="05b51-111">Usar o Windows PowerShell remoto para gerenciar usuários de email: adicione e gerencie usuários de email executando o Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="05b51-111">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell.</span></span> <span data-ttu-id="05b51-112">Este método é útil para adicionar vários registros e criar scripts.</span><span class="sxs-lookup"><span data-stu-id="05b51-112">This method is useful for adding multiple records and creating scripts.</span></span>
    
> [!NOTE]
> <span data-ttu-id="05b51-113">Você pode adicionar usuários no centro de administração do Microsoft 365, no entanto, esses usuários não podem ser usados como destinatários de email.</span><span class="sxs-lookup"><span data-stu-id="05b51-113">You can add users in the Microsoft 365 admin center, however these users can't be used as mail recipients.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="05b51-114">Antes de você começar</span><span class="sxs-lookup"><span data-stu-id="05b51-114">Before you begin</span></span>

- <span data-ttu-id="05b51-p105">Os procedimentos neste tópico exigem permissões específicas. Consulte cada procedimento para ver informações sobre permissões.</span><span class="sxs-lookup"><span data-stu-id="05b51-p105">Procedures in this topic require specific permissions. See each procedure for its permissions information.</span></span>
    
- <span data-ttu-id="05b51-117">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="05b51-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="05b51-p106">Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="05b51-p106">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="05b51-121">Utilizar a sincronização de diretórios para gerenciar usuários de email</span><span class="sxs-lookup"><span data-stu-id="05b51-121">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="05b51-122">Esta seção oferece informações sobre o gerenciamento de usuários de email usando a sincronização de diretório.</span><span class="sxs-lookup"><span data-stu-id="05b51-122">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="05b51-123">Se você usar a sincronização de diretório para gerenciar seus destinatários, ainda poderá adicionar e gerenciar usuários no centro de administração do Microsoft 365, mas eles não serão sincronizados com o Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="05b51-123">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="05b51-124">Isso porque a sincronização de diretórios sincroniza apenas destinatários de seu Active Directory local com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="05b51-124">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="05b51-125">A sincronização de diretório é recomendada para uso com os seguintes recursos: > **Listas de remetentes confiáveis e bloqueados do Outlook**: quando sincronizadas com o serviço, essas listas terão precedência sobre a filtragem de spam.</span><span class="sxs-lookup"><span data-stu-id="05b51-125">Using directory synchronization is recommended for use with the following features: > **Outlook safe sender and blocked sender lists** - When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="05b51-126">Isso permite que os usuários gerenciem suas próprias listas de remetentes confiáveis e bloqueados por usuário ou por domínio.</span><span class="sxs-lookup"><span data-stu-id="05b51-126">This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis.</span></span><span data-ttu-id="05b51-127"> > *\*Bloqueio de Borda Baseado em Diretório (DBEB)*\*: para obter mais informações sobre DBEB, consulte [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="05b51-127"> > *\*Directory Based Edge Blocking (DBEB)** - For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span><span data-ttu-id="05b51-128"> > *\*Quarentena de spam de usuário final*\*: para acessar a quarentena de spam de usuário final, os usuários finais devem ter uma ID de usuário e senha válidas no Office 365.</span><span class="sxs-lookup"><span data-stu-id="05b51-128"> > *\*End user spam quarantine** - In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="05b51-129">Os clientes do EOP que estão protegendo caixas de correio locais devem ser usuários de email válidos.</span><span class="sxs-lookup"><span data-stu-id="05b51-129">EOP customers protecting on-premises mailboxes must be valid email users.</span></span><span data-ttu-id="05b51-130"> > *\*Regras de fluxo** de emails-quando você usa a sincronização de diretório, os usuários e grupos existentes do Active Directory são carregados automaticamente para a nuvem e você pode criar regras de fluxo de emails (também conhecidas como regras de transporte) que direcionam usuários específicos e/ou grupos sem precisar adicioná-los manualmente por meio do PowerShell de proteção do Exchange Online ou do Eat.</span><span class="sxs-lookup"><span data-stu-id="05b51-130"> > *\*Mail flow rules** - When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="05b51-131">Observe que os [grupos dinâmicos de distribuição](https://go.microsoft.com/fwlink/?LinkId=507569) não podem ser sincronizados através da sincronização de diretório.</span><span class="sxs-lookup"><span data-stu-id="05b51-131">Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span> 
  
 <span data-ttu-id="05b51-132">**Antes de você começar**</span><span class="sxs-lookup"><span data-stu-id="05b51-132">**Before you begin**</span></span>
  
<span data-ttu-id="05b51-133">Obtenha as permissões necessárias e prepare-se para a sincronização de diretórios, como descrito em [Preparar a sincronização de diretórios](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span><span class="sxs-lookup"><span data-stu-id="05b51-133">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories"></a><span data-ttu-id="05b51-134">Sincronizar diretórios de usuário</span><span class="sxs-lookup"><span data-stu-id="05b51-134">To synchronize user directories</span></span>

1. <span data-ttu-id="05b51-135">Ative a sincronização de diretórios, como descrito em [Ativar a sincronização de diretórios](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span><span class="sxs-lookup"><span data-stu-id="05b51-135">Activate directory synchronization, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>
    
2. <span data-ttu-id="05b51-136">Configure seu computador de sincronização de diretórios, como descrito em [Configurar o computador de sincronização de diretórios](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span><span class="sxs-lookup"><span data-stu-id="05b51-136">Set up your directory synchronization computer, as described in [Set up your directory sync computer](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span></span>
    
3. <span data-ttu-id="05b51-137">Sincronize seus diretórios como descrito em [Usar o Assistente de Configuração para sincronizar diretórios](http://go.microsoft.com/fwlink/?LinkId=308912).</span><span class="sxs-lookup"><span data-stu-id="05b51-137">Synchronize your directories, as described in [Use the Configuration Wizard to sync your directories](http://go.microsoft.com/fwlink/?LinkId=308912).</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="05b51-p109">Após a conclusão do Assistente de Configuração da Ferramenta de Sincronização do Microsoft Azure Active Directory, a conta **MSOL_AD_SYNC** será criada em sua floresta do Active Directory. Esta conta é usada para ler e sincronizar suas informações do Active Directory local. Para que a sincronização de diretórios funcione corretamente, verifique se a porta TCP 443 em seu servidor de sincronização de diretórios local está aberta.</span><span class="sxs-lookup"><span data-stu-id="05b51-p109">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span> 
  
4. <span data-ttu-id="05b51-141">Ative usuários sincronizados, como descrito em [Ative os usuários sincronizados](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span><span class="sxs-lookup"><span data-stu-id="05b51-141">Activate synced users, as described in [Activate synced users](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span></span>
    
5. <span data-ttu-id="05b51-142">Gerencie a sincronização de diretórios, como descrito em [Gerenciar a sincronização de diretórios](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span><span class="sxs-lookup"><span data-stu-id="05b51-142">Manage directory synchronization, as described in [Manage directory synchronization](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span></span>
    
6. <span data-ttu-id="05b51-p110">Verifique se o EOP está sincronizando corretamente. No EAC, vá para **Destinatários** \> **Contatos** e veja se a lista de usuários foi corretamente sincronizada com seu ambiente local.</span><span class="sxs-lookup"><span data-stu-id="05b51-p110">Verify that EOP is synchronizing correctly. In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span> 
    
## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="05b51-145">Usar o EAC para gerenciar usuários de email</span><span class="sxs-lookup"><span data-stu-id="05b51-145">Use the EAC to manage mail users</span></span>

<span data-ttu-id="05b51-146">Esta seção oferece informações sobre a adição e o gerenciamento de usuários de email diretamente no EAC.</span><span class="sxs-lookup"><span data-stu-id="05b51-146">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
 <span data-ttu-id="05b51-147">**Antes de iniciar**</span><span class="sxs-lookup"><span data-stu-id="05b51-147">**Before you begin**</span></span>
  
<span data-ttu-id="05b51-p111">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e grupos de funções" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="05b51-p111">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
  
### <a name="to-add-a-mail-user-in-the-eac"></a><span data-ttu-id="05b51-150">Adicionar um usuário de email ao EAC</span><span class="sxs-lookup"><span data-stu-id="05b51-150">To add a mail user in the EAC</span></span>

1. <span data-ttu-id="05b51-151">Crie um usuário de email em **Destinatários** \> **Contatos** no EAC e clique em **Novo +**.</span><span class="sxs-lookup"><span data-stu-id="05b51-151">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>
    
2. <span data-ttu-id="05b51-152">Na página **Novo usuário de email**, insira as informações do usuário, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05b51-152">On the **New mail user** page, enter the user's information, including the following:</span></span> 
    
   ****

|<span data-ttu-id="05b51-153">**Propriedade do usuário de email**</span><span class="sxs-lookup"><span data-stu-id="05b51-153">**Mail user property**</span></span>|<span data-ttu-id="05b51-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05b51-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05b51-155">**Nome**, **Iniciais** e **Sobrenome**</span><span class="sxs-lookup"><span data-stu-id="05b51-155">**First name**, **Initials**, and **Last name**</span></span> <br/> |<span data-ttu-id="05b51-156">Digite o nome completo do usuário nas caixas apropriadas.</span><span class="sxs-lookup"><span data-stu-id="05b51-156">Type the user's full name in the appropriate boxes.</span></span>  <br/> |
|<span data-ttu-id="05b51-157">**Nome para exibição**</span><span class="sxs-lookup"><span data-stu-id="05b51-157">**Display name**</span></span> <br/> |<span data-ttu-id="05b51-p112">Digite um nome, usando até 64 caracteres. Por padrão, essa caixa mostra os nomes nas caixas **Nome**, **Iniciais** e **Sobrenome**, se houver. É necessário fornecer o nome para exibição.  </span><span class="sxs-lookup"><span data-stu-id="05b51-p112">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.  </span></span><br/> |
|<span data-ttu-id="05b51-161">**Alias**</span><span class="sxs-lookup"><span data-stu-id="05b51-161">**Alias**</span></span> <br/> |<span data-ttu-id="05b51-p113">Digite um alias exclusivo, usando até 64 caracteres para o usuário. O alias é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="05b51-p113">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>  <br/> |
|<span data-ttu-id="05b51-164">**Endereço de email externo**</span><span class="sxs-lookup"><span data-stu-id="05b51-164">**External email address**</span></span> <br/> |<span data-ttu-id="05b51-165">Digite o endereço de email externo do usuário.</span><span class="sxs-lookup"><span data-stu-id="05b51-165">Type the external email address of the user.</span></span>  <br/> |
|<span data-ttu-id="05b51-166">**ID de usuário**</span><span class="sxs-lookup"><span data-stu-id="05b51-166">**User id**</span></span> <br/> |<span data-ttu-id="05b51-p114">Digite o nome que o usuário de email usará para entrar no serviço. O nome de entrada do usuário consiste em um nome de usuário à esquerda do símbolo (@) e um sufixo à direita. Geralmente, o sufixo é o nome de domínio no qual a conta de usuário reside.</span><span class="sxs-lookup"><span data-stu-id="05b51-p114">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>  <br/> |
|<span data-ttu-id="05b51-170">**Nova senha**</span><span class="sxs-lookup"><span data-stu-id="05b51-170">**New password**</span></span> <br/> |<span data-ttu-id="05b51-p115">Digite a senha que o usuário de email usará para entrar no serviço. Verifique se a senha fornecida é compatível com os requisitos de comprimento, complexidade e histórico do domínio no qual você está criando a conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="05b51-p115">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>  <br/> |
|<span data-ttu-id="05b51-173">**Confirmação da senha**</span><span class="sxs-lookup"><span data-stu-id="05b51-173">**Confirm password**</span></span> <br/> |<span data-ttu-id="05b51-174">Digite novamente a senha para confirmá-la.</span><span class="sxs-lookup"><span data-stu-id="05b51-174">Retype the password to confirm it.</span></span>  <br/> |
   
3. <span data-ttu-id="05b51-p116">Clique em **Salvar** para criar o novo usuário de email. O novo usuário deve aparecer na lista de usuários.</span><span class="sxs-lookup"><span data-stu-id="05b51-p116">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span> 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a><span data-ttu-id="05b51-177">Adicionar ou remover um usuário de email no EAC</span><span class="sxs-lookup"><span data-stu-id="05b51-177">To edit or remove a mail user in the EAC</span></span>

- <span data-ttu-id="05b51-178">No EAC, acesse **Destinatários** \> **Contatos**.</span><span class="sxs-lookup"><span data-stu-id="05b51-178">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="05b51-179">Na lista de usuários, clique no usuário que você deseja exibir ou alterar e selecione **Editar** ![ícone](../media/ITPro-EAC-EditIcon.gif) de edição para atualizar as configurações do usuário, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="05b51-179">In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed.</span></span> <span data-ttu-id="05b51-180">Você pode alterar o nome, o alias ou as informações de contato do usuário, e pode registrar informações detalhadas sobre a função do usuário na organização.</span><span class="sxs-lookup"><span data-stu-id="05b51-180">You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization.</span></span> <span data-ttu-id="05b51-181">Você também pode selecionar um usuário e escolher **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.gif) para excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="05b51-181">You can also select a user and then choose **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a><span data-ttu-id="05b51-182">Usar o Windows PowerShell remoto para gerenciar usuários de email</span><span class="sxs-lookup"><span data-stu-id="05b51-182">Use remote Windows PowerShell to manage mail users</span></span>

<span data-ttu-id="05b51-183">Esta seção fornece informações sobre como adicionar e gerenciar usuários de email usando o Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="05b51-183">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
 <span data-ttu-id="05b51-184">**Antes de iniciar**</span><span class="sxs-lookup"><span data-stu-id="05b51-184">**Before you begin**</span></span>
  
- <span data-ttu-id="05b51-p118">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e grupos de funções" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="05b51-p118">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
    
- <span data-ttu-id="05b51-187">Lembre-se de que quando estiver criando usuários de email usando cmdlets do PowerShell remoto, você pode encontrar limitações.</span><span class="sxs-lookup"><span data-stu-id="05b51-187">Be aware that when creating mail users by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="05b51-188">Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis.</span><span class="sxs-lookup"><span data-stu-id="05b51-188">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="05b51-189">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Conectar-se ao Exchange Online Protection usando o PowerShell Remoto](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="05b51-189">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
 <span data-ttu-id="05b51-190">**Para adicionar um usuário de email usando o PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="05b51-190">**To add a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="05b51-191">O exemplo usa o cmdlet [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) para criar uma conta de usuário habilitado para email em nome de Diogo Martins com os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="05b51-191">This example uses the [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span> 
  
- <span data-ttu-id="05b51-192">O primeiro nome é Diogo e o sobrenome é Martins.</span><span class="sxs-lookup"><span data-stu-id="05b51-192">The first name is Jeffrey and the last name is Zeng.</span></span>
    
- <span data-ttu-id="05b51-193">O nome é Diogo e o nome de exibição é Diogo Martins.</span><span class="sxs-lookup"><span data-stu-id="05b51-193">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>
    
- <span data-ttu-id="05b51-194">O alias é diogom.</span><span class="sxs-lookup"><span data-stu-id="05b51-194">The alias is jeffreyz.</span></span>
    
- <span data-ttu-id="05b51-195">O endereço de email externo é diogom@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="05b51-195">The external email address is jzeng@tailspintoys.com.</span></span>
    
- <span data-ttu-id="05b51-196">O nome de usuário do Office 365 é diogom@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="05b51-196">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>
    
- <span data-ttu-id="05b51-197">A senha é Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="05b51-197">The password is Pa$$word1.</span></span>
    
```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 <span data-ttu-id="05b51-198">**Para verificar se funcionou**</span><span class="sxs-lookup"><span data-stu-id="05b51-198">**To verify that this worked**</span></span>
  
<span data-ttu-id="05b51-199">Execute o cmdlet [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) conforme as etapas a seguir para mostrar as informações sobre o novo usuário de email Diogo Martins:</span><span class="sxs-lookup"><span data-stu-id="05b51-199">Run the [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet as follows to display information about new mail user Jeffrey Zeng:</span></span> 
  
```Powershell
Get-User "Jeffrey Zeng"

```

 <span data-ttu-id="05b51-200">**Para editar as propriedades de um usuário de email usando o PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="05b51-200">**To edit the properties of a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="05b51-201">Use os cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) e [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) para visualizar ou alterar propriedades para usuários de email.</span><span class="sxs-lookup"><span data-stu-id="05b51-201">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlets to view or change properties for mail users.</span></span> 
  
<span data-ttu-id="05b51-202">Este exemplo define o endereço de email externo de Brenda Fernandes.</span><span class="sxs-lookup"><span data-stu-id="05b51-202">This example sets the external email address for Pilar Pinilla.</span></span>
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="05b51-203">Este exemplo define a propriedade Company de todos os usuários de email como Contoso.</span><span class="sxs-lookup"><span data-stu-id="05b51-203">This example sets the Company property for all mail users to Contoso.</span></span>
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 <span data-ttu-id="05b51-204">**Para verificar se funcionou**</span><span class="sxs-lookup"><span data-stu-id="05b51-204">**To verify that this worked**</span></span>
  
<span data-ttu-id="05b51-p119">No exemplo anterior, alteramos as propriedades do usuário de email Brenda Fernandes, use o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) para verificar as alterações. (Observe que você pode visualizar várias propriedades para vários contatos de email.)</span><span class="sxs-lookup"><span data-stu-id="05b51-p119">In the previous example where we changed the properties for mail user Pilar Pinella, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. (Note that you can view multiple properties for multiple mail contacts.)</span></span> 
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

<span data-ttu-id="05b51-207">No exemplo anterior em que a propriedade Company foi definida como Contoso para todos os usuários de email, execute o comando a seguir para verificar as alterações:</span><span class="sxs-lookup"><span data-stu-id="05b51-207">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="05b51-208">Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis.</span><span class="sxs-lookup"><span data-stu-id="05b51-208">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span> 
  
 <span data-ttu-id="05b51-209">**Para remover um usuário de email usando o PowerShell remoto**</span><span class="sxs-lookup"><span data-stu-id="05b51-209">**To remove a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="05b51-210">Este exemplo usa o cmdlet [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) para excluir o usuário Diogo Martins:</span><span class="sxs-lookup"><span data-stu-id="05b51-210">This example uses the [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet to delete user Jeffrey Zeng:</span></span> 
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="05b51-211">**Para verificar se funcionou**</span><span class="sxs-lookup"><span data-stu-id="05b51-211">**To verify that this worked**</span></span>
  
<span data-ttu-id="05b51-p120">Execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira. Uma mensagem de erro deve ser exibida já que o usuário não existe mais.</span><span class="sxs-lookup"><span data-stu-id="05b51-p120">Run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows. You should get an error message since the user no longer exists.</span></span> 
  
```Powershell
Get-Recipient Jeffrey | fl
```


