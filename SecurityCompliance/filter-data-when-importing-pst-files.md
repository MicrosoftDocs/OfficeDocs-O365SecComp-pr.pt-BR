---
title: Filtrar dados ao importar arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens que realmente obtém importados para as caixas de correio de destino. Importação inteligente permite proativamente decidir quais dados para importação e o que deixar para trás. Importação inteligente também fornece ideias sobre os dados que você está importando para o Office 365. '
ms.openlocfilehash: c90d9df62c7d8c411196b283acec37959fc95e57
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038194"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="4c576-105">Filtrar dados ao importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="4c576-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="4c576-p102">Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens em arquivos PST que realmente obtém importou para as caixas de correio de destino. Aqui está como ele funciona:</span><span class="sxs-lookup"><span data-stu-id="4c576-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="4c576-108">Depois de criar e enviar um trabalho de importação de PST, arquivos PST são carregados para uma área de armazenamento do Azure na nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c576-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="4c576-109">O Office 365 analisa os dados em arquivos PST, de forma segura e, identificando a idade dos itens de caixa de correio e os tipos de mensagem diferente incluídos nos arquivos PST.</span><span class="sxs-lookup"><span data-stu-id="4c576-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="4c576-p103">Quando a análise for concluída e os dados estão prontos para importação, você tem a opção para importar todos os dados nos arquivos PST como está ou reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados. Por exemplo, você pode optar por:</span><span class="sxs-lookup"><span data-stu-id="4c576-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="4c576-112">Importe apenas os itens de uma determinada idade.</span><span class="sxs-lookup"><span data-stu-id="4c576-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="4c576-113">Importe os tipos de mensagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="4c576-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="4c576-114">Exclua mensagens enviadas ou recebidas por pessoas específicas.</span><span class="sxs-lookup"><span data-stu-id="4c576-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="4c576-115">Depois de configurar as definições de filtro, o Office 365 importa somente os dados que satisfazem os critérios de filtragem para as caixas de correio de destino especificados no trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="4c576-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="4c576-116">O gráfico a seguir mostra o processo de importação inteligente e destaca as tarefas que você realizar e as tarefas realizadas pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c576-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![O processo de importação inteligente no Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="4c576-118">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="4c576-118">Before you begin</span></span>

