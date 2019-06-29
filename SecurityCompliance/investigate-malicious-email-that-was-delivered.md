---
title: Encontre e investigue emails mal-intencionados que foram fornecidos (investigação de ameaças e resposta do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Saiba como usar os recursos de investigação e resposta contra ameaças para encontrar e investigar emails mal-intencionados.
ms.openlocfilehash: 5f8c615bed07b75cd3c06ec48f5ba73586f0f6d5
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394286"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a><span data-ttu-id="9caad-103">Encontre e investigue emails mal-intencionados que foram entregues (Office 365 Advanced Threat Protection Plan 2)</span><span class="sxs-lookup"><span data-stu-id="9caad-103">Find and investigate malicious email that was delivered (Office 365 Advanced Threat Protection Plan 2)</span></span>

<span data-ttu-id="9caad-104">A [proteção avançada contra ameaças do Office 365](office-365-atp.md) permite investigar as atividades que colocam seus usuários em risco e tomar medidas para proteger sua organização.</span><span class="sxs-lookup"><span data-stu-id="9caad-104">[Office 365 Advanced Threat Protection](office-365-atp.md) lets you to investigate activities that put your users at risk and take action to protect your organization.</span></span> <span data-ttu-id="9caad-105">Por exemplo, se você fizer parte da equipe de segurança da sua organização, poderá encontrar e investigar mensagens de email suspeitas que foram entregues aos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="9caad-105">For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users.</span></span> <span data-ttu-id="9caad-106">Você pode fazer isso usando o [Explorador de ameaças (ou detecções em tempo real)](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="9caad-106">You can do this by using [Threat Explorer (or real-time detections)](threat-explorer.md).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="9caad-107">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="9caad-107">Before you begin...</span></span>

<span data-ttu-id="9caad-108">Verifique se os seguintes requisitos são atendidos:</span><span class="sxs-lookup"><span data-stu-id="9caad-108">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="9caad-109">Sua organização tem a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (plano 1 ou plano 2) e as [licenças são atribuídas aos usuários](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span><span class="sxs-lookup"><span data-stu-id="9caad-109">Your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 or Plan 2) and [licenses are assigned to users](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span></span>
    
- <span data-ttu-id="9caad-110">O [log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) está ativado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="9caad-110">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="9caad-111">Sua organização tem políticas definidas para antispam, anti-malware, anti-phishing e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9caad-111">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on.</span></span> <span data-ttu-id="9caad-112">Confira [proteção contra ameaças no Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="9caad-112">See [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="9caad-113">Você é um administrador global do Office 365 ou tem o administrador de segurança ou a função de pesquisa e limpeza atribuída no centro de &amp; conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="9caad-113">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="9caad-114">Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9caad-114">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="9caad-115">Lidando com emails suspeitos</span><span class="sxs-lookup"><span data-stu-id="9caad-115">Dealing with suspicious emails</span></span>

<span data-ttu-id="9caad-116">Invasores mal-intencionados podem estar enviando emails aos seus usuários para tentarem e Phish suas credenciais e obter acesso aos segredos corporativos!</span><span class="sxs-lookup"><span data-stu-id="9caad-116">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets!</span></span> <span data-ttu-id="9caad-117">Para evitar isso, você deve usar os serviços de proteção contra ameaças no Office 365, incluindo [proteção do Exchange Online](eop/exchange-online-protection-overview.md) e [proteção avançada contra ameaças](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="9caad-117">To prevent this, you should use the threat protection services in Office 365, including [Exchange Online Protection](eop/exchange-online-protection-overview.md) and [Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="9caad-118">No entanto, há ocasiões em que um invasor pode enviar emails para seus usuários que contenham uma URL e apenas mais tarde, fazer essa URL apontar para conteúdo mal-intencionado (malware, etc.).</span><span class="sxs-lookup"><span data-stu-id="9caad-118">However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.).</span></span> <span data-ttu-id="9caad-119">Como alternativa, você pode perceber muito tarde que um usuário em sua organização foi comprometido e enquanto esse usuário foi comprometido, um invasor usou essa conta para enviar emails a outros usuários da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="9caad-119">Alternately, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company.</span></span> <span data-ttu-id="9caad-120">Como parte da limpeza desses dois cenários, talvez você queira remover mensagens de email de caixas de entrada de usuários.</span><span class="sxs-lookup"><span data-stu-id="9caad-120">As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes.</span></span> <span data-ttu-id="9caad-121">Em situações como essas, você pode usar o [Explorador de ameaças (ou detecções em tempo real)](threat-explorer.md) para encontrar e remover essas mensagens de email!</span><span class="sxs-lookup"><span data-stu-id="9caad-121">In situations like these, you can leverage [Threat Explorer (or real-time detections)](threat-explorer.md) to find and remove those email messages!</span></span>

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a><span data-ttu-id="9caad-122">Onde os emails redirecionados são localizados após a tomada de ações</span><span class="sxs-lookup"><span data-stu-id="9caad-122">Where re-routed emails are located after actions are taken</span></span>

<span data-ttu-id="9caad-123">As detecções de tempo real do explorador de ameaças adicionaram os campos de ação de entrega e local de entrega no local do status de entrega.</span><span class="sxs-lookup"><span data-stu-id="9caad-123">Threat Explorer real-time detections has added the Delivery Action and Delivery Location fields in the place of Delivery Status.</span></span> <span data-ttu-id="9caad-124">Isso resulta em uma imagem mais completa de onde seus emails se esterram.</span><span class="sxs-lookup"><span data-stu-id="9caad-124">This results in a more complete picture of where your emails land.</span></span> <span data-ttu-id="9caad-125">Parte do objetivo dessa alteração é tornar a busca mais fácil para pessoas de operações de segurança, mas o resultado líquido é saber o local dos emails de problemas em um relance.</span><span class="sxs-lookup"><span data-stu-id="9caad-125">Part of the goal of this change is to make hunting easier for Security Ops people, but the net result is knowing the location of problem emails at a glance.</span></span>

<span data-ttu-id="9caad-126">O status de entrega agora é dividido em duas colunas:</span><span class="sxs-lookup"><span data-stu-id="9caad-126">Delivery Status is now broken out into two columns:</span></span>

- <span data-ttu-id="9caad-127">**Ação de entrega** -Qual é o status desse email?</span><span class="sxs-lookup"><span data-stu-id="9caad-127">**Delivery Action** - What is the status of this email?</span></span>
- <span data-ttu-id="9caad-128">**Local de entrega** -onde esse email foi roteado como resultado?</span><span class="sxs-lookup"><span data-stu-id="9caad-128">**Delivery Location** - Where was this email routed as a result?</span></span>

<span data-ttu-id="9caad-129">A ação de entrega é a ação realizada em um email devido a políticas ou detecções existentes.</span><span class="sxs-lookup"><span data-stu-id="9caad-129">Delivery Action is the action taken on an email due to existing policies or detections.</span></span> <span data-ttu-id="9caad-130">Veja a seguir as possíveis ações que um email pode executar:</span><span class="sxs-lookup"><span data-stu-id="9caad-130">Here are the possible actions an email can take:</span></span>

1. <span data-ttu-id="9caad-131">**Entregue** – o email foi entregue à caixa de entrada ou pasta de um usuário, e o usuário pode acessá-lo diretamente.</span><span class="sxs-lookup"><span data-stu-id="9caad-131">**Delivered** – email was delivered to inbox or folder of a user and the user can directly access it.</span></span>
2. <span data-ttu-id="9caad-132">**Lixo eletrônico** – o email foi enviado à pasta de lixo eletrônico ou à pasta excluída do usuário, e o usuário tem acesso a emails na pasta lixo eletrônico ou excluído.</span><span class="sxs-lookup"><span data-stu-id="9caad-132">**Junked** – email was sent to either user’s junk folder or deleted folder, and the user has access to emails in their Junk or Deleted folder.</span></span>
3. <span data-ttu-id="9caad-133">**Bloqueado** – todos os emails que estão em quarentena, que falharam ou foram descartados.</span><span class="sxs-lookup"><span data-stu-id="9caad-133">**Blocked** – any emails that's quarantined, that  failed, or was dropped.</span></span> <span data-ttu-id="9caad-134">Isso é completamente inacessível pelo usuário!</span><span class="sxs-lookup"><span data-stu-id="9caad-134">This is completely inaccessible by the user!</span></span>
4. <span data-ttu-id="9caad-135">**Substituído** – qualquer email onde anexos mal-intencionados são substituídos por arquivos. txt que indicam que o anexo era mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="9caad-135">**Replaced** – any email where malicious attachments are replaced by .txt files that state the attachment was malicious.</span></span>
 
<span data-ttu-id="9caad-136">O local de entrega mostra os resultados das políticas e detecções que executam post-Delivery.</span><span class="sxs-lookup"><span data-stu-id="9caad-136">Delivery location shows the results of policies and detections that run post-delivery.</span></span> <span data-ttu-id="9caad-137">Ele está vinculado a uma ação de entrega.</span><span class="sxs-lookup"><span data-stu-id="9caad-137">It's linked to a Delivery Action.</span></span> <span data-ttu-id="9caad-138">Este campo foi adicionado para dar informações sobre a ação tomada quando um email de problema é encontrado.</span><span class="sxs-lookup"><span data-stu-id="9caad-138">This field was added to give insight into the action taken when a problem mail is found.</span></span> <span data-ttu-id="9caad-139">Estes são os possíveis valores de local de entrega:</span><span class="sxs-lookup"><span data-stu-id="9caad-139">Here are the possible values of delivery location:</span></span>

1. <span data-ttu-id="9caad-140">**Caixa de entrada ou pasta** – o email está na caixa de entrada ou uma pasta (de acordo com suas regras de email).</span><span class="sxs-lookup"><span data-stu-id="9caad-140">**Inbox or folder** – The email is in inbox or a folder (according to your email rules).</span></span>
2. <span data-ttu-id="9caad-141">**Local ou externo** – a caixa de correio não existe na nuvem, mas está no local.</span><span class="sxs-lookup"><span data-stu-id="9caad-141">**On-prem or external** – The mailbox doesn’t exist on cloud but is on -premises.</span></span>
3. <span data-ttu-id="9caad-142">**Pasta lixo eletrônico** – o email na pasta lixo eletrônico de um usuário.</span><span class="sxs-lookup"><span data-stu-id="9caad-142">**Junk folder** – The email in in the Junk folder of a user.</span></span>
4. <span data-ttu-id="9caad-143">**Pasta itens excluídos** – o email na pasta itens excluídos de um usuário.</span><span class="sxs-lookup"><span data-stu-id="9caad-143">**Deleted items folder** – The email in the Deleted items folder of a user.</span></span>
5. <span data-ttu-id="9caad-144">**Quarentena** – o email em quarentena e não está na caixa de correio de um usuário.</span><span class="sxs-lookup"><span data-stu-id="9caad-144">**Quarantine** – The email in quarantine, and is not in a user’s mailbox.</span></span>
6. <span data-ttu-id="9caad-145">**Falha** – o email não pôde chegar à caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="9caad-145">**Failed** – The email failed to reach the mailbox.</span></span>
7. <span data-ttu-id="9caad-146">**Descartado** – o email é perdido em algum lugar no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9caad-146">**Dropped** – The email gets lost somewhere in the Mailflow.</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="9caad-147">Localizar e excluir emails suspeitos que foram entregues</span><span class="sxs-lookup"><span data-stu-id="9caad-147">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="9caad-148">O Gerenciador de ameaças (às vezes chamado de Explorer) é um relatório poderoso que pode servir a vários propósitos, como localizar e excluir mensagens, identificar o endereço IP de um remetente de email mal-intencionado ou iniciar um incidente para investigação adicional.</span><span class="sxs-lookup"><span data-stu-id="9caad-148">Threat Explorer (sometimes called Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation.</span></span> <span data-ttu-id="9caad-149">O procedimento a seguir se concentra no uso do Explorer para localizar e excluir emails mal-intencionados de caixas de correio de destinatários.</span><span class="sxs-lookup"><span data-stu-id="9caad-149">The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span>

<span data-ttu-id="9caad-150">Para ver as alterações no campo status da entrega anterior (agora, a ação de entrega e o local de entrega):</span><span class="sxs-lookup"><span data-stu-id="9caad-150">To see the changes to the former Delivery Status field (now Delivery Action and Delivery Location):</span></span> 

1. <span data-ttu-id="9caad-151">Acesse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="9caad-151">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="9caad-152">Isso leva você para o centro &amp; de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="9caad-152">This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="9caad-153">No painel de navegação à esquerda, escolha **Gerenciador**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="9caad-153">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>

![Captura de tela do explorador de ameaças.](media/Threat Explorer Delivery Action and Delivery Location.PNG)

<!--Comment>
    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a><span data-ttu-id="9caad-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9caad-155">Related topics</span></span>

[<span data-ttu-id="9caad-156">Office 365 plano avançado de proteção contra ameaças 2</span><span class="sxs-lookup"><span data-stu-id="9caad-156">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="9caad-157">Proteção contra ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="9caad-157">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="9caad-158">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="9caad-158">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

