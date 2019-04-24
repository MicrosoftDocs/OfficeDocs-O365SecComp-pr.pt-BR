---
title: Executar o módulo de processo e carregar dados na descoberta eletrônica avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Saiba como usar o centro de conformidade de &amp; segurança do Office 365 para acessar a descoberta eletrônica avançada do Office 365 e executar o módulo de processo para um caso.  '
ms.openlocfilehash: 95c73c034ed2ffa1c45f9aacd8463c497a842859
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261391"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8e3c9-103">Executar o módulo de processo e carregar dados na descoberta eletrônica avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="8e3c9-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8e3c9-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="8e3c9-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8e3c9-106">Esta seção descreve a funcionalidade do módulo de processo de descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="8e3c9-107">Além dos dados de arquivo, os metadados como tipo de arquivo, extensão, local ou caminho, data e hora de criação, autor, responsáveis e assunto podem ser carregados na descoberta eletrônica avançada e salvos para cada caso.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-107">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case.</span></span> <span data-ttu-id="8e3c9-108">Alguns metadados são calculados pela descoberta eletrônica avançada, por exemplo, quando os arquivos nativos são carregados.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-108">Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="8e3c9-109">A descoberta eletrônica avançada fornece valores de metadados do sistema, como agrupamento Near-Duplicate ou pontuações de relevância.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-109">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores.</span></span> <span data-ttu-id="8e3c9-110">Outros metadados, como anotações de arquivo, podem ser adicionados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-110">Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="8e3c9-111">Processo em execução</span><span class="sxs-lookup"><span data-stu-id="8e3c9-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="8e3c9-112">Os números de lote são atribuídos a um arquivo durante o processo para permitir o controle de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-112">Batch numbers are assigned to a file during Process to allow the tracking of files.</span></span> <span data-ttu-id="8e3c9-113">O número de lote também permite a identificação de lotes de processos para reprocessamento de opções.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-113">The batch number also enables identification of Process batches for reprocessing options.</span></span> <span data-ttu-id="8e3c9-114">Filtros adicionais estão disponíveis para filtragem por número de lote e sessões.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-114">Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="8e3c9-115">Execute as etapas a seguir para executar o processo.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="8e3c9-116">[Abra o centro de conformidade &amp; de segurança do Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3c9-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="8e3c9-117">Vá para \> **descoberta eletrônica** de \*\* &amp; investigação\*\* e clique em **ir para descoberta eletrônica avançada**.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="8e3c9-118">Em descoberta eletrônica avançada, selecione o caso apropriado na página **casos** exibidos e clique em **ir para o caso**.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="8e3c9-119">Na **configuração** **preparar** \> **processo** \> , selecione um contêiner na lista de contêineres disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Clique em processar para adicionar os resultados da pesquisa ao caso](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="8e3c9-121">Clique em **Configurações avançadas...** se você deseja adicionar o contêiner como arquivos semente ou como arquivos previamente marcados.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="8e3c9-122">Use arquivos semente para acelerar o treinamento para problemas com riqueza baixa (geralmente 2% ou menos).</span><span class="sxs-lookup"><span data-stu-id="8e3c9-122">Use seed files to accelerate training for issues with low richness (usually 2%, or less).</span></span> <span data-ttu-id="8e3c9-123">Para arquivos semente, é recomendável que você selecione uma variedade de arquivos distintomente relevantes e processe cerca de 20-50 sementes por problema (muitos arquivos semente podem distorcer os resultados de relevância).</span><span class="sxs-lookup"><span data-stu-id="8e3c9-123">For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results).</span></span> <span data-ttu-id="8e3c9-124">Os arquivos semente devem ser revisados pela mesma pessoa que vai treinar o problema.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-124">Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="8e3c9-125">Use arquivos previamente marcados para automatizar o treinamento de relevância.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-125">Use pre-tagged files to automate Relevance training.</span></span> <span data-ttu-id="8e3c9-126">Você deve marcar pelo menos 1.500 arquivos e manter a proporção de arquivos que não são relevantes o mesmo que o da coleção adicionado à relevância.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-126">You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance.</span></span> <span data-ttu-id="8e3c9-127">Esses arquivos devem ser marcados manualmente e você deve ter certeza na qualidade da marcação.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-127">These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Captura de tela da página de configurações avançadas para processar arquivos em lotes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="8e3c9-129">Na seção **propagação** :</span><span class="sxs-lookup"><span data-stu-id="8e3c9-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="8e3c9-130">Escolha **Marcar como arquivos semente** para marcar o contêiner como arquivos semente.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-130">Choose **Mark as seed files** to mark the container as seed files.</span></span> <span data-ttu-id="8e3c9-131">Você também precisa optar por atribuí-los por problema no menu suspenso **para o problema** .</span><span class="sxs-lookup"><span data-stu-id="8e3c9-131">You also need choose to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="8e3c9-132">Escolha **relevante** ou **não relevante** na lista suspensa **marca** .</span><span class="sxs-lookup"><span data-stu-id="8e3c9-132">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8e3c9-133">Depois de definir os arquivos como **semente**, você não pode marcá-los como **previamente marcados**.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="8e3c9-134">Na seção **arquivos previamente marcados** :</span><span class="sxs-lookup"><span data-stu-id="8e3c9-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="8e3c9-135">Escolha **Marcar como arquivos previamente marcados** para marcar o contêiner como arquivos previamente marcados.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-135">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files.</span></span> <span data-ttu-id="8e3c9-136">Você também precisará atribuí-los por problema no menu suspenso **para o problema** .</span><span class="sxs-lookup"><span data-stu-id="8e3c9-136">You also need to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="8e3c9-137">Escolha **relevante** ou **não relevante** na lista suspensa **marca** .</span><span class="sxs-lookup"><span data-stu-id="8e3c9-137">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8e3c9-138">Depois de definir os arquivos como **previamente marcados**, você não pode marcá-los como **semente**.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="8e3c9-139">Na seção **marcação** de emails.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-139">In the **Email tagging** section.</span></span> <span data-ttu-id="8e3c9-140">defina qual parte de um email processado deve ser marcada como semente ou pré-selecionado.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-140">set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="8e3c9-141">Para começar, clique em **processar**.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-141">To begin, click **Process**.</span></span> <span data-ttu-id="8e3c9-142">Quando concluído, os resultados do processo são exibidos.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-142">When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="8e3c9-143">Opcion Se for necessário atribuir fontes de dados a um determinado, você poderá adicionar e editar os \*\*\*\* \> nomes dos responsáveis pelo **Gerenciamento** e atribuir os responsáveis pela \*\*\*\* \> **atribuição**de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="8e3c9-144">Se você adicionar à ocorrência, então poderá processar novamente.</span><span class="sxs-lookup"><span data-stu-id="8e3c9-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e3c9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e3c9-145">See also</span></span>

[<span data-ttu-id="8e3c9-146">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="8e3c9-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="8e3c9-147">Exibir resultados do módulo de processo</span><span class="sxs-lookup"><span data-stu-id="8e3c9-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

