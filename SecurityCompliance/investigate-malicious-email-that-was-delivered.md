---
title: Localizar e investigar email mal-intencionado que foi entregue (Office 365 Threat Intelligence)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection: M365-security-compliance
description: Aprenda a usar inteligência de ameaça para localizar e investigar email mal-intencionado.
ms.openlocfilehash: c7492ccf2a7fa5d67b256264c6ed6fbdb06bcbc8
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995182"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a><span data-ttu-id="5d8d9-103">Localizar e investigar email mal-intencionado que foi entregue (Office 365 Threat Intelligence)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-103">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>

<span data-ttu-id="5d8d9-p101">[Office 365 Threat Intelligence](office-365-ti.md) permite investigar atividades que colocam seus usuários em risco e ações para proteger sua organização. Por exemplo, se você fazem parte da equipe de segurança da sua organização, poderá localizar e investigar mensagens de email suspeitas que foram entregues aos seus usuários. Você pode fazer isso usando o [Gerenciador de ameaça](get-started-with-ti.md#threat-explorer).</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p101">[Office 365 Threat Intelligence](office-365-ti.md) enables you to investigate activities that put your users at risk and take action to protect your organization. For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users. You can do this by using [Threat Explorer](get-started-with-ti.md#threat-explorer).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5d8d9-p102">Iniciando no fevereiro de 2019 e aplicação nos próximos meses várias, inteligência de dados do Office 365 ameaça está se tornando Office 365 avançadas ameaça proteção plano 2, com os recursos de proteção de ameaça adicional. Para saber mais, consulte [preços e planos de proteção de ameaça avançadas do Office 365](https://products.office.com/exchange/advance-threat-protection) e o [Office 365 avançadas Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="5d8d9-109">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="5d8d9-109">Before you begin...</span></span>

<span data-ttu-id="5d8d9-110">Verifique se os seguintes requisitos são atendidos:</span><span class="sxs-lookup"><span data-stu-id="5d8d9-110">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="5d8d9-111">Sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md) e [Atribuir licenças aos usuários no Office 365 para empresas](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span><span class="sxs-lookup"><span data-stu-id="5d8d9-111">Your organization has [Office 365 Threat Intelligence](office-365-ti.md) and [Assign licenses to users in Office 365 for business](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span></span>
    
- <span data-ttu-id="5d8d9-112">[Log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) é ativada para sua organização.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-112">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="5d8d9-p103">Sua organização tem políticas definidas para antispam, antimalware, antiphishing e assim por diante. Consulte [gerenciamento de segurança do Office 365 de ameaça &amp; Centro de conformidade](threat-management.md).</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p103">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on. See [Threat management in the Office 365 Security &amp; Compliance Center](threat-management.md).</span></span>
    
- <span data-ttu-id="5d8d9-p104">Você é um administrador global do Office 365 ou você tem o administrador de segurança ou a função de pesquisa e limpar atribuída na segurança &amp; Centro de conformidade. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p104">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="5d8d9-117">Lidando com emails suspeitos</span><span class="sxs-lookup"><span data-stu-id="5d8d9-117">Dealing with suspicious emails</span></span>

<span data-ttu-id="5d8d9-p105">Invasores mal-intencionados podem ser enviar email aos seus usuários para testar e phishing suas credenciais e acessar os seus segredos corporativos! Para impedir isso, você deve usar os serviços de proteção de ameaça oferecidos pelo Office 365, incluindo o Exchange Online Protection e proteção avançada de ameaça. No entanto, há ocasiões quando um invasor pode enviar emails para seus usuários contendo uma URL e apenas no futuro fazer esse ponto de URL conteúdo mal-intencionado (malware, etc.). Como alternativa, você pode perceber muito depois que um usuário em sua organização foi comprometido e enquanto o usuário foi comprometido, o invasor usados essa conta para enviar email para outros usuários da sua empresa. Como parte do limpando esses dois cenários, convém remover mensagens de email de entrada dos usuários. Em situações como essas, você pode aproveitar o Explorer de ameaça para encontrar e remover essas mensagens de email!</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p105">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets! In order to prevent this, you should use the threat protection services offered by Office 365, including Exchange Online Protection and Advanced Threat Protection. However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.). Alternatively, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company. As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes. In situations like these, you can leverage Threat Explorer to find and remove those email messages!</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="5d8d9-124">Localizar e excluir email suspeita que foi entregue</span><span class="sxs-lookup"><span data-stu-id="5d8d9-124">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="5d8d9-p106">[Gerenciador de ameaça](get-started-with-ti.md#threat-explorer) (também conhecido como Explorer) é um relatório poderoso que pode atender a vários propósitos, como Localizando e excluindo mensagens, que identifica o endereço IP de um remetente do email maliciosa ou iniciar um incidente para uma investigação detalhada. O procedimento a seguir se concentra em usando o Explorer para localizar e excluir email maliciosa de caixas de correio de destinatários.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p106">[Threat Explorer](get-started-with-ti.md#threat-explorer) (also referred to as Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation. The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span> 
  
1. <span data-ttu-id="5d8d9-p107">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. Isso leva você para a segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="5d8d9-129">No painel de navegação esquerdo, escolha **gerenciamento de ameaça** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-129">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>
    
3. <span data-ttu-id="5d8d9-130">No menu Exibir, escolha **todos os emails**.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-130">In the View menu, choose **All email**.</span></span><br/><span data-ttu-id="5d8d9-131">![Use o menu Exibir para escolher entre eletrônico e conteúdo de relatórios](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-131">![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span></span>
  
4. <span data-ttu-id="5d8d9-132">Observe os rótulos que aparecem no relatório, como **entregues**, **desconhecido**ou **entregue ao lixo**.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-132">Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.</span></span><br/><span data-ttu-id="5d8d9-133">![Gerenciador de ameaça mostrando dados para todos os emails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-133">![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span></span><br/><span data-ttu-id="5d8d9-134">(Dependendo das ações que foram feitas em mensagens de email para sua organização, você poderá ver rótulos adicionais, como **bloqueado** ou **foi substituído**.)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-134">(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)</span></span>
    
5. <span data-ttu-id="5d8d9-135">No relatório, escolha **entregue** para exibir somente os emails que terminou nas caixas de entrada dos usuários.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-135">In the report, choose **Delivered** to view only emails that ended up in users' inboxes.</span></span><br/><span data-ttu-id="5d8d9-136">![Clicando em "Entregue ao lixo" remove dados de modo de exibição](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-136">![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span></span>
  
6. <span data-ttu-id="5d8d9-137">O gráfico abaixo, revise a lista de **Email** abaixo do gráfico.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-137">Below the chart, review the **Email** list below the chart.</span></span><br/><span data-ttu-id="5d8d9-138">![O gráfico abaixo, exibir uma lista de mensagens de email que foram detectados](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-138">![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span></span>
  
7. <span data-ttu-id="5d8d9-p108">Na lista, escolha um item para exibir mais detalhes sobre essa mensagem de email. Por exemplo, você pode clicar a linha de assunto para exibir informações sobre o remetente, recipients, anexos e outras semelhantes mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p108">In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.</span></span><br/>![Você pode exibir informações adicionais sobre um item, incluindo detalhes e todos os anexos](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. <span data-ttu-id="5d8d9-142">Depois de exibir informações sobre as mensagens de email, selecione um ou mais itens na lista para ativar **+ ações**.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-142">After viewing information about email messages, select one or more items in the list to activate **+ Actions**.</span></span>
    
9. <span data-ttu-id="5d8d9-p109">Use a lista **+ ações** para aplicar uma ação, como itens de **Mover para excluído** . Isso excluirá as mensagens selecionadas de caixas de correio dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="5d8d9-p109">Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.</span></span><br/><span data-ttu-id="5d8d9-145">![Quando você seleciona uma ou mais mensagens de email, você poderá escolher entre várias ações disponíveis](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span><span class="sxs-lookup"><span data-stu-id="5d8d9-145">![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="5d8d9-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d8d9-146">Related topics</span></span>

[<span data-ttu-id="5d8d9-147">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="5d8d9-147">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="5d8d9-148">Proteção contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="5d8d9-148">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="5d8d9-149">Exibir relatórios de proteção de ameaça avançadas do Office 365</span><span class="sxs-lookup"><span data-stu-id="5d8d9-149">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

