---
title: Exibir os relatórios de prevenção contra perda de dados
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Com os relatórios DLP no Office 365, você pode exibir rapidamente o número de correspondências de política DLP, substituições ou falsos positivos; Consulte se eles estiver tendências para cima ou para baixo ao longo do tempo; Filtrar o relatório de maneiras diferentes; e exibir os detalhes adicionais, selecionando um ponto em uma linha no gráfico.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013905"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="cba36-103">Exibir os relatórios de prevenção contra perda de dados</span><span class="sxs-lookup"><span data-stu-id="cba36-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="cba36-p101">Depois de criar sua perda de dados políticas prevention (DLP), você vai querer verificar se ele estão funcionando conforme você destinada e ajudá-lo a permanecer em conformidade. Com o DLP relatórios na segurança do Office 365 &amp; Centro de conformidade, você pode visualizar rapidamente:</span><span class="sxs-lookup"><span data-stu-id="cba36-p101">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant. With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="cba36-p102">**Correspondências de política DLP** Este relatório mostra a contagem de correspondências de política DLP ao longo do tempo. Você pode filtrar o relatório por data, local, política ou ação. Você pode usar este relatório para:</span><span class="sxs-lookup"><span data-stu-id="cba36-p102">**DLP policy matches** This report shows the count of DLP policy matches over time. You can filter the report by date, location, policy, or action. You can use this report to:</span></span> 
    
  - <span data-ttu-id="cba36-p103">Ajustar ou refinar suas políticas de DLP conforme você executá-los no modo de teste. Você pode exibir a regra específica que correspondem o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cba36-p103">Tune or refine your DLP policies as you run them in test mode. You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="cba36-111">Se concentrar em períodos de tempo específicos e entender os motivos para picos e tendências.</span><span class="sxs-lookup"><span data-stu-id="cba36-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="cba36-112">Descubra os processos de negócios que violam as políticas de DLP da sua organização.</span><span class="sxs-lookup"><span data-stu-id="cba36-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="cba36-113">Compreenda qualquer impacto nos negócios das diretivas DLP, conferindo quais ações estão sendo aplicadas ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cba36-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="cba36-114">Verificar a conformidade com uma determinada política DLP mostrando as correspondências dessa política.</span><span class="sxs-lookup"><span data-stu-id="cba36-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="cba36-115">Exibir uma lista dos principais usuários e repita a usuários que estão contribuindo para incidentes em sua organização.</span><span class="sxs-lookup"><span data-stu-id="cba36-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="cba36-116">Exiba uma lista dos principais tipos de informações confidenciais em sua organização.</span><span class="sxs-lookup"><span data-stu-id="cba36-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="cba36-p104">**Incidentes DLP** Este relatório também mostra correspondências de política ao longo do tempo, como a política faz a correspondência de relatório. No entanto, a política corresponde correspondências de apresentações de relatório em um nível de regra; Por exemplo, se um email correspondida três regras diferentes, a correspondências de política relatório mostra três diferentes itens de linha. Em contrapartida, o relatório de incidentes mostra correspondências em um nível de item; Por exemplo, se um email correspondida três regras diferentes, o relatório de incidentes mostra um único item de linha para essa parte do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cba36-p104">**DLP incidents** This report also shows policy matches over time, like the policy matches report. However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items. By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="cba36-p105">Porque as contagens de relatório são agregadas de forma diferente, o relatório de correspondências de política é melhor para identificando correspondências com regras específicas e ajuste fino políticas de DLP. O relatório de incidentes é melhor para identificar partes específicas de conteúdo que são problemáticos para suas políticas de DLP.</span><span class="sxs-lookup"><span data-stu-id="cba36-p105">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies. The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="cba36-p106">**Substituições e falsos positivos DLP** Se a sua política DLP permite aos usuários substituí-la ou relatar um falso positivo, esse relatório mostra uma contagem de tais instâncias ao longo do tempo. Você pode filtrar o relatório por data, local ou política. Você pode usar este relatório para:</span><span class="sxs-lookup"><span data-stu-id="cba36-p106">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time. You can filter the report by date, location, or policy. You can use this report to:</span></span> 
    
  - <span data-ttu-id="cba36-125">Ajustar ou refinar suas políticas de DLP, conferindo quais políticas incorrem um alto número de falsos positivos.</span><span class="sxs-lookup"><span data-stu-id="cba36-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="cba36-126">Exiba as justificativas enviadas pelos usuários quando eles resolvem uma dica de política, substituindo a política.</span><span class="sxs-lookup"><span data-stu-id="cba36-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="cba36-127">Descobrir onde o conflito de políticas DLP com processos de negócios válida por incorrer em um alto número de usuário substitui.</span><span class="sxs-lookup"><span data-stu-id="cba36-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="cba36-p107">Todos os relatórios DLP podem mostrar dados desde o período de tempo de quatro meses mais recente. Os dados mais recentes podem demorar até 24 horas apareça nos relatórios.</span><span class="sxs-lookup"><span data-stu-id="cba36-p107">All DLP reports can show data from the most recent four-month time period. The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="cba36-130">Você pode encontrar esses relatórios na segurança &amp; Centro de conformidade \> **relatórios** \> **painel**.</span><span class="sxs-lookup"><span data-stu-id="cba36-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![Relatório de correspondências de política DLP](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="cba36-132">Exibir a justificação enviada por um usuário para uma substituição</span><span class="sxs-lookup"><span data-stu-id="cba36-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="cba36-133">Se sua política DLP permite que os usuários substituí-la, use o falso positivo e substituir o relatório para exibir o texto enviado por usuários na dica de política.</span><span class="sxs-lookup"><span data-stu-id="cba36-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Campo justificativa nos detalhes do relatório de substituição de falso positivo DLP e](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="cba36-135">Combater ideias e recomendações</span><span class="sxs-lookup"><span data-stu-id="cba36-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="cba36-136">Relatórios podem mostrar ideias e recomendações, onde você pode clicar no ícone de aviso vermelho para ver detalhes específicos sobre possíveis problemas e tomar corretivas possíveis.</span><span class="sxs-lookup"><span data-stu-id="cba36-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![Clicar em um ícone de ideias para ver os detalhes e ações a serem tomadas](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="cba36-138">Encontre os cmdlets para os relatórios DLP</span><span class="sxs-lookup"><span data-stu-id="cba36-138">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="cba36-139">Para usar a maioria dos cmdlets para a segurança &amp; Centro de conformidade, você precisa:</span><span class="sxs-lookup"><span data-stu-id="cba36-139">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="cba36-140">Conecte-se para a segurança do Office 365 &amp; usando o PowerShell remoto do Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="cba36-140">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="cba36-141">Use qualquer uma dessas [a segurança do Office 365 &amp; cmdlets do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="cba36-141">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="cba36-p108">No entanto, os relatórios DLP precisam receber dados dos across Office 365, incluindo o Exchange Online. Por esse motivo, os cmdlets para os relatórios de DLP estão disponíveis no Exchange Online Powershell — não na segurança &amp; Powershell do Centro de conformidade. Portanto, para usar os cmdlets para os relatórios de DLP, você precisa:</span><span class="sxs-lookup"><span data-stu-id="cba36-p108">However, DLP reports need pull data from across Office 365, including Exchange Online. For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell. Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="cba36-145">Conectar-se ao Exchange Online usando o PowerShell remoto</span><span class="sxs-lookup"><span data-stu-id="cba36-145">Connect to Exchange Online using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="cba36-146">Use qualquer um desses cmdlets para os relatórios de DLP:</span><span class="sxs-lookup"><span data-stu-id="cba36-146">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="cba36-147">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="cba36-147">Get-DlpDetectionsReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="cba36-148">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="cba36-148">Get-DlpDetailReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

