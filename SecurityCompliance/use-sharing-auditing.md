---
title: Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'O compartilhamento é uma atividade importante no SharePoint Online e no OneDrive for Business. Agora, os administradores podem usar a auditoria de compartilhamento no log de auditoria do Office 365 para determinar como o compartilhamento está sendo usado em sua organização. '
ms.openlocfilehash: a363ebe2e8b1697521ab5f84df0b3fc221a2abcd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157893"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="45462-104">Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="45462-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="45462-105">O compartilhamento é uma atividade importante no SharePoint Online e no OneDrive for Business e é amplamente usado nas organizações do Office 365.</span><span class="sxs-lookup"><span data-stu-id="45462-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="45462-106">Agora, os administradores podem usar a auditoria de compartilhamento no log de auditoria do Office 365 para determinar como o compartilhamento está sendo usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="45462-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="45462-107">O esquema de compartilhamento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="45462-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="45462-108">Eventos de compartilhamento (exceto o compartilhamento de política e eventos de link de compartilhamento) são diferentes dos eventos relacionados a arquivos e pastas de uma maneira principal: um usuário está executando uma ação que tem algum efeito sobre outro usuário.</span><span class="sxs-lookup"><span data-stu-id="45462-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="45462-109">Por exemplo, o usuário A fornece ao usuário B acesso a um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45462-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="45462-110">Neste exemplo, o usuário A é o *usuário* que está agindo e o usuário B é o *usuário de destino*.</span><span class="sxs-lookup"><span data-stu-id="45462-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="45462-111">No esquema de arquivos do SharePoint, a ação do usuário que está agindo só afeta o próprio arquivo.</span><span class="sxs-lookup"><span data-stu-id="45462-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="45462-112">Quando o usuário A abre um arquivo, as únicas informações necessárias no \*\*\*\* evento fileaccessed são o usuário que está agindo.</span><span class="sxs-lookup"><span data-stu-id="45462-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="45462-113">Para resolver essa diferença, há um esquema separado, chamado esquema de *compartilhamento do SharePoint*, que captura mais informações sobre o compartilhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="45462-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="45462-114">Isso garante que os administradores tenham mais informações sobre quem compartilhou um recurso e o usuário com o qual o recurso foi compartilhado.</span><span class="sxs-lookup"><span data-stu-id="45462-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="45462-115">O esquema de compartilhamento fornece dois campos adicionais no log de auditoria relacionado aos eventos de compartilhamento:</span><span class="sxs-lookup"><span data-stu-id="45462-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="45462-116">**TargetUserOrGroupName** -armazena o UPN ou o nome do usuário ou grupo de destino com o qual um recurso foi compartilhado (usuário B no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="45462-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="45462-117">**TargetUserOrGroupType** -identifica se o usuário ou grupo de destino é um membro, convidado, grupo ou parceiro.</span><span class="sxs-lookup"><span data-stu-id="45462-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="45462-118">Esses dois campos, além de outras propriedades do esquema de log de auditoria do Office 365, como User, Operation e Date, podem informar a história completa sobre *qual* usuário compartilhou *o* recurso com *quem* e *quando*.</span><span class="sxs-lookup"><span data-stu-id="45462-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="45462-119">Há outra propriedade de esquema que é importante para o texto de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="45462-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="45462-120">A propriedade **EVENTDATA** armazena informações adicionais sobre o compartilhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="45462-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="45462-121">Por exemplo, quando um usuário compartilha um site com outro usuário, isso é feito adicionando-se o usuário de destino a um grupo do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="45462-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="45462-122">A propriedade **EVENTDATA** captura essas informações adicionais para fornecer contexto para administradores.</span><span class="sxs-lookup"><span data-stu-id="45462-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="45462-123">O modelo de compartilhamento do SharePoint e eventos de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="45462-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="45462-124">O compartilhamento é definido de fato por três eventos \*\*\*\* separados: compartilhando, **SharingInvitationCreated**e **SharingInvitaitonAccepted**.</span><span class="sxs-lookup"><span data-stu-id="45462-124">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="45462-125">Este é o fluxo de trabalho para como o compartilhamento de eventos é registrado no log de auditoria do Office 365.</span><span class="sxs-lookup"><span data-stu-id="45462-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Fluxograma de como o compartilhamento de auditoria funciona](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="45462-127">Quando um usuário (o usuário agindo) deseja compartilhar um recurso com outro usuário (o usuário de destino), o SharePoint (ou o OneDrive for Business) primeiro verifica se o endereço de email do usuário de destino já está associado a uma conta de usuário no diretório da organização.</span><span class="sxs-lookup"><span data-stu-id="45462-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="45462-128">Se o usuário de destino estiver no diretório da organização, o SharePoint fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="45462-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="45462-129">Atribui imediatamente as permissões de usuário de destino para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="45462-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="45462-130">Envia uma notificação de compartilhamento para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="45462-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="45462-131">Registra um \*\*\*\* evento sharingset.</span><span class="sxs-lookup"><span data-stu-id="45462-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="45462-132">Se uma conta de usuário para o usuário de destino não estiver no diretório da organização, o SharePoint fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="45462-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="45462-133">Cria um convite de compartilhamento e o envia para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="45462-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="45462-134">Registra um evento **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="45462-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="45462-135">O evento **SharingInvitationCreated** é sempre associado ao compartilhamento de convidados ou externo quando o usuário de destino não tem acesso ao recurso que foi compartilhado.</span><span class="sxs-lookup"><span data-stu-id="45462-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="45462-136">Quando o usuário de destino aceita o convite de compartilhamento que é enviado a eles (clicando no link no convite), o SharePoint registra um evento **SharingInvitationAccepted** e atribui as permissões de usuário de destino para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="45462-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="45462-137">Informações adicionais sobre o usuário de destino também são registradas, como a identidade do usuário para o qual o convite foi enviado e o usuário que aceitou o convite.</span><span class="sxs-lookup"><span data-stu-id="45462-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="45462-138">Em alguns casos, esses usuários (ou endereços de email) podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="45462-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="45462-139">Como identificar recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="45462-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="45462-140">Um requisito comum para administradores é criar uma lista de todos os recursos que foram compartilhados com usuários fora da organização.</span><span class="sxs-lookup"><span data-stu-id="45462-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="45462-141">Usando a auditoria de compartilhamento no Office 365, os administradores agora podem gerar essa lista.</span><span class="sxs-lookup"><span data-stu-id="45462-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="45462-142">Veja como.</span><span class="sxs-lookup"><span data-stu-id="45462-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="45462-143">Etapa 1: Pesquisar eventos de compartilhamento e exportar os resultados para um arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="45462-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="45462-144">A primeira etapa é Pesquisar o log de auditoria do Office 365 para eventos de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="45462-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="45462-145">Para obter mais detalhes (incluindo as permissões necessárias) sobre pesquisa no log de auditoria, consulte [Search the Audit Log in the Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="45462-145">For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="45462-146">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="45462-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="45462-147">Entre no Office 365 usando a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="45462-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="45462-148">No painel esquerdo do centro de conformidade do & de segurança, clique em**pesquisa de log de auditoria**de **pesquisa**  > .</span><span class="sxs-lookup"><span data-stu-id="45462-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="45462-149">A página **pesquisa de log de auditoria** é exibida.</span><span class="sxs-lookup"><span data-stu-id="45462-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="45462-150">Em **atividades**, clique em **compartilhar atividades** para pesquisar somente eventos de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="45462-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Em atividades, selecione compartilhar atividades](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="45462-152">Selecione um intervalo de data e hora para localizar os eventos de compartilhamento que ocorreram dentro desse período.</span><span class="sxs-lookup"><span data-stu-id="45462-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="45462-153">Clique em **Pesquisar** para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="45462-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="45462-154">Quando a pesquisa é concluída e os resultados são exibidos, clique em **Exportar resultados** \> **baixar todos os resultados**.</span><span class="sxs-lookup"><span data-stu-id="45462-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="45462-155">Depois que você selecionar a opção Exportar, uma mensagem será exibida na parte inferior da janela que solicitará que você abra ou salve o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="45462-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="45462-156">Clique em **salvar** \> **salvar como** e salve o arquivo CSV em uma pasta no computador local.</span><span class="sxs-lookup"><span data-stu-id="45462-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="45462-157">Etapa 2: filtrar o arquivo CSV para recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="45462-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="45462-158">A próxima etapa é filtrar o CSV para os eventos **sharingset** e **SharingInvitationCreated** e exibir os eventos em que a propriedade **TargetUserOrGroupType** é **Guest**.</span><span class="sxs-lookup"><span data-stu-id="45462-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="45462-159">Você usará o recurso de consulta de energia no Excel para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="45462-159">You'll use the Power Query feature in Excel to do this.</span></span> <span data-ttu-id="45462-160">O procedimento a seguir é executado no Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="45462-160">The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="45462-161">No Excel 2016, abra uma pasta de trabalho em branco.</span><span class="sxs-lookup"><span data-stu-id="45462-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="45462-162">Clique na guia **dados** .</span><span class="sxs-lookup"><span data-stu-id="45462-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="45462-163">Clique em **nova consulta** \> **de arquivo** \> **de CSV**.</span><span class="sxs-lookup"><span data-stu-id="45462-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Na guia dados, selecione Nova consulta, selecione de arquivo e, em seguida, selecione do CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="45462-165">Abra o arquivo CSV que você baixou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="45462-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="45462-166">O arquivo CSV é aberto no editor de consultas.</span><span class="sxs-lookup"><span data-stu-id="45462-166">The CSV file is opened in the Query Editor.</span></span> <span data-ttu-id="45462-167">Observe que há quatro colunas: **hora**, **usuário**, **ação**e **detalhes**.</span><span class="sxs-lookup"><span data-stu-id="45462-167">Note that there are four columns: **Time**, **User**, **Action**, and **Detail**.</span></span> <span data-ttu-id="45462-168">A coluna de **detalhes** é um campo de várias propriedades.</span><span class="sxs-lookup"><span data-stu-id="45462-168">The **Detail** column is a multi-property field.</span></span> <span data-ttu-id="45462-169">A próxima etapa é criar uma nova coluna para cada uma das propriedades na coluna **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="45462-169">The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="45462-170">Selecione a coluna **detalhes** e, na guia **página inicial** , clique em **dividir coluna** \> **por**delimitador.</span><span class="sxs-lookup"><span data-stu-id="45462-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Na guia página inicial, clique em dividir coluna e, em seguida, clique em por delimitador](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="45462-172">Na janela **dividir coluna por** delimitador, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="45462-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="45462-173">Em **selecionar ou inserir**delimitador, selecione **vírgula**.</span><span class="sxs-lookup"><span data-stu-id="45462-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="45462-174">Em **dividir**, selecione **em cada ocorrência do**delimitador.</span><span class="sxs-lookup"><span data-stu-id="45462-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="45462-175">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="45462-175">Click **OK**.</span></span>
    
    <span data-ttu-id="45462-176">A coluna de **detalhes** é dividida em várias colunas.</span><span class="sxs-lookup"><span data-stu-id="45462-176">The **Detail** column is split into multiple columns.</span></span> <span data-ttu-id="45462-177">Cada nova coluna é denominada **detail. 1**, **detail. 2**, **detail. 3**e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="45462-177">Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on.</span></span> <span data-ttu-id="45462-178">Você notará que os valores em cada célula das colunas **detail. n** são prefixados com o nome da propriedade; por exemplo, **operação: sharingset**, **Operation: SharingInvitationAccepted**e **Operation: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="45462-178">You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![A coluna de detalhes é dividida em várias colunas, uma para cada propriedade](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="45462-180">Na guia **arquivo** , clique em **fechar &amp; carregamento** para fechar o editor de consultas e abrir o arquivo em uma pasta de trabalho do Excel.</span><span class="sxs-lookup"><span data-stu-id="45462-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="45462-181">A próxima etapa é filtrar o arquivo para exibir apenas os eventos **sharingset** e **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="45462-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="45462-182">Vá para a guia **página inicial** e, em seguida, selecione a coluna **ação** .</span><span class="sxs-lookup"><span data-stu-id="45462-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="45462-183">Na lista **suspensa &amp; filtro de classificação** , desmarque todas as seleções e, em seguida, selecione compartilhamentos e **SharingInvitationCreated**e clique em **OK**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="45462-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="45462-184">O Excel exibe as linhas dos \*\*\*\* eventos sharingset e **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="45462-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="45462-185">Vá até a coluna chamada **detail. 17** (ou qualquer coluna que contenha a propriedade **TargetUserOrGroupType** ) e selecione-a.</span><span class="sxs-lookup"><span data-stu-id="45462-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="45462-186">Na lista **suspensa &amp; filtro de classificação** , desmarque todas as seleções e, em seguida, selecione **TargetUserOrGroupType: convidado**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="45462-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="45462-187">Agora o Excel exibe as linhas dos eventos **SharingInvitationCreated** e **sharingset** e onde o usuário de destino está fora da sua organização, pois os usuários externos são identificados pelo valor **TargetUserOrGroupType: Guest**.</span><span class="sxs-lookup"><span data-stu-id="45462-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="45462-188">A tabela a seguir mostra todos os usuários da organização que compartilharam recursos com um usuário convidado em um intervalo de datas especificado.</span><span class="sxs-lookup"><span data-stu-id="45462-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Compartilhando eventos no log de auditoria do Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="45462-190">Embora não esteja incluído na tabela anterior, a coluna **detail. 10** (ou qualquer coluna contém a propriedade **ObjectID** ) identifica o recurso que foi compartilhado com o usuário de destino; por exemplo `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="45462-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="45462-191">Se você quiser identificar quando um usuário convidado foi realmente atribuído a permissões para acessar um recurso (em vez de apenas os recursos que foram compartilhados com eles), repita as etapas 10, 11 e 12 e filtre o **SharingInvitationAccepted** e o \*\*sharingset \*\*eventos na etapa 10.</span><span class="sxs-lookup"><span data-stu-id="45462-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
