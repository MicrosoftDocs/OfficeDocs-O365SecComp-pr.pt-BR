---
title: Habilitar a auditoria de caixa de correio no Office 365
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
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: No Office 365, você pode ativar o log de auditoria de caixa de correio para registrar o acesso à caixa de correio por proprietários de caixa de correio, representantes e administradores. Por padrão, a auditoria de caixa de correio no Office 365 não está ativado. Após habilitar uma caixa de correio do log de auditoria de caixa de correio, você pode pesquisar o log de auditoria do Office 365 para atividades realizadas na caixa de correio.
ms.openlocfilehash: 6d3de226e7c0e03be824b14e1b16fadaae3f040e
ms.sourcegitcommit: 8294182d4dd124f035a221de0b90159ef7eec4ae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2018
ms.locfileid: "25639660"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Habilitar a auditoria de caixa de correio no Office 365
  
No Office 365, você pode ativar o log de auditoria de caixa de correio para registrar o acesso à caixa de correio por proprietários de caixa de correio, representantes e administradores. Por padrão, a auditoria de caixa de correio no Office 365 não está ativado. Isso significa que eventos de auditoria de caixa de correio não aparecerá nos resultados ao pesquisar o log de auditoria do Office 365 para atividade de caixa de correio. Mas depois que você ativa uma caixa de correio do usuário do log de auditoria de caixa de correio, você pode pesquisar o log de auditoria para atividade de caixa de correio. Além disso, quando a auditoria de caixa de correio log está ativado, algumas ações executadas pelos administradores, delegados, e proprietários são registrados por padrão. Para criar logs (e, em seguida, procure) ações adicionais, consulte a etapa 3.

## <a name="before-you-begin"></a>Antes de começar
  
- Você precisa usar o PowerShell do Exchange Online para habilitar a caixa de correio do log de auditoria. Não é possível utilizar a segurança do Office 365 &amp; Centro de conformidade ou centro de administração do Exchange.
    
- Não será possível habilitar o log da caixa de correio que está associado a um grupo do Office 365 ou de uma equipe no Microsoft Teams de auditoria de caixa de correio.
    
- Um administrador que recebeu a permissão de Acesso Completo à caixa de correio de um usuário é considerado um usuário representante.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>Etapa 1: Conectar ao Exchange Online PowerShell

1. No computador local, abra o Windows PowerShell e execute o comando a seguir.
   
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

Depois de se conectar à sua organização do Exchange Online, use o PowerShell para habilitar uma caixa de correio do log de auditoria de caixa de correio. Como alternativa, é possível habilitar a auditoria de caixa de correio para todas as caixas de correio em sua organização.
  
Este exemplo habilita a caixa de correio do Pilar Pinilla do log de auditoria de caixa de correio.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Esse exemplo habilita o log de auditoria de caixa de correio para todas as caixas de correio em sua organização.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Etapa 3: Especificar ações de proprietário para auditoria

