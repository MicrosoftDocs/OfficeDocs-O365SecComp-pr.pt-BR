---
title: Atividade de auditoria do modo de exibição dos responsáveis
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8219ae8a061f6d08dd37da5b7f2974dd86c68f04
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607318"
---
# <a name="viewing-custodian-audit-activity"></a><span data-ttu-id="00756-102">Exibindo a atividade de auditoria dos responsáveis</span><span class="sxs-lookup"><span data-stu-id="00756-102">Viewing custodian audit activity</span></span>

<span data-ttu-id="00756-p101">Precisa encontrar se um usuário exibido um documento específico ou removidos de um item de suas caixas de correio? EDiscovery avançado (Preview) agora é integrado com a ferramenta de pesquisa de log de auditoria existente no Centro de conformidade do & de segurança. Usando essa experiência incorporada, você pode usar a ferramenta de gerenciamento dos responsáveis eDiscovery avançado (Preview) para facilitar sua investigação facilmente acessando e pesquisar a atividade responsáveis dentro de seu caso.</span><span class="sxs-lookup"><span data-stu-id="00756-p101">Need to find if a user viewed a specific document or purged an item from their mailbox? Advanced eDiscovery (Preview) is now integrated with the existing audit log search tool in the Security & Compliance Center. Using this embedded experience, you can use the Advanced eDiscovery (Preview) Custodian Management tool to facilitate your investigation by easily accessing and searching the activity for custodians within your case.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="00756-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="00756-106">Before you begin</span></span>

<span data-ttu-id="00756-p102">Você precisa ter a função Logs de auditoria somente para exibição ou Logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de funções de gerenciamento da organização na página permissões no Centro de administração do Exchange e gerenciamento de conformidade. Para conceder a um usuário a capacidade de pesquisar o log de auditoria de eDiscovery avançado (Preview) com o nível mínimo de privilégios, você pode criar um grupo de função personalizada no Exchange Online, adicionar a função Logs de auditoria somente para exibição ou Logs de auditoria e, em seguida, adicionar o usuário como membro do novo GA de função grupo. Para obter mais informações, consulte gerenciar grupos de função no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="00756-p102">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to search the Office 365 audit log. By default, these roles are assigned to the Compliance Management and Organization Management role groups on the Permissions page in the Exchange admin center. To give a user the ability to search the Advanced eDiscovery (Preview) audit log with the minimum level of privileges, you can create a custom role group in Exchange Online, add the View-Only Audit Logs or Audit Logs role, and then add the user as a member of the new role group. For more information, see Manage role groups in Exchange Online.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00756-p103">Se você atribuir um usuário a função Logs de auditoria somente para exibição ou Logs de auditoria na página permissões no Centro de conformidade do & de segurança, eles não possam pesquisar no log de auditoria do Office 365. Você precisa atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="00756-p103">If you assign a user the View-Only Audit Logs or Audit Logs role on the Permissions page in the Security & Compliance Center, they won't be able to search the Office 365 audit log. You have to assign the permissions in Exchange Online. This is because the underlying cmdlet used to search the audit log is an Exchange Online cmdlet.</span></span>

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a><span data-ttu-id="00756-114">Etapa 1: Criar uma pesquisa de log de auditoria de eDiscovery avançado (Preview)</span><span class="sxs-lookup"><span data-stu-id="00756-114">Step 1: Create an Advanced eDiscovery (Preview) audit log search</span></span>

   1. <span data-ttu-id="00756-115">Selecione uma ocorrência existente a **segurança & Centro de conformidade gt _ avançado descoberta eletrônica (Preview)**.</span><span class="sxs-lookup"><span data-stu-id="00756-115">Select an existing case from the **Security & Compliance Center > Advanced eDiscovery (Preview)**.</span></span>
   
   2. <span data-ttu-id="00756-116">Navegue até a guia **responsáveis** e selecione dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="00756-116">Navigate to the **Custodians** tab and select a custodian.</span></span>
   
   3. <span data-ttu-id="00756-117">Uma vez que você selecionou um funcionário encarregado, clique em **Exibir dos responsáveis atividade** do painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="00756-117">Once you have selected a custodian, click **View Custodian Activity** from the details panel.</span></span>
   
   4. <span data-ttu-id="00756-118">Configure os seguintes critérios de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="00756-118">Configure the following search criteria:</span></span>
      
      <span data-ttu-id="00756-p104">r. **atividades** - clique na lista suspensa para exibir as atividades que você pode pesquisar. Depois de executar a pesquisa, somente os registros de auditoria para as atividades selecionadas são exibidos. A seleção de **Mostrar os resultados de todas as atividades** exibirá resultados para todas as atividades que atendem aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="00756-p104">a. **Activities** - Click the drop-down list to display the activities that you can search for. After you run the search, only the audit records for the selected activities are displayed. Selecting **Show results for all activities** will display results for all activities that meet the other search criteria.</span></span>
      
      <span data-ttu-id="00756-p105">b. a **Data de início e data de término** - selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. Últimos sete dias são marcados por padrão. A data e hora são apresentados no formato Tempo Universal Coordenado (UTC). O intervalo de datas máximo que você pode especificar é um ano.</span><span class="sxs-lookup"><span data-stu-id="00756-p105">b. **Start date and End date** - Select a date and time range to display the events that occurred within that period. The last seven days are selected by default. The date and time are presented in Coordinated Universal Time (UTC) format. The maximum date range that you can specify is one year.</span></span>
      
      <span data-ttu-id="00756-p106">resultados para mais c. **responsáveis** - Click nesta caixa e selecione um funcionário encarregado de específico para exibir a pesquisa. Registros de auditoria da atividade selecionada executadas pelos usuários que você selecionar nesta caixa são exibidos na lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="00756-p106">c. **Custodians** - Click in this box and then select a specific custodian to display search results for. Audit records for the selected activity performed by the users you select in this box are displayed in the list of results.</span></span>
    
    1. <span data-ttu-id="00756-p107">Clique em **pesquisa** para executar a pesquisa usando os critérios de pesquisa. Os resultados da pesquisa são carregados e, após alguns momentos são exibidas em resultados na página de pesquisa dos responsáveis atividades.</span><span class="sxs-lookup"><span data-stu-id="00756-p107">Click **Search** to run the search using your search criteria. The search results are loaded, and after a few moments they are displayed under Results on the Custodian Activities search page.</span></span> 

