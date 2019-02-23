---
title: Habilitar a auditoria de caixa de correio no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: No Office 365, você pode ativar o log de auditoria de caixa de correio para registrar o acesso à caixa de correio por proprietários de caixa de correio, representantes e administradores. Por padrão, a auditoria de caixa de correio no Office 365 não está ativada. Depois de habilitar o log de auditoria de caixa de correio para uma caixa de correio, você pode pesquisar o log de auditoria do Office 365 para atividades realizadas na caixa de correio.
ms.openlocfilehash: bb110e95d27feb8ae82b62803d218a2b38528692
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214601"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Habilitar a auditoria de caixa de correio no Office 365
  
No Office 365, você pode ativar o log de auditoria de caixa de correio para registrar o acesso à caixa de correio por proprietários de caixa de correio, representantes e administradores. Por padrão, a auditoria de caixa de correio no Office 365 não está ativada. Isso significa que os eventos de auditoria de caixa de correio não aparecerão nos resultados quando você pesquisar o log de auditoria do Office 365 para a atividade de caixa de correio. Mas depois de ativar o log de auditoria de caixa de correio para uma caixa de correio de usuário, você pode pesquisar no log de auditoria pela atividade de caixa de correio. Além disso, quando o registro em log de auditoria de caixa de correio está ativado, algumas ações executadas por administradores, representantes e proprietários são registradas por padrão. Para registrar (e, em seguida, Pesquisar) ações adicionais, consulte a etapa 3.

## <a name="before-you-begin"></a>Antes de começar
  
- Você precisa usar o PowerShell do Exchange Online para habilitar o log de auditoria de caixa de correio. Você não pode usar o centro de &amp; conformidade de segurança do Office 365 ou o centro de administração do Exchange.
    
- Não é possível habilitar o log de auditoria de caixa de correio para a caixa de correio associada a um grupo do Office 365 ou uma equipe no Microsoft Teams.
    
- Um administrador que recebeu a permissão de Acesso Completo à caixa de correio de um usuário é considerado um usuário representante.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>Etapa 1: conectar-se ao PowerShell do Exchange Online

1. Em seu computador local, abra o Windows PowerShell e execute o comando a seguir.
   
    ```
    $UserCredential = Get-Credential
    ```

2. Na caixa de diálogo **Solicitação de Credenciais do Windows PowerShell**, digite o nome de usuário e a senha de sua conta de administrador global do Office 365 e clique em **OK**.
    
3. Execute o seguinte comando:
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. Execute o seguinte comando.

    ```
    Import-PSSession $Session
    ```
   
4. Para verificar se você está conectado à sua organização do Exchange Online, execute o comando a seguir para obter uma lista de todas as caixas de correio de sua organização.
    
    ```
    Get-Mailbox
    ```
  
