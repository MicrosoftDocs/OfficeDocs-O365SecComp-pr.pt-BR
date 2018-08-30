---
title: Acompanhar análises de relevância na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Saiba como visualizar e interpretar os resultados para problemas de maiusculas no eDiscovery avançadas do Office 365 e o status de treinamento de relevância.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524710"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a>Acompanhar análises de relevância na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
No eDiscovery avançada, na guia faixa de relevância exibe a validade calculada do treinamento relevância executada na guia marca e indica a próxima etapa para tirar no processo de treinamento interativas em relevância. 
  
## <a name="tracking-relevance-training-status"></a>Status de treinamento de relevância de rastreamento

1. Exiba os detalhes a seguir na faixa de relevância para os problemas de maiusculas, conforme mostrado no exemplo a seguir de uma caixa de diálogo **nome do problema** abaixo. 
    
  - **Avaliação**: este indicador de progresso mostra até que grau a relevância treinamento executadas até esse ponto alcançou a meta de avaliação em termos de margem de erro. O aperfeiçoamento em termos dos resultados de treinamento da relevância também é exibido. 
    
  - **Treinamento**: essa tela de dica de ferramenta e indicador de progresso codificada indica o treinamento de relevância de resultados estabilidade e uma escala numérica mostrando o número de amostras de treinamento de relevância marcados para cada questão. Especialista monitora o andamento do processo de treinamento de relevância repetitivo. 
    
  - **Cálculo de lote**: esse indicador de progresso fornece informações sobre a conclusão de cálculo de lote.
    
  - **Próxima etapa**: exibe a recomendação para a próxima etapa a ser executada. 
    
    No exemplo, é mostrada uma avaliação concluída com êxito para um problema, indicado pelo indicador de progresso de cor concluídas e a marca de seleção. Marcação está em andamento, mas o caso ainda é considerado instável (o status de estabilidade também é mostrado em uma dica de ferramenta). A recomendação de etapa próxima é "treinamento". 
    
    ![Etapa 1 do treinamento do Controle de Relevância](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    O modo de exibição expandido exibe opções e informações adicionais. A margem de erro atual exibido é a margem de erro de cancelamento de no estado atual da avaliação, recebe os arquivos de avaliação (já marcados) existente.
    
    > [!NOTE]
    >  O estágio de avaliação pode ser desviado desmarcando a caixa de seleção de **avaliação** por problema e, em seguida, para "todos os problemas". No entanto, como resultado, não haverá nenhuma estatísticas para esse problema. > Desmarcar a caixa de seleção **Assessment** só pode ser feito antes de avaliação é executada. Onde várias questões existirem no caso, avaliação é ignorada apenas se a caixa de seleção estiver desmarcada para cada questão 
  
    Quando assessment não for concluído com o exemplo primeiro conjunto de arquivos, avaliação pode ser a próxima etapa para marcação mais arquivos. 
    
    Na **relevância** \> **trilha**, o indicador de progresso de treinamento e a dica de ferramenta indicam o número estimado de exemplos adicionais necessárias para alcançar a estabilidade. Essa estimativa fornece uma diretriz para o treinamento adicional necessário.
    
    ![Treinamento do controle de relevância](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. Quando tiver concluído de marcação e se você precisar continuar, treinamento, clique em **treinamento**. Outro conjunto de amostra de arquivos é gerado a partir do arquivo carregado definido para treinamento adicional. Você retorna à guia marca para marcar e treinar mais arquivos.
    
### <a name="reaching-stable-training-levels"></a>Atingir níveis de treinamento estável

Depois que os arquivos de avaliação obtiveram um nível estável de treinamento, eDiscovery Avançado está pronto para cálculo de lote.
  
> [!NOTE]
> Normalmente, após três estável amostras de treinamento, a próxima etapa é "Cálculo de lote". Pode haver exceções, por exemplo, quando não havia alterações para a marcação dos arquivos de exemplos anteriores ou quando os arquivos de propagação foram adicionados. 
  
### <a name="performing-batch-calculation"></a>Executando o cálculo de lote

Cálculo de lote é executado como a próxima etapa quando treinamento for concluído com êxito (quando um status de treinamento estável é mostrado pela barra de progresso, uma marca de seleção e o status estável na dica de ferramenta.) Cálculo de lote aplica o conhecimento adquirido durante o treinamento de relevância à população todo o arquivo, para avaliar a relevância dos arquivos e atribuir as pontuações de relevância.
  
Quando houver mais de um problema, cálculo de lote é feito por um problema. Durante o cálculo de lote, progresso é monitorado durante o processamento de todos os arquivos. 
  
Aqui, a próxima etapa recomendada é "None", que indica que nenhuma treinamento de relevância repetitivo adicional é necessário nesse momento. A próxima fase é o **relevância \> decida** tab. 
  
Se você deseja importar novos arquivos após o cálculo de lote, o administrador pode adicionar os arquivos importados para uma nova carga.
  
> [!NOTE]
> Se você clicar em **Cancelar** durante o cálculo de lote, o processo salva o que já foi executado. Se você executar novamente o cálculo do lote, o processo continuará partir do último ponto executado. 
  
### <a name="assessing-tagging-consistency"></a>Avaliando a marcação de consistência

Se houver inconsistências no arquivo de marcação, ele pode afetar a análise. A marcação de processo de consistência de eDiscovery avançada pode ser usada quando os resultados não forem ideais ou consistência está em dúvida. Uma lista dos arquivos de forma inconsistente marcados possíveis é retornada, e pode ser examinados e novamente marcados, conforme necessário.
  
> [!NOTE]
> Após sete ou mais Arredonda treinamento seguir avaliação, consistência de marcação pode ser exibida em **relevância** \> **Track** \> **problema** \> **resultados detalhados** \> **progresso de treinamento**. Este examinar é feita para um problema ao mesmo tempo. 
  
1. No **relevância \> Track**, expanda linha de um problema.
    
2. À direita da **próxima etapa**, clique em **Modificar**.
    
3. Selecione **inconsistências de marca** como a opção de **próxima etapa** , após sete exemplos de treinamento e clique **Okey**.
    
4. Selecione **inconsistências de marca**. Na guia **marca** abre exibindo uma lista das inconsistências para marcar novamente conforme necessário. 
    
5. Clique em **Calcular** para enviar as alterações. A próxima etapa depois de marcar inconsistências é "treinamento". 
    
## <a name="viewing-and-using-relevance-results"></a>Exibindo e usando resultados de relevância

No **relevância \> Track** guia, expanda a linha de um problema e ao lado de **resultados detalhados**, clique em **Exibir**. Os painéis de resultados detalhados são exibidos, conforme mostrado e descrito abaixo.
  
![Resultados detalhado do treinamento de relevância](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a>Resumo de marcação

 No exemplo mostrado abaixo, a **marcação resumida** exibe os totais para cada um dos arquivo os processos de marcação, treinamento e avaliação. 
  
![Resumo de marcação de controle de relevância](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a>Palavras-chave

Uma palavra-chave é uma cadeia de caracteres exclusiva, word, frase ou sequência de palavras em um arquivo identificado por eDiscovery avançado, como um indicador de significativo se um arquivo é relevante. As colunas de "Include" listam palavra-chave e espessuras nos arquivos marcados como relevantes e as colunas "Excluir" lista palavras-chave e espessuras nos arquivos marcados como não é relevante.
  
EDiscovery avançado atribui valores de peso de negativo ou positivo de palavra-chave. O peso maior, maior a probabilidade de que um arquivo no qual a palavra-chave aparece é atribuído com uma pontuação maior de relevância durante o cálculo de lote. 
  
A lista de descoberta eletrônica avançada de palavras-chave pode ser usada para complementar uma lista criada por um especialista ou como uma verificação de integridade indiretas a qualquer momento no arquivo do processo de revisão.
  
### <a name="training-progress"></a>Progresso do treinamento

Painel de **Progresso de treinamento** inclui um treinamento progresso qualidade e gráfico indicador display, conforme mostrado no exemplo a seguir. 
  
![Progresso do treinamento do Controle de Relevância](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 **Indicador de qualidade de treinamento**: exibe a classificação da marca consistência da seguinte maneira:
  
- **BOM**: arquivos estão marcados de forma consistente. (Luz verde exibido)
    
- **Médio**: alguns arquivos podem ser marcados de forma inconsistente. (Amarelo claro exibido)
    
- **Aviso**: muitos arquivos podem ser marcados de forma inconsistente. (Luz vermelha exibido)
    
 **Gráfico de progresso de treinamento**: mostra o grau de estabilidade de treinamento de relevância após um número de ciclos de treinamento de relevância em comparação com o valor da medida de F. Como podemos mover da esquerda para a direita pelo gráfico, restringe o intervalo de confiança e é usado, junto com a medida de F, por eDiscovery avançado relevância para determinar a estabilidade quando o treinamento de relevância de resultados otimizados.
  
> [!NOTE]
> Relevância usa F2, uma métrica de medida de F onde Recall recebe o dobro peso como precisão. Para casos com riqueza alta (mais de 25%), usos de relevância F1 (taxa de 1:1). A taxa de medida de F pode ser configurada na **instalação de relevância** \> **Configurações avançadas**. 
  
### <a name="batch-calculation-results"></a>Resultados do cálculo de lote

Painel de **resultados de cálculo de lote** inclui o número de arquivos que foram marcados para a relevância, da seguinte maneira: 
  
- **Êxito**
    
- **Vazio**: não contém texto, por exemplo, somente espaços/guias
    
- **Falha**: devido ao tamanho excessivo ou não pôde ser lido
    
- **Ignorado**: devido ao tamanho excessivo
    
- **Nebulous**: contém texto insignificante ou nenhuma recursos relevantes para o problema
    
> [!NOTE]
> Vazio, falhou, Ignored ou Nebulous receberá uma pontuação de relevância de -1. 
  
### <a name="training-statistics"></a>Estatísticas de treinamento

O painel de **estatísticas de treinamento** exibe estatísticas e gráficos com base nos resultados de treinamento de relevância de descoberta eletrônica avançado. 
  
![Estatística do treinamento do controle de relevância](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
Este modo de exibição mostra o seguinte:
  
- **Taxa de cancelamento de revisão**: pontuações de comparação dos resultados de acordo com a relevância em uma revisão Hipoteticamente linear. Cancelamento é estimado de acordo com o conjunto de tamanho do conjunto de revisão.
    
- **Parâmetros**: cumulativa calculado das estatísticas referentes à revisão definida em relação à população arquivo para o caso de inteiro.
    
- **Revise**: porcentagem de arquivos para analisar com base neste corte.
    
- **Cancelar**: arquivos de porcentagem de relevante no conjunto de revisão. 
    
- **Distribuição por pontuação de relevância**: arquivos na exibição cinza escuro para a esquerda estão abaixo a pontuação de fechamento. Uma dica de ferramenta exibe a pontuação de relevância e a porcentagem relacionada de arquivos no arquivo revisão definido em relação aos arquivos total.
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Executando e revisão de avaliação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Executando o treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Tomar decisões com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

