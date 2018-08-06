---
title: Relatórios e rastreamento de mensagem no Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: O Microsoft Proteção do Exchange Online (EOP) oferece muitos relatórios diferentes que podem ajudá-lo a determinar o status e a integridade gerais de sua organização. Existem também ferramentas que ajudam você a solucionar problemas com eventos específicos (tais como uma mensagem que não chega aos destinatários pretendidos), e relatórios de auditoria para ajudar nos requisitos de conformidade. A tabela a seguir descreve os relatórios e as ferramentas de solução de problemas disponíveis para o administradores de EOP.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027138"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="b0d94-105">Relatórios e rastreamento de mensagem no Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b0d94-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="b0d94-p102">Microsoft Exchange Online Protection (EOP) oferece vários relatórios diferentes que podem ajudá-lo a determinam o status geral e a integridade da sua organização. Há também ferramentas para ajudá-lo a solucionar problemas de eventos específicos (por exemplo, uma mensagem que chegam não para seus destinatários pretendidos) e relatórios de auditoria para auxiliar com os requisitos de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b0d94-p102">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization. There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="b0d94-108">Relatórios de uso</span><span class="sxs-lookup"><span data-stu-id="b0d94-108">Usage reports</span></span>

<span data-ttu-id="b0d94-109">**Grupos do Office 365atividade** Exibir informações sobre a quantidade de Grupos do Office 365 que são criados e usados.</span><span class="sxs-lookup"><span data-stu-id="b0d94-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="b0d94-110">**Atividade de email** Exibir informações sobre o número de mensagens enviadas, recebidas e lidas em toda sua organização e por usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="b0d94-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="b0d94-p103">**Uso do aplicativo de email** Exibir informações sobre os aplicativos de email que são usados. Isso inclui o número total de conexões para cada aplicativo e as versões do Outlook que estão se conectando.</span><span class="sxs-lookup"><span data-stu-id="b0d94-p103">**Email app usage** View information about the email apps that are used. This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="b0d94-113">**Uso de caixa de correio** Exibir informações sobre o armazenamento usado, consumo de cota, contagem de itens e última atividade (atividade de leitura ou envio) para caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="b0d94-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="b0d94-114">Consulte os seguintes recursos para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="b0d94-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="b0d94-115">Relatórios do Office 365 no Centro de administração - grupos do Office 365</span><span class="sxs-lookup"><span data-stu-id="b0d94-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="b0d94-116">Relatórios do Office 365 no Centro de administrador - Atividade de email</span><span class="sxs-lookup"><span data-stu-id="b0d94-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="b0d94-117">Relatórios do Office 365 no Centro de administrador - Uso do aplicativo de email</span><span class="sxs-lookup"><span data-stu-id="b0d94-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="b0d94-118">Relatórios do Office 365 no Centro de administrador - Uso de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="b0d94-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a><span data-ttu-id="b0d94-119">Segurança &amp; relatórios de conformidade no Centro de administração do Office 365</span><span class="sxs-lookup"><span data-stu-id="b0d94-119">Security &amp; compliance reports in the Office 365 admin center</span></span>

<span data-ttu-id="b0d94-120">Esses relatórios aprimorados fornecem uma experiência interativa de relatórios para os administradores do EOP, que inclui informações de resumo e a capacidade de fazer uma busca detalhada para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="b0d94-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="b0d94-121">**Proteção avançada contra ameaças (ATP)** Exibir informações sobre links e anexos seguros que fazem parte da ATP.</span><span class="sxs-lookup"><span data-stu-id="b0d94-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="b0d94-122">**EOP** Exibir informações sobre detecções de malware, mensagens falsificadas, detecções de spam e fluxo de emails de e para sua organização.</span><span class="sxs-lookup"><span data-stu-id="b0d94-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="b0d94-123">Exibir relatórios de proteção de ameaça avançadas e Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b0d94-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="b0d94-124">Relatórios personalizados usando o Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b0d94-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="b0d94-125">Criar relatórios que estão disponíveis no Centro de administração do Office 365 usando o Microsoft Graph ver programaticamente os subtópicos de [trabalhar com relatórios de uso do Office 365 no Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span><span class="sxs-lookup"><span data-stu-id="b0d94-125">Programmatically create reports that are available in the Office 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="b0d94-126">Relatórios personalizados usando serviços Web de relatório</span><span class="sxs-lookup"><span data-stu-id="b0d94-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="b0d94-127">Crie relatórios de maneira programática disponível PowerShell do Exchange Online Protection cmdlets de relatório usando a filtragem de consulta do REST/ODATA2.</span><span class="sxs-lookup"><span data-stu-id="b0d94-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="b0d94-128">Consulte o [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span><span class="sxs-lookup"><span data-stu-id="b0d94-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="b0d94-129">Rastreamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="b0d94-129">Message trace</span></span>

