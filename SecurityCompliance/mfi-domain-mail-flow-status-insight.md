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
description: Os administradores podem saber mais sobre a visão geral do status do fluxo de email de domínio no painel de fluxo de emails no centro de conformidade do & de segurança.
ms.openlocfilehash: 851ef1438f111a36f69563670bbd0835a9956edc
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868581"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="7bda6-103">Visão superior do status do fluxo de emails do domínio</span><span class="sxs-lookup"><span data-stu-id="7bda6-103">Top domain mail flow status insight</span></span>

<span data-ttu-id="7bda6-104">A visão geral do **status do fluxo de email do domínio** oferece o status atual dos domínios da sua organização em termos de fluxo de emails.</span><span class="sxs-lookup"><span data-stu-id="7bda6-104">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="7bda6-105">Essa percepção ajuda a identificar e solucionar problemas de domínios que estão enfrentando problemas de ***impacto de fluxo*** de emails (por exemplo, não é possível receber emails externos), especialmente expirações de domínio ou domínios com registros MX incorretos.</span><span class="sxs-lookup"><span data-stu-id="7bda6-105">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![A visão geral do status do fluxo de domínio no painel de fluxo de emails no centro de conformidade do & de segurança](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="7bda6-107">Quando você clica em **Exibir detalhes** na percepção, um submenu aparece mostrando mais detalhes para o status de cada domínio.</span><span class="sxs-lookup"><span data-stu-id="7bda6-107">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="7bda6-108">Uma marca de seleção verde para um domínio indica que o registro MX atual (quando você navegou para o painel de insights de fluxo de emails) corresponde ao valor que temos no registro e que o domínio recebeu emails durante as últimas duas horas.</span><span class="sxs-lookup"><span data-stu-id="7bda6-108">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="7bda6-109">Um x vermelho para um domínio indica que o registro MX foi alterado e que o domínio não recebeu nenhum email durante as últimas 6 horas.</span><span class="sxs-lookup"><span data-stu-id="7bda6-109">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="7bda6-110">Isso provavelmente indica que o domínio expirou ou que o registro MX foi atualizado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="7bda6-110">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="7bda6-111">Verifique com o seu registrador de domínio ou serviço de hospedagem DNS para ver se o domínio expirou ou se o registro MX do domínio está incorreto.</span><span class="sxs-lookup"><span data-stu-id="7bda6-111">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![O submenu de detalhes da visão superior do status do fluxo de domínio](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="7bda6-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bda6-113">See also</span></span>

<span data-ttu-id="7bda6-114">Para obter mais informações sobre outros insights de fluxo de email no painel de fluxo de emails, consulte [Mail Flow insights no centro de conformidade de & de segurança](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7bda6-114">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
