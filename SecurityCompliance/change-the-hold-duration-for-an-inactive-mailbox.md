---
title: Alterar a duração de espera para uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Depois que uma caixa de correio do Office 365 é feita inativa, você pode alterar a duração da retenção ou política de retenção do Office 365 atribuído à caixa de correio inativa. A duração de espera define quanto tempo os itens na pasta são mantidos itens recuperáveis.
ms.openlocfilehash: e3d1d6c7ec0311813dfa1144cc960d2fed9e160d
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038054"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="b4f5f-104">Alterar a duração de espera para uma caixa de correio inativa no Office 365</span><span class="sxs-lookup"><span data-stu-id="b4f5f-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="b4f5f-p102">Uma caixa de correio inativa é usada para reter o email de um antigo do funcionário depois que ele deixa a sua organização. Uma caixa de correio fica inativa quando um litígio, um bloqueio In-loco, uma política de retenção do Office 365, ou uma isenção que está associado a um caso de eDiscovery é colocada na caixa de correio e a conta de usuário do Office 365 correspondente é excluída. O conteúdo de uma caixa de correio inativa é retido para a duração da retenção feita na caixa de correio antes que ela foi feita inativa. A duração de espera define quanto tempo os itens na pasta são mantidos itens recuperáveis. Quando a duração da retenção expira para um item na pasta itens recuperáveis, o item é excluído permanentemente (descartados) da caixa de correio inativa. Depois que uma caixa de correio é feita inativa, você pode alterar a duração da retenção ou política de retenção do Office 365 atribuído à caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b4f5f-p103">Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="b4f5f-116">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="b4f5f-116">Before you begin</span></span>

