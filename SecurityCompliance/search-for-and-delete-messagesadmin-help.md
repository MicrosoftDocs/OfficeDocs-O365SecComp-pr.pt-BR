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
# <a name="search-for-and-delete-messages---admin-help"></a>Procurar e excluir mensagens - Ajuda para administradores
  
Os administradores podem usar o cmdlet **Search-Mailbox** para pesquisar caixas de correio do usuário e, em seguida, excluir mensagens de uma caixa de correio. 
  
Para pesquisar e excluir mensagens em uma etapa, execute o cmdlet **Search-Mailbox** com a opção _DeleteContent_ No enTanto, ao fazer isso, você não pode visualizar os resultados da pesquisa ou gerar um log de mensagens que serão retornadas pela pesquisa, e você poderá excluir inadvertidamente mensagens que não pretendia. Para visualizar um log das mensagens encontradas na pesquisa antes de serem excluídas, execute o cmdlet **Search-Mailbox** com o comutador de _logon_ . 
  
Como uma proteção adicional, você pode primeiro copiar as mensagens para outra caixa de correio usando os parâmetros _TargetMailbox_ e _TargetFolder_ . Ao fazer isso, você mantém uma cópia das mensagens excluídas caso precise acessá-las novamente. 
  
## <a name="before-you-begin"></a>Antes de começar

- Tempo estimado para conclusão: 10 minutos. O tempo real pode variar dependendo do tamanho da caixa de correio e da consulta de pesquisa.
    
- Não é possível usar o EAC (Centro de administração do Exchange) para realizar esses procedimentos. É necessário usar o Shell.
    
- Você precisa ter as duas funções de gerenciamento a seguir para pesquisar e excluir mensagens nas caixas de correio dos usuários:
    
  - **Pesquisa de caixa de correio**-essa função permite pesquisar mensagens em várias caixas de correio em sua organização. Os administradores não são atribuídos a essa função por padrão. Para atribuir a si mesmo esta função para que você possa Pesquisar caixas de correio, adicione a si mesmo como membro do grupo de função gerenciamento de descoberta. Consulte [Adicionar um usuário ao grupo de função gerenciamento de descoberta](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).
    
  - **Exportação de importação de caixa de correio** -essa função permite excluir mensagens da caixa de correio de um usuário. Por padrão, essa função não é atribuída a nenhum grupo de função. Para excluir mensagens de caixas de correio dos usuários, você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização. Para obter mais informações, consulte a seção "adicionar uma função a um grupo de funções" em [Manage role groups](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) . 
    
- Se a caixa de correio da qual você deseja excluir mensagens tiver a recuperação de item único habilitada, primeiro você deverá desabilitar o recurso. Para obter mais informações, consulte [habilitar ou desabilitar a recuperação de item único para uma caixa de correio](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).
    
- Se a caixa de correio a partir da qual você deseja excluir mensagens for colocada em espera, recomendamos verificar com o gerenciamento de registros ou departamento legal antes de remover a retenção e excluir o conteúdo da caixa de correio. Após obter a aprovação, siga as etapas listadas no tópico [limpar a pasta itens recuperáveis](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).
    
- Você pode pesquisar um máximo de 10.000 caixas de correio usando o cmdlet **Search-Mailbox** . Se você é uma organização do Exchange Online e tem mais de 10.000 caixas de correio, você pode usar o recurso de pesquisa de conformidade (ou o cmdlet **New-ComplianceSearch** correspondente) para pesquisar um número ilimitado de caixas de correio. Em seguida, você pode usar o cmdlet **New-ComplianceSearchAction** para excluir as mensagens retornadas por uma pesquisa de conformidade. Para saber mais, confira [Pesquisar e excluir mensagens de email da sua organização do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=786856).
    
- Se você incluir uma consulta de pesquisa (usando o parâmetro *SearchQuery* ), o cmdlet **Search-Mailbox** retornará um máximo de 10.000 itens nos resultados da pesquisa. Portanto, se você incluir uma consulta de pesquisa, talvez seja necessário executar o comando **Search-Mailbox** várias vezes para excluir mais de 10.000 itens. 
    
- A caixa de correio de arquivo morto do usuário também será pesquisada quando você executar o cmdlet **Search-Mailbox** . Da mesma forma, os itens na caixa de correio de arquivo morto principal serão excluídos quando você usar o cmdlet **Search-Mailbox** com a opção _DeleteContent_ . Para evitar isso, você pode incluir a opção *DoNotIncludeArchive* Além disso, recomendamos que você não use a opção _DeleteContent_ para excluir mensagens em caixas de correio do Exchange Online com o arquivamento de expansão automática habilitado, pois pode ocorrer perda de dados inesperada. 
    
## <a name="search-messages-and-log-the-search-results"></a>Pesquisar mensagens e registrar os resultados da pesquisa em log

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e registra em log os resultados da pesquisa na pasta SearchAndDeleteLog da caixa de correio do administrador. As mensagens não são copiadas para a caixa de correio de destino ou excluídas dela.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Este exemplo pesquisa todas as caixas de correio na organização em busca de mensagens que tenham qualquer tipo de arquivo anexado que contenha a palavra "cavalo de Tróia" no nome do arquivo e envia uma mensagem de log para a caixa de correio do administrador.
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).
  
 
## <a name="search-and-delete-messages"></a>Pesquisar e excluir mensagens

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e exclui as mensagens da caixa de correio de origem sem copiar os resultados da pesquisa para outra pasta. Como explicado anteriormente, você precisa ter a função de gerenciamento de Importação e Exportação de Caixas de Correio para excluir mensagens da caixa de correio de um usuário.
  
> [!IMPORTANT]
> Quando você usa o cmdlet **Search-Mailbox** com a opção _DeleteContent_ , as mensagens são excluídas permanentemente da caixa de correio de origem. Antes de excluir mensagens permanentemente, recomendamos que você use o comutador de _logon_ para gerar um log das mensagens encontradas na pesquisa antes de elas serem excluídas ou copiar as mensagens para outra caixa de correio antes de excluí-las da caixa de correio de origem. 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto, copia os resultados da pesquisa para a pasta AprilStewart-DeletedMessages na caixa de correio BackupMailbox e exclui as mensagens da caixa de correio de Isabel.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

Este exemplo pesquisa todas as caixas de correio na organização em busca de mensagens com a linha de assunto "baixar este arquivo" e as exclui permanentemente. 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).

## <a name="using-the--loglevel-full-parameter"></a>Usando o parâmetro completo-LogLevel

Em alguns dos exemplos anteriores, o parâmetro _logLevel_ , com o `Full` valor, é usado para registrar informações detalhadas sobre os resultados retornados pelo cmdlet **Search-Mailbox** . Quando você inclui este parâmetro, uma mensagem de email é criada e enviada para a caixa de correio especificada pelo parâmetro _TargetMailbox_ . O arquivo de log (que é um arquivo de formato CSV chamado Search Results. csv) é anexado a essa mensagem de email e estará localizado na pasta especificada pelo parâmetro _TargetFolder_ . O arquivo de log contém uma linha para cada mensagem incluída nos resultados da pesquisa quando você executa o cmdlet **Search-Mailbox** . 
