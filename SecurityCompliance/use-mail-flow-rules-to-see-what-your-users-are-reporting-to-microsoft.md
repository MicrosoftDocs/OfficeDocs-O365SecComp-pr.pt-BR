---
title: Usar regras de fluxo de email para ver o que os usuários são relatórios à Microsoft
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/23/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email à Microsoft para análise e usá-los em seus próprios processos de segurança
ms.openlocfilehash: f2376668e2a1a16eba9913178a100fc31763b227
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026768"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="148a2-103">Usar regras de fluxo de email para ver o que os usuários são relatórios à Microsoft</span><span class="sxs-lookup"><span data-stu-id="148a2-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="148a2-p101">Há várias maneiras que você pode enviar as mensagens negativas falsos positivas e falsos para a Microsoft para análise. Como administrador, você pode usar as regras de fluxo de correio para ver o que os usuários são relatórios para a Microsoft como spam, golpes de phishing e não spam. Para obter mais informações, consulte o [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Por outro lado, você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email à Microsoft para análise e usá-los em seus próprios processos de segurança.</span><span class="sxs-lookup"><span data-stu-id="148a2-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="148a2-108">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="148a2-108">What do you need to know before you begin?</span></span>
<span data-ttu-id="148a2-109"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="148a2-109"></span></span>

<span data-ttu-id="148a2-110">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="148a2-110">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="148a2-p102">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Regras de transporte" no tópico [permissões de política e conformidade de mensagens](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) e a entrada "Políticas de caixa de correio do Outlook Web App" no tópico [permissões de dispositivos móveis e clientes](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) .</span><span class="sxs-lookup"><span data-stu-id="148a2-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook Web App mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="148a2-113">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="148a2-113">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="148a2-114">Usar o EAC para criar uma regra de fluxo de email para exibir lixo manual, phishing e relatórios não sendo lixo eletrônico dos usuários</span><span class="sxs-lookup"><span data-stu-id="148a2-114">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>
<span data-ttu-id="148a2-115"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="148a2-115"></span></span>

1. <span data-ttu-id="148a2-116">No EAC, navegue até **Fluxo de email** \> **Regras**.</span><span class="sxs-lookup"><span data-stu-id="148a2-116">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="148a2-117">Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png) e em seguida, selecione **Criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="148a2-117">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="148a2-118">Dê um nome à regra e então clique em **Mais opções**.</span><span class="sxs-lookup"><span data-stu-id="148a2-118">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="148a2-119">Em **Aplicar esta regra se**, selecione **O destinatário** e escolha **endereço inclui qualquer uma destas palavras**.</span><span class="sxs-lookup"><span data-stu-id="148a2-119">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="148a2-120">Na caixa **especificar palavras ou frases**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="148a2-120">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="148a2-p103">Digite **abuse@messaging.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png); depois digite **junk@office365.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esses endereços de email são usados para enviar mensagens de falso negativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="148a2-p103">Type **abuse@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="148a2-p104">Digite **phish@office365.microsoft.com** e, em seguida, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esse endereço de email é usado para enviar mensagens de phishing perdidas à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="148a2-p104">Type **phish@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="148a2-p105">Digite **false_positive@messaging.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png); depois digite **not_junk@office365.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esses endereços de email são usados para enviar mensagens de falso positivo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="148a2-p105">Type **false_positive@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **not_junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="148a2-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="148a2-127">Click **ok**.</span></span>
    
6. <span data-ttu-id="148a2-128">Em **faça o seguinte**, selecione **Cco da mensagem para...** e, em seguida e, em seguida, selecione as caixas de correio em que você gostaria de recebem as mensagens.</span><span class="sxs-lookup"><span data-stu-id="148a2-128">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="148a2-p106">Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. O tópico [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contém mais informações sobre estas seleções.</span><span class="sxs-lookup"><span data-stu-id="148a2-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contains more information about these selections.</span></span> 
    
8. <span data-ttu-id="148a2-p107">Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras.</span><span class="sxs-lookup"><span data-stu-id="148a2-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="148a2-134">Depois de criar e aplicar a regra, todas as mensagens que são enviadas de sua organização para os endereços de email especificados serão copiadas para a caixa de correio especificada.</span><span class="sxs-lookup"><span data-stu-id="148a2-134">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