Quando você habilita a auditoria de uma caixa de correio, algumas ações executadas pelo proprietário da caixa de correio são auditadas por padrão. Você precisa especificar outras ações de proprietário de auditoria. Consulte a tabela na seção [ações de auditoria de caixa de correio](#mailbox-auditing-actions) para uma lista e uma descrição das ações de proprietário que são registradas por padrão e outras ações que podem ser auditadas. 
  
Este exemplo adiciona as ações de proprietário **MailboxLogin** e **HardDelete** à caixa de correio auditoria de caixa de correio do Pilar Pinilla. Este exemplo pressupõe que a auditoria de caixa de correio já foi ativado para esta caixa de correio. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

Este exemplo habilita o log de caixa de correio do Don Hall de auditoria de caixa de correio e especifica que somente a ação **MailboxLogin** executada pelo proprietário da caixa de correio será registrada. Observe que este exemplo substitui a ação de UpdateFolderPermissions padrão. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
Este exemplo adiciona as ações de proprietário **SoftDelete** , **HardDelete**e **MailboxLogin**para todas as caixas de correio na organização. Este exemplo pressupõe que a auditoria de caixa de correio já foi habilitado para todas as caixas de correio. 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a>Como você sabe se funcionou?

Para verificar se você habilitou o log de auditoria para uma caixa de correio, use o cmdlet **Get-Mailbox** para recuperar as configurações de auditoria dessa caixa de correio. 
  
Esse exemplo recupera as configurações de auditoria de Clara Barbosa.

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
Este exemplo recupera as configurações de auditoria de todas as caixas de correio em sua organização.

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
Um valor de **True** referente à propriedade **AuditEnabled** verifica que auditoria de caixa de correio log está habilitado. 
    
## <a name="mailbox-auditing-actions"></a>Ações de auditoria de caixa de correio
  
A tabela a seguir lista as ações que podem ser registradas por caixa de correio do log de auditoria. A tabela inclui qual ação pode ser registrada para os tipos de logon de usuário diferente. Na tabela, um **não** indica que uma ação não puder ser registrada para esse tipo de logon. Um asterisco ( **\*** ) indica que a ação é registrada por padrão, quando o log de auditoria de caixa de correio está habilitada para a caixa de correio. 
  
|**Action**|**Descrição**|**Administrador**|**Representante\*\*\***|**Proprietário**|
|:-----|:-----|:-----|:-----|:-----|
|**Copiar** <br/> |Uma mensagem foi copiada a outra pasta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Criar** <br/> |Um item é criado na pasta Calendário, contatos, anotações ou tarefas na caixa de correio; Por exemplo, uma nova solicitação de reunião é criada. Observe que a criação, enviando ou recebendo uma mensagem não sofre auditoria. Além disso, não é auditado criando uma pasta de caixa de correio.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**FolderBind** <br/> |Uma pasta da caixa de correio foi acessada. Esta ação também é registrada quando o administrador ou representante abrem a caixa de correio.  <br/> |Sim  <br/> |Sim\*\*  <br/> |Não  <br/> |
|**HardDelete** <br/> |Uma mensagem foi removida da pasta de Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**MailboxLogin** <br/> |O usuário entrou em sua caixa de correio.  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|**MessageBind** <br/> |Uma mensagem foi exibida no painel de visualização ou aberta.  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|**Move** <br/> |Uma mensagem foi movida para outra pasta.  <br/> |Sim  <br/> |Sim  <br/> |Sim  <br/> |
|**MoveToDeletedItems** <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**SendAs** <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SendOnBehalf** <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Não  <br/> |
|**SoftDelete** <br/> |Uma mensagem foi excluída permanentemente da pasta Itens Excluídos. Os itens excluídos temporariamente são movidos para a pasta Itens Recuperáveis.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**Atualizar** <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim  <br/> |
|**UpdateCalendarDelegation** <br/> |Uma representação de calendário foi atribuída a uma caixa de correio. Delegação de calendário oferece a outra pessoa nas mesmas permissões de organização para gerenciar o calendário do proprietário da caixa de correio.  <br/> |Sim\*  <br/> |Não  <br/> |Sim\*  <br/> |
|**UpdateFolderPermissions** <br/> |Uma permissão de pasta foi alterada. Controle de permissões de pasta quais usuários em sua organização podem acessar pastas em uma caixa de correio e as mensagens localizadas nessas pastas.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
|**UpdateInboxRules** <br/> |Uma regra de caixa de correio foram adicionada, removida ou alterada. Regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e execute as ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou exclusão de uma mensagem.  <br/> |Sim\*  <br/> |Sim\*  <br/> |Sim\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Auditados por padrão, se a auditoria está habilitada para uma caixa de correio.<br/><br/>  <sup>\*\*</sup>Entradas para ações de vincular pasta executadas por representantes são consolidadas. Uma entrada de log é gerada para acesso a pastas individuais dentro de um período de tempo de 24 horas.<br/><br/><sup>\*\*\*</sup>Um administrador que tenha sido atribuído a permissão de acesso completo à caixa de correio de um usuário é considerado um usuário delegado. 
  
Se você não precisar mais determinados tipos de ações de caixa de correio a ser auditado, você deve modificar a configuração de log de auditoria da caixa de correio para desabilitar essas ações. Entradas de log existentes não são limpo até o limite de idade de retenção para entradas do log de auditoria for atingido. Para obter mais informações sobre a idade de retenção para as entradas de log de auditoria, consulte a seção "antes de começar" na [pesquisa da auditoria, faça logon no Centro de conformidade & segurança do Office 365](search-the-audit-log-in-security-and-compliance.md#before-you-begin).
  
## <a name="more-infotab"></a>[Mais informações](#tab/)
  
- Use o log de auditoria do Office 365 para procurar a atividade de caixa de correio que foram registrados. Você pode procurar atividade para uma caixa de correio de usuário específico. A captura de tela a seguir mostra uma lista de atividades de caixa de correio que você pode pesquisar no log de auditoria do Office 365. Observe que essas atividades são as mesmas ações que são descritas na seção "Ações de auditoria de caixa de correio", neste tópico.
    
    ![Você pode pesquisar o log de auditoria do Office 365 para ações de auditoria de caixa de correio, selecionando "Atividades de caixa de correio do Exchange" na lista suspensa de atividades](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    A tabela a seguir descreve cada atividade de caixa de correio que você pode pesquisar e mostra a caixa de correio correspondente a auditoria de ação.
    
    |**Atividade no log de auditoria**|**Ação de auditoria de caixa de correio**|
    |:-----|:-----|
    |Item de caixa de correio criada  <br/> |Criar  <br/> |
    |Mensagens copiadas para outra pasta  <br/> |Copiar  <br/> |
    |Usuário se conectou à caixa de correio  <br/> |MailboxLogin  <br/> |
    |Enviada usando permissões Enviar em nome de mensagem  <br/> |SendOnBehalf  <br/> |
    |Mensagens limpas da caixa de correio  <br/> |HardDelete  <br/> |
    |Movido mensagens para a pasta Itens excluídos  <br/> |MoveToDeletedItems  <br/> |
    |Movido mensagens para outra pasta  <br/> |Move  <br/> |
    |Enviada usando permissões Enviar como de mensagem  <br/> |SendAs  <br/> |
    |Mensagem atualizada  <br/> |Atualizar  <br/> |
    |Mensagens excluídas da pasta Itens excluídos  <br/> |SoftDelete  <br/> |
    |Adicionadas as permissões para pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Permissões de modificação da pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Permissões removidas da pasta  <br/> |UpdateFolderPermissions  <br/> |
    |Usuário adicionado ou removido com o acesso de representante à pasta de calendário  <br/> |UpdateCalendarDelegation  <br/> |
   
    Observe que as atividades **adicionadas delegar permissões de caixa de correio** e **foram removidas Delegar permissões de caixa de correio** mostradas a captura de tela anterior não estão relacionadas a ações de auditoria de caixa de correio. Eles indicam se um administrador atribuída ou removido a permissão de caixa de correio FullAccess. 
    
    Para obter informações sobre o log de auditoria do Office 365, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).
    
- Considera-se que as caixas de correio sejam acessadas por um administrador apenas nos seguintes cenários:
    
  - EDiscovery local no Exchange Online ou pesquisa de conteúdo no Office 365 é usada para pesquisar uma caixa de correio.
    
  - O [Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) é usado para acessar a caixa de correio. 
    
- Ao habilitar o log de auditoria para uma caixa de correio, você também pode especificar quais ações do usuário (por exemplo, acesso, movimentação ou exclusão de uma mensagem) serão registradas para cada tipo de logon (administrador, representante, ou proprietário). 
    
- Para desabilitar o log de auditoria de caixa de correio, execute o seguinte comando:

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- As ações que são auditadas para cada tipo de usuário não são exibidas quando você executa o cmdlet **Get-Mailbox** . Mas você pode executar os seguintes comandos para exibir todas as ações auditadas para um tipo de logon do usuário específico. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Você também pode exportar o log de auditoria de caixa de correio e especifique as entradas para incluir um ou mais usuários. Cada entrada no relatório e o log de auditoria inclui informações sobre quem executou a ação e quando, a ação executada e se a ação foi bem-sucedida. Para obter mais informações, consulte [exportar logs de auditoria de caixa de correio](https://go.microsoft.com/fwlink/p/?LinkID=404104).
