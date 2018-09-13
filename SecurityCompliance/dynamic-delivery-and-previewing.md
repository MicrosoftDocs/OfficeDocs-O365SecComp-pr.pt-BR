---
title: Entrega dinâmica e visualização de anexos do Office 365 ATP seguros
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Ao configurar suas políticas de anexos seguros ATP, escolha entrega dinâmica para evitar atrasos de mensagem e permitem que as pessoas visualizem anexos que estão sendo examinados.
ms.openlocfilehash: 23ef316ed35b89ef1fad5e9639dd10e76036a4f3
ms.sourcegitcommit: 82fd4c85b952819157fbb13175c7b2dbbdff510f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965238"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="1fb13-103">Entrega dinâmica e visualização de anexos do Office 365 ATP seguros</span><span class="sxs-lookup"><span data-stu-id="1fb13-103">Dynamic delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="1fb13-p101">Entrega dinâmica é uma opção que pode ser selecionada para. Leia este artigo para saber mais sobre a entrega dinâmica e capacidades de visualização de anexo no [ATP anexos de seguros no Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="1fb13-p101">Dynamic delivery is an option that can be selected for . Read this article to learn about dynamic delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="1fb13-106">Funciona como dinâmico de entrega</span><span class="sxs-lookup"><span data-stu-id="1fb13-106">How dynamic delivery works</span></span>

<span data-ttu-id="1fb13-p102">Quando você [Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md), você pode escolher entre várias opções, como **Bloquear**, **Substituir**e **Entrega dinâmico**. Dependendo de como as políticas são configuradas, os destinatários de email podem levar algum secundária na entrega de email enquanto seus anexos são verificados. Para evitar atrasos de mensagem, escolha **Entrega dinâmico**.</span><span class="sxs-lookup"><span data-stu-id="1fb13-p102">When you [set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md), you can choose from several options, such as **Block**, **Replace**, and **Dynamic Delivery**. Depending on how your policies are configured, email recipients can experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
<span data-ttu-id="1fb13-p103">A opção de entrega dinâmica elimina atrasos de email enviando o corpo de uma mensagem de email por meio de um espaço reservado para cada anexo de email. O espaço reservado permanece até que o anexo é verificado pelo [ATP anexos de seguros no Office 365](atp-safe-attachments.md). Destinatários de email podem ler e responder às suas mensagens de email imediatamente, sabendo que seus anexos estão sendo analisados.</span><span class="sxs-lookup"><span data-stu-id="1fb13-p103">The dynamic delivery option eliminates email delays by sending the body of an email message through with a placeholder for each email attachment. The placeholder remains until the attachment is scanned by [ATP Safe Attachments in Office 365](atp-safe-attachments.md). Email recipients can read and respond to their email messages right away, knowing that their attachments are being analyzed.</span></span>
  
<span data-ttu-id="1fb13-p104">A maioria dos PDFs e Office documentos podem ser visualizados no modo de segurança, enquanto a verificação ATP está em andamento. Se um anexo não é compatível com o Visualizador de entrega dinâmico, os destinatários de email Consulte espaço reservado anexo até que a verificação de anexos de seguros ATP seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1fb13-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the dynamic delivery previewer, email recipients see the attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>
  
