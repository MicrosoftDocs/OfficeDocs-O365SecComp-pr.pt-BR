---
title: Excluir uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: Quando não há mais precisa preservar o conteúdo de uma caixa de correio inativa do Office 365, você pode excluir permanentemente a caixa de correio inativa, removendo isenção. Depois de remover a retenção, a caixa de correio inativa é marcada para exclusão e é excluída permanentemente depois que ela é processada.
ms.openlocfilehash: a7284be650d7ec6c89a6fdc43d8614603d6f1e19
ms.sourcegitcommit: 82fd4c85b952819157fbb13175c7b2dbbdff510f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965248"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a>Excluir uma caixa de correio inativa no Office 365

Uma caixa de correio inativa é usada para preservação de emails de um antigo do funcionário depois que ele deixa a sua organização. Quando não há mais precisa preservar o conteúdo de uma caixa de correio inativa, você pode excluir permanentemente a caixa de correio inativa, removendo a retenção. Além disso, é possível que vários bloqueios podem ser colocados em uma caixa de correio inativa. Por exemplo, uma caixa de correio inativa pode ser colocada em litígio e em um ou mais retenções locais. Além disso, uma política de retenção do Office 365 (criados no Office 365 Security &amp; Centro de conformidade) podem ser aplicadas à caixa de correio inativa. Você precisa remover todas as isenções e políticas de retenção do Office 365 de uma caixa de correio inativa para excluí-lo. Depois de remover o isenções e políticas de retenção, a caixa de correio inativa é marcada para exclusão e é excluída permanentemente depois que ela é processada.
  
> [!IMPORTANT]
> Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco. 
  
