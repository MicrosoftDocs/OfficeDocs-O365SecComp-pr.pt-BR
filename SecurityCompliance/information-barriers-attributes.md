---
title: Atributos para políticas de barreira de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use este artigo como referência para vários atributos que podem ser usados em políticas de barreira de informações.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668272"
---
# <a name="attributes-for-information-barrier-policies-preview"></a><span data-ttu-id="c2488-103">Atributos para políticas de barreira de informações (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="c2488-103">Attributes for information barrier policies (Preview)</span></span>

<span data-ttu-id="c2488-104">Determinados atributos no Azure Active Directory podem ser usados para segmentar usuários.</span><span class="sxs-lookup"><span data-stu-id="c2488-104">Certain attributes in Azure Active Directory can be used to segment users.</span></span> <span data-ttu-id="c2488-105">Os segmentos são então usados como filtros para políticas de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="c2488-105">Segments are then used as filters for information barrier policies.</span></span> <span data-ttu-id="c2488-106">Por exemplo, você pode usar o **Departamento** para definir segmentos de usuários por departamento em sua organização (supondo que nenhum único funcionário funcione para dois departamentos ao mesmo tempo).</span><span class="sxs-lookup"><span data-stu-id="c2488-106">For example, you might use **Department** to define segments of users by department within your organization (assuming no single employee works for two departments at the same time).</span></span> 

