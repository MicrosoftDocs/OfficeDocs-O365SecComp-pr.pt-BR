---
title: Colocar um bloqueio in-loco em uma caixa de correio excluída de forma reversível no Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Saiba como criar um bloqueio in-loco para uma caixa de correio excluída de forma reversível para torná-la inativa e preservar seu conteúdo. Em seguida, você pode usar as ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.
ms.openlocfilehash: 70feb265e95741406dbf170c6be70bd83b2ec081
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223520"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="378be-104">Colocar um bloqueio in-loco em uma caixa de correio excluída de forma reversível no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="378be-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="378be-p102">Saiba como criar um bloqueio in-loco para uma caixa de correio excluída de forma reversível para torná-la inativa e preservar seu conteúdo. Em seguida, você pode usar as ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="378be-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="378be-p103">Adiamos o prazo para a criação de novas suspensões in-loco no Exchange Online (nos planos autônomos do Office 365 e do Exchange Online). Mas, posteriormente neste ano ou no início do próximo ano, você não poderá criar novos bloqueios in-loco no Exchange Online. Como alternativa ao uso de bloqueio in-loco, você pode usar [casos de descoberta eletrônica](https://go.microsoft.com/fwlink/?linkid=780738) ou [políticas de retenção](https://go.microsoft.com/fwlink/?linkid=827811) no centro &amp; de conformidade de segurança do Office 365. Depois de encerrarmos novas suspensões in-loco, você ainda poderá modificar bloqueios in-loco existentes e criar novos bloqueios in-loco no Exchange Server 2013 e implantações híbridas do Exchange ainda terão suporte. Além disso, você ainda poderá colocar caixas de correio em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="378be-p103">We've postponed the deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="378be-p104">Você pode ter uma situação em que uma pessoa deixou sua organização e a conta de usuário correspondente e caixa de correio foram excluídas. Posteriormente, você perceberá que há informações na caixa de correio que precisam ser preservadas. O que você pode fazer? Se o período de retenção de caixa de correio excluída ainda não tiver expirado, você pode colocar um bloqueio in-loco na caixa de correio excluída (chamada de caixa de correio excluída por software) e torná-la uma caixa de correio inativa. Uma *caixa de correio inativa* é usada para preservar o email de um funcionário anterior, depois que ele deixa sua organização. O conteúdo de uma caixa de correio inativa é preservado para a duração do bloqueio in-loco que foi colocado na caixa de correio excluída por software quando ele foi tornado inativo. Após a caixa de correio ser desativada, você pode pesquisar a caixa de correio usando a descoberta eletrônica in-loco no Exchange Online, pesquisa de &amp; conteúdo no centro de conformidade de segurança do Office 365 ou no centro de descoberta eletrônica no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="378be-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="378be-p105">No Exchange Online, uma caixa de correio excluída por software é uma caixa de correio excluída, mas pode ser recuperada dentro de um período de retenção específico. O período de retenção de caixa de correio excluída de forma reversível no Exchange Online é de 30 dias. Isso significa que a caixa de correio pode ser recuperada (ou criada em uma caixa de correio inativa) em 30 dias após a exclusão. Após 30 dias, uma caixa de correio excluída por software é marcada para exclusão permanente e não pode ser recuperada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="378be-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="378be-123">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="378be-123">Before you begin</span></span>

- <span data-ttu-id="378be-p106">Você precisa usar o cmdlet **New-MailboxSearch** no Windows PowerShell para colocar um bloqueio in-loco em uma caixa de correio excluída de forma reversível. Você não pode usar o centro de administração do Exchange (Eat) ou o centro de descoberta eletrônica no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="378be-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="378be-126">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira o artigo [Conectar-se ao Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="378be-126">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="378be-127">Execute o seguinte comando para obter informações de identidade sobre as caixas de correio excluídas por software em sua organização.</span><span class="sxs-lookup"><span data-stu-id="378be-127">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="378be-128">Para obter mais informações sobre caixas de correio inativas, consulte [visão geral das caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="378be-128">For more information about inactive mailboxes, see [Overview of inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="378be-129">Colocar um bloqueio in-loco em uma caixa de correio excluída de forma reversível para torná-la uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="378be-129">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>

<span data-ttu-id="378be-p107">Use o cmdlet **New-MailboxSearch** para tornar uma caixa de correio de exclusão flexível uma caixa de correio inativa. Para obter mais informações, consulte [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="378be-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="378be-132">Criar uma variável que contém as propriedades da caixa de correio excluída de forma reversível.</span><span class="sxs-lookup"><span data-stu-id="378be-132">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > <span data-ttu-id="378be-p108">No comando anterior, use o valor da propriedade **distinguishedName** ou **ExchangeGuid** para identificar a caixa de correio excluída de forma reversível. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto é possível que uma caixa de correio ativa e uma caixa de correio excluída de forma reversível possam ter o mesmo endereço SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="378be-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="378be-p109">Crie um bloqueio in-loco e coloque-o na caixa de correio excluída de forma reversível. Neste exemplo, não é especificada nenhuma duração de retenção. Isso significa que os itens serão mantidos indefinidamente ou até que a retenção seja removida da caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="378be-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   <span data-ttu-id="378be-p110">Você também pode especificar uma duração de retenção ao criar o bloqueio in-loco. Este exemplo mantém itens na caixa de correio inativa por aproximadamente 7 anos.</span><span class="sxs-lookup"><span data-stu-id="378be-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. <span data-ttu-id="378be-140">Após alguns momentos, execute um dos seguintes comandos para verificar se a caixa de correio excluída por software é uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="378be-140">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    <span data-ttu-id="378be-141">Ou</span><span class="sxs-lookup"><span data-stu-id="378be-141">Or</span></span>
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a><span data-ttu-id="378be-142">Mais informações</span><span class="sxs-lookup"><span data-stu-id="378be-142">More information</span></span>

<span data-ttu-id="378be-p111">Após tornar uma caixa de correio inativa excluída por software, há várias maneiras de gerenciar a caixa de correio. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="378be-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- [<span data-ttu-id="378be-145">Alterar a duração de retenção de uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="378be-145">Change the hold duration for an inactive mailbox</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [<span data-ttu-id="378be-146">Recuperar uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="378be-146">Recover an inactive mailbox</span></span>](recover-an-inactive-mailbox.md)
    
- [<span data-ttu-id="378be-147">Restaurar uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="378be-147">Restore an inactive mailbox</span></span>](restore-an-inactive-mailbox.md)
    
- <span data-ttu-id="378be-148">[Excluir uma caixa de correio inativa](delete-an-inactive-mailbox.md) (removendo a retenção)</span><span class="sxs-lookup"><span data-stu-id="378be-148">[Delete an inactive mailbox](delete-an-inactive-mailbox.md) (by removing the hold)</span></span>
