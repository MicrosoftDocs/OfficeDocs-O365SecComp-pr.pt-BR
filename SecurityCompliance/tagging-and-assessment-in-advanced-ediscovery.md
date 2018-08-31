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
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a>Marcação e avaliação na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Esta seção descreve o procedimento para o módulo de avaliação de relevância de eDiscovery avançado. 
  
## <a name="performing-assessment-training-and-analysis"></a>Executando a análise e treinamento da avaliação

1. No **relevância \> Track** , clique em **avaliação** para iniciar a avaliação casos. 
    
    Por exemplo, fins deste procedimento, um conjunto de avaliação de amostra de 500 arquivos é criado e na guia **marca** for exibida, que contém o painel de marcação, o conteúdo do arquivo exibido e outras opções de marca. 
    
    ![Guia Marca de Relevância para Avaliação](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. Revisar cada arquivo na amostra, determinar a relevância do arquivo para cada questão de maiusculas e marcar o arquivo usando o Relevance (R), não relevante (NR) e evitar botões no painel do **Painel de marcação** . 
    
    > [!NOTE]
    >  Avaliação requer 500 arquivos marcados. Se os arquivos são "ignorados", você receberá mais arquivos a marca. 
  
3. Após todos os arquivos na amostra de marcação, clique em **Calcular**. 
    
    Margem de erro atual de avaliação e riqueza são calculadas e exibidas na guia **Faixa de relevância** , com detalhes expandidas por problema, conforme mostrado abaixo. Para obter mais detalhes sobre essa caixa de diálogo são descritos na seção posterior "Resultados de avaliações de revisão". 
    
    ![Controle de relevância - avaliação](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > Por padrão, é recomendável que você prossiga para a próxima etapa do padrão quando o indicador de progresso de avaliação para o problema for concluído, indicando que a amostra de avaliação foi revisada e arquivos relevantes suficientes foram marcados. > Caso contrário, se você quiser exibir os resultados da guia **controlar** e a margem de erro e a próxima etapa de controle, clique em **Modificar** adjacente à **Próxima etapa**, selecione **Continuar avaliação**e, em seguida, clique em **Okey**. 
  
1. Clique em **Modificar** à direita da caixa de seleção de **avaliação** para exibir e especifique os parâmetros de avaliação por problema. Uma caixa de diálogo de **nível de avaliação** para cada questão for exibida, conforme mostrado no exemplo a seguir: 
    
    ![Problema de caso de nível de avaliação](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    Os seguintes parâmetros para o problema são calculados e exibidos na caixa de diálogo **nível de avaliação** : 
    
    **Estimativas de margem de erro de destino para Recordação**: com base nesse valor, o número estimado de arquivos adicionais necessários para analisar é calculado. A margem utilizada para Recordação é mais de 75% e com um nível de confiança de 95%. 
    
    **Arquivos de avaliação adicionais necessários**: indica quantas mais arquivos são necessários se os requisitos da margem de erro atual não foram atendidos. 
    
2. Para ajustar a margem de erro atual e ver o efeito das margens de erro diferente (por problema):
    
1. Na lista **Selecione o problema** , selecione um problema. 
    
2. Na **margem de erro de destino para Recordação estima**, insira um novo valor.
    
3. Clique em **atualizar valores** para ver o impacto dos ajustes. 
    
3. Clique em **Avançado** na caixa de diálogo **nível de avaliação** para ver os seguintes parâmetros adicionais e detalhes: 
    
    ![Exibição avançada de problema de caso de nível de avaliação](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    **Riqueza estimado**: estimado riqueza de acordo com os resultados atuais de avaliação
    
    **Para Recordação presumida**: por padrão, a margem de erro de destino se aplica para recuperá-lo acima de 75%. Clique em **Editar** alterar esse parâmetro e controlar a margem de erro em um intervalo diferente de valores de cancelamento. 
    
    **Nível de confiança**: por padrão, a margem de erro recomendados para a confiança é 95%. Clique em **Editar** , se você quiser alterar esse parâmetro. 
    
    **Margem de erro riqueza Expected**: dado os valores atualizados, trate a esperado margem de erro da sofisticação, depois que todos os arquivos de avaliação adicionais sejam revisados.
    
    **Arquivos de avaliação adicionais necessários**: dado os valores atualizados, o número de avaliação adicional arquivos que precisam ser revisados para alcançar o destino.
    
    **Arquivos de avaliação total necessário**: total de dado os valores atualizados, arquivos de avaliação necessários para revisão.
    
    **Número de expected de arquivos relevantes na avaliação**: dado os valores atualizados, o número esperado de arquivos relevantes na avaliação inteira depois que todos os arquivos de avaliação adicionais sejam revisados.
    
4. Clique em **recalcular valores**, se os parâmetros forem alterados. Quando tiver terminado, se houver um problema, clique em **Okey** para salvar as alterações (ou **próximo** quando há várias questões para revisar ou modificar e, em seguida, **término**). 
    
    Quando há várias questões, depois que todos os problemas foram revisados ou ajustados, um **nível de avaliação: Resumo** caixa de diálogo é exibida, conforme mostrado no exemplo a seguir. 
    
    ![Resumo do nível de análise](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    Após a conclusão bem-sucedida da avaliação, vá para o próximo estágio no treinamento de relevância.
    
## <a name="reviewing-assessment-results"></a>Revisar os resultados da avaliação

Após uma amostra da avaliação é marcada, os resultados da avaliação são calculados e exibidos na guia faixa de relevância.
  
Os seguintes resultados são exibidos na exibição Track expandida: 
  
- Estimativas de margem de erro atual Assessment para Recordação
    
- Riqueza estimada
    
- Arquivos de avaliação adicionais necessários (para revisão)
    
A margem de erro Assessment atual é a margem de erro recomendada por eDiscovery avançado. O número exibido para os "arquivos avaliação adicionais necessários" corresponde a essa recomendação.
  
O indicador de progresso Assessment mostra o nível de conclusão da avaliação, dada a margem de erro atual. Quando a avaliação estiver em andamento, o usuário será marcar outro exemplo de avaliação.
  
Quando o indicador de progresso assessment mostra assessment como concluído, isso significa que a revisão de amostra de avaliação foi concluída e arquivos relevantes suficientes foram marcados. 
  
A exibição de acompanhar expandida mostra a próxima etapa recomendada, as estatísticas de avaliação e acesso aos resultados detalhados.
  
Quando riqueza for muito baixa, o número de arquivos de avaliação adicionais necessários para alcançar um número mínimo de arquivos relevantes para produzir estatísticas úteis é muito alto. EDiscovery avançado recomendará a seguir adiante para treinamento. O indicador de progresso de avaliação será sombreado, e nenhum estatísticas estarão disponíveis. 
  
Na ausência de estatística com base estabilização, haverá resultados com um nível mais baixo de nível de precisão e confiança. No entanto, esses resultados podem ser usados para encontrar arquivos relevantes quando você não precisa saber a porcentagem de arquivos relevantes encontrados. Da mesma forma, esse status pode ser usado para treinar problemas com baixa riqueza, onde as pontuações de relevância podem acelerar o acesso aos arquivos relevantes para um problema específico.
  
> [!TIP]
> No **relevância \> Track** guia, a exibição de problema expandido, as seguintes opções de exibição estão disponíveis: > a recomendada próxima etapa, como **próxima etapa: marcação** pode ser desviada (por problema) clicando no botão **Modificar** para seu direito e, em seguida, selecionando uma etapa diferente na **próxima etapa**. Quando o indicador de progresso assessment não for concluído, a avaliação será a opção recomendada próxima, para marcar mais arquivos de avaliação e aumentar a exatidão estatísticas. > Você pode alterar a margem de erro e avaliar seu impacto, clicando em **Modificar**e, na caixa de **diálogo de nível de avaliação**, alterando a **margem de erro de destino para Recordação estimativas**e, em seguida, clicando em **atualizar valores**. Além disso, nessa caixa de diálogo, você pode exibir as opções avançadas, clicando em **Avançado**. > Você pode exibir as estatísticas de nível de avaliação adicionais e seu impacto clicando em **Exibir**. No diálogo resultados detalhe exibido, o estatísticas estão disponíveis por problema, quando há pelo menos 500 arquivos de avaliação marcados e pelo menos 18 arquivos estão marcados como relevantes para o problema. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

