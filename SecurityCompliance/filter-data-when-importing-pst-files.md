---
title: Filtrar dados ao importar arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens que realmente são importados para as caixas de correio de destino. A importação inteligente permite que você decida de forma proativa quais dados importar e o que deixar atrás. A importação inteligente também fornece informações sobre os dados que você está importando para o Office 365. '
ms.openlocfilehash: 49399f11a71069059ffae2d03482ac7ffe03daf0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219811"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="da243-105">Filtrar dados ao importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="da243-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="da243-p102">Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens em arquivos PST que realmente são importados para as caixas de correio de destino. Veja como funciona:</span><span class="sxs-lookup"><span data-stu-id="da243-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="da243-108">Depois de criar e enviar um trabalho de importação de PST, os arquivos PST são carregados para uma área de armazenamento do Azure na nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="da243-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="da243-109">O Office 365 analisa os dados nos arquivos PST, de forma segura e segura, identificando a idade dos itens da caixa de correio e os diferentes tipos de mensagens incluídos nos arquivos PST.</span><span class="sxs-lookup"><span data-stu-id="da243-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="da243-p103">Quando a análise é concluída e os dados estão prontos para importação, você tem a opção de importar todos os dados nos arquivos PST como estão ou aparar os dados que são importados por meio da definição de filtros que controlam quais dados são importados. Por exemplo, você pode optar por:</span><span class="sxs-lookup"><span data-stu-id="da243-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="da243-112">Importe somente os itens de uma determinada idade.</span><span class="sxs-lookup"><span data-stu-id="da243-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="da243-113">Importar tipos de mensagem selecionados.</span><span class="sxs-lookup"><span data-stu-id="da243-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="da243-114">Excluir mensagens enviadas ou recebidas por pessoas específicas.</span><span class="sxs-lookup"><span data-stu-id="da243-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="da243-115">Após definir as configurações de filtro, o Office 365 importa somente os dados que atendem aos critérios de filtragem para as caixas de correio de destino especificadas no trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="da243-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="da243-116">O gráfico a seguir mostra o processo de importação inteligente e realça as tarefas executadas e as tarefas realizadas pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="da243-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![O processo de importação inteligente no Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="da243-118">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="da243-118">Before you begin</span></span>

