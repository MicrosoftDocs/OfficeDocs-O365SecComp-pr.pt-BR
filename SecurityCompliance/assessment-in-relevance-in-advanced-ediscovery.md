---
title: Entender e avaliação em relevância na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Obtenha uma visão geral do estágio de avaliação e sua função na determinação o aperfeiçoamento em termos de problemas durante o treinamento de relevância no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524065"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="a9ad3-103">Entender e avaliação em relevância na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="a9ad3-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="a9ad3-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a9ad3-p102">Descoberta eletrônica avançada permite avaliação preliminar, por exemplo, para os problemas definidos e os dados importados para uma ocorrência. EDiscovery avançado permite que o especialista tomar decisões referentes a uma abordagem de adoção e aplicá-las ao projeto de revisão do documento.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="a9ad3-108">Avaliação de compreensão</span><span class="sxs-lookup"><span data-stu-id="a9ad3-108">Understanding assessment</span></span>

<span data-ttu-id="a9ad3-p103">Na avaliação, especialista analisa um conjunto aleatório de pelo menos 500 arquivos, que são usadas para determinar o aperfeiçoamento em termos dos problemas e para produzir as estatísticas que refletem os resultados de treinamento. Avaliação é bem-sucedida quando arquivos suficientes relevantes são encontrados para chegar a um nível de estatístico que ajudarão a relevância para fornecer estatísticas precisas e determinar efetivamente o ponto de estabilização do processo de treinamento do eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="a9ad3-p104">Quanto maior que o número de relevantes arquivos no conjunto de avaliação, mais preciso as estatísticas e a eficácia do algoritmo estabilidade. O número de arquivos relevantes dentro dos arquivos de avaliação depende do aperfeiçoamento em termos do problema. Riqueza indica a porcentagem estimada dos arquivos relevantes no conjunto relevante para um problema. Problemas com maior riqueza alcançará um número maior de arquivos relevantes mais rapidamente do que os problemas com riqueza inferior. Problemas com riqueza extremamente baixa (por exemplo, 2% ou menos) exigirá uma avaliação muito grande definida para chegar a um número significativo de arquivos relevantes.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="a9ad3-p105">As estatísticas, que são apresentadas nas guias Track e decida durante o treinamento e após o cálculo de lote, incluem estimativas de cancelamento de conjuntos de revisão diferente. Em estatística, estimativas baseadas em uma amostra definido (nesse caso, os arquivos de avaliação) incluem a margem de erro e o nível de confiança da margem erro. Por exemplo, recall estimado de 80% pode ter uma margem de erro de mais ou menos de 5% com um nível de confiança de 95%. Isso significa que o cancelamento estimado é realmente de % de 75-85% e essa estimativa tem a confiança de 95%. Quanto maior o conjunto de avaliação, a margem de erro se torna menor e as estatísticas são mais precisas.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="a9ad3-p106">Depois que o especialista analisa um conjunto de avaliação inicial de 500 arquivos, relevância é capaz de determinar a margem atual de erro dos valores de cancelamento. Relevância também definirá uma margem de padrão de erro que ele recomenda alcance para otimizar o conjunto de avaliação. Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="a9ad3-124">Se a avaliação já definida gerou uma margem de erro de mais ou menos de 10%, relevância recomendará para mover-se para treinamento (sem revisão de avaliação adicional é necessária).</span><span class="sxs-lookup"><span data-stu-id="a9ad3-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="a9ad3-125">Se o conjunto de avaliação gerou uma margem de erro de mais ou menos 13%, relevância poderia recomendar a revisão de outro conjunto de arquivos de avaliação para alcançar uma margem menor.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="a9ad3-126">Se riqueza é extremamente baixa, relevância poderia recomendar interrompendo assessment, embora a margem de erro é grande (tornando estatísticas impraticável), porque o conjunto de avaliação necessária alcançar uma útil margem de erro é muito grande.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="a9ad3-p107">Cada problema tem seu próprio riqueza, atual margem de erro e estimado como resultado, o número de arquivos de avaliação adicionais. O próximo conjunto de avaliação é criado de acordo com o número máximo de arquivos (até 1.000 em um único conjunto).</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="a9ad3-p108">Você pode aceitar as recomendações de relevância ou ajustar a margem atual de erro de acordo com suas necessidades. A margem atual do padrão de erro é determinada para Recordação igual ou acima de 75%.</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a9ad3-p109">O estágio de avaliação pode ser ignorado de, além de **relevância \> Track** guia no modo de exibição expandido para um problema, desmarcando a caixa de seleção de **avaliação** por problema e, em seguida, para "todos os problemas". No entanto, como resultado, não haverá nenhuma estatísticas para esse problema. > Desmarcar a caixa de seleção **Assessment** só pode ser feito antes de avaliação é executada. Onde várias questões existirem no caso, avaliação é ignorada apenas se a caixa de seleção estiver desmarcada para cada questão</span><span class="sxs-lookup"><span data-stu-id="a9ad3-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9ad3-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9ad3-135">See also</span></span>

[<span data-ttu-id="a9ad3-136">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="a9ad3-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a9ad3-137">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="a9ad3-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a9ad3-138">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="a9ad3-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a9ad3-139">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="a9ad3-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a9ad3-140">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="a9ad3-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a9ad3-141">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="a9ad3-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

