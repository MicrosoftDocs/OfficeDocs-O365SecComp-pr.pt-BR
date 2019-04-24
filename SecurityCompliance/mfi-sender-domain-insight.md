---
title: Corrigir a percepção do domínio do remetente
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Os administradores podem saber mais sobre a correção do domínio do remetente no painel de fluxo de emails no centro de conformidade do & de segurança.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: bd62d6d0b42edfd1eedf543d7d8bb68903c7c608
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252162"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="d6f2d-103">Corrigir a percepção do domínio do remetente</span><span class="sxs-lookup"><span data-stu-id="d6f2d-103">Fix sender domain insight</span></span>

> [!NOTE]
> <span data-ttu-id="d6f2d-104">Os recursos descritos neste tópico não foram implantados em todas as organizações do Office 365 e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="d6f2d-105">O Office 365 requer mensagens de envio de ambientes de email locais internos para o Office 365 para atender a determinados critérios de segurança:</span><span class="sxs-lookup"><span data-stu-id="d6f2d-105">Office 365 requires messages sending from internal on-premises email environments to Office 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="d6f2d-106">Você criou um conector de entrada no Office 365 para autenticar conexões SMTP do seu servidor de email local usando o endereço IP de origem ou um certificado.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-106">You've created an inbound connector in Office 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="d6f2d-107">Você configurou seu servidor de email local para retransmitir emails por meio do Office 365 para o mundo externo.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-107">You've configured your on-premises email server to relay email via Office 365 to external world.</span></span>

- <span data-ttu-id="d6f2d-108">Na configuração, uma das seguintes instruções é verdadeira:</span><span class="sxs-lookup"><span data-stu-id="d6f2d-108">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="d6f2d-109">O domínio de email do remetente está registrado na sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-109">The sender's email domain is registered in your Office 365 organization.</span></span> <span data-ttu-id="d6f2d-110">Para obter mais informações, consulte adicionar domínios no Office 365.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-110">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="d6f2d-111">Seu servidor de email local está configurado para usar um certificado para enviar emails para o Office 365, o certificado contém ou corresponde exatamente a um nome de domínio que você registrou no Office 365 e criou um conector baseado em certificado no Office 365 com esse Domain.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-111">Your on-premises email server is configured to use a certificate to send email to Office 365, the certificate contains or exactly matches a domain name that you've registered in Office 365, and you've created a certificate based connector in Office 365 with that domain.</span></span> 

<span data-ttu-id="d6f2d-112">As mensagens que não atenderem aos critérios não serão atribuídas à organização e poderão ser rejeitadas.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-112">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="d6f2d-113">A **solução de correção de domínio do remetente** mostra emails do seu ambiente local que não atendem aos critérios, ajuda a identificar máquinas potencialmente comprometidas e contas de usuário em seu ambiente de email local e ajuda você a realizar ações de correção.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-113">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![A correção do domínio do remetente se aprofunda no painel de fluxo de emails no centro de conformidade do & de segurança](media/sender-domain-insight-selected.png)

<span data-ttu-id="d6f2d-115">Ao clicar em **Exibir detalhes**, você será levado para outro widget com mais detalhes, conforme mostrado no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="d6f2d-115">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![O widget detalhes na visão corrigir domínio do remetente](media/sender-domain-view-details.png)

<span data-ttu-id="d6f2d-117">Você verá o conector de entrada usado para entregar as mensagens ao Office 365.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-117">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="d6f2d-118">Você também pode clicar em **Exibir IDs de mensagem de amostra** para ver os detalhes das mensagens que foram enviadas de seu ambiente de email local.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-118">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="d6f2d-119">Como essas mensagens foram rejeitadas pelo Office 365, não é possível usar o rastreamento de mensagens, mas você pode usar as IDs de mensagem de exemplo para rastrear as mensagens no seu ambiente de email local.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-119">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![Exibir IDs de mensagem de exemplo na solução corrigir domínio do remetente](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a><span data-ttu-id="d6f2d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6f2d-121">See also</span></span>

<span data-ttu-id="d6f2d-122">Para obter mais informações sobre outros insights de fluxo de email no painel de fluxo de emails, consulte [Mail Flow insights no centro de conformidade de & de segurança](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d6f2d-122">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
