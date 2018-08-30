---
title: Valores de nível compatível com dados em massa
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
description: Correspondências em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são correspondências em massa boa que enviam queria mensagens com conteúdo relevante para seus assinantes. Essas mensagens geram reclamações alguns destinatários. Outras correspondências em massa enviam mensagens não solicitadas que bastante se parecer com spam e geram muitas reclamações de destinatários. Para distinguir esses tipos de correspondências em massa, mensagens de correspondências em massa recebem uma classificação em massa compatível com nível (BCL). Intervalo de classificações de BCL entre 1 e 9, dependendo de como provavelmente o mensageiro em massa é gerar reclamações. Um remetente que tem uma classificação de 9 BCL é provável de gerar muitas reclamações de destinatários, enquanto uma classificação de BCL 3 é improvável gerar muitas reclamações. A Microsoft usa fontes internas e de terceiros para identificar o email em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho X-Microsoft-Antispam de cada mensagem. Para obter mais informações sobre este cabeçalho da mensagem, consulte cabeçalhos de mensagem antispam.
ms.openlocfilehash: c4100b0d289398d9333369071c9886309f2abcb4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003050"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="87b4b-112">Valores de nível compatível com dados em massa</span><span class="sxs-lookup"><span data-stu-id="87b4b-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="87b4b-p102">Correspondências em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são correspondências em massa boa que enviam queria mensagens com conteúdo relevante para seus assinantes. Essas mensagens geram reclamações alguns destinatários. Outras correspondências em massa enviam mensagens não solicitadas que bastante se parecer com spam e geram muitas reclamações de destinatários. Para distinguir esses tipos de correspondências em massa, mensagens de correspondências em massa recebem uma classificação em massa compatível com nível (BCL). Intervalo de classificações de BCL entre 1 e 9, dependendo de como provavelmente o mensageiro em massa é gerar reclamações. Um remetente que tem uma classificação de 9 BCL é provável de gerar muitas reclamações de destinatários, enquanto uma classificação de BCL 3 é improvável gerar muitas reclamações. A Microsoft usa fontes internas e de terceiros para identificar o email em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho **X-Microsoft-Antispam** de cada mensagem. Para obter mais informações sobre este cabeçalho da mensagem, consulte [cabeçalhos de mensagem antispam](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="87b4b-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="87b4b-123">Você pode usar valores BCL para definir o nível desejado de sua organização requer seguindo as etapas em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)de filtragem em massa.</span><span class="sxs-lookup"><span data-stu-id="87b4b-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="87b4b-p103">Mais valores BCL são adicionados e serão incluídos aqui no futuro. A tabela a seguir lista e descreve os valores BCL que estão atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="87b4b-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87b4b-126">**Valor BCL**</span><span class="sxs-lookup"><span data-stu-id="87b4b-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="87b4b-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="87b4b-127">**Description**</span></span> <br/> |
|<span data-ttu-id="87b4b-128">0</span><span class="sxs-lookup"><span data-stu-id="87b4b-128">0</span></span>  <br/> |<span data-ttu-id="87b4b-129">A mensagem não é de um remetente em massa.</span><span class="sxs-lookup"><span data-stu-id="87b4b-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="87b4b-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="87b4b-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="87b4b-131">A mensagem é de um remetente em massa que gera algumas reclamações.</span><span class="sxs-lookup"><span data-stu-id="87b4b-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="87b4b-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="87b4b-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="87b4b-133">A mensagem é de um remetente em massa que gera um número misto de reclamações.</span><span class="sxs-lookup"><span data-stu-id="87b4b-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="87b4b-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="87b4b-134">8, 9</span></span>  <br/> |<span data-ttu-id="87b4b-135">A mensagem é de um remetente em massa que gera um alto número de reclamações</span><span class="sxs-lookup"><span data-stu-id="87b4b-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   

