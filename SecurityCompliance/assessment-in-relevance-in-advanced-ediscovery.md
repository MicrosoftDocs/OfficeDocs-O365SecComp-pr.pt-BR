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
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Entender e avaliação em relevância na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Descoberta eletrônica avançada permite avaliação preliminar, por exemplo, para os problemas definidos e os dados importados para uma ocorrência. EDiscovery avançado permite que o especialista tomar decisões referentes a uma abordagem de adoção e aplicá-las ao projeto de revisão do documento.
  
## <a name="understanding-assessment"></a>Avaliação de compreensão

Na avaliação, especialista analisa um conjunto aleatório de pelo menos 500 arquivos, que são usadas para determinar o aperfeiçoamento em termos dos problemas e para produzir as estatísticas que refletem os resultados de treinamento. Avaliação é bem-sucedida quando arquivos suficientes relevantes são encontrados para chegar a um nível de estatístico que ajudarão a relevância para fornecer estatísticas precisas e determinar efetivamente o ponto de estabilização do processo de treinamento do eDiscovery avançado. 
  
Quanto maior que o número de relevantes arquivos no conjunto de avaliação, mais preciso as estatísticas e a eficácia do algoritmo estabilidade. O número de arquivos relevantes dentro dos arquivos de avaliação depende do aperfeiçoamento em termos do problema. Riqueza indica a porcentagem estimada dos arquivos relevantes no conjunto relevante para um problema. Problemas com maior riqueza alcançará um número maior de arquivos relevantes mais rapidamente do que os problemas com riqueza inferior. Problemas com riqueza extremamente baixa (por exemplo, 2% ou menos) exigirá uma avaliação muito grande definida para chegar a um número significativo de arquivos relevantes.
  
As estatísticas, que são apresentadas nas guias Track e decida durante o treinamento e após o cálculo de lote, incluem estimativas de cancelamento de conjuntos de revisão diferente. Em estatística, estimativas baseadas em uma amostra definido (nesse caso, os arquivos de avaliação) incluem a margem de erro e o nível de confiança da margem erro. Por exemplo, recall estimado de 80% pode ter uma margem de erro de mais ou menos de 5% com um nível de confiança de 95%. Isso significa que o cancelamento estimado é realmente de % de 75-85% e essa estimativa tem a confiança de 95%. Quanto maior o conjunto de avaliação, a margem de erro se torna menor e as estatísticas são mais precisas. 
  
Depois que o especialista analisa um conjunto de avaliação inicial de 500 arquivos, relevância é capaz de determinar a margem atual de erro dos valores de cancelamento. Relevância também definirá uma margem de padrão de erro que ele recomenda alcance para otimizar o conjunto de avaliação. Estes são alguns exemplos:
  
- Se a avaliação já definida gerou uma margem de erro de mais ou menos de 10%, relevância recomendará para mover-se para treinamento (sem revisão de avaliação adicional é necessária). 
    
- Se o conjunto de avaliação gerou uma margem de erro de mais ou menos 13%, relevância poderia recomendar a revisão de outro conjunto de arquivos de avaliação para alcançar uma margem menor. 
    
- Se riqueza é extremamente baixa, relevância poderia recomendar interrompendo assessment, embora a margem de erro é grande (tornando estatísticas impraticável), porque o conjunto de avaliação necessária alcançar uma útil margem de erro é muito grande.
    
Cada problema tem seu próprio riqueza, atual margem de erro e estimado como resultado, o número de arquivos de avaliação adicionais. O próximo conjunto de avaliação é criado de acordo com o número máximo de arquivos (até 1.000 em um único conjunto).
  
Você pode aceitar as recomendações de relevância ou ajustar a margem atual de erro de acordo com suas necessidades. A margem atual do padrão de erro é determinada para Recordação igual ou acima de 75%.
  
> [!NOTE]
> O estágio de avaliação pode ser ignorado de, além de **relevância \> Track** guia no modo de exibição expandido para um problema, desmarcando a caixa de seleção de **avaliação** por problema e, em seguida, para "todos os problemas". No entanto, como resultado, não haverá nenhuma estatísticas para esse problema. > Desmarcar a caixa de seleção **Assessment** só pode ser feito antes de avaliação é executada. Onde várias questões existirem no caso, avaliação é ignorada apenas se a caixa de seleção estiver desmarcada para cada questão 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

