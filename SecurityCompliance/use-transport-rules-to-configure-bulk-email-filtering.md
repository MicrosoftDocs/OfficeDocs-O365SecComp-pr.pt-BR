---
title: Usar regras de fluxo de email para configurar o email em massa filtragem no Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Os administradores podem Saiba como usar regras de fluxo de correio no Exchange Online Protection para filtragem de email em massa.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382802"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="7dfe7-103">Usar regras de fluxo de email para configurar o email em massa filtragem no Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="7dfe7-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="7dfe7-p101">Você pode definir filtros de conteúdo de toda a empresa para e-mails de spam e em massa usando as políticas de filtro de conteúdo de spam padrão. Confira [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) e [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) sobre como configurar as políticas de filtro de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="7dfe7-p102">Se você quiser mais opções para filtrar mensagens em massa, você pode criar regras de fluxo de email (também conhecido como regras de transporte) para procurar padrões de texto ou frases frequentemente encontradas em emails em massa. Qualquer mensagem que contém essas duas características será marcada como spam. Usar essas regras pode ajudar a reduzir a quantidade de email em massa indesejados que recebe de sua organização.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p102">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
<span data-ttu-id="7dfe7-109">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="7dfe7-109">**Notes**:</span></span>

- <span data-ttu-id="7dfe7-110">Antes de criar regras de fluxo do email documentados neste tópico, recomendamos que você leia primeiro [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) e [valores de nível de reclamações em massa](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe7-110">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
- <span data-ttu-id="7dfe7-p103">Os procedimentos a seguir marcar uma mensagem como spam para toda sua organização. No entanto, você pode adicionar outra condição para aplicar essas regras apenas a destinatários específicos na sua organização. Dessa forma, o email em massa agressivo filtragem de configurações pode ser aplicadas a alguns usuários que são altamente direcionados, enquanto o restante de seus usuários (que principalmente obter email em massa que eles se inscreveu no) não são afetados.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p103">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="7dfe7-114">Criar regra de fluxo de email para filtrar mensagens de email em massa com base em padrões de texto</span><span class="sxs-lookup"><span data-stu-id="7dfe7-114">Create mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="7dfe7-115">No Centro de administração do Exchange (EAC), vá para **Fluxo de emails** \> **Regras**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="7dfe7-116">Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione **Criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="7dfe7-117">Especifique um nome para a regra.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="7dfe7-p104">Clique em **mais opções**. Em **Aplicar esta regra se**, selecione **o assunto ou corpo** \> **assunto ou corpo corresponde a esses padrões de texto**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="7dfe7-120">Na caixa de diálogo **especificar palavras ou expressões**, adicione, uma de cada vez, as seguintes expressões regulares que são normalmente encontradas em emails em massa e clique em **ok** quando tiver concluído:</span><span class="sxs-lookup"><span data-stu-id="7dfe7-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="7dfe7-121">Se não puder ver o conteúdo desse email\,</span><span class="sxs-lookup"><span data-stu-id="7dfe7-121">If you are unable to view the content of this email\, please</span></span>
    
   - <span data-ttu-id="7dfe7-122">\\>cancele sua inscrição( aqui)?( com segurança)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="7dfe7-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
   - <span data-ttu-id="7dfe7-123">Se não quiser receber mais comunicações como esta\,</span><span class="sxs-lookup"><span data-stu-id="7dfe7-123">If you do not wish to receive further communications like this\, please</span></span>
    
   - <span data-ttu-id="7dfe7-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
   - <span data-ttu-id="7dfe7-127">Para parar de receber esses+emails\:http\://</span><span class="sxs-lookup"><span data-stu-id="7dfe7-127">To stop receiving these\s+emails\:http\://</span></span>
    
   - <span data-ttu-id="7dfe7-128">Para cancelar a assinatura de \w+ (f\-?letter | e?-?mail | newsletter)</span><span class="sxs-lookup"><span data-stu-id="7dfe7-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
   - <span data-ttu-id="7dfe7-129">não (deseja )mais?(receber|ver) \w+ email</span><span class="sxs-lookup"><span data-stu-id="7dfe7-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
   - <span data-ttu-id="7dfe7-130">Se não puder ver o conteúdo desse email\, clique aqui</span><span class="sxs-lookup"><span data-stu-id="7dfe7-130">If you are unable to view the content of this email\, please click here</span></span>
    
   - <span data-ttu-id="7dfe7-131">Para garantir o recebimento de (ofertas diárias|nossos e-?mails)\, adicione</span><span class="sxs-lookup"><span data-stu-id="7dfe7-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
   - <span data-ttu-id="7dfe7-132">Se não quiser mais receber esses emails</span><span class="sxs-lookup"><span data-stu-id="7dfe7-132">If you no longer wish to receive these emails</span></span>
    
   - <span data-ttu-id="7dfe7-133">para alterar (preferências de inscrição|preferências or cancelar inscrição)</span><span class="sxs-lookup"><span data-stu-id="7dfe7-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
   - <span data-ttu-id="7dfe7-134">clique (aqui para|em) cancelar a inscrição</span><span class="sxs-lookup"><span data-stu-id="7dfe7-134">click (here to|the) unsubscribe</span></span>
    
   <span data-ttu-id="7dfe7-135">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="7dfe7-135">**Notes**:</span></span>

   - <span data-ttu-id="7dfe7-p106">A lista acima não é um conjunto exaustiva de expressões regulares encontradas em emails em massa; mais podem ser adicionados ou removidos conforme necessário. No entanto, é um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p106">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
   - <span data-ttu-id="7dfe7-p107">A pesquisa por palavras ou padrões de texto no assunto ou outros campos de cabeçalho na mensagem ocorre *depois que* a mensagem tem sido decodificada desde a transferência de conteúdo MIME método que foi usado para transmitir a mensagem binária entre os servidores SMTP texto ASCII de codificação. Você não pode usar as condições ou exceções para pesquisar o raw (geralmente, Base64) codificado valores do assunto ou outros campos de cabeçalho nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p107">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="7dfe7-140">Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="7dfe7-141">Na caixa de diálogo **especificar SCL**, defina o SCL como **5**, **6** ou **9** e clique em **ok**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="7dfe7-p108">Definir o SCL como 5 ou 6 executará a ação de **Spam** , durante a configuração do SCL para 9 leva a ação de **spam de alta confiança** , conforme configurado na política de filtro de conteúdo. O serviço executará a ação definida na política de filtro de conteúdo. A ação padrão é entregar a mensagem para a pasta de lixo eletrônico dos destinatários, mas ações diferentes podem ser configuradas conforme descrito em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p108">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7dfe7-145">Se sua ação configurada for a mensagem em quarentena em vez de enviá-lo para a pasta de lixo eletrônico dos destinatários, a mensagem será enviada para a quarentena administrador conforme uma correspondência de regra de fluxo de email e ele não estará disponível em quarentena de spam do usuário final ou através de usuário final notificações de spam.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="7dfe7-146">Para saber mais sobre os valores de SCL do serviço, veja [Níveis de confiança de spam](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe7-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="7dfe7-147">Salve a regra.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-147">Save the rule.</span></span>
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="7dfe7-148">Criar uma regra de fluxo de email para filtrar mensagens de email em massa com base em frases</span><span class="sxs-lookup"><span data-stu-id="7dfe7-148">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="7dfe7-149">No EAC, vá para **Fluxo de emails** \> **Regras**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="7dfe7-150">Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione **Criar uma nova regra**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="7dfe7-151">Especifique um nome para a regra.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="7dfe7-p109">Clique em **mais opções**. Em **Aplicar esta regra se**, selecione **o assunto ou corpo** \> **assunto ou corpo inclui qualquer uma destas palavras**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p109">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="7dfe7-154">Na caixa de diálogo **especificar palavras ou expressões**, adicione, uma de cada vez, as seguintes frases comuns encontradas em emails em massa e clique em **ok** quando tiver concluído:</span><span class="sxs-lookup"><span data-stu-id="7dfe7-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="7dfe7-155">para alterar suas preferências ou cancelar a assinatura</span><span class="sxs-lookup"><span data-stu-id="7dfe7-155">to change your preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="7dfe7-156">Alterar as preferências de email ou cancelar a assinatura</span><span class="sxs-lookup"><span data-stu-id="7dfe7-156">Modify email preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="7dfe7-157">Este é um email promocional</span><span class="sxs-lookup"><span data-stu-id="7dfe7-157">This is a promotional email</span></span>
    
   - <span data-ttu-id="7dfe7-158">Você está recebendo este email porque solicitou uma assinatura</span><span class="sxs-lookup"><span data-stu-id="7dfe7-158">You are receiving this email because you requested a subscription</span></span>
    
   - <span data-ttu-id="7dfe7-159">clique aqui para cancelar a assinatura</span><span class="sxs-lookup"><span data-stu-id="7dfe7-159">click here to unsubscribe</span></span>
    
   - <span data-ttu-id="7dfe7-160">Você recebeu este email porque se inscreveu em</span><span class="sxs-lookup"><span data-stu-id="7dfe7-160">You have received this email because you are subscribed</span></span>
    
   - <span data-ttu-id="7dfe7-161">Se não quiser mais receber nosso boletim informativo por email</span><span class="sxs-lookup"><span data-stu-id="7dfe7-161">If you no longer wish to receive our email newsletter</span></span>
    
   - <span data-ttu-id="7dfe7-162">para cancelar a assinatura desse boletim informativo</span><span class="sxs-lookup"><span data-stu-id="7dfe7-162">to unsubscribe from this newsletter</span></span>
    
   - <span data-ttu-id="7dfe7-163">Se tiver problema para ver este email</span><span class="sxs-lookup"><span data-stu-id="7dfe7-163">If you have trouble viewing this email</span></span>
    
   - <span data-ttu-id="7dfe7-164">Isto é um anúncio</span><span class="sxs-lookup"><span data-stu-id="7dfe7-164">This is an advertisement</span></span>
    
   - <span data-ttu-id="7dfe7-165">você gostaria de cancelar a assinatura ou alterar sua</span><span class="sxs-lookup"><span data-stu-id="7dfe7-165">you would like to unsubscribe or change your</span></span>
    
   - <span data-ttu-id="7dfe7-166">ver este email como uma página da Web</span><span class="sxs-lookup"><span data-stu-id="7dfe7-166">view this email as a webpage</span></span>
    
   - <span data-ttu-id="7dfe7-167">Você está recebendo este email porque se inscreveu em</span><span class="sxs-lookup"><span data-stu-id="7dfe7-167">You are receiving this email because you are subscribed</span></span>
    
   <span data-ttu-id="7dfe7-p110">**Observação**: mais uma vez, esta lista não é um conjunto exaustiva de frases encontradas em emails em massa; mais podem ser adicionados ou removidos conforme necessário. No entanto, é um bom ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p110">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="7dfe7-170">Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="7dfe7-171">Na caixa de diálogo **especificar SCL**, defina o SCL como **5**, **6** ou **9** e clique em **ok**.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="7dfe7-p111">Definir o SCL como 5 ou 6 executará a ação de **Spam** , durante a configuração do SCL para 9 leva a ação de **spam de alta confiança** , conforme configurado na política de filtro de conteúdo. O serviço executará a ação definida na política de filtro de conteúdo. A ação padrão é entregar a mensagem para a pasta de lixo eletrônico dos destinatários, mas ações diferentes podem ser configuradas conforme descrito em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe7-p111">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7dfe7-175">Se sua ação configurada for a mensagem em quarentena em vez de enviá-lo para a pasta de lixo eletrônico dos destinatários, a mensagem será enviada para a quarentena administrador conforme uma correspondência de regra de fluxo de email e ele não estará disponível em quarentena de spam do usuário final ou através de usuário final notificações de spam.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="7dfe7-176">Para saber mais sobre os valores de SCL do serviço, veja [Níveis de confiança de spam](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7dfe7-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="7dfe7-177">Salve a regra.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-177">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="7dfe7-178">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="7dfe7-178">For more information</span></span>

[<span data-ttu-id="7dfe7-179">Qual é a diferença entre lixo eletrônico e email em massa?</span><span class="sxs-lookup"><span data-stu-id="7dfe7-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="7dfe7-180">Valores de nível compatível com dados em massa</span><span class="sxs-lookup"><span data-stu-id="7dfe7-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="7dfe7-181">Configurar suas políticas de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="7dfe7-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="7dfe7-182">Opções de filtragem de spam avançadas</span><span class="sxs-lookup"><span data-stu-id="7dfe7-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
