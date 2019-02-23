---
title: Decisão baseada nos resultados da Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Saiba como a guia decidir na descoberta eletrônica avançada do Office 365 fornece dados que podem ajudá-lo a determinar o tamanho correto do conjunto de arquivos de caso. '
ms.openlocfilehash: c4767e703d03ef5dbdb808332e873d22094d7bca
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216101"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="acd0f-103">Decisão baseada nos resultados da Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="acd0f-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="acd0f-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="acd0f-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="acd0f-106">Na descoberta eletrônica avançada, a guia decidir fornece informações adicionais para exibir e usar estatísticas de suporte à decisão para determinar o tamanho do conjunto de análise de arquivos de caso.</span><span class="sxs-lookup"><span data-stu-id="acd0f-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="acd0f-107">Usando a guia decidir</span><span class="sxs-lookup"><span data-stu-id="acd0f-107">Using the Decide tab</span></span>

![Decisão de Relevância](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="acd0f-109">Essa guia inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="acd0f-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="acd0f-110">**Problema**: aqui, você pode selecionar o problema de interesse na lista.</span><span class="sxs-lookup"><span data-stu-id="acd0f-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="acd0f-p102">**Taxa de recuperação de revisão**: comparação de análise de descoberta eletrônica avançada de acordo com as pontuações de relevância. O ponto de corte no gráfico representa a porcentagem de arquivos a serem revisados, mapeados para uma pontuação de relevância. Isso é usado na fase de teste de relevância e como um limite de exportação para a seleção. O ponto de corte padrão, para o número de arquivos a serem revisados, é o ponto no qual o equilíbrio entre reCall e Precision é ideal. O ponto de corte real deve ser determinado pelo usuário dependendo dos objetivos e da troca de custo (% revisão) e risco (% recall). Usando o controle deslizante, você pode ajustar o ponto de corte e ver o efeito no gráfico e nos parâmetros, ao ajustar a porcentagem de arquivos relevantes a serem recuperados e antes de validar uma decisão.</span><span class="sxs-lookup"><span data-stu-id="acd0f-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="acd0f-p103">**Parâmetros**: revisar, renovar, os parâmetros de custo total relevantes e totais são estatísticas calculadas cumulativas referentes ao conjunto de revisão em relação à coleção para o caso inteiro. As definições desses parâmetros são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="acd0f-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="acd0f-118">**Revisão**: porcentagem de arquivos a serem revisados com base nesse corte.</span><span class="sxs-lookup"><span data-stu-id="acd0f-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="acd0f-119">**Recall**: porcentagem de arquivos relevantes no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="acd0f-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="acd0f-120">**Próximo relevante**: custo para revisar e identificar um arquivo relevante adicional que não está atualmente no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="acd0f-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="acd0f-p104">**Custo total**: custo para a revisão desse percentual dos arquivos de caso. As configurações de parâmetros de custo podem ser definidas pelo gerente de caso.</span><span class="sxs-lookup"><span data-stu-id="acd0f-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="acd0f-p105">**Distribuição por Pontuação de relevância**: os arquivos na exibição cinza escuro à esquerda estão abaixo da Pontuação de corte. Uma dica de ferramenta exibe a pontuação de relevância e a porcentagem relacionada de arquivos no conjunto de arquivos de revisão em relação ao total de arquivos.</span><span class="sxs-lookup"><span data-stu-id="acd0f-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="acd0f-p106">O painel de detalhes expandido exibe detalhes adicionais. Os arquivos nas figuras de coleção não incluem arquivos vazios ou nebulous. Os números de arquivos da família representam arquivos que não são carregados em relevância, ainda que sejam contados como parte da família.</span><span class="sxs-lookup"><span data-stu-id="acd0f-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acd0f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="acd0f-128">See also</span></span>

[<span data-ttu-id="acd0f-129">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="acd0f-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="acd0f-130">Noções básicas sobre avaliação em relevância</span><span class="sxs-lookup"><span data-stu-id="acd0f-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="acd0f-131">Marcação e avaliação</span><span class="sxs-lookup"><span data-stu-id="acd0f-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="acd0f-132">Realizando treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="acd0f-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="acd0f-133">Análise de relevância de rastreamento</span><span class="sxs-lookup"><span data-stu-id="acd0f-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="acd0f-134">Testando análise de relevância</span><span class="sxs-lookup"><span data-stu-id="acd0f-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

