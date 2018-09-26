---
title: Preparar um arquivo CSV para uma lista de IDs de pesquisa de conteúdo no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Use o arquivo de Results.csv ou Items.csv não indexadas a partir de uma pesquisa de conteúdo existente para criar uma pesquisa de lista de identificação que retorna um mensagens de email específicos. Pesquisas de lista de ID geralmente são usadas para devolver os itens de caixa de correio parcialmente indexados.
ms.openlocfilehash: 9a7583c8f83626afb8dc0452bf72d834c8a28275
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038274"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="fdcc8-104">Preparar um arquivo CSV para uma lista de IDs de pesquisa de conteúdo no Office 365</span><span class="sxs-lookup"><span data-stu-id="fdcc8-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="fdcc8-p102">Você pode pesquisar mensagens de email da caixa de correio específica e outros itens de caixa de correio usando uma lista de IDs do Exchange. Para criar uma pesquisa de ID de lista (formalmente chamada de uma pesquisa de destino), você enviar um arquivo (CSV) de valores separados por vírgula que identifica os itens de caixa de correio específica a ser pesquisado. O arquivo CSV você pode usar o arquivo de **Results.csv** ou o arquivo **Não indexadas Items.csv** que estão incluídos ao exportar os resultados de pesquisa de conteúdo ou exportar um relatório de pesquisa de conteúdo de e a pesquisa de conteúdo existente. Em seguida, você editar um desses arquivos para indicar os itens específicos para pesquisa e, em seguida, criar uma nova pesquisa de lista de ID e enviar o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="fdcc8-109">Eis uma rápida visão geral do processo de criação de uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="fdcc8-110">Criar e executar uma pesquisa de conteúdo novo ou guiada na segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="fdcc8-p103">Exportar os resultados de pesquisa de conteúdo ou exportar o relatório de pesquisa de conteúdo. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="fdcc8-113">Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="fdcc8-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="fdcc8-114">Exportar um relatório da Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="fdcc8-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="fdcc8-p104">Editar o arquivo **Results.csv** ou o **Items.csv não indexadas** e identificar os itens de caixa de correio específica que você deseja incluir na lista pesquisa ID. Consulte as [instruções](#prepare-the-csv-file-for-an-id-list-search) para preparar um arquivo CSV para uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="fdcc8-p105">Criar uma nova lista de ID Pesquisar (veja as [instruções](#create-an-id-list-search)) e enviar o arquivo CSV que você preparou. A consulta de pesquisa que é criada pesquisará apenas para os itens selecionados no arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fdcc8-p106">Pesquisas de lista de ID são permitidas apenas aos itens de caixa de correio. Não é possível pesquisar para SharePoint e pesquisa de lista de documentos do OneDrive em uma ID.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="fdcc8-p107">**Por que criar uma pesquisa de lista de ID?** Se você for capaz de determinar que se um item estiver respondendo a uma solicitação de descoberta eletrônica baseada nos metadados nos arquivos de **Results.csv** ou **Items.csv não indexados** , você pode usar uma pesquisa de ID de lista para localizar, visualize e exporte esse item para determinar se ele tiver sido definido respondendo ao caso de forma que você está investigando. Pesquisas de lista de ID são geralmente usadas para pesquisar e retornar um conjunto específico de itens indexados.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="fdcc8-124">Preparar o arquivo CSV para uma pesquisa de ID de lista</span><span class="sxs-lookup"><span data-stu-id="fdcc8-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="fdcc8-p108">Após exportar os resultados de pesquisa ou o relatório para uma pesquisa de conteúdo, você pode executar as seguintes etapas para preparar o arquivo CSV para uma pesquisa de ID de lista. Este arquivo CSV identificará cada item na pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="fdcc8-p109">Observe que você pode usar um arquivo CSV de uma pesquisa que incluía contas do OneDrive e sites do SharePoint, mas você pode selecionar *apenas* os itens de caixa de correio para uma pesquisa de ID de lista. Se você selecionar um documento no SharePoint ou OneDrive, o arquivo CSV falhará validação quando você criar uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="fdcc8-129">Abra o arquivo **Results.csv** ou **Items.csv não indexados** no Excel.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="fdcc8-p110">Inserir uma nova coluna e nomeie-o **selecionados**. Não importa onde inserir a coluna. Para sua conveniência, considere a possibilidade de inseri-lo à esquerda da primeira coluna.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="fdcc8-p111">Na coluna **selecionado** , digite **Sim** na célula que corresponde ao item que você deseja pesquisar. Repita essa etapa para cada item que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="fdcc8-p112">Quando você abre o arquivo CSV no Excel, o formato de dados para a coluna de **ID de documento** é alterado para **Geral**. Isso resulta na exibição a ID de documento para um item no científico notação. Por exemplo, o documento que ID de "481037338205" é exibido como "4.81037E + 11" você precisará executar as próximas etapas para alterar o formato dos dados da coluna de **ID de documento** para o **número** para restaurar o formato correto para a ID do documento. Se você não fizer isso, haverá falha na pesquisa de lista de identificação que usa o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="fdcc8-139">Clique com o botão toda a coluna de **ID de documento** e selecione **Formatar células**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="fdcc8-140">Na caixa **categoria** , clique em **número**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="fdcc8-p113">Alterar o número de casas decimais como **0**e clique em **Okey** para salvar suas alterações. Observe que os valores na coluna ID do documento são alterados para números.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="fdcc8-143">Aqui está um exemplo da um arquivo CSV que está pronto para ser enviada para uma pesquisa de conteúdo de lista de ID.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Exemplo de um arquivo CSV para uma pesquisa de conteúdo direcionado](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="fdcc8-p114">Salve o arquivo CSV ou usar **Salvar como** para salvar o arquivo com o nome de arquivo diferente. Em ambos os casos, certifique-se de salvar o arquivo com o formato CSV.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="fdcc8-147">Criar uma pesquisa de ID de lista</span><span class="sxs-lookup"><span data-stu-id="fdcc8-147">Create an ID list search</span></span>

<span data-ttu-id="fdcc8-148">A próxima etapa é criar uma nova pesquisa de conteúdo de lista ID e enviar o arquivo CSV que você preparou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fdcc8-p115">Você deve criar uma pesquisa de lista ID não mais de 2 dias após exportar os resultados ou o relatório de uma pesquisa de conteúdo. Se a pesquisa de resultados ou relatar onde exportados há mais de 2 dias, você deve exportar novamente os resultados de pesquisa ou relatório para gerar os arquivos CSV atualizados. Então, você pode preparar um dos arquivos CSV atualizados e usá-lo para criar uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="fdcc8-152">Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="fdcc8-153">Na página de **pesquisa** , clique na seta ao lado de ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nova pesquisa**e clique em **Pesquisar por ID de lista**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Clique em Pesquisar por ID de lista, na lista suspensa de pesquisa novo](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="fdcc8-155">No submenu **Pesquisar por lista ID** , nomeie a pesquisa (e, opcionalmente, descreva-) e, em seguida, clique em **Procurar** e selecione o arquivo CSV que você preparou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="fdcc8-p116">O Office 365 tenta validar o arquivo CSV. Se a validação falhar, será exibida uma mensagem de erro que podem ajudá-lo a solucionar problemas de erros de validação. O arquivo CSV deve ser validado com êxito para criar uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="fdcc8-159">Após o CSV arquivo é validado com êxito, clique em **pesquisa** para criar a pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="fdcc8-160">Aqui está um exemplo de como os resultados de pesquisa estimados e a consulta que é gerada para uma pesquisa de ID de lista.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Consulta de pesquisa para uma pesquisa de conteúdo direcionada no painel de detalhes](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="fdcc8-162">Observe que o número de itens estimados exibido em estatísticas para a pesquisa de ID deve corresponder o número de itens que você selecionou no arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="fdcc8-163">Visualizar ou exportar os itens retornados pela pesquisa lista ID.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fdcc8-p117">Se você mover uma caixa de correio depois de criar uma pesquisa de ID de lista, a consulta para a pesquisa não devolvem os itens especificados. Isso ocorre porque a propriedade **DocumentId** para itens de caixa de correio são alteradas quando uma caixa de correio forem movida. Na instância rara quando uma caixa de correio é movida depois de criar uma pesquisa de ID de lista, você deve criar uma nova pesquisa de conteúdo (ou atualizar os resultados de pesquisa para a pesquisa de conteúdo existente) e, em seguida, exportar a pesquisa resulta ou relatar para gerar os arquivos CSV atualizados que podem ser usados  para criar uma nova pesquisa de lista de ID.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
