---
title: Limpeza Automática Zero Hora – proteção contra spam e malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
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
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857239"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="cebb3-104">Limpeza Automática Zero Hora – proteção contra spam e malware</span><span class="sxs-lookup"><span data-stu-id="cebb3-104">Zero-hour auto purge - protection against spam and malware</span></span>

<span data-ttu-id="cebb3-p102">Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="cebb3-107">ZAP está disponível com o Exchange Online Protection for incluído com qualquer assinatura do Office 365 que contenha caixas de correio Exchange Online padrão.</span><span class="sxs-lookup"><span data-stu-id="cebb3-107">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>
  
## <a name="how-does-zap-work"></a><span data-ttu-id="cebb3-108">Como funciona o ZAP?</span><span class="sxs-lookup"><span data-stu-id="cebb3-108">How does ZAP work?</span></span>

<span data-ttu-id="cebb3-p103">Atualizações de assinaturas de mecanismo e malware antispam do Office 365 em tempo real em uma base diária. No entanto, os usuários ainda podem obter mal-intencionado mensagens entregues a suas caixas de entrada para uma variedade de motivos, inclusive quando o conteúdo foi aproveitado por vez depois que ela foi entregue primeiro aos usuários. Apagar tudo isso por meio do monitoramento continuamente é atualizado para as assinaturas de spam e malware Office 365, de endereços e, portanto, encontrar e remover mensagens previamente distribuídas já nas caixas de entrada. Para email que já foi identificada como spam, ZAP move mensagens não lidas para pasta de lixo eletrônico do usuário. Para malware detectado recentemente, ZAP remove os anexos da mensagem de email, independentemente se o email foi lido ou não. O inverso é verdadeiro para mensagens que foram classificadas incorretamente como sendo maliciosas.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p103">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including when the content was weaponized at a time after it was first delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures, and can therefore find and remove previously delivered messages already in inboxes. For mail that was already identified as spam, ZAP moves unread messages to the user's Junk mail folder. For newly detected malware, ZAP removes the attachments from the email message, regardless of whether the mail was read or not. The reverse is true for messages that were incorrectly classified as malicious.</span></span>
  
<span data-ttu-id="cebb3-115">A ação ZAP é perfeita para o usuário de caixa de correio, ele ou ela não será notificada que de correio foi movida.</span><span class="sxs-lookup"><span data-stu-id="cebb3-115">The ZAP action is seamless for the mailbox user, he or she is not notified the mail has been moved.</span></span>
  
