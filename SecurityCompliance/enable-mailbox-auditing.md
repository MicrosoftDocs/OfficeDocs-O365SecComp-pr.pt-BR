---
title: Gerenciar a auditoria de caixa de correio
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: O registro em log de auditoria de caixa de correio é ativado por padrão no Microsoft 365 (também chamado de auditoria de caixa de correio padrão ou de caixa de correio ativada por padrão). Isso significa que determinadas ações executadas por proprietários de caixa de correio, representantes e administradores são automaticamente registrados em um log de auditoria de caixa de correio, onde você pode pesquisar atividades realizadas na caixa de correio.
ms.openlocfilehash: 38632798aedfa34ee7568a7038d5ff906888619c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256979"
---
# <a name="manage-mailbox-auditing"></a>Gerenciar a auditoria de caixa de correio
  
A partir de janeiro de 2019, a Microsoft está ativando o log de auditoria de caixa de correio por padrão para todas as organizações 365 da Microsoft. Isso significa que determinadas ações executadas por proprietários, representantes e administradores de caixa de correio são automaticamente registradas, e os registros de auditoria de caixa de correio correspondentes estarão disponíveis quando você procurá-los no log de auditoria de caixa de correio. Antes de a auditoria da caixa de correio ser ativada por padrão, você precisava habilitá-la manualmente para cada caixa de correio de usuário em sua organização. 

Estes são alguns benefícios da auditoria de caixa de correio ativada por padrão:

- A auditoria será habilitada por padrão quando você criar uma nova caixa de correio. Você não precisará habilitá-lo manualmente para novos usuários. 

- Você não terá o gerenciamento das ações da caixa de correio que são auditadas. Um conjunto definido de ações de caixa de correio é auditado por padrão para cada tipo de logon. Esses [tipos de logon](#mailbox-actions-logged-by-default) são proprietário, representante e administrador.

- Novas ações de caixa de correio lançadas pela Microsoft serão auditadas por padrão. Quando a Microsoft lança uma nova ação de caixa de correio (particularmente as que ajudam a proteger sua organização e a ajudar com investigações jurídicas), elas serão automaticamente adicionadas à lista de ações de caixa de correio auditadas por padrão. Isso significa que você não precisa adicionar novas ações à lista de ações de caixa de correio executadas por proprietários, representantes ou administradores. 

- Certifique-se de que você está auditando as mesmas ações para todas as caixas de correio para ter uma diretiva de auditoria de caixa de correio consistente em sua organização.

> [!TIP]
> O importante a ser lembrado é que, com o lançamento da auditoria de caixa de correio ativa por padrão, não é necessário fazer nada para gerenciar a auditoria de caixa de correio. No enTanto, se você quiser saber mais, alterar o comportamento das configurações padrão ou desativá-la completamente, este artigo pode ajudá-lo com isso.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>Verificar se a auditoria de caixa de correio está ativada por padrão

Para verificar se a auditoria de caixa de correio ativa por padrão está ativada para sua organização, execute o seguinte comando no [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):

```
Get-OrganizationConfig | FL AuditDisabled
``` 

Um valor **false** indica que a auditoria da caixa de correio ativa por padrão está habilitada para sua organização. 

Quando a auditoria de caixa de correio ativada por padrão é ativada (quando a propriedade *AuditDisabled* é definida como **false**), a configuração organizacional substituirá a configuração de auditoria de caixa de correio para uma caixa de correio específica. Por exemplo, se a propriedade *AuditEnabled* de uma caixa de correio estiver definida como **false**, mas a auditoria de caixa de correio ativada por padrão para sua organização, as ações de caixa de correio padrão serão auditadas para essa caixa de correio. Se a auditoria de caixa de correio foi explicitamente desabilitada para uma caixa de correio específica e você ainda deseja desativá-la, é possível configurar o bypass de auditoria de caixa de correio para o proprietário da caixa de correio e outros usuários com acesso delegado à caixa de correio. Para obter mais informações, consulte a seção [ignorar o log de auditoria de caixa de correio](#bypass-mailbox-audit-logging) neste artigo.

> [!NOTE]
> Quando a auditoria de caixa de correio ativa por padrão, a propriedade *AuditEnabled* de uma caixa de correio não será alterada para **true** se tiver sido definida como **false**no momento. Em outras palavras, a auditoria de caixa de correio ativada por padrão ignora a propriedade *AuditEnabled* de uma caixa de correio.

## <a name="supported-mailbox-types"></a>Tipos de caixa de correio suportados

A tabela a seguir mostra os tipos de caixa de correio com suporte no momento pela auditoria de caixa de correio ativada por padrão:

|Tipo de caixa de correio|Com suporte|Sem suporte|
|:---------|:---------:|:---------:|
|Caixas de correio de usuário    |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         |
|Caixas de correio compartilhadas    |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |       |
|Caixas de correio de grupo do Office 365    |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)         |         |
|Caixas de correio de recurso    |      |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |
|Caixas de correio de pastas públicas    |       |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)  |
||||

