---
title: Excluir uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: Quando não há mais precisa preservar o conteúdo de uma caixa de correio inativa do Office 365, você pode excluir permanentemente a caixa de correio inativa, removendo isenção. Depois de remover a retenção, a caixa de correio inativa é marcada para exclusão e é excluída permanentemente depois que ela é processada.
ms.openlocfilehash: 91b73fff6ca319735289abe7ea9351b5fba931a0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523527"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="6eeb3-104">Excluir uma caixa de correio inativa no Office 365</span><span class="sxs-lookup"><span data-stu-id="6eeb3-104">Delete an inactive mailbox in Office 365</span></span>

<span data-ttu-id="6eeb3-p102">Uma caixa de correio inativa é usada para preservação de emails de um antigo do funcionário depois que ele deixa a sua organização. Quando não há mais precisa preservar o conteúdo de uma caixa de correio inativa, você pode excluir permanentemente a caixa de correio inativa, removendo a retenção. Além disso, é possível que vários bloqueios podem ser colocados em uma caixa de correio inativa. Por exemplo, uma caixa de correio inativa pode ser colocada em litígio e em um ou mais retenções locais. Além disso, uma política de retenção do Office 365 (criados no Office 365 Security &amp; Centro de conformidade) podem ser aplicadas à caixa de correio inativa. Você precisa remover todas as isenções e políticas de retenção do Office 365 de uma caixa de correio inativa para excluí-lo. Depois de remover o isenções e políticas de retenção, a caixa de correio inativa é marcada para exclusão e é excluída permanentemente depois que ela é processada.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p102">An inactive mailbox is used to preserve a former employee's email after he or she leaves your organization. When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold. Also, it's possible that multiple holds might be placed on an inactive mailbox. For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds. Additionally, an Office 365 retention policy (created in the Office 365 Security &amp; Compliance Center) might be applied to the inactive mailbox. You have to remove all holds and Office 365 retention policies from an inactive mailbox to delete it. After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6eeb3-p103">Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
<span data-ttu-id="6eeb3-117">Consulte a seção de [informações adicionais](delete-an-inactive-mailbox.md#moreinfo) para obter uma descrição do que acontece após isenções serem removidas de uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-117">See the [More information](delete-an-inactive-mailbox.md#moreinfo) section for a description of what happens after holds are removed from an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6eeb3-118">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="6eeb3-118">Before you begin</span></span>

- <span data-ttu-id="6eeb3-p104">Você precisa usar o PowerShell do Exchange Online para remover um litígio de uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Você pode usar o PowerShell do Exchange Online ou o EAC para remover um bloqueio In-loco de uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p104">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the Exchange admin center (EAC). For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). You can use Exchange Online PowerShell or the EAC to remove an In-Place Hold from an inactive mailbox.</span></span> 
    
- <span data-ttu-id="6eeb3-p105">Você pode copiar o conteúdo de uma caixa de correio inativa para outra caixa de correio antes de remover a retenção e excluir uma caixa de correio inativa. Para obter detalhes, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p105">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox. For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="6eeb3-p106">Se você remove a política de retenção do Office 365 ou espera de uma caixa de correio inativa e o período de retenção de caixa de correio excluída da caixa de correio tiver expirado, a caixa de correio será excluída permanentemente. Depois que ele for excluído, ela não pode ser recuperada. Antes de remover a retenção, certifique-se de que você não precisa mais o conteúdo na caixa de correio. Se você quiser reativar uma caixa de correio inativa, você pode recuperar a ele. Para obter detalhes, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p106">If you remove the hold or Office 365 retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted. After it's deleted, it can't be recovered. Before you remove the hold, be sure that you no longer need the contents in the mailbox. If you want to re-activate an inactive mailbox, you can recover it. For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="6eeb3-130">Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-130">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="6eeb3-131">Etapa 1: Identificar os bloqueios em uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="6eeb3-131">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="6eeb3-p107">Conforme indicado anteriormente, uma política de retenção de litígio, bloqueio In-loco ou Office 365 pode ser colocada em uma caixa de correio inativa. A primeira etapa é identificar os bloqueios em uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p107">As previously stated, a Litigation Hold, In-Place Hold, or Office 365 retention policy might be placed on an inactive mailbox. The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="6eeb3-134">Execute o seguinte comando para exibir as informações de espera para todas as caixas de correio inativas na sua organização.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-134">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="6eeb3-p108">O valor de **True** para a propriedade **LitigationHoldEnabled** indica que a caixa de correio inativa está em retenção de litígio. Se um bloqueio In-loco é colocado em uma caixa de correio inativa, o GUID de retenção é exibido como o valor da propriedade **InPlaceHolds** . Por exemplo, os seguintes resultados para duas caixas de correio inativas mostram que um litígio for colocado em Ann Beebe e que dois In-Place Holds são colocados em Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p108">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property. For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span></span> 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> <span data-ttu-id="6eeb3-p109">Se muita In-Place Holds é colocada em uma caixa de correio inativa, nem todos os GUIDs de bloqueio In-loco serão exibidos. Você pode executar o seguinte comando para exibir todos os GUIDs de espera a In-loco:`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p109">If a lot of In-Place Holds are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed. You can run the following command to display all the In-Place Hold GUIDs:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="6eeb3-140">Etapa 2: Remover uma isenção de uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="6eeb3-140">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="6eeb3-p110">Depois de identificar que tipo de espera é colocado na caixa de correio inativa (e se há vários bloqueios), a próxima etapa é para remover os bloqueios na caixa de correio. Conforme indicado anteriormente, você precisa remover todas as isenções para excluir permanentemente uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p110">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox. As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span> 
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="6eeb3-143">Remover um bloqueio de litígio</span><span class="sxs-lookup"><span data-stu-id="6eeb3-143">Remove a Litigation Hold</span></span>

<span data-ttu-id="6eeb3-p111">Conforme indicado anteriormente, você precisará usar o Windows PowerShell para remover um litígio de uma caixa de correio inativa. Você não pode usar o EAC. Execute o seguinte comando para remover um litígio.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p111">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the EAC. Run the following command to remove a Litigation Hold.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="6eeb3-p112">A melhor maneira de identificar uma caixa de correio inativa é usando seu valor de nome distinto ou o GUID do Exchange. Usar um desses valores ajuda a evitar a acidentalmente especificando a caixa de correio errada.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p112">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-in-place-holds"></a><span data-ttu-id="6eeb3-149">Remover retenções locais</span><span class="sxs-lookup"><span data-stu-id="6eeb3-149">Remove In-Place Holds</span></span>

 <span data-ttu-id="6eeb3-150">Há duas maneiras de remover um bloqueio In-loco de uma caixa de correio inativa:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-150">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="6eeb3-151">**Excluir o objeto de bloqueio In-loco** Se a caixa de correio inativa que você deseja excluir permanentemente a caixa de correio de origem somente para um bloqueio In-loco, você pode excluir apenas o objeto de bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-151">**Delete the In-Place Hold object** If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6eeb3-p113">Você precisa desabilitar a espera antes de excluir um objeto de bloqueio In-loco. Se você tentar excluir um objeto de bloqueio In-loco que tem a suspensão habilitada, você receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p113">You have to disable the hold before you can delete an In-Place Hold object. If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="6eeb3-154">**Remover a caixa de correio inativa como uma caixa de correio de origem de um bloqueio In-loco** Se você deseja reter outras caixas de correio de origem para um bloqueio In-loco, você pode remover a caixa de correio inativa da lista de caixas de correio de origem e manter o objeto de bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-154">**Remove the inactive mailbox as a source mailbox of an In-Place Hold** If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span> 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a><span data-ttu-id="6eeb3-155">Usar o EAC para excluir um bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="6eeb3-155">Use the EAC to delete an In-Place Hold</span></span>

1. <span data-ttu-id="6eeb3-p114">Se você souber o nome do bloqueio In-loco que você deseja excluir, você pode ir para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa que você deseja excluir permanentemente. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p114">If you know the name of the In-Place Hold that you want to delete, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="6eeb3-159">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-159">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
<span data-ttu-id="6eeb3-160"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6eeb3-160"><<<<<<< HEAD</span></span>
3. <span data-ttu-id="6eeb3-161">Selecione o bloqueio In-loco que deseja excluir e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-161">Select the In-Place Hold you want to delete, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
=======
3. <span data-ttu-id="6eeb3-p115">Selecione o bloqueio In-loco que deseja excluir e clique em **Editar**! [Ícone de edição](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p115">Select the In-Place Hold you want to delete, and then click **Edit**! [Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
>>>>>>> <span data-ttu-id="6eeb3-164">conversão de markjjo</span><span class="sxs-lookup"><span data-stu-id="6eeb3-164">markjjo-conversion</span></span>
    
4. <span data-ttu-id="6eeb3-165">Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades de página, clique em **Bloqueio In-loco**, desmarque a caixa de **conteúdo do local que corresponda a consulta de pesquisa em caixas de correio selecionadas em espera** e, em seguida, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-165">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span></span>
    
5. <span data-ttu-id="6eeb3-166">Sobre o **Descoberta eletrônica In-loco &amp; mantenha** de página, selecione o bloqueio In-loco novamente e, em seguida, clique em **Excluir**![ícone Excluir](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-166">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>
    
6. <span data-ttu-id="6eeb3-167">No aviso, clique em **Sim** para excluir o bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-167">On the warning, click **Yes** to delete the In-Place Hold.</span></span> 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a><span data-ttu-id="6eeb3-168">Use o PowerShell do Exchange Online para excluir um bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="6eeb3-168">Use Exchange Online PowerShell to delete an In-Place Hold</span></span>

1. <span data-ttu-id="6eeb3-p116">Crie uma variável que contém as propriedades de bloqueio de In-loco que você deseja excluir. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p116">Create a variable that contains the properties of the In-Place Hold that you want to delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="6eeb3-171">Desabilite a isenção em In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-171">Disable the hold on the In-Place Hold.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. <span data-ttu-id="6eeb3-172">Exclua o bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-172">Delete the In-Place Hold.</span></span>
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="6eeb3-173">Usar o EAC para remover uma caixa de correio inativa de um bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="6eeb3-173">Use the EAC to remove an inactive mailbox from an In-Place Hold</span></span>

1. <span data-ttu-id="6eeb3-p117">Se você souber o nome do In-Place Hold é colocado na caixa de correio inativa, você pode ir para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de bloqueio In-loco colocado na caixa de correio. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p117">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="6eeb3-177">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-177">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="6eeb3-178">Selecione o bloqueio In-loco que é colocado na caixa de correio inativa e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-178">Select the In-Place Hold that is placed on the inactive mailbox, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="6eeb3-179">Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades página, clique em **fontes**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-179">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span></span>
    
5. <span data-ttu-id="6eeb3-180">Na lista de caixas de correio de origem, clique no nome da caixa de correio inativa que você deseja remover e, em seguida, clique em **Remover**![ícone Remover](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-180">In the list of source mailboxes, click the name of the inactive mailbox that you want to remove, and then click **Remove**![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span></span>
    
6. <span data-ttu-id="6eeb3-p118">Clique em **Salvar** para salvar as alterações. Será exibida uma mensagem informando que a operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p118">Click **Save** to save the change. A message is displayed saying the operation was successfully completed.</span></span> 
    
7. <span data-ttu-id="6eeb3-183">Repita as etapas 1 a 6 para remover a outras retenções locais colocado na caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-183">Repeat steps 1 through 6 to remove other In-Place Holds placed on the inactive mailbox.</span></span>
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="6eeb3-184">Use o PowerShell do Exchange Online para remover uma caixa de correio inativa de um bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="6eeb3-184">Use Exchange Online PowerShell to remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="6eeb3-p119">Se o bloqueio In-loco contiver um grande número de caixas de correio de origem, é possível que a caixa de correio inativa não será listada na página **fontes** no EAC. Até 3.000 caixas de correio são exibidas na página **fontes** quando você edita um bloqueio In-loco. Se uma caixa de correio inativa não estiver listada na página **fontes** , você pode usar o PowerShell do Exchange Online para removê-lo a In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p119">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC. Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold. If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="6eeb3-p120">Crie uma variável que contém as propriedades de bloqueio In-loco colocado na caixa de correio inativa. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p120">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](delete-an-inactive-mailbox.md#step1).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="6eeb3-190">Verifique se a caixa de correio inativa está listada como uma caixa de correio de origem para o bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-190">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 
    
```
  $InPlaceHold.Sources
```

   <span data-ttu-id="6eeb3-p121">**Observação:** A propriedade de *fontes* de In-Place Hold identifica as caixas de correio de origem pelas suas propriedades *LegacyExchangeDN* . Como essa propriedade identifica exclusivamente a caixas de correio inativas, usando a propriedade *fontes* de In-Place Hold ajuda a impedir a remoção de caixa de correio errado. Isso também ajuda a evitar problemas se duas caixas de correio tiverem o mesmo alias ou o endereço SMTP.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p121">**Note:** The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties. Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox. This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 
   
3. <span data-ttu-id="6eeb3-p122">Remova a caixa de correio inativa da lista de caixas de correio de origem na variável. Certifique-se de usar o **LegacyExchangeDN** da caixa de correio inativa retornado pelo comando na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p122">Remove the inactive mailbox from the list of source mailboxes in the variable. Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. <span data-ttu-id="6eeb3-196">Verifique se a caixa de correio inativa é removida da lista de caixas de correio de origem na variável.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-196">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>
    
```
  $InPlaceHold.Sources
```

5. <span data-ttu-id="6eeb3-197">Modifica o bloqueio In-loco com a lista atualizada de caixas de correio de origem, que não inclui a caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-197">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. <span data-ttu-id="6eeb3-198">Verifique se que a caixa de correio inativa será removida da lista de caixas de correio de origem para o bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-198">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a><span data-ttu-id="6eeb3-199">Mais informações</span><span class="sxs-lookup"><span data-stu-id="6eeb3-199">More information</span></span>

- <span data-ttu-id="6eeb3-p123">**Uma caixa de correio inativa é um tipo de caixa de correio excluída.** No Exchange Online, uma caixa de correio excluída é uma caixa de correio que tenha sido excluída, mas pode ser recuperada em um período de retenção específico. O período de retenção de caixa de correio excluída no Exchange Online é 30 dias. Isso significa que a caixa de correio pode ser recuperada dentro de 30 dias do que está sendo excluída. Após 30 dias, uma caixa de correio excluída é marcada para exclusão permanente e não pode ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p123">**An inactive mailbox is a type of soft-deleted mailbox.** In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered within 30 days of being soft-deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span> 
    
- <span data-ttu-id="6eeb3-p124">**o que acontece depois de você remove a retenção em uma caixa de correio inativa?** A caixa de correio é tratada como outras caixas de correio excluída e é marcada para exclusão permanente depois que o período de retenção de caixa de correio excluída 30 dias expira. Esse período de retenção começa na data quando a caixa de correio foi feita pela primeira vez inativa. Essa data é conhecida como a data de exclusão reversível, que é a data em que a conta de usuário correspondente do Office 365 foi excluída ou quando a caixa de correio do Exchange Online foi excluída com o cmdlet **Remove-Mailbox** . A data de exclusão reversível não é a data em que você pode remover a retenção.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p124">**What happens after you remove the hold on an inactive mailbox?** The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires. This retention period starts on the date when the mailbox was first made inactive. This date is known as the soft-deleted date, which is the date the corresponding Office 365 user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet. The soft-deleted date isn't the date on which you remove the hold.</span></span> 
    
- <span data-ttu-id="6eeb3-p125">**é uma caixa de correio inativa permanentemente excluída imediatamente após a suspensão seja removida?** Se a data de exclusão reversível para uma caixa de correio inativa for mais de 30 dias, a caixa de correio não será excluída permanentemente assim que você remove a retenção. A caixa de correio será marcada para exclusão permanente e é excluída na próxima vez que ela é processada.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p125">**Is an inactive mailbox permanently deleted immediately after the hold is removed?** If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold. The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span> 
    
- <span data-ttu-id="6eeb3-p126">**Como o período de retenção de caixa de correio excluída afeta a caixas de correio inativas?** Se a data de exclusão reversível para uma caixa de correio inativa for mais de 30 dias antes da data em que a suspensão foi removida, a caixa de correio é marcada para exclusão permanente. Mas, se uma caixa de correio inativa tem uma data de exclusão reversível nos últimos 30 dias e você remove a retenção, você pode recuperar a caixa de correio até que o período de retenção de caixa de correio excluída expira. Para obter detalhes, consulte [Excluir ou restaurar caixas de correio do usuário no Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). Depois que o período de retenção de caixa de correio excluída expira, você tem siga os procedimentos para a recuperação de uma caixa de correio inativa. Para obter detalhes, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p126">**How does the soft-deleted mailbox retention period affect inactive mailboxes?** If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion. But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires. For details, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). After the soft-deleted mailbox retention period expires, you have follow the procedures for recovering an inactive mailbox. For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="6eeb3-p127">**Como você exibe informações sobre uma caixa de correio inativa depois que a suspensão seja removida?** Depois que um bloqueio seja removido e a caixa de correio inativa é revertida para uma caixa de correio excluída, ela não será retornada usando o parâmetro *InactiveMailboxOnly* com o cmdlet **Get-Mailbox** . Mas você pode exibir informações sobre a caixa de correio usando o comando **Get-Mailbox-SoftDeletedMailbox** . Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p127">**How do you display information about an inactive mailbox after the hold is removed?** After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet. But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command. For example:</span></span> 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
<span data-ttu-id="6eeb3-p128">No exemplo acima, a propriedade *WhenSoftDeleted* identifica a data de exclusão reversível, que neste exemplo é 30 de outubro de 2014. Se esta caixa de correio excluída anteriormente era uma caixa de correio inativa para o qual a suspensão foi removida, ele será permanentemente excluídos 30 dias após o valor da propriedade *WhenSoftDeleted* . Nesse caso, a caixa de correio é excluída permanentemente após 30 de novembro de 2014.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-p128">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014. If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property. In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>

