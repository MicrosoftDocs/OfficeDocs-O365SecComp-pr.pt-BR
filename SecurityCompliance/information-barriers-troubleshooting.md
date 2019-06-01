---
title: Solucionando problemas de barreiras de informações
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
description: Use este artigo como um guia para solucionar problemas de barreiras de informações.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668269"
---
# <a name="troubleshooting-information-barriers-preview"></a><span data-ttu-id="ed189-103">Solucionando problemas de barreiras de informações (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="ed189-103">Troubleshooting information barriers (Preview)</span></span>

<span data-ttu-id="ed189-104">As barreiras de informação podem ajudar sua organização a permanecer em conformidade com requisitos legais e regulamentações do setor.</span><span class="sxs-lookup"><span data-stu-id="ed189-104">Information barriers can help your organization remain compliant with legal requirements and industry regulations.</span></span> <span data-ttu-id="ed189-105">Por exemplo, com barreiras de informações, você pode restringir a comunicação entre grupos específicos de usuários para evitar um conflito de interesses ou outros problemas.</span><span class="sxs-lookup"><span data-stu-id="ed189-105">For example, with information barriers, you can restrict communication between specific groups of users to avoid a conflict of interest or other issues.</span></span> <span data-ttu-id="ed189-106">Para saber mais, confira [barreiras de informação (versão prévia)](information-barriers.md).</span><span class="sxs-lookup"><span data-stu-id="ed189-106">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span>

<span data-ttu-id="ed189-107">Este artigo fornece orientações que podem ser usadas para obter respostas a perguntas ou resolver problemas que podem surgir com as barreiras de informação.</span><span class="sxs-lookup"><span data-stu-id="ed189-107">This article provides guidance you can use to get answers to questions or resolve issues that may arise with information barriers.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="ed189-108">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="ed189-108">Before you begin...</span></span>

<span data-ttu-id="ed189-109">Para executar as tarefas descritas neste artigo, você deve receber uma função apropriada, como uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="ed189-109">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span>
- <span data-ttu-id="ed189-110">Administrador global do Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ed189-110">Microsoft 365 Enterprise Global Administrator</span></span>
- <span data-ttu-id="ed189-111">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="ed189-111">Office 365 Global Administrator</span></span>
- <span data-ttu-id="ed189-112">Administrador de Conformidade</span><span class="sxs-lookup"><span data-stu-id="ed189-112">Compliance Administrator</span></span>
- <span data-ttu-id="ed189-113">Gerenciamento de conformidade IB (esta é uma nova função!)</span><span class="sxs-lookup"><span data-stu-id="ed189-113">IB Compliance Management (this is a new role!)</span></span>

