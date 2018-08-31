---
title: Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Saiba como usar a segurança do Office 365 &amp; Centro de conformidade para acessar o eDiscovery avançadas do Office 365 e execute o módulo de processo para uma ocorrência.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524066"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="fac76-103">Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="fac76-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="fac76-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="fac76-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="fac76-106">Esta seção descreve a funcionalidade do módulo de processo de descoberta eletrônica avançado.</span><span class="sxs-lookup"><span data-stu-id="fac76-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="fac76-p102">Além dos dados de arquivo, metadados, como o tipo de arquivo, extensão, local ou caminho, data de criação e tempo, dos responsáveis, autor e assunto, podem ser carregado no avançada de descoberta eletrônica e salva para cada caso. Por exemplo, alguns metadados é calculado por eDiscovery avançado, quando os arquivos nativos são carregados.</span><span class="sxs-lookup"><span data-stu-id="fac76-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="fac76-p103">EDiscovery avançado fornece valores de metadados, agrupamentos de quase duplicados ou as pontuações de relevância de sistema. Outros metadados, como anotações de arquivo, podem ser adicionados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="fac76-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="fac76-111">Processo em execução</span><span class="sxs-lookup"><span data-stu-id="fac76-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="fac76-p104">Números de lote são atribuídos a um arquivo durante o processo para permitir que o controle dos arquivos. O número de lote também permite que a identificação de lotes de processo para opções de reprocessamento. Filtros adicionais estão disponíveis para filtrar por número de lote e sessões.</span><span class="sxs-lookup"><span data-stu-id="fac76-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="fac76-115">Execute as seguintes etapas para executar o processo.</span><span class="sxs-lookup"><span data-stu-id="fac76-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="fac76-116">[Abrir a segurança do Office 365 &amp; Centro de conformidade](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="fac76-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="fac76-117">Vá para **pesquisa &amp; investigação** \> **eDiscovery** e, em seguida, clique em **Ir para descoberta eletrônica avançada**.</span><span class="sxs-lookup"><span data-stu-id="fac76-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="fac76-118">No eDiscovery avançada, selecione o caso apropriado na página **casos** exibida e clique em **Ir para o caso**.</span><span class="sxs-lookup"><span data-stu-id="fac76-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="fac76-119">Em **Prepare** \> **processo** \> **instalação**, selecione um contêiner da lista de recipientes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fac76-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Clique em processar para adicionar os resultados da pesquisa ao caso](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="fac76-121">Clique em **… Configurações avançadas** , se você deseja adicionar o contêiner, como arquivos de propagação ou como arquivos previamente marcados.</span><span class="sxs-lookup"><span data-stu-id="fac76-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="fac76-p105">Usar arquivos de propagação para acelerar o treinamento para problemas com baixa riqueza (geralmente 2% ou menos). Para arquivos de propagação, é recomendável que você selecione uma variedade de arquivos distintamente relevantes e processar sobre sementes 20 e 50 por problema (muitos arquivos de propagação podem distorcer os resultados de relevância). Arquivos de propagação devem ser revisados pela mesma pessoa que irá treinar o problema.</span><span class="sxs-lookup"><span data-stu-id="fac76-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="fac76-p106">Use arquivos previamente marcados para automatizar treinamento de relevância. Você deve marcar pelo menos 1.500 arquivos e manter a proporção de relevantes para arquivos não relevantes os mesmos que a coleção adicionada a relevância. Esses arquivos devem ser marcados manualmente, e você deve ter a certeza na qualidade da marcação.</span><span class="sxs-lookup"><span data-stu-id="fac76-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Captura de tela de avançadas a página de configurações de processamento de arquivos em lotes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="fac76-129">Na seção de **propagação** :</span><span class="sxs-lookup"><span data-stu-id="fac76-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="fac76-p107">Escolha **Marcar como arquivos de propagação** para marcar o contêiner como arquivos de propagação. Você também precisa escolher para atribuí-las por um problema de **problema** drop-down. Escolha **relevantes** ou **não é relevante** no menu suspenso **marca** .</span><span class="sxs-lookup"><span data-stu-id="fac76-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fac76-133">Depois que você definir arquivos como **propagação**, você não pode marcá-las como **previamente marcado**.</span><span class="sxs-lookup"><span data-stu-id="fac76-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="fac76-134">Na seção **arquivos previamente marcados** :</span><span class="sxs-lookup"><span data-stu-id="fac76-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="fac76-p108">Escolha **Marcar como arquivos previamente marcados** para marcar o contêiner como arquivos previamente marcados. Você também precisará atribuí-las por um problema de **problema** drop-down. Escolha **relevantes** ou **não é relevante** no menu suspenso **marca** .</span><span class="sxs-lookup"><span data-stu-id="fac76-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fac76-138">Depois que você definir arquivos como **previamente marcado**, você não pode marcá-las como **propagação**.</span><span class="sxs-lookup"><span data-stu-id="fac76-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="fac76-p109">Na seção **Email marcação** . conjunto que parte de um email processado devem ser marcada como propagação ou previamente marcado.</span><span class="sxs-lookup"><span data-stu-id="fac76-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="fac76-p110">Para começar, clique em **processo**. Quando concluir, os resultados do processo são exibidos.</span><span class="sxs-lookup"><span data-stu-id="fac76-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="fac76-143">(Opcional) Se você precisa atribuir a fontes de dados para dos responsáveis específico, você pode adicionar e editar os nomes dos responsáveis em **responsáveis** \> **Gerenciar** e atribuir responsáveis em **responsáveis** \> **atribuir**.</span><span class="sxs-lookup"><span data-stu-id="fac76-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="fac76-144">Se você adicionar ao caso, você pode processar novamente.</span><span class="sxs-lookup"><span data-stu-id="fac76-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fac76-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="fac76-145">See also</span></span>

[<span data-ttu-id="fac76-146">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="fac76-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="fac76-147">Exibição de resultados de módulo de processo</span><span class="sxs-lookup"><span data-stu-id="fac76-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

