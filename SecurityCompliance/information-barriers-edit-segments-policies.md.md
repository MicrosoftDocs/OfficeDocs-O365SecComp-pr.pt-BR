---
title: Editar ou remover políticas de barreira de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Saiba como editar ou remover políticas para barreiras de informação.
ms.openlocfilehash: e6bed4df2329d426f86bd4cde07bdc7d1a2792cd
ms.sourcegitcommit: 7c48ce016fa9f45a3813467f7c5a2fd72f9b8f49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35215644"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="176dc-103">Editar ou remover políticas de barreira de informações (visualização)</span><span class="sxs-lookup"><span data-stu-id="176dc-103">Edit or remove information barrier policies (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="176dc-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="176dc-104">Overview</span></span>

<span data-ttu-id="176dc-105">Depois de [definir as políticas de barreira de informações](information-barriers-policies.md), talvez seja necessário fazer alterações nas políticas ou nos segmentos de usuário, como parte da [solução de problemas](information-barriers-troubleshooting.md) ou de manutenção regular.</span><span class="sxs-lookup"><span data-stu-id="176dc-105">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="176dc-106">Use este artigo como uma guia.</span><span class="sxs-lookup"><span data-stu-id="176dc-106">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="176dc-107">Para executar as tarefas descritas neste artigo, você deve receber uma função apropriada, como uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="176dc-107">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="176dc-108">– Administrador global do Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="176dc-108">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="176dc-109">– Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="176dc-109">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="176dc-110">-Administrador de conformidade</span><span class="sxs-lookup"><span data-stu-id="176dc-110">- Compliance Administrator</span></span><br/><span data-ttu-id="176dc-111">– Gerenciamento de conformidade do IB (esta é uma nova função!)</span><span class="sxs-lookup"><span data-stu-id="176dc-111">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="176dc-112">Para saber mais sobre os pré-requisitos para barreiras de informações, consulte [pré-requisitos (para políticas de barreira de informações)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="176dc-112">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="176dc-113">Certifique-se de [se conectar ao PowerShell do centro de conformidade & segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="176dc-113">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="176dc-114">Editar atributos da conta de usuário</span><span class="sxs-lookup"><span data-stu-id="176dc-114">Edit user account attributes</span></span>

<span data-ttu-id="176dc-115">Use este procedimento para editar atributos que são usados para segmentar usuários.</span><span class="sxs-lookup"><span data-stu-id="176dc-115">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="176dc-116">Por exemplo, se você estiver usando um atributo Department e uma ou mais contas de usuário não tiver atualmente nenhum valor listado para departamento, você deverá editar essas contas de usuário para incluir informações de departamento.</span><span class="sxs-lookup"><span data-stu-id="176dc-116">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="176dc-117">Os atributos da conta de usuário são usados para definir os segmentos de modo que as políticas de barreira de informações possam ser atribuídas.</span><span class="sxs-lookup"><span data-stu-id="176dc-117">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="176dc-118">Para exibir detalhes de uma conta de usuário específica, como valores de atributo e segmentos atribuídos, use o cmdlet **Get-InformationBarrierRecipientStatus** com parâmetros de identidade.</span><span class="sxs-lookup"><span data-stu-id="176dc-118">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

   <span data-ttu-id="176dc-119">Possuem`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="176dc-119">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 
    
   <span data-ttu-id="176dc-120">Você pode usar qualquer valor que identifique exclusivamente cada usuário, como nome, alias, nome diferenciado, nome de domínio canônico, endereço de email ou GUID.</span><span class="sxs-lookup"><span data-stu-id="176dc-120">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 
    
   <span data-ttu-id="176dc-121">Exemplo: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="176dc-121">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 
    
   <span data-ttu-id="176dc-122">Neste exemplo, nos referimos a duas contas de usuário no Office 365: *meganb* para *Megan*e *alexw* para *Alex*.</span><span class="sxs-lookup"><span data-stu-id="176dc-122">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
   <span data-ttu-id="176dc-123">(Você também pode usar esse cmdlet para um único usuário: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="176dc-123">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> 
    
2. <span data-ttu-id="176dc-124">Determine o atributo que você deseja editar para o (s) perfil (es) da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="176dc-124">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="176dc-125">Consulte [atributos para diretivas de barreira de informações (visualização)](information-barriers-attributes.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="176dc-125">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="176dc-126">Edite uma ou mais contas de usuário para incluir valores para o atributo selecionado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="176dc-126">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="176dc-127">Para fazer isso, use um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="176dc-127">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="176dc-128">Para editar uma única conta, confira [Adicionar ou atualizar as informações de perfil de um usuário usando o Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="176dc-128">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="176dc-129">Para editar várias contas (ou usar o PowerShell para editar uma única conta), confira [Configurar Propriedades da conta de usuário com o Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="176dc-129">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="176dc-130">Editar um segmento</span><span class="sxs-lookup"><span data-stu-id="176dc-130">Edit a segment</span></span>

<span data-ttu-id="176dc-131">Use este procedimento para editar a definição de um segmento de usuário.</span><span class="sxs-lookup"><span data-stu-id="176dc-131">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="176dc-132">Por exemplo, você pode alterar o nome de um segmento ou o filtro que é usado para determinar quem está incluído no segmento.</span><span class="sxs-lookup"><span data-stu-id="176dc-132">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="176dc-133">Para exibir todos os segmentos existentes, use o cmdlet **Get-OrganizationSegment** .</span><span class="sxs-lookup"><span data-stu-id="176dc-133">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="176dc-134">Possuem`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="176dc-134">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="176dc-135">Você verá uma lista de segmentos e detalhes para cada um, como tipo de segmento, seu valor UserGroupFilter, que o criou ou modificou pela última vez, GUID e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="176dc-135">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="176dc-136">Imprima ou salve sua lista de segmentos para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="176dc-136">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="176dc-137">Por exemplo, se quiser editar um segmento, você precisará saber seu nome ou identificar o valor (usado com o parâmetro Identity).</span><span class="sxs-lookup"><span data-stu-id="176dc-137">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="176dc-138">Para editar um segmento, use o cmdlet **set-OrganizationSegment** com o parâmetro **Identity** e detalhes relevantes.</span><span class="sxs-lookup"><span data-stu-id="176dc-138">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="176dc-139">Possuem`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="176dc-139">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="176dc-140">Exemplo: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="176dc-140">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="176dc-141">Neste exemplo, para o segmento que tem o GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, atualizamos o nome do departamento para "HRDept".</span><span class="sxs-lookup"><span data-stu-id="176dc-141">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="176dc-142">Ao concluir a edição dos segmentos da sua organização, você pode [definir](information-barriers-policies.md#part-2-define-information-barrier-policies) ou [Editar](#edit-a-policy) as políticas de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="176dc-142">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="176dc-143">Editar uma política</span><span class="sxs-lookup"><span data-stu-id="176dc-143">Edit a policy</span></span>

1. <span data-ttu-id="176dc-144">Para exibir uma lista de políticas de barreira de informações atuais, use o cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="176dc-144">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="176dc-145">Possuem`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="176dc-145">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="176dc-146">Na lista de resultados, identifique a política que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="176dc-146">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="176dc-147">Observe o GUID e o nome da política.</span><span class="sxs-lookup"><span data-stu-id="176dc-147">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="176dc-148">Use o cmdlet **set-InformationBarrierPolicy** com um parâmetro **Identity** e especifique as alterações que deseja fazer.</span><span class="sxs-lookup"><span data-stu-id="176dc-148">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="176dc-149">Exemplo: Suponha que uma política foi definida para bloquear o segmento de *pesquisa* de se comunicar com os segmentos *vendas* e *marketing* .</span><span class="sxs-lookup"><span data-stu-id="176dc-149">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="176dc-150">A política foi definida usando este cmdlet:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="176dc-150">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="176dc-151">Suponha que queremos alterá-lo para que as pessoas no segmento de *pesquisa* só possam se comunicar com pessoas no segmento de *RH* .</span><span class="sxs-lookup"><span data-stu-id="176dc-151">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="176dc-152">Para fazer essa alteração, usamos este cmdlet:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="176dc-152">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="176dc-153">Neste exemplo, alteramos "SegmentsBlocked" para "SegmentsAllowed" e especificamos o segmento *HR* .</span><span class="sxs-lookup"><span data-stu-id="176dc-153">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="176dc-154">Quando terminar de editar uma política, certifique-se de aplicar as alterações.</span><span class="sxs-lookup"><span data-stu-id="176dc-154">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="176dc-155">(Consulte [aplicar políticas de barreira de informações](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span><span class="sxs-lookup"><span data-stu-id="176dc-155">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="176dc-156">Definir uma política para o status inativo</span><span class="sxs-lookup"><span data-stu-id="176dc-156">Set a policy to inactive status</span></span>

1. <span data-ttu-id="176dc-157">Para exibir uma lista de políticas de barreira de informações atuais, use o cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="176dc-157">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="176dc-158">Possuem`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="176dc-158">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="176dc-159">Na lista de resultados, identifique a política que você deseja alterar (ou remover).</span><span class="sxs-lookup"><span data-stu-id="176dc-159">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="176dc-160">Observe o GUID e o nome da política.</span><span class="sxs-lookup"><span data-stu-id="176dc-160">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="176dc-161">Para definir o status da política como inativo, use o cmdlet **set-InformationBarrierPolicy** com um parâmetro Identity e o parâmetro State definido como inativo.</span><span class="sxs-lookup"><span data-stu-id="176dc-161">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="176dc-162">Possuem`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="176dc-162">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="176dc-163">Neste exemplo, definimos uma política de barreira de informações que tem o GUID *43c37853-ea10-4b90-a23d-ab8c9377247* para um status inativo.</span><span class="sxs-lookup"><span data-stu-id="176dc-163">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="176dc-164">Para aplicar suas alterações, use o cmdlet **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="176dc-164">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="176dc-165">Possuem`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="176dc-165">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="176dc-166">As alterações são aplicadas, usuário por usuário, para sua organização.</span><span class="sxs-lookup"><span data-stu-id="176dc-166">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="176dc-167">Se sua organização for grande, pode levar 24 horas (ou mais) para que esse processo seja concluído.</span><span class="sxs-lookup"><span data-stu-id="176dc-167">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="176dc-168">(Como uma diretriz geral, leva cerca de uma hora para processar as contas de usuário 5.000.)</span><span class="sxs-lookup"><span data-stu-id="176dc-168">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="176dc-169">Neste ponto, uma ou mais políticas de barreira de informações estão definidas para o status inativo.</span><span class="sxs-lookup"><span data-stu-id="176dc-169">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="176dc-170">A partir daqui, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="176dc-170">From here, you can do any of the following:</span></span>
- <span data-ttu-id="176dc-171">Mantê-lo como está (uma política definida como status inativo não tem efeito sobre os usuários)</span><span class="sxs-lookup"><span data-stu-id="176dc-171">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="176dc-172">Editar uma política</span><span class="sxs-lookup"><span data-stu-id="176dc-172">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="176dc-173">Remover uma política</span><span class="sxs-lookup"><span data-stu-id="176dc-173">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="176dc-174">Remover uma política</span><span class="sxs-lookup"><span data-stu-id="176dc-174">Remove a policy</span></span>

1. <span data-ttu-id="176dc-175">Para exibir uma lista de políticas de barreira de informações atuais, use o cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="176dc-175">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="176dc-176">Possuem`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="176dc-176">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="176dc-177">Na lista de resultados, identifique a política que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="176dc-177">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="176dc-178">Observe o GUID e o nome da política.</span><span class="sxs-lookup"><span data-stu-id="176dc-178">Note the policy's GUID and name.</span></span> <span data-ttu-id="176dc-179">Certifique-se de que a política está definida como status inativo.</span><span class="sxs-lookup"><span data-stu-id="176dc-179">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="176dc-180">Use o cmdlet **Remove-InformationBarrierPolicy** com um parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="176dc-180">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="176dc-181">Possuem`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="176dc-181">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="176dc-182">Exemplo: Suponha que queremos remover uma política com GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span><span class="sxs-lookup"><span data-stu-id="176dc-182">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="176dc-183">Para fazer isso, usamos este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="176dc-183">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="176dc-184">Quando solicitado, confirme a alteração.</span><span class="sxs-lookup"><span data-stu-id="176dc-184">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="176dc-185">Repita as etapas 1-2 para cada política que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="176dc-185">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="176dc-186">Quando terminar de remover as políticas, aplique as alterações.</span><span class="sxs-lookup"><span data-stu-id="176dc-186">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="176dc-187">Para fazer isso, use o cmdlet **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="176dc-187">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="176dc-188">Possuem`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="176dc-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="176dc-189">As alterações são aplicadas, usuário por usuário, para sua organização.</span><span class="sxs-lookup"><span data-stu-id="176dc-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="176dc-190">Se sua organização for grande, pode levar 24 horas (ou mais) para que esse processo seja concluído.</span><span class="sxs-lookup"><span data-stu-id="176dc-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="176dc-191">Parar um aplicativo de política</span><span class="sxs-lookup"><span data-stu-id="176dc-191">Stop a policy application</span></span>

<span data-ttu-id="176dc-192">Se, depois de começar a aplicar as políticas de barreira de informações, você quiser impedir que essas políticas sejam aplicadas, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="176dc-192">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="176dc-193">Tenha em mente que levará aproximadamente 30-35 minutos para que o processo seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="176dc-193">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="176dc-194">Para exibir o status do aplicativo de política de barreira de informações mais recente, use o cmdlet **Get-InformationBarrierPoliciesApplicationStatus** .</span><span class="sxs-lookup"><span data-stu-id="176dc-194">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="176dc-195">Possuem`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="176dc-195">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="176dc-196">Observe o GUID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="176dc-196">Note the application's GUID.</span></span>

2. <span data-ttu-id="176dc-197">Use o cmdlet **Stop-InformationBarrierPoliciesApplication** com um parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="176dc-197">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="176dc-198">Possuem`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="176dc-198">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="176dc-199">Exemplo: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="176dc-199">Example: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

    <span data-ttu-id="176dc-200">Neste exemplo, estamos interrompendo as políticas de barreira de informações de serem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="176dc-200">In this example, we are stopping information barrier policies from being applied.</span></span>

## <a name="related-articles"></a><span data-ttu-id="176dc-201">Artigos relacionados</span><span class="sxs-lookup"><span data-stu-id="176dc-201">Related articles</span></span>

[<span data-ttu-id="176dc-202">Obter uma visão geral das barreiras de informação</span><span class="sxs-lookup"><span data-stu-id="176dc-202">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="176dc-203">Definir políticas para barreiras de informação (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="176dc-203">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="176dc-204">Saiba mais sobre as barreiras de informação no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="176dc-204">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="176dc-205">Atributos para políticas de barreira de informações (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="176dc-205">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="176dc-206">Solucionando problemas de barreiras de informações (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="176dc-206">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
