---
title: Recuperar uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: 'Se um antigo funcionário retornará à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho de um funcionário departed, você pode recuperar o conteúdo da caixa de correio inativa no Office 365. Ao recuperar uma caixa de correio inativa, ela é convertida em uma nova caixa de correio que contém o conteúdo da caixa de correio inativa. '
ms.openlocfilehash: dcc84e44454a75f8b4dac953599632d632f340b9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524613"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Recuperar uma caixa de correio inativa no Office 365

Uma caixa de correio inativa (que é um tipo de caixa de correio excluída) é usada para preservação de emails de um antigo do funcionário depois que ele deixa a sua organização. Se esse funcionário retorna à sua organização ou outro funcionário leva as responsabilidades de trabalho do funcionário anterior, há duas maneiras que você pode disponibilizar o conteúdo da caixa de correio inativa para um usuário: 
  
- **Recuperar uma caixa de correio inativa** Se o antigo funcionário retornará à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho do funcionário anterior, você pode recuperar o conteúdo da caixa de correio inativa. Este método converte a caixa de correio inativa uma nova caixa de correio ativa que contém o conteúdo da caixa de correio inativa. Depois que ele seja recuperado, a caixa de correio inativa não existe mais. Os procedimentos neste tópico descrevem esse método. 
    
- **Restaurar uma caixa de correio inativa** Se outro funcionário leva as responsabilidades de trabalho do funcionário anterior, ou se outro usuário precisa acessar o conteúdo da caixa de correio inativa, você pode restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Você também pode restaurar o arquivamento de uma caixa de correio inativa. Para obter os procedimentos para esse método, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
    
