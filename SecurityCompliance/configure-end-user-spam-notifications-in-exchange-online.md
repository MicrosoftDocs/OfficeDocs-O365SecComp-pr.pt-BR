---
title: Configurar as notificações de spam do usuário final no Exchange Online
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
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Você pode configurar as notificações de spam do usuário final para a política padrão de filtro de conteúdo para toda a organização ou para políticas personalizadas de filtro de conteúdo que são aplicadas aos domínios.
ms.openlocfilehash: da370497f78d7f253276c908061a9a80e2f74938
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002735"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="77573-103">Configurar as notificações de spam do usuário final no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="77573-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77573-p101">Este tópico é para clientes Exchange Online que estão protegendo as caixas de correio hospedadas em nuvem. Clientes do Exchange Online Protection (EOP) que estão protegendo as caixas de correio locais em vez disso, devem ler o tópico a seguir: [Configure notificações de spam do usuário final no EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="77573-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="77573-p102">Você pode configurar as notificações de spam do usuário final para a política padrão de filtro de conteúdo para toda a organização ou para políticas personalizadas de filtro de conteúdo que são aplicadas aos domínios. Habilitar mensagens de notificação de spam do usuário final permite que os usuários finais gerenciem as suas próprias mensagens de spam em quarentena. As notificações de spam do usuário final não podem ser usadas com as políticas aplicadas a usuários ou grupos, ou a uma política com exceções.</span><span class="sxs-lookup"><span data-stu-id="77573-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="77573-p103">As notificações de spam do usuário final contém uma lista de todas as mensagens de spam em quarentena que o usuário final recebeu durante um período de tempo que você configurou (você pode especificar um valor entre 1 e 15 dias). Você também pode configurar o idioma no qual a mensagem de notificação será escrita.</span><span class="sxs-lookup"><span data-stu-id="77573-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="77573-111">Após receber uma mensagem de notificação, os usuários dinais podem clicar para mover o email de spam para a caixa de entrada ou relatar o email de spam como Não é Lixo Eletrônico, neste caso será enviado para a Equipe de Análise de Spam do Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77573-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="77573-112">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="77573-112">What do you need to know before you begin?</span></span>

<span data-ttu-id="77573-113">Tempo estimado para conclusão: 2 minutos</span><span class="sxs-lookup"><span data-stu-id="77573-113">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="77573-p104">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Antispam" no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="77573-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="77573-116">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="77573-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="77573-117">Use o EAC para configurar as notificações de spam do usuário final</span><span class="sxs-lookup"><span data-stu-id="77573-117">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="77573-118">No Centro de Administração do Exchange (EAC), navegue até **Proteção** \> **Filtro de conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="77573-118">In the Exchange admin center (EAC), navigate to **Protection** \> **Content filter**.</span></span>
    
2. <span data-ttu-id="77573-119">Selecione a política de filtro de conteúdo para a qual você deseja habilitar as notificações de spam do usuário final (elas são desabilitadas por padrão).</span><span class="sxs-lookup"><span data-stu-id="77573-119">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="77573-120">No painel direito, onde as informações resumidas sobre política aparecem, clique no link **Configurar notificações de spam para o usuário final**.</span><span class="sxs-lookup"><span data-stu-id="77573-120">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="77573-121">Na caixa de diálogo posterior, você pode configurar as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="77573-121">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="77573-p105">**Habilitar notificações de spam para o usuário final** Marque esta caixa de seleção para habilitar notificações de spam para o usuário final para esta política. (De outra forma, se esta política estiver habilitada, você pode desmarcar esta caixa de seleção para desabilitar as notificações de spam para usuário final para esta política.)</span><span class="sxs-lookup"><span data-stu-id="77573-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="77573-p106">**Envie notificações de spam para o usuário final a cada (dias)** Especifique a frequência com a qual as notificações de spam para o usuário final são enviadas. O padrão é 3 dias. Você pode especificar entre 1 e 15 dias. Se você especificar 7 dias, por exemplo, a notificação incluirá uma lista de todas as mensagens para aquele usuários dos últimos 7 dias que foram enviadas para a quarentena de spam.</span><span class="sxs-lookup"><span data-stu-id="77573-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="77573-128">**Idioma da notificação** Usando a lista suspensa, escolha o idioma de escrita das notificações de spam para o usuário final para esta diretiva.</span><span class="sxs-lookup"><span data-stu-id="77573-128">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="77573-p107">Clique em **salvar**. Um resumo das suas configurações de política de filtro de conteúdo, incluindo as suas cnfigurações de notificação de spam para o usuário final, aparecem no painel do lado direito.</span><span class="sxs-lookup"><span data-stu-id="77573-p107">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="77573-p108">As notificações de spam do usuário final só serão funcionais para as políticas de filtragem de conteúdo que estiverem habilitadas. >  As notificações de spam do usuário final só são enviadas uma vez por dia. O horário de entrega da notificação não pode ser garantido para qualquer cliente específico e não é configurável.</span><span class="sxs-lookup"><span data-stu-id="77573-p108">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="77573-p109">**Dica:** Se você deseja testar notificações de spam do usuário final enviando-as para um conjunto limitado de usuários antes de implementá-las completamente, crie uma política de filtro de conteúdo personalizado que habilite as notificações de spam do usuário final dos domínios nos quais os usuários residem. Em seguida, no EAC, em **Fluxo de email \> regras**, crie uma regra de transporte para bloquear as mensagens de quarantine@messaging.microsoft.com (o endereço de email que envia notificações) com exceções para os usuários dos quais você deseja receber notificações. A imagem a seguir é um exemplo de criação de uma exceção de dois usuários (SaraD e AlbertoD) do domínio Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="77573-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Regra de transporte para testar notificações de spam do usuário final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="77573-138">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="77573-138">For more information</span></span>

[<span data-ttu-id="77573-139">Configurar suas políticas de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="77573-139">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  