---
title: Gerenciar um incidente de derramamento de dados no Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo descreve o uso da nova ferramenta de investigações de dados (visualização) no centro de conformidade do & de segurança do Office 365 para gerenciar um incidente de derramamento de dados.
ms.openlocfilehash: 93cbbed8763f0af31ab8d4e32348f01bfda17a2a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218121"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a><span data-ttu-id="514fe-103">Gerenciar um incidente de derramamento de dados no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="514fe-103">Manage a data spillage incident in Microsoft 365</span></span> 

<span data-ttu-id="514fe-p101">Data derramamento é quando um documento confidencial é liberado em um ambiente não confiável. Quando um incidente de derramamento de dados é detectado, é importante avaliar rapidamente o tamanho e os locais do derramamento, examinar as atividades do usuário em torno dele e, em seguida, limpar permanentemente os dados derramados do sistema.</span><span class="sxs-lookup"><span data-stu-id="514fe-p101">Data spillage is when a confidential document is released into an untrusted environment. When a data spillage incident is detected, it's important to quickly assess the size and locations of the spillage, examine user activities around it, and then permanently purge the spilled data from the system.</span></span>

## <a name="scope-of-this-article"></a><span data-ttu-id="514fe-106">Escopo deste artigo</span><span class="sxs-lookup"><span data-stu-id="514fe-106">Scope of this article</span></span>

<span data-ttu-id="514fe-107">Este artigo fornece uma lista de instruções sobre como remover permanentemente itens das caixas de correio do Office 365 para que eles não sejam mais acessíveis ou recuperáveis por usuários ou administradores.</span><span class="sxs-lookup"><span data-stu-id="514fe-107">This article provides a list of instructions on how to permanently remove items from Office 365 mailboxes so they are no longer accessible or recoverable by users or admins.</span></span> 

> [!NOTE]
> <span data-ttu-id="514fe-108">Quando você exclui itens localizados em um site do SharePoint ou do OneDrive for Business, eles são mantidos por 93 dias a partir do momento em que são excluídos do local original.</span><span class="sxs-lookup"><span data-stu-id="514fe-108">When you delete items located in a SharePoint or OneDrive for Business site, they are retained for 93 days from the time you delete them from their original location.</span></span>

## <a name="scenario"></a><span data-ttu-id="514fe-109">Cenário</span><span class="sxs-lookup"><span data-stu-id="514fe-109">Scenario</span></span>

<span data-ttu-id="514fe-p102">Você é informado de um incidente de derramamento de dados em que um funcionário compartilhou inadvertidamente um documento altamente confidencial com várias pessoas por email. Você deseja avaliar rapidamente quem recebeu este documento, tanto dentro e fora da sua organização. Após investigar o incidente, você planeja compartilhar suas descobertas com outros investigadores para analisar e, em seguida, remover permanentemente os dados derramados do Office 365. Após a conclusão da investigação, você deseja remover todas as evidências.</span><span class="sxs-lookup"><span data-stu-id="514fe-p102">You're informed of a data spillage incident where an employee unknowingly shared a highly-confidential document with multiple people through email. You want to quickly assess who received this document, both inside and outside of your organization. After you've investigate the incident, you plan to share your findings with other investigators to review, and then permanently remove the spilled data from Office 365. After the investigation is complete, you want to remove all evidence.</span></span> 

## <a name="workflow"></a><span data-ttu-id="514fe-114">Fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="514fe-114">Workflow</span></span>

<span data-ttu-id="514fe-115">Este é o fluxo de trabalho para usar investigações de dados (visualização) para gerenciar um incidente de derramamento de dados:</span><span class="sxs-lookup"><span data-stu-id="514fe-115">Here's the workflow for using Data Investigations (Preview) to manage a data spillage incident:</span></span>

1.  <span data-ttu-id="514fe-116">Criar uma investigação de dados.</span><span class="sxs-lookup"><span data-stu-id="514fe-116">Create a data investigation.</span></span>

