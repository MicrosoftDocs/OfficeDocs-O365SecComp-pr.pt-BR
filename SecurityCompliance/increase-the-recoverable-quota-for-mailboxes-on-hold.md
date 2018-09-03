---
title: Aumentar a cota de Itens Recuperáveis para caixas de correio em espera
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Habilite a caixa de correio de arquivo morto e ativar o arquivamento para aumentar o tamanho da pasta itens recuperáveis para uma caixa de correio no Office 365 expansão automática. '
ms.openlocfilehash: cd2d07e6ef1637343798ccb71870c8d436f10574
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782088"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="37cc7-103">Aumentar a cota de Itens Recuperáveis para caixas de correio em espera</span><span class="sxs-lookup"><span data-stu-id="37cc7-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="37cc7-p101">A política de retenção padrão — denominada política MRM padrão — isto é automaticamente aplicadas para novas caixas de correio no Exchange Online contém uma marca de retenção nomeados dias de 14 de itens recuperáveis mover para arquivo morto. Nesta marca de retenção move itens da pasta itens recuperáveis na caixa de correio principal do usuário para a pasta itens recuperáveis na caixa de correio de arquivo morto do usuário depois que o período de retenção de 14 dias expira para um item. Para isso acontecer, a caixa de correio de arquivo morto do usuário deve ser habilitada. Se a caixa de correio de arquivo morto não estiver habilitada, nenhuma ação é executada, que significa que itens em que a pasta para uma caixa de correio em retenção de itens recuperáveis não foram movidas para a caixa de correio de arquivo morto após o período de retenção de 14 dias expirar. Como nothing é excluído de uma caixa de correio em espera, é possível que a cota de armazenamento para a pasta itens recuperáveis pode ser excedida, especialmente se a caixa de correio de arquivo morto do usuário não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="37cc7-p102">Para ajudar a reduzir a chance de exceder esse limite, a cota de armazenamento para a pasta itens recuperáveis é automaticamente aumentou de 30 GB para 100 GB quando uma isenção for colocada em uma caixa de correio no Exchange Online. Se a caixa de correio de arquivo morto estiver habilitada, a cota de armazenamento para a pasta itens recuperáveis na caixa de correio de arquivamento também é aumentada de 30 GB para 100 GB. Se o arquivamento de expansão automática de recurso no Exchange Online é habilitada, a cota de armazenamento para a pasta itens recuperáveis no arquivo do usuário será ilimitada.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="37cc7-112"> A tabela a seguir resume a cota de armazenamento da pasta Itens Recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="37cc7-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="37cc7-113">**Local da pasta Itens Recuperáveis**</span><span class="sxs-lookup"><span data-stu-id="37cc7-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="37cc7-114">**Caixas de correio não em espera**</span><span class="sxs-lookup"><span data-stu-id="37cc7-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="37cc7-115">**Caixas de correio em espera**</span><span class="sxs-lookup"><span data-stu-id="37cc7-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37cc7-116">Caixa de correio principal</span><span class="sxs-lookup"><span data-stu-id="37cc7-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="37cc7-117">30 GB</span><span class="sxs-lookup"><span data-stu-id="37cc7-117">30 GB</span></span>  <br/> |<span data-ttu-id="37cc7-118">100 GB</span><span class="sxs-lookup"><span data-stu-id="37cc7-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="37cc7-119">Caixa de correio de arquivo morto<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="37cc7-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="37cc7-120">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="37cc7-120">Unlimited</span></span>  <br/> |<span data-ttu-id="37cc7-121">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="37cc7-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="37cc7-122">**Cota de armazenamento total para a pasta Itens Recuperáveis**</span><span class="sxs-lookup"><span data-stu-id="37cc7-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="37cc7-123">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="37cc7-123">Unlimited</span></span>  <br/> |<span data-ttu-id="37cc7-124">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="37cc7-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="37cc7-p103"><sup>\*</sup>A cota de armazenamento inicial para a caixa de correio de arquivo morto é de 100 GB para usuários com uma licença do Exchange Online (plano 2). No entanto, quando expansão automática arquivamento está ativado para caixas de correio em espera, a cota de armazenamento para ambos os a caixa de correio de arquivo morto e a pasta itens recuperáveis é aumentado para 110 GB. Espaço de armazenamento de arquivo morto adicional será provisionado quando necessário que resulta em uma quantidade ilimitada de armazenamento de arquivamento. Para obter mais informações sobre a expansão automática arquivamento, consulte [Overview of arquivamento ilimitado no Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="37cc7-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on for mailboxes on hold, the storage quota for both the the archive mailbox and the Recoverable Items folder is increased to 110 GB. Additional archive storage space will be provisioned when necessary which results in an unlimited amount of archive storage. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="37cc7-129">Quando a cota de armazenamento da pasta Itens Recuperáveis na caixa de correio principal de uma caixa de correio em espera está quase atingindo o limite, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="37cc7-129">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="37cc7-p104">**Habilitar a caixa de correio de arquivo morto e ativar o arquivamento expansão automática** - você pode habilitar uma capacidade de armazenamento ilimitado para a pasta itens recuperáveis simplesmente com a habilitação da caixa de correio de arquivo morto e, em seguida, ativem o recurso de arquivamento expansão automática no Exchange Online. Isso resulta em 110 GB para a pasta itens recuperáveis na caixa de correio primária e uma quantidade ilimitada de capacidade de armazenamento para a pasta itens recuperáveis no arquivo do usuário. Consulte como: [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="37cc7-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 110 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="37cc7-p105">Depois de habilitar o arquivamento para uma caixa de correio que está prestes a exceder a cota de armazenamento para a pasta itens recuperáveis, talvez você queira executar o Assistente de pasta gerenciada para disparar manualmente o Assistente para processar a caixa de correio, para que os itens expirados são movidos do Pasta itens recuperáveis na caixa de correio de arquivo morto. Para obter instruções, consulte a [etapa 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Observe que os outros itens na caixa de correio do usuário podem ser movidos para a nova caixa de correio de arquivo morto. Considere informando ao usuário que isso pode acontecer depois de habilitar a caixa de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="37cc7-p106">**Criar uma política de retenção personalizada para caixas de correio em espera** - além de habilitar a caixa de correio de arquivo morto e arquivamento de caixas de correio em retenção de litígio ou bloqueio In-loco, expansão automática também convém criar uma política de retenção personalizada para caixas de correio em espera. Isso vamos você aplicar uma política de retenção a caixas de correio em espera é diferente da política MRM padrão que é aplicado a caixas de correio que não estão em espera. Isso permite que você para aplicar marcas de retenção projetados especificamente para caixas de correio em espera. Isso inclui a criação de uma nova marca de retenção para a pasta itens recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="37cc7-141">O restante deste tópico descreve os procedimentos passo a passo para criar uma política de retenção personalizada para caixas de correio em espera.</span><span class="sxs-lookup"><span data-stu-id="37cc7-141">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="37cc7-142">Etapa 1: criar uma marca de retenção personalizada para a pasta Itens Recuperáveis</span><span class="sxs-lookup"><span data-stu-id="37cc7-142">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="37cc7-143">[[Etapa 2: criar uma nova política de retenção para caixas de correio em espera](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="37cc7-143">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="37cc7-144">Etapa 3: Aplicar a nova política de retenção a caixas de correio em espera</span><span class="sxs-lookup"><span data-stu-id="37cc7-144">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="37cc7-145">(Opcional) Etapa 4: executar o Assistente de Pasta Gerenciada para aplicar as novas configurações de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-145">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="37cc7-146">Etapa 1: Criar uma marca de retenção personalizada para a pasta Itens Recuperáveis</span><span class="sxs-lookup"><span data-stu-id="37cc7-146">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="37cc7-p107">A primeira etapa é criar uma marca de retenção personalizados (chamada de uma marca de política de retenção ou RPT) para a pasta itens recuperáveis. Conforme explicado anteriormente, este RPT move itens da pasta itens recuperáveis na caixa de correio principal do usuário para a pasta itens recuperáveis na caixa de correio de arquivo morto do usuário. Você precisa usar o PowerShell para criar um RPT para a pasta itens recuperáveis. Você não pode usar o Centro de administração do Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="37cc7-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. [<span data-ttu-id="37cc7-151">Conectar-se ao Exchange Online usando o PowerShell remoto</span><span class="sxs-lookup"><span data-stu-id="37cc7-151">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. <span data-ttu-id="37cc7-152">Execute o seguinte comando para criar um novo relatório para a pasta Itens Recuperáveis: </span><span class="sxs-lookup"><span data-stu-id="37cc7-152">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="37cc7-p108">Por exemplo, o comando a seguir cria um relatório para a pasta Itens Recuperáveis denominado "Itens Recuperáveis para caixas de correio em retenção: 30 dias", com um período de retenção de 30 dias. Isso significa que depois que um item estiver na pasta Itens Recuperáveis por 30 dias, ele será movido para a pasta Itens Recuperáveis na caixa de correio de arquivo morto do usuário.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="37cc7-p109">É recomendável que o período de retenção (definido pelo parâmetro _AgeLimitForRetention_ ) para o RPT itens recuperáveis é o mesmo que o período de retenção de itens excluídos para as caixas de correio que será aplicada a RPT para. Isso permite que um usuário o período de retenção de item excluído inteira para recuperar itens excluídos antes que eles serão movidos para a caixa de correio de arquivo morto. No exemplo anterior, o período de retenção foi definido como 30 dias, com base na pressuposição de que o período de retenção de itens excluídos para caixas de correio também é 30 dias. Uma caixa de correio do Exchange Online é configurada para reter itens excluídos 14 dias, por padrão. Mas você pode alterar essa configuração para um máximo de 30 dias. Para obter mais informações, consulte [alterar o período de retenção de item excluído de uma caixa de correio no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span><span class="sxs-lookup"><span data-stu-id="37cc7-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="37cc7-161">Etapa 2: Criar uma nova política de retenção para caixas de correio em espera</span><span class="sxs-lookup"><span data-stu-id="37cc7-161">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="37cc7-p110">A próxima etapa é criar uma nova política de retenção e adicionar marcas de retenção a ela, inclusive o RPT de Itens Recuperáveis que você criou na Etapa 1. Essa nova política será aplicada às caixas de correio em espera na próxima etapa. </span><span class="sxs-lookup"><span data-stu-id="37cc7-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="37cc7-p111">Antes de criar a nova política de retenção, determine as marcas de retenção adicionais que você deseja adicionar. Confira a lista das marcas de retenção adicionadas à política MRM Padrão e informações sobre como criar novas marcas de retenção em:</span><span class="sxs-lookup"><span data-stu-id="37cc7-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="37cc7-166">Padrão política de retenção no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="37cc7-166">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="37cc7-167">Pastas padrão que suportam marcas de diretiva de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-167">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="37cc7-168">A seção "Criar uma marca de retenção" no tópico [criar uma política de retenção](https://go.microsoft.com/fwlink/p/?LinkId=404422) .</span><span class="sxs-lookup"><span data-stu-id="37cc7-168">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="37cc7-169">Você pode usar o EAC ou o Exchange Online PowerShell para criar uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="37cc7-169">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="37cc7-170">Usar o EAC para criar uma política de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-170">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="37cc7-171">No EAC, vá até **gerenciamento de conformidade** \> **políticas de retenção**e, em seguida, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="37cc7-171">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="37cc7-172">Na página **Nova política de retenção**, em **Nome**, digite um nome que descreva o propósito da política de retenção, por exemplo, **MRM Policy for Mailboxes on Hold**. </span><span class="sxs-lookup"><span data-stu-id="37cc7-172">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="37cc7-173">Em **marcas de retenção**, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="37cc7-173">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="37cc7-174">Na lista de marcas de retenção, selecione o relatório de itens recuperáveis que você criou na Etapa 1 e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-174">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![Selecione a marca de retenção personalizada Itens Recuperáveis](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="37cc7-p112">Selecione marcas de retenção adicionais para adicionar à política de retenção. Por exemplo, convém adicionar as mesmas marcas que são incluídas na Política de MRM Padrão.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="37cc7-178">Quando terminar de adicionar marcas de retenção, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-178">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="37cc7-179">Clique em **Salvar** para criar a nova política de retenção. </span><span class="sxs-lookup"><span data-stu-id="37cc7-179">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="37cc7-180">Observe que as marcas de retenção vinculadas à política de retenção são exibidas no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="37cc7-180">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![Marcas de retenção vinculadas à política de retenção são exibidas no painel de detalhes](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="37cc7-182">Use o PowerShell do Exchange Online para criar uma política de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-182">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="37cc7-183">Execute o comando a seguir para criar a nova política de retenção para caixas de correio em espera. </span><span class="sxs-lookup"><span data-stu-id="37cc7-183">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="37cc7-184">Por exemplo, o comando a seguir cria a política de retenção e as marcas de retenção vinculadas que são exibidas na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="37cc7-184">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="37cc7-185">Etapa 3: Aplicar a nova política de retenção a caixas de correio em espera</span><span class="sxs-lookup"><span data-stu-id="37cc7-185">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="37cc7-p113">A última etapa é aplicar a nova política de retenção que você criou na etapa 2 para caixas de correio em espera em sua organização. Você pode usar o EAC ou o Exchange Online PowerShell para aplicar a política de retenção para uma única caixa de correio ou para várias caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="37cc7-188">Usar o EAC para aplicar a nova política de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-188">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="37cc7-189">Acesse **Destinatários** \> **Caixas de Correio**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-189">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="37cc7-190">Na exibição de lista, selecione a caixa de correio que você deseja aplicar a política de retenção e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="37cc7-190">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="37cc7-191">Na página **Caixa de Correio do Usuário**, clique em **Recursos de caixa de correio**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-191">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="37cc7-192">Em **Política de retenção**, selecione a política de retenção que você criou na Etapa 2 e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-192">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="37cc7-193">Você também pode usar o EAC para aplicar a política de retenção a várias caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="37cc7-193">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="37cc7-194">Acesse **Destinatários** \> **Caixas de Correio**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-194">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="37cc7-195">No modo de exibição de lista, use as teclas Shift ou Ctrl, para selecionar várias caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="37cc7-195">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="37cc7-196">No painel de detalhes, clique em **Mais opções**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-196">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="37cc7-197">Em **Política de Retenção**, clique em **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="37cc7-197">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="37cc7-198">Na página **Atribuir em massa uma política de retenção**, selecione a política de retenção que você criou na Etapa 2 e clique em **Salvar**. </span><span class="sxs-lookup"><span data-stu-id="37cc7-198">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="37cc7-199">Use o PowerShell do Exchange Online para aplicar a nova política de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-199">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="37cc7-p114">Você pode usar o PowerShell do Exchange Online para aplicar uma nova política de retenção a uma única caixa de correio. Mas o poder real do PowerShell é que você pode usá-lo a identificar rapidamente todas as caixas de correio em sua organização que estão na lista litígio ou bloqueio In-loco e aplicam a nova política de retenção para todas as caixas de correio em espera em um único comando. Aqui estão alguns exemplos de como usar o PowerShell do Exchange para aplicar uma política de retenção a uma ou mais caixas de correio. Todos os exemplos de aplicam a política de retenção que foi criada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="37cc7-204">Este exemplo aplica a nova política de retenção à caixa de correio de Clara Barbosa.</span><span class="sxs-lookup"><span data-stu-id="37cc7-204">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="37cc7-205">Este exemplo aplica a nova política de retenção a todas as caixas de correio na organização que estão em Retenção de Litígio.</span><span class="sxs-lookup"><span data-stu-id="37cc7-205">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="37cc7-206">Este exemplo aplica a nova política de retenção a todas as caixas de correio na organização que estão em Bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="37cc7-206">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="37cc7-207">Você pode usar o cmdlet **Get-Mailbox** para verificar se a nova política de retenção foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="37cc7-207">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="37cc7-208">Aqui estão alguns exemplos para verificar se os comandos nos exemplos anteriores aplicaram a "Política MRM a caixas de correio em espera" em caixas de correio em Retenção de Litígio e caixas de correio em Bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="37cc7-208">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="37cc7-209">(Opcional) Etapa 4: Executar o Assistente de Pasta Gerenciada para aplicar as novas configurações de retenção</span><span class="sxs-lookup"><span data-stu-id="37cc7-209">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="37cc7-p115">Depois de aplicar a nova política de retenção a caixas de correio em espera, pode demorar até sete dias no Exchange Online para o Assistente de pasta gerenciada processar essas caixas de correio usando as configurações da nova política de retenção. Em vez de esperar executar o Assistente de pasta gerenciada, você pode usar o cmdlet **Start-ManagedFolderAssistant** para acionar manualmente o Assistente para processar as caixas de correio que você aplicou a nova política de retenção para.</span><span class="sxs-lookup"><span data-stu-id="37cc7-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="37cc7-212">Execute o comando a seguir para iniciar o Assistente de Pasta Gerenciada para caixa de correio de Clara Barbosa.</span><span class="sxs-lookup"><span data-stu-id="37cc7-212">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="37cc7-213">Execute os comandos a seguir para iniciar o Assistente de Pasta Gerenciada para todas as caixas de correio em espera.</span><span class="sxs-lookup"><span data-stu-id="37cc7-213">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="37cc7-214">Mais informações</span><span class="sxs-lookup"><span data-stu-id="37cc7-214">More information</span></span>

- <span data-ttu-id="37cc7-p116">Após habilitar a caixa de correio de arquivo morto do usuário, considere informando ao usuário que outros itens em suas caixas de correio (não apenas itens na pasta itens recuperáveis) podem ser movidos para a caixa de correio de arquivo morto. Isto ocorre porque a política MRM padrão atribuído às caixas de correio Exchange Online contém uma marca de retenção (nomeada padrão para a 2 anos movem para arquivo morto) que move itens na caixa de correio de arquivo morto dois anos após a data em que o item foi entregue à caixa de correio ou criado pela usuário. Para obter mais informações, consulte a [Política de retenção padrão no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span><span class="sxs-lookup"><span data-stu-id="37cc7-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="37cc7-p117">Após habilitar a caixa de correio de arquivo morto do usuário, você também pode instruir o usuário que eles podem recuperar os itens excluídos na pasta itens recuperáveis em suas caixas de correio de arquivo morto. Eles podem fazer isso no Outlook, selecionando a pasta **Itens excluídos** na caixa de correio de arquivo morto e, em seguida, clicando em **Recuperar itens excluídos do servidor** , na guia **página inicial** . Para obter mais informações sobre a recuperação de itens excluídos, consulte [que recuperar itens excluídos no Outlook para Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span><span class="sxs-lookup"><span data-stu-id="37cc7-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
