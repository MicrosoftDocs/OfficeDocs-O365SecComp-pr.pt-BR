---
title: Alterar a duração da retenção para uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Depois que uma caixa de correio do Office 365 é desativada, você pode alterar a duração da política de retenção de bloqueio ou do Office 365 atribuída à caixa de correio inativa. A duração da retenção define por quanto tempo os itens da pasta itens recuperáveis são mantidos.
ms.openlocfilehash: f51750a0e822a4786f332639203b08ba4b5e2ba7
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295884"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="694b2-104">Alterar a duração da retenção para uma caixa de correio inativa no Office 365</span><span class="sxs-lookup"><span data-stu-id="694b2-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="694b2-p102">Uma caixa de correio inativa é usada para manter o email de um funcionário anterior, depois que ele deixa sua organização. Uma caixa de correio fica inativa quando uma retenção de litígio, um bloqueio in-loco, uma política de retenção do Office 365 ou uma retenção associada a uma ocorrência de descoberta eletrônica é colocada na caixa de correio e a conta de usuário do Office 365 correspondente é excluída. O conteúdo de uma caixa de correio inativa é mantido pela duração da retenção que foi colocada na caixa de correio antes de ser desativada. A duração da retenção define por quanto tempo os itens da pasta itens recuperáveis são mantidos. Quando a duração da retenção expira para um item na pasta itens recuperáveis, o item é excluído permanentemente (limpo) da caixa de correio inativa. Depois que uma caixa de correio for desativada, você poderá alterar a duração da política de retenção de espera ou do Office 365 atribuída à caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="694b2-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="694b2-p103">Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco.</span><span class="sxs-lookup"><span data-stu-id="694b2-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="694b2-116">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="694b2-116">Before you begin</span></span>

