---
title: Configurando o gerenciamento de acesso privilegiado no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Use este tópico para saber mais sobre como configurar o gerenciamento de acesso privilegiado no Office 365
ms.openlocfilehash: 47cae93a41b0fd60645021f6f299645777a9a2e1
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25011837"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="f3744-103">Configurando o gerenciamento de acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="f3744-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3744-104">Este tópico aborda as diretrizes de implantação e configuração para recursos somente está disponíveis no Office 365 E5 e avançadas SKUs de conformidade.</span><span class="sxs-lookup"><span data-stu-id="f3744-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="f3744-p101">Este tópico vai orientá-lo por meio de habilitando e configurando o gerenciamento de acesso privilegiado em sua organização do Office 365. Você pode usar tanto o acesso de privilegiado o Centro de administração do Microsoft 365 ou PowerShell de gerenciamento do Exchange para gerenciar e usar.</span><span class="sxs-lookup"><span data-stu-id="f3744-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="f3744-107">Habilitar e configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="f3744-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="f3744-108">Siga estas etapas para configurar e usar o acesso privilegiado em sua organização do Office 365:</span><span class="sxs-lookup"><span data-stu-id="f3744-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="f3744-109">Etapa 1: Criar um grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="f3744-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="f3744-p102">Antes de começar a usar o acesso de privilégio, determine quem terá autoridade de aprovação para solicitações de entrada para acesso a tarefas com privilégios elevados e privilegiados. Qualquer usuário que faz parte do grupo dos aprovadores poderão aprovar solicitações de acesso. Esta opção estiver ativada, criando um grupo de segurança habilitados para email no Office 365.</span><span class="sxs-lookup"><span data-stu-id="f3744-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="f3744-113">Etapa 2: Habilitar o acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="f3744-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="f3744-114">Acesso privilegiado deve ser explicitamente ativado no Office 365 com o grupo de aprovador padrão e incluindo um conjunto de contas de sistema que deseja sejam excluídos do controle de acesso de gerenciamento de acesso privilegiado.</span><span class="sxs-lookup"><span data-stu-id="f3744-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="f3744-115">Etapa 3: Criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="f3744-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="f3744-p103">Criar uma política de aprovação permite definir os requisitos específicos de aprovação com escopo em tarefas individuais. As opções de tipo de aprovação são **Auto** ou **Manual**.</span><span class="sxs-lookup"><span data-stu-id="f3744-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="f3744-118">Etapa 4: Enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="f3744-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="f3744-p104">Uma vez ativado, com privilégios de acesso requer aprovações para executar qualquer tarefa que tem uma política de aprovação associados definida. Os usuários que precisam executar tarefas incluídas na uma política de aprovação deve solicitar e receber aprovação de acesso para que as permissões necessárias para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f3744-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="f3744-p105">Após a aprovação for concedida, o usuário solicitante pode executar a tarefa pretendida e acesso privilegiado será autorizar e executar a tarefa em nome dos usuários. A aprovação permanecerá válida para os solicitados duração (duração padrão é 4 horas), durante o qual o solicitante pode executar a tarefa pretendida várias vezes. Todas essas execuções são registradas e torná-los disponíveis para auditoria de conformidade e segurança.</span><span class="sxs-lookup"><span data-stu-id="f3744-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3744-p106">Se você quiser usar o PowerShell de gerenciamento do Exchange para habilitar e configurar o acesso privilegiado, siga as etapas em [Connect to Exchange Online PowerShell usando a autenticação multifator](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) para se conectar ao PowerShell do Exchange Online com o Office 365 credenciais. Você não precisará habilitar a autenticação multifator para sua organização do Office 365 usar as etapas para habilitar o acesso privilegiado ao conectar ao PowerShell do Exchange Online. Conexão com a autenticação multifator cria um token de OAuth que é usado pelo acesso privilegiado para assinar suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="f3744-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="f3744-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="f3744-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="f3744-128">Etapa 1 - Criar grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="f3744-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="f3744-129">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="f3744-130">No Centro de administração, vá para **grupos** > **Adicionar um grupo**.</span><span class="sxs-lookup"><span data-stu-id="f3744-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="f3744-131">Selecione o tipo de grupo do **grupo de segurança habilitados para email** e, em seguida, preencha os campos de **nome**, **endereço de email do grupo**e **Descrição** para o novo grupo.</span><span class="sxs-lookup"><span data-stu-id="f3744-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="f3744-p107">Salve o grupo. Pode levar alguns minutos para que o grupo a ser totalmente configurado e aparecem no Centro de administração do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f3744-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="f3744-134">Selecione grupo do aprovador novo e selecione **Editar** para adicionar usuários ao grupo.</span><span class="sxs-lookup"><span data-stu-id="f3744-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="f3744-135">Salve o grupo.</span><span class="sxs-lookup"><span data-stu-id="f3744-135">Save the group.</span></span>

