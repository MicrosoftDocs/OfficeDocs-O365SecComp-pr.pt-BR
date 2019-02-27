---
title: Como identificar o tipo de retenção de uma caixa de correio do Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Saiba como identificar os diferentes tipos de retenção que podem ser colocados em uma caixa de correio do Office 365. Esses tipos de isenções incluem retenção de litígio, bloqueios de descoberta eletrônica e políticas de retenção do Office 365. Você também pode determinar se um usuário foi excluído de uma política de retenção em toda a organização
ms.openlocfilehash: 5b9e8437b688a5c1b35726834c3d80d07cc4ba50
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296804"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Como identificar o tipo de retenção de uma caixa de correio do Exchange Online

Este artigo explica como identificar as isenções colocadas nas caixas de correio do Exchange Online no Office 365.

O Office 365 oferece diversas maneiras pelas quais sua organização pode impedir que o conteúdo da caixa de correio seja excluído permanentemente. Isso permite que sua organização retenha o conteúdo para atender regularmente à conformidade ou para a duração de outros tipos de investigações legais. Veja a seguir uma lista dos recursos de retenção (também chamados de *isenções*) no Office 365:

- **Retenção de litígio** -isenções que são aplicadas às caixas de correio do usuário no Exchange Online.

- **bloqueios de descoberta eletrônica** associados a uma ocorrência de descoberta eletrônica no centro de conformidade do _AMP_ de segurança. as suspensões de descoberta eletrônica podem ser aplicadas às caixas de correio do usuário e na caixa de correio correspondente dos grupos do Office 365 e do Microsoft Teams.

- **Bloqueios in-loco** aplicados às caixas de correio do usuário usando a ferramenta de bloqueio de descoberta eletrônica in-loco do & no centro de administração do Exchange no Exchange Online.

