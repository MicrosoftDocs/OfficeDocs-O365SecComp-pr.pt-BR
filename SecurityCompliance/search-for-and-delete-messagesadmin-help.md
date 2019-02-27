---
title: Procurar e excluir mensagens - Ajuda para administradores
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: Os administradores podem usar o cmdlet Search-Mailbox para pesquisar caixas de correio do usuário e, em seguida, excluir mensagens de uma caixa de correio.
ms.openlocfilehash: 718a23f649843420ccfd924be72752a99278da4c
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297124"
---
# <a name="search-for-and-delete-messages---admin-help"></a><span data-ttu-id="e4558-103">Procurar e excluir mensagens - Ajuda para administradores</span><span class="sxs-lookup"><span data-stu-id="e4558-103">Search for and delete messages - Admin help</span></span>
  
<span data-ttu-id="e4558-104">Os administradores podem usar o cmdlet **Search-Mailbox** para pesquisar caixas de correio do usuário e, em seguida, excluir mensagens de uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="e4558-104">Administrators can use the **Search-Mailbox** cmdlet to search user mailboxes and then delete messages from a mailbox.</span></span> 
  
<span data-ttu-id="e4558-p101">Para pesquisar e excluir mensagens em uma etapa, execute o cmdlet **Search-Mailbox** com a opção _DeleteContent_ No enTanto, ao fazer isso, você não pode visualizar os resultados da pesquisa ou gerar um log de mensagens que serão retornadas pela pesquisa, e você poderá excluir inadvertidamente mensagens que não pretendia. Para visualizar um log das mensagens encontradas na pesquisa antes de serem excluídas, execute o cmdlet **Search-Mailbox** com o comutador de _logon_ .</span><span class="sxs-lookup"><span data-stu-id="e4558-p101">To search and delete messages in one step, run the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch. However, when you do this, you can't preview search results or generate a log of messages that will be returned by the search, and you may inadvertently delete messages that you didn't intend to. To preview a log of the messages found in the search before they're deleted, run the **Search-Mailbox** cmdlet with the  _LogOnly_ switch.</span></span> 
  
<span data-ttu-id="e4558-p102">Como uma proteção adicional, você pode primeiro copiar as mensagens para outra caixa de correio usando os parâmetros _TargetMailbox_ e _TargetFolder_ . Ao fazer isso, você mantém uma cópia das mensagens excluídas caso precise acessá-las novamente.</span><span class="sxs-lookup"><span data-stu-id="e4558-p102">As an additional safeguard, you can first copy the messages to another mailbox by using the  _TargetMailbox_ and  _TargetFolder_ parameters. By doing this, you retain a copy of the deleted messages in case you need to access them again.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="e4558-110">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="e4558-110">Before you begin</span></span>

- <span data-ttu-id="e4558-p103">Tempo estimado para conclusão: 10 minutos. O tempo real pode variar dependendo do tamanho da caixa de correio e da consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e4558-p103">Estimated time to complete: 10 minutes. The actual time may vary depending on the size of the mailbox and the search query.</span></span>
    
- <span data-ttu-id="e4558-p104">Não é possível usar o EAC (Centro de administração do Exchange) para realizar esses procedimentos. É necessário usar o Shell.</span><span class="sxs-lookup"><span data-stu-id="e4558-p104">You can't use the Exchange admin center (EAC) to perform these procedures. You must use the Shell.</span></span>
    
