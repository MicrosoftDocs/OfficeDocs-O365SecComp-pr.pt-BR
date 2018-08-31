---
title: Configurar as notificações de spam para o usuário final no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
description: Você pode configurar as notificações de spam do usuário final para a política padrão de filtro de conteúdo para toda a organização ou para políticas personalizadas de filtro de conteúdo que são aplicadas aos domínios.
ms.openlocfilehash: 990fa31cc22b33d235d6e8f106511996a52212a2
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002920"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="1500a-103">Configurar as notificações de spam para o usuário final no EOP</span><span class="sxs-lookup"><span data-stu-id="1500a-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1500a-p101">Este tópico é para clientes do Exchange Online Protection (EOP) que estão protegendo as caixas de correio local. Clientes do Exchange Online que estão protegendo as caixas de correio hospedadas em nuvem em vez disso, devem ler o tópico a seguir: [Configure End-User spam notificações no Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="1500a-p101">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes. Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="1500a-p102">Você pode configurar as notificações de spam do usuário final para a política padrão de filtro de conteúdo para toda a organização ou para políticas personalizadas de filtro de conteúdo que são aplicadas aos domínios. Habilitar mensagens de notificação de spam do usuário final permite que os usuários finais gerenciem as suas próprias mensagens de spam em quarentena. As notificações de spam do usuário final não podem ser usadas com as políticas aplicadas a usuários ou grupos, ou a uma política com exceções.</span><span class="sxs-lookup"><span data-stu-id="1500a-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="1500a-p103">As notificações de spam do usuário final contém uma lista de todas as mensagens de spam em quarentena que o usuário final recebeu durante um período de tempo que você configurou (você pode especificar um valor entre 1 e 15 dias). Você também pode configurar o idioma no qual a mensagem de notificação será escrita.</span><span class="sxs-lookup"><span data-stu-id="1500a-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="1500a-111">Após receber uma mensagem de notificação, os usuários dinais podem clicar para mover o email de spam para a caixa de entrada ou relatar o email de spam como Não é Lixo Eletrônico, neste caso será enviado para a Equipe de Análise de Spam do Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1500a-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1500a-112">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="1500a-112">What do you need to know before you begin?</span></span>
<span data-ttu-id="1500a-113"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="1500a-113"></span></span>

<span data-ttu-id="1500a-114">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="1500a-114">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="1500a-p104">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Antispam", no tópico [Permissões de recurso no EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="1500a-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](eop/feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="1500a-117">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="1500a-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="1500a-118">Use o EAC para configurar as notificações de spam do usuário final</span><span class="sxs-lookup"><span data-stu-id="1500a-118">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="1500a-119">No Centro de Administração do Exchange (EAC), navegue até **Proteção** \> **Filtro de conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="1500a-119">In the Exchange admin center (EAC), navigate to **Protection** \> **Content filter**.</span></span>
    
2. <span data-ttu-id="1500a-120">Selecione a política de filtro de conteúdo para a qual você deseja habilitar as notificações de spam do usuário final (elas são desabilitadas por padrão).</span><span class="sxs-lookup"><span data-stu-id="1500a-120">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="1500a-121">No painel direito, onde as informações resumidas sobre política aparecem, clique no link **Configurar notificações de spam para o usuário final**.</span><span class="sxs-lookup"><span data-stu-id="1500a-121">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="1500a-122">Na caixa de diálogo posterior, você pode configurar as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="1500a-122">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="1500a-p105">**Habilitar notificações de spam para o usuário final** Marque esta caixa de seleção para habilitar notificações de spam para o usuário final para esta política. (De outra forma, se esta política estiver habilitada, você pode desmarcar esta caixa de seleção para desabilitar as notificações de spam para usuário final para esta política.)</span><span class="sxs-lookup"><span data-stu-id="1500a-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="1500a-p106">**Envie notificações de spam para o usuário final a cada (dias)** Especifique a frequência com a qual as notificações de spam para o usuário final são enviadas. O padrão é 3 dias. Você pode especificar entre 1 e 15 dias. Se você especificar 7 dias, por exemplo, a notificação incluirá uma lista de todas as mensagens para aquele usuários dos últimos 7 dias que foram enviadas para a quarentena de spam.</span><span class="sxs-lookup"><span data-stu-id="1500a-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="1500a-129">**Idioma da notificação** Usando a lista suspensa, escolha o idioma de escrita das notificações de spam para o usuário final para esta diretiva.</span><span class="sxs-lookup"><span data-stu-id="1500a-129">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="1500a-p107">Clique em **salvar**. Um resumo das suas configurações de política de filtro de conteúdo, incluindo as suas cnfigurações de notificação de spam para o usuário final, aparecem no painel do lado direito.</span><span class="sxs-lookup"><span data-stu-id="1500a-p107">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="1500a-p108">As notificações de spam do usuário final só serão funcionais para as políticas de filtragem de conteúdo que estiverem habilitadas. >  As notificações de spam do usuário final só são enviadas uma vez por dia. O horário de entrega da notificação não pode ser garantido para qualquer cliente específico e não é configurável.</span><span class="sxs-lookup"><span data-stu-id="1500a-p108">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="1500a-p109">**Dica:** Se você deseja testar notificações de spam do usuário final enviando-as para um conjunto limitado de usuários antes de implementá-las completamente, crie uma política de filtro de conteúdo personalizado que habilite as notificações de spam do usuário final dos domínios nos quais os usuários residem. Em seguida, no EAC, em **Fluxo de email \> regras**, crie uma regra de transporte para bloquear as mensagens de quarantine@messaging.microsoft.com (o endereço de email que envia notificações) com exceções para os usuários dos quais você deseja receber notificações. A imagem a seguir é um exemplo de criação de uma exceção de dois usuários (SaraD e AlbertoD) do domínio Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="1500a-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Regra de transporte para testar notificações de spam do usuário final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="1500a-139">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="1500a-139">For more information</span></span>

[<span data-ttu-id="1500a-140">Configurar suas políticas de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="1500a-140">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