## <a name="step-2-view-the-audit-log-search-results"></a><span data-ttu-id="00756-133">Etapa 2: Exibir os resultados da pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="00756-133">Step 2: View the audit log search results</span></span>

<span data-ttu-id="00756-p108">Os resultados de uma pesquisa de log de auditoria são exibidos em resultados na página log de auditoria dos responsáveis. Um máximo de 5.000 eventos (mais recentes) são exibidos em incrementos de 150 eventos. Para exibir mais eventos você pode usar a barra de rolagem no painel de resultados ou você pode pressionar Shift + End para exibir os eventos de 150 Avançar.</span><span class="sxs-lookup"><span data-stu-id="00756-p108">The results of an audit log search are displayed under Results on the Custodian Audit log page. A maximum of 5,000 (newest) events are displayed in increments of 150 events. To display more events you can use the scroll bar in the Results pane or you can press Shift + End to display the next 150 events.</span></span>

<span data-ttu-id="00756-137">Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa.</span><span class="sxs-lookup"><span data-stu-id="00756-137">The results contain the following information about each event returned by the search.</span></span>
- <span data-ttu-id="00756-138">**Data**: A data e hora (no formato UTC) quando o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="00756-138">**Date**: The date and time (in UTC format) when the event occurred.</span></span>

- <span data-ttu-id="00756-p109">**Endereço IP**: O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido no formato de endereço de um IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="00756-p109">**IP address**: The IP address of the device that was used when the activity was logged. The IP address is displayed in either an IPv4 or IPv6 address format.</span></span>

- <span data-ttu-id="00756-141">**Usuário**: A conta de usuário (ou serviço) que executou a ação que acionou o evento.</span><span class="sxs-lookup"><span data-stu-id="00756-141">**User**: The user (or service account) who performed the action that triggered the event.</span></span>

- <span data-ttu-id="00756-p110">**Atividade**: A atividade executada pelo usuário. Esse valor corresponde às atividades selecionado na lista suspensa atividades. Para um evento do log de auditoria do administrador do Exchange, o valor nessa coluna é um cmdlet do Exchange.</span><span class="sxs-lookup"><span data-stu-id="00756-p110">**Activity**: The activity performed by the user. This value corresponds to the activities that you selected in the Activities drop down list. For an event from the Exchange admin audit log, the value in this column is an Exchange cmdlet.</span></span>

