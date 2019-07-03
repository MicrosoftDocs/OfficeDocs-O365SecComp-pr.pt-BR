---
title: Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
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
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435231"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="7fe64-104">Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="7fe64-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="7fe64-105">O compartilhamento é uma atividade importante no SharePoint Online e no OneDrive for Business e é amplamente usado nas organizações do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fe64-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="7fe64-106">Agora, os administradores podem usar a auditoria de compartilhamento no log de auditoria do Office 365 para determinar como o compartilhamento está sendo usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="7fe64-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="7fe64-107">O esquema de compartilhamento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="7fe64-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="7fe64-108">Eventos de compartilhamento (exceto o compartilhamento de política e eventos de link de compartilhamento) são diferentes dos eventos relacionados a arquivos e pastas de uma maneira principal: um usuário está executando uma ação que tem algum efeito sobre outro usuário.</span><span class="sxs-lookup"><span data-stu-id="7fe64-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="7fe64-109">Por exemplo, o usuário A fornece ao usuário B acesso a um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7fe64-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="7fe64-110">Neste exemplo, o usuário A é o *usuário* que está agindo e o usuário B é o *usuário de destino*.</span><span class="sxs-lookup"><span data-stu-id="7fe64-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="7fe64-111">No esquema de arquivos do SharePoint, a ação do usuário que está agindo só afeta o próprio arquivo.</span><span class="sxs-lookup"><span data-stu-id="7fe64-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="7fe64-112">Quando o usuário A abre um arquivo, as únicas informações necessárias no \*\*\*\* evento fileaccessed são o usuário que está agindo.</span><span class="sxs-lookup"><span data-stu-id="7fe64-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="7fe64-113">Para resolver essa diferença, há um esquema separado, chamado esquema de *compartilhamento do SharePoint*, que captura mais informações sobre o compartilhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="7fe64-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="7fe64-114">Isso garante que os administradores tenham mais informações sobre quem compartilhou um recurso e o usuário com o qual o recurso foi compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7fe64-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="7fe64-115">O esquema de compartilhamento fornece dois campos adicionais no log de auditoria relacionado aos eventos de compartilhamento:</span><span class="sxs-lookup"><span data-stu-id="7fe64-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="7fe64-116">**TargetUserOrGroupName** – armazena o UPN ou o nome do usuário ou grupo de destino com o qual um recurso foi compartilhado (usuário B no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="7fe64-116">**TargetUserOrGroupName** – Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="7fe64-117">**TargetUserOrGroupType** – identifica se o usuário ou grupo de destino é um membro, convidado, grupo ou parceiro.</span><span class="sxs-lookup"><span data-stu-id="7fe64-117">**TargetUserOrGroupType** – Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="7fe64-118">Esses dois campos, além de outras propriedades do esquema de log de auditoria do Office 365, como User, Operation e Date, podem informar a história completa sobre *qual* usuário compartilhou *o* recurso com *quem* e *quando*.</span><span class="sxs-lookup"><span data-stu-id="7fe64-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="7fe64-119">Há outra propriedade de esquema que é importante para o texto de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fe64-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="7fe64-120">A propriedade **EVENTDATA** armazena informações adicionais sobre o compartilhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="7fe64-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="7fe64-121">Por exemplo, quando um usuário compartilha um site com outro usuário, isso é feito adicionando-se o usuário de destino a um grupo do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7fe64-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="7fe64-122">A propriedade **EVENTDATA** captura essas informações adicionais para fornecer contexto para administradores.</span><span class="sxs-lookup"><span data-stu-id="7fe64-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="7fe64-123">O modelo de compartilhamento do SharePoint e eventos de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="7fe64-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="7fe64-124">O compartilhamento é definido por três eventos separados \*\*\*\*: sharingset, **SharingInvitationCreated**e **SharingInvitaitonAccepted**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-124">Sharing is defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="7fe64-125">Este é o fluxo de trabalho para como o compartilhamento de eventos é registrado no log de auditoria do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fe64-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Fluxograma de como o compartilhamento de auditoria funciona](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="7fe64-127">Quando um usuário (o usuário agindo) deseja compartilhar um recurso com outro usuário (o usuário de destino), o SharePoint (ou o OneDrive for Business) primeiro verifica se o endereço de email do usuário de destino já está associado a uma conta de usuário no diretório da organização.</span><span class="sxs-lookup"><span data-stu-id="7fe64-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="7fe64-128">Se o usuário de destino estiver no diretório da organização, o SharePoint fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7fe64-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="7fe64-129">Atribui imediatamente as permissões de usuário de destino para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe64-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="7fe64-130">Envia uma notificação de compartilhamento para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="7fe64-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="7fe64-131">Registra um \*\*\*\* evento sharingset.</span><span class="sxs-lookup"><span data-stu-id="7fe64-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="7fe64-132">Se uma conta de usuário para o usuário de destino não estiver no diretório da organização, o SharePoint fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7fe64-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="7fe64-133">Cria um convite de compartilhamento e o envia para o endereço de email do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="7fe64-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="7fe64-134">Registra um evento **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="7fe64-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="7fe64-135">O evento **SharingInvitationCreated** é sempre associado ao compartilhamento de convidados ou externo quando o usuário de destino não tem acesso ao recurso que foi compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7fe64-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="7fe64-136">Quando o usuário de destino aceita o convite de compartilhamento que é enviado a eles (clicando no link no convite), o SharePoint registra um evento **SharingInvitationAccepted** e atribui as permissões de usuário de destino para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe64-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="7fe64-137">Informações adicionais sobre o usuário de destino também são registradas, como a identidade do usuário para o qual o convite foi enviado e o usuário que aceitou o convite.</span><span class="sxs-lookup"><span data-stu-id="7fe64-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="7fe64-138">Em alguns casos, esses usuários (ou endereços de email) podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="7fe64-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="7fe64-139">Como identificar recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="7fe64-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="7fe64-140">Um requisito comum para administradores é criar uma lista de todos os recursos que foram compartilhados com usuários fora da organização.</span><span class="sxs-lookup"><span data-stu-id="7fe64-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="7fe64-141">Usando a auditoria de compartilhamento no Office 365, os administradores agora podem gerar essa lista.</span><span class="sxs-lookup"><span data-stu-id="7fe64-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="7fe64-142">Veja como.</span><span class="sxs-lookup"><span data-stu-id="7fe64-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="7fe64-143">Etapa 1: Pesquisar eventos de compartilhamento e exportar os resultados para um arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="7fe64-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="7fe64-144">A primeira etapa é Pesquisar o log de auditoria do Office 365 para eventos de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fe64-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="7fe64-145">Para obter mais informações (incluindo as permissões necessárias) sobre pesquisa no log de auditoria, consulte [Pesquisar o log de auditoria no centro de conformidade de & de segurança](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="7fe64-145">For more information (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="7fe64-146">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7fe64-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7fe64-147">Entre no Office 365 usando a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="7fe64-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="7fe64-148">No painel esquerdo do centro de conformidade & segurança, clique em \*\*\*\*  > **pesquisa de log de auditoria**de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fe64-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="7fe64-149">A página **pesquisa de log de auditoria** é exibida.</span><span class="sxs-lookup"><span data-stu-id="7fe64-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="7fe64-150">Em **atividades**, clique em **compartilhar e acessar as atividades de solicitação** para pesquisar eventos relacionados ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fe64-150">Under **Activities**, click **Sharing and access request activities** to search for sharing-related events.</span></span> 
    
    ![Em atividades, selecione compartilhar e acessar atividades de solicitação](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="7fe64-152">Selecione um intervalo de data e hora para localizar os eventos de compartilhamento que ocorreram dentro desse período.</span><span class="sxs-lookup"><span data-stu-id="7fe64-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="7fe64-153">Clique em **Pesquisar** para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fe64-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="7fe64-154">Quando a pesquisa é concluída e os resultados são exibidos, clique em **Exportar resultados** \> **baixar todos os resultados**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-154">When the search is finished running and the results are displayed, click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="7fe64-155">Depois que você selecionar a opção Exportar, uma mensagem será exibida na parte inferior da janela que solicitará que você abra ou salve o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="7fe64-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="7fe64-156">Clique em **salvar** \> **salvar como** e salve o arquivo CSV em uma pasta no computador local.</span><span class="sxs-lookup"><span data-stu-id="7fe64-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="7fe64-157">Etapa 2: filtrar o arquivo CSV para recursos compartilhados com usuários externos</span><span class="sxs-lookup"><span data-stu-id="7fe64-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="7fe64-158">A próxima etapa é filtrar o CSV para os eventos **sharingset** e **SharingInvitationCreated** e exibir os eventos em que a propriedade **TargetUserOrGroupType** é **Guest**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="7fe64-159">Use a ferramenta Editor de consulta de alimentação no Excel para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7fe64-159">You use the Power Query Editor tool in Excel to do this.</span></span> <span data-ttu-id="7fe64-160">Para obter instruções detalhadas, consulte [Export, configure e View Audit Log Records](export-view-audit-log-records.md).</span><span class="sxs-lookup"><span data-stu-id="7fe64-160">For step-by-step instructions, see [Export, configure, and view audit log records](export-view-audit-log-records.md).</span></span> 

<span data-ttu-id="7fe64-161">Após seguir as instruções no tópico anterior para preparar o arquivo CSV, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7fe64-161">After you've followed the instructions in the previous topic to prepare the CSV file, do the following:</span></span>
    
1. <span data-ttu-id="7fe64-162">Abra o arquivo CSV que você preparou com o editor de consulta de energia.</span><span class="sxs-lookup"><span data-stu-id="7fe64-162">Open the CSV file that you prepared with the Power Query Editor.</span></span> 

2. <span data-ttu-id="7fe64-163">Na guia **página inicial** , clique em **classificar & filtro**e, em seguida, clique em **Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-163">On the **Home** tab, click **Sort & Filter**, and then click **Filter**.</span></span>
    
3. <span data-ttu-id="7fe64-164">Na lista suspensa **classificar & filtro** na coluna **operações** , desmarque todas as seleções e, em seguida, selecione **compartilhamento** e **SharingInvitationCreated**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-164">In the **Sort & Filter** dropdown list on the **Operations** column, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="7fe64-165">O Excel exibe as linhas dos \*\*\*\* eventos sharingset e **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="7fe64-165">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
4. <span data-ttu-id="7fe64-166">Vá até a coluna chamada **TargetUserOrGroupType** e selecione-a.</span><span class="sxs-lookup"><span data-stu-id="7fe64-166">Go to the column named **TargetUserOrGroupType** and select it.</span></span> 
    
5. <span data-ttu-id="7fe64-167">Na lista suspensa **classificar & filtro** , desmarque todas as seleções e, em seguida, selecione **TargetUserOrGroupType: convidado**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-167">In the **Sort & Filter** dropdown list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="7fe64-168">Agora o Excel exibe as linhas dos eventos **SharingInvitationCreated** e **sharingset** e onde o usuário de destino está fora da sua organização, pois os usuários externos são identificados pelo valor **TargetUserOrGroupType: Guest**.</span><span class="sxs-lookup"><span data-stu-id="7fe64-168">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="7fe64-169">A tabela a seguir mostra todos os usuários da organização que compartilharam recursos com um usuário convidado em um intervalo de datas especificado.</span><span class="sxs-lookup"><span data-stu-id="7fe64-169">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Compartilhando eventos no log de auditoria do Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="7fe64-171">Embora não esteja incluído na tabela anterior, a propriedade **ObjectID** identifica o recurso que foi compartilhado com o usuário de destino; por exemplo `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="7fe64-171">Although it's not included in the previous table, the **ObjectId** property identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="7fe64-172">Se você deseja identificar quando um usuário convidado foi realmente atribuído a permissões para acessar um recurso (em vez de apenas os recursos que foram compartilhados com eles), repita as etapas 2, 3 e 4 e filtre o **SharingInvitationAccepted** e o **sharingset** eventos na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="7fe64-172">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 2, 3, and 4, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 5.</span></span> 