Para saber mais, ou se você tiver problemas para se conectar à sua organização do Exchange Online, confira [Conectar-se ao Exchange Online usando o PowerShell remoto](https://go.microsoft.com/fwlink/p/?LinkId=517283).
  
## <a name="step-2-enable-mailbox-audit-logging"></a>Etapa 2: Habilitar log de auditoria de caixas de correio

Depois de se conectar à sua organização do Exchange Online, use o PowerShell para habilitar o log de auditoria de caixa de correio para uma caixa de correio. Como alternativa, você pode habilitar a auditoria de caixa de correio para todas as caixas de correio em sua organização.
  
Este exemplo habilita o log de auditoria de caixa de correio para a caixa de correio de pilar Fernandes.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Esse exemplo habilita o log de auditoria de caixa de correio para todas as caixas de correio em sua organização.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Etapa 3: Especificar ações de proprietário para auditoria

Quando você habilita a auditoria para uma caixa de correio, algumas ações executadas pelo proprietário da caixa de correio são auditadas por padrão. É necessário especificar outras ações de proprietário para auditoria. Consulte a tabela na seção [ações de auditoria de caixa de correio](#mailbox-auditing-actions) para obter uma lista e descrição das ações de proprietário que são registradas por padrão e as outras ações que podem ser auditadas. 
  
Este exemplo adiciona as ações de proprietário **MailboxLogin** e **HardDelete** à auditoria de caixa de correio para a caixa de correio de pilar Fernandes. Este exemplo pressupõe que a auditoria de caixa de correio já foi habilitada para esta caixa de correio. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

Este exemplo habilita o log de auditoria de caixa de correio para a caixa de correio de Aníbal Sousa e especifica que somente a ação **MailboxLogin** executada pelo proprietário da caixa de correio será registrada. Observe que este exemplo substitui a ação padrão do UpdateFolderPermissions. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
Este exemplo adiciona as ações de proprietário **MailboxLogin**, **HardDelete**e **SoftDelete** a todas as caixas de correio na organização. Este exemplo pressupõe que a auditoria de caixa de correio já foi habilitada para todas as caixas de correio. 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se você habilitou o log de auditoria para uma caixa de correio, use o cmdlet **Get-Mailbox** para recuperar as configurações de auditoria dessa caixa de correio. 
  
Esse exemplo recupera as configurações de auditoria de Clara Barbosa.

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
Este exemplo recupera as configurações de auditoria de todas as caixas de correio em sua organização.

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
Um valor **true** para a propriedade **AuditEnabled** verifica se o log de auditoria de caixa de correio está habilitado. 
    
## <a name="mailbox-auditing-actions"></a>Ações de auditoria de caixa de correio
  
A tabela a seguir lista as ações que podem ser registradas pelo log de auditoria de caixa de correio. A tabela inclui quais ações podem ser registradas para os diferentes tipos de logon de usuário. Na tabela, um **não** indica que uma ação não pode ser registrada para esse tipo de logon. Um asterisco ( **\*** ) indica que a ação é registrada por padrão quando o log de auditoria de caixa de correio está habilitado para a caixa de correio. 
  
|**Action**|**Descrição**|**Administrador**|**Destino\*\*\***|**Proprietário**|
|:-----|:-----|:-----|:-----|:-----|
|**Copiar** <br/> |Uma mensagem foi copiada a outra pasta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Criar** <br/> |Um item é criado na pasta calendário, contatos, anotações ou tarefas na caixa de correio; por exemplo, uma nova solicitação de reunião é criada. Observe que a criação, o envio ou o recebimento de uma mensagem não é auditado. Além disso, criar uma pasta de caixa de correio não é auditada.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**FolderBind** <br/> |Uma pasta da caixa de correio foi acessada. Esta ação também é registrada quando o administrador ou representante abrem a caixa de correio.  <br/> |Sim  <br/> |Sim\*\*  <br/> |Não  <br/> |
|**HardDelete** <br/> |Uma mensagem foi removida da pasta de Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**MailboxLogin** <br/> |O usuário entrou em sua caixa de correio.  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|**MessageBind** <br/> |Uma mensagem foi exibida no painel de visualização ou aberta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Move** <br/> |Uma mensagem foi movida para outra pasta.  <br/> |Sim  <br/> |Sim   <br/> |Sim  <br/> |
|**MoveToDeletedItems** <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**SendAs** <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SendOnBehalf** <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SoftDelete** <br/> |Uma mensagem foi excluída permanentemente da pasta Itens Excluídos. Os itens excluídos temporariamente são movidos para a pasta Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**Atualizar** <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**UpdateCalendarDelegation** <br/> |Uma delegação de calendário foi atribuída a uma caixa de correio. A delegação de calendário oferece a outra pessoa na mesma organização permissões para gerenciar o calendário do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Não  <br/> |Sim\*  <br/> |
|**UpdateFolderPermissions** <br/> |Uma permissão de pasta foi alterada. As permissões de pasta controlam quais usuários em sua organização podem acessar pastas em uma caixa de correio e as mensagens localizadas nessas pastas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**UpdateInboxRules** <br/> |Uma regra de caixa de entrada foi adicionada, removida ou alterada. As regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e realizar ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou excluir uma mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Auditado por padrão se a auditoria estiver habilitada para uma caixa de correio.<br/><br/>  <sup>\*\*</sup>As entradas para ações de associação de pasta executadas pelos representantes são consolidadas. Uma entrada de log é gerada para acesso a pastas individuais dentro de um período de 24 horas.<br/><br/><sup>\*\*\*</sup>Um administrador que recebeu a permissão de acesso total à caixa de correio de um usuário é considerado um usuário representante. 
  
Se você não precisar mais de certos tipos de ações de caixa de correio a serem auditadas, modifique a configuração de log de auditoria da caixa de correio para desabilitar essas ações. As entradas de log existentes não serão limpas até que o limite de idade de retenção para entradas de log de auditoria seja atingido. Para obter mais informações sobre a idade de retenção para entradas de log de auditoria, consulte a seção "antes de começar" em [Pesquisar o log de auditoria no centro de conformidade do & de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md#before-you-begin).
  
## <a name="more-infotab"></a>[Mais informações](#tab/)
  
- Use o log de auditoria do Office 365 para pesquisar a atividade de caixa de correio que foi registrada. Você pode procurar atividade para uma caixa de correio de usuário específica. A captura de tela a seguir mostra uma lista de atividades de caixa de correio que você pode pesquisar no log de auditoria do Office 365. Observe que essas atividades são as mesmas descritas na seção "ações de auditoria de caixa de correio" neste tópico.
    
    ![Você pode pesquisar no log de auditoria do Office 365 para ações de auditoria de caixa de correio selecionando "atividades de caixa de correio do Exchange" na lista suspensa de atividades](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    A tabela a seguir descreve cada atividade de caixa de correio que você pode pesquisar e mostra a ação de auditoria de caixa de correio correspondente.
    
    |**Atividade no log de auditoria**|**Ação de auditoria de caixa de correio**|
    |:-----|:-----|
    |Item de caixa de correio criado  <br/> |Criar  <br/> |
    |Mensagens coPiadas para outra pasta  <br/> |Copiar  <br/> |
    |Usuário conectado à caixa de correio  <br/> |MailboxLogin  <br/> |
    |Mensagem enviada usando permissões Enviar em nome de  <br/> |SendOnBehalf  <br/> |
    |Mensagens limpas da caixa de correio  <br/> |HardDelete  <br/> |
    |Mensagens moVidas para a pasta itens excluídos  <br/> |MoveToDeletedItems  <br/> |
    |Mensagens moVidas para outra pasta  <br/> |Move  <br/> |
    |Mensagem enviada usando permissões Enviar como  <br/> |SendAs  <br/> |
    |Mensagem atualizada  <br/> |Atualizar  <br/> |
    |Mensagens excluídas da pasta itens excluídos  <br/> |SoftDelete  <br/> |
    |Permissões adicionadas à pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Permissões modificadas da pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Permissões reMovidas da pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Usuário adicionado ou removido com acesso de representante à pasta calendário  <br/> |UpdateCalendarDelegation  <br/> |
   
    Observe que as **** atividades de permissões de caixa de correio delegada e removidas de **caixa de correio delegadas** mostradas na captura de tela anterior não estão relacionadas às ações de auditoria Eles indicam se um administrador atribuiu ou removeu a permissão de caixa de correio FullAccess. 
    
    Para obter informações sobre o log de auditoria do Office 365, confira [Pesquisar o log de auditoria &amp; no centro de conformidade de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md).
    
- Considera-se que as caixas de correio sejam acessadas por um administrador apenas nos seguintes cenários:
    
  - A descoberta eletrônica in-loco no Exchange Online ou na pesquisa de conteúdo no Office 365 é usada para pesquisar uma caixa de correio.
    
  - O [Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) é usado para acessar a caixa de correio. 
    
- Ao habilitar o log de auditoria para uma caixa de correio, você também pode especificar quais ações do usuário (por exemplo, acesso, movimentação ou exclusão de uma mensagem) serão registradas para cada tipo de logon (administrador, representante, ou proprietário). 
    
- Para desabilitar o log de auditoria de caixa de correio, execute o seguinte comando:

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- As ações auditadas para cada tipo de usuário não são exibidas quando você executa o cmdlet **Get-Mailbox** . Mas você pode executar os seguintes comandos para exibir todas as ações auditadas para um tipo de logon de usuário específico. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Você também pode exportar um log de auditoria de caixa de correio e especificar as entradas a serem incluídas para um ou mais usuários. Cada entrada no relatório e o log de auditoria inclui informações sobre quem executou a ação e quando, a ação executada e se a ação foi bem-sucedida. Para obter mais informações, consulte [Exportar logs de auditoria de caixa de correio](https://go.microsoft.com/fwlink/p/?LinkID=404104).