<span data-ttu-id="c2488-107">Este artigo fornece uma lista de atributos que podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="c2488-107">This article provides a list of attributes that can be used.</span></span> <span data-ttu-id="c2488-108">Para saber mais sobre as barreiras de informação, confira os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="c2488-108">To learn more about information barriers, see the following resources:</span></span>
- [<span data-ttu-id="c2488-109">Barreiras de informação (visualização)</span><span class="sxs-lookup"><span data-stu-id="c2488-109">Information barriers (Preview)</span></span>](information-barriers.md)
- [<span data-ttu-id="c2488-110">Definir políticas para barreiras de informações no Microsoft Teams (visualização)</span><span class="sxs-lookup"><span data-stu-id="c2488-110">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a><span data-ttu-id="c2488-111">Como usar atributos em políticas de barreira de informações</span><span class="sxs-lookup"><span data-stu-id="c2488-111">How to use attributes in information barrier policies</span></span>

<span data-ttu-id="c2488-112">Os atributos listados neste artigo podem ser usados para definir (ou editar) segmentos de usuários.</span><span class="sxs-lookup"><span data-stu-id="c2488-112">The attributes listed in this article can be used to define (or edit) segments of users.</span></span> <span data-ttu-id="c2488-113">Os segmentos são usados como parâmetros (UserGroupFilter) em políticas de barreira de informações, conforme mostrado nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="c2488-113">Segments are used as parameters (UserGroupFilter) in information barrier policies, as shown in the following examples:</span></span>

|<span data-ttu-id="c2488-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c2488-114">Example</span></span>  |<span data-ttu-id="c2488-115">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2488-115">Cmdlet</span></span>  |
|---------|---------|
|<span data-ttu-id="c2488-116">Definir um segmento chamado Segment1 usando o atributo Department</span><span class="sxs-lookup"><span data-stu-id="c2488-116">Define a segment called Segment1 using the Department attribute</span></span>     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|<span data-ttu-id="c2488-117">Defina um segmento chamado segmenta usando o atributo MemberOf (Suponha que este atributo contenha nomes de grupo, como "Blueus")</span><span class="sxs-lookup"><span data-stu-id="c2488-117">Define a segment called SegmentA using the MemberOf attribute (suppose this attribute contains group names, such as "BlueGroup")</span></span>     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|<span data-ttu-id="c2488-118">Defina um segmento chamado DayTraders usando ExtensionAttribute1 (Suponha que este atributo contenha cargos, como "DayTrader")</span><span class="sxs-lookup"><span data-stu-id="c2488-118">Define a segment called DayTraders using ExtensionAttribute1 (suppose this attribute contains job titles, such as "DayTrader")</span></span>|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

<span data-ttu-id="c2488-119">Ao definir segmentos, use o mesmo atributo para todos os seus segmentos.</span><span class="sxs-lookup"><span data-stu-id="c2488-119">When you define segments, use the same attribute for all your segments.</span></span> <span data-ttu-id="c2488-120">Por exemplo, se você definir alguns segmentos usando *Departamento*, defina todos os segmentos usando *Departamento*.</span><span class="sxs-lookup"><span data-stu-id="c2488-120">For example, if you define some segments using *Department*, define all of the segments using *Department*.</span></span> <span data-ttu-id="c2488-121">Não defina alguns segmentos usando o *Departamento* e outros usando *memberOf*.</span><span class="sxs-lookup"><span data-stu-id="c2488-121">Don't define some segments using *Department* and others using *MemberOf*.</span></span> <span data-ttu-id="c2488-122">Certifique-se de que seus segmentos não se sobreponham; cada usuário deve ser atribuído a exatamente um segmento.</span><span class="sxs-lookup"><span data-stu-id="c2488-122">Make sure your segments do not overlap; each user should be assigned to exactly one segment.</span></span> 

<span data-ttu-id="c2488-123">Para saber mais, confira [definir segmentos usando o PowerShell](information-barriers-policies.md#define-segments-using-powershell).</span><span class="sxs-lookup"><span data-stu-id="c2488-123">To learn more, see [Define segments using PowerShell](information-barriers-policies.md#define-segments-using-powershell).</span></span>

## <a name="reference"></a><span data-ttu-id="c2488-124">Referência</span><span class="sxs-lookup"><span data-stu-id="c2488-124">Reference</span></span>

<span data-ttu-id="c2488-125">A tabela a seguir lista os atributos que você pode usar com as barreiras de informação.</span><span class="sxs-lookup"><span data-stu-id="c2488-125">The following table lists the attributes that you can use with information barriers.</span></span>

|<span data-ttu-id="c2488-126">Nome da Propriedade do Active Directory do Azure (nome para exibição LDAP)</span><span class="sxs-lookup"><span data-stu-id="c2488-126">Azure Active Directory property name (LDAP display name)</span></span>  |<span data-ttu-id="c2488-127">Nome da Propriedade do Exchange</span><span class="sxs-lookup"><span data-stu-id="c2488-127">Exchange property name</span></span>  |
|---------|---------|
|<span data-ttu-id="c2488-128">Coautores</span><span class="sxs-lookup"><span data-stu-id="c2488-128">Co</span></span>       | <span data-ttu-id="c2488-129">Coautores</span><span class="sxs-lookup"><span data-stu-id="c2488-129">Co</span></span>        |
|<span data-ttu-id="c2488-130">Empresa</span><span class="sxs-lookup"><span data-stu-id="c2488-130">Company</span></span>     |<span data-ttu-id="c2488-131">Empresa</span><span class="sxs-lookup"><span data-stu-id="c2488-131">Company</span></span>         |
|<span data-ttu-id="c2488-132">Departamento</span><span class="sxs-lookup"><span data-stu-id="c2488-132">Department</span></span>     |<span data-ttu-id="c2488-133">Departamento</span><span class="sxs-lookup"><span data-stu-id="c2488-133">Department</span></span>         |
|<span data-ttu-id="c2488-134">ExtensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="c2488-134">ExtensionAttribute1</span></span> |<span data-ttu-id="c2488-135">CustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="c2488-135">CustomAttribute1</span></span>  |
|<span data-ttu-id="c2488-136">ExtensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="c2488-136">ExtensionAttribute2</span></span> |<span data-ttu-id="c2488-137">CustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="c2488-137">CustomAttribute2</span></span>  |
|<span data-ttu-id="c2488-138">ExtensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="c2488-138">ExtensionAttribute3</span></span> |<span data-ttu-id="c2488-139">CustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="c2488-139">CustomAttribute3</span></span>  |
|<span data-ttu-id="c2488-140">ExtensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="c2488-140">ExtensionAttribute4</span></span> |<span data-ttu-id="c2488-141">CustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="c2488-141">CustomAttribute4</span></span>  |
|<span data-ttu-id="c2488-142">ExtensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="c2488-142">ExtensionAttribute5</span></span> |<span data-ttu-id="c2488-143">CustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="c2488-143">CustomAttribute5</span></span>  |
|<span data-ttu-id="c2488-144">ExtensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="c2488-144">ExtensionAttribute6</span></span> |<span data-ttu-id="c2488-145">CustomAttribute6</span><span class="sxs-lookup"><span data-stu-id="c2488-145">CustomAttribute6</span></span>  |
|<span data-ttu-id="c2488-146">ExtensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="c2488-146">ExtensionAttribute7</span></span> |<span data-ttu-id="c2488-147">CustomAttribute7</span><span class="sxs-lookup"><span data-stu-id="c2488-147">CustomAttribute7</span></span>  |
|<span data-ttu-id="c2488-148">ExtensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="c2488-148">ExtensionAttribute8</span></span> |<span data-ttu-id="c2488-149">CustomAttribute8</span><span class="sxs-lookup"><span data-stu-id="c2488-149">CustomAttribute8</span></span>  |
|<span data-ttu-id="c2488-150">ExtensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="c2488-150">ExtensionAttribute9</span></span> |<span data-ttu-id="c2488-151">CustomAttribute9</span><span class="sxs-lookup"><span data-stu-id="c2488-151">CustomAttribute9</span></span>  |
|<span data-ttu-id="c2488-152">ExtensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="c2488-152">ExtensionAttribute10</span></span> |<span data-ttu-id="c2488-153">CustomAttribute10</span><span class="sxs-lookup"><span data-stu-id="c2488-153">CustomAttribute10</span></span>  |
|<span data-ttu-id="c2488-154">ExtensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="c2488-154">ExtensionAttribute11</span></span> |<span data-ttu-id="c2488-155">CustomAttribute11</span><span class="sxs-lookup"><span data-stu-id="c2488-155">CustomAttribute11</span></span>  |
|<span data-ttu-id="c2488-156">ExtensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="c2488-156">ExtensionAttribute12</span></span> |<span data-ttu-id="c2488-157">CustomAttribute12</span><span class="sxs-lookup"><span data-stu-id="c2488-157">CustomAttribute12</span></span>  |
|<span data-ttu-id="c2488-158">ExtensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="c2488-158">ExtensionAttribute13</span></span> |<span data-ttu-id="c2488-159">CustomAttribute13</span><span class="sxs-lookup"><span data-stu-id="c2488-159">CustomAttribute13</span></span>  |
|<span data-ttu-id="c2488-160">ExtensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="c2488-160">ExtensionAttribute14</span></span> |<span data-ttu-id="c2488-161">CustomAttribute14</span><span class="sxs-lookup"><span data-stu-id="c2488-161">CustomAttribute14</span></span>  |
|<span data-ttu-id="c2488-162">ExtensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="c2488-162">ExtensionAttribute15</span></span> |<span data-ttu-id="c2488-163">CustomAttribute15</span><span class="sxs-lookup"><span data-stu-id="c2488-163">CustomAttribute15</span></span>  |
|<span data-ttu-id="c2488-164">MSExchExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="c2488-164">MSExchExtensionCustomAttribute1</span></span> |<span data-ttu-id="c2488-165">ExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="c2488-165">ExtensionCustomAttribute1</span></span> |
|<span data-ttu-id="c2488-166">MSExchExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="c2488-166">MSExchExtensionCustomAttribute2</span></span> |<span data-ttu-id="c2488-167">ExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="c2488-167">ExtensionCustomAttribute2</span></span> |
|<span data-ttu-id="c2488-168">MSExchExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="c2488-168">MSExchExtensionCustomAttribute3</span></span> |<span data-ttu-id="c2488-169">ExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="c2488-169">ExtensionCustomAttribute3</span></span> |
|<span data-ttu-id="c2488-170">MSExchExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="c2488-170">MSExchExtensionCustomAttribute4</span></span> |<span data-ttu-id="c2488-171">ExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="c2488-171">ExtensionCustomAttribute4</span></span> |
|<span data-ttu-id="c2488-172">MSExchExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="c2488-172">MSExchExtensionCustomAttribute5</span></span> |<span data-ttu-id="c2488-173">ExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="c2488-173">ExtensionCustomAttribute5</span></span> |
|<span data-ttu-id="c2488-174">MailNickname</span><span class="sxs-lookup"><span data-stu-id="c2488-174">MailNickname</span></span> |<span data-ttu-id="c2488-175">Alias</span><span class="sxs-lookup"><span data-stu-id="c2488-175">Alias</span></span> |
|<span data-ttu-id="c2488-176">PhysicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="c2488-176">PhysicalDeliveryOfficeName</span></span> |<span data-ttu-id="c2488-177">Office</span><span class="sxs-lookup"><span data-stu-id="c2488-177">Office</span></span> |
|<span data-ttu-id="c2488-178">PostalCode</span><span class="sxs-lookup"><span data-stu-id="c2488-178">PostalCode</span></span> |<span data-ttu-id="c2488-179">PostalCode</span><span class="sxs-lookup"><span data-stu-id="c2488-179">PostalCode</span></span> |
|<span data-ttu-id="c2488-180">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c2488-180">ProxyAddresses</span></span> |<span data-ttu-id="c2488-181">EndereçosEmail</span><span class="sxs-lookup"><span data-stu-id="c2488-181">EmailAddresses</span></span> |
|<span data-ttu-id="c2488-182">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="c2488-182">StreetAddress</span></span> |<span data-ttu-id="c2488-183">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="c2488-183">StreetAddress</span></span> |
|<span data-ttu-id="c2488-184">TargetAddress</span><span class="sxs-lookup"><span data-stu-id="c2488-184">TargetAddress</span></span> |<span data-ttu-id="c2488-185">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c2488-185">ExternalEmailAddress</span></span> |
|<span data-ttu-id="c2488-186">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="c2488-186">UsageLocation</span></span> |<span data-ttu-id="c2488-187">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="c2488-187">UsageLocation</span></span> |
|<span data-ttu-id="c2488-188">Principal</span><span class="sxs-lookup"><span data-stu-id="c2488-188">UserPrincipalName</span></span>  |<span data-ttu-id="c2488-189">Principal</span><span class="sxs-lookup"><span data-stu-id="c2488-189">UserPrincipalName</span></span>  |
|<span data-ttu-id="c2488-190">Correio</span><span class="sxs-lookup"><span data-stu-id="c2488-190">Mail</span></span>   |<span data-ttu-id="c2488-191">WindowsEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c2488-191">WindowsEmailAddress</span></span>    |
|<span data-ttu-id="c2488-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2488-192">Description</span></span>    |<span data-ttu-id="c2488-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2488-193">Description</span></span>    |
|<span data-ttu-id="c2488-194">Tattoo</span><span class="sxs-lookup"><span data-stu-id="c2488-194">MemberOf</span></span>   |<span data-ttu-id="c2488-195">MemberOfGroup</span><span class="sxs-lookup"><span data-stu-id="c2488-195">MemberOfGroup</span></span>  |

## <a name="related-topics"></a><span data-ttu-id="c2488-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2488-196">Related topics</span></span>

[<span data-ttu-id="c2488-197">Definir políticas para barreiras de informações no Microsoft Teams (visualização)</span><span class="sxs-lookup"><span data-stu-id="c2488-197">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="c2488-198">Solucionando problemas de barreiras de informações (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="c2488-198">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)

[<span data-ttu-id="c2488-199">Barreiras de informação (visualização)</span><span class="sxs-lookup"><span data-stu-id="c2488-199">Information barriers (Preview)</span></span>](information-barriers.md)



