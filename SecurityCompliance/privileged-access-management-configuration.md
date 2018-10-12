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
ms.openlocfilehash: 13d278c8e8555aa069035c2f03b23db69a475b43
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522252"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>Configurando o gerenciamento de acesso privilegiado no Office 365

> [!IMPORTANT]
> Este tópico aborda as diretrizes de implantação e configuração para recursos somente está disponíveis no Office 365 E5 e avançadas SKUs de conformidade.

Este tópico vai orientá-lo por meio de habilitando e configurando o gerenciamento de acesso privilegiado em sua organização do Office 365. Você pode usar o Centro de administração do Microsoft 365 ou o PowerShell de gerenciamento do Exchange para gerenciar e usar acesso privilegiado. 

## <a name="enable-and-configure-privileged-access-management"></a>Habilitar e configurar o gerenciamento de acesso privilegiado

Siga estas etapas para configurar e usar o acesso privilegiado em sua organização do Office 365:

- [Etapa 1: Criar um grupo do aprovador](privileged-access-management-configuration.md#step1)

    Antes de começar a usar o acesso de privilégio, determine quem terá autoridade de aprovação para solicitações de entrada para acesso a tarefas com privilégios elevados e privilegiados. Qualquer usuário que faz parte do grupo dos aprovadores poderão aprovar solicitações de acesso. Esta opção estiver ativada, criando um grupo de segurança habilitados para email no Office 365.

- [Etapa 2: Habilitar o acesso privilegiado](privileged-access-management-configuration.md#step2)

    Acesso privilegiado deve ser explicitamente ativado no Office 365 com o grupo de aprovador padrão e incluindo um conjunto de contas de sistema que deseja sejam excluídos do controle de acesso de gerenciamento de acesso privilegiado.

- [Etapa 3: Criar uma política de acesso](privileged-access-management-configuration.md#step3)

    Criar uma política de aprovação permite definir os requisitos específicos de aprovação com escopo em tarefas individuais. As opções de tipo de aprovação são **Auto** ou **Manual**.

- [Etapa 4: Enviar/aprovar solicitações de acesso privilegiado](privileged-access-management-configuration.md#step4)

    Uma vez ativado, com privilégios de acesso requer aprovações para executar qualquer tarefa que tem uma política de aprovação associados definida. Os usuários que precisam executar tarefas incluídas na uma política de aprovação deve solicitar e receber aprovação de acesso para que as permissões necessárias para executar a tarefa.

Após a aprovação for concedida, o usuário solicitante pode executar a tarefa pretendida e acesso privilegiado será autorizar e executar a tarefa em nome dos usuários. A aprovação permanecerá válida para os solicitados duração (duração padrão é 4 horas), durante o qual o solicitante pode executar a tarefa pretendida várias vezes. Todas essas execuções são registradas e torná-los disponíveis para auditoria de conformidade e segurança. 

> [!NOTE]
> Se você quiser usar o PowerShell de gerenciamento do Exchange para habilitar e configurar o acesso privilegiado, siga as etapas em [Connect to Exchange Online PowerShell usando a autenticação multifator](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) para se conectar ao PowerShell do Exchange Online com o Office 365 credenciais. Você não precisará habilitar a autenticação multifator para sua organização do Office 365 usar as etapas para habilitar o acesso privilegiado ao conectar ao PowerShell do Exchange Online. Conexão com a autenticação multifator cria um token de OAuth que é usado pelo acesso privilegiado para assinar suas solicitações.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Etapa 1 - Criar grupo do aprovador

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.

2. No Centro de administração, vá para **grupos** > **Adicionar um grupo**.

3. Selecione o tipo de grupo do **grupo de segurança habilitados para email** e, em seguida, preencha os campos de **nome**, **endereço de email do grupo**e **Descrição** para o novo grupo.

4. Salve o grupo. Pode levar alguns minutos para que o grupo a ser totalmente configurado e aparecem no Centro de administração do Office 365.

5. Selecione grupo do aprovador novo e selecione **Editar** para adicionar usuários ao grupo.

6. Salve o grupo.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Etapa 2 - habilitar acesso privilegiado

### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.

2. No Centro de administração, vá para **Configurações > segurança e privacidade** > **acesso privilegiado**.

3. Ative o controle **exigem aprovações para acesso privilegiado** .

4. Atribua um grupo do aprovador que você criou na etapa 1 como o **grupo de aprovadores padrão**.

5. **Salvar** e **Fechar**.

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
> Contas de sistema recurso é disponibilizado garantir que certas automáticos em suas organizações podem trabalhar sem dependência no acesso privilegiado, no entanto, é recomendável que tal exclusões ser excepcionais e devem ser aprovados e auditadas aqueles permitidos regularmente.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Etapa 3: criar uma política de acesso

Você pode criar e configurar políticas de acesso privilegiado até 30 para sua organização do Office 365.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Selecione **solicitações e gerenciar políticas de acesso**.

4. Selecione **Configurar políticas** e **Adicionar uma política**.

5. Nos campos de lista suspensa, selecione os valores apropriados para sua organização:
    
    **Tipo de política**: tarefa, função ou grupo de função

    **Escopo da política**: Exchange ou o Office 365

    **Nome da política**: selecione as diretivas disponíveis

    **Tipo de aprovação**: Manual ou automático

    **Grupo de aprovação**: selecione o grupo de aprovadores criado na etapa 1

6. Selecione **criar** e em seguida **Fechar**. Pode levar alguns minutos para a diretiva a ser totalmente configurada e habilitada.

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online PowerShell para criar e definir uma política de aprovação:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Exemplo:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Etapa 4: Enviar/aprovar solicitações de acesso privilegiado

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Autorização de elevação solicitante para executar tarefas com privilégios

Solicitações de acesso privilegiado são válidas por até 24 horas depois que a solicitação é enviada. Se não aprovadas ou negadas, as solicitações expiram e acesso não for aprovado.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Selecione **solicitações e gerenciar políticas de acesso**.

4. Selecione **nova solicitação**. Nos campos de lista suspensa, selecione os valores apropriados para sua organização:

    **Tipo de solicitação**: tarefa, função ou grupo de função

    **Escopo de solicitação**: Exchange

    **Solicitar para**: selecione as diretivas disponíveis

    **Duração (horas)**: número de horas de acesso solicitado. Não há um limite no número de horas que podem ser solicitados.

    **Comentários**: campo de texto para comentários relacionados à sua solicitação de acesso

5. Selecione **Salvar** e **Fechar**. Sua solicitação será enviada ao grupo do aprovador via email.

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online PowerShell para criar e enviar uma solicitação de aprovação ao grupo do aprovador:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Exemplo:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Exibir o status das solicitações de elevação
Depois que uma solicitação de aprovação é criada, o status da solicitação de elevação podem ser revisadas no Centro de administração ou no Exchange identificação do PowerShell de gerenciamento usando o associado com a solicitação.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Selecione **solicitações e gerenciar políticas de acesso**.

4. Selecione **Exibir** para filtrar solicitações enviadas por status **pendente**, **aprovado**, **negados**ou **Lockbox do cliente** .

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online PowerShell para exibir o status de uma solicitação de aprovação para uma ID de solicitação específica:
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Exemplo:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>Aprovar uma solicitação de autorização de elevação
Quando uma solicitação de aprovação é criada, os membros do grupo aprovador relevantes receberão uma notificação de e-mail e podem aprovar a solicitação associada com o ID de solicitação. O solicitante será notificado da aprovação de solicitação ou negação via mensagem de email.

#### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando suas credenciais.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Selecione **solicitações e gerenciar políticas de acesso**.

4. Selecione uma solicitação listada para exibir os detalhes e agir em relação a solicitação.

5. Selecione **Aprovar** para aprovar a solicitação ou selecione **Negar** negar a solicitação. Anteriormente solicitações aprovadas podem ter acesso revogado selecionando **revogar**.

#### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online PowerShell para aprovar uma solicitação de autorização de elevação:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Exemplo:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Execute o seguinte comando no Exchange Online PowerShell para negar uma solicitação de autorização de elevação:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Exemplo:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Excluir uma política de acesso privilegiado no Office 365
Você pode excluir uma política de acesso privilegiado se ele não é mais necessária em sua organização.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Selecione **solicitações e gerenciar políticas de acesso**.

4. Selecione **Configurar diretivas**.

5. Selecione a política que você deseja excluir e selecionando **Remover política**.

6. Selecione **Fechar**.

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online Powershell para excluir uma política de acesso privilegiado:

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>Desabilitar acesso privilegiado no Office 365

Se necessário, você pode desativar o gerenciamento de acesso privilegiado para sua organização. Desabilitando privilegiada acesso não exclui quaisquer políticas de aprovação associados ou a grupos de aprovador.

### <a name="using-the-microsoft-365-admin-center"></a>Usando o Centro de administração do Microsoft 365

1. Entrar no [Centro de administração do Microsoft 365](https://portal.office.com) usando credenciais de uma conta de administrador em sua organização.

2. No Centro de administração, vá para **configurações** > **de segurança e privacidade** > **acesso privilegiado**.

3. Ative o controle **exigem aprovações para acesso privilegiado** .

### <a name="using-exchange-management-powershell"></a>Usando o PowerShell de gerenciamento do Exchange

Execute o seguinte comando no Exchange Online Powershell para desabilitar o acesso privilegiado:

```
Disable-ElevatedAccessControl
```