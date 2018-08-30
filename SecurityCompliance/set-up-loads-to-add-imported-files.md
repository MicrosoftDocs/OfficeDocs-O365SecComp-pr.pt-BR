---
title: Configurar carregamentos para adicionar arquivos importados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Revise as etapas para adicionar arquivos importados ao última carga definidos ou lote, de arquivos antes da execução de treinamento de relevância no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524578"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="6e3b9-103">Configurar carregamentos para adicionar arquivos importados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6e3b9-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="6e3b9-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="6e3b9-p102">EDiscovery avançado, uma carga é um novo lote de arquivos adicionados a um caso. Por padrão, uma carga é definida e todos os arquivos importados são adicionados a ela. Antes de executar o treinamento de relevância, os arquivos importados devem ser adicionados à carga.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="6e3b9-109">Considere os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="6e3b9-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="6e3b9-p103">Novos arquivos são conhecidos como se parecer com os arquivos anteriores carregados no banco de dados caso ou a carga anterior de arquivos era um conjunto aleatório usando o conjunto de arquivos. Neste exemplo, adicione os arquivos importados para o carregamento de arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="6e3b9-p104">Novos arquivos são diferentes daqueles anteriores (por exemplo, a partir de uma fonte diferente), ou você não tiver nenhum conhecimento prévio que elas são semelhantes ou diferentes para as cargas anteriores. Neste cenário, adicione os arquivos importados para um novo arquivo de carga. EDiscovery avançado reconhece isso como um cenário de cargas sem interrupção, chama um processo que os, bloqueia o treinamento de relevância e cálculos de lote até que o ajuste for concluída, e a nova carga é integrada e treinada.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="6e3b9-115">Adicionando arquivos importados para a carga atual</span><span class="sxs-lookup"><span data-stu-id="6e3b9-115">Adding imported files to the current load</span></span>

