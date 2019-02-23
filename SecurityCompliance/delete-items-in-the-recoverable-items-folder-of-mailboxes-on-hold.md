---
title: Excluir itens da pasta itens recuperáveis das caixas de correio baseadas em nuvem em manter ajuda do administrador
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Para administradores: excluir itens na pasta itens recuperáveis de um usuário para uma caixa de correio do Exchange Online, mesmo se essa caixa de correio for colocada em retenção legal. Essa é uma maneira eficaz de excluir dados que foram desfeitos acidentalmente no Office 365.'
ms.openlocfilehash: f3518dc1009b4e95472473f76e6cd41011bc6b3e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216951"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="64fc1-104">Excluir itens da pasta itens recuperáveis das caixas de correio baseadas em nuvem em manter ajuda do administrador</span><span class="sxs-lookup"><span data-stu-id="64fc1-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="64fc1-p102">A pasta itens recuperáveis para uma caixa de correio do Exchange Online existe para proteger contra exclusões acidentais ou mal-intencionadas. Também é usado para armazenar itens que são mantidos e acessados pelos recursos de conformidade do Office 365, como bloqueios e pesquisas de descoberta eletrônica. No enTanto, em algumas situações, as organizações podem ter dados que são retidos acidentalmente na pasta itens recuperáveis que devem ser excluídos. Por exemplo, um usuário pode enviar ou encaminhar uma mensagem de email que contenha informações confidenciais ou informações que possam ter sérias conseqüências de negócios. Mesmo que a mensagem seja excluída permanentemente, ela pode ser retida indefinidamente porque uma retenção legal foi colocada na caixa de correio. Este cenário é conhecido como dados derramamento porque os dados foram desfeitos acidentalmente no Office 365. Nessas situações, você pode excluir itens na pasta itens recuperáveis de um usuário para uma caixa de correio do Exchange Online, mesmo que essa caixa de correio seja colocada em espera com um dos diferentes recursos de retenção no Office 365. Esses tipos de isenções incluem bloqueios de litígio, isenções in-loco, retenções de descoberta eletrônica e políticas de retenção do Office 365 criadas no centro &amp; de conformidade de segurança do Office 365.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="64fc1-p103">Este artigo explica como excluir itens da pasta itens recuperáveis para caixas de correio baseadas em nuvem que estão em espera. Este procedimento envolve desabilitar o acesso à caixa de correio e desabilitar a recuperação de item único, desabilitar o assistente de pasta gerenciada do processamento da caixa de correio, removendo temporariamente a retenção, excluindo itens da pasta itens recuperáveis e revertendo a caixa de correio para a configuração anterior. Este é o processo:</span><span class="sxs-lookup"><span data-stu-id="64fc1-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="64fc1-116">Etapa 1: coletar informações sobre a caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="64fc1-117">Etapa 2: preparar a caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="64fc1-118">Etapa 3: remover todas as isenções da caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="64fc1-119">Etapa 4: remover o atraso no bloqueio da caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="64fc1-120">Etapa 5: excluir itens na pasta itens recuperáveis</span><span class="sxs-lookup"><span data-stu-id="64fc1-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="64fc1-121">Etapa 6: reverter a caixa de correio para o estado anterior</span><span class="sxs-lookup"><span data-stu-id="64fc1-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="64fc1-p104">Os procedimentos descritos neste artigo resultarão na exclusão permanente de dados (removidos) de uma caixa de correio do Exchange Online. Isso significa que as mensagens excluídas da pasta itens recuperáveis não podem ser recuperadas e não estarão disponíveis para descoberta legal ou outros fins de conformidade. Se você deseja excluir mensagens de uma caixa de correio que é colocada em espera como parte de uma retenção de litígio, bloqueio in-loco, retenção de descoberta eletrônica ou política de retenção do Office 365 criada no &amp; centro de conformidade de segurança do Office 365, consulte seu gerenciamento de registros ou legal departamentos antes da remoção da isenção. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de derramamento de dados tem prioridade.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="64fc1-126">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="64fc1-126">Before you begin</span></span>