- <span data-ttu-id="b4f5f-p104">Você precisa usar o PowerShell do Exchange Online para alterar a duração de espera de um litígio em uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Mas você pode usar o PowerShell do Exchange Online ou o EAC para alterar a duração de espera de um bloqueio In-loco. Você pode usar a segurança do Office 365 &amp; Centro de conformidade ou a segurança &amp; PowerShell do Centro de conformidade para alterar a duração de espera para uma política de retenção do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="b4f5f-121">Para conectar ao PowerShell do Exchange Online ou segurança &amp; PowerShell do Centro de conformidade, consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b4f5f-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="b4f5f-122">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="b4f5f-122">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [<span data-ttu-id="b4f5f-123">Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="b4f5f-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="b4f5f-p105">Observe que retém associado a casos de eDiscovery são infinitas isenções, que significa que não há nenhuma duração de espera pode ser alterada. Itens são mantidos indefinidamente ou até que a suspensão seja removida e a caixa de correio inativa é excluída.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="b4f5f-126">Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="b4f5f-127">Etapa 1: Identificar os bloqueios em uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="b4f5f-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="b4f5f-128">Porque os diferentes tipos de isenções ou uma ou mais políticas de retenção do Office 365 podem ser colocadas em uma caixa de correio inativa, a primeira etapa é identificar os bloqueios em uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="b4f5f-129">Execute o seguinte comando no Exchange Online PowerShell para exibir as informações de espera para todas as caixas de correio inativas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="b4f5f-p106">O valor de **True** para a propriedade **LitigationHoldEnabled** indica que a caixa de correio inativa está em retenção de litígio. Se um bloqueio In-loco, retenção de descoberta eletrônica ou política de retenção do Office 365 é colocada em uma caixa de correio inativa, um GUID para a política de retenção ou retenção é exibido como o valor da propriedade **InPlaceHolds** . Por exemplo, o exemplo a seguir mostra resultados de caixas de correio inativas 5.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
<span data-ttu-id="b4f5f-133">A tabela a seguir identifica os cinco tipos diferentes de espera que foram usados para tornar cada caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="b4f5f-134">**Caixa de correio inativa**</span><span class="sxs-lookup"><span data-stu-id="b4f5f-134">**Inactive mailbox**</span></span>|<span data-ttu-id="b4f5f-135">**Tipo de bloqueio**</span><span class="sxs-lookup"><span data-stu-id="b4f5f-135">**Hold type**</span></span>|<span data-ttu-id="b4f5f-136">**Como identificar o bloqueio na caixa de correio inativa**</span><span class="sxs-lookup"><span data-stu-id="b4f5f-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4f5f-137">Ann Beebe</span><span class="sxs-lookup"><span data-stu-id="b4f5f-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="b4f5f-138">Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="b4f5f-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="b4f5f-139">A propriedade *LitigationHoldEnabled* estiver definida como `True`.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="b4f5f-140">Pilar Pinilla</span><span class="sxs-lookup"><span data-stu-id="b4f5f-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="b4f5f-141">Bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="b4f5f-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="b4f5f-p107">A propriedade *InPlaceHolds* contém o GUID do In-Place Hold é colocado na caixa de correio inativa. Você pode dizer que isso é um bloqueio In-loco, porque a ID não começa com um prefixo.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="b4f5f-144">Você pode usar o ' Get-MailboxSearch - InPlaceHoldIdentity<hold GUID></span><span class="sxs-lookup"><span data-stu-id="b4f5f-144">You can use the  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span></span> | <span data-ttu-id="b4f5f-145">FL' command no PowerShell do Exchange Online para obter mais informações sobre o bloqueio In-loco na caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-145">FL\` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="b4f5f-146">Mario Necaise</span><span class="sxs-lookup"><span data-stu-id="b4f5f-146">Mario Necaise</span></span>  <br/> |<span data-ttu-id="b4f5f-147">Política de retenção do Office 365 toda a organização na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="b4f5f-147">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="b4f5f-p108">A propriedade *InPlaceHolds* está vazia. Isso indica que um ou mais toda a organização ou (Exchange toda) Office 365 política de retenção é aplicada à caixa de correio inativa. Nesse caso, é possível executar o ' Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  \`Get-OrganizationConfig</span></span> | <span data-ttu-id="b4f5f-151">Select-Object - ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="b4f5f-151">Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="b4f5f-152">Nome de FL'</span><span class="sxs-lookup"><span data-stu-id="b4f5f-152">FL Name\`</span></span><br/><br/>
|<span data-ttu-id="b4f5f-153">Carol Olson</span><span class="sxs-lookup"><span data-stu-id="b4f5f-153">Carol Olson</span></span>  <br/> |<span data-ttu-id="b4f5f-154">Política de retenção do Office 365 na segurança &amp; Centro de conformidade aplicadas a caixas de correio específicas</span><span class="sxs-lookup"><span data-stu-id="b4f5f-154">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="b4f5f-p109">A propriedade *InPlaceHolds* contém o GUID da política de retenção Office 365 que é aplicado à caixa de correio inativa. Você pode dizer que essa é uma política de retenção aplicada às caixas de correio específicas, porque o GUID começa com a `mbx` prefixo. Observe que, se o GUID da política de retenção aplicada à caixa de correio inativa iniciados com o `skp` prefixo, que indica se a política de retenção é aplicada para Skype para conversas de negócios.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="b4f5f-158">A política de retenção da identidade do Office 365 que é aplicada à caixa de correio inativa, execute o seguinte comando na segurança &amp; PowerShell do Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-158">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> <span data-ttu-id="b4f5f-159">' Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="b4f5f-159">\`Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="b4f5f-160">Nome de FL` <br/><br/>Be sure to remove the  `mbx` or  `skp' prefix quando você executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-160">FL Name` <br/><br/>Be sure to remove the  `mbx` or  `skp\` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="b4f5f-161">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="b4f5f-161">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="b4f5f-162">retenção de caso de descoberta eletrônica na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="b4f5f-162">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="b4f5f-p110">A propriedade *InPlaceHolds* contém o GUID da isenção casos de eDiscovery que é colocado na caixa de correio inativa. Você pode dizer que isso é uma espera de casos de eDiscovery, porque o GUID começa com a `UniH` prefixo.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="b4f5f-p111">Você pode usar o `Get-CaseHoldPolicy` cmdlet em Security &amp; PowerShell do Centro de conformidade para obter mais informações sobre o caso de eDiscovery que o bloqueio na caixa de correio inativa está associado. Por exemplo, você pode executar o comando ' Get-CaseHoldPolicy<hold GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="b4f5f-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  \`Get-CaseHoldPolicy <hold GUID without prefix></span></span> | <span data-ttu-id="b4f5f-167">Nome de FL` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/> `$CaseHold.CaseId Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="b4f5f-167">FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId</span></span> | <span data-ttu-id="b4f5f-168">Nome de FL'</span><span class="sxs-lookup"><span data-stu-id="b4f5f-168">FL Name\`</span></span><br/><br/><br/> <span data-ttu-id="b4f5f-p112">**Observação:** Não recomendamos usando a descoberta eletrônica contém de caixas de correio inativas. Isso ocorre porque os casos de eDiscovery servem para casos específicos e de ligação de tempo relacionados a uma questão legal. Em algum momento, um caso jurídico provavelmente será finalizado e os bloqueios associados à ocorrência serão removidos e o caso de descoberta eletrônica estará fechado (ou excluídos). Na verdade, se uma isenção que é colocada em uma caixa de correio inativa é associada a um caso de eDiscovery e a suspensão seja removida ou o caso de descoberta eletrônica é fechado ou excluído, a caixa de correio inativa será excluída permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="b4f5f-173">Para obter mais informações sobre as políticas de retenção do Office 365, consulte [Visão geral das políticas de retenção](retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-173">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="b4f5f-174">Etapa 2: Alterar a duração de espera para uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="b4f5f-174">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="b4f5f-175">Depois de identificar que tipo de espera é colocado na caixa de correio inativa (e se há vários bloqueios), a próxima etapa é para alterar a duração da espera.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-175">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="b4f5f-176">Alterar a duração de um litígio</span><span class="sxs-lookup"><span data-stu-id="b4f5f-176">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="b4f5f-p113">Aqui está como usar o PowerShell do Exchange Online para alterar a duração de espera para um litígio que é colocada em uma caixa de correio inativa. Você não pode usar o EAC. Execute o seguinte comando para alterar a duração de espera. Neste exemplo, a duração da retenção é alterada para um período ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="b4f5f-181">O resultado é que os itens na caixa de correio inativa são mantidos indefinidamente ou até que a suspensão seja removida ou a duração da retenção é alterada para um valor diferente.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-181">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="b4f5f-p114">A melhor maneira de identificar uma caixa de correio inativa é usando seu valor de **Nome distinto** ou o **GUID do Exchange** . Usar um desses valores ajuda a evitar a acidentalmente especificando a caixa de correio errada.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="b4f5f-184">Alterar a duração de um bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="b4f5f-184">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="b4f5f-185">Você pode usar o EAC ou o PowerShell do Exchange Online para alterar a duração de espera de um bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-185">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="b4f5f-186">Usar o EAC para alterar a duração de espera</span><span class="sxs-lookup"><span data-stu-id="b4f5f-186">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="b4f5f-p115">Se você souber o nome do bloqueio In-loco que você deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa. Use o GUID bloqueio In-loco que você obteve na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="b4f5f-190">No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-190">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="b4f5f-191">Selecione o bloqueio In-loco você deseja alterar e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-191">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="b4f5f-192">Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades página, clique em **Bloqueio In-loco**.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-192">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="b4f5f-193">Um dos seguintes com base no atual duração da retenção:</span><span class="sxs-lookup"><span data-stu-id="b4f5f-193">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="b4f5f-194">Clique em **espera indefinidamente** para reter itens por um período ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-194">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="b4f5f-p116">Clique em **especificar o número de dias para reter itens em relação à sua data de recebimento** para reter itens por um período específico. Digite o número de dias em que você deseja reter itens para.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![Captura de tela da alteração da duração de um Bloqueio In-loco](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="b4f5f-198">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-198">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="b4f5f-199">Use o PowerShell do Exchange Online para alterar a duração de espera</span><span class="sxs-lookup"><span data-stu-id="b4f5f-199">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="b4f5f-p117">Se você souber o nome do bloqueio In-loco que você deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa. Use o GUID bloqueio In-loco que você obteve na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="b4f5f-p118">Execute o seguinte comando para alterar a duração de espera. Neste exemplo, a duração da retenção é alterada para 2,555 dias (aproximadamente sete anos).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="b4f5f-205">Para alterar a duração de espera para um período ilimitado de tempo, use _- ItemHoldPeriod ilimitado_.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-205">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="b4f5f-206">Mais informações</span><span class="sxs-lookup"><span data-stu-id="b4f5f-206">More information</span></span>

- <span data-ttu-id="b4f5f-p119">**Como a duração da retenção é calculada para um item em uma caixa de correio inativa?** A duração é calculada a partir da data original de um item de caixa de correio foi recebido ou criado.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="b4f5f-p120">**o que acontece quando a duração da retenção expira?** Quando a duração da retenção expira para um item de caixa de correio na pasta itens recuperáveis, o item é excluído permanentemente (descartados) da caixa de correio inativa. Se não houver nenhuma duração especificada para o bloqueio colocado na caixa de correio inativa, itens na pasta itens recuperáveis nunca são limpos (a menos que a duração de espera para a caixa de correio inativa mudou).</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="b4f5f-p121">**é uma política de retenção do Exchange ainda processada em caixas de correio inativas?** Se uma política de retenção do Exchange (os registros de mensagens gerenciamento ou MRM, recurso no Exchange Online) foi aplicada a uma caixa de correio quando ela foi feita inativa, as políticas de exclusão (que são configuradas com uma ação de retenção **Excluir** as marcas de retenção) será Continue a serem processados na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão são movidos para a pasta itens recuperáveis quando o período de retenção expira. Os itens são limpos, em seguida, da caixa de correio inativa quando a duração de espera para um item expira.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="b4f5f-p122">Por outro lado, quaisquer políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa serão ignoradas. Isso significa que os itens em uma caixa de correio inativa que estão marcados com uma política de arquivamento permanecem na caixa de correio principal quando o período de retenção expira. Elas não serão movidas para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Porque um usuário não pode entrar em uma caixa de correio inativa, não há nenhum motivo para consumir recursos do datacenter para processar as diretivas de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="b4f5f-p123">**Para verificar se a nova duração da retenção, execute um dos seguintes comandos.** O primeiro comando destina litígio; o segundo é para bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="b4f5f-p124">**Como caixas de correio regulares, a Managed pasta Assistant (MFA) também processa caixas de correio inativas.** No Exchange Online, o MFA processa caixas de correio aproximadamente uma vez a cada 7 dias. Depois de alterar a duração de espera para uma caixa de correio inativa, você pode usar o cmdlet **Start-ManagedFolderAssistant** para iniciar imediatamente o processamento a nova duração de espera para a caixa de correio inativa. Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="b4f5f-p125">**Se muita isenções são colocados em uma caixa de correio inativa, nem todos da isenção GUIDs serão exibidos.** Você pode executar o seguinte comando para exibir os GUIDs de todas as isenções (exceto litígio retém) que são colocadas em uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="b4f5f-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
