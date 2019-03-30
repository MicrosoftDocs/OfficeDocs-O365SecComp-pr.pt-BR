---
title: ConFigurando o gerenciamento de acesso privilegiado no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: Use este tópico para saber mais sobre como configurar o gerenciamento de acesso privilegiado no Office 365
ms.openlocfilehash: 9d0f5955eb2fd67d245bad3e7a9b1b89769bd947
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001144"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="0d186-103">ConFigurando o gerenciamento de acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="0d186-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d186-104">Este tópico aborda as diretrizes de implantação e configuração dos recursos disponíveis atualmente no Office 365 E5 e nas SKUs de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="0d186-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="0d186-105">Este tópico irá orientá-lo na habilitação e configuração do gerenciamento de acesso privilegiado na sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d186-105">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="0d186-106">Você pode usar o centro de administração do Microsoft 365 ou o PowerShell de gerenciamento do Exchange para gerenciar e usar o acesso privilegiado.</span><span class="sxs-lookup"><span data-stu-id="0d186-106">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="0d186-107">Habilitar e configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="0d186-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="0d186-108">Siga estas etapas para configurar e usar o acesso privilegiado na sua organização do Office 365:</span><span class="sxs-lookup"><span data-stu-id="0d186-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="0d186-109">Etapa 1: criar um grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="0d186-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="0d186-110">Antes de começar a usar o acesso de privilégio, determine quem terá autoridade de aprovação para solicitações de entrada para acesso a tarefas privilegiadas e privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="0d186-110">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="0d186-111">Qualquer usuário que faça parte do grupo aprovadores poderá aprovar as solicitações de acesso.</span><span class="sxs-lookup"><span data-stu-id="0d186-111">Any user who is part of the Approvers’ group will be able to approve access requests.</span></span> <span data-ttu-id="0d186-112">Isso é habilitado através da criação de um grupo de segurança habilitado para email no Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d186-112">This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="0d186-113">Etapa 2: habilitar o acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="0d186-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="0d186-114">O acesso privilegiado precisa estar explicitamente ativado no Office 365 com o grupo de aprovadores padrão e incluir um conjunto de contas de sistema que você deseja excluir do controle de acesso de gerenciamento de acesso privilegiado.</span><span class="sxs-lookup"><span data-stu-id="0d186-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="0d186-115">Etapa 3: criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="0d186-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="0d186-116">A criação de uma política de aprovação permite definir os requisitos de aprovação específicos delimitados em tarefas individuais.</span><span class="sxs-lookup"><span data-stu-id="0d186-116">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="0d186-117">As opções de tipo de aprovação são **auto** ou **manual**.</span><span class="sxs-lookup"><span data-stu-id="0d186-117">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="0d186-118">Etapa 4: enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="0d186-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="0d186-119">Uma vez habilitado, o acesso privilegiado requer aprovações para executar qualquer tarefa com uma política de aprovação associada definida.</span><span class="sxs-lookup"><span data-stu-id="0d186-119">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined.</span></span> <span data-ttu-id="0d186-120">Os usuários que precisam executar tarefas incluídas na política de aprovação devem solicitar e receber aprovação de acesso para ter as permissões necessárias para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0d186-120">Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="0d186-121">Depois que a aprovação for concedida, o usuário solicitante poderá executar a tarefa pretendida e o acesso privilegiado autorizará e executará a tarefa no nome dos usuários.</span><span class="sxs-lookup"><span data-stu-id="0d186-121">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf.</span></span> <span data-ttu-id="0d186-122">A aprovação permanece válida para a duração solicitada (a duração padrão é de 4 horas), durante a qual o solicitante pode executar a tarefa pretendida várias vezes.</span><span class="sxs-lookup"><span data-stu-id="0d186-122">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="0d186-123">Todas essas execuções são registradas e disponibilizadas para auditoria de segurança e conformidade.</span><span class="sxs-lookup"><span data-stu-id="0d186-123">All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d186-124">Se você quiser usar o PowerShell de gerenciamento do Exchange para habilitar e configurar o acesso privilegiado, siga as etapas em [conectar ao PowerShell do Exchange Online usando a autenticação](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) multifator para se conectar ao PowerShell do Exchange Online com seu Office 365 las.</span><span class="sxs-lookup"><span data-stu-id="0d186-124">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="0d186-125">Você não precisa habilitar a autenticação multifator para sua organização do Office 365 para usar as etapas para habilitar o acesso privilegiado ao se conectar ao PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0d186-125">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="0d186-126">A conexão com a autenticação multifator cria um token OAuth usado pelo acesso privilegiado para assinar suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="0d186-126">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="0d186-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="0d186-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="0d186-128">Etapa 1: criar um grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="0d186-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="0d186-129">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando as credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-129">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="0d186-130">No centro de administração, vá para **grupos** > **Adicionar um grupo**.</span><span class="sxs-lookup"><span data-stu-id="0d186-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="0d186-131">Selecione o tipo de grupo de **segurança habilitado para email** e preencha os **campos nome**, endereço de **email do grupo**e **Descrição** do novo grupo.</span><span class="sxs-lookup"><span data-stu-id="0d186-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="0d186-132">Salve o grupo.</span><span class="sxs-lookup"><span data-stu-id="0d186-132">Save the group.</span></span> <span data-ttu-id="0d186-133">Pode levar alguns minutos para que o grupo seja totalmente configurado e apareça no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d186-133">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="0d186-134">Selecione o novo grupo do aprovador e selecione **Editar** para adicionar usuários ao grupo.</span><span class="sxs-lookup"><span data-stu-id="0d186-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="0d186-135">Salve o grupo.</span><span class="sxs-lookup"><span data-stu-id="0d186-135">Save the group.</span></span>

