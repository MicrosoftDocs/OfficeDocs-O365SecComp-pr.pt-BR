---
title: Habilitar o suplemento de Mensagem de relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: ad07d594a78b8134984b48f08898ad1ba697e03a
ms.sourcegitcommit: 49b565f6a57febe53f331b2605d6a06d11e2d0be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/18/2018
ms.locfileid: "25638005"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="e7b4d-103">Habilitar o suplemento de Mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="e7b4d-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="e7b4d-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e7b4d-104">Overview</span></span>

<span data-ttu-id="e7b4d-p101">O suplemento de mensagem de relatório para o Outlook e Outlook na Web permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando [A proteção de ameaça avançadas do Office 365](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornece equipe de segurança da sua organização com informações úteis, que eles podem usar para analisar e atualizar diretivas de segurança.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="e7b4d-p102">Por exemplo, suponha que as pessoas são relatórios muitas mensagens como phishing. Este mostra informações no [Painel de segurança](security-dashboard.md) e outros relatórios. Equipe de segurança da sua organização pode usar essas informações como uma indicação de que as políticas de AntiPhishing talvez precisem ser atualizados. Ou, se as pessoas estão relatando muita mensagens que foram sinalizados como lixo eletrônico, como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, talvez seja necessário ajustar o [políticas antispam](configure-the-anti-spam-policies.md)equipe de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="e7b4d-112">O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e produtos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="e7b4d-113">Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="e7b4d-113">Outlook on the Web</span></span>
 - <span data-ttu-id="e7b4d-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="e7b4d-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="e7b4d-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b4d-115">Outlook 2016</span></span>
 - <span data-ttu-id="e7b4d-116">Outlook 2016 para Mac</span><span class="sxs-lookup"><span data-stu-id="e7b4d-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="e7b4d-117">Outlook incluído com o Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="e7b4d-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="e7b4d-118">Se você for um usuário individual, você pode [Habilitar o suplemento de mensagem de relatório por conta própria](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="e7b4d-119">Se você for um administrador do Exchange Online, você pode [Habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-119">If you're an Exchange Online administrator, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="e7b4d-120">Obtenha a mensagem de relatório suplemento para si mesmo</span><span class="sxs-lookup"><span data-stu-id="e7b4d-120">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="e7b4d-121">Em que o [Office armazenar](https://appsource.microsoft.com/product/office/WA104381180?src=office), obtenha a mensagem de relatório suplemento.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-121">In the [Office store](https://appsource.microsoft.com/product/office/WA104381180?src=office), get the Report Message add-in.</span></span>
    
2. <span data-ttu-id="e7b4d-122">Escolha **GET IT agora**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-122">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="e7b4d-123">![Relatar mensagem - obtê-lo agora](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-123">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="e7b4d-p103">Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p103">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="e7b4d-126">Entrar no seu email do Office 365 usando seu trabalho ou a conta de escola (para uso de negócios) ou a sua conta da Microsoft (para uso pessoal).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-126">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    

<span data-ttu-id="e7b4d-127">Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-127">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="e7b4d-128">No Outlook no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-128">In Outlook the icon looks like this:</span></span> <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="e7b4d-130">No Outlook Web App no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-130">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="e7b4d-132">Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-132">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="e7b4d-133">Obter e habilitar o suplemento de mensagem de relatório para sua organização</span><span class="sxs-lookup"><span data-stu-id="e7b4d-133">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7b4d-134">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-134">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>

1. <span data-ttu-id="e7b4d-135">Vá para [https://portal.office.com](https://portal.office.com) e entrar usando sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-135">Go to [https://portal.office.com](https://portal.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="e7b4d-136">Escolha **Admin** para ir para o Centro de administração.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-136">Choose **Admin** to go to the Admin center.</span></span> 
    
3. <span data-ttu-id="e7b4d-137">Escolha **Admin centrais** \> **Exchange** para ir para o Centro de administração do Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-137">Choose **Admin centers** \> **Exchange** to go to the Exchange admin center (EAC).</span></span> 
    
4. <span data-ttu-id="e7b4d-138">Escolha **organização** \> **suplementos**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-138">Choose **organization** \> **add-ins**.</span></span> 
    
5. <span data-ttu-id="e7b4d-139">Escolha **+**  >  **Adicionar da Office Store**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-139">Choose **+** > **Add from the Office Store**.</span></span><br/><span data-ttu-id="e7b4d-140">![Escolha Adicionar da Office Store](media/EAC-Org-AddFromOfficeStore.png)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-140">![Choose Add from the Office Store](media/EAC-Org-AddFromOfficeStore.png)</span></span><br/><span data-ttu-id="e7b4d-141">Isso abre a Office Store no seu navegador da web.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-141">This opens the Office Store in your web browser.</span></span>
    
6. <span data-ttu-id="e7b4d-142">Procure a mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-142">Search for Report Message.</span></span><br/>![Procure a mensagem de relatório](media/ReportMessageSearchOfficeStore.png)<br/>
    
7. <span data-ttu-id="e7b4d-144">Na lista de **aplicativos** , selecione **A mensagem de relatório**e escolha **Obter TI agora**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-144">In the **Apps** list, select **Report Message**, and then choose **GET IT NOW**.</span></span><br/><span data-ttu-id="e7b4d-145">![Escolha GET IT agora](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-145">![Choose GET IT NOW](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
8. <span data-ttu-id="e7b4d-p104">Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
    ![Clique em Continuar para aceitar os termos e a diretiva de privacidade](media/ReportMessageTermsAndConditions.png)
  
9. <span data-ttu-id="e7b4d-p105">Um assistente é aberto para ajudá-lo a configurar as informações de revisão de suplemento a mensagem de relatório e escolha **próximo** para continuar.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p105">A wizard opens to help you configure the Report Message add-in. Review the information, and choose **Next** to continue.</span></span><br/><span data-ttu-id="e7b4d-151">![Mensagem suplemento do Assistente de relatório para o Office 365](media/ReportMessageAdminInstallUI.png)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-151">![Report Message add-in wizard for Office 365](media/ReportMessageAdminInstallUI.png)</span></span><br/> 

10. <span data-ttu-id="e7b4d-152">Especifique a configuração padrão que você deseja atribuir ao usuário para o suplemento de mensagem de relatório.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-152">Specify the default setting you want users to have for the Report Message add-in.</span></span><br/>![Especificar configurações padrão para o suplemento de mensagem de relatório](media/ReportMessageUserOptionsAdminsSet.png)<br/>
    
11. <span data-ttu-id="e7b4d-154">Especifica quem obtém a mensagem de relatório suplemento.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-154">Specify who gets the Report Message add-in.</span></span> <br/>![Especificar quem obtém a mensagem de relatório de suplemento](media/ReportMessageChooseWhoGetsItAdminSettings.png)<br/>

12. <span data-ttu-id="e7b4d-156">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-156">Choose **Save**.</span></span> <br/>
> [!TIP]
> <span data-ttu-id="e7b4d-157">Recomendamos a [configuração de uma regra para obter uma cópia das mensagens de email relatado pelos usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-157">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="e7b4d-p106">Dependendo do que você selecionou usando o assistente, pessoas da sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponíveis. Pessoas da sua organização verá os ícones a seguir:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="e7b4d-160">No Outlook no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-160">In Outlook the icon looks like this:</span></span> <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="e7b4d-162">No Outlook Web App no ícone tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="e7b4d-162">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="e7b4d-164">Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários</span><span class="sxs-lookup"><span data-stu-id="e7b4d-164">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7b4d-165">Você deve ser um administrador do Exchange Online para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-165">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="e7b4d-p107">Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="e7b4d-168">No EAC, selecione o **fluxo de email** \> **regras**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-168">In the EAC, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="e7b4d-169">Escolha **+** \> **criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-169">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="e7b4d-170">Na caixa **nome** , digite um nome, como envios.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-170">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="e7b4d-171">Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-171">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="e7b4d-172">Na tela **Especificar palavras ou expressões** , adicione junk@office365.microsoft.com e phish@office365.microsoft.com e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-172">In the **specify words or phrases** screen, add junk@office365.microsoft.com and phish@office365.microsoft.com, and then choose **OK**.</span></span> 
    
    ![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. <span data-ttu-id="e7b4d-174">Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-174">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="e7b4d-175">Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-175">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span> 
    
    ![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. <span data-ttu-id="e7b4d-177">Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-177">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="e7b4d-178">Em **Escolher um modo para essa regra**, escolha **Enforce**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-178">Under **Choose a mode for this rule**, choose **Enforce**.</span></span> 
    
    ![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. <span data-ttu-id="e7b4d-180">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-180">Choose **Save**.</span></span> 
    
<span data-ttu-id="e7b4d-p108">Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-the-default-settings-for-the-report-message-add-in"></a><span data-ttu-id="e7b4d-183">Analisar ou editar as configurações padrão para o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="e7b4d-183">Review or edit the default settings for the Report Message add-in</span></span>

<span data-ttu-id="e7b4d-184">Você pode analisar e editar as configurações padrão para o suplemento de mensagem de relatório usando o Centro de administração.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-184">You can review and edit the default settings for the Report Message add-in using the Admin Center.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e7b4d-185">Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-185">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="e7b4d-p109">Se apenas, você instalou o suplemento de mensagem de relatório para sua organização, você já será na página serviços e suplementos. Caso contrário, vá [aqui](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) e entrar usando sua conta de trabalho ou da escola para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-p109">If you've just installed the Report Message add-in for your organization, you'll already be on the Services & add-ins page. Otherwise, go [here](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="e7b4d-188">Procure a **Mensagem de relatório**e selecioná-lo.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-188">Search for **Report Message**, and then select it.</span></span><br/><span data-ttu-id="e7b4d-189">![Serviços e suplementos para o Office 365](media/ReportMessage-o365servicesaddins.png)</span><span class="sxs-lookup"><span data-stu-id="e7b4d-189">![Services and add-ins for Office 365](media/ReportMessage-o365servicesaddins.png)</span></span><br/> 
    
3. <span data-ttu-id="e7b4d-190">Um painel aberto que exibe as configurações que foram selecionadas para o suplemento de mensagem de relatório durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-190">A pane opens that displays the settings that were selected for the Report Message add-in during deployment.</span></span><br/>![Configurações para o suplemento de mensagem de relatório](media/ReportMessage-reviewaddinsettings.png)<br/> 

4. <span data-ttu-id="e7b4d-192">Revise e, se necessário, editar configurações para o suplemento de mensagem de relatório e salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="e7b4d-192">Review and if needed, edit settings for the Report Message add-in, and then save your changes.</span></span>
    
## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="e7b4d-193">Saiba como usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="e7b4d-193">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="e7b4d-194">Consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="e7b4d-194">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="e7b4d-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7b4d-195">Related topics</span></span>

[<span data-ttu-id="e7b4d-196">Usar o suplemento de mensagem de relatório</span><span class="sxs-lookup"><span data-stu-id="e7b4d-196">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="e7b4d-197">Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="e7b4d-197">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="e7b4d-198">Exibir relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="e7b4d-198">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="e7b4d-199">Use o Explorer na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="e7b4d-199">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