- <span data-ttu-id="00756-p111">**Item**: O objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta de usuário que foi atualizada. Nem todas as atividades têm um valor nessa coluna.</span><span class="sxs-lookup"><span data-stu-id="00756-p111">**Item**: The object that was created or modified as a result of the corresponding activity. For example, the file that was viewed or modified or the user account that was updated. Not all activities have a value in this column.</span></span>

- <span data-ttu-id="00756-p112">**Detalhes**: detalhes adicionais sobre uma atividade. Novamente, nem todas as atividades terá um valor.</span><span class="sxs-lookup"><span data-stu-id="00756-p112">**Detail**: Additional detail about an activity. Again, not all activities will have a value.</span></span>

## <a name="step-3-filter-the-search-results"></a><span data-ttu-id="00756-150">Etapa 3: Filtrar os resultados de pesquisa</span><span class="sxs-lookup"><span data-stu-id="00756-150">Step 3: Filter the search results</span></span>

<span data-ttu-id="00756-p113">Além de classificar, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Isso pode ajudá-lo a rapidamente filtrar os resultados para um usuário específico ou atividade.</span><span class="sxs-lookup"><span data-stu-id="00756-p113">In addition to sorting, you can also filter the results of an audit log search. This can help you quickly filter the results for a specific user or activity.</span></span> 

<span data-ttu-id="00756-153">Para filtrar os resultados:</span><span class="sxs-lookup"><span data-stu-id="00756-153">To filter the results:</span></span>

 1. <span data-ttu-id="00756-154">Criar e executar uma pesquisa de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="00756-154">Create and run an audit log search.</span></span>
  
2. <span data-ttu-id="00756-155">Quando os resultados são exibidos, clique em **filtrar os resultados**.</span><span class="sxs-lookup"><span data-stu-id="00756-155">When the results are displayed, click **Filter results**.</span></span>
 
3. <span data-ttu-id="00756-156">Caixas de palavra-chave serão exibidas em cada cabeçalho de coluna.</span><span class="sxs-lookup"><span data-stu-id="00756-156">Keyword boxes are displayed under each column header.</span></span>
  
4. <span data-ttu-id="00756-p114">Clique em uma das caixas em um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna que você está filtrando. Os resultados serão reajustar dinamicamente para exibir os eventos que correspondem ao seu filtro.</span><span class="sxs-lookup"><span data-stu-id="00756-p114">Click one of the boxes under a column header and type a word or phrase, depending on the column you're filtering on. The results will dynamically readjust to display the events that match your filter.</span></span>
  
5. <span data-ttu-id="00756-159">Para limpar um filtro, clique em **X** na caixa filtro ou basta clicar em **ocultar a filtragem**.</span><span class="sxs-lookup"><span data-stu-id="00756-159">To clear a filter, click the **X** in the filter box or just click **Hide filtering**.</span></span>

## <a name="export-the-search-results-to-a-file"></a><span data-ttu-id="00756-160">Exportar resultados da pesquisa para um arquivo</span><span class="sxs-lookup"><span data-stu-id="00756-160">Export the search results to a file</span></span>

<span data-ttu-id="00756-p115">Você pode exportar os resultados de uma pesquisa de log de auditoria para um arquivo de (CSV) de valores separados por vírgulas no computador local. Você pode abrir este arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e a divisão de uma única coluna (que contém as células de valores múltiplos) em várias colunas.</span><span class="sxs-lookup"><span data-stu-id="00756-p115">You can export the results of an audit log search to a comma separated value (CSV) file on your local computer. You can open this file in Microsoft Excel and use features such as search, sorting, filtering, and splitting a single column (that contains multi-value cells) into multiple columns.</span></span>

1. <span data-ttu-id="00756-163">Executar uma pesquisa de log de auditoria e posteriormente revisar os critérios de pesquisa até que você tenha os resultados desejados.</span><span class="sxs-lookup"><span data-stu-id="00756-163">Run an audit log search, and then revise the search criteria until you have the desired results.</span></span>
  
