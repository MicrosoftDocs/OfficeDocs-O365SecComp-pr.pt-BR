---
title: Fluxo de emails no Centro de Conformidade e Segurança
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: Os administradores podem saber mais sobre o painel de fluxo de emails no centro de conformidade do & de segurança.
ms.openlocfilehash: c7c1a6a16c908f42098500c1015b3c3994175818
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155873"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a><span data-ttu-id="f4d21-103">Fluxo de emails no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="f4d21-103">Mail flow insights in the Security & Compliance Center</span></span>

<span data-ttu-id="f4d21-104">Os administradores podem usar o painel de fluxo de emails no centro de conformidade do & de segurança para descobrir tendências, insights e realizar ações para corrigir problemas relacionados ao fluxo de emails em sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f4d21-104">Admins can use mail flow dashboard in the Security & Compliance Center to discover trends, insights and take actions to fix issues related to mail flow in their Office 365 organization.</span></span>

<span data-ttu-id="f4d21-105">As ideias, os relatórios e os widgets disponíveis no painel de fluxo de emails são:</span><span class="sxs-lookup"><span data-stu-id="f4d21-105">The insights, reports, and widgets that are available in the mail flow dashboard are:</span></span>

- [<span data-ttu-id="f4d21-106">Relatório de mapa de fluxo de email</span><span class="sxs-lookup"><span data-stu-id="f4d21-106">Mail flow map report</span></span>](mfi-mail-flow-map-report.md)

- [<span data-ttu-id="f4d21-107">Visão do status do fluxo de email de domínio</span><span class="sxs-lookup"><span data-stu-id="f4d21-107">Domain mail flow status insight</span></span>](mfi-domain-mail-flow-status-insight.md)

- [<span data-ttu-id="f4d21-108">Relatório de clientes de autenticação SMTP</span><span class="sxs-lookup"><span data-stu-id="f4d21-108">SMTP Auth clients report</span></span>](mfi-smtp-auth-clients-report.md)

- [<span data-ttu-id="f4d21-109">Percepção do domínio do remetente</span><span class="sxs-lookup"><span data-stu-id="f4d21-109">Sender domain insight</span></span>](mfi-sender-domain-insight.md)

- [<span data-ttu-id="f4d21-110">Notificação de falha na entrega</span><span class="sxs-lookup"><span data-stu-id="f4d21-110">Non-delivery report</span></span>](mfi-non-delivery-report.md)

- [<span data-ttu-id="f4d21-111">Relatório de domínio não aceito</span><span class="sxs-lookup"><span data-stu-id="f4d21-111">Non-accepted domain report</span></span>](mfi-non-accepted-domain-report.md)

- [<span data-ttu-id="f4d21-112">Fluxo de entrada e saída de emails</span><span class="sxs-lookup"><span data-stu-id="f4d21-112">Outbound and inbound mail flow</span></span>](mfi-outbound-and-inbound-mail-flow.md)

- [<span data-ttu-id="f4d21-113">Alertas de filas e filas</span><span class="sxs-lookup"><span data-stu-id="f4d21-113">Queue alerts and Queues</span></span>](mfi-queue-alerts-and-queues.md)

- [<span data-ttu-id="f4d21-114">Relatório de encaminhamento automático de mensagens</span><span class="sxs-lookup"><span data-stu-id="f4d21-114">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)

- [<span data-ttu-id="f4d21-115">Insight de loop de email</span><span class="sxs-lookup"><span data-stu-id="f4d21-115">Mail loop insight</span></span>](mfi-mail-loop-insight.md)

- [<span data-ttu-id="f4d21-116">Insights de regras de fluxo de email – modo lento</span><span class="sxs-lookup"><span data-stu-id="f4d21-116">Slow mail flow rules insight</span></span>](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a><span data-ttu-id="f4d21-117">Permissões necessárias para exibir o painel de fluxo de emails</span><span class="sxs-lookup"><span data-stu-id="f4d21-117">Permissions required to view the mail flow dashboard</span></span>

<span data-ttu-id="f4d21-118">O painel de fluxo de emails está disponível para:</span><span class="sxs-lookup"><span data-stu-id="f4d21-118">The mail flow dashboard is available to:</span></span>

- <span data-ttu-id="f4d21-119">Membros da função de **administrador global do Office 365** .</span><span class="sxs-lookup"><span data-stu-id="f4d21-119">Members of the **Office 365 global administrator** role.</span></span>

- <span data-ttu-id="f4d21-120">Membros da função de **administrador do Exchange 365 do Office** .</span><span class="sxs-lookup"><span data-stu-id="f4d21-120">Members of **Office 365 Exchange administrator** role.</span></span>

- <span data-ttu-id="f4d21-121">Membros da **função de administrador de fluxo** de emails no centro de conformidade do _AMP_ de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4d21-121">Members of the **Mail flow administrator role** in the Security & Compliance Center.</span></span> <span data-ttu-id="f4d21-122">Se essa função for explicitamente atribuída a um usuário que não é membro das funções de administrador global ou administrador do Exchange:</span><span class="sxs-lookup"><span data-stu-id="f4d21-122">If this role is explicitly assigned to a user who isn't a member of the global administrator or Exchange administrator roles:</span></span>

  - <span data-ttu-id="f4d21-123">O usuário deve fazer logon no centro de conformidade do & de segurança [https://protection.office.com](https://protection.office.com)diretamente em.</span><span class="sxs-lookup"><span data-stu-id="f4d21-123">The user must log in to the Security & Compliance Center directly at [https://protection.office.com](https://protection.office.com).</span></span>

  - <span data-ttu-id="f4d21-124">O usuário só terá permissão somente leitura para o painel de fluxo de emails.</span><span class="sxs-lookup"><span data-stu-id="f4d21-124">The user will only have read-only permission to the mail flow dashboard.</span></span>

  - <span data-ttu-id="f4d21-125">O usuário não terá acesso ao portal de administração do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f4d21-125">The user won't have access to the Office 365 admin portal.</span></span>

<span data-ttu-id="f4d21-126">Para obter mais informações sobre a função de administrador global do Office 365, consulte [about office 365 admin Roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="f4d21-126">For more information about the Office 365 global administrator role, see [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span></span>

<span data-ttu-id="f4d21-127">Para obter informações sobre como atribuir funções do centro de conformidade do & de segurança aos usuários, consulte [fornecer aos usuários acesso ao centro de conformidade do & de segurança](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="f4d21-127">For information on assigning Security & Compliance Center roles to users, see [Give users access to the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span></span>

## <a name="where-to-find-the-mail-flow-dashboard"></a><span data-ttu-id="f4d21-128">Onde encontrar o painel de fluxo de emails</span><span class="sxs-lookup"><span data-stu-id="f4d21-128">Where to find the mail flow dashboard</span></span>

1. <span data-ttu-id="f4d21-129">Vá para o centro de conformidade do & [https://protection.office.com](https://protection.office.com)de segurança em.</span><span class="sxs-lookup"><span data-stu-id="f4d21-129">Go to the Security & Compliance Center at [https://protection.office.com](https://protection.office.com).</span></span>

2. <span data-ttu-id="f4d21-130">Expanda **fluxo de email** e selecione **painel**.</span><span class="sxs-lookup"><span data-stu-id="f4d21-130">Expand **Mail flow** and then select **Dashboard**.</span></span>

   ![O painel de fluxo de emails no centro de conformidade do & de segurança do Office 365](media/mail-flow-dashboard-v2.png)
