---
title: Habilitar o suplemento de Mensagem de Relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995152"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="94301-103">Habilitar o suplemento de Mensagem de Relatório</span><span class="sxs-lookup"><span data-stu-id="94301-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="94301-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="94301-104">Overview</span></span>

<span data-ttu-id="94301-p101">O suplemento de mensagem de relatório para o Outlook e Outlook na web permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando [A proteção de ameaça avançadas do Office 365](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornece equipe de segurança da sua organização com informações úteis, que eles podem usar para analisar e atualizar diretivas de segurança.</span><span class="sxs-lookup"><span data-stu-id="94301-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="94301-p102">Por exemplo, suponha que as pessoas são relatórios muitas mensagens como phishing. Este mostra informações no [Painel de segurança](security-dashboard.md) e outros relatórios. Equipe de segurança da sua organização pode usar essas informações como uma indicação de que as políticas de AntiPhishing talvez precisem ser atualizados. Ou, se as pessoas estão relatando muita mensagens que foram sinalizados como lixo eletrônico, como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, talvez seja necessário ajustar o [políticas antispam](configure-the-anti-spam-policies.md)equipe de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="94301-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="94301-112">O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e produtos a seguir:</span><span class="sxs-lookup"><span data-stu-id="94301-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="94301-113">Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="94301-113">Outlook on the web</span></span>
 - <span data-ttu-id="94301-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="94301-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="94301-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94301-115">Outlook 2016</span></span>
 - <span data-ttu-id="94301-116">Outlook 2016 para Mac</span><span class="sxs-lookup"><span data-stu-id="94301-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="94301-117">Outlook incluído com o Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="94301-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="94301-p103">O suplemento de mensagem de relatório para o Outlook e Outlook na web não é exatamente a mesma coisa que o [Filtro de Email de lixo eletrônico do Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), embora ambos podem ser usados para marcar um email como lixo eletrônico, não lixo ou uma tentativa de phishing. O suplemento de mensagem de relatório para o Outlook e Outlook na web notifica Microsoft sobre email classificados incorretamente, enquanto o filtro de lixo eletrônico do Outlook é usado para organizar as mensagens de email na caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="94301-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="94301-120">Se você for um usuário individual, você pode [Habilitar o suplemento de mensagem de relatório por conta própria](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="94301-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="94301-p104">Se você é um administrador global do Office 365 ou um administrador do Exchange Online e Exchange está configurado para usar a autenticação OAuth, você pode [Habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization). O suplemento do relatório de mensagem agora está disponível por meio da [Implantação centralizados](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="94301-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="94301-123">Obtenha a mensagem de relatório suplemento para si mesmo</span><span class="sxs-lookup"><span data-stu-id="94301-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="94301-124">No [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), procure o [suplemento de mensagem de relatório](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="94301-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="94301-125">Escolha **GET IT agora**.</span><span class="sxs-lookup"><span data-stu-id="94301-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="94301-126">![Relatar mensagem - obtê-lo agora](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="94301-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="94301-p105">Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="94301-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="94301-129">Entrar no Office 365 usando o seu trabalho ou conta escola (para uso de negócios) ou sua conta da Microsoft (para uso pessoal).</span><span class="sxs-lookup"><span data-stu-id="94301-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="94301-130">Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="94301-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="94301-131">No Outlook, o ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="94301-131">In Outlook, the icon looks like this:</span></span> <br/> ![Relatar o ícone do suplemento de mensagem do Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="94301-133">No Outlook Web App (ou Outlook na web), o ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="94301-133">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook no ícone de mensagem de relatório na web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="94301-135">Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="94301-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="94301-136">Obter e habilitar o suplemento de mensagem de relatório para sua organização</span><span class="sxs-lookup"><span data-stu-id="94301-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94301-p106">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa. Além disso, o Exchange deve ser configurado para usar a autenticação OAuth para saber mais, consulte [requisitos do Exchange (centralizados implantação dos suplementos)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="94301-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="94301-139">Vá até a [página de suplementos do serviços &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="94301-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="94301-140">![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="94301-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="94301-141">Escolha **+ implantar o suplemento**.</span><span class="sxs-lookup"><span data-stu-id="94301-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="94301-142">![Escolha implantar o suplemento](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="94301-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="94301-143">Na tela do **Novo suplemento** , revise as informações e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="94301-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="94301-144">![Detalhes do novo suplemento](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="94301-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="94301-145">Selecione **eu quiser adicionar um suplemento da Office Store**e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="94301-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="94301-146">![Eu quiser adicionar um novo suplemento](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="94301-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="94301-147">Mensagem de **Relatório**e na lista de resultados, ao lado do **Suplemento de mensagem do relatório**de pesquisa, escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="94301-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="94301-148">![Procure a mensagem de relatório e escolha Adicionar](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="94301-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="94301-149">Na tela de **Mensagem de relatório** , revise as informações e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="94301-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="94301-150">![Detalhes da mensagem de relatório](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="94301-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="94301-151">Especifique as configurações de usuário padrão para o Outlook e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="94301-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="94301-152">![Relatar as configurações padrão de mensagem do Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="94301-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="94301-153">Especificar quem obtém o suplemento de mensagem de relatório e escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="94301-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="94301-154">![Quem obtém a mensagem de relatório suplemento](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="94301-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="94301-155">Recomendamos a [configuração de uma regra para obter uma cópia das mensagens de email relatado pelos usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="94301-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="94301-p107">Dependendo do item selecionado ao configurar o suplemento (etapas 7-8 acima), as pessoas na sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponíveis. Pessoas da sua organização verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="94301-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="94301-158">No Outlook, o ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="94301-158">In Outlook, the icon looks like this:</span></span> <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="94301-160">No Outlook Web App (ou Outlook na web), o ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="94301-160">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="94301-162">Quando você notifica os usuários sobre o suplemento de mensagem de relatório, inclua um link para [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="94301-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="94301-163">Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários</span><span class="sxs-lookup"><span data-stu-id="94301-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94301-164">Você deve ser um administrador do Exchange Online para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="94301-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="94301-p108">Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.</span><span class="sxs-lookup"><span data-stu-id="94301-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="94301-167">No Centro de administração do Exchange, escolha **fluxo de emails** \> **regras**.</span><span class="sxs-lookup"><span data-stu-id="94301-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="94301-168">Escolha **+** \> **criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="94301-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="94301-169">Na caixa **nome** , digite um nome, como envios.</span><span class="sxs-lookup"><span data-stu-id="94301-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="94301-170">Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**.</span><span class="sxs-lookup"><span data-stu-id="94301-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="94301-171">Na tela **Especificar palavras ou expressões** , adicione `junk@office365.microsoft.com` e `phish@office365.microsoft.com`e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="94301-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="94301-172">![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="94301-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="94301-173">Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**.</span><span class="sxs-lookup"><span data-stu-id="94301-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="94301-174">Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="94301-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="94301-175">![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="94301-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="94301-176">Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**.</span><span class="sxs-lookup"><span data-stu-id="94301-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="94301-177">Em **Escolher um modo para essa regra**, escolha **Enforce**.</span><span class="sxs-lookup"><span data-stu-id="94301-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="94301-178">![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="94301-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="94301-179">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="94301-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="94301-p109">Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) ou suas configurações [antispam](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="94301-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="94301-182">Saiba como usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="94301-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="94301-183">Consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="94301-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="94301-184">Analisar ou editar as configurações para o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="94301-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="94301-185">Você pode examinar e editar as configurações padrão para o suplemento de mensagem de relatório na [página de suplementos do & de serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="94301-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="94301-186">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="94301-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="94301-187">Vá até a [página de suplementos do serviços &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="94301-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="94301-188">![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="94301-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="94301-189">Localize e selecione o suplemento de mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="94301-189">Find and select the Report Message add-in.</span></span><br/>![Localize e selecione o suplemento de mensagem de relatório](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="94301-191">Na tela de mensagem de relatório, revise e editar configurações, conforme apropriado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="94301-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Configurações para o suplemento de mensagem de relatório](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="94301-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94301-193">Related topics</span></span>

[<span data-ttu-id="94301-194">Usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="94301-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="94301-195">Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="94301-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="94301-196">Exibir relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="94301-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="94301-197">Use o Explorer na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="94301-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

