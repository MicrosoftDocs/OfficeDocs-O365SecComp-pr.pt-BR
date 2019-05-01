---
title: Criptografia de mensagem avançada do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: A criptografia de mensagem avançada no Office 365 ajuda as organizações a cumprir suas obrigações de conformidade, permitindo que os administradores expirem e revogassem o acesso por meio de um portal da Web do Office 365 para emails criptografados.
ms.openlocfilehash: a775803a8d2678441f319c0145e96e7d19c26f7e
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506703"
---
# <a name="office-365-advanced-message-encryption"></a>Criptografia de mensagem avançada do Office 365

A criptografia de mensagem avançada do Office 365 está disponível na parte superior da criptografia de mensagem do Office 365 em determinadas assinaturas. A criptografia avançada de mensagens está incluída no [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), no Office 365 Enterprise E5 e no Office 365 Education a5. Se sua organização tiver uma assinatura do Office 365 que não inclua a criptografia de mensagem avançada do Office 365, você poderá comprar a criptografia de mensagem avançada como um complemento com a conformidade E5 do SKU de conformidade avançada.

Este artigo faz parte de uma série maior de artigos sobre a [criptografia de mensagens do Office 365](ome.md).

A criptografia de mensagem avançada no Office 365 ajuda os clientes a cumprir as obrigações de conformidade que exigem controles mais flexíveis sobre destinatários externos e seu acesso a emails criptografados. Com a criptografia de mensagem avançada no Office 365, você pode controlar emails confidenciais compartilhados fora da organização com políticas automáticas. Você configura essas políticas para identificar tipos de informações confidenciais, como PII, finanças ou IDs de integridade, ou pode usar palavras-chave para melhorar a proteção. Depois de configurar as políticas, você emparelhará políticas com os modelos de email com identidade visual personalizada e, em seguida, adicionará uma data de expiração para obter controle adicional para emails que se encaixam na política. Além disso, os administradores podem controlar ainda mais os emails criptografados acessados externamente por meio de um portal da Web seguro revogando o acesso ao email a qualquer momento.

Você só pode definir uma expiração para e revogar emails enviados para destinatários externos.

Com a criptografia de mensagem avançada do Office 365, sempre que você aplicar a identidade visual personalizada, o Office 365 aplica o wrapper a emails que se ajustam à regra de fluxo de emails para a qual você aplica o modelo. Além disso, a expiração só poderá ser usada se a identidade visual personalizada for usada. Só é possível revogar mensagens recebidas pelo portal.

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Introdução à criptografia de mensagem avançada do Office 365

Os tópicos a seguir descrevem como configurar e usar a criptografia de mensagem avançada.

Sua organização deve ter uma assinatura que inclua a criptografia de mensagem avançada do Office 365. Para obter informações detalhadas sobre assinaturas suportadas, consulte a [Descrição de política de mensagens e serviço de conformidade](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).

Configure os novos recursos de criptografia de mensagem do Office 365 se eles ainda não estiverem configurados para aproveitar os recursos avançados de criptografia de mensagens, que fornecem proteção adicional sobre as mensagens criptografadas compartilhadas externamente. Se você não tiver a criptografia de mensagem do Office 365 configurada, confira [configurar novos recursos de criptografia de mensagens do office 365](set-up-new-message-encryption-capabilities.md).

[Definir uma data de expiração para email criptografado pela criptografia de mensagem avançada do Office 365](ome-advanced-expiration.md). Controlar emails confidenciais compartilhados fora da organização com políticas automáticas que aprimoram a proteção, expirando o acesso por meio de um portal da Web seguro para emails criptografados.

[Revogar emails criptografados pela criptografia de mensagem avançada do Office 365](revoke-ome-encrypted-mail.md). Controle emails confidenciais compartilhados fora da organização e aprimore a proteção revogando o acesso por meio de um portal da Web seguro para emails criptografados.  