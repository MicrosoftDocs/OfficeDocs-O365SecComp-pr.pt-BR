---
title: Classificação de Segurança do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559084"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="cf4c8-105">Classificação de Segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="cf4c8-105">Office 365 Secure Score</span></span>

<span data-ttu-id="cf4c8-p102">**Resumo** Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação. Leia este artigo para obter uma visão geral de pontuação seguro e como você pode usá-lo.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p102">**Summary** Ever wonder how secure your organization really is in Office 365? Secure Score is here to help. Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score. Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="cf4c8-110">Como obter a pontuação de seguro</span><span class="sxs-lookup"><span data-stu-id="cf4c8-110">How to get to Secure Score</span></span>

<span data-ttu-id="cf4c8-111">Se sua organização tiver uma assinatura que inclui o [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)ou Business Premium do Office 365 e você tem as [permissões necessárias](#required-permissions), você pode exibir a pontuação da organização seguro visitando [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="cf4c8-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="cf4c8-112">Como alternativa, você pode visitar o Centro de conformidade do & de segurança ([https://protection.office.com](https://protection.office.com)), onde você encontrará um widget pontuação seguro que fornece com sua pontuação atual.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Widget da pontuação de seguro](media/SecureScoreWidget-o365.png)

<span data-ttu-id="cf4c8-114">O widget inclui um link para seu painel pontuação seguro.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Painel de pontuação de seguro](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="cf4c8-116">Como funciona</span><span class="sxs-lookup"><span data-stu-id="cf4c8-116">How it works</span></span>

<span data-ttu-id="cf4c8-p103">Pontuação segura determina quais serviços do Office 365 que você estiver usando (por exemplo, Exchange, SharePoint e OneDrive), em seguida, compara as configurações e as atividades a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como bem alinhado à sua organização estiver com as práticas recomendadas de segurança. Você também terá recomendações sobre etapas que podem ser realizadas para melhorar a pontuação da sua organização.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p103">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft. You'll get a score based on how well aligned your organization is with security best practices. You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Fila de ações na ferramenta de pontuação seguro do Office 365](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="cf4c8-p104">Pontuação segura calcula sua pontuação com base nos serviços fornecidos por que você comprou. Por exemplo, se você comprou somente um plano do Exchange Online, você não marcados para recursos de segurança do SharePoint Online. Denominador da pontuação de é a soma de todas as linhas de base para os controles que se aplicam aos produtos que você comprou. O numerador é a soma de todos os controles para os quais você concluída ou parcialmente concluído, as ações para atender a esse controle.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p104">Secure Score calculates your score based on the services you purchased. For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features. The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased. The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="cf4c8-125">Expanda uma ação para saber quais etapas a serem seguidas, protegem-lo contra as ameaças que ele ajudará e quantos pontos sua pontuação aumentará depois que você segue a recomendação.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Ação expandida na ferramenta de pontuação seguro do Office 365](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="cf4c8-127">Para ver o impacto de suas ações na segurança da sua organização, selecione a guia do **Analisador de pontuação** e analisar o histórico.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Guia do analisador de pontuação da ferramenta pontuação seguro do Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="cf4c8-129">O gráfico abaixo, você verá uma lista de ações e pontuações por categoria.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Na guia analisador de pontuação mostrando um ponto de dados selecionado do gráfico](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="cf4c8-131">Ações que são rotuladas como **[Não avaliados]** são aquelas que você pode executar para sua organização, mas porque não estão conectados à pontuação seguro, eles não são avaliados.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="cf4c8-p105">Na página do **Analisador de pontuação** , clique em um ponto de dados para um determinado dia, role para baixo para ver as ações concluídas e incompletas daquele dia descobrir o que são alteradas. A pontuação é calculada uma vez por dia (cerca 1:00 AM. PST). Se você fizer uma alteração em uma ação medida, a pontuação atualizará automaticamente o próximo dia. Leva até 48 horas para que uma alteração refletido na sua pontuação.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p105">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed. The score is calculated once per day (around 1:00 AM PST). If you make a change to a measured action, the score will automatically update the next day. It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="cf4c8-p106">Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram recursos que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e a pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p106">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted features that can offset the risk of being breached. No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="cf4c8-139">Como o ajuda a pontuação de seguro</span><span class="sxs-lookup"><span data-stu-id="cf4c8-139">How Secure Score helps</span></span>

<span data-ttu-id="cf4c8-p107">Com pontuação seguro, você pode ajudar a melhorar a situação de segurança da sua organização usando os recursos internos de segurança no Office 365 (muitos dos quais você já adquiriu mas não estar ciente). Aprender mais sobre esses recursos pode ajudar a fornecer tranquilo que você estiver levando os procedimentos apropriados para proteger sua organização contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p107">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of). Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="cf4c8-p108">Mas não apenas se o nosso word para ele. Clientes que utilizam o Secure pontuação vimos seus pontuação aumentar a cinco vezes maior em relação a clientes que não são utilizá-lo. (O aumento de seus pontuação corresponde com os recursos de segurança que está sendo usados em suas organizações.)</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p108">But don't just take our word for it. Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it. (The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf4c8-p109">Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram controles que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-p109">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted controls which can offset the risk of being breached. No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="cf4c8-148">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="cf4c8-148">Required permissions</span></span>

<span data-ttu-id="cf4c8-149">Para exibir e usar o seu painel pontuação seguro, você deve ter uma das seguintes funções no Windows Azure Active Directory:</span><span class="sxs-lookup"><span data-stu-id="cf4c8-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in Azure Active Directory:</span></span>
- <span data-ttu-id="cf4c8-150">Administrador global</span><span class="sxs-lookup"><span data-stu-id="cf4c8-150">Global Administrator</span></span>
- <span data-ttu-id="cf4c8-151">Administrador de faturamento</span><span class="sxs-lookup"><span data-stu-id="cf4c8-151">Billing Administrator</span></span>
- <span data-ttu-id="cf4c8-152">Administrador de usuários</span><span class="sxs-lookup"><span data-stu-id="cf4c8-152">User Administrator</span></span>
- <span data-ttu-id="cf4c8-153">Administrador de senha</span><span class="sxs-lookup"><span data-stu-id="cf4c8-153">Password Administrator</span></span>
- <span data-ttu-id="cf4c8-154">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="cf4c8-154">Security Administrator</span></span>
- <span data-ttu-id="cf4c8-155">Leitor de segurança</span><span class="sxs-lookup"><span data-stu-id="cf4c8-155">Security Reader</span></span>
- <span data-ttu-id="cf4c8-156">Administrador do Exchange</span><span class="sxs-lookup"><span data-stu-id="cf4c8-156">Exchange Administrator</span></span>
- <span data-ttu-id="cf4c8-157">Administrador do SharePoint</span><span class="sxs-lookup"><span data-stu-id="cf4c8-157">SharePoint Administrator</span></span>

 <span data-ttu-id="cf4c8-158">Usuários que não estão atribuídos a uma função de administrador não conseguirá acessar pontuação seguro.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf4c8-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf4c8-159">Related topics</span></span>

[<span data-ttu-id="cf4c8-160">Visão geral do painel de segurança</span><span class="sxs-lookup"><span data-stu-id="cf4c8-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="cf4c8-161">Qual assinatura eu tenho?</span><span class="sxs-lookup"><span data-stu-id="cf4c8-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)