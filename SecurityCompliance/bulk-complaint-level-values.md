---
title: Valores de nível de reclamação em massa
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
ms.collection:
- M365-security-compliance
description: Os emails em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são bons remetentes em massa que enviam mensagens desejadas com conteúdo relevante para seus assinantes. Essas mensagens geram poucas reclamações de destinatários. Outros remetentes em massa enviam mensagens não solicitadas que parecem muito parecidas com spam e geram muitas queixas de destinatários. Para distinguir esses tipos de remetentes em massa, as mensagens de email em massa recebem uma classificação de BCL (nível de reclamação em massa). A classificação de BCL varia de 1 a 9, dependendo da probabilidade de o remetente de mensagens em massa gerar queixas. Um remetente que tenha uma classificação da BCL 9 provavelmente gerará muitas queixas de destinatários, enquanto uma classificação da BCL 3 será improvável de gerar muitas queixas. A Microsoft usa fontes internas e de terceiros para identificar emails em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho X-Microsoft-antispam de cada mensagem. Para obter mais informações sobre esse cabeçalho de mensagem, consulte anti-spam Message Headers.
ms.openlocfilehash: a948e90ba436dcfdb78df856e090983e6015bb0a
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276011"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="0616f-112">Valores de nível de reclamação em massa</span><span class="sxs-lookup"><span data-stu-id="0616f-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="0616f-p102">Os emails em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são bons remetentes em massa que enviam mensagens desejadas com conteúdo relevante para seus assinantes. Essas mensagens geram poucas reclamações de destinatários. Outros remetentes em massa enviam mensagens não solicitadas que parecem muito parecidas com spam e geram muitas queixas de destinatários. Para distinguir esses tipos de remetentes em massa, as mensagens de email em massa recebem uma classificação de BCL (nível de reclamação em massa). A classificação de BCL varia de 1 a 9, dependendo da probabilidade de o remetente de mensagens em massa gerar queixas. Um remetente que tenha uma classificação da BCL 9 provavelmente gerará muitas queixas de destinatários, enquanto uma classificação da BCL 3 será improvável de gerar muitas queixas. A Microsoft usa fontes internas e de terceiros para identificar emails em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho **X-Microsoft-antispam** de cada mensagem. Para obter mais informações sobre esse cabeçalho de mensagem, consulte [anti-spam Message Headers](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="0616f-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="0616f-123">Você pode usar valores de BCL para definir o nível desejado de filtragem em massa que sua organização requer, seguindo as etapas em [Configure Your spam filter Policies](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0616f-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="0616f-p103">Mais valores de BCL estão sendo adicionados e serão incluídos aqui no futuro. A tabela a seguir lista e descreve os valores de BCL que estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="0616f-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0616f-126">**Valor de BCL**</span><span class="sxs-lookup"><span data-stu-id="0616f-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="0616f-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0616f-127">**Description**</span></span> <br/> |
|<span data-ttu-id="0616f-128">,0</span><span class="sxs-lookup"><span data-stu-id="0616f-128">0</span></span>  <br/> |<span data-ttu-id="0616f-129">A mensagem não é de um remetente em massa.</span><span class="sxs-lookup"><span data-stu-id="0616f-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="0616f-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="0616f-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="0616f-131">A mensagem é de um remetente em massa que gera algumas reclamações.</span><span class="sxs-lookup"><span data-stu-id="0616f-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="0616f-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="0616f-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="0616f-133">A mensagem é de um remetente em massa que gera um número misto de reclamações.</span><span class="sxs-lookup"><span data-stu-id="0616f-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="0616f-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="0616f-134">8, 9</span></span>  <br/> |<span data-ttu-id="0616f-135">A mensagem é de um remetente em massa que gera um grande número de reclamações</span><span class="sxs-lookup"><span data-stu-id="0616f-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   

