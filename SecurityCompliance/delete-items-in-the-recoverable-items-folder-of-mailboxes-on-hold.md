---
title: Excluir itens na pasta itens recuperáveis de caixas de correio baseadas em nuvem em espera - ajuda de Admin
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Para administradores: excluir itens na pasta de itens recuperáveis de um usuário para uma caixa de correio Exchange Online, mesmo se essa caixa de correio é colocada em retenção legal. Essa é uma maneira eficaz para excluir dados que é acidentalmente sido derramados no Office 365.'
ms.openlocfilehash: a10965ad088da98b4e4d84d823c124e5b192d505
ms.sourcegitcommit: b164d4af65709133e0b512a4327a70fae13a974d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25577080"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>Excluir itens na pasta itens recuperáveis de caixas de correio baseadas em nuvem em espera - ajuda de Admin

A pasta itens recuperáveis para uma caixa de correio do Exchange Online existe para proteger contra exclusões acidentais ou mal-intencionados. Ele também é usado para armazenar itens que são mantidos e acessados pelos recursos de conformidade do Office 365, como isenções e descoberta eletrônica pesquisas. No entanto, em determinadas situações, as organizações podem ter sido acidentalmente mantido na pasta itens recuperáveis que eles devem excluir dados. Por exemplo, um usuário pode enviar ou encaminhar uma mensagem de email que contém informações confidenciais ou informações que podem ter consequências de negócios sérios inconscientemente. Mesmo que a mensagem é excluída permanentemente, ele pode mantido indefinidamente porque uma retenção legal foi colocada na caixa de correio. Este cenário é conhecido como algum derramamento de dados porque os dados foram derramou acidentalmente ao Office 365. Nesses casos, você pode excluir itens na pasta de itens recuperáveis de um usuário para uma caixa de correio Exchange Online, mesmo se essa caixa de correio é colocada em espera com um dos recursos de retenção diferente no Office 365. Esses tipos de isenções incluem retenções de litígio, retenções locais, isenções de descoberta eletrônica e políticas de retenção do Office 365 criadas no Office 365 Security &amp; Centro de conformidade. 
  
 Este artigo explica como excluir itens da pasta itens recuperáveis para caixas de correio baseadas em nuvem que estiverem em espera. Esse procedimento envolve desabilitando o acesso à caixa de correio e desabilitar a recuperação de item único, desabilitando o Assistente de pasta gerenciada da caixa de correio de processamento, removendo temporariamente a retenção, excluindo itens da pasta itens recuperáveis e, então, revertendo a caixa de correio para a configuração anterior. Aqui está o processo: 
  
