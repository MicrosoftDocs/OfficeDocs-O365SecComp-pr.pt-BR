---
title: Limpeza Automática Zero Hora – proteção contra spam e malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749315"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="63203-104">Limpeza Automática Zero Hora – proteção contra spam e malware</span><span class="sxs-lookup"><span data-stu-id="63203-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="63203-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="63203-105">Overview</span></span>

<span data-ttu-id="63203-p102">Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com malware, spam ou phishing que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado; email pode ser zapped devido ao conteúdo de email, URLs ou anexos.</span><span class="sxs-lookup"><span data-stu-id="63203-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="63203-108">ZAP está disponível com o Exchange Online Protection for incluído com qualquer assinatura do Office 365 que contenha caixas de correio Exchange Online padrão.</span><span class="sxs-lookup"><span data-stu-id="63203-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="63203-109">ZAP está ativado por padrão, mas as seguintes condições devem ser atendidas:</span><span class="sxs-lookup"><span data-stu-id="63203-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="63203-110">**Ação de spam** é definido para **mover a mensagem para a pasta Lixo eletrônico**.</span><span class="sxs-lookup"><span data-stu-id="63203-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="63203-111">Você também pode criar uma nova política de filtro de spam que se aplica somente a um conjunto de usuários se não desejar que todas as caixas de correio a ser filtrada pelo ZAP.</span><span class="sxs-lookup"><span data-stu-id="63203-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="63203-p103">Os usuários têm mantidos seu padrão configurações de lixo eletrônico e não tem desativado de proteção de lixo eletrônico. (Consulte [alterar o nível de proteção em que o filtro de lixo eletrônico](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) para obter detalhes sobre as opções de usuário no Outlook.)</span><span class="sxs-lookup"><span data-stu-id="63203-p103">Users have kept their default junk mail settings, and have not turned off junk email protection. (See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="63203-114">Como funciona o ZAP?</span><span class="sxs-lookup"><span data-stu-id="63203-114">How does ZAP work?</span></span>

<span data-ttu-id="63203-p104">Atualizações de assinaturas de mecanismo e malware antispam do Office 365 em tempo real em uma base diária. No entanto, os usuários ainda podem obter mal-intencionado mensagens entregues a suas caixas de entrada para uma variedade de motivos, incluindo se o conteúdo é aproveitado depois de ser entregue aos usuários. Apagar tudo isso por meio do monitoramento continuamente atualiza e as assinaturas do Office 365 spam e malware de endereços. ZAP pode encontrar e remover mensagens entregues anteriormente que já estão nas caixas de entrada dos usuários.</span><span class="sxs-lookup"><span data-stu-id="63203-p104">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures. ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 

- <span data-ttu-id="63203-119">Para email que é identificado como spam, ZAP move mensagens não lidas para a pasta Lixo eletrônico dos usuários.</span><span class="sxs-lookup"><span data-stu-id="63203-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 

- <span data-ttu-id="63203-120">Para email que é identificado como spam, ZAP move mensagens para a pasta de lixo eletrônico dos usuários, independentemente se o email foi lido.</span><span class="sxs-lookup"><span data-stu-id="63203-120">For mail that is identified as spam, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="63203-121">Para malware detectado recentemente, ZAP remove anexos das mensagens de email, independentemente se o email foi lido.</span><span class="sxs-lookup"><span data-stu-id="63203-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="63203-122">A ação ZAP é perfeita para o usuário de caixa de correio; eles não são notificados se uma mensagem de email for movida.</span><span class="sxs-lookup"><span data-stu-id="63203-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="63203-123">Permitir listas, [regras de fluxo de correio](https://go.microsoft.com/fwlink/p/?LinkId=722755)e regras do usuário final ou filtros adicionais têm precedência sobre ZAP.</span><span class="sxs-lookup"><span data-stu-id="63203-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="63203-124">Para revisar ou definir uma política de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="63203-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="63203-125">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="63203-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="63203-126">Em **gerenciamento de ameaça**, escolha **anti-spam**.</span><span class="sxs-lookup"><span data-stu-id="63203-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="63203-127">Revise as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="63203-127">Review the standard settings.</span></span> 

4. <span data-ttu-id="63203-p105">Se desejar personalizar suas configurações, selecione a guia **personalizada** e ativar **configurações personalizadas**. Editar suas configurações e, se desejar, escolha **+ criar uma política** para adicionar uma nova diretiva.</span><span class="sxs-lookup"><span data-stu-id="63203-p105">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**. Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="63203-130">Para ver se ZAP movida sua mensagem</span><span class="sxs-lookup"><span data-stu-id="63203-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="63203-131">Se você quiser ver se ZAP movida sua mensagem, você pode usar o [relatório de Status de proteção de ameaça](view-email-security-reports.md#threat-protection-status-report) (tanto na [Ameaça Explorer](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="63203-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="63203-132">Para desabilitar ZAP</span><span class="sxs-lookup"><span data-stu-id="63203-132">To disable ZAP</span></span>
  
<span data-ttu-id="63203-133">Se você deseja desabilitar Apagar tudo para seu locatário do Office 365 ou um conjunto de usuários, use o parâmetro **ZapEnabled** do [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet do EOP.</span><span class="sxs-lookup"><span data-stu-id="63203-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="63203-134">No exemplo a seguir, ZAP está desabilitado para uma política de filtro de conteúdo chamada "Test".</span><span class="sxs-lookup"><span data-stu-id="63203-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="63203-135">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="63203-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="63203-136">O que acontece se uma mensagem legítima é movida para a pasta Lixo eletrônico?</span><span class="sxs-lookup"><span data-stu-id="63203-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="63203-p106">Você deve seguir o processo de emissão normal de falsos positivos. A única razão seria movida a mensagem da caixa de entrada para a pasta Lixo eletrônico seria porque o serviço determinou que a mensagem foi spam ou mal intencionado.</span><span class="sxs-lookup"><span data-stu-id="63203-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="63203-139">Se usar a quarentena do Office 365 em vez da pasta de lixo eletrônico?</span><span class="sxs-lookup"><span data-stu-id="63203-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="63203-140">ZAP não move mensagens em quarentena na caixa de entrada no momento.</span><span class="sxs-lookup"><span data-stu-id="63203-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="63203-141">E se eu tiver uma regra de fluxo de email personalizado (bloquear / permitir regra)?</span><span class="sxs-lookup"><span data-stu-id="63203-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="63203-p107">Regras criadas por administradores (regras de fluxo de email) ou regras de bloqueio e permitir têm precedência. Essas mensagens são excluídas dos critérios de recurso.</span><span class="sxs-lookup"><span data-stu-id="63203-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="63203-144">Tópicos Relacionados</span><span class="sxs-lookup"><span data-stu-id="63203-144">Related Topics</span></span>

[<span data-ttu-id="63203-145">Proteção antispam de emails do Office 365</span><span class="sxs-lookup"><span data-stu-id="63203-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="63203-146">Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos</span><span class="sxs-lookup"><span data-stu-id="63203-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

