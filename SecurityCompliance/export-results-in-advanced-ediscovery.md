---
title: Exportar resultados na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Saiba como definir opções para exportar os resultados do eDiscovery avançadas do Office 365, incluindo o procedimento para especificar os parâmetros de um lote de exportação. '
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524647"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="08f7e-103">Exportar resultados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="08f7e-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="08f7e-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="08f7e-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="08f7e-106">Este tópico descreve as opções de configuração de exportação de eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="08f7e-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="08f7e-107">**Neste tópico:**</span><span class="sxs-lookup"><span data-stu-id="08f7e-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="08f7e-108">Definição de lotes de exportação e sessões</span><span class="sxs-lookup"><span data-stu-id="08f7e-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="08f7e-109">Exportações incrementais e adicionais</span><span class="sxs-lookup"><span data-stu-id="08f7e-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="08f7e-110">Configurar os parâmetros de exportação em lote</span><span class="sxs-lookup"><span data-stu-id="08f7e-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="08f7e-111">Exporte os arquivos de saída de relatório</span><span class="sxs-lookup"><span data-stu-id="08f7e-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="08f7e-112">Definição de lotes de exportação e sessões</span><span class="sxs-lookup"><span data-stu-id="08f7e-112">Defining export batches and sessions</span></span>
<span data-ttu-id="08f7e-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="08f7e-113"></span></span>

<span data-ttu-id="08f7e-p102">Um lote de exportação permite que o processo de exportação usando um conjunto de parâmetros definidos. EDiscovery avançado permite que você defina lotes para personalizar cada exportação.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="08f7e-p103">Parâmetros são definidos por lote de exportação. Um lote denominado "Exportar lote 01" é criado por padrão para o primeiro lote de um caso. Você também pode editar o nome de lote e a descrição.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="08f7e-119">Uma sessão de exportação é uma execução de exportação de eDiscovery avançada dentro de um lote de exportação.</span><span class="sxs-lookup"><span data-stu-id="08f7e-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="08f7e-120">Exportações incrementais e adicionais</span><span class="sxs-lookup"><span data-stu-id="08f7e-120">Incremental and additional exports</span></span>
<span data-ttu-id="08f7e-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="08f7e-121"></span></span>

<span data-ttu-id="08f7e-p104">Você pode executar várias sessões de exportação dentro de um lote de exportação, para garantir resultados consistentes com base nos parâmetros e o mesmo modelo de exportação. Para cada sessão dentro de um lote, você pode exportar analytics para recentemente processados dados maiusculas e processar cada "incrementalmente".</span><span class="sxs-lookup"><span data-stu-id="08f7e-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="08f7e-p105">Para exportar usando um conjunto de parâmetros diferentes, você precisa primeiro criar um novo lote. A primeira sessão no novo lote produzirá resultados para arquivos processados no caso de até o momento, se ou não esses arquivos foram importados e processados por um ou vários importações. Cada lote recalcula dinamização, semelhança, inclusives, etc. Sessões usam os parâmetros definidos para o lote e não recalcular dinamização, semelhança, inclusives, etc. para cada execução da sessão.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="08f7e-p106">Por exemplo, suponha que um caso foi importado e seus dados analisados. Para recuperar perto duplicatas e Email Threading resultados para os dados incrementais, clique em **criar exportar sessão** no mesmo lote que era usado para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="08f7e-129">Configurar os parâmetros de exportação em lote</span><span class="sxs-lookup"><span data-stu-id="08f7e-129">Set up batch export parameters</span></span>
<span data-ttu-id="08f7e-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="08f7e-130"></span></span>

