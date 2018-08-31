---
title: Marcação e avaliação na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Revise as etapas para executar o treinamento de avaliação, incluindo arquivos de marcação e revisar os resultados da avaliação no eDiscovery avançadas do Office 365. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523924"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="2cbbd-103">Marcação e avaliação na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2cbbd-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="2cbbd-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="2cbbd-106">Esta seção descreve o procedimento para o módulo de avaliação de relevância de eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="2cbbd-107">Executando a análise e treinamento da avaliação</span><span class="sxs-lookup"><span data-stu-id="2cbbd-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="2cbbd-108">No **relevância \> Track** , clique em **avaliação** para iniciar a avaliação casos.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="2cbbd-109">Por exemplo, fins deste procedimento, um conjunto de avaliação de amostra de 500 arquivos é criado e na guia **marca** for exibida, que contém o painel de marcação, o conteúdo do arquivo exibido e outras opções de marca.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![Guia Marca de Relevância para Avaliação](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="2cbbd-111">Revisar cada arquivo na amostra, determinar a relevância do arquivo para cada questão de maiusculas e marcar o arquivo usando o Relevance (R), não relevante (NR) e evitar botões no painel do **Painel de marcação** .</span><span class="sxs-lookup"><span data-stu-id="2cbbd-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="2cbbd-p102">Avaliação requer 500 arquivos marcados. Se os arquivos são "ignorados", você receberá mais arquivos a marca.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="2cbbd-114">Após todos os arquivos na amostra de marcação, clique em **Calcular**.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="2cbbd-p103">Margem de erro atual de avaliação e riqueza são calculadas e exibidas na guia **Faixa de relevância** , com detalhes expandidas por problema, conforme mostrado abaixo. Para obter mais detalhes sobre essa caixa de diálogo são descritos na seção posterior "Resultados de avaliações de revisão".</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![Controle de relevância - avaliação](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="2cbbd-p104">Por padrão, é recomendável que você prossiga para a próxima etapa do padrão quando o indicador de progresso de avaliação para o problema for concluído, indicando que a amostra de avaliação foi revisada e arquivos relevantes suficientes foram marcados. > Caso contrário, se você quiser exibir os resultados da guia **controlar** e a margem de erro e a próxima etapa de controle, clique em **Modificar** adjacente à **Próxima etapa**, selecione **Continuar avaliação**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="2cbbd-p105">Clique em **Modificar** à direita da caixa de seleção de **avaliação** para exibir e especifique os parâmetros de avaliação por problema. Uma caixa de diálogo de **nível de avaliação** para cada questão for exibida, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![Problema de caso de nível de avaliação](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="2cbbd-123">Os seguintes parâmetros para o problema são calculados e exibidos na caixa de diálogo **nível de avaliação** :</span><span class="sxs-lookup"><span data-stu-id="2cbbd-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="2cbbd-p106">**Estimativas de margem de erro de destino para Recordação**: com base nesse valor, o número estimado de arquivos adicionais necessários para analisar é calculado. A margem utilizada para Recordação é mais de 75% e com um nível de confiança de 95%.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="2cbbd-126">**Arquivos de avaliação adicionais necessários**: indica quantas mais arquivos são necessários se os requisitos da margem de erro atual não foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="2cbbd-127">Para ajustar a margem de erro atual e ver o efeito das margens de erro diferente (por problema):</span><span class="sxs-lookup"><span data-stu-id="2cbbd-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="2cbbd-128">Na lista **Selecione o problema** , selecione um problema.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="2cbbd-129">Na **margem de erro de destino para Recordação estima**, insira um novo valor.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="2cbbd-130">Clique em **atualizar valores** para ver o impacto dos ajustes.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="2cbbd-131">Clique em **Avançado** na caixa de diálogo **nível de avaliação** para ver os seguintes parâmetros adicionais e detalhes:</span><span class="sxs-lookup"><span data-stu-id="2cbbd-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![Exibição avançada de problema de caso de nível de avaliação](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="2cbbd-133">**Riqueza estimado**: estimado riqueza de acordo com os resultados atuais de avaliação</span><span class="sxs-lookup"><span data-stu-id="2cbbd-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="2cbbd-p107">**Para Recordação presumida**: por padrão, a margem de erro de destino se aplica para recuperá-lo acima de 75%. Clique em **Editar** alterar esse parâmetro e controlar a margem de erro em um intervalo diferente de valores de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="2cbbd-p108">**Nível de confiança**: por padrão, a margem de erro recomendados para a confiança é 95%. Clique em **Editar** , se você quiser alterar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="2cbbd-138">**Margem de erro riqueza Expected**: dado os valores atualizados, trate a esperado margem de erro da sofisticação, depois que todos os arquivos de avaliação adicionais sejam revisados.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="2cbbd-139">**Arquivos de avaliação adicionais necessários**: dado os valores atualizados, o número de avaliação adicional arquivos que precisam ser revisados para alcançar o destino.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="2cbbd-140">**Arquivos de avaliação total necessário**: total de dado os valores atualizados, arquivos de avaliação necessários para revisão.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="2cbbd-141">**Número de expected de arquivos relevantes na avaliação**: dado os valores atualizados, o número esperado de arquivos relevantes na avaliação inteira depois que todos os arquivos de avaliação adicionais sejam revisados.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="2cbbd-p109">Clique em **recalcular valores**, se os parâmetros forem alterados. Quando tiver terminado, se houver um problema, clique em **Okey** para salvar as alterações (ou **próximo** quando há várias questões para revisar ou modificar e, em seguida, **término**).</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="2cbbd-144">Quando há várias questões, depois que todos os problemas foram revisados ou ajustados, um **nível de avaliação: Resumo** caixa de diálogo é exibida, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Resumo do nível de análise](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="2cbbd-146">Após a conclusão bem-sucedida da avaliação, vá para o próximo estágio no treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="2cbbd-147">Revisar os resultados da avaliação</span><span class="sxs-lookup"><span data-stu-id="2cbbd-147">Reviewing assessment results</span></span>

<span data-ttu-id="2cbbd-148">Após uma amostra da avaliação é marcada, os resultados da avaliação são calculados e exibidos na guia faixa de relevância.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="2cbbd-149">Os seguintes resultados são exibidos na exibição Track expandida:</span><span class="sxs-lookup"><span data-stu-id="2cbbd-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="2cbbd-150">Estimativas de margem de erro atual Assessment para Recordação</span><span class="sxs-lookup"><span data-stu-id="2cbbd-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="2cbbd-151">Riqueza estimada</span><span class="sxs-lookup"><span data-stu-id="2cbbd-151">Estimated richness</span></span>
    
- <span data-ttu-id="2cbbd-152">Arquivos de avaliação adicionais necessários (para revisão)</span><span class="sxs-lookup"><span data-stu-id="2cbbd-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="2cbbd-p110">A margem de erro Assessment atual é a margem de erro recomendada por eDiscovery avançado. O número exibido para os "arquivos avaliação adicionais necessários" corresponde a essa recomendação.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="2cbbd-p111">O indicador de progresso Assessment mostra o nível de conclusão da avaliação, dada a margem de erro atual. Quando a avaliação estiver em andamento, o usuário será marcar outro exemplo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="2cbbd-157">Quando o indicador de progresso assessment mostra assessment como concluído, isso significa que a revisão de amostra de avaliação foi concluída e arquivos relevantes suficientes foram marcados.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="2cbbd-158">A exibição de acompanhar expandida mostra a próxima etapa recomendada, as estatísticas de avaliação e acesso aos resultados detalhados.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="2cbbd-p112">Quando riqueza for muito baixa, o número de arquivos de avaliação adicionais necessários para alcançar um número mínimo de arquivos relevantes para produzir estatísticas úteis é muito alto. EDiscovery avançado recomendará a seguir adiante para treinamento. O indicador de progresso de avaliação será sombreado, e nenhum estatísticas estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="2cbbd-p113">Na ausência de estatística com base estabilização, haverá resultados com um nível mais baixo de nível de precisão e confiança. No entanto, esses resultados podem ser usados para encontrar arquivos relevantes quando você não precisa saber a porcentagem de arquivos relevantes encontrados. Da mesma forma, esse status pode ser usado para treinar problemas com baixa riqueza, onde as pontuações de relevância podem acelerar o acesso aos arquivos relevantes para um problema específico.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="2cbbd-p114">No **relevância \> Track** guia, a exibição de problema expandido, as seguintes opções de exibição estão disponíveis: > a recomendada próxima etapa, como **próxima etapa: marcação** pode ser desviada (por problema) clicando no botão **Modificar** para seu direito e, em seguida, selecionando uma etapa diferente na **próxima etapa**. Quando o indicador de progresso assessment não for concluído, a avaliação será a opção recomendada próxima, para marcar mais arquivos de avaliação e aumentar a exatidão estatísticas. > Você pode alterar a margem de erro e avaliar seu impacto, clicando em **Modificar**e, na caixa de **diálogo de nível de avaliação**, alterando a **margem de erro de destino para Recordação estimativas**e, em seguida, clicando em **atualizar valores**. Além disso, nessa caixa de diálogo, você pode exibir as opções avançadas, clicando em **Avançado**. > Você pode exibir as estatísticas de nível de avaliação adicionais e seu impacto clicando em **Exibir**. No diálogo resultados detalhe exibido, o estatísticas estão disponíveis por problema, quando há pelo menos 500 arquivos de avaliação marcados e pelo menos 18 arquivos estão marcados como relevantes para o problema.</span><span class="sxs-lookup"><span data-stu-id="2cbbd-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2cbbd-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cbbd-171">See also</span></span>

[<span data-ttu-id="2cbbd-172">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2cbbd-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="2cbbd-173">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="2cbbd-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2cbbd-174">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="2cbbd-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2cbbd-175">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="2cbbd-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2cbbd-176">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="2cbbd-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2cbbd-177">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="2cbbd-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

