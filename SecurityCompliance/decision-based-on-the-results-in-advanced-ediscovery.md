---
title: Decisão baseada nos resultados da Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Saiba como a guia decida no eDiscovery avançadas do Office 365 fornece dados que podem ajudar a determinam o tamanho correto do conjunto de arquivos casos a revisão. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523770"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="479a7-103">Decisão baseada nos resultados da Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="479a7-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="479a7-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="479a7-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="479a7-106">No eDiscovery avançada, na guia decida fornece informações adicionais para exibir e usar as estatísticas de suporte de decisão para determinar o tamanho do conjunto de arquivos casos a revisão.</span><span class="sxs-lookup"><span data-stu-id="479a7-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="479a7-107">Usando a guia decida</span><span class="sxs-lookup"><span data-stu-id="479a7-107">Using the Decide tab</span></span>

![Decisão de Relevância](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="479a7-109">Este guia inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="479a7-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="479a7-110">**Problema**: a partir daqui, você pode selecionar o problema de interesse da lista.</span><span class="sxs-lookup"><span data-stu-id="479a7-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="479a7-p102">**Taxa de cancelamento de revisão**: comparação de avançadas de revisão de descoberta eletrônica de acordo com as pontuações de relevância. O ponto de corte no gráfico representa a porcentagem de arquivos a serem revisados, mapeada para uma pontuação de relevância. Isso é usado na fase de teste de relevância e como um limite de exportação para remoção. O ponto de corte padrão, o número de arquivos a serem revisados estiver no ponto no qual o equilíbrio entre o cancelamento e a precisão é ideal. O ponto de corte real deve ser determinado pelo usuário dependendo objetivos e a compensação de custo (% revisão) e o risco (% recall). Usando o controle deslizante, você pode ajustar o ponto de corte e ver o efeito no gráfico e parâmetros, ao ajustar a porcentagem de arquivos relevantes a ser recuperada e antes de validar uma decisão.</span><span class="sxs-lookup"><span data-stu-id="479a7-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="479a7-p103">**Parâmetros**: analise, lembre-se de que os parâmetros de custo Total e relevantes próximas são cumulativas estatísticas calculadas referentes à revisão definida em relação à coleção para o caso de toda. As definições para esses parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="479a7-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="479a7-118">**Revise**: porcentagem de arquivos para analisar com base neste corte.</span><span class="sxs-lookup"><span data-stu-id="479a7-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="479a7-119">**Cancelar**: porcentagem de arquivos relevantes no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="479a7-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="479a7-120">**Próximo relevantes**: custo para examinar e identificar um arquivo relevante adicional que não está na revisão definido.</span><span class="sxs-lookup"><span data-stu-id="479a7-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="479a7-p104">**Custo total**: custo para revisar essa porcentagem dos arquivos de maiusculas. Configurações de custo do parâmetro podem ser definidas pelo gerente de maiusculas.</span><span class="sxs-lookup"><span data-stu-id="479a7-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="479a7-p105">**Distribuição por pontuação de relevância**: arquivos na exibição cinza escuro para a esquerda estão abaixo a pontuação de fechamento. Uma dica de ferramenta exibe a pontuação de relevância e a porcentagem relacionada de arquivos no arquivo revisão definido em relação aos arquivos total.</span><span class="sxs-lookup"><span data-stu-id="479a7-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="479a7-p106">Painel de detalhes expandido exibe detalhes adicionais. Arquivos em ilustrações da coleção não incluem arquivos vazios ou nebulous. Ilustrações de arquivos família representam arquivos que são carregados no relevância, ainda não ainda contabilizados como parte da família.</span><span class="sxs-lookup"><span data-stu-id="479a7-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="479a7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="479a7-128">See also</span></span>

[<span data-ttu-id="479a7-129">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="479a7-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="479a7-130">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="479a7-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="479a7-131">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="479a7-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="479a7-132">Executando o treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="479a7-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="479a7-133">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="479a7-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="479a7-134">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="479a7-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

