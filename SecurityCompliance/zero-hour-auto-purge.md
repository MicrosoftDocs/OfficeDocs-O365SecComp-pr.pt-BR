---
title: Limpeza automática de zero horas-proteção contra spam e malware
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: A limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos seus usuários e renderiza o conteúdo mal-intencionado inofensivo. Como o ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.
ms.openlocfilehash: b28de1b05843e3f5b0f6e7fc905c96f094c277f9
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524015"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="8d7a3-104">Limpeza automática de zero horas-proteção contra spam e malware</span><span class="sxs-lookup"><span data-stu-id="8d7a3-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="8d7a3-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="8d7a3-105">Overview</span></span>

<span data-ttu-id="8d7a3-106">A limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com phishing, spam ou malware que já foram entregues às caixas de entrada dos seus usuários e renderiza o conteúdo mal-intencionado inofensivo.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="8d7a3-107">Como o ZAP depende do tipo de conteúdo mal-intencionado detectado; os emails podem ser zapped devido a conteúdo, URLs ou anexos de email.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="8d7a3-108">O ZAP está disponível com a proteção do Exchange Online padrão incluída em qualquer assinatura do Office 365 que contenha caixas de correio do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="8d7a3-109">O ZAP é ativado por padrão, mas as seguintes condições devem ser atendidas:</span><span class="sxs-lookup"><span data-stu-id="8d7a3-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="8d7a3-110">A **ação de spam** é definida para **mover a mensagem para a pasta lixo eletrônico**.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="8d7a3-111">Você também pode criar uma nova política de filtro de spam que se aplique somente a um conjunto de usuários se não quiser que todas as caixas de correio sejam filtradas por ZAP.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="8d7a3-112">Os usuários mantiveram suas configurações de lixo eletrônico padrão e não desativaram a proteção de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="8d7a3-113">(Consulte [alterar o nível de proteção no filtro de lixo eletrônico](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) para obter detalhes sobre as opções do usuário no Outlook.)</span><span class="sxs-lookup"><span data-stu-id="8d7a3-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="8d7a3-114">Como o ZAP funciona?</span><span class="sxs-lookup"><span data-stu-id="8d7a3-114">How does ZAP work?</span></span>

<span data-ttu-id="8d7a3-115">O Office 365 atualiza as assinaturas de malware e mecanismo antispam em tempo real diariamente.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="8d7a3-116">No enTanto, os usuários ainda podem obter mensagens mal-intencionadas entregues às suas caixas de entrada por vários motivos, incluindo se o conteúdo é enarmado depois de ser entregue aos usuários.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="8d7a3-117">O ZAP aborda isso ao monitorar atualizações continuamente nas assinaturas de spam e malware do Office 365.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="8d7a3-118">ZAP pode localizar e remover mensagens entregues anteriormente que já estão nas caixas de entrada dos usuários.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 

- <span data-ttu-id="8d7a3-119">Para email identificado como spam, o ZAP move as mensagens não lidas para a pasta lixo eletrônico dos usuários.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 

- <span data-ttu-id="8d7a3-120">Para email identificado como Phish, o ZAP move mensagens para a pasta lixo eletrônico dos usuários, independentemente se o email foi lido.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-120">For mail that is identified as phish, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="8d7a3-121">Para malware recém detectado, ZAP remove anexos de mensagens de email, independentemente de o email ter sido lido.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="8d7a3-122">A ação ZAP é transparente para o usuário da caixa de correio; Eles não são notificados quando uma mensagem de email é movida.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="8d7a3-123">As listas de permissões, [as regras de fluxo](https://go.microsoft.com/fwlink/p/?LinkId=722755)de emails e as regras de usuário final ou filtros adicionais têm precedência sobre o zap.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="8d7a3-124">Para revisar ou configurar uma política de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="8d7a3-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="8d7a3-125">AcEsse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="8d7a3-126">Em **Gerenciamento de ameaças**, escolha **anti-spam**.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="8d7a3-127">Revise as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-127">Review the standard settings.</span></span> 

4. <span data-ttu-id="8d7a3-128">Se você quiser personalizar suas configurações, selecione a guia **personalizado** e ative **as configurações personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-128">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**.</span></span> <span data-ttu-id="8d7a3-129">Edite suas configurações e, se desejar, escolha **+ criar uma política** para adicionar uma nova política.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-129">Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="8d7a3-130">Para ver se ZAP moveu sua mensagem</span><span class="sxs-lookup"><span data-stu-id="8d7a3-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="8d7a3-131">Se você deseja ver se ZAP moveu sua mensagem, pode usar o relatório de [status de proteção contra ameaças](view-email-security-reports.md#threat-protection-status-report) (ou o [Gerenciador de ameaças](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="8d7a3-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="8d7a3-132">Para desabilitar o ZAP</span><span class="sxs-lookup"><span data-stu-id="8d7a3-132">To disable ZAP</span></span>
  
<span data-ttu-id="8d7a3-133">Se você quiser desabilitar o ZAP para o seu locatário do Office 365, ou um conjunto de usuários, use o parâmetro **ZapEnabled** de [set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet EOP.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="8d7a3-134">No exemplo a seguir, o ZAP é desabilitado para uma política de filtro de conteúdo chamada "Test".</span><span class="sxs-lookup"><span data-stu-id="8d7a3-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="8d7a3-135">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="8d7a3-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="8d7a3-136">O que acontece se uma mensagem legítima for movida para a pasta lixo eletrônico?</span><span class="sxs-lookup"><span data-stu-id="8d7a3-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="8d7a3-137">Você deve seguir o processo de relatório normal para falsos positivos.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-137">You should follow the normal reporting process for false-positives.</span></span> <span data-ttu-id="8d7a3-138">A única razão pela qual a mensagem seria movida da caixa de entrada para a pasta lixo eletrônico seria porque o serviço determinou que a mensagem era spam ou mal-intencionada.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-138">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="8d7a3-139">E se eu usar a quarentena do Office 365 em vez da pasta lixo eletrônico?</span><span class="sxs-lookup"><span data-stu-id="8d7a3-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="8d7a3-140">ZAP não move mensagens para a quarentena da caixa de entrada neste momento.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="8d7a3-141">E se eu tiver uma regra de fluxo de emails personalizada (regra bloquear/permitir)?</span><span class="sxs-lookup"><span data-stu-id="8d7a3-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="8d7a3-142">Regras criadas por administradores (regras de fluxo de emails) ou regras de bloqueio e permissão têm precedência.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-142">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="8d7a3-143">Essas mensagens são excluídas dos critérios de recurso.</span><span class="sxs-lookup"><span data-stu-id="8d7a3-143">Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="8d7a3-144">Tópicos Relacionados</span><span class="sxs-lookup"><span data-stu-id="8d7a3-144">Related Topics</span></span>

[<span data-ttu-id="8d7a3-145">Proteção anti-spam de emails do Office 365</span><span class="sxs-lookup"><span data-stu-id="8d7a3-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="8d7a3-146">Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos</span><span class="sxs-lookup"><span data-stu-id="8d7a3-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)
  

