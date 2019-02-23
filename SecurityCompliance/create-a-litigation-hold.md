---
title: Criar uma retenção de litígio no Office 365
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
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218651"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="676bf-102">Criar uma retenção de litígio no Office 365</span><span class="sxs-lookup"><span data-stu-id="676bf-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="676bf-p101">Você pode colocar uma caixa de correio em retenção de litígio para reter todo o conteúdo da caixa de correio, incluindo itens excluídos e as versões originais de itens modificados. Quando você coloca uma caixa de correio de usuário em retenção de litígio, o conteúdo da caixa de correio de arquivo morto do usuário (se estiver habilitado) também é mantido. Ao criar uma retenção, você pode especificar uma duração de retenção (também chamada de *retenção baseada em tempo*) para que os itens excluídos e modificados sejam mantidos por um período especificado e, em seguida, excluídos permanentemente da caixa de correio. Ou você pode simplesmente reter o conteúdo indefinidamente (chamado de *retenção infinita*) ou até que a retenção de litígio seja removida. Se você especificar um período de duração de retenção, ele é calculado a partir da data em que uma mensagem é recebida ou de um item de caixa de correio é criado.</span><span class="sxs-lookup"><span data-stu-id="676bf-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="676bf-108">Veja o que acontece quando você cria uma retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="676bf-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="676bf-109">Os itens excluídos permanentemente pelo usuário são mantidos na pasta itens recuperáveis na caixa de correio do usuário para a duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="676bf-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="676bf-110">Os itens que são removidos da pasta itens recuperáveis pelo usuário são mantidos pela duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="676bf-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="676bf-111">A cota de armazenamento da pasta itens recuperáveis aumentou de 30 GB para 110 GB.</span><span class="sxs-lookup"><span data-stu-id="676bf-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="676bf-112">Os itens nas caixas de correio principal e de arquivo morto do usuário são mantidos</span><span class="sxs-lookup"><span data-stu-id="676bf-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="676bf-113">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="676bf-113">Before you begin</span></span>

- <span data-ttu-id="676bf-p102">Para colocar uma caixa de correio do Exchange Online em retenção de litígio, é necessário atribuir uma licença do Exchange Online Plan 2. Se uma licença do Exchange Online plano 1 for atribuída a uma caixa de correio, você precisará atribuí-la a uma licença de arquivamento do Exchange Online separada para colocá-la em espera.</span><span class="sxs-lookup"><span data-stu-id="676bf-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="676bf-116">Colocar uma caixa de correio em retenção de litígio no centro de administração do Office 365</span><span class="sxs-lookup"><span data-stu-id="676bf-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="676bf-117">Aqui estão as etapas para colocar um Maibox em retenção de litígio usando o centro de administração do Office 365.</span><span class="sxs-lookup"><span data-stu-id="676bf-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="676bf-118">AcEsse https://portal.office.com/adminportal/home e entre usando sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="676bf-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="676bf-119">Clique em usuários**ativos** do painel de navegação à esquerda. \*\*\*\* > </span><span class="sxs-lookup"><span data-stu-id="676bf-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="676bf-120">Selecione o usuário cuja caixa de correio você deseja colocar em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="676bf-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="676bf-121">Na página de saída, clique em **configurações de email**e, em seguida, clique em **Editar** ao lado de **retenção de litígio**.</span><span class="sxs-lookup"><span data-stu-id="676bf-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="676bf-122">Na página **retenção de litígio** , clique no botão de alternância para ativar a retenção de litígio e conclua as seguintes configurações opcionais exibidas:</span><span class="sxs-lookup"><span data-stu-id="676bf-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    <span data-ttu-id="676bf-p103">a. **duração da retenção (dias)** : Use esta caixa para criar uma retenção baseada em tempo e especificar quanto tempo os itens de caixa de correio serão mantidos quando a caixa de correio for colocada em retenção de litígio. A duração é calculada a partir da data em que um item de caixa de correio é recebido ou criado. Se você deixar essa caixa em branco, os itens serão mantidos indefinidamente ou até que a retenção seja removida. Use dias para especificar a duração.</span><span class="sxs-lookup"><span data-stu-id="676bf-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="676bf-p104">b. **Observação** : Use esta caixa para informar ao usuário que a caixa de correio está em retenção de litígio. A nota aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook.</span><span class="sxs-lookup"><span data-stu-id="676bf-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="676bf-p105">**página da Web** c: Use esta caixa para direcionar o usuário para um site para obter mais informações sobre a retenção de litígio. Essa URL aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook.</span><span class="sxs-lookup"><span data-stu-id="676bf-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="676bf-137">Clique em **salvar** para criar a retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="676bf-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="676bf-138">Após criar a isenção, as configurações de email na página de saída mostrarão que a retenção de litígio está ativada para o usuário selecionado.</span><span class="sxs-lookup"><span data-stu-id="676bf-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

<span data-ttu-id="676bf-140">Para obter mais informações sobre como criar e gerenciar isenções de litígio e usar o PowerShell do Exchange Online para criar uma retenção de litígio em massa, consulte [colocar uma caixa de correio em retenção de litígio](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="676bf-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
