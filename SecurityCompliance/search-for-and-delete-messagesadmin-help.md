---
title: Pesquisar e excluir mensagens - ajuda de Admin
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: Os administradores podem usar o cmdlet Search-Mailbox para pesquisar caixas de correio do usuário e, em seguida, excluir mensagens de uma caixa de correio.
ms.openlocfilehash: ed110c4a3e36a93970af99e9548aa293d94307fd
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026578"
---
# <a name="search-for-and-delete-messages---admin-help"></a>Pesquisar e excluir mensagens - ajuda de Admin
  
Os administradores podem usar o cmdlet **Search-Mailbox** para pesquisar caixas de correio do usuário e, em seguida, excluir mensagens de uma caixa de correio. 
  
Para pesquisar e excluir mensagens em uma única etapa, execute o cmdlet **Search-Mailbox** com a opção _DeleteContent_ . No entanto, quando você fizer isso, não é possível visualizar resultados da pesquisa ou gerar um log de mensagens que serão retornados pela pesquisa, e você pode excluir mensagens que não pretendia inadvertidamente. Para visualizar um log das mensagens localizadas na pesquisa antes que eles estiver excluídos, execute o cmdlet **Search-Mailbox** com a opção _LogOnly_ . 
  
Como uma salvaguarda adicional, primeiro você pode copiar as mensagens para outra caixa de correio usando os parâmetros _TargetMailbox_ e _TargetFolder_ . Ao fazer isso, você detém uma cópia das mensagens excluídas, caso seja necessário para acessá-los novamente. 
  
## <a name="what-do-i-need-to-know-before-i-begin"></a>O que eu preciso saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 10 minutos. O tempo real pode variar dependendo do tamanho da caixa de correio e da consulta de pesquisa.
    
- Não é possível usar o EAC (Centro de administração do Exchange) para realizar esses procedimentos. É necessário usar o Shell.
    
- Você precisa ser atribuído ambas as seguintes funções de gerenciamento para procurar e excluir mensagens nas caixas de correio dos usuários:
    
  - **Pesquisa de caixa de correio** Essa função permite pesquisar por mensagens em várias caixas de correio em sua organização. Os administradores não estão atribuídos a essa função por padrão. Para atribuir sozinho esta função para que você pode pesquisar caixas de correio, adicione si mesmo como membro do grupo de funções de gerenciamento de descoberta. Consulte [Adicionar um usuário ao grupo de função de gerenciamento de descoberta](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).
    
  - **Caixa de correio importar e exportar** Essa função permite que você excluir mensagens da caixa de correio do usuário. Por padrão, essa função não é atribuída a qualquer grupo de funções. Para excluir mensagens de caixas de correio dos usuários, você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Para obter mais informações, consulte a seção "Adicionar uma função a um grupo de funções" em [Gerenciar grupos de função](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) . 
    
- Se a caixa de correio a partir do qual você deseja excluir mensagens tiver a recuperação de item único habilitada, primeiro será necessário desabilitar o recurso. Para obter mais informações, consulte [Habilitar ou desabilitar a recuperação de item único para uma caixa de correio](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).
    
- Se a caixa de correio a partir do qual você deseja excluir mensagens for colocada em espera, recomendamos que você verifique com o gerenciamento de registros ou o departamento jurídico antes de remover a retenção e excluam o conteúdo de caixa de correio. Depois de obter aprovação, siga as etapas listadas no tópico [Clean Up a pasta itens recuperáveis](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).
    
- Você pode pesquisar um máximo de 10.000 caixas de correio usando o cmdlet **Search-Mailbox** . Caso você seja uma organização do Exchange Online e têm mais de 10.000 caixas de correio, você pode usar o recurso de pesquisa de conformidade (ou o cmdlet **New-ComplianceSearch** correspondente) para um número ilimitado de caixas de correio de pesquisa. Em seguida, você pode usar o cmdlet **New-ComplianceSearchAction** para excluir as mensagens retornadas por uma pesquisa de conformidade. Para obter mais informações, consulte [Procurar e excluir mensagens de email da sua organização do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=786856).
    
