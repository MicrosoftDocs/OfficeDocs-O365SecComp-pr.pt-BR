---
title: Usar análises expressas na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Saiba como executar o modo de análise Express de eDiscovery avançadas do Office 365
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523919"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="cd36f-103">Usar análises expressas na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="cd36f-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="cd36f-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="cd36f-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="cd36f-106">Você pode usar o **Express análise** para analisar rapidamente um caso e exportar os resultados.</span><span class="sxs-lookup"><span data-stu-id="cd36f-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="cd36f-p102">Você pode usar a análise express para calcular perto duplicatas e segmentos de email e calcular temas. Você também pode definir determinados parâmetros para temas, semelhança do documento e os arquivos de exportação nas [Configurações avançadas para análise Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span><span class="sxs-lookup"><span data-stu-id="cd36f-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="cd36f-109">Executar a análise de Express</span><span class="sxs-lookup"><span data-stu-id="cd36f-109">Run Express analysis</span></span>

1. <span data-ttu-id="cd36f-110">Na guia **analysis Express** (1), selecione um contêiner para habilitar o * * Express analysis * * (2) e os botões de **Configurações avançadas** .</span><span class="sxs-lookup"><span data-stu-id="cd36f-110">In the **Express analysis** (1) tab, select a container to enable the ** Express analysis ** (2), and **Advanced settings** buttons.</span></span> 
    
    ![Captura de tela da página análise Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="cd36f-112">Em **Analisar parâmetros**:</span><span class="sxs-lookup"><span data-stu-id="cd36f-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="cd36f-p103">Verifique **Calcular perto duplicatas e segmentos de email** se você deseja executar a análise. Ele é selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="cd36f-p104">Verifique se **Calcular temas** para processar todos os arquivos e atribua temas de. Ele é selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="cd36f-117">Em **Exportar destino**:</span><span class="sxs-lookup"><span data-stu-id="cd36f-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="cd36f-118">Verifique a **baixar para a máquina local** para baixar para seu computador local.</span><span class="sxs-lookup"><span data-stu-id="cd36f-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="cd36f-119">Se você marcar **Exportar para blob Azure definidas pelo usuário** , em seguida, você também pode especificar um token de URL e SAS do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cd36f-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="cd36f-p105">Depois que um pacote de exportação é armazenado para o usuário definido Azure blob, os dados não mais são gerenciados por eDiscovery avançado. ele é gerenciado pelo Azure blob. Isso significa que se você excluir o caso, os arquivos exportados ainda vai permanecer no Azure blob.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="cd36f-123">**Salvar SAS token para sessão de exportação futuras**: se estiver marcado, o token SAS será criptografado no banco de dados interno para uso futuro da descoberta eletrônica avançado.</span><span class="sxs-lookup"><span data-stu-id="cd36f-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cd36f-p106">Atualmente, o token SAS expira após um mês. Se você tentar baixar após mais de um mês em que você precise desfazer última sessão, exporte novamente.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="cd36f-126">Para iniciar a análise express com padrão configurações, escolha **Express análise**e exibirá a página **status da tarefa**</span><span class="sxs-lookup"><span data-stu-id="cd36f-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="cd36f-127">Na página **status da tarefa** , você pode expandir as guias de **processo**, **Analisar** e **Exportar** para exibir os detalhes sobre a execução express.</span><span class="sxs-lookup"><span data-stu-id="cd36f-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Captura de tela de avançadas página status de tarefa de análise do eDiscovery Express](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="cd36f-129">Escolha a página de **Resumo de análise de Express** para listar as informações detalhadas sobre a execução.</span><span class="sxs-lookup"><span data-stu-id="cd36f-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="cd36f-p107">Na parte inferior da página de **Resumo de análise de Express** , escolha a **última sessão de Download** para baixar a análise arquivos PA seu computador local. Primeiro, você terá que baixar a ferramenta de exportação de descoberta eletrônica e cole a chave de exportação para a ferramenta de exportação de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="cd36f-132">Configurações avançadas para análise Express</span><span class="sxs-lookup"><span data-stu-id="cd36f-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="cd36f-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="cd36f-133"></span></span>

<span data-ttu-id="cd36f-134">Opcionalmente, você pode definir **Configurações avançadas** para alterar os parâmetros de análise Express padrão.</span><span class="sxs-lookup"><span data-stu-id="cd36f-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="cd36f-135">Na seção **Analisar** :</span><span class="sxs-lookup"><span data-stu-id="cd36f-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="cd36f-136">Na **quase duplicatas e segmentos de email**, insira o valor de **semelhança do documento** ou aceite o padrão de 65%.</span><span class="sxs-lookup"><span data-stu-id="cd36f-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="cd36f-p108">O **número máximo de temas** Insira ou selecione um valor para o número de temas para criar. O padrão é 200.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="cd36f-p109">Aumento do número de temas afeta o desempenho, bem como a capacidade de um tema para generalizar. Quanto maior o número de temas, mais granular são. Por exemplo, se um conjunto de 50 temas incluir um tema, como "Basquete, rumo, Cortador de Lakers"; 300 temas podem incluir separados temas: "Estimula os", "Cortador de", "Lakers". Se você tivesse sem reconhecimento do tema "Basquete" e usa esse recurso para ECA, vendo o tema "Basquete" poderia ser útil. Mas, se o processamento teve muitos temas, você nunca pode ver a palavra "Basquete" e talvez não saiba que rumo e cortador é boa temas basquete revisar, em vez de itens que vá é inicializado e usado para cabelo.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="cd36f-p110">Nos **temas sugeridos** escolha **Modificar** para sugerir palavras de tema para controlar o processamento de temas. EDiscovery avançado será enfocam essas palavras sugeridas e tente criar um ou mais temas relevantes, com base nas configurações de "Número de temas do Max".</span><span class="sxs-lookup"><span data-stu-id="cd36f-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="cd36f-p111">Por exemplo, se a palavra sugerida é "computer", e você especificou "2" como o "número máximo de temas", o eDiscovery avançado tentará gere dois temas que se relacionam com a palavra "computador". Os dois temas poderiam ser "software de computador" e "hardware de computador", por exemplo.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![Adicionar tema sugerido](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="cd36f-149">**Modo** Na lista suspensa, selecione uma opção de **temas** :</span><span class="sxs-lookup"><span data-stu-id="cd36f-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="cd36f-150">**Criar e aplicar modelo**: calcula temas por modelos a partir de um segmento dos arquivos e distribui arquivos entre eles.</span><span class="sxs-lookup"><span data-stu-id="cd36f-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="cd36f-p112">**Criar modelo**: calcula um modelo de temas de um segmento dos arquivos. O processo de aplicar de divisão de arquivos é feito separadamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="cd36f-p113">**Aplicar modelo**: essa opção é mostrada somente se um modelo foi criado anteriormente e ainda não foi aplicado. Isso dividirá os arquivos com base nos temas.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="cd36f-155">Na seção **Exportar** :</span><span class="sxs-lookup"><span data-stu-id="cd36f-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="cd36f-156">No **lote de exportação selecione**:</span><span class="sxs-lookup"><span data-stu-id="cd36f-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="cd36f-157">Na lista **Exportar lote** , selecione o nome do lote ou exportar resultados para o lote de exportação 01, (o lote padrão).</span><span class="sxs-lookup"><span data-stu-id="cd36f-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="cd36f-p114">Para exportar os resultados para novos arquivos adicionados a um caso existente, continue com o lote atual. Para criar uma sessão no lote, selecione o mesmo número de lote e clique em **criar exportar sessão** , você pode usar essa opção para exportar os mesmos parâmetros como o lote anterior, de forma incremental.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="cd36f-p115">Para exportar para um novo lote, clique em **Adicionar**![Adicionar ícone](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) e insira um novo nome em **nome de lote** (ou aceite o padrão) e uma descrição na **Descrição do lote**. Clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="cd36f-162">Para editar um nome de lote ou descrição, selecione o nome na **exportação em lote**, clique em **Editar** ![ícone Editar](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)e, em seguida, modifique os campos.</span><span class="sxs-lookup"><span data-stu-id="cd36f-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cd36f-p116">Depois de executar sessões de um lote de exportação, eles não podem ser excluídos. Além disso, apenas alguns parâmetros podem ser editados depois que a primeira sessão é executada.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="cd36f-165">Para criar um lote de exportação duplicados, escolha o **lote de exportação de duplicata**![criar um ícone de lote de exportação duplicados](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) e insira um nome e uma descrição para o lote duplicado no painel.</span><span class="sxs-lookup"><span data-stu-id="cd36f-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="cd36f-166">Para excluir um lote de exportação, escolha **Excluir**![excluir um ícone de lote de exportação](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="cd36f-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="cd36f-167">Para exibir o histórico de um lote, escolha o **histórico de lote**![ícone de histórico de exibição](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="cd36f-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="cd36f-p117">Em definir p **opulation:** selecione **incluir somente os arquivos acima pontuação de interrupção de relevância** e/ou **refinar lote de exportação** , se quiser ajustar as configurações para o lote de exportação. Se você selecionar a opção **incluir somente os arquivos acima pontuação de interrupção de relevância**, o **problema** é habilitada e se a pontuação de relevância do arquivo for superior a pontuação de interrupção para o problema selecionado, o arquivo será exportado. O arquivo será exportado, a menos que ele for excluído pelo ' filtro **para revisão** . Se você selecionar **refinar exportação lote**, em seguida, a **eliminação da duplicação** e **Filter by 'Para revisão' campo** botões de opção estão habilitados. Se você escolher **eliminação da duplicação**, e depois duplicatas arquivos vai ser filtrada-out acordo com a política definida: [caso nível (padrão): a partir de cada conjunto de arquivos duplicados no caso de inteiro, apenas um arquivo será sua duplicação eliminado. Nível dos responsáveis: de cada conjunto de arquivos duplicados do dos responsáveis mesmo, apenas um arquivo será sua duplicação eliminado. Um registro de todos os arquivos duplicados está disponível na saída de exportação. Se você escolher campo **Filter by 'para revisão'** , selecione **Modificar em metadados** para inserir suas configurações de campo **'para revisão'**. Selecione **os arquivos de entrada incluir**para incluir os arquivos de origem no conteúdo do pacote. Você pode desmarcar essa opção para acelerar o processo de exportação. Observe que os arquivos nativos serão exportados em qualquer caso.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="cd36f-179">Em **definir metadados**, selecione entre as seguintes opções na lista **Exportar modelo** (uma vez por sessão).</span><span class="sxs-lookup"><span data-stu-id="cd36f-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="cd36f-p118">**Padrão**: conjunto básico de propriedades, metadados e itens de dados. Use esta opção quando importar dados já foi processados no eDiscovery avançado e exportar dados são carregados com um sistema que já contém os arquivos. Por padrão, exporte modelo colunas são criadas e preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="cd36f-p119">**Todos**: o conjunto completo de metadados padrão, incluindo todos os dados de processamento, bem como as pontuações de analisar e a relevância. Este modelo é necessário quando eDiscovery avançado realiza o processamento e dados de arquivo são carregados no sistema externo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="cd36f-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="cd36f-185">**Problemas**: selecione **Todos os problemas** ou selecione um problema específico que você criou.</span><span class="sxs-lookup"><span data-stu-id="cd36f-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="cd36f-186">Escolha **Okey**para salvar as configurações avançadas, **Restaurar padrões** para usar valores padrão ou em **Cancelar** para cancelar a definição de configurações avançadas.</span><span class="sxs-lookup"><span data-stu-id="cd36f-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd36f-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd36f-187">See also</span></span>
<span data-ttu-id="cd36f-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="cd36f-188"></span></span>

[<span data-ttu-id="cd36f-189">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="cd36f-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

