---
title: Relatório de mapa de fluxo de email
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Os administradores podem saber mais sobre o relatório de mapa de fluxo de emails no painel de fluxo de emails no centro de conformidade do & de segurança.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: bd05ff5cb78adb9dd89dbe3f69c2c3a78d2b1df9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252404"
---
# <a name="mail-flow-map-report"></a><span data-ttu-id="ad399-103">Relatório de mapa de fluxo de email</span><span class="sxs-lookup"><span data-stu-id="ad399-103">Mail flow map report</span></span>

> [!NOTE]
> <span data-ttu-id="ad399-104">Os recursos descritos neste tópico não foram implantados em todas as organizações do Office 365 e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="ad399-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="ad399-105">Este relatório fornece ideias sobre como os emails fluem pela sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ad399-105">This report gives insights as to how mail flows through your Office 365 organization.</span></span> <span data-ttu-id="ad399-106">Você pode usar essas informações para aprender padrões, identificar anomalias e corrigir problemas conforme eles surgem.</span><span class="sxs-lookup"><span data-stu-id="ad399-106">You can use this information to learn patterns, identify anomalies, and fix issues as they arise.</span></span>

![O relatório do mapa de fluxo de emails no painel de fluxo de emails no centro de conformidade do & de segurança](media/mail-flow-map-selected.png)

## <a name="mail-flow-map-widget"></a><span data-ttu-id="ad399-108">Widget mapa de fluxo de email</span><span class="sxs-lookup"><span data-stu-id="ad399-108">Mail flow map widget</span></span>

<span data-ttu-id="ad399-109">Por padrão, o mapa de fluxo de emails mostra o padrão de fluxo de emails de alto nível do dia anterior.</span><span class="sxs-lookup"><span data-stu-id="ad399-109">By default, the mail flow map shows the high level mail flow pattern from the previous day.</span></span> <span data-ttu-id="ad399-110">Você pode usar as setas à esquerda e à direita para dias diferentes.</span><span class="sxs-lookup"><span data-stu-id="ad399-110">You can use the left and right arrows for different days.</span></span> <span data-ttu-id="ad399-111">Focalizar o cursor do mouse sobre cada área no relatório mostrará o volume de emails de e para sua organização do Office 365, conforme mostrado no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="ad399-111">Hovering your mouse cursor over each area in the report will show the volume of mail to and from your Office 365 organization as shown in the following diagram:</span></span>

![Setas para a esquerda e para a direita no widget mapa de fluxo de emails](media/mail-flow-map-widget.png)

## <a name="overview"></a><span data-ttu-id="ad399-113">Visão Geral</span><span class="sxs-lookup"><span data-stu-id="ad399-113">Overview</span></span>

<span data-ttu-id="ad399-114">Clicar no widget **mapa de fluxo** de emails o levará para o relatório de **mapa de fluxo** de emails.</span><span class="sxs-lookup"><span data-stu-id="ad399-114">Clicking on the **Mail flow map** widget will take you to the **Mail flow map** report.</span></span> <span data-ttu-id="ad399-115">Aqui você pode ver o nível mais granular do relatório, você pode clicar em Exibir tabela de detalhes para ver os dados detalhados.</span><span class="sxs-lookup"><span data-stu-id="ad399-115">Here you can see more granular level of report, you can click View details table to see detailed data.</span></span> <span data-ttu-id="ad399-116">Você também pode baixar o relatório detalhado clicando em solicitação de relatório.</span><span class="sxs-lookup"><span data-stu-id="ad399-116">You can also download the detailed report by clicking Request report.</span></span>

![Exibição de visão geral no relatório de mapa de fluxo de emails](media/mail-flow-map-overview.png)

## <a name="details"></a><span data-ttu-id="ad399-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ad399-118">Details</span></span>

<span data-ttu-id="ad399-119">Por padrão, **Mostrar dados por** está definido como o valor **visão geral**.</span><span class="sxs-lookup"><span data-stu-id="ad399-119">By default, **Show data for** is set to the value **Overview**.</span></span> <span data-ttu-id="ad399-120">Ao clicar no menu suspenso e selecionar **detalhes**, o modo de exibição alterna para o nível de domínio detalhes.</span><span class="sxs-lookup"><span data-stu-id="ad399-120">When you click on the drop down and select **Detail**, the view switches to the domain level detail.</span></span>

![Selecionar detalhes em mostrar dados para no modo de exibição visão geral no relatório de mapa de fluxo de emails](media/mail-flow-map-select-detail.png)

<span data-ttu-id="ad399-122">Os principais remetentes e domínios de destinatário são listados, e o restante será colocado em **outros** , conforme mostrado nos seguintes diagramas:</span><span class="sxs-lookup"><span data-stu-id="ad399-122">The top sender and recipient domains are listed, and the rest will be put in **Others** as shown in the following diagrams:</span></span>

![Exibição de detalhes no relatório de mapa de fluxo de emails](media/mail-flow-map-detail.png)

## <a name="related-insights"></a><span data-ttu-id="ad399-124">Informações relacionadas</span><span class="sxs-lookup"><span data-stu-id="ad399-124">Related insights</span></span>

<span data-ttu-id="ad399-125">Os insights relacionados são mostrados abaixo do mapa de fluxo de emails, se estiverem disponíveis (por exemplo, o remetente do domínio ou as informações de loop de email).</span><span class="sxs-lookup"><span data-stu-id="ad399-125">Related insights are shown beneath the Mail flow map if they're available (for example, the Sender domain insight or the Mail loop insight).</span></span>

## <a name="see-also"></a><span data-ttu-id="ad399-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad399-126">See also</span></span>

<span data-ttu-id="ad399-127">Para obter mais informações sobre outros insights de fluxo de email no painel de fluxo de emails, consulte [Mail Flow insights no centro de conformidade de & de segurança](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ad399-127">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>