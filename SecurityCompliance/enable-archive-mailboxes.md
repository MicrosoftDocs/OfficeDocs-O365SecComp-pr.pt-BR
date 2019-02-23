---
title: Habilitar caixas de correio de arquivo morto no centro &amp; de conformidade de segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Use o centro de conformidade &amp; de segurança do Office 365 para habilitar caixas de correio de arquivo morto para suportar a retenção de mensagens, os requisitos de descoberta eletrônica e de bloqueio da sua organização.
ms.openlocfilehash: 10e20d09c531d6758d8011030aea64a6c30cdf9b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217281"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="73da0-103">Habilitar caixas de correio de arquivo morto no centro &amp; de conformidade de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="73da0-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="73da0-p101">O arquivamento no Office 365 (também chamado de arquivamento in-loco) fornece aos usuários espaço de armazenamento adicional de caixa de correio. Depois de ativar as caixas de correio de arquivo morto, os usuários podem acessar e armazenar mensagens em suas caixas de correio de arquivo morto usando o Microsoft Outlook e o Outlook na Web (anteriormente conhecido como Outlook Web App). Os usuários também podem mover ou copiar mensagens entre a caixa de correio principal e a caixa de correio de arquivo morto. Eles também podem recuperar itens excluídos da pasta itens recuperáveis em suas caixas de correio de arquivo morto usando a ferramenta recuperar itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="73da0-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App). Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="73da0-p102">O Office 365 fornece uma quantidade ilimitada de armazenamento de arquivos com o recurso de arquivamento de expansão automática. Quando o arquivamento de expansão automática está ativado e, em seguida, a cota de armazenamento inicial na caixa de correio de arquivo morto de um usuário é atingida, o Office 365 adiciona automaticamente espaço de armazenamento adicional. Isso significa que os usuários não ficarão sem espaço de armazenamento de caixa de correio e você não precisará gerenciar nada depois de habilitar inicialmente a caixa de correio de arquivo morto e ativar o arquivamento de expansão automática para sua organização. Para obter mais informações, consulte [Overview of Unlimited Archiving in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="73da0-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="73da0-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="73da0-112">Before you begin</span></span>

