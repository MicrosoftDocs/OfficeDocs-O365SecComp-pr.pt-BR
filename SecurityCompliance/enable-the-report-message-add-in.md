---
title: Habilitar o suplemento de Mensagem de relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: f35899d3f0be9ee07cb6dae5c5fec40395948340
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706365"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="968a5-103">Habilitar o suplemento de Mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="968a5-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="968a5-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="968a5-104">Overview</span></span>

<span data-ttu-id="968a5-p101">O suplemento de mensagem de relatório para o Outlook e Outlook na Web permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando [A proteção de ameaça avançadas do Office 365](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornece equipe de segurança da sua organização com informações úteis, que eles podem usar para analisar e atualizar diretivas de segurança.</span><span class="sxs-lookup"><span data-stu-id="968a5-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="968a5-p102">Por exemplo, suponha que as pessoas são relatórios muitas mensagens como phishing. Este mostra informações no [Painel de segurança](security-dashboard.md) e outros relatórios. Equipe de segurança da sua organização pode usar essas informações como uma indicação de que as políticas de AntiPhishing talvez precisem ser atualizados. Ou, se as pessoas estão relatando muita mensagens que foram sinalizados como lixo eletrônico, como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, talvez seja necessário ajustar o [políticas antispam](configure-the-anti-spam-policies.md)equipe de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="968a5-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="968a5-112">O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e produtos a seguir:</span><span class="sxs-lookup"><span data-stu-id="968a5-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="968a5-113">Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="968a5-113">Outlook on the Web</span></span>
 - <span data-ttu-id="968a5-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="968a5-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="968a5-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="968a5-115">Outlook 2016</span></span>
 - <span data-ttu-id="968a5-116">Outlook 2016 para Mac</span><span class="sxs-lookup"><span data-stu-id="968a5-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="968a5-117">Outlook incluído com o Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="968a5-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="968a5-118">Se você for um usuário individual, você pode [Habilitar o suplemento de mensagem de relatório por conta própria](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="968a5-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="968a5-p103">Se você é um administrador global do Office 365 ou um administrador do Exchange Online e Exchange está configurado para usar a autenticação OAuth, você pode [Habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization). O suplemento do relatório de mensagem agora está disponível por meio da [Implantação centralizados](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="968a5-p103">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="968a5-121">Obtenha a mensagem de relatório suplemento para si mesmo</span><span class="sxs-lookup"><span data-stu-id="968a5-121">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="968a5-122">No [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), procure o [suplemento de mensagem de relatório](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="968a5-122">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="968a5-123">Escolha **GET IT agora**.</span><span class="sxs-lookup"><span data-stu-id="968a5-123">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="968a5-124">![Relatar mensagem - obtê-lo agora](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-124">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="968a5-p104">Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="968a5-127">Entrar no seu email do Office 365 usando seu trabalho ou a conta de escola (para uso de negócios) ou a sua conta da Microsoft (para uso pessoal).</span><span class="sxs-lookup"><span data-stu-id="968a5-127">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="968a5-128">Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="968a5-128">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="968a5-129">No Outlook no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="968a5-129">In Outlook the icon looks like this:</span></span> <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="968a5-131">No Outlook Web App no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="968a5-131">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="968a5-133">Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="968a5-133">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="968a5-134">Obter e habilitar o suplemento de mensagem de relatório para sua organização</span><span class="sxs-lookup"><span data-stu-id="968a5-134">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="968a5-p105">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa. Além disso, o Exchange deve ser configurado para usar a autenticação OAuth para saber mais, consulte [requisitos do Exchange (centralizados implantação dos suplementos)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="968a5-p105">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="968a5-137">Ir para a [página de suplementos & serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365 novo.</span><span class="sxs-lookup"><span data-stu-id="968a5-137">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="968a5-138">![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-138">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="968a5-139">Escolha **+ implantar o suplemento**.</span><span class="sxs-lookup"><span data-stu-id="968a5-139">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="968a5-140">![Escolha implantar o suplemento](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-140">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="968a5-141">Na tela do novo suplemento, revise as informações e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-141">In the New Add-In screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="968a5-142">![Detalhes do novo suplemento](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-142">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="968a5-143">Selecione **eu quiser adicionar um suplemento da Office Store**e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-143">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="968a5-144">![Eu quiser adicionar um novo suplemento](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-144">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="968a5-145">Pesquisa de mensagem de relatório e na lista de resultados, ao lado do relatório de mensagem suplemento, escolha Adicionar.</span><span class="sxs-lookup"><span data-stu-id="968a5-145">Search for Report Message, and in the list of results, next to the Report Message Add-In, choose Add.</span></span><br/>![Procure a mensagem de relatório e escolha Adicionar](media/NewAddInScreen3.png)<br/>
    
6. <span data-ttu-id="968a5-147">Na tela de mensagem de relatório, revise as informações e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-147">On the Report Message screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="968a5-148">![Detalhes da mensagem de relatório](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-148">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="968a5-149">Especifique as configurações de usuário padrão para o Outlook e escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-149">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="968a5-150">![Relatar as configurações padrão de mensagem do Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-150">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="968a5-151">Especificar quem obtém o suplemento de mensagem de relatório e escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-151">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="968a5-152">![Quem obtém a mensagem de relatório suplemento](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-152">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="968a5-153">Recomendamos a [configuração de uma regra para obter uma cópia das mensagens de email relatado pelos usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span><span class="sxs-lookup"><span data-stu-id="968a5-153">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="968a5-p106">Dependendo do que você selecionou usando o assistente, pessoas da sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponíveis. Pessoas da sua organização verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="968a5-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="968a5-156">No Outlook no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="968a5-156">In Outlook the icon looks like this:</span></span> <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="968a5-158">No Outlook Web App no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="968a5-158">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="968a5-160">Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários</span><span class="sxs-lookup"><span data-stu-id="968a5-160">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="968a5-161">Você deve ser um administrador do Exchange Online para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="968a5-161">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="968a5-p107">Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.</span><span class="sxs-lookup"><span data-stu-id="968a5-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="968a5-164">No Centro de administração do Exchange, escolha **fluxo de emails** \> **regras**.</span><span class="sxs-lookup"><span data-stu-id="968a5-164">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="968a5-165">Escolha **+** \> **criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="968a5-165">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="968a5-166">Na caixa **nome** , digite um nome, como envios.</span><span class="sxs-lookup"><span data-stu-id="968a5-166">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="968a5-167">Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**.</span><span class="sxs-lookup"><span data-stu-id="968a5-167">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="968a5-168">Na tela **Especificar palavras ou expressões** , adicione `junk@office365.microsoft.com` e `phish@office365.microsoft.com`e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="968a5-168">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="968a5-169">![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-169">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="968a5-170">Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**.</span><span class="sxs-lookup"><span data-stu-id="968a5-170">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="968a5-171">Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="968a5-171">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="968a5-172">![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-172">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="968a5-173">Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**.</span><span class="sxs-lookup"><span data-stu-id="968a5-173">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="968a5-174">Em **Escolher um modo para essa regra**, escolha **Enforce**.</span><span class="sxs-lookup"><span data-stu-id="968a5-174">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="968a5-175">![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-175">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="968a5-176">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="968a5-176">Choose **Save**.</span></span> 
    
<span data-ttu-id="968a5-p108">Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="968a5-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="968a5-179">Analisar ou editar as configurações para o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="968a5-179">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="968a5-180">Você pode examinar e editar as configurações padrão para o relatório de mensagem suplemento na [página serviços e suplementos](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="968a5-180">You can review and edit the default settings for the Report Message Add-In in the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="968a5-181">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="968a5-181">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="968a5-182">Ir para a [página de suplementos & serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365 novo.</span><span class="sxs-lookup"><span data-stu-id="968a5-182">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="968a5-183">![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="968a5-183">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="968a5-184">Localize e selecione o suplemento do relatório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="968a5-184">Find and select the Report Message Add-In.</span></span><br/>![Localize e selecione o suplemento de mensagem de relatório](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="968a5-186">Na tela de mensagem de relatório, revise e editar configurações, conforme apropriado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="968a5-186">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Configurações para o suplemento de mensagem de relatório](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="968a5-188">Saiba como usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="968a5-188">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="968a5-189">Consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="968a5-189">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="968a5-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="968a5-190">Related topics</span></span>

[<span data-ttu-id="968a5-191">Usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="968a5-191">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="968a5-192">Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="968a5-192">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="968a5-193">Exibir relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="968a5-193">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="968a5-194">Use o Explorer na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="968a5-194">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