[Etapa 1: Coletar informações sobre a caixa de correio](#step-1-collect-information-about-the-mailbox)

[Etapa 2: Preparar a caixa de correio](#step-2-prepare-the-mailbox)

[Etapa 3: Remova todas as isenções da caixa de correio](#step-3-remove-all-holds-from-the-mailbox)

[Etapa 4: Remover a retenção de atraso da caixa de correio](#step-4-remove-the-delay-hold-from-the-mailbox)

[Etapa 5: Excluir itens na pasta itens recuperáveis](#step-5-delete-items-in-the-recoverable-items-folder)

[Etapa 6: Reverter a caixa de correio ao estado anterior](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> Os procedimentos descritos neste artigo resultará em dados sendo permanentemente excluídos (purgados) de uma caixa de correio do Exchange Online. Isso significa que as mensagens que você exclua da pasta itens recuperáveis não podem ser recuperadas e não estarão disponíveis para descoberta legal ou outras finalidades de conformidade. Se você deseja excluir mensagens de uma caixa de correio é colocada em espera como parte de um litígio, bloqueio In-loco, retenção de descoberta eletrônica, ou política de retenção do Office 365 criados na segurança do Office 365 &amp; Centro de conformidade, a seleção com o gerenciamento de registros ou o departamento jurídico departamentos antes de remover o bloqueio. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de algum derramamento de dados tem prioridade. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser atribuído ambas as seguintes funções de gerenciamento no Exchange Online para pesquisar e excluir mensagens da pasta itens recuperáveis na etapa 5.
    
  - **Pesquisa de caixa de correio** - essa função permite que você para pesquisar caixas de correio em sua organização. Os administradores do Exchange não estão atribuídos a essa função por padrão. Para atribuir a mesmo essa função, adicione si mesmo como membro do grupo de funções de gerenciamento de descoberta no Exchange Online. 
    
  - **Caixa de correio importar e exportar** - essa função permite que você para excluir mensagens da caixa de correio do usuário. Por padrão, essa função não é atribuída a qualquer grupo de funções. Para excluir mensagens de caixas de correio dos usuários, você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento de organização no Exchange Online. 
    
- Caixas de correio inativas não é compatível com o procedimento descrito neste artigo. Isso acontece porque você não é possível aplicar novamente uma espera (ou a política de retenção do Office 365) para uma caixa de correio inativa depois que você removê-lo. Quando você remove uma isenção de uma caixa de correio inativa, ela é alterada para uma caixa de correio normal excluída e serão permanentemente excluída da sua organização depois que ele é processado pelo Assistente de pasta gerenciada.
    
- Você não pode executar este procedimento para uma caixa de correio que tenha sido atribuída a uma política de retenção do Office 365 foi bloqueado com um bloqueio de preservação. Isso acontece porque um bloqueio preservação impede que você removendo ou excluindo a caixa de correio da diretiva de retenção do Office 365 e desabilitem o Assistente de pasta gerenciada na caixa de correio. Para obter mais informações sobre o bloqueio de políticas de retenção, consulte [bloqueio de uma política de retenção](retention-policies.md#locking-a-retention-policy).
    
- Se uma caixa de correio não será colocada em espera (ou não tem a recuperação de item único habilitada), você pode simplesmente excluir os itens da pasta itens recuperáveis. Para obter mais informações sobre como fazer isso, consulte [Procurar e excluir mensagens ](https://go.microsoft.com/fwlink/?linkid=852453).
  
## <a name="step-1-collect-information-about-the-mailbox"></a>Etapa 1: Coletar informações sobre a caixa de correio

Essa primeira etapa é coletar propriedades selecionadas da caixa de correio de destino que afetarão a esse procedimento. Certifique-se de anotar essas configurações ou salvá-los em um arquivo de texto, porque você irá alterar algumas dessas propriedades e, em seguida, reverter para os valores originais na etapa 6, depois que você excluir itens da pasta itens recuperáveis. Aqui está uma lista das propriedades de caixa de correio que você precisa coletar.
  
-  *SingleItemRecoveryEnabled* e *RetainDeletedItemsFor* ; Se necessário, você desabilitar a recuperação única e aumentar o período de retenção de itens excluídos na etapa 3. 
    
-  *LitigationHoldEnabled* e *InPlaceHolds* ; Você precisa identificar todos os bloqueios colocados na caixa de correio, para que possa removê-los temporariamente na etapa 3. Consulte a seção de [informações adicionais](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) para obter dicas sobre como identificar a retenção de tipo pode ser colocada em uma caixa de correio. 
    
Além disso, você precisará fazer a caixa de correio configurações acesso para cliente, portanto, você pode desabilitá-los temporariamente para que o proprietário (ou outros usuários) não possam acessar a caixa de correio durante esse procedimento. Finalmente, você pode obter o tamanho atual e o número de itens na pasta itens recuperáveis. Depois que você excluir itens na pasta itens recuperáveis na etapa 5, você vai usar essas informações para verificar se os itens foram removidos realmente.
  
1. [Conecte-se para o Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Certifique-se de usar um nome de usuário e senha para uma conta de administrador que tenha sido atribuída as funções de gerenciamento apropriado no Exchange Online. 
    
2. Execute o seguinte comando para obter mais informações sobre a recuperação de item único e o período de retenção de item excluído.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   Se a recuperação de item único está habilitada, você terá desabilitá-lo na etapa 2. Se o período de retenção de item excluído não é definido por 30 dias (o valor máximo no Exchange Online), e em seguida, você pode aumentá-lo na etapa 2. 
    
3. Execute o seguinte comando para obter configurações de acesso da caixa de correio de caixa de correio. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   Você irá desabilitar todos esses métodos de acesso na etapa 2.
    
4. Execute o seguinte comando para obter mais informações sobre o Office 365 políticas de retenção aplicadas à caixa de correio e isenções.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > Se há muitos valores na propriedade *InPlaceHolds* e nem todos eles são exibidos, poderá executar o `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada valor em uma linha separada. 
  
5. Execute o seguinte comando para obter informações sobre quaisquer políticas de retenção do Office 365 de toda a organização. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   Se sua organização tiver quaisquer políticas de retenção do Office 365 de toda a organização, você terá que excluir a caixa de correio dessas políticas na etapa 3.

   > [!TIP]
    > Se há muitos valores na propriedade *InPlaceHolds* e nem todos eles são exibidos, poderá executar o `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` comando para exibir cada valor em uma linha separada. 
  
6. Execute o seguinte comando para obter o tamanho atual e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio principal do usuário. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Se a caixa de correio de arquivo morto do usuário estiver habilitada, execute o seguinte comando para obter o tamanho e o número total de itens em pastas e subpastas na pasta itens recuperáveis em suas caixas de correio de arquivo morto. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Quando você excluir itens na etapa 5, você pode optar por excluir ou não excluir itens na pasta itens recuperáveis na caixa de correio de arquivo morto principal do usuário. Observe que, se a expansão automática de arquivamento estiver habilitado para a caixa de correio, itens em uma caixa de correio de arquivo morto auxiliar não serão excluídos.
  
## <a name="step-2-prepare-the-mailbox"></a>Etapa 2: Preparar a caixa de correio

Depois de coletar e o salvamento de informações sobre a caixa de correio, a próxima etapa é preparar a caixa de correio, executando as seguintes tarefas: 
  
- **Desabilitar o acesso do cliente à caixa de correio** para que o proprietário da caixa de correio não pode acessar suas caixas de correio e faça as alterações nos dados de caixa de correio durante esse procedimento. 
    
- **Aumentar o período de retenção de itens excluídos** para 30 dias (o valor máximo no Exchange Online) para que os itens não são removidos da pasta itens recuperáveis antes de excluí-los na etapa 5. 
    
- **Desabilitar a recuperação de Item única** para os itens que não serão mantidas (por toda a duração do período de retenção de item excluído) após a exclusão da pasta itens recuperáveis na etapa 5. 
    
- **Desativar o Assistente de pasta gerenciada** para que ele não processar a caixa de correio e manter os itens que você excluir na etapa 5. 
    
Execute as seguintes etapas no PowerShell do Exchange Online.
  
1. Execute o seguinte comando para desabilitar todo o acesso de cliente à caixa de correio. A sintaxe do comando pressupõe que todos os métodos de acesso do cliente foram habilitados na caixa de correio.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > Ela pode levar até 60 minutos para desabilitar todos os métodos de acesso do cliente à caixa de correio. Observe que desabilitar esses métodos de acesso não desconectar o proprietário da caixa de correio que eles tiver entrados no momento. Se o proprietário não estiver conectado, eles não será capazes de acessar suas caixas de correio depois desses métodos de acesso estão desabilitados. 
  
2. Execute o seguinte comando para aumentar o período de retenção de itens excluídos o número máximo de 30 dias. Pressupõe que a configuração atual é menor que 30 dias. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. Execute o seguinte comando para desabilitar a recuperação de item único.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > Ela pode levar até 60 minutos para desabilitar a recuperação de item único. Não exclua os itens na pasta itens recuperáveis até que esse período tiver expirado. 
  
4. Execute o seguinte comando para impedir o Assistente de pasta gerenciada de processamento da caixa de correio. Conforme explicado anteriormente, é possível desabilitar Assistente de pasta gerenciada somente se uma política de retenção do Office 365 com um bloqueio preservação não é aplicada à caixa de correio. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>Etapa 3: Remova todas as isenções da caixa de correio

A última etapa antes de excluir itens da pasta itens recuperáveis é remover todas as isenções (que você identificou na etapa 1) colocadas na caixa de correio. Todas as isenções devem ser removidas para que os itens não serão mantidas após a exclusão da pasta itens recuperáveis. As seções a seguir contêm informações sobre como remover tipos diferentes de isenções em uma caixa de correio. Consulte a seção de [informações adicionais](#more-information) para obter dicas sobre como identificar a retenção de tipo pode ser colocada em uma caixa de correio. Para obter informações adicionais, consulte [como identificar o tipo de bloqueio colocado em uma caixa de correio do Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).
  
> [!CAUTION]
> Conforme indicado anteriormente, consulte o gerenciamento de registros ou departamentos legais antes de remover uma isenção de uma caixa de correio. 
  
 ### <a name="litigation-hold"></a>Retenção de litígio
  
Execute o seguinte comando no Exchange Online PowerShell para remover um litígio da caixa de correio.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> Semelhante ao desabilitando os métodos de acesso do cliente e a recuperação de item único, ele pode levar até 60 minutos para remover a retenção de litígio. Não exclua itens da pasta itens recuperáveis até que esse período tiver expirado. 
  
 ### <a name="in-place-hold"></a>Bloqueio In-loco
  
Execute o seguinte comando no Exchange Online PowerShell para identificar o bloqueio In-loco que é colocado na caixa de correio. Use o GUID para o bloqueio In-loco que você identificou na etapa 1. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
Depois de identificar o bloqueio In-loco, você pode usar o Centro de administração do Exchange (EAC) ou PowerShell do Exchange Online para remover a caixa de correio de isenção. Para obter mais informações, consulte [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>Políticas do Office 365 retenção aplicadas a caixas de correio específicas
  
Execute o seguinte comando [a segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/?linkid=627084) para identificar a política de retenção do Office 365 que é aplicada à caixa de correio. Usar o GUID (não incluindo o `mbx` ou `skp` prefixo) para a política de retenção que você identificou na etapa 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
Depois de identificar a política de retenção, vá para a **governança de data** \> página de **retenção** na segurança &amp; Centro de conformidade, edite a política de retenção que você identificou na etapa anterior e remover a caixa de correio da lista de destinatários incluídos na política de retenção. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>Políticas de retenção do Office 365 de toda a organização
  
Toda a organização e as políticas de retenção de todo o Exchange Office 365 são aplicadas a cada caixa de correio na organização. Eles são aplicados no nível da organização (não o nível de caixa de correio) e são retornados quando você executa o cmdlet **Get-OrganizationConfig** na etapa 1. Execute o seguinte comando [segurança &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/?linkid=627084) para identificar as políticas de retenção do Office 365 de toda a organização. Usar o GUID (não incluindo o `mbx` prefixo) para as políticas de retenção de toda a organização que você identificou na etapa 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

Depois de identificar as políticas de retenção do Office 365 de toda a organização, vá para a **governança de data** \> página **retenção** de segurança &amp; Centro de conformidade, edite cada política de retenção de toda a organização que você identificou no anterior etapa e adicione a caixa de correio à lista de destinatários excluídos. Fazer isso removerá da caixa de correio do usuário a política de retenção. 

### <a name="office-365-retention-labels"></a>Rótulos de retenção do Office 365

Sempre que um usuário aplica um rótulo que está configurado para reter o conteúdo ou manter e excluir conteúdo para qualquer pasta ou um item em suas caixas de correio, a propriedade de caixa de correio de *ComplianceTagHoldApplied* é definida como **True**. Quando isso acontece, a caixa de correio é considerada como estar em espera, como se ele foi colocado em retenção de litígio ou atribuído a uma política de retenção do Office 365.

Para exibir o valor da propriedade *ComplianceTagHoldApplied* , execute o seguinte comando no PowerShell do Exchange Online:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Depois que você identificou que uma caixa de correio está em espera porque um rótulo de retenção é aplicado a uma pasta ou um item, você pode usar a ferramenta de pesquisa de conteúdo na segurança & Centro de conformidade para procurar itens de rotulado usando a condição de pesquisa ComplianceTag. Para obter mais informações, consulte a seção "Critérios de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md#conditions-for-common-properties).

Para obter mais informações sobre rótulos, consulte [Visão geral do Office 365 rótulos](labels.md).

 ### <a name="ediscovery-case-holds"></a>caso de descoberta eletrônica retenções
  
Execute os seguintes comandos [segurança &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/?linkid=627084) para identificar a retenção associada a um caso de eDiscovery que é aplicado à caixa de correio. Usar o GUID (não incluindo o `UniH` prefixo) para o eDiscovery, bloqueio que você identificou na etapa 1. Observe que o segundo comando exibe o nome da isenção é associada a; o caso de descoberta eletrônica o terceiro comando exibe o nome da isenção. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

Depois que você identificou o nome do caso de descoberta eletrônica e isenção, vá para o **pesquisa &amp; investigação** \> página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade, abra a ocorrência e remover a caixa de correio da isenção. Para obter mais informações, consulte [gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](manage-ediscovery-cases.md).
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>Etapa 4: Remover a retenção de atraso da caixa de correio

Depois de qualquer tipo de espera é removido de uma caixa de correio, o valor da propriedade *DelayHoldApplied* caixa de correio é definido como **True**. Isso ocorre na próxima vez em que processa a caixa de correio e detecta que foi removida uma isenção Assistente de pasta gerenciada. Isso é chamado um *atraso de espera* e significa que a remoção real da isenção foi adiada por 30 dias impedir que os dados sejam excluídos permanentemente da caixa de correio. (A finalidade de uma isenção de atraso é dar uma oportunidade para pesquisar ou recuperar itens de caixa de correio que serão removidos após um bloqueio seja removido de admins.)  Quando uma isenção de atraso é colocada na caixa de correio, a caixa de correio é considerada ainda ser em espera por um período ilimitado, como se a caixa de correio estava em suspensão de litígio. Após 30 dias, a retenção de atraso expira, e o Office 365 automaticamente tentar remover a retenção de atraso (definindo a propriedade *DelayHoldApplied* como **False**) para que a suspensão seja removida de fato. 

Antes de excluir itens na etapa 5, você precisa remover a retenção de atraso da caixa de correio. Primeiro, determine se a retenção de atraso será aplicada à caixa de correio executando o seguinte comando no PowerShell do Exchange Online:

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Se o valor da propriedade *DelayHoldApplied* estiver definido como **False**, uma isenção atraso não foi colocada na caixa de correio. Você pode ir para a etapa 5 e excluir itens na pasta itens recuperáveis.

Se o valor da propriedade *DelayHoldApplied* é definido como **True**, execute o seguinte comando para remover a retenção de atraso:

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Observe que você deve ser atribuído a função de retenção Legal no Exchange Online para usar o parâmetro *RemoveDelayHoldApplied* .

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>Etapa 5: Excluir itens na pasta itens recuperáveis

Agora você está pronto para realmente excluir itens na pasta itens recuperáveis usando o cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) no Exchange Online PowerShell. Você tem três opções ao executar o cmdlet **Search-Mailbox** . 
  
- Copie itens para uma caixa de correio de destino antes de excluí-los para que você possa examinar os itens, se necessário, antes de excluí-los.
    
- Copiar itens para uma caixa de correio de destino e excluí-los no mesmo comando.
    
- Exclua itens sem copiá-los para uma caixa de correio de destino. 
    
Observe que os itens na pasta itens recuperáveis na caixa de correio de arquivo morto principal do usuário também será excluída quando você executa o * * Search-Mailbox * * cmdlet. Para impedir isso, você pode incluir a opção *DoNotIncludeArchive* . E conforme indicado anteriormente, se o arquivamento expansão automática está habilitada para a caixa de correio, o * * Search-Mailbox * * cmdlet não excluído itens em uma caixa de correio de arquivo morto auxiliar. Para obter mais informações sobre a expansão automática para arquivamento, consulte [Overview of arquivamento ilimitado no Office 365](unlimited-archiving.md).
  
> [!NOTE]
> Se você incluir uma consulta de pesquisa (usando o parâmetro *SearchQuery* ), o cmdlet **Search-Mailbox** retornará um máximo de 10.000 itens nos resultados da pesquisa. Portanto, se você incluir uma consulta de pesquisa, você pode precisar executar o comando **Search-Mailbox** várias vezes para excluir mais de 10.000 itens. 
  
Os exemplos a seguir mostram a sintaxe de comando para cada uma dessas opções. Esses exemplos usam o `-SearchQuery size>0` valor de parâmetro, que exclui todos os itens de todas as subpastas na pasta itens recuperáveis. Se você precisar excluir apenas os itens que correspondam às condições específicas, você também pode usar o parâmetro *SearchQuery* para especificar outras condições, como o assunto de uma mensagem ou um intervalo de datas. Consulte os [outros exemplos de como usar o parâmetro SearchQuery](#other-examples-of-using-the-searchquery-parameter) abaixo. 
  
### <a name="example-1"></a>Exemplo 1

Este exemplo copia todos os itens na pasta de itens recuperáveis do usuário para uma pasta na caixa de correio de pesquisa de descoberta da sua organização. Isso permite que você examine os itens antes de excluí-los permanentemente.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

No exemplo anterior, não é obrigatório para copiar itens para a caixa de correio de pesquisa de descoberta. Você pode copiar mensagens para qualquer caixa de correio de destino. No entanto, para impedir o acesso aos dados de caixa de correio potencialmente confidenciais, é recomendável copiar mensagens para uma caixa de correio que tem acesso restrito a pessoal autorizado. Por padrão, a acesso à caixa de correio de pesquisa de descoberta padrão é restrito no Exchange aos membros do grupo de funções de gerenciamento de descoberta, Online. 
  
### <a name="example-2"></a>Exemplo 2

Este exemplo copia todos os itens na pasta de itens recuperáveis do usuário para uma pasta na caixa de correio de pesquisa de descoberta da sua organização e, em seguida, exclui os itens da pasta de itens recuperáveis do usuário.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>Exemplo 3

Este exemplo exclui todos os itens na pasta de itens recuperáveis do usuário, sem copiá-los para uma caixa de correio de destino. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>Outros exemplos de como usar o parâmetro SearchQuery

Aqui estão alguns exemplos de como usar o parâmetro *SearchQuery* para localizar mensagens específicas. Se você usar o parâmetro *SearchQuery* para procurar itens específicos, considere a possibilidade de copiar os resultados da pesquisa para uma caixa de correio de destino, para que você possa Revise os resultados de pesquisa e, em seguida, revisá-la se necessário, antes de excluir os resultados de uma pesquisa. 
  
Este exemplo retorna as mensagens que contêm uma frase específica no campo assunto.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

Este exemplo retorna as mensagens que foram enviadas dentro do intervalo de datas especificado.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
Este exemplo retorna as mensagens que foram enviadas para a pessoa especificada.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>Verificar se os itens foram excluídos

Para verificar se você tiver com êxito itens excluídos da pasta itens recuperáveis de uma caixa de correio, use o cmdlet **Get-MailboxFolderStatistics** no Exchange Online PowerShell para verificar se o tamanho e número de itens na pasta itens recuperáveis. Você pode comparar essas estatísticas com os que você coletou na etapa 1. 
  
Execute o seguinte comando para obter o tamanho atual e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio principal do usuário. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
Execute o seguinte comando para obter o tamanho e o número total de itens em pastas e subpastas na pasta itens recuperáveis na caixa de correio de arquivo morto do usuário. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>Etapa 6: Reverter a caixa de correio ao estado anterior

A etapa final é reverter a caixa de correio de volta para a configuração anterior. Isso significa redefinir as propriedades que você alterou na etapa 2 e reaplicação os bloqueios que você removeu na etapa 3. Isso inclui:
  
- Alterando o período de retenção de item excluído de volta ao seu valor anterior. Como alternativa, você pode simplesmente deixar essa definição como 30 dias, o valor máximo no Exchange Online.
    
- Reabilitar a recuperação de Item única.
    
- Habilitar novamente os métodos de acesso do cliente para que o proprietário possa acessar suas caixas de correio.
    
- Novamente, aplicando as políticas de retenção do Office 365 que você removeu e isenções.
    
- Habilitar novamente o Assistente de pasta gerenciada para processar a caixa de correio.
    
> [!IMPORTANT]
> Recomendamos que você aguarde 24 horas após reaplicação uma espera ou o Office 365 política retenção (e verificar se ele está no lugar) antes de você habilitar novamente o Assistente de pasta gerenciada para processar a caixa de correio. 
  
Execute as seguintes etapas (na sequência especificada) no PowerShell do Exchange Online.
  
1. Executar o seguinte comando para alterar o período de retenção de item excluído de volta ao seu valor original. Pressupõe que a configuração anterior é menor que 30 dias; Por exemplo, 14 dias. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. Execute o seguinte comando para reabilitar a recuperação de item único.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. Execute o seguinte comando para reabilitar a todos os métodos de acesso do cliente à caixa de correio.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. Reaplicar os bloqueios que você removeu na etapa 3. Dependendo do tipo de espera, use um dos seguintes procedimentos.
    
    **Retenção de litígio**
    
    Execute o seguinte comando para reabilitar um litígio da caixa de correio.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **In-Place Hold**
    
    Use o EAT (ou PowerShell do Exchange Online) para adicionar a caixa de correio de volta para o bloqueio In-loco. 
    
    **Políticas do Office 365 retenção aplicadas a caixas de correio específicas**
    
    Usar a segurança &amp; Centro de conformidade para adicionar a caixa de correio de volta para a política de retenção do Office 365. Vá até a **governança de data** \> página de **retenção** na segurança &amp; Centro de conformidade, editar a política de retenção e adicione a caixa de correio voltar à lista de destinatários a política de retenção aplicada às. 
    
    **Políticas de retenção do Office 365 de toda a organização**
    
    Se você removeu um toda a organização ou a política de retenção de todo o Exchange excluindo-lo da diretiva, em seguida, use a segurança &amp; excluiu de centro de conformidade para remover a caixa de correio da lista de usuários. Vá até a **governança de data** \> página de **retenção** na segurança &amp; Centro de conformidade, edite a política de retenção de toda a organização e remover a caixa de correio da lista de destinatários excluídos. Fazer isso novamente aplicará a diretiva de retenção a caixa de correio do usuário. 
    
    **caso de descoberta eletrônica retenções**
    
    Usar a segurança &amp; Centro de conformidade para adicionar a caixa de correio de volta a retenção que está associado a um caso de eDiscovery. Vá até o **pesquisa &amp; investigação** \> página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade, abra o caso e adicionar caixa de correio de volta à isenção. 
    
5. Execute o seguinte comando para permitir que o Assistente de pasta gerenciada processar a caixa de correio novamente. Conforme anteriormente mencionado, recomendamos que você aguarde 24 horas após reaplicação uma espera ou o Office 365 política retenção (e verificar se ele está no lugar) antes de você habilitar novamente o Assistente de pasta gerenciada. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. Para verificar que a caixa de correio tiver sido revertida para sua configuração anterior, você pode executar os seguintes comandos e compare as configurações para aqueles que você coletou na etapa 1.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>Mais informações

Aqui está uma tabela que descreve como identificar os diferentes tipos de isenções com base nos valores na propriedade *InPlaceHolds* quando você executar os cmdlets **Get-Mailbox** ou **Get-OrganizationConfig** . Para obter informações mais detalhadas, consulte [como identificar o tipo de bloqueio colocado em uma caixa de correio do Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).

Como previamente explicado, você precisa remover todas as isenções e políticas de retenção do Office 365 de uma caixa de correio antes com êxito podem excluir itens na pasta itens recuperáveis. 
  
|**Tipo de bloqueio**|**Valor de exemplo**|**Como identificar a suspensão**|
|:-----|:-----|:-----|
|Retenção de litígio  <br/> | `True` <br/> |A propriedade *LitigationHoldEnabled* estiver definida como `True`.  <br/> |
|Bloqueio In-loco  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |A propriedade *InPlaceHolds* contém o GUID do In-Place Hold é colocado na caixa de correio. Você pode dizer que isso é um bloqueio In-loco, porque o GUID não começa com um prefixo.<br/> Você pode usar o ' Get-MailboxSearch - InPlaceHoldIdentity<hold GUID> | FL' command no PowerShell do Exchange Online para obter mais informações sobre o bloqueio In-loco na caixa de correio.  <br/> |
| Políticas de retenção do Office 365 na segurança &amp; Centro de conformidade aplicadas a caixas de correio específicas  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> ou  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |Quando você executar o cmdlet **Get-Mailbox** , a propriedade *InPlaceHolds* também contém os GUIDs do Office 365 políticas de retenção aplicadas à caixa de correio. Você pode identificar as políticas de retenção porque o GUID começa com a `mbx` prefixo. Observe que, se o GUID da política de retenção começa com a `skp` prefixo, que indica que a política de retenção é aplicada para Skype para conversas de negócios.<br/> A política de retenção da identidade do Office 365 que é aplicada à caixa de correio, execute o seguinte comando na segurança &amp; PowerShell do Centro de conformidade: <br/> <br/>' Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nome de FL`<br/><br/>Be sure to remove the  `mbx` or  `skp' prefix quando você executar esse comando.  <br/> |
|Políticas de retenção do Office 365 toda a organização na segurança &amp; Centro de conformidade  <br/> |Nenhum valor  <br/> ou  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(indica que a caixa de correio é excluída de uma política de toda a organização)  <br/> |Mesmo se a propriedade *InPlaceHolds* estiver vazia, quando você executar o cmdlet **Get-Mailbox** , ainda pode haver um ou mais toda a organização Office 365 políticas de retenção aplicadas à caixa de correio.  <br/> Para verificar isso, você pode executar o ' Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nome de FL`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `- mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696' <br/> |
|retenção de caso de descoberta eletrônica na segurança &amp; Centro de conformidade  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |A propriedade *InPlaceHolds* também contém o GUID do qualquer espera associado a um caso de eDiscovery na segurança &amp; Centro de conformidade pode ser colocada na caixa de correio. Você pode dizer que isso é uma espera de casos de eDiscovery, porque o GUID começa com a `UniH` prefixo.<br/> Você pode usar o `Get-CaseHoldPolicy` cmdlet em Security &amp; PowerShell do Centro de conformidade para obter mais informações sobre o caso de eDiscovery que o bloqueio na caixa de correio está associado. Por exemplo, você pode executar o comando ' Get-CaseHoldPolicy<hold GUID without prefix> | Nome de FL` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/>`$CaseHold.CaseId Get-ComplianceCase | Nome de FL'


