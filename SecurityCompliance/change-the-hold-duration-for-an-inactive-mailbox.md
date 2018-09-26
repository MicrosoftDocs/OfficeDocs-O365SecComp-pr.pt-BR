---
title: Alterar a duração de espera para uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Depois que uma caixa de correio do Office 365 é feita inativa, você pode alterar a duração da retenção ou política de retenção do Office 365 atribuído à caixa de correio inativa. A duração de espera define quanto tempo os itens na pasta são mantidos itens recuperáveis.
ms.openlocfilehash: e3d1d6c7ec0311813dfa1144cc960d2fed9e160d
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038054"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a>Alterar a duração de espera para uma caixa de correio inativa no Office 365

Uma caixa de correio inativa é usada para reter o email de um antigo do funcionário depois que ele deixa a sua organização. Uma caixa de correio fica inativa quando um litígio, um bloqueio In-loco, uma política de retenção do Office 365, ou uma isenção que está associado a um caso de eDiscovery é colocada na caixa de correio e a conta de usuário do Office 365 correspondente é excluída. O conteúdo de uma caixa de correio inativa é retido para a duração da retenção feita na caixa de correio antes que ela foi feita inativa. A duração de espera define quanto tempo os itens na pasta são mantidos itens recuperáveis. Quando a duração da retenção expira para um item na pasta itens recuperáveis, o item é excluído permanentemente (descartados) da caixa de correio inativa. Depois que uma caixa de correio é feita inativa, você pode alterar a duração da retenção ou política de retenção do Office 365 atribuído à caixa de correio inativa.
  
> [!IMPORTANT]
> Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa usar o PowerShell do Exchange Online para alterar a duração de espera de um litígio em uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Mas você pode usar o PowerShell do Exchange Online ou o EAC para alterar a duração de espera de um bloqueio In-loco. Você pode usar a segurança do Office 365 &amp; Centro de conformidade ou a segurança &amp; PowerShell do Centro de conformidade para alterar a duração de espera para uma política de retenção do Office 365.
    
