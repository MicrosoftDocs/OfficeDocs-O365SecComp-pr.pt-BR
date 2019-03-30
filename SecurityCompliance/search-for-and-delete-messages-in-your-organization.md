---
title: Procurar e excluir mensagens de email na sua organização do Office 365-ajuda do administrador
ms.author: markjjo
author: markjjo
manager: laurawi
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
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Use o recurso de pesquisa e limpeza no centro de conformidade do & de segurança no Office 365 para pesquisar e excluir uma mensagem de email de todas as caixas de correio em sua organização.
ms.openlocfilehash: c6fa0d09852016b918375dbff5a19468886d86b3
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000264"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Procurar e excluir mensagens de email na sua organização do Office 365-ajuda do administrador

**Este artigo é para administradores. Você está tentando localizar itens na sua caixa de correio que deseja excluir? Consulte [Localizar uma mensagem ou um item com pesquisa instantânea](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Você pode usar o recurso de pesquisa de conteúdo no Office 365 para procurar e excluir uma mensagem de email de todas as caixas de correio em sua organização. Isso pode ajudar você a encontrar e remover emails possivelmente prejudiciais ou de alto risco, por exemplo:
  
- Mensagens que contenham anexos ou vírus perigosos
    
- Mensagens de phishing
    
- Mensagens que contêm dados confidenciais
    
> [!CAUTION]
> Pesquisa e limpeza é um recurso poderoso que permite a qualquer pessoa com as permissões necessárias para excluir mensagens de email de caixas de correio em sua organização. 
  
## <a name="before-you-begin"></a>Antes de começar

- Para criar e executar uma pesquisa de conteúdo, você precisa ser membro do grupo de função **Gerenciador de descoberta eletrônica** ou ser atribuído à função de gerenciamento de **pesquisa de conformidade** . Para excluir mensagens, você precisa ser membro do grupo de função **Gerenciamento da organização** ou ter a função de gerenciamento de **pesquisa e limpeza** atribuída. Para obter informações sobre como adicionar usuários a um grupo de funções, consulte [conceder aos usuários acesso ao centro de segurança e conformidade](grant-access-to-the-security-and-compliance-center.md).
    
- Você precisa usar o PowerShell de segurança do & de conformidade para excluir mensagens. ConFira a [etapa 2](#step-2-connect-to-security--compliance-center-powershell) para obter instruções sobre como se conectar.
    
- No máximo 10 itens por caixa de correio podem ser removidos ao mesmo tempo. Como o recurso de pesquisa e remoção de mensagens tem como objetivo ser uma ferramenta de resposta a incidentes, esse limite ajuda a garantir que as mensagens sejam rapidamente removidas das caixas de correio. Este recurso não tem como objetivo limpar as caixas de correio do usuário. Para excluir mais de 10 itens, você pode usar o comando **Search-Mailbox-DeleteContent** no PowerShell do Exchange Online. ConFira [Pesquisar e excluir mensagens-ajuda do administrador](search-for-and-delete-messagesadmin-help.md).
    
- O número máximo de caixas de correio em uma pesquisa de conteúdo que você pode excluir itens em uma ação de pesquisa e limpeza é 50.000. Se a pesquisa de conteúdo (que você criou na [etapa 1](#step-1-create-a-content-search-to-find-the-message-to-delete)) tiver mais de 50.000 caixas de correio de origem, a ação de limpeza (que você cria na etapa 3) falhará. Consulte a seção [mais informações](#more-information) para obter uma dica sobre como executar uma operação de pesquisa e limpeza em mais de 50.000 caixas de correio. 
    
- O procedimento neste artigo só pode ser usado para excluir itens em caixas de correio do Exchange Online e pastas públicas. Você não pode usá-lo para excluir conteúdo de sites do SharePoint ou do OneDrive for Business.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Etapa 1: Criar uma Pesquisa de conteúdo para localizar a mensagem para exclusão

A primeira etapa é criar e executar uma pesquisa de conteúdo a fim de localizar a mensagem que você deseja remover das caixas de correio em sua organização. Você pode criar a pesquisa usando o centro de conformidade do & de segurança ou executando os cmdlets **New-ComplianceSearch** e **Start-ComplianceSearch** . As mensagens que correspondem à consulta para esta pesquisa serão excluídas executando o comando **New-ComplianceSearchAction-Purge** na [etapa 3](#step-3-delete-the-message). Para saber mais sobre como criar uma pesquisa de conteúdo e configurar as consultas da pesquisa, confira os tópicos a seguir: 
  
- [Pesquisa de conteúdo no Office 365](content-search.md)
    
- [Consultas de palavras-chave para pesquisa de conteúdo](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Os locais de conteúdo pesquisados na pesquisa de conteúdo que você cria nesta etapa não podem incluir os sites do SharePoint ou do OneDrive for Business. Você pode incluir somente caixas de correio e pastas públicas em uma pesquisa de conteúdo que será usada para mensagens de email. Se a pesquisa de conteúdo incluir sites, você receberá um erro na etapa 3 quando executar o cmdlet **New-ComplianceSearchAction** . 
  
### <a name="tips-for-finding-messages-to-remove"></a>Dicas para localizar mensagens para remoção

O objetivo da consulta de pesquisa é restringir os resultados da pesquisa apenas à mensagem ou mensagens que você deseja remover. Veja algumas dicas:
  
- Se você souber o texto ou a frase exata usada na linha de assunto da mensagem, use a propriedade **Subject** na consulta de pesquisa. 
    
- Se você souber a data exata (ou o intervalo de datas) da mensagem, inclua a propriedade **Received** na consulta de pesquisa. 
    
- Se você souber quem enviou a mensagem, inclua a propriedade **From** na consulta de pesquisa. 
    
- Visualize os resultados da pesquisa para verificar se a pesquisa de conteúdo retornou apenas a mensagem (ou mensagens) que você deseja excluir.
    
- Use as estatísticas de estimativa de pesquisa (exibidas no painel de detalhes da pesquisa no centro de conformidade do & de segurança ou usando o cmdlet [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ) para obter uma contagem do número total de resultados. 
    
Aqui estão dois exemplos de consultas para localizar mensagens de email suspeitas.
  
- Essa consulta retornará as mensagens que foram recebidas pelos usuários entre 13 de abril de 2016 e 14 de abril de 2016 e que contêm as palavras "ação" e "obrigatório" na linha de assunto.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Essa consulta retornará as mensagens que foram enviadas por chatsuwloginsset12345@outlook.com e que contêm a frase exata "Atualizar as informações da sua conta" na linha de assunto.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Etapa 2: conectar-se ao Security & central de conformidade do PowerShell

A próxima etapa é conectar-se ao PowerShell do centro de conformidade do & de segurança para sua organização. Para obter instruções detalhadas, confira conectar- [se ao PowerShell do centro de conformidade do & de segurança](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Se a sua conta do Office 365 usar a MFA (autenticação multifator) ou a autenticação federada, você não poderá usar as instruções do tópico anterior sobre como conectar-se ao PowerShell do centro de conformidade do & de segurança. Em vez disso, consulte as instruções no tópico [conectar-se ao PowerShell do centro de conformidade do & de segurança usando a autenticação](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell)multifator.
  
## <a name="step-3-delete-the-message"></a>Etapa 3: excluir a mensagem

Depois de criar e aprimorar uma pesquisa de conteúdo para retornar a mensagem que você deseja remover e está conectado ao & de segurança do centro de conformidade, a etapa final é executar o cmdlet **New-ComplianceSearchAction** para excluir a mensagem. Você pode excluir a mensagem de forma simples ou permanente. Uma mensagem excluída por software é movida para a pasta itens recuperáveis de um usuário e retida até que o período de retenção do item excluído expire. As mensagens excluídas por hardware são marcadas para remoção permanente da caixa de correio e serão removidas permanentemente na próxima vez que a caixa de correio for processada pelo assistente de pasta gerenciada. Se a recuperação de item único estiver habilitada para a caixa de correio, os itens excluídos por hardware serão removidos permanentemente depois que o período de retenção de itens excluídos expirar. Se uma caixa de correio for colocada em espera, as mensagens excluídas serão preservadas até que a duração da retenção do item expire ou até que a retenção seja removida da caixa de correio.
  
No exemplo a seguir, o comando irá excluir os resultados de pesquisa retornados por uma pesquisa de conteúdo chamada "remover mensagem de phishing". 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Para excluir por hardware os itens retornados pela pesquisa de conteúdo "remover mensagem de phishing", execute este comando:

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Observe que, quando você executa o comando anterior para excluir mensagens de forma reversível ou permanente, a pesquisa especificada ** pelo parâmetro searchName é a pesquisa de conteúdo que você criou na etapa 1. 
  
Para obter mais informações, consulte [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Mais informações

- **Como obter o status da operação de pesquisa e remoção?**

    Execute o **Get-ComplianceSearchAction** para obter o status da operação de exclusão. Observe que o objeto que é criado quando você executa o cmdlet **New-ComplianceSearchAction** é chamado usando este formato: `<name of Content Search>_Purge`. 
    
- **O que acontece após a exclusão de uma mensagem?**

   Uma mensagem que é excluída com `New-ComplianceSearchAction -Purge -PurgeType HardDelete` o comando é movida para a pasta purges e não pode ser acessada pelo usuário. Depois que a mensagem for movida para a pasta Purges, a mensagem será mantida pela duração do período de retenção do item excluído se a recuperação de item único estiver habilitada para a caixa de correio. (No Office 365, a recuperação de item individual é habilitada por padrão quando uma nova caixa de correio é criada.) Após o período de retenção do item excluído expirar, a mensagem será marcada para exclusão permanente e será removida do Office 365 na próxima vez que a caixa de correio for processada pelo assistente de pasta gerenciada. 

   Se você usar o `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` comando, as mensagens serão movidas para a pasta exclusões na pasta itens recuperáveis do usuário. Ele não é removido imediatamente do Office 365. O usuário pode recuperar mensagens na pasta Itens Excluídos de acordo com o período de retenção do item excluído configurado para a caixa de correio. Após esse período de retenção (ou se o usuário remover a mensagem antes do período expirar), a mensagem será movida para a pasta Remoções e não poderá mais ser acessada pelo usuário. Uma vez na pasta exPurgates, a mensagem será mantida pela duração com base no período de retenção de itens excluídos configurado para a caixa de correio se a recuperação de itens únicos estiver habilitada para a caixa de correio. (No Office 365, a recuperação de item individual é habilitada por padrão quando uma nova caixa de correio é criada.) Após o período de retenção do item excluído expirar, a mensagem será marcada para exclusão permanente e será removida do Office 365 na próxima vez que a caixa de correio for processada pelo assistente de pasta gerenciada. 
    
- **E se você precisar excluir uma mensagem de mais de 50.000 caixas de correio?**

    Conforme mencionado anteriormente, você pode executar uma operação de pesquisa e limpeza em um máximo de 50.000 caixas de correio. Se você tiver que executar uma operação de pesquisa e limpeza em mais de 50.000 caixas de correio, considere a criação de filtros de permissões de pesquisa temporários que reduziria o número de caixas de correio que seriam pesquisadas em menos de 50.000 caixas de correio. Por exemplo, se sua organização contiver caixas de correio em diferentes departamentos, Estados ou países, você poderá criar um filtro de permissões de pesquisa de caixa de correio com base em uma dessas propriedades de caixa de correio para pesquisar um subconjunto de caixas de correio em sua organização. Depois de criar o filtro permissões de pesquisa, você criaria a pesquisa (descrita na etapa 1) e excluiria a mensagem (descrita na etapa 3). Em seguida, você pode editar o filtro para pesquisar e limpar mensagens em um conjunto diferente de caixas de correio. Para obter mais informações sobre a criação de filtros de permissões de pesquisa, consulte [Configure Permissions Filtering for Content Search](permissions-filtering-for-content-search.md).
    
- **Os itens não indexados incluídos nos resultados da pesquisa serão excluídos?**

    Não, o comando ' New-ComplianceSearchAction-Purge não exclui itens não indexados. 
    
- **O que acontece quando uma mensagem é excluída de uma caixa de correio que foi colocada em bloqueio in-loco ou retenção de litígio ou é atribuída a uma política de retenção do Office 365?**

    Depois que a mensagem é eliminada e movida para a pasta Purges, a mensagem é mantida até que a duração da retenção expire. Se a duração da retenção for ilimitada, os itens serão retidos até que a retenção seja removida ou a duração da retenção seja alterada.
    
- **Por que o fluxo de trabalho de pesquisa e remoção é dividido entre diferentes grupos de função de central de segurança e conformidade?**

    Conforme explicado anteriormente, uma pessoa deve ser membro do grupo de funções Gerente de Descoberta Eletrônica ou receber a função de gerenciamento de Pesquisa de Conformidade para pesquisar nas caixas de correio. Para excluir mensagens, a pessoa precisa ser membro do grupo de funções Gerenciamento da Organização ou receber a função de gerenciamento Pesquisa e Limpar. Isso possibilita o controle de quem pode pesquisar nas caixas de correio da organização e quem pode excluir mensagens. 
