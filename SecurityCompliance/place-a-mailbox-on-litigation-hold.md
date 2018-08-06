---
title: Colocar uma caixa de correio em Retenção de Litígio
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Colocar uma caixa de correio em Retenção de Litígio também preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. '
ms.openlocfilehash: 8f440f5fc0bc7dafd639bdf8136808aa2f3bd35f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026438"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="36fe9-103">Colocar uma caixa de correio em Retenção de Litígio</span><span class="sxs-lookup"><span data-stu-id="36fe9-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="36fe9-p101">Colocar uma caixa de correio em Retenção de Litígio também preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Ao colocar a caixa de correio de um usuário em Retenção de Litígio, o conteúdo na caixa de correio de arquivo morto do usuário (se habilitada) também é colocado em retenção. Itens excluídos e modificados são preservados por um determinado período, ou até você remover a caixa de correio da Retenção de Litígio. Todos os itens da caixa de correio são retornados em uma pesquisa de [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx).</span><span class="sxs-lookup"><span data-stu-id="36fe9-p101">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items. When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold. Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold. All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="36fe9-p102">Litígio preserva itens na pasta itens recuperáveis na caixa de correio do usuário. Dependendo do número e tamanho dos itens excluídos ou modificados, o tamanho da pasta itens recuperáveis da caixa de correio pode aumentar rapidamente. A pasta itens recuperáveis é configurada com uma cota de alta por padrão. No Exchange Online, essa cota automaticamente é aumentada quando você realiza uma caixa de correio em retenção de litígio. No Exchange Server 2013, recomendamos que você monitorar caixas de correio são colocadas em retenção de litígio semanalmente para garantir que eles não alcançam os limites das cotas de itens recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p102">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox. Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly. The Recoverable Items folder is configured with a high quota by default. In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold. In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="36fe9-113">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="36fe9-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="36fe9-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-114"></span></span>

- <span data-ttu-id="36fe9-115">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="36fe9-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="36fe9-116">A configuração de Retenção de Litígio pode demorar até 60 minutos para entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="36fe9-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="36fe9-p103">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Bloqueio In-loco" no tópico [permissões de política e conformidade de mensagens](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) .</span><span class="sxs-lookup"><span data-stu-id="36fe9-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="36fe9-p104">Para colocar uma caixa de correio do Exchange Online em litígio, ele deve ser atribuído a uma licença do Exchange Online (plano 2). Se uma caixa de correio for atribuída a uma licença do Exchange Online (plano 1), você teria atribuí-lo de uma licença separada de arquivamento do Exchange Online para colocá-la em espera.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p104">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license. If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="36fe9-p105">Conforme explicado anteriormente, quando você realiza um litígio na caixa de correio do usuário, o conteúdo na caixa de correio de arquivo morto do usuário também é colocado em espera. Se você colocar um litígio em uma caixa de correio principal no local em uma implantação híbrida do Exchange, a caixa de correio de arquivamento baseado em nuvem (se ativado) também é colocada em espera.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p105">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold. If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="36fe9-p106">No Exchange Online, a cota da pasta itens recuperáveis automaticamente é aumentada para 100 GB quando você realiza uma caixa de correio em retenção de litígio. O tamanho padrão dessa pasta é 30 GB.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p106">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold. The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="36fe9-p107">Litígio preserva itens excluídos e também preserva as versões originais de itens modificados até que a suspensão seja removida. Opcionalmente, você pode especificar um período de retenção, que preserva a um item de caixa de correio para o período de tempo especificado. Se você especificar uma período de duração de espera, ele é calculado a partir da data de uma mensagem é recebida ou um item de caixa de correio é criado. Para preservar itens que atendam aos critérios especificados, use um bloqueio In-loco para criar uma pausa baseado em consulta. Para obter detalhes, consulte [criar ou remover um bloqueio In-loco](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span><span class="sxs-lookup"><span data-stu-id="36fe9-p107">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed. You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period. If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created. To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold. For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="36fe9-p108">Para usar o Shell para colocar uma caixa de correio do Exchange Online em espera, você precisa usar o PowerShell do Exchange Online. Para obter mais informações, consulte [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="36fe9-p108">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell. For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="36fe9-p109">Não há suporte para colocar uma Retenção de Litígio em uma caixa de correio de pasta pública. Você precisa usar o Bloqueio In-loco para colocar uma retenção em pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p109">Placing a Litigation Hold on a public folder mailbox isn't supported. You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="36fe9-134">Usar o EAC para colocar uma caixa de correio em retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="36fe9-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="36fe9-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-135"></span></span>

