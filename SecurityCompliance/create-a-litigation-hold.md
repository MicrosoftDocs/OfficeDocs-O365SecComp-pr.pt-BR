---
title: Criar uma retenção de litígio
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: e4cb614167f89cb6e99d96aa94027ba90d86543e
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862403"
---
# <a name="create-a-litigation-hold"></a><span data-ttu-id="2af45-102">Criar uma retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="2af45-102">Create a Litigation Hold</span></span>

<span data-ttu-id="2af45-103">Você pode colocar uma caixa de correio em retenção de litígio para reter todo o conteúdo da caixa de correio, incluindo itens excluídos e as versões originais de itens modificados.</span><span class="sxs-lookup"><span data-stu-id="2af45-103">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items.</span></span> <span data-ttu-id="2af45-104">Quando você coloca uma caixa de correio de usuário em retenção de litígio, o conteúdo da caixa de correio de arquivo morto do usuário (se estiver habilitado) também é mantido.</span><span class="sxs-lookup"><span data-stu-id="2af45-104">When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained.</span></span> <span data-ttu-id="2af45-105">Ao criar uma retenção, você pode especificar uma duração de retenção (também chamada de *retenção baseada em tempo*) para que os itens excluídos e modificados sejam mantidos por um período especificado e, em seguida, excluídos permanentemente da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2af45-105">When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox.</span></span> <span data-ttu-id="2af45-106">Ou você pode simplesmente reter o conteúdo indefinidamente (chamado de *retenção infinita*) ou até que a retenção de litígio seja removida.</span><span class="sxs-lookup"><span data-stu-id="2af45-106">Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed.</span></span> <span data-ttu-id="2af45-107">Se você especificar um período de duração de retenção, ele é calculado a partir da data em que uma mensagem é recebida ou de um item de caixa de correio é criado.</span><span class="sxs-lookup"><span data-stu-id="2af45-107">If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="2af45-108">Veja o que acontece quando você cria uma retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="2af45-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="2af45-109">Os itens excluídos permanentemente pelo usuário são mantidos na pasta itens recuperáveis na caixa de correio do usuário para a duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="2af45-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="2af45-110">Os itens que são removidos da pasta itens recuperáveis pelo usuário são mantidos pela duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="2af45-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="2af45-111">A cota de armazenamento da pasta itens recuperáveis aumentou de 30 GB para 110 GB.</span><span class="sxs-lookup"><span data-stu-id="2af45-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="2af45-112">Os itens nas caixas de correio principal e de arquivo morto do usuário são mantidos</span><span class="sxs-lookup"><span data-stu-id="2af45-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="2af45-113">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="2af45-113">Before you begin</span></span>

- <span data-ttu-id="2af45-114">Para colocar uma caixa de correio do Exchange Online em retenção de litígio, é necessário atribuir uma licença do Exchange Online Plan 2.</span><span class="sxs-lookup"><span data-stu-id="2af45-114">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license.</span></span> <span data-ttu-id="2af45-115">Se uma licença do Exchange Online plano 1 for atribuída a uma caixa de correio, você precisará atribuí-la a uma licença de arquivamento do Exchange Online separada para colocá-la em espera.</span><span class="sxs-lookup"><span data-stu-id="2af45-115">If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="2af45-116">Colocar uma caixa de correio em Retenção de Litígio</span><span class="sxs-lookup"><span data-stu-id="2af45-116">Place a mailbox on Litigation Hold</span></span>

<span data-ttu-id="2af45-117">Aqui estão as etapas para colocar uma caixa de correio em retenção de litígio usando o centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="2af45-117">Here are the steps to place a mailbox on Litigation Hold using the Exchange admin center.</span></span>

