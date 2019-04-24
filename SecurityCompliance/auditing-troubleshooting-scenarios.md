---
title: Pesquisar o log de auditoria do Office 365 para solucionar problemas de cenários comuns
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
- MET150
- MOE150
description: Você pode usar a ferramenta de pesquisa de log de auditoria do Office 365 para ajudá-lo a solucionar problemas comuns, como investigar uma conta comprometida ou descobrir quem configurou o encaminhamento de email para uma caixa de correio.
ms.openlocfilehash: bd0483f2b2e209dc0cbd2b03eda928fd8d44d7b0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250229"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Pesquisar o log de auditoria do Office 365 para solucionar problemas de cenários comuns

Este artigo descreve como usar a ferramenta de pesquisa de log de auditoria do Office 365 para ajudá-lo a solucionar problemas de cenários de suporte comuns. Isso inclui o uso do log de auditoria para:

- Localizar o endereço IP do computador usado para acessar uma conta comprometida
- Determinar quem configurou o encaminhamento de email para uma caixa de correio
- Determinar se um usuário excluiu itens de email em suas caixas de correio
- Determinar se um usuário criou uma regra de caixa de entrada

## <a name="using-the-office-365-audit-log-search-tool"></a>Usando a ferramenta de pesquisa de log de auditoria do Office 365

Cada um dos cenários de solução de problemas descritos neste artigo se baseia em usar a ferramenta de pesquisa de log de auditoria no centro de segurança e conformidade do Office 365. Esta seção lista as permissões necessárias para pesquisar o log de auditoria e descreve as etapas para acessar e executar pesquisas de log de auditoria. Cada seção de cenário fornece orientações específicas sobre como configurar uma consulta de pesquisa de log de auditoria e o que procurar nas informações detalhadas nos registros de auditoria que correspondem aos critérios de pesquisa.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Permissões necessárias para usar a ferramenta de pesquisa de log de auditoria