Consulte a seção de [informações adicionais](delete-an-inactive-mailbox.md#moreinfo) para obter uma descrição do que acontece após isenções serem removidas de uma caixa de correio inativa. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa usar o PowerShell do Exchange Online para remover um litígio de uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Você pode usar o PowerShell do Exchange Online ou o EAC para remover um bloqueio In-loco de uma caixa de correio inativa. 
    
- Você pode copiar o conteúdo de uma caixa de correio inativa para outra caixa de correio antes de remover a retenção e excluir uma caixa de correio inativa. Para obter detalhes, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
    
- Se você remove a política de retenção do Office 365 ou espera de uma caixa de correio inativa e o período de retenção de caixa de correio excluída da caixa de correio tiver expirado, a caixa de correio será excluída permanentemente. Depois que ele for excluído, ela não pode ser recuperada. Antes de remover a retenção, certifique-se de que você não precisa mais o conteúdo na caixa de correio. Se você quiser reativar uma caixa de correio inativa, você pode recuperar a ele. Para obter detalhes, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
- Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Etapa 1: Identificar os bloqueios em uma caixa de correio inativa

Conforme indicado anteriormente, uma política de retenção de litígio, bloqueio In-loco ou Office 365 pode ser colocada em uma caixa de correio inativa. A primeira etapa é identificar os bloqueios em uma caixa de correio inativa.
  
Execute o seguinte comando para exibir as informações de espera para todas as caixas de correio inativas na sua organização.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

O valor de **True** para a propriedade **LitigationHoldEnabled** indica que a caixa de correio inativa está em retenção de litígio. Se um bloqueio In-loco é colocado em uma caixa de correio inativa, o GUID de retenção é exibido como o valor da propriedade **InPlaceHolds** . Por exemplo, os seguintes resultados para duas caixas de correio inativas mostram que um litígio for colocado em Ann Beebe e que dois In-Place Holds são colocados em Pilar Pinilla. 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> Se muita In-Place Holds é colocada em uma caixa de correio inativa, nem todos os GUIDs de bloqueio In-loco serão exibidos. Você pode executar o seguinte comando para exibir todos os GUIDs de espera a In-loco:`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a>Etapa 2: Remover uma isenção de uma caixa de correio inativa

Depois de identificar que tipo de espera é colocado na caixa de correio inativa (e se há vários bloqueios), a próxima etapa é para remover os bloqueios na caixa de correio. Conforme indicado anteriormente, você precisa remover todas as isenções para excluir permanentemente uma caixa de correio inativa. 
  
### <a name="remove-a-litigation-hold"></a>Remover um bloqueio de litígio

Conforme indicado anteriormente, você precisará usar o Windows PowerShell para remover um litígio de uma caixa de correio inativa. Você não pode usar o EAC. Execute o seguinte comando para remover um litígio.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> A melhor maneira de identificar uma caixa de correio inativa é usando seu valor de nome distinto ou o GUID do Exchange. Usar um desses valores ajuda a evitar a acidentalmente especificando a caixa de correio errada. 
  
### <a name="remove-in-place-holds"></a>Remover retenções locais

 Há duas maneiras de remover um bloqueio In-loco de uma caixa de correio inativa: 
  
- **Excluir o objeto de bloqueio In-loco** Se a caixa de correio inativa que você deseja excluir permanentemente a caixa de correio de origem somente para um bloqueio In-loco, você pode excluir apenas o objeto de bloqueio In-loco. 
    
    > [!NOTE]
    > Você precisa desabilitar a espera antes de excluir um objeto de bloqueio In-loco. Se você tentar excluir um objeto de bloqueio In-loco que tem a suspensão habilitada, você receberá uma mensagem de erro. 
  
- **Remover a caixa de correio inativa como uma caixa de correio de origem de um bloqueio In-loco** Se você deseja reter outras caixas de correio de origem para um bloqueio In-loco, você pode remover a caixa de correio inativa da lista de caixas de correio de origem e manter o objeto de bloqueio In-loco. 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a>Usar o EAC para excluir um bloqueio In-loco

1. Se você souber o nome do bloqueio In-loco que você deseja excluir, você pode ir para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de In-Place Hold é colocado na caixa de correio inativa que você deseja excluir permanentemente. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
3. Selecione o bloqueio In-loco que deseja excluir e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades de página, clique em **Bloqueio In-loco**, desmarque a caixa de **conteúdo do local que corresponda a consulta de pesquisa em caixas de correio selecionadas em espera** e, em seguida, clique em **Salvar**.
    
5. Sobre o **Descoberta eletrônica In-loco &amp; mantenha** de página, selecione o bloqueio In-loco novamente e, em seguida, clique em **Excluir**![ícone Excluir](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).
    
6. No aviso, clique em **Sim** para excluir o bloqueio In-loco. 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a>Use o PowerShell do Exchange Online para excluir um bloqueio In-loco

1. Crie uma variável que contém as propriedades de bloqueio de In-loco que você deseja excluir. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Desabilite a isenção em In-Place Hold.
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. Exclua o bloqueio In-loco.
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Usar o EAC para remover uma caixa de correio inativa de um bloqueio In-loco

1. Se você souber o nome do In-Place Hold é colocado na caixa de correio inativa, você pode ir para a próxima etapa. Caso contrário, execute o seguinte comando para obter o nome de bloqueio In-loco colocado na caixa de correio. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. No EAC, vá até **gerenciamento de conformidade** \> **Descoberta eletrônica In-loco &amp; mantenha**.
    
3. Selecione o bloqueio In-loco que é colocado na caixa de correio inativa e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Sobre o **Descoberta eletrônica In-loco &amp; mantenha** propriedades página, clique em **fontes**.
    
5. Na lista de caixas de correio de origem, clique no nome da caixa de correio inativa que você deseja remover e, em seguida, clique em **Remover**![ícone Remover](media/adf01106-cc79-475c-8673-065371c1897b.gif).
    
6. Clique em **Salvar** para salvar as alterações. Será exibida uma mensagem informando que a operação foi concluída com êxito. 
    
7. Repita as etapas 1 a 6 para remover a outras retenções locais colocado na caixa de correio inativa.
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Use o PowerShell do Exchange Online para remover uma caixa de correio inativa de um bloqueio In-loco

Se o bloqueio In-loco contiver um grande número de caixas de correio de origem, é possível que a caixa de correio inativa não será listada na página **fontes** no EAC. Até 3.000 caixas de correio são exibidas na página **fontes** quando você edita um bloqueio In-loco. Se uma caixa de correio inativa não estiver listada na página **fontes** , você pode usar o PowerShell do Exchange Online para removê-lo a In-Place Hold. 
  
1. Crie uma variável que contém as propriedades de bloqueio In-loco colocado na caixa de correio inativa. Usar o GUID bloqueio In-loco que você obteve na [etapa 1: identificar os bloqueios em uma caixa de correio inativa](delete-an-inactive-mailbox.md#step1).
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Verifique se a caixa de correio inativa está listada como uma caixa de correio de origem para o bloqueio In-loco. 
    
```
  $InPlaceHold.Sources
```

   **Observação:** A propriedade de *fontes* de In-Place Hold identifica as caixas de correio de origem pelas suas propriedades *LegacyExchangeDN* . Como essa propriedade identifica exclusivamente a caixas de correio inativas, usando a propriedade *fontes* de In-Place Hold ajuda a impedir a remoção de caixa de correio errado. Isso também ajuda a evitar problemas se duas caixas de correio tiverem o mesmo alias ou o endereço SMTP. 
   
3. Remova a caixa de correio inativa da lista de caixas de correio de origem na variável. Certifique-se de usar o **LegacyExchangeDN** da caixa de correio inativa retornado pelo comando na etapa anterior. 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. Verifique se a caixa de correio inativa é removida da lista de caixas de correio de origem na variável.
    
```
  $InPlaceHold.Sources
```

5. Modifica o bloqueio In-loco com a lista atualizada de caixas de correio de origem, que não inclui a caixa de correio inativa.
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. Verifique se que a caixa de correio inativa será removida da lista de caixas de correio de origem para o bloqueio In-loco.
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a>Mais informações

- **Uma caixa de correio inativa é um tipo de caixa de correio excluída.** No Exchange Online, uma caixa de correio excluída é uma caixa de correio que tenha sido excluída, mas pode ser recuperada em um período de retenção específico. O período de retenção de caixa de correio excluída no Exchange Online é 30 dias. Isso significa que a caixa de correio pode ser recuperada dentro de 30 dias do que está sendo excluída. Após 30 dias, uma caixa de correio excluída é marcada para exclusão permanente e não pode ser recuperada. 
    
- **o que acontece depois de você remove a retenção em uma caixa de correio inativa?** A caixa de correio é tratada como outras caixas de correio excluída e é marcada para exclusão permanente depois que o período de retenção de caixa de correio excluída 30 dias expira. Esse período de retenção começa na data quando a caixa de correio foi feita pela primeira vez inativa. Essa data é conhecida como a data de exclusão reversível, que é a data em que a conta de usuário correspondente do Office 365 foi excluída ou quando a caixa de correio do Exchange Online foi excluída com o cmdlet **Remove-Mailbox** . A data de exclusão reversível não é a data em que você pode remover a retenção. 
    
- **é uma caixa de correio inativa permanentemente excluída imediatamente após a suspensão seja removida?** Se a data de exclusão reversível para uma caixa de correio inativa for mais de 30 dias, a caixa de correio não será excluída permanentemente assim que você remove a retenção. A caixa de correio será marcada para exclusão permanente e é excluída na próxima vez que ela é processada. 
    
- **Como o período de retenção de caixa de correio excluída afeta a caixas de correio inativas?** Se a data de exclusão reversível para uma caixa de correio inativa for mais de 30 dias antes da data em que a suspensão foi removida, a caixa de correio é marcada para exclusão permanente. Mas, se uma caixa de correio inativa tem uma data de exclusão reversível nos últimos 30 dias e você remove a retenção, você pode recuperar a caixa de correio até que o período de retenção de caixa de correio excluída expira. Para obter detalhes, consulte [Excluir ou restaurar caixas de correio do usuário no Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). Depois que o período de retenção de caixa de correio excluída expira, você tem siga os procedimentos para a recuperação de uma caixa de correio inativa. Para obter detalhes, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
- **Como você exibe informações sobre uma caixa de correio inativa depois que a suspensão seja removida?** Depois que um bloqueio seja removido e a caixa de correio inativa é revertida para uma caixa de correio excluída, ela não será retornada usando o parâmetro *InactiveMailboxOnly* com o cmdlet **Get-Mailbox** . Mas você pode exibir informações sobre a caixa de correio usando o comando **Get-Mailbox-SoftDeletedMailbox** . Por exemplo: 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
No exemplo acima, a propriedade *WhenSoftDeleted* identifica a data de exclusão reversível, que neste exemplo é 30 de outubro de 2014. Se esta caixa de correio excluída anteriormente era uma caixa de correio inativa para o qual a suspensão foi removida, ele será permanentemente excluídos 30 dias após o valor da propriedade *WhenSoftDeleted* . Nesse caso, a caixa de correio é excluída permanentemente após 30 de novembro de 2014.

