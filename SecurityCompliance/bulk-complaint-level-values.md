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
# <a name="bulk-complaint-level-values"></a>Valores de nível compatível com dados em massa

Correspondências em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são correspondências em massa boa que enviam queria mensagens com conteúdo relevante para seus assinantes. Essas mensagens geram reclamações alguns destinatários. Outras correspondências em massa enviam mensagens não solicitadas que bastante se parecer com spam e geram muitas reclamações de destinatários. Para distinguir esses tipos de correspondências em massa, mensagens de correspondências em massa recebem uma classificação em massa compatível com nível (BCL). Intervalo de classificações de BCL entre 1 e 9, dependendo de como provavelmente o mensageiro em massa é gerar reclamações. Um remetente que tem uma classificação de 9 BCL é provável de gerar muitas reclamações de destinatários, enquanto uma classificação de BCL 3 é improvável gerar muitas reclamações. A Microsoft usa fontes internas e de terceiros para identificar o email em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho **X-Microsoft-Antispam** de cada mensagem. Para obter mais informações sobre este cabeçalho da mensagem, consulte [cabeçalhos de mensagem antispam](anti-spam-message-headers.md). 
  
Você pode usar valores BCL para definir o nível desejado de sua organização requer seguindo as etapas em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)de filtragem em massa.
  
Mais valores BCL são adicionados e serão incluídos aqui no futuro. A tabela a seguir lista e descreve os valores BCL que estão atualmente em uso.
  
|||
|:-----|:-----|
|**Valor BCL** <br/> |**Descrição** <br/> |
|0  <br/> |A mensagem não é de um remetente em massa.  <br/> |
|1, 2, 3  <br/> |A mensagem é de um remetente em massa que gera algumas reclamações.  <br/> |
|4, 5, 6, 7  <br/> |A mensagem é de um remetente em massa que gera um número misto de reclamações.  <br/> |
|8, 9  <br/> |A mensagem é de um remetente em massa que gera um alto número de reclamações  <br/> |
   