<span data-ttu-id="08f7e-p107">A ferramenta de exportação de descoberta eletrônica é usada para exportar os resultados da pesquisa de descoberta eletrônica avançada ao computador local. Para aumentar a taxa de transferência de transferência de dados e a velocidade o processo de exportação, você pode configurar uma configuração de registro do Windows no computador que você usa para exportar os resultados da pesquisa. Se você quiser aumentar a velocidade de download, configure a configuração do registro antes de configurar os parâmetros de exportação. Para obter mais informações, consulte [aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span><span class="sxs-lookup"><span data-stu-id="08f7e-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="08f7e-135">No eDiscovery avançada, selecione um caso e clique em **Exportar** \> **instalação**.</span><span class="sxs-lookup"><span data-stu-id="08f7e-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
  - <span data-ttu-id="08f7e-136">Na lista **Exportar lote** , selecione o nome do lote ou exportar resultados para o lote de exportação 01, (o lote padrão).</span><span class="sxs-lookup"><span data-stu-id="08f7e-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="08f7e-p108">Para exportar os resultados para novos arquivos adicionados a um caso existente, continue com o lote atual. Para criar uma sessão no lote, selecione o mesmo número de lote e clique em **criar exportar sessão** , você pode usar essa opção para exportar os mesmos parâmetros como o lote anterior, de forma incremental.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="08f7e-p109">Para exportar para um novo lote, clique em **Adicionar**![Adicionar ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)e insira um novo nome em **nome de lote** (ou aceite o padrão) e uma descrição na **Descrição do lote**. Clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p109">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="08f7e-141">Para editar um nome de lote ou descrição, selecione o nome na **exportação em lote**, clique em **Editar** ![ícone Editar](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)e, em seguida, modifique os campos.</span><span class="sxs-lookup"><span data-stu-id="08f7e-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="08f7e-p110">Depois de executar sessões de um lote de exportação, eles não podem ser excluídos. Além disso, apenas alguns parâmetros podem ser editados depois que a primeira sessão é executada.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="08f7e-144">Para criar um lote de exportação duplicados, escolha o **lote de exportação de duplicata**![criar um ícone de lote de exportação duplicados](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) e insira um nome e uma descrição para o lote duplicado no painel.</span><span class="sxs-lookup"><span data-stu-id="08f7e-144">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="08f7e-145">Para excluir um lote de exportação, escolha **Excluir**![excluir um ícone de lote de exportação](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="08f7e-145">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="08f7e-146">Para exibir o histórico de um lote, escolha o **histórico de lote**![ícone de histórico de exibição](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="08f7e-146">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="08f7e-147">Em **população**, selecione **incluir somente os arquivos acima pontuação de interrupção de relevância** e/ou **refinar lote de exportação** , se você quiser ajustar as configurações para o lote de exportação.</span><span class="sxs-lookup"><span data-stu-id="08f7e-147">Under **Population**,Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="08f7e-p111">Se você selecionar a opção **incluir somente os arquivos acima pontuação de interrupção de relevância**, o **problema** é habilitado. Se a pontuação de relevância do arquivo for superior a pontuação de interrupção para o problema selecionado, o arquivo será exportado, a menos que ele é excluído pelo filtro 'para revisão'.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
<span data-ttu-id="08f7e-p112">Se você selecionar **refinar exportação lote**, a **eliminação da duplicação** e filtrar por 'Para revisão' botões de opção de campo são ativados. Se você escolher **eliminação da duplicação**, e os arquivos duplicados serão filtrados de acordo com a política definida [caso nível (padrão): a partir de cada conjunto de arquivos duplicados no caso de inteiro, apenas um arquivo será sua duplicação eliminado. Nível dos responsáveis: de cada conjunto de arquivos duplicados do dos responsáveis mesmo, apenas um arquivo será sua duplicação eliminado.] A saída de exportação contém um registro de todos os arquivos duplicados. Se você escolher campo **Filter by 'para revisão'** , selecione **Modificar em metadados** para inserir suas configurações de campo **'para revisão'** . Selecione **os arquivos de entrada incluir** para incluir os arquivos de origem no conteúdo do pacote. Você pode desmarcar essa configuração para acelerar o processo de exportação. Observe que os arquivos nativos serão exportados em qualquer caso.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="08f7e-157">Em **metadados**, selecione entre as seguintes opções na lista **Exportar modelo** (uma vez por sessão).</span><span class="sxs-lookup"><span data-stu-id="08f7e-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="08f7e-p113">**Padrão**: conjunto básico de propriedades, metadados e itens de dados. Use esta opção quando importar dados já foi processados no eDiscovery avançado e exportar dados são carregados com um sistema que já contém os arquivos. Por padrão, exporte modelo colunas são criadas e preenchidas.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="08f7e-p114">**Todos**: o conjunto completo de metadados padrão, incluindo todos os dados de processamento, bem como as pontuações de analisar e a relevância. Este modelo é necessário quando eDiscovery avançado realiza o processamento e dados de arquivo são carregados no sistema externo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="08f7e-163">**Problemas**: selecione **Todos os problemas** ou selecione um problema específico que você criou.</span><span class="sxs-lookup"><span data-stu-id="08f7e-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="08f7e-164">Em **destino**:</span><span class="sxs-lookup"><span data-stu-id="08f7e-164">Under **Destination**:</span></span>
    
  - <span data-ttu-id="08f7e-165">**Baixe a máquina local**</span><span class="sxs-lookup"><span data-stu-id="08f7e-165">**Download to local machine**</span></span>
    
  - <span data-ttu-id="08f7e-166">**Exportar para definidas pelo usuário blob Azure**: se essa opção estiver marcada, você pode especificar um token de URL e SAS do contêiner.</span><span class="sxs-lookup"><span data-stu-id="08f7e-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="08f7e-p115">Assim que um pacote de exportação é armazenado para o usuário definido Azure blob, os dados não mais são gerenciados por eDiscovery avançado; ele é gerenciado pelo Azure blob. Isso significa que se você excluir o caso, os arquivos exportados ainda vai permanecer no Azure blob.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="08f7e-169">**Salvar SAS token para sessão de exportação futuras**: se estiver marcado, o token SAS será criptografado no banco de dados interno para uso futuro da descoberta eletrônica avançado.</span><span class="sxs-lookup"><span data-stu-id="08f7e-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="08f7e-p116">Atualmente, o token SAS expira após um mês. Se você tentar baixar após mais de um mês em que você precise desfazer última sessão, exporte novamente.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="08f7e-172">Clique em **Modificar** para definir a "para revisão ' Configurações de campo.</span><span class="sxs-lookup"><span data-stu-id="08f7e-172">Click **Modify** to set the "for review' field settings.</span></span> 
    
> ![Configurar para seetings de campo de revisão de um lote de exportação](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> <span data-ttu-id="08f7e-174">Em **Emails** , selecione os emails que você deseja exportar:</span><span class="sxs-lookup"><span data-stu-id="08f7e-174">In **Emails** select the emails you want to export:</span></span> 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> <span data-ttu-id="08f7e-175">Em **documentos** , selecione os documentos que você deseja exportar:</span><span class="sxs-lookup"><span data-stu-id="08f7e-175">In **Documents** select the documents you want to export:</span></span> 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> <span data-ttu-id="08f7e-176">Em **anexos** , selecione os anexos que você deseja exportar</span><span class="sxs-lookup"><span data-stu-id="08f7e-176">In **Attachments** select the attachments you want to export</span></span> 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> <span data-ttu-id="08f7e-p117">Em **Micellaneous** , você pode optar por **Trate anexos como documentos**, **trate emails como documentos**ou **Expandir para incluir arquivos família**. Quando você escolhe **Expand para incluir arquivos família**, para cada arquivo que foi sinalizado para revisão, todos os arquivos da mesma família também serão sinalizados.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p117">In **Micellaneous** you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
    Choose **Save** to save the settings. 
    
7. <span data-ttu-id="08f7e-179">Depois de especificar os parâmetros de exportação, para iniciar o lote de exportação, clique em **criar exportar a sessão**.</span><span class="sxs-lookup"><span data-stu-id="08f7e-179">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="08f7e-p118">Durante a exportação, o status é exibido em **status da tarefa**. Os resultados são exibidos no **Resumo de exportação**.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p118">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
8. <span data-ttu-id="08f7e-182">Na janela de **Download de arquivos** , clique em **Copiar para a área de transferência** para copiar a chave de exportação.</span><span class="sxs-lookup"><span data-stu-id="08f7e-182">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![Baixar arquivos](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. <span data-ttu-id="08f7e-184">Clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="08f7e-184">Click **Close**.</span></span> 
    
    <span data-ttu-id="08f7e-185">A ferramenta de exportação de descoberta eletrônica é iniciada.</span><span class="sxs-lookup"><span data-stu-id="08f7e-185">The eDiscovery Export Tool is started.</span></span>
    
    ![Ferramenta de exportação de Descoberta Eletrônica](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. <span data-ttu-id="08f7e-187">Em que a **ferramenta de exportação de descoberta eletrônica**:</span><span class="sxs-lookup"><span data-stu-id="08f7e-187">In the **eDiscovery Export Tool**:</span></span>
    
1. <span data-ttu-id="08f7e-188">Em **Colar a assinatura de acesso compartilhado que será usada para conectar a fonte**, cole a chave de exportação que youcopied na área de transferência na etapa 7.</span><span class="sxs-lookup"><span data-stu-id="08f7e-188">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
2. <span data-ttu-id="08f7e-189">Clique em **Procurar** para selecionar o local de destino para armazenar os arquivos de exportação baixado na máquina local.</span><span class="sxs-lookup"><span data-stu-id="08f7e-189">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
11. <span data-ttu-id="08f7e-p119">Clique em **Iniciar**. Os arquivos de exportação são baixados para a máquina local. Se você escolher **Exportar para blob Azure definidas pelo usuário** na etapa 4, a sessão é exportada para um destino de URL de armazenamento de Blob de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p119">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span> 
    
<span data-ttu-id="08f7e-192">Para obter uma descrição completa dos campos no relatório de exportação, consulte [exportar campos do relatório](export-report-fields-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="08f7e-192">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="08f7e-193">Exporte os arquivos de saída de relatório</span><span class="sxs-lookup"><span data-stu-id="08f7e-193">Export report output files</span></span>
<span data-ttu-id="08f7e-194"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="08f7e-194"></span></span>

<span data-ttu-id="08f7e-195">A tabela a seguir lista os arquivos de saída que são gerados quando você executa um lote de exportação.</span><span class="sxs-lookup"><span data-stu-id="08f7e-195">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="08f7e-196">**Nome do arquivo**</span><span class="sxs-lookup"><span data-stu-id="08f7e-196">**File name**</span></span>|<span data-ttu-id="08f7e-197">**Tipo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="08f7e-197">**File type**</span></span>|<span data-ttu-id="08f7e-198">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08f7e-198">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08f7e-199">Resumo de exportação</span><span class="sxs-lookup"><span data-stu-id="08f7e-199">Export summary</span></span>  <br/> |<span data-ttu-id="08f7e-200">CSV</span><span class="sxs-lookup"><span data-stu-id="08f7e-200">csv</span></span>  <br/> |<span data-ttu-id="08f7e-201">Um arquivo de log gerado pela ferramenta de exportação de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="08f7e-201">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="08f7e-202">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="08f7e-202">Trace</span></span>  <br/> |<span data-ttu-id="08f7e-203">txt</span><span class="sxs-lookup"><span data-stu-id="08f7e-203">txt</span></span>  <br/> |<span data-ttu-id="08f7e-204">Um arquivo de log gerado pela ferramenta de exportação de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="08f7e-204">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="08f7e-205">Arquivos de texto extraídos</span><span class="sxs-lookup"><span data-stu-id="08f7e-205">Extracted text files</span></span>  <br/> |<span data-ttu-id="08f7e-206">Pasta de arquivo</span><span class="sxs-lookup"><span data-stu-id="08f7e-206">File folder</span></span>  <br/> |<span data-ttu-id="08f7e-207">Pasta que contém os arquivos de texto extraídos dos arquivos exportados.</span><span class="sxs-lookup"><span data-stu-id="08f7e-207">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="08f7e-208">Entrada ou arquivos nativos</span><span class="sxs-lookup"><span data-stu-id="08f7e-208">Input or native files</span></span>  <br/> |<span data-ttu-id="08f7e-209">Pasta de arquivo</span><span class="sxs-lookup"><span data-stu-id="08f7e-209">File folder</span></span>  <br/> |<span data-ttu-id="08f7e-210">Pasta que contém os arquivos nativos e entrados dos arquivos exportados.</span><span class="sxs-lookup"><span data-stu-id="08f7e-210">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="08f7e-211">Lista de exportação</span><span class="sxs-lookup"><span data-stu-id="08f7e-211">Export list</span></span>  <br/> |<span data-ttu-id="08f7e-212">xlsx</span><span class="sxs-lookup"><span data-stu-id="08f7e-212">xlsx</span></span>  <br/> |<span data-ttu-id="08f7e-p120">Metadados de arquivos exportados no formato xlsx. Campos nos arquivos estão de acordo com seleciona de usuário do modelo a ser exportado. Se necessário, vários arquivos são criados, cada um contém linhas de 100 a 150 mil. Se um determinado valor conterá mais caracteres do que uma célula do Excel pode conter (atualmente o limite é 32.767 caracteres), e em seguida, excluirá o valor para o tamanho máximo permitido. Se um valor é cortado, cor de plano de fundo da célula é vermelho para indicar isso ao usuário." Os participantes de email"é um exemplo de um campo que pode exceder o limite de comprimento, se o email foi enviado para uma distribuição grandes. Para obter detalhes sobre os campos de saída, consulte [exportar campos do relatório](export-report-fields-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="08f7e-p120">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="08f7e-219">Carregar arquivo</span><span class="sxs-lookup"><span data-stu-id="08f7e-219">Load file</span></span>  <br/> |<span data-ttu-id="08f7e-220">CSV</span><span class="sxs-lookup"><span data-stu-id="08f7e-220">csv</span></span>  <br/> |<span data-ttu-id="08f7e-p121">Metadados de arquivos exportados no formato csv para carregamento em outro aplicativo. Campos nos arquivos estão de acordo com seleciona de usuário do modelo a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p121">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="08f7e-223">Indicador de sucesso</span><span class="sxs-lookup"><span data-stu-id="08f7e-223">Success indicator</span></span>  <br/> |<span data-ttu-id="08f7e-224">txt</span><span class="sxs-lookup"><span data-stu-id="08f7e-224">txt</span></span>  <br/> |<span data-ttu-id="08f7e-p122">Só é criado durante a exportação para um 3rd Azure blob de terceiros. Se a exportação tiver êxito completamente, o arquivo será criado. Em caso de falha, ou parcial sucesso o arquivo não será criado. Arquivo será criado na pasta raiz, permitindo que automatizado de acompanhamento no status de lotes/sessões de exportação diferentes. Este é um arquivo vazio. Seu nome é: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span><span class="sxs-lookup"><span data-stu-id="08f7e-p122">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08f7e-231">Confira também</span><span class="sxs-lookup"><span data-stu-id="08f7e-231">See also</span></span>
<span data-ttu-id="08f7e-232"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="08f7e-232"></span></span>

[<span data-ttu-id="08f7e-233">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="08f7e-233">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="08f7e-234">Exibir o histórico de lote e exportando resultados passado</span><span class="sxs-lookup"><span data-stu-id="08f7e-234">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="08f7e-235">Configuração rápida da Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="08f7e-235">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="08f7e-236">Campos de exportação de relatório</span><span class="sxs-lookup"><span data-stu-id="08f7e-236">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="08f7e-237">Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365</span><span class="sxs-lookup"><span data-stu-id="08f7e-237">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

