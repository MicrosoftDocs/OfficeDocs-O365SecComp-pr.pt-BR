---
title: Exibir relatórios de segurança de email no &amp; centro de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection: M365-security-compliance
description: Saiba como encontrar e usar relatórios de segurança de email para sua organização com o Office 365 Enterprise. Relatórios de segurança de email estão disponíveis no &amp; centro de conformidade de segurança.
ms.openlocfilehash: 809bfbdfdda8bd1ed9b88c9bca7e9ce14d774868
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216411"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="9a5e0-104">Exibir relatórios de segurança de email no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="9a5e0-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="9a5e0-p102">Vários relatórios de segurança de email estão disponíveis no [centro de &amp; conformidade de segurança](https://security.microsoft.com) para ajudá-lo a ver como os recursos antispam e antimalware no Office 365 estão protegendo sua organização. Se você tiver as [permissões necessárias](#what-permissions-are-needed-to-view-these-reports), poderá exibir esses relatórios no centro de conformidade &amp; de segurança acessando o **painel**de **relatórios** \> .</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p102">A variety of email security reports are available in the [Security &amp; Compliance Center](https://security.microsoft.com) to help you see how anti-spam and anti-malware features in Office 365 are protecting your organization. If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![O painel &amp; do centro de conformidade de segurança pode ajudá-lo a ver onde a proteção avançada contra ameaças está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="9a5e0-108">Os relatórios de segurança de email incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a5e0-108">Your email security reports include the following:</span></span>
  
- [<span data-ttu-id="9a5e0-109">Relatório de status de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="9a5e0-109">Threat Protection Status report</span></span>](view-email-security-reports.md#tps) 
    
- [<span data-ttu-id="9a5e0-110">Relatório de detecções de malware</span><span class="sxs-lookup"><span data-stu-id="9a5e0-110">Malware Detections report</span></span>](view-email-security-reports.md#maldet)
    
- [<span data-ttu-id="9a5e0-111">Relatório de malware superior</span><span class="sxs-lookup"><span data-stu-id="9a5e0-111">Top Malware report</span></span>](#top-malware-report)
    
- [<span data-ttu-id="9a5e0-112">Relatório de principais remetentes e destinatários</span><span class="sxs-lookup"><span data-stu-id="9a5e0-112">Top Senders and Recipients report</span></span>](view-email-security-reports.md#topsenders)
    
- [<span data-ttu-id="9a5e0-113">Relatório de falsificação de email</span><span class="sxs-lookup"><span data-stu-id="9a5e0-113">Spoof Mail report</span></span>](#spoof-mail-report)
    
- [<span data-ttu-id="9a5e0-114">Relatório de detecções de spam</span><span class="sxs-lookup"><span data-stu-id="9a5e0-114">Spam Detections report</span></span>](#spam-detections-report)
    
- [<span data-ttu-id="9a5e0-115">Relatório de email enviado e recebido</span><span class="sxs-lookup"><span data-stu-id="9a5e0-115">Sent and received email report</span></span>](view-email-security-reports.md#sentreceivedemail)
    
- <span data-ttu-id="9a5e0-116">[Relatório de mensagens relatadas pelo usuário](view-email-security-reports.md#userreported) (novo!)</span><span class="sxs-lookup"><span data-stu-id="9a5e0-116">[User-reported messages report](view-email-security-reports.md#userreported) (new!)</span></span> 
    
## <a name="threat-protection-status-report"></a><span data-ttu-id="9a5e0-117">Relatório de status de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="9a5e0-117">Threat Protection Status report</span></span>

<span data-ttu-id="9a5e0-p103">O novo relatório de **status de proteção contra ameaças** é um relatório inteligente que mostra emails mal-intencionados que foram detectados e bloqueados pela proteção do Exchange Online. Este relatório mostra informações sobre o email identificado como malware ou uma tentativa de phishing.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p103">The new **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection. This report shows information about email identified as malware or a phishing attempt.</span></span> 

> [!NOTE]
> <span data-ttu-id="9a5e0-p104">Um relatório de status de proteção contra ameaças está disponível para clientes que tenham o [Office 365 ATP](office-365-atp.md) ou o [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); no entanto, as informações exibidas no relatório de status de proteção contra ameaças para clientes ATP provavelmente conterão dados diferentes do que os clientes do EOP podem ver. Por exemplo, os clientes do EOP podem exibir informações sobre malware detectado no email, mas não informações sobre [arquivos mal-intencionados detectados no SharePoint Online, no onedrive ou no Microsoft Teams](atp-for-spo-odb-and-teams.md), um recurso específico de ATP. ([Saiba mais sobre os relatórios de ATP](view-reports-for-atp.md).)</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md), an ATP-specific capability. ([Learn more about ATP reports](view-reports-for-atp.md).)</span></span>
  
<span data-ttu-id="9a5e0-123">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para o **painel** \> **relatórios** \> **status de proteção contra ameaças**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-123">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Relatório de status de proteção contra ameaças](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="9a5e0-p105">Quando você abre o relatório de status de proteção contra ameaças pela primeira vez, o relatório mostra os dados dos últimos sete dias por padrão; no entanto, você pode clicar em **filtros** e alterar o intervalo de datas para até 90 dias de detalhes. Este relatório é útil para ver a eficácia e o impacto dos recursos de proteção do Exchange Online da sua organização e para tendência de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p105">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail. This report is useful for viewing the effectiveness and impact of your organization's Exchange Online Protection features, and for longer-term trending.</span></span> 
  
![Filtros de relatório de status de proteção contra ameaças](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="9a5e0-128">Você também pode escolher se deseja exibir dados para emails identificados como mal-intencionados, emails identificados como tentativas de phishing ou emails identificados como contendo malware.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-128">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![Opções de exibição do relatório de status de proteção contra ameaças](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="9a5e0-130">Relatório de detecções de malware</span><span class="sxs-lookup"><span data-stu-id="9a5e0-130">Malware Detections report</span></span>

<span data-ttu-id="9a5e0-131">O relatório de **detecções de malware** mostra quantas mensagens de entrada e saída foram detectadas como contendo malware para sua organização.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-131">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="9a5e0-132">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para relatórios de **malware**de **painel** \> de **relatórios** \> .</span><span class="sxs-lookup"><span data-stu-id="9a5e0-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![Exemplo de relatório de detecções de malware](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="9a5e0-p106">Semelhante a outros relatórios, como o relatório de status de proteção contra ameaças, o relatório exibe dados dos últimos sete dias por padrão. No enTanto, você pode escolher **filtros** para alterar o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p106">Similar to other reports, like the Threat Protection Status report, the report displays data for the past seven days by default. However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="9a5e0-136">Relatório de malware superior</span><span class="sxs-lookup"><span data-stu-id="9a5e0-136">Top Malware report</span></span>

<span data-ttu-id="9a5e0-137">O relatório de **malware superior** mostra os vários tipos de malware detectados pelo Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-137">The **Top Malware** report shows the various kinds of malware that was detected by Exchange Online.</span></span> 
  
<span data-ttu-id="9a5e0-138">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para **painel** \> de **relatórios** \> de **malware superior**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-138">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![Malware EOP superior](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="9a5e0-140">Ao passar o mouse sobre uma fatia no gráfico de pizza, você pode ver o nome de um tipo de malware e quantas mensagens foram detectadas como tendo esse malware.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-140">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="9a5e0-141">Clique (ou toque) no relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-141">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Este relatório mostra o malware superior detectado para sua organização](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="9a5e0-143">Abaixo do gráfico, você verá uma lista de malware detectado e quantas mensagens foram detectadas como tendo esse malware.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-143">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="9a5e0-144">Relatório de principais remetentes e destinatários</span><span class="sxs-lookup"><span data-stu-id="9a5e0-144">Top Senders and Recipients report</span></span>

<span data-ttu-id="9a5e0-145">O relatório de **remetentes e destinatários principais** é um gráfico de pizza mostrando seus principais remetentes de email.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-145">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="9a5e0-146">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para **painel** \> de **relatórios** \> **principais remetentes e destinatários**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-146">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![Para exibir esse relatório, no centro de &amp; conformidade de segurança, vá para \> painel \> de relatórios principais remetentes e destinatários](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="9a5e0-148">Ao passar o mouse sobre uma fatia no gráfico de pizza, você pode ver uma contagem de mensagens enviadas ou recebidas.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-148">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="9a5e0-149">Clique (ou toque) no relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-149">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="9a5e0-p107">Use a lista **Mostrar dados de** para escolher se deseja exibir dados para os remetentes principais, receptores, destinatários de spam e destinatários de malware. Você também pode ver quem recebeu o malware que foi detectado pela proteção avançada contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p107">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients. You can also see who received malware that was detected by Advanced Threat Protection.</span></span> 
  
![Use a lista Mostrar dados para exibir informações específicas](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="9a5e0-153">Abaixo do gráfico, você verá quem os principais remetentes ou destinatários de emails foram, juntamente com uma contagem de mensagens enviadas ou recebidas pelo período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-153">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-mail-report"></a><span data-ttu-id="9a5e0-154">Relatório de falsificação de email</span><span class="sxs-lookup"><span data-stu-id="9a5e0-154">Spoof Mail report</span></span>

<span data-ttu-id="9a5e0-155">O relatório de **email** de falsificação mostra quantas mensagens de email de falsificação foram detectadas, e delas, que foram consideradas "boas" (emails falsos realizados por motivos de negócios legítimos).</span><span class="sxs-lookup"><span data-stu-id="9a5e0-155">The **Spoof Mail** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="9a5e0-156">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para **relatório** \> de falsificação de **painel** \> \*\*\*\* de relatórios.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-156">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![Para exibir esse relatório, no centro de &amp; conformidade de segurança, vá para \> o \> painel relatórios email de spoof](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="9a5e0-158">Ao passar o mouse sobre um dia no gráfico, você pode ver quantas mensagens de email de falsificação foram recebidas.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-158">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="9a5e0-159">Clique (ou toque) no relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-159">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="9a5e0-160">Relatório de detecções de spam</span><span class="sxs-lookup"><span data-stu-id="9a5e0-160">Spam Detections report</span></span>

<span data-ttu-id="9a5e0-161">O relatório **detecções de spam** mostra todo o conteúdo de spam bloqueado pelo Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-161">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> 
  
<span data-ttu-id="9a5e0-162">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para relatórios de **spam**de **painel** \> de **relatórios** \> .</span><span class="sxs-lookup"><span data-stu-id="9a5e0-162">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![Para exibir esse relatório, no centro de &amp; conformidade de segurança, vá para \> painel \> de relatórios EOP detecções de spam](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="9a5e0-p108">Ao passar o mouse sobre um dia no gráfico, você pode ver quantos itens foram bloqueados naquele dia, bem como os itens são categorizados. Por exemplo, você pode ver quantas mensagens de spam foram filtradas e quantos itens vieram de um endereço IP bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p108">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized. For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="9a5e0-166">Clique (ou toque) no relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-166">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![O relatório de detecções de spam informa quantas mensagens de spam foram bloqueadas ou filtradas](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="9a5e0-p109">Abaixo do gráfico, você verá uma lista de itens de spam que foram detectados. Selecione um item para exibir informações adicionais, como se o item de spam era de entrada ou de saída, sua ID de mensagem e seu destinatário.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p109">Below the chart, you'll see a list of spam items that were detected. Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="9a5e0-170">Relatório de email enviado e recebido</span><span class="sxs-lookup"><span data-stu-id="9a5e0-170">Sent and received email report</span></span>

<span data-ttu-id="9a5e0-171">O relatório de **email enviado e recebido** é um relatório inteligente que mostra informações sobre emails de entrada e saída, incluindo detecções de spam, malware e email identificados como "bom".</span><span class="sxs-lookup"><span data-stu-id="9a5e0-171">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="9a5e0-172">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), vá para o **painel** \> **relatórios** \> **enviado e recebido emails**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-172">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![Para exibir esse relatório, no centro de &amp; conformidade de segurança, vá para \> o \> painel relatórios enviado e recebido email](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="9a5e0-p110">Ao passar o mouse sobre um dia no gráfico, você pode ver quantas mensagens vieram e como essas mensagens são categorizadas. Por exemplo, você pode ver quantas mensagens foram detectadas como contendo malware e quantas foram identificadas como spam.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p110">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized. For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="9a5e0-176">Clique (ou toque) no relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-176">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="9a5e0-177">Você pode usar a lista **dividir por** para exibir informações por tipo ou por direção (entrada e saída).</span><span class="sxs-lookup"><span data-stu-id="9a5e0-177">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![Use a lista dividir por para exibir informações por tipo ou direção](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="9a5e0-p111">Abaixo do gráfico, você verá uma lista de categorias de email, como **GoodMail**, **SpamContentFiltered**e assim por diante. Selecione uma categoria para exibir informações adicionais, como ações que foram tomadas para malware e se o email era de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p111">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on. Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![Este relatório informa sobre o anti-malware, antispam e outras detecções de mensagens](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a><span data-ttu-id="9a5e0-182">Relatório de mensagens relatadas pelo usuário (novo!)</span><span class="sxs-lookup"><span data-stu-id="9a5e0-182">User-reported messages report (new!)</span></span>

<span data-ttu-id="9a5e0-183">O relatório de mensagens relatadas pelo **usuário** mostra informações sobre as mensagens de email que os usuários relataram como lixo eletrônico, tentativas de phishing ou emails de boa qualidade usando o suplemento de [mensagem de relatório](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="9a5e0-183">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md).</span></span>
  
<span data-ttu-id="9a5e0-p112">Os detalhes estão disponíveis para cada mensagem, incluindo o motivo da entrega, como uma exceção de política de spam ou uma regra de fluxo de email configurada para sua organização. Para exibir detalhes, selecione um item na lista relatórios do usuário e, em seguida, exiba as informações nas guias **Resumo** e **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p112">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization. To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![O relatório mensagens reLatadas pelo usuário mostra as mensagens que os usuários rotularam como lixo eletrônico, não lixo eletrônico ou tentativas de phishing.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="9a5e0-187">Para exibir esse relatório, no [centro de &amp; conformidade de segurança](https://protection.office.com), siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="9a5e0-187">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), do one of the following:</span></span>
  
- <span data-ttu-id="9a5e0-188">Vá para o **painel** \> **Gerenciamento** \> **de ameaças mensagens relatadas pelo usuário**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-188">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="9a5e0-189">Vá para **Gerenciamento** \> de ameaças **revise** \> **mensagens relatadas pelo usuário**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-189">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![No centro de &amp; conformidade de segurança, escolha revisão \> \> de gerenciamento de ameaças mensagens relatadas pelo usuário](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="9a5e0-p113">Para que o relatório de mensagens relatadas pelo usuário funcione corretamente, o **log de auditoria deve estar ativado** para o seu ambiente do Office 365. Isso geralmente é feito por alguém que tenha a função de logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p113">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="9a5e0-194">Quais permissões são necessárias para exibir esses relatórios?</span><span class="sxs-lookup"><span data-stu-id="9a5e0-194">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="9a5e0-195">Para exibir e usar os relatórios descritos neste artigo, **você deve ter uma função apropriada atribuída para o centro de conformidade de segurança &amp; e o centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="9a5e0-195">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="9a5e0-196">Para o centro &amp; de conformidade de segurança, você deve ter uma das seguintes funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="9a5e0-196">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="9a5e0-197">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="9a5e0-197">Organization Management</span></span>
    - <span data-ttu-id="9a5e0-198">Administrador de segurança (isso pode ser atribuído no centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()</span><span class="sxs-lookup"><span data-stu-id="9a5e0-198">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>
    - <span data-ttu-id="9a5e0-199">Leitor de segurança</span><span class="sxs-lookup"><span data-stu-id="9a5e0-199">Security Reader</span></span>

- <span data-ttu-id="9a5e0-200">Para o Exchange Online, você deve ter uma das seguintes funções atribuídas no centro de administração do Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() ou com cmdlets do PowerShell (Confira [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="9a5e0-200">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="9a5e0-201">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="9a5e0-201">Organization Management</span></span>
    - <span data-ttu-id="9a5e0-202">Gerenciamento de Organização Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="9a5e0-202">View-only Organization Management</span></span>
    - <span data-ttu-id="9a5e0-203">Função de Destinatários Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="9a5e0-203">View-Only Recipients role</span></span>
    - <span data-ttu-id="9a5e0-204">Gerenciamento de Conformidade</span><span class="sxs-lookup"><span data-stu-id="9a5e0-204">Compliance Management</span></span>

<span data-ttu-id="9a5e0-205">Para saber mais, confira os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="9a5e0-205">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="9a5e0-206">Permissões no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="9a5e0-206">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="9a5e0-207">Permissões de recursos no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="9a5e0-207">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="9a5e0-208">E se os relatórios não estiverem mostrando dados?</span><span class="sxs-lookup"><span data-stu-id="9a5e0-208">What if the reports aren't showing data?</span></span>

<span data-ttu-id="9a5e0-p114">Se você não estiver vendo dados nos seus relatórios, verifique se as suas políticas estão configuradas corretamente. Para saber mais, consulte [anti-spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="9a5e0-p114">If you are not seeing data in your reports, double-check that your policies are set up correctly. To learn more, see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="9a5e0-211">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a5e0-211">Related topics</span></span>

[<span data-ttu-id="9a5e0-212">Proteção anti-spam de emails do Office 365</span><span class="sxs-lookup"><span data-stu-id="9a5e0-212">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="9a5e0-213">Relatórios e insights no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="9a5e0-213">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="9a5e0-214">Criar um cronograma para um relatório no centro de &amp; conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="9a5e0-214">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="9a5e0-215">Configurar e baixar um relatório personalizado no centro de conformidade &amp; de segurança</span><span class="sxs-lookup"><span data-stu-id="9a5e0-215">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

