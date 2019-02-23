---
title: Entrega dinâmica e visualização com anexos seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Ao configurar as políticas de anexos seguros de ATP, você escolhe a entrega dinâmica para evitar atrasos de mensagens e permite que as pessoas visualizem os anexos que estão sendo examinados.
ms.openlocfilehash: 1fb221d28a4089db8a4278903107c610d6825f5e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218391"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="da169-103">Entrega dinâmica e visualização com anexos seguros de ATP do Office 365</span><span class="sxs-lookup"><span data-stu-id="da169-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="da169-p101">**Resumo**: a entrega dinâmica é uma opção que pode ser selecionada para [anexos seguros de ATP](atp-safe-attachments.md). Leia este artigo para saber mais sobre a entrega dinâmica e recursos de visualização de anexos nos [anexos seguros de ATP no Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="da169-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="da169-p102">Quando [as políticas de anexos seguros de ATP estão](set-up-atp-safe-attachments-policies.md) configuradas para sua organização, há várias opções de como os anexos de email são tratados. Eles incluem **bloqueio**, **substituição**e **entrega dinâmica**. Dependendo de como as políticas de anexos seguros de ATP estão configuradas, os destinatários de email podem enfrentar um atraso secundário na entrega de emails enquanto seus anexos são verificados. Para evitar atrasos de mensagens, escolha **entrega dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="da169-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="da169-110">Como a entrega dinâmica funciona</span><span class="sxs-lookup"><span data-stu-id="da169-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="da169-p103">A entrega dinâmica elimina os atrasos de email enviando o corpo de uma mensagem de email para o destinatário com um espaço reservado para cada anexo de email. O espaço reservado permanece até que uma cópia do anexo seja verificada e determinada como sendo segura por [anexos seguros de ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="da169-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="da169-113">Como cada anexo é limpo, ele está disponível para ser aberto ou baixado.</span><span class="sxs-lookup"><span data-stu-id="da169-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="da169-114">Se um anexo for considerado mal-intencionado, ele será enviado para a quarentena, onde alguém da equipe de segurança da sua organização (como um administrador global do Office 365 ou administrador de segurança) pode [gerenciar mensagens em quarentena no Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="da169-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="da169-p104">A maioria dos documentos PDFs e do Office pode ser visualizada no modo de segurança enquanto a verificação ATP está em andamento. Se um anexo não for compatível com o modo de exibição de entrega dinâmica, os destinatários de email verão um espaço reservado de anexo até que a verificação de anexos seguros de ATP esteja concluída.</span><span class="sxs-lookup"><span data-stu-id="da169-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

> [!TIP]
> <span data-ttu-id="da169-117">Se você estiver usando um dispositivo móvel e os PDFs não estiverem sendo renderizados no primeiro Visualizador de entrega dinâmica, tente entrar no Office 365 usando seu navegador móvel.</span><span class="sxs-lookup"><span data-stu-id="da169-117">If you're using a mobile device, and PDFs are not rendering in Dynamic Delivery previewer at first, try signing into Office 365 using your mobile browser.</span></span>

<span data-ttu-id="da169-118">Com a entrega dinâmica, as pessoas podem ler e responder às mensagens de email imediatamente, enquanto seus anexos estão sendo analisados.</span><span class="sxs-lookup"><span data-stu-id="da169-118">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="da169-p105">A verificação de anexos seguros de ATP ocorre na mesma região onde seus dados do Office 365 residem. Para obter mais informações sobre a geografia do Data Center, confira [onde estão seus dados?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="da169-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="da169-121">O que acontece quando alguém encaminha um email que contém um anexo?</span><span class="sxs-lookup"><span data-stu-id="da169-121">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="da169-p106">Suponha que uma organização esteja usando a entrega dinâmica para a [política de anexos seguros de ATP](set-up-atp-safe-attachments-policies.md)e alguém receba um email que contenha um anexo. Agora, suponha que a pessoa encaminhe a mensagem de email para outra pessoa. O que acontece? Depende de os destinatários adicionais estarem incluídos nas políticas de anexos seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="da169-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="da169-126">Se um destinatário for coberto por uma política de anexos seguros de ATP usando a opção de entrega dinâmica, o destinatário verá o espaço reservado, com a capacidade de visualizar arquivos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="da169-126">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="da169-127">Se um destinatário não for coberto por uma política de anexos seguros de ATP, o email e o anexo serão enviados, sem os espaços reservados para verificação de anexos seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="da169-127">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="da169-128">O que é necessário para que a entrega dinâmica funcione?</span><span class="sxs-lookup"><span data-stu-id="da169-128">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="da169-129">Sua organização deve ter a [proteção avançada contra ameaças do Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="da169-129">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="da169-130">As políticas devem ser definidas para anexos seguros de ATP usando a opção de entrega dinâmica (consulte [Configurar políticas de anexos seguros de ATP no Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="da169-130">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="da169-131">O email da sua organização deve estar hospedado no Office 365</span><span class="sxs-lookup"><span data-stu-id="da169-131">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="da169-132">Há situações em que a entrega dinâmica não está disponível?</span><span class="sxs-lookup"><span data-stu-id="da169-132">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="da169-p107">Há determinados cenários em que a entrega dinâmica não é suportada. Isso inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="da169-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="da169-135">Mensagens de email que estão em pastas públicas</span><span class="sxs-lookup"><span data-stu-id="da169-135">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="da169-136">Mensagens de email que são roteadas de e de volta para a caixa de correio do usuário usando regras personalizadas</span><span class="sxs-lookup"><span data-stu-id="da169-136">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="da169-137">Mensagens de email que são movidas (automática ou manualmente) da caixa de correio hospedada e em outros locais, incluindo pastas de arquivos mortos</span><span class="sxs-lookup"><span data-stu-id="da169-137">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="da169-138">Mensagens de email excluídas</span><span class="sxs-lookup"><span data-stu-id="da169-138">Email messages that are deleted</span></span>
    
- <span data-ttu-id="da169-139">Uma pasta de pesquisa de caixa de correio do usuário que está em um estado de erro</span><span class="sxs-lookup"><span data-stu-id="da169-139">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="da169-p108">Ambientes nos quais um administrador do Exchange Online habilitou o Exclaimer. Para resolver isso, confira [mensagens com anexos não são entregues quando a entrega dinâmica e o Exclaimer da ATP são usados](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="da169-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="da169-142">Mensagens criptografadas com [S/MIME (Secure/Multipurpose Internet Mail Extensions)](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="da169-142">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>

