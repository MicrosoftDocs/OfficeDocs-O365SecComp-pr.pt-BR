---
title: Exibir relatórios de proteção de ameaça avançadas do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Saiba como encontrar e usar os relatórios para o Office 365 avançadas Threat Protection na segurança &amp; Centro de conformidade.
ms.openlocfilehash: a17f182f5c8d79e7863b26324a3c073ef18f14c9
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014943"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="2f803-103">Exibir relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="2f803-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="2f803-p101">Se sua organização tem [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP) e você tem as [permissões necessárias](#what-permissions-are-needed-to-view-these-reports), você pode usar vários relatórios ATP na segurança &amp; Centro de conformidade. (Vá para **relatórios** \> **Dashboard**.)</span><span class="sxs-lookup"><span data-stu-id="2f803-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="2f803-p102">Relatórios de ATP incluem o [relatório de Status de proteção de ameaça](#threat-protection-status-report), o [relatório de tipos de arquivo ATP](#atp-file-types-report)e o [relatório de disposição de mensagem ATP](#atp-message-disposition-report). Este artigo descreve os relatórios de ATP e inclui links para [Exibir os relatórios adicionais](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="2f803-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="2f803-109">Relatório de Status de proteção de ameaça</span><span class="sxs-lookup"><span data-stu-id="2f803-109">Threat Protection Status report</span></span>

<span data-ttu-id="2f803-p103">O relatório de **Status de proteção de ameaça** é um modo de exibição único que reúne informações sobre email mal-intencionado do conteúdo e mal-intencionados detectadas e bloqueadas pelo [Office 365 ATP](office-365-atp.md)e o [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP). O relatório fornece uma contagem agregada exclusivo de mensagens de email com conteúdo mal-intencionado (arquivos ou endereços de site (URLs)) bloqueado pelo mecanismo antimalware, [zero horas automático Limpar (ZAP)](zero-hour-auto-purge.md)e recursos de ATP, como [Links de seguros ATP](atp-safe-links.md), [ATP seguros Anexos](atp-safe-attachments.md)e [os recursos de AntiPhishing ATP](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="2f803-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2f803-p104">Um relatório de Status de proteção de ameaça está disponível para clientes que possuem [ATP do Office 365](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); No entanto, as informações exibidas no relatório de Status de proteção de ameaça para clientes ATP provavelmente irá conter dados diferentes de quais clientes EOP podem ver. Por exemplo, o relatório de Status de proteção de ameaça para clientes ATP irá conter informações sobre [arquivos mal-intencionados detectada no SharePoint Online, OneDrive ou equipes da Microsoft](atp-for-spo-odb-and-teams.md). Tais informações serão específicas para ATP, portanto, os clientes que tenham o EOP, mas não ATP não verá os detalhes em seu relatório de Status de proteção de ameaça.</span><span class="sxs-lookup"><span data-stu-id="2f803-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="2f803-115">Para exibir o relatório de Status de proteção de ameaça, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **O Status de proteção de ameaça**.</span><span class="sxs-lookup"><span data-stu-id="2f803-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Relatório de Status de proteção de ameaça ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="2f803-117">Para obter o status detalhado para um dia, passe o mouse sobre o gráfico.</span><span class="sxs-lookup"><span data-stu-id="2f803-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Dados de Status de proteção de ameaça ATP para um dia](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="2f803-p105">Por padrão, o relatório de Status de proteção de ameaça mostra dados para os últimos sete dias. No entanto, você pode escolher **filtros** e alterar o intervalo de datas para exibir dados por até 90 dias.</span><span class="sxs-lookup"><span data-stu-id="2f803-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Filtros do Status de proteção de ameaça ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="2f803-122">Você também pode usar o menu **Exibir dados por** alterar quais informações são exibidas no relatório.</span><span class="sxs-lookup"><span data-stu-id="2f803-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Opções de visualização para o relatório de Status de proteção de ameaça ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="2f803-124">Relatório de tipos de arquivo ATP</span><span class="sxs-lookup"><span data-stu-id="2f803-124">ATP File Types report</span></span>

<span data-ttu-id="2f803-125">O relatório de **Tipos de arquivo ATP** mostra o tipo de arquivos detectados como mal-intencionado por [ATP anexos de seguros](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="2f803-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="2f803-126">Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **ATP tipos de arquivo**.</span><span class="sxs-lookup"><span data-stu-id="2f803-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Relatório de tipos de arquivo ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="2f803-128">Quando você focaliza em um determinado dia, você pode ver a divisão dos tipos de arquivos mal-intencionado que foram detectados pelo [ATP anexos de seguros](atp-safe-attachments.md) e [antispam &amp; proteção antimalware no Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="2f803-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Dados de relatório de tipos de arquivo ATP por um dia](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="2f803-130">Relatório de disposição de mensagem ATP</span><span class="sxs-lookup"><span data-stu-id="2f803-130">ATP Message Disposition report</span></span>

<span data-ttu-id="2f803-131">O relatório de **Disposição de mensagem ATP** mostra as ações que foram feitas para mensagens de email que foram detectadas como tendo conteúdo mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="2f803-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="2f803-132">Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **ATP disposição de mensagem**.</span><span class="sxs-lookup"><span data-stu-id="2f803-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Relatório de descarte de mensagens de ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="2f803-134">Quando você focaliza uma barra no gráfico, você pode ver quais ações foram realizadas para email detectado daquele dia.</span><span class="sxs-lookup"><span data-stu-id="2f803-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Dados de relatório de descarte de mensagens ATP para um dia](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="2f803-136">Exibir os relatórios adicionais</span><span class="sxs-lookup"><span data-stu-id="2f803-136">Additional reports to view</span></span>

<span data-ttu-id="2f803-137">Além dos relatórios de ATP descritos neste artigo, vários outros relatórios estão disponíveis, conforme descrito na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="2f803-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>


|<span data-ttu-id="2f803-138">Tipo de relatório</span><span class="sxs-lookup"><span data-stu-id="2f803-138">Report type</span></span>  |<span data-ttu-id="2f803-139">Saiba mais</span><span class="sxs-lookup"><span data-stu-id="2f803-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="2f803-140">**Relatórios de segurança de email**, como uma parte superior de remetentes e destinatários relatório, um relatório de falsificação de email e um relatório detecções de Spam.</span><span class="sxs-lookup"><span data-stu-id="2f803-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="2f803-141">Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="2f803-142">**Explorer** (também conhecido como ameaça Explorer, isso é incluído no [Office 365 Threat Intelligence](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="2f803-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="2f803-143">Use o Explorer na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="2f803-p106">**Resultados do EOP e ATP** (Isto é um relatório personalizado que você gera usando o PowerShell). Este relatório contém informações, como o domínio, data, tipo de evento, direção, ação e contagem de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2f803-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="2f803-146">Referência do cmdlet Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="2f803-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="2f803-p107">**Detecções de EOP e ATP** (Isto é um relatório personalizado que você gera usando o PowerShell). Este relatório contém detalhes sobre arquivos mal-intencionados ou URLs, tentativas de phishing, representação e outras possíveis ameaças em arquivos ou email.</span><span class="sxs-lookup"><span data-stu-id="2f803-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="2f803-149">Referência do cmdlet Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="2f803-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="2f803-150">Quais permissões são necessárias para exibir os relatórios de ATP?</span><span class="sxs-lookup"><span data-stu-id="2f803-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="2f803-151">Para exibir e usar os relatórios descritos neste artigo, **você deve ter uma função apropriada atribuída em ambos os a segurança &amp; Centro de conformidade e Exchange Admin Center**.</span><span class="sxs-lookup"><span data-stu-id="2f803-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned in both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="2f803-152">Para obter a segurança &amp; Centro de conformidade, você deve ter uma das seguintes funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="2f803-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="2f803-153">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="2f803-153">Organization Management</span></span>
    - <span data-ttu-id="2f803-154">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="2f803-154">Security Administrator</span></span>
    - <span data-ttu-id="2f803-155">Leitor de segurança</span><span class="sxs-lookup"><span data-stu-id="2f803-155">Security Reader</span></span>

- <span data-ttu-id="2f803-156">Para o Exchange Online, você deve ter uma das seguintes funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="2f803-156">For Exchange Online, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="2f803-157">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="2f803-157">Organization Management</span></span>
    - <span data-ttu-id="2f803-158">Gerenciamento de Organização Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="2f803-158">View-only Organization Management</span></span>
    - <span data-ttu-id="2f803-159">Função de Destinatários Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="2f803-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="2f803-160">Gerenciamento de Conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-160">Compliance Management</span></span>

<span data-ttu-id="2f803-161">Para saber mais, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="2f803-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="2f803-162">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="2f803-163">Permissões de recursos no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2f803-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="2f803-164">Se os relatórios não são mostrando dados?</span><span class="sxs-lookup"><span data-stu-id="2f803-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="2f803-p108">Se você não está vendo dados em seus relatórios ATP, confira a suas políticas estão configuradas corretamente. Sua organização deve ter [políticas de Links de ATP seguros](set-up-atp-safe-links-policies.md) e [anexos de seguros ATP políticas](set-up-atp-safe-attachments-policies.md) definidas na ordem de proteção de ATP estar em vigor. Consulte também a [proteção antispam e antimalware no Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="2f803-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="2f803-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f803-168">Related topics</span></span>

[<span data-ttu-id="2f803-169">Relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="2f803-170">Para criar um cronograma para um relatório na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="2f803-171">Configurar e fazer o download de um relatório personalizado na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="2f803-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

