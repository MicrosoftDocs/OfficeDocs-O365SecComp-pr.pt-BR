---
title: Restaurar uma caixa de correio inativa no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Se um novo funcionário ou outro usuário precisa acessar o conteúdo de uma caixa de correio inativa no Office 365, você pode restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente.
ms.openlocfilehash: e0add2b63a48edc27795143324c83153b15dcf8c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523530"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Restaurar uma caixa de correio inativa no Office 365

Uma caixa de correio inativa (que é um tipo de caixa de correio excluída) é usada para reter o email de um antigo do funcionário depois que ele deixa a sua organização. Se outro funcionário leva as responsabilidades de trabalho do funcionário departed ou que funcionário retorna à sua organização, há duas maneiras que você pode disponibilizar o conteúdo da caixa de correio inativa para um usuário: 
  
- **Restaurar uma caixa de correio inativa** Se outro funcionário leva as responsabilidades de trabalho do funcionário departed, ou se outro usuário precisa acessar o conteúdo da caixa de correio inativa, você pode restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Você também pode restaurar o arquivamento de uma caixa de correio inativa. Depois que ele é restaurado, a caixa de correio inativa é preservada e é mantida como uma caixa de correio inativa. Este tópico descreve os procedimentos para restaurar uma caixa de correio inativa. 
    
- **Recuperar uma caixa de correio inativa** Se o funcionário departed retornará à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho do funcionário departed, você pode recuperar o conteúdo da caixa de correio inativa. Este método converte a caixa de correio inativa em uma nova caixa de correio que contém o conteúdo da caixa de correio inativa. Depois que ele seja recuperado, a caixa de correio inativa não existe mais. Para obter os procedimentos passo a passo, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
Consulte a seção **mais informações** neste artigo para obter mais detalhes sobre as diferenças entre a restauração e recuperação de uma caixa de correio inativa. 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa usar o Exchange Online PowerShell para restaurar uma caixa de correio inativa. Você não pode usar o Centro de administração do Exchange (EAC). Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Execute o seguinte comando no Exchange Online PowerShell para obter informações de identidade para as caixas de correio inativas em sua organização. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     Use as informações retornadas por esse comando para restaurar uma caixa de correio inativa específica.
    
- Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="restore-an-inactive-mailbox"></a>Restaurar uma caixa de correio inativa

Use o cmdlet **New-MailboxRestoreRequest** com os parâmetros _SourceMailbox_ e _TargetMailbox_ para restaurar o conteúdo de uma caixa de correio inativa para uma caixa de correio existente. Para obter mais informações sobre como usar esse cmdlet, consulte [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).
  
1. Crie uma variável que contém as propriedades da caixa de correio inativa. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > No comando anterior, use o valor da propriedade **DistinguishedName** ou **ExchangeGUID** para identificar a caixa de correio inativa. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto que é possível que um ativas e uma caixa de correio inativa podem ter o mesmo endereço SMTP principal. 
  
2. Restaure o conteúdo da caixa de correio inativa para uma caixa de correio existente. O conteúdo da caixa de correio inativa (caixa de correio de origem) será mesclado nas pastas correspondentes na caixa de correio existente (caixa de correio de destino).
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   Como alternativa, você pode especificar uma pasta de nível superior na caixa de correio de destino em que deseja restaurar o conteúdo da caixa de correio inativa. Se a pasta de destino especificada ou a estrutura de pasta de destino ainda não existir na caixa de correio de destino, ele é criado durante o processo de restauração. 
    
    Este exemplo copia os itens de caixa de correio e subpastas a partir de uma caixa de correio inativa para uma pasta denominada "Caixa de correio inativa" na estrutura de pastas de nível superior da caixa de correio de destino.
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a>Restaurar o arquivo morto de uma caixa de correio inativa

Se uma caixa de correio inativa tiver uma caixa de correio de arquivo morto, você também pode restaurá-lo à caixa de correio de arquivo morto de uma caixa de correio existente. Para restaurar o arquivo morto de uma caixa de correio inativa, você precisa adicionar os switches _SourceIsArchive_ e _TargetIsAchive_ ao comando usado para restaurar uma caixa de correio inativa. 
  
1. Crie uma variável que contém as propriedades da caixa de correio inativa. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > No comando anterior, use o valor da propriedade **DistinguishedName** ou **ExchangeGUID** para identificar a caixa de correio inativa. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto que é possível que um ativas e uma caixa de correio inativa podem ter o mesmo endereço SMTP principal. 
  
2. Restaure o conteúdo do arquivamento da caixa de correio inativa (arquivo de origem) para o arquivamento de uma caixa de correio existente (arquivo de destino). Neste exemplo, o conteúdo do arquivamento do código-fonte é copiado para uma pasta denominada "Arquivo inativo de caixa de correio" no arquivamento da caixa de correio de destino.

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a>Mais informações

