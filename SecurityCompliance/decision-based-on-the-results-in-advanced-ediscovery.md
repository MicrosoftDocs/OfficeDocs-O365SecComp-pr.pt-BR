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
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a>Decisão baseada nos resultados da Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
 No eDiscovery avançada, na guia decida fornece informações adicionais para exibir e usar as estatísticas de suporte de decisão para determinar o tamanho do conjunto de arquivos casos a revisão. 
  
## <a name="using-the-decide-tab"></a>Usando a guia decida

![Decisão de Relevância](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
Este guia inclui o seguinte:
  
- **Problema**: a partir daqui, você pode selecionar o problema de interesse da lista. 
    
- **Taxa de cancelamento de revisão**: comparação de avançadas de revisão de descoberta eletrônica de acordo com as pontuações de relevância. O ponto de corte no gráfico representa a porcentagem de arquivos a serem revisados, mapeada para uma pontuação de relevância. Isso é usado na fase de teste de relevância e como um limite de exportação para remoção. O ponto de corte padrão, o número de arquivos a serem revisados estiver no ponto no qual o equilíbrio entre o cancelamento e a precisão é ideal. O ponto de corte real deve ser determinado pelo usuário dependendo objetivos e a compensação de custo (% revisão) e o risco (% recall). Usando o controle deslizante, você pode ajustar o ponto de corte e ver o efeito no gráfico e parâmetros, ao ajustar a porcentagem de arquivos relevantes a ser recuperada e antes de validar uma decisão.
    
- **Parâmetros**: analise, lembre-se de que os parâmetros de custo Total e relevantes próximas são cumulativas estatísticas calculadas referentes à revisão definida em relação à coleção para o caso de toda. As definições para esses parâmetros são:
    
    **Revise**: porcentagem de arquivos para analisar com base neste corte. 
    
    **Cancelar**: porcentagem de arquivos relevantes no conjunto de revisão. 
    
    **Próximo relevantes**: custo para examinar e identificar um arquivo relevante adicional que não está na revisão definido. 
    
    **Custo total**: custo para revisar essa porcentagem dos arquivos de maiusculas. Configurações de custo do parâmetro podem ser definidas pelo gerente de maiusculas.
    
- **Distribuição por pontuação de relevância**: arquivos na exibição cinza escuro para a esquerda estão abaixo a pontuação de fechamento. Uma dica de ferramenta exibe a pontuação de relevância e a porcentagem relacionada de arquivos no arquivo revisão definido em relação aos arquivos total.
    
Painel de detalhes expandido exibe detalhes adicionais. Arquivos em ilustrações da coleção não incluem arquivos vazios ou nebulous. Ilustrações de arquivos família representam arquivos que são carregados no relevância, ainda não ainda contabilizados como parte da família.
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Executando o treinamento de relevância](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

