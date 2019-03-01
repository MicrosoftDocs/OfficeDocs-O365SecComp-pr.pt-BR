---
title: Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: Os administradores podem aprender a rotear spam para pastas de lixo eletrônico do usuário no Exchange Online Protection.
ms.openlocfilehash: 80c3e3cab1bdaf85e815ab1acc790cc907ebbb91
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341372"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="aa134-103">Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário</span><span class="sxs-lookup"><span data-stu-id="aa134-103">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa134-p101">Este tópico aplica-se apenas aos clientes do proteção do Exchange Online (EOP) que hospedam caixas de correio no local em uma implantação híbrida. Os clientes do Exchange Online cujas caixas de correio são totalmente hospedadas no Office 365 não precisam executar esses comandos.</span><span class="sxs-lookup"><span data-stu-id="aa134-p101">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="aa134-p102">A ação antispam padrão para os clientes do EOP é mover as mensagens de spam para a pasta lixo eletrônico dos destinatários. Para que essa ação funcione com caixas de correio locais, você deve configurar as regras de fluxo de mensagens do Exchange (também conhecidas como regras de transporte) em seus servidores de borda ou Hub no local para detectar cabeçalhos de spam adicionados pelo EOP. Essas regras de fluxo de emails definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover o spam para a pasta lixo eletrônico de cada caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="aa134-p102">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder. In order for this action to work with on-premises mailboxes, you must configure Exchange mail flow rules (also known as transport rules) on your on-premises Edge or Hub servers to detect spam headers added by EOP. These mail flow rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="aa134-109">Para adicionar regras de fluxo de email para garantir que o spam seja movido para a pasta lixo eletrônico usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa134-109">To add mail flow rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="aa134-p103">Acessar o Shell de gerenciamento do Exchange para o Exchange Server local. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização local do Exchange, confira **abrir o Shell**.</span><span class="sxs-lookup"><span data-stu-id="aa134-p103">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="aa134-112">Execute o seguinte comando para encaminhar mensagens de spam filtradas por conteúdo para a pasta Lixo Eletrônico:</span><span class="sxs-lookup"><span data-stu-id="aa134-112">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="aa134-113">Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkContentFilteredMail.</span><span class="sxs-lookup"><span data-stu-id="aa134-113">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="aa134-114">Execute o seguinte comando para encaminhar mensagens marcadas como spam, antes da aplicação do filtro de conteúdo, para a pasta Lixo Eletrônico:</span><span class="sxs-lookup"><span data-stu-id="aa134-114">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="aa134-115">Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkMailBeforeReachingContentFilter.</span><span class="sxs-lookup"><span data-stu-id="aa134-115">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="aa134-116">Execute o seguinte comando para garantir que as mensagens de remetentes em uma lista de bloqueios na política de filtro de spam, como a lista de bloqueios de **remetente** , sejam encaminhadas para a pasta lixo eletrônico:</span><span class="sxs-lookup"><span data-stu-id="aa134-116">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="aa134-117">Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkMailInSenderBlockList.</span><span class="sxs-lookup"><span data-stu-id="aa134-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="aa134-p104">Se você não quiser usar a ação **mover mensagem para a pasta lixo eletrônico** , você pode escolher outra ação em suas políticas de filtro de conteúdo no centro de administração do Exchange. Para obter mais informações, consulte [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Para obter mais informações sobre esses campos no cabeçalho da mensagem, consulte [anti-spam Message Headers](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="aa134-p104">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa134-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa134-121">See also</span></span>

[<span data-ttu-id="aa134-122">Cmdlet New-TransportRule</span><span class="sxs-lookup"><span data-stu-id="aa134-122">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

