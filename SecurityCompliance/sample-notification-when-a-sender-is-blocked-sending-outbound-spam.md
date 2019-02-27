---
title: Notificação de exemplo quando um remetente é bloqueado enviando spam de saída
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
ms.collection:
- M365-security-compliance
description: 'Quando um remetente é bloqueado do serviço devido ao envio de spam de saída, o administrador de domínio especificado ao configurar a política de spam de saída receberá um email de notificação semelhante ao seguinte:'
ms.openlocfilehash: 94af965505f7541600a6cd7937ae881226a2ac79
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275471"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="c51da-103">Notificação de exemplo quando um remetente é bloqueado enviando spam de saída</span><span class="sxs-lookup"><span data-stu-id="c51da-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="c51da-104">Quando um remetente é bloqueado do serviço devido ao envio de spam de saída, o administrador de domínio especificado ao [Configurar a política de spam de saída](configure-the-outbound-spam-policy.md) receberá um email de notificação semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="c51da-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="c51da-105">**Endereço do remetente:** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c51da-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="c51da-106">**Assunto:** Notificação de spam de \<saída- *nome* \> da conta bloqueado do envio de email de saída    </span><span class="sxs-lookup"><span data-stu-id="c51da-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="c51da-107">**Corpo:** Esta é uma resposta automática do sistema de análise de spam do Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="c51da-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="c51da-p101">Você está sendo contatado porque detectamos altos volumes de email marcados como spam ou outro comportamento suspeito originado da sua organização. As contas de email a seguir foram impedidas de enviar email (eles ainda podem receber emails):</span><span class="sxs-lookup"><span data-stu-id="c51da-p101">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization. The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="c51da-110">\<*nome da conta*  \></span><span class="sxs-lookup"><span data-stu-id="c51da-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="c51da-p102">É provável que essa conta de email tenha sido comprometida. Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="c51da-p102">It is likely that this email account has been compromised. Please follow these steps:</span></span>
  
1. <span data-ttu-id="c51da-113">Resolva este problema ao seu lado:</span><span class="sxs-lookup"><span data-stu-id="c51da-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="c51da-114">Alterar a senha da conta.</span><span class="sxs-lookup"><span data-stu-id="c51da-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="c51da-115">Determinando como a conta foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="c51da-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="c51da-116">Tomar precauções para garantir que essa vulnerabilidade não será explorada novamente.</span><span class="sxs-lookup"><span data-stu-id="c51da-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="c51da-117">Confirmando que a fila de saída de emails foi limpa de todas as mensagens transgressores.</span><span class="sxs-lookup"><span data-stu-id="c51da-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="c51da-118">Entre em contato com o suporte da Microsoft usando seu canal de contato normal.</span><span class="sxs-lookup"><span data-stu-id="c51da-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="c51da-119">Explique que você tem um usuário que é bloqueado pelo envio de emails e que o problema foi tratado.</span><span class="sxs-lookup"><span data-stu-id="c51da-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="c51da-120">O agente criará um tíquete de suporte com as informações que você fornecer e o escalonará para ter o endereço de email ou o domínio desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="c51da-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="c51da-121">Depois que o endereço tiver sido desbloqueado e não tiver outros problemas, você será contatado e alertado para o desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="c51da-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="c51da-122">Obrigado por nos ajudar a controlar emails indesejados.</span><span class="sxs-lookup"><span data-stu-id="c51da-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="c51da-123">Proteção do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c51da-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="c51da-124">\*\*Observação: não responda a este email à medida que ele é enviado de um endereço não monitorado\*\*</span><span class="sxs-lookup"><span data-stu-id="c51da-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="c51da-125">Você também pode entrar em contato com o suporte via opções documentadas em [ajuda e suporte para o EOP](eop/help-and-support-for-eop.md).</span><span class="sxs-lookup"><span data-stu-id="c51da-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

