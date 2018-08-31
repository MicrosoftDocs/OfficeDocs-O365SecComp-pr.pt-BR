---
title: Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
description: A ação de antispam padrão para clientes do EOP é mover mensagens de spam para a pasta de lixo eletrônico dos destinatários. Para esta ação trabalhar com caixas de correio local, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou de Hub local para detectar os cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover de spam para a pasta Lixo eletrônico de cada caixa de correio.
ms.openlocfilehash: 1b0a9e5ee39820baade714612ca0b0bdb7a81bb9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002850"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="acea3-105">Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário</span><span class="sxs-lookup"><span data-stu-id="acea3-105">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acea3-p102">Este tópico se aplica somente aos clientes do Exchange Online Protection (EOP) que hospedam as caixas de correio local em uma implantação híbrida. Clientes do Exchange Online cujas caixas de correio são totalmente hospedado no Office 365 não precisará executar esses comandos.</span><span class="sxs-lookup"><span data-stu-id="acea3-p102">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="acea3-p103">A ação de antispam padrão para clientes do EOP é mover mensagens de spam para a pasta de lixo eletrônico dos destinatários. Para esta ação trabalhar com caixas de correio local, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou de Hub local para detectar os cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover de spam para a pasta Lixo eletrônico de cada caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="acea3-p103">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder. In order for this action to work with on-premises mailboxes, you must configure Exchange Transport rules on your on-premises Edge or Hub servers to detect spam headers added by EOP. These Transport rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="acea3-111">Para adicionar transporte regras para garantir que spam é movido para a pasta Lixo eletrônico usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="acea3-111">To add transport rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="acea3-p104">Acesse o Shell de gerenciamento do Exchange para seu servidor do Exchange local. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização do Exchange local, consulte **Abrir o Shell**.</span><span class="sxs-lookup"><span data-stu-id="acea3-p104">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="acea3-114">Execute o seguinte comando para encaminhar mensagens de spam filtradas por conteúdo para a pasta Lixo Eletrônico:</span><span class="sxs-lookup"><span data-stu-id="acea3-114">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="acea3-115">Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkContentFilteredMail.</span><span class="sxs-lookup"><span data-stu-id="acea3-115">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="acea3-116">Execute o seguinte comando para encaminhar mensagens marcadas como spam, antes da aplicação do filtro de conteúdo, para a pasta Lixo Eletrônico:</span><span class="sxs-lookup"><span data-stu-id="acea3-116">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="acea3-117">Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkMailBeforeReachingContentFilter.</span><span class="sxs-lookup"><span data-stu-id="acea3-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="acea3-118">Execute o seguinte comando para garantir que as mensagens de remetentes em uma lista de bloqueios na política de filtro de spam, como a lista de **bloqueio de remetente** , são roteadas para a pasta Lixo eletrônico:</span><span class="sxs-lookup"><span data-stu-id="acea3-118">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="acea3-119">Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkMailInSenderBlockList.</span><span class="sxs-lookup"><span data-stu-id="acea3-119">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="acea3-p105">Se você não quiser usar a ação de **mover a mensagem para a pasta Lixo eletrônico** , você pode escolher outra ação em suas políticas de filtro de conteúdo no Centro de administração do Exchange. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Para obter mais informações sobre esses campos no cabeçalho da mensagem, consulte [cabeçalhos de mensagem antispam](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="acea3-p105">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acea3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="acea3-123">See also</span></span>

[<span data-ttu-id="acea3-124">Cmdlet New-TransportRule.</span><span class="sxs-lookup"><span data-stu-id="acea3-124">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

