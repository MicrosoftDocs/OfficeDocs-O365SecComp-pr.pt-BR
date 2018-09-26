---
title: Criar um litígio no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037954"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="0c964-102">Criar um litígio no Office 365</span><span class="sxs-lookup"><span data-stu-id="0c964-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="0c964-p101">Você pode colocar uma caixa de correio em retenção de litígio para reter todo o conteúdo de caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Quando você realiza uma caixa de correio do usuário na retenção de litígio, conteúdo, na caixa de correio de arquivo morto do usuário (se ele estiver habilitado) também é mantido. Quando você cria uma pausa, você pode especificar uma duração de espera (também chamada de uma *baseadas em tempo de espera*) para que excluído e itens modificados são mantidos por um período especificado e excluídos permanentemente da caixa de correio. Ou você pode apenas reter conteúdo indefinidamente (chamado uma *espera infinita*) ou até que a retenção de litígio foi removida. Se você especificar uma período de duração de espera, ele é calculado a partir da data de uma mensagem é recebida ou um item de caixa de correio é criado.</span><span class="sxs-lookup"><span data-stu-id="0c964-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="0c964-108">Aqui está o que acontece quando você cria um litígio.</span><span class="sxs-lookup"><span data-stu-id="0c964-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="0c964-109">Itens que são excluídos permanentemente pelo usuário são mantidos na pasta itens recuperáveis na caixa de correio do usuário para a duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="0c964-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="0c964-110">Itens que são removidos da pasta itens recuperáveis pelo usuário são retidos para a duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="0c964-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="0c964-111">A cota de armazenamento para a pasta itens recuperáveis é aumentada de 30 GB para 110 GB.</span><span class="sxs-lookup"><span data-stu-id="0c964-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="0c964-112">Itens em primário do usuário e as caixas de correio de arquivo morto são mantidos</span><span class="sxs-lookup"><span data-stu-id="0c964-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="0c964-113">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="0c964-113">Before you begin</span></span>

- <span data-ttu-id="0c964-p102">Para colocar uma caixa de correio do Exchange Online em litígio, ele deve ser atribuído a uma licença do Exchange Online plano 2. Se uma caixa de correio for atribuída a uma licença do Exchange Online plano 1, você teria atribuí-lo de uma licença separada de arquivamento do Exchange Online para colocá-la em espera.</span><span class="sxs-lookup"><span data-stu-id="0c964-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="0c964-116">Colocar uma caixa de correio em retenção de litígio no Centro de administração do Office 365</span><span class="sxs-lookup"><span data-stu-id="0c964-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="0c964-117">Aqui estão as etapas para colocar um maibox em retenção de litígio usando o Centro de administração do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0c964-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="0c964-118">Vá para https://portal.office.com/adminportal/home e entrar usando sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="0c964-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="0c964-119">Clique em **usuários** > **usuários ativos** no painel de navegação à esquerda.</span><span class="sxs-lookup"><span data-stu-id="0c964-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="0c964-120">Selecione o usuário cuja caixa de correio que você deseja colocar em retenção de litígio.</span><span class="sxs-lookup"><span data-stu-id="0c964-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="0c964-121">Na página dinamicamente-out, clique em **configurações de email**e clique em **Editar** ao lado de **litígio**.</span><span class="sxs-lookup"><span data-stu-id="0c964-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="0c964-122">Na página de **litígio** , clique na alternância para ativar litígio e concluir as seguintes configurações opcionais que são exibidas:</span><span class="sxs-lookup"><span data-stu-id="0c964-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1.PNG](media/O365-LitigationHold1.png)

    <span data-ttu-id="0c964-p103">r. **duração da retenção (dias)** -Use esta caixa para criar uma pausa baseadas em tempo e especifique por quanto tempo os itens de caixa de correio são mantidos quando a caixa de correio for colocada em retenção de litígio. A duração é calculada a partir da data de um item de caixa de correio é recebido ou criado. Se você deixar essa caixa em branco, os itens são mantidos indefinidamente ou até que a suspensão seja removida. Use dias para especificar a duração.</span><span class="sxs-lookup"><span data-stu-id="0c964-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="0c964-p104">b. **Nota** - Use esta caixa para informar ao usuário suas caixas de correio está em retenção de litígio. A nota será exibida na página informações da conta na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior. Para acessar esta página, os usuários podem clicar o **arquivo** no Outlook.</span><span class="sxs-lookup"><span data-stu-id="0c964-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="0c964-p105">c. a **página da Web** - Use esta caixa para direcionar o usuário para um site para obter mais informações sobre retenção de litígio. Essa URL aparece na página informações da conta na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior. Para acessar esta página, os usuários podem clicar o **arquivo** no Outlook.</span><span class="sxs-lookup"><span data-stu-id="0c964-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="0c964-137">Clique em **Salvar** para criar o litígio.</span><span class="sxs-lookup"><span data-stu-id="0c964-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="0c964-138">Depois de criar a retenção, as configurações de email na página dinamicamente-out mostra que litígio esteja ativado para o usuário selecionado.</span><span class="sxs-lookup"><span data-stu-id="0c964-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2.PNG](media/O365-LitigationHold2.png)

<span data-ttu-id="0c964-140">Para obter mais informações sobre como criar e gerenciar retenções de litígio e usando o PowerShell do Exchange Online para criação em massa litígio contém, consulte [colocar uma caixa de correio em retenção de litígio](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="0c964-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
