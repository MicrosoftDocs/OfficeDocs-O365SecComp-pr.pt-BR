---
title: Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Saiba como usar a inteligência de ameaças para localizar e investigar emails mal-intencionados.
ms.openlocfilehash: d5b08338bc0a3a6a88ea498861ab9e27522b759d
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241903"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a><span data-ttu-id="10ad9-103">Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)</span><span class="sxs-lookup"><span data-stu-id="10ad9-103">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>

<span data-ttu-id="10ad9-p101">O [Office 365 Threat Intelligence](office-365-ti.md) permite investigar as atividades que colocam seus usuários em risco e tomar medidas para proteger sua organização. Por exemplo, se você fizer parte da equipe de segurança da sua organização, poderá encontrar e investigar mensagens de email suspeitas que foram entregues aos seus usuários. Você pode fazer isso usando o [Explorador de ameaças](get-started-with-ti.md#threat-explorer).</span><span class="sxs-lookup"><span data-stu-id="10ad9-p101">[Office 365 Threat Intelligence](office-365-ti.md) enables you to investigate activities that put your users at risk and take action to protect your organization. For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users. You can do this by using [Threat Explorer](get-started-with-ti.md#threat-explorer).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="10ad9-p102">A partir de fevereiro de 2019 e saindo dos próximos meses, o Office 365 Threat Intelligence está se tornando o Office 365 Advanced Threat Protection Plan 2, com recursos adicionais de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="10ad9-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="10ad9-109">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="10ad9-109">Before you begin...</span></span>

<span data-ttu-id="10ad9-110">Verifique se os seguintes requisitos são atendidos:</span><span class="sxs-lookup"><span data-stu-id="10ad9-110">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="10ad9-111">Sua organização tem a [inteligência contra ameaças do office 365](office-365-ti.md) e [atribui licenças aos usuários no Office 365 para empresas](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span><span class="sxs-lookup"><span data-stu-id="10ad9-111">Your organization has [Office 365 Threat Intelligence](office-365-ti.md) and [Assign licenses to users in Office 365 for business](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span></span>
    
- <span data-ttu-id="10ad9-112">O [log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) está ativado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="10ad9-112">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="10ad9-p103">Sua organização tem políticas definidas para antispam, anti-malware, anti-phishing e assim por diante. Consulte [Gerenciamento de ameaças no centro de conformidade &amp; de segurança do Office 365](threat-management.md).</span><span class="sxs-lookup"><span data-stu-id="10ad9-p103">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on. See [Threat management in the Office 365 Security &amp; Compliance Center](threat-management.md).</span></span>
    
- <span data-ttu-id="10ad9-p104">Você é um administrador global do Office 365 ou tem o administrador de segurança ou a função de pesquisa e limpeza atribuída no centro de &amp; conformidade de segurança. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="10ad9-p104">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="10ad9-117">Lidando com emails suspeitos</span><span class="sxs-lookup"><span data-stu-id="10ad9-117">Dealing with suspicious emails</span></span>

<span data-ttu-id="10ad9-p105">Invasores mal-intencionados podem estar enviando emails aos seus usuários para tentarem e Phish suas credenciais e obter acesso aos segredos corporativos! Para evitar isso, você deve usar os serviços de proteção contra ameaças oferecidos pelo Office 365, incluindo proteção do Exchange Online e proteção avançada contra ameaças. No enTanto, há ocasiões em que um invasor pode enviar emails para seus usuários que contenham uma URL e apenas mais tarde, fazer essa URL apontar para conteúdo mal-intencionado (malware, etc.). Como alternativa, você pode perceber muito tarde que um usuário em sua organização foi comprometido e enquanto esse usuário foi comprometido, um invasor usou essa conta para enviar emails a outros usuários da sua empresa. Como parte da limpeza desses dois cenários, talvez você queira remover mensagens de email de caixas de entrada de usuários. Em situações como essas, você pode usar o explorador de ameaças para encontrar e remover essas mensagens de email!</span><span class="sxs-lookup"><span data-stu-id="10ad9-p105">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets! In order to prevent this, you should use the threat protection services offered by Office 365, including Exchange Online Protection and Advanced Threat Protection. However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.). Alternatively, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company. As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes. In situations like these, you can leverage Threat Explorer to find and remove those email messages!</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="10ad9-124">Localizar e excluir emails suspeitos que foram entregues</span><span class="sxs-lookup"><span data-stu-id="10ad9-124">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="10ad9-p106">[Explorador de ameaças](get-started-with-ti.md#threat-explorer) (também chamado de Explorer), é um relatório poderoso que pode servir a vários propósitos, como localizar e excluir mensagens, identificar o endereço IP de um remetente de email mal-intencionado ou iniciar um incidente para investigação adicional. O procedimento a seguir se concentra no uso do Explorer para localizar e excluir emails mal-intencionados de caixas de correio de destinatários.</span><span class="sxs-lookup"><span data-stu-id="10ad9-p106">[Threat Explorer](get-started-with-ti.md#threat-explorer) (also referred to as Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation. The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span> 
  
1. <span data-ttu-id="10ad9-p107">AcEsse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365. Isso leva você para o centro &amp; de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="10ad9-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="10ad9-129">No painel de navegação à esquerda, escolha **Gerenciador**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="10ad9-129">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>
    
3. <span data-ttu-id="10ad9-130">No menu Exibir, escolha **todos os emails**.</span><span class="sxs-lookup"><span data-stu-id="10ad9-130">In the View menu, choose **All email**.</span></span><br/><span data-ttu-id="10ad9-131">![Usar o menu Exibir para escolher entre relatórios de email e conteúdo](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span><span class="sxs-lookup"><span data-stu-id="10ad9-131">![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span></span>
  
4. <span data-ttu-id="10ad9-132">Observe os rótulos que aparecem no relatório, como **entregue**, **desconhecido**ou **entregue ao lixo eletrônico**.</span><span class="sxs-lookup"><span data-stu-id="10ad9-132">Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.</span></span><br/><span data-ttu-id="10ad9-133">![Explorador de ameaças mostrando dados para todos os emails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span><span class="sxs-lookup"><span data-stu-id="10ad9-133">![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span></span><br/><span data-ttu-id="10ad9-134">(Dependendo das ações que foram tomadas nas mensagens de email de sua organização, você poderá ver rótulos adicionais, como bloqueados \*\*\*\* ou **substituídos**.)</span><span class="sxs-lookup"><span data-stu-id="10ad9-134">(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)</span></span>
    
5. <span data-ttu-id="10ad9-135">No relatório, escolha **entregue** para exibir apenas os emails que acabaram nas caixas de entrada dos usuários.</span><span class="sxs-lookup"><span data-stu-id="10ad9-135">In the report, choose **Delivered** to view only emails that ended up in users' inboxes.</span></span><br/><span data-ttu-id="10ad9-136">![Clicar em "entregue a lixo eletrônico" remove esses dados da exibição](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span><span class="sxs-lookup"><span data-stu-id="10ad9-136">![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span></span>
  
6. <span data-ttu-id="10ad9-137">Abaixo do gráfico, revise \*\*\*\* a lista de emails abaixo do gráfico.</span><span class="sxs-lookup"><span data-stu-id="10ad9-137">Below the chart, review the **Email** list below the chart.</span></span><br/><span data-ttu-id="10ad9-138">![Abaixo do gráfico, exiba uma lista de mensagens de email que foram detectadas](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span><span class="sxs-lookup"><span data-stu-id="10ad9-138">![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span></span>
  
7. <span data-ttu-id="10ad9-p108">Na lista, escolha um item para exibir mais detalhes sobre a mensagem de email. Por exemplo, você pode clicar na linha de assunto para exibir informações sobre o remetente, destinatários, anexos e outras mensagens de email semelhantes.</span><span class="sxs-lookup"><span data-stu-id="10ad9-p108">In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.</span></span><br/>![Você pode visualizar informações adicionais sobre um item, incluindo detalhes e todos os anexos](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. <span data-ttu-id="10ad9-142">Após exibir informações sobre mensagens de email, selecione um ou mais itens na lista para ativar **+ ações**.</span><span class="sxs-lookup"><span data-stu-id="10ad9-142">After viewing information about email messages, select one or more items in the list to activate **+ Actions**.</span></span>
    
9. <span data-ttu-id="10ad9-p109">Use a lista de **ações +** para aplicar uma ação, como **mover para itens excluídos** . Isso excluirá as mensagens selecionadas das caixas de correio dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="10ad9-p109">Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.</span></span><br/><span data-ttu-id="10ad9-145">![Ao selecionar uma ou mais mensagens de email, você pode escolher entre várias ações disponíveis](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span><span class="sxs-lookup"><span data-stu-id="10ad9-145">![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="10ad9-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10ad9-146">Related topics</span></span>

[<span data-ttu-id="10ad9-147">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="10ad9-147">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="10ad9-148">Proteção contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="10ad9-148">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="10ad9-149">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="10ad9-149">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

