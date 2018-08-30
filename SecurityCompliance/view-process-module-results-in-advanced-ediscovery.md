---
title: Exibir os resultados do Módulo de processo na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Saiba mais sobre como localizar os resultados de um módulo de processo executar em eDiscovery avançadas do Office 365, incluindo o status da tarefa e o processo de resumo.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523470"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="2c610-103">Exibir os resultados do Módulo de processo na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2c610-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="2c610-104">Após **Preparar** \> **processo** é iniciado, você pode exibir o andamento e os resultados.</span><span class="sxs-lookup"><span data-stu-id="2c610-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c610-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="2c610-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="2c610-107">Status do processo de tarefa</span><span class="sxs-lookup"><span data-stu-id="2c610-107">Process task status</span></span>

<span data-ttu-id="2c610-108">Em **Prepare** \> **processo** \> **resultados**, a página mostra o status atual (se o processo está sendo executado) ou o último status de tarefa de status do processo conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c610-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![Status da tarefa do módulo de processamento](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="2c610-110">As tarefas exibidas podem variar dependendo das opções de processo selecionadas.</span><span class="sxs-lookup"><span data-stu-id="2c610-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="2c610-111">**Inventário**: eDiscovery avançado itera todos os arquivos selecionados para o processo e executa a coleta de dados básica.</span><span class="sxs-lookup"><span data-stu-id="2c610-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="2c610-112">**Calcular assinaturas**: calcula as assinaturas digitais de MD5.</span><span class="sxs-lookup"><span data-stu-id="2c610-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="2c610-p102">**Extração de compostos**: extrai interna ou contida arquivos recursivamente de arquivos compostos (por exemplo, PST, ZIP, MSG). Arquivos extraídos são armazenados na pasta maiusculas do caso.</span><span class="sxs-lookup"><span data-stu-id="2c610-p102">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG). Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="2c610-115">**Banco de dados de sincronização**: o processo de banco de dados interno.</span><span class="sxs-lookup"><span data-stu-id="2c610-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="2c610-p103">**Cópia de arquivo**: arquivos do processo de cópias. Essa tarefa é sempre exibida, mesmo quando a opção avançada de arquivos de cópia está selecionada.</span><span class="sxs-lookup"><span data-stu-id="2c610-p103">**File copy**: Copies Process files. This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="2c610-p104">**Extração de texto**: quando houver arquivos nativos, eDiscovery avançado extrai o texto desses arquivos usando DTSearch. O texto extraído desses arquivos é armazenado como arquivos de texto na pasta maiusculas.</span><span class="sxs-lookup"><span data-stu-id="2c610-p104">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch. The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="2c610-120">**Atualizando metadados**: processa os metadados carregado.</span><span class="sxs-lookup"><span data-stu-id="2c610-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="2c610-121">**Finalizing**: processamento interno que finaliza dados de carregado arquivos maiusculas (por exemplo, identificar os arquivos de erro e êxito).</span><span class="sxs-lookup"><span data-stu-id="2c610-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="2c610-p105">Status da tarefa: exibido após a conclusão da tarefa. Enquanto estiver executando tarefas, a duração da execução é exibida.</span><span class="sxs-lookup"><span data-stu-id="2c610-p105">Task status: Displayed after task completion. While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c610-124">Tarefas concluídas também podem incluir totais de arquivos que o processamento foi concluído ou arquivos com erros.</span><span class="sxs-lookup"><span data-stu-id="2c610-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="2c610-p106">"Cancelar" fornece uma opção de reversão para interromper a execução do processo e, em seguida, reverta para a população de dados anterior ou salvo dados processados. Reversão limpa processados todos os dados. Se você não quiser que os dados processados a ser perdida (por exemplo, você planeja recarregar esses arquivos), selecione o "Cancelar" opção nessa janela escolher não fazer a reversão.</span><span class="sxs-lookup"><span data-stu-id="2c610-p106">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data. Rollback clears all processed data. If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="2c610-128">Resumo do processo</span><span class="sxs-lookup"><span data-stu-id="2c610-128">Process summary</span></span>

<span data-ttu-id="2c610-129">Em Prepare \> processo \> resultados \> Process resumo, uma divisão dos resultados de arquivo carregado é exibida de acordo com os resultados de processamento e de erro do arquivo bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2c610-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="2c610-130">Os painéis apresentam uma exibição gráfica das estatísticas de arquivo importado, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2c610-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="2c610-131">Todos os arquivos no caso de d: **Resumo de processo se acumulam**.</span><span class="sxs-lookup"><span data-stu-id="2c610-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="2c610-132">**Resumo do processo de última**: arquivos carregados da última sessão, ou ação.</span><span class="sxs-lookup"><span data-stu-id="2c610-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="2c610-133">**Famílias últimos**: informações de família no caso (se houver).</span><span class="sxs-lookup"><span data-stu-id="2c610-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="2c610-134">Se os arquivos de **propagação** foram adicionados, o número de arquivos de propagação é listado por problema que foi definido para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="2c610-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="2c610-135">Se a marcação dos arquivos de **propagação** falhou, que também é citado.</span><span class="sxs-lookup"><span data-stu-id="2c610-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="2c610-136">Se o arquivos **previamente marcado** foram adicionados, o número de arquivos previamente marcados estará listado por problema que foi definido para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="2c610-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="2c610-137">Se a marcação de arquivos **previamente marcado** falhou, que também é citado.</span><span class="sxs-lookup"><span data-stu-id="2c610-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Resumo do módulo de processamento](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="2c610-139">Resumo de processo acumulados e último gráficos</span><span class="sxs-lookup"><span data-stu-id="2c610-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="2c610-140">Barra à esquerda inclui fonte + arquivos extraídos: qual é a todos os arquivos encontrados.</span><span class="sxs-lookup"><span data-stu-id="2c610-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="2c610-141">À direita da barra, processadas, inclui:</span><span class="sxs-lookup"><span data-stu-id="2c610-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="2c610-142">Arquivos com erros de carregamento</span><span class="sxs-lookup"><span data-stu-id="2c610-142">Files with load errors</span></span>
    
- <span data-ttu-id="2c610-143">Arquivos carregados com êxito, que podem incluir:</span><span class="sxs-lookup"><span data-stu-id="2c610-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="2c610-144">**Existente**: arquivos que foram carregados antes e agora são carregados novamente (incluindo duplicatas).</span><span class="sxs-lookup"><span data-stu-id="2c610-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="2c610-145">**Texto**: arquivos exclusivos com texto.</span><span class="sxs-lookup"><span data-stu-id="2c610-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="2c610-146">**Não-texto**: esvaziar arquivos de texto, arquivos de texto nativo vazio, arquivos de texto não nativos.</span><span class="sxs-lookup"><span data-stu-id="2c610-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="2c610-147">**Duplicar**o s: duplicata arquivos com texto.</span><span class="sxs-lookup"><span data-stu-id="2c610-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="2c610-148">Últimos erros do processo</span><span class="sxs-lookup"><span data-stu-id="2c610-148">Last process errors</span></span>

<span data-ttu-id="2c610-149">Em Prepare \> processo \> resultados \> últimos erros de processo, detalhes dos erros na última ação realizada ou sessão são exibidos.</span><span class="sxs-lookup"><span data-stu-id="2c610-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Erros do módulo de processamento](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="2c610-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c610-151">See also</span></span>

[<span data-ttu-id="2c610-152">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2c610-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="2c610-153">Executando o módulo de processo e carregamento de dados</span><span class="sxs-lookup"><span data-stu-id="2c610-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