<span data-ttu-id="ed189-114">Para saber mais sobre funções e permissões, consulte [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="ed189-114">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="ed189-115">Para saber mais sobre os pré-requisitos para barreiras de informações, consulte [pré-requisitos (para políticas de barreira de informações)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ed189-115">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span>

<span data-ttu-id="ed189-116">Além disso, certifique [-se de se conectar ao PowerShell do centro de conformidade & segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="ed189-116">Also, make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a><span data-ttu-id="ed189-117">Problema: as pessoas estão inesperadamente impedidas de se comunicar no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ed189-117">Issue: People are unexpectedly blocked from communicating in Microsoft Teams</span></span> 

<span data-ttu-id="ed189-118">Nesse caso, as pessoas estão relatando problemas inesperados ao se comunicar no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ed189-118">In this case, people are reporting unexpected issues communicating in Microsoft Teams.</span></span> <span data-ttu-id="ed189-119">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="ed189-119">Examples:</span></span>
- <span data-ttu-id="ed189-120">Um usuário não consegue encontrar ou se comunicar com outro usuário no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ed189-120">A user is unable to find or communicate with another user in Microsoft Teams.</span></span>
- <span data-ttu-id="ed189-121">Um usuário não pode ver ou selecionar outro usuário no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ed189-121">A user cannot see or select another user in Microsoft Teams.</span></span>
- <span data-ttu-id="ed189-122">Um usuário pode ver, mas não pode enviar mensagens para outro usuário no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ed189-122">A user can see, but cannot send messages to, another user in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="ed189-123">O que fazer</span><span class="sxs-lookup"><span data-stu-id="ed189-123">What to do</span></span>

1. <span data-ttu-id="ed189-124">Determinar se os usuários são afetados por uma política de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="ed189-124">Determine whether the users are affected by an information barrier policy.</span></span> <span data-ttu-id="ed189-125">Para fazer isso, use o cmdlet **Get-InformationBarrierRecipientStatus** com o parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="ed189-125">To do this, use the **Get-InformationBarrierRecipientStatus** cmdlet with the Identity parameter.</span></span> 

    <span data-ttu-id="ed189-126">A sintaxe é`Get-InformationBarrierRecipientStatus -Identity`</span><span class="sxs-lookup"><span data-stu-id="ed189-126">The syntax is `Get-InformationBarrierRecipientStatus -Identity`</span></span>

    <span data-ttu-id="ed189-127">Você pode usar qualquer valor de identidade que identifique exclusivamente cada destinatário, como nome, alias, nome diferenciado (DN), DN canônica, endereço de email ou GUID.</span><span class="sxs-lookup"><span data-stu-id="ed189-127">You can use any identity value that uniquely identifies each recipient, such as Name, Alias, Distinguished name (DN), Canonical DN, Email address, or GUID.</span></span>

    <span data-ttu-id="ed189-128">Exemplo: `Get-InformationBarrierRecipientStatus -Identity meganb`</span><span class="sxs-lookup"><span data-stu-id="ed189-128">Example: `Get-InformationBarrierRecipientStatus -Identity meganb`</span></span>

    <span data-ttu-id="ed189-129">Neste exemplo, estamos usando um alias (*meganb*) para o parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="ed189-129">In this example, we are using an alias (*meganb*) for the Identity parameter.</span></span> <span data-ttu-id="ed189-130">Este cmdlet retornará informações que indicam se o usuário é afetado por uma política de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="ed189-130">This cmdlet will return information that indicates whether the user is affected by an information barrier policy.</span></span> <span data-ttu-id="ed189-131">(Procure \* ExoPolicyId: \<GUID>.)</span><span class="sxs-lookup"><span data-stu-id="ed189-131">(Look for \*ExoPolicyId: \<GUID>.)</span></span>

    <span data-ttu-id="ed189-132">Se os usuários não estiverem incluídos nas políticas de barreira de informações, entre em contato com o suporte.</span><span class="sxs-lookup"><span data-stu-id="ed189-132">If the users are not included in information barrier policies, contact support.</span></span> <span data-ttu-id="ed189-133">Caso contrário, prossiga para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="ed189-133">Otherwise, proceed to the next step.</span></span>

2. <span data-ttu-id="ed189-134">Descubra quais segmentos estão incluídos em uma política de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="ed189-134">Find out which segments are included in an information barrier policy.</span></span> <span data-ttu-id="ed189-135">Para fazer isso, use o `Get-InformationBarrierPolicy` cmdlet com o parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="ed189-135">To do this, use the `Get-InformationBarrierPolicy` cmdlet with the Identity parameter.</span></span> <span data-ttu-id="ed189-136">Use detalhes, como o GUID da política (ExoPolicyId) que você recebeu durante a etapa anterior, como um valor de identidade.</span><span class="sxs-lookup"><span data-stu-id="ed189-136">Use details, such as the policy GUID (ExoPolicyId) you received during the previous step, as an identity value.</span></span>

    <span data-ttu-id="ed189-137">Exemplo: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span><span class="sxs-lookup"><span data-stu-id="ed189-137">Example: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span></span>

    <span data-ttu-id="ed189-138">Neste exemplo, estamos obtendo informações detalhadas sobre a política de barreira de informações que tem o ExoPolicyId *b42c3d0f-49E9-4506-a0a5-bf2853b5df6f*.</span><span class="sxs-lookup"><span data-stu-id="ed189-138">In this example, we are getting detailed information about the information barrier policy that has ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span></span>
    
    <span data-ttu-id="ed189-139">Depois de executar o cmdlet, nos resultados, procure os valores **AssignedSegment**, **SegmentsAllowed**e **SegmentsBlocked** .</span><span class="sxs-lookup"><span data-stu-id="ed189-139">After you run the cmdlet, in the results, look for **AssignedSegment**, **SegmentsAllowed**, and **SegmentsBlocked** values.</span></span>

    <span data-ttu-id="ed189-140">Exemplo: depois de executar `Get-InformationBarrierPolicy` o cmdlet, vimos o seguinte na lista de resultados:</span><span class="sxs-lookup"><span data-stu-id="ed189-140">Example: After running the `Get-InformationBarrierPolicy` cmdlet, we saw the following in our list of results:</span></span>

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    <span data-ttu-id="ed189-141">Nesse caso, podemos ver que uma política de barreira de informações afeta as pessoas que estão nos segmentos de vendas e de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ed189-141">In this case, we can see that an information barrier policy affects people who are in the Sales and Research segments.</span></span> <span data-ttu-id="ed189-142">Nesse caso, as pessoas em vendas são impedidas de se comunicar com pessoas em pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ed189-142">In this case, people in Sales are prevented from communicating with people in Research.</span></span> <span data-ttu-id="ed189-143">Se isso parecer correto, as barreiras de informação estão funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="ed189-143">If this seems correct, then information barriers are working as expected.</span></span> <span data-ttu-id="ed189-144">Caso contrário, vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="ed189-144">If not, proceed to the next step.</span></span>

4. <span data-ttu-id="ed189-145">Certifique-se de que seus segmentos estejam definidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="ed189-145">Make sure your segments are defined correctly.</span></span> <span data-ttu-id="ed189-146">Para fazer isso, use o `Get-OrganizationSegment` cmdlet e revise a lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="ed189-146">To do this, use the `Get-OrganizationSegment` cmdlet, and review the list of results.</span></span> 

    <span data-ttu-id="ed189-147">Para exibir detalhes de um segmento específico, use o `Get-OrganizationSegment` cmdlet com um parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="ed189-147">To view details for a specific segment, use the `Get-OrganizationSegment` cmdlet with an Identity parameter.</span></span> 

    <span data-ttu-id="ed189-148">Exemplo: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span><span class="sxs-lookup"><span data-stu-id="ed189-148">Example: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span></span>

    <span data-ttu-id="ed189-149">Neste exemplo, estamos obtendo informações sobre o segmento que tem GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span><span class="sxs-lookup"><span data-stu-id="ed189-149">In this example, we are getting information about the segment that has GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span></span>

    <span data-ttu-id="ed189-150">Revise os detalhes do segmento.</span><span class="sxs-lookup"><span data-stu-id="ed189-150">Review the details for the segment.</span></span> <span data-ttu-id="ed189-151">Se necessário, [edite um segmento](information-barriers-policies.md#edit-a-segment)e, em seguida, use `Start-InformationBarrierPoliciesApplication` o cmdlet novamente.</span><span class="sxs-lookup"><span data-stu-id="ed189-151">If necessary, [edit a segment](information-barriers-policies.md#edit-a-segment), and then re-use the `Start-InformationBarrierPoliciesApplication` cmdlet.</span></span>

    <span data-ttu-id="ed189-152">Se você ainda estiver tendo problemas com a política de barreira de informações, entre em contato com o suporte.</span><span class="sxs-lookup"><span data-stu-id="ed189-152">If you are still having issues with your information barrier policy, contact support.</span></span>
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a><span data-ttu-id="ed189-153">Problema: o processo do aplicativo de barreira de informações está demorando muito</span><span class="sxs-lookup"><span data-stu-id="ed189-153">Issue: The information barrier application process is taking too long</span></span>

<span data-ttu-id="ed189-154">Depois de executar o cmdlet **Start-InformationBarrierPoliciesApplication** , o processo está demorando muito tempo para terminar.</span><span class="sxs-lookup"><span data-stu-id="ed189-154">After running the **Start-InformationBarrierPoliciesApplication** cmdlet, the process is taking a really long time to finish.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="ed189-155">O que fazer</span><span class="sxs-lookup"><span data-stu-id="ed189-155">What to do</span></span>

1. <span data-ttu-id="ed189-156">Tenha em mente que quando você executa o cmdlet aplicativo de política, as políticas de barreira de informações são aplicadas (ou removidas), usuário por usuário para todas as contas da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ed189-156">Keep in mind that when you run the policy application cmdlet, information barrier policies are being applied (or removed), user by user, for all accounts in your organization.</span></span> <span data-ttu-id="ed189-157">Se você tiver muitos usuários, levará algum tempo para ser processado.</span><span class="sxs-lookup"><span data-stu-id="ed189-157">If you have a lot of users, it will take a while to process.</span></span> <span data-ttu-id="ed189-158">(Como uma diretriz geral, leva cerca de uma hora para processar as contas de usuário 5.000.)</span><span class="sxs-lookup"><span data-stu-id="ed189-158">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span> 

2. <span data-ttu-id="ed189-159">Use o cmdlet **Get-InformationBarrierPoliciesApplicationStatus** para verificar o status.</span><span class="sxs-lookup"><span data-stu-id="ed189-159">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet to verify status.</span></span>

    <span data-ttu-id="ed189-160">Possuem`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="ed189-160">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="ed189-161">Para exibir o status de todos os aplicativos de política de barreira de informações, use`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="ed189-161">To display status for all information barrier policy applications, use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span>

    <span data-ttu-id="ed189-162">Isso exibirá informações sobre se o aplicativo de política foi concluído, falhou ou está em andamento..</span><span class="sxs-lookup"><span data-stu-id="ed189-162">This will display information about whether policy application completed, failed, or is in progress..</span></span>

3. <span data-ttu-id="ed189-163">Dependendo dos resultados da etapa 2, execute uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ed189-163">Depending on the results of step 2, take one of the following steps:</span></span>

    - <span data-ttu-id="ed189-164">Se o aplicativo não tiver sido iniciado e tiver sido mais de 45 minutos desde que o cmdlet **Start-InformationBarrierPoliciesApplication** foi executado, revise o log de auditoria para ver se há algum erro nas definições de política ou algum outro motivo pelo qual o o aplicativo não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ed189-164">If the application has not started, and it has been more than 45 minutes since the **Start-InformationBarrierPoliciesApplication** cmdlet has been run, review your audit log to see if there are any errors in policy definitions, or some other reason why the application has not started.</span></span>

    - <span data-ttu-id="ed189-165">Se o aplicativo falhou, revise seus segmentos e políticas.</span><span class="sxs-lookup"><span data-stu-id="ed189-165">If the application has failed, review your segments and policies.</span></span> <span data-ttu-id="ed189-166">Se necessário, [edite segmentos](information-barriers-policies.md#edit-a-segment) e/ou [edite políticas](information-barriers-policies.md#edit-a-policy)e, em seguida, execute o cmdlet **Start-InformationBarrierPoliciesApplication** novamente.</span><span class="sxs-lookup"><span data-stu-id="ed189-166">If necessary, [edit segments](information-barriers-policies.md#edit-a-segment) and/or [edit policies](information-barriers-policies.md#edit-a-policy), and then run the **Start-InformationBarrierPoliciesApplication** cmdlet again.</span></span>

    - <span data-ttu-id="ed189-167">Se o aplicativo ainda estiver em andamento, permita que mais tempo seja concluído.</span><span class="sxs-lookup"><span data-stu-id="ed189-167">If the application is still in progress, allow more time for it to complete.</span></span> <span data-ttu-id="ed189-168">Se houver vários dias, entre em contato com o suporte.</span><span class="sxs-lookup"><span data-stu-id="ed189-168">If it has been several days, contact support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed189-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed189-169">Related topics</span></span>

[<span data-ttu-id="ed189-170">Definir políticas para barreiras de informações no Microsoft Teams (visualização)</span><span class="sxs-lookup"><span data-stu-id="ed189-170">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="ed189-171">Barreiras de informação (visualização)</span><span class="sxs-lookup"><span data-stu-id="ed189-171">Information barriers (Preview)</span></span>](information-barriers.md)



