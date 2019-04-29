---
title: Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Siga estas etapas para configurar os aplicativos do Azure AD Office 365 para serem controlados pelo controle de aplicativo de acesso condicional do Office 365 Cloud app Security.
ms.openlocfilehash: 74cc415220282491694bf417a6761fd43a6d3521
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402939"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a><span data-ttu-id="9a41d-103">Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365</span><span class="sxs-lookup"><span data-stu-id="9a41d-103">Deploy Conditional Access App Control for Office 365 apps</span></span>

|<span data-ttu-id="9a41d-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9a41d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9a41d-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9a41d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9a41d-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9a41d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9a41d-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9a41d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9a41d-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="9a41d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9a41d-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="9a41d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="9a41d-110">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="9a41d-110">You are here!</span></span>  <br/> [<span data-ttu-id="9a41d-111">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="9a41d-111">Next step</span></span>](ocas-session-policies.md) <br/> |[<span data-ttu-id="9a41d-112">Começar a usar</span><span class="sxs-lookup"><span data-stu-id="9a41d-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="9a41d-113">Siga estas etapas para configurar os aplicativos do Azure AD Office 365 para serem controlados pelo controle de aplicativo de acesso condicional do Office 365 Cloud app Security.</span><span class="sxs-lookup"><span data-stu-id="9a41d-113">Follow these steps to configure Azure AD Office 365 apps to be controlled by Office 365 Cloud App Security Conditional Access App Control.</span></span>

