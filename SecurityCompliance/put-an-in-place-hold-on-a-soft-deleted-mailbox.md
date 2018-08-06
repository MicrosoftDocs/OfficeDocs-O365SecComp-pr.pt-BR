---
title: Colocar um bloqueio In-loco em uma caixa de correio excluída no Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Saiba como criar um bloqueio In-loco para uma caixa de correio excluída para torná-la inativa e preservar o seu conteúdo. Em seguida, você pode usar ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.
ms.openlocfilehash: 226929764fe39b99f526301029d4a41e2fa486cc
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027608"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Colocar um bloqueio In-loco em uma caixa de correio excluída no Exchange Online

Saiba como criar um bloqueio In-loco para uma caixa de correio excluída para torná-la inativa e preservar o seu conteúdo. Em seguida, você pode usar ferramentas de descoberta eletrônica da Microsoft para pesquisar a caixa de correio inativa.
  
> [!NOTE]
> Podemos foi adiada o prazo 1 de julho de 2017 de criação de novos retenções locais no Exchange Online (em planos autônomos do Office 365 e o Exchange Online). Mas este ano ou próximo ano inicial, você não poderá criar novos retenções locais no Exchange Online. Como alternativa ao uso retenções locais, você pode usar [casos de descoberta eletrônica](https://go.microsoft.com/fwlink/?linkid=780738) ou [políticas de retenção](https://go.microsoft.com/fwlink/?linkid=827811) no Office 365 Security &amp; Centro de conformidade. Depois que o novo, podemos descomissionar retenções locais, você ainda poderá modificar existentes In-Place Holds e criação de novos retenções locais no Exchange Server 2013 e implantações híbridas do Exchange serão ainda suportadas. E, então, você ainda poderá colocar caixas de correio em retenção de litígio. 
  
Você pode ter uma situação em que uma pessoa tenha deixado a sua organização e sua conta de usuário correspondente e uma caixa de correio foram excluídos. Posteriormente, você percebe que não há informações na caixa de correio que precisa ser preservado. O que você pode fazer? Se o período de retenção de caixa de correio excluída não tiver expirado, você pode colocar um bloqueio In-loco na caixa de correio excluída (chamado de uma caixa de correio excluída) e torná-la uma caixa de correio inativa. Uma *caixa de correio inativa* é usado para preservação de emails de um antigo do funcionário depois que ele deixa a sua organização. O conteúdo de uma caixa de correio inativa é preservado para a duração de In-Place Hold foi é colocada na caixa de correio excluída quando ela foi feita inativa. Depois que a caixa de correio é feita inativa, você pode pesquisar a caixa de correio usando a descoberta eletrônica In-loco no Exchange Online, pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, ou o Centro de descoberta eletrônica no SharePoint Online. 
  
> [!NOTE]
> No Exchange Online, uma caixa de correio excluída é uma caixa de correio que tenha sido excluída, mas pode ser recuperada em um período de retenção específico. O período de retenção de caixa de correio excluída no Exchange Online é 30 dias. Isso significa que a caixa de correio pode ser recuperado (ou fez uma caixa de correio inativa) dentro de 30 dias do que está sendo excluído. Após 30 dias, uma caixa de correio excluída é marcada para exclusão permanente e não pode ser recuperada ou feita inativa. 
  
## <a name="before-you-begin"></a>Antes de começar
<a name="sectionSection0"> </a>

- Você precisa usar o cmdlet **New-MailboxSearch** no Windows PowerShell para colocar um bloqueio In-loco em uma caixa de correio excluída. É possível usar o Centro de administração do Exchange (EAC) ou o Centro de descoberta eletrônica no SharePoint Online. 
    
- Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira o artigo [Conectar-se ao Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Execute o seguinte comando para obter informações de identidade sobre as caixas de correio excluída na sua organização. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Para obter mais informações sobre caixas de correio inativas, consulte [caixas de correio inativas no Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Colocar um bloqueio In-loco em uma caixa de correio excluída para torná-la uma caixa de correio inativa
<a name="sectionSection1"> </a>

Use o cmdlet **New-MailboxSearch** para fazer uma caixa de correio excluída uma caixa de correio inativa. Para obter mais informações, consulte [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).
  
1. Crie uma variável que contém as propriedades da caixa de correio excluída. 
    
  ```
  $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
  ```

    > [!IMPORTANT]
    > No comando anterior, use o valor da propriedade **DistinguishedName** ou **ExchangeGuid** para identificar a caixa de correio excluída. Essas propriedades são exclusivas para cada caixa de correio em sua organização, enquanto que é possível que uma caixa de correio ativa e uma caixa de correio excluída podem ter o mesmo endereço SMTP principal. 
  
2. Criar um bloqueio In-loco e coloque-o na caixa de correio excluída. Neste exemplo, não há duração de espera é especificada. Isso significa que os itens serão mantidos indefinidamente ou até que a suspensão seja removida da caixa de correio inativa.
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
  
  ```

    Você também pode especificar uma duração de espera quando você cria o bloqueio In-loco. Este exemplo contém os itens na caixa de correio inativa de aproximadamente sete anos.
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
  ```

3. Após alguns momentos, execute um dos seguintes comandos para verificar se a caixa de correio excluída é uma caixa de correio inativa.
    
  ```
  Get-Mailbox -InactiveMailboxOnly
  ```

    Ou
    
  ```
  Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
  ```

## <a name="more-information"></a>Mais informações
<a name="sectionSection2"> </a>

Depois de fazer uma caixa de correio excluída uma caixa de correio inativa, há várias maneiras que você pode gerenciar a caixa de correio. Para obter mais informações, consulte:
  
- [Alterar a duração de espera para uma caixa de correio inativa no Exchange Online](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [Recuperar uma caixa de correio inativa no Exchange Online](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [Restaurar uma caixa de correio inativa no Exchange Online](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [Remover uma isenção de uma caixa de correio inativa no Exchange Online](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    

