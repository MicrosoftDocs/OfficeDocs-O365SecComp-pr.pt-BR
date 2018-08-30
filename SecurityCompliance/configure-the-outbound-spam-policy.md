---
title: Configurar a política de spam de saída
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
description: A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados.
ms.openlocfilehash: b6185cfded28613cb5a512882aefb1a99db158db
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002397"
---
# <a name="configure-the-outbound-spam-policy"></a><span data-ttu-id="e8eb1-103">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="e8eb1-103">Configure the outbound spam policy</span></span>

<span data-ttu-id="e8eb1-p101">A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados. Semelhante a filtragem de entrada, a filtragem de spam de saída é composta de filtragem de conexão e de conteúdo, porém, as configurações do filtro de saída não são configuráveis. Se uma mensagem de saída é considerada spam, ela é roteada através do pool de entrega de risco mais alto, que reduz a probabilidade do pool de IP de saída normal estar sendo adicionado a uma lista de bloqueio. Se um cliente continua a enviar spam de saída através do serviço, será impedido de enviar mensagens. Embora a filtragem de spam de saída não possa ser desabilitada nem modificada, você pode configurar várias configurações de spam de saída para toda a empresa por meio da política padrão de spam de saída.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p101">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients. Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable. If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list. If a customer continues to send outbound spam through the service, they will be blocked from sending messages. Although outbound spam filtering cannot be disabled or changed, you can configure several company-wide outbound spam settings via the default outbound spam policy.</span></span> 
  
<span data-ttu-id="e8eb1-109">O vídeo a seguir mostra como configurar a política de spam de saída:</span><span class="sxs-lookup"><span data-stu-id="e8eb1-109">The following video shows how to configure the outbound spam policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e8eb1-110">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="e8eb1-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="e8eb1-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="e8eb1-111"></span></span>

<span data-ttu-id="e8eb1-112">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="e8eb1-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="e8eb1-p102">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a "entrada de antispam no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="e8eb1-115">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-115">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
<span data-ttu-id="e8eb1-p103">O procedimento a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) para examinar suas configurações e o [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) para editar as configurações de política de spam de saída. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p103">The following procedure can also be performed via remote PowerShell. Use the [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet to review your settings, and the [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) to edit your outbound spam policy settings. To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a><span data-ttu-id="e8eb1-120">Utilize o EAC para editar a política de spam de saída padrão</span><span class="sxs-lookup"><span data-stu-id="e8eb1-120">Use the EAC to edit the default outbound spam policy</span></span>
<span data-ttu-id="e8eb1-121"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="e8eb1-121"></span></span>

<span data-ttu-id="e8eb1-122">Utilize o procedimento a seguir para editar a política de spam de saída padrão.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-122">Use the following procedure to edit the default outbound spam policy:</span></span>
  
### <a name="to-configure-the-default-outbound-spam-policy"></a><span data-ttu-id="e8eb1-123">Para configurar a política de spam de saída padrão.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-123">To configure the default outbound spam policy</span></span>

1. <span data-ttu-id="e8eb1-124">No centro de administração do Exchange (EAC), navegue até **Proteção** \> **Spam de saída**, e, em seguida clique duas vezes em política padrão.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-124">In the Exchange admin center (EAC), navigate to **Protection** \> **Outbound spam**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="e8eb1-125">Selecione a opção de menu **Preferências de saída de spam**.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-125">Select the **Outbound spam preferences** menu option.</span></span> 
    
3. <span data-ttu-id="e8eb1-126">Marque as seguintes caixas de seleção referentes às mensagens de saída e, em seguida, especifique um endereço de email associado ou endereços na caixa de entrada associada (elas podem ser listas de distribuição se forem resolvidas como destinos SMTP válidos):</span><span class="sxs-lookup"><span data-stu-id="e8eb1-126">Select the following check boxes pertaining to outbound messages, and then specify an associated email address or addresses in the accompanying input box (these can be distribution lists if they resolve as valid SMTP destinations):</span></span>
    
1. <span data-ttu-id="e8eb1-p104">Envie uma cópia de todas as mensagens suspeitas de email de saída para **o(s) seguinte(s) endereço(s) de email**. Estas são as mensagens que são marcadas como spam pelo filtro (independentemente da classificação de SCL) Elas não são rejeitadas pelo filtro, mas são roteadas pelo pool de entrega de risco mais alto. Separe com ponto e vírgula os diversos endereços. Observe que os destinatários especificados receberão as mensagens como um endereço com cópia oculta (Bcc) (os campos De e Para são o remetente e o destinatário originais).</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p104">**Send a copy of all suspicious outbound email messages to the following email address or addresses**. These are messages that are marked as spam by the filter (regardless of the SCL rating). They are not rejected by the filter but are routed through the higher risk delivery pool. Separate multiple addresses with a semicolon. Note that the recipients specified will receive the messages as a Blind carbon copy (Bcc) address (the From and To fields are the original sender and recipient).</span></span>
    
2. <span data-ttu-id="e8eb1-p105">Envie uma notificação para o seguinte endereço de email quando um remetente for bloqueado por enviar **spam de saída**. Separe com ponto e vírgula os diversos endereços.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p105">**Send a notification to the following email address when a sender is blocked sending outbound spam**. Separate multiple addresses with a semicolon.</span></span>
    
    <span data-ttu-id="e8eb1-p106">Quando uma quantidade significativa de spam é provenientes de um usuário específico, o usuário está desabilitado enviem mensagens de email. O administrador do domínio, que é especificado usando essa configuração, será informado que mensagens de saída são bloqueadas para esse usuário. Para ver qual essa notificação aparência, consulte [notificação de amostra quando um remetente for bloqueado enviem spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Para obter informações sobre a obtenção reabilitado, consulte [Remover um usuário, o domínio ou o endereço IP a partir de uma lista de bloqueios após o envio de mensagens de spam](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p106">When a significant amount of spam is originating from a particular user, the user is disabled from sending email messages. The administrator for the domain, who is specified using this setting, will be informed that outbound messages are blocked for this user. To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>
    
4. <span data-ttu-id="e8eb1-p107">Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="e8eb1-p107">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="e8eb1-140">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="e8eb1-140">For more information</span></span>
<span data-ttu-id="e8eb1-141"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="e8eb1-141"></span></span>

[<span data-ttu-id="e8eb1-142">Pool de alto risco de entrega para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="e8eb1-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)
  
[<span data-ttu-id="e8eb1-143">Perguntas frequentes sobre a proteção antispam</span><span class="sxs-lookup"><span data-stu-id="e8eb1-143">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