- <span data-ttu-id="4c576-p104">As etapas neste tópico pressupõem que você criou um trabalho de importação de PST no serviço de importação do Office 365 usando o carregamento de rede ou o envio de unidade. Para obter instruções detalhadas, consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="4c576-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="4c576-121">Usar o carregamento de rede para importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="4c576-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="4c576-122">Usar o envio de unidade para importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="4c576-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="4c576-p105">Depois de criar um trabalho de importação usando o carregamento de rede, o status do trabalho de importação na página Importar página na segurança do Office 365 &amp; Centro de conformidade é definido como **análise em andamento**, que significa que o Office 365 é analisar os dados nos arquivos PST que você carregado. Clique em **Atualizar**![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) para atualizar o status do trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="4c576-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="4c576-125">Para o envio de trabalhos de importação de unidade, os dados serão analisados pelo Office 365 depois que o pessoal do Microsoft data center recebe seu disco rígido e carregar os arquivos PST para a área de armazenamento do Azure para sua organização.</span><span class="sxs-lookup"><span data-stu-id="4c576-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="4c576-126">Filtre os dados que obtém importou para caixas de correio</span><span class="sxs-lookup"><span data-stu-id="4c576-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="4c576-127">Depois que você criou um PST trabalho de importação, siga estas etapas para filtrar os dados antes de importá-lo para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c576-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="4c576-128">Vá para [https://protection.office.com/](https://protection.office.com/) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c576-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="4c576-129">No painel esquerdo da segurança do Office 365 &amp; Centro de conformidade, clique em **Governança dados** \> **importação**.</span><span class="sxs-lookup"><span data-stu-id="4c576-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="4c576-p106">Os trabalhos de importação para a sua organização estão listados na página **Importar** . Observe que o valor de **Análise concluída** na coluna **Status** indica os trabalhos de importação que tenham sido analisados pelo Office 365 e estiver pronto para ser importado.</span><span class="sxs-lookup"><span data-stu-id="4c576-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![Status de análise concluída indica o que Office 365 tenha analisado os dados em arquivos PST](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="4c576-133">Clique em **pronto para importar para o Office 365** para o trabalho de importação que você deseja concluir.</span><span class="sxs-lookup"><span data-stu-id="4c576-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="4c576-134">Um efeito de saída de página é exibido com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="4c576-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="4c576-135">Clique em **Importar para o Office 365**.</span><span class="sxs-lookup"><span data-stu-id="4c576-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="4c576-p107">A página de **seus dados de filtro** é exibida. Ele contém as ideias de dados sobre os dados nos arquivos PST para o trabalho de importação, incluindo informações sobre a idade dos dados.</span><span class="sxs-lookup"><span data-stu-id="4c576-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![O filtro de sua página de dados mostra as ideias de dados dos arquivos PST para o trabalho de importação](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="4c576-139">Com base em se ou não deseja reduzir os dados são importados para o Office 365, em **você deseja filtrar seus dados?**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="4c576-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="4c576-p108">a. clique em **Sim, desejo filtrá-la antes da importação** para reduzir os dados que você importar e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4c576-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="4c576-142">A página **Importar dados para a página do Office 365** é exibida com as ideias de dados detalhados da análise que executadas do Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c576-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![O Office 365 exibe as ideias de dados detalhados da sua análise dos arquivos PST](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="4c576-p109">O gráfico nesta página mostra a quantidade de dados que serão importados. Informações sobre cada tipo de mensagem encontrada nos arquivos PST são exibidas no gráfico. Você pode passar o cursor sobre cada barra para exibir informações específicas sobre esse tipo de mensagem. Há também uma lista suspensa com valores de idade diferentes com base na análise dos arquivos PST. Quando você seleciona uma idade na lista suspensa, o gráfico é atualizado para mostrar a quantidade de dados será importado para a idade selecionada.</span><span class="sxs-lookup"><span data-stu-id="4c576-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="4c576-p110">b. para configurar filtros de adição para reduzir a quantidade de dados que serão importados, clique em **mais opções de filtragem**.</span><span class="sxs-lookup"><span data-stu-id="4c576-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![Configurar os filtros na página mais opções para reduzir os dados importados](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="4c576-152">Você pode configurar esses filtros:</span><span class="sxs-lookup"><span data-stu-id="4c576-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="4c576-p111">**Idade** - selecionar uma idade, portanto, somente os itens que são mais recente do que a idade especificada será importada. Consulte a seção de [informações adicionais](filter-data-when-importing-pst-files.md#moreinfo) para obter uma descrição sobre como o Office 365 determina partições de memória de idade para o filtro de **duração** .</span><span class="sxs-lookup"><span data-stu-id="4c576-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="4c576-p112">**Tipo** - esta seção mostra todos os tipos de mensagem foram encontrados nos arquivos PST para o trabalho de importação. Você pode desmarcar uma caixa ao lado de um tipo de mensagem que você deseja excluir. Observe que você não pode excluir o tipo de mensagem. Consulte a seção de [informações adicionais](filter-data-when-importing-pst-files.md#moreinfo) para obter uma lista de itens de caixa de correio que estão incluídos na categoria outra.</span><span class="sxs-lookup"><span data-stu-id="4c576-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="4c576-p113">**Os usuários** - é possível excluir mensagens que são enviadas ou recebidas por pessoas específicas. Para excluir as pessoas que aparecem no campo From: campo para: field ou Cc: campo das mensagens, clique em **excluir usuários** ao lado desse tipo de destinatário. Digite o endereço de email (endereço SMTP) da pessoa, clique em **Adicionar**![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) adicioná-los à lista de usuários excluídos para esse tipo de destinatário, e clique em **Salvar** para salvar a lista de usuários excluídos.</span><span class="sxs-lookup"><span data-stu-id="4c576-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="4c576-p114">O Office 365 não mostra ideias de dados resultantes de configuração do filtro de **pessoas** . No entanto, se você definir esse filtro para excluir mensagens enviadas ou recebidas por pessoas específicas, essas mensagens não serão excluídas durante o processo de importação.</span><span class="sxs-lookup"><span data-stu-id="4c576-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="4c576-p115">c. clique em **Aplicar** no dinamicamente **Opções de filtragem mais** check-out de página para salvar suas configurações de filtro.</span><span class="sxs-lookup"><span data-stu-id="4c576-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="4c576-p116">Os dados ideias sobre na página **Importar dados para o Office 365** é atualizadas com base em suas configurações de filtro, incluindo a quantidade total de dados que serão importados com base nas configurações de filtro. Observe que um resumo das configurações de filtro também é mostrado. Você pode clicar em **Editar** ao lado de um filtro para alterar a configuração, se necessário.</span><span class="sxs-lookup"><span data-stu-id="4c576-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![As ideias de dados são atualizadas com base em suas configurações de filtro](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="4c576-p117">d. clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4c576-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="4c576-p118">Uma página de status é exibida mostrando as configurações de filtro. Novamente, você pode editar as configurações de filtro.</span><span class="sxs-lookup"><span data-stu-id="4c576-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="4c576-p119">e. clique em **Importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida.</span><span class="sxs-lookup"><span data-stu-id="4c576-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="4c576-177">Ou</span><span class="sxs-lookup"><span data-stu-id="4c576-177">Or</span></span>
    
    <span data-ttu-id="4c576-p120">a. clique em **não, eu quiser importar tudo** para importar todos os dados nos arquivos PST para o Office 365 e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4c576-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="4c576-p121">b. na página **Importar dados para o Office 365** , clique em **Importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida.</span><span class="sxs-lookup"><span data-stu-id="4c576-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="4c576-p122">Na página **Importar** , clique em **Atualizar** ![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). O status do trabalho de importação é exibido na coluna **Status** .</span><span class="sxs-lookup"><span data-stu-id="4c576-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="4c576-185">Clique no trabalho para exibir informações mais detalhadas, como o status de cada arquivo PST e as configurações de filtro que você configurou à importação.</span><span class="sxs-lookup"><span data-stu-id="4c576-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="4c576-186">Mais informações</span><span class="sxs-lookup"><span data-stu-id="4c576-186">More information</span></span>

- <span data-ttu-id="4c576-p123">Como o Office 365 determinar os incrementos para o filtro de idade? Quando o Office 365 analisa um arquivo PST, ele analisa o carimbo de hora de enviados ou recebidos de cada item (se um item tiver uma timestamp enviado e recebido, a data mais antiga estiver selecionado). Em seguida, o Office 365 examina o valor de ano para esse carimbo de hora e compara com a data atual para determinar a idade do item. Esses anos, em seguida, são usados como os valores na lista suspensa para o filtro de **duração** . Por exemplo, se um arquivo PST tem mensagens de 2015, 2016 e de 2014, valores do filtro de **idade** seria **ano 1**, **2 anos**e **3 anos**.</span><span class="sxs-lookup"><span data-stu-id="4c576-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="4c576-p124">A tabela a seguir lista os tipos de mensagem que estão incluídos na **categoria no filtro **tipo** dinamicamente **mais opções** check-out da página** (consulte a Etapa 5b no procedimento anterior). No momento, você não pode excluir itens na categoria "Outras" quando você importa PSTs para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c576-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="4c576-194">**ID de classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="4c576-194">**Message class ID**</span></span>|<span data-ttu-id="4c576-195">**Itens de caixa de correio que usam essa classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="4c576-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="4c576-196">IPM. Atividade</span><span class="sxs-lookup"><span data-stu-id="4c576-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="4c576-197">Entradas de diário</span><span class="sxs-lookup"><span data-stu-id="4c576-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="4c576-198">IPM. Documento</span><span class="sxs-lookup"><span data-stu-id="4c576-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="4c576-199">Documentos e arquivos (não anexados a uma mensagem de email)</span><span class="sxs-lookup"><span data-stu-id="4c576-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="4c576-200">IPM. Arquivo</span><span class="sxs-lookup"><span data-stu-id="4c576-200">IPM.File</span></span>  <br/> |<span data-ttu-id="4c576-201">(o mesmo que IPM. Documento)</span><span class="sxs-lookup"><span data-stu-id="4c576-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="4c576-202">IPM. Note.IMC.Notification</span><span class="sxs-lookup"><span data-stu-id="4c576-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="4c576-203">Relatórios enviados por Internet Mail Connect, que é o gateway do Exchange Server para a Internet</span><span class="sxs-lookup"><span data-stu-id="4c576-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="4c576-204">IPM. Note.Microsoft.Fax</span><span class="sxs-lookup"><span data-stu-id="4c576-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="4c576-205">Mensagens de fax</span><span class="sxs-lookup"><span data-stu-id="4c576-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="4c576-206">IPM. Note.Rules.Oof.Template.Microsoft</span><span class="sxs-lookup"><span data-stu-id="4c576-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="4c576-207">Mensagens de resposta automática de ausência temporária</span><span class="sxs-lookup"><span data-stu-id="4c576-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="4c576-208">IPM. Note.Rules.ReplyTemplate.Microsoft</span><span class="sxs-lookup"><span data-stu-id="4c576-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="4c576-209">Respostas enviadas por uma regra de caixa de entrada</span><span class="sxs-lookup"><span data-stu-id="4c576-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="4c576-210">IPM. OLE. Classe</span><span class="sxs-lookup"><span data-stu-id="4c576-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="4c576-211">Exceções para uma série recorrente</span><span class="sxs-lookup"><span data-stu-id="4c576-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="4c576-212">IPM. Recall.Report</span><span class="sxs-lookup"><span data-stu-id="4c576-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="4c576-213">Relatórios de cancelamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="4c576-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="4c576-214">IPM. Remoto</span><span class="sxs-lookup"><span data-stu-id="4c576-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="4c576-215">Mensagens de email remoto</span><span class="sxs-lookup"><span data-stu-id="4c576-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="4c576-216">IPM. Relatório</span><span class="sxs-lookup"><span data-stu-id="4c576-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="4c576-217">Relatórios de status do item</span><span class="sxs-lookup"><span data-stu-id="4c576-217">Item status reports</span></span>  <br/> |