<span data-ttu-id="f3744-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="f3744-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="f3744-137">Etapa 2 - habilitar acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="f3744-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-138">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-139">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="f3744-140">No Centro de administração, vá para **Configurações > segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-141">Ative o controle **exigem aprovações para acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="f3744-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="f3744-142">Atribua um grupo do aprovador que você criou na etapa 1 como o **grupo de aprovadores padrão**.</span><span class="sxs-lookup"><span data-stu-id="f3744-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="f3744-143">**Salvar** e **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="f3744-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-144">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-145">Execute o seguinte comando no PowerShell do Exchange Online para habilitar o acesso privilegiado e atribuir o grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="f3744-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="f3744-146">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="f3744-147">Contas de sistema recurso é disponibilizado garantir que certas automáticos em suas organizações podem trabalhar sem dependência no acesso privilegiado, no entanto, é recomendável que tal exclusões ser excepcionais e devem ser aprovados e auditadas aqueles permitidos regularmente.</span><span class="sxs-lookup"><span data-stu-id="f3744-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="f3744-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="f3744-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="f3744-149">Etapa 3: criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="f3744-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="f3744-150">Você pode criar e configurar políticas de acesso privilegiado até 30 para sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f3744-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-151">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-152">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="f3744-153">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-154">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="f3744-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f3744-155">Selecione **Configurar políticas** e **Adicionar uma política**.</span><span class="sxs-lookup"><span data-stu-id="f3744-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="f3744-156">Nos campos de lista suspensa, selecione os valores apropriados para sua organização:</span><span class="sxs-lookup"><span data-stu-id="f3744-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="f3744-157">**Tipo de política**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="f3744-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="f3744-158">**Escopo da política**: Exchange ou o Office 365</span><span class="sxs-lookup"><span data-stu-id="f3744-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="f3744-159">**Nome da política**: selecione as diretivas disponíveis</span><span class="sxs-lookup"><span data-stu-id="f3744-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="f3744-160">**Tipo de aprovação**: Manual ou automático</span><span class="sxs-lookup"><span data-stu-id="f3744-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="f3744-161">**Grupo de aprovação**: selecione o grupo de aprovadores criado na etapa 1</span><span class="sxs-lookup"><span data-stu-id="f3744-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="f3744-p108">Selecione **criar** e em seguida **Fechar**. Pode levar alguns minutos para a diretiva a ser totalmente configurada e habilitada.</span><span class="sxs-lookup"><span data-stu-id="f3744-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-164">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-165">Execute o seguinte comando no Exchange Online PowerShell para criar e definir uma política de aprovação:</span><span class="sxs-lookup"><span data-stu-id="f3744-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="f3744-166">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="f3744-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="f3744-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="f3744-168">Etapa 4: Enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="f3744-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="f3744-169">Autorização de elevação solicitante para executar tarefas com privilégios</span><span class="sxs-lookup"><span data-stu-id="f3744-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="f3744-p109">Solicitações de acesso privilegiado são válidas por até 24 horas depois que a solicitação é enviada. Se não aprovadas ou negadas, as solicitações expiram e acesso não for aprovado.</span><span class="sxs-lookup"><span data-stu-id="f3744-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-172">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-173">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="f3744-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="f3744-174">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-175">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="f3744-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f3744-p110">Selecione **nova solicitação**. Nos campos de lista suspensa, selecione os valores apropriados para sua organização:</span><span class="sxs-lookup"><span data-stu-id="f3744-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="f3744-178">**Tipo de solicitação**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="f3744-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="f3744-179">**Escopo de solicitação**: Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="f3744-180">**Solicitar para**: selecione as diretivas disponíveis</span><span class="sxs-lookup"><span data-stu-id="f3744-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="f3744-p111">**Duração (horas)**: número de horas de acesso solicitado. Não há um limite no número de horas que podem ser solicitados.</span><span class="sxs-lookup"><span data-stu-id="f3744-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="f3744-183">**Comentários**: campo de texto para comentários relacionados à sua solicitação de acesso</span><span class="sxs-lookup"><span data-stu-id="f3744-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="f3744-p112">Selecione **Salvar** e **Fechar**. Sua solicitação será enviada ao grupo do aprovador via email.</span><span class="sxs-lookup"><span data-stu-id="f3744-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-186">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-187">Execute o seguinte comando no Exchange Online PowerShell para criar e enviar uma solicitação de aprovação ao grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="f3744-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="f3744-188">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="f3744-189">Exibir o status das solicitações de elevação</span><span class="sxs-lookup"><span data-stu-id="f3744-189">View status of elevation requests</span></span>
<span data-ttu-id="f3744-190">Depois que uma solicitação de aprovação é criada, o status da solicitação de elevação podem ser revisadas no Centro de administração ou no Exchange identificação do PowerShell de gerenciamento usando o associado com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f3744-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-191">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-192">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="f3744-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="f3744-193">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-194">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="f3744-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f3744-195">Selecione **Exibir** para filtrar solicitações enviadas por status **pendente**, **aprovado**, **negados**ou **Lockbox do cliente** .</span><span class="sxs-lookup"><span data-stu-id="f3744-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-196">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-197">Execute o seguinte comando no Exchange Online PowerShell para exibir o status de uma solicitação de aprovação para uma ID de solicitação específica:</span><span class="sxs-lookup"><span data-stu-id="f3744-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="f3744-198">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="f3744-199">Aprovar uma solicitação de autorização de elevação</span><span class="sxs-lookup"><span data-stu-id="f3744-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="f3744-p113">Quando uma solicitação de aprovação é criada, os membros do grupo aprovador relevantes receberão uma notificação de e-mail e podem aprovar a solicitação associada com o ID de solicitação. O solicitante será notificado da aprovação de solicitação ou negação via mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f3744-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-202">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-203">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="f3744-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="f3744-204">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-205">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="f3744-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f3744-206">Selecione uma solicitação listada para exibir os detalhes e agir em relação a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f3744-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="f3744-p114">Selecione **Aprovar** para aprovar a solicitação ou selecione **Negar** negar a solicitação. Anteriormente solicitações aprovadas podem ter acesso revogado selecionando **revogar**.</span><span class="sxs-lookup"><span data-stu-id="f3744-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-209">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-210">Execute o seguinte comando no Exchange Online PowerShell para aprovar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="f3744-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="f3744-211">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="f3744-212">Execute o seguinte comando no Exchange Online PowerShell para negar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="f3744-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="f3744-213">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f3744-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="f3744-214">Excluir uma política de acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="f3744-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="f3744-215">Você pode excluir uma política de acesso privilegiado se ele não é mais necessária em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-216">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-217">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="f3744-218">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-219">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="f3744-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f3744-220">Selecione **Configurar diretivas**.</span><span class="sxs-lookup"><span data-stu-id="f3744-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="f3744-221">Selecione a política que você deseja excluir e selecionando **Remover política**.</span><span class="sxs-lookup"><span data-stu-id="f3744-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="f3744-222">Selecione **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="f3744-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-223">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-224">Execute o seguinte comando no Exchange Online Powershell para excluir uma política de acesso privilegiado:</span><span class="sxs-lookup"><span data-stu-id="f3744-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="f3744-225">Desabilitar acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="f3744-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="f3744-p115">Se necessário, você pode desativar o gerenciamento de acesso privilegiado para sua organização. Desabilitando privilegiada acesso não exclui quaisquer políticas de aprovação associados ou a grupos de aprovador.</span><span class="sxs-lookup"><span data-stu-id="f3744-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="f3744-228">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3744-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="f3744-229">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f3744-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="f3744-230">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="f3744-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f3744-231">Ative o controle **exigem aprovações para acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="f3744-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="f3744-232">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="f3744-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="f3744-233">Execute o seguinte comando no Exchange Online Powershell para desabilitar o acesso privilegiado:</span><span class="sxs-lookup"><span data-stu-id="f3744-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```