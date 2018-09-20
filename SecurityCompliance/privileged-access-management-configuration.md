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
ms.openlocfilehash: 6494505554a02f005df8f45839c9575094acbf1a
ms.sourcegitcommit: d31904e81f81d0fba75309a2bc8bbfb05565a0b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2018
ms.locfileid: "24055246"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="49867-103">Configurando o gerenciamento de acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="49867-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49867-104">Este tópico aborda as diretrizes de implantação e configuração para recursos somente está disponíveis no Office 365 E5 e avançadas SKUs de conformidade.</span><span class="sxs-lookup"><span data-stu-id="49867-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="49867-p101">Este tópico vai orientá-lo por meio de habilitando e configurando o gerenciamento de acesso privilegiado em sua organização do Office 365. Você pode usar tanto o acesso de privilegiado o Centro de administração do Microsoft 365 ou PowerShell de gerenciamento do Exchange para gerenciar e usar.</span><span class="sxs-lookup"><span data-stu-id="49867-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="49867-107">Habilitar e configurar o gerenciamento de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="49867-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="49867-108">Siga estas etapas para configurar e usar o acesso privilegiado em sua organização do Office 365:</span><span class="sxs-lookup"><span data-stu-id="49867-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="49867-109">Etapa 1: Criar um grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="49867-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="49867-p102">Antes de começar a usar o acesso de privilégio, determine quem terá autoridade de aprovação para solicitações de entrada para acesso a tarefas com privilégios elevados e privilegiados. Qualquer usuário que faz parte do grupo dos aprovadores poderão aprovar solicitações de acesso. Esta opção estiver ativada, criando um grupo de segurança habilitados para email no Office 365.</span><span class="sxs-lookup"><span data-stu-id="49867-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="49867-113">Etapa 2: Habilitar o acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="49867-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="49867-114">Acesso privilegiado deve ser explicitamente ativado no Office 365 com o grupo de aprovador padrão e incluindo um conjunto de contas de sistema que deseja sejam excluídos do controle de acesso de gerenciamento de acesso privilegiado.</span><span class="sxs-lookup"><span data-stu-id="49867-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="49867-115">Etapa 3: Criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="49867-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="49867-p103">Criar uma política de aprovação permite definir os requisitos específicos de aprovação com escopo em tarefas individuais. As opções de tipo de aprovação são **Auto** ou **Manual**.</span><span class="sxs-lookup"><span data-stu-id="49867-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="49867-118">Etapa 4: Enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="49867-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="49867-p104">Uma vez ativado, com privilégios de acesso requer aprovações para executar qualquer tarefa que tem uma política de aprovação associados definida. Os usuários que precisam executar tarefas incluídas na uma política de aprovação deve solicitar e receber aprovação de acesso para que as permissões necessárias para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="49867-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="49867-p105">Após a aprovação for concedida, o usuário solicitante pode executar a tarefa pretendida e acesso privilegiado será autorizar e executar a tarefa em nome dos usuários. A aprovação permanecerá válida para os solicitados duração (duração padrão é 4 horas), durante o qual o solicitante pode executar a tarefa pretendida várias vezes. Todas essas execuções são registradas e torná-los disponíveis para auditoria de conformidade e segurança.</span><span class="sxs-lookup"><span data-stu-id="49867-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="49867-p106">Se você quiser usar o PowerShell de gerenciamento do Exchange para habilitar e configurar o acesso privilegiado, siga as etapas em [Connect to Exchange Online PowerShell usando a autenticação multifator](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) para se conectar ao PowerShell do Exchange Online com o Office 365 credenciais. Você não precisará habilitar a autenticação multifator para sua organização do Office 365 usar as etapas para habilitar o acesso privilegiado ao conectar ao PowerShell do Exchange Online. Conexão com a autenticação multifator cria um token de OAuth que é usado pelo acesso privilegiado para assinar suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="49867-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="49867-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="49867-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="49867-128">Etapa 1 - Criar grupo do aprovador</span><span class="sxs-lookup"><span data-stu-id="49867-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="49867-129">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="49867-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="49867-130">No Centro de administração, vá para **grupos** > **Adicionar um grupo**.</span><span class="sxs-lookup"><span data-stu-id="49867-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="49867-131">Selecione o tipo de grupo do **grupo de segurança habilitados para email** e, em seguida, preencha os campos de **nome**, **endereço de email do grupo**e **Descrição** para o novo grupo.</span><span class="sxs-lookup"><span data-stu-id="49867-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="49867-p107">Salve o grupo. Pode levar alguns minutos para que o grupo a ser totalmente configurado e aparecem no Centro de administração do Office 365.</span><span class="sxs-lookup"><span data-stu-id="49867-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="49867-134">Selecione grupo do aprovador novo e selecione **Editar** para adicionar usuários ao grupo.</span><span class="sxs-lookup"><span data-stu-id="49867-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="49867-135">Salve o grupo.</span><span class="sxs-lookup"><span data-stu-id="49867-135">Save the group.</span></span>