<span data-ttu-id="b0d94-p104">Mensagens de email são conforme elas viajam através do EOP. Você pode determinar se uma mensagem de email foi recebida, rejeitada, adiada ou entregue pelo serviço. Ele também mostra quais ações foram realizadas na mensagem antes de que atingiu seu status final.</span><span class="sxs-lookup"><span data-stu-id="b0d94-p104">Follows email messages as they travel through EOP. You can determine if an email message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="b0d94-133">Você pode usar essa informação para responder com eficiência às perguntas dos seus usuários, solucionar problemas de fluxo de email, validar alterações de política e reduzir a necessidade de contatar o suporte técnico para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="b0d94-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="b0d94-134">Consulte [rastrear uma mensagem de Email](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0d94-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="b0d94-135">Registro em log de auditoria</span><span class="sxs-lookup"><span data-stu-id="b0d94-135">Audit logging</span></span>

<span data-ttu-id="b0d94-p105">Rastreia alterações específicas feitas por administradores para sua organização. Esses relatórios podem ajudar você a solucionar problemas de configuração ou encontrar a causa de problemas relacionados à conformidade ou de segurança.  consulte [relatórios de auditoria no EOP](auditing-reports-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="b0d94-p105">Tracks specific changes made by admins to your organization. These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.  see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="b0d94-139">Disponibilidade e latência de dados de relatórios e rastreamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="b0d94-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="b0d94-140">A tabela a seguir descreve quando dados de relatórios e rastreamento de mensagens do EOP estão disponíveis e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="b0d94-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="b0d94-141">**Tipo de relatório**</span><span class="sxs-lookup"><span data-stu-id="b0d94-141">**Report type**</span></span> <br/> |<span data-ttu-id="b0d94-142">**Dados disponíveis por (período retrospectivo)**</span><span class="sxs-lookup"><span data-stu-id="b0d94-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="b0d94-143">**Latência**</span><span class="sxs-lookup"><span data-stu-id="b0d94-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="b0d94-144">Relatórios resumidos de proteção de email</span><span class="sxs-lookup"><span data-stu-id="b0d94-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="b0d94-145">90 dias</span><span class="sxs-lookup"><span data-stu-id="b0d94-145">90 days</span></span>  <br/> |<span data-ttu-id="b0d94-p106">A agregação de dados de mensagens geralmente é concluída em 24 a 48 horas. Algumas pequenas alterações agregadas progressivas podem ocorrer por até 5 dias.</span><span class="sxs-lookup"><span data-stu-id="b0d94-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="b0d94-148">Relatórios de detalhes de proteção de email</span><span class="sxs-lookup"><span data-stu-id="b0d94-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="b0d94-149">90 dias</span><span class="sxs-lookup"><span data-stu-id="b0d94-149">90 days</span></span>  <br/> |<span data-ttu-id="b0d94-p107">Para obter dados detalhados de um período menor que sete dias, os dados deverão aparecer no prazo de 24 horas, mas a operação talvez não seja concluída em até 48 horas. Algumas pequenas alterações incrementais podem ocorrer por até cinco dias.</span><span class="sxs-lookup"><span data-stu-id="b0d94-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="b0d94-152">Para exibir relatórios detalhados de mensagens ocorridas em um período superior a sete dias, os resultados podem demorar umas poucas horas.</span><span class="sxs-lookup"><span data-stu-id="b0d94-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="b0d94-153">Dados de rastreamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="b0d94-153">Message trace data</span></span>  <br/> |<span data-ttu-id="b0d94-154">90 dias</span><span class="sxs-lookup"><span data-stu-id="b0d94-154">90 days</span></span>  <br/> |<span data-ttu-id="b0d94-155">Ao rastrear mensagens ocorridas em um período menor que 7 dias, as mensagens devem aparecer no intervalo de 5 a 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="b0d94-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="b0d94-156">Ao rastrear mensagens ocorridas em um período superior a 7 dias, os resultados podem demorar umas poucas horas.</span><span class="sxs-lookup"><span data-stu-id="b0d94-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b0d94-157">A disponibilidade e a latência de dados são as mesmas, sejam elas solicitadas por meio do Centro de administração do Office 365 ou pelo PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="b0d94-157">Data availability and latency is the same whether requested via the Office 365 admin center or remote PowerShell.</span></span> 
  

