---
title: Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Permissões do aplicativo na segurança de aplicativo de nuvem do Office 365 ajudarão-lo a gerenciar os aplicativos que seus usuários baixem para uso com dados do Office 365
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524446"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a><span data-ttu-id="f25c1-103">Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="f25c1-103">Manage app permissions using Office 365 Cloud App Security</span></span>

<span data-ttu-id="f25c1-104">Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f25c1-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="f25c1-105">Avaliação * *\>**</span><span class="sxs-lookup"><span data-stu-id="f25c1-105">****Evaluation** \>**</span></span>|<span data-ttu-id="f25c1-106">Planejamento * *\>**</span><span class="sxs-lookup"><span data-stu-id="f25c1-106">****Planning** \>**</span></span>|<span data-ttu-id="f25c1-107">Implantação * *\>**</span><span class="sxs-lookup"><span data-stu-id="f25c1-107">****Deployment** \>**</span></span>|<span data-ttu-id="f25c1-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f25c1-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="f25c1-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="f25c1-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="f25c1-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="f25c1-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="f25c1-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="f25c1-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="f25c1-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="f25c1-112">You are here!</span></span>  <br/> [<span data-ttu-id="f25c1-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f25c1-113">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="f25c1-p101">Pessoas amor apps e eles baixá-las com frequência, especialmente os aplicativos que as pessoas utilizam pense salvará tempo, facilitando a obter no trabalho ou escola informações. No entanto, alguns aplicativos potencialmente poderia ser um risco de segurança para sua organização, dependendo de quais informações eles acessarem e como eles lidam com essas informações. Com a [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md), se você for um administrador global ou de segurança, você pode gerenciar permissões do aplicativo para sua organização. Você pode ver as pessoas de aplicativos estão usando com dados do Office 365, que permissões estes aplicativos tem e muito mais.</span><span class="sxs-lookup"><span data-stu-id="f25c1-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage app permissions for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="f25c1-118">Este artigo descreve como criar uma consulta de aplicativo, como aprovar ou proibir um aplicativo e aonde ir para gerenciar permissões de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f25c1-118">This article describes where to go to manage app permissions, how to approve or ban an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-app-permissions-page"></a><span data-ttu-id="f25c1-119">Como encontrar a página Gerenciar aplicativo permissões</span><span class="sxs-lookup"><span data-stu-id="f25c1-119">How to find the Manage app permissions page</span></span>
<span data-ttu-id="f25c1-120"><a name="findappperms"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-120"></span></span>

> [!NOTE]
> <span data-ttu-id="f25c1-p102">Permissões de aplicativo são gerenciadas no portal de segurança de aplicativo de nuvem do Office 365. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="f25c1-p102">App permissions are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="f25c1-p103">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.)</span><span class="sxs-lookup"><span data-stu-id="f25c1-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="f25c1-126">Vá para **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="f25c1-126">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="f25c1-127">Clique (ou toque) **vá para segurança de aplicativo de nuvem do Office 365**.</span><span class="sxs-lookup"><span data-stu-id="f25c1-127">Click (or tap) **Go to Office 365 Cloud App Security**.</span></span>
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > <span data-ttu-id="f25c1-p104">Se a segurança de aplicativo de nuvem do Office 365 não está ativada ainda, você pode fazer isso nesta página. Consulte [Prepare-se para a segurança de aplicativo de nuvem do Office 365](get-ready-for-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="f25c1-p104">If Office 365 Cloud App Security is not turned on yet, you can do that on this page. See [Get ready for Office 365 Cloud App Security](get-ready-for-office-365-cas.md).</span></span> 
  
4. <span data-ttu-id="f25c1-131">Escolha **investigar** \> **permissões do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="f25c1-131">Choose **Investigate** \> **App permissions**.</span></span>
    
    ![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a><span data-ttu-id="f25c1-133">O que você verá na página Gerenciar aplicativo permissões</span><span class="sxs-lookup"><span data-stu-id="f25c1-133">What you'll see on the Manage app permissions page</span></span>
<span data-ttu-id="f25c1-134"><a name="whatsonpage"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-134"></span></span>

<span data-ttu-id="f25c1-135">A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar aplicativo permissões.</span><span class="sxs-lookup"><span data-stu-id="f25c1-135">The following table describes the controls and options available on the Manage app permissions page.</span></span>
  
|<span data-ttu-id="f25c1-136">**Item**</span><span class="sxs-lookup"><span data-stu-id="f25c1-136">**Item**</span></span>|<span data-ttu-id="f25c1-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f25c1-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f25c1-138">Ícone básica na barra de aplicativos de consulta</span><span class="sxs-lookup"><span data-stu-id="f25c1-138">Basic icon in the app query bar</span></span>  <br/> ![Ícone que indica o modo de exibição de consulta básica para consultar as permissões do aplicativo](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="f25c1-140">Selecione essa opção para alternar para o modo de exibição avançado.</span><span class="sxs-lookup"><span data-stu-id="f25c1-140">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="f25c1-141">(Se você vir **básica**, você está usando o modo de exibição avançado)</span><span class="sxs-lookup"><span data-stu-id="f25c1-141">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="f25c1-142">Ícone Avançado na barra de aplicativos de consulta</span><span class="sxs-lookup"><span data-stu-id="f25c1-142">Advanced icon in the app query bar</span></span>  <br/> ![Ícone que indica avançadas do modo de exibição de consulta para consultar as permissões do aplicativo](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="f25c1-144">Selecione essa opção para alternar para modo de exibição básico.</span><span class="sxs-lookup"><span data-stu-id="f25c1-144">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="f25c1-145">(Se você vir **Avançado**, você está usando o modo de exibição básico.)</span><span class="sxs-lookup"><span data-stu-id="f25c1-145">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="f25c1-146">Abrir ou fechar o ícone de todos os detalhes na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f25c1-146">Open or close all details icon in the app list</span></span>  <br/> ![Clique nesse ícone para abrir ou fechar todos os detalhes para todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="f25c1-148">Selecione esse ícone para exibir mais ou menos detalhes sobre cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f25c1-148">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="f25c1-149">Ícone de exportar na lista de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f25c1-149">Export icon in the app list</span></span>  <br/> ![Clique nesse ícone para exportar um arquivo csv de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="f25c1-151">Selecione esse ícone para exportar um arquivo CSV que contém uma lista de aplicativos, o número de usuários para cada aplicativo, permissões associadas com o aplicativo, o nível de permissões, estado do aplicativo e usar nível de comunidade.</span><span class="sxs-lookup"><span data-stu-id="f25c1-151">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="f25c1-152">Nome</span><span class="sxs-lookup"><span data-stu-id="f25c1-152">Name</span></span>  <br/> |<span data-ttu-id="f25c1-p105">Usar esse recurso para ver o nome de um App. Selecione o nome para exibir mais informações, como seu descrição, o publisher, o site da Web app e o ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f25c1-p105">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="f25c1-155">Autorizado pelo</span><span class="sxs-lookup"><span data-stu-id="f25c1-155">Authorized by</span></span>  <br/> |<span data-ttu-id="f25c1-p106">Use esta opção para ver quantos usuários tenham autorizados a um aplicativo para acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="f25c1-p106">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="f25c1-158">Nível de permissões</span><span class="sxs-lookup"><span data-stu-id="f25c1-158">Permissions Level</span></span>  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="f25c1-p107">Use esta opção para ver quanto acesso um aplicativo tem aos dados do Office 365. Níveis de permissões indicam **baixa**, **média**ou **alta**, onde **baixa** pode indicar que o aplicativo acessa somente perfil e o nome de um usuário. Selecione o nível para exibir mais informações, como permissões concedidas para o aplicativo, o uso da comunidade e atividade relacionada no [log de governança](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="f25c1-p107">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="f25c1-163">Estado do aplicativo ( **Banned**, **aprovado**ou **Undetermined**)</span><span class="sxs-lookup"><span data-stu-id="f25c1-163">App state ( **Banned**, **Approved**, or **Undetermined**)</span></span>  <br/> <span data-ttu-id="f25c1-164">![Ícones de permissões do aplicativo depois sendo permitidos, bloqueados ou nenhuma ação foi executada por um administrador](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span><span class="sxs-lookup"><span data-stu-id="f25c1-164">![App permissions icons after being allowed, blocked, or no action has been taken by an admin](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span></span>|<span data-ttu-id="f25c1-165">Use esta opção para marcar um aplicativo como aprovado ou Banned ou deixá-lo como indeterminado.</span><span class="sxs-lookup"><span data-stu-id="f25c1-165">Use this to mark an app as Approved or Banned, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="f25c1-166">Marcar um aplicativo como aprovados</span><span class="sxs-lookup"><span data-stu-id="f25c1-166">Mark an app as approved</span></span>
<span data-ttu-id="f25c1-167"><a name="approveapp"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-167"></span></span>

<span data-ttu-id="f25c1-168">Na página **Gerenciar permissões de aplicativo** , localize o aplicativo que você deseja aprovar e escolha o ícone **app marca como aprovado** .</span><span class="sxs-lookup"><span data-stu-id="f25c1-168">On the **Manage app permissions** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Escolha o aplicativo de marca como ícone aprovado](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
<span data-ttu-id="f25c1-170">O ícone fica verde, e o aplicativo em particular for aprovado para todos os usuários do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f25c1-170">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f25c1-p108">Quando você marca um aplicativo como aprovados, não há nenhum efeito sobre o usuário final. Marcação visualmente os aplicativos que foram aprovados ajuda a separá-los dos aplicativos que ainda não foram revisados ainda.</span><span class="sxs-lookup"><span data-stu-id="f25c1-p108">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="f25c1-173">Proibir um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f25c1-173">Ban an app</span></span>
<span data-ttu-id="f25c1-174"><a name="banapp"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-174"></span></span>

1. <span data-ttu-id="f25c1-175">Na página **Gerenciar permissões de aplicativo** , localize o aplicativo que você deseja proibir e escolha o ícone **app marca como proibidos** .</span><span class="sxs-lookup"><span data-stu-id="f25c1-175">On the **Manage app permissions** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span> 
    
    ![Escolha o aplicativo de marca como ícone proibido](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. <span data-ttu-id="f25c1-177">Escolha se deseja que os usuários saibam o que foi proibido seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f25c1-177">Choose whether to let users know that their app has been banned.</span></span>
    
    <span data-ttu-id="f25c1-178">(Recomendado) Para permitir que os usuários saibam, selecione **usuários Notify que recebem acesso para este aplicativo proibido**e adicione ou edite uma mensagem de notificação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f25c1-178">(Recommended) To let users know, select **Notify users who granted access to this banned app**, and add or edit a custom notification message.</span></span>
    
    <span data-ttu-id="f25c1-179">Para não permitir que os usuários saibam, desmarque **usuários Notify que recebem acesso para este aplicativo proibido**.</span><span class="sxs-lookup"><span data-stu-id="f25c1-179">To not let users know, clear **Notify users who granted access to this banned app**.</span></span>
    
    ![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. <span data-ttu-id="f25c1-181">Escolha **aplicativo proibir**.</span><span class="sxs-lookup"><span data-stu-id="f25c1-181">Choose **Ban app**.</span></span>
    
## <a name="create-an-app-query"></a><span data-ttu-id="f25c1-182">Criar uma consulta de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f25c1-182">Create an app query</span></span>
<span data-ttu-id="f25c1-183"><a name="createapp"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-183"></span></span>

1. <span data-ttu-id="f25c1-p109">Na barra de consulta do aplicativo, se você vir **Avançado**, clique (ou toque)-lo para ir para o modo de exibição avançado. (Se você vir Basic, você estiver usando o modo de exibição avançado; manter sua opinião como está.)</span><span class="sxs-lookup"><span data-stu-id="f25c1-p109">In the app query bar, if you see **Advanced**, click (or tap) it to go to the Advanced view. (If you see Basic, you are using the Advanced view; keep your view as it is.)</span></span>
    
2. <span data-ttu-id="f25c1-p110">Use a lista **Selecionar um filtro** para escolher uma opção. A tabela a seguir resume as opções de filtro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f25c1-p110">Use the **Select a filter** list to choose an option. The following table summarizes your available filter options.</span></span> 
    
|<span data-ttu-id="f25c1-188">**Utilize esse filtro**</span><span class="sxs-lookup"><span data-stu-id="f25c1-188">**Use this filter**</span></span>|<span data-ttu-id="f25c1-189">**Para exibir**</span><span class="sxs-lookup"><span data-stu-id="f25c1-189">**To display**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f25c1-190">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="f25c1-190">**App**</span></span> <br/> |<span data-ttu-id="f25c1-191">Aplicativos com determinados nomes</span><span class="sxs-lookup"><span data-stu-id="f25c1-191">Apps with certain names</span></span>  <br/> |
|<span data-ttu-id="f25c1-192">**Estado do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="f25c1-192">**App state**</span></span> <br/> |<span data-ttu-id="f25c1-193">Aplicativos com base em seu estado (aprovado, Banned ou Undetermined)</span><span class="sxs-lookup"><span data-stu-id="f25c1-193">Apps based on their state (Approved, Banned, or Undetermined)</span></span>  <br/> |
|<span data-ttu-id="f25c1-194">**Uso da comunidade**</span><span class="sxs-lookup"><span data-stu-id="f25c1-194">**Community use**</span></span> <br/> |<span data-ttu-id="f25c1-195">Aplicativos com base na comunidade usam níveis (Rare, Uncommon ou comum)</span><span class="sxs-lookup"><span data-stu-id="f25c1-195">Apps based on community use levels (Rare, Uncommon, or Common)</span></span>  <br/> |
|<span data-ttu-id="f25c1-196">**Nível de permissão**</span><span class="sxs-lookup"><span data-stu-id="f25c1-196">**Permission level**</span></span> <br/> |<span data-ttu-id="f25c1-197">Aplicativos com base em determinados níveis de permissão</span><span class="sxs-lookup"><span data-stu-id="f25c1-197">Apps based on certain permission levels</span></span>  <br/> |
|<span data-ttu-id="f25c1-198">**Permissões**</span><span class="sxs-lookup"><span data-stu-id="f25c1-198">**Permissions**</span></span> <br/> |<span data-ttu-id="f25c1-199">Aplicativos que necessitam de determinadas permissões</span><span class="sxs-lookup"><span data-stu-id="f25c1-199">Apps that require certain permissions</span></span>  <br/> |
|<span data-ttu-id="f25c1-200">**Publicador**</span><span class="sxs-lookup"><span data-stu-id="f25c1-200">**Publisher**</span></span> <br/> |<span data-ttu-id="f25c1-201">Aplicativos de determinados fornecedores</span><span class="sxs-lookup"><span data-stu-id="f25c1-201">Apps from certain publishers</span></span>  <br/> |
|<span data-ttu-id="f25c1-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f25c1-202">**User**</span></span> <br/> |<span data-ttu-id="f25c1-203">Aplicativos que um determinado usuário autorizado</span><span class="sxs-lookup"><span data-stu-id="f25c1-203">Apps that a certain user authorized</span></span>  <br/> |
   
3. <span data-ttu-id="f25c1-204">Selecione **é igual a** ou **diferente**e, em seguida, especifique um valor para o filtro.</span><span class="sxs-lookup"><span data-stu-id="f25c1-204">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
4. <span data-ttu-id="f25c1-205">Para adicionar mais filtros, selecione o (sinal de adição</span><span class="sxs-lookup"><span data-stu-id="f25c1-205">To add more filters, select the plus sign (</span></span>![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="f25c1-207">) e repita as etapas 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="f25c1-207">), and then repeat steps 2 and 3.</span></span>
    
5. <span data-ttu-id="f25c1-208">Para remover um filtro, selecione o x (</span><span class="sxs-lookup"><span data-stu-id="f25c1-208">To remove a filter, select the x (</span></span>![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="f25c1-210">) ao lado do nome de um filtro.</span><span class="sxs-lookup"><span data-stu-id="f25c1-210">) next to a filter name.</span></span>
    
<span data-ttu-id="f25c1-211">Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.</span><span class="sxs-lookup"><span data-stu-id="f25c1-211">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="f25c1-212">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f25c1-212">Next steps</span></span>
<span data-ttu-id="f25c1-213"><a name="nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="f25c1-213"></span></span>

- [<span data-ttu-id="f25c1-214">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="f25c1-214">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="f25c1-215">Revise seus [logs de tráfego da Web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="f25c1-215">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="f25c1-216">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="f25c1-216">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

