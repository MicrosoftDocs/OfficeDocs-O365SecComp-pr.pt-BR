---
title: Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Aplicativos OAuth no Office 365 Cloud app Security o ajudam a gerenciar os aplicativos que seus usuários baixam para uso com os dados do Office 365
ms.openlocfilehash: 510cb64f2267c99b783f86a69f7b7a84db8d84dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219821"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="6710c-103">Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="6710c-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="6710c-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6710c-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="6710c-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6710c-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="6710c-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6710c-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="6710c-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6710c-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="6710c-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="6710c-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="6710c-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="6710c-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="6710c-110">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="6710c-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="6710c-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="6710c-111">You are here!</span></span>  <br/> [<span data-ttu-id="6710c-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="6710c-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="6710c-p101">As pessoas adoram os aplicativos e os baixam com frequência, especialmente os aplicativos que as pessoas acham poupar tempo, facilitando a obtenção de suas informações de trabalho ou escola. No enTanto, alguns aplicativos podem ser um risco de segurança para sua organização, dependendo de quais informações eles acessam e como eles lidam com essas informações. Com o [Office 365 Cloud app Security](office-365-cas-overview.md), se você for um administrador de segurança ou global, você pode gerenciar aplicativos OAuth para sua organização. Você pode ver os aplicativos que as pessoas estão usando com dados do Office 365, quais permissões esses aplicativos têm e mais.</span><span class="sxs-lookup"><span data-stu-id="6710c-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="6710c-117">Este artigo descreve onde ir para gerenciar aplicativos OAuth, como aprovar, proibir ou relatar um aplicativo e como criar uma consulta de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6710c-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="6710c-118">Como localizar a página Gerenciar aplicativos OAuth</span><span class="sxs-lookup"><span data-stu-id="6710c-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="6710c-p102">Os aplicativos OAuth são gerenciados no portal do Office 365 Cloud app Security. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, confira [permissões no centro de &amp; conformidade de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6710c-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="6710c-122">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="6710c-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="6710c-123">Escolha **investigar** \> **aplicativos OAuth**.</span><span class="sxs-lookup"><span data-stu-id="6710c-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="6710c-124">![No portal do O365 CAS, escolha investigar.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="6710c-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="6710c-125">O que você verá na página Gerenciar aplicativos OAuth</span><span class="sxs-lookup"><span data-stu-id="6710c-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="6710c-126">A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar aplicativos OAuth.</span><span class="sxs-lookup"><span data-stu-id="6710c-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="6710c-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="6710c-127">**Item**</span></span>|<span data-ttu-id="6710c-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6710c-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6710c-129">Ícone básico na barra de consulta do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6710c-129">Basic icon in the app query bar</span></span>  <br/> ![Ícone que indica o modo de exibição de consulta básica para consulta](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="6710c-131">Selecione esta opção para mudar para o modo de exibição avançado.</span><span class="sxs-lookup"><span data-stu-id="6710c-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="6710c-132">(Se você vir **básico**, você está usando o modo de exibição avançado)</span><span class="sxs-lookup"><span data-stu-id="6710c-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="6710c-133">Ícone avançado na barra de consulta do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6710c-133">Advanced icon in the app query bar</span></span>  <br/> ![Ícone que indica o modo de exibição de consulta avançado para consulta](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="6710c-135">Selecione esta opção para alternar para o modo de exibição básico.</span><span class="sxs-lookup"><span data-stu-id="6710c-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="6710c-136">(Se você vir **avançado**, você está usando o modo de exibição básico.)</span><span class="sxs-lookup"><span data-stu-id="6710c-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="6710c-137">Abrir ou fechar todos os ícones de detalhes na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6710c-137">Open or close all details icon in the app list</span></span>  <br/> ![Clique neste ícone para abrir ou fechar todos os detalhes de todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="6710c-139">Selecione este ícone para exibir mais ou menos detalhes sobre cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6710c-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="6710c-140">Ícone exportar na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6710c-140">Export icon in the app list</span></span>  <br/> ![Clique neste ícone para exportar um arquivo CSV de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="6710c-142">Selecione este ícone para exportar um arquivo CSV que contém uma lista de aplicativos, número de usuários para cada aplicativo, permissões associadas ao aplicativo, nível de permissões, estado do aplicativo e nível de uso da Comunidade.</span><span class="sxs-lookup"><span data-stu-id="6710c-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="6710c-143">Nome</span><span class="sxs-lookup"><span data-stu-id="6710c-143">Name</span></span>  <br/> |<span data-ttu-id="6710c-p103">Use este para ver o nome de um aplicativo. Selecione o nome para exibir mais informações, como descrição, editor, site de aplicativo e ID de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6710c-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="6710c-146">Autorizado por</span><span class="sxs-lookup"><span data-stu-id="6710c-146">Authorized by</span></span>  <br/> |<span data-ttu-id="6710c-p104">Use esta para ver quantos usuários autorizaram um aplicativo a acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="6710c-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="6710c-149">Nível de permissões</span><span class="sxs-lookup"><span data-stu-id="6710c-149">Permissions Level</span></span>  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="6710c-p105">Use isso para ver quanto acesso um aplicativo tem aos dados do Office 365. Os níveis de permissão indicam **baixo**, **médio**ou **alto**, onde **baixo** pode indicar que o aplicativo acessa apenas o perfil e o nome do usuário. Selecione o nível para exibir mais informações, como permissões concedidas ao aplicativo, uso da Comunidade e atividade relacionada no log de [governança](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="6710c-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="6710c-154">Último autorizado</span><span class="sxs-lookup"><span data-stu-id="6710c-154">Last authorized</span></span> <br/> |<span data-ttu-id="6710c-155">Use isso para ver a data e a hora em que um aplicativo OAuth foi autorizado pela última vez a acessar os dados do Office 365 da sua organização.</span><span class="sxs-lookup"><span data-stu-id="6710c-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="6710c-156">Ações</span><span class="sxs-lookup"><span data-stu-id="6710c-156">Actions</span></span><br/>![Aplicativos OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="6710c-158">Use esta caixa para ver ou marcar um aplicativo como aprovado ou proibido, relatar um aplicativo OAuth para a Microsoft ou deixá-lo como indeterminado.</span><span class="sxs-lookup"><span data-stu-id="6710c-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="6710c-159">Marcar um aplicativo como aprovado</span><span class="sxs-lookup"><span data-stu-id="6710c-159">Mark an app as approved</span></span>

<span data-ttu-id="6710c-160">Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja aprovar e escolha o ícone **Marcar aplicativo como aprovado** .</span><span class="sxs-lookup"><span data-stu-id="6710c-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Escolha o ícone marcar aplicativo como aprovado](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="6710c-162">O ícone fica verde e o aplicativo é aprovado para todos os seus usuários do Office 365.</span><span class="sxs-lookup"><span data-stu-id="6710c-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6710c-p106">Quando você marca um aplicativo como aprovado, não há efeito no usuário final. Marcar visualmente os aplicativos que são aprovados ajuda a separá-los de aplicativos que ainda não foram revisados.</span><span class="sxs-lookup"><span data-stu-id="6710c-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="6710c-165">Proibir um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6710c-165">Ban an app</span></span>

1. <span data-ttu-id="6710c-166">Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja proibir e escolha o ícone **Marcar aplicativo como proibido** .</span><span class="sxs-lookup"><span data-stu-id="6710c-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="6710c-167">![Escolha o ícone marcar aplicativo como proibido](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="6710c-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="6710c-p107">Na caixa mensagem de notificação, mantenha o texto existente como está ou personalize o texto. Escolha se deseja permitir que os usuários saibam que seu aplicativo foi banido.</span><span class="sxs-lookup"><span data-stu-id="6710c-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="6710c-171">Escolha **proibir aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="6710c-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="6710c-172">Relatar um aplicativo OAuth para a Microsoft</span><span class="sxs-lookup"><span data-stu-id="6710c-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="6710c-173">Se você deseja enviar um aplicativo OAuth para a Microsoft para análise, é possível relatar esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6710c-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="6710c-174">Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja enviar para análise.</span><span class="sxs-lookup"><span data-stu-id="6710c-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="6710c-175">Escolha as reticências verticais e, em seguida, escolha **relatar aplicativo..**..</span><span class="sxs-lookup"><span data-stu-id="6710c-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="6710c-176">![Relatar um aplicativo OAuth](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="6710c-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="6710c-p108">Na caixa de diálogo **relatar este aplicativo** , use a lista suspensa para indicar sua preocupação. Por padrão, **este aplicativo é mal-intencionado** selecionado. No enTanto, você pode escolher uma das outras opções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6710c-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="6710c-180">![Relatar um aplicativo OAuth](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="6710c-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="6710c-181">Recomenda Mantenha a opção de contato selecionado e confirme (ou edite) o endereço de email listado.</span><span class="sxs-lookup"><span data-stu-id="6710c-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="6710c-182">Escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="6710c-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="6710c-183">Criar uma consulta de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6710c-183">Create an app query</span></span>

<span data-ttu-id="6710c-184">Recomendamos usar o modo de exibição avançado, que tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="6710c-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Modo de exibição avançado](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="6710c-p109">Na barra de consulta do aplicativo, se você vir **avançado**, você está usando o modo de exibição básico. Clique (ou toque) em **avançado** para ir para o modo de exibição avançado.</span><span class="sxs-lookup"><span data-stu-id="6710c-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Exibição básica](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="6710c-189">Na barra de consulta, use a lista **selecionar um filtro** para escolher uma opção.</span><span class="sxs-lookup"><span data-stu-id="6710c-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="6710c-190">**Aplicativo** Aplicativos com determinados nomes</span><span class="sxs-lookup"><span data-stu-id="6710c-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="6710c-191">**Estado do aplicativo** Aplicativos com base em seu estado (aprovado, proibido ou indeterminado)</span><span class="sxs-lookup"><span data-stu-id="6710c-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="6710c-192">**Uso da Comunidade** Aplicativos baseados em níveis de uso da Comunidade (raro, incomum ou comum)</span><span class="sxs-lookup"><span data-stu-id="6710c-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="6710c-193">**Nível de permissão** Aplicativos com base em determinados níveis de permissão</span><span class="sxs-lookup"><span data-stu-id="6710c-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="6710c-194">**Permissões** Aplicativos que exigem determinadas permissões</span><span class="sxs-lookup"><span data-stu-id="6710c-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="6710c-195">**Publisher**  Aplicativos de determinados editores</span><span class="sxs-lookup"><span data-stu-id="6710c-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="6710c-196">**Usuário** Aplicativos que um determinado usuário autorizou</span><span class="sxs-lookup"><span data-stu-id="6710c-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="6710c-197">Selecione **igual a** ou **diferente**de e especifique um valor para o filtro.</span><span class="sxs-lookup"><span data-stu-id="6710c-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="6710c-198">Para adicionar mais filtros, selecione o sinal de adição (</span><span class="sxs-lookup"><span data-stu-id="6710c-198">To add more filters, select the plus sign (</span></span>![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="6710c-200">) e repita as etapas 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="6710c-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="6710c-201">Para remover um filtro, selecione o x (</span><span class="sxs-lookup"><span data-stu-id="6710c-201">To remove a filter, select the x (</span></span>![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="6710c-203">) ao lado de um nome de filtro.</span><span class="sxs-lookup"><span data-stu-id="6710c-203">) next to a filter name.</span></span>
    
<span data-ttu-id="6710c-204">Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.</span><span class="sxs-lookup"><span data-stu-id="6710c-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="6710c-205">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="6710c-205">Next steps</span></span>

- [<span data-ttu-id="6710c-206">ReVisar e executar ação em alertas</span><span class="sxs-lookup"><span data-stu-id="6710c-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="6710c-207">Examinar seus [logs de tráfego da Web e fontes de dados para o Office 365 Cloud app Security](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="6710c-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="6710c-208">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="6710c-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

