---
title: Visão superior do status do fluxo de emails do domínio
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Os administradores podem saber mais sobre a visão geral do status do fluxo de email de domínio no painel de fluxo de emails no centro de conformidade do & de segurança do Office 365.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 04aa986982465a4c66fbf99f517fb34622d65e19
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722737"
---
# <a name="top-domain-mail-flow-status-insight"></a>Visão superior do status do fluxo de emails do domínio

> [!NOTE]
> Os recursos descritos neste tópico não foram implantados em todas as organizações do Office 365 e estão sujeitos a alterações.

A visão geral do **status do fluxo de email do domínio** oferece o status atual dos domínios da sua organização em termos de fluxo de emails. Essa percepção ajuda a identificar e solucionar problemas de domínios que estão enfrentando problemas de ***impacto de fluxo*** de emails (por exemplo, não é possível receber emails externos), especialmente expirações de domínio ou domínios com registros MX incorretos.

![A visão superior do status do fluxo de domínio no painel de fluxo de emails no centro de conformidade do & de segurança do Office 365](media/domain-mail-flow-status-selected.png)

Quando você clica em **Exibir detalhes** na percepção, um submenu aparece mostrando mais detalhes para o status de cada domínio.

Uma marca de seleção verde para um domínio indica que o registro MX atual (quando você navegou para o painel de insights de fluxo de emails) corresponde ao valor que temos no registro e que o domínio recebeu emails durante as últimas duas horas.

Um x vermelho para um domínio indica que o registro MX foi alterado e que o domínio não recebeu nenhum email durante as últimas 6 horas. Isso provavelmente indica que o domínio expirou ou que o registro MX foi atualizado incorretamente. Verifique com o seu registrador de domínio ou serviço de hospedagem DNS para ver se o domínio expirou ou se o registro MX do domínio está incorreto.

![O submenu de detalhes da visão superior do status do fluxo de domínio](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a>Confira também

Para obter mais informações sobre outros insights de fluxo de email no painel de fluxo de emails, consulte [Mail Flow insights no centro de conformidade de & de segurança](mail-flow-insights-v2.md).