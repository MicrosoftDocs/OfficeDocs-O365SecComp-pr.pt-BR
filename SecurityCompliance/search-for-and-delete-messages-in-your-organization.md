---
title: Pesquisar e excluir mensagens de email em sua organização do Office 365 - ajuda de Admin
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
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Usar a pesquisa e limpar o recurso no Office 365 Security &amp; Centro de conformidade para pesquisar e excluir uma mensagem de email de todas as caixas de correio em sua organização.
ms.openlocfilehash: be83b2e3e765980ae401356b924c26c53386a2b3
ms.sourcegitcommit: d6a28c4f6db6a676ca960173e8ff8f17d4aa1c4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2019
ms.locfileid: "29755252"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Pesquisar e excluir mensagens de email em sua organização do Office 365 - ajuda de Admin

**Este artigo destina-se a administradores. Você está tentando localizar itens na sua caixa de correio que você deseja excluir? Consulte [Localizar uma mensagem ou item com a pesquisa instantânea](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Você pode usar o recurso de pesquisa de conteúdo no Office 365 para pesquisar e excluir uma mensagem de email de todas as caixas de correio em sua organização. Isso pode ajudá-lo a encontrar e remover email potencialmente prejudicial ou de alto risco, tais como:
  
- Mensagens que contêm anexos perigosos ou vírus
    
- Mensagens de phishing
    
- Mensagens que contêm dados confidenciais
    
> [!CAUTION]
> Pesquisa e limpar é um poderoso recurso que permite que qualquer pessoa atribuída as permissões necessárias para excluir mensagens de email das caixas de correio em sua organização. 
  
## <a name="before-you-begin"></a>Antes de começar

- Para criar e executar uma pesquisa de conteúdo, você precisa ser membro do grupo de função de **gerente de descoberta eletrônica** ou ser atribuída a função de gerenciamento de **Conformidade de pesquisa** . Para excluir mensagens, você precisa ser membro do grupo de funções de **Gerenciamento da organização** ou ser atribuída a função de gerenciamento de **Pesquisa e limpar** . Para obter informações sobre como adicionar usuários a um grupo de funções, consulte [Conceder aos usuários acesso para o Centro de conformidade do & de segurança do Office 365](grant-access-to-the-security-and-compliance-center.md).
    
- Você precisa usar segurança & PowerShell do Centro de conformidade para excluir mensagens. Consulte a [etapa 2](#step-2-connect-to-security-amp-compliance-center-powershell) para obter instruções sobre como se conectar.
    
- Um máximo de 10 itens por caixa de correio pode ser removido de uma só vez. Como a capacidade de pesquisar e remover mensagens destina-se para ser uma ferramenta de resposta a incidentes, esse limite ajuda a garantir que as mensagens rapidamente serão removidas das caixas de correio. Esse recurso não é destinado a limpar caixas de correio do usuário. Para excluir mais de 10 itens, você pode usar o comando **Search-Mailbox-DeleteContent** no PowerShell do Exchange Online. Consulte [Procurar e excluir mensagens - ajuda de Admin](search-for-and-delete-messagesadmin-help.md).
    
- O número máximo de caixas de correio em uma pesquisa de conteúdo que você pode excluir itens na fazendo uma pesquisa e ação de limpeza é 50.000. Se a pesquisa de conteúdo (que você criar na [etapa 1](#step-1-create-a-content-search-to-find-the-message-to-delete)) tem mais de 50.000 caixas de correio de origem, a ação de limpeza (que você criar na etapa 3) falhará. Consulte a seção de [informações adicionais](#more-information) para uma dica sobre como realizar uma pesquisa e limpar a operação em mais de 50.000 caixas de correio. 
    
- O procedimento neste artigo só pode ser usado para excluir itens em caixas de correio do Exchange Online e as pastas públicas. Você não pode usá-lo para excluir o conteúdo do SharePoint ou OneDrive para sites corporativos.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Etapa 1: Criar uma Pesquisa de conteúdo para localizar a mensagem para exclusão

A primeira etapa é criar e executar uma pesquisa de conteúdo para encontrar a mensagem que você deseja remover de caixas de correio em sua organização. Você pode criar a pesquisa usando a segurança &amp; Centro de conformidade ou executando os cmdlets **New-ComplianceSearch** e **Start-ComplianceSearch** . As mensagens que correspondem à consulta para esta pesquisa será excluída executando o **New-ComplianceSearchAction-limpar** command na [etapa 3](#step-3-delete-the-message). Para obter informações sobre como criar uma pesquisa de conteúdo e configuração de consultas de pesquisa, consulte os tópicos a seguir: 
  
- [Pesquisa de conteúdo no Office 365](content-search.md)
    
- [Consultas de palavra-chave de pesquisa de conteúdo](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Os locais de conteúdo que são pesquisados na pesquisa de conteúdo que você criar nesta etapa não podem incluir SharePoint ou OneDrive para sites corporativos. Você pode incluir apenas caixas de correio e pastas públicas em uma pesquisa de conteúdo que será usado para mensagens de email. Se a pesquisa de conteúdo inclui sites, você receberá um erro na etapa 3 quando você executa o cmdlet **New-ComplianceSearchAction** . 
  
### <a name="tips-for-finding-messages-to-remove"></a>Dicas para localizar mensagens para remoção

O objetivo da consulta de pesquisa é restringir os resultados da pesquisa apenas à mensagem ou mensagens que você deseja remover. Veja algumas dicas:
  
- Se você souber o texto ou a frase exata usada na linha de assunto da mensagem, use a propriedade **Subject** na consulta de pesquisa. 
    
- Se você souber a data exata (ou o intervalo de datas) da mensagem, inclua a propriedade **Received** na consulta de pesquisa. 
    
- Se você souber quem enviou a mensagem, inclua a propriedade **From** na consulta de pesquisa. 
    
- Visualize os resultados da pesquisa para verificar se a pesquisa de conteúdo retornou apenas a mensagem (ou mensagens) que você deseja excluir.
    
- Use as estatísticas de estimativa de pesquisa (exibidos no painel de detalhes da pesquisa na segurança &amp; Centro de conformidade ou usando o cmdlet [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ) para obter uma contagem do número total de resultados. 
    
Aqui estão dois exemplos de consultas para localizar mensagens de email suspeitas.
  
- Essa consulta retornará as mensagens que foram recebidas pelos usuários entre 13 de abril de 2016 e 14 de abril de 2016 e que contêm as palavras "ação" e "obrigatório" na linha de assunto.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Essa consulta retornará as mensagens que foram enviadas por chatsuwloginsset12345@outlook.com e que contêm a frase exata "Atualizar as informações da sua conta" na linha de assunto.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Etapa 2: Conectar ao PowerShell de centro de conformidade de & de segurança

A próxima etapa é conectar para segurança & PowerShell do Centro de conformidade para sua organização. Para obter instruções detalhadas, consulte [conectar a segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Se a sua conta do Office 365 usa a autenticação multifator (MFA) ou federados autenticação, é possível usar as instruções no tópico anterior sobre como conectar a segurança & PowerShell do Centro de conformidade. Em vez disso, consulte as instruções no tópico [conectar ao PowerShell do Centro de conformidade de & de segurança do Office 365 usando a autenticação multifator](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).
  
## <a name="step-3-delete-the-message"></a>Etapa 3: Excluir a mensagem

Depois que você criou e uma pesquisa de conteúdo para retornar a mensagem que você deseja remover e conectados à segurança-refinado &amp; PowerShell do Centro de conformidade, a etapa final é executar o cmdlet **New-ComplianceSearchAction** para excluir a mensagem. Você pode reversível ou disco rígido-excluir a mensagem. Uma mensagem excluída é movida para a pasta de itens recuperáveis do usuário e retida até que o período de retenção de item excluído expirar. Mensagens excluídas de disco rígido são marcadas para remoção permanente da caixa de correio e serão removidas permanentemente na próxima vez em que a caixa de correio é processada pelo Assistente de pasta gerenciada. Se a recuperação de item único está habilitada para a caixa de correio, itens excluídos rígido serão removidas permanentemente depois que o período de retenção de item excluído expira. Se uma caixa de correio for colocada em espera, as mensagens excluídas são preservadas até que a duração de espera para o item expira ou até que a suspensão seja removida da caixa de correio.
  
No exemplo a seguir, o comando irá reversível excluir os resultados de pesquisa retornados por uma pesquisa de conteúdo chamado "Remover a mensagem de Phishing". 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Disco rígido-excluídos os itens retornados pela pesquisa conteúda "Remover a mensagem de Phishing", você precisará executar este comando:

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Observe que, quando você executa o comando anterior às mensagens soft - ou disco rígido-delete, a pesquisa especificada pelo parâmetro *SearchName* é a pesquisa de conteúdo que você criou na etapa 1. 
  
Para obter mais informações, consulte [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Mais informações

- **Como você obter o status da pesquisa e remover operação?**

    Execute o **Get-ComplianceSearchAction** para obter o status sobre a operação de exclusão. Observe que o objeto que é criado quando você executar o cmdlet **New-ComplianceSearchAction** é denominado usando este formato: `<name of Content Search>_Purge`. 
    
- **O que acontece após a exclusão de uma mensagem?**

   Uma mensagem que será excluída com a `New-ComplianceSearchAction -Purge -PurgeType HardDelete` comando é movido para a pasta limpezas e não pode ser acessado pelo usuário. Depois que a mensagem é movida para a pasta limpezas, a mensagem é mantida durante o período de retenção de item excluído se a recuperação de item único está habilitada para a caixa de correio. (No Office 365, recuperação de item único está habilitada por padrão quando uma nova caixa de correio é criada.) Depois que o período de retenção de item excluído expira, a mensagem é marcada para exclusão permanente e vai ser removida do Office 365 na próxima vez em que a caixa de correio é processada pelo Assistente de pasta gerenciada. 

   Se você usar o `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` de comando, as mensagens são movidas para a pasta de exclusões na pasta de itens recuperáveis do usuário. Ele não é imediatamente removido do Office 365. O usuário pode recuperar mensagens na pasta Itens excluídos para a duração com base no período de retenção de item excluído configurado para a caixa de correio. Depois que esse período de retenção expira (ou se o usuário limpa a mensagem antes que ela expirará), a mensagem é movida para a pasta limpezas e não pode mais ser acessada pelo usuário. Uma vez na pasta limpezas, a mensagem é mantida para a duração com base no período de retenção de item excluído configurado para a caixa de correio, caso a recuperação de itens único está habilitada para a caixa de correio. (No Office 365, recuperação de item único está habilitada por padrão quando uma nova caixa de correio é criada.) Depois que o período de retenção de item excluído expira, a mensagem é marcada para exclusão permanente e vai ser removida do Office 365 na próxima vez que a caixa de correio é processada pelo Assistente de pasta gerenciada. 
    
- **E se você tiver que excluir uma mensagem de mais de 50.000 caixas de correio?**

    Conforme indicado anteriormente, você pode realizar uma pesquisa e operação em um máximo de caixas de 50.000 correio de limpeza. Se você precisar fazer uma pesquisa e limpar a operação em mais de 50.000 caixas de correio, considere a criação de filtros de permissões de pesquisa temporário que seriam reduzir o número de caixas de correio que seria ser pesquisados a menos de 50.000 caixas de correio. Por exemplo, se sua organização contiver caixas de correio em diferentes departamentos, estados ou países, você pode criar um filtro de permissões de pesquisa de caixa de correio com base em uma dessas propriedades de caixa de correio para pesquisar um subconjunto de caixas de correio em sua organização. Depois de criar o filtro de permissões de pesquisa, crie a pesquisa (descrita na etapa 1) e, em seguida, excluir a mensagem (descrita na etapa 3). Em seguida, você pode editar o filtro para pesquisar e limpar mensagens em um conjunto diferente de caixas de correio. Para obter mais informações sobre como criar filtros de permissões de pesquisa, consulte [Configure permissions filtragem para a pesquisa de conteúdo](permissions-filtering-for-content-search.md).
    
- **Serão incluídos nos resultados da pesquisa de itens indexados excluídos?**

    Não, o ' New-ComplianceSearchAction-comando Limpar não excluir itens indexados. 
    
- **O que acontece se uma mensagem for excluída de uma caixa de correio que foi colocada em retenção In-loco ou retenção de litígio ou é atribuída a uma política de retenção do Office 365?**

    Depois que a mensagem é limpo e movida para a pasta limpezas, a mensagem é retida até que a duração da retenção expira. Se a duração da retenção for ilimitada, itens são mantidos até que a suspensão seja removida ou a duração da retenção é alterada.
    
- **Por que é a pesquisa e remover dividido entre diferentes grupos de função do Centro de conformidade & de segurança do fluxo de trabalho?**

    Conforme explicado anteriormente, uma pessoa deve ser membro do grupo de função de Gerenciador de descoberta eletrônica ou ser atribuída a função de gerenciamento de conformidade de pesquisa para pesquisar caixas de correio. Para excluir mensagens, uma pessoa deve ser membro do grupo de funções de gerenciamento da organização ou ser atribuída a função de gerenciamento de pesquisa e limpar. Isso possibilita para controlar quem pode pesquisar caixas de correio na organização e quem pode excluir mensagens. 