- <span data-ttu-id="64fc1-127">Você precisa ter as duas funções de gerenciamento a seguir no Exchange Online para pesquisar e excluir mensagens da pasta itens recuperáveis na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="64fc1-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="64fc1-p105">**Pesquisa de caixa de correio** -essa função permite pesquisar caixas de correio em sua organização. Os administradores do Exchange não são atribuídos a essa função por padrão. Para atribuir a si mesmo esta função, adicione a si mesmo como membro do grupo de função gerenciamento de descoberta no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="64fc1-p106">**Exportação de importação de caixa de correio** -essa função permite excluir mensagens da caixa de correio de um usuário. Por padrão, essa função não é atribuída a nenhum grupo de função. Para excluir mensagens de caixas de correio dos usuários, você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="64fc1-p107">O procedimento descrito neste artigo não tem suporte para caixas de correio inativas. Isso ocorre porque você não pode aplicar novamente uma retenção (ou a política de retenção do Office 365) a uma caixa de correio inativa após removê-la. Quando você remove uma retenção de uma caixa de correio inativa, ela é alterada para uma caixa de correio normal excluída por software e será excluída permanentemente da sua organização depois de ser processada pelo assistente de pasta gerenciada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="64fc1-p108">Você não pode executar esse procedimento para uma caixa de correio que tenha sido atribuída a uma política de retenção do Office 365 que tenha sido bloqueada com um bloqueio de preservação. Isso ocorre porque um bloqueio de preservação impede que você remova ou exclua a caixa de correio da política de retenção do Office 365 e desabilite o assistente de pasta gerenciada na caixa de correio. Para obter mais informações sobre as políticas de retenção de bloqueio, consulte [bloquear uma política de retenção](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="64fc1-p109">Se uma caixa de correio não for colocada em espera (ou não tiver a recuperação de item único habilitada), você poderá simplesmente excluir os itens da pasta itens recuperáveis. Para obter mais informações sobre como fazer isso, confira [Pesquisar e excluir mensagens ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="64fc1-142">Etapa 1: coletar informações sobre a caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="64fc1-p110">Essa primeira etapa é coletar as propriedades selecionadas da caixa de correio de destino que afetem esse procedimento. Certifique-se de anotar essas configurações ou salvá-las em um arquivo de texto porque você alterará algumas dessas propriedades e reverterá para os valores originais na etapa 6, após excluir itens da pasta itens recuperáveis. Veja a seguir uma lista das propriedades de caixa de correio que você precisa coletar.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="64fc1-146">*SingleItemRecoveryEnabled* e *RetainDeletedItemsFor* ; se necessário, você desabilitará a recuperação única e aumentará o período de retenção de itens excluídos na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="64fc1-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="64fc1-p111">*LitigationHoldEnabled* e *InPlaceHolds* ; Você precisa identificar todas as suspensões colocadas na caixa de correio para que possa removê-las temporariamente na etapa 3. Consulte a seção [mais informações](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) para obter dicas sobre como identificar a retenção de tipo que pode ser colocada em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="64fc1-p112">Além disso, é necessário obter as configurações de acesso do cliente da caixa de correio para que você possa desabilitá-las temporariamente para que o proprietário (ou outros usuários) não possa acessar a caixa de correio durante esse procedimento. Por fim, você pode obter o tamanho atual e o número de itens na pasta itens recuperáveis. Após excluir itens da pasta itens recuperáveis na etapa 5, você usará essas informações para verificar se os itens foram realmente removidos.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="64fc1-p113">[Conecte-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/?linkid=396554). Certifique-se de usar um nome de usuário e senha para uma conta de administrador que tenha sido atribuída às funções de gerenciamento apropriadas no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="64fc1-154">Execute o seguinte comando para obter informações sobre a recuperação de item único e o período de retenção de item excluído.</span><span class="sxs-lookup"><span data-stu-id="64fc1-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="64fc1-p114">Se a recuperação de item único estiver habilitada, você terá que desabilitá-lo na etapa 2. Se o período de retenção de itens excluídos não estiver definido por 30 dias (o valor máximo no Exchange Online), você poderá aumentá-lo na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="64fc1-157">Execute o seguinte comando para obter as configurações de acesso à caixa de correio para a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="64fc1-158">Você desabilitará todos esses métodos de acesso na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="64fc1-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="64fc1-159">Execute o seguinte comando para obter informações sobre as políticas de retenção de isenções e do Office 365 aplicadas à caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="64fc1-160">Se houver muitos valores na propriedade *InPlaceHolds* e nem todos eles forem exibidos, você poderá executar o `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada valor em uma linha separada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="64fc1-161">Execute o seguinte comando para obter informações sobre as políticas de retenção do Office 365 em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="64fc1-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="64fc1-162">Se sua organização tiver as políticas de retenção do Office 365 em toda a organização, você terá que excluir a caixa de correio dessas políticas na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="64fc1-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="64fc1-163">Se houver muitos valores na propriedade *InPlaceHolds* e nem todos eles forem exibidos, você poderá executar o `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada valor em uma linha separada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="64fc1-164">Execute o seguinte comando para obter o tamanho atual e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="64fc1-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="64fc1-165">Se a caixa de correio de arquivo morto do usuário estiver habilitada, execute o seguinte comando para obter o tamanho e o número total de itens em pastas e subpastas na pasta itens recuperáveis em suas caixas de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="64fc1-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="64fc1-p115">Ao excluir itens na etapa 5, você pode optar por excluir ou não excluir itens da pasta itens recuperáveis na caixa de correio de arquivo morto principal do usuário. Observe que se o arquivamento de expansão automática estiver habilitado para a caixa de correio, os itens em uma caixa de correio de arquivo morto auxiliar não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="64fc1-168">Etapa 2: preparar a caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="64fc1-169">Após coletar e salvar informações sobre a caixa de correio, a próxima etapa é preparar a caixa de correio executando as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="64fc1-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="64fc1-170">**Desabilitar o acesso do cliente à caixa de correio** para que o proprietário da caixa de correio não possa acessar a caixa de correio e fazer quaisquer alterações nos dados da caixa de correio durante esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="64fc1-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="64fc1-171">**Aumente o período de retenção de itens excluídos** para 30 dias (o valor máximo no Exchange Online) para que os itens não sejam removidos da pasta itens recuperáveis antes que você possa excluí-los na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="64fc1-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="64fc1-172">**Desabilitar a recuperação de item único** para que os itens não sejam retidos (pela duração do período de retenção do item excluído) depois de excluí-los da pasta itens recuperáveis na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="64fc1-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="64fc1-173">**Desative o assistente de pasta gerenciada** para que ele não processe a caixa de correio e mantenha os itens excluídos na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="64fc1-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="64fc1-174">Execute as etapas a seguir no PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="64fc1-p116">Execute o comando a seguir para desabilitar todo o acesso do cliente à caixa de correio. A sintaxe do comando pressupõe que todos os métodos de acesso para cliente foram habilitados na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="64fc1-p117">Pode levar até 60 minutos para desabilitar todos os métodos de acesso para cliente para a caixa de correio. Observe que desabilitar esses métodos de acesso não desconectará o proprietário da caixa de correio no qual está conectado no momento. Se o proprietário não estiver conectado, não será possível acessar a caixa de correio após a desabilitação dos métodos de acesso.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="64fc1-p118">Execute o seguinte comando para aumentar o período de retenção de item excluído no máximo 30 dias. Isso pressupõe que a configuração atual é inferior a 30 dias.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="64fc1-182">Execute o comando a seguir para desabilitar a recuperação de item único.</span><span class="sxs-lookup"><span data-stu-id="64fc1-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="64fc1-p119">Pode levar até 60 minutos para desabilitar a recuperação de item único. Não exclua itens na pasta itens recuperáveis até que esse período tenha decorrido.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="64fc1-p120">Execute o comando a seguir para impedir que o assistente de pasta gerenciada processe a caixa de correio. Conforme explicado anteriormente, você pode desabilitar o assistente de pasta gerenciada somente se uma política de retenção do Office 365 com um bloqueio de preservação não for aplicada à caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="64fc1-187">Etapa 3: remover todas as isenções da caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="64fc1-p121">A última etapa para que você possa excluir itens da pasta itens recuperáveis é remover todas as isenções (que você identificou na etapa 1) colocadas na caixa de correio. Todas as isenções devem ser removidas para que os itens não sejam retidos após serem excluídos da pasta itens recuperáveis. As seções a seguir contêm informações sobre como remover diferentes tipos de bloqueios em uma caixa de correio. Consulte a seção [mais informações](#more-information) para obter dicas sobre como identificar a retenção de tipo que pode ser colocada em uma caixa de correio. Para obter informações adicionais, consulte [como identificar o tipo de retenção colocado em uma caixa de correio do Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="64fc1-193">Conforme mencionado anteriormente, confira o gerenciamento de registros ou os departamentos legais antes de remover uma retenção de uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="64fc1-194">Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="64fc1-194">Litigation Hold</span></span>
  
<span data-ttu-id="64fc1-195">Execute o seguinte comando no PowerShell do Exchange Online para remover uma retenção de litígio da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="64fc1-p122">Semelhante à desabilitação dos métodos de acesso para cliente e recuperação de item único, pode levar até 60 minutos para remover a retenção de litígio. Não exclua itens da pasta itens recuperáveis até que esse período tenha decorrido.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="64fc1-198">Bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="64fc1-198">In-Place Hold</span></span>
  
<span data-ttu-id="64fc1-p123">Execute o seguinte comando no PowerShell do Exchange Online para identificar o bloqueio in-loco colocado na caixa de correio. Use o GUID do bloqueio in-loco identificado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="64fc1-p124">Após identificar o bloqueio in-loco, você pode usar o centro de administração do Exchange (Eat) ou o PowerShell do Exchange Online para remover a caixa de correio da isenção. Para obter mais informações, consulte [criar ou remover um bloqueio in-loco](https://go.microsoft.com/fwlink/?linkid=852668).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="64fc1-203">Políticas de retenção do Office 365 aplicadas a caixas de correio específicas</span><span class="sxs-lookup"><span data-stu-id="64fc1-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="64fc1-p125">Execute o seguinte comando no [PowerShell do centro &amp; de conformidade de segurança do Office 365](https://go.microsoft.com/fwlink/?linkid=627084) para identificar a política de retenção do Office 365 que é aplicada à caixa de correio. Use o GUID (não incluindo o `mbx` prefixo `skp` ou) para a política de retenção que você identificou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="64fc1-206">Após identificar a política de retenção, vá para a página **retenção** de **governança** \> de data no &amp; centro de conformidade de segurança, edite a política de retenção que você identificou na etapa anterior e remova a caixa de correio da lista de destinatários incluídos na política de retenção.</span><span class="sxs-lookup"><span data-stu-id="64fc1-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="64fc1-207">Políticas de retenção do Office 365 em toda a organização</span><span class="sxs-lookup"><span data-stu-id="64fc1-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="64fc1-p126">As políticas de retenção de toda a organização e do Exchange 365 são aplicadas a todas as caixas de correio na organização. Eles são aplicados no nível da organização (não no nível da caixa de correio) e são retornados quando você executa o cmdlet **Get-OrganizationConfig** na etapa 1. Execute o seguinte comando no [PowerShell &amp; do centro de conformidade de segurança](https://go.microsoft.com/fwlink/?linkid=627084) para identificar as políticas de retenção do Office 365 em toda a organização. Use o GUID (não incluindo o `mbx` prefixo) para as políticas de retenção em toda a organização que você identificou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="64fc1-p127">após identificar as políticas de retenção do Office 365 em toda a organização, vá para a página \> **retenção** de governança de &amp; **data** no centro de conformidade de segurança, edite cada política de retenção em toda a organização que você identificou na etapa anterior e adicione a caixa de correio à lista de destinatários excluídos. Isso removerá a caixa de correio do usuário da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="64fc1-214">Rótulos de retenção do Office 365</span><span class="sxs-lookup"><span data-stu-id="64fc1-214">Office 365 retention labels</span></span>

<span data-ttu-id="64fc1-p128">Sempre que um usuário aplica um rótulo que é configurado para reter conteúdo ou reter e, em seguida, excluir conteúdo para qualquer pasta ou item em suas caixas de correio, a propriedade de caixa de correio *ComplianceTagHoldApplied* é definida como **true**. Quando isso acontece, a caixa de correio é considerada em espera, assim como se foi feita em retenção de litígio ou atribuída a uma política de retenção do Office 365.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="64fc1-217">Para exibir o valor da propriedade *ComplianceTagHoldApplied* , execute o seguinte comando no PowerShell do Exchange Online:</span><span class="sxs-lookup"><span data-stu-id="64fc1-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="64fc1-p129">Depois de identificar que uma caixa de correio está em espera porque um rótulo de retenção é aplicado a uma pasta ou item, você pode usar a ferramenta de pesquisa de conteúdo no centro de conformidade do & de segurança para pesquisar itens rotulados usando a condição de pesquisa ComplianceTag. Para obter mais informações, consulte a seção "condições de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="64fc1-220">Para obter mais informações sobre rótulos, consulte [Overview of Office 365 Labels](labels.md).</span><span class="sxs-lookup"><span data-stu-id="64fc1-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="64fc1-221">retenção de ocorrência de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="64fc1-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="64fc1-p130">Execute os seguintes comandos no [PowerShell &amp; do centro de conformidade de segurança](https://go.microsoft.com/fwlink/?linkid=627084) para identificar o bloqueio associado a uma ocorrência de descoberta eletrônica aplicada à caixa de correio. Use o GUID (não incluindo o `UniH` prefixo) para o bloqueio de descoberta eletrônica que você identificou na etapa 1. Observe que o segundo comando exibe o nome da ocorrência de descoberta eletrônica à qual a retenção está associada; o terceiro comando exibe o nome da retenção.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="64fc1-p131">Depois de identificar o nome do caso de descoberta eletrônica e a retenção, vá para a página de **descoberta eletrônica** de investigação \> de &amp; \*\*pesquisa &amp; \*\* no centro de conformidade de segurança, abra o caso e remova a caixa de correio da isenção. Para obter mais informações, consulte [gerenciar casos de descoberta eletrônica no centro &amp; de conformidade de segurança do Office 365](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="64fc1-227">Etapa 4: remover o atraso no bloqueio da caixa de correio</span><span class="sxs-lookup"><span data-stu-id="64fc1-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="64fc1-p132">Após qualquer tipo de retenção ser removido de uma caixa de correio, o valor da propriedade de caixa de correio *DelayHoldApplied* é definido como **true**. Isso ocorre na próxima vez que o assistente de pasta gerenciada processa a caixa de correio e detecta que uma retenção foi removida. Isso é chamado de *espera de atraso* e significa que a remoção real da retenção está atrasada por 30 dias para evitar que os dados sejam excluídos permanentemente da caixa de correio. (O objetivo de um atraso na espera é dar aos administradores uma oportunidade de Pesquisar ou recuperar itens de caixa de correio que serão removidos após a remoção de uma retenção.)  Quando um atraso de espera é colocado na caixa de correio, a caixa de correio ainda é considerada em espera por uma duração ilimitada, como se a caixa de correio estivesse em retenção de litígio. Após 30 dias, o atraso esperado expira e o Office 365 tentará automaticamente remover o atraso de espera (definindo a propriedade *DelayHoldApplied* como **false**) para que a retenção seja realmente removida.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed. This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="64fc1-p133">Antes de poder excluir itens na etapa 5, você deve remover o atraso de retenção da caixa de correio. Primeiro, determine se a espera de atraso é aplicada à caixa de correio executando o seguinte comando no PowerShell do Exchange Online:</span><span class="sxs-lookup"><span data-stu-id="64fc1-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="64fc1-p134">Se o valor da propriedade *DelayHoldApplied* for definido como **false**, uma espera de atraso não foi colocada na caixa de correio. Você pode ir para a etapa 5 e excluir itens na pasta itens recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p134">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox. You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="64fc1-237">Se o valor da propriedade *DelayHoldApplied* for definido como **true**, execute o seguinte comando para remover o atraso de retenção:</span><span class="sxs-lookup"><span data-stu-id="64fc1-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="64fc1-238">Observe que você deve receber a função de retenção legal no Exchange Online para usar o parâmetro *RemoveDelayHoldApplied* .</span><span class="sxs-lookup"><span data-stu-id="64fc1-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="64fc1-239">Etapa 5: excluir itens na pasta itens recuperáveis</span><span class="sxs-lookup"><span data-stu-id="64fc1-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="64fc1-p135">Agora, você está pronto para excluir itens na pasta itens recuperáveis usando o cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) no PowerShell do Exchange Online. Você tem três opções ao executar o cmdlet **Search-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="64fc1-p135">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="64fc1-242">Copiar itens para uma caixa de correio de destino antes de excluí-los, de forma que você possa revisar os itens, se necessário, antes de excluí-los.</span><span class="sxs-lookup"><span data-stu-id="64fc1-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="64fc1-243">Copiar itens para uma caixa de correio de destino e excluí-los no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="64fc1-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="64fc1-244">Excluir itens sem copiá-los para uma caixa de correio de destino.</span><span class="sxs-lookup"><span data-stu-id="64fc1-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="64fc1-p136">Observe que os itens na pasta itens recuperáveis na caixa de correio de arquivo morto principal do usuário também serão excluídos quando você executar o cmdlet **Search-Mailbox** . Para evitar isso, você pode incluir a opção *DoNotIncludeArchive* E conforme mencionado anteriormente, se o arquivamento de expansão automática estiver habilitado para a caixa de correio, o cmdlet \* \* Search-Mailbox \* \* não excluirá itens em uma caixa de correio de arquivo auxiliar. Para obter mais informações sobre o arquivamento de expansão automática, consulte [Overview of Unlimited Archiving in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p136">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the **Search-Mailbox** cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="64fc1-p137">Se você incluir uma consulta de pesquisa (usando o parâmetro *SearchQuery* ), o cmdlet **Search-Mailbox** retornará um máximo de 10.000 itens nos resultados da pesquisa. Portanto, se você incluir uma consulta de pesquisa, talvez seja necessário executar o comando **Search-Mailbox** várias vezes para excluir mais de 10.000 itens.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p137">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="64fc1-p138">Os exemplos a seguir mostram a sintaxe de comando de cada uma dessas opções. Estes exemplos usam o `-SearchQuery size>0` valor de parâmetro, que exclui todos os itens de todas as subpastas da pasta itens recuperáveis. Se você precisar excluir apenas os itens que correspondem a condições específicas, você também pode usar o parâmetro *SearchQuery* para especificar outras condições, como o assunto de uma mensagem ou um intervalo de datas. ConFira os [outros exemplos de como usar o parâmetro SearchQuery a](#other-examples-of-using-the-searchquery-parameter) seguir.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p138">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="64fc1-255">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64fc1-255">Example 1</span></span>

<span data-ttu-id="64fc1-p139">Este exemplo copia todos os itens da pasta itens recuperáveis do usuário para uma pasta na caixa de correio de pesquisa de descoberta da sua organização. Isso permite que você revise os itens antes de excluí-los permanentemente.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p139">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="64fc1-p140">No exemplo anterior, não é necessário copiar itens para a caixa de correio de pesquisa de descoberta. Você pode copiar mensagens para qualquer caixa de correio de destino. No enTanto, para impedir o acesso a dados potencialmente confidenciais de caixa de correio, é recomendável copiar mensagens para uma caixa de correio que tenha acesso restrito a pessoal autorizado. Por padrão, o acesso à caixa de correio de pesquisa de descoberta padrão é restrito aos membros do grupo de função gerenciamento de descoberta no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p140">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="64fc1-262">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="64fc1-262">Example 2</span></span>

<span data-ttu-id="64fc1-263">Este exemplo copia todos os itens da pasta itens recuperáveis do usuário para uma pasta na caixa de correio de pesquisa de descoberta da organização e, em seguida, exclui os itens da pasta itens recuperáveis do usuário.</span><span class="sxs-lookup"><span data-stu-id="64fc1-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="64fc1-264">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="64fc1-264">Example 3</span></span>

<span data-ttu-id="64fc1-265">Este exemplo exclui todos os itens na pasta itens recuperáveis do usuário, sem copiá-los para uma caixa de correio de destino.</span><span class="sxs-lookup"><span data-stu-id="64fc1-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="64fc1-266">Outros exemplos de uso do parâmetro SearchQuery</span><span class="sxs-lookup"><span data-stu-id="64fc1-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="64fc1-p141">Aqui estão alguns exemplos de como usar o parâmetro *SearchQuery* para localizar mensagens específicas. Se você usar o parâmetro *SearchQuery* para procurar itens específicos, considere copiar os resultados da pesquisa para uma caixa de correio de destino para que você possa revisar os resultados da pesquisa e, em seguida, revisar a consulta, se necessário, antes de excluir os resultados de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p141">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="64fc1-269">Este exemplo retorna mensagens que contêm uma frase específica no campo Subject.</span><span class="sxs-lookup"><span data-stu-id="64fc1-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="64fc1-270">Este exemplo retorna mensagens que foram enviadas dentro do intervalo de datas especificado.</span><span class="sxs-lookup"><span data-stu-id="64fc1-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="64fc1-271">Este exemplo retorna mensagens que foram enviadas para a pessoa especificada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="64fc1-272">Verificar se os itens foram excluídos</span><span class="sxs-lookup"><span data-stu-id="64fc1-272">Verify that items were deleted</span></span>

<span data-ttu-id="64fc1-p142">Para verificar se você excluiu com êxito itens da pasta itens recuperáveis de uma caixa de correio, use o cmdlet **Get-MailboxFolderStatistics** no PowerShell do Exchange Online para verificar o tamanho e o número de itens na pasta itens recuperáveis. Você pode comparar essas estatísticas com as que você coletou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p142">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="64fc1-275">Execute o seguinte comando em para obter o tamanho atual e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="64fc1-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="64fc1-276">Execute o seguinte comando para obter o tamanho e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio de arquivo morto do usuário.</span><span class="sxs-lookup"><span data-stu-id="64fc1-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="64fc1-277">Etapa 6: reverter a caixa de correio para o estado anterior</span><span class="sxs-lookup"><span data-stu-id="64fc1-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="64fc1-p143">A etapa final é reverter a caixa de correio de volta à configuração anterior. Isso significa redefinir as propriedades que você alterou na etapa 2 e aplicar novamente as isenções que foram removidas na etapa 3. Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="64fc1-p143">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="64fc1-p144">Alterar o período de retenção do item excluído de volta para o valor anterior. Como alternativa, você pode simplesmente deixar esse conjunto como 30 dias, o valor máximo no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p144">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="64fc1-283">Reabilitar a recuperação de item único.</span><span class="sxs-lookup"><span data-stu-id="64fc1-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="64fc1-284">Habilitar novamente os métodos de acesso para cliente para que o proprietário possa acessar a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="64fc1-285">Aplicando novamente as políticas de retenção de isenções e do Office 365 que você removeu.</span><span class="sxs-lookup"><span data-stu-id="64fc1-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="64fc1-286">Habilitar novamente o assistente de pasta gerenciada para processar a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="64fc1-287">Recomendamos que você Aguarde 24 horas após a reaplicação de uma política de retenção de bloqueio ou do Office 365 (e verifique se ela está no local) antes de reabilitar o assistente de pasta gerenciada para processar a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="64fc1-288">Execute as seguintes etapas (na sequência especificada) no PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="64fc1-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="64fc1-p145">Execute o seguinte comando para alterar o período de retenção do item excluído de volta para seu valor original. Isso pressupõe que a configuração anterior tenha menos de 30 dias; por exemplo, 14 dias.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p145">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="64fc1-291">Execute o seguinte comando para reabilitar a recuperação de item único.</span><span class="sxs-lookup"><span data-stu-id="64fc1-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="64fc1-292">Execute o seguinte comando para reabilitar todos os métodos de acesso para cliente para a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="64fc1-p146">Aplique novamente as isenções que você removeu na etapa 3. Dependendo do tipo de retenção, use um dos procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p146">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="64fc1-295">**Retenção de litígio**</span><span class="sxs-lookup"><span data-stu-id="64fc1-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="64fc1-296">Execute o seguinte comando para reabilitar uma retenção de litígio para a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="64fc1-297">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="64fc1-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="64fc1-298">Use o Eat (ou o PowerShell do Exchange Online) para adicionar a caixa de correio de volta ao bloqueio in-loco.</span><span class="sxs-lookup"><span data-stu-id="64fc1-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="64fc1-299">**Políticas de retenção do Office 365 aplicadas a caixas de correio específicas**</span><span class="sxs-lookup"><span data-stu-id="64fc1-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="64fc1-p147">Use o centro &amp; de conformidade de segurança para adicionar a caixa de correio de volta à política de retenção do Office 365. Vá para a página **retenção** de **governança** \> de data no &amp; centro de conformidade de segurança, edite a política de retenção e adicione a caixa de correio de volta à lista de destinatários aos quais a política de retenção é aplicada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p147">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="64fc1-302">**Políticas de retenção do Office 365 em toda a organização**</span><span class="sxs-lookup"><span data-stu-id="64fc1-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="64fc1-p148">Se você removeu uma política de retenção em toda a organização ou em todo o Exchange excluindo-a da política, &amp; use o centro de conformidade de segurança para remover a caixa de correio da lista de usuários excluídos. Vá para a página **retenção** de **governança** \> de data no &amp; centro de conformidade de segurança, edite a política de retenção em toda a organização e remova a caixa de correio da lista de destinatários excluídos. Isso reaplicará a política de retenção à caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p148">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="64fc1-306">**retenção de ocorrência de descoberta eletrônica**</span><span class="sxs-lookup"><span data-stu-id="64fc1-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="64fc1-p149">Use o centro &amp; de conformidade de segurança para adicionar a caixa de correio de volta à retenção associada a uma ocorrência de descoberta eletrônica. Vá para a página de **descoberta eletrônica** de investigação \> de &amp; \*\*pesquisa &amp; \*\* no centro de conformidade de segurança, abra o caso e adicione a caixa de correio de volta à isenção.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p149">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="64fc1-p150">Execute o seguinte comando para permitir que o assistente de pasta gerenciada processe a caixa de correio novamente. Conforme mencionado anteriormente, recomendamos que você espere 24 horas após a reaplicação de uma política de retenção de bloqueio ou do Office 365 (e confirmar se ela está no lugar) antes de reabilitar o assistente de pasta gerenciada.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p150">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="64fc1-311">Para verificar se a caixa de correio foi revertida para a configuração anterior, você pode executar os seguintes comandos e comparar as configurações com as que você coletou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64fc1-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="64fc1-312">Mais informações</span><span class="sxs-lookup"><span data-stu-id="64fc1-312">More information</span></span>

<span data-ttu-id="64fc1-p151">Aqui está uma tabela que descreve como identificar diferentes tipos de isenções com base nos valores da propriedade *InPlaceHolds* quando você executa os cmdlets **Get-Mailbox** ou **Get-OrganizationConfig** . Para obter informações mais detalhadas, consulte [como identificar o tipo de retenção colocado em uma caixa de correio do Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="64fc1-p151">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="64fc1-315">Conforme explicado anteriormente, você deve remover todas as retenções e políticas de retenção do Office 365 de uma caixa de correio antes de poder excluir itens com êxito na pasta itens recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="64fc1-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="64fc1-316">**Tipo de bloqueio**</span><span class="sxs-lookup"><span data-stu-id="64fc1-316">**Hold type**</span></span>|<span data-ttu-id="64fc1-317">**Valor de exemplo**</span><span class="sxs-lookup"><span data-stu-id="64fc1-317">**Example value**</span></span>|<span data-ttu-id="64fc1-318">**Como identificar a isenção**</span><span class="sxs-lookup"><span data-stu-id="64fc1-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64fc1-319">Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="64fc1-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="64fc1-320">A propriedade *LitigationHoldEnabled* está definida como `True`.</span><span class="sxs-lookup"><span data-stu-id="64fc1-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="64fc1-321">Bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="64fc1-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="64fc1-p152">A propriedade *InPlaceHolds* contém o GUID do bloqueio in-loco colocado na caixa de correio. É possível dizer que isso é um bloqueio in-loco porque o GUID não começa com um prefixo.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p152">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="64fc1-324">Você pode usar o `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` comando no PowerShell do Exchange Online para obter informações sobre o bloqueio in-loco da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-324">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="64fc1-325">Políticas de retenção do Office 365 no &amp; centro de conformidade de segurança aplicado a caixas de correio específicas</span><span class="sxs-lookup"><span data-stu-id="64fc1-325">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="64fc1-326">ou</span><span class="sxs-lookup"><span data-stu-id="64fc1-326">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="64fc1-p153">Quando você executa o cmdlet **Get-Mailbox** , a propriedade *INPLACEHOLDS* também contém GUIDs das políticas de retenção do Office 365 aplicadas à caixa de correio. Você pode identificar as políticas de retenção porque o GUID começa `mbx` com o prefixo. Observe que, se o GUID da política de retenção começar com `skp` o prefixo, isso indica que a política de retenção é aplicada às conversas do Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p153">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="64fc1-330">Para identificar a política de retenção do Office 365 aplicada à caixa de correio, execute o seguinte comando no &amp; PowerShell do centro de conformidade de segurança:</span><span class="sxs-lookup"><span data-stu-id="64fc1-330">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="64fc1-331">Certifique-se de remover `mbx` o `skp` prefixo ou ao executar este comando.</span><span class="sxs-lookup"><span data-stu-id="64fc1-331">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="64fc1-332">Políticas de retenção do Office 365 em toda a organização &amp; no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="64fc1-332">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="64fc1-333">Nenhum valor</span><span class="sxs-lookup"><span data-stu-id="64fc1-333">No value</span></span>  <br/> <span data-ttu-id="64fc1-334">ou</span><span class="sxs-lookup"><span data-stu-id="64fc1-334">or</span></span>  <br/>  <span data-ttu-id="64fc1-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(indica que a caixa de correio é excluída de uma política de toda a organização)</span><span class="sxs-lookup"><span data-stu-id="64fc1-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="64fc1-336">Mesmo se a propriedade *InPlaceHolds* estiver vazia quando você executar o cmdlet **Get-Mailbox** , ainda poderá haver uma ou mais políticas de retenção do Office 365 em toda a organização aplicadas à caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="64fc1-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="64fc1-p154">Para verificar isso, você pode executar o `Get-OrganizationConfig | FL InPlaceHolds` comando no PowerShell do Exchange Online para obter uma lista dos GUIDs das políticas de retenção do Office 365 em toda a organização. O GUID das políticas de retenção em toda a organização aplicada às caixas de correio do `mbx` Exchange começam com o prefixo; por exemplo `mbxa3056bb15562480fadb46ce523ff7b02`.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p154">To verify this, you can run the  `Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <span data-ttu-id="64fc1-339">Para identificar a política de retenção do Office 365 em toda a organização que é aplicada à caixa de correio, execute o &amp; seguinte comando no PowerShell do centro de conformidade de segurança:</span><span class="sxs-lookup"><span data-stu-id="64fc1-339">To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="64fc1-340">Observe que, se uma caixa de correio for excluída de uma política de retenção do Office 365 em toda a organização, o GUID da política de retenção será exibido na propriedade *InPlaceHolds* da caixa de correio do usuário quando você executar o cmdlet **Get-Mailbox** ; é identificado pelo prefixo `-mbx`; por exemplo,`-mbxe9b52bf7ab3b46a286308ecb29624696`</span><span class="sxs-lookup"><span data-stu-id="64fc1-340">Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696`</span></span> <br/> |
|<span data-ttu-id="64fc1-341">retenção de caso de descoberta eletrônica &amp; no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="64fc1-341">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="64fc1-p155">A propriedade *InPlaceHolds* também contém o GUID de qualquer isenção associada a uma ocorrência de descoberta eletrônica &amp; no centro de conformidade de segurança que possa ser colocado na caixa de correio. É possível dizer que esta é uma retenção de caso de descoberta eletrônica porque o `UniH` GUID começa com o prefixo.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p155">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="64fc1-p156">Você pode usar o `Get-CaseHoldPolicy` cmdlet no PowerShell &amp; do centro de conformidade de segurança para obter informações sobre a ocorrência de descoberta eletrônica à qual a retenção da caixa de correio está associada. Por exemplo, você pode executar o comando `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` para exibir o nome da retenção de caso que está na caixa de correio. Certifique-se de remover `UniH` o prefixo ao executar este comando.</span><span class="sxs-lookup"><span data-stu-id="64fc1-p156">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="64fc1-347">Para identificar a ocorrência de descoberta eletrônica à qual a retenção da caixa de correio está associada, execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="64fc1-347">To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:</span></span><br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