Você precisa receber a função de logs de auditoria somente para exibição ou logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de função gerenciamento de conformidade e gerenciamento da organização na página **permissões** no centro de administração do Exchange. Observe que os administradores globais no Office 365 e Microsoft 365 são automaticamente adicionados como membros do grupo de função gerenciamento da organização no Exchange Online. Para obter mais informações, consulte [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Executando pesquisas de log de auditoria

Esta seção descreve as noções básicas para criar e executar pesquisas de log de auditoria. Use estas instruções como ponto de partida para cada cenário de solução de problemas neste artigo. Para obter instruções passo a passo detalhadas, consulte [Search the Audit Log](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. AcEsse [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) e entre usando sua conta corporativa ou de estudante.
    
    A página **pesquisa de log de auditoria** é exibida. 
    
    ![Configure critérios e clique em Pesquisar para executar a pesquisa](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Você pode configurar os seguintes critérios de pesquisa. Observe que cada cenário de solução de problemas neste artigo recomendará orientações específicas para configurar esses campos.
    
    a. **Atividades** -clique na lista suspensa para exibir as atividades que você pode pesquisar. Depois de executar a pesquisa, somente os registros de auditoria das atividades selecionadas são exibidos. Selecionar **Mostrar resultados de todas as atividades** exibirá os resultados de todas as atividades que atendem aos outros critérios de pesquisa. Você também precisará deixar este campo em branco em alguns dos cenários de solução de problemas.
    
    b. **Data de início** e **data de término** -selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. Os últimos sete dias são selecionados por padrão. A data e a hora são apresentadas no formato UTC (tempo Universal Coordenado). O intervalo de datas máximo que você pode especificar é de 90 dias.

    c. **Usuários** – clique nesta caixa e selecione um ou mais usuários para exibir os resultados da pesquisa. Os registros de auditoria da atividade selecionada executada pelos usuários selecionados nesta caixa são exibidos na lista de resultados. Deixe esta caixa em branco para retornar entradas para todos os usuários (e contas de serviço) em sua organização.
    
    d. **Arquivo, pasta ou site** -digite alguns ou todos os nomes de arquivo ou pasta para pesquisar atividades relacionadas ao arquivo de pasta que contém a palavra-chave especificada. Você também pode especificar uma URL de um arquivo ou pasta. Se você usar uma URL, certifique-se de digitar o caminho de URL completo ou se digitar apenas uma parte da URL, não inclua nenhum caractere ou espaço especial. Deixe esta caixa em branco para retornar entradas para todos os arquivos e pastas em sua organização. Observe que esse campo é deixado em branco em todos os cenários de solução de problemas neste artigo.
    
5. Clique em **Pesquisar** para executar a pesquisa usando seus critérios de pesquisa. 
    
    Os resultados da pesquisa são carregados e após alguns momentos em que são exibidos em **resultados** na página **pesquisa de log de auditoria** . Cada uma das seções a seguir fornecerá orientações sobre as coisas a serem procuradas no cenário específico de solução de problemas.

    Para obter mais informações sobre a exibição, filtragem ou exportação de resultados de pesquisa de log de auditoria, consulte:

    - [Exibir resultados da pesquisa](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtrar resultados da pesquisa](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exportar resultados de pesquisa](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Localizando o endereço IP do computador usado para acessar uma conta comprometida

O endereço IP correspondente a uma atividade realizada por qualquer usuário é incluído na maioria dos registros de auditoria. As informações sobre o cliente usado também estão incluídas no registro de auditoria.

ConFira aqui como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** – se relevante para o seu caso, selecione uma atividade específica a ser pesquisada. Para solucionar problemas de contas comprometidas, considere selecionar o **usuário conectado à** atividade de caixa de correio em **atividades de caixa de correio do Exchange**. Isso retornará registros de auditoria, mostrando o endereço IP que foi usado ao entrar na caixa de correio. Caso contrário, deixe este campo em branco para retornar os registros de auditoria de todas as atividades. 

> [!TIP]
> Deixar este campo em branco retornará **** as atividades userlogged, que é uma atividade do Azure Active Directory que indica que alguém entrou em uma conta de usuário do Office 365. Use filtragem nos resultados da pesquisa para exibir os **** registros de auditoria userlogind.

**Data de início** e **data de término** -selecione um intervalo de datas que se aplica à sua investigação.

**Usuários** – se estiver investigando uma conta comprometida, selecione o usuário cuja conta foi comprometida. Isso retornará registros de auditoria para atividades realizadas por essa conta de usuário.

**Arquivo, pasta ou site** -deixe este campo em branco.

Depois de executar a pesquisa, o endereço IP de cada atividade é exibido na coluna **endereço IP** nos resultados da pesquisa. Clique no registro nos resultados da pesquisa para exibir informações mais detalhadas sobre a página do menu de atalho.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Determinando quem configurou o encaminhamento de email para uma caixa de correio

Quando o encaminhamento de emails é configurado para uma caixa de correio, as mensagens de email enviadas para a caixa de correio são encaminhadas para outra caixa de correio. As mensagens podem ser encaminhadas para os usuários dentro ou fora da sua organização. Quando o encaminhamento de emails é configurado em uma caixa de correio, o cmdlet do Exchange Online subjacente usado é **Set-Mailbox**.

ConFira aqui como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** -deixe este campo em branco para que a pesquisa retorne registros de auditoria de todas as atividades. Isso é necessário para retornar registros de auditoria relacionados ao cmdlet **Set-Mailbox** .

**Data de início** e **data de término** -selecione um intervalo de datas que se aplica à sua investigação.

**Usuários** – a menos que você esteja investigando um problema de encaminhamento de email para um usuário específico, deixe este campo em branco. Isso ajudará a identificar se o encaminhamento de emails foi configurado para qualquer usuário.

**Arquivo, pasta ou site** -deixe este campo em branco.

Depois de executar a pesquisa, clique em **filtrar resultados** na página de resultados da pesquisa. Na caixa em cabeçalho da coluna **atividade** , digite **Set-Mailbox** para que apenas os registros de auditoria relacionados ao cmdlet **Set-Mailbox** sejam exibidos.

![Filtrando os resultados de uma pesquisa de log de auditoria](media/emailforwarding1.png)

Neste ponto, você precisa examinar os detalhes de cada registro de auditoria para determinar se a atividade está relacionada ao encaminhamento de email. Clique no registro de auditoria para exibir a página do submenu **detalhes** e, em seguida, clique em **mais informações**. A captura de tela e as descrições a seguir destacam as informações que indicam que o encaminhamento de emails foi definido na caixa de correio.

![Informações detalhadas do registro de auditoria](media/emailforwarding2.png)

a. No campo **ObjectID** , o alias da caixa de correio para o qual o encaminhamento de email foi definido é exibido. Essa caixa de correio também é exibida na coluna **Item** na página de resultados da pesquisa.

b. No campo **parâmetros** , o valor *ForwardingSmtpAddress* indica que o encaminhamento de emails foi definido na caixa de correio. Neste exemplo, o email está sendo encaminhado para o endereço de email mike@contoso.com, que está fora da organização do alpinehouse.onmicrosoft.com.

c. O valor *true* para o parâmetro *DeliverToMailboxAndForward* indica que uma cópia da mensagem entregue ao Sarad@alpinehouse.onmicrosoft.com *e* é encaminhada para o endereço de email especificado pelo *ForwardingSmtpAddress *o parâmetro, que neste exemplo é Mike@contoso.com. Se o valor do parâmetro *DeliverToMailboxAndForward* for definido como *false*, o email será encaminhada somente para o endereço especificado pelo parâmetro *ForwardingSmtpAddress* . Ele não é entregue à caixa de correio especificada no campo **ObjectID** .

d. O campo **userid** indica o usuário que define o encaminhamento de emails na caixa de correio especificada no campo de campo **ObjectID** . Esse usuário também é exibido na coluna **usuário** na página de resultados da pesquisa. Nesse caso, parece que o proprietário da caixa de correio define o encaminhamento de email em sua caixa de correio.

Se você determinar que o encaminhamento de emails não deve ser definido na caixa de correio, é possível removê-lo executando o seguinte comando no PowerShell do Exchange Online:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Consulte o artigo [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) para obter mais informações sobre os parâmetros relacionados ao encaminhamento de email.

## <a name="determining-if-a-user-deleted-email-items"></a>Determinando se um usuário excluiu itens de email

A partir de janeiro de 2019, a Microsoft está ativando o log de auditoria de caixa de correio por padrão para todas as organizações do Office 365 e Microsoft. Isso significa que determinadas ações executadas por proprietários de caixa de correio são automaticamente registradas, e os registros de auditoria de caixa de correio correspondentes estarão disponíveis quando você procurá-los no log de auditoria de caixa de correio. Antes de a auditoria da caixa de correio ser ativada por padrão, você precisava habilitá-la manualmente para cada caixa de correio de usuário em sua organização. 

As ações de caixa de correio registradas por padrão incluem as ações de caixa de correio SoftDelete e HardDelete executadas por proprietários de caixa de correio. Isso significa que você pode usar as seguintes etapas para pesquisar o log de auditoria em busca de eventos relacionados a itens de email excluídos. Para obter mais informações sobre a auditoria de caixa de correio por padrão, consulte [Manage Mailbox Auditing](enable-mailbox-auditing.md).

ConFira aqui como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** – em **atividades de caixa de correio do Exchange**, selecione uma ou ambas as atividades a seguir:

- **Mensagens excluídas da pasta itens excluídos** -esta atividade corresponde à ação de auditoria de caixa de correio do **SoftDelete** . Essa atividade também é registrada quando um usuário exclui permanentemente um item selecionando-o e pressionando **Shift + Delete**. Depois que um item é excluído permanentemente, o usuário pode recuperá-lo até que expire o período de retenção do item excluído.

- **Mensagens limpas da caixa de correio** -esta atividade corresponde à ação de auditoria de caixa de correio do **HardDelete** . Isso é registrado quando um usuário limpa um item da pasta itens recuperáveis. Os administradores podem usar a ferramenta de pesquisa de conteúdo no centro de segurança e conformidade para pesquisar e recuperar itens excluídos até que o período de retenção do item excluído expire ou maior se a caixa de correio do usuário estiver em espera.

**Data de início** e **data de término** -selecione um intervalo de datas que se aplica à sua investigação.

**Usuários** – se você selecionar um usuário neste campo, a ferramenta de pesquisa de log de auditoria retornará registros de auditoria para itens de email que foram excluídos (SoftDeleted ou HardDeleted) pelo usuário especificado. Em alguns casos, o usuário que exclui um email pode não ser o proprietário da caixa de correio.

**Arquivo, pasta ou site** -deixe este campo em branco.

Depois de executar a pesquisa, você pode filtrar os resultados da pesquisa para exibir os registros de auditoria para itens excluídos por software ou para itens excluídos. Clique no registro de auditoria para exibir a página do submenu **detalhes** e, em seguida, clique em **mais informações**. Informações adicionais sobre o item excluído, como a linha de assunto e o local do item quando ele foi excluído, são exibidas no campo **AffectedItems** . As capturas de tela a seguir mostram um exemplo do campo **AffectedItems** de um item excluído de forma reversível e de um item excluído.

**Exemplo de campo AffectedItems para item excluído por software**

![Registro de auditoria para item excluído por software](media/softdeleteditem.png)

**Exemplo de campo AffectedItems para item excluído por hardware**

![Registro de auditoria para item de email excluído por hardware](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Recuperando itens de email excluídos

Os usuários podem recuperar itens excluídos de forma reversível se o período de retenção de itens excluídos não tiver expirado. No Exchange Online, o período de retenção de itens excluídos padrão é de 14 dias, mas os administradores podem aumentar essa configuração para um máximo de 30 dias. Aponte os usuários para o artigo [recuperar itens ou emails excluídos no Outlook na Web](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) para obter instruções sobre como recuperar itens excluídos.

Conforme explicado anteriormente, os administradores podem ser capazes de recuperar os itens excluídos de forma fixa se o período de retenção de itens excluídos não tiver expirado ou se a caixa de correio estiver em espera, caso em que os itens são mantidos até que a duração da retenção expire. Quando você executa uma pesquisa de conteúdo, os itens excluídos de forma reversível e excluídos de forma fixa na pasta itens recuperáveis são retornados nos resultados da pesquisa se eles corresponderem à consulta de pesquisa. Para obter mais informações sobre a execução de pesquisas de conteúdo, consulte [pesquisa de conteúdo no Office 365](content-search.md).

> [!TIP]
> Para procurar itens de email excluídos, pesquise toda ou parte da linha de assunto que é exibida no campo **AffectedItems** no registro de auditoria.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Determinando se um usuário criou uma regra de caixa de entrada

Quando os usuários criam uma regra de caixa de entrada para sua caixa de correio do Exchange Online, um registro de auditoria correspondente é salvo no log de auditoria. Para obter mais informações sobre regras de caixa de entrada, consulte:

- [Usar regras de caixa de entrada no Outlook na Web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Gerenciar mensagens de email no Outlook usando regras](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

ConFira aqui como configurar uma consulta de pesquisa de log de auditoria para este cenário:

**Atividades** – em **atividades de caixa de correio do Exchange**, selecione **novo-InboxRule criar/modificar/habilitar/desabilitar regra de caixa de entrada**.

**Data de início** e **data de término** -selecione um intervalo de datas que se aplica à sua investigação.

**Usuários** – a menos que você esteja investigando um usuário específico, deixe este campo em branco. Isso ajudará a identificar novas regras de caixa de entrada configuradas por qualquer usuário.

**Arquivo, pasta ou site** -deixe este campo em branco.

Depois de executar a pesquisa, todos os registros de auditoria dessa atividade serão exibidos nos resultados da pesquisa. Clique em um registro de auditoria para exibir a página do submenu **detalhes** e, em seguida, clique em **mais informações**. As informações sobre as configurações da regra de caixa de entrada são exibidas no campo **parâmetros** . A captura de tela e as descrições a seguir destacam as informações sobre regras de caixa de entrada.

![Registro de auditoria para nova regra de caixa de entrada](media/NewInboxRuleRecord.png)

a. No campo **ObjectID** , o nome completo da regra de caixa de entrada é exibido. Esse nome inclui o alias da caixa de correio do usuário (por exemplo, em inglês) e o nome da regra de caixa de entrada (por exemplo, "mover mensagens do administrador").

b. No campo **parâmetros** , a condição da regra de caixa de entrada é exibida. Neste exemplo, a condição é especificada pelo parâmetro *from* . O valor definido para o parâmetro from indica que a regra de caixa *de* entrada atua no email enviado por admin@alpinehouse.onmicrosoft.com. Para obter uma lista completa dos parâmetros que podem ser usados para definir condições de regras de caixa de entrada, consulte o artigo [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. O parâmetro *MoveToFolder* especifica a ação para a regra de caixa de entrada; Neste exemplo, as mensagens recebidas de admin@alpinehouse.onmicrosoft.com são movidas para a pasta denominada *AdminSearch*. Consulte também o artigo [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) para obter uma lista completa de parâmetros que podem ser usados para definir a ação de uma regra de caixa de entrada.

d. O campo **userid** indica o usuário que criou a regra de caixa de entrada especificada no campo **ObjectID** . Esse usuário também é exibido na coluna **usuário** na página de resultados da pesquisa.