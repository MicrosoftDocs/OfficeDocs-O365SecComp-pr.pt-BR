---
title: Alertas de fila e filas
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Os administradores podem conhecer alertas de fila e filas no painel de fluxo de email no Centro de conformidade do & de segurança do Office 365.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685311"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="0df4d-103">Alertas de fila e filas</span><span class="sxs-lookup"><span data-stu-id="0df4d-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="0df4d-104">Alertas de fila</span><span class="sxs-lookup"><span data-stu-id="0df4d-104">Queue alerts</span></span>

<span data-ttu-id="0df4d-p101">Quando as mensagens não podem ser enviadas da sua organização do Office 365 para seu local ou servidores de email do parceiro usando conectores, as mensagens são enfileiradas no Office 365. Exemplos comuns que causam essa condição são:</span><span class="sxs-lookup"><span data-stu-id="0df4d-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="0df4d-107">O conector está configurado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="0df4d-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="0df4d-108">Houve alterações de rede ou um firewall em seu ambiente local.</span><span class="sxs-lookup"><span data-stu-id="0df4d-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="0df4d-p102">O Office 365 continuarão repetir a entrega por 48 horas. Após 48 horas, as mensagens expirarão e serão retornadas para os remetentes em relatórios de falha na entrega (também conhecido como um NDRs ou pulando para mensagens).</span><span class="sxs-lookup"><span data-stu-id="0df4d-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="0df4d-p103">Se o volume de email na fila excede o limite de pré-definidos (o valor padrão é 2000 mensagens), os alertas estarão disponíveis no painel do fluxo de email em **alertas recentes**e admins receberá uma notificação de email (para seus endereços de email alternativos) . Para configurar o limite de alerta, limite diário de notificação e/ou destinatários de alerta, consulte a seção de **alertas de fila personalizar** abaixo.</span><span class="sxs-lookup"><span data-stu-id="0df4d-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Alertas de fila na área de alertas recentes do painel de fluxo de email no Centro de conformidade do & de segurança do Office 365](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="0df4d-114">Personalizar os alertas de fila</span><span class="sxs-lookup"><span data-stu-id="0df4d-114">Customize queue alerts</span></span>

<span data-ttu-id="0df4d-p104">Ideias de fluxo de email criar uma política de alerta nomeado **mensagens foram adiadas** (a caixa de seleção **Enviar notificações de email** no exemplo captura de tela abaixo) encontrado em **alertas** \> **Políticas de alerta**. Você pode modificar os destinatários de limite e alerta clicando na política.</span><span class="sxs-lookup"><span data-stu-id="0df4d-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Navegação de alertas](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="0df4d-118">Você verá um novo blade de informações de política, você agora pode clicar em **Editar política**.</span><span class="sxs-lookup"><span data-stu-id="0df4d-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Editar Política ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="0df4d-p105">O blade informações será alterado para **Editar política**. Agora você pode alterar os destinatários da mensagem de alerta, o limite no número de notificações enviadas por dia e o limite mínimo para acionar o alerta (200 ou mais).</span><span class="sxs-lookup"><span data-stu-id="0df4d-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Editar política Blade](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="0df4d-123">Detalhes de alerta de fila</span><span class="sxs-lookup"><span data-stu-id="0df4d-123">Queue alert details</span></span>

<span data-ttu-id="0df4d-124">Quando você clica no alerta, os detalhes de alerta aparecem em um painel de submenu.</span><span class="sxs-lookup"><span data-stu-id="0df4d-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Na área de alertas recentes do painel de fluxo de email no Centro de conformidade do & de segurança do Office 365, selecione um alerta de fila](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![O submenu detalhes alerta de fila no Centro de conformidade do & de segurança do Office 365](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="0df4d-127">Você pode clicar em **Exibir fila** nos detalhes do alertas para ver os detalhes da fila, problemas e links para as correções disponíveis em um novo painel de submenu.</span><span class="sxs-lookup"><span data-stu-id="0df4d-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![O submenu detalhes alerta de fila no Centro de conformidade do & de segurança do Office 365](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Exibir a fila nos detalhes do alertas](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="0df4d-130">Filas</span><span class="sxs-lookup"><span data-stu-id="0df4d-130">Queues</span></span>

<span data-ttu-id="0df4d-p106">Mesmo que o volume de mensagem na fila ainda não excedeu o limite, você ainda pode usar a área de **filas** do painel de controle de fluxo de email para ver as mensagens que foram enfileiradas por mais de uma hora. Você pode usar a área de **filas** para monitorar o número de mensagens na fila (o valor 0 indica o fluxo de emails é Okey) e executar a ação antes que o número de mensagens na fila fique muito grande.</span><span class="sxs-lookup"><span data-stu-id="0df4d-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Filas em que o painel de fluxo de email no Centro de conformidade do & de segurança do Office 365](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="0df4d-134">Quando você clicar o número de mensagens na fila em **filas**, os detalhes de fila e orientação sobre como corrigir o problema serão exibidos em um painel de submenu (o mesmo submenu exibido após você clicar em **Exibir fila** nos detalhes de um alerta de fila).</span><span class="sxs-lookup"><span data-stu-id="0df4d-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Detalhes da fila](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
