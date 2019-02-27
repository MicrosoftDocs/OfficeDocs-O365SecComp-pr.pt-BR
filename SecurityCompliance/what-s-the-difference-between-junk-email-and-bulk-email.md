---
title: Qual é a diferença entre lixo eletrônico e email em massa?
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
description: Os clientes às vezes askwhat a diferença entre lixo eletrônico e mensagens de email em massa? O objetivo deste tópico é explicar a diferença e fornecer informações sobre as diferentes opções disponíveis para o Exchange Online e o Exchange Online Protection (EOP).
ms.openlocfilehash: 877912c94af5d4b399769759189d091c62d50075
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275711"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a><span data-ttu-id="63f3d-103">Qual é a diferença entre lixo eletrônico e email em massa?</span><span class="sxs-lookup"><span data-stu-id="63f3d-103">What's the difference between junk email and bulk email?</span></span>

<span data-ttu-id="63f3d-p101">Às vezes, os clientes perguntam "qual é a diferença entre lixo eletrônico e mensagens de email em massa?" O objetivo deste tópico é explicar a diferença e fornecer informações sobre as várias opções disponíveis no Exchange Online e no Proteção do Exchange Online (EOP).</span><span class="sxs-lookup"><span data-stu-id="63f3d-p101">Customers sometimes ask "what's the difference between junk email and bulk email messages?" The purpose of this topic is to explain the difference and to provide information about the different options that are available for both in Exchange Online and Exchange Online Protection (EOP).</span></span>
  
 <span data-ttu-id="63f3d-106">**O que é lixo eletrônico?**</span><span class="sxs-lookup"><span data-stu-id="63f3d-106">**What's junk email?**</span></span>
  
<span data-ttu-id="63f3d-p102">As mensagens de lixo eletrônico são mensagens de "spam", significando emails não solicitados (e geralmente indesejados) que são filtrados pelo serviço. Por padrão, o serviço rejeita a mensagem de spam com base na reputação do endereço IP de envio. Entretanto, se ele passa pela inspeção de IP, mas é classificado como spam pelos filtros de conteúdo, a mensagem é enviada para a pasta Lixo Eletrônico dos destinatários pretendidos.</span><span class="sxs-lookup"><span data-stu-id="63f3d-p102">Junk email messages are "spam" messages, which are unsolicited (and typically unwanted) email messages that are filtered by the service. By default, the service rejects the spam message based on the reputation of the sending IP address. However, if it passes IP inspection but is classified as spam by the content filters, the message is sent to the Junk Email folder of the intended recipients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="63f3d-p103">A ação executada em mensagens filtradas por conteúdo é configurável por meio de políticas de filtro de conteúdo no centro de administração do Exchange (Eat), conforme descrito em [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Além disso, se você discordar da classificação de spam, poderá relatar mensagens que você considerar como spam ou não spam para a Microsoft de várias maneiras, conforme descrito em [enviar mensagens de spam, não spam e golpes de phishing para a Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="63f3d-p103">The action performed on content-filtered messages is configurable via content filter policies in the Exchange admin center (EAC), as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md). Also, if you disagree with the spam classification, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="63f3d-112">**O que é email em massa?**</span><span class="sxs-lookup"><span data-stu-id="63f3d-112">**What's bulk email?**</span></span>
  
<span data-ttu-id="63f3d-p104">Email em massa é um tipo de mensagem de email mais difícil de classificar. Embora o lixo eletrônico seja uma ameaça constante, o email em massa geralmente é composto por uma mensagem publicitária ou de marketing que, muito provavelmente, não será enviada repetidas vezes. O email em massa é de interesse de alguns usuários e, de fato, eles podem ter deliberadamente concordado em receber essas mensagens, embora outros usuários talvez considerem esse tipo de mensagem como spam. Por exemplo, alguns usuários querem receber emails publicitários da Contoso Corporation ou convites para uma conferência futura sobre segurança cibernética; já outros usuários consideram tais emails como spam.</span><span class="sxs-lookup"><span data-stu-id="63f3d-p104">Bulk email, also referred to as gray mail, is a type of email message that's more difficult to classify. Whereas junk email is a constant threat, bulk email is typically comprised of an advertisement or marketing message that's not likely to get sent repeatedly. Bulk email is wanted by some users, and in fact they may have deliberately signed up to receive these messages, while other users may consider these types of messages to be spam. For example, some users want to receive advertising emails from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider such emails to be spam.</span></span>
  
## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="63f3d-117">Como gerenciar o email em massa</span><span class="sxs-lookup"><span data-stu-id="63f3d-117">How to manage bulk email</span></span>

<span data-ttu-id="63f3d-p105">A maneira de gerenciar o email em massa não é uma decisão clara - afinal, se todos os emails em massa forem classificados como spam, os usuários interessados poderão reclamar e enviá-los como um falso positivo (mensagem de não spam e que foi incorretamente marcada como spam). Por outro lado, se todos os emails em massa forem liberados, os usuários não interessados poderão reclamar e enviá-los como uma mensagem de spam que escapou à inspeção (falso negativo) e chegou inadvertidamente à caixa de entrada deles.</span><span class="sxs-lookup"><span data-stu-id="63f3d-p105">How to manage bulk email isn't a clear cut decision, because if all bulk email is classified as spam, the users that want it may complain and submit it as a false positive (non-spam) message that was wrongly marked as spam. On the other hand, if all bulk email is let through, the users that don't want it may complain and submit it as a missed spam message (false negative) that wrongly arrived in their inbox.</span></span>
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a><span data-ttu-id="63f3d-120">Habilitar o controle de sensibilidade de email em massa na política de filtro de conteúdo</span><span class="sxs-lookup"><span data-stu-id="63f3d-120">Enable bulk mail sensitivity control in the content filter policy</span></span>

<span data-ttu-id="63f3d-p106">Dependendo da política de sua empresa em mensagens de email em massa, os administradores podem selecionar um limite para atribuir o email em massa. A configuração é configurável por meio de políticas de filtro de conteúdo no Eat. ConFira [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) para as etapas. Você pode escolher uma configuração de limite de 1-9, onde 1 marca a maior parte dos emails em massa como spam, e 9 permite que a maior parte dos emails em massa seja entregue. Em seguida, o serviço realiza a ação configurada, como enviar a mensagem para a pasta lixo eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="63f3d-p106">Depending on your company's policy on bulk email messages, admins can select a threshold to assign the bulk email. The setting is configurable via content filter policies in the EAC. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) for the steps. You can choose a threshold setting from 1-9, where 1 marks most bulk email as spam, and 9 allows most bulk email to be delivered. The service then performs the configured action, such as sending the message to the recipient's Junk Email folder.</span></span> 
  