<span data-ttu-id="0d186-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="0d186-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="0d186-137">Etapa 2-habilitar o acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="0d186-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-138">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="0d186-139">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando as credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-139">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="0d186-140">No centro de administração, vá para **configurações > segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-141">Habilitar as **aprovações de controle de acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="0d186-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="0d186-142">Atribua o grupo do aprovador que você criou na etapa 1 como o **grupo de aprovadoRes padrão**.</span><span class="sxs-lookup"><span data-stu-id="0d186-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="0d186-143">**Salvar** e **fechar**.</span><span class="sxs-lookup"><span data-stu-id="0d186-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-144">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-145">Execute o seguinte comando no PowerShell do Exchange Online para habilitar o acesso privilegiado e atribuir o grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="0d186-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="0d186-146">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="0d186-147">O recurso de contas de sistema é disponibilizado para garantir que determinadas automaçãos em suas organizações possam trabalhar sem dependências de acesso privilegiado, no entanto, é recomendável que essas exclusões sejam excepcionais e que as permitidas sejam aprovadas e auditadas atualizado.</span><span class="sxs-lookup"><span data-stu-id="0d186-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="0d186-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="0d186-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="0d186-149">Etapa 3: criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="0d186-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="0d186-150">Você pode criar e configurar até 30 políticas de acesso privilegiado para sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d186-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-151">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="0d186-152">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando as credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-152">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="0d186-153">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-154">Selecione **gerenciar políticas e solicitações de acesso**.</span><span class="sxs-lookup"><span data-stu-id="0d186-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="0d186-155">Selecione **Configurar políticas** e selecione **Adicionar uma política**.</span><span class="sxs-lookup"><span data-stu-id="0d186-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="0d186-156">Nos campos suspensos, selecione os valores apropriados para a sua organização:</span><span class="sxs-lookup"><span data-stu-id="0d186-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="0d186-157">**Tipo de política**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="0d186-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="0d186-158">**Escopo da política**: Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-158">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="0d186-159">**Nome da política**: selecione nas políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="0d186-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="0d186-160">**Tipo de aprovação**: manual ou automática</span><span class="sxs-lookup"><span data-stu-id="0d186-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="0d186-161">**Grupo de aprovação**: selecione o grupo aprovadores criado na etapa 1</span><span class="sxs-lookup"><span data-stu-id="0d186-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="0d186-162">Selecione **criar** e **fechar**.</span><span class="sxs-lookup"><span data-stu-id="0d186-162">Select **Create** and then **Close**.</span></span> <span data-ttu-id="0d186-163">Pode levar alguns minutos até que a política seja totalmente configurada e habilitada.</span><span class="sxs-lookup"><span data-stu-id="0d186-163">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-164">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-165">Execute o seguinte comando no PowerShell do Exchange Online para criar e definir uma política de aprovação:</span><span class="sxs-lookup"><span data-stu-id="0d186-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="0d186-166">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="0d186-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="0d186-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="0d186-168">Etapa 4: enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="0d186-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="0d186-169">Solicitando autorização de elevação para executar tarefas privilegiadas</span><span class="sxs-lookup"><span data-stu-id="0d186-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="0d186-170">As solicitações de acesso privilegiado são válidas por até 24 horas após o envio da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0d186-170">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="0d186-171">Se não for aprovada ou negada, as solicitações expirarão e o acesso não será aprovado.</span><span class="sxs-lookup"><span data-stu-id="0d186-171">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-172">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="0d186-173">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="0d186-173">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="0d186-174">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-175">Selecione **gerenciar políticas e solicitações de acesso**.</span><span class="sxs-lookup"><span data-stu-id="0d186-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="0d186-176">Selecione **nova solicitação**.</span><span class="sxs-lookup"><span data-stu-id="0d186-176">Select **New request**.</span></span> <span data-ttu-id="0d186-177">Nos campos suspensos, selecione os valores apropriados para a sua organização:</span><span class="sxs-lookup"><span data-stu-id="0d186-177">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="0d186-178">**Tipo de solicitação**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="0d186-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="0d186-179">**Escopo da solicitação**: Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="0d186-180">**Solicitação de**: selecione nas políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="0d186-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="0d186-181">**Duração (horas)**: número de horas de acesso solicitado.</span><span class="sxs-lookup"><span data-stu-id="0d186-181">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="0d186-182">Não há um limite no número de horas que podem ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0d186-182">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="0d186-183">**Comments**: campo de texto para comentários relacionados à sua solicitação de acesso</span><span class="sxs-lookup"><span data-stu-id="0d186-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="0d186-184">Selecione **salvar** e **fechar**.</span><span class="sxs-lookup"><span data-stu-id="0d186-184">Select **Save** and then **Close**.</span></span> <span data-ttu-id="0d186-185">Sua solicitação será enviada ao grupo do aprovador por email.</span><span class="sxs-lookup"><span data-stu-id="0d186-185">Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-186">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-187">Execute o seguinte comando no PowerShell do Exchange Online para criar e enviar uma solicitação de aprovação para o grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="0d186-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="0d186-188">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="0d186-189">Exibir o status das solicitações de elevação</span><span class="sxs-lookup"><span data-stu-id="0d186-189">View status of elevation requests</span></span>
<span data-ttu-id="0d186-190">Após a criação de uma solicitação de aprovação, o status da solicitação de elevação poderá ser revisado no centro de administração ou no PowerShell de gerenciamento do Exchange usando o ID de solicitação associado.</span><span class="sxs-lookup"><span data-stu-id="0d186-190">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-191">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-191">Using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="0d186-192">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="0d186-192">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="0d186-193">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-193">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-194">Selecione **gerenciar políticas e solicitações de acesso**.</span><span class="sxs-lookup"><span data-stu-id="0d186-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="0d186-195">Selecione **Exibir** para filtrar solicitações enviadas por status **pendente**, **aprovado**, **negado**ou de lockbox do **cliente** .</span><span class="sxs-lookup"><span data-stu-id="0d186-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-196">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-197">Execute o seguinte comando no PowerShell do Exchange Online para exibir um status de solicitação de aprovação para uma ID de solicitação específica:</span><span class="sxs-lookup"><span data-stu-id="0d186-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="0d186-198">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="0d186-199">Aprovar uma solicitação de autorização de elevação</span><span class="sxs-lookup"><span data-stu-id="0d186-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="0d186-200">Quando uma solicitação de aprovação é criada, os membros do grupo de aprovadores relevantes receberão uma notificação por email e poderão aprovar a solicitação associada ao ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0d186-200">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="0d186-201">O solicitante será notificado sobre a aprovação da solicitação ou a negação via mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0d186-201">The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-202">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-202">Using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="0d186-203">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="0d186-203">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="0d186-204">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-204">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-205">Selecione **gerenciar políticas e solicitações de acesso**.</span><span class="sxs-lookup"><span data-stu-id="0d186-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="0d186-206">Selecione uma solicitação listada para exibir os detalhes e executar a ação na solicitação.</span><span class="sxs-lookup"><span data-stu-id="0d186-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="0d186-207">Selecione **aprovar** para aprovar a solicitação ou selecione **negar** para negar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="0d186-207">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="0d186-208">As solicitações aprovadas anteriormente podem ter acesso revogado ao \*\*\*\* selecionar revogar.</span><span class="sxs-lookup"><span data-stu-id="0d186-208">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-209">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-210">Execute o seguinte comando no PowerShell do Exchange Online para aprovar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="0d186-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="0d186-211">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="0d186-212">Execute o seguinte comando no PowerShell do Exchange Online para negar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="0d186-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="0d186-213">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d186-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="0d186-214">Excluir uma política de acesso privilegiada no Office 365</span><span class="sxs-lookup"><span data-stu-id="0d186-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="0d186-215">Você pode excluir uma política de acesso privilegiado se ela não for mais necessária em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-216">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-216">Using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="0d186-217">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando as credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="0d186-218">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-218">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-219">Selecione **gerenciar políticas e solicitações de acesso**.</span><span class="sxs-lookup"><span data-stu-id="0d186-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="0d186-220">Selecione **Configurar políticas**.</span><span class="sxs-lookup"><span data-stu-id="0d186-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="0d186-221">Selecione a política que você deseja excluir e, em seguida, selecione **remover política**.</span><span class="sxs-lookup"><span data-stu-id="0d186-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="0d186-222">Selecione **fechar**.</span><span class="sxs-lookup"><span data-stu-id="0d186-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-223">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-224">Execute o seguinte comando no PowerShell do Exchange Online para excluir uma política de acesso privilegiada:</span><span class="sxs-lookup"><span data-stu-id="0d186-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="0d186-225">Desabilitar o acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="0d186-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="0d186-226">Se necessário, você pode desabilitar o gerenciamento de acesso privilegiado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-226">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="0d186-227">Desabilitar o acesso privilegiado não exclui nenhuma política de aprovação associada ou grupos de aprovadores.</span><span class="sxs-lookup"><span data-stu-id="0d186-227">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="0d186-228">Usando o centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d186-228">Using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="0d186-229">Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com) usando as credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d186-229">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="0d186-230">No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.</span><span class="sxs-lookup"><span data-stu-id="0d186-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="0d186-231">Habilitar as **aprovações de controle de acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="0d186-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="0d186-232">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="0d186-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="0d186-233">Execute o seguinte comando no PowerShell do Exchange Online para desabilitar o acesso privilegiado:</span><span class="sxs-lookup"><span data-stu-id="0d186-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```