## <a name="mailbox-actions-logged-by-default"></a>Ações de caixa de correio registradas por padrão

Um conjunto de ações de caixa de correio é registrado por padrão para cada um dos seguintes tipos de logon:  

   - **Proprietário** -o proprietário da caixa de correio. 
   
   - **Representante** -outro usuário ao qual foi atribuída a permissão SendAs, SendOnBehalf ou FullAccess à caixa de correio de uma pessoa. Observe que um administrador que foi atribuído a permissão FullAccess para a caixa de correio de um usuário também é considerado um usuário representante.
   
    - **Admin** -as caixas de correio são consideradas acessadas por um tipo de logon de administrador somente nos seguintes cenários:
    
       - Quando uma caixa de correio é pesquisada com uma das seguintes ferramentas de descoberta eletrônica da Microsoft: 

         - Pesquisa de conteúdo no centro de conformidade.
       
         -  Descoberta eletrônica ou descoberta eletrônica avançada no centro de conformidade.
       
         - Descoberta eletrônica in-loco no Exchange Online.
       - Quando o [Editor MAPI do Microsoft Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=204086) é usado para acessar a caixa de correio.     

A tabela a seguir lista as ações de caixa de correio atualmente registradas por padrão para cada tipo de logon.

|Ações de administrador|Ações de representante|Ações do proprietário|
|:---------|:---------|:---------|
|Criar    |Criar       | HardDelete        |
|HardDelete    |HardDelete        |MoveToDeletedItems       |
|MoveToDeletedItems    |MoveToDeletedItems         |SoftDelete         |
|SendAs    |SendAs      |    Atualizar     |
|SendOnBehalf    |SendOnBehalf       |UpdateCalendarDelegation        |
|SoftDelete     |SoftDelete      | UpdateFolderPermissions        |
|Atualizar    |Atualizar       |UpdateInboxRules         |
|UpdateCalendarDelegation    | UpdateFolderPermissions        |         |
|UpdateFolderPermissions     | UpdateInboxRules        |         |
|UpdateInboxRules     |         |         |
||||

Aqui estão as descrições para essas ações de caixa de correio. 

|Ação de caixa de correio|Descrição|
|:---------|:---------|
|**Criar** <br/> |Um item foi criado na pasta calendário, contatos, anotações ou tarefas na caixa de correio; por exemplo, uma nova solicitação de reunião é criada. Observe que a criação, o envio ou o recebimento de uma mensagem não é auditado. Além disso, criar uma pasta de caixa de correio não é auditada.  <br/> |
|**HardDelete** <br/> |Uma mensagem foi removida da pasta de Itens Recuperáveis.  <br/> |
|**MoveToDeletedItems** <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |
|**SendAs** <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |
|**SendOnBehalf** <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |
|**SoftDelete** <br/> |Uma mensagem foi excluída permanentemente da pasta Itens Excluídos. Os itens excluídos temporariamente são movidos para a pasta Itens Recuperáveis.  <br/> |
|**Atualização** <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |
|**UpdateCalendarDelegation** <br/> |Uma delegação de calendário foi atribuída a uma caixa de correio. A delegação de calendário oferece a outra pessoa na mesma organização permissões para gerenciar o calendário do proprietário da caixa de correio.  <br/> |
|**UpdateFolderPermissions** <br/> |Uma permissão de pasta foi alterada. As permissões de pasta controlam quais usuários em sua organização podem acessar pastas em uma caixa de correio e as mensagens localizadas nessas pastas.  <br/> |
|**UpdateInboxRules** <br/> |Uma regra de caixa de entrada foi adicionada, removida ou alterada. As regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e realizar ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou excluir uma mensagem.  <br/> |
|||