2.  <span data-ttu-id="514fe-117">Procure os dados derramados.</span><span class="sxs-lookup"><span data-stu-id="514fe-117">Search for the spilled data.</span></span>

3.  <span data-ttu-id="514fe-118">Revise e investigue o incidente.</span><span class="sxs-lookup"><span data-stu-id="514fe-118">Review and investigate the incident.</span></span>

4.  <span data-ttu-id="514fe-119">Excluir permanentemente os dados derramados.</span><span class="sxs-lookup"><span data-stu-id="514fe-119">Permanently delete the spilled data.</span></span>

5.  <span data-ttu-id="514fe-120">Feche ou exclua a investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-120">Close or delete the investigation.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="514fe-121">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="514fe-121">Before you begin</span></span>

- <span data-ttu-id="514fe-p103">Você usará a ferramenta de investigações de dados (visualização) no centro de conformidade do & de segurança do Office 365 para criar uma investigação, procurar os dados derramados e examiná-los e analisá-los. Em seguida, você usará o PowerShell do centro de conformidade do & de segurança para excluir permanentemente os dados derramados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="514fe-p103">You'll use the Data Investigations (Preview) tool in the Office 365 Security & Compliance Center to create an investigation, search for the spilled data, and review and analyze it. Then you'll use Security & Compliance Center PowerShell to permanently delete the spilled data from Office 365.</span></span> 

- <span data-ttu-id="514fe-124">Para criar uma investigação, você precisa ser membro do grupo de função Administrador de conformidade no centro de conformidade do & de segurança.</span><span class="sxs-lookup"><span data-stu-id="514fe-124">To create an investigation, you have to be a member of the Compliance Administrator role group in the Security & Compliance Center.</span></span>