- <span data-ttu-id="694b2-p104">Você precisa usar o PowerShell do Exchange Online para alterar a duração da retenção para uma retenção de litígio em uma caixa de correio inativa. Você não pode usar o centro de administração do Exchange (Eat). Mas você pode usar o PowerShell do Exchange Online ou o Eat para alterar a duração da retenção de um bloqueio in-loco. Você pode usar o centro de conformidade &amp; de segurança do Office 365 &amp; ou o PowerShell do centro de conformidade de segurança para alterar a duração de retenção de uma política de retenção do Office 365.</span><span class="sxs-lookup"><span data-stu-id="694b2-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="694b2-121">Para se conectar ao PowerShell do Exchange Online &amp; ou do centro de conformidade de segurança, consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="694b2-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="694b2-122">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="694b2-122">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [<span data-ttu-id="694b2-123">Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="694b2-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="694b2-p105">Observe que as suspensões associadas às ocorrências de descoberta eletrônica são infinitas, o que significa que não há duração de retenção que pode ser alterada. Os itens são retidos para sempre ou até que a retenção seja removida e a caixa de correio inativa seja excluída.</span><span class="sxs-lookup"><span data-stu-id="694b2-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="694b2-126">Para obter mais informações sobre caixas de correio inativas, consulte [inativa caixas de correio no Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="694b2-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="694b2-127">Etapa 1: identificar as isenções em uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="694b2-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="694b2-128">Como diferentes tipos de isenções ou uma ou mais políticas de retenção do Office 365 podem ser colocadas em uma caixa de correio inativa, a primeira etapa é identificar as isenções em uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="694b2-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="694b2-129">Execute o seguinte comando no PowerShell do Exchange Online para exibir as informações de retenção de todas as caixas de correio inativas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="694b2-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="694b2-p106">O valor de **true** para a propriedade **LitigationHoldEnabled** indica que a caixa de correio inativa está em retenção de litígio. Se um bloqueio in-loco, um bloqueio de descoberta eletrônica ou uma política de retenção do Office 365 for colocado em uma caixa de correio inativa, um GUID para a política de retenção ou bloqueio será exibido como o valor da propriedade **InPlaceHolds** . Por exemplo, o seguinte mostra os resultados de cinco caixas de correio inativas.</span><span class="sxs-lookup"><span data-stu-id="694b2-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
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
   
<span data-ttu-id="694b2-133">A tabela a seguir identifica os cinco tipos de retenção diferentes que foram usados para tornar cada caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="694b2-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="694b2-134">**Caixa de correio inativa**</span><span class="sxs-lookup"><span data-stu-id="694b2-134">**Inactive mailbox**</span></span>|<span data-ttu-id="694b2-135">**Tipo de bloqueio**</span><span class="sxs-lookup"><span data-stu-id="694b2-135">**Hold type**</span></span>|<span data-ttu-id="694b2-136">**Como identificar a retenção na caixa de correio inativa**</span><span class="sxs-lookup"><span data-stu-id="694b2-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="694b2-137">Ana Beebe</span><span class="sxs-lookup"><span data-stu-id="694b2-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="694b2-138">Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="694b2-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="694b2-139">A propriedade *LitigationHoldEnabled* está definida como `True`.</span><span class="sxs-lookup"><span data-stu-id="694b2-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="694b2-140">Pilar Fernandes</span><span class="sxs-lookup"><span data-stu-id="694b2-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="694b2-141">Bloqueio In-loco</span><span class="sxs-lookup"><span data-stu-id="694b2-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="694b2-p107">A propriedade *InPlaceHolds* contém o GUID do bloqueio in-loco colocado na caixa de correio inativa. É possível dizer que isso é um bloqueio in-loco porque a ID não começa com um prefixo.</span><span class="sxs-lookup"><span data-stu-id="694b2-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="694b2-144">Você pode usar o `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` comando no PowerShell do Exchange Online para obter informações sobre o bloqueio in-loco na caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="694b2-144">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="694b2-145">Mario Necaise</span><span class="sxs-lookup"><span data-stu-id="694b2-145">Mario Necaise</span></span>  <br/> |<span data-ttu-id="694b2-146">Política de retenção do Office 365 em toda a organização &amp; no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="694b2-146">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="694b2-p108">A propriedade *InPlaceHolds* está vazia. Isso indica que uma ou mais políticas de retenção do Office 365 em toda a organização ou (no Exchange) são aplicadas à caixa de correio inativa. Nesse caso, você pode executar o `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` comando no PowerShell do Exchange Online para obter uma lista dos GUIDs das políticas de retenção do Office 365 em toda a organização. O GUID para políticas de retenção em toda a organização que são aplicadas às caixas de correio do `mbx` Exchange começam com o prefixo; por exemplo `mbxa3056bb15562480fadb46ce523ff7b02`.</span><span class="sxs-lookup"><span data-stu-id="694b2-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <br/><span data-ttu-id="694b2-151">Para identificar a política de retenção do Office 365 aplicada à caixa de correio inativa, execute o seguinte comando no &amp; PowerShell do centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="694b2-151">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span>  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|<span data-ttu-id="694b2-152">Carol Olson</span><span class="sxs-lookup"><span data-stu-id="694b2-152">Carol Olson</span></span>  <br/> |<span data-ttu-id="694b2-153">Política de retenção do Office 365 no &amp; centro de conformidade de segurança aplicada a caixas de correio específicas</span><span class="sxs-lookup"><span data-stu-id="694b2-153">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="694b2-p109">A propriedade *InPlaceHolds* contém o GUID da política de retenção do Office 365 que é aplicada à caixa de correio inativa. Você pode dizer que esta é uma política de retenção que se aplica a caixas de correio específicas porque o `mbx` GUID começa com o prefixo. Observe que, se o GUID da política de retenção aplicado à caixa de correio inativa `skp` começou com o prefixo, isso indicaria que a política de retenção é aplicada às conversas do Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="694b2-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="694b2-157">Para identificar a política de retenção do Office 365 aplicada à caixa de correio inativa, execute o seguinte comando no &amp; PowerShell do centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="694b2-157">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/><span data-ttu-id="694b2-158">Certifique-se de remover `mbx` o `skp` prefixo ou ao executar este comando.</span><span class="sxs-lookup"><span data-stu-id="694b2-158">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="694b2-159">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="694b2-159">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="694b2-160">retenção de caso de descoberta eletrônica &amp; no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="694b2-160">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="694b2-p110">A propriedade *InPlaceHolds* contém o GUID da retenção de ocorrência de descoberta eletrônica que é colocada na caixa de correio inativa. É possível dizer que esta é uma retenção de caso de descoberta eletrônica porque o `UniH` GUID começa com o prefixo.</span><span class="sxs-lookup"><span data-stu-id="694b2-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="694b2-p111">Você pode usar o `Get-CaseHoldPolicy` cmdlet no PowerShell &amp; do centro de conformidade de segurança para obter informações sobre a ocorrência de descoberta eletrônica à qual a retenção está associada à caixa de correio inativa. Por exemplo, você pode executar o comando `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` para exibir o nome da retenção de caso que está na caixa de correio inativa. Certifique-se de remover `UniH` o prefixo ao executar este comando.</span><span class="sxs-lookup"><span data-stu-id="694b2-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="694b2-166">Para identificar a ocorrência de descoberta eletrônica à qual a retenção está associada à caixa de correio inativa, execute os seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="694b2-166">To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.</span></span>  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> <span data-ttu-id="694b2-p112">**Observação:** Não recomendamos o uso de bloqueios de descoberta eletrônica para caixas de correio inativas. Isso ocorre porque os casos de descoberta eletrônica se destinam a casos específicos e associados a tempo relacionados a um problema legal. Em algum momento, um caso jurídico provavelmente será encerrado e as suspensões associadas ao caso serão removidas e o caso de descoberta eletrônica será fechado (ou excluído). Na verdade, se uma retenção colocada em uma caixa de correio inativa estiver associada a uma ocorrência de descoberta eletrônica e a retenção for liberada ou se a ocorrência de descoberta eletrônica estiver fechada ou excluída, a caixa de correio inativa será excluída permanentemente.</span><span class="sxs-lookup"><span data-stu-id="694b2-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="694b2-171">Para obter mais informações sobre as políticas de retenção do Office 365, consulte [visão geral das políticas de retenção](retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="694b2-171">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="694b2-172">Etapa 2: alterar a duração da retenção de uma caixa de correio inativa</span><span class="sxs-lookup"><span data-stu-id="694b2-172">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="694b2-173">Depois de identificar o tipo de retenção que é colocado na caixa de correio inativa (e se há várias isenções), a próxima etapa é alterar a duração da retenção.</span><span class="sxs-lookup"><span data-stu-id="694b2-173">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="694b2-174">Alterar a duração de uma retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="694b2-174">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="694b2-p113">ConFira aqui como usar o PowerShell do Exchange Online para alterar a duração da retenção para uma retenção de litígio que é colocada em uma caixa de correio inativa. Você não pode usar o Eat. Execute o seguinte comando para alterar a duração da retenção. Neste exemplo, a duração da retenção é alterada para um período de tempo ilimitado.</span><span class="sxs-lookup"><span data-stu-id="694b2-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="694b2-179">O resultado é que os itens da caixa de correio inativa são mantidos indefinidamente ou até que a retenção seja removida ou a duração da retenção seja alterada para um valor diferente.</span><span class="sxs-lookup"><span data-stu-id="694b2-179">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="694b2-p114">A melhor maneira de identificar uma caixa de correio inativa é usando seu **nome distinto** ou valor de **GUID do Exchange** . O uso de um desses valores ajuda a evitar a especificação acidental da caixa de correio errada.</span><span class="sxs-lookup"><span data-stu-id="694b2-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="694b2-182">Alterar a duração de um bloqueio in-loco</span><span class="sxs-lookup"><span data-stu-id="694b2-182">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="694b2-183">Você pode usar o Eat ou o PowerShell do Exchange Online para alterar a duração da retenção para um bloqueio in-loco.</span><span class="sxs-lookup"><span data-stu-id="694b2-183">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="694b2-184">Usar o Eat para alterar a duração da retenção</span><span class="sxs-lookup"><span data-stu-id="694b2-184">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="694b2-p115">Se você souber o nome do bloqueio in-loco que deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome do bloqueio in-loco que é colocado na caixa de correio inativa. Use o GUID de bloqueio in-loco obtido na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="694b2-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="694b2-188">No Eat, vá para **Gerenciamento** \> **de conformidade e descoberta eletrônica &amp; in-loco**.</span><span class="sxs-lookup"><span data-stu-id="694b2-188">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="694b2-189">Selecione o bloqueio in-loco que você deseja alterar e clique em **Editar** ![ícone](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)de edição.</span><span class="sxs-lookup"><span data-stu-id="694b2-189">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="694b2-190">Na página Propriedades **de retenção de &amp; descoberta eletrônica in-loco** , clique **em bloqueio in-loco**.</span><span class="sxs-lookup"><span data-stu-id="694b2-190">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="694b2-191">Siga um destes procedimentos com base na duração atual da retenção:</span><span class="sxs-lookup"><span data-stu-id="694b2-191">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="694b2-192">Clique em **reter** indefinidamente para reter itens por um período de tempo ilimitado.</span><span class="sxs-lookup"><span data-stu-id="694b2-192">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="694b2-p116">Clique em **especificar número de dias para manter os itens em relação à data de recebimento** para reter itens por um período específico. Digite o número de dias para os quais você deseja armazenar itens.</span><span class="sxs-lookup"><span data-stu-id="694b2-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![Captura de tela da alteração da duração de um Bloqueio In-loco](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="694b2-196">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="694b2-196">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="694b2-197">Usar o PowerShell do Exchange Online para alterar a duração da retenção</span><span class="sxs-lookup"><span data-stu-id="694b2-197">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="694b2-p117">Se você souber o nome do bloqueio in-loco que deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome do bloqueio in-loco que é colocado na caixa de correio inativa. Use o GUID de bloqueio in-loco obtido na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="694b2-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="694b2-p118">Execute o seguinte comando para alterar a duração da retenção. Neste exemplo, a duração da retenção é alterada para 2.555 dias (aproximadamente sete anos).</span><span class="sxs-lookup"><span data-stu-id="694b2-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="694b2-203">Para alterar a duração da retenção para um período de tempo ilimitado, use _-ItemHoldPeriod_Unlimited.</span><span class="sxs-lookup"><span data-stu-id="694b2-203">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="694b2-204">Mais informações</span><span class="sxs-lookup"><span data-stu-id="694b2-204">More information</span></span>

- <span data-ttu-id="694b2-p119">**Como a duração da retenção é calculada para um item em uma caixa de correio inativa?** A duração é calculada a partir da data original em que um item de caixa de correio foi recebido ou criado.</span><span class="sxs-lookup"><span data-stu-id="694b2-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="694b2-p120">**O que acontece quando a duração da retenção expira?** Quando a duração da retenção expira para um item de caixa de correio na pasta itens recuperáveis, o item é excluído permanentemente (limpo) da caixa de correio inativa. Se não houver nenhuma duração especificada para a retenção colocada na caixa de correio inativa, os itens na pasta itens recuperáveis nunca serão removidos (a menos que a duração da retenção de caixa de correio inativa seja alterada).</span><span class="sxs-lookup"><span data-stu-id="694b2-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="694b2-p121">**Uma política de retenção do Exchange ainda é processada em caixas de correio inativas?** Se uma política de retenção do Exchange (o recurso gerenciamento de registros de mensagens ou MRM, no Exchange Online) tiver sido aplicada a uma caixa de correio quando for desativada, as políticas de exclusão (que são marcas de retenção configuradas com uma ação de retenção de **exclusão** ) serão continuar a ser processado na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão são movidos para a pasta itens recuperáveis quando o período de retenção expira. Esses itens são, então, removidos da caixa de correio inativa quando a duração da retenção de um item expira.</span><span class="sxs-lookup"><span data-stu-id="694b2-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="694b2-p122">Por outro lado, todas as políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção do **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa são ignoradas. Isso significa que os itens em uma caixa de correio inativa que estão marcados com uma política de arquivo morto permanecem na caixa de correio principal quando o período de retenção expira. Eles não são movidos para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Como um usuário não pode entrar em uma caixa de correio inativa, não há motivo para consumir recursos de datacenter para processar políticas de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="694b2-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="694b2-p123">**Para verificar a duração da nova retenção, execute um dos seguintes comandos.** O primeiro comando é para retenção de litígio; o segundo é para bloqueio in-loco.</span><span class="sxs-lookup"><span data-stu-id="694b2-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="694b2-p124">**Assim como as caixas de correio normais, o assistente de pasta gerenciada (MFA) também processa caixas de correio inativas.** No Exchange Online, a MFA processa as caixas de correio aproximadamente uma vez a cada 7 dias. Após alterar a duração da retenção para uma caixa de correio inativa, você pode usar o cmdlet **Start-ManagedFolderAssistant** para iniciar imediatamente o processamento da nova duração de retenção para a caixa de correio inativa. Execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="694b2-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="694b2-p125">**Se uma grande quantidade de isenções for colocada em uma caixa de correio inativa, nem todos os GUIDs de retenção serão exibidos.** Você pode executar o comando a seguir para exibir os GUIDs de todas as isenções (exceto as isenções de litígio) que são colocadas em uma caixa de correio inativa.</span><span class="sxs-lookup"><span data-stu-id="694b2-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
