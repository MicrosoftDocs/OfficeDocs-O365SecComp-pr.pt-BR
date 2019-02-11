---
title: Use o módulo de relevância para analisar dados no eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56e83a1f8a951fd6e14172122a5e86447c6f2ccf
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695167"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a>Use o módulo de relevância para analisar dados no eDiscovery avançado (Preview)

No eDiscovery avançado (Preview), o módulo de relevância inclui o treinamento de relevância e a revisão dos arquivos relacionados a um caso. O fluxo de trabalho de relevância é exibido e descrito a seguir:
  
![Fluxo de trabalho de relevância](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Ciclos de avaliação e de rastreamento**:
    
  - **Avaliação**: habilita a avaliação preliminar com base em uma amostra aleatória de arquivos e usa essa avaliação para aplicar decisões para determinar o desempenho do processo de codificação de previsão. 
    
  - **Acompanhar**: calcular e exibir resultados provisórios da avaliação ao monitorar estatística validade do processo. 
    
- **Ciclos de treinamento e controle**
    
  - **Marca**: eDiscovery avançado (Preview) aprende critérios de relevância específicos para cada questão com base na revisão de repetitivo do especialista e marcação de arquivos individuais.
    
  - **Acompanhar**: calcular e exibir resultados provisórios do treinamento ao monitorar estatística validade do processo de relevância. 
    
- **Cálculo de lote**: os critérios de relevância aprendidos e acumulados é aplicado à coleção todo o arquivo e uma pontuação de relevância é gerada para cada arquivo.
    
- **Decida**: os resultados da análise aplicada ao caso inteiro é exibido após o cálculo de lote e dados usados para tomar decisões de revisão de documento são exibidos.
    
- **Teste**: resultados podem ser testados para verificar a validade e a eficácia do processamento de eDiscovery avançado (Preview).

- **Pesquisa**: quando o fluxo de trabalho de relevância for concluído, você pode usar a saída como percentil de leitura de um documento para seu problema quando você executa uma consulta em seu conjunto de trabalho.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Diretrizes para treinamento de relevância e revisão

A seguir está uma visão geral das diretrizes para treinamento de relevância e revisão:
  
- **Erros e inconsistências**: se erros de marcação são feitos durante o treinamento, retorne à amostras de arquivo anterior para corrigi-los. Se há muitos erros para corrigir ou não há uma nova perspectiva do problema ou caso, os critérios de relevância devem ser redefinidos pelo administrador e o treinamento de relevância reiniciados.
    
- **Treinamento e marcação**: 
    
  - Arquivos devem ser marcados com base no conteúdo apenas. Não consideram metadados, como dos responsáveis, data ou caminho do arquivo. 
    
  - Não consideram data indicações de intervalo do texto quando os arquivos de marcação.
    
  - Não consideram imagens gráficas incorporadas quando os arquivos de marcação.
     
  - Ignorar texto aplicado a relevância será removido no conteúdo do arquivo exibido no modo de exibição de texto em relevância. Se os valores para Ignorar texto foram definidos após a relevância já treinamento Introdução, o novo texto ignorado será aplicado aos arquivos de exemplo criados a partir do ponto no qual ele foi definido. O recurso Ignorar texto deve ser usado com cautela, como usá-las pode reduzir o desempenho da análise de arquivo
    
  - Use a opção **Ignorar a marcação** somente quando necessário. EDiscovery avançado (Preview) não treinar com base em arquivos ignorados. Na avaliação, se é difícil identificar se um arquivo é relevante, é melhor a marca como Relevant (R) ou não relevante (NR) sempre que possível, em vez de selecionando **Ignorar**. Quando o eDiscovery avançado (Preview) avalia treinamento, ele poderá ser visto quão bem esses tipos de arquivos foram processados.
    
  - Mesmo com um valor muito pequeno do texto extraído os arquivos deve ser marcado em treinamento como R/NR, e não como "Ignorar", quando possível. 
    
  - Marcação pode afetar o classificador, desde que o arquivo pode ser lido e pode ser marcado como R/NR.
    
  - O número de sequência de arquivo na lista de arquivos de amostra exibida na guia **marca** permite que o usuário retornar na ordem exibida original dos arquivos. 
    
  - Você pode voltar à qualquer amostra e alterar a marcação de avaliação e treinamento definidas para arquivos. As alterações serão aplicadas ao criar o próximo exemplo.
    
  - Excel descoberta arquivos no formato PDF devem ser tratados da mesma como arquivos nativos do Excel quando os arquivos de marcação.
    
  - Quando estiver em dúvida sobre a marcação de relevância de um arquivo, consulte um especialista. Marcação incorreto durante o treinamento de relevância pode causar perda de tempo posteriormente no processo e também pode ter um impacto negativo sobre a qualidade dos resultados gerais.
    
  - Palavras-chave que foram definidas no palavras-chave listas serão exibidas em cores para ajudar o usuário a identificar arquivos relevantes durante a marcação.
    
- **Cálculo de lote**: arquivos que foram marcados como R/NR pelo especialista receberá uma pontuação entre 0 e 100. Isso se aplica a marcação feitas antes de cálculo de lote. Se o especialista alternado o problema para ocioso após o cálculo de lote e continua a marcação esse problema, as pontuações recentemente marcadas não será 100/0, mas em vez disso, a pontuação original.
    
- **Problemas e modo de amostragem**: problemas são normalmente desativados quando o trabalho neles é concluído (treinamento de relevância é estabilizado e cálculo de lote foi realizado), quando os problemas são cancelados ou quando outro usuário está funcionando sobre os problemas.
    
## <a name="steps-in-relevance-training"></a>Etapas em treinamento de relevância

No **relevância \> Track** guia, o eDiscovery avançado oferece recomendações sobre como prosseguir no processamento, com as próximas etapas a seguir. As implicações estão descritas a seguir quando cada uma das etapas a seguir é recomendada no processo de treinamento de relevância. 
  
- Marcação / continuar a marcação: revisão do arquivo e a marcação de relevância realizado por um especialista para cada arquivo e emitir dentro de uma amostra.
    
  - Implicação: Uma amostra existente deve ser marcado.
    
- Avaliação / continuar assessment: habilita a validação inicial de relevância de ocorrência do problema e uma exibição preliminar da relevância da população arquivo importada para o caso atual.
    
  - Implicação: Avaliação mais é necessário ou recomendada.
    
- Treinamento / continuar treinamento: processo durante o qual avançado eDiscovery aprende com o especialista que é o arquivo de marcação amostras e adquire a capacidade de identificar os critérios de relevância pertinentes à cada questão dentro do contexto de cada caso.
    
  - Implicação: O problema precisa mais treinamento; o próximo exemplo deve ser criado e marcado. 
    
- Cálculo de lote: processo de relevância no qual avançado eDiscovery leva o conhecimento adquirido durante o estágio de treinamento e aplica à população todo o arquivo. Todos os arquivos no grupo de arquivos pertinentes são avaliados para a relevância e atribuídos a uma pontuação de relevância.
    
  - Implicação: O problema tem estabilizada e cálculo de lote pode ser executado.
    
- Recuperar o atraso: Relevância indica quando um especialista analisa e marcas de obter um exemplo dos arquivos selecionados de um carregamento de arquivo adicionais durante um cenário de aplicação do carrega.
    
  - Implicação: Foi adicionada uma nova carga e recuperar o atraso é necessário para continuar trabalhando.
    
- Marcar inconsistências: processo identifica, por meio de um algoritmo de descoberta eletrônica avançado, inconsistências no arquivo de marcação de processo que pode ter um impacto negativo a análise.
    
  - Implicação: O próximo exemplo incluirá arquivos que foram marcados nos exemplos anteriores e seus recursos de marcação devem ser refeito.
    
- Atualizar classificador: permite ao usuário aplicar marcação ou alterações de propagação.
    
  - Implicação: Marcação e propagação alterações podem ser aplicadas sem precisar executar manualmente o outro exemplo de relevância.
    
- Em espera: A relevância treinamento processo seja concluído.
    
  - Implicação: Nenhum treinamento relevância é necessário nesse momento.
    
Embora eDiscovery avançado orienta você durante o processo, com próximas etapas recomendadas em estágios diferentes, ele também permite que você para navegar entre páginas e guias e fazer escolhas em situações de endereço que podem ser pertinentes à sua caso individual, o problema, ou processo de revisão de documento. 
  
É possível aceitar ou substituir a próxima etapa de descoberta eletrônica avançada escolhas de processamento. Se você deseja executar uma etapa que não seja a próxima etapa recomendada, clique na **próxima etapa** listados na exibição expandida problema na caixa de diálogo, clique no botão **Modificar** ao lado da próxima etapa e selecione outra opção de etapa em próximo. 
  
> [!NOTE]
> Algumas opções podem permanecer desabilitadas após desbloqueando conforme eles não são suportados para uso nesse momento no processo. 
  
## <a name="more-information"></a>Mais informações

[Noções básicas sobre avaliação na relevância](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](../test-relevance-analysis-in-advanced-ediscovery.md)

[Consultar dentro do conjunto de trabalho](working-set-search.md)
