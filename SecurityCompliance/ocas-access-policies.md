---
title: Políticas de acesso no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: As políticas de acesso do Office 365 Cloud app Security permitem o monitoramento em tempo real e o controle sobre o acesso a aplicativos em nuvem com base no usuário, local, dispositivo e aplicativo. Você pode criar políticas de acesso para qualquer dispositivo, incluindo dispositivos que não são associados ao domínio, e não gerenciados pelo Windows Intune, distribuindo certificados de cliente para dispositivos gerenciados ou usando certificados existentes, como certificados MDM de terceiros. Por exemplo, você pode implantar certificados de cliente em dispositivos gerenciados e, em seguida, bloquear o acesso de dispositivos sem um certificado.
ms.openlocfilehash: 5e8b8fa293420bc9ff3616daf288b8e02a2eb768
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262994"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a><span data-ttu-id="71be0-105">Políticas de acesso no Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="71be0-105">Access policies in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="71be0-106">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="71be0-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="71be0-107">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="71be0-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="71be0-108">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="71be0-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="71be0-109">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="71be0-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="71be0-110">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="71be0-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="71be0-111">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="71be0-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="71be0-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="71be0-112">You are here!</span></span>  <br/> [<span data-ttu-id="71be0-113">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="71be0-113">Next step</span></span>](group-your-ip-addresses-in-ocas.md) <br/> |[<span data-ttu-id="71be0-114">Começar a usar</span><span class="sxs-lookup"><span data-stu-id="71be0-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="71be0-115">As políticas de acesso do Office 365 Cloud app Security permitem o monitoramento em tempo real e o controle sobre o acesso a aplicativos em nuvem com base no usuário, local, dispositivo e aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71be0-115">Office 365 Cloud App Security access policies enable real-time monitoring and control over access to cloud apps based on user, location, device, and app.</span></span> <span data-ttu-id="71be0-116">Você pode criar políticas de acesso para qualquer dispositivo, incluindo dispositivos que não são associados ao domínio, e não gerenciados pelo Windows Intune, distribuindo certificados de cliente para dispositivos gerenciados ou usando certificados existentes, como certificados MDM de terceiros.</span><span class="sxs-lookup"><span data-stu-id="71be0-116">You can create access policies for any device, including devices that aren't domain joined, and not managed by Windows Intune by rolling out client certificates to managed devices or by using existing certificates, such as third-party MDM certificates.</span></span> <span data-ttu-id="71be0-117">Por exemplo, você pode implantar certificados de cliente em dispositivos gerenciados e, em seguida, bloquear o acesso de dispositivos sem um certificado.</span><span class="sxs-lookup"><span data-stu-id="71be0-117">For example, you can deploy client certificates to managed devices, and then block access from devices without a certificate.</span></span>

<span data-ttu-id="71be0-118">Em vez de permitir ou bloquear totalmente o acesso, com [políticas](ocas-session-policies.md) de sessão, você pode permitir o acesso enquanto monitora a sessão e/ou limita as atividades específicas da sessão.</span><span class="sxs-lookup"><span data-stu-id="71be0-118">Instead of allowing or blocking access completely, with [session policies](ocas-session-policies.md) you can allow access while monitoring the session and/or limit specific session activities.</span></span>

## <a name="prerequisites-to-using-access-policies"></a><span data-ttu-id="71be0-119">Pré-requisitos para usar políticas de acesso</span><span class="sxs-lookup"><span data-stu-id="71be0-119">Prerequisites to using access policies</span></span>

- <span data-ttu-id="71be0-120">Licença do Azure AD Premium P1</span><span class="sxs-lookup"><span data-stu-id="71be0-120">Azure AD Premium P1 license</span></span>

- <span data-ttu-id="71be0-121">Os aplicativos relevantes devem ser [implantados com o controle de aplicativo de acesso condicional](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span><span class="sxs-lookup"><span data-stu-id="71be0-121">The relevant apps should be [deployed with Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span></span>

- <span data-ttu-id="71be0-122"> uma [política de acesso condicional do Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)deve estar no lugar que redireciona os usuários para o Office 365 Cloud App Security, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="71be0-122">An [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) should be in place that redirects users to Office 365 Cloud App Security, as described below.</span></span>

## <a name="create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="71be0-123">Criar uma política de acesso condicional do Azure AD</span><span class="sxs-lookup"><span data-stu-id="71be0-123">Create an Azure AD conditional access policy</span></span>

<span data-ttu-id="71be0-124">As políticas de acesso condicional do Azure Active Directory e diretivas de sessão de segurança do Cloud app funcionam em tandem para examinar cada sessão de usuário e tomar decisões sobre a política para cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71be0-124">Azure Active Directory conditional access policies and Cloud App Security session policies work in tandem to examine each user session and make policy decisions for each app.</span></span> <span data-ttu-id="71be0-125">Para configurar uma política de acesso condicional no Azure AD, siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="71be0-125">To set up a conditional access policy in Azure AD, follow this procedure:</span></span>

1. <span data-ttu-id="71be0-126">Configure uma [política de acesso condicional do Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)com atribuições para o usuário ou grupo de usuários e o aplicativo que você deseja controlar com o controle de aplicativo de acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="71be0-126">Configure an [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) with assignments for user or group of users and the app you want to control with Conditional Access App Control.</span></span><br><span data-ttu-id="71be0-127">Observação: somente os aplicativos que foram implantados com o  [controle de aplicativo de acesso condicional](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)serão afetados por essa política.</span><span class="sxs-lookup"><span data-stu-id="71be0-127">NOTE: Only apps that were [deployed with Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) will be affected by this policy.</span></span>

2. <span data-ttu-id="71be0-128">encaminhe os usuários para o Office 365 Cloud App Security selecionando as  **restrições de usar o controle de aplicativo de acesso condicional**em **sessão**.</span><span class="sxs-lookup"><span data-stu-id="71be0-128">Route users to Office 365 Cloud App Security by selecting the **Use Conditional Access App Control enforced restrictions** under **Session**.</span></span>

## <a name="create-a-cloud-app-security-access-policy"></a><span data-ttu-id="71be0-129">Criar uma política de acesso de segurança do Cloud app</span><span class="sxs-lookup"><span data-stu-id="71be0-129">Create a Cloud App Security access policy</span></span>

<span data-ttu-id="71be0-130">Para criar uma nova política de acesso, siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="71be0-130">To create a new access policy, follow this procedure:</span></span>

1. <span data-ttu-id="71be0-131">No portal, selecione **controle** seguido por **políticas**.</span><span class="sxs-lookup"><span data-stu-id="71be0-131">In the portal, select **Control** followed by **Policies**.</span></span>

2. <span data-ttu-id="71be0-132">Na página **políticas** , clique em **criar política** e selecione **política de acesso**.</span><span class="sxs-lookup"><span data-stu-id="71be0-132">In the **Policies** page, click **Create policy** and select **Access policy**.</span></span>

3. <span data-ttu-id="71be0-133">Na janela **política** de acesso, atribua um nome para a política, como *bloquear o acesso de dispositivos não gerenciados*.</span><span class="sxs-lookup"><span data-stu-id="71be0-133">In the **Access policy** window, assign a name for your policy, such as *Block access from unmanaged devices*.</span></span>

4. <span data-ttu-id="71be0-134">Nas **atividades correspondentes a todas as seguintes** seções, em **origem da atividade**, selecione filtros de atividade adicionais a serem aplicados à política.</span><span class="sxs-lookup"><span data-stu-id="71be0-134">In the **Activities matching all of the following** section, Under **Activity source**, select additional activity filters to apply to the policy.</span></span> <span data-ttu-id="71be0-135">Os filtros incluem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="71be0-135">Filters include the following options:</span></span>
    
    - <span data-ttu-id="71be0-136">**Marcas de dispositivo**: Use este filtro para identificar dispositivos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="71be0-136">**Device tags**: Use this filter to identify unmanaged devices.</span></span>
    
    - <span data-ttu-id="71be0-137">**Local**: Use este filtro para identificar locais desconhecidos (e, portanto, arriscados).</span><span class="sxs-lookup"><span data-stu-id="71be0-137">**Location**: Use this filter to identify unknown (and therefore risky) locations.</span></span>
    
    - <span data-ttu-id="71be0-138">**Endereço IP**: Use este filtro para filtrar por endereços IP ou usar marcas de endereço IP previamente atribuídas.</span><span class="sxs-lookup"><span data-stu-id="71be0-138">**IP address**: Use this filter to filter per IP addresses or use previously assigned IP address tags.</span></span>
    
    - <span data-ttu-id="71be0-139">**Marca de agente do usuário**: Use este filtro para habilitar o heurístico para identificar aplicativos móveis e de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="71be0-139">**User agent tag**: Use this filter to enable the heuristic to identify mobile and desktop apps.</span></span> <span data-ttu-id="71be0-140">Esse filtro pode ser definido como igual ou diferente de.</span><span class="sxs-lookup"><span data-stu-id="71be0-140">This filter can be set to equals or does not equal.</span></span> <span data-ttu-id="71be0-141">Os valores devem ser testados em relação aos aplicativos móveis e de área de trabalho para cada aplicativo de nuvem.</span><span class="sxs-lookup"><span data-stu-id="71be0-141">The values should be tested against your mobile and desktop apps for each cloud app.</span></span>

5. <span data-ttu-id="71be0-142">Em **ações**, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="71be0-142">Under **Actions**, select one of the following options:</span></span>
    
    - <span data-ttu-id="71be0-143">**Permitir**: defina esta ação para permitir explicitamente o acesso de acordo com os filtros de política definidos.</span><span class="sxs-lookup"><span data-stu-id="71be0-143">**Allow**: Set this action to explicitly allow access according to the policy filters you set.</span></span>
    
    - <span data-ttu-id="71be0-144">**Bloquear**: defina esta ação para bloquear explicitamente o acesso de acordo com os filtros de política definidos.</span><span class="sxs-lookup"><span data-stu-id="71be0-144">**Block**: Set this action to explicitly block access according to the policy filters you set.</span></span>

6. <span data-ttu-id="71be0-145">Você pode **criar um alerta para cada evento coincidente com a severidade da política**e definir um limite de alerta e selecionar se deseja que o alerta seja um email, uma mensagem de texto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="71be0-145">You can **Create an alert for each matching event with the policy's severity** and set an alert limit and select whether you want the alert as an email, a text message or both.</span></span>

## <a name="next-steps"></a><span data-ttu-id="71be0-146">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="71be0-146">Next steps</span></span>

- [<span data-ttu-id="71be0-147">Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="71be0-147">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)