---
title: Classificação de Segurança do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Você já se perguntou qual é a segurança da sua organização no Office 365? A pontuação segura está aqui para ajudar. A pontuação segura analisa a segurança da sua organização com base em suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262429"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="c1c19-105">Classificação de Segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="c1c19-105">Office 365 Secure Score</span></span>

<span data-ttu-id="c1c19-106">**Resumo** Você já se perguntou qual é a segurança da sua organização no Office 365?</span><span class="sxs-lookup"><span data-stu-id="c1c19-106">**Summary** Ever wonder how secure your organization really is in Office 365?</span></span> <span data-ttu-id="c1c19-107">A pontuação segura está aqui para ajudar.</span><span class="sxs-lookup"><span data-stu-id="c1c19-107">Secure Score is here to help.</span></span> <span data-ttu-id="c1c19-108">A pontuação segura analisa a segurança da sua organização com base em suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.</span><span class="sxs-lookup"><span data-stu-id="c1c19-108">Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score.</span></span> <span data-ttu-id="c1c19-109">Leia este artigo para obter uma visão geral da Pontuação segura e como você pode usá-lo.</span><span class="sxs-lookup"><span data-stu-id="c1c19-109">Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="c1c19-110">Como obter a pontuação segura</span><span class="sxs-lookup"><span data-stu-id="c1c19-110">How to get to Secure Score</span></span>