Consulte a seção de [informações adicionais](recover-an-inactive-mailbox.md#moreinfo) para obter mais detalhes sobre as diferenças entre a recuperação e a restauração de uma caixa de correio inativa e para obter uma descrição do que acontece quando uma caixa de correio inativa seja recuperada.
  
> [!NOTE]
> Podemos foi adiada o prazo de criação de novos retenções locais para tornar uma caixa de correio inativa. Mas, em algum momento no futuro, você não conseguirá criar novos retenções locais no Exchange Online. Nesse momento, políticas de retenção apenas contém de litígio e o Office 365 podem ser usadas para criar uma caixa de correio inativa. No entanto, existentes caixas de correio inativas que estão em In-loco bloqueio ainda serão suportadas e você pode continuar a gerenciar as isenções de In-loco em caixas de correio inativas. Isso inclui alterando a duração de um bloqueio In-loco e excluir permanentemente uma caixa de correio inativa, removendo o bloqueio In-loco. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa usar o Exchange Online PowerShell para restaurar uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Execute o seguinte comando para obter informações de identidade para as caixas de correio inativas em sua organização. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    Use as informações retornadas por esse comando para recuperar uma caixa de correio inativa específica.
    
- Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="recover-an-inactive-mailbox"></a>Recuperar uma caixa de correio inativa

Use o cmdlet **New-Mailbox** com o parâmetro *InactiveMailbox* para recuperar uma caixa de correio inativa. 
  
1. Crie uma variável que contém as propriedades da caixa de correio inativa. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > No comando anterior, use o valor da propriedade **DistinguishedName** ou **ExchangeGUID** para identificar a caixa de correio inativa. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto que é possível que um ativas e uma caixa de correio inativa podem ter o mesmo endereço SMTP principal. 
  
2. Este exemplo usa as propriedades obtidas no comando anterior e recupera a caixa de correio inativa para uma caixa de correio ativa para o usuário de Ann Beebe. Certifique-se de que os valores especificados para os parâmetros de *nome* e *MicrosoftOnlineServicesID* são exclusivos dentro da sua organização. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    O endereço SMTP principal para a caixa de correio inativa recuperada terá o mesmo valor que daquela especificada pelo parâmetro *MicrosoftOnlineServicesID* . 
    
Após recuperar uma caixa de correio inativa, uma nova conta de usuário do Office 365 também é criada. Você deve ativar esta conta de usuário, atribuindo uma licença. Para atribuir uma licença no Centro de administração do Office 365, consulte [atribuir ou remover licenças para o Office 365 para empresas](https://go.microsoft.com/fwlink/p/?LinkId=276798).
  
## <a name="more-information"></a>Mais informações

- **Qual é a principal diferença entre recuperação e a restauração de uma caixa de correio inativa?** Ao recuperar uma caixa de correio inativa, basicamente, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio está vinculada a uma nova conta de usuário. Depois que ele seja recuperado, a caixa de correio inativa não existe mais e quaisquer alterações feitas ao conteúdo na caixa de correio nova afetará o conteúdo que foi originalmente em espera na caixa de correio inativa. Por outro lado, quando você restaura uma caixa de correio inativa, o conteúdo meramente é copiado para outra caixa de correio. A caixa de correio inativa é preservada e permanece uma caixa de correio inativa. Quaisquer alterações feitas ao conteúdo na caixa de correio de destino não afetarão o conteúdo original mantido na caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada usando a descoberta eletrônica In-loco, seu conteúdo possa ser restaurado para outra caixa de correio ou pode ser recuperado ou excluído posteriormente. 
    
- **o que acontece quando você recuperar uma caixa de correio inativa?** Ao recuperar uma caixa de correio inativa, ocorrerá o seguinte: 
    
  - Bloqueio de litígio (se ele foi habilitado para a caixa de correio inativa) foi removido.
    
  - Retenções locais serão removidos. Isso significa que a caixa de correio inativa será removida como uma caixa de correio de origem de qualquer bloqueio In-loco ou pesquisas de descoberta eletrônica In-loco. 
    
  - A caixa de correio inativa é removida da quaisquer políticas de retenção do Office 365 que where aplicado a ela.
    
  - O período de recuperação de item único (que é definido pela propriedade **RetainDeletedItemsFor** caixa de correio) é definido como 30 dias. Normalmente, quando uma nova caixa de correio é criada no Exchange Online, esse período de retenção é definido para 14 dias. Essa configuração para o valor máximo de 30 dias proporciona mais tempo para recuperar todos os dados que tenham sido permanentemente excluídos (ou limpos) da caixa de correio inativa. Você também pode desabilitar a recuperação de item único ou definir a recuperação de item único período de volta para o padrão de 14 dias. Para obter mais informações, consulte [Habilitar ou desabilitar a recuperação de item único para uma caixa de correio](https://go.microsoft.com/fwlink/?linkid=856769).
    
  - Retenção é habilitada e a duração de espera de retenção é definida como 30 dias. Isso significa que a política de retenção do Exchange padrão e qualquer Office 365 toda a organização ou todo o Exchange políticas de retenção que são atribuídas a nova caixa de correio não serão processadas por 30 dias. Isso oferece o funcionário retornando ou o novo proprietário do tempo inativo de caixa de correio recuperada para gerenciar as mensagens antigas. Caso contrário, a política de retenção do Exchange ou o Office 365 pode excluir itens antigos da caixa de correio (ou mover itens para a caixa de correio de arquivo morto, se ele estiver habilitado) que tiverem expirado com base nas configurações definidas para as políticas de retenção do Exchange ou o Office 365. Após 30 dias, o intervalo de retenção expira, a propriedade de caixa de correio de **RetentionHoldEnabled** estiver definida como **False**e Assistente de pasta gerenciada inicia as políticas atribuídas à caixa de correio de processamento. Se você não precisa desta vez adicional, você pode remover apenas o status em retenção. Como alternativa, você pode aumentar a duração da retenção retenção usando o comando **Set-Mailbox-EndDateForRetentionHold** . Para obter mais informações, consulte [retenção local de uma caixa de correio em retenção](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Colocar um bloqueio na caixa de correio recuperada, se você precisar preservar o estado original da caixa de correio inativa.** Para impedir que o novo proprietário da caixa de correio ou a política de retenção a exclusão permanente de todas as mensagens da caixa de correio inativa recuperada, você pode colocar a caixa de correio em retenção de litígio para obter mais informações, consulte [Place uma caixa de correio em retenção de litígio](https://go.microsoft.com/fwlink/?linkid=856286).
    
- **A ID de usuário que você pode usar ao recuperar uma caixa de correio inativa?** Ao recuperar uma caixa de correio inativa, o valor especificado para o parâmetro *MicrosoftOnlineServicesID* pode ser diferente daquele original que tiver sido associado a caixa de correio inativa. Você também pode usar a identificação de usuário original. Mas, conforme indicado anteriormente, certifique-se de que os valores usados para o *nome* e *MicrosoftOnlineServicesID* são exclusivos dentro da sua organização ao recuperar a caixa de correio inativa. 
    
- **e se o período de retenção de caixa de correio para a caixa de correio inativa não tenha expirado?** Se uma caixa de correio inativa foi excluída há menos de 30 dias, você não pode usar o comando **New-Mailbox-InactiveMailbox** recuperá-lo. Você tem que recuperá-lo, restaurando a conta de usuário correspondente do Office 365. Para obter mais informações, consulte [Excluir ou restaurar os usuários](https://go.microsoft.com/fwlink/p/?LinkId=279162).
    
- **Como verifico se o período de retenção de caixa de correio excluída para uma caixa de correio inativa expirou?** Execute o seguinte comando. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    Se não houver um valor para a propriedade **ExternalDirectoryObjectId** , o período de retenção de caixa de correio expirou, e você pode recuperar a caixa de correio inativa executando o comando **New-Mailbox-InactiveMailbox** . Se houver um valor para a propriedade **ExternalDirectoryObjectId** , o período de retenção de caixa de correio excluída não tenha expirado e você precisar recuperar a caixa de correio restaurando a conta de usuário do Office 365. Consulte [Excluir ou restaurar usuários](https://go.microsoft.com/fwlink/p/?LinkId=279162)
    
- **Considere habilitar a caixa de correio de arquivo morto após recuperar uma caixa de correio inativa.** Isso permite que o retornando usuário ou novo funcionário mover mensagens antigas para a caixa de correio de arquivo morto. E quando o status em retenção expira, a política de arquivamento que faz parte da política de retenção de Exchange padrão atribuída ao Exchange Online caixas de correio moverá itens que estão dois anos ou mais antiga para a caixa de correio de arquivo morto. Se você não habilitar a caixa de correio de arquivo morto, itens com mais de dois anos permanecerá na caixa de correio principal do usuário. Para obter mais informações, consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md).
 