<span data-ttu-id="49867-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="49867-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="49867-137">Etapa 2 - habilitar acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="49867-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-138">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-139">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="49867-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="49867-140">No Centro de administração, vá para **Configurações > segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-141">Ative o controle **exigem aprovações para acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="49867-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="49867-142">Atribua um grupo do aprovador que você criou na etapa 1 como o **grupo de aprovadores padrão**.</span><span class="sxs-lookup"><span data-stu-id="49867-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="49867-143">**Salvar** e **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="49867-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-144">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-145">Execute o seguinte comando no PowerShell do Exchange Online para habilitar o acesso privilegiado e atribuir o grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="49867-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="49867-146">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="49867-147">Contas de sistema recurso é disponibilizado garantir que certas automáticos em suas organizações podem trabalhar sem dependência no acesso privilegiado, no entanto, é recomendável que tal exclusões ser excepcionais e devem ser aprovados e auditadas aqueles permitidos regularmente.</span><span class="sxs-lookup"><span data-stu-id="49867-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="49867-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="49867-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="49867-149">Etapa 3: criar uma política de acesso</span><span class="sxs-lookup"><span data-stu-id="49867-149">Step 3 - Create an access policy</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-150">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-150">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-151">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="49867-151">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="49867-152">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-152">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-153">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="49867-153">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="49867-154">Selecione **Configurar políticas** e **Adicionar uma política**.</span><span class="sxs-lookup"><span data-stu-id="49867-154">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="49867-155">Nos campos de lista suspensa, selecione os valores apropriados para sua organização:</span><span class="sxs-lookup"><span data-stu-id="49867-155">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="49867-156">**Tipo de política**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="49867-156">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="49867-157">**Escopo da política**: Exchange ou o Office 365</span><span class="sxs-lookup"><span data-stu-id="49867-157">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="49867-158">**Nome da política**: selecione as diretivas disponíveis</span><span class="sxs-lookup"><span data-stu-id="49867-158">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="49867-159">**Tipo de aprovação**: Manual ou automático</span><span class="sxs-lookup"><span data-stu-id="49867-159">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="49867-160">**Grupo de aprovação**: selecione o grupo de aprovadores criado na etapa 1</span><span class="sxs-lookup"><span data-stu-id="49867-160">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="49867-p108">Selecione **criar** e em seguida **Fechar**. Pode levar alguns minutos para a diretiva a ser totalmente configurada e habilitada.</span><span class="sxs-lookup"><span data-stu-id="49867-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-163">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-163">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-164">Execute o seguinte comando no Exchange Online PowerShell para criar e definir uma política de aprovação:</span><span class="sxs-lookup"><span data-stu-id="49867-164">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="49867-165">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-165">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="49867-166"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="49867-166"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="49867-167">Etapa 4: Enviar/aprovar solicitações de acesso privilegiado</span><span class="sxs-lookup"><span data-stu-id="49867-167">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="49867-168">Autorização de elevação solicitante para executar tarefas com privilégios</span><span class="sxs-lookup"><span data-stu-id="49867-168">Requesting elevation authorization to execute privileged tasks</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-169">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-169">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-170">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="49867-170">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="49867-171">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-172">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="49867-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="49867-p109">Selecione **nova solicitação**. Nos campos de lista suspensa, selecione os valores apropriados para sua organização:</span><span class="sxs-lookup"><span data-stu-id="49867-p109">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="49867-175">**Tipo de solicitação**: tarefa, função ou grupo de função</span><span class="sxs-lookup"><span data-stu-id="49867-175">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="49867-176">**Escopo de solicitação**: Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-176">**Request scope**: Exchange</span></span>

    <span data-ttu-id="49867-177">**Solicitar para**: selecione as diretivas disponíveis</span><span class="sxs-lookup"><span data-stu-id="49867-177">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="49867-178">**Duração (horas)**: número de horas de acesso solicitado</span><span class="sxs-lookup"><span data-stu-id="49867-178">**Duration (hours)**: Number of hours of requested access</span></span>

    <span data-ttu-id="49867-179">**Comentários**: campo de texto para comentários relacionados à sua solicitação de acesso</span><span class="sxs-lookup"><span data-stu-id="49867-179">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="49867-p110">Selecione **Salvar** e **Fechar**. Sua solicitação será enviada ao grupo do aprovador via email.</span><span class="sxs-lookup"><span data-stu-id="49867-p110">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-182">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-182">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-183">Execute o seguinte comando no Exchange Online PowerShell para criar e enviar uma solicitação de aprovação ao grupo do aprovador:</span><span class="sxs-lookup"><span data-stu-id="49867-183">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="49867-184">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-184">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="49867-185">Exibir o status das solicitações de elevação</span><span class="sxs-lookup"><span data-stu-id="49867-185">View status of elevation requests</span></span>
