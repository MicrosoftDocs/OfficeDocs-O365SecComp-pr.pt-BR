---
title: Pesquisar o log de auditoria do Office 365 para solucionar problemas de cenários comuns
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
description: Você pode usar a ferramenta de pesquisa de log de auditoria do Office 365 para ajudá-lo a solucionar problemas comuns, como uma investigação de uma conta comprometida ou descobrir quem configurar encaminhamento de email para uma caixa de correio.
ms.openlocfilehash: 930e311712e49214ca2a51e256c29e5f959deab8
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2018
ms.locfileid: "27123894"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Pesquisar o log de auditoria do Office 365 para solucionar problemas de cenários comuns

Este artigo descreve como usar a ferramenta de pesquisa de log de auditoria do Office 365 para ajudá-lo a solucionar problemas de cenários comuns de suporte. Isso inclui o uso do log de auditoria para:

- Localize o endereço IP do computador usado para acessar uma conta comprometida
- Determinar quem configurar encaminhamento de email para uma caixa de correio
- Determinar se um usuário excluiu itens de email em suas caixas de correio
- Determinar se um usuário criada uma regra de caixa de entrada

## <a name="using-the-office-365-audit-log-search-tool"></a>Usando a ferramenta de pesquisa de log de auditoria do Office 365

Cada um dos cenários de solução de problemas descritos neste artigo são baseados em usando a ferramenta de pesquisa de log de auditoria no Centro de conformidade & segurança do Office 365. Esta seção lista as permissões exigidas para pesquisar o log de auditoria e descreve as etapas para acessar e executar pesquisas de log de auditoria. Cada seção do cenário fornece orientações específicas sobre como configurar uma consulta de pesquisa de log de auditoria e o que procurar as informações detalhadas nos registros de auditoria que correspondem aos critérios de pesquisa.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Permissões necessárias para usar a ferramenta de pesquisa de log de auditoria