<span data-ttu-id="73da0-p103">Você precisa receber a função de destinatários de email no Exchange Online para habilitar ou desabilitar caixas de correio de arquivo morto. Por padrão, essa função é atribuída aos grupos de função gerenciamento de destinatários e gerenciamento de organização na página **permissões** no centro de administração do Exchange. Se você não vir a página **arquivo morto** no centro &amp; de conformidade de segurança, peça ao administrador para atribuir as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="73da0-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="73da0-116">Habilitar uma caixa de correio de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="73da0-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="73da0-117">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="73da0-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="73da0-118">Entre no Office 365 usando a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="73da0-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="73da0-119">No painel esquerdo do centro de conformidade &amp; de segurança, clique em arquivamento de **governança** \> \*\*\*\* de dados.</span><span class="sxs-lookup"><span data-stu-id="73da0-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="73da0-p104">A página **Arquivo Morto** é exibida. A coluna **Caixa de correio de arquivo morto** indica se uma caixa de correio de arquivo morto está habilitada ou desabilitada para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="73da0-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="73da0-122">Na lista de caixas de correio, selecione o usuário para o qual você deseja habilitar a caixa de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Clique em habilitar no painel de detalhes do usuário selecionado para habilitar a caixa de correio de arquivo morto](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="73da0-124">No painel de detalhes do usuário selecionado, clique em **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="73da0-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="73da0-p105">Um aviso é exibido dizendo que se você habilitar a caixa de correio de arquivo morto, os itens da caixa de correio do usuário mais antigos do que a política de arquivamento atribuída à caixa de correio serão movidos para a nova caixa de correio de arquivo morto. A política de arquivo morto padrão que faz parte da política de retenção atribuída às caixas de correio do Exchange Online transfere itens para a caixa de correio de arquivo morto dois anos após a data em que o item foi entregue à caixa de correio ou criado pelo usuário. Para obter mais informações, consulte a seção **mais** informações neste artigo.</span><span class="sxs-lookup"><span data-stu-id="73da0-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="73da0-128">Clique em **Sim** para habilitar a caixa de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="73da0-p106">Pode levar alguns momentos para criar a caixa de correio de arquivo morto. Quando ele é criado, a **caixa de correio de arquivo morto: habilitada** é exibida no painel de detalhes para o usuário selecionado. Talvez seja necessário clicar em **Atualizar** ![ícone](media/O365-MDM-Policy-RefreshIcon.gif) de atualização para atualizar as informações no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="73da0-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="73da0-p107">Você pode também habilitar caixas de correio de arquivo morto em massa, selecionando vários usuários com caixas de correio de arquivo morto (use as teclas Shift ou Ctrl). Depois de selecionar várias caixas de correio, clique em **Habilitar** no painel de detalhes. </span><span class="sxs-lookup"><span data-stu-id="73da0-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="73da0-134">Desabilitar uma caixa de correio de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="73da0-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="73da0-p108">Você também pode usar a página **arquivo morto** no centro &amp; de conformidade de segurança para desabilitar a caixa de correio de arquivo morto de um usuário. Após desabilitar uma caixa de correio de arquivo morto, você poderá reconectá-la à caixa de correio principal do usuário dentro de 30 dias de desabilitá-la. Nesse caso, o conteúdo original da caixa de correio de arquivo morto é restaurado. Após 30 dias, o conteúdo da caixa de correio de arquivo morto original é excluído permanentemente e não pode ser recuperado. Portanto, se você reabilitar o arquivo morto mais de 30 dias após desabilitá-lo, uma nova caixa de correio de arquivo morto será criada.</span><span class="sxs-lookup"><span data-stu-id="73da0-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="73da0-p109">Observe que a política de arquivo morto padrão atribuída às caixas de correio dos usuários move itens para a caixa de correio de arquivo morto dois anos após a data em que o item é entregue. Se você desabilitar a caixa de correio de arquivo morto de um usuário, nenhuma ação será realizada nos itens de caixa de correio e ela permanecerá na caixa de correio principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="73da0-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="73da0-142">Para desabilitar uma caixa de correio de arquivo morto:</span><span class="sxs-lookup"><span data-stu-id="73da0-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="73da0-143">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="73da0-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="73da0-144">Entre no Office 365 usando a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="73da0-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="73da0-145">No painel esquerdo do centro de conformidade &amp; de segurança, clique em arquivamento de **governança** \> \*\*\*\* de dados.</span><span class="sxs-lookup"><span data-stu-id="73da0-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="73da0-p110">A página **Arquivo Morto** é exibida. A coluna **Caixa de correio de arquivo morto** indica se uma caixa de correio de arquivo morto está habilitada ou desabilitada para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="73da0-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="73da0-148">Na lista de caixas de correio, selecione o usuário para o qual você deseja habilitar a caixa de correio arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="73da0-149">No painel de detalhes, clique em **Desabilitar**.</span><span class="sxs-lookup"><span data-stu-id="73da0-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="73da0-150">Uma mensagem de aviso é exibida dizendo que você terá 30 dias para reabilitar a caixa de correio de arquivo morto e, após 30 dias, todas as informações no arquivo morto serão excluídas permanentemente.</span><span class="sxs-lookup"><span data-stu-id="73da0-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="73da0-151">Clique em **Sim** para desabilitar a caixa de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="73da0-p111">Pode levar alguns instantes para desabilitar a caixa de correio de arquivo morto. Quando estiver desabilitada, **caixa de correio de arquivo morto: Disabled** será exibido no painel de detalhes para o usuário selecionado. Talvez seja necessário clicar em **Atualizar** ![ícone](media/O365-MDM-Policy-RefreshIcon.gif) de atualização para atualizar as informações no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="73da0-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="73da0-p112">Você pode também desabilitar caixas de correio de arquivo morto em massa, selecionando vários usuários com caixas de correio de arquivo morto (use as teclas Shift ou Ctrl). Depois de selecionar várias caixas de correio, clique em **Desabilitar** no painel de detalhes. </span><span class="sxs-lookup"><span data-stu-id="73da0-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="73da0-157">Usar o PowerShell do Exchange Online para habilitar ou desabilitar caixas de correio de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="73da0-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="73da0-p113">Você também pode usar o PowerShell do Exchange Online para habilitar caixas de correio de arquivo morto. O principal motivo para usar o PowerShell é que você pode habilitar rapidamente a caixa de correio de arquivo morto para todos os usuários em sua organização.</span><span class="sxs-lookup"><span data-stu-id="73da0-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="73da0-p114">A primeira etapa é conectar-se ao PowerShell do Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="73da0-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="73da0-162">Depois de se conectar ao Exchange Online, você pode executar os comandos nas seções a seguir para habilitar ou desabilitar caixas de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="73da0-163">Habilitar caixas de correio de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="73da0-163">Enable archive mailboxes</span></span>

<span data-ttu-id="73da0-164">Execute o seguinte comando para habilitar a caixa de correio de arquivo morto para um único usuário.</span><span class="sxs-lookup"><span data-stu-id="73da0-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="73da0-165">Execute o seguinte comando para habilitar a caixa de correio de arquivo morto para todos os usuários em sua organização (cuja caixa de correio de arquivo morto não está habilitada no momento).</span><span class="sxs-lookup"><span data-stu-id="73da0-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="73da0-166">Desabilitar caixas de correio de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="73da0-166">Disable archive mailboxes</span></span>

<span data-ttu-id="73da0-167">Execute o seguinte comando para desabilitar a caixa de correio de arquivo morto para um único usuário.</span><span class="sxs-lookup"><span data-stu-id="73da0-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="73da0-168">Execute o seguinte comando para desabilitar a caixa de correio de arquivo morto para todos os usuários em sua organização (cuja caixa de correio de arquivo morto está habilitada no momento).</span><span class="sxs-lookup"><span data-stu-id="73da0-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="73da0-169">Mais informações</span><span class="sxs-lookup"><span data-stu-id="73da0-169">More information</span></span>
  
- <span data-ttu-id="73da0-p115">As caixas de correio de arquivo morto ajudam você e seus usuários a atender aos requisitos de retenção, eDiscovery e bloqueio da sua organização. Por exemplo, você pode usar a política de retenção do Exchange da sua organização para mover o conteúdo da caixa de correio para a caixa de correio de arquivo morto dos usuários. Ao usar a ferramenta de pesquisa de conteúdo no centro &amp; de conformidade de segurança para pesquisar conteúdo específico na caixa de correio de um usuário, a caixa de correio de arquivo morto do usuário também será pesquisada. E, quando você coloca uma retenção de litígio ou aplica uma política de retenção do Office 365 à caixa de correio de um usuário, os itens na caixa de correio de arquivo morto também são mantidos.</span><span class="sxs-lookup"><span data-stu-id="73da0-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="73da0-p116">Quando uma caixa de correio de arquivo morto está habilitada, os usuários podem armazenar mensagens em suas caixas de correio de arquivo morto. Os usuários podem acessar suas caixas de correio de arquivo morto usando o Microsoft Outlook e o Outlook na Web. Usando qualquer um desses aplicativos cliente, os usuários podem exibir mensagens em suas caixas de correio de arquivo morto e mover ou copiar mensagens entre a caixa de correio principal e a caixa de correio de arquivo morto. Os usuários também podem recuperar itens excluídos da pasta itens recuperáveis em suas caixas de correio de arquivo morto usando a ferramenta recuperar itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="73da0-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="73da0-p117">Após as caixas de correio de arquivo morto serem habilitadas, sua organização pode aproveitar a política de retenção padrão do Exchange (também chamada de gerenciamento de registros de mensagens ou política de MRM) que é atribuída automaticamente a cada caixa de correio. Quando uma caixa de correio de arquivo morto está habilitada, a política de retenção padrão do Exchange faz automaticamente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="73da0-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="73da0-180">Move os itens que têm dois anos ou mais da caixa de correio principal do usuário para suas caixas de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="73da0-181">Move os itens que têm 14 dias ou mais da pasta Itens Recuperáveis na caixa de correio principal do usuário para a pasta Itens Recuperáveis nas caixas de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="73da0-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="73da0-182">Para obter mais informações sobre caixas de correio de arquivo morto e políticas de retenção do Exchange, consulte:</span><span class="sxs-lookup"><span data-stu-id="73da0-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="73da0-183">Marcas e políticas de retenção</span><span class="sxs-lookup"><span data-stu-id="73da0-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="73da0-184">Política de retenção padrão no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="73da0-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="73da0-185">Configurar uma política de arquivo morto e exclusão para caixas de correio em sua organização do Office 365</span><span class="sxs-lookup"><span data-stu-id="73da0-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
