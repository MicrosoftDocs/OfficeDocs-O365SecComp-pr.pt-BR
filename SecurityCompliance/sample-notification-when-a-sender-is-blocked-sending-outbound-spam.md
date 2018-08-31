---
title: Notificação de amostra quando um remetente for bloqueado enviem spam de saída
ms.author: krowley
author: kccross
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
description: 'Quando um remetente seja bloqueado para o serviço devido ao envio de spam de saída, o administrador de domínio especificado quando você configurar a política de spam de saída receberá um email de notificação semelhante ao seguinte:'
ms.openlocfilehash: b9fcdf9c2f44a4446a678ca4b22a0a12b24b6fd4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003240"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="9891e-103">Notificação de amostra quando um remetente for bloqueado enviem spam de saída</span><span class="sxs-lookup"><span data-stu-id="9891e-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="9891e-104">Quando um remetente é bloqueado pelo serviço devido ao envio de saída de spam, o administrador de domínio especificado quando você [Configurar a política de spam de saída](configure-the-outbound-spam-policy.md) receberá um email de notificação semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="9891e-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="9891e-105">**Endereço do remetente:** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9891e-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="9891e-106">**Assunto:** Notificação de spam de saída - \< *nome da conta* \> bloqueado para enviar email de saída    </span><span class="sxs-lookup"><span data-stu-id="9891e-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="9891e-107">**Corpo:** Esta é uma resposta automática do sistema de análise de Spam do Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="9891e-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="9891e-p101">Você está sendo contatado porque foi detectado volumes altos de email marcadas como spam ou outro comportamento suspeito, provenientes de sua organização. As contas de email a seguir foram bloqueadas enviem email (eles ainda poderá receber email):</span><span class="sxs-lookup"><span data-stu-id="9891e-p101">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization. The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="9891e-110">\<*nome da conta*  \></span><span class="sxs-lookup"><span data-stu-id="9891e-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="9891e-p102">É provável que essa conta de email foi comprometida. Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9891e-p102">It is likely that this email account has been compromised. Please follow these steps:</span></span>
  
1. <span data-ttu-id="9891e-113">Resolva esse problema no seu lado a lado:</span><span class="sxs-lookup"><span data-stu-id="9891e-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="9891e-114">Alterando a senha da conta.</span><span class="sxs-lookup"><span data-stu-id="9891e-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="9891e-115">Determinar como a conta foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="9891e-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="9891e-116">Tomando precauções para garantir que essa vulnerabilidade não vai ser explorada novamente.</span><span class="sxs-lookup"><span data-stu-id="9891e-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="9891e-117">Confirmando que a sua fila de mensagens de saída foi limpa de todas as mensagens ofensivos.</span><span class="sxs-lookup"><span data-stu-id="9891e-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="9891e-118">Contate o suporte da Microsoft usando seu canal de contato regular.</span><span class="sxs-lookup"><span data-stu-id="9891e-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="9891e-119">Explique que você tenha um usuário que seja bloqueado para enviar email e que o problema tiver sido resolvido com.</span><span class="sxs-lookup"><span data-stu-id="9891e-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="9891e-120">O agente criará um tíquete de suporte com as informações que você forneça e escalá-lo para configurar o endereço de email ou domínio desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="9891e-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="9891e-121">Depois que o endereço foi desbloqueado e pendentes sem outros problemas, você será contatado e alertado sobre o desbloqueando.</span><span class="sxs-lookup"><span data-stu-id="9891e-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="9891e-122">Obrigado por auxiliando conosco controlando indesejadas de email.</span><span class="sxs-lookup"><span data-stu-id="9891e-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="9891e-123">Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="9891e-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="9891e-124">\*\*Observação:-não responda a este email conforme ela é enviada de um endereço não monitorado\*\*</span><span class="sxs-lookup"><span data-stu-id="9891e-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="9891e-125">Você também pode contatar o suporte via as opções documentados em [Ajuda e suporte para EOP](eop/help-and-support-for-eop.md).</span><span class="sxs-lookup"><span data-stu-id="9891e-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

