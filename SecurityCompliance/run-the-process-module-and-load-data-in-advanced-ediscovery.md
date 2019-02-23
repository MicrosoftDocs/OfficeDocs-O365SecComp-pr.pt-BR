---
title: Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365
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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217601"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ce8f3-103">Executar o Módulo de processo e carregar dados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ce8f3-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="ce8f3-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="ce8f3-106">Esta seção descreve a funcionalidade do módulo de processo de descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="ce8f3-p102">Além dos dados de arquivo, os metadados como tipo de arquivo, extensão, local ou caminho, data e hora de criação, autor, responsáveis e assunto podem ser carregados na descoberta eletrônica avançada e salvos para cada caso. Alguns metadados são calculados pela descoberta eletrônica avançada, por exemplo, quando os arquivos nativos são carregados.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="ce8f3-p103">A descoberta eletrônica avançada fornece valores de metadados do sistema, como agrupamento Near-Duplicate ou pontuações de relevância. Outros metadados, como anotações de arquivo, podem ser adicionados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="ce8f3-111">Processo em execução</span><span class="sxs-lookup"><span data-stu-id="ce8f3-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="ce8f3-p104">Os números de lote são atribuídos a um arquivo durante o processo para permitir o controle de arquivos. O número de lote também permite a identificação de lotes de processos para reprocessamento de opções. Filtros adicionais estão disponíveis para filtragem por número de lote e sessões.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="ce8f3-115">Execute as etapas a seguir para executar o processo.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="ce8f3-116">[Abra o centro de conformidade &amp; de segurança do Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8f3-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="ce8f3-117">Vá para \> **descoberta eletrônica** de \*\* &amp; investigação\*\* e clique em **ir para descoberta eletrônica avançada**.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="ce8f3-118">Em descoberta eletrônica avançada, selecione o caso apropriado na página **casos** exibidos e clique em **ir para o caso**.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="ce8f3-119">Na **configuração** **preparar** \> **processo** \> , selecione um contêiner na lista de contêineres disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Clique em processar para adicionar os resultados da pesquisa ao caso](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="ce8f3-121">Clique em **Configurações avançadas...** se você deseja adicionar o contêiner como arquivos semente ou como arquivos previamente marcados.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="ce8f3-p105">Use arquivos semente para acelerar o treinamento para problemas com riqueza baixa (geralmente 2% ou menos). Para arquivos semente, é recomendável que você selecione uma variedade de arquivos distintomente relevantes e processe cerca de 20-50 sementes por problema (muitos arquivos semente podem distorcer os resultados de relevância). Os arquivos semente devem ser revisados pela mesma pessoa que vai treinar o problema.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="ce8f3-p106">Use arquivos previamente marcados para automatizar o treinamento de relevância. Você deve marcar pelo menos 1.500 arquivos e manter a proporção de arquivos que não são relevantes o mesmo que o da coleção adicionado à relevância. Esses arquivos devem ser marcados manualmente e você deve ter certeza na qualidade da marcação.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Captura de tela da página de configurações avançadas para processar arquivos em lotes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="ce8f3-129">Na seção **propagação** :</span><span class="sxs-lookup"><span data-stu-id="ce8f3-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="ce8f3-p107">Escolha **Marcar como arquivos semente** para marcar o contêiner como arquivos semente. Você também precisa optar por atribuí-los por problema no menu suspenso **para o problema** . Escolha **relevante** ou **não relevante** na lista suspensa **marca** .</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ce8f3-133">Depois de definir os arquivos como **semente**, você não pode marcá-los como **previamente marcados**.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="ce8f3-134">Na seção **arquivos previamente marcados** :</span><span class="sxs-lookup"><span data-stu-id="ce8f3-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="ce8f3-p108">Escolha **Marcar como arquivos previamente marcados** para marcar o contêiner como arquivos previamente marcados. Você também precisará atribuí-los por problema no menu suspenso **para o problema** . Escolha **relevante** ou **não relevante** na lista suspensa **marca** .</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ce8f3-138">Depois de definir os arquivos como **previamente marcados**, você não pode marcá-los como **semente**.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="ce8f3-p109">Na seção **marcação** de emails. defina qual parte de um email processado deve ser marcada como semente ou pré-selecionado.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="ce8f3-p110">Para começar, clique em **processar**. Quando concluído, os resultados do processo são exibidos.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="ce8f3-143">Opcion Se for necessário atribuir fontes de dados a um determinado, você poderá adicionar e editar os \*\*\*\* \> nomes dos responsáveis pelo **Gerenciamento** e atribuir os responsáveis pela \*\*\*\* \> **atribuição**de responsáveis.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="ce8f3-144">Se você adicionar à ocorrência, então poderá processar novamente.</span><span class="sxs-lookup"><span data-stu-id="ce8f3-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce8f3-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce8f3-145">See also</span></span>

[<span data-ttu-id="ce8f3-146">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="ce8f3-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ce8f3-147">Exibir resultados do módulo de processo</span><span class="sxs-lookup"><span data-stu-id="ce8f3-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

