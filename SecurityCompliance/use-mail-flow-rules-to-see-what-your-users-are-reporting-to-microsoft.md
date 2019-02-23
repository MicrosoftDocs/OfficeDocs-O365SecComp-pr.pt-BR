---
title: Usar regras de fluxo de emails para ver o que seus usuários estão relatando para a Microsoft
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email para a Microsoft para análise e usá-las em seus próprios processos de segurança
ms.openlocfilehash: 7ee8fb2bca1071ccd4080379485c1670a5e66a73
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206404"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="4c8ca-103">Usar regras de fluxo de emails para ver o que seus usuários estão relatando para a Microsoft</span><span class="sxs-lookup"><span data-stu-id="4c8ca-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="4c8ca-p101">Há várias maneiras pelas quais você pode enviar mensagens falsas positivas e falsas negativas para a Microsoft para análise. Como administrador, você pode usar regras de fluxo de email para ver o que seus usuários estão relatando à Microsoft como spam, não spam e golpes de phishing. Para obter mais informações, consulte [enviar mensagens de spam, não spam e golpes de phishing para a Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Por outro lado, você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email para a Microsoft para análise e usá-las em seus próprios processos de segurança.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4c8ca-108">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="4c8ca-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="4c8ca-109">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="4c8ca-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="4c8ca-p102">Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o entrada "regras de transporte" no tópico [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) e The "Outlook on the Web Mailbox Policies" no tópico [clients and Mobile](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) Devices Permissions.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook on the web mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="4c8ca-112">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de administração do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="4c8ca-113">Use o Eat para criar uma regra de fluxo de emails para exibir o lixo eletrônico, phishing e não os relatórios de lixo eletrônico</span><span class="sxs-lookup"><span data-stu-id="4c8ca-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="4c8ca-114">No EAC, navegue até **Fluxo de email** \> **Regras**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="4c8ca-115">Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="4c8ca-116">Dê um nome à regra e então clique em **Mais opções**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="4c8ca-117">Em **Aplicar esta regra se**, selecione **O destinatário** e escolha **endereço inclui qualquer uma destas palavras**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="4c8ca-118">Na caixa **especificar palavras ou frases**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c8ca-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="4c8ca-p103">Digite `abuse@messaging.microsoft.com` e, em ![seguida,](media/ITPro-EAC-AddIcon.gif)clique em Adicionar ícone `junk@office365.microsoft.com` e digite e ![, em](media/ITPro-EAC-AddIcon.gif)seguida, clique em Adicionar ícone. Esses endereços de email são usados para enviar mensagens negativas falsas para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p103">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="4c8ca-p104">Digite `phish@office365.microsoft.com` e clique em ![adicionar ícone](media/ITPro-EAC-AddIcon.gif). Esse endereço de email é usado para enviar mensagens de phishing perdidas para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p104">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="4c8ca-p105">Digite `false_positive@messaging.microsoft.com` e, em ![seguida,](media/ITPro-EAC-AddIcon.gif)clique em Adicionar ícone `not_junk@office365.microsoft.com` e digite e ![, em](media/ITPro-EAC-AddIcon.gif)seguida, clique em Adicionar ícone. Esses endereços de email são usados para enviar mensagens positivas falsas para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p105">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="4c8ca-125">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="4c8ca-126">Em **faça o seguinte**, selecione **Cco a mensagem para...** e, em seguida, selecione as caixas de correio nas quais você gostaria de receber as mensagens.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="4c8ca-p106">Se quiser, você pode fazer seleções para auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. Recomendamos testar a regra por um período antes de aplicá-la. Consulte [procedimentos para regras de fluxo de emails](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="4c8ca-p107">Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="4c8ca-132">Depois de criar e impor a regra, todas as mensagens enviadas da sua organização para os endereços de email especificados serão copiadas para a caixa de correio especificada.</span><span class="sxs-lookup"><span data-stu-id="4c8ca-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

