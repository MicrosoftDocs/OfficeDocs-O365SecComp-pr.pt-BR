---
title: Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Aplicativos de OAuth na segurança de aplicativo de nuvem do Office 365 ajudarão-lo a gerenciar os aplicativos que seus usuários baixem para uso com dados do Office 365
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603682"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="b6f8c-103">Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b6f8c-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="b6f8c-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b6f8c-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b6f8c-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b6f8c-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b6f8c-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b6f8c-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b6f8c-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b6f8c-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b6f8c-108">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="b6f8c-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b6f8c-109">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="b6f8c-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="b6f8c-110">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="b6f8c-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="b6f8c-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="b6f8c-111">You are here!</span></span>  <br/> [<span data-ttu-id="b6f8c-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b6f8c-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="b6f8c-p101">Pessoas amor apps e eles baixá-las com frequência, especialmente os aplicativos que as pessoas utilizam pense salvará tempo, facilitando a obter no trabalho ou escola informações. No entanto, alguns aplicativos potencialmente poderia ser um risco de segurança para sua organização, dependendo de quais informações eles acessarem e como eles lidam com essas informações. Com a [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md), se você for um administrador global ou de segurança, você pode gerenciar aplicativos de OAuth para sua organização. Você pode ver as pessoas de aplicativos estão usando com dados do Office 365, que permissões estes aplicativos tem e muito mais.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="b6f8c-117">Este artigo descreve como criar uma consulta de aplicativo, como aprovar, proibir ou informar sobre um aplicativo e aonde ir para gerenciar aplicativos de OAuth.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="b6f8c-118">Como encontrar a página Gerenciar OAuth aplicativos</span><span class="sxs-lookup"><span data-stu-id="b6f8c-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="b6f8c-p102">Aplicativos do OAuth são gerenciados no portal de segurança de aplicativo de nuvem do Office 365. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="b6f8c-122">Vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="b6f8c-123">Escolha a **investigar** \> **OAuth apps**.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="b6f8c-124">![No portal do O365 CAS, escolha investigar.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="b6f8c-125">O que você verá na página Gerenciar OAuth aplicativos</span><span class="sxs-lookup"><span data-stu-id="b6f8c-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="b6f8c-126">A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar OAuth aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="b6f8c-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="b6f8c-127">**Item**</span></span>|<span data-ttu-id="b6f8c-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b6f8c-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6f8c-129">Ícone básica na barra de aplicativos de consulta</span><span class="sxs-lookup"><span data-stu-id="b6f8c-129">Basic icon in the app query bar</span></span>  <br/> ![Ícone que indica o modo de exibição de consulta básica para consultar](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="b6f8c-131">Selecione essa opção para alternar para o modo de exibição avançado.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="b6f8c-132">(Se você vir **básica**, você está usando o modo de exibição avançado)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="b6f8c-133">Ícone Avançado na barra de aplicativos de consulta</span><span class="sxs-lookup"><span data-stu-id="b6f8c-133">Advanced icon in the app query bar</span></span>  <br/> ![Ícone que indica o modo de exibição de consulta avançada para consultar](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="b6f8c-135">Selecione essa opção para alternar para modo de exibição básico.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="b6f8c-136">(Se você vir **Avançado**, você está usando o modo de exibição básico.)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="b6f8c-137">Abrir ou fechar o ícone de todos os detalhes na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b6f8c-137">Open or close all details icon in the app list</span></span>  <br/> ![Clique nesse ícone para abrir ou fechar todos os detalhes para todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="b6f8c-139">Selecione esse ícone para exibir mais ou menos detalhes sobre cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="b6f8c-140">Ícone de exportar na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b6f8c-140">Export icon in the app list</span></span>  <br/> ![Clique nesse ícone para exportar um arquivo csv de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="b6f8c-142">Selecione esse ícone para exportar um arquivo CSV que contém uma lista de aplicativos, o número de usuários para cada aplicativo, permissões associadas com o aplicativo, o nível de permissões, estado do aplicativo e usar nível de comunidade.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="b6f8c-143">Nome</span><span class="sxs-lookup"><span data-stu-id="b6f8c-143">Name</span></span>  <br/> |<span data-ttu-id="b6f8c-p103">Usar esse recurso para ver o nome de um App. Selecione o nome para exibir mais informações, como seu descrição, o publisher, o site da Web app e o ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="b6f8c-146">Autorizado pelo</span><span class="sxs-lookup"><span data-stu-id="b6f8c-146">Authorized by</span></span>  <br/> |<span data-ttu-id="b6f8c-p104">Use esta opção para ver quantos usuários tenham autorizados a um aplicativo para acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="b6f8c-149">Nível de permissões</span><span class="sxs-lookup"><span data-stu-id="b6f8c-149">Permissions Level</span></span>  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="b6f8c-p105">Use esta opção para ver quanto acesso um aplicativo tem aos dados do Office 365. Níveis de permissões indicam **baixa**, **média**ou **alta**, onde **baixa** pode indicar que o aplicativo acessa somente perfil e o nome de um usuário. Selecione o nível para exibir mais informações, como permissões concedidas para o aplicativo, o uso da comunidade e atividade relacionada no [log de governança](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="b6f8c-154">Última autorizados</span><span class="sxs-lookup"><span data-stu-id="b6f8c-154">Last authorized</span></span> <br/> |<span data-ttu-id="b6f8c-155">Use esta opção para ver a data e hora de que um aplicativo de OAuth última foi autorizado para acessar dados do Office 365 da sua organização.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="b6f8c-156">Ações</span><span class="sxs-lookup"><span data-stu-id="b6f8c-156">Actions</span></span><br/>![Aplicativos do OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="b6f8c-158">Use esta opção para ver ou para marcar um aplicativo como aprovado ou Banned, um aplicativo do OAuth do relatório para a Microsoft ou deixá-lo como indeterminado.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="b6f8c-159">Marcar um aplicativo como aprovados</span><span class="sxs-lookup"><span data-stu-id="b6f8c-159">Mark an app as approved</span></span>

<span data-ttu-id="b6f8c-160">Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja aprovar e escolha o ícone **app marca como aprovado** .</span><span class="sxs-lookup"><span data-stu-id="b6f8c-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Escolha o aplicativo de marca como ícone aprovado](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="b6f8c-162">O ícone fica verde, e o aplicativo em particular for aprovado para todos os usuários do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b6f8c-p106">Quando você marca um aplicativo como aprovados, não há nenhum efeito sobre o usuário final. Marcação visualmente os aplicativos que foram aprovados ajuda a separá-los dos aplicativos que ainda não foram revisados ainda.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="b6f8c-165">Proibir um aplicativo</span><span class="sxs-lookup"><span data-stu-id="b6f8c-165">Ban an app</span></span>

1. <span data-ttu-id="b6f8c-166">Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja proibir e escolha o ícone **app marca como proibidos** .</span><span class="sxs-lookup"><span data-stu-id="b6f8c-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="b6f8c-167">![Escolha o aplicativo de marca como ícone proibido](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="b6f8c-p107">Na caixa de mensagem de notificação, mantenha o texto existente como está ou personalizar o texto. Escolha se deseja que os usuários saibam o que foi proibido seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="b6f8c-171">Escolha **aplicativo proibir**.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="b6f8c-172">Reportar um aplicativo do OAuth para a Microsoft</span><span class="sxs-lookup"><span data-stu-id="b6f8c-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="b6f8c-173">Se você deseja enviar um aplicativo do OAuth para a Microsoft para análise, é possível denunciar desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="b6f8c-174">Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja enviar para análise.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="b6f8c-175">Escolha as reticências vertical e, em seguida, escolha **relatório App...**.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="b6f8c-176">![Informar sobre um aplicativo OAuth](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="b6f8c-p108">Na caixa de diálogo **deste aplicativo de relatório** , use a lista suspensa para indicar sua preocupação. Por padrão, **Este aplicativo é mal-intencionado** está selecionada. No entanto, você pode escolher em uma das outras opções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="b6f8c-180">![Informar sobre um aplicativo OAuth](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="b6f8c-181">(Recomendado) Mantenha a opção para contatá-lo selecionado e o endereço de email listado confirmar (ou editar).</span><span class="sxs-lookup"><span data-stu-id="b6f8c-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="b6f8c-182">Escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="b6f8c-183">Criar uma consulta de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b6f8c-183">Create an app query</span></span>

<span data-ttu-id="b6f8c-184">É recomendável usar o modo de exibição avançado, tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="b6f8c-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Modo de exibição avançado](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="b6f8c-p109">Na barra de consulta do aplicativo, se você vir **Avançado**, você está usando o modo de exibição básico. Clique (ou toque) **Avançado** para ir para o modo de exibição avançado.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Exibição básica](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="b6f8c-189">Na barra de consulta, use a lista **Selecionar um filtro** para escolher uma opção.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="b6f8c-190">**App** Aplicativos com determinados nomes</span><span class="sxs-lookup"><span data-stu-id="b6f8c-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="b6f8c-191">**Estado do aplicativo** Aplicativos com base em seu estado (aprovado, Banned ou Undetermined)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="b6f8c-192">**Use da comunidade** Aplicativos com base na comunidade usam níveis (Rare, Uncommon ou comum)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="b6f8c-193">**Nível de permissão** Aplicativos com base em determinados níveis de permissão</span><span class="sxs-lookup"><span data-stu-id="b6f8c-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="b6f8c-194">**Permissões** Aplicativos que necessitam de determinadas permissões</span><span class="sxs-lookup"><span data-stu-id="b6f8c-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="b6f8c-195">**Publisher**  Aplicativos de determinados fornecedores</span><span class="sxs-lookup"><span data-stu-id="b6f8c-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="b6f8c-196">**Usuário** Aplicativos que um determinado usuário autorizado</span><span class="sxs-lookup"><span data-stu-id="b6f8c-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="b6f8c-197">Selecione **é igual a** ou **diferente**e, em seguida, especifique um valor para o filtro.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="b6f8c-198">Para adicionar mais filtros, selecione o (sinal de adição</span><span class="sxs-lookup"><span data-stu-id="b6f8c-198">To add more filters, select the plus sign (</span></span>![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="b6f8c-200">) e repita as etapas 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="b6f8c-201">Para remover um filtro, selecione o x (</span><span class="sxs-lookup"><span data-stu-id="b6f8c-201">To remove a filter, select the x (</span></span>![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="b6f8c-203">) ao lado do nome de um filtro.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-203">) next to a filter name.</span></span>
    
<span data-ttu-id="b6f8c-204">Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="b6f8c-205">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b6f8c-205">Next steps</span></span>

- [<span data-ttu-id="b6f8c-206">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="b6f8c-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="b6f8c-207">Revise seus [logs de tráfego da Web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="b6f8c-208">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="b6f8c-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