<span data-ttu-id="6e3b9-p105">Todos os arquivos importados devem ser adicionados a uma carga a serem processados no eDiscovery avançado. Arquivos importados são adicionados à última carga definida. Se você importar arquivos adicionais posteriormente, eles também devem ser adicionados à carga.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="6e3b9-119">No **relevância \> instalação relevância** guia, selecione **cargas**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Guia Cargas de Configuração de Relevância](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="6e3b9-p106">**Arquivos de inclusão**: selecionar uma opção para arquivos a serem incluídos. Por padrão, a adição de arquivos para a carga atual baseado na população "Todos os arquivos".</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="6e3b9-p107">Carrege todos os arquivos culled disponíveis na relevância. Se você pretende carregar apenas um subconjunto dos arquivos disponíveis, primeiro consulte com suporte, como carregar subconjuntos pode prejudicar o treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="6e3b9-125">Em **gerenciamento de cargas**, selecione uma carga.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="6e3b9-p108">Clique em **Adicionar arquivos**. Os arquivos são adicionados à carga e uma mensagem de confirmação é exibida.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="6e3b9-128">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-128">Click **OK**.</span></span>
    
<span data-ttu-id="6e3b9-129">Os arquivos agora podem ser processados no eDiscovery avançado relevância para os arquivos de treinamento.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="6e3b9-130">Um nome de carga dentro de um caso de edição</span><span class="sxs-lookup"><span data-stu-id="6e3b9-130">Editing a load name within a case</span></span>

<span data-ttu-id="6e3b9-131">Se a alteração do nome de carga, é recomendável usar um nome que é relevante ao caso.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="6e3b9-132">No **relevância \> instalação relevância** guia, selecione **cargas**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="6e3b9-p109">Na lista de **cargas de gerenciamento** , selecione uma carga e clique no ícone **Editar** . A janela de carga de editar é exibida.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="6e3b9-135">Insira as alterações e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="6e3b9-136">Adicionando arquivos importados para uma nova carga</span><span class="sxs-lookup"><span data-stu-id="6e3b9-136">Adding imported files to a new load</span></span>

<span data-ttu-id="6e3b9-137">Depois de iniciar o treinamento de relevância ou executando o cálculo de lote, convém importar e processar um conjunto adicional de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="6e3b9-p110">Durante o ajuste, você pode criar, marcar e analisar o conjunto de ajuste. EDiscovery avançado compara sua avaliação dos arquivos relevantes e não-relevantes na carga da nova no carregamentos anteriores. Com base nos resultados, você é solicitado a tomar decisões de recuperar o atraso, se necessário e avançado eDiscovery fornece recomendações com base nas informações de relevância acumuladas.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="6e3b9-141">Aplicação de cargas e funcionalidade os varia da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6e3b9-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="6e3b9-142">Quando você importa um novo arquivo de carga após o cálculo de lote, o eDiscovery avançado determina até que ponto os arquivos se encaixam em uma das seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="6e3b9-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="6e3b9-143">Semelhante (homogêneo): um round novo e personalizado de treinamento de relevância não é necessária e o conhecimento acumulado pela carga anterior pode ser aplicado "no estado em que se encontra" à carga nova.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="6e3b9-144">DISTINCT (heterogêneo): um round novo e personalizado de treinamento de relevância é necessária e o conhecimento acumulado pela carga anterior não pode ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="6e3b9-145">Esses termos referem-se ao nível de semelhança de arquivos entre cargas e não no carrega.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="6e3b9-p111">Ao importar um novo arquivo de carga durante o treinamento de relevância (antes de cálculo de lote), ajuste permite continuar treinamento relevância fazendo o conjunto de arquivos Unido. Descoberta eletrônica avançada não estimar se a carga nova é semelhante ao ou distinta da carga anterior. Ele simplesmente coleta informações sobre a nova carga e habilita a relevância de treinamento continuar na nova e anterior define dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="6e3b9-149">Quando houver várias questões em treinamento de relevância, bem como problemas após o cálculo de lote, o processo de recuperar o atraso é executado uma vez por todos os problemas e os resultados são calculados e exibidos para cada questão.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6e3b9-p112">O tamanho da amostra recuperar o atraso pode variar. Ele depende do tamanho da carga nova em relação às cargas anteriores e o número de amostras concluídas antes de adicionar a nova carga. O exemplo de ajuste geralmente é um conjunto de arquivos de 200 para 2.000 para a nova carga.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="6e3b9-p113">Recuperar o atraso interrompe quaisquer outras tarefas e requer revisão e marcação de arquivo individuais. Portanto, você pode reduzir sobrecarga quando você adiciona novos arquivos em grandes lotes.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="6e3b9-155">Adicionar uma nova carga de arquivo usando os e sem interrupção carrega</span><span class="sxs-lookup"><span data-stu-id="6e3b9-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="6e3b9-156">No **relevância \> instalação relevância** guia, selecione **cargas**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="6e3b9-p114">Em **gerenciamento de cargas**, clique o **+** ícone para adicionar uma carga. Uma mensagem de confirmação é exibida.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="6e3b9-p115">Clique em **Sim** para continuar. A caixa de diálogo **Adicionar novo carregar** é exibida.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6e3b9-161">Você só pode adicionar uma nova carga se ações foram realizadas à carga anterior.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="6e3b9-p116">Na caixa de diálogo **Adicionar novo de carga** , digite as informações de **carregar o nome** e a **Descrição** e clique em **Okey**. EDiscovery avançado adiciona uma nova carga.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="6e3b9-p117">Para importar o novo arquivo de carga, clique em **Adicionar arquivos**. Todos os novos arquivos são adicionados a essa carga. Depois de descoberta eletrônica avançada importa os arquivos, ela reconhece o cenário de cargas sem interrupção e indica ajuste como a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="6e3b9-167">Clique em **recuperar o atraso** na parte inferior da caixa de diálogo para executar o cenário.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="6e3b9-168">Um único conjunto de recuperar o atraso, normalmente contendo os arquivos de 200 para 2.000 da carga de novo, é criado para todos os problemas permitir a marcação de arquivo simultâneo.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="6e3b9-169">São fornecidos detalhes sobre se cargas são similares ou distintos, se o eDiscovery avançado mescladas ou divididas o carrega automaticamente e informações relacionadas ao processamento na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="6e3b9-p118">Você pode marcar os arquivos e executar uma operação de calcular. A marcação habilita a relevância determinar se as cargas são similares ou distintos e permite que você continuar trabalhando com o novo conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="6e3b9-172">Depois que o conjunto de recuperar o atraso é analisado, exibir **relevância \> Track** para os resultados do ajuste.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="6e3b9-173">Se a nova carga de arquivo foi adicionada durante o treinamento de relevância (isto é, o problema ainda não tiver passaram pelo cálculo de lote), **treinamento continuar** é a próxima etapa, independentemente dos resultados do ajuste.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="6e3b9-p119">As cargas de novas e anteriores são processadas como uma carga e treinamento de relevância continua no conjunto Unido. Você agora estiverem terminadas com este procedimento e pode continuar treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="6e3b9-176">Se a carga nova foi adicionada após o cálculo de lote, vá para as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="6e3b9-177">Para cargas novas adicionadas após o cálculo de lote, eDiscovery avançado determina se a nova carga é semelhante ao ou distintos de carregamentos anteriores, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6e3b9-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="6e3b9-p120">Se cargas encontradas para ser semelhante: nenhum treinamento relevância adicional é necessário. O painel mostra a próxima etapa recomendada é executar * * cálculo de lote * * novamente para calcular as pontuações de relevância para o novo carregamento. Cargas foram encontradas seja semelhante, de modo a análise de classificador anterior pode ser executada em novos arquivos.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run ** Batch calculation ** again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="6e3b9-p121">Se cargas encontradas distinto: treinamento mais relevância é necessário e a próxima etapa é a decisão de ajuste. Selecione uma decisão de ajuste da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="6e3b9-p122">Se você selecionar **Mesclar cargas**, eDiscovery avançado mescla cargas anteriores e novas para o conjunto de treinamento. Embora a primeira carga passou pelo cálculo em lotes, mais treinamento será necessária. Continue treinamento cargas novas e anteriores juntos. Cálculo de lote, em seguida, será executado novamente e as pontuações de cálculo de lote anteriores devem ser ignoradas. Escolha esta seleção quando as pontuações de relevância de cargas existentes podem ser recalculadas, por exemplo, quando a revisão dos carregamentos de arquivo existente não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="6e3b9-p123">Se você selecionar a **divisão carrega**, continue treinamento relevância somente sobre a carga de nova. Neste exemplo, pontuações de cálculo de lote anteriores permanecerá como está. Escolha esta opção quando não da pontuações de relevância existentes para cargas existentes seja recalculadas, por exemplo, se a revisão de cargas existentes já tenha sido iniciada. As pontuações de relevância são gerenciadas separadamente a partir deste ponto em diante e não podem ser mescladas.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="6e3b9-192">Clique em **continuar treinamento**.</span><span class="sxs-lookup"><span data-stu-id="6e3b9-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e3b9-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e3b9-193">See also</span></span>

[<span data-ttu-id="6e3b9-194">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6e3b9-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="6e3b9-195">Definindo os problemas e como atribuir usuários</span><span class="sxs-lookup"><span data-stu-id="6e3b9-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="6e3b9-196">Definindo realçado palavras-chave e avançadas opções</span><span class="sxs-lookup"><span data-stu-id="6e3b9-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

