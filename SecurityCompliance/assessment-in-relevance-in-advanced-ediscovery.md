---
title: Entender e avaliação em relevância na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Obtenha uma visão geral do estágio de avaliação e sua função para determinar a riqueza de problemas durante o treinamento de relevância na descoberta eletrônica avançada do Office 365.
ms.openlocfilehash: 1ddaa7ef37f762d7b63bb6c0c51193ff382b8d6b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212971"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="66a10-103">Entender e avaliação em relevância na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="66a10-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="66a10-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="66a10-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="66a10-p102">A descoberta eletrônica avançada permite a avaliação prévia, por exemplo, para os problemas definidos e os dados importados para um caso. A descoberta eletrônica avançada permite que o especialista tome decisões relacionadas à abordagem adotada e as aplique ao projeto de revisão de documentos.</span><span class="sxs-lookup"><span data-stu-id="66a10-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="66a10-108">Noções básicas sobre avaliação</span><span class="sxs-lookup"><span data-stu-id="66a10-108">Understanding assessment</span></span>

<span data-ttu-id="66a10-p103">Em avaliação, o especialista revisa um conjunto aleatório de pelo menos 500 arquivos, que são usados para determinar a riqueza dos problemas e produzir estatísticas que refletem os resultados de treinamento. A avaliação é bem-sucedida quando são encontrados arquivos relevantes suficientes para atingir um nível estatístico que ajudará a garantir a relevância avançada de descoberta eletrônica para fornecer estatísticas precisas e para determinar efetivamente o ponto de estabilização no processo de treinamento.</span><span class="sxs-lookup"><span data-stu-id="66a10-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="66a10-p104">Quanto maior o número de arquivos relevantes no conjunto de avaliação, mais precisos são as estatísticas e a eficácia do algoritmo de estabilidade. O número de arquivos relevantes dentro dos arquivos de avaliação depende da riqueza do problema. Riqueza é a porcentagem estimada de arquivos relevantes no conjunto relevante para um problema. Problemas com maior riqueza atingirão um número maior de arquivos relevantes mais rapidamente do que problemas com riqueza inferior. Problemas com riqueza extremamente baixa (por exemplo, 2% ou menos) exigirão um conjunto de avaliação muito grande para alcançar um número significativo de arquivos relevantes.</span><span class="sxs-lookup"><span data-stu-id="66a10-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="66a10-p105">As estatísticas, que são apresentadas no controle e decidem as guias durante o treinamento e depois do cálculo em lotes, incluem estimativas de recall para diferentes conjuntos de revisão. Em estatísticas, as estimativas baseadas em um conjunto de amostra (neste caso, os arquivos de avaliação) incluem a margem de erro e o nível de confiança dessa margem de erro. Por exemplo, a recuperação estimada de 80% pode ter uma margem de erro de mais ou menos 5% com um nível de confiança de 95%. Isso significa que a RECALL estimada é de 75%-85% e esta estimativa tem 95% de confiança. Quanto maior o conjunto de avaliação, a margem de erro torna-se menor e as estatísticas são mais precisas.</span><span class="sxs-lookup"><span data-stu-id="66a10-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="66a10-p106">Depois que o especialista revisa um conjunto de avaliação inicial de 500 arquivos, a relevância é capaz de determinar a margem atual de erro dos valores de recuperação. A relevância também definirá uma margem de erro padrão que recomenda o acesso para otimizar o conjunto de avaliação. Veja a seguir alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="66a10-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="66a10-124">Se o conjunto de avaliação já tiver resultado uma margem de erro de mais ou menos 10%, será recomendável passar para o treinamento (nenhuma análise adicional da avaliação é necessária).</span><span class="sxs-lookup"><span data-stu-id="66a10-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="66a10-125">Se o conjunto de avaliação tiver uma margem de erro de mais ou menos 13%, a relevância poderá recomendar a revisão de outro conjunto de arquivos de avaliação para alcançar uma margem menor.</span><span class="sxs-lookup"><span data-stu-id="66a10-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="66a10-126">Se a riqueza for extremamente baixa, a relevância poderá ser recomendável parando a avaliação, mesmo que a margem de erro seja grande (tornando as estatísticas impraticáveis) porque o conjunto de avaliação necessário para atingir uma margem de erro útil é muito grande.</span><span class="sxs-lookup"><span data-stu-id="66a10-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="66a10-p107">Cada problema tem sua própria riqueza, margem atual de erro e, como resultado, o número estimado de arquivos de avaliação adicionais. O próximo conjunto de avaliação é criado de acordo com o número máximo de arquivos (até 1.000 em um único conjunto).</span><span class="sxs-lookup"><span data-stu-id="66a10-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="66a10-p108">Você pode aceitar as recomendações de relevância ou ajustar a margem de erro atual de acordo com suas necessidades. A margem de erro atual padrão é determinada para a recuperação em igual ou acima de 75%.</span><span class="sxs-lookup"><span data-stu-id="66a10-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="66a10-p109">O estágio de avaliação pode ser ignorado, na guia **controle \> de relevância** no modo de exibição expandido para um problema, desmarcando a caixa de seleção de **avaliação** por problema e, em seguida, para "todos os problemas". No enTanto, como resultado, não haverá estatísticas para esse problema. > a caixa de seleção de **avaliação** só pode ser feita antes da avaliação ser realizada. Onde houver vários problemas em um caso, a avaliação será ignorada somente se a caixa de seleção estiver desmarcada para cada problema</span><span class="sxs-lookup"><span data-stu-id="66a10-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66a10-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a10-135">See also</span></span>

[<span data-ttu-id="66a10-136">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="66a10-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="66a10-137">Marcação e avaliação</span><span class="sxs-lookup"><span data-stu-id="66a10-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="66a10-138">Treinamento de marcação e relevância</span><span class="sxs-lookup"><span data-stu-id="66a10-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="66a10-139">Análise de relevância de rastreamento</span><span class="sxs-lookup"><span data-stu-id="66a10-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="66a10-140">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="66a10-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="66a10-141">Testando análise de relevância</span><span class="sxs-lookup"><span data-stu-id="66a10-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