- Para conectar ao PowerShell do Exchange Online ou segurança &amp; PowerShell do Centro de conformidade, consulte um dos seguintes tópicos:
    
  - [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365](https://go.microsoft.com/fwlink/?linkid=799771)
    
- Observe que retém associado a casos de eDiscovery são infinitas isenções, que significa que não há nenhuma duração de espera pode ser alterada. Itens são mantidos indefinidamente ou até que a suspensão seja removida e a caixa de correio inativa é excluída.
    
- Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Etapa 1: Identificar os bloqueios em uma caixa de correio inativa

Porque os diferentes tipos de isenções ou uma ou mais políticas de retenção do Office 365 podem ser colocadas em uma caixa de correio inativa, a primeira etapa é identificar os bloqueios em uma caixa de correio inativa.
  
Execute o seguinte comando no Exchange Online PowerShell para exibir as informações de espera para todas as caixas de correio inativas em sua organização.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
O valor de **True** para a propriedade **LitigationHoldEnabled** indica que a caixa de correio inativa está em retenção de litígio. Se um bloqueio In-loco, retenção de descoberta eletrônica ou política de retenção do Office 365 é colocada em uma caixa de correio inativa, um GUID para a política de retenção ou retenção é exibido como o valor da propriedade **InPlaceHolds** . Por exemplo, o exemplo a seguir mostra resultados de caixas de correio inativas 5. 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
A tabela a seguir identifica os cinco tipos diferentes de espera que foram usados para tornar cada caixa de correio inativa.
  
|**Caixa de correio inativa**|**Tipo de bloqueio**|**Como identificar o bloqueio na caixa de correio inativa**|
|:-----|:-----|:-----|
|Ann Beebe  <br/> |Retenção de litígio  <br/> |A propriedade *LitigationHoldEnabled* estiver definida como `True`.  <br/> |
|Pilar Pinilla  <br/> |Bloqueio In-loco  <br/> |A propriedade *InPlaceHolds* contém o GUID do In-Place Hold é colocado na caixa de correio inativa. Você pode dizer que isso é um bloqueio In-loco, porque a ID não começa com um prefixo.<br/> Você pode usar o ' Get-MailboxSearch - InPlaceHoldIdentity<hold GUID> | FL' command no PowerShell do Exchange Online para obter mais informações sobre o bloqueio In-loco na caixa de correio inativa.  <br/> |
|Mario Necaise  <br/> |Política de retenção do Office 365 toda a organização na segurança &amp; Centro de conformidade  <br/> |A propriedade *InPlaceHolds* está vazia. Isso indica que um ou mais toda a organização ou (Exchange toda) Office 365 política de retenção é aplicada à caixa de correio inativa. Nesse caso, é possível executar o ' Get-OrganizationConfig | Select-Object - ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nome de FL'<br/><br/>
|Carol Olson  <br/> |Política de retenção do Office 365 na segurança &amp; Centro de conformidade aplicadas a caixas de correio específicas  <br/> |A propriedade *InPlaceHolds* contém o GUID da política de retenção Office 365 que é aplicado à caixa de correio inativa. Você pode dizer que essa é uma política de retenção aplicada às caixas de correio específicas, porque o GUID começa com a `mbx` prefixo. Observe que, se o GUID da política de retenção aplicada à caixa de correio inativa iniciados com o `skp` prefixo, que indica se a política de retenção é aplicada para Skype para conversas de negócios.<br/><br/> A política de retenção da identidade do Office 365 que é aplicada à caixa de correio inativa, execute o seguinte comando na segurança &amp; PowerShell do Centro de conformidade.<br/><br/> ' Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nome de FL` <br/><br/>Be sure to remove the  `mbx` or  `skp' prefix quando você executar esse comando.  <br/> |
|Abraham McMahon  <br/> |retenção de caso de descoberta eletrônica na segurança &amp; Centro de conformidade  <br/> |A propriedade *InPlaceHolds* contém o GUID da isenção casos de eDiscovery que é colocado na caixa de correio inativa. Você pode dizer que isso é uma espera de casos de eDiscovery, porque o GUID começa com a `UniH` prefixo.<br/> Você pode usar o `Get-CaseHoldPolicy` cmdlet em Security &amp; PowerShell do Centro de conformidade para obter mais informações sobre o caso de eDiscovery que o bloqueio na caixa de correio inativa está associado. Por exemplo, você pode executar o comando ' Get-CaseHoldPolicy<hold GUID without prefix> | Nome de FL` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/> `$CaseHold.CaseId Get-ComplianceCase | Nome de FL'<br/><br/><br/> **Observação:** Não recomendamos usando a descoberta eletrônica contém de caixas de correio inativas. Isso ocorre porque os casos de eDiscovery servem para casos específicos e de ligação de tempo relacionados a uma questão legal. Em algum momento, um caso jurídico provavelmente será finalizado e os bloqueios associados à ocorrência serão removidos e o caso de descoberta eletrônica estará fechado (ou excluídos). Na verdade, se uma isenção que é colocada em uma caixa de correio inativa é associada a um caso de eDiscovery e a suspensão seja removida ou o caso de descoberta eletrônica é fechado ou excluído, a caixa de correio inativa será excluída permanentemente. 

Para obter mais informações sobre as políticas de retenção do Office 365, consulte [Visão geral das políticas de retenção](retention-policies.md).
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>Etapa 2: Alterar a duração de espera para uma caixa de correio inativa

Depois de identificar que tipo de espera é colocado na caixa de correio inativa (e se há vários bloqueios), a próxima etapa é para alterar a duração da espera. 
  
### <a name="change-the-duration-for-a-litigation-hold"></a>Alterar a duração de um litígio

Aqui está como usar o PowerShell do Exchange Online para alterar a duração de espera para um litígio que é colocada em uma caixa de correio inativa. Você não pode usar o EAC. Execute o seguinte comando para alterar a duração de espera. Neste exemplo, a duração da retenção é alterada para um período ilimitado.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

O resultado é que os itens na caixa de correio inativa são mantidos indefinidamente ou até que a suspensão seja removida ou a duração da retenção é alterada para um valor diferente.
  
> [!TIP]
> A melhor maneira de identificar uma caixa de correio inativa é usando seu valor de **Nome distinto** ou o **GUID do Exchange** . Usar um desses valores ajuda a evitar a acidentalmente especificando a caixa de correio errada. 
  
### <a name="change-the-duration-for-an-in-place-hold"></a>Alterar a duração de um bloqueio In-loco

 Você pode usar o EAC ou o PowerShell do Exchange Online para alterar a duração de espera de um bloqueio In-loco. 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a>Usar o EAC para alterar a duração de espera

1. Se você souber o nome do bloqueio In-loco que você deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa. Use o GUID bloqueio In-loco que você obteve na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
3. Selecione o bloqueio In-loco você deseja alterar e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades página, clique em **Bloqueio In-loco**. 
    
5. Um dos seguintes com base no atual duração da retenção:
    
1. Clique em **espera indefinidamente** para reter itens por um período ilimitado. 
    
2. Clique em **especificar o número de dias para reter itens em relação à sua data de recebimento** para reter itens por um período específico. Digite o número de dias em que você deseja reter itens para. 
    
    ![Captura de tela da alteração da duração de um Bloqueio In-loco](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. Clique em **Salvar**.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Use o PowerShell do Exchange Online para alterar a duração de espera

1. Se você souber o nome do bloqueio In-loco que você deseja alterar, vá para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa. Use o GUID bloqueio In-loco que você obteve na [etapa 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. Execute o seguinte comando para alterar a duração de espera. Neste exemplo, a duração da retenção é alterada para 2,555 dias (aproximadamente sete anos). 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     Para alterar a duração de espera para um período ilimitado de tempo, use _- ItemHoldPeriod ilimitado_.
  
## <a name="more-information"></a>Mais informações

- **Como a duração da retenção é calculada para um item em uma caixa de correio inativa?** A duração é calculada a partir da data original de um item de caixa de correio foi recebido ou criado. 
    
- **o que acontece quando a duração da retenção expira?** Quando a duração da retenção expira para um item de caixa de correio na pasta itens recuperáveis, o item é excluído permanentemente (descartados) da caixa de correio inativa. Se não houver nenhuma duração especificada para o bloqueio colocado na caixa de correio inativa, itens na pasta itens recuperáveis nunca são limpos (a menos que a duração de espera para a caixa de correio inativa mudou). 
    
- **é uma política de retenção do Exchange ainda processada em caixas de correio inativas?** Se uma política de retenção do Exchange (os registros de mensagens gerenciamento ou MRM, recurso no Exchange Online) foi aplicada a uma caixa de correio quando ela foi feita inativa, as políticas de exclusão (que são configuradas com uma ação de retenção **Excluir** as marcas de retenção) será Continue a serem processados na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão são movidos para a pasta itens recuperáveis quando o período de retenção expira. Os itens são limpos, em seguida, da caixa de correio inativa quando a duração de espera para um item expira. 
    
    Por outro lado, quaisquer políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa serão ignoradas. Isso significa que os itens em uma caixa de correio inativa que estão marcados com uma política de arquivamento permanecem na caixa de correio principal quando o período de retenção expira. Elas não serão movidas para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Porque um usuário não pode entrar em uma caixa de correio inativa, não há nenhum motivo para consumir recursos do datacenter para processar as diretivas de arquivamento. 
    
- **Para verificar se a nova duração da retenção, execute um dos seguintes comandos.** O primeiro comando destina litígio; o segundo é para bloqueio In-loco. 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- **Como caixas de correio regulares, a Managed pasta Assistant (MFA) também processa caixas de correio inativas.** No Exchange Online, o MFA processa caixas de correio aproximadamente uma vez a cada 7 dias. Depois de alterar a duração de espera para uma caixa de correio inativa, você pode usar o cmdlet **Start-ManagedFolderAssistant** para iniciar imediatamente o processamento a nova duração de espera para a caixa de correio inativa. Execute o seguinte comando. 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- **Se muita isenções são colocados em uma caixa de correio inativa, nem todos da isenção GUIDs serão exibidos.** Você pode executar o seguinte comando para exibir os GUIDs de todas as isenções (exceto litígio retém) que são colocadas em uma caixa de correio inativa. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
