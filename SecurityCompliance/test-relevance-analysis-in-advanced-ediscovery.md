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
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a>Testar análises de relevância na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Guia de teste no eDiscovery avançado permite testar, comparar e validar a qualidade geral do processamento. Esses testes são executados após o cálculo de lote. Marcando os arquivos da coleção, com um perito torna o final opinião sobre se cada arquivo marcado está realmente relevante ao caso. 
  
Em cenários único e vários problemas, testes geralmente são executadas por um problema. Os resultados podem ser exibidos após cada teste e resultados de teste podem ser refeitos com arquivos de teste de amostra especificado.
  
## <a name="testing-the-rest"></a>Testando o restante

O teste de "Testar o Rest" é usado para validar as decisões de remoção, por exemplo, para revisar somente os arquivos acima uma pontuação de corte relevância específico com base nos resultados finais eDiscovery avançado. Especialista analisa uma amostra de arquivos em uma pontuação de fechamento selecionado para avaliar o número de arquivos relevantes nesse conjunto.
  
Esse teste fornece estatísticas e uma comparação entre o conjunto de revisão e o teste da população Rest. Os resultados do conjunto de revisão são aqueles calculado por relevância durante o treinamento. Os resultados incluem cálculos, com base nas configurações e parâmetros de entrada, tais como:
  
- Teste as estatísticas de amostra do número de arquivos em uma amostra e identificados arquivos relevantes. 
    
- Comparação tabular dos parâmetros população do conjunto de revisão e os demais, por exemplo, o número de arquivos, número estimado de arquivos relevantes, riqueza estimada e o custo médio de localização de um arquivo relevante adicional. Custo parâmetro podem ser definidas pelo administrador.
    
1. Abrir o **relevância \> teste** guia. 
    
2. Na aba **teste** , clique em **Testar de novo**. A caixa de diálogo **Criar teste** é exibida, conforme mostrado no exemplo a seguir. 
    
    ![Resultados de “Test the Rest” de relevância](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. Em **nome do teste**e **Descrição**, digite o nome e descrição.
    
4. Na lista **tipo de teste** , selecione **o restante do teste**
    
5. No **problema / categoria** lista, selecione o nome do problema. 
    
6. Na lista **de carga** , selecione a carga. 
    
7. Na pasta **% de leitura**, aceite o valor padrão ou selecione um valor para a pontuação de relevância de fechamento. 
    
8. Em **Definir tamanho**, ou aceite o valor padrão. Observe que os ícones de restauração restaurará os valores padrão.
    
9. Clique em **Iniciar a marcação**. Uma amostra de teste é gerada.
    
10. Revise e marcar cada um dos arquivos no **relevância \> marca** guia e quando terminar, clique em **Calcular**.
    
11. Na aba teste, você pode clicar **Exibir resultados** para ver os resultados do teste. Um exemplo é mostrado na figura a seguir. 
    
    ![Resultados do “Test the rest”](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
Na figura acima, a seção de **parâmetros de amostra** da tabela contém detalhes sobre o número de arquivos na amostra de marcados por especialista e o número de arquivos relevantes, encontrada nesse exemplo. 
  
A seção **parâmetros da população** da tabela contém os resultados do teste, incluindo a população de conjunto de revisão de arquivos com uma pontuação abaixo o corte selecionado e população "O Rest" dos arquivos com pontuação acima o corte selecionado. Para cada população, os seguintes resultados são exibidos: 
  
- Inclui os arquivos com % de leitura - corte indicado
    
- O número total de arquivos 
    
- O número estimado de arquivos relevantes 
    
- O aperfeiçoamento em termos estimado 
    
- O custo médio de revisão de localização do outro arquivo relevante
    
## <a name="testing-the-slice"></a>Teste a fatia

"Testar o fatia" teste realiza testes semelhante ao "Testar o restante" testar, mas com um segmento do arquivo definido conforme especificado pelas % de leitura de relevância.
  
1. Abrir o **relevância \> teste** guia. 
    
2. Na aba **teste** , clique em **Testar de novo**. A caixa de diálogo **Criar teste** é exibida. 
    
3. Em **nome do teste** e **Descrição**, digite as informações.
    
4. Na lista **tipo de teste** , selecione **teste da fatia**.
    
5. Na lista de **problema** , selecione o nome do problema. 
    
6. Na lista **de carga** , selecione a carga. 
    
7. Na **leitura % entre**, aceite a valores de intervalo de baixa e alta padrão ou selecione valores para as pontuações de relevância de fechamento. 
    
8. Em **Definir tamanho**, selecione um valor ou aceite o valor padrão.
    
    Os ícones de restauração irá restaurar o valor padrão.
    
9. Clique em **Iniciar a marcação**. Uma amostra de teste é gerada.
    
10. Revise e marcar cada um dos arquivos no **relevância \> marca** guia e quando terminar, clique em **Calcular**. 
    
11. Na aba teste, você pode clicar **Exibir resultados** para ver os resultados do teste. 
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)