<span data-ttu-id="9a41d-114">**Etapa 1: [criar uma política de teste de acesso condicional do Azure ad](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span><span class="sxs-lookup"><span data-stu-id="9a41d-114">**Step 1: [Create an Azure AD conditional access test policy](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span></span>

<span data-ttu-id="9a41d-115">**Etapa 2: [entrar com um usuário com escopo de política nos aplicativos](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span><span class="sxs-lookup"><span data-stu-id="9a41d-115">**Step 2: [Sign in with a user scoped to the policy in the apps](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span></span>

<span data-ttu-id="9a41d-116">**Etapa 3: se você não tiver selecionado uma política de segurança do aplicativo de nuvem interna no Azure AD ou se quiser aplicar a política a um aplicativo não-----------------no [portal, configure os controles avançados no portal do Cloud app Security](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span><span class="sxs-lookup"><span data-stu-id="9a41d-116">**Step 3: If you did not select a built-in Cloud App Security policy in Azure AD or if you want to apply the policy to a non-featured app, [Configure advanced controls in the Cloud App Security portal](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span></span>

<span data-ttu-id="9a41d-117">**Etapa 4: [testar a implantação](#step-4-test-the-deployment)**</span><span class="sxs-lookup"><span data-stu-id="9a41d-117">**Step 4: [Test the deployment](#step-4-test-the-deployment)**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a41d-118">para implantar o controle de aplicativo de acesso condicional para aplicativos do Office 365, você precisa de uma [licença válida para o Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) , bem como uma licença de segurança do aplicativo na nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a41d-118">To deploy Conditional Access App Control for Office 365 apps, you need a valid [license for Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) as well as a Office 365 Cloud App Security license.</span></span>

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a><span data-ttu-id="9a41d-119">Etapa 1: criar uma política de teste de acesso condicional do Azure AD</span><span class="sxs-lookup"><span data-stu-id="9a41d-119">Step 1: Create an Azure AD conditional access test policy</span></span> 

1. <span data-ttu-id="9a41d-120">No Azure Active Directory, em **segurança**, clique em **acesso condicional**.</span><span class="sxs-lookup"><span data-stu-id="9a41d-120">In Azure Active Directory, under **Security**, click on **Conditional access**.</span></span>

2. <span data-ttu-id="9a41d-121">Clique em **nova política** e crie uma nova política.</span><span class="sxs-lookup"><span data-stu-id="9a41d-121">Click **New policy** and create a new policy.</span></span>

3. <span data-ttu-id="9a41d-122">Na política de teste, em **usuários**, atribua um usuário de teste ou usuário que possa ser usado para logon inicial e verificação.</span><span class="sxs-lookup"><span data-stu-id="9a41d-122">In the TEST policy, under **Users**, assign a test user or user that can be used for an initial sign-on and verification.</span></span>

4. <span data-ttu-id="9a41d-123">Na política de teste, em **Cloud app**, atribua os aplicativos que você deseja controlar com o controle de aplicativo de acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="9a41d-123">In the TEST policy, under **Cloud app**, assign the apps you want to control with Conditional Access App Control.</span></span>

5. <span data-ttu-id="9a41d-124">Em **sessão**, defina a política para usar uma das políticas internas, **monitorar somente** ou **bloquear downloads**.</span><span class="sxs-lookup"><span data-stu-id="9a41d-124">Under **Session**, set the policy to use either of the built-in policies, **Monitor only** or **Block downloads**.</span></span> <span data-ttu-id="9a41d-125">Ou selecione **usar política** personalizada para definir uma política avançada no portal do Cloud app Security.</span><span class="sxs-lookup"><span data-stu-id="9a41d-125">Or select **Use custom policy** to set an advanced policy in the Cloud App Security portal.</span></span>

6. <span data-ttu-id="9a41d-126">Adicione qualquer **atribuição** de condição ou **controle** de concessão aplicáveis (opcional).</span><span class="sxs-lookup"><span data-stu-id="9a41d-126">Add any applicable **Condition assignments** or **Grant controls** (optional).</span></span>

> ![Acesso condicional do Azure AD](media/OCASimage1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a><span data-ttu-id="9a41d-128">Etapa 2: entrar com um usuário com escopo de política nos aplicativos</span><span class="sxs-lookup"><span data-stu-id="9a41d-128">Step 2: Sign in with a user scoped to the policy in the apps</span></span> 

<span data-ttu-id="9a41d-129">Após criar a política, entre em cada aplicativo configurado nessa política.</span><span class="sxs-lookup"><span data-stu-id="9a41d-129">After you've created the policy, sign in to each app configured in that policy.</span></span> <span data-ttu-id="9a41d-130">Certifique-se de entrar usando um usuário configurado na política.</span><span class="sxs-lookup"><span data-stu-id="9a41d-130">Make sure you sign in using a user configured in the policy.</span></span> <span data-ttu-id="9a41d-131">Certifique-se de sair primeiro das sessões existentes.</span><span class="sxs-lookup"><span data-stu-id="9a41d-131">Make sure to first sign out of existing sessions.</span></span>

<span data-ttu-id="9a41d-132">O Cloud app Security sincronizará seus detalhes de política com seus servidores para cada aplicativo novo no qual você fizer logon.</span><span class="sxs-lookup"><span data-stu-id="9a41d-132">Cloud App Security will sync your policy details to its servers for each new app you log in to.</span></span> <span data-ttu-id="9a41d-133">Isso pode levar até um minuto.</span><span class="sxs-lookup"><span data-stu-id="9a41d-133">This may take up to one minute.</span></span>

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a><span data-ttu-id="9a41d-134">Etapa 3: configurar controles avançados no portal do Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9a41d-134">Step 3: Configure advanced controls in the Cloud App Security portal</span></span> 

<span data-ttu-id="9a41d-135">As instruções acima ajudaram você a criar uma política interna de segurança do aplicativo na nuvem para aplicativos em destaque diretamente no Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9a41d-135">The instructions above helped you create a built-in Cloud App Security policy for featured apps directly in Azure AD.</span></span>

<span data-ttu-id="9a41d-136">para configurar uma política avançada, crie uma política de [acesso](ocas-access-policies.md) ou uma [política](ocas-session-policies.md) de sessão no portal do Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="9a41d-136">To configure an advanced policy, create an [access policy](ocas-access-policies.md) or a [session policy](ocas-session-policies.md) in the Office 365 Cloud App Security portal.</span></span>

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a><span data-ttu-id="9a41d-137">Para identificar dispositivos usando certificados de cliente (isso é opcional):</span><span class="sxs-lookup"><span data-stu-id="9a41d-137">To identify devices using client certificates (this is optional):</span></span>

1. <span data-ttu-id="9a41d-138">Vá para as configurações COG e escolha **identificação de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="9a41d-138">Go to the settings cog and choose **Device identification**.</span></span>

2. <span data-ttu-id="9a41d-139">Carregar um ou mais certificados raiz ou intermediários.</span><span class="sxs-lookup"><span data-stu-id="9a41d-139">Upload one or more root or intermediate certificates.</span></span>

3. <span data-ttu-id="9a41d-140">Após o carregamento do certificado, você pode criar políticas de acesso e políticas de sessão com base na **marca de dispositivo** e **certificado de cliente válido**.</span><span class="sxs-lookup"><span data-stu-id="9a41d-140">After the certificate is uploaded, you can create access policies and session policies based on **Device tag** and **Valid client certificate**.</span></span>

![ID do dispositivo de controle de aplicativo de acesso condicional](media/OCASimage2.png)

> [!NOTE]
> <span data-ttu-id="9a41d-142">Um certificado só é solicitado a partir de um usuário se a sessão corresponder a uma política que use o filtro de certificado de cliente válido.</span><span class="sxs-lookup"><span data-stu-id="9a41d-142">A certificate is only requested from a user if the session matches a policy that uses the valid client certificate filter.</span></span>
> 
## <a name="step-4-test-the-deployment"></a><span data-ttu-id="9a41d-143">Etapa 4: testar a implantação</span><span class="sxs-lookup"><span data-stu-id="9a41d-143">Step 4: Test the deployment</span></span> 

1. <span data-ttu-id="9a41d-144">Primeiro saia de qualquer sessão existente.</span><span class="sxs-lookup"><span data-stu-id="9a41d-144">First sign out of any existing sessions.</span></span> <span data-ttu-id="9a41d-145">Em seguida, tente entrar em cada aplicativo que foi implantado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9a41d-145">Then, try to sign in to each app that was successfully deployed.</span></span> <span data-ttu-id="9a41d-146">Entre usando um usuário que coincida com a política configurada no Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9a41d-146">Sign in using a user that matches the policy configured in Azure AD.</span></span>

2. <span data-ttu-id="9a41d-147">No portal do Cloud app Security, em **Investigate**, selecione **log de atividades**e certifique-se de que as atividades de logon sejam capturadas para cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a41d-147">In the Cloud App Security portal, under **Investigate**, select **Activity log**, and make sure the login activities are captured for each app.</span></span>

3. <span data-ttu-id="9a41d-148">Você pode filtrar clicando em **avançado**e, em seguida, filtragem usando **controle de acesso de origem igual a**.</span><span class="sxs-lookup"><span data-stu-id="9a41d-148">You can filter by clicking on **Advanced**, and then filtering using **Source equals Access control**.</span></span>

4. <span data-ttu-id="9a41d-149">É recomendável que você entre em aplicativos móveis e de área de trabalho de dispositivos gerenciados e não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="9a41d-149">It's recommended that you sign into mobile and desktop apps from managed and unmanaged devices.</span></span> <span data-ttu-id="9a41d-150">Isso é para garantir que as atividades sejam capturadas corretamente no log de atividades.</span><span class="sxs-lookup"><span data-stu-id="9a41d-150">This is to make sure that the activities are properly captured in the activity log.</span></span> <span data-ttu-id="9a41d-151">Para verificar se a atividade foi capturada corretamente, clique em uma atividade de logon de logon único para que ela abra a gaveta de atividade.</span><span class="sxs-lookup"><span data-stu-id="9a41d-151">To verify that the activity is properly captured, click on a single sign-on log on activity so that it opens the activity drawer.</span></span> <span data-ttu-id="9a41d-152">Certifique-se de que a **marca** de agente do usuário reflita corretamente se o dispositivo é um cliente nativo (ou seja, um aplicativo móvel ou de área de trabalho) ou se o dispositivo é um dispositivo gerenciado (compatível, domínio associado ou certificado de cliente válido).</span><span class="sxs-lookup"><span data-stu-id="9a41d-152">Make sure the **User agent tag** properly reflects whether the device is a native client (meaning either a mobile or desktop app) or the device is a managed device (compliant, domain joined, or valid client certificate).</span></span>

> [!NOTE]
> <span data-ttu-id="9a41d-153">Depois de implantado, você não pode remover um aplicativo da página de controle de aplicativo de acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="9a41d-153">After it is deployed, you can't remove an app from the Conditional Access App Control page.</span></span> <span data-ttu-id="9a41d-154">Contanto que você não defina uma sessão ou política de acesso no aplicativo, o controle de aplicativo de acesso condicional não alterará qualquer comportamento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a41d-154">As long as you don't set a session or access policy on the app, the Conditional Access App Control won't change any behavior for the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9a41d-155">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9a41d-155">Next steps</span></span>

- [<span data-ttu-id="9a41d-156">Saiba mais sobre as políticas de sessão no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9a41d-156">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="9a41d-157">Saiba mais sobre as políticas de acesso no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9a41d-157">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 

- [<span data-ttu-id="9a41d-158">Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9a41d-158">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)