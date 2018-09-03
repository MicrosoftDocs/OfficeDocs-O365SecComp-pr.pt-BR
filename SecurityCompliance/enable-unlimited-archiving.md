---
title: Habilitar o arquivamento ilimitado no Office 365 - ajuda de Admin
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: 'Para administradores: Aprenda a habilitar o arquivamento de expansão automática no Office 365, que fornece aos usuários com armazenamento ilimitado para suas caixas de correio do Exchange Online. Você pode habilitar a expansão automática de arquivamento para toda sua organização ou apenas para usuários específicos.'
ms.openlocfilehash: ede3e75a021d750160268ccf06ac4fe1637d219a
ms.sourcegitcommit: 81c2fd5cd940c51bc43ac7858c7bdfa207ce401a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/03/2018
ms.locfileid: "23809696"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Habilitar o arquivamento ilimitado no Office 365 - ajuda de Admin

Você pode usar o recurso de arquivamento expansão automática Exchange Online no Office 365 para habilitar o espaço de armazenamento ilimitado para caixas de correio de arquivo morto. Quando a expansão automática de arquivamento é ativada, espaço de armazenamento adicional é adicionado automaticamente à caixa de correio de arquivo morto do usuário quando o limite de armazenamento que se aproxima. O resultado é a capacidade de armazenamento de caixa de correio ilimitado. Você pode ativar expansão automática de arquivamento para todos em sua organização ou apenas para usuários específicos. Para obter mais informações sobre a expansão automática arquivamento, consulte [Overview of arquivamento ilimitado no Office 365](unlimited-archiving.md).

## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser um administrador global na sua organização do Office 365 ou um membro do grupo de função do gerenciamento da organização em sua organização do Exchange Online para habilitar o arquivamento de expansão automática para toda sua organização ou para usuários específicos. Como alternativa, você precisa ser membro de um grupo de função que atribuiu a função destinatários de email para habilitar a expansão automática de arquivamento para usuários específicos.
    
- Caixa de correio de arquivo morto do usuário deve estar habilitado para poder habilitar expansão automática de arquivamento. Uma licença do Exchange Online plano 2 para habilitar a caixa de correio de arquivo morto deve ser atribuído a um usuário. Se um usuário é atribuído com uma licença do Exchange Online plano 1, você teria para atribuí-las uma licença separada de arquivamento do Exchange Online para habilitar suas caixas de correio de arquivo morto. Consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md).
    
- Você também pode usar o PowerShell para habilitar o arquivamento de caixas de correio. Consulte a seção de [informações adicionais](#more-information) para obter um exemplo do comando do PowerShell que você pode usar para habilitar o arquivamento de caixas de correio para todos os usuários em sua organização. 
    
- Expansão automática arquivamento também oferece suporte a caixas de correio compartilhadas. Para habilitar o arquivamento para uma caixa de correio compartilhada, é necessária uma licença do Exchange Online plano 2 ou uma licença do Exchange Online plano 1 com uma licença de arquivamento do Exchange Online.
    
- Você não pode usar o Centro de administração do Exchange ou a segurança &amp; Centro de conformidade para habilitar o arquivamento de expansão automática. Você tem que usar o PowerShell do Exchange Online. Para conectar à sua organização do Exchange Online usando o PowerShell remoto, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>Habilitar o arquivamento de expansão automática para toda sua organização

Você pode habilitar a expansão automática arquivamento para toda sua organização. Depois que você ativá-lo, expansão automática arquivamento será habilitado para caixas de correio de usuário existentes e novas caixas de correio do usuário que são criadas. Quando você cria novas caixas de correio do usuário, certifique-se de habilitar a caixa de correio de arquivo morto principal do usuário para que o recurso de arquivamento expansão automática funcionará para a nova caixa de correio do usuário.
  
1. [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Execute o seguinte comando no PowerShell do Exchange Online para habilitar a expansão automática arquivamento para toda sua organização.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>Habilitar o arquivamento de expansão automática para usuários específicos

Em vez de habilitar a expansão automática de arquivamento para cada usuário em sua organização, você poderá habilitá-lo apenas para usuários específicos. Você pode fazer isso porque apenas alguns usuários podem ter uma necessidade para um armazenamento de arquivo morto muito grande.
  
Quando você habilita a expansão automática de arquivamento para um usuário específico e caixa de correio do usuário em espera ou atribuído a uma política de retenção do Office 365, as alterações de duas configurações a seguir são feitas:
  
- A cota de armazenamento de caixa de correio de arquivo morto principal do usuário é aumentada pelo 10 GB (de 100 GB para 110 GB). A cota de aviso de arquivamento também é aumentada pelo 10 GB (de 90 GB para 100 GB).
    
- A cota de armazenamento para a pasta itens recuperáveis na caixa de correio principal do usuário é aumentada pelo 10 GB (além de 100 GB para 110 GB). A cota de aviso de itens recuperáveis também é aumentada pelo 10 GB (de 90 GB para 100 GB). Essas alterações são aplicáveis somente se a caixa de correio em espera ou atribuído a uma política de retenção do Office 365.
    
Esse espaço adicional é adicionado para evitar problemas de armazenamento que podem ocorrer antes do arquivamento de expansão automática está provisionado. Observe que armazenamento adicional espaço *não é* adicionado quando você habilita a expansão automática arquivamento para toda sua organização, conforme descrito na seção anterior. 
  
1. [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Execute o seguinte comando no PowerShell do Exchange Online para habilitar a expansão automática de arquivamento para um usuário específico. Conforme explicado anteriormente, o correio de arquivo morto do usuário (arquivo principal) deve estar habilitado antes de ativar o arquivamento para esse usuário expansão automática.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> Em uma implantação híbrida do Exchange, você não pode usar o comando **Enable-Mailbox-AutoExpandingArchive** para habilitar o arquivamento para específicos um usuário cuja caixa de correio primária está no local expansão automática e suas caixas de correio de arquivo morto é baseado em nuvem. Para habilitar a expansão automática arquivamento para caixas de correio de arquivamento baseado em nuvem em uma implantação híbrida do Exchange, você precisará executar o comando **Set-OrganizationConfig-AutoExpandingArchive** o PowerShell para habilitar a expansão automática de arquivamento para no Exchange Online toda a organização. Se um usuário principal da e caixas de correio de arquivo morto são ambos baseada na nuvem, você pode usar o comando **Enable-Mailbox-AutoExpandingArchive** para habilitar o arquivamento de expansão automática para esse usuário específico. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>Verificar se o arquivamento de expansão automática está habilitada

Para verificar se o arquivamento de expansão automática está habilitada para sua organização, execute o seguinte comando no PowerShell do Exchange Online.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

Um valor de `True` indica que o arquivamento de expansão automática está habilitada para a organização. 
  
Para verificar que a expansão automática de arquivamento é habilitar para um usuário específico, execute o seguinte comando no PowerShell do Exchange Online.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
Um valor de `True` indica que o arquivamento de expansão automática está habilitada para o usuário. 
  
Depois que você habilitar o arquivamento de expansão automática, mantenha as seguintes coisas em mente:
  
- Se você executar o comando **Set-OrganizationConfig-AutoExpandingArchive** para habilitar a expansão automática de arquivamento para sua organização, você não precisa executar o **Enable-Mailbox-AutoExpandingArchive** em caixas de correio individuais. Observe que o cmdlet **Set-OrganizationConfig** para habilitar a expansão automática de arquivamento para sua organização não altera a propriedade *AutoExpandingArchiveEnabled* em caixas de correio de usuário para execução `True`.
    
- Da mesma forma, os valores para as propriedades de caixa de correio de *ArchiveQuota* e *ArchiveWarningQuota* não são alterados quando você habilita a expansão automática de arquivamento. Na verdade, quando você habilita o arquivamento de expansão automática para uma caixa de correio do usuário e a propriedade *AutoExpandingArchiveEnabled* estiver definida como `True`, as propriedades *ArchiveQuota* e *ArchiveWarningQuota* apenas serão ignoradas. Aqui está um exemplo dessas propriedades de caixa de correio após a expansão automática de arquivamento estiver habilitado para caixa de correio do usuário. 
    
    ![Propriedades ArchiveQuota e ArchiveWarningQuota são ignoradas após habilitar a expansão automática de arquivamento](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>Mais informações

- Você também pode usar o PowerShell para habilitar o arquivamento de caixas de correio. Por exemplo, você pode executar o seguinte comando no Exchange Online PowerShell para habilitar caixas de correio de arquivamento para todos os usuários cuja caixa de correio de arquivo morto já não estiver habilitada.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- Depois que você ativa arquivamento para sua organização ou para um usuário específico expansão automática, uma caixa de correio de arquivo morto é convertida em um arquivo morto expansão automática quando a caixa de correio de arquivo morto (incluindo a pasta itens recuperáveis) atinge 90 GB. Pode levar até 30 dias para o espaço de armazenamento adicional a ser provisionado.
    
- Depois que você ativa arquivamento expansão automática, ele não pode ser desativado.
    
- Expansão automática de arquivamento é suportado para caixas de correio de arquivamento baseado em nuvem em uma implantação híbrida do Exchange para usuários que possuem uma caixa de correio principal no local. No entanto, após a expansão automática de arquivamento estiver habilitado para uma caixa de correio de arquivamento baseado em nuvem, você não pode desativar-placa essa caixa de correio de arquivo morto volta para a organização do Exchange local.
    
- Para obter uma lista de clientes do Outlook que os usuários podem usar para acessar itens na área de armazenamento adicional na sua caixa de correio de arquivo morto, consulte a seção "Requisitos do Outlook para acessar os itens em um arquivo morto autoexpandida" no [Overview of ilimitado arquivamento no Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) .
    
- Conforme explicado anteriormente, 10 GB é adicionada à cota de armazenamento de caixa de correio de arquivo morto principal do usuário (e para a pasta itens recuperáveis se a caixa de correio estiver em espera) ao executar o comando **Enable-Mailbox-AutoExpandingArchive** . Isso oferece armazenamento adicional até que o espaço de armazenamento de autoexpandida é provisionado (que pode demorar até 30 dias). Esse espaço de armazenamento adicional não será adicionado ao executar o **Set-OrganizationConfig-AutoExpandingArchive** para habilitar o arquivamento de expansão automática para todas as caixas de correio em sua organização. Se habilitado a expansão automática de arquivamento para toda a organização, mas precisa adicionar o adicional 10 GB de espaço de armazenamento para um usuário específico, você pode executar o comando **Enable-Mailbox-AutoExpandingArchive** essa caixa de correio. Observe que você receberá uma mensagem de erro informando que a expansão automática de arquivamento já tiver sido habilitado, mas o espaço de armazenamento adicional será adicionado à caixa de correio. 