- <span data-ttu-id="e4558-115">Você precisa ter as duas funções de gerenciamento a seguir para pesquisar e excluir mensagens nas caixas de correio dos usuários:</span><span class="sxs-lookup"><span data-stu-id="e4558-115">You need to be assigned both of the following management roles to search for and delete messages in users' mailboxes:</span></span>
    
  - <span data-ttu-id="e4558-p105">**Pesquisa de caixa de correio**-essa função permite pesquisar mensagens em várias caixas de correio em sua organização. Os administradores não são atribuídos a essa função por padrão. Para atribuir a si mesmo esta função para que você possa Pesquisar caixas de correio, adicione a si mesmo como membro do grupo de função gerenciamento de descoberta. Consulte [Adicionar um usuário ao grupo de função gerenciamento de descoberta](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4558-p105">**Mailbox Search**- This role allows you to search for messages across multiple mailboxes in your organization. Administrators aren't assigned this role by default. To assign yourself this role so that you can search mailboxes, add yourself as a member of the Discovery Management role group. See [Add a User to the Discovery Management Role Group](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).</span></span>
    
  - <span data-ttu-id="e4558-p106">**Exportação de importação de caixa de correio** -essa função permite excluir mensagens da caixa de correio de um usuário. Por padrão, essa função não é atribuída a nenhum grupo de função. Para excluir mensagens de caixas de correio dos usuários, você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização. Para obter mais informações, consulte a seção "adicionar uma função a um grupo de funções" em [Manage role groups](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e4558-p106">**Mailbox Import Export** - This role allows you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group. For more information, see the "Add a role to a role group" section in [Manage Role Groups](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) .</span></span> 
    
- <span data-ttu-id="e4558-p107">Se a caixa de correio da qual você deseja excluir mensagens tiver a recuperação de item único habilitada, primeiro você deverá desabilitar o recurso. Para obter mais informações, consulte [habilitar ou desabilitar a recuperação de item único para uma caixa de correio](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4558-p107">If the mailbox from which you want to delete messages has single item recovery enabled, you must first disable the feature. For more information, see [Enable or disable single item recovery for a mailbox](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).</span></span>
    
- <span data-ttu-id="e4558-p108">Se a caixa de correio a partir da qual você deseja excluir mensagens for colocada em espera, recomendamos verificar com o gerenciamento de registros ou departamento legal antes de remover a retenção e excluir o conteúdo da caixa de correio. Após obter a aprovação, siga as etapas listadas no tópico [limpar a pasta itens recuperáveis](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4558-p108">If the mailbox from which you want to delete messages is placed on hold, we recommend that you check with your records management or legal department before removing the hold and deleting the mailbox content. After you obtain approval, follow the steps listed in the topic [Clean Up the Recoverable Items Folder](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).</span></span>
    
- <span data-ttu-id="e4558-p109">Você pode pesquisar um máximo de 10.000 caixas de correio usando o cmdlet **Search-Mailbox** . Se você é uma organização do Exchange Online e tem mais de 10.000 caixas de correio, você pode usar o recurso de pesquisa de conformidade (ou o cmdlet **New-ComplianceSearch** correspondente) para pesquisar um número ilimitado de caixas de correio. Em seguida, você pode usar o cmdlet **New-ComplianceSearchAction** para excluir as mensagens retornadas por uma pesquisa de conformidade. Para saber mais, confira [Pesquisar e excluir mensagens de email da sua organização do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=786856).</span><span class="sxs-lookup"><span data-stu-id="e4558-p109">You can search a maximum of 10,000 mailboxes using the **Search-Mailbox** cmdlet. If you're an Exchange Online organization and have more than 10,000 mailboxes, you can use the Compliance Search feature (or the corresponding **New-ComplianceSearch** cmdlet) to search an unlimited number of mailboxes. Then you can use the **New-ComplianceSearchAction** cmdlet to delete the messages returned by a compliance search. For more information, see [Search for and delete email messages from your Office 365 organization](https://go.microsoft.com/fwlink/p/?LinkId=786856).</span></span>
    
- <span data-ttu-id="e4558-p110">Se você incluir uma consulta de pesquisa (usando o parâmetro *SearchQuery* ), o cmdlet **Search-Mailbox** retornará um máximo de 10.000 itens nos resultados da pesquisa. Portanto, se você incluir uma consulta de pesquisa, talvez seja necessário executar o comando **Search-Mailbox** várias vezes para excluir mais de 10.000 itens.</span><span class="sxs-lookup"><span data-stu-id="e4558-p110">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
    
- <span data-ttu-id="e4558-p111">A caixa de correio de arquivo morto do usuário também será pesquisada quando você executar o cmdlet **Search-Mailbox** . Da mesma forma, os itens na caixa de correio de arquivo morto principal serão excluídos quando você usar o cmdlet **Search-Mailbox** com a opção _DeleteContent_ . Para evitar isso, você pode incluir a opção *DoNotIncludeArchive* Além disso, recomendamos que você não use a opção _DeleteContent_ para excluir mensagens em caixas de correio do Exchange Online com o arquivamento de expansão automática habilitado, pois pode ocorrer perda de dados inesperada.</span><span class="sxs-lookup"><span data-stu-id="e4558-p111">The user's archive mailbox will also be searched when you run the **Search-Mailbox** cmdlet. Similarly, items in the primary archive mailbox will be deleted when you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch. To prevent this, you can include the  *DoNotIncludeArchive*  switch. Also, we recommend that you don't use the  _DeleteContent_ switch to delete messages in Exchange Online mailboxes that have auto-expanding archiving enabled because unexpected data loss may occur.</span></span> 
    
## <a name="search-messages-and-log-the-search-results"></a><span data-ttu-id="e4558-138">Pesquisar mensagens e registrar os resultados da pesquisa em log</span><span class="sxs-lookup"><span data-stu-id="e4558-138">Search messages and log the search results</span></span>

<span data-ttu-id="e4558-p112">Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e registra em log os resultados da pesquisa na pasta SearchAndDeleteLog da caixa de correio do administrador. As mensagens não são copiadas para a caixa de correio de destino ou excluídas dela.</span><span class="sxs-lookup"><span data-stu-id="e4558-p112">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and logs the search results in the SearchAndDeleteLog folder of the administrator's mailbox. Messages aren't copied to or deleted from the target mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="e4558-141">Este exemplo pesquisa todas as caixas de correio na organização em busca de mensagens que tenham qualquer tipo de arquivo anexado que contenha a palavra "cavalo de Tróia" no nome do arquivo e envia uma mensagem de log para a caixa de correio do administrador.</span><span class="sxs-lookup"><span data-stu-id="e4558-141">This example searches all mailboxes in the organization for messages that have any type of attached file that contains the word "Trojan" in the filename and sends a log message to the administrator's mailbox.</span></span>
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="e4558-142">Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4558-142">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>
  
 
## <a name="search-and-delete-messages"></a><span data-ttu-id="e4558-143">Pesquisar e excluir mensagens</span><span class="sxs-lookup"><span data-stu-id="e4558-143">Search and delete messages</span></span>

<span data-ttu-id="e4558-p113">Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e exclui as mensagens da caixa de correio de origem sem copiar os resultados da pesquisa para outra pasta. Como explicado anteriormente, você precisa ter a função de gerenciamento de Importação e Exportação de Caixas de Correio para excluir mensagens da caixa de correio de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e4558-p113">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and deletes the messages from the source mailbox without copying the search results to another folder. As previously explained, you need to be assigned the Mailbox Import Export management role to delete messages from a user's mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e4558-p114">Quando você usa o cmdlet **Search-Mailbox** com a opção _DeleteContent_ , as mensagens são excluídas permanentemente da caixa de correio de origem. Antes de excluir mensagens permanentemente, recomendamos que você use o comutador de _logon_ para gerar um log das mensagens encontradas na pesquisa antes de elas serem excluídas ou copiar as mensagens para outra caixa de correio antes de excluí-las da caixa de correio de origem.</span><span class="sxs-lookup"><span data-stu-id="e4558-p114">When you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch, messages are permanently deleted from the source mailbox. Before you permanently delete messages, we recommend that you either use the  _LogOnly_ switch to generate a log of the messages found in the search before they're deleted or copy the messages to another mailbox before deleting them from the source mailbox.</span></span> 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

<span data-ttu-id="e4558-148">Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto, copia os resultados da pesquisa para a pasta AprilStewart-DeletedMessages na caixa de correio BackupMailbox e exclui as mensagens da caixa de correio de Isabel.</span><span class="sxs-lookup"><span data-stu-id="e4558-148">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field, copies the search results to the folder AprilStewart-DeletedMessages in the mailbox BackupMailbox, and deletes the messages from April's mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

<span data-ttu-id="e4558-149">Este exemplo pesquisa todas as caixas de correio na organização em busca de mensagens com a linha de assunto "baixar este arquivo" e as exclui permanentemente.</span><span class="sxs-lookup"><span data-stu-id="e4558-149">This example searches all mailboxes in the organization for messages with the subject line "Download this file", and then permanently deletes them.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

<span data-ttu-id="e4558-150">Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4558-150">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>

## <a name="using-the--loglevel-full-parameter"></a><span data-ttu-id="e4558-151">Usando o parâmetro completo-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e4558-151">Using the -LogLevel Full parameter</span></span>

<span data-ttu-id="e4558-p115">Em alguns dos exemplos anteriores, o parâmetro _logLevel_ , com o `Full` valor, é usado para registrar informações detalhadas sobre os resultados retornados pelo cmdlet **Search-Mailbox** . Quando você inclui este parâmetro, uma mensagem de email é criada e enviada para a caixa de correio especificada pelo parâmetro _TargetMailbox_ . O arquivo de log (que é um arquivo de formato CSV chamado Search Results. csv) é anexado a essa mensagem de email e estará localizado na pasta especificada pelo parâmetro _TargetFolder_ . O arquivo de log contém uma linha para cada mensagem incluída nos resultados da pesquisa quando você executa o cmdlet **Search-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="e4558-p115">In some of the previous examples, the  _LogLevel_ parameter, with the  `Full` value is used to log detailed information about the results returned by the **Search-Mailbox** cmdlet. When you included this parameter, an email message is created and sent to the mailbox specified by the  _TargetMailbox_ parameter. The log file (which is a CSV-formatted file named Search Results.csv) is attached to this email message, and will be located in the folder specified by the  _TargetFolder_ parameter. The log file contains a row for each message that's included in the search results when you run the **Search-Mailbox** cmdlet.</span></span> 