<span data-ttu-id="49867-186">Depois que uma solicitação de aprovação é criada, o status da solicitação de elevação podem ser revisadas no Centro de administração ou no Exchange identificação do PowerShell de gerenciamento usando o associado com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="49867-186">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-187">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-187">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-188">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="49867-188">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="49867-189">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-189">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-190">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="49867-190">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="49867-191">Selecione **Exibir** para filtrar solicitações enviadas por status **pendente**, **aprovado**, **negados**ou **Lockbox do cliente** .</span><span class="sxs-lookup"><span data-stu-id="49867-191">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-192">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-192">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-193">Execute o seguinte comando no Exchange Online PowerShell para exibir o status de uma solicitação de aprovação para uma ID de solicitação específica:</span><span class="sxs-lookup"><span data-stu-id="49867-193">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="49867-194">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-194">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="49867-195">Aprovar uma solicitação de autorização de elevação</span><span class="sxs-lookup"><span data-stu-id="49867-195">Approving an elevation authorization request</span></span>
<span data-ttu-id="49867-p111">Quando uma solicitação de aprovação é criada, os membros do grupo aprovador relevantes receberão uma notificação de e-mail e podem aprovar a solicitação associada com o ID de solicitação. O solicitante será notificado da aprovação de solicitação ou negação via mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="49867-p111">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-198">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-198">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-199">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="49867-199">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="49867-200">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-200">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-201">Selecione **solicitações e gerenciar políticas de acesso**.</span><span class="sxs-lookup"><span data-stu-id="49867-201">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="49867-202">Selecione uma solicitação listada para exibir os detalhes e agir em relação a solicitação.</span><span class="sxs-lookup"><span data-stu-id="49867-202">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="49867-p112">Selecione **Aprovar** para aprovar a solicitação ou selecione **Negar** negar a solicitação. Anteriormente solicitações aprovadas podem ter acesso revogado selecionando **revogar**.</span><span class="sxs-lookup"><span data-stu-id="49867-p112">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-205">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-205">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-206">Execute o seguinte comando no Exchange Online PowerShell para aprovar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="49867-206">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="49867-207">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-207">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="49867-208">Execute o seguinte comando no Exchange Online PowerShell para negar uma solicitação de autorização de elevação:</span><span class="sxs-lookup"><span data-stu-id="49867-208">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="49867-209">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="49867-209">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="49867-210">Desabilitar acesso privilegiado no Office 365</span><span class="sxs-lookup"><span data-stu-id="49867-210">Disable privileged access in Office 365</span></span>

<span data-ttu-id="49867-p113">Se necessário, você pode desativar o gerenciamento de acesso privilegiado para sua organização. Desabilitando privilegiada acesso não exclui quaisquer políticas de aprovação associados ou a grupos de aprovador.</span><span class="sxs-lookup"><span data-stu-id="49867-p113">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="49867-213">Usando o Centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="49867-213">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="49867-214">Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.</span><span class="sxs-lookup"><span data-stu-id="49867-214">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="49867-215">No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.</span><span class="sxs-lookup"><span data-stu-id="49867-215">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="49867-216">Ative o controle **exigem aprovações para acesso privilegiado** .</span><span class="sxs-lookup"><span data-stu-id="49867-216">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="49867-217">Usando o PowerShell de gerenciamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="49867-217">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="49867-218">Execute o seguinte comando no Exchange Online Powershell para desabilitar o acesso privilegiado:</span><span class="sxs-lookup"><span data-stu-id="49867-218">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```