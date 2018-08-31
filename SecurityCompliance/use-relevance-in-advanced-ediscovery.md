---
title: Usar o Módulo de relevância na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Saiba mais sobre o módulo de relevância no eDiscovery avançadas do Office 365, incluindo um fluxo de trabalho e as diretrizes e as etapas para revisão de treinamento e o arquivo.  '
ms.openlocfilehash: 2cf75ef95291c5393367ce01fb0cd660f9b99145
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523816"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="3dc80-103">Usar o Módulo de relevância na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="3dc80-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="3dc80-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="3dc80-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="3dc80-p102">No eDiscovery avançado, o módulo de relevância inclui o treinamento de relevância e a revisão dos arquivos relacionados a um caso. O fluxo de trabalho de relevância é exibido e descrito a seguir:</span><span class="sxs-lookup"><span data-stu-id="3dc80-p102">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Fluxo de trabalho de relevância](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="3dc80-109">**Ciclos de avaliação e de rastreamento**:</span><span class="sxs-lookup"><span data-stu-id="3dc80-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="3dc80-110">**Avaliação**: eDiscovery avançada permite avaliação preliminar com base em uma amostra aleatória de arquivos e usa essa avaliação para aplicar decisões para determinar o desempenho do processo de codificação de previsão.</span><span class="sxs-lookup"><span data-stu-id="3dc80-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="3dc80-111">**Acompanhar**: eDiscovery avançado calcula e exibe resultados provisórios da avaliação ao monitorar estatística validade do processo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="3dc80-112">**Ciclos de treinamento e acompanhamento**:</span><span class="sxs-lookup"><span data-stu-id="3dc80-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="3dc80-113">**Marca**: eDiscovery avançado aprende critérios de relevância específicos para cada questão com base na revisão de repetitivo do especialista e marcação de arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="3dc80-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="3dc80-114">**Acompanhar**: eDiscovery avançado calcula e exibe resultados provisórios do treinamento ao monitorar estatística validade do processo de relevância.</span><span class="sxs-lookup"><span data-stu-id="3dc80-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="3dc80-115">**Cálculo de lote**: eDiscovery avançado leva os critérios de relevância aprendidos e acumulados, aplica-se à coleção todo o arquivo e gera as pontuações de relevância de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="3dc80-116">**Decida**: eDiscovery Avançado exibe os resultados da análise aplicada ao caso inteiro após o cálculo de lote e exibe dados para tomar decisões de revisão do documento.</span><span class="sxs-lookup"><span data-stu-id="3dc80-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="3dc80-117">**Teste**: eDiscovery avançado resultados podem ser testados para verificar a validade e a eficácia do processamento de descoberta eletrônica avançado.</span><span class="sxs-lookup"><span data-stu-id="3dc80-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="3dc80-118">Diretrizes para treinamento de relevância e revisão</span><span class="sxs-lookup"><span data-stu-id="3dc80-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="3dc80-119">A seguir está uma visão geral das diretrizes para treinamento de relevância e revisão:</span><span class="sxs-lookup"><span data-stu-id="3dc80-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="3dc80-p103">**Erros e inconsistências**: se erros de marcação são feitos durante o treinamento, retorne à amostras de arquivo anterior para corrigi-los. Se há muitos erros para corrigir ou não há uma nova perspectiva do problema ou caso, os critérios de relevância devem ser redefinidos pelo administrador e o treinamento de relevância reiniciados.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p103">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="3dc80-122">**Treinamento e marcação**:</span><span class="sxs-lookup"><span data-stu-id="3dc80-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="3dc80-p104">Arquivos devem ser marcados com base no conteúdo apenas. Não consideram metadados, como dos responsáveis, data ou caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p104">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="3dc80-125">Não consideram data indicações de intervalo do texto quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="3dc80-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="3dc80-126">Não consideram imagens gráficas incorporadas quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="3dc80-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="3dc80-p105">Se a exibição de um arquivo usando o ícone **formatada de modo de exibição de texto** durante a marcação não considera a formatação do texto. Por exemplo, uma palavra exibida com um tachado (uma linha horizontal por meio de seu centro, indicando a exclusão) ainda é considerada por relevância como parte do texto analisado.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p105">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text. For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="3dc80-p106">Ignorar texto aplicado a relevância (conforme definido pelo Gerenciador de maiusculas ou administrador) serão removidos no conteúdo do arquivo exibido no modo de exibição de texto em relevância. Se os valores para Ignorar texto foram definidos após a relevância já treinamento Introdução, o novo texto ignorado será aplicado aos arquivos de exemplo criados a partir do ponto no qual ele foi definido. O recurso Ignorar texto deve ser usado com cautela, como usá-las pode reduzir o desempenho da análise de arquivo</span><span class="sxs-lookup"><span data-stu-id="3dc80-p106">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="3dc80-p107">Use a opção **Ignorar a marcação** somente quando necessário. EDiscovery avançada não treinar com base em arquivos ignorados. Na avaliação, se é difícil identificar se um arquivo é relevante, é melhor a marca como Relevant (R) ou não relevante (NR) sempre que possível, em vez de selecionando **Ignorar**. Quando o eDiscovery avançado avalia treinamento, ele poderá ser visto quão bem esses tipos de arquivos foram processados.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p107">Use the **Skip tagging** option only when necessary. Advanced eDiscovery does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="3dc80-136">Mesmo com um valor muito pequeno do texto extraído os arquivos deve ser marcado em treinamento como R/NR, e não como "Ignorar", quando possível.</span><span class="sxs-lookup"><span data-stu-id="3dc80-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="3dc80-137">Marcação pode afetar o classificador, desde que o arquivo pode ser lido e pode ser marcado como R/NR.</span><span class="sxs-lookup"><span data-stu-id="3dc80-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="3dc80-138">O número de sequência de arquivo na lista de arquivos de amostra exibida na guia **marca** permite que o usuário retornar na ordem exibida original dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="3dc80-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="3dc80-p108">Você pode voltar à qualquer amostra e alterar a marcação de avaliação e treinamento definidas para arquivos. As alterações serão aplicadas ao criar o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p108">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="3dc80-141">Excel descoberta arquivos no formato PDF devem ser tratados da mesma como arquivos nativos do Excel quando os arquivos de marcação.</span><span class="sxs-lookup"><span data-stu-id="3dc80-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="3dc80-p109">Quando estiver em dúvida sobre a marcação de relevância de um arquivo, consulte um especialista. Marcação incorreto durante o treinamento de relevância pode causar perda de tempo posteriormente no processo e também pode ter um impacto negativo sobre a qualidade dos resultados gerais.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p109">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="3dc80-144">Palavras-chave que foram definidas no palavras-chave listas serão exibidas em cores para ajudar o usuário a identificar arquivos relevantes durante a marcação.</span><span class="sxs-lookup"><span data-stu-id="3dc80-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="3dc80-p110">**Cálculo de lote**: arquivos que foram marcados como R/NR pelo especialista receberá uma pontuação entre 0 e 100. Isso se aplica a marcação feitas antes de cálculo de lote. Se o especialista alternado o problema para ocioso após o cálculo de lote e continua a marcação esse problema, as pontuações recentemente marcadas não será 100/0, mas em vez disso, a pontuação original.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p110">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="3dc80-148">**Problemas e modo de amostragem**: problemas são normalmente desativados quando o trabalho neles é concluído (treinamento de relevância é estabilizado e cálculo de lote foi realizado), quando os problemas são cancelados ou quando outro usuário está funcionando sobre os problemas.</span><span class="sxs-lookup"><span data-stu-id="3dc80-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="3dc80-149">Etapas em treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="3dc80-149">Steps in Relevance training</span></span>

<span data-ttu-id="3dc80-p111">No **relevância \> Track** guia, o eDiscovery avançado oferece recomendações sobre como prosseguir no processamento, com as próximas etapas a seguir. As implicações estão descritas a seguir quando cada uma das etapas a seguir é recomendada no processo de treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p111">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="3dc80-152">Marcação / continuar a marcação: revisão do arquivo e a marcação de relevância realizado por um especialista para cada arquivo e emitir dentro de uma amostra.</span><span class="sxs-lookup"><span data-stu-id="3dc80-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="3dc80-153">Implicação: Uma amostra existente deve ser marcado.</span><span class="sxs-lookup"><span data-stu-id="3dc80-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="3dc80-154">Avaliação / continuar assessment: habilita a validação inicial de relevância de ocorrência do problema e uma exibição preliminar da relevância da população arquivo importada para o caso atual.</span><span class="sxs-lookup"><span data-stu-id="3dc80-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="3dc80-155">Implicação: Avaliação mais é necessário ou recomendada.</span><span class="sxs-lookup"><span data-stu-id="3dc80-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="3dc80-156">Treinamento / continuar treinamento: processo durante o qual avançado eDiscovery aprende com o especialista que é o arquivo de marcação amostras e adquire a capacidade de identificar os critérios de relevância pertinentes à cada questão dentro do contexto de cada caso.</span><span class="sxs-lookup"><span data-stu-id="3dc80-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="3dc80-157">Implicação: O problema precisa mais treinamento; o próximo exemplo deve ser criado e marcado.</span><span class="sxs-lookup"><span data-stu-id="3dc80-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="3dc80-p112">Cálculo de lote: processo de relevância no qual avançado eDiscovery leva o conhecimento adquirido durante o estágio de treinamento e aplica à população todo o arquivo. Todos os arquivos no grupo de arquivos pertinentes são avaliados para a relevância e atribuídos a uma pontuação de relevância.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p112">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="3dc80-160">Implicação: O problema tem estabilizada e cálculo de lote pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="3dc80-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="3dc80-161">Recuperar o atraso: Relevância indica quando um especialista analisa e marcas de obter um exemplo dos arquivos selecionados de um carregamento de arquivo adicionais durante um cenário de aplicação do carrega.</span><span class="sxs-lookup"><span data-stu-id="3dc80-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="3dc80-162">Implicação: Foi adicionada uma nova carga e recuperar o atraso é necessário para continuar trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3dc80-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="3dc80-163">Marcar inconsistências: processo identifica, por meio de um algoritmo de descoberta eletrônica avançado, inconsistências no arquivo de marcação de processo que pode ter um impacto negativo a análise.</span><span class="sxs-lookup"><span data-stu-id="3dc80-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="3dc80-164">Implicação: O próximo exemplo incluirá arquivos que foram marcados nos exemplos anteriores e seus recursos de marcação devem ser refeito.</span><span class="sxs-lookup"><span data-stu-id="3dc80-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="3dc80-165">Atualizar classificador: permite ao usuário aplicar marcação ou alterações de propagação.</span><span class="sxs-lookup"><span data-stu-id="3dc80-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="3dc80-166">Implicação: Marcação e propagação alterações podem ser aplicadas sem precisar executar manualmente o outro exemplo de relevância.</span><span class="sxs-lookup"><span data-stu-id="3dc80-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="3dc80-167">Em espera: A relevância treinamento processo seja concluído.</span><span class="sxs-lookup"><span data-stu-id="3dc80-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="3dc80-168">Implicação: Nenhum treinamento relevância é necessário nesse momento.</span><span class="sxs-lookup"><span data-stu-id="3dc80-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="3dc80-169">Embora eDiscovery avançado orienta você durante o processo, com próximas etapas recomendadas em estágios diferentes, ele também permite que você para navegar entre páginas e guias e fazer escolhas em situações de endereço que podem ser pertinentes à sua caso individual, o problema, ou processo de revisão de documento.</span><span class="sxs-lookup"><span data-stu-id="3dc80-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="3dc80-p113">É possível aceitar ou substituir a próxima etapa de descoberta eletrônica avançada escolhas de processamento. Se você deseja executar uma etapa que não seja a próxima etapa recomendada, clique na **próxima etapa** listados na exibição expandida problema na caixa de diálogo, clique no botão **Modificar** ao lado da próxima etapa e selecione outra opção de etapa em próximo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-p113">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3dc80-172">Algumas opções podem permanecer desabilitadas após desbloqueando conforme eles não são suportados para uso nesse momento no processo.</span><span class="sxs-lookup"><span data-stu-id="3dc80-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dc80-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dc80-173">See also</span></span>

[<span data-ttu-id="3dc80-174">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="3dc80-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-175">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="3dc80-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-176">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="3dc80-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-177">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="3dc80-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-178">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="3dc80-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-179">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="3dc80-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3dc80-180">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="3dc80-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

