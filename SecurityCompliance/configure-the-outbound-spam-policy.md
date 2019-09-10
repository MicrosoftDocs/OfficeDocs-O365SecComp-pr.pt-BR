---
title: Configurar notificações de política de spam de saída no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Os administradores podem aprender a modificar as configurações de notificação para detecções de spam de saída no Office 365.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822511"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a><span data-ttu-id="bce4f-103">Configurar notificações de política de spam de saída no Office 365</span><span class="sxs-lookup"><span data-stu-id="bce4f-103">Configure outbound spam policy notifications in Office 365</span></span>

<span data-ttu-id="bce4f-104">A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados.</span><span class="sxs-lookup"><span data-stu-id="bce4f-104">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients.</span></span> <span data-ttu-id="bce4f-105">Semelhante a filtragem de entrada, a filtragem de spam de saída é composta de filtragem de conexão e de conteúdo, porém, as configurações do filtro de saída não são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="bce4f-105">Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable.</span></span> <span data-ttu-id="bce4f-106">Se uma mensagem de saída é considerada spam, ela é roteada através do pool de entrega de risco mais alto, que reduz a probabilidade do pool de IP de saída normal estar sendo adicionado a uma lista de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="bce4f-106">If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span> <span data-ttu-id="bce4f-107">Se um cliente continua a enviar spam de saída através do serviço, será impedido de enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="bce4f-107">If a customer continues to send outbound spam through the service, they will be blocked from sending messages.</span></span>

<span data-ttu-id="bce4f-108">Embora você não possa desabilitar ou alterar a filtragem de spam de saída, é possível definir as seguintes configurações de notificação de spam de saída:</span><span class="sxs-lookup"><span data-stu-id="bce4f-108">Although you can't disable or change outbound spam filtering, you can configure the following outbound spam notification settings:</span></span>

- <span data-ttu-id="bce4f-109">**Enviar cópias de mensagens suspeitas**: essas mensagens são marcadas como spam (independentemente da classificação de SCL) e não são rejeitadas pelo filtro, mas são roteadas através do pool de entrega de risco mais alto.</span><span class="sxs-lookup"><span data-stu-id="bce4f-109">**Send copies of suspicious messages**: These messages are marked as spam (regardless of the SCL rating) and are not rejected by the filter, but are routed through the higher risk delivery pool.</span></span> <span data-ttu-id="bce4f-110">Você pode usar o centro de administração do Exchange (Eat) ou os cmdlets \*\* \*-HostedOutboundSpamFilterPolicy\*\* no PowerShell do Exchange Online ou do Exchange Online Protection para especificar destinatários de adição para essas mensagens detectadas.</span><span class="sxs-lookup"><span data-stu-id="bce4f-110">You can use the Exchange admin center (EAC) or the **\*-HostedOutboundSpamFilterPolicy** cmdlets in Exchange Online PowerShell or Exchange Online Protection PowerShell to specify addition recipients for these detected messages.</span></span> <span data-ttu-id="bce4f-111">Observe que os destinatários são adicionados como destinatários **Cco** (os campos **de** e **para** são o remetente e o destinatário originais).</span><span class="sxs-lookup"><span data-stu-id="bce4f-111">Note that the recipients are added as **Bcc** recipients (the **From** and **To** fields are the original sender and recipient).</span></span>