<span data-ttu-id="cebb3-116">Permitir listas, [regras de fluxo de correio](https://go.microsoft.com/fwlink/p/?LinkId=722755)e regras do usuário final ou filtros adicionais têm precedência sobre ZAP.</span><span class="sxs-lookup"><span data-stu-id="cebb3-116">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
 <span data-ttu-id="cebb3-117">**Neste artigo:**</span><span class="sxs-lookup"><span data-stu-id="cebb3-117">**In this article:**</span></span>
  
> [<span data-ttu-id="cebb3-118">Definir a política de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="cebb3-118">Set spam filter policy</span></span>](zero-hour-auto-purge.md#BK_SetSpam)
    
> [<span data-ttu-id="cebb3-119">Consulte se ZAP movidos sua mensagem</span><span class="sxs-lookup"><span data-stu-id="cebb3-119">See if ZAP moved your message</span></span>](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [<span data-ttu-id="cebb3-120">Desabilitar ZAP</span><span class="sxs-lookup"><span data-stu-id="cebb3-120">Disable ZAP</span></span>](zero-hour-auto-purge.md#BK_Posh)
    
> [<span data-ttu-id="cebb3-121">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="cebb3-121">FAQ</span></span>](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a><span data-ttu-id="cebb3-122">Trabalhando com ZAP</span><span class="sxs-lookup"><span data-stu-id="cebb3-122">Working with ZAP</span></span>

<span data-ttu-id="cebb3-123">ZAP está ativado por padrão, mas você precisará certificar-se de que algumas das condições forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="cebb3-123">ZAP is turned on by default, but you do have to make sure a couple of conditions are met:</span></span>
  
- <span data-ttu-id="cebb3-124">Política de filtro de spam é definida para [mover a mensagem para a pasta Lixo eletrônico](zero-hour-auto-purge.md#BK_SetSpam).</span><span class="sxs-lookup"><span data-stu-id="cebb3-124">Spam filter policy is set to [Move message to Junk Email folder](zero-hour-auto-purge.md#BK_SetSpam).</span></span>
    
    <span data-ttu-id="cebb3-125">Você também pode criar uma nova política de filtro de spam que se aplica somente a um conjunto de usuários se não desejar que todas as caixas de correio a ser filtrada pelo ZAP.</span><span class="sxs-lookup"><span data-stu-id="cebb3-125">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>
    
- <span data-ttu-id="cebb3-126">O usuário [opções \> lixo eletrônico](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span><span class="sxs-lookup"><span data-stu-id="cebb3-126">The user's [Options \> Junk Email](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span></span>
    
<span data-ttu-id="cebb3-127">Se você quiser [ver se ZAP movida sua mensagem](zero-hour-auto-purge.md#BK_DidZAPMove), você pode usar a ferramenta de rastreamento de mensagem do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cebb3-127">If you want [to see if ZAP moved your message](zero-hour-auto-purge.md#BK_DidZAPMove), you can use the Exchange Online message trace tool.</span></span>
  
<span data-ttu-id="cebb3-128">Os administradores também podem [Desabilitar ZAP](zero-hour-auto-purge.md#BK_Posh) usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cebb3-128">Admins can also [disable ZAP](zero-hour-auto-purge.md#BK_Posh) by using PowerShell.</span></span> 
  
 <span data-ttu-id="cebb3-129">**Para definir a política de filtro de spam**</span><span class="sxs-lookup"><span data-stu-id="cebb3-129">**To set spam filter policy**</span></span>
  
1. <span data-ttu-id="cebb3-130">Entrar no [Where entrar no Office 365 para empresas](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) e escolha **proteção** \> **filtro de spam**.</span><span class="sxs-lookup"><span data-stu-id="cebb3-130">Sign in to the [Where to sign in to Office 365 for business](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) and choose **protection** \> **spam filter**.</span></span> 
    
    ![No EAC, escolha a proteção e, em seguida, o filtro de spam](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. <span data-ttu-id="cebb3-132">Escolha a política de filtro que você deseja ajustar, ou escolha **Adicionar**![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="cebb3-132">Either choose the filter policy you want to adjust, or choose **add**![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) to create a new one.</span></span> 
    
    <span data-ttu-id="cebb3-p104">A captura de tela anterior, a política é chamada "Default", mas se você criar políticas de filtro de spam adicional podem fornecer-lhes um nome diferente. Você também pode aplicar a política a apenas um conjunto limitado de usuários.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p104">In the previous screen shot, the policy is named "Default", but if you create additional spam filter policies you can give them a different name. You can also apply the policy to only a limited set of users.</span></span>
    
3. <span data-ttu-id="cebb3-135">Na janela de política, escolha **ações em massa e de spam**e certifique-se de que o **Spam** seja definido como **Mover mensagem para a pasta Lixo eletrônico**.</span><span class="sxs-lookup"><span data-stu-id="cebb3-135">In the policy window, choose **spam and bulk actions**, and make sure that **Spam** is set to **Move message to Junk Email folder**.</span></span> 
    
    <span data-ttu-id="cebb3-136">Se você escolher **Salvar** neste ponto, a política se aplica ao seu locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="cebb3-136">If you choose **Save** at this point, the policy applies to your Office 365 tenant.</span></span> 
    
    ![Conjuntos de ações em massa e de spam para mover a mensagem para a pasta Lixo eletrônico](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. <span data-ttu-id="cebb3-p105">Se você criou uma nova política, e você deseja aplicar a política a apenas um conjunto de usuários, role para a seção **Aplicada a** na janela de filtro de diretiva e dos controles de menu escolher os **destinatários**, **domínio**ou **associações de grupo** você deseja aplicar a política. Você também pode definir exceções e condições adicionais.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p105">If you created a new policy, and you want to apply the policy to only a set of users, scroll to the **Applied To** section in the policy filter window, and in the menu controls choose the **recipients**, **domain**, or **group memberships** you want to apply the policy to. You can also set additional conditions and exceptions.</span></span> 
    
    ![Na seção aplicada a escolher os destinatários](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    <span data-ttu-id="cebb3-141">Escolha **Salvar** para aplicar a política aos usuários selecionados.</span><span class="sxs-lookup"><span data-stu-id="cebb3-141">Choose **Save** to apply the policy to the selected users.</span></span> 
    
 <span data-ttu-id="cebb3-142">**Para ver se ZAP movida sua mensagem**</span><span class="sxs-lookup"><span data-stu-id="cebb3-142">**To see if ZAP moved your message**</span></span>
  
- <span data-ttu-id="cebb3-143">Você pode usar a [descobrir e corrigir problemas de entrega de email como um Office 365 para administração de empresa](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) para determinar se a mensagem foi movida pela ZAP:</span><span class="sxs-lookup"><span data-stu-id="cebb3-143">You can use the [Find and fix email delivery issues as an Office 365 for business admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) to determine if the message was moved by ZAP:</span></span> 
    
    <span data-ttu-id="cebb3-144">Procure o texto "Zero horas automático Limpar (ZAP)" em seus detalhes de rastreamento para identificar uma mensagem que foi movida por ZAP.</span><span class="sxs-lookup"><span data-stu-id="cebb3-144">Look for the text "Zero-Hour Auto Purge (ZAP)" in your trace details to identify a message that was moved by ZAP.</span></span>
    
 <span data-ttu-id="cebb3-145">**Para desabilitar ZAP**</span><span class="sxs-lookup"><span data-stu-id="cebb3-145">**To disable ZAP**</span></span>
  
- <span data-ttu-id="cebb3-146">Se você deseja desabilitar Apagar tudo para seu locatário do Office 365 ou um conjunto de usuários, use o parâmetro **ZapEnabled** do [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet do EOP.</span><span class="sxs-lookup"><span data-stu-id="cebb3-146">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
    <span data-ttu-id="cebb3-147">No exemplo a seguir, ZAP está desabilitado para uma política de filtro de conteúdo chamada "Test".</span><span class="sxs-lookup"><span data-stu-id="cebb3-147">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a><span data-ttu-id="cebb3-148">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="cebb3-148">FAQ</span></span>
<span data-ttu-id="cebb3-149"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="cebb3-149"></span></span>

 <span data-ttu-id="cebb3-150">**O que acontece se uma mensagem legítima é movida para a pasta Lixo eletrônico?**</span><span class="sxs-lookup"><span data-stu-id="cebb3-150">**What happens if a legitimate message is moved to the junk mail folder?**</span></span>
  
<span data-ttu-id="cebb3-p106">Você deve seguir o processo de emissão normal de falsos positivos. A única razão seria movida a mensagem da caixa de entrada para a pasta Lixo eletrônico seria porque o serviço determinou que a mensagem foi spam ou mal intencionado.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
 <span data-ttu-id="cebb3-153">**Se usar a quarentena do Office 365 em vez da pasta de lixo eletrônico?**</span><span class="sxs-lookup"><span data-stu-id="cebb3-153">**What if I use the Office 365 quarantine instead of the junk mail folder?**</span></span>
  
<span data-ttu-id="cebb3-154">ZAP não move mensagens em quarentena na caixa de entrada no momento.</span><span class="sxs-lookup"><span data-stu-id="cebb3-154">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
 <span data-ttu-id="cebb3-155">**E se eu tiver uma regra de fluxo de email personalizado (bloquear / permitir regra)?**</span><span class="sxs-lookup"><span data-stu-id="cebb3-155">**What If I have a custom mail flow rule (Block/ Allow Rule)?**</span></span>
  
<span data-ttu-id="cebb3-p107">Regras criadas por administradores (regras de fluxo de email) ou regras de bloqueio e permitir têm precedência. Essas mensagens são excluídas dos critérios de recurso.</span><span class="sxs-lookup"><span data-stu-id="cebb3-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="cebb3-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cebb3-158">Related Topics</span></span>
<span data-ttu-id="cebb3-159"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="cebb3-159"></span></span>

[<span data-ttu-id="cebb3-160">Proteção antispam de emails do Office 365</span><span class="sxs-lookup"><span data-stu-id="cebb3-160">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="cebb3-161">Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos</span><span class="sxs-lookup"><span data-stu-id="cebb3-161">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