1. <span data-ttu-id="36fe9-136">Acesse **Destinatários** \> **Caixas de Correio**.</span><span class="sxs-lookup"><span data-stu-id="36fe9-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="36fe9-137">Na lista de caixas de correio de usuários, clique na caixa de correio para a qual você deseja habilitar ou desabilitar a Retenção de Litígio e clique em **Editar**![Ícone de edição](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="36fe9-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="36fe9-138">Na página de propriedades da caixa de correio, clique em **recursos de caixa de correio.**</span><span class="sxs-lookup"><span data-stu-id="36fe9-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="36fe9-139">Em **Retenção de Litígio: Desativado**, clique em **Habilitar** para colocar a caixa de correio em Retenção de Litígio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="36fe9-140">Na página **de Litígio**, insira as seguintes informações opcionais.</span><span class="sxs-lookup"><span data-stu-id="36fe9-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="36fe9-p110">**Duração da retenção de litígio (dias)** Use esta caixa para especificar por quanto tempo os itens da caixa de correio devem ser mantidos quando esta estiver em Retenção de Litígio. A duração é calculada a partir da data em que um item de caixa de correio é recebido ou criado. Se você deixar esta caixa em branco, os itens serão mantidos indefinidamente ou até que a retenção seja removida. Use dias para especificar a duração.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="36fe9-p111">**Observação** Use esta caixa para informar ao usuário que suas caixas de correio está em retenção de litígio. A nota será exibida na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p111">**Note** Use this box to inform the user their mailbox is on Litigation Hold. The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="36fe9-p112">**URL** Use esta caixa para direcionar o usuário para um site para obter mais informações sobre retenção de litígio. Essa URL aparecerá na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p112">**URL** Use this box to direct the user to a website for more information about Litigation Hold. This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="36fe9-149">Clique em **Salvar** na página **Retenção de Litígio** e, em seguida, clique em **Salvar** na página de propriedades da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="36fe9-150">Usar o Shell para colocar uma caixa de correio em Retenção de Litígio indefinidamente</span><span class="sxs-lookup"><span data-stu-id="36fe9-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="36fe9-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-151"></span></span>

<span data-ttu-id="36fe9-p113">Este exemplo coloca a caixa de correio bsuneja@contoso.com em Retenção de Litígio. Os itens na caixa de correio serão retidos indefinidamente ou até que a retenção seja removida.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="36fe9-154">Quando você coloca uma caixa de correio em retenção de litígio indefinidamente (ao não especificar um período de duração), o valor da propriedade  _LitigationHoldDuration_ é definido como  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="36fe9-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="36fe9-155">Usar o Shell para colocar uma caixa de correio em Retenção de Litígio e preservar itens por um período específico</span><span class="sxs-lookup"><span data-stu-id="36fe9-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="36fe9-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-156"></span></span>

<span data-ttu-id="36fe9-157">Este exemplo coloca a caixa de correio bsuneja@contoso.com em Retenção de Litígio e preserva itens por 2555 dias (aproximadamente sete anos).</span><span class="sxs-lookup"><span data-stu-id="36fe9-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="36fe9-158">Usar o Shell para colocar todas as caixas de correio em Retenção de Litígio por um período específico</span><span class="sxs-lookup"><span data-stu-id="36fe9-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="36fe9-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-159"></span></span>

<span data-ttu-id="36fe9-p114">A sua organização pode exigir que todos os dados de caixas de correio sejam preservados durante um período específico. Antes de colocar todas as caixas de correio de uma organização em Retenção de Litígio, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="36fe9-p114">Your organization may require that all mailbox data be preserved for a specific period of time. Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="36fe9-162">Este exemplo coloca todas as caixas de correio de usuários na organização em Retenção de Litígio por um ano (365 dias).</span><span class="sxs-lookup"><span data-stu-id="36fe9-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="36fe9-163">O exemplo usa o cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx)para recuperar todas as caixas de correio na organização, especifica um filtro de destinatários para incluir todas as caixas de correio de usuários e, então, envia essa lista ao cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) para ativar a Retenção de Litígio e definir a duração da retenção. </span><span class="sxs-lookup"><span data-stu-id="36fe9-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="36fe9-164">Para aplicar uma retenção indefinida a todas as caixas de correio de usuários, execute o comando anterior, mas não inclua o parâmetro  _LitigationHoldDuration_.</span><span class="sxs-lookup"><span data-stu-id="36fe9-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="36fe9-165">Consulte a seção [Mais informações](#moreinfo.md) para obter exemplos de como usar outras propriedades de destinatários em um filtro para incluir ou excluir uma ou mais caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="36fe9-166">Usar o Shell para remover a Retenção de Litígio de uma caixa de correio </span><span class="sxs-lookup"><span data-stu-id="36fe9-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="36fe9-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-167"></span></span>

<span data-ttu-id="36fe9-168">Este exemplo remove a Retenção de Litígio da caixa de correio bsuneja@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="36fe9-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="36fe9-169">M</span><span class="sxs-lookup"><span data-stu-id="36fe9-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="36fe9-170">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="36fe9-170">How do you know this worked?</span></span>
<span data-ttu-id="36fe9-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-171"></span></span>