Você precisa ter a função Logs de auditoria somente para exibição ou Logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de função de gerenciamento de conformidade e gerenciamento da organização na página **permissões** no Centro de administração do Exchange. Para obter mais informações, consulte a [função de gerenciar grupos no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Pesquisas de log de auditoria em execução

Esta seção descreve as Noções básicas para criar e executar pesquisas de log de auditoria. Use estas instruções como ponto de partida para cada cenário de solução de problemas neste artigo. Para obter instruções detalhadas, consulte [Search da auditoria, faça logon no Centro de conformidade & segurança do Office 365 ](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Acesse [https://protection.office.com](https://protection.office.com).
  
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.

3. No painel à esquerda do Centro de conformidade & segurança, clique em **Pesquisar & investigação** > **pesquisa de log de auditoria**.
    
    A página de **pesquisa de log de auditoria** é exibida. 
    
    ![Configurar critérios e, em seguida, clique em Pesquisar para executar a pesquisa](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Você pode configurar os seguintes critérios de pesquisa. Observe que cada cenário de solução de problemas neste artigo recomendará a orientação específica para configurar esses campos.
    
    r. **atividades** - clique na lista suspensa para exibir as atividades que você pode pesquisar. Depois de executar a pesquisa, somente os registros de auditoria para as atividades selecionadas são exibidos. A seleção de **Mostrar os resultados de todas as atividades** exibirá resultados para todas as atividades que atendem aos critérios de pesquisa. Você também precisa deixe este campo em branco em alguns dos cenários de solução de problemas.
    
    b. **Data de início** e **Data de término** - selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. Últimos sete dias são marcados por padrão. A data e hora são apresentados no formato Tempo Universal Coordenado (UTC). O intervalo de datas máximo que você pode especificar é 90 dias.

    resultados para mais c. **usuários** - clique nesta caixa e selecione um ou mais usuários para exibir a pesquisa. Registros de auditoria da atividade selecionada executadas pelos usuários que você selecionar nesta caixa são exibidos na lista de resultados. Deixe esta caixa em branco para retornar as entradas para todos os usuários (e contas de serviço) em sua organização.
    
    d. o **arquivo, pasta ou site** - digite parte ou todo um nome de arquivo ou pasta para procurar a atividade relacionada ao arquivo da pasta que contém a palavra-chave especificada. Você também pode especificar uma URL de um arquivo ou pasta. Se você usar uma URL, certifique-se de que o tipo o caminho completo do URL, ou se você digitar apenas uma parte da URL, não inclua quaisquer caracteres especiais ou espaços. Deixe esta caixa em branco para retornar as entradas para todos os arquivos e pastas em sua organização. Observe que este campo for deixado em branco em todos os cenários de solução de problemas neste artigo.
    
5. Clique em **pesquisa** para executar a pesquisa usando os critérios de pesquisa. 
    
    Os resultados da pesquisa são carregados e, após alguns momentos são exibidas em **resultados** na página de **pesquisa de log de auditoria** . Cada um para as seções a seguir fornece orientação sobre o que procurar o cenário de solução de problemas específico.

    Para obter mais informações sobre a visualização, filtragem ou exportar os resultados de pesquisa do log de auditoria, consulte:

    - [Exibir resultados da pesquisa](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtrar os resultados da pesquisa](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exportar resultados de pesquisa](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Localizar o endereço IP do computador usado para acessar uma conta comprometida

O endereço IP correspondente a uma atividade realizada por qualquer usuário que está incluído na maioria dos registros de auditoria. Informações sobre o cliente usada também estão incluídas no registro de auditoria.

Aqui está como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** - se relevantes ao seu caso, selecione uma atividade específica a ser pesquisado. Para contas comprometidas de solução de problemas, considere a possibilidade de selecionar a atividade do **usuário conectado à caixa de correio** em **atividades de caixa de correio do Exchange**. Isso retornará a auditoria registra mostrando o endereço IP que foi usado ao fazer logon na caixa de correio. Caso contrário, deixe este campo em branco para retornar os registros de auditoria para todas as atividades. 

> [!TIP]
> Deixe este campo em branco retornará **UserLoggedIn** atividades, que é uma atividade do Azure Active Directory que indica que alguém tenha entrado em uma conta de usuário do Office 365. Use a filtragem nos resultados da pesquisa para exibir os registros de auditoria de **UserLoggedIn** .

**Data de início** e **Data de término** - selecione um intervalo de datas que se aplica à sua investigação.

**Os usuários** - se você estiver investigando uma conta comprometida, selecione o usuário cuja conta foi comprometida. Isso retornará os registros de auditoria para atividades realizadas àquela conta de usuário.

**Arquivos, pastas ou sites** - deixar vazio este campo.

Após executar a pesquisa, o endereço IP para cada atividade é exibido na coluna **endereço IP** nos resultados da pesquisa. Clique no registro nos resultados da pesquisa para exibir informações mais detalhadas na página submenu.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Determinar quem configurar encaminhamento de email para uma caixa de correio

Quando o encaminhamento de email estiver configurado para uma caixa de correio, mensagens de email que são enviadas à caixa de correio são encaminhadas para outra caixa de correio. As mensagens podem ser encaminhadas aos usuários dentro ou fora da sua organização. Quando o encaminhamento de email estiver configurado em uma caixa de correio, o cmdlet Exchange Online subjacente que é usado é **Set-Mailbox**.

Aqui está como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** - deixe esse campo em branco para que a pesquisa retorna registros de auditoria para todas as atividades. Isso é necessário para retornar qualquer auditar registros relacionados para o cmdlet **Set-Mailbox** .

**Data de início** e **Data de término** - selecione um intervalo de datas que se aplica à sua investigação.

**Os usuários** -, a menos que você está investigando um problema para um usuário específico de encaminhamento de email, deixe este campo em branco. Isso ajudará a identificar se o encaminhamento de email foi configurado para qualquer usuário.

**Arquivos, pastas ou sites** - deixar vazio este campo.

Após executar a pesquisa, clique em **Filtrar resultados** na página de resultados da pesquisa. Na caixa sob o cabeçalho da coluna de **atividade** , digite **Set-Mailbox** para que apenas os registros de auditoria relacionados para o cmdlet **Set-Mailbox** sejam exibidos.

![Filtrando os resultados de uma pesquisa de log de auditoria](media/emailforwarding1.png)

Neste ponto, você precisará analisar os detalhes de cada registro de auditoria para determinar se a atividade está relacionada ao encaminhamento de email. Clique no registro de auditoria para exibir a página **detalhes** do submenu e clique em **obter mais informações**. As seguinte captura de tela e descrições destaques as informações que indicam o encaminhamento de email foi definidas na caixa de correio.

![Informações detalhadas do registro de auditoria](media/emailforwarding2.png)

r. no campo **ObjectId** , o alias da caixa de correio que o encaminhamento de email foi definido em é exibida. Esta caixa de correio também será exibida na coluna de **Item** na página de resultados da pesquisa.

b. no campo de **parâmetros** , o valor *ForwardingSmtpAddress* indica que encaminhar email tiver sido definida na caixa de correio. Neste exemplo, o email está sendo encaminhado para o email endereço mike@contoso.com, que está fora da organização alpinehouse.onmicrosoft.com.

c. o valor *True* para o parâmetro *DeliverToMailboxAndForward* indica que uma cópia da mensagem entregue sarad@alpinehouse.onmicrosoft.com *e* é encaminhada para o endereço de email especificado pelo *ForwardingSmtpAddress *parâmetro, que neste exemplo é mike@contoso.com. Se o valor para o parâmetro *DeliverToMailboxAndForward* estiver definido como *False*, o email só será encaminhada para o endereço especificado pelo parâmetro *ForwardingSmtpAddress* . Ele não é entregue à caixa de correio especificada no campo **ObjectId** .

d. o campo **UserId** indica que o usuário que definir o encaminhamento de email na caixa de correio especificada no campo de campo **ObjectId** . Esse usuário também é exibido na coluna **User** na página de resultados da pesquisa. Nesse caso, parece que o proprietário da caixa de correio definir o encaminhamento de email na sua caixa de correio.

Se você determinar que o encaminhamento de email não deve ser definido na caixa de correio, você pode removê-lo executando o seguinte comando no PowerShell do Exchange Online:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Consulte o artigo [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) para obter mais informações sobre os parâmetros relacionados ao encaminhamento de email.

## <a name="determining-if-a-user-deleted-email-items"></a>Determinando se um usuário excluiu itens de email

Antes que os registros de log de auditoria sobre excluído itens de email são salvos no log de auditoria do Office 365, auditoria de caixa de correio deve estar habilitado para cada caixa de correio do usuário em sua organização. Além disso, as ações de caixa de correio SoftDelete e HardDelete precisa ser habilitado para auditoria. Para obter instruções, consulte [Habilitar caixa de correio auditorias no Office 365](enable-mailbox-auditing.md). Se a auditoria de caixa de correio já está habilitada para usuários, use as etapas a seguir para pesquisar o log de auditoria para eventos relacionados a itens de email excluído.

Aqui está como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** - em **atividades de caixa de correio do Exchange**, selecione uma ou ambas as seguintes atividades:

- **As mensagens excluídas da pasta Itens excluídos** - esta atividade corresponde à caixa de correio **SoftDelete** ação de auditoria. Esta atividade também é registrada quando um usuário exclui permanentemente um item selecionando-o e pressionando **Shift + Delete**. Depois que um item é excluído permanentemente, o usuário pode recuperar a ele até o período de retenção de item excluído expira.

- **Purged mensagens de caixa de correio** - esta atividade corresponde à caixa de correio **HardDelete** ação de auditoria. Isso é registrado quando um usuário limpa um item da pasta itens recuperáveis. Os administradores podem usar a ferramenta de pesquisa de conteúdo no Centro de conformidade & segurança do Office 365 para procurar e recuperar limpo itens até o período de retenção de item excluído expira ou se mais caixas de correio do usuário estiver em espera.

**Data de início** e **Data de término** - selecione um intervalo de datas que se aplica à sua investigação.

**Os usuários** - se você selecionar um usuário neste campo, a ferramenta de pesquisa de log de auditoria retornará os registros de auditoria para itens de email que foram excluídos (SoftDeleted ou HardDeleted) por usuário que você especificar. Em alguns casos, o usuário que exclui um email não pode ser o proprietário da caixa de correio.

**Arquivos, pastas ou sites** - deixar vazio este campo.

Depois de executar a pesquisa, você pode filtrar os resultados de pesquisa para exibir os registros de auditoria para itens excluída ou para itens excluídos de disco rígido. Clique no registro de auditoria para exibir a página **detalhes** do submenu e clique em **obter mais informações**. Informações adicionais sobre o item excluído, como a linha de assunto e o local do item quando ele foi excluído, são exibidas no campo **AffectedItems** . As capturas de tela a seguintes mostram um exemplo do campo **AffectedItems** de um item excluída e um item excluído de disco rígido.

**Exemplo de campo AffectedItems para item excluída**

![Registro de auditoria para item excluída](media/softdeleteditem.png)

**Exemplo de campo AffectedItems de item excluído de disco rígido**

![Registro de auditoria para o item de email excluída por disco rígido](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Recuperando itens de email excluídos

Os usuários podem recuperar itens excluída se o período de retenção de itens excluídos não expirou. No Exchange Online, o período de retenção de itens excluído do padrão é de 14 dias, mas os administradores podem aumentar essa configuração para um máximo de 30 dias. Ponto de usuários para o artigo [recuperar itens excluídos ou email no Outlook Web App](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) para obter instruções sobre como recuperar os itens excluíram.

Conforme explicado anteriormente, os administradores podem ser capazes de recuperar itens excluídos de disco rígido, se o período de retenção de item excluído não expirou ou se a caixa de correio estiver em espera, caso em que os itens são mantidos até que a duração da retenção expira. Quando você executa uma pesquisa de conteúdo, excluída e disco rígido excluídos itens na pasta itens recuperáveis são retornadas nos resultados da pesquisa, caso haja correspondência com a consulta de pesquisa. Para obter mais informações sobre como executar pesquisas de conteúdo, consulte o [Conteúdo de pesquisa no Office 365](content-search.md).

> [!TIP]
> Para procurar itens de email excluído, procure todo ou parte da linha de assunto exibida no campo **AffectedItems** do registro de auditoria.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Determinando se um usuário criada uma regra de caixa de entrada

Quando os usuários criarem uma regra de caixa de entrada para suas caixas de correio do Exchange Online, um registro de auditoria correspondente é salvo no log de auditoria. Para obter mais informações sobre regras de caixa de entrada, consulte:

- [Usar regras de caixa de entrada do Outlook na web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Gerenciar mensagens de email no Outlook usando regras](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Aqui está como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** - em **atividades de caixa de correio do Exchange**, selecione **New-InboxRule criar/modificar/habilitar/desabilitar a regra de caixa de entrada**.

**Data de início** e **Data de término** - selecione um intervalo de datas que se aplica à sua investigação.

**Os usuários** -, a menos que você está investigando um usuário específico, deixe este campo em branco. Isso ajudará a identificar novas regras de caixa de entrada configuradas por qualquer usuário.

**Arquivos, pastas ou sites** - deixar vazio este campo.

Depois de executar a pesquisa, quaisquer registros de auditoria para esta atividade são exibidos nos resultados da pesquisa. Clique em um registro de auditoria para exibir a página de submenu **detalhes** e, em seguida, clique em **obter mais informações**. Informações sobre as definições de regra de caixa de entrada são exibidas no campo **parâmetros** . As descrições e os captura de tela a seguir destaca as informações sobre regras de caixa de entrada.

![Registro de auditoria para nova regra de caixa de entrada](media/NewInboxRuleRecord.png)

r. no campo **ObjectId** , o nome completo da regra de caixa de entrada é exibido. Esse nome inclui o alias da caixa de correio do usuário (por exemplo, SaraD) e o nome da regra de caixa de entrada (por exemplo, "mover mensagens de admin").

b. no campo de **parâmetros** , a condição da regra de caixa de entrada é exibida. Neste exemplo, a condição é especificada pelo parâmetro *de* . O valor definido para o parâmetro *de* indica que a regra de caixa de entrada atua no email enviado por admin@alpinehouse.onmicrosoft.com. Para obter uma lista completa dos parâmetros que podem ser usados para definir as condições de regras de caixa de entrada, consulte o artigo de [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. o parâmetro *MoveToFolder* Especifica a ação da regra de caixa de entrada; Neste exemplo, as mensagens recebidas de admin@alpinehouse.onmicrosoft.com são movidas para a pasta denominada *AdminSearch*. Consulte também o artigo de [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) para obter uma lista completa de parâmetros que podem ser usados para definir a ação de uma regra de caixa de entrada.

d. o campo **UserId** indicam que o usuário que criou a regra de caixa de entrada especificada no campo **ObjectId** . Esse usuário também é exibido na coluna **User** na página de resultados da pesquisa.