<span data-ttu-id="1fb13-p105">Como cada anexo estiver desmarcado, ele é automaticamente reanexado à mensagem de email original. Se um anexo é determinado mal-intencionado, ela será enviada para quarentena, onde uma pessoa na equipe de segurança da sua organização (por exemplo, um administrador global do Office 365 ou segurança) pode [Gerenciar mensagens em quarentena no Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="1fb13-p105">As each attachment is cleared, it is automatically reattached to the original email message. If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="1fb13-117">O que acontece quando alguém encaminha um email que contenha um anexo?</span><span class="sxs-lookup"><span data-stu-id="1fb13-117">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="1fb13-p106">Suponha que uma organização está usando o dynamic entrega para sua [política de anexos de ATP seguros](set-up-atp-safe-attachments-policies.md)e alguém recebe um email que contenha um anexo. Agora suponha que a pessoa está prestes a encaminhar a mensagem de email para outra pessoa. O que acontece? Isso depende se os destinatários adicionais são incluídos nas políticas de anexos de ATP seguros.</span><span class="sxs-lookup"><span data-stu-id="1fb13-p106">Suppose that an organization is using dynamic delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person is about to forward the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="1fb13-122">Se um destinatário é coberto por uma política de anexos de seguros ATP usando a opção de entrega dinâmico, o receptor vê espaço reservado, com a capacidade de visualizar arquivos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="1fb13-122">If a recipient is covered by an ATP Safe Attachments policy using the dynamic delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="1fb13-123">Se um destinatário não é abordado por uma política de anexos de seguros ATP, então a email e o anexo irão através de, sem anexos de seguros ATP verificação ou espaços reservados de anexo.</span><span class="sxs-lookup"><span data-stu-id="1fb13-123">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="1fb13-124">O que é necessário para entrega dinâmica funcionar?</span><span class="sxs-lookup"><span data-stu-id="1fb13-124">What's required for dynamic delivery to work?</span></span>

- <span data-ttu-id="1fb13-125">Sua organização deve ter [A proteção de ameaça avançadas do Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="1fb13-125">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="1fb13-126">As políticas devem ser definidas para anexos seguros ATP, usando a opção de entrega dinâmico (consulte [Set up políticas ATP anexos de seguros no Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="1fb13-126">Policies must be defined for ATP Safe Attachments using the dynamic delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="1fb13-127">Email da sua organização deve ser hospedado no Office 365</span><span class="sxs-lookup"><span data-stu-id="1fb13-127">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="1fb13-128">Existem cenários para o qual a entrega dinâmica não está disponível?</span><span class="sxs-lookup"><span data-stu-id="1fb13-128">Are there scenarios for which dynamic delivery is not available?</span></span>

<span data-ttu-id="1fb13-p107">Há determinadas situações em que a entrega dinâmica não é suportada. Isso inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1fb13-p107">There are certain scenarios in which dynamic delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="1fb13-131">Mensagens de email que estão em pastas públicas</span><span class="sxs-lookup"><span data-stu-id="1fb13-131">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="1fb13-132">Mensagens de email que são roteadas de ausência temporária e, em seguida, que voltou ao caixa de correio do usuário usando regras personalizadas</span><span class="sxs-lookup"><span data-stu-id="1fb13-132">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="1fb13-133">Mensagens que são movidas (automática ou manualmente) fora da caixa de correio hospedada e em outros locais, incluindo pastas de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="1fb13-133">Messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="1fb13-134">Mensagens que são excluídas</span><span class="sxs-lookup"><span data-stu-id="1fb13-134">Messages that are deleted</span></span>
    
- <span data-ttu-id="1fb13-135">Pasta de pesquisa de caixa de correio de um usuário que está em um estado de erro</span><span class="sxs-lookup"><span data-stu-id="1fb13-135">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="1fb13-p108">Ambientes em que um administrador do Exchange Online tiver habilitado Exclaimer. (Consulte [mensagens com anexos não são entregues quando são usados ATP dinâmicos de entrega e Exclaimer](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span><span class="sxs-lookup"><span data-stu-id="1fb13-p108">Environments in which an Exchange Online admin has enabled Exclaimer. (See [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span></span>

- <span data-ttu-id="1fb13-138">Mensagens criptografadas com o Secure/Multipurpose Internet Mail Extensions ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="1fb13-138">Messages encrypted with Secure/Multipurpose Internet Mail Extensions ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="1fb13-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fb13-139">Related topics</span></span>

<span data-ttu-id="1fb13-140">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="1fb13-140">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  
[<span data-ttu-id="1fb13-141">Anexos de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="1fb13-141">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="1fb13-142">Configurar políticas de anexos de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="1fb13-142">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="1fb13-143">Links de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="1fb13-143">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)

[<span data-ttu-id="1fb13-144">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="1fb13-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

