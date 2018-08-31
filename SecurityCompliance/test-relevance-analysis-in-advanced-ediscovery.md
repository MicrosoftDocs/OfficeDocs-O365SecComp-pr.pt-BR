---
title: Testar análises de relevância na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Saiba como usar a guia teste após o cálculo de lote no eDiscovery avançadas do Office 365 para testar, comparar e validar a qualidade geral do processamento.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524074"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="121fc-103">Testar análises de relevância na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="121fc-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="121fc-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="121fc-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="121fc-p102">Guia de teste no eDiscovery avançado permite testar, comparar e validar a qualidade geral do processamento. Esses testes são executados após o cálculo de lote. Marcando os arquivos da coleção, com um perito torna o final opinião sobre se cada arquivo marcado está realmente relevante ao caso.</span><span class="sxs-lookup"><span data-stu-id="121fc-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="121fc-p103">Em cenários único e vários problemas, testes geralmente são executadas por um problema. Os resultados podem ser exibidos após cada teste e resultados de teste podem ser refeitos com arquivos de teste de amostra especificado.</span><span class="sxs-lookup"><span data-stu-id="121fc-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="121fc-111">Testando o restante</span><span class="sxs-lookup"><span data-stu-id="121fc-111">Testing the rest</span></span>

<span data-ttu-id="121fc-p104">O teste de "Testar o Rest" é usado para validar as decisões de remoção, por exemplo, para revisar somente os arquivos acima uma pontuação de corte relevância específico com base nos resultados finais eDiscovery avançado. Especialista analisa uma amostra de arquivos em uma pontuação de fechamento selecionado para avaliar o número de arquivos relevantes nesse conjunto.</span><span class="sxs-lookup"><span data-stu-id="121fc-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="121fc-p105">Esse teste fornece estatísticas e uma comparação entre o conjunto de revisão e o teste da população Rest. Os resultados do conjunto de revisão são aqueles calculado por relevância durante o treinamento. Os resultados incluem cálculos, com base nas configurações e parâmetros de entrada, tais como:</span><span class="sxs-lookup"><span data-stu-id="121fc-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="121fc-117">Teste as estatísticas de amostra do número de arquivos em uma amostra e identificados arquivos relevantes.</span><span class="sxs-lookup"><span data-stu-id="121fc-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="121fc-p106">Comparação tabular dos parâmetros população do conjunto de revisão e os demais, por exemplo, o número de arquivos, número estimado de arquivos relevantes, riqueza estimada e o custo médio de localização de um arquivo relevante adicional. Custo parâmetro podem ser definidas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="121fc-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="121fc-120">Abrir o **relevância \> teste** guia.</span><span class="sxs-lookup"><span data-stu-id="121fc-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="121fc-p107">Na aba **teste** , clique em **Testar de novo**. A caixa de diálogo **Criar teste** é exibida, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="121fc-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Resultados de “Test the Rest” de relevância](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="121fc-124">Em **nome do teste**e **Descrição**, digite o nome e descrição.</span><span class="sxs-lookup"><span data-stu-id="121fc-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="121fc-125">Na lista **tipo de teste** , selecione **o restante do teste**</span><span class="sxs-lookup"><span data-stu-id="121fc-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="121fc-126">No **problema / categoria** lista, selecione o nome do problema.</span><span class="sxs-lookup"><span data-stu-id="121fc-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="121fc-127">Na lista **de carga** , selecione a carga.</span><span class="sxs-lookup"><span data-stu-id="121fc-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="121fc-128">Na pasta **% de leitura**, aceite o valor padrão ou selecione um valor para a pontuação de relevância de fechamento.</span><span class="sxs-lookup"><span data-stu-id="121fc-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="121fc-p108">Em **Definir tamanho**, ou aceite o valor padrão. Observe que os ícones de restauração restaurará os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="121fc-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="121fc-p109">Clique em **Iniciar a marcação**. Uma amostra de teste é gerada.</span><span class="sxs-lookup"><span data-stu-id="121fc-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="121fc-133">Revise e marcar cada um dos arquivos no **relevância \> marca** guia e quando terminar, clique em **Calcular**.</span><span class="sxs-lookup"><span data-stu-id="121fc-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="121fc-p110">Na aba teste, você pode clicar **Exibir resultados** para ver os resultados do teste. Um exemplo é mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="121fc-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![Resultados do “Test the rest”](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="121fc-137">Na figura acima, a seção de **parâmetros de amostra** da tabela contém detalhes sobre o número de arquivos na amostra de marcados por especialista e o número de arquivos relevantes, encontrada nesse exemplo.</span><span class="sxs-lookup"><span data-stu-id="121fc-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="121fc-p111">A seção **parâmetros da população** da tabela contém os resultados do teste, incluindo a população de conjunto de revisão de arquivos com uma pontuação abaixo o corte selecionado e população "O Rest" dos arquivos com pontuação acima o corte selecionado. Para cada população, os seguintes resultados são exibidos:</span><span class="sxs-lookup"><span data-stu-id="121fc-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="121fc-140">Inclui os arquivos com % de leitura - corte indicado</span><span class="sxs-lookup"><span data-stu-id="121fc-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="121fc-141">O número total de arquivos</span><span class="sxs-lookup"><span data-stu-id="121fc-141">The total number of files</span></span> 
    
- <span data-ttu-id="121fc-142">O número estimado de arquivos relevantes</span><span class="sxs-lookup"><span data-stu-id="121fc-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="121fc-143">O aperfeiçoamento em termos estimado</span><span class="sxs-lookup"><span data-stu-id="121fc-143">The estimated richness</span></span> 
    
- <span data-ttu-id="121fc-144">O custo médio de revisão de localização do outro arquivo relevante</span><span class="sxs-lookup"><span data-stu-id="121fc-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="121fc-145">Teste a fatia</span><span class="sxs-lookup"><span data-stu-id="121fc-145">Testing the slice</span></span>

<span data-ttu-id="121fc-146">"Testar o fatia" teste realiza testes semelhante ao "Testar o restante" testar, mas com um segmento do arquivo definido conforme especificado pelas % de leitura de relevância.</span><span class="sxs-lookup"><span data-stu-id="121fc-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="121fc-147">Abrir o **relevância \> teste** guia.</span><span class="sxs-lookup"><span data-stu-id="121fc-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="121fc-p112">Na aba **teste** , clique em **Testar de novo**. A caixa de diálogo **Criar teste** é exibida.</span><span class="sxs-lookup"><span data-stu-id="121fc-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="121fc-150">Em **nome do teste** e **Descrição**, digite as informações.</span><span class="sxs-lookup"><span data-stu-id="121fc-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="121fc-151">Na lista **tipo de teste** , selecione **teste da fatia**.</span><span class="sxs-lookup"><span data-stu-id="121fc-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="121fc-152">Na lista de **problema** , selecione o nome do problema.</span><span class="sxs-lookup"><span data-stu-id="121fc-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="121fc-153">Na lista **de carga** , selecione a carga.</span><span class="sxs-lookup"><span data-stu-id="121fc-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="121fc-154">Na **leitura % entre**, aceite a valores de intervalo de baixa e alta padrão ou selecione valores para as pontuações de relevância de fechamento.</span><span class="sxs-lookup"><span data-stu-id="121fc-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="121fc-155">Em **Definir tamanho**, selecione um valor ou aceite o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="121fc-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="121fc-156">Os ícones de restauração irá restaurar o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="121fc-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="121fc-p113">Clique em **Iniciar a marcação**. Uma amostra de teste é gerada.</span><span class="sxs-lookup"><span data-stu-id="121fc-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="121fc-159">Revise e marcar cada um dos arquivos no **relevância \> marca** guia e quando terminar, clique em **Calcular**.</span><span class="sxs-lookup"><span data-stu-id="121fc-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="121fc-160">Na aba teste, você pode clicar **Exibir resultados** para ver os resultados do teste.</span><span class="sxs-lookup"><span data-stu-id="121fc-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="121fc-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="121fc-161">See also</span></span>

[<span data-ttu-id="121fc-162">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="121fc-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="121fc-163">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="121fc-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="121fc-164">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="121fc-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="121fc-165">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="121fc-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="121fc-166">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="121fc-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="121fc-167">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="121fc-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

