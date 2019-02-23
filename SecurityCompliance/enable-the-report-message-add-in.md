---
title: Habilitar o suplemento de Mensagem de Relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Saiba como habilitar o suplemento de mensagem de relatório para o Outlook e o Outlook na Web, para usuários individuais ou para toda a organização.
ms.openlocfilehash: 48bd8937622588bbf5a1e07b9d4341e937c5cf7f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217381"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="ff961-103">Habilitar o suplemento de Mensagem de Relatório</span><span class="sxs-lookup"><span data-stu-id="ff961-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="ff961-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="ff961-104">Overview</span></span>

<span data-ttu-id="ff961-p101">O suplemento de mensagem de relatório para o Outlook e o Outlook na Web permite que as pessoas relatem facilmente emails mal classificados, sejam seguros ou mal-intencionados, para a Microsoft e seus afiliados para análise. A Microsoft usa esses envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando a [proteção avançada contra ameaças do office 365](office-365-atp.md) ou o [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornecerá à equipe de segurança da sua organização informações úteis que podem ser usadas para revisar e atualizar políticas de segurança.</span><span class="sxs-lookup"><span data-stu-id="ff961-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="ff961-p102">Por exemplo, suponha que as pessoas estejam relatando muitas mensagens como phishing. Essas informações são superfícies no [painel de segurança](security-dashboard.md) e em outros relatórios. A equipe de segurança da sua organização pode usar essas informações como indicação de que as políticas anti-phishing podem precisar ser atualizadas. Ou, se as pessoas estiverem relatando muitas mensagens que foram sinalizadas como lixo eletrônico como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, a equipe de segurança da sua organização poderá precisar ajustar [políticas antispam](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ff961-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="ff961-112">O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e os seguintes produtos:</span><span class="sxs-lookup"><span data-stu-id="ff961-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="ff961-113">Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="ff961-113">Outlook on the web</span></span>
 - <span data-ttu-id="ff961-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="ff961-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="ff961-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff961-115">Outlook 2016</span></span>
 - <span data-ttu-id="ff961-116">Outlook 2016 para Mac</span><span class="sxs-lookup"><span data-stu-id="ff961-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="ff961-117">Outlook incluído no Office 365 proPlus</span><span class="sxs-lookup"><span data-stu-id="ff961-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="ff961-p103">O suplemento de mensagem de relatório para o Outlook e o Outlook na Web não é exatamente o mesmo que o [filtro de lixo eletrônico do Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), embora ambos possam ser usados para marcar email como lixo eletrônico, não lixo eletrônico ou uma tentativa de phishing. O suplemento de mensagem de relatório para o Outlook e o Outlook na Web notifica a Microsoft sobre emails incorretamente classificados, enquanto o filtro de lixo eletrônico do Outlook é usado para organizar mensagens de email na caixa de correio de um usuário.</span><span class="sxs-lookup"><span data-stu-id="ff961-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="ff961-120">Se você for um usuário individual, é possível [habilitar o relatório de suplemento de mensagens para você](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="ff961-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="ff961-p104">Se você for um administrador global do Office 365 ou um administrador do Exchange Online e o Exchange estiver configurado para usar a autenticação OAuth, você poderá [habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization). O suplemento de mensagem de relatório agora está disponível por meio da [implantação centralizada](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="ff961-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="ff961-123">Obter o suplemento de mensagem de relatório para você mesmo</span><span class="sxs-lookup"><span data-stu-id="ff961-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="ff961-124">No [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), procure o [suplemento de mensagem de relatório](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="ff961-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="ff961-125">Escolha **obtê-lo agora**.</span><span class="sxs-lookup"><span data-stu-id="ff961-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="ff961-126">![Mensagem de relatório-obter agora](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="ff961-p105">Revise os termos de uso e política de privacidade. Em seguida, escolha **continuar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="ff961-129">Entre no Office 365 usando sua conta corporativa ou de estudante (para uso comercial) ou sua conta da Microsoft (para uso pessoal).</span><span class="sxs-lookup"><span data-stu-id="ff961-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="ff961-130">Depois que o suplemento estiver instalado e habilitado, você verá os seguintes ícones:</span><span class="sxs-lookup"><span data-stu-id="ff961-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="ff961-131">No Outlook, o ícone tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="ff961-131">In Outlook, the icon looks like this:</span></span> <br/> ![Ícone de suplemento de mensagem de relatório para Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="ff961-133">No Outlook na Web (anteriormente conhecido como Outlook Web App), o ícone tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="ff961-133">In Outlook on the web (formerly known as Outlook Web App), the icon looks like this:</span></span><br/>![Ícone de suplemento da mensagem de relatório da Web do Outlook](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="ff961-135">Como próxima etapa, saiba como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="ff961-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="ff961-136">Obter e habilitar o suplemento de mensagem de relatório para sua organização</span><span class="sxs-lookup"><span data-stu-id="ff961-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff961-p106">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para concluir essa tarefa. Além disso, o Exchange deve ser configurado para usar a autenticação OAuth para saber mais, consulte [Exchange Requirements (implantação centralizada de suplementos)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="ff961-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="ff961-139">Vá para a [página de suplementos de serviços do &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ff961-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="ff961-140">![Página serviços e suplementos no novo centro de administração do Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="ff961-141">Escolha **+ implantar suplemento**.</span><span class="sxs-lookup"><span data-stu-id="ff961-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="ff961-142">![Escolha implantar suplemento](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="ff961-143">Na tela **novo suplemento** , revise as informações e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="ff961-144">![Novos detalhes do suplemento](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="ff961-145">Selecione **desejo adicionar um suplemento da Office Store**e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="ff961-146">![Desejo adicionar um novo suplemento](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="ff961-147">Procure por **mensagem de relatório**e, na lista de resultados, ao lado do **suplemento de mensagem de relatório**, escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="ff961-148">![Procure por mensagem de relatório e escolha Adicionar](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="ff961-149">Na tela de **mensagens de relatório** , revise as informações e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="ff961-150">![Detalhes da mensagem de relatório](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="ff961-151">Especifique as configurações padrão do usuário para o Outlook e, em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="ff961-152">![Configurações padrão de mensagens de relatório para o Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="ff961-153">Especifique quem recebe o suplemento de mensagem de relatório e, em seguida, escolha **salvar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="ff961-154">![Quem recebe o suplemento de mensagem de relatório](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="ff961-155">Recomendamos [Configurar uma regra para obter uma cópia das mensagens de email relatadas por seus usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="ff961-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="ff961-p107">Dependendo do que você selecionou quando configurou o suplemento (etapas 7-8 acima), as pessoas em sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponível. As pessoas na sua organização verão os seguintes ícones:</span><span class="sxs-lookup"><span data-stu-id="ff961-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="ff961-158">No Outlook, o ícone tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="ff961-158">In Outlook, the icon looks like this:</span></span> <br/> ![Ícone de suplemento de mensagem de relatório para Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="ff961-160">No Outlook na Web, o ícone tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="ff961-160">In Outlook on the web, the icon looks like this:</span></span><br/>![Ícone de suplemento da mensagem de relatório da Web do Outlook](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="ff961-162">Ao notificar os usuários sobre o suplemento de mensagens de relatório, inclua um link para [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="ff961-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="ff961-163">Configurar uma regra para obter uma cópia das mensagens de email relatadas por seus usuários</span><span class="sxs-lookup"><span data-stu-id="ff961-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff961-164">Você deve ser um administrador do Exchange Online para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff961-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="ff961-p108">Você pode configurar uma regra para obter uma cópia das mensagens de email relatadas por usuários em sua organização. Faça isso depois de baixar e habilitar o suplemento de mensagem de relatório para sua organização.</span><span class="sxs-lookup"><span data-stu-id="ff961-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="ff961-167">No centro de administração do Exchange, escolha **regras**de **fluxo** \> de email.</span><span class="sxs-lookup"><span data-stu-id="ff961-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="ff961-168">Escolha **+** \> **criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="ff961-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="ff961-169">Na caixa **nome** , digite um nome, como envios.</span><span class="sxs-lookup"><span data-stu-id="ff961-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="ff961-170">Na lista **aplicar esta regra se** , escolha **o endereço do destinatário inclui..**.</span><span class="sxs-lookup"><span data-stu-id="ff961-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="ff961-171">Na tela **especificar palavras ou frases** , adicione `junk@office365.microsoft.com` e `phish@office365.microsoft.com`, em seguida, escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff961-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="ff961-172">![Especificar os endereços de email de lixo eletrônico e phishing da regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="ff961-173">Na lista **faça o seguinte...** , escolha **Cco a mensagem para..**..</span><span class="sxs-lookup"><span data-stu-id="ff961-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="ff961-174">Adicione um administrador global, um administrador de segurança e/ou um leitor de segurança que deve receber uma cópia de cada mensagem de email que as pessoas relatam à Microsoft e, em seguida, escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff961-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="ff961-175">![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="ff961-176">Selecione **auditar esta regra com nível de severidade**e escolha **médio**.</span><span class="sxs-lookup"><span data-stu-id="ff961-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="ff961-177">Em **escolher um modo para essa regra**, escolha **impor**.</span><span class="sxs-lookup"><span data-stu-id="ff961-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="ff961-178">![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="ff961-179">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ff961-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="ff961-p109">Com essa regra em vigor, sempre que alguém em sua organização relatar uma mensagem de email usando o suplemento de mensagem de relatório, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia dessa mensagem. Essas informações podem permitir que você configure ou ajuste políticas, como as políticas de [links seguros de ATP do Office 365](atp-safe-links.md) ou suas configurações [antispam](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="ff961-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="ff961-182">Saiba como usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="ff961-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="ff961-183">ConFira [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="ff961-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="ff961-184">Revise ou edite as configurações do suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="ff961-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="ff961-185">Você pode revisar e editar as configurações padrão para o suplemento de mensagem de relatório na [página de suplementos de serviços do &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="ff961-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ff961-186">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para concluir essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff961-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="ff961-187">Vá para a [página de suplementos de serviços do &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ff961-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="ff961-188">![Página serviços e suplementos no novo centro de administração do Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="ff961-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="ff961-189">Localize e selecione o suplemento de mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="ff961-189">Find and select the Report Message add-in.</span></span><br/>![Localizar e selecionar o suplemento de mensagem de relatório](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="ff961-191">Na tela de mensagens de relatório, revise e edite as configurações conforme apropriado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="ff961-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Configurações para o suplemento de mensagem de relatório](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="ff961-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff961-193">Related topics</span></span>

[<span data-ttu-id="ff961-194">Usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="ff961-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="ff961-195">Exibir relatórios de segurança de email no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="ff961-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="ff961-196">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ff961-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="ff961-197">Usar o Explorer no centro &amp; de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="ff961-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