- **Qual é a principal diferença entre recuperação e a restauração de uma caixa de correio inativa?** Ao recuperar uma caixa de correio inativa, basicamente, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio está vinculada a uma nova conta de usuário. Depois que ele seja recuperado, a caixa de correio inativa não existe mais e quaisquer alterações feitas ao conteúdo na caixa de correio nova afetará o conteúdo que foi originalmente em espera na caixa de correio inativa. Por outro lado, quando você restaura uma caixa de correio inativa, o conteúdo meramente é copiado para outra caixa de correio. A caixa de correio inativa é preservada e permanece uma caixa de correio inativa. Quaisquer alterações feitas ao conteúdo na caixa de correio de destino não afetarão o conteúdo original mantido na caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada, usando a [ferramenta de pesquisa de conteúdo](run-a-content-search-in-the-security-and-compliance-center.md) no Office 365 Security &amp; Centro de conformidade, seu conteúdo possa ser restaurado para outra caixa de correio, ou pode ser recuperado ou excluído posteriormente. 
    
- **Como localizar caixas de correio inativas?** Para obter uma lista das caixas de correio inativas em sua organização e exibir informações úteis para a restauração de uma caixa de correio inativa, você pode executar esse comando. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **Usar uma política de retenção de litígio ou do Office 365 para reter o conteúdo de caixa de correio inativa.** Se você deseja manter o estado de uma caixa de correio inativa depois que ele é restaurado, você pode colocar a caixa de correio de destino em [Litígio](https://go.microsoft.com/fwlink/?linkid=856286) ou aplicar uma [política de retenção do Office 365](retention-policies.md) , antes de restaurar a caixa de correio inativa. Isto evitará a exclusão permanente de todos os itens da caixa de correio inativa depois que eles estiver sendo restaurados na caixa de correio de destino. 
    
- **Enable retenção na caixa de correio de destino antes de restaurar uma caixa de correio inativa.** Como itens de caixa de correio de uma caixa de correio inativa poderiam ser antigos, você deve considerar a ativação retenção na caixa de correio de destino antes de restaurar uma caixa de correio inativa. Quando você coloca uma caixa de correio em retenção espera, a política de retenção é atribuída a ele não será processada até que a suspensão de retenção seja removida ou até que a retenção período expirar. Isso permite que o proprietário do tempo de caixa de correio de destino para gerenciar mensagens antigas da caixa de correio inativa. Caso contrário, a política de retenção pode excluir itens antigos (ou mover itens para a caixa de correio de arquivo morto, se ele estiver habilitado) que tiverem expirado com base nas configurações de retenção configuradas para a caixa de correio de destino. Para obter mais informações, consulte [colocar uma caixa de correio em retenção retenção no Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **o que a opção AllowLegacyDNMismatch fazer?** Nos exemplos anteriores para restaurar uma caixa de correio inativa, a opção de **AllowLegacyDNMismatch** é usada para permitir a restauração de caixa de correio inativa para uma caixa de correio de destino diferente. Em um cenário típico de restauração, o objetivo é restaurar conteúdo onde as caixas de correio de origem e destino são a mesma caixa de correio. Portanto, por padrão, o cmdlet **New-MailboxRestoreRequest** verifica para certificar-se de que o valor da propriedade **LegacyExchangeDN** nas caixas de correio de origem e destino é o mesmo. Isso ajuda a impede que você acidentalmente restaurando uma caixa de correio de origem para a caixa de correio de destino errado. Se você tentar restaurar uma caixa de correio inativa sem usar a opção **AllowLegacyDNMismatch** , o comando pode falhar se as caixas de correio de origem e destino têm valores diferentes para a propriedade **LegacyExchangeDN** . 
    
- **Você pode usar outros parâmetros com o cmdlet New-MailboxRestoreRequest para implementar os cenários de restauração diferente para caixas de correio inativas.** Por exemplo, você pode executar este comando para restaurar o arquivo morto da caixa de correio inativa na caixa de correio principal da caixa de correio de destino. 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  Você também pode restaurar a caixa de correio inativa principal para o arquivamento da caixa de correio de destino, executando este comando.

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- **o que significa que o TargetRootFolder parâmetro fazer?** Conforme explicado anteriormente, você pode usar o parâmetro **TargetRootFolder** para especificar uma pasta na parte superior da estrutura de pastas (também chamada de raiz) na caixa de correio de destino em que deseja restaurar o conteúdo da caixa de correio inativa. Se você não usar esse parâmetro, itens de caixa de correio da caixa de correio inativa são mesclados em pastas padrão correspondente da caixa de correio de destino e pastas personalizadas são recriadas na raiz da caixa de correio de destino. As ilustrações a seguir destacam essas diferenças entre não usar e o parâmetro **TargetRootFolder** . 
    
    **Hierarquia de pastas em que a caixa de correio de destino quando o parâmetro TargetRootFolder não será usado**
    
    ![Captura de tela quando o parâmetro TargetRootFolder não é usado](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    **Hierarquia de pastas em que a caixa de correio de destino quando o parâmetro TargetRootFolder é usado**
    
    ![Captura de tela quando o parâmetro TargetRootFolder é usado](media/300da592-7323-48db-b8a4-07012259d113.png)

  