2. <span data-ttu-id="00756-164">Clique em Exportar resultados e selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="00756-164">Click Export results and select one of the following options:</span></span>

    - <span data-ttu-id="00756-p116">**Salvar carregado resultados:** Escolha esta opção para exportar apenas as entradas que são exibidas em **resultados** na página de **pesquisa de log de auditoria dos responsáveis** . O arquivo CSV que é baixado contém as mesmas colunas (e dados) exibidos na página (data, usuário, atividade, Item e detalhes). Uma coluna adicional (intitulada **mais**) está incluída no arquivo CSV que contém mais informações da entrada de log de auditoria. Porque você está exportando os mesmos resultados que são carregados (e visualizável) na página de pesquisa de log de auditoria, um máximo de 5.000 entradas são exportados.</span><span class="sxs-lookup"><span data-stu-id="00756-p116">**Save loaded results:** Choose this option to export only the entries that are displayed under **Results** on the **Custodian Audit log search** page. The CSV file that is downloaded contains the same columns (and data) displayed on the page (Date, User, Activity, Item, and Details). An additional column (titled **More**) is included in the CSV file that contains more information from the audit log entry. Because you're exporting the same results that are loaded (and viewable) on the Audit log search page, a maximum of 5,000 entries are exported.</span></span>
        
    - <span data-ttu-id="00756-p117">**Baixe todos os resultados:** Escolha esta opção para exportar todas as entradas de log de auditoria do Office 365 que atendam aos critérios de pesquisa. Para um grande conjunto de resultados da pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além de 5.000 resultados que podem ser exibidos na página de pesquisa de **log de auditoria dos responsáveis** . Essa opção baixar os dados brutos do log de auditoria para um arquivo CSV e contém informações adicionais da entrada de log de auditoria em uma coluna chamada AuditData. Pode levar mais tempo para baixar o arquivo, se você escolher essa opção de exportação porque o arquivo pode ser muito maior daquela que é baixado se você escolher a opção outra.</span><span class="sxs-lookup"><span data-stu-id="00756-p117">**Download all results:** Choose this option to export all entries from the Office 365 audit log that meet the search criteria. For a large set of search results, choose this option to download all entries from the audit log in addition to the 5,000 results that can be displayed on the **Custodian Audit log** search page. This option will download the raw data from the audit log to a CSV file, and contains additional information from the audit log entry in a column named AuditData. It may take longer to download the file if you choose this export option because the file may be much larger than the one that's downloaded if you choose the other option.</span></span>
    
      > [!IMPORTANT]
      > <span data-ttu-id="00756-p118">Você pode baixar um máximo de 50.000 entradas para um arquivo CSV de uma pesquisa de log de auditoria único. Se 50.000 entradas são baixadas para o arquivo CSV, você pode assumir provavelmente há mais de 50.000 eventos que atendidos os critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas de log de auditoria. Você pode precisar executar várias pesquisas com menores intervalos de data para exportar entradas mais de 50.000.</span><span class="sxs-lookup"><span data-stu-id="00756-p118">You can download a maximum of 50,000 entries to a CSV file from a single audit log search. If 50,000 entries are downloaded to the CSV file, you can probably assume there are more than 50,000 events that met the search criteria. To export more than this limit, try using a date range to reduce the number of audit log entries. You might have to run multiple searches with smaller date ranges to export more than 50,000 entries.</span></span>
        

3. <span data-ttu-id="00756-177">Depois de selecionar uma opção de exportação, uma mensagem é exibida na parte inferior da janela solicitando que você abra o arquivo CSV, salve-o na pasta Downloads ou salvá-lo em uma pasta específica</span><span class="sxs-lookup"><span data-stu-id="00756-177">After you select an export option, a message is displayed at the bottom of the window that prompts you to open the CSV file, save it to the Downloads folder, or save it to a specific folder</span></span>

[!NOTE] 
 <span data-ttu-id="00756-178">Para obter mais informações sobre a visualização, filtragem ou exportar os resultados de pesquisa do log de auditoria, consulte:</span><span class="sxs-lookup"><span data-stu-id="00756-178">For more information about viewing, filtering, or exporting audit log search results, see:</span></span>
   - <span data-ttu-id="00756-179">Exiba a lista de atividades auditadas</span><span class="sxs-lookup"><span data-stu-id="00756-179">View List of Audited Activities</span></span> 
   - <span data-ttu-id="00756-180">Antes de começar: Logs de auditoria unificada</span><span class="sxs-lookup"><span data-stu-id="00756-180">Before You Begin: Unified Audit Logs</span></span>
 