<span data-ttu-id="c1c19-111">Se sua organização tem uma assinatura que inclui o [office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [o Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)ou o Office 365 Business Premium e você tem as [permissões necessárias](#required-permissions), pode exibir a pontuação segura da sua organização visitando [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="c1c19-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="c1c19-112">Como alternativa, você pode visitar o centro de conformidade do &[https://protection.office.com](https://protection.office.com)de segurança (), onde encontrará um widget de Pontuação segura que fornece a sua pontuação atual.</span><span class="sxs-lookup"><span data-stu-id="c1c19-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Widget Pontuação segura](media/SecureScoreWidget-o365.png)

<span data-ttu-id="c1c19-114">O widget inclui um link para seu painel de Pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="c1c19-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Painel de Pontuação segura](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="c1c19-116">Como funciona</span><span class="sxs-lookup"><span data-stu-id="c1c19-116">How it works</span></span>

<span data-ttu-id="c1c19-117">A pontuação segura determina quais serviços do Office 365 você está usando (como OneDrive, SharePoint e Exchange) e compara suas configurações e atividades com uma linha de base estabelecida pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1c19-117">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft.</span></span> <span data-ttu-id="c1c19-118">Você receberá uma pontuação com base em como a organização está bem alinhada com as práticas recomendadas de segurança.</span><span class="sxs-lookup"><span data-stu-id="c1c19-118">You'll get a score based on how well aligned your organization is with security best practices.</span></span> <span data-ttu-id="c1c19-119">Você também terá recomendações sobre as etapas que você pode tomar para melhorar a pontuação da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c1c19-119">You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Fila de ações na ferramenta de Pontuação segura do Office 365](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="c1c19-121">A pontuação segura calcula sua pontuação com base nos serviços que você comprou.</span><span class="sxs-lookup"><span data-stu-id="c1c19-121">Secure Score calculates your score based on the services you purchased.</span></span> <span data-ttu-id="c1c19-122">Por exemplo, se você comprou apenas um plano do Exchange Online, você não terá a Pontuação dos recursos de segurança do SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c1c19-122">For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features.</span></span> <span data-ttu-id="c1c19-123">O denominador da pontuação é a soma de todas as linhas de base para os controles que se aplicam aos produtos que você comprou.</span><span class="sxs-lookup"><span data-stu-id="c1c19-123">The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased.</span></span> <span data-ttu-id="c1c19-124">O numerador é a soma de todos os controles que você concluiu, ou parcialmente concluído, as ações para preencher esse controle.</span><span class="sxs-lookup"><span data-stu-id="c1c19-124">The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="c1c19-125">Expanda uma ação para saber mais sobre as etapas a serem tomadas, as ameaças às quais ele ajudará a proteger você e quantos pontos sua pontuação aumentará depois que você seguir a recomendação.</span><span class="sxs-lookup"><span data-stu-id="c1c19-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Ação expandida na ferramenta de Pontuação segura do Office 365](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="c1c19-127">Para ver o impacto de suas ações na segurança da sua organização, selecione a guia analisador de **pontos** e revise o histórico.</span><span class="sxs-lookup"><span data-stu-id="c1c19-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Guia analisador de pontos da ferramenta de Pontuação segura do Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="c1c19-129">Abaixo do gráfico, você verá uma lista de resultados e ações por categoria.</span><span class="sxs-lookup"><span data-stu-id="c1c19-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Gráfico na guia do analisador de pontos mostrando um ponto de dados selecionado](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="c1c19-131">As ações que são rotuladas como **[não classificadas]** são aquelas que podem ser realizadas na sua organização, mas como não estão conectadas à pontuação segura, elas não são pontuadas.</span><span class="sxs-lookup"><span data-stu-id="c1c19-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="c1c19-132">Na página **analisador de Pontuação** , clique em um ponto de dados para um dia específico e, em seguida, role para baixo para ver as ações concluídas e incompletas desse dia para descobrir o que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c1c19-132">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed.</span></span> <span data-ttu-id="c1c19-133">A pontuação é calculada uma vez por dia (em torno de 1:00 AM PST).</span><span class="sxs-lookup"><span data-stu-id="c1c19-133">The score is calculated once per day (around 1:00 AM PST).</span></span> <span data-ttu-id="c1c19-134">Se você fizer uma alteração em uma ação medida, a pontuação será automaticamente atualizada no dia seguinte.</span><span class="sxs-lookup"><span data-stu-id="c1c19-134">If you make a change to a measured action, the score will automatically update the next day.</span></span> <span data-ttu-id="c1c19-135">Leva até 48 horas para que uma alteração seja refletida na sua pontuação.</span><span class="sxs-lookup"><span data-stu-id="c1c19-135">It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="c1c19-136">A pontuação segura não expressa uma medida absoluta da probabilidade de você ser violada.</span><span class="sxs-lookup"><span data-stu-id="c1c19-136">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="c1c19-137">Ele expressa a extensão à qual você adotou recursos que podem compensar o risco de ser violado.</span><span class="sxs-lookup"><span data-stu-id="c1c19-137">It expresses the extent to which you have adopted features that can offset the risk of being breached.</span></span> <span data-ttu-id="c1c19-138">Nenhum serviço pode garantir que você não será violado, e a pontuação segura não deve ser interpretada como uma garantia de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="c1c19-138">No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="c1c19-139">Como a pontuação segura ajuda</span><span class="sxs-lookup"><span data-stu-id="c1c19-139">How Secure Score helps</span></span>

<span data-ttu-id="c1c19-140">Com a pontuação segura, você pode ajudar a melhorar a postura de segurança da sua organização usando os recursos de segurança internos no Office 365 (muitos dos quais você já comprou, mas pode não estar ciente).</span><span class="sxs-lookup"><span data-stu-id="c1c19-140">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of).</span></span> <span data-ttu-id="c1c19-141">Saber mais sobre esses recursos pode ajudar a garantir que você esteja seguindo as etapas certas para proteger sua organização contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="c1c19-141">Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="c1c19-142">Mas não considere apenas nossa palavra.</span><span class="sxs-lookup"><span data-stu-id="c1c19-142">But don't just take our word for it.</span></span> <span data-ttu-id="c1c19-143">Os clientes que usam a pontuação segura perceberam que a pontuação aumentou cinco vezes mais do que os clientes que não o estão usando.</span><span class="sxs-lookup"><span data-stu-id="c1c19-143">Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it.</span></span> <span data-ttu-id="c1c19-144">(O aumento na pontuação corresponde aos recursos de segurança que estão sendo usados em suas organizações.)</span><span class="sxs-lookup"><span data-stu-id="c1c19-144">(The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="c1c19-145">A pontuação segura não expressa uma medida absoluta da probabilidade de você ser violada.</span><span class="sxs-lookup"><span data-stu-id="c1c19-145">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="c1c19-146">Ele expressa a extensão à qual você adotou controles que podem compensar o risco de ser violado.</span><span class="sxs-lookup"><span data-stu-id="c1c19-146">It expresses the extent to which you have adopted controls which can offset the risk of being breached.</span></span> <span data-ttu-id="c1c19-147">Nenhum serviço pode garantir que você não será violado, e a pontuação segura não deve ser interpretada como uma garantia de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="c1c19-147">No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="c1c19-148">Permissões obrigatórias</span><span class="sxs-lookup"><span data-stu-id="c1c19-148">Required permissions</span></span>

<span data-ttu-id="c1c19-149">Para exibir e usar seu painel de Pontuação segura, você deve receber uma das seguintes funções no [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span><span class="sxs-lookup"><span data-stu-id="c1c19-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>
- <span data-ttu-id="c1c19-150">Administrador global</span><span class="sxs-lookup"><span data-stu-id="c1c19-150">Global Administrator</span></span>
- <span data-ttu-id="c1c19-151">Administrador de cobrança</span><span class="sxs-lookup"><span data-stu-id="c1c19-151">Billing Administrator</span></span>
- <span data-ttu-id="c1c19-152">Administrador de usuários</span><span class="sxs-lookup"><span data-stu-id="c1c19-152">User Administrator</span></span>
- <span data-ttu-id="c1c19-153">Administrador de senha</span><span class="sxs-lookup"><span data-stu-id="c1c19-153">Password Administrator</span></span>
- <span data-ttu-id="c1c19-154">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="c1c19-154">Security Administrator</span></span>
- <span data-ttu-id="c1c19-155">Leitor de segurança</span><span class="sxs-lookup"><span data-stu-id="c1c19-155">Security Reader</span></span>
- <span data-ttu-id="c1c19-156">Administrador do Exchange</span><span class="sxs-lookup"><span data-stu-id="c1c19-156">Exchange Administrator</span></span>
- <span data-ttu-id="c1c19-157">Administrador do SharePoint</span><span class="sxs-lookup"><span data-stu-id="c1c19-157">SharePoint Administrator</span></span>

 <span data-ttu-id="c1c19-158">Os usuários que não são atribuídos a uma função de administrador não poderão acessar a pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="c1c19-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1c19-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1c19-159">Related topics</span></span>

[<span data-ttu-id="c1c19-160">Visão geral do painel de segurança</span><span class="sxs-lookup"><span data-stu-id="c1c19-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="c1c19-161">Qual assinatura eu tenho?</span><span class="sxs-lookup"><span data-stu-id="c1c19-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
