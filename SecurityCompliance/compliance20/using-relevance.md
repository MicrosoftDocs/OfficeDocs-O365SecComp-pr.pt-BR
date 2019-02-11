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
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a><span data-ttu-id="785c1-102">Use o módulo de relevância para analisar dados no eDiscovery avançado (Preview)</span><span class="sxs-lookup"><span data-stu-id="785c1-102">Use the Relevance module to analyze data in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="785c1-p101">No eDiscovery avançado (Preview), o módulo de relevância inclui o treinamento de relevância e a revisão dos arquivos relacionados a um caso. O fluxo de trabalho de relevância é exibido e descrito a seguir:</span><span class="sxs-lookup"><span data-stu-id="785c1-p101">In Advanced eDiscovery (Preview), the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Fluxo de trabalho de relevância](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="785c1-106">**Ciclos de avaliação e de rastreamento**:</span><span class="sxs-lookup"><span data-stu-id="785c1-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="785c1-107">**Avaliação**: habilita a avaliação preliminar com base em uma amostra aleatória de arquivos e usa essa avaliação para aplicar decisões para determinar o desempenho do processo de codificação de previsão.</span><span class="sxs-lookup"><span data-stu-id="785c1-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="785c1-108">**Acompanhar**: calcular e exibir resultados provisórios da avaliação ao monitorar estatística validade do processo.</span><span class="sxs-lookup"><span data-stu-id="785c1-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="785c1-109">**Ciclos de treinamento e controle**</span><span class="sxs-lookup"><span data-stu-id="785c1-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="785c1-110">**Marca**: eDiscovery avançado (Preview) aprende critérios de relevância específicos para cada questão com base na revisão de repetitivo do especialista e marcação de arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="785c1-110">**Tag**: Advanced eDiscovery (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="785c1-111">**Acompanhar**: calcular e exibir resultados provisórios do treinamento ao monitorar estatística validade do processo de relevância.</span><span class="sxs-lookup"><span data-stu-id="785c1-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="785c1-112">**Cálculo de lote**: os critérios de relevância aprendidos e acumulados é aplicado à coleção todo o arquivo e uma pontuação de relevância é gerada para cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="785c1-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="785c1-113">**Decida**: os resultados da análise aplicada ao caso inteiro é exibido após o cálculo de lote e dados usados para tomar decisões de revisão de documento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="785c1-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="785c1-114">**Teste**: resultados podem ser testados para verificar a validade e a eficácia do processamento de eDiscovery avançado (Preview).</span><span class="sxs-lookup"><span data-stu-id="785c1-114">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery (Preview) processing.</span></span>

- <span data-ttu-id="785c1-115">**Pesquisa**: quando o fluxo de trabalho de relevância for concluído, você pode usar a saída como percentil de leitura de um documento para seu problema quando você executa uma consulta em seu conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="785c1-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="785c1-116">Diretrizes para treinamento de relevância e revisão</span><span class="sxs-lookup"><span data-stu-id="785c1-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="785c1-117">A seguir está uma visão geral das diretrizes para treinamento de relevância e revisão:</span><span class="sxs-lookup"><span data-stu-id="785c1-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="785c1-p102">**Erros e inconsistências**: se erros de marcação são feitos durante o treinamento, retorne à amostras de arquivo anterior para corrigi-los. Se há muitos erros para corrigir ou não há uma nova perspectiva do problema ou caso, os critérios de relevância devem ser redefinidos pelo administrador e o treinamento de relevância reiniciados.</span><span class="sxs-lookup"><span data-stu-id="785c1-p102">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="785c1-120">**Treinamento e marcação**:</span><span class="sxs-lookup"><span data-stu-id="785c1-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="785c1-p103">Arquivos devem ser marcados com base no conteúdo apenas. Não consideram metadados, como dos responsáveis, data ou caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="785c1-p103">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="785c1-123">Não consideram data indicações de intervalo do texto quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="785c1-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="785c1-124">Não consideram imagens gráficas incorporadas quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="785c1-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="785c1-p104">Ignorar texto aplicado a relevância será removido no conteúdo do arquivo exibido no modo de exibição de texto em relevância. Se os valores para Ignorar texto foram definidos após a relevância já treinamento Introdução, o novo texto ignorado será aplicado aos arquivos de exemplo criados a partir do ponto no qual ele foi definido. O recurso Ignorar texto deve ser usado com cautela, como usá-las pode reduzir o desempenho da análise de arquivo</span><span class="sxs-lookup"><span data-stu-id="785c1-p104">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="785c1-p105">Use a opção **Ignorar a marcação** somente quando necessário. EDiscovery avançado (Preview) não treinar com base em arquivos ignorados. Na avaliação, se é difícil identificar se um arquivo é relevante, é melhor a marca como Relevant (R) ou não relevante (NR) sempre que possível, em vez de selecionando **Ignorar**. Quando o eDiscovery avançado (Preview) avalia treinamento, ele poderá ser visto quão bem esses tipos de arquivos foram processados.</span><span class="sxs-lookup"><span data-stu-id="785c1-p105">Use the **Skip tagging** option only when necessary. Advanced eDiscovery (Preview) does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="785c1-132">Mesmo com um valor muito pequeno do texto extraído os arquivos deve ser marcado em treinamento como R/NR, e não como "Ignorar", quando possível.</span><span class="sxs-lookup"><span data-stu-id="785c1-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="785c1-133">Marcação pode afetar o classificador, desde que o arquivo pode ser lido e pode ser marcado como R/NR.</span><span class="sxs-lookup"><span data-stu-id="785c1-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="785c1-134">O número de sequência de arquivo na lista de arquivos de amostra exibida na guia **marca** permite que o usuário retornar na ordem exibida original dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="785c1-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="785c1-p106">Você pode voltar à qualquer amostra e alterar a marcação de avaliação e treinamento definidas para arquivos. As alterações serão aplicadas ao criar o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="785c1-p106">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="785c1-137">Excel descoberta arquivos no formato PDF devem ser tratados da mesma como arquivos nativos do Excel quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="785c1-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="785c1-p107">Quando estiver em dúvida sobre a marcação de relevância de um arquivo, consulte um especialista. Marcação incorreto durante o treinamento de relevância pode causar perda de tempo posteriormente no processo e também pode ter um impacto negativo sobre a qualidade dos resultados gerais.</span><span class="sxs-lookup"><span data-stu-id="785c1-p107">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="785c1-140">Palavras-chave que foram definidas no palavras-chave listas serão exibidas em cores para ajudar o usuário a identificar arquivos relevantes durante a marcação.</span><span class="sxs-lookup"><span data-stu-id="785c1-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="785c1-p108">**Cálculo de lote**: arquivos que foram marcados como R/NR pelo especialista receberá uma pontuação entre 0 e 100. Isso se aplica a marcação feitas antes de cálculo de lote. Se o especialista alternado o problema para ocioso após o cálculo de lote e continua a marcação esse problema, as pontuações recentemente marcadas não será 100/0, mas em vez disso, a pontuação original.</span><span class="sxs-lookup"><span data-stu-id="785c1-p108">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="785c1-144">**Problemas e modo de amostragem**: problemas são normalmente desativados quando o trabalho neles é concluído (treinamento de relevância é estabilizado e cálculo de lote foi realizado), quando os problemas são cancelados ou quando outro usuário está funcionando sobre os problemas.</span><span class="sxs-lookup"><span data-stu-id="785c1-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="785c1-145">Etapas em treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="785c1-145">Steps in Relevance training</span></span>

<span data-ttu-id="785c1-p109">No **relevância \> Track** guia, o eDiscovery avançado oferece recomendações sobre como prosseguir no processamento, com as próximas etapas a seguir. As implicações estão descritas a seguir quando cada uma das etapas a seguir é recomendada no processo de treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="785c1-p109">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="785c1-148">Marcação / continuar a marcação: revisão do arquivo e a marcação de relevância realizado por um especialista para cada arquivo e emitir dentro de uma amostra.</span><span class="sxs-lookup"><span data-stu-id="785c1-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="785c1-149">Implicação: Uma amostra existente deve ser marcado.</span><span class="sxs-lookup"><span data-stu-id="785c1-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="785c1-150">Avaliação / continuar assessment: habilita a validação inicial de relevância de ocorrência do problema e uma exibição preliminar da relevância da população arquivo importada para o caso atual.</span><span class="sxs-lookup"><span data-stu-id="785c1-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="785c1-151">Implicação: Avaliação mais é necessário ou recomendada.</span><span class="sxs-lookup"><span data-stu-id="785c1-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="785c1-152">Treinamento / continuar treinamento: processo durante o qual avançado eDiscovery aprende com o especialista que é o arquivo de marcação amostras e adquire a capacidade de identificar os critérios de relevância pertinentes à cada questão dentro do contexto de cada caso.</span><span class="sxs-lookup"><span data-stu-id="785c1-152">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="785c1-153">Implicação: O problema precisa mais treinamento; o próximo exemplo deve ser criado e marcado.</span><span class="sxs-lookup"><span data-stu-id="785c1-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="785c1-p110">Cálculo de lote: processo de relevância no qual avançado eDiscovery leva o conhecimento adquirido durante o estágio de treinamento e aplica à população todo o arquivo. Todos os arquivos no grupo de arquivos pertinentes são avaliados para a relevância e atribuídos a uma pontuação de relevância.</span><span class="sxs-lookup"><span data-stu-id="785c1-p110">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="785c1-156">Implicação: O problema tem estabilizada e cálculo de lote pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="785c1-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="785c1-157">Recuperar o atraso: Relevância indica quando um especialista analisa e marcas de obter um exemplo dos arquivos selecionados de um carregamento de arquivo adicionais durante um cenário de aplicação do carrega.</span><span class="sxs-lookup"><span data-stu-id="785c1-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="785c1-158">Implicação: Foi adicionada uma nova carga e recuperar o atraso é necessário para continuar trabalhando.</span><span class="sxs-lookup"><span data-stu-id="785c1-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="785c1-159">Marcar inconsistências: processo identifica, por meio de um algoritmo de descoberta eletrônica avançado, inconsistências no arquivo de marcação de processo que pode ter um impacto negativo a análise.</span><span class="sxs-lookup"><span data-stu-id="785c1-159">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="785c1-160">Implicação: O próximo exemplo incluirá arquivos que foram marcados nos exemplos anteriores e seus recursos de marcação devem ser refeito.</span><span class="sxs-lookup"><span data-stu-id="785c1-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="785c1-161">Atualizar classificador: permite ao usuário aplicar marcação ou alterações de propagação.</span><span class="sxs-lookup"><span data-stu-id="785c1-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="785c1-162">Implicação: Marcação e propagação alterações podem ser aplicadas sem precisar executar manualmente o outro exemplo de relevância.</span><span class="sxs-lookup"><span data-stu-id="785c1-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="785c1-163">Em espera: A relevância treinamento processo seja concluído.</span><span class="sxs-lookup"><span data-stu-id="785c1-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="785c1-164">Implicação: Nenhum treinamento relevância é necessário nesse momento.</span><span class="sxs-lookup"><span data-stu-id="785c1-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="785c1-165">Embora eDiscovery avançado orienta você durante o processo, com próximas etapas recomendadas em estágios diferentes, ele também permite que você para navegar entre páginas e guias e fazer escolhas em situações de endereço que podem ser pertinentes à sua caso individual, o problema, ou processo de revisão de documento.</span><span class="sxs-lookup"><span data-stu-id="785c1-165">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="785c1-p111">É possível aceitar ou substituir a próxima etapa de descoberta eletrônica avançada escolhas de processamento. Se você deseja executar uma etapa que não seja a próxima etapa recomendada, clique na **próxima etapa** listados na exibição expandida problema na caixa de diálogo, clique no botão **Modificar** ao lado da próxima etapa e selecione outra opção de etapa em próximo.</span><span class="sxs-lookup"><span data-stu-id="785c1-p111">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="785c1-168">Algumas opções podem permanecer desabilitadas após desbloqueando conforme eles não são suportados para uso nesse momento no processo.</span><span class="sxs-lookup"><span data-stu-id="785c1-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="785c1-169">Mais informações</span><span class="sxs-lookup"><span data-stu-id="785c1-169">More information</span></span>

[<span data-ttu-id="785c1-170">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="785c1-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="785c1-171">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="785c1-171">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="785c1-172">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="785c1-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="785c1-173">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="785c1-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="785c1-174">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="785c1-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="785c1-175">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="785c1-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="785c1-176">Consultar dentro do conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="785c1-176">Query within working set</span></span>](working-set-search.md)
