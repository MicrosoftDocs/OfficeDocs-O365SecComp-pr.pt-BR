---
title: Como identificar o tipo de retenção de uma caixa de correio do Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Aprenda a identificar os diferentes tipos de espera que pode ser colocado em uma caixa de correio do Office 365. Esses tipos de isenções incluem litígio, isenções de descoberta eletrônica e políticas de retenção do Office 365. Você também pode determinar se um usuário uma política de retenção de toda a organização foram excluído
ms.openlocfilehash: 1572b34d3f9abef2fb922fc9b01d1f5a27fcdf7b
ms.sourcegitcommit: e4ebef6aaf756eefb86c9f3a602cf75f5d344271
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026508"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Como identificar o tipo de retenção de uma caixa de correio do Exchange Online

Este artigo explica como identificar isenções colocadas em caixas de correio Exchange Online no Office 365.

O Office 365 oferece diversas maneiras de se sua organização pode impedir que o conteúdo de caixa de correio sejam excluídas permanentemente. Isso permite que sua organização reter o conteúdo para atender aos mais problemáticos de conformidade ou para a duração do departamento jurídico ou de outros tipos de investigações. Aqui está uma lista dos recursos de retenção (também chamado *retém*) no Office 365:

- **Litígio** - isenções que são aplicadas a caixas de correio do usuário no Exchange Online.

- **Mantenha a descoberta eletrônica** - isenções que estão associados um caso de descoberta eletrônica no Centro de conformidade & segurança. isenções de descoberta eletrônica podem ser aplicadas a caixas de correio do usuário e na caixa de correio correspondente para o Office 365 grupos e Teams da Microsoft.

- **In-Place Hold** - isenções que são aplicadas a caixas de correio de usuário usando a ferramenta de espera & descoberta eletrônica In-loco na administração do Exchange center no Exchange Online.