- <span data-ttu-id="da243-p104">As etapas neste tópico pressupõem que você tenha criado um trabalho de importação de PST no serviço de importação do Office 365 usando o carregamento de rede ou o envio de unidades. Para obter instruções detalhadas, consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="da243-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="da243-121">Usar o carregamento de rede para importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="da243-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="da243-122">Usar o envio de unidade para importar arquivos PST para o Office 365</span><span class="sxs-lookup"><span data-stu-id="da243-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="da243-p105">Após criar um trabalho de importação usando o carregamento de rede, o status do trabalho de importação na página de importação no Office 365 &amp; Security Compliance Center é definido como **análise em andamento**, o que significa que o Office 365 está analisando os dados nos arquivos pst que você submeti. Clique \*\*\*\*![em atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) atualização para atualizar o status do trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="da243-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="da243-125">Para trabalhos de importação de fornecimento de unidades, os dados serão analisados pelo Office 365 após a equipe de data center da Microsoft receber seu disco rígido e carregar os arquivos PST para a área de armazenamento do Azure para sua organização.</span><span class="sxs-lookup"><span data-stu-id="da243-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="da243-126">Filtrar dados que são importados para caixas de correio</span><span class="sxs-lookup"><span data-stu-id="da243-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="da243-127">Depois de criar um trabalho de importação de PST, siga estas etapas para filtrar os dados antes de importá-los para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="da243-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="da243-128">AcEsse [https://protection.office.com/](https://protection.office.com/) e entre usando as credenciais de uma conta de administrador na sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="da243-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="da243-129">no painel esquerdo do centro de conformidade de segurança &amp; do Office 365, clique em **importação**de **governança** \> de dados.</span><span class="sxs-lookup"><span data-stu-id="da243-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="da243-p106">Os trabalhos de importação de sua organização estão listados na página **importar** . Observe que o valor de **análise concluída** na coluna **status** indica os trabalhos de importação que foram analisados pelo Office 365 e que estão prontos para importação.</span><span class="sxs-lookup"><span data-stu-id="da243-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![O status de conclusão da análise indica que o Office 365 analisou os dados nos arquivos PST](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="da243-133">Clique em **pronto para importar para o Office 365** para o trabalho de importação que você deseja concluir.</span><span class="sxs-lookup"><span data-stu-id="da243-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="da243-134">Uma página de sobrevôo é exibida com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="da243-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="da243-135">Clique em **importar para o Office 365**.</span><span class="sxs-lookup"><span data-stu-id="da243-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="da243-p107">O **filtro em que sua página de dados** é exibida. Ele contém insights de dados sobre os dados nos arquivos PST para o trabalho de importação, incluindo informações sobre a idade dos dados.</span><span class="sxs-lookup"><span data-stu-id="da243-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![A página Filtrar seus dados mostra as informações de dados dos arquivos PST para o trabalho de importação](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="da243-139">Dependendo se você deseja ou não aparar os dados que são importados para o Office 365, em deseja **Filtrar seus dados?**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="da243-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="da243-p108">a. clique em **Sim, quero filtrá-lo antes de importar** para aparar os dados que você importou e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="da243-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="da243-142">A página **importar dados para o office 365** é exibida com as informações detalhadas sobre os dados da análise que o Office 365 executou.</span><span class="sxs-lookup"><span data-stu-id="da243-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![O Office 365 exibe informações detalhadas sobre os dados de análise dos arquivos PST](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="da243-p109">O gráfico nesta página mostra a quantidade de dados que serão importados. As informações sobre cada tipo de mensagem encontrada nos arquivos PST são exibidas no gráfico. Você pode passar o cursor sobre cada barra para exibir informações específicas sobre esse tipo de mensagem. Há também uma lista suspensa com valores de idade diferentes com base na análise dos arquivos PST. Quando você seleciona uma idade na lista suspensa, o gráfico é atualizado para mostrar a quantidade de dados que será importada para a idade selecionada.</span><span class="sxs-lookup"><span data-stu-id="da243-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="da243-p110">b. para configurar filtros de adição para reduzir a quantidade de dados importados, clique em **mais opções de filtragem**.</span><span class="sxs-lookup"><span data-stu-id="da243-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![Configure os filtros na página mais opções para aparar os dados que são importados](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="da243-152">Você pode configurar esses filtros:</span><span class="sxs-lookup"><span data-stu-id="da243-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="da243-p111">**Idade** -selecione uma idade para que apenas os itens mais recentes do que a idade especificada serão importados. Consulte a seção [mais informações](filter-data-when-importing-pst-files.md#moreinfo) para obter uma descrição sobre como o Office 365 determina os buckets de idade para o filtro de **idade** .</span><span class="sxs-lookup"><span data-stu-id="da243-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="da243-p112">**Tipo** -esta seção mostra todos os tipos de mensagem que foram encontrados nos arquivos pst para o trabalho de importação. Você pode desmarcar uma caixa ao lado de um tipo de mensagem que você deseja excluir. Observe que não é possível excluir o outro tipo de mensagem. Consulte a seção [mais informações](filter-data-when-importing-pst-files.md#moreinfo) para obter uma lista de itens de caixa de correio que estão incluídos na outra categoria.</span><span class="sxs-lookup"><span data-stu-id="da243-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="da243-p113">**Usuários** – é possível excluir mensagens enviadas ou recebidas por pessoas específicas. Para excluir pessoas que aparecem no campo de:, para: ou no campo CC: de mensagens, clique em **excluir usuários** ao lado desse tipo de destinatário. Digite o endereço de email (endereço SMTP) da pessoa, clique em **Adicionar**![novo](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ícone para adicioná-los à lista de usuários excluídos para esse tipo de destinatário e clique em **salvar** para salvar a lista de usuários excluídos.</span><span class="sxs-lookup"><span data-stu-id="da243-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="da243-p114">O Office 365 não mostra informações de dados que resultam da configuração do filtro de **pessoas** . No enTanto, se você definir esse filtro para excluir mensagens enviadas ou recebidas por pessoas específicas, essas mensagens serão excluídas durante o processo de importação real.</span><span class="sxs-lookup"><span data-stu-id="da243-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="da243-p115">c. clique em **aplicar** na página **mais opções de filtragem** sair para salvar as configurações de filtro.</span><span class="sxs-lookup"><span data-stu-id="da243-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="da243-p116">As informações sobre os dados da página **importar dados para o Office 365** são atualizadas com base nas configurações de filtro, incluindo a quantidade total de dados que serão importados com base nas configurações de filtro. Observe que um resumo das configurações de filtro também é mostrado. Você pode clicar em **Editar** ao lado de um filtro para alterar a configuração, se necessário.</span><span class="sxs-lookup"><span data-stu-id="da243-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![As insights de dados são atualizadas com base nas configurações de filtro](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="da243-p117">d. clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="da243-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="da243-p118">Uma página de status é exibida mostrando suas configurações de filtro. Novamente, você pode editar qualquer uma das configurações de filtro.</span><span class="sxs-lookup"><span data-stu-id="da243-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="da243-p119">e. clique em **importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida.</span><span class="sxs-lookup"><span data-stu-id="da243-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="da243-177">Ou</span><span class="sxs-lookup"><span data-stu-id="da243-177">Or</span></span>
    
    <span data-ttu-id="da243-p120">a. clique em **não, desejo importar tudo** para importar todos os dados dos arquivos pst para o Office 365 e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="da243-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="da243-p121">b. na página **importar dados para o Office 365** , clique em **importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida.</span><span class="sxs-lookup"><span data-stu-id="da243-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="da243-p122">Na página **importar** , clique em **Atualizar** ![atualização](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). O status do trabalho de importação é exibido na coluna **status** .</span><span class="sxs-lookup"><span data-stu-id="da243-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="da243-185">Clique em importar o trabalho para exibir informações mais detalhadas, como o status de cada arquivo PST e as configurações de filtro que você configurou.</span><span class="sxs-lookup"><span data-stu-id="da243-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="da243-186">Mais informações</span><span class="sxs-lookup"><span data-stu-id="da243-186">More information</span></span>

- <span data-ttu-id="da243-p123">Como o Office 365 determina os incrementos para o filtro de idade? Quando o Office 365 analisa um arquivo PST, ele analisa o carimbo de data/hora enviado ou recebido de cada item (se um item tiver um carimbo de data/hora enviado e recebido, a data mais antiga é selecionada). Em seguida, o Office 365 examina o valor de ano desse carimbo de data/hora e o compara à data atual para determinar a idade do item. Essas idades são usadas como os valores na lista suspensa para o filtro de **idade** . Por exemplo, se um arquivo PST tiver mensagens de 2016, 2015 e 2014, os valores no filtro de **idade** serão **1 ano**, **2 anos**e **3 anos**.</span><span class="sxs-lookup"><span data-stu-id="da243-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="da243-p124">A tabela a seguir lista os tipos de mensagens que estão incluídos na **outra** categoria do filtro de **tipo** na página **mais opções** de saída (consulte a etapa 5b no procedimento anterior). No momento, não é possível excluir itens na categoria "outros" quando você importa PSTs para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="da243-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="da243-194">**ID da classe da mensagem**</span><span class="sxs-lookup"><span data-stu-id="da243-194">**Message class ID**</span></span>|<span data-ttu-id="da243-195">**Itens de caixa de correio que usam esta classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="da243-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="da243-196">IPM. Atividade</span><span class="sxs-lookup"><span data-stu-id="da243-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="da243-197">Entradas de diário</span><span class="sxs-lookup"><span data-stu-id="da243-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="da243-198">IPM. Documento</span><span class="sxs-lookup"><span data-stu-id="da243-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="da243-199">Documentos e arquivos (não anexados a uma mensagem de email)</span><span class="sxs-lookup"><span data-stu-id="da243-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="da243-200">IPM. Arquivo</span><span class="sxs-lookup"><span data-stu-id="da243-200">IPM.File</span></span>  <br/> |<span data-ttu-id="da243-201">(igual a IPM. Documento</span><span class="sxs-lookup"><span data-stu-id="da243-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="da243-202">IPM. Nota. IMC. Notification</span><span class="sxs-lookup"><span data-stu-id="da243-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="da243-203">Relatórios enviados pelo Internet mail Connect, que é o gateway do Exchange Server para a Internet</span><span class="sxs-lookup"><span data-stu-id="da243-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="da243-204">IPM. Observação. Microsoft. fax</span><span class="sxs-lookup"><span data-stu-id="da243-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="da243-205">Mensagens de fax</span><span class="sxs-lookup"><span data-stu-id="da243-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="da243-206">IPM. Note. Rules. OOF. Template. Microsoft</span><span class="sxs-lookup"><span data-stu-id="da243-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="da243-207">Mensagens de resposta automática de ausência temporária</span><span class="sxs-lookup"><span data-stu-id="da243-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="da243-208">IPM. Note. Rules. Replytemplate. Microsoft</span><span class="sxs-lookup"><span data-stu-id="da243-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="da243-209">Respostas enviadas por uma regra de caixa de entrada</span><span class="sxs-lookup"><span data-stu-id="da243-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="da243-210">IPM. OLE. Classificação</span><span class="sxs-lookup"><span data-stu-id="da243-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="da243-211">Exceções de uma série recorrente</span><span class="sxs-lookup"><span data-stu-id="da243-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="da243-212">IPM. ReCall. Report</span><span class="sxs-lookup"><span data-stu-id="da243-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="da243-213">Relatórios de recuperação de mensagens</span><span class="sxs-lookup"><span data-stu-id="da243-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="da243-214">IPM. Remota</span><span class="sxs-lookup"><span data-stu-id="da243-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="da243-215">Mensagens de email remotas</span><span class="sxs-lookup"><span data-stu-id="da243-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="da243-216">IPM. Lo</span><span class="sxs-lookup"><span data-stu-id="da243-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="da243-217">Relatórios de status do item</span><span class="sxs-lookup"><span data-stu-id="da243-217">Item status reports</span></span>  <br/> |
