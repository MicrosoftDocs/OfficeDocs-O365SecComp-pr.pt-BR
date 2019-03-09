---
title: Usar notificações de spam do usuário para liberar e relatar mensagens em quarentena no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Se seu administrador habilitar as notificações para usuários, você receberá uma mensagem de notificação que lista as mensagens enviadas para sua caixa de correio que foram identificadas como spam, massa ou mensagens de phishing. Você pode liberar ou relatar mensagens depois de ser notificado.
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492720"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="1e6cb-104">Usar notificações de spam do usuário para liberar e relatar mensagens em quarentena no Office 365</span><span class="sxs-lookup"><span data-stu-id="1e6cb-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="1e6cb-105">Se seu administrador habilitar notificações de spam para usuários, você receberá uma mensagem de notificação que lista as mensagens endereçadas à sua caixa de correio que foram identificadas como spam e colocadas em quarentena.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="1e6cb-106">Se você é um administrador e deseja habilitar esse recurso, você pode escolher a opção ao [modificar uma política antispam padrão](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="1e6cb-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="1e6cb-107">A mensagem recebida inclui o número de mensagens de spam em quarentena que você tem e a data e a hora (no UTC ou horário coordenado universal) da última mensagem na lista.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="1e6cb-108">A lista inclui o seguinte para cada mensagem:</span><span class="sxs-lookup"><span data-stu-id="1e6cb-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="1e6cb-109">**Remetente** O nome de envio e o endereço de email da mensagem em quarentena.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="1e6cb-110">**Assunto** O texto da linha do assunto da mensagem em quarentena.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="1e6cb-111">**Data** A data e a hora (em UTC) em que a mensagem foi colocada em quarentena.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="1e6cb-112">**Tamanho** O tamanho da mensagem, em kilobytes (KBs).</span><span class="sxs-lookup"><span data-stu-id="1e6cb-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="1e6cb-113">No momento, há duas ações que você pode realizar com uma mensagem em quarentena:</span><span class="sxs-lookup"><span data-stu-id="1e6cb-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="1e6cb-114">**Liberar para caixa de entrada** Escolha esta caixa de correio para enviar a mensagem para sua caixa de entrada, onde você pode exibi-la.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="1e6cb-115">**Relatar como não sendo lixo eletrônico** Escolha esta para enviar uma cópia da mensagem para a Microsoft para análise.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-115">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis.</span></span> <span data-ttu-id="1e6cb-116">A equipe de spam avalia e analisa a mensagem e, dependendo dos resultados da análise, ajusta as regras do filtro antispam para permitir a passagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-116">The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="1e6cb-117">Esteja ciente do seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e6cb-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="1e6cb-118">As mensagens colocadas em quarentena porque corresponderam a uma regra de fluxo de emails não estão incluídas nas mensagens em quarentena do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-118">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="1e6cb-119">Somente as mensagens em quarentena por spam estão listadas.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-119">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="1e6cb-120">Você só pode liberar uma mensagem e relatá-la como falso positivo (e não como lixo eletrônico) uma vez.</span><span class="sxs-lookup"><span data-stu-id="1e6cb-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

