---
title: Colocar um bloqueio In-loco em uma caixa de correio excluída no Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Saiba como criar um bloqueio In-loco para uma caixa de correio excluída para torná-la inativa e preservar o seu conteúdo. Em seguida, você pode usar ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.
ms.openlocfilehash: b4ef4ee26e98c8234f64d0879391f8fec89ffd3c
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038244"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="75a57-104">Colocar um bloqueio In-loco em uma caixa de correio excluída no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75a57-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="75a57-p102">Saiba como criar um bloqueio In-loco para uma caixa de correio excluída para torná-la inativa e preservar o seu conteúdo. Em seguida, você pode usar ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="75a57-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="75a57-p103">Podemos foi adiada o prazo 1 de julho de 2017 de criação de novos retenções locais no Exchange Online (em planos autônomos do Office 365 e o Exchange Online). Mas este ano ou próximo ano inicial, você não poderá criar novos retenções locais no Exchange Online. Como alternativa ao uso retenções locais, você pode usar [casos de descoberta eletrônica](https://go.microsoft.com/fwlink/?linkid=780738) ou [políticas de retenção](https://go.microsoft.com/fwlink/?linkid=827811) no Office 365 Security &amp; Centro de conformidade. Depois que o novo, podemos descomissionar retenções locais, você ainda poderá modificar existentes In-Place Holds e criação de novos retenções locais no Exchange Server 2013 e implantações híbridas do Exchange serão ainda suportadas. E, então, você ainda poderá colocar caixas de correio em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="75a57-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="75a57-p104">Você pode ter uma situação em que uma pessoa tenha deixado a sua organização e sua conta de usuário correspondente e uma caixa de correio foram excluídos. Posteriormente, você percebe que não há informações na caixa de correio que precisa ser preservado. O que você pode fazer? Se o período de retenção de caixa de correio excluída não tiver expirado, você pode colocar um bloqueio In-loco na caixa de correio excluída (chamado de uma caixa de correio excluída) e torná-la uma caixa de correio inativa. Uma *caixa de correio inativa* é usado para preservação de emails de um antigo do funcionário depois que ele deixa a sua organização. O conteúdo de uma caixa de correio inativa é preservado para a duração de In-Place Hold foi é colocada na caixa de correio excluída quando ela foi feita inativa. Depois que a caixa de correio é feita inativa, você pode pesquisar a caixa de correio usando a descoberta eletrônica In-loco no Exchange Online, pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, ou o Centro de descoberta eletrônica no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="75a57-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="75a57-p105">No Exchange Online, uma caixa de correio excluída é uma caixa de correio que tenha sido excluída, mas pode ser recuperada em um período de retenção específico. O período de retenção de caixa de correio excluída no Exchange Online é 30 dias. Isso significa que a caixa de correio pode ser recuperado (ou fez uma caixa de correio inativa) dentro de 30 dias do que está sendo excluído. Após 30 dias, uma caixa de correio excluída é marcada para exclusão permanente e não pode ser recuperada ou feita inativa.</span><span class="sxs-lookup"><span data-stu-id="75a57-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="75a57-123">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="75a57-123">Before you begin</span></span>
<span data-ttu-id="75a57-124"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="75a57-124"></span></span>

- <span data-ttu-id="75a57-p106">Você precisa usar o cmdlet **New-MailboxSearch** no Windows PowerShell para colocar um bloqueio In-loco em uma caixa de correio excluída. É possível usar o Centro de administração do Exchange (EAC) ou o Centro de descoberta eletrônica no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="75a57-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="75a57-127">Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira o artigo [Conectar-se ao Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="75a57-127">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="75a57-128">Execute o seguinte comando para obter informações de identidade sobre as caixas de correio excluída na sua organização.</span><span class="sxs-lookup"><span data-stu-id="75a57-128">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="75a57-129">Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span><span class="sxs-lookup"><span data-stu-id="75a57-129">For more information about inactive mailboxes, see [Inactive mailboxes in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="75a57-130">Colocar um bloqueio In-loco em uma caixa de correio excluída para torná-la uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="75a57-130">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>
<span data-ttu-id="75a57-131"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="75a57-131"></span></span>

<span data-ttu-id="75a57-p107">Use o cmdlet **New-MailboxSearch** para fazer uma caixa de correio excluída uma caixa de correio inativa. Para obter mais informações, consulte [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="75a57-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="75a57-134">Crie uma variável que contém as propriedades da caixa de correio excluída.</span><span class="sxs-lookup"><span data-stu-id="75a57-134">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
  ```
  $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
  ```

    > [!IMPORTANT]
    > <span data-ttu-id="75a57-p108">No comando anterior, use o valor da propriedade **DistinguishedName** ou **ExchangeGuid** para identificar a caixa de correio excluída. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto que é possível que uma caixa de correio ativa e uma caixa de correio excluída podem ter o mesmo endereço SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="75a57-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="75a57-p109">Criar um bloqueio In-loco e coloque-o na caixa de correio excluída. Neste exemplo, não há duração de espera é especificada. Isso significa que os itens serão mantidos indefinidamente ou até que a suspensão seja removida da caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="75a57-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
  
  ```

    <span data-ttu-id="75a57-p110">Você também pode especificar uma duração de espera quando você cria o bloqueio In-loco. Este exemplo contém os itens na caixa de correio inativa de aproximadamente sete anos.</span><span class="sxs-lookup"><span data-stu-id="75a57-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
  ```

3. <span data-ttu-id="75a57-142">Após alguns momentos, execute um dos seguintes comandos para verificar se a caixa de correio excluída é uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="75a57-142">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly
  ```

    <span data-ttu-id="75a57-143">Ou</span><span class="sxs-lookup"><span data-stu-id="75a57-143">Or</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
  ```

## <a name="more-information"></a><span data-ttu-id="75a57-144">Mais informações</span><span class="sxs-lookup"><span data-stu-id="75a57-144">More information</span></span>
<span data-ttu-id="75a57-145"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="75a57-145"></span></span>

<span data-ttu-id="75a57-p111">Depois de fazer uma caixa de correio excluída uma caixa de correio inativa, há várias maneiras que você pode gerenciar a caixa de correio. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="75a57-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- [<span data-ttu-id="75a57-148">Alterar a duração de espera para uma caixa de correio inativa no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75a57-148">Change the hold duration for an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [<span data-ttu-id="75a57-149">Recuperar uma caixa de correio inativa no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75a57-149">Recover an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [<span data-ttu-id="75a57-150">Restaurar uma caixa de correio inativa no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75a57-150">Restore an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [<span data-ttu-id="75a57-151">Remover uma isenção de uma caixa de correio inativa no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75a57-151">Remove a hold from an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    

