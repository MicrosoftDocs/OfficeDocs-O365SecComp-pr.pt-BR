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
ms.openlocfilehash: af8058ff852bbf290084e42d1f4c72d6fcee0e27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221081"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>ConFigurando o gerenciamento de acesso privilegiado no Office 365

> [!IMPORTANT]
> Este tópico aborda as diretrizes de implantação e configuração dos recursos disponíveis atualmente no Office 365 E5 e nas SKUs de conformidade avançada.

Este tópico irá orientá-lo na habilitação e configuração do gerenciamento de acesso privilegiado na sua organização do Office 365. Você pode usar o centro de administração do Microsoft 365 ou o PowerShell de gerenciamento do Exchange para gerenciar e usar o acesso privilegiado. 

## <a name="enable-and-configure-privileged-access-management"></a>Habilitar e configurar o gerenciamento de acesso privilegiado

Siga estas etapas para configurar e usar o acesso privilegiado na sua organização do Office 365:

- [Etapa 1: criar um grupo do aprovador](privileged-access-management-configuration.md#step1)

    Antes de começar a usar o acesso de privilégio, determine quem terá autoridade de aprovação para solicitações de entrada para acesso a tarefas privilegiadas e privilegiadas. Qualquer usuário que faça parte do grupo aprovadores poderá aprovar as solicitações de acesso. Isso é habilitado através da criação de um grupo de segurança habilitado para email no Office 365.

- [Etapa 2: habilitar o acesso privilegiado](privileged-access-management-configuration.md#step2)

    O acesso privilegiado precisa estar explicitamente ativado no Office 365 com o grupo de aprovadores padrão e incluir um conjunto de contas de sistema que você deseja excluir do controle de acesso de gerenciamento de acesso privilegiado.

- [Etapa 3: criar uma política de acesso](privileged-access-management-configuration.md#step3)

    A criação de uma política de aprovação permite definir os requisitos de aprovação específicos delimitados em tarefas individuais. As opções de tipo de aprovação são **auto** ou **manual**.

- [Etapa 4: enviar/aprovar solicitações de acesso privilegiado](privileged-access-management-configuration.md#step4)

    Uma vez habilitado, o acesso privilegiado requer aprovações para executar qualquer tarefa com uma política de aprovação associada definida. Os usuários que precisam executar tarefas incluídas na política de aprovação devem solicitar e receber aprovação de acesso para ter as permissões necessárias para executar a tarefa.

Depois que a aprovação for concedida, o usuário solicitante poderá executar a tarefa pretendida e o acesso privilegiado autorizará e executará a tarefa no nome dos usuários. A aprovação permanece válida para a duração solicitada (a duração padrão é de 4 horas), durante a qual o solicitante pode executar a tarefa pretendida várias vezes. Todas essas execuções são registradas e disponibilizadas para auditoria de segurança e conformidade. 

> [!NOTE]
> Se você quiser usar o PowerShell de gerenciamento do Exchange para habilitar e configurar o acesso privilegiado, siga as etapas em [conectar ao PowerShell do Exchange Online usando a autenticação](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) multifator para se conectar ao PowerShell do Exchange Online com seu Office 365 las. Você não precisa habilitar a autenticação multifator para sua organização do Office 365 para usar as etapas para habilitar o acesso privilegiado ao se conectar ao PowerShell do Exchange Online. A conexão com a autenticação multifator cria um token OAuth usado pelo acesso privilegiado para assinar suas solicitações.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Etapa 1: criar um grupo do aprovador

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando as credenciais de uma conta de administrador em sua organização.

2. No centro de administração, vá para **grupos** > **Adicionar um grupo**.

3. Selecione o tipo de grupo de **segurança habilitado para email** e preencha os **campos nome**, endereço de **email do grupo**e **Descrição** do novo grupo.

4. Salve o grupo. Pode levar alguns minutos para que o grupo seja totalmente configurado e apareça no centro de administração do Office 365.

5. Selecione o novo grupo do aprovador e selecione **Editar** para adicionar usuários ao grupo.

6. Salve o grupo.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Etapa 2-habilitar o acesso privilegiado

### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando as credenciais de uma conta de administrador em sua organização.

2. No centro de administração, vá para **configurações > segurança & privacidade** > **privilegiada**.

3. Habilitar as **aprovações de controle de acesso privilegiado** .

4. Atribua o grupo do aprovador que você criou na etapa 1 como o **grupo de aprovadoRes padrão**.

5. **Salvar** e **fechar**.

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para habilitar o acesso privilegiado e atribuir o grupo do aprovador:
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
Exemplo:
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> O recurso de contas de sistema é disponibilizado para garantir que determinadas automaçãos em suas organizações possam trabalhar sem dependências de acesso privilegiado, no entanto, é recomendável que essas exclusões sejam excepcionais e que as permitidas sejam aprovadas e auditadas atualizado.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Etapa 3: criar uma política de acesso

Você pode criar e configurar até 30 políticas de acesso privilegiado para sua organização do Office 365.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando as credenciais de uma conta de administrador em sua organização.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Selecione **gerenciar políticas e solicitações de acesso**.

4. Selecione **Configurar políticas** e selecione **Adicionar uma política**.

5. Nos campos suspensos, selecione os valores apropriados para a sua organização:
    
    **Tipo de política**: tarefa, função ou grupo de função

    **Escopo da política**: Exchange ou Office 365

    **Nome da política**: selecione nas políticas disponíveis

    **Tipo de aprovação**: manual ou automática

    **Grupo de aprovação**: selecione o grupo aprovadores criado na etapa 1

6. Selecione **criar** e **fechar**. Pode levar alguns minutos até que a política seja totalmente configurada e habilitada.

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para criar e definir uma política de aprovação:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Exemplo:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Etapa 4: enviar/aprovar solicitações de acesso privilegiado

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Solicitando autorização de elevação para executar tarefas privilegiadas

As solicitações de acesso privilegiado são válidas por até 24 horas após o envio da solicitação. Se não for aprovada ou negada, as solicitações expirarão e o acesso não será aprovado.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Selecione **gerenciar políticas e solicitações de acesso**.

4. Selecione **nova solicitação**. Nos campos suspensos, selecione os valores apropriados para a sua organização:

    **Tipo de solicitação**: tarefa, função ou grupo de função

    **Escopo da solicitação**: Exchange

    **Solicitação de**: selecione nas políticas disponíveis

    **Duração (horas)**: número de horas de acesso solicitado. Não há um limite no número de horas que podem ser solicitadas.

    **Comments**: campo de texto para comentários relacionados à sua solicitação de acesso

5. Selecione **salvar** e **fechar**. Sua solicitação será enviada ao grupo do aprovador por email.

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para criar e enviar uma solicitação de aprovação para o grupo do aprovador:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Exemplo:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Exibir o status das solicitações de elevação
Após a criação de uma solicitação de aprovação, o status da solicitação de elevação poderá ser revisado no centro de administração ou no PowerShell de gerenciamento do Exchange usando o ID de solicitação associado.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Selecione **gerenciar políticas e solicitações de acesso**.

4. Selecione **Exibir** para filtrar solicitações enviadas por status **pendente**, **aprovado**, **negado**ou de lockbox do **cliente** .

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para exibir um status de solicitação de aprovação para uma ID de solicitação específica:
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Exemplo:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>Aprovar uma solicitação de autorização de elevação
Quando uma solicitação de aprovação é criada, os membros do grupo de aprovadores relevantes receberão uma notificação por email e poderão aprovar a solicitação associada ao ID da solicitação. O solicitante será notificado sobre a aprovação da solicitação ou a negação via mensagem de email.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Selecione **gerenciar políticas e solicitações de acesso**.

4. Selecione uma solicitação listada para exibir os detalhes e executar a ação na solicitação.

5. Selecione **aprovar** para aprovar a solicitação ou selecione **negar** para negar a solicitação. As solicitações aprovadas anteriormente podem ter acesso revogado ao **** selecionar revogar.

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para aprovar uma solicitação de autorização de elevação:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Exemplo:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Execute o seguinte comando no PowerShell do Exchange Online para negar uma solicitação de autorização de elevação:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Exemplo:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Excluir uma política de acesso privilegiada no Office 365
Você pode excluir uma política de acesso privilegiado se ela não for mais necessária em sua organização.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando as credenciais de uma conta de administrador em sua organização.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Selecione **gerenciar políticas e solicitações de acesso**.

4. Selecione **Configurar políticas**.

5. Selecione a política que você deseja excluir e, em seguida, selecione **remover política**.

6. Selecione **fechar**.

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para excluir uma política de acesso privilegiada:

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>Desabilitar o acesso privilegiado no Office 365

Se necessário, você pode desabilitar o gerenciamento de acesso privilegiado para sua organização. Desabilitar o acesso privilegiado não exclui nenhuma política de aprovação associada ou grupos de aprovadores.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o centro de administração do Microsoft 365

1. Entre no [centro de administração do Microsoft 365](https://portal.office.com) usando as credenciais de uma conta de administrador em sua organização.

2. No centro de administração, vá para **configurações** > **segurança & privacidade** > **privilegiada**.

3. Habilitar as **aprovações de controle de acesso privilegiado** .

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no PowerShell do Exchange Online para desabilitar o acesso privilegiado:

```
Disable-ElevatedAccessControl
```