- <span data-ttu-id="514fe-p104">Para excluir mensagens, você precisa ser membro do grupo de função gerenciamento da organização no centro de conformidade do & de segurança ou ser atribuído à função de pesquisa e limpeza. Para obter informações sobre como adicionar usuários a um grupo de funções, consulte [conceder aos usuários acesso ao centro de conformidade do & de segurança](../grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="514fe-p104">To delete messages, you have to be a member of the Organization Management role group in the Security & Compliance Center or be assigned the Search and Purge role. For information about adding users to a role group, see [Give users access to the Security & Compliance Center](../grant-access-to-the-security-and-compliance-center.md).</span></span> 

- <span data-ttu-id="514fe-p105">Para controlar quais caixas de correio de usuário e contas do OneDrive podem pesquisar, sua organização pode configurar os limites de conformidade. Para obter mais informações, [Configure os limites de conformidade para investigações de descoberta eletrônica](../set-up-compliance-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="514fe-p105">To control which user mailboxes and OneDrive accounts an investigator can search, your organization can set up compliance boundaries. For more information, [Set up compliance boundaries for eDiscovery investigations](../set-up-compliance-boundaries.md).</span></span> 

## <a name="step-1-create-a-data-investigation"></a><span data-ttu-id="514fe-129">Etapa 1: criar uma investigação de dados</span><span class="sxs-lookup"><span data-stu-id="514fe-129">Step 1: Create a data investigation</span></span>

<span data-ttu-id="514fe-130">Para criar uma investigação de dados:</span><span class="sxs-lookup"><span data-stu-id="514fe-130">To create a data investigation:</span></span>

1. <span data-ttu-id="514fe-131">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="514fe-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="514fe-132">Entre no Office 365 usando a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="514fe-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="514fe-133">No centro de conformidade do & de segurança, clique em **investigações de dados**.</span><span class="sxs-lookup"><span data-stu-id="514fe-133">In the Security & Compliance Center, click **Data Investigations**.</span></span>
 
4. <span data-ttu-id="514fe-134">Na página **investigações de dados (visualização)** , clique em **criar uma nova investigação**.</span><span class="sxs-lookup"><span data-stu-id="514fe-134">On the **Data Investigations (Preview)** page, click **Create a new investigation**.</span></span>
    
5. <span data-ttu-id="514fe-p106">Na nova página de submenu de **investigação de dados** , dê um nome à investigação (obrigatório) e digite um número de investigação e uma descrição opcionais. Observe que o nome deve ser exclusivo em sua organização.</span><span class="sxs-lookup"><span data-stu-id="514fe-p106">On the **New data investigation** flyout page, give the investigation a name (required), and then type an optional investigation number and description. Note that the name must be unique in your organization.</span></span>

6. <span data-ttu-id="514fe-137">Em **você deseja definir configurações adicionais depois de criar esta investigação?**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="514fe-137">Under **Do you want to configure additional settings after creating this investigation?**, do one of the following:</span></span>

    - <span data-ttu-id="514fe-p107">Clique em **Sim** para criar a investigação e exiba a página **configurações** no novo caso. Isso permite adicionar membros à investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-p107">Click **Yes** to create the investigation, and display the **Settings** page in the new case. This allows you to add members to the investigation.</span></span>
    
    - <span data-ttu-id="514fe-p108">Clique em **não** para apenas criar a investigação e exibi-la na lista de casos na página **investigações de dados (visualização)** . Se você escolher essa opção, será adicionado como o único membro da investigação, e as configurações padrão de pesquisa e análise serão usadas. Você pode adicionar membros ou alterar as configurações a qualquer momento após a criação da investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-p108">Click **No** to just create the investigation and display it in the list of cases on the **Data Investigations (Preview)** page. If you choose this option, you will be added as the only member of the investigation and the default search and analytics settings will be used. You can add members or change settings any time after the investigation is created.</span></span>

7. <span data-ttu-id="514fe-143">Clique em **salvar** para criar a investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-143">Click **Save** to create the investigation.</span></span>

    <span data-ttu-id="514fe-144">A nova investigação é exibida na lista na página **investigações de dados (visualização)** .</span><span class="sxs-lookup"><span data-stu-id="514fe-144">The new investigation is displayed in the list on the **Data Investigations (Preview)** page.</span></span> 

8. <span data-ttu-id="514fe-145">Para abrir uma investigação, clique no nome da investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-145">To open an investigation, click the name of the investigation.</span></span> 

    <span data-ttu-id="514fe-146">A guia **página inicial** da investigação é exibida.</span><span class="sxs-lookup"><span data-stu-id="514fe-146">The **Home** tab for the investigation is displayed.</span></span> 

> [!TIP]
> <span data-ttu-id="514fe-147">Considere o estabelecimento de uma Convenção de nomenclatura para investigações e forneça tantas informações quantas forem necessárias no nome e na descrição para que você possa localizar e consultar no futuro, se necessário.</span><span class="sxs-lookup"><span data-stu-id="514fe-147">Consider establishing a naming convention for investigations and provide as much information as you can in the name and description so you can locate and refer to in the future if necessary.</span></span>
 
## <a name="step-2-search-for-the-spilled-data"></a><span data-ttu-id="514fe-148">Etapa 2: Pesquisar os dados derramados</span><span class="sxs-lookup"><span data-stu-id="514fe-148">Step 2: Search for the spilled data</span></span> 
 
<span data-ttu-id="514fe-p109">Se você souber quais usuários você deseja pesquisar por dados derramados, você pode adicioná-los como pessoas de interesse para mapear suas fontes de dados para a investigação e pesquisar rapidamente a sua caixa de correio e a conta do OneDrive. Para adicionar pessoas de interesse à investigação, clique em **pessoas de interesse**e, em seguida, clique em **adicionar pessoas de interesse**.</span><span class="sxs-lookup"><span data-stu-id="514fe-p109">If you know which users you want to search for spilled data, you can add them as people of interest to map their data sources to the investigation and quickly search their mailbox and OneDrive account. To add people of interest to the investigation, click **People of interest**, and then click **Add people of interest**.</span></span> 

<span data-ttu-id="514fe-p110">Na guia **pesquisas** , você pode criar pesquisas para localizar os dados derramados. Você usará a mesma consulta de pesquisa que usou para localizar os dados derramados para excluir essas mesmas mensagens na [etapa 4](##step-4:-permanently-delete-the-spilled-data). Para obter mais informações sobre a criação de pesquisas, consulte [criar uma pesquisa para coletar dados](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="514fe-p110">On the **Searches** tab, you can create searches to find the spilled data. You will use the same search query that you used to find the spilled data to delete those same messages in [Step 4](##step-4:-permanently-delete-the-spilled-data). For more information about creating searches, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="514fe-p111">Depois de executar a pesquisa, você pode Visualizar amostras de resultados de pesquisa e exibir estatísticas de pesquisa para avaliar a eficácia da consulta de pesquisa. Depois de identificar os itens que você deseja excluir do Office 365, você pode clicar na guia **incidentes** e, em seguida, criar um incidente e adicionar resultados de pesquisa que contenham esses itens.</span><span class="sxs-lookup"><span data-stu-id="514fe-p111">After you run the search, you can preview samples of search results and view search statistics to evaluate the effectiveness of your search query. Once you identify the items that you want to delete from Office 365, you can click the **Incidents** tab, and then create an incident and add search results that contain those items.</span></span> 

<span data-ttu-id="514fe-p112">Para fazer isso, clique na pesquisa que você deseja investigar. Na página do menu suspenso, clique em **Adicionar resultados a incidentes** e siga as instruções. Em seguida, no incidente, você pode revisar documentos individuais, investigar quem teve acesso aos documentos e exportar os documentos. Para simplesmente excluir os documentos em vez de analisá-los, vá para a [etapa 4](##step-4:-permanently-delete-the-spilled-data).</span><span class="sxs-lookup"><span data-stu-id="514fe-p112">To do this, click the search that you want to investigate. On the flyout page, click **Add results to incident** and follow the instructions. Then in the incident, you can review individual documents, investigate who had access to documents, and export the documents. To simply delete the documents instead of reviewing them, go to [Step 4](##step-4:-permanently-delete-the-spilled-data).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="514fe-p113">As palavras-chave que você usa na consulta de pesquisa podem conter os dados reais derramados que você está pesquisando. Por exemplo, se você estiver procurando documentos que contenham um número de seguro social e usá-lo como uma palavra-chave na consulta de pesquisa, você deverá excluir a consulta posteriormente para evitar mais derramamento. Você pode excluir a pesquisa ou excluir toda a investigação na [etapa 5](##step-5:-close-or-delete-investigation).</span><span class="sxs-lookup"><span data-stu-id="514fe-p113">The keywords that you use in the search query may contain the actual spilled data that you're searching for. For example, if you searching for documents containing a social security number and you use it as a keyword in the search query, you must delete the query afterwards to avoid further spillage. You can delete search or delete the entire investigation in [Step 5](##step-5:-close-or-delete-investigation).</span></span> 

## <a name="step-3-review-and-investigate"></a><span data-ttu-id="514fe-163">Etapa 3: analisar e investigar</span><span class="sxs-lookup"><span data-stu-id="514fe-163">Step 3: Review and investigate</span></span> 

<span data-ttu-id="514fe-p114">Na investigação, vá para a guia **incidentes** e clique no incidente que você criou na etapa anterior. Depois que o trabalho de processamento for concluído e os resultados da pesquisa forem adicionados ao incidente, você poderá revisar documentos individuais em seu formato nativo, formato de texto ou um formato Near-Native. Você pode criar consultas adicionais para restringir ainda mais a lista de documentos e marcar documentos para indicar resultados de sua investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-p114">In the investigation, go to **Incidents** tab and click on the incident that you created in the previous step. After the processing job is completed and the search results are added to the incident, you can review individual documents in their native format, text format, or a near-native format. You can create additional queries to further narrow the list of documents, and tag documents to indicate findings from your investigation.</span></span>

<span data-ttu-id="514fe-p115">Para agrupar documentos e obter mais assistência para revisão, clique em **gerenciar incidente**. No bloco de **análise** , clique em **analisar**. Isso executará análises avançadas, como detecção de duplicidades, encadeamento de emails e análise de tema. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="514fe-p115">To group documents and get more assistance for your review, click **Manage incident**. In the **Analytics** tile, click **Analyze**. This will run advanced analytics such as duplicate detection, email threading, and theme analysis. For more information, see:</span></span>

- [<span data-ttu-id="514fe-171">Detecção próxima duplicação</span><span class="sxs-lookup"><span data-stu-id="514fe-171">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="514fe-172">Encadeamento de email</span><span class="sxs-lookup"><span data-stu-id="514fe-172">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="514fe-173">Temas</span><span class="sxs-lookup"><span data-stu-id="514fe-173">Themes</span></span>](themes.md)

<span data-ttu-id="514fe-p116">Para determinar quais usuários estão envolvidos no derramamento de dados, você pode criar uma nova consulta no incidente e usar as condições remetente/autor e destinatários. Isso criará uma lista de todos os remetentes, destinatários e autores encontrados nos dados coletados que foram adicionados ao incidente. Certifique-se de examinar a lista para determinar se há usuários externos na lista. Para obter mais informações, consulte [Search Conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="514fe-p116">To determine which users are involved in the data spillage, you can create a new query in the incident and then use the Sender/Author and Recipients conditions. This will create a list of all senders, recipients and authors found in collected data that was added to the incident. Be sure to examine the list to determine if there are any external users in the list. For more information, see [Search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>

## <a name="step-4-permanently-delete-the-spilled-data"></a><span data-ttu-id="514fe-178">Etapa 4: excluir permanentemente os dados derramados</span><span class="sxs-lookup"><span data-stu-id="514fe-178">Step 4: Permanently delete the spilled data</span></span>

### <a name="deleting-mailbox-items"></a><span data-ttu-id="514fe-179">Excluir itens de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="514fe-179">Deleting mailbox items</span></span>

<span data-ttu-id="514fe-p117">Após revisar e validar que os resultados da pesquisa contenham apenas as mensagens de email que devem ser excluídas, você pode excluí-las permanentemente executando o comando **New-ComplianceSearchAction-remove-purge HardDelete** em Security & Compliance Central do PowerShell. Para obter instruções, confira [Pesquisar e excluir mensagens de email](../search-for-and-delete-messages-in-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="514fe-p117">After you review and validate that the search results contain only the email messages that must be deleted, you can permanently delete them by running the **New-ComplianceSearchAction -Purge -PurgeType HardDelete** command in Security & Compliance Center PowerShell. For instructions, see [Search for and delete email messages](../search-for-and-delete-messages-in-your-organization.md).</span></span> 

<span data-ttu-id="514fe-p118">Observe que, se a recuperação de item único estiver habilitada para caixas de correio em sua organização, os itens excluídos permanentemente serão mantidos na pasta itens recuperáveis do usuário (e acessíveis por administradores) até que o período de retenção do item excluído termine (o padrão é 14 dias). Além disso, se qualquer uma das caixas de correio que contêm dados derramados estiver em um bloqueio legal ou atribuída a uma política de retenção, a mensagem limpa será mantida na pasta itens recuperáveis até que a retenção seja removida ou a caixa de correio seja excluída das políticas de retenção. Para excluir mensagens de forma rígida imediatamente, você precisa executar tarefas de adição. Para obter instruções, consulte [excluir itens da pasta itens recuperáveis das caixas de correio baseadas em nuvem em espera ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span><span class="sxs-lookup"><span data-stu-id="514fe-p118">Note that if single item recovery is enabled for mailboxes in your organization, permanently deleted items will be retained in the user's Recoverable items folder (and accessible by admins) until the deleted item retention period ends (default is 14 days). Additionally, if any of the mailboxes that contain spilled data are on a legal hold or assigned to a retention policy, purged message will be retained in Recoverable items folder until the hold is removed or the mailbox is excluded from retention policies. To hard delete messages immediately, you need to perform addition tasks. For instructions, see [Delete items in the Recoverable Items folder of cloud-based mailboxes on hold ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="514fe-p119">Consulte o gerenciamento de registros ou os departamentos legais antes de remover uma política de retenção ou bloqueio. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de derramamento de dados tem prioridade.</span><span class="sxs-lookup"><span data-stu-id="514fe-p119">Check with your records management or legal departments before removing a hold or retention policy. Your organization may have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 

### <a name="deleting-site-items"></a><span data-ttu-id="514fe-188">Excluindo itens de site</span><span class="sxs-lookup"><span data-stu-id="514fe-188">Deleting site items</span></span>

<span data-ttu-id="514fe-p120">Para excluir permanentemente um documento de um site do SharePoint ou de uma conta do OneDrive for Business, exclua-o e, em seguida, exclua-o do site e, em seguida, exclua-o da lixeira do conjunto de sites. Para obter instruções, consulte [Excluir documentos no SharePoint e no onedrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span><span class="sxs-lookup"><span data-stu-id="514fe-p120">To permanently delete a document from a SharePoint site or OneDrive for Business account, you have to delete it and then you have to delete from the site and then delete it from the site collection Recycle Bin. For instructions, see [Delete documents in SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span></span>

<span data-ttu-id="514fe-p121">Como alternativa, você pode excluir um conjunto de sites inteiro que pode conter dados derramados. Para obter instruções, consulte [excluir um conjunto de sites](https://docs.microsoft.com/sharepoint/delete-site-collection).</span><span class="sxs-lookup"><span data-stu-id="514fe-p121">Alternatively, you can delete an entire site collection that might contained spilled data. For instructions, see [Delete a site collection](https://docs.microsoft.com/sharepoint/delete-site-collection).</span></span>

## <a name="step-5-close-or-delete-the-investigation"></a><span data-ttu-id="514fe-193">Etapa 5: fechar ou excluir a investigação</span><span class="sxs-lookup"><span data-stu-id="514fe-193">Step 5: Close or delete the investigation</span></span>

<span data-ttu-id="514fe-p122">Após excluir documentos nos locais de conteúdo de origem (caixas de correio ou sites), você ainda terá cópias desses documentos que você adicionou aos incidentes como parte da sua investigação. Para evitar mais dados derramamento, considere a possibilidade de excluir a investigação.</span><span class="sxs-lookup"><span data-stu-id="514fe-p122">After you delete documents in the source content locations (mailboxes or sites), you will still have copies of these documents that you added to incidents as part of your investigation. To avoid further data spillage, you should consider deleting the investigation.</span></span>

<span data-ttu-id="514fe-196">Para excluir uma investigação:</span><span class="sxs-lookup"><span data-stu-id="514fe-196">To delete an investigation:</span></span>

1. <span data-ttu-id="514fe-197">Na guia **configurações** , clique em **informações de investigação**.</span><span class="sxs-lookup"><span data-stu-id="514fe-197">On the **Settings** tab, click **Investigation information**.</span></span>

2. <span data-ttu-id="514fe-198">Clique em **excluir caso**.</span><span class="sxs-lookup"><span data-stu-id="514fe-198">Click  **Delete case**.</span></span> 

<span data-ttu-id="514fe-p123">Se você não precisar excluir a investigação ou se quiser salvar as informações coletadas durante a investigação, clique em **fechar caso**. Em uma data posterior, você pode reabrir investigações fechadas.</span><span class="sxs-lookup"><span data-stu-id="514fe-p123">If you don't need to delete the investigation or if you want to save the information that you collected during the investigation, you can click **Close case**. At a later date, you can re-open closed investigations.</span></span>