- Se você incluir uma consulta de pesquisa (usando o parâmetro *SearchQuery* ), o cmdlet **Search-Mailbox** retornará um máximo de 10.000 itens nos resultados da pesquisa. Portanto, se você incluir uma consulta de pesquisa, você pode precisar executar o comando **Search-Mailbox** várias vezes para excluir mais de 10.000 itens. 
    
- Caixa de correio de arquivo morto do usuário também devem ser pesquisada quando você executa o cmdlet **Search-Mailbox** . Da mesma forma, os itens na caixa de correio de arquivo morto principal serão excluídos quando você usa o cmdlet **Search-Mailbox** com a opção _DeleteContent_ . Para impedir isso, você pode incluir a opção *DoNotIncludeArchive* . Além disso, é recomendável que você não usar a opção _DeleteContent_ para excluir mensagens no Exchange Online caixas de correio que tenham a expansão automática arquivamento habilitado, pois pode ocorrer a perda de dados inesperada. 
    
## <a name="search-messages-and-log-the-search-results"></a>Pesquisar mensagens e registrar os resultados da pesquisa em log
<a name="sectionSection1"> </a>

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e registra em log os resultados da pesquisa na pasta SearchAndDeleteLog da caixa de correio do administrador. As mensagens não são copiadas para a caixa de correio de destino ou excluídas dela.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Este exemplo procura todas as caixas de correio na organização para mensagens que têm qualquer tipo de arquivo anexado que contém a palavra "Troia" no nome de arquivo e envia uma mensagem de log para a caixa de correio do administrador.
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).
  
[Return to top](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="search-and-delete-messages"></a>Pesquisar e excluir mensagens
<a name="sectionSection2"> </a>

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto e exclui as mensagens da caixa de correio de origem sem copiar os resultados da pesquisa para outra pasta. Como explicado anteriormente, você precisa ter a função de gerenciamento de Importação e Exportação de Caixas de Correio para excluir mensagens da caixa de correio de um usuário.
  
> [!IMPORTANT]
> Quando você usa o cmdlet **Search-Mailbox** com a opção _DeleteContent_ , as mensagens são excluídas permanentemente da caixa de correio de origem. Antes de excluir mensagens permanentemente, recomendamos que você use a opção _LogOnly_ para gerar um log das mensagens localizadas na pesquisa antes que eles estiver excluídos ou copie as mensagens para outra caixa de correio antes de excluí-las da caixa de correio de origem. 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

Este exemplo pesquisa na caixa de correio de Isabel Martins mensagens que contenham a frase "Seu extrato bancário" no campo Assunto, copia os resultados da pesquisa para a pasta AprilStewart-DeletedMessages na caixa de correio BackupMailbox e exclui as mensagens da caixa de correio de Isabel.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

Este exemplo procura todas as caixas de correio na organização para mensagens com a linha de assunto "Download esse arquivo" e, em seguida, exclui-los permanentemente. 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

Para obter informações detalhadas de sintaxes e parâmetros, consulte [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).
  
[Return to top](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="using-the--loglevel-full-parameter"></a>Usando o parâmetro de total - LogLevel
<a name="sectionSection3"> </a>

Em alguns dos exemplos anteriores, o parâmetro _LogLevel_ , com o `Full` valor é usado para registrar informações detalhadas sobre os resultados retornados pelo cmdlet **Search-Mailbox** . Quando você tiver incluído neste parâmetro, uma mensagem de email é criada e enviada à caixa de correio especificada pelo parâmetro _TargetMailbox_ . O arquivo de log (que é um arquivo de formato CSV chamado pesquisa Results.csv) é anexado a esta mensagem de email e estará localizado na pasta especificada pelo parâmetro _TargetFolder_ . O arquivo de log contém uma linha para cada mensagem que está incluída nos resultados da pesquisa quando você executa o cmdlet **Search-Mailbox** . 
  

