---
title: Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: Você pode criar uma regra de transporte que define o nível de confiança de spam (SCL) de uma mensagem de email. O SCL é que uma medida de uma mensagem como provavelmente é spam. Spam é mensagens de email não solicitadas (e normalmente indesejadas). O serviço age diferentes em uma mensagem, dependendo de sua classificação do SCL. Por exemplo, você talvez queira ignorar spam filtragem de conteúdo de mensagens que são enviadas de pessoas dentro da organização, pois você confia que uma mensagem enviada internamente de um colega não é spam. Você usando regras de transporte para definir o valor SCL de uma mensagem dá maior controle na manipulação de spam.
ms.openlocfilehash: 7abd0d1881374b1f2a4bd32ee480445f7683d1b3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002890"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="0b801-108">Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens</span><span class="sxs-lookup"><span data-stu-id="0b801-108">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="0b801-p102">Você pode criar uma regra de transporte que define o nível de confiança de spam (SCL) de uma mensagem de email. O SCL é que uma medida de uma mensagem como provavelmente é spam. Spam é mensagens de email não solicitadas (e normalmente indesejadas). O serviço age diferentes em uma mensagem, dependendo de sua classificação do SCL. Por exemplo, você talvez queira ignorar spam filtragem de conteúdo de mensagens que são enviadas de pessoas dentro da organização, pois você confia que uma mensagem enviada internamente de um colega não é spam. Você usando regras de transporte para definir o valor SCL de uma mensagem dá maior controle na manipulação de spam.</span><span class="sxs-lookup"><span data-stu-id="0b801-p102">You can create a transport rule that sets the spam confidence level (SCL) of an email message. The SCL is a measure of how likely a message is to be spam. Spam is unsolicited (and typically unwanted) email messages. The service takes different action on a message depending on its SCL rating. For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam. Using transport rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="0b801-115">**O que você precisa saber antes de começar?**</span><span class="sxs-lookup"><span data-stu-id="0b801-115">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="0b801-116">Tempo estimado para concluir este procedimento: 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="0b801-116">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="0b801-p103">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Regras de transporte" em [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou [permissões de recursos no EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="0b801-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="0b801-119">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="0b801-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="0b801-120">Para criar uma regra de transporte que define o SCL de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="0b801-120">To create a transport rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="0b801-121">No Centro de administração do Exchange (EAC), escolha o **fluxo de email** \> **regras**.</span><span class="sxs-lookup"><span data-stu-id="0b801-121">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="0b801-122">Escolha **novo**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e, em seguida, selecione **criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="0b801-122">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="0b801-123">Especifique um nome para a regra.</span><span class="sxs-lookup"><span data-stu-id="0b801-123">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="0b801-124">Escolha **mais opções**e, em seguida, em **Aplicar esta regra se**, especifique uma condição que acionará a ação que você vai definir para essa regra (que é para definir o valor SCL).</span><span class="sxs-lookup"><span data-stu-id="0b801-124">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="0b801-125">Por exemplo, você pode definir **o remetente** \> **é interno/externo**e, em seguida, na caixa de diálogo **Selecionar local do remetente** , selecione **dentro da organização**e escolha **okey**.</span><span class="sxs-lookup"><span data-stu-id="0b801-125">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span></br>
    <span data-ttu-id="0b801-126">![Selecione o local do remetente](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b801-126">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="0b801-127">Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.</span><span class="sxs-lookup"><span data-stu-id="0b801-127">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="0b801-128">Na caixa de diálogo **especificar SCL** , selecione um dos seguintes valores e escolha **okey**:</span><span class="sxs-lookup"><span data-stu-id="0b801-128">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="0b801-129">**Filtragem de spam de desvio** - este define o SCL como -1, que significa que a filtragem de conteúdo não será realizado.</span><span class="sxs-lookup"><span data-stu-id="0b801-129">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="0b801-130">**0-4** - quando você definir o SCL como um desses valores, a mensagem será passada ao longo para o filtro de conteúdo para processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="0b801-130">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="0b801-p104">**5, 6** - quando você definir o SCL como um desses valores, a ação especificada de **Spam** nas políticas de filtro de conteúdo aplicáveis serão aplicadas. Por padrão, a ação é para enviar a mensagem para a pasta de lixo eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b801-p104">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="0b801-p105">**7-9** - quando você definir o SCL como um desses valores, a ação especificada de **spam de alta confiabilidade** nas políticas de filtro de conteúdo aplicáveis serão aplicadas. Por padrão, a ação é para enviar a mensagem para a pasta de lixo eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b801-p105">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="0b801-p106">Para obter mais informações sobre como configurar suas políticas de filtro de conteúdo, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Para obter mais informações sobre valores SCL no serviço, veja [Spam confidence levels](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0b801-p106">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="0b801-137">Especificar propriedades adicionais para a regra e escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="0b801-137">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="0b801-138">Para obter mais informações sobre as propriedades adicionais que você pode selecionar ou especificar para esta regra, consulte [usar o EAC para criar uma regra de transporte](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span><span class="sxs-lookup"><span data-stu-id="0b801-138">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="0b801-139">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="0b801-139">How do you know this worked?</span></span>

<span data-ttu-id="0b801-p107">Para verificar se esse procedimento está funcionando corretamente, enviar uma mensagem de email a alguém de dentro de sua organização e verifique se a ação executada na mensagem é conforme o esperado. Por exemplo, se você **definir o nível de confiança de spam (SCL)** para **filtragem de spam de desvio**, em seguida, a mensagem deve ser enviada à caixa de entrada do destinatário especificado. No entanto, se você **definir o nível de confiança de spam (SCL)** **9**e a ação de **spam de alta confiabilidade** para suas políticas de filtro de conteúdo aplicável for mover a mensagem para a pasta Lixo eletrônico, em seguida, a mensagem deve ser enviada para o especificado pasta de lixo eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b801-p107">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

