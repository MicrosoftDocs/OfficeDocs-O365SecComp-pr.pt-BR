---
title: Introdução à política DLP padrão
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Antes de criar sua primeira diretiva de prevention (DLP) de perda de dados até mesmo, DLP é ajudar a proteger suas informações confidenciais com uma política padrão. Essa diretiva padrão e seu recomendação (mostrada abaixo) ajudam a manter seu conteúdo confidencial seguro por informando quando o número do cartão de email ou documentos contendo um crédito foram compartilhadas com alguém de fora da sua organização.
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524718"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="761ff-104">Introdução à política DLP padrão</span><span class="sxs-lookup"><span data-stu-id="761ff-104">Get started with the default DLP policy</span></span>

<span data-ttu-id="761ff-p102">Antes de criar sua primeira diretiva de prevention (DLP) de perda de dados até mesmo, DLP é ajudar a proteger suas informações confidenciais com uma política padrão. Essa diretiva padrão e seu recomendação (mostrada abaixo) ajudam a manter seu conteúdo confidencial seguro por informando quando o número do cartão de email ou documentos contendo um crédito foram compartilhadas com alguém de fora da sua organização. Você verá essa recomendação na página **inicial** da segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="761ff-p102">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy. This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization. You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="761ff-p103">Você pode usar este widget para visualizar rapidamente quando e quanta informação confidencial foi compartilhada e, em seguida, refinar a política DLP padrão em apenas um ou dois cliques. Você também pode editar a política DLP padrão a qualquer momento, porque ele é totalmente personalizável. Observe que se você não vir a recomendação inicialmente, tente clicando em **+ mais** na parte inferior da seção **recomendado para você** .</span><span class="sxs-lookup"><span data-stu-id="761ff-p103">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two. You can also edit the default DLP policy at any time because it's fully customizable. Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Widget denominado adicionais proteger conteúdo compartilhado](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="761ff-112">Exibir o relatório e refinar a política DLP padrão</span><span class="sxs-lookup"><span data-stu-id="761ff-112">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="761ff-113">Quando o widget mostra que os usuários compartilhou informações confidenciais com pessoas fora da sua organização, escolha a **política de DLP refinar** na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="761ff-113">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="761ff-p104">O relatório detalhado mostra quando e como a quantidade de conteúdo que contém os números de cartão de crédito foi compartilhada nos últimos 30 dias. Observe que as correspondências de regra podem levar até 48 horas seja mostrada no widget.</span><span class="sxs-lookup"><span data-stu-id="761ff-p104">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days. Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="761ff-116">Para ajudar a proteger as informações confidenciais, a política DLP padrão:</span><span class="sxs-lookup"><span data-stu-id="761ff-116">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="761ff-117">Detecta quando o conteúdo no Exchange, SharePoint e OneDrive que contém o número de pelo menos um cartão de crédito é compartilhado com pessoas fora da sua organização.</span><span class="sxs-lookup"><span data-stu-id="761ff-117">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="761ff-p105">Mostra uma dica de política e envia uma notificação de e-mail para usuários quando eles tentam compartilhar essas informações confidenciais com pessoas fora da sua organização. Para obter mais informações sobre essas opções, consulte [Enviar notificações por email e Mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md).</span><span class="sxs-lookup"><span data-stu-id="761ff-p105">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization. For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="761ff-p106">Gera relatórios de atividade detalhada de modo que você pode controlar coisas como quem o conteúdo compartilhado com pessoas fora da sua organização e quando eles fizeram. Você pode usar os [relatórios DLP](view-the-dlp-reports.md) e os [dados de log de auditoria](search-the-audit-log-in-security-and-compliance.md) (onde **atividade** = **DLP**) para ver essa informação.</span><span class="sxs-lookup"><span data-stu-id="761ff-p106">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it. You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="761ff-122">Para refinar rapidamente a política DLP padrão, você pode optar por fazer com que ele:</span><span class="sxs-lookup"><span data-stu-id="761ff-122">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="761ff-123">Envie um email de relatório de incidente quando usuários compartilharem essas informações confidenciais com pessoas fora da sua organização.</span><span class="sxs-lookup"><span data-stu-id="761ff-123">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="761ff-124">Adicione outros usuários para o relatório de incidente de email.</span><span class="sxs-lookup"><span data-stu-id="761ff-124">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="761ff-125">Bloqueie o acesso ao conteúdo que contém as informações confidenciais, mas permitir que o usuário substituir e compartilhar ou enviar se eles precisam.</span><span class="sxs-lookup"><span data-stu-id="761ff-125">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="761ff-126">Para obter mais informações sobre relatórios de incidentes ou restrição de acesso, consulte [Visão geral das políticas de prevenção de perda de dados](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="761ff-126">For more information on incident reports or restricting access, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="761ff-127">Se você quiser alterar essas opções mais tarde, você pode editar o padrão a política de DLP a qualquer momento - consulte a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="761ff-127">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Configurações de widget denominado adicionais de protegem conteúdo compartilhado](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="761ff-129">Editar a política DLP padrão</span><span class="sxs-lookup"><span data-stu-id="761ff-129">Edit the default DLP policy</span></span>

<span data-ttu-id="761ff-130">Esta diretiva é chamada **política padrão DLP do Office 365** e aparece na **prevenção de perda de dados** na página **política** de segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="761ff-130">This policy is named **Default Office 365 DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="761ff-p107">Essa diretiva é totalmente personalizável, o mesmo que qualquer política DLP que você criou do zero. Você também pode desativar ou excluir a diretiva, para que os usuários não são mais recebem dicas de política ou notificações de email.</span><span class="sxs-lookup"><span data-stu-id="761ff-p107">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch. You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![Política de DLP chamada política padrão DLP do Office 365](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="761ff-134">Quando o widget e não aparecem</span><span class="sxs-lookup"><span data-stu-id="761ff-134">When the widget does and does not appear</span></span>

<span data-ttu-id="761ff-135">O widget denominado **proteger ainda mais o conteúdo compartilhado** aparece na seção **recomendado para você** da página **inicial** da segurança &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="761ff-135">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="761ff-136">Este widget aparece somente quando:</span><span class="sxs-lookup"><span data-stu-id="761ff-136">This widget appears only when:</span></span>
  
- <span data-ttu-id="761ff-p108">Não há nenhuma políticas de prevenção de perda de dados na segurança &amp; Centro de conformidade ou centro de administração do Exchange. Este widget destina-se para ajudá-lo a começar a usar DLP, portanto, ela não será exibido se você já tem políticas de DLP.</span><span class="sxs-lookup"><span data-stu-id="761ff-p108">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange Admin Center. This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="761ff-139">O conteúdo que contém pelo menos um cartão de crédito foi compartilhado com alguém de fora da sua organização nos últimos 30 dias.</span><span class="sxs-lookup"><span data-stu-id="761ff-139">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="761ff-140">Observe que as correspondências de regra podem levar até 48 horas esteja disponível para o widget, portanto após informações confidenciais shared externamente são detectadas, pode levar até dois dias para a recomendação apareça.</span><span class="sxs-lookup"><span data-stu-id="761ff-140">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="761ff-141">Finalmente, depois de usar o widget para refinar a política DLP padrão, o widget desaparecerá da página **inicial** .</span><span class="sxs-lookup"><span data-stu-id="761ff-141">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