- **Política de retenção do office 365** - retém o conteúdo em caixas de correio do usuário no Exchange Online e na caixa de correio correspondente para o Office 365 grupos e Teams da Microsoft. Você pode criar uma retenção política mantém Skype para conversas de negócios, que são armazenadas em caixas de correio do usuário.

  Há dois tipos de políticas de retenção do Office 365 que podem ser atribuídas a caixas de correio.

    - **Políticas de retenção local específico** - essas são as diretivas que foram atribuídas aos locais de conteúdo de usuários específicos. Você pode usar o cmdlet **Get-Mailbox** no PowerShell do Exchange Online para obter informações sobre as políticas de retenção atribuídos a caixas de correio específicas.

    - **Políticas de retenção de toda a organização** - essas são as políticas que são atribuídas a todos os locais de conteúdo na sua organização. Você pode usar o cmdlet **Get-OrganizationConfig** no PowerShell do Exchange Online para obter informações sobre as políticas de retenção de toda a organização. Para obter mais informações, consulte a seção "Aplicando uma política de retenção para toda a organização ou locais específicos" em [políticas de retenção de visão geral do Office 365](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Rótulos de retenção do office 365** - se um usuário aplica um rótulo de retenção do Office 365 (aquele que está configurado para reter o conteúdo ou manter e excluir conteúdo) para *qualquer* pasta ou item em suas caixas de correio, uma isenção é colocado na caixa de correio, como se fosse a caixa de correio colocado em retenção de litígio ou atribuído a uma política de retenção do Office 365. Para obter mais informações, consulte a seção [identificando a caixas de correio em espera porque um rótulo de retenção tiver sido aplicado a uma pasta ou item](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) neste artigo.

Para gerenciar caixas de correio em espera, você precisa identificar o tipo de espera é colocada em uma caixa de correio, para que você possa realizar tarefas como alterar a duração de espera, temporária ou permanentemente a remoção de retenção ou excluindo uma caixa de correio de uma política de retenção do Office 365. Nesses casos, a primeira etapa é identificar o tipo de bloqueio colocado na caixa de correio. E porque vários bloqueios (e tipos diferentes de isenções) podem ser colocados em uma única caixa de correio, você vai ter que identifique todas as isenções colocadas em uma caixa de correio se você deseja remover ou alterar essas isenções.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Etapa 1: Obter o GUID de isenções colocados em uma caixa de correio

Você pode executar os cmdlets a seguir no PowerShell do Exchange Online para obter o GUID dos bloqueios são colocadas em uma caixa de correio. Depois de obter um GUID, você pode usá-lo para identificar a retenção específica na etapa 2. Observe que não contém litígio são identificados por um GUID. Isenções de litígio são habilitadas ou desabilitadas para uma caixa de correio.

- **Get-Mailbox** - uso contém esse cmdlet para determinar se a retenção de litígio está habilitada para uma caixa de correio e para obter os GUIDs de eDiscovery, retenções locais e políticas de retenção do Office 365 especificamente atribuídos a uma caixa de correio. A saída desse cmdlet também indicará se uma caixa de correio foram excluída explicitamente uma política de retenção de toda a organização.

- **Get-OrganizationConfig** - Use este cmdlet para obter os GUIDs de políticas de retenção de toda a organização.

Para conectar ao Exchange Online PowerShell, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Execute o seguinte comando para obter mais informações sobre o Office 365 políticas de retenção aplicadas a uma caixa de correio e isenções.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Se há muitos valores na propriedade InPlaceHolds e nem todos eles são exibidos, poderá executar o `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada GUID em uma linha separada.

A tabela a seguir descreve como identificar os diferentes tipos de isenções com base nos valores na propriedade *InPlaceHolds* quando você executa o cmdlet **Get-Mailbox** .


|Tipo de bloqueio  |Valor de exemplo  |Como identificar a suspensão  |
|---------|---------|---------|
|Retenção de litígio     |    `True`     |     Litígio está habilitado para uma caixa de correio se a propriedade *LitigationHoldEnabled* estiver definida como `True`.    |
|retenção de descoberta eletrônica     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   A *propriedade InPlaceHolds* contém o GUID do qualquer espera associado a um caso de descoberta eletrônica no Centro de conformidade & segurança. Você pode dizer que isso é uma espera de descoberta eletrônica, porque o GUID começa com a `UniH` prefixo (que indica um bloqueio unificado).      |
|Bloqueio In-loco     |     `c0ba3ce811b6432a8751430937152491` <br/> ou <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     A propriedade *InPlaceHolds* contém o GUID do In-Place Hold é colocado na caixa de correio. Você pode dizer que isso é um bloqueio In-loco, porque o GUID ou não começa com um prefixo ou ele começa com a `cld` prefixo.     |
|Política de retenção de Office 365 especificamente aplicada à caixa de correio     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> ou <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     A propriedade InPlaceHolds contém os GUIDs de qualquer política de retenção local específico que é aplicado à caixa de correio. Você pode identificar as políticas de retenção porque o GUID começa com a `mbx` ou o `skp` prefixo. O `skp` prefixo indica se a política de retenção é aplicada para Skype para conversas de negócios na caixa de correio do usuário.    |
|Excluídos de uma política de retenção do Office 365 de toda a organização     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Se uma caixa de correio é excluída de uma política de retenção do Office 365 de toda a organização, o GUID para a política de retenção a caixa de correio é excluída da é exibido na propriedade InPlaceHolds e é identificado pelo `-mbx` prefixo.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Se a propriedade *InPlaceHolds* estiver vazia, quando você executar o cmdlet **Get-Mailbox** , ainda pode haver um ou mais toda a organização Office 365 políticas de retenção aplicadas à caixa de correio. Execute o seguinte comando no Exchange Online PowerShell para obter uma lista de GUIDs de políticas de retenção do Office 365 de toda a organização.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Se há muitos valores na propriedade InPlaceHolds e nem todos eles são exibidos, poderá executar o `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada GUID em uma linha separada.

A tabela a seguir descreve os diferentes tipos de armazenamentos de toda a organização e como identificar cada tipo com base nos GUIDs contidos na propriedade *InPlaceHolds* quando você executa o cmdlet **Get-OrganizationConfig** .


|Tipo de bloqueio  |Valor de exemplo  |Descrição  |
|---------|---------|---------|
|As diretivas do Office 365 de retenção aplicada a caixas de correio do Exchange, pastas públicas do Exchange e equipes chats    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Políticas de retenção de toda a organização aplicadas a caixas de correio do Exchange, pastas públicas do Exchange, e chats 1xN no Microsoft Teams são identificados por GUIDs que começam com a `mbx` prefixo. Observe que 1xN chats são armazenadas na caixa de correio dos participantes individuais de bate-papo.      |
|Diretiva do Office 365 retenção aplicada às mensagens de canal de equipes e grupos do Office 365     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Políticas de retenção de toda a organização aplicadas aos grupos do Office 365 e mensagens de canal no Microsoft Teams são identificadas por GUIDs que começam com a `grp` prefixo. Observe que as mensagens de canal são armazenadas na caixa de correio grupo que está associada um Team Microsoft.     |

Mais informações sobre diretivas de retenção aplicadas a Teams da Microsoft, consulte a seção "Local do equipes" [Visão geral das políticas de retenção](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Entendendo o formato do valor InPlaceHolds diretivas de retenção

Além do prefixo (mbx, skp ou grp) que identifica um item na propriedade InPlaceHolds como uma política de retenção do Office 365, o valor também contém um sufixo que identifica o tipo de ação de retenção que está configurado para a política. Por exemplo, o sufixo de ação é realçado em negrito nos exemplos a seguir:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

A tabela a seguir define as três ações de retenção possíveis:

|Valor  |Descrição  |
|---------|---------|
|**1**     | Indica que a política de retenção está configurada para excluir itens; a política não reter itens.        |
|**2**    |    Indica que a política de retenção é configurada para reter itens; a política não excluir itens depois que o período de retenção expira.     |
|**3**     |   Indica que a política de retenção é configurada para reter itens e, em seguida, excluí-los após o período de retenção expira.      |

Para obter mais informações sobre ações de retenção, consulte a seção "Retenção de conteúdo para um período de tempo específico" em [Visão geral das políticas de retenção](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Etapa 2: Usando o GUID para identificar o bloqueio

Depois de obter o GUID de uma isenção que é aplicado a uma caixa de correio, a próxima etapa é usar esse GUID para identificar o bloqueio. As seções a seguir mostram como identificar o nome da isenção (e outras informações) usando a GUID de espera.

### <a name="ediscovery-holds"></a>isenções de descoberta eletrônica

Execute os seguintes comandos em segurança & PowerShell do Centro de conformidade para identificar uma espera de descoberta eletrônica que é aplicada à caixa de correio. Usar o GUID (não incluindo o prefixo UniH) para o eDiscovery espera que você identificou na etapa 1. O primeiro comando cria uma variável que contém informações sobre o bloqueio; Essa variável é usada nos outros comandos. O segundo comando exibe o nome do caso de eDiscovery que isenção está associada. O terceiro comando exibe o nome da isenção e uma lista de isenção aplica-se para as caixas de correio.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Para conectar a segurança & PowerShell do Centro de conformidade, consulte [Connect to Office 365 Security & PowerShell do Centro de conformidade](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>Bloqueio In-loco

Execute o seguinte comando no PowerShell do Exchange Online para identificar o bloqueio In-loco que é aplicado à caixa de correio. Use o GUID para o bloqueio In-loco que você identificou na etapa 1. O comando exibe o nome da isenção e uma lista de isenção aplica-se para as caixas de correio.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Observe que, se o GUID para o bloqueio In-loco começará com o `cld` prefix, certifique-se de incluir o prefixo ao executar o comando anterior.

### <a name="office-365-retention-policies"></a>Políticas de retenção do Office 365

Execute o seguinte comando no PowerShell do Centro de conformidade & segurança à identidade a política de retenção do Office 365 (específica ou de toda a organização local) que é aplicada à caixa de correio. Use o GUID (não incluindo o prefixo mbx, skp ou grp ou o sufixo de ação) que você identificou na etapa 1.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>Identificação de caixas de correio em espera porque um rótulo de retenção tiver sido aplicado a uma pasta ou item

Sempre que um usuário aplica um rótulo de retenção que está configurado para reter o conteúdo ou manter e excluir conteúdo para qualquer pasta ou um item em suas caixas de correio, a propriedade de caixa de correio de *ComplianceTagHoldApplied* é definida como **True**. Quando isso acontece, a caixa de correio é considerada como estar em espera, como se ele foi colocado em retenção de litígio ou atribuído a uma política de retenção do Office 365. Quando a propriedade *ComplianceTagHoldApplied* é definida como **True**, as seguintes ações podem ocorrer:

- Se a caixa de correio ou da conta de usuário do Office 365 do usuário for excluída, a caixa de correio torna-se uma [caixa de correio inativa](inactive-mailboxes-in-office-365.md).
- Você não poderá desabilitar a caixa de correio (caixa de correio primária ou a caixa de correio de arquivo morto, se ele estiver habilitado).
- Itens na caixa de correio podem ser retidos por mais do que o esperado. Isso ocorre porque a caixa de correio estiver em espera e, portanto, não há itens serão permanentemente excluídos (purgados).

Para exibir o valor da propriedade *ComplianceTagHoldApplied* , execute o seguinte comando no PowerShell do Exchange Online:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Para obter mais informações sobre os rótulos de retenção, consulte [Visão geral do Office 365 rótulos de retenção](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>Mantenha a gerenciar caixas de correio em atraso

Depois de qualquer tipo de espera é removido de uma caixa de correio, o valor da propriedade *DelayHoldApplied* caixa de correio é definido como **True**. Isso ocorre na próxima vez em que processa a caixa de correio e detecta que foi removida uma isenção Assistente de pasta gerenciada. Isso é chamado um *atraso de espera* e significa que a remoção real da isenção foi adiada por 30 dias impedir que os dados sejam excluídas permanentemente (purgados) da caixa de correio. Isso admins uma oportunidade para pesquisar ou recuperar itens de caixa de correio que serão removidos após a suspensão seja removida de fato. Quando uma isenção de atraso é colocada na caixa de correio, a caixa de correio é considerada ainda ser em espera por um período ilimitado, como se a caixa de correio estava em suspensão de litígio. Após 30 dias, a retenção de atraso expira, e o Office 365 automaticamente tentar remover a retenção de atraso (definindo a propriedade *DelayHoldApplied* como **False**) para que a suspensão serão realmente removida. Após a propriedade *DelayHoldApplied* como **False**, os itens que estão marcados para remoção vão ser removidos na próxima vez em que a caixa de correio é processada pelo Assistente de pasta gerenciada.

Para exibir o valor da propriedade *DelayHoldApplied* para uma caixa de correio, execute o seguinte comando no PowerShell do Exchange Online.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Para remover a retenção de atraso antes que ela expire, você pode executar o seguinte comando no PowerShell do Exchange Online: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Observe que você deve ser atribuído a função de retenção Legal no Exchange Online para usar o parâmetro *RemoveDelayHoldApplied* 

Para remover a retenção de atraso em uma caixa de correio inativa, execute o seguinte comando no PowerShell do Exchange Online:

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> A melhor maneira de especificar uma caixa de correio inativa no comando anterior é usar seu valor de nome distinto ou o GUID do Exchange. Usar um desses valores ajuda a evitar a acidentalmente especificando a caixa de correio errada. 

## <a name="next-steps"></a>Próximas etapas

Depois de identificar os bloqueios que são aplicados a uma caixa de correio, você pode executar tarefas como alterar a duração da retenção, temporariamente ou remover permanentemente a isenção ou, no caso de políticas de retenção do Office 365, excluindo uma caixa de correio inativa da diretiva. Para obter mais informações sobre a realização de tarefas relacionadas ao isenções, consulte um dos seguintes tópicos:

- Execute o [Set-RetentionCompliancePolicy - AddExchangeLocationException \<caixa de correio do usuário >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) command no PowerShell do Centro de conformidade & segurança para excluir uma caixa de correio de uma política de retenção do Office 365 de toda a organização. Observe que este comando pode apenas ser usado para as políticas de retenção em que o valor da propriedade *ExchangeLocation* é igual a `All`.

- Execute o [Set-Mailbox - ExcludeFromOrgHolds \<mantenha GUID sem o prefixo ou sufixo >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) command no PowerShell do Exchange Online para excluir uma caixa de correio inativa de uma política de retenção do Office 365 de toda a organização.

- [Alterar a duração de espera para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md)

- [Excluir itens na pasta de Itens recuperáveis de caixas de correio baseadas em nuvem em retenção](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
