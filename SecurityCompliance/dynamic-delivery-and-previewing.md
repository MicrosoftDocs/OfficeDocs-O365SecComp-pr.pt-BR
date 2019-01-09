---
title: Entrega dinâmica e visualização de anexos do Office 365 ATP seguros
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Ao configurar suas políticas de anexos seguros ATP, escolha entrega dinâmica para evitar atrasos de mensagem e permitem que as pessoas visualizem anexos que estão sendo examinados.
ms.openlocfilehash: 95c270e871c3febb13eef8c4374d996fc763315b
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769825"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="cddd5-103">Entrega dinâmica e visualização de anexos do Office 365 ATP seguros</span><span class="sxs-lookup"><span data-stu-id="cddd5-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="cddd5-p101">**Resumo**: entrega dinâmica é uma opção que pode ser selecionada para [ATP anexos de seguros](atp-safe-attachments.md). Leia este artigo para saber mais sobre a entrega dinâmicos e recursos de visualização de anexo no [ATP anexos de seguros no Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="cddd5-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="cddd5-p102">Quando [as políticas de anexos de seguros ATP são configuradas](set-up-atp-safe-attachments-policies.md) para sua organização, há várias opções para como anexos de email são manipulados. Isso inclui **Bloquear**, **Substitua**e **Entrega dinâmico**. Dependendo de como as políticas de anexos de seguros ATP são configuradas, os destinatários do email podem sofrer um atraso secundário na entrega de email enquanto seus anexos são verificados. Para evitar atrasos de mensagem, escolha **Entrega dinâmico**.</span><span class="sxs-lookup"><span data-stu-id="cddd5-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="cddd5-110">Como funciona a entrega dinâmico</span><span class="sxs-lookup"><span data-stu-id="cddd5-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="cddd5-p103">Entrega dinâmica elimina atrasos de email, enviando o corpo de uma mensagem de email por meio para o destinatário com um espaço reservado para cada anexo de email. O espaço reservado permanece até que uma cópia do anexo é examinada e determinada seguros pela [ATP anexos de seguros](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="cddd5-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="cddd5-113">Como cada anexo estiver desmarcado, ele está disponível para abrir ou baixar.</span><span class="sxs-lookup"><span data-stu-id="cddd5-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="cddd5-114">Se um anexo é determinado mal-intencionado, ela será enviada para quarentena, onde uma pessoa na equipe de segurança da sua organização (por exemplo, um administrador global do Office 365 ou segurança) pode [Gerenciar mensagens em quarentena no Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="cddd5-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="cddd5-p104">A maioria dos PDFs e Office documentos podem ser visualizados no modo de segurança, enquanto a verificação ATP está em andamento. Se um anexo não é compatível com o Visualizador de entrega dinâmico, os destinatários de email Consulte um espaço reservado de anexo até que a verificação de anexos de seguros ATP seja concluída.</span><span class="sxs-lookup"><span data-stu-id="cddd5-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

<span data-ttu-id="cddd5-117">Com o fornecimento dinâmico, pessoas podem ler e responder às suas mensagens de email imediatamente, enquanto seus anexos estão sendo analisados.</span><span class="sxs-lookup"><span data-stu-id="cddd5-117">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="cddd5-p105">Anexos de seguros ATP verificação leva coloque na mesma região onde estão seus dados do Office 365. Para obter mais informações sobre Geografia do Centro de dados, consulte [onde estão seus dados localizados?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="cddd5-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="cddd5-120">O que acontece quando alguém encaminha um email que contenha um anexo?</span><span class="sxs-lookup"><span data-stu-id="cddd5-120">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="cddd5-p106">Suponha que uma organização está usando dinâmico de entrega para a sua [política de anexos de ATP seguros](set-up-atp-safe-attachments-policies.md)e alguém recebe um email que contenha um anexo. Agora suponha que a pessoa encaminhe a mensagem de email para outra pessoa. O que acontece? Isso depende se os destinatários adicionais são incluídos nas políticas de anexos de ATP seguros.</span><span class="sxs-lookup"><span data-stu-id="cddd5-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="cddd5-125">Se um destinatário é coberto por uma política de anexos de seguros ATP usando a opção de entrega dinâmico, o receptor vê espaço reservado, com a capacidade de visualizar arquivos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="cddd5-125">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="cddd5-126">Se um destinatário não é abordado por uma política de anexos de seguros ATP, então a email e o anexo irão através de, sem anexos de seguros ATP verificação ou espaços reservados de anexo.</span><span class="sxs-lookup"><span data-stu-id="cddd5-126">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="cddd5-127">O que é necessário para entrega dinâmica funcionar?</span><span class="sxs-lookup"><span data-stu-id="cddd5-127">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="cddd5-128">Sua organização deve ter [A proteção de ameaça avançadas do Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="cddd5-128">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="cddd5-129">As políticas devem ser definidas para anexos seguros ATP, usando a opção de entrega dinâmico (consulte [Set up políticas ATP anexos de seguros no Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="cddd5-129">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="cddd5-130">Email da sua organização deve ser hospedado no Office 365</span><span class="sxs-lookup"><span data-stu-id="cddd5-130">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="cddd5-131">Existem cenários entrega dinâmica para o qual não está disponível?</span><span class="sxs-lookup"><span data-stu-id="cddd5-131">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="cddd5-p107">Há determinadas situações em que a entrega dinâmica não é suportada. Isso inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cddd5-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="cddd5-134">Mensagens de email que estão em pastas públicas</span><span class="sxs-lookup"><span data-stu-id="cddd5-134">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="cddd5-135">Mensagens de email que são roteadas de ausência temporária e, em seguida, que voltou ao caixa de correio do usuário usando regras personalizadas</span><span class="sxs-lookup"><span data-stu-id="cddd5-135">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="cddd5-136">Mensagens de email que serão movidas (automática ou manualmente) fora da caixa de correio hospedada e em outros locais, incluindo pastas de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="cddd5-136">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="cddd5-137">Mensagens de email excluídas</span><span class="sxs-lookup"><span data-stu-id="cddd5-137">Email messages that are deleted</span></span>
    
- <span data-ttu-id="cddd5-138">Pasta de pesquisa de caixa de correio de um usuário que está em um estado de erro</span><span class="sxs-lookup"><span data-stu-id="cddd5-138">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="cddd5-p108">Ambientes em que um administrador do Exchange Online tiver habilitado Exclaimer. Para resolver esse problema, consulte [mensagens com anexos não são entregues quando ATP dinâmicos de entrega e Exclaimer são usados](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="cddd5-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="cddd5-141">Mensagens criptografadas com o [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="cddd5-141">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>
    