<span data-ttu-id="36fe9-172">Para verificar se você aplicou com sucesso a Retenção de Litígio em uma caixa de correio, faça um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="36fe9-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="36fe9-173">No EAC:</span><span class="sxs-lookup"><span data-stu-id="36fe9-173">In the EAC:</span></span>
    
1. <span data-ttu-id="36fe9-174">Acesse **Destinatários** \> **Caixas de Correio**.</span><span class="sxs-lookup"><span data-stu-id="36fe9-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="36fe9-175">Na lista de caixas de correio de usuários, clique na caixa de correio para a qual deseja verificar as configurações de Retenção de Litígio e clique em **Editar**![Ícone de edição](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="36fe9-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="36fe9-176">Na página de propriedades da caixa de correio, clique em **recursos de caixa de correio.**</span><span class="sxs-lookup"><span data-stu-id="36fe9-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="36fe9-177">Em **Retenção de Litígio**, verifique se a retenção está habilitada.</span><span class="sxs-lookup"><span data-stu-id="36fe9-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="36fe9-p115">Clique em **Exibir detalhes** para verificar quando a caixa de correio foi colocada em retenção de litígio e por quem. Você também pode verificar ou alterar os valores nas caixas opcionais **Duração da retenção de litígio (dias)**, **Observação** e **URL**.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="36fe9-180">No Shell, execute um destes comandos:</span><span class="sxs-lookup"><span data-stu-id="36fe9-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="36fe9-181">ou</span><span class="sxs-lookup"><span data-stu-id="36fe9-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="36fe9-182">Se uma caixa de correio é colocada em Retenção de Litígio indefinidamente, o valor da propriedade  _LitigationHoldDuration_ é definido como  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="36fe9-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="36fe9-183">Mais informações</span><span class="sxs-lookup"><span data-stu-id="36fe9-183">More information</span></span>
<span data-ttu-id="36fe9-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="36fe9-184"></span></span>

- <span data-ttu-id="36fe9-185">Se sua organização exige que todos os dados da caixa de correio sejam preservados por um período específico de tempo, considere o seguinte antes de colocar todas as caixas de correio da organização em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="36fe9-p116">Quando você usa o comando anterior para colocar uma retenção em todas as caixas de correio em uma organização (ou um subconjunto de caixas de correio que correspondem a um filtro de destinatário especificado) somente caixas de correio que existem no momento em que você executar o comando são colocadas em retenção. Se você criar novas caixas de correio posteriormente, execute o comando mais uma vez para colocá-las em retenção. Caso crie novas caixas de correio com frequência, você pode executar o comando como uma tarefa agendada com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="36fe9-p117">Colocação de todas as caixas de correio em retenção de litígio pode afetar significativamente o tamanho das caixas postais. Em uma organização do Exchange Server 2013, planeje armazenamento suficiente atender aos requisitos de preservação da sua organização.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p117">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes. In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="36fe9-p118">A pasta itens recuperáveis tem seu próprio limite de armazenamento, portanto não são considerados itens na pasta rumo ao limite de armazenamento de caixa de correio. Conforme explicado anteriormente, a preservação de dados de caixa de correio por um longo período de tempo resultar em crescimento da pasta itens recuperáveis na caixa de correio do usuário e arquivamento. Para acomodar esse aumento no Exchange Online, a cota da pasta itens recuperáveis é automaticamente aumentou de 30 GB para 100 GB quando você realiza uma caixa de correio em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p118">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit. As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive. To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="36fe9-p119">No Exchange Server 2013, o limite de armazenamento padrão para a pasta itens recuperáveis também é 30 GB. Recomendamos que você deseja monitorar periodicamente o tamanho dessa pasta para garantir que ele não atinge o limite. Para obter mais informações, consulte a [Pasta itens recuperáveis](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="36fe9-p119">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB. We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit. For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="36fe9-p120">O comando anterior coloca uma retenção em todas as caixas de correio usando um filtro de destinatário que retorna todas as caixas de correio. Você pode usar outras propriedades de destinatário para obter uma lista de caixas de correio específicas, que você pode, então, enviar ao cmdlet **Set-Mailbox** para colocar uma Retenção de Litígio nessas caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="36fe9-p121">Eis alguns exemplos de usar os cmdlets **Get-Mailbox** e **Get-Recipient** para obter um subconjunto de caixas de correio com base em propriedades de usuário ou de caixa de correio comuns. Esses exemplos supõem que as propriedades de caixa de correio relevantes (como  _CustomAttributeN_ ou  _Department_) foram preenchidas.</span><span class="sxs-lookup"><span data-stu-id="36fe9-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    <span data-ttu-id="36fe9-p122">Você pode usar outras propriedades de caixa de correio em um filtro para incluir ou excluir caixas de correio. Para saber mais, confira [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="36fe9-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