Para obter uma lista completa de ações de caixa de correio, incluindo ações que estão disponíveis, mas não estão incluídas no conjunto de ações padrão, consulte a seção [ações de auditoria de caixa de correio](#mailbox-auditing-actions) neste artigo.

> [!IMPORTANT]
> Se você tiver configurado explicitamente as ações da caixa de correio para fazer a auditoria de qualquer tipo de logon antes de a auditoria da caixa de correio ativada por padrão para a organização, a configuração existente da caixa de correio terá precedência e não será substituída pela caixa de correio padrão ações descritas nesta seção. Se, a qualquer momento, você quiser reverter para as ações de caixa de correio padrão, poderá fazer isso executando o comando **Set-Mailbox-** defaultauditset. Para obter mais informações sobre como fazer isso, consulte a seção [restaurar as ações de caixa de correio padrão](#restore-the-default-mailbox-actions) neste artigo.

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>Verifique se as ações de caixa de correio padrão estão sendo registradas para cada tipo de logon

Com o lançamento da auditoria de caixa de correio ativada por padrão, uma nova ** propriedade de caixa de correio chamada defaultauditset foi adicionada. Esta propriedade indica se as ações de caixa de correio padrão (gerenciadas pela Microsoft) estão sendo auditadas para cada tipo de logon para uma caixa de correio especificada. Você pode executar o seguinte comando para exibir os valores dessa propriedade:

```
Get-Mailbox <username> | FL DefaultAuditSet
```

Um valor `Admin, Delegate, Owner` indica que as ações de caixa de correio padrão para todos os três tipos de logon estão sendo auditadas e que um administrador em sua organização *não* alterou as ações para qualquer tipo de logon. Observação Este é o estado padrão após a auditoria da caixa de correio ativada por padrão na sua organização. 

Se um administrador em sua organização tiver alterado as ações de caixa de correio que são auditadas para um tipo de logon (usando o cmdlet **Set-Mailbox** com os parâmetros *AuditAdmin*, *AuditDelegate*ou *AuditOwner* ), o valor para a ** Propriedade defaultauditset será diferente do valor padrão. Por exemplo, um valor de `Owner` indica que somente as ações de caixa de correio padrão para o proprietário da caixa de correio estão sendo auditadas e `Delegate` que `Admin` as ações para e foram alteradas. Se não houver valores exibidos para a propriedade ** defaultauditset (também chamada de valor *nulo* ), as ações de caixa de correio para todos os três tipos de logon foram alteradas.

Consulte a seção [alterar ou restaurar ações de caixa de correio registradas por padrão](#change-or-restore-mailbox-actions-logged-by-default) neste artigo para obter mais informações sobre como alterar as ações da caixa de correio que são auditadas.

### <a name="display-a-list-of-mailbox-actions-logged-by-default"></a>Exibir uma lista de ações de caixa de correio registradas por padrão

Você pode executar os seguintes comandos no PowerShell do Exchange Online para exibir a lista de ações de caixa de correio que estão atualmente em uma caixa de correio para cada tipo de logon:

**Ações do proprietário**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditOwner
```

**Ações de representante**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditDelegate
```

**Ações de administrador**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>Alterar ou restaurar ações de caixa de correio registradas por padrão

Como explicado anteriormente, um dos principais benefícios da auditoria de caixa de correio por padrão é que não é necessário gerenciar as ações de caixas de correio que são auditadas. A Microsoft faz isso para você e adicionará automaticamente novas ações de caixa de correio para serem auditadas por padrão ao serem lançadas. No enTanto, sua organização pode ter razões para auditar um conjunto de ações de caixa de correio que são diferentes dos padrões. Esta seção mostra como alterar as ações da caixa de correio que são auditadas para cada tipo de logon e como reverter de volta para as ações padrão gerenciadas pela Microsoft.

> [!IMPORTANT]
> Se você fizer qualquer alteração nas ações de caixa de correio para um usuário que está registrado por padrão (conforme descrito na próxima seção), todas as novas ações de caixa de correio lançadas pela Microsoft não serão auditadas para essas caixas de correio. Você terá que adicionar explicitamente uma nova ação de caixa de correio à lista de ações que são auditadas para um tipo de logon.

### <a name="change-the-mailbox-actions-to-audit"></a>Alterar as ações da caixa de correio para auditoria

Você pode usar o cmdlet **Set-Mailbox** com os parâmetros *AuditAdmin*, *AuditDelegate*ou *AuditOwner* para alterar as ações da caixa de correio que são auditadas, dependendo do tipo de logon. Como esses parâmetros relacionados à auditoria são parâmetros de vários valores (o que significa que podem ter mais de um valor), há duas maneiras diferentes de alterá-los.

- Você pode especificar várias ações de caixa de correio que substituem as ações existentes usando a `action1,action2,...actionN`seguinte sintaxe:.

- Você pode adicionar ou remover uma ou mais ações de caixa de correio sem afetar quaisquer registros existentes usando a seguinte `@{Add="action1","value2"}` sintaxe `@{Remove="action1","action2"}`: ou.

Independentemente de qual método você usa para alterar as ações de caixa de correio que são auditadas, as ações de caixa de correio auditadas por padrão (para o tipo de logon que você alterou) não serão mais gerenciadas pela Microsoft. Além disso, o valor do tipo de logon que você alterou não será exibido ** no parâmetro de caixa de correio defaultauditset [descrito anteriormente](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type).

Veja a seguir alguns exemplos de como usar um destes métodos para alterar as ações da caixa de correio para auditar cada um dos diferentes tipos de logon. 

Este exemplo altera as ações da caixa de correio de administrador substituindo as ações padrão por SoftDelete e HardDelete. 

```
Set-Mailbox <username> -AuditAdmin HardDelete,SoftDelete
```

Este exemplo adiciona a ação de proprietário MailboxLogin. 

```
Set-Mailbox <username> -AuditOwner @{Add="MailboxLogin"}
```

Este exemplo remove a ação de representante MoveToDeletedItems.

```
Set-Mailbox <username> -AuditDelegate @{Remove="MoveToDeletedItems"}
```

#### <a name="checking-the-defaultauditset-property"></a>Verificar a propriedade defaultAuditset

Após alterar as ações de caixa de correio padrão para um tipo de ** logon, a propriedade defaultauditset da caixa de correio será atualizada automaticamente para refletir essa alteração. Por exemplo, se você executar `Get-Mailbox <username> | FL DefaultAuditSet` a primeira vez que adicionar ou remover uma ação de proprietário de caixa de correio, o comando retornará um valor `Admin, Delegate`de. Isso indica que as ações de caixa de correio padrão do proprietário foram alteradas isso também significa que qualquer nova ação de proprietário de caixa de correio liberada pela Microsoft não será automaticamente adicionada a essa caixa de correio. O mesmo vale para alterar as ações de caixa de correio para o tipo de logon de representante ou administrador.

### <a name="restore-the-default-mailbox-actions"></a>Restaurar as ações de caixa de correio padrão

Se você fez alterações nas ações da caixa de correio que são auditadas para um tipo de logon, é possível restaurar as ações de caixa de correio padrão que `Set-Mailbox -DefaultAuditSet` são auditadas executando o comando. Ao fazer isso, ocorrerão as seguintes coisas:

- A lista atual de ações de caixa de correio será substituída pelas ações de caixa de correio padrão para o tipo de logon apropriado.
 
- Todas as novas ações de caixa de correio lançadas pela Microsoft serão automaticamente adicionadas à lista para o tipo de logon apropriado.

- A [propriedade de caixa de correio](#checking-the-defaultauditset-property) defaultauditset será atualizada para incluir o tipo de logon apropriado.

Para restaurar as ações de caixa de correio padrão para todos os tipos de logon, execute o seguinte comando:

```
Set-Mailbox <username> -DefaultAuditSet Admin,Delegate,Owner
```

Você pode usar esse comando para restaurar as ações de caixa de correio padrão para qualquer um dos tipos de logon (usando os valores **admin**, **delegate**ou **Owner** para o parâmetro defaultauditset.) **

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>Desativar a auditoria de caixa de correio por padrão para sua organização

Se, por algum motivo, sua organização decidir que não deseja auditar as ações da caixa de correio, você pode desativar a auditoria de caixa de correio por padrão para toda a sua organização, executando o seguinte comando no PowerShell do Exchange Online:

```
Set-OrganizationConfig -AuditDisabled $true
```

Quando a auditoria de caixa de correio ativada por padrão está desativada (a propriedade *AuditDisabled* é definida como **true**) para a organização, ocorrerá o seguinte:

- A auditoria de caixa de correio está desabilitada para sua organização.

- Nenhuma ação de caixa de correio será auditada (desde o momento em que a auditoria estiver desabilitada para a organização), mesmo que a propriedade *AuditEnabled* em uma caixa de correio esteja definida como **true**.

- A auditoria de caixa de correio não será habilitada para novas caixas de correio e a definição da propriedade *AuditEnabled* em uma nova caixa de correio (ou existente) como **true** será ignorada.

- Qualquer configuração de associação de bypass de auditoria de caixa de correio (configurada usando o cmdlet **Set-MailboxAuditBypassAssociation** ) será ignorada.

- Registros de auditoria de caixa de correio existentes serão mantidos até que o limite de idade do log de auditoria do registro expire.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>Habilitar a auditoria de caixa de correio por padrão

Para ativar novamente a auditoria de caixa de correio em sua organização, basta executar o seguinte comando no PowerShell do Exchange Online:

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>Ignorar log de auditoria de caixa de correio

No momento, não é possível desabilitar a auditoria de caixa de correio para caixas de correio específicas quando a auditoria de caixa de correio ativa por padrão em sua organização. Por exemplo, a definição da propriedade de caixa de correio *AuditEnabled* como **false** será ignorada.  No enTanto, você ainda pode usar o cmdlet **Set-MailboxAuditBypassAssociation** no PowerShell do Exchange Online para impedir que as ações de caixa de correio realizadas por usuários específicos sejam registradas. Quando você ignora a auditoria de caixa de correio, as ações de caixa de correio executadas por um usuário específico não são auditadas, independentemente da caixa de correio em que essas ações estão sendo executadas. Se você ignorar a auditoria de caixa de correio para um usuário específico, as ações do proprietário da caixa de correio realizadas por esse usuário não serão registradas. E, se esse mesmo usuário receber permissões para a caixa de correio de outro usuário (ou uma caixa de correio compartilhada), as ações de representante realizadas pelo primeiro usuário também não serão registradas.

Para ignorar o log de auditoria de caixa de correio para um usuário específico, execute o seguinte comando:

```
Set-MailboxAuditBypassAssociation -Identity <username> -AuditByPassEnabled $true
```

Para verificar se a auditoria foi ignorada para o usuário especificado, execute o seguinte comando:

```
Get-MailboxAuditBypassAssociation -Identity <username> | FL AuditByPassEnabled
```

Um valor **true** indica que o log de auditoria de caixa de correio é ignorado para esse usuário.

## <a name="mailbox-auditing-actions"></a>Ações de auditoria de caixa de correio
  
A tabela a seguir resume as ações que são auditadas para cada tipo de logon de usuário. Na tabela, um asterisco ( **\*** ) indica que a ação é registrada por padrão. Um **não** indica que uma ação não pode ser registrada para esse tipo de logon. Observe que um administrador ao qual foi atribuída a permissão de acesso total à caixa de correio de um usuário é considerado um usuário representante. 
  
|**Action**|**Descrição**|**Admin**|**Delegar**|**Owner**|
|:-----|:-----|:-----|:-----|:-----|
|**Copy** <br/> |Uma mensagem foi copiada a outra pasta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Create** <br/> |Um item é criado nas pastas Calendário, Contatos, Anotações ou Tarefas na caixa de correio; por exemplo, é criada uma nova solicitação de reunião. Observe que a criação, o envio ou o recebimento de uma mensagem não é auditado. Além disso, criar uma pasta de caixa de correio não é auditada.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**FolderBind**\** <br/> |Uma pasta da caixa de correio foi acessada. Esta ação também é registrada quando o administrador ou representante abrem a caixa de correio.  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|**HardDelete** <br/> |Uma mensagem foi removida da pasta de Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**MailboxLogin** <br/> |O usuário entrou em sua caixa de correio.  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|**MessageBind**\*** <br/> |Uma mensagem foi exibida no painel de visualização ou aberta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Move** <br/> |Uma mensagem foi movida para outra pasta.  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|**MoveToDeletedItems** <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**SendAs** <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SendOnBehalf** <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SoftDelete** <br/> |Uma mensagem foi excluída permanentemente da pasta Itens Excluídos. Os itens excluídos temporariamente são movidos para a pasta Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**Atualização** <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**UpdateCalendarDelegation** <br/> |Uma delegação de calendário foi atribuída a uma caixa de correio. A delegação de calendário permite que outra pessoa nas permissões da organização gerencie o calendário do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Não  <br/> |Sim\*  <br/> |
|**UpdateFolderPermissions** <br/> |Uma permissão de pasta foi alterada. As permissões de pasta controlam quais usuários em sua organização podem acessar pastas em uma caixa de correio e as mensagens localizadas nessas pastas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**UpdateInboxRules** <br/> |Uma regra de caixa de entrada foi adicionada, removida ou alterada. As regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e realizar ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou excluir uma mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Auditado por padrão quando a auditoria de caixa de correio padrão é habilitada para o tipo de logon. <br/><br/>  <sup>\*\*</sup>Os registros de auditoria para ações de associação de pastas executadas por representantes são consolidados. Um registro de auditoria é gerado para acesso a pastas individuais dentro de um período de 24 horas. <br/><br/> A ação MessageBind foi preterida no Exchange Online e não está mais disponível para ser adicionada à lista de ações de caixa de correio para o tipo de logon de administrador. <sup> \* \* \* </sup> 

## <a name="more-information"></a>Mais informações

- Por padrão, os registros de log de auditoria de caixa de correio são mantidos por 90 dias e depois excluídos. Você pode alterar o limite de idade para registros de log de auditoria usando o comando **Set-Mailbox-AuditLogAgeLimit** no PowerShell do Exchange Online. Observe que aumentar o limite de idade padrão para registros de auditoria de caixa de correio não afeta o limite de idade de 90 dias para registros de log de auditoria de caixa de correio no log de auditoria do Microsoft 365. Por exemplo, se você aumentar o limite de idade para registros de log de auditoria de caixa de correio para 365 dias, um registro de auditoria de caixa de correio poderá ser pesquisado no log de auditoria de 365 da Microsoft para apenas 90 dias após o evento correspondente ocorreu. Nesse caso, você teria que pesquisar o log de auditoria de caixa de correio do usuário em registros com mais de 90 dias. Para obter mais informações sobre como pesquisar logs de auditoria de caixa de correio, consulte [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog).

- Se você alterou a propriedade *AuditLogAgeLimit* para uma caixa de correio antes de a auditoria da caixa de correio ativada por padrão para a organização, o limite de idade do log de auditoria existente para essa caixa de correio não será alterado; em outras palavras, a auditoria de caixa de correio ativada por padrão não afeta o limite de idade atual para registros de auditoria de caixa de correio.

- Os registros de log de auditoria de caixa de correio são ** armazenados em uma subpasta (auditorias nomeadas) na pasta itens recuperáveis na caixa de correio de cada usuário. Considere os seguintes aspectos em relação aos registros de auditoria de caixa de correio e à pasta itens recuperáveis.
   
    - Os registros de auditoria de caixa de correio são considerados na cota de armazenamento da pasta itens recuperáveis, que é 30GB por padrão (a cota de aviso é de 20 GB). Observe que a cota de armazenamento da pasta itens recuperáveis é aumentada automaticamente de até 100 GB (cota de aviso de 90 MB) quando uma retenção é colocada em uma caixa de correio ou quando a caixa de correio é atribuída a uma política de retenção no centro de conformidade.

    - Os registros de auditoria de caixa de correio também são contados em relação ao limite da pasta [itens recuperáveis](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits). O número máximo de itens (que são registros de auditoria, nesse caso) que podem ser armazenados na subpasta Auditorias é de 3 milhões itens. 

      > [!NOTE]
      > É improvável que a auditoria de caixa de correio por padrão afete a cota de armazenamento ou o limite de pasta da pasta itens recuperáveis. 

    - Você pode executar o seguinte comando no PowerShell do Exchange Online para exibir o tamanho e o número de itens na subpasta auditorias da pasta itens recuperáveis: 
       ```
       Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | FL FolderPath,FolderSize,ItemsInFolder
       ```

     - Você não pode acessar diretamente um registro de log de auditoria na pasta itens recuperáveis; em vez disso, você usa o cmdlet **Search-MailboxAuditLog** ou pesquisa o Microsoft 365 Audit Log para localizar e exibir registros de auditoria de caixa de correio.

- Se uma caixa de correio for colocada em espera ou atribuída a uma política de retenção no centro de conformidade, os registros de log de auditoria ainda serão mantidos pela duração definida pela propriedade *AuditLogAgeLimit* para a caixa de correio (que é definida como 90 dias por padrão). Para manter os registros de log de auditoria mais longos para caixas de correio em espera, você precisa aumentar o período de retenção aumentando o valor da propriedade *AuditLogAgeLimit* .