- <span data-ttu-id="bce4f-112">**Enviar notificações quando um remetente é bloqueado**: quando uma quantidade significativa de spam é proveniente de um determinado usuário, o usuário é desabilitado de enviar mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="bce4f-112">**Send notifications when a sender is blocked**: When a significant amount of spam is coming from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="bce4f-113">Os administradores são notificados por padrão, mas você pode usar a [política de alerta](alert-policies.md) **do usuário que está impedido de enviar emails** no centro de conformidade & segurança do Office 365 para configurar destinatários de notificação adicionais.</span><span class="sxs-lookup"><span data-stu-id="bce4f-113">Admins are notified by default, but you can use the **User restricted from sending email** [alert policy](alert-policies.md) in the Office 365 Security & Compliance Center to configure additional notification recipients.</span></span>

  <span data-ttu-id="bce4f-114">Para ver a aparência dessa notificação, confira [exemplo de notificação quando um remetente estiver bloqueado enviando spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span><span class="sxs-lookup"><span data-stu-id="bce4f-114">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="bce4f-115">Para obter informações sobre como habilitar novamente, consulte [removendo um usuário, domínio ou endereço IP de uma lista de bloqueios após o envio de email de spam](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="bce4f-115">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="bce4f-116">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="bce4f-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="bce4f-117">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="bce4f-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="bce4f-118">Para abrir o Centro de Conformidade e Segurança, confira [Acessar o Centro de Conformidade e Segurança do Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="bce4f-118">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="bce4f-119">Para abrir o Eat, confira [centro de administração do Exchange no Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) ou [no centro de administração do Exchange no Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="bce4f-119">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="bce4f-120">Para abrir o PowerShell do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="bce4f-120">To open Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="bce4f-121">Para abrir o PowerShell do Exchange Online Protection, confira [conectar-se ao PowerShell do Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="bce4f-121">To open Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="bce4f-122">Sua conta precisa receber permissões para que você possa executar este procedimento.</span><span class="sxs-lookup"><span data-stu-id="bce4f-122">Your account needs to be assigned permissions before you can perform this procedure.</span></span> <span data-ttu-id="bce4f-123">Para ver de que permissões você precisa, consulte a entrada de função "Gerenciar alertas" em [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="bce4f-123">To see what permissions you need, see the "Manage Alerts" role entry in [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="bce4f-124">Use o Eat para configurar destinatários adicionais para mensagens de spam de saída</span><span class="sxs-lookup"><span data-stu-id="bce4f-124">Use the EAC to configure additional recipients for outbound spam messages</span></span>

1. <span data-ttu-id="bce4f-125">No Eat, vá para **proteção** \> **spam de saída**.</span><span class="sxs-lookup"><span data-stu-id="bce4f-125">In the EAC, go to **Protection** \> **Outbound spam**.</span></span>

2. <span data-ttu-id="bce4f-126">Selecione a política denominada **padrão**e clique em **Editar** ![ícone](media/ITPro-EAC-EditIcon.png)de edição.</span><span class="sxs-lookup"><span data-stu-id="bce4f-126">Select the policy named **Default**, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>

3. <span data-ttu-id="bce4f-127">Na página de propriedades que é aberta, verifique se a guia **preferências de spam de saída** está selecionada e, em seguida, defina a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="bce4f-127">In the properties page that opens, verify that the **Outbound spam preferences** tab is selected, and then configure the following setting:</span></span>

   <span data-ttu-id="bce4f-128">**Envie uma cópia de todas as mensagens de email de saída suspeitas para o endereço ou endereços de email a seguir**: marque a caixa de seleção e insira os endereços de email de um ou mais administradores que devem ser adicionados ao campo **Cco** de mensagens detectadas.</span><span class="sxs-lookup"><span data-stu-id="bce4f-128">**Send a copy of all suspicious outbound email messages to the following email address or addresses**: Select the check box and enter the email addresses of one or more administrators who should be added to the **Bcc** field of detected messages.</span></span> <span data-ttu-id="bce4f-129">Separe vários endereços de email com um ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="bce4f-129">Separate multiple email addresses with a semicolon ( ; ).</span></span>

   <span data-ttu-id="bce4f-130">Quando concluir, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bce4f-130">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="bce4f-131">Usar o PowerShell do Exchange Online ou do Exchange Online Protection para configurar destinatários adicionais para mensagens de spam de saída</span><span class="sxs-lookup"><span data-stu-id="bce4f-131">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure additional recipients for outbound spam messages</span></span>

<span data-ttu-id="bce4f-132">Para habilitar e configurar destinatários adicionais para mensagens de spam de saída, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="bce4f-132">To enable and configure additional recipients for outbound spam messages, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- <span data-ttu-id="bce4f-133">Para especificar os destinatários que substituem todos os valores existentes, `emailaddress1,emailaddress2,...emailaddressN`use a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="bce4f-133">To specify recipients that overwrite all existing values, use the syntax `emailaddress1,emailaddress2,...emailaddressN`.</span></span>

- <span data-ttu-id="bce4f-134">Para adicionar ou remover seletivamente destinatários sem afetar as outras entradas, use a sintaxe `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span><span class="sxs-lookup"><span data-stu-id="bce4f-134">To selectively add or remove recipients without affecting the other entries, use the syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span></span>

<span data-ttu-id="bce4f-135">Este exemplo habilita e configura o chris@contoso.com, o laura@contoso.com e o julia@contoso.com como destinatários Cco para mensagens de spam de saída.</span><span class="sxs-lookup"><span data-stu-id="bce4f-135">This example enables and configures chris@contoso.com, laura@contoso.com and julia@contoso.com as Bcc recipients for outbound spam messages.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

<span data-ttu-id="bce4f-136">Este exemplo adiciona michelle@contoso.com como um destinatário adicional Cco.</span><span class="sxs-lookup"><span data-stu-id="bce4f-136">This example adds michelle@contoso.com as an additional Bcc recipient.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

<span data-ttu-id="bce4f-137">Este exemplo remove chris@contoso.com e julia@contoso.com da lista de destinatários Cco.</span><span class="sxs-lookup"><span data-stu-id="bce4f-137">This example removes chris@contoso.com and julia@contoso.com from the list of Bcc recipients.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

<span data-ttu-id="bce4f-138">Para informações detalhadas de sintaxes e de parâmetros, consulte [set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="bce4f-138">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

<span data-ttu-id="bce4f-139">**Observação**: execute o comando `Get-HostedOutboundSpamFilterPolicy | Format-List` para ver os valores atuais das propriedades *BccSuspiciousOutboundMail* e *BccSuspiciousOutboundAdditionalRecipients* .</span><span class="sxs-lookup"><span data-stu-id="bce4f-139">**Note**: Run the command `Get-HostedOutboundSpamFilterPolicy | Format-List` to see the current values of the *BccSuspiciousOutboundMail* and *BccSuspiciousOutboundAdditionalRecipients* properties.</span></span>

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a><span data-ttu-id="bce4f-140">Usar o centro de conformidade de & de segurança para configurar notificações quando um remetente for bloqueado</span><span class="sxs-lookup"><span data-stu-id="bce4f-140">Use the Security & Compliance Center to configure notifications when a sender is blocked</span></span>

1. <span data-ttu-id="bce4f-141">No centro de conformidade & segurança, vá para \*\*\*\* \> **políticas de alerta**de alertas.</span><span class="sxs-lookup"><span data-stu-id="bce4f-141">In the Security & Compliance Center, go to **Alerts** \> **Alert Policies**.</span></span>

2. <span data-ttu-id="bce4f-142">Localize e selecione a política chamada **usuário impedida de enviar emails**.</span><span class="sxs-lookup"><span data-stu-id="bce4f-142">Find and select the policy named **User restricted from sending email**.</span></span>

3. <span data-ttu-id="bce4f-143">Na saída aberta, clique em **Editar política**.</span><span class="sxs-lookup"><span data-stu-id="bce4f-143">In the fly out that opens, click **Edit policy**.</span></span>

4. <span data-ttu-id="bce4f-144">Na página **Editar destinatários** exibida, defina as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="bce4f-144">In the **Edit recipients** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="bce4f-145">**Enviar notificações por email**: Verifique se **em** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="bce4f-145">**Send email notifications**: Verify that **On** is selected.</span></span>

   - <span data-ttu-id="bce4f-146">**Destinatários de email**: por padrão, o **TenantAdmins** é o único valor aqui.</span><span class="sxs-lookup"><span data-stu-id="bce4f-146">**Email recipients**: By default **TenantAdmins** is the only value here.</span></span> <span data-ttu-id="bce4f-147">Para adicionar destinatários adicionais, clique em um ponto vazio nesta caixa, comece a digitar o destinatário e selecione o destinatário quando seu nome for resolvido.</span><span class="sxs-lookup"><span data-stu-id="bce4f-147">To add additional recipients, click in an empty spot in this box, start typing the recipient, and select the recipient when their name resolves.</span></span> <span data-ttu-id="bce4f-148">Para remover destinatários, clique no **X** ao lado de seus nomes.</span><span class="sxs-lookup"><span data-stu-id="bce4f-148">To remove recipients, click on the **X** next to their names.</span></span>

   - <span data-ttu-id="bce4f-149">**Limite diário de notificação**: o valor padrão é **sem limite**, mas você pode configurar vários limites de 1 a 200.</span><span class="sxs-lookup"><span data-stu-id="bce4f-149">**Daily notification limit**: The default value is **No limit**, but you can configure various limits from 1 to 200.</span></span>

   <span data-ttu-id="bce4f-150">Quando concluir, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bce4f-150">When you're finished, click **Save**.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="bce4f-151">Para saber mais</span><span class="sxs-lookup"><span data-stu-id="bce4f-151">For more information</span></span>

[<span data-ttu-id="bce4f-152">Pool de entrega de alto risco para mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="bce4f-152">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="bce4f-153">Perguntas frequentes sobre proteção antispam</span><span class="sxs-lookup"><span data-stu-id="bce4f-153">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
