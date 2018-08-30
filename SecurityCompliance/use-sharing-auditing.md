---
title: Usar o compartilhamento auditorias no log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'O compartilhamento é uma atividade fundamental no SharePoint Online e o OneDrive for Business. Os administradores agora podem usar compartilhamento auditorias no log de auditoria do Office 365 para determinar como compartilhamento está sendo usado em suas organizações. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524165"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="5bbfe-104">Usar o compartilhamento auditorias no log de auditoria do Office 365</span><span class="sxs-lookup"><span data-stu-id="5bbfe-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="5bbfe-p102">Compartilhamento é uma atividade fundamental no SharePoint Online e o OneDrive for Business e é amplamente usado nas organizações do Office 365. Os administradores agora podem usar compartilhamento auditorias no log de auditoria do Office 365 para determinar como compartilhamento está sendo usado em suas organizações.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="5bbfe-107">O esquema de compartilhamento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5bbfe-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="5bbfe-p103">Eventos de compartilhamento (excluindo compartilhamento de política e vincular eventos) são diferentes dos eventos relacionados a pasta e arquivo de uma maneira primária: um usuário está sendo uma ação que tem efeito algum outro usuário. Por exemplo, o usuário fornece acesso de usuário B para um arquivo. Neste exemplo, o usuário A é a *atuação de usuário* e o usuário B é o *usuário de destino*. No esquema de arquivo do SharePoint, a ação do usuário atuando afeta somente o arquivo em si. Quando o usuário A abre um arquivo, a única informação necessária para o evento **FileAccessed** é o usuário atuando. Para resolver essa diferença, não há um esquema separado, chamado o *esquema de compartilhamento do SharePoint*, que captura mais informações sobre compartilhamento de eventos. Isso garante que os administradores têm mais percepção que compartilhou um recurso e o recurso de usuário foi compartilhado com.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="5bbfe-115">O esquema de compartilhamento fornece dois campos adicionais no log de auditoria relacionados ao compartilhamento de eventos:</span><span class="sxs-lookup"><span data-stu-id="5bbfe-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="5bbfe-116">**TargetUserOrGroupName** - armazena o UPN ou o nome do usuário de destino ou grupo que um recurso foi compartilhado com (usuário B no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="5bbfe-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="5bbfe-117">**TargetUserOrGroupType** - identifica se o usuário de destino ou grupo é um membro, convidado, grupo ou parceiro.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="5bbfe-118">Esses dois campos, além de outras propriedades do Office 365 o esquema de log de auditoria como usuário, operação e data podem dizer a história completa sobre *quais* usuários shared *quais* recursos com *quem* e *quando*.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="5bbfe-p104">Não há outra propriedade de esquema que são importante para a história de compartilhamento. A propriedade **EventData** armazena informações adicionais sobre o compartilhamento de eventos. Por exemplo, quando um usuário compartilhar um site com outro usuário, isso é realizado por meio da adição de usuário de destino para um grupo do SharePoint. A propriedade **EventData** captura essas informações adicionais para fornecer um contexto para administradores.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="5bbfe-123">O modelo de compartilhamento e de eventos do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5bbfe-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="5bbfe-p105">Compartilhamento é definido por três eventos separados: **SharingSet**, **SharingInvitationCreated**e **SharingInvitaitonAccepted**. Aqui está o fluxo de trabalho para compartilhamento como eventos são registrados no log de auditoria do Office 365.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Fluxograma de como funciona a auditoria de compartilhamento](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="5bbfe-p106">Quando um usuário (o usuário atuando) quiser compartilhar um recurso com outro usuário (o usuário de destino), SharePoint (ou OneDrive for Business) primeiro verifica se o endereço de email do usuário de destino já está associado uma conta de usuário no diretório da organização. Se o usuário de destino está no diretório da organização, o SharePoint faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="5bbfe-129">Atribui imediatamente as permissões de usuário de destino para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="5bbfe-130">Envia uma notificação de compartilhamento para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="5bbfe-131">Registra um evento **SharingSet** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="5bbfe-132">Se uma conta de usuário para o usuário de destino não estiver no diretório da organização, o SharePoint faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5bbfe-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="5bbfe-133">Cria um convite de compartilhamento e envia para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="5bbfe-134">Registra um evento **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="5bbfe-135">O evento **SharingInvitationCreated** mais sempre é associado externo ou convidado de compartilhamento quando o usuário de destino não tem acesso ao recurso que foi compartilhado.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="5bbfe-p107">Quando o usuário de destino aceita o convite de compartilhamento que enviou a eles (clicando no link do convite), SharePoint registra um evento **SharingInvitationAccepted** e atribui as permissões de usuário de destino para acessar o recurso. Informações adicionais sobre o usuário de destino também são registradas, como a identidade do usuário que você recebeu o convite e o usuário que realmente aceitou o convite. Em alguns casos, esses usuários (ou endereços de email) podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="5bbfe-139">Como identificar os recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="5bbfe-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="5bbfe-p108">Um requisito comum para administradores está criando uma lista de todos os recursos que foram compartilhados com usuários fora da organização. Usando o compartilhamento auditorias no Office 365, os administradores agora podem gerar nessa lista. Aqui está como.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="5bbfe-143">Etapa 1: Pesquisar eventos de compartilhamento e exportar os resultados para um arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="5bbfe-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="5bbfe-p109">A primeira etapa é pesquisar o log de auditoria do Office 365 para o compartilhamento de eventos. Para obter mais detalhes (incluindo as permissões necessárias) sobre como pesquisar no log de auditoria, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="5bbfe-146">Vá para [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="5bbfe-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="5bbfe-147">Entrar no Office 365 usando sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="5bbfe-148">No painel à esquerda da segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação**e clique em **pesquisa de log de auditoria**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="5bbfe-149">A página de **pesquisa de log de auditoria** é exibida.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="5bbfe-150">Em **atividades**, clique em **atividades de compartilhamento** para pesquisar somente para compartilhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Em atividades, selecione atividades de compartilhamento](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="5bbfe-152">Selecione um intervalo de data e hora para encontrar os eventos de compartilhamento que ocorreram nesse período.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="5bbfe-153">Clique em **pesquisa** para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="5bbfe-154">Quando terminar a pesquisa em execução e os resultados são exibidos, clique em **exportar os resultados da** \> **Baixe todos os resultados**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="5bbfe-155">Depois de selecionar a opção Exportar, uma mensagem é exibida na parte inferior da janela solicitando que você abrir ou salvar o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="5bbfe-156">Clique em **Salvar** \> **Salvar como** e salve o arquivo CSV para uma pasta no computador local.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="5bbfe-157">Etapa 2: Filtrar o arquivo CSV para recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="5bbfe-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="5bbfe-p110">A próxima etapa é para filtrar o CSV para os eventos **SharingSet** e **SharingInvitationCreated** e para exibir os eventos cuja propriedade **TargetUserOrGroupType** for **Convidado**. Você usará o recurso de consulta de energia no Excel para fazer isso. O procedimento a seguir é executado no Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="5bbfe-161">No Excel 2016, abra uma pasta de trabalho em branco.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="5bbfe-162">Clique na guia **Dados**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="5bbfe-163">Clique em **Nova consulta** \> **de arquivo** \> **De CSV**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Na guia dados, selecione nova consulta, selecione o arquivo e selecione de CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="5bbfe-165">Abra o arquivo CSV que você baixou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="5bbfe-p111">O arquivo CSV é aberto no Editor de consulta. Observe que não existem quatro colunas: **tempo**, **usuário**, **ação**e **detalhes**. A coluna de **detalhes** é um campo de propriedade múltiplos. A próxima etapa é criar uma nova coluna para cada uma das propriedades na coluna **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="5bbfe-170">Selecione a coluna de **detalhes** e, em seguida, na guia **página inicial** , clique em **Coluna dividida** \> **Pelo delimitador**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Na guia página inicial, clique em coluna dividida e, em seguida, clique em por delimitador](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="5bbfe-172">Na janela de **Coluna dividida por delimitador** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5bbfe-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="5bbfe-173">Em **Selecionar ou digitar delimitador**, selecione **por vírgulas**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="5bbfe-174">Em **divisão**, selecione **em cada ocorrência do delimitador**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="5bbfe-175">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-175">Click **OK**.</span></span>
    
    <span data-ttu-id="5bbfe-p112">A coluna de **detalhes** é dividida em várias colunas. Cada nova coluna é nomeada **Detail.1**, **Detail.2**, **Detail.3**e assim por diante. Você perceberá que os valores em cada célula nas colunas **Detail.n** são prefixados com o nome da propriedade; Por exemplo, **Operação: SharingSet**, **Operação: SharingInvitationAccepted**e **Operação: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![A coluna de detalhes é dividida em várias colunas, um para cada propriedade](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="5bbfe-180">Na guia **arquivo** , clique em **Fechar &amp; carga** feche o Editor de consulta e abra o arquivo em uma pasta de trabalho do Excel.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="5bbfe-181">A próxima etapa é filtrar o arquivo para exibir somente os eventos **SharingSet** e **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="5bbfe-182">Vá para a guia **página inicial** e selecione a coluna **ação** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="5bbfe-183">No **Classificar &amp; filtro** lista suspensa, limpar todas as seleções, em seguida, selecione **SharingSet** e **SharingInvitationCreated**e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="5bbfe-184">Excel exibe as linhas para os eventos **SharingSet** e **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="5bbfe-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="5bbfe-185">Vá para a coluna nomeada **Detail.17** (ou que julgar coluna contém a propriedade **TargetUserOrGroupType** ) e selecioná-la.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="5bbfe-186">No **Classificar &amp; filtro** lista suspensa, limpar todas as seleções, em seguida, selecione **TargetUserOrGroupType:Guest**e clique **Okey**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="5bbfe-187">Agora Excel exibe as linhas para eventos **SharingInvitationCreated** e **SharingSet** e onde o usuário de destino está fora da sua organização, pois os usuários externos são identificados pelo valor **TargetUserOrGroupType:Guest**.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="5bbfe-188">A tabela a seguir mostra todos os usuários da organização que recursos compartilhados com um usuário convidado dentro de um intervalo de datas especificado.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Log de auditoria de eventos de compartilhamento no Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="5bbfe-190">Embora ele não está incluído na tabela anterior, a coluna **Detail.10** (ou que julgar coluna contém a propriedade **ObjectId** ) identifica o recurso que foi compartilhado com o usuário de destino; Por exemplo `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="5bbfe-191">Se você quiser identificar quando um usuário convidado foi realmente atribuído permissões para acessar um recurso (e não apenas os recursos que where compartilhados com eles), repita as etapas 10, 11 e 12 e filtrar os **SharingInvitationAccepted** e **SharingSet **eventos na etapa 10.</span><span class="sxs-lookup"><span data-stu-id="5bbfe-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
