---
title: Relatórios de supervisão
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: Usar relatórios de supervisão para ver quais e-mails conformidade precisa revisar e quem ele deve executar.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523653"
---
# <a name="supervision-reports"></a><span data-ttu-id="646f0-103">Relatórios de supervisão</span><span class="sxs-lookup"><span data-stu-id="646f0-103">Supervision reports</span></span>

<span data-ttu-id="646f0-p101">As diretivas de supervisão definem qual communications em sua organização precisam revisão para fins de conformidade e quem executará as revisões. Use os relatórios de supervisão para ver a atividade de revisão no nível de política e revisor. Para cada diretiva, você também pode exibir live estatísticas sobre o estado atual da atividade de revisão. [Saiba mais sobre as diretivas de supervisão](configure-supervision-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="646f0-p101">Supervision policies define which communications in your organization need review for compliance, and who will perform those reviews. Use the supervision reports to see the review activity at the policy and reviewer level. For each policy, you can also view live statistics on the current state of review activity. [Learn more about supervision policies ](configure-supervision-policies.md) .</span></span> 
  
> [!NOTE]
> <span data-ttu-id="646f0-p102">Usando diretivas de supervisão requer uma assinatura do Office 365 E5 para sua organização. Se você não tiver que plano e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="646f0-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="646f0-110">Você pode usar os relatórios de supervisão para:</span><span class="sxs-lookup"><span data-stu-id="646f0-110">You can use the supervision reports to:</span></span>
  
- <span data-ttu-id="646f0-111">Verificar se as suas políticas estão funcionando conforme pretendido.</span><span class="sxs-lookup"><span data-stu-id="646f0-111">Verify that your policies are working as you intended.</span></span> 
    
- <span data-ttu-id="646f0-112">Descubra quantos emails estão sendo identificados para revisão.</span><span class="sxs-lookup"><span data-stu-id="646f0-112">Find out how many emails are being identified for review.</span></span>
    
- <span data-ttu-id="646f0-p103">Descubra quantos emails não são compatíveis com e quais estão passando a revisão. Essas informações podem ajudá-lo a decidir se deseja ajustar suas políticas ou alterar o número de revisores.</span><span class="sxs-lookup"><span data-stu-id="646f0-p103">Find out how many emails aren't compliant and which ones are passing review. This information can help you decide whether to fine-tune your policies or change the number of reviewers.</span></span>
    
## <a name="view-the-supervision-report"></a><span data-ttu-id="646f0-115">Exibir o relatório de supervisão</span><span class="sxs-lookup"><span data-stu-id="646f0-115">View the Supervision report</span></span>

1. <span data-ttu-id="646f0-116">Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com/) usando as credenciais de uma conta de administrador em sua organização do Office 365 que tenha permissões para exibir relatórios de supervisão..</span><span class="sxs-lookup"><span data-stu-id="646f0-116">Sign into the [Security &amp; Compliance Center](https://protection.office.com/) using the credentials for an admin account in your Office 365 organization that has permissions to view supervision reports..</span></span> 
    
2. <span data-ttu-id="646f0-p104">Vá para **relatórios** \> **painel**. Você verá um relatório widget para supervisão e outros relatórios, você tem acesso ao.</span><span class="sxs-lookup"><span data-stu-id="646f0-p104">Go to **Reports** \> **Dashboard**. You'll see a reporting widget for supervision and other reports you have access to.</span></span>
    
3. <span data-ttu-id="646f0-119">Clique em widget **supervisão** para abrir a página de relatório detalhado.</span><span class="sxs-lookup"><span data-stu-id="646f0-119">Click the **Supervision** widget to open the detailed report page.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="646f0-p105">Se você não conseguir acessar a página de **relatórios** , verifique se você for um membro do grupo de função de análise de supervisão, conforme descrito em [tornar supervisão disponível na sua organização](configure-supervision-policies.md#SRavailable). Sejam incluídos na função grupo permite que você criar e gerenciar supervisão políticas e executar o relatório.</span><span class="sxs-lookup"><span data-stu-id="646f0-p105">If you aren't able to access the **Reports** page, check that you're a member of the Supervisory Review role group, as described in [Make supervision available in your organization](configure-supervision-policies.md#SRavailable). Being included in this role group lets you create and manage supervision polices and run the report.</span></span> 
  
## <a name="how-to-use-the-report"></a><span data-ttu-id="646f0-122">Como usar o relatório</span><span class="sxs-lookup"><span data-stu-id="646f0-122">How to use the report</span></span>

<span data-ttu-id="646f0-p106">Quando uma diretiva de supervisão identifica um email para revisão, o email é entregue a pasta de supervisão do revisor no Outlook e Outlook web app. Este relatório lista o nome da política de cada e o número de comunicações em cada estágio no processo de revisão.</span><span class="sxs-lookup"><span data-stu-id="646f0-p106">When a supervision policy identifies an email for review, the email is delivered to the reviewer's Supervision folder in Outlook and Outlook web app. This report lists each policy's name and the number of communications at each stage in the review process.</span></span>
  
<span data-ttu-id="646f0-125">Use o relatório para:</span><span class="sxs-lookup"><span data-stu-id="646f0-125">Use the report to:</span></span>
  
- <span data-ttu-id="646f0-126">Exibir dados para todos ou políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="646f0-126">View data for all or specific policies.</span></span>
    
- <span data-ttu-id="646f0-127">Exibir dados agrupados por tipo de marca (por exemplo, compatível, Questionable, etc.), revisor ou tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="646f0-127">View data grouped by tag type (such as Compliant, Questionable, etc.), reviewer, or message type.</span></span>
    
- <span data-ttu-id="646f0-128">Exporte dados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="646f0-128">Export data to a CSV file.</span></span>
    
- <span data-ttu-id="646f0-129">Filtre dados com base na data de revisão da atividade, tipo de marca, revisor, tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="646f0-129">Filter data based on review activity date, tag type, reviewer, message type.</span></span>
    
<span data-ttu-id="646f0-130">Aqui está uma divisão dos valores que talvez você veja na coluna **tipo de marca** .</span><span class="sxs-lookup"><span data-stu-id="646f0-130">Here's a breakdown of the values you might see in the **Tag type** column.</span></span> 
  
|<span data-ttu-id="646f0-131">**Tipo de marca**</span><span class="sxs-lookup"><span data-stu-id="646f0-131">**Tag type**</span></span>|<span data-ttu-id="646f0-132">**O que significa**</span><span class="sxs-lookup"><span data-stu-id="646f0-132">**What it means**</span></span>|
|:-----|:-----|
|<span data-ttu-id="646f0-133">Não examinado</span><span class="sxs-lookup"><span data-stu-id="646f0-133">Not Reviewed</span></span>  <br/> |<span data-ttu-id="646f0-p107">O número de emails que ainda não foram revisadas. Esses emails são Aguardando revisão na pasta de supervisão do revisor no Outlook.</span><span class="sxs-lookup"><span data-stu-id="646f0-p107">The number of emails that have not been reviewed yet. These emails are awaiting review in the reviewer's supervision folder in Outlook.</span></span>  <br/> |
|<span data-ttu-id="646f0-136">Compatível com</span><span class="sxs-lookup"><span data-stu-id="646f0-136">Compliant</span></span>  <br/> |<span data-ttu-id="646f0-p108">O número de emails revisado e marcado como compatível. Nenhuma ação adicional será necessária.</span><span class="sxs-lookup"><span data-stu-id="646f0-p108">The number of emails reviewed and marked as compliant. No further action is needed.</span></span>  <br/> |
|<span data-ttu-id="646f0-139">Questionáveis</span><span class="sxs-lookup"><span data-stu-id="646f0-139">Questionable</span></span>  <br/> |<span data-ttu-id="646f0-p109">O número de emails analisado e marcado questionável. Isso funciona como um sinalizador; outros revisores podem ajudar a verificar se um email precisa investigação para fins de conformidade.</span><span class="sxs-lookup"><span data-stu-id="646f0-p109">The number of emails reviewed and marked questionable. This acts as a flag; other reviewers can help check whether an email needs investigation for compliance.</span></span>  <br/> |
|<span data-ttu-id="646f0-142">Incompatíveis (ativo)</span><span class="sxs-lookup"><span data-stu-id="646f0-142">Non-Compliant (Active)</span></span>  <br/> |<span data-ttu-id="646f0-143">O número de emails não compatíveis que revisores estão atualmente investigando.</span><span class="sxs-lookup"><span data-stu-id="646f0-143">The number of non-compliant emails that reviewers are currently investigating.</span></span>  <br/> |
|<span data-ttu-id="646f0-144">Incompatíveis (resolvido)</span><span class="sxs-lookup"><span data-stu-id="646f0-144">Non-Compliant (Resolved)</span></span>  <br/> |<span data-ttu-id="646f0-145">O número de emails não compatíveis que revisores investigados e resolvido.</span><span class="sxs-lookup"><span data-stu-id="646f0-145">The number of non-compliant emails that reviewers investigated and resolved.</span></span>  <br/> |
   
## <a name="more-details"></a><span data-ttu-id="646f0-146">Mais detalhes</span><span class="sxs-lookup"><span data-stu-id="646f0-146">More details</span></span>

- <span data-ttu-id="646f0-147">Diretivas de supervisão primeiro devem ser provisionadas antes que eles serão exibidos nesse relatório.</span><span class="sxs-lookup"><span data-stu-id="646f0-147">Supervision policies must first be provisioned before they will appear in this report.</span></span>
    
- <span data-ttu-id="646f0-p110">Se as diretivas forem excluídas, dados históricos ainda são mostrados. No entanto, eles estiver indicados como "política inexistente" e a função **Exportar** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="646f0-p110">If policies are deleted, historical data is still shown. However, they're indicated as a "Non-existent policy", and the **Export** function isn't available.</span></span> 
    
- <span data-ttu-id="646f0-p111">Se o relatório não mostrar todos os dados por padrão, talvez seja porque o intervalo de datas atual não tem quaisquer dados para mostrar. Nesses casos, use o controle de **filtros** para alterar o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="646f0-p111">If the report doesn't show any data by default, it might be because the current date range doesn't have any data to show. In these cases, use the **Filters** control to change the date range.</span></span> 
    