1. <span data-ttu-id="2af45-118">AcEsse [https://outlook.office.com/ecp](https://outlook.office.com/ecp) e entre usando sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="2af45-118">Go to [https://outlook.office.com/ecp](https://outlook.office.com/ecp) and sign in using your global administrator account.</span></span>

2. <span data-ttu-id="2af45-119">Clique em **destinatários _GT_ caixas de correio** no painel de navegação esquerdo.</span><span class="sxs-lookup"><span data-stu-id="2af45-119">Click **Recipients > Mailboxes** in the left navigation pane.</span></span>

3. <span data-ttu-id="2af45-120">Selecione a caixa de correio que você deseja colocar em retenção de litígio e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="2af45-120">Select the mailbox that you want to place on Litigation Hold, and then click **Edit**.</span></span>

4. <span data-ttu-id="2af45-121">Na página de propriedades da caixa de correio, clique em **Recursos da Caixa de Correio**.</span><span class="sxs-lookup"><span data-stu-id="2af45-121">On the mailbox properties page, click **Mailbox features**.</span></span>
    
5. <span data-ttu-id="2af45-122">Em **Retenção de Litígio: Desativado**, clique em **Habilitar** para colocar a caixa de correio em Retenção de Litígio.</span><span class="sxs-lookup"><span data-stu-id="2af45-122">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span>
    
6. <span data-ttu-id="2af45-123">Na página **retenção de litígio** , insira as seguintes informações opcionais:</span><span class="sxs-lookup"><span data-stu-id="2af45-123">On the **Litigation hold** page, enter the following optional information:</span></span> 
    
    - <span data-ttu-id="2af45-124">**Duração da retenção de litígio (dias)** – Use esta caixa para criar uma retenção baseada em tempo e especificar quanto tempo os itens de caixa de correio devem ser mantidos quando a caixa de correio é colocada em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="2af45-124">**Litigation hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold.</span></span> <span data-ttu-id="2af45-125">A duração é calculada a partir da data em que um item de caixa de correio é recebido ou criado.</span><span class="sxs-lookup"><span data-stu-id="2af45-125">The duration is calculated from the date a mailbox item is received or created.</span></span> <span data-ttu-id="2af45-126">Quando a duração da retenção expira para um item específico, esse item não será mais preservado.</span><span class="sxs-lookup"><span data-stu-id="2af45-126">When the hold duration expires for a specific item, that item will no longer be preserved.</span></span> <span data-ttu-id="2af45-127">Se você deixar essa caixa em branco, os itens serão preservados indefinidamente ou até que a retenção seja removida.</span><span class="sxs-lookup"><span data-stu-id="2af45-127">If you leave this box blank, items are preserved indefinitely or until the hold is removed.</span></span> <span data-ttu-id="2af45-128">Use dias para especificar a duração.</span><span class="sxs-lookup"><span data-stu-id="2af45-128">Use days to specify the duration.</span></span>
    
    - <span data-ttu-id="2af45-129">**Observação** : Use esta caixa para informar ao usuário que sua caixa de correio está em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="2af45-129">**Note** - Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="2af45-130">A nota aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2af45-130">The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later.</span></span> <span data-ttu-id="2af45-131">Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook.</span><span class="sxs-lookup"><span data-stu-id="2af45-131">To access this page, users can click **File** in Outlook.</span></span>
    
    - <span data-ttu-id="2af45-132">**URL** : Use esta caixa para direcionar o usuário para um site para obter mais informações sobre a retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="2af45-132">**URL** - Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="2af45-133">Essa URL aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2af45-133">This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later.</span></span> <span data-ttu-id="2af45-134">Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook..</span><span class="sxs-lookup"><span data-stu-id="2af45-134">To access this page, users can click **File** in Outlook..</span></span>

7. <span data-ttu-id="2af45-135">Clique em **salvar** na página **retenção de litígio** e, em seguida, clique em **salvar** na página de propriedades da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2af45-135">Click **Save** on the **Litigation hold** page, and then click **Save** on the mailbox properties page.</span></span>

### <a name="create-a-litigation-hold-using-powershell"></a><span data-ttu-id="2af45-136">Criar uma retenção de litígio usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="2af45-136">Create a Litigation Hold using PowerShell</span></span>

<span data-ttu-id="2af45-137">Você também pode criar uma retenção de litígio executando o seguinte comando no [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="2af45-137">You can also create a Litigation Hold by running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $true
```

<span data-ttu-id="2af45-138">O comando anterior preserva os itens indefinidamente porque a duração da retenção não é especificada.</span><span class="sxs-lookup"><span data-stu-id="2af45-138">The previous command preserves items indefinitely because the hold duration isn't specified.</span></span> <span data-ttu-id="2af45-139">Para criar uma retenção baseada em tempo, usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="2af45-139">To created a time-based hold, using the following command:</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

<span data-ttu-id="2af45-140">Para obter mais informações, consulte [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox).</span><span class="sxs-lookup"><span data-stu-id="2af45-140">For more information, see [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox).</span></span>

## <a name="how-does-litigation-hold-work"></a><span data-ttu-id="2af45-141">Como funciona a retenção de litígio?</span><span class="sxs-lookup"><span data-stu-id="2af45-141">How does Litigation Hold work?</span></span>

<span data-ttu-id="2af45-142">No fluxo de trabalho normal de item excluído, um item de caixa de correio é movido para a subpasta Exclusões na pasta Itens recuperáveis quando um usuário o excluir permanentemente (Shift + Delete) ou o excluir da pasta Itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="2af45-142">In the normal deleted item workflow, a mailbox item is moved to the Deletions subfolder in the Recoverable Items folder when a user permanently deletes it (Shift + Delete) or deletes it from the Deleted Items folder.</span></span> <span data-ttu-id="2af45-143">Uma política de exclusão (que é uma marca de retenção configurada com uma ação de retenção de exclusão) também move itens para a subpasta Exclusões quando o período de retenção expira.</span><span class="sxs-lookup"><span data-stu-id="2af45-143">A deletion policy (which is a retention tag configured with a Delete retention action) also moves items to the Deletions subfolder when the retention period expires.</span></span> <span data-ttu-id="2af45-144">Quando um usuário descarta um item da pasta Itens recuperáveis ou quando o período de retenção do item excluído expira para um item, ele é movido para a subpasta Exclusões na pasta Itens recuperáveis e marcado para exclusão permanente.</span><span class="sxs-lookup"><span data-stu-id="2af45-144">When a user purges an item in the Recoverable Items folder or when the deleted item retention period expires for an item, it's moved to the Purges subfolder in the Recoverable Items folder and marked for permanent deletion.</span></span> <span data-ttu-id="2af45-145">Ele será excluído do Exchange na próxima vez em que a caixa de correio for processada pelo Assistente de Pasta Gerenciada (MFA).</span><span class="sxs-lookup"><span data-stu-id="2af45-145">It will be purged from Exchange the next time the mailbox is processed by the Managed Folder Assistant (MFA).</span></span>

<span data-ttu-id="2af45-p108">Quando uma caixa de correio é colocada em retenção de litígio, os itens na subpasta Exclusões são preservados durante o período especificado pela retenção de litígio. A duração da retenção é calculada a partir da data original em que um item foi recebido ou criado e define por quanto tempo os itens na subpasta Exclusões são retidos. Quando expira o período de retenção de um item na subpasta Exclusões, o item é marcado para exclusão permanente e é excluído da Exchange na próxima vez em que a caixa de correio for processada pelo MFA. Se uma caixa de correio for colocada em retenção indefinida, os itens nunca serão excluídos da subpasta Exclusões.</span><span class="sxs-lookup"><span data-stu-id="2af45-p108">When a mailbox is placed on Litigation Hold, items in the Purges subfolder are preserved for the hold duration specified by the Litigation Hold. The hold duration is calculated from the original date an item was received or created, and defines how long items in the Purges subfolder are held. When the hold duration expires for an item in the Purges subfolder, the item is marked for permanent deletion and will be purged from Exchange the next time the mailbox is processed by the MFA. If an indefinite hold is placed on a mailbox, items will never be purged from the Purges subfolder.</span></span>

<span data-ttu-id="2af45-150">A imagem a seguir mostra as subpastas nas pastas Itens Recuperáveis e o processo de fluxo de trabalho de retenção.</span><span class="sxs-lookup"><span data-stu-id="2af45-150">The following illustration shows the subfolders in the Recoverable Items folders and the hold workflow process.</span></span>

![Ciclo de vida de retenção de litígio](media/LitigationHoldLifeCycle.png)

> [!NOTE]
> <span data-ttu-id="2af45-152">Se uma retenção associada a uma ocorrência de descoberta eletrônica for colocada em uma caixa de correio, os itens excluídos serão movidos da subpasta Exclusões para a subpasta retenções quando e serão preservados até que a caixa de correio seja liberada da descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="2af45-152">If a hold associated with an eDiscovery case is placed on a mailbox, purged items are moved from the Deletions subfolder to the DiscoveryHolds subfolder and are preserved until the mailbox is released from the eDiscovery hold.</span></span>
  