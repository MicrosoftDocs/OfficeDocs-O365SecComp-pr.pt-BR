---
title: Aumentar a cota de Itens Recuperáveis para caixas de correio em espera
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Habilite a caixa de correio de arquivo morto e ativar o arquivamento para aumentar o tamanho da pasta itens recuperáveis para uma caixa de correio no Office 365 expansão automática. '
ms.openlocfilehash: a347155645d7c058080b1db7fd47f7ea16249724
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522272"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>Aumentar a cota de Itens Recuperáveis para caixas de correio em espera

A política de retenção padrão — denominada política MRM padrão — isto é automaticamente aplicadas para novas caixas de correio no Exchange Online contém uma marca de retenção nomeados dias de 14 de itens recuperáveis mover para arquivo morto. Nesta marca de retenção move itens da pasta itens recuperáveis na caixa de correio principal do usuário para a pasta itens recuperáveis na caixa de correio de arquivo morto do usuário depois que o período de retenção de 14 dias expira para um item. Para isso acontecer, a caixa de correio de arquivo morto do usuário deve ser habilitada. Se a caixa de correio de arquivo morto não estiver habilitada, nenhuma ação é executada, que significa que itens em que a pasta para uma caixa de correio em retenção de itens recuperáveis não foram movidas para a caixa de correio de arquivo morto após o período de retenção de 14 dias expirar. Como nothing é excluído de uma caixa de correio em espera, é possível que a cota de armazenamento para a pasta itens recuperáveis pode ser excedida, especialmente se a caixa de correio de arquivo morto do usuário não está habilitada. 
  
Para ajudar a reduzir a chance de exceder esse limite, a cota de armazenamento para a pasta itens recuperáveis é automaticamente aumentou de 30 GB para 100 GB quando uma isenção for colocada em uma caixa de correio no Exchange Online. Se a caixa de correio de arquivo morto estiver habilitada, a cota de armazenamento para a pasta itens recuperáveis na caixa de correio de arquivamento também é aumentada de 30 GB para 100 GB. Se o arquivamento de expansão automática de recurso no Exchange Online é habilitada, a cota de armazenamento para a pasta itens recuperáveis no arquivo do usuário será ilimitada.
  
  A tabela a seguir resume a cota de armazenamento da pasta Itens Recuperáveis. 
  
|**Local da pasta Itens Recuperáveis**|**Caixas de correio não em espera**|**Caixas de correio em espera**|
|:-----|:-----|:-----|
|Caixa de correio principal  <br/> |30 GB  <br/> |100 GB  <br/> |
|Caixa de correio de arquivo morto<sup>\*</sup> <br/> |Ilimitado  <br/> |Ilimitado  <br/> |
|**Cota de armazenamento total para a pasta Itens Recuperáveis** <br/> |Ilimitado  <br/> |Ilimitado  <br/> |
   
> [!NOTE]
> <sup>\*</sup>A cota de armazenamento inicial para a caixa de correio de arquivo morto é de 100 GB para usuários com uma licença do Exchange Online (plano 2). No entanto, quando a expansão automática de arquivamento é ativada para caixas de correio em espera, a cota de armazenamento para a caixa de correio de arquivo morto e a pasta itens recuperáveis é aumentada para 110 GB. Espaço de armazenamento de arquivo morto adicional será provisionado quando necessário que resulta em uma quantidade ilimitada de armazenamento de arquivamento. Para obter mais informações sobre a expansão automática arquivamento, consulte [Overview of arquivamento ilimitado no Office 365](unlimited-archiving.md). 
  
Quando a cota de armazenamento da pasta Itens Recuperáveis na caixa de correio principal de uma caixa de correio em espera está quase atingindo o limite, você pode fazer o seguinte:
  
- **Habilitar a caixa de correio de arquivo morto e ativar o arquivamento expansão automática** - você pode habilitar uma capacidade de armazenamento ilimitado para a pasta itens recuperáveis simplesmente com a habilitação da caixa de correio de arquivo morto e, em seguida, ativem o recurso de arquivamento expansão automática no Exchange Online. Isso resulta em 110 GB para a pasta itens recuperáveis na caixa de correio primária e uma quantidade ilimitada de capacidade de armazenamento para a pasta itens recuperáveis no arquivo do usuário. Consulte como: [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).
    
    > [!NOTE]
    > Depois de habilitar o arquivamento para uma caixa de correio que está prestes a exceder a cota de armazenamento para a pasta itens recuperáveis, talvez você queira executar o Assistente de pasta gerenciada para disparar manualmente o Assistente para processar a caixa de correio, para que os itens expirados são movidos do Pasta itens recuperáveis na caixa de correio de arquivo morto. Para obter instruções, consulte a [etapa 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Observe que os outros itens na caixa de correio do usuário podem ser movidos para a nova caixa de correio de arquivo morto. Considere informando ao usuário que isso pode acontecer depois de habilitar a caixa de correio de arquivo morto. 
  
- **Criar uma política de retenção personalizada para caixas de correio em espera** - além de habilitar a caixa de correio de arquivo morto e arquivamento de caixas de correio em retenção de litígio ou bloqueio In-loco, expansão automática também convém criar uma política de retenção personalizada para caixas de correio em espera. Isso vamos você aplicar uma política de retenção a caixas de correio em espera é diferente da política MRM padrão que é aplicado a caixas de correio que não estão em espera. Isso permite que você para aplicar marcas de retenção projetados especificamente para caixas de correio em espera. Isso inclui a criação de uma nova marca de retenção para a pasta itens recuperáveis. 
    
O restante deste tópico descreve os procedimentos passo a passo para criar uma política de retenção personalizada para caixas de correio em espera.
  
[Etapa 1: criar uma marca de retenção personalizada para a pasta Itens Recuperáveis](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[Etapa 2: criar uma nova política de retenção para caixas de correio em espera](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[Etapa 3: Aplicar a nova política de retenção a caixas de correio em espera](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[(Opcional) Etapa 4: executar o Assistente de Pasta Gerenciada para aplicar as novas configurações de retenção](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>Etapa 1: Criar uma marca de retenção personalizada para a pasta Itens Recuperáveis

A primeira etapa é criar uma marca de retenção personalizados (chamada de uma marca de política de retenção ou RPT) para a pasta itens recuperáveis. Conforme explicado anteriormente, este RPT move itens da pasta itens recuperáveis na caixa de correio principal do usuário para a pasta itens recuperáveis na caixa de correio de arquivo morto do usuário. Você precisa usar o PowerShell para criar um RPT para a pasta itens recuperáveis. Você não pode usar o Centro de administração do Exchange (EAC). 
  
1. [Conectar-se ao Exchange Online usando o PowerShell remoto](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. Execute o seguinte comando para criar um novo relatório para a pasta Itens Recuperáveis:  
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    Por exemplo, o comando a seguir cria um relatório para a pasta Itens Recuperáveis denominado "Itens Recuperáveis para caixas de correio em retenção: 30 dias", com um período de retenção de 30 dias. Isso significa que depois que um item estiver na pasta Itens Recuperáveis por 30 dias, ele será movido para a pasta Itens Recuperáveis na caixa de correio de arquivo morto do usuário.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > É recomendável que o período de retenção (definido pelo parâmetro _AgeLimitForRetention_ ) para o RPT itens recuperáveis é o mesmo que o período de retenção de itens excluídos para as caixas de correio que será aplicada a RPT para. Isso permite que um usuário o período de retenção de item excluído inteira para recuperar itens excluídos antes que eles serão movidos para a caixa de correio de arquivo morto. No exemplo anterior, o período de retenção foi definido como 30 dias, com base na pressuposição de que o período de retenção de itens excluídos para caixas de correio também é 30 dias. Uma caixa de correio do Exchange Online é configurada para reter itens excluídos 14 dias, por padrão. Mas você pode alterar essa configuração para um máximo de 30 dias. Para obter mais informações, consulte [alterar o período de retenção de item excluído de uma caixa de correio no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940). 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>Etapa 2: Criar uma nova política de retenção para caixas de correio em espera

A próxima etapa é criar uma nova política de retenção e adicionar marcas de retenção a ela, inclusive o RPT de Itens Recuperáveis que você criou na Etapa 1. Essa nova política será aplicada às caixas de correio em espera na próxima etapa.  
  
Antes de criar a nova política de retenção, determine as marcas de retenção adicionais que você deseja adicionar. Confira a lista das marcas de retenção adicionadas à política MRM Padrão e informações sobre como criar novas marcas de retenção em:
  
- [Padrão política de retenção no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [Pastas padrão que suportam marcas de diretiva de retenção](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- A seção "Criar uma marca de retenção" no tópico [criar uma política de retenção](https://go.microsoft.com/fwlink/p/?LinkId=404422) .
    
Você pode usar o EAC ou o Exchange Online PowerShell para criar uma política de retenção.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>Usar o EAC para criar uma política de retenção
  
1. No EAC, vá até **gerenciamento de conformidade** \> **políticas de retenção**e, em seguida, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).
    
2. Na página **Nova política de retenção**, em **Nome**, digite um nome que descreva o propósito da política de retenção, por exemplo, **MRM Policy for Mailboxes on Hold**.  
    
3. Em **marcas de retenção**, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).
    
4. Na lista de marcas de retenção, selecione o relatório de itens recuperáveis que você criou na Etapa 1 e clique em **Adicionar**.
    
    ![Selecione a marca de retenção personalizada Itens Recuperáveis](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. Selecione marcas de retenção adicionais para adicionar à política de retenção. Por exemplo, convém adicionar as mesmas marcas que são incluídas na Política de MRM Padrão.
    
6. Quando terminar de adicionar marcas de retenção, clique em **OK**.
    
7. Clique em **Salvar** para criar a nova política de retenção.  
    
    Observe que as marcas de retenção vinculadas à política de retenção são exibidas no painel de detalhes.
    
    ![Marcas de retenção vinculadas à política de retenção são exibidas no painel de detalhes](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Use o PowerShell do Exchange Online para criar uma política de retenção
  
Execute o comando a seguir para criar a nova política de retenção para caixas de correio em espera.  
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

Por exemplo, o comando a seguir cria a política de retenção e as marcas de retenção vinculadas que são exibidas na ilustração anterior.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>Etapa 3: Aplicar a nova política de retenção a caixas de correio em espera

A última etapa é aplicar a nova política de retenção que você criou na etapa 2 para caixas de correio em espera em sua organização. Você pode usar o EAC ou o Exchange Online PowerShell para aplicar a política de retenção para uma única caixa de correio ou para várias caixas de correio. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>Usar o EAC para aplicar a nova política de retenção
  
1. Acesse **Destinatários** \> **Caixas de Correio**.
    
2. Na exibição de lista, selecione a caixa de correio que você deseja aplicar a política de retenção e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Na página **Caixa de Correio do Usuário**, clique em **Recursos de caixa de correio**.
    
4. Em **Política de retenção**, selecione a política de retenção que você criou na Etapa 2 e clique em **Salvar**.
    
Você também pode usar o EAC para aplicar a política de retenção a várias caixas de correio.
  
1. Acesse **Destinatários** \> **Caixas de Correio**.
    
2. No modo de exibição de lista, use as teclas Shift ou Ctrl, para selecionar várias caixas de correio.
    
3. No painel de detalhes, clique em **Mais opções**.
    
4. Em **Política de Retenção**, clique em **Atualizar**.
    
5. Na página **Atribuir em massa uma política de retenção**, selecione a política de retenção que você criou na Etapa 2 e clique em **Salvar**.  
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Use o PowerShell do Exchange Online para aplicar a nova política de retenção
  
Você pode usar o PowerShell do Exchange Online para aplicar uma nova política de retenção a uma única caixa de correio. Mas o poder real do PowerShell é que você pode usá-lo a identificar rapidamente todas as caixas de correio em sua organização que estão na lista litígio ou bloqueio In-loco e aplicam a nova política de retenção para todas as caixas de correio em espera em um único comando. Aqui estão alguns exemplos de como usar o PowerShell do Exchange para aplicar uma política de retenção a uma ou mais caixas de correio. Todos os exemplos de aplicam a política de retenção que foi criada na etapa 2.
  
Este exemplo aplica a nova política de retenção à caixa de correio de Clara Barbosa.
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Este exemplo aplica a nova política de retenção a todas as caixas de correio na organização que estão em Retenção de Litígio.
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Este exemplo aplica a nova política de retenção a todas as caixas de correio na organização que estão em Bloqueio In-loco.
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Você pode usar o cmdlet **Get-Mailbox** para verificar se a nova política de retenção foi aplicada. 
  
Aqui estão alguns exemplos para verificar se os comandos nos exemplos anteriores aplicaram a "Política MRM a caixas de correio em espera" em caixas de correio em Retenção de Litígio e caixas de correio em Bloqueio In-loco.
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a>(Opcional) Etapa 4: Executar o Assistente de Pasta Gerenciada para aplicar as novas configurações de retenção

Depois de aplicar a nova política de retenção a caixas de correio em espera, pode demorar até sete dias no Exchange Online para o Assistente de pasta gerenciada processar essas caixas de correio usando as configurações da nova política de retenção. Em vez de esperar executar o Assistente de pasta gerenciada, você pode usar o cmdlet **Start-ManagedFolderAssistant** para acionar manualmente o Assistente para processar as caixas de correio que você aplicou a nova política de retenção para. 
  
Execute o comando a seguir para iniciar o Assistente de Pasta Gerenciada para caixa de correio de Clara Barbosa.
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

Execute os comandos a seguir para iniciar o Assistente de Pasta Gerenciada para todas as caixas de correio em espera.
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a>Mais informações

- Após habilitar a caixa de correio de arquivo morto do usuário, considere informando ao usuário que outros itens em suas caixas de correio (não apenas itens na pasta itens recuperáveis) podem ser movidos para a caixa de correio de arquivo morto. Isto ocorre porque a política MRM padrão atribuído às caixas de correio Exchange Online contém uma marca de retenção (nomeada padrão para a 2 anos movem para arquivo morto) que move itens na caixa de correio de arquivo morto dois anos após a data em que o item foi entregue à caixa de correio ou criado pela usuário. Para obter mais informações, consulte a [Política de retenção padrão no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- Após habilitar a caixa de correio de arquivo morto do usuário, você também pode instruir o usuário que eles podem recuperar os itens excluídos na pasta itens recuperáveis em suas caixas de correio de arquivo morto. Eles podem fazer isso no Outlook, selecionando a pasta **Itens excluídos** na caixa de correio de arquivo morto e, em seguida, clicando em **Recuperar itens excluídos do servidor** , na guia **página inicial** . Para obter mais informações sobre a recuperação de itens excluídos, consulte [que recuperar itens excluídos no Outlook para Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829). 