- **Política de retenção do office 365** – retém o conteúdo nas caixas de correio do usuário no Exchange Online e na caixa de correio correspondente dos grupos do Office 365 e do Microsoft Teams. Você pode criar uma política de retenção que mantém as conversas do Skype for Business, que são armazenadas nas caixas de correio do usuário.

  Há dois tipos de políticas de retenção do Office 365 que podem ser atribuídos às caixas de correio.

    - **Políticas de retenção de local específico** -essas são as políticas atribuídas aos locais de conteúdo de usuários específicos. Você usa o cmdlet **Get-Mailbox** no PowerShell do Exchange Online para obter informações sobre políticas de retenção atribuídas a caixas de correio específicas.

    - **Políticas de retenção em toda a organização** -são as políticas atribuídas a todos os locais de conteúdo em sua organização. Você usa o cmdlet **Get-OrganizationConfig** no PowerShell do Exchange Online para obter informações sobre políticas de retenção em toda a organização. Para obter mais informações, consulte a seção "aplicando uma política de retenção a uma organização inteira ou locais específicos" em [visão geral das políticas de retenção do Office 365](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Rótulos de retenção do office 365** -se um usuário aplicar um rótulo de retenção do Office 365 (um que esteja configurado para reter conteúdo ou reter e excluir conteúdo) em *qualquer* pasta ou item na caixa de correio, uma retenção será colocada na caixa de correio como se a caixa de correio estivesse colocado em retenção de litígio ou atribuído a uma política de retenção do Office 365. Para obter mais informações, consulte o artigo [identificando caixas de correio em espera porque um rótulo de retenção foi aplicado a uma seção de pasta ou item](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) neste artigo.

Para gerenciar caixas de correio em espera, talvez seja necessário identificar o tipo de retenção colocado em uma caixa de correio para que você possa realizar tarefas como alterar a duração da retenção, remover temporariamente ou permanentemente a retenção ou excluir uma caixa de correio de uma política de retenção do Office 365. Nesses casos, a primeira etapa é identificar o tipo de retenção colocado na caixa de correio. E como várias isenções (e diferentes tipos de isenções) podem ser colocadas em uma única caixa de correio, você precisará identificar todas as isenções colocadas em uma caixa de correio se quiser remover ou alterar essas isenções.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Etapa 1: obter o GUID para isenções colocadas em uma caixa de correio

Você pode executar os dois cmdlets a seguir no PowerShell do Exchange Online para obter o GUID das isenções que são colocadas em uma caixa de correio. Depois de obter um GUID, use-o para identificar o bloqueio específico na etapa 2. Observe que as isenções de litígio não são identificadas por um GUID. A retenção de litígio está habilitada ou desabilitada para uma caixa de correio.

- **Get-Mailbox** -Use este cmdlet para determinar se a retenção de litígio está habilitada para uma caixa de correio e para obter os GUIDs de bloqueios de descoberta eletrônica, bloqueio in-loco e políticas de retenção do Office 365 atribuídas especificamente a uma caixa de correio. A saída desse cmdlet também indica se uma caixa de correio foi explicitamente excluída de uma política de retenção em toda a organização.

- **Get-OrganizationConfig** -Use este cmdlet para obter os GUIDs de políticas de retenção em toda a organização.

Para se conectar ao PowerShell do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Execute o seguinte comando para obter informações sobre as políticas de retenção de isenções e do Office 365 aplicadas a uma caixa de correio.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Se houver muitos valores na propriedade InPlaceHolds e nem todos eles forem exibidos, você poderá executar o `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada GUID em uma linha separada.

A tabela a seguir descreve como identificar diferentes tipos de isenções com base nos valores da propriedade *InPlaceHolds* quando você executa o cmdlet **Get-Mailbox** .


|Tipo de bloqueio  |Valor de exemplo  |Como identificar a isenção  |
|---------|---------|---------|
|Retenção de litígio     |    `True`     |     A retenção de litígio está habilitada para uma caixa ** de correio se a propriedade `True`LitigationHoldEnabled estiver definida como.    |
|retenção de descoberta eletrônica     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   A *Propriedade InPlaceHolds* contém o GUID de qualquer isenção associada a uma ocorrência de descoberta eletrônica no centro de conformidade do _AMP_ de segurança. É possível dizer que esse é um bloqueio de descoberta eletrônica porque o GUID `UniH` começa com o prefixo (que denota uma retenção unificada).      |
|Bloqueio In-loco     |     `c0ba3ce811b6432a8751430937152491` <br/> ou <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     A propriedade *InPlaceHolds* contém o GUID do bloqueio in-loco colocado na caixa de correio. Você pode dizer que isso é um bloqueio in-loco, pois o GUID não começa com um prefixo ou começa com o `cld` prefixo.     |
|Política de retenção do Office 365 aplicada especificamente à caixa de correio     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> ou <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     A propriedade InPlaceHolds contém GUIDs de qualquer política de retenção de local específica que é aplicada à caixa de correio. Você pode identificar as políticas de retenção porque o GUID começa `mbx` com o `skp` ou o prefixo. O `skp` prefixo indica que a política de retenção é aplicada às conversas do Skype for Business na caixa de correio do usuário.    |
|Excluído de uma política de retenção do Office 365 em toda a organização     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Se uma caixa de correio for excluída de uma política de retenção do Office 365 em toda a organização, o GUID da política de retenção para a qual a caixa de correio é excluída `-mbx` é exibida na propriedade InPlaceHolds e é identificado pelo prefixo.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Se a propriedade *InPlaceHolds* estiver vazia quando você executar o cmdlet **Get-Mailbox** , ainda poderá haver uma ou mais políticas de retenção do Office 365 em toda a organização aplicadas à caixa de correio. Execute o seguinte comando no PowerShell do Exchange Online para obter uma lista de GUIDs para as políticas de retenção do Office 365 em toda a organização.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Se houver muitos valores na propriedade InPlaceHolds e nem todos eles forem exibidos, você poderá executar o `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada GUID em uma linha separada.

A tabela a seguir descreve os diferentes tipos de bloqueios de toda a organização e como identificar cada tipo com base nos GUIDs contidos na propriedade *InPlaceHolds* quando você executa o cmdlet **Get-OrganizationConfig** .


|Tipo de bloqueio  |Valor de exemplo  |Descrição  |
|---------|---------|---------|
|Políticas de retenção do Office 365 aplicadas a caixas de correio do Exchange, pastas públicas do Exchange e chats do Microsoft Teams    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Políticas de retenção em toda a organização aplicadas às caixas de correio do Exchange, pastas públicas do Exchange e chats do 1xN no Microsoft Teams são identificadas `mbx` por GUIDs que começam com o prefixo. Observe que os chat do 1xN são armazenados na caixa de correio dos participantes individuais do chat.      |
|Política de retenção do Office 365 aplicada a grupos do Office 365 e mensagens de canal do teams     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Políticas de retenção em toda a organização aplicadas a grupos do Office 365 e mensagens de canal no Microsoft Teams são identificadas por `grp` GUIDs que começam com o prefixo. Observe que as mensagens do canal são armazenadas na caixa de correio de grupo associada a uma equipe da Microsoft.     |

Para obter mais políticas de retenção de informações aplicadas ao Microsoft Teams, consulte a seção "local da equipe" [visão geral das políticas de retenção](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Noções básicas sobre o formato do valor InPlaceHolds para políticas de retenção

Além do prefixo (MBX, SKP ou GRP) que identifica um item na propriedade InPlaceHolds como uma política de retenção do Office 365, o valor também contém um sufixo que identifica o tipo de ação de retenção que é configurado para a política. Por exemplo, o sufixo de ação é realçado em negrito nos seguintes exemplos:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

A tabela a seguir define as três ações de retenção possíveis:

|Valor  |Descrição  |
|---------|---------|
|**1**     | Indica que a política de retenção está configurada para excluir itens; a política não retém itens.        |
|**duas**    |    Indica que a política de retenção está configurada para reter itens; a política não excluirá itens depois que o período de retenção expirar.     |
|**3D**     |   Indica que a política de retenção está configurada para reter itens e excluí-los depois que o período de retenção expira.      |

Para obter mais informações sobre ações de retenção, consulte a seção "retendo conteúdo por um período específico de tempo" em [visão geral das políticas de retenção](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Etapa 2: usar o GUID para identificar a retenção

Depois de obter o GUID de uma retenção aplicada a uma caixa de correio, a próxima etapa é usar esse GUID para identificar a isenção. As seções a seguir mostram como identificar o nome da retenção (e outras informações) usando o GUID de retenção.

### <a name="ediscovery-holds"></a>bloqueios de descoberta eletrônica

Execute os seguintes comandos no Security & Compliance Center PowerShell para identificar uma retenção de descoberta eletrônica aplicada à caixa de correio. Use o GUID (não incluindo o prefixo UniH) para o bloqueio de descoberta eletrônica que você identificou na etapa 1. O primeiro comando cria uma variável que contém informações sobre a retenção; Essa variável é usada em outros comandos. O segundo comando exibe o nome da ocorrência de descoberta eletrônica à qual a retenção está associada. O terceiro comando exibe o nome da retenção e uma lista das caixas de correio às quais o bloqueio se aplica.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Para se conectar ao & de segurança do centro de conformidade do Windows, confira [conectar-se ao PowerShell do centro de conformidade do Office 365 Security &](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>Bloqueio In-loco

Execute o seguinte comando no PowerShell do Exchange Online para identificar o bloqueio in-loco aplicado à caixa de correio. Use o GUID do bloqueio in-loco identificado na etapa 1. O comando exibe o nome da retenção e uma lista das caixas de correio às quais o bloqueio se aplica.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Observe que, se o GUID do bloqueio in-loco começar com o `cld` prefixo, certifique-se de incluir o prefixo ao executar o comando anterior.

### <a name="office-365-retention-policies"></a>Políticas de retenção do Office 365

Execute o seguinte comando no & de segurança do centro de conformidade do Microsoft PowerShell para identificar a política de retenção do Office 365 (local de toda a organização ou específica) que é aplicada à caixa de correio. Use o GUID (sem incluir o prefixo MBX, SKP ou GRP ou o sufixo de ação) identificado na etapa 1.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>Identificando caixas de correio em espera porque um rótulo de retenção foi aplicado a uma pasta ou item

Sempre que um usuário aplica um rótulo de retenção que é configurado para reter conteúdo ou reter e, em seguida, excluir conteúdo para qualquer pasta ou item em suas caixas de correio, a propriedade de caixa de correio *ComplianceTagHoldApplied* é definida como **true**. Quando isso acontece, a caixa de correio é considerada em espera, assim como se foi feita em retenção de litígio ou atribuída a uma política de retenção do Office 365. Quando a propriedade *ComplianceTagHoldApplied* é definida como **true**, as seguintes coisas podem ocorrer:

- Se a caixa de correio ou a conta de usuário do Office 365 do usuário for excluída, a caixa de correio se tornará uma [caixa de correio inativa](inactive-mailboxes-in-office-365.md).
- Você não poderá desabilitar a caixa de correio (a caixa de correio principal ou a caixa de correio de arquivo morto, se ela estiver habilitada).
- Os itens na caixa de correio podem ser mantidos mais tempo do que o esperado. Isso ocorre porque a caixa de correio está em espera e, portanto, nenhum item será excluído permanentemente (limpo).

Para exibir o valor da propriedade *ComplianceTagHoldApplied* , execute o seguinte comando no PowerShell do Exchange Online:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Para obter mais informações sobre rótulos de retenção, consulte [visão geral dos rótulos de retenção do Office 365](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>Gerenciando caixas de correio em espera de atraso

Após qualquer tipo de retenção ser removido de uma caixa de correio, o valor da propriedade de caixa de correio *DelayHoldApplied* é definido como **true**. Isso ocorre na próxima vez que o assistente de pasta gerenciada processa a caixa de correio e detecta que uma retenção foi removida. Isso é chamado de espera de *atraso* e significa que a remoção real da retenção está atrasada por 30 dias para evitar que os dados sejam excluídos permanentemente (removidos) da caixa de correio. Isso dá aos administradores uma oportunidade de Pesquisar ou recuperar itens de caixa de correio que serão removidos após a retenção ser realmente removida. Quando um atraso de espera é colocado na caixa de correio, a caixa de correio ainda é considerada em espera por uma duração ilimitada, como se a caixa de correio estivesse em retenção de litígio. Após 30 dias, o atraso esperado expira e o Office 365 tentará automaticamente remover o atraso de espera (definindo a propriedade *DelayHoldApplied* como **false**) para que a retenção seja realmente removida. Após a propriedade *DelayHoldApplied* como **false**, os itens marcados para remoção serão removidos na próxima vez que a caixa de correio for processada pelo assistente de pasta gerenciada.

Para exibir o valor da propriedade *DelayHoldApplied* de uma caixa de correio, execute o seguinte comando no PowerShell do Exchange Online.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Para remover o atraso antes da expiração, você pode executar o seguinte comando no PowerShell do Exchange Online: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Observe que você deve receber a função de retenção legal no Exchange Online para usar o parâmetro *RemoveDelayHoldApplied* 

Para remover o atraso de espera em uma caixa de correio inativa, execute o seguinte comando no PowerShell do Exchange Online:

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> A melhor maneira de especificar uma caixa de correio inativa no comando anterior é usar seu nome distinto ou valor de GUID do Exchange. O uso de um desses valores ajuda a evitar a especificação acidental da caixa de correio errada. 

## <a name="next-steps"></a>Próximas etapas

Após identificar as isenções aplicadas a uma caixa de correio, você pode executar tarefas como alterar a duração da retenção, remover temporariamente ou permanentemente a retenção ou, no caso das políticas de retenção do Office 365, excluindo uma caixa de correio inativa da política. Para obter mais informações sobre a execução de tarefas relacionadas a isenções, consulte um dos seguintes tópicos:

- Execute o comando [set-RetentionCompliancePolicy- \<AddExchangeLocationException User mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) no PowerShell do centro de conformidade do & de segurança para excluir uma caixa de correio de uma política de retenção do Office 365 em toda a organização. Observe que esse comando só pode ser usado para políticas de retenção onde o valor da propriedade *ExchangeLocation* é `All`igual a.

- Execute o [GUID de retenção Set- \<Mailbox-ExcludeFromOrgHolds sem prefixo ou comando suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) no PowerShell do Exchange Online para excluir uma caixa de correio inativa de uma política de retenção do Office 365 em toda a organização.

- [Alterar a duração da retenção para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md)

- [Excluir itens na pasta de Itens recuperáveis de caixas de correio baseadas em nuvem em retenção](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
