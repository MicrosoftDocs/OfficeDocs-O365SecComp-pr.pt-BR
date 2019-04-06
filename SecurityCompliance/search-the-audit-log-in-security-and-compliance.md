---
title: Pesquisar o log de auditoria no centro de conformidade do & de segurança
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
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Use o centro de conformidade do & de segurança para pesquisar o log de auditoria unificado para exibir as atividades do usuário e do administrador na sua organização do Office 365. '
ms.openlocfilehash: d593c7d5403f658175850a66a55603dab2b60d42
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479677"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Pesquisar o log de auditoria no centro de conformidade do & de segurança

## <a name="introduction"></a>Introdução

Precisa localizar se um usuário exibir um documento específico ou limpar um item de sua caixa de correio? Em caso afirmativo, você pode usar o centro &amp; de conformidade de segurança do Office 365 para pesquisar o log de auditoria unificada para exibir as atividades do usuário e do administrador na sua organização do Office 365. Por que um log de auditoria unificado? Como é possível pesquisar os seguintes tipos de atividade de usuário e administrador no Office 365:
  
- Atividade do usuário no SharePoint Online e no OneDrive for Business
    
- Atividade do usuário no Exchange Online (log de auditoria de caixa de correio do Exchange)
    
    > [!IMPORTANT]
    > O log de auditoria de caixa de correio deve ser ativado para cada caixa de correio do usuário antes que a atividade do usuário no Exchange Online seja registrada. Para obter mais informações, consulte [habilitar a auditoria de caixa de correio no Office 365](enable-mailbox-auditing.md).
  
- Atividade de administração no SharePoint Online
    
- Atividade de administração no Azure Active Directory (o serviço de diretório para o Office 365)
    
- Atividade de administração no Exchange Online (log de auditoria do administrador do Exchange)
    
- Atividade de usuário e administrador no Sway
    
- atividades de descoberta eletrônica no centro de conformidade e segurança
    
- Atividade de usuário e administrador no Power BI
    
- Atividade de usuário e administrador no Microsoft Teams

- Atividade de usuário e administrador no Dynamics 365
    
- Atividade de usuário e administrador no Yammer
 
- Atividade de usuário e administrador no Microsoft Flow
    
- Atividade de usuário e administrador no Microsoft Stream

- Atividade de Analista e administração no Microsoft Workplace Analytics

- Atividade de usuário e administrador no Microsoft PowerApps
    
   
## <a name="before-you-begin"></a>Antes de começar

Certifique-se de ler os seguintes itens antes de começar a pesquisar o log de auditoria do Office 365.
  
- Você (ou outro administrador) deve primeiro ativar o registro em log de auditoria antes de começar a pesquisar o log de auditoria do Office 365. Para ativá-la, basta clicar em **iniciar a gravação da atividade de administrador e usuário** na página pesquisa de log de **auditoria** no centro de conformidade do & de segurança. (Se você não vir este link, a auditoria já foi ativada para sua organização.) Depois que você ativá-la, será exibida uma mensagem dizendo que o log de auditoria está sendo preparado e que você pode executar uma pesquisa em algumas horas após a conclusão da preparação. Você só precisa fazer isso uma vez. 
    
    > [!NOTE]
    > Estamos no processo de ativar a auditoria por padrão. Até então, você pode ativá-lo conforme descrito anteriormente. 
  
- Você precisa receber a função de logs de auditoria somente para exibição ou logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de função gerenciamento de conformidade e gerenciamento da organização na página **permissões** no centro de administração do Exchange. Observe que os administradores globais no Office 365 e Microsoft 365 são automaticamente adicionados como membros do grupo de função gerenciamento da organização no Exchange Online. Para conceder ao usuário a capacidade de Pesquisar o log de auditoria do Office 365 com o nível mínimo de privilégios, você pode criar um grupo de função personalizado no Exchange Online, adicionar os logs de auditoria somente para exibição ou a função logs de auditoria e, em seguida, adicionar o usuário como membro do novo grupo de funções. Para obter mais informações, consulte [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Se você atribuir a um usuário a função logs de auditoria somente para exibição ou logs de auditoria na página **permissões** no centro de conformidade do _AMP_ de segurança, elas não poderão pesquisar o log de auditoria do Office 365. Você precisa atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online. 
  
- Quando uma atividade auditada é executada por um usuário ou administrador, um registro de auditoria é gerado e armazenado no log de auditoria do Office 365 para sua organização. O período de tempo que um registro de auditoria é mantido (e pesquisável no log de auditoria) depende da sua assinatura do Office 365 e, especificamente, do tipo da licença atribuída a um usuário específico.

     - **Office 365 E3** -os registros de auditoria são mantidos por 90 dias. Isso significa que você pode pesquisar o log de auditoria para atividades realizadas nos últimos 90 dias.

     - **Office 365 E5** -os registros de auditoria são mantidos por 365 dias (um ano). Isso significa que você pode pesquisar o log de auditoria para atividades realizadas no último ano. A retenção de registros de auditoria por um ano também está disponível para usuários que recebem uma licença E3/Exchange Online Plan 1 e que têm uma licença complementar de conformidade avançada do Office 365.

        > [!NOTE]
        > O período de retenção de um ano para registros de auditoria para organizações E5 (ou organizações E3 que possuem licenças de complemento de conformidade avançada) atualmente está disponível apenas como parte de um programa de visualização privado. Para se inscrever neste programa de visualização, registre uma solicitação com o [suporte da Microsoft](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) e inclua o seguinte como a descrição do que você precisa ajuda com: "visualização privada do log de auditoria do Office 365 de longo prazo".

- Se quiser desativar a pesquisa de log de auditoria no Office 365 para sua organização, você pode executar o seguinte comando no PowerShell remoto conectado à sua organização do Exchange Online:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Para ativar a pesquisa de auditoria novamente, você pode executar o seguinte comando no PowerShell do Exchange Online:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Para obter mais informações, consulte desativar [pesquisa de log de auditoria no Office 365](turn-audit-log-search-on-or-off.md).
    
- Conforme mencionado anteriormente, o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online, que é o **UnifiedAuditLog de pesquisa**. Isso significa que você pode usar esse cmdlet para pesquisar o log de auditoria do Office 365 em vez de usar a página **pesquisa de log de auditoria** no centro de conformidade do _AMP_ de segurança. Você precisa executar esse cmdlet no PowerShell remoto conectado à sua organização do Exchange Online. Para obter mais informações, consulte [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Se você deseja baixar dados programaticamente do log de auditoria do Office 365, recomendamos usar a API da atividade de gerenciamento do Office 365 em vez de usar um script do PowerShell. A API de atividade de gerenciamento do Office 365 é um serviço Web REST que você pode usar para desenvolver operações, segurança e soluções de monitoramento de conformidade para sua organização. Para obter mais informações, consulte [referência da API de atividade de gerenciamento do Office 365](https://go.microsoft.com/fwlink/?linkid=852309).
    
- Pode levar até 30 minutos ou até 24 horas após a ocorrência de um evento para que a entrada do log de auditoria correspondente seja exibida nos resultados da pesquisa. A tabela a seguir mostra o tempo que leva para os diferentes serviços no Office 365.
    
    |**Serviço do Office 365**|**30 minutos**|**24 horas**|
    |:-----|:-----|:-----|
    |Proteção avançada contra ameaças e inteligência contra ameaças  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (eventos de logon do usuário)  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (eventos de administração)  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |Prevenção contra perda de dados  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
    |Dynamics 365 CRM <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Descoberta eletrônica  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Forms  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Teams  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Centro de Conformidade e Segurança  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |SharePoint Online e OneDrive for Business  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- O Azure Active Directory (Azure AD) é o serviço de diretório para o Office 365. O log de auditoria unificada contém atividades de usuário, grupo, aplicativo, domínio e diretório realizadas no centro de administração do Microsoft 365 ou no portal de gerenciamento do Azure. Para obter uma lista completa de eventos do Azure AD, confira [eventos do Azure Active Directory Audit Report](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Os logs de auditoria do Exchange Online consistem em dois tipos de eventos: eventos de administração do Exchange (ações tomadas por administradores) e eventos de caixa de correio (ações tomadas por usuários em caixas de correio). Observe que a auditoria de caixa de correio não é habilitada por padrão. Ele deve ser habilitado para cada caixa de correio do usuário antes que os eventos de caixa de correio possam ser pesquisados no log de auditoria do Office 365. Para obter mais informações sobre auditoria de caixa de correio e as ações de auditoria de caixa de correio registradas, consulte [habilitar auditoria de caixa de correio no Office 365](enable-mailbox-auditing.md).
    
- O log de auditoria do Power BI não está habilitado por padrão. Para pesquisar atividades do Power BI no log de auditoria do Office 365, você precisa habilitar a auditoria no portal de administração do Power BI. Para obter instruções, consulte a seção "logs de auditoria" no [portal de administração do Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
    
    
## <a name="search-the-audit-log"></a>Pesquisar o log de auditoria

Este é o processo de pesquisa do log de auditoria no Office 365.
  
[Etapa 1: executar uma pesquisa de log de auditoria](#step-1-run-an-audit-log-search)
  
[Etapa 2: exibir os resultados da pesquisa](#step-2-view-the-search-results)

[Etapa 3: filtrar os resultados da pesquisa](#step-3-filter-the-search-results)

[Etapa 4: exportar os resultados da pesquisa para um arquivo](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Etapa 1: executar uma pesquisa de log de auditoria

1. Acesse [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
    > [!TIP]
    > Use uma sessão de navegação privada (não uma sessão normal) para acessar o centro de conformidade do & de segurança, pois isso impedirá que a credencial com a qual você está conectado no momento seja usada. Para abrir uma sessão de navegação InPrivate no Internet Explorer ou no Microsoft Edge, basta pressionar CTRL + SHIFT + P. Para abrir uma sessão de navegação privada no Google Chrome (chamado de janela incógnito), pressione CTRL + SHIFT + N. 
  
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel esquerdo do centro de conformidade do & de segurança, clique em **Pesquisar**e clique em **pesquisa de log de auditoria**.
    
    A página **pesquisa de log de auditoria** é exibida. 
    
    ![Configurar critérios e clicar em Pesquisar para executar o relatório](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Primeiro você precisa ativar o log de auditoria antes de executar uma pesquisa de log de auditoria. Se o link **Iniciar gravação de usuário e atividade de administrador** for exibido, clique nele para ativar a auditoria. Se você não vir este link, a auditoria já foi ativada para sua organização. 
  
4. Configure os seguintes critérios de pesquisa:
    
    a. **Atividades** do Clique na lista suspensa para exibir as atividades que você pode pesquisar. As atividades do usuário e do administrador são organizadas em grupos de atividades relacionadas. Você pode selecionar atividades específicas ou pode clicar no nome do grupo de atividades para selecionar todas as atividades no grupo. Você também pode clicar em uma atividade selecionada para desmarcar a seleção. Depois de executar a pesquisa, somente as entradas de log de auditoria das atividades selecionadas são exibidas. Selecionar **Mostrar resultados de todas as atividades** exibirá os resultados de todas as atividades realizadas pelo usuário ou grupo de usuários selecionado. 
    
    Mais de 100 as atividades de usuário e de administrador são registradas no log de auditoria do Office 365. Clique na guia **atividades auditadas** no tópico deste artigo para ver as descrições de cada atividade em cada um dos diferentes serviços do Office 365. 
    
    b. **Data de início** e **data de término** os últimos sete dias são selecionados por padrão. Selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. A data e a hora são apresentadas no formato UTC (tempo Universal Coordenado). O intervalo de datas máximo que você pode especificar é de 90 dias. Um erro será exibido se o intervalo de datas selecionado for maior que 90 dias. 
    
    > [!TIP]
    > Se você estiver usando o intervalo de datas máximo de 90 dias, selecione a hora atual para a **data de início**. Caso contrário, você receberá um erro dizendo que a data de início é anterior à data de término. Se você ativou a auditoria nos últimos 90 dias, o intervalo de datas máximo não pode ser iniciado antes da data em que a auditoria foi ativada. 
  
    c. **Usuários** do Clique nesta caixa e selecione um ou mais usuários para exibir os resultados da pesquisa. As entradas de log de auditoria para a atividade selecionada executada pelos usuários selecionados nesta caixa são exibidas na lista de resultados. Deixe esta caixa em branco para retornar entradas para todos os usuários (e contas de serviço) em sua organização. 
    
    d. **Arquivo, pasta ou site** Digite alguns ou todos os nomes de arquivo ou pasta para pesquisar atividade relacionada ao arquivo de pasta que contém a palavra-chave especificada. Você também pode especificar uma URL de um arquivo ou pasta. Se você usar uma URL, certifique-se de digitar o caminho de URL completo ou se digitar apenas uma parte da URL, não inclua nenhum caractere ou espaço especial. 
    
    Deixe esta caixa em branco para retornar entradas para todos os arquivos e pastas em sua organização.
    
    > [!TIP]
    > Se você estiver procurando todas as atividades relacionadas a um **site**, adicione o símbolo curinga (\*) após a URL para retornar todas as entradas desse site; por exemplo, **"https://contoso-my.sharepoint.com/personal/*"**.
    
5. Clique em **Pesquisar** para executar a pesquisa usando seus critérios de pesquisa. 
    
    Os resultados da pesquisa são carregados e após alguns momentos em que são exibidos em **resultados**. Quando a pesquisa é concluída, o número de resultados encontrados é exibido. Observe que um máximo de 5.000 eventos será exibido no painel de **resultados** em incrementos de 150 eventos; se mais de 5.000 eventos atenderem aos critérios de pesquisa, os eventos 5.000 mais recentes serão exibidos. 
    
    ![O número de resultados é exibido após a conclusão da pesquisa](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Dicas para pesquisar o log de auditoria

- Você pode selecionar atividades específicas para pesquisa clicando no nome da atividade. Ou você pode pesquisar todas as atividades em um grupo (como **atividades de arquivo e pasta**) clicando no nome do grupo. Se uma atividade for selecionada, você poderá clicar nela para cancelar a seleção. Você também pode usar a caixa de pesquisa para exibir as atividades que contêm a palavra-chave que você digita.
    
    ![Clique em nome do grupo de atividades para selecionar todas as atividades](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Você precisa selecionar **Mostrar resultados de todas as atividades** na lista de **atividades** para exibir eventos do log de auditoria do administrador do Exchange. Eventos desse log de auditoria exibem um nome de cmdlet (por exemplo, **Set-Mailbox** ) na coluna **atividade** nos resultados. Para obter mais informações, clique na guia **atividades auditadas** neste tópico e, em seguida, clique em **atividades de administração do Exchange**.
    
    Da mesma forma, há algumas atividades de auditoria que não têm um item correspondente na lista de **atividades** . Se você souber o nome da operação para essas atividades, poderá pesquisar todas as atividades e, em seguida, filtrar os resultados digitando o nome da operação na caixa da coluna **atividade** . Consulte [etapa 3: filtrar os resultados da pesquisa](#step-3-filter-the-search-results) para obter mais informações sobre a filtragem dos resultados. 
    
- Clique em **limpar** para limpar os critérios de pesquisa atuais. O intervalo de datas retorna para o padrão dos últimos sete dias. Você também pode clicar em **limpar tudo para mostrar os resultados de todas as atividades** para cancelar todas as atividades selecionadas. 
    
- Se forem encontrados resultados 5.000, provavelmente você poderá supor que há mais de 5.000 eventos que atingiram os critérios de pesquisa. Você pode refinar os critérios de pesquisa e executar novamente a pesquisa para retornar menos resultados, ou pode exportar todos os resultados da pesquisa, selecionando **Exportar resultados** \> **baixar todos os resultados**.

  
### <a name="step-2-view-the-search-results"></a>Etapa 2: exibir os resultados da pesquisa

Os resultados de uma pesquisa de log de auditoria são exibidos em **resultados** na página **pesquisa de log de auditoria** . Como mencionado anteriormente, um máximo de 5.000 (mais recentes) eventos é exibido em incrementos de 150 eventos. Para exibir mais eventos, você pode usar a barra de rolagem no painel de **resultados** ou pode pressionar **Shift + End** para exibir os próximos 150 eventos. 
  
Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa.
  
- **Data:** A data e a hora (no formato UTC) quando o evento ocorreu. 
    
- **Endereço IP:** O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido em um formato de endereço IPv4 ou IPv6. 
    
- **Usuário:** O usuário (ou conta de serviço) que executou a ação que disparou o evento. 
    
- **Atividade:** A atividade realizada pelo usuário. Esse valor corresponde às atividades que você selecionou na lista suspensa **atividades** . Para um evento do log de auditoria do administrador do Exchange, o valor desta coluna é um cmdlet do Exchange. 
    
- **Item:** O objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta de usuário que foi atualizada. Nem todas as atividades têm um valor nesta coluna. 
    
- **Detalhe:** Detalhes adicionais sobre uma atividade. Novamente, nem todas as atividades terão um valor. 
    
> [!TIP]
> Clique em um cabeçalho de coluna em **resultados** para classificar os resultados. Você pode classificar os resultados de a a Z ou Z para A. Clique no cabeçalho de **Data** para classificar os resultados do mais antigo para o mais recente ou mais recente. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Exibir os detalhes de um evento específico

Você pode visualizar mais detalhes sobre um evento clicando no registro do evento na lista de resultados da pesquisa. Uma página de **detalhes** é exibida contendo as propriedades detalhadas do registro de eventos. As propriedades exibidas dependem do serviço do Office 365 em que o evento ocorre. Para exibir esses detalhes, clique em **mais informações**. Para obter descrições, consulte [propriedades detalhadas no log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
![Clique em mais informações para exibir as propriedades detalhadas do registro de eventos do log de auditoria](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Etapa 3: filtrar os resultados da pesquisa

Além da classificação, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Este é um ótimo recurso que pode ajudá-lo a filtrar rapidamente os resultados de um usuário ou atividade específico. Você pode criar inicialmente uma ampla pesquisa e, em seguida, filtrar rapidamente os resultados para ver eventos específicos. Em seguida, você pode restringir os critérios de pesquisa e executar novamente a pesquisa para retornar um conjunto menor e mais conciso de resultados.
  
Para filtrar os resultados:
  
1. Execute uma pesquisa de log de auditoria.
    
2. Quando os resultados forem exibidos, clique em **filtrar resultados**.
    
    As caixas de palavras-chave são exibidas sob cada cabeçalho de coluna.
    
3. Clique em uma das caixas sob um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna que você está filtrando. Os resultados serão reajustados dinamicamente para exibir os eventos que correspondam ao seu filtro.
    
    ![Digite uma palavra no filtro para exibir eventos que correspondam ao filtro](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Para limpar um filtro, clique no **X** na caixa filtro ou clique em **ocultar filtragem**.
    
> [!TIP]
> Para exibir eventos do log de auditoria do administrador do Exchange, **-** digite a (travessão) na caixa filtro de **atividade** . Isso exibirá os nomes de cmdlet, que são exibidos na coluna **atividade** dos eventos de administração do Exchange. Em seguida, você pode classificar os nomes de cmdlets em ordem alfabética. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Etapa 4: exportar os resultados da pesquisa para um arquivo

Você pode exportar os resultados de uma pesquisa de log de auditoria para um arquivo CSV (valor separado por vírgula) no computador local. Você pode abrir esse arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e divisão de uma única coluna (que contém células de vários valores) em várias colunas.
  
1. Execute uma pesquisa de log de auditoria e revise os critérios de pesquisa até que você tenha os resultados desejados.
    
2. Clique em **Exportar resultados** e selecione uma das seguintes opções: 
    
  - **Salvar resultados carregados** Escolha essa opção para exportar apenas as entradas que são exibidas em **resultados** na página * * pesquisa de log de auditoria * *. O arquivo CSV baixado contém as mesmas colunas (e dados) exibidas na página (data, usuário, atividade, item e detalhes). Uma coluna adicional (chamada **mais**) é incluída no arquivo CSV que contém mais informações da entrada do log de auditoria. Como você está exportando os mesmos resultados que são carregados (e exibíveis) na página **pesquisa de log de auditoria** , um máximo de 5.000 entradas são exportadas. 
    
  - **Baixar todos os resultados** Escolha essa opção para exportar todas as entradas do log de auditoria do Office 365 que atendam aos critérios de pesquisa. Para obter um grande conjunto de resultados de pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além dos resultados 5.000 que podem ser exibidos na página **pesquisa de log de auditoria** . Essa opção baixará os dados brutos do log de auditoria para um arquivo CSV e conterá informações adicionais da entrada do log de auditoria em uma coluna chamada **AuditData**. Pode levar mais tempo para baixar o arquivo se você escolher essa opção de exportação porque o arquivo pode ser muito maior do que o baixado, se você escolher a outra opção.
    
    > [!IMPORTANT]
    > Você pode baixar um máximo de 50.000 entradas para um arquivo CSV de uma única pesquisa de log de auditoria. Se as entradas 50.000 forem baixadas para o arquivo CSV, provavelmente você poderá supor que há mais de 50.000 eventos que atingiram os critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas de log de auditoria. Você pode ter que executar várias pesquisas com intervalos de datas menores para exportar mais de 50.000 entradas. 
  
3. Após selecionar uma opção de exportação, uma mensagem é exibida na parte inferior da janela que solicita que você abra o arquivo CSV, salve-o na pasta downloads ou salve-o em uma pasta específica.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>Mais informações sobre como exportar resultados de pesquisa de log de auditoria

- A opção **baixar todos os resultados** baixa os dados brutos do log de auditoria do Office 365 para um arquivo CSV. Esse arquivo contém nomes de coluna diferentes (CreationDate, UserIds, Operation, AuditData) do que o arquivo baixado se você selecionar a opção **salvar resultados carregados** . Os valores dos dois arquivos CSV diferentes para a mesma atividade também podem ser diferentes. Por exemplo, a atividade na coluna **ação** no arquivo CSV e pode ter um valor diferente da versão "amigável" que é exibida na coluna **atividade** na página **pesquisa de log de auditoria** ; por exemplo, MailboxLogin vs. usuário conectado à caixa de correio.
    
- Se você baixar todos os resultados, o arquivo CSV conterá uma coluna chamada **AuditData**, que contém informações adicionais sobre cada evento. Conforme mencionado anteriormente, esta coluna contém uma propriedade de vários valores para várias propriedades do registro de log de auditoria. Cada um dos pares **Propriedade: valor** nessa propriedade de vários valores é separado por uma vírgula. Você pode usar a consulta de energia no Excel para dividir esta coluna em várias colunas, de forma que cada propriedade tenha sua própria coluna. Isso permitirá que você classifique e filtre em uma ou mais dessas propriedades. Para saber como fazer isso, confira a seção "dividir uma coluna por delimitador" em [dividir uma coluna de texto (consulta de força)](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662).
    
    Após dividir a coluna **AuditData** , você pode filtrar a coluna **operações** para exibir as propriedades detalhadas de um tipo específico de atividade. 
    
- Há um limite de 3.060 caracteres para os dados exibidos no campo **AuditData** para um registro de auditoria. Se o limite de 3.060 caracteres for excedido, os dados nesse campo serão truncados. 
    
- Ao baixar todos os resultados de uma consulta de pesquisa que contenha eventos de diferentes serviços do Office 365, a coluna **AuditData** no arquivo CSV contém propriedades diferentes, dependendo do serviço em que a ação foi executada. Por exemplo, as entradas dos logs de auditoria do Exchange e do Azure AD incluem uma propriedade denominada **ResultStatus** que indica se a ação foi bem-sucedida ou não. Essa propriedade não é incluída para eventos no SharePoint. Da mesma forma, os eventos do SharePoint têm uma propriedade que identifica a URL do site para atividades relacionadas a arquivos e pastas. Para reduzir esse comportamento, considere o uso de pesquisas diferentes para exportar os resultados das atividades de um único serviço. 
    
    Para obter uma descrição das propriedades listadas na coluna **AuditData** no arquivo CSV, quando você baixar todos os resultados e o serviço ao qual cada um se aplica, consulte [propriedades detalhadas no log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Atividades auditadas

As tabelas desta seção descrevem as atividades que são auditadas no Office 365. Você pode pesquisar esses eventos pesquisando o log de auditoria no centro de segurança e conformidade.
  
Essas tabelas agrupam atividades relacionadas ou as atividades de um serviço específico do Office 365. As tabelas incluem o nome amigável que é exibido na lista suspensa **atividades** e o nome da operação correspondente que aparece nas informações detalhadas de um registro de auditoria e no arquivo CSV quando você exporta os resultados da pesquisa. Para obter descrições das informações detalhadas, consulte [propriedades detalhadas no log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
Clique em um dos seguintes links para ir para uma tabela específica.
  
||||
|:-----|:-----|:-----|
|[Atividades de arquivo e página](#file-and-page-activities)<br/> |[Atividades de pasta](#folder-activities)<br/> |[Compartilhamento e acesso às atividades de solicitação](#sharing-and-access-request-activities)<br/> |
|[Atividades de sincronização](#synchronization-activities)<br/> |[Atividades de administração do site](#site-administration-activities)<br/> |[Atividades de caixa de correio do Exchange](#exchange-mailbox-activities)<br/> |
|[Atividades do Sway](#sway-activities) <br/> |[Atividades de administração de usuário](#user-administration-activities) <br/> |[Atividades de administração de grupos do Azure AD](#azure-ad-group-administration-activities) <br/> 
|[Atividades de administração de aplicativos](#application-administration-activities) <br/> |[Atividades de administração de função](#role-administration-activities) <br/> |[Atividades de administração de diretório](#directory-administration-activities) <br/>| 
|[atividades de descoberta eletrônica](#ediscovery-activities) <br/> |[Atividades do Power BI](#power-bi-activities) <br/> |[Análise de local de trabalho da Microsoft](#microsoft-workplace-analytics-activities)<br/>|
|[Atividades do Microsoft Teams](#microsoft-teams-activities) <br/> |[Atividades do Yammer](#yammer-activities) <br/> |[Atividades de fluxo da Microsoft](#microsoft-flow-activities) <br/>|
|[Atividades do Microsoft PowerApps](#microsoft-powerapps)<br/>|[Atividades do Microsoft Stream](#microsoft-stream-activities) <br/>|[Atividades de administração do Exchange](#exchange-admin-audit-log)<br/>|
||||
   
  
### <a name="file-and-page-activities"></a>Atividades de arquivo e página
  
A tabela a seguir descreve as atividades de arquivo e de página no SharePoint Online e no OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Arquivo acEssado  <br/> |FileAccessed  <br/> |A conta do usuário ou do sistema acessa um arquivo.  <br/> |
|(nenhum)  <br/> |FileAccessedExtended  <br/> |Isso está relacionado à atividade "arquivo acEssado" (arquivos acessados). Um evento FileAccessedExtended é registrado quando a mesma pessoa acessa continuamente um arquivo por um período de tempo estendido (até 3 horas). O objetivo do registro em log de eventos do FileAccessedExtended é reduzir o número de eventos de arquivo que são registrados quando um arquivo é acessado continuamente. Isso ajuda a reduzir o ruído de vários registros de fileAccess para o que é essencialmente a mesma atividade do usuário e permite que você se concentre no evento inicial (e mais importante) fileAccessed.  <br/> |
|Arquivo com check-in  <br/> |FileCheckem  <br/> |O usuário faz o check-in de um documento que fez check-out de uma biblioteca de documentos.  <br/> |
|Arquivo com check-out  <br/> |FileCheckout  <br/> |O usuário faz check-out de um documento localizado em uma biblioteca de documentos. Os usuários podem fazer check-out e alterações nos documentos que foram compartilhados com eles.  <br/> |
|Arquivo copiado  <br/> |FileCopied  <br/> |O usuário copia um documento de um site. O arquivo copiado pode ser salvo em outra pasta no site.  <br/> |
|Arquivo excluído  <br/> |FileDeleted  <br/> |O usuário exclui um documento de um site.  <br/> |
|Arquivo excluído da lixeira  <br/> |FileDeletedFirstStageRecycleBin  <br/> |O usuário exclui um arquivo da lixeira de um site.  <br/> |
|Arquivo excluído da lixeira de segundo estágio  <br/> |FileDeletedSecondStageRecycleBin  <br/> |O usuário exclui um arquivo da lixeira de segundo estágio de um site.  <br/> |
|Detectado malware no arquivo  <br/> |FileMalwareDetected  <br/> |O mecanismo antivírus do SharePoint detecta malware em um arquivo.  <br/> |
|Check-out de arquivo Descartado  <br/> |FileCheckOutDiscarded  <br/> |O usuário descarta (ou desfaz) um arquivo em check-out. Isso significa que todas as alterações que ele tiver feito nesse arquivo durante o estado de check-out serão descartados, e não salvas na versão do documento localizada na biblioteca de documentos.  <br/> |
|Arquivo baixado  <br/> |FileDownloaded  <br/> |O usuário baixa um documento de um site.  <br/> |
|Arquivo modificado  <br/> |FileModified  <br/> |A conta de usuário ou sistema modifica o conteúdo ou as propriedades de um documento localizado em um site.  <br/> |
|(nenhum)  <br/> |FileModifiedExtended  <br/> |Isso está relacionado à atividade "arquivo modificado" (fileModified). Um evento FileModifiedExtended é registrado quando a mesma pessoa modifica continuamente um arquivo por um período de tempo estendido (até 3 horas). O objetivo de registrar eventos do FileModifiedExtended é reduzir o número de eventos fileModified que são registrados quando um arquivo é modificado continuamente. Isso ajuda a reduzir o ruído de vários registros fileModified para o que é essencialmente a mesma atividade do usuário e permite que você se concentre no evento inicial (e mais importante) fileModified.  <br/> |
|Arquivo movido  <br/> |FileMoved  <br/> |O usuário move um documento de seu local atual em um site para um novo local.  <br/> |
|Reciclagem de todas as versões secundárias do arquivo  <br/> |FileVersionsAllMinorsRecycled  <br/> |O usuário exclui todas as versões secundárias do histórico de versões de um arquivo. As versões excluídas são movidas para a lixeira do site.  <br/> |
|Recicla todas as versões do arquivo  <br/> |FileVersionsAllRecycled  <br/> |O usuário exclui todas as versões do histórico de versões de um arquivo. As versões excluídas são movidas para a lixeira do site.  <br/> |
|Versão reciclada do arquivo  <br/> |FileVersionRecycled  <br/> |O usuário exclui uma versão do histórico de versões de um arquivo. A versão excluída é movida para a lixeira do site.  <br/> |
|Arquivo renomeado  <br/> |FileRenamed  <br/> |O usuário renomeia um documento em um site.  <br/> |
|Arquivo restaurado  <br/> |FileRestored  <br/> |O usuário restaura um documento da lixeira de um site.  <br/> |
|Arquivo carregado  <br/> |FileUploaded  <br/> |O usuário carrega um documento em uma pasta de um site.  <br/> |
|Página exibida  <br/> |PageViewed  <br/> |O usuário exibe uma página em um site. Isso não inclui o uso de um navegador da Web para exibir arquivos localizados em uma biblioteca de documentos.  <br/> |
|(nenhum)  <br/> |PageViewedExtended  <br/> |Isso está relacionado à atividade "página exibida" (PageViewed). Um evento PageViewedExtended é registrado quando a mesma pessoa visualiza continuamente uma página da Web por um longo período de tempo (até 3 horas). O objetivo de registrar eventos do PageViewedExtended é reduzir o número de eventos PageViewed que são registrados quando uma página é exibida continuamente. Isso ajuda a reduzir o ruído de vários registros do PageViewed para o que é essencialmente a mesma atividade do usuário e permite que você se concentre no evento inicial (e mais importante) PageViewed.  <br/> |
||||
  
### <a name="folder-activities"></a>Atividades de pasta
  
A tabela a seguir descreve as atividades de pasta no SharePoint Online e no OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Pasta coPiada  <br/> |FolderCopied  <br/> |O usuário copia uma pasta de um site para outro local no SharePoint ou no OneDrive for Business.  <br/> |
|Pasta criada  <br/> |FolderCreated  <br/> |O usuário cria uma pasta em um site.  <br/> |
|Pasta excluída  <br/> |FolderDeleted  <br/> |O usuário exclui uma pasta de um site.  <br/> |
|Pasta excluída da lixeira  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |O usuário exclui uma pasta da lixeira em um site.  <br/> |
|Pasta excluída da lixeira de segundo estágio  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |O usuário exclui uma pasta da lixeira de segundo estágio em um site.  <br/> |
|Pasta modificada  <br/> |FolderModified  <br/> |O usuário modifica uma pasta em um site. Isso inclui a alteração dos metadados da pasta, como a alteração de marcas e propriedades.  <br/> |
|Pasta movida  <br/> |FolderMoved  <br/> |O usuário move uma pasta para um local diferente em um site.  <br/> |
|Pasta renomeada  <br/> |FolderRenamed  <br/> |O usuário renomeia uma pasta em um site.  <br/> |
|Pasta restaurada  <br/> |FolderRestored  <br/> |O usuário restaura uma pasta excluída da lixeira em um site.  <br/> |
||||
  
### <a name="sharing-and-access-request-activities"></a>Compartilhamento e acesso às atividades de solicitação
  
A tabela a seguir descreve as atividades de compartilhamento de usuários e solicitações de acesso no SharePoint Online e no OneDrive for Business. Para eventos de compartilhamento, a coluna de **detalhes** em **resultados** identifica o nome do usuário ou grupo com o qual o item foi compartilhado e se esse usuário ou grupo é membro ou convidado em sua organização. Para obter mais informações, consulte [usar a auditoria de compartilhamento no log de auditoria do Office 365](use-sharing-auditing.md).
  
> [!NOTE]
> Os usuários podem ser *Membros* ou *convidados* com base na propriedade UserType do objeto user. Um membro geralmente é um funcionário, e um convidado geralmente é um colaborador fora da sua organização. Quando um usuário aceita um convite de compartilhamento (e ainda não faz parte da sua organização), uma conta de convidado é criada para eles no diretório da sua organização. Após o usuário convidado ter uma conta no seu diretório, os recursos podem ser compartilhados diretamente com eles (sem exigir um convite). 
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Solicitação de acesso aceito  <br/> |AccessRequestAccepted  <br/> |Uma solicitação de acesso a um site, pasta ou documento foi aceita e o usuário solicitante recebeu acesso.  <br/> |
|Convite de compartilhamento aceito  <br/> |SharingInvitationAccepted  <br/> |O usuário (membro ou convidado) aceitou um convite de compartilhamento e recebeu acesso a um recurso. Esse evento inclui informações sobre o usuário que foi convidado e o endereço de email usado para aceitar o convite (eles podem ser diferentes). Essa atividade geralmente acompanha um segundo evento que descreve como o usuário recebeu acesso ao recurso, por exemplo, adicionar o usuário a um grupo que tem acesso ao recurso.  <br/> |
|Adicionado o nível de permissão para o conjunto de sites  <br/> |PermissionLevelAdded  <br/> |Um nível de permissão foi adicionado a um conjunto de sites.  <br/> |
|Usuário adicionado ao link seguro  <br/> |AddedToSecureLink  <br/> |Um usuário foi adicionado à lista de entidades que podem usar este link de compartilhamento seguro.  <br/> |
|Convite de compartilhamento bloqueado  <br/> |SharingInvitationBlocked  <br/> | Um convite de compartilhamento enviado por um usuário em sua organização é bloqueado por causa de uma política de compartilhamento externa que permite ou impede o compartilhamento externo com base no domínio do usuário de destino. Nesse caso, o convite de compartilhamento foi bloqueado porque:  <br/>  O domínio do usuário de destino não está incluído na lista de domínios permitidos.  <br/>  Ou  <br/>  O domínio do usuário de destino está incluído na lista de domínios bloqueados.  <br/>  Para obter mais informações sobre como permitir ou bloquear o compartilhamento externo com base em domínios, consulte [Restricted Domains Sharing in SharePoint Online e onedrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Herança de nível de permissão de quebrou  <br/> |PermissionLevelsInheritanceBroken  <br/> |Um item foi alterado para que ele não herde mais níveis de permissão de seu pai.  <br/> |
|Herança de compartilhamento de quebrou  <br/> |SharingInheritanceBroken  <br/> |Um item foi alterado para que ele não herde mais as permissões de compartilhamento de seu pai.  <br/> |
|Criou um link compartilhável pela empresa  <br/> |CompanyLinkCreated  <br/> |O usuário criou um link para toda a empresa em um recurso. os links para toda a empresa só podem ser usados por membros em sua organização. Eles não podem ser usados por convidados.  <br/> |
|Solicitação de acesso criada  <br/> |AccessRequestCreated  <br/> |O usuário solicita acesso a um site, pasta ou documento que eles não têm permissões para acessar.  <br/> |
|Criou um link anônimo  <br/> |AnonymousLinkCreated  <br/> |O usuário criou um link anônimo para um recurso. Qualquer pessoa com este link pode acessar o recurso sem precisar ser autenticado.  <br/> |
|Link seguro criado  <br/> |SecureLinkCreated  <br/> |Um link de compartilhamento seguro foi criado para esse item.  <br/> |
|Convite de compartilhamento criado  <br/> |SharingInvitationCreated  <br/> |O usuário compartilhou um recurso no SharePoint Online ou no OneDrive for Business com um usuário que não está no diretório da sua organização.  <br/> |
|Excluído o link seguro  <br/> |SecureLinkDeleted  <br/> |Um link de compartilhamento seguro foi excluído.  <br/> |
|Solicitação de acesso negado  <br/> |AccessRequestDenied  <br/> |Uma solicitação de acesso a um site, pasta ou documento foi negada.  <br/> |
|Nível de permissão modificado no conjunto de sites  <br/> |PermissionLevelModified  <br/> |Um nível de permissão foi alterado em um conjunto de sites.  <br/> |
|Removido um link compartilhável da empresa  <br/> |CompanyLinkRemoved  <br/> |O usuário removeu um link para toda a empresa em um recurso. O link não pode mais ser usado para acessar o recurso.  <br/> |
|Removido um link anônimo  <br/> |AnonymousLinkRemoved  <br/> |O usuário removeu um link anônimo para um recurso. O link não pode mais ser usado para acessar o recurso.  <br/> |
|Nível de permissão removido do conjunto de sites  <br/> |PermissionLevelRemoved  <br/> |Um nível de permissão foi removido de um conjunto de sites.  <br/> |
|Herança de compartilhamento restaurada  <br/> |SharingInheritanceReset  <br/> |Uma alteração foi feita para que um item herde permissões de compartilhamento de seu pai.  <br/> |
|Arquivo, pasta ou site compartilhado  <br/> |SharingSet  <br/> |Usuário (membro ou convidado) compartilhou um arquivo, uma pasta ou um site no SharePoint ou no OneDrive for Business com um usuário no diretório da sua organização. O valor na coluna **detalhes** para esta atividade identifica o nome do usuário com o qual o recurso foi compartilhado e se esse usuário é um membro ou um convidado. Essa atividade geralmente acompanha um segundo evento que descreve como o usuário recebeu acesso ao recurso; por exemplo, adicionar o usuário a um grupo que tenha acesso ao recurso.  <br/> |
|Solicitação de acesso atualizado  <br/> |AccessRequestUpdated  <br/> |Uma solicitação de acesso a um item foi atualizada.  <br/> |
|Atualizou um link anônimo  <br/> |AnonymousLinkUpdated  <br/> |O usuário atualizou um link anônimo para um recurso. O campo atualizado é incluído na propriedade EventData quando você exporta os resultados da pesquisa.  <br/> |
|Convite de compartilhamento atualizado  <br/> |SharingInvitationUpdated  <br/> |Um convite de compartilhamento externo foi atualizado.  <br/> |
|Usou um link anônimo  <br/> |AnonymousLinkUsed  <br/> |Um usuário anônimo acessou um recurso usando um link anônimo. A identidade do usuário pode ser desconhecida, mas você pode obter outros detalhes, como o endereço IP do usuário.  <br/> |
|Arquivo, pasta ou site não compartilhado  <br/> |SharingRevoked  <br/> |Usuário (membro ou convidado) descompartilhou um arquivo, pasta ou site que foi compartilhado anteriormente com outro usuário.  <br/> |
|Usou um link compartilhável pela empresa  <br/> |CompanyLinkUsed  <br/> |O usuário acessou um recurso usando um link para toda a empresa.  <br/> |
|Link de segurança usado  <br/> |SecureLinkUsed  <br/> |Um usuário usou um link seguro.  <br/> |
|Usuário adicionado ao link seguro  <br/> |AddedToSecureLink  <br/> |Um usuário foi adicionado à lista de entidades que podem usar um link de compartilhamento seguro.  <br/> |
|Usuário removido do link seguro  <br/> |RemovedFromSecureLink  <br/> |Um usuário foi removido da lista de entidades que podem usar um link de compartilhamento seguro.  <br/> |
|Convite de compartilhamento do Withdrew  <br/> |SharingInvitationRevoked  <br/> |O usuário Withdrew um convite de compartilhamento para um recurso.  <br/> |
||||
  
### <a name="synchronization-activities"></a>Atividades de sincronização
  
A tabela a seguir lista as atividades de sincronização de arquivo no SharePoint Online e no OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Computador com permissão para sincronizar arquivos  <br/> |ManagedSyncClientAllowed  <br/> |O usuário estabelece com êxito uma relação de sincronização com um site. A relação de sincronização é bem-sucedida porque o computador do usuário é membro de um domínio que foi adicionado à lista de domínios (chamada de lista de *destinatários confiáveis* ) que pode acessar as bibliotecas de documentos em sua organização.  <br/> Para obter mais informações sobre esse recurso, confira [Usar os cmdlets do Windows PowerShell para habilitar a sincronização do OneDrive para domínios que estão na Lista de Destinatários Confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Computador bloqueado de sincronizar arquivos  <br/> |UnmanagedSyncClientBlocked  <br/> |O usuário tenta estabelecer uma relação de sincronização com um site de um computador que não é membro do domínio da sua organização ou é membro de um domínio que não foi adicionado à lista de domínios (chamada de *lista de destinatários confiáveis)* que pode acessar o documento bibliotecas da sua organização. A relação de sincronização não é permitida e o computador do usuário é impedido de sincronizar, fazer download ou fazer upload de arquivos em uma biblioteca de documentos.  <br/> Para obter informações sobre esse recurso, confira [Usar os cmdlets do Windows PowerShell para habilitar a sincronização do OneDrive para domínios que estão na Lista de Destinatários Confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Arquivos baixados para o computador  <br/> |FileSyncDownloadedFull  <br/> |O usuário estabelece uma relação de sincronização e baixa com êxito os arquivos pela primeira vez para o computador a partir de uma biblioteca de documentos.  <br/> |
|Alterações de arquivo baixadas para o computador  <br/> |FileSyncDownloadedPartial  <br/> |O usuário baixa com êxito qualquer alteração nos arquivos de uma biblioteca de documentos. Essa atividade indica que todas as alterações feitas nos arquivos da biblioteca de documentos foram baixadas para o computador do usuário. Somente as alterações foram baixadas porque a biblioteca de documentos foi baixada anteriormente pelo usuário (conforme indicado na atividade **arquivos baixados para o computador** ).  <br/> |
|Arquivos carregados na biblioteca de documentos  <br/> |FileSyncUploadedFull  <br/> |O usuário estabelece uma relação de sincronização e carrega com êxito os arquivos pela primeira vez do seu computador para uma biblioteca de documentos.  <br/> |
|Alterações de arquivo carregadas na biblioteca de documentos  <br/> |FileSyncUploadedPartial  <br/> |O usuário carrega com êxito as alterações nos arquivos de uma biblioteca de documentos. Esse evento indica que quaisquer alterações feitas na versão local de um arquivo de uma biblioteca de documentos foram carregadas com êxito para a biblioteca de documentos. Somente as alterações são descarregadas porque esses arquivos foram carregados anteriormente pelo usuário (conforme indicado na atividade * * carregado arquivos na biblioteca de documentos * *).  <br/> |
||||
  
### <a name="site-administration-activities"></a>Atividades de administração do site
  
A tabela a seguir lista os eventos resultantes das tarefas de administração do site no SharePoint Online.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionado agente de usuário isento  <br/> |ExemptUserAgentSet  <br/> |Um administrador global ou do SharePoint adiciona um agente do usuário à lista de agentes de usuário isentos no centro de administração do SharePoint.  <br/> |
|Adicionou o administrador do conjunto de sites  <br/> |SiteCollectionAdminAdded  <br/> |O administrador do conjunto de sites ou proprietário adiciona uma pessoa como um administrador de conjunto de sites para um site. Os administradores do conjunto de sites têm permissões de controle total para o conjunto de sites e todos os subsites. Essa atividade também é registrada quando um administrador dá acesso a uma conta do OneDrive de um usuário (editando o perfil do usuário no centro de administração do SharePoint ou [usando o centro de administração 365 da Microsoft](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)). <br/> |
|(nenhum)  <br/> |SiteCollectionAdminRemoved <br/> |O administrador do conjunto de sites ou proprietário remove uma pessoa como um administrador de conjunto de sites de um site. Essa atividade também é registrada quando um administrador se remove da lista de administradores de conjunto de sites para a conta do OneDrive de um usuário (editando o perfil do usuário no centro de administração do SharePoint).  Observe que para retornar essa atividade nos resultados de pesquisa do log de auditoria, você precisa pesquisar todas as atividades. <br/> |
|Usuário ou grupo adicionado ao grupo do SharePoint  <br/> |AddedToGroup  <br/> |O usuário adicionou um membro ou convidado a um grupo do SharePoint. Isso pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento de compartilhamento.  <br/> |
|Usuário permitido para criar grupos  <br/> |AllowGroupCreationSet  <br/> |O administrador ou proprietário do site adiciona um nível de permissão a um site que permite que um usuário atribuído essa permissão para criar um grupo para esse site.  <br/> |
|Movimentação geográfica do site canCelada  <br/> |SiteGeoMoveCancelled  <br/> |Um administrador global ou do SharePoint cancela com êxito uma movimentação geográfica de site do SharePoint ou do OneDrive. O recurso multiGeográfico permite que uma organização do Office 365 alcance vários geografias do Office 365 datacenter, que são chamados de GEOS. Para obter mais informações, consulte [recursos de várias geografias no onedrive e no SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Alterou uma política de compartilhamento  <br/> |SharingPolicyChanged  <br/> |Um administrador global ou do SharePoint alterou uma política de compartilhamento do SharePoint usando o portal de administração do Office 365, o portal de administração do SharePoint ou o Shell de gerenciamento do SharePoint Online. Qualquer alteração nas configurações da política de compartilhamento da sua organização será registrada. A política alterada é identificada no campo **ModifiedProperties** nas propriedades detalhadas do registro do evento.  <br/> |
|Política de acesso de dispositivo alterada  <br/> |DeviceAccessPolicyChanged  <br/> |Um administrador global ou do SharePoint alterou a política de dispositivos não gerenciados para sua organização. Esta política controla o acesso ao SharePoint, OneDrive e Office 365 de dispositivos que não estão associados à sua organização. A configuração desta política exige uma assinatura corporativa + segurança. Para obter informações, consulte [Controlar o acesso de dispositivos gerenciados](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).  <br/> |
|Agentes de usuário isentos alterados  <br/> |CustomizeExemptUsers  <br/> |Um administrador global ou do SharePoint personalizou a lista de agentes de usuário isentos no centro de administração do SharePoint. Você pode especificar quais agentes de usuário isentar do recebimento de uma página da Web inteira para indexação. Isso significa que quando um agente de usuário especificado como isento encontra um formulário do InfoPath, o formulário será retornado como um arquivo XML, em vez de uma página da Web inteira. Isso torna a indexação de formulários do InfoPath mais rápida.  <br/> |
|Política de acesso à rede alterada  <br/> |NetworkAccessPolicyChanged  <br/> |Um administrador global ou do SharePoint alterou a política de acesso baseado em local (também chamada de limite de rede confiável) no centro de administração do SharePoint ou usando o SharePoint Online PowerShell. Esse tipo de política controla quem pode acessar os recursos do SharePoint e do OneDrive em sua organização com base em intervalos de endereços IP autorizados que você especificar. Para obter mais informações, consulte [controlar o acesso aos dados do SharePoint Online e do onedrive baseados no local de rede](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).  <br/> |
|Movimentação geográfica de site concluída  <br/> |SiteGeoMoveCompleted  <br/> |Uma movimentação geográfica de site que foi agendada por um administrador global em sua organização foi concluída com êxito. O recurso multiGeográfico permite que uma organização do Office 365 alcance vários geografias do Office 365 datacenter, que são chamados de GEOS. Para obter mais informações, consulte [recursos de várias geografias no onedrive e no SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Grupo criado  <br/> |GroupAdded  <br/> |O administrador ou proprietário do site cria um grupo para um site ou realiza uma tarefa que resulta em um grupo sendo criado. Por exemplo, na primeira vez que um usuário cria um link para compartilhar um arquivo, um grupo de sistemas é adicionado ao site do OneDrive for Business do usuário. Esse evento também pode ser o resultado de um usuário ter criado um link com permissões de edição para um arquivo compartilhado.  <br/> |
|Criado enviado para conexão  <br/> |SendToConnectionAdded  <br/> |Um administrador global ou do SharePoint cria uma nova conexão enviar para na página Gerenciamento de registros no centro de administração do SharePoint. Uma conexão Enviar para especifica configurações para um repositório de documentos ou um centro de registros. Quando você cria uma conexão Enviar para, um Organizador de Conteúdo pode enviar documentos para o local especificado.  <br/> |
|Conjunto de sites criado  <br/> |SiteCollectionCreated  <br/> |Um administrador global ou do SharePoint cria um novo conjunto de sites em sua organização do SharePoint Online ou um usuário provisiona o site do OneDrive for Business.  <br/> |
|Grupo excluído  <br/> |GroupRemoved  <br/> |O usuário exclui um grupo de um site.  <br/> |
|Excluído enviado para conexão  <br/> |SendToConnectionRemoved  <br/> |Um SharePoint ou administrador global exclui uma conexão enviar para na página Gerenciamento de registros no centro de administração do SharePoint.  <br/> |
|Site excluído  <br/> |SiteDeleted  <br/> |O administrador do site exclui um site.  <br/> |
|Visualização de documento habilitada  <br/> |PreviewModeEnabledSet  <br/> |O administrador do site habilita a visualização do documento para um site.  <br/> |
|Fluxo de trabalho herdado habilitado  <br/> |LegacyWorkflowEnabledSet  <br/> |O administrador ou proprietário do site adiciona o tipo de conteúdo Tarefa de fluxo de trabalho do SharePoint 2013 ao site. Os administradores globais também podem ativar fluxos de trabalho para toda a organização no Centro de Administração do SharePoint.  <br/> |
|Ativado o Office on Demand  <br/> |OfficeOnDemandSet  <br/> |O administrador do site habilita o Office on Demand, que permite aos usuários acessar a versão mais recente dos aplicativos da área de trabalho do Office. O Office on Demand está habilitado no Centro de administração do SharePoint e exige uma assinatura do Office 365 que inclua aplicativos completos do Office instalados.  <br/> |
|RSS feeds habilitados  <br/> |NewsFeedEnabledSet  <br/> |O administrador ou proprietário do site permite RSS feeds para um site. Os administradores globais podem ativar feeds RSS para toda a organização no Centro de administração do SharePoint.  <br/> |
|Configuração de solicitação de acesso modificada  <br/> |WebRequestAccessModified  <br/> |As configurações de solicitação de acesso foram modificadas em um site.  <br/> |
|Membros modificados podem compartilhar configuração  <br/> |WebMembersCanShareModified  <br/> |A configuração **Membros podem compartilhar** foi modificada em um site.  <br/> |
|Permissões de site modificadas  <br/> |SitePermissionsModified  <br/> |O administrador do site ou proprietário (ou conta do sistema) altera o nível de permissão atribuído a um grupo em um site. Essa atividade também será registrada se todas as permissões forem removidas de um grupo.  <br/> > [!NOTE]> essa operação foi preterida no SharePoint Online. Para localizar eventos relacionados, você pode pesquisar outras atividades relacionadas à permissão, como o **administrador do conjunto de sites adicionado**, **adicionado usuário ou grupo ao grupo do SharePoint**, **usuário permitido para criar grupos**, **grupo criado**e **excluído grupo.**         |
|Usuário ou grupo removido do grupo do SharePoint  <br/> |RemovedFromGroup  <br/> |O usuário removeu um membro ou convidado de um grupo do SharePoint. Isso pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento de descompartilhamento.  <br/> |
|Site renomeado  <br/> |SiteRenamed  <br/> |O administrador ou proprietário do site renomeia um site  <br/> |
|Permissões de administrador de site solicitadas  <br/> |SiteAdminChangeRequest  <br/> |As solicitações de usuário a serem adicionadas como um administrador de conjunto de sites para um conjunto de sites. Os administradores do conjunto de sites têm permissões de controle total para o conjunto de sites e todos os subsites.  <br/> |
|Movimentação geográfica do site agendado  <br/> |SiteGeoMoveScheduled  <br/> |Um administrador global ou do SharePoint agenda uma movimentação geográfica de site do SharePoint ou do OneDrive. O recurso multiGeográfico permite que uma organização do Office 365 alcance vários geografias do Office 365 datacenter, que são chamados de GEOS. Para obter mais informações, consulte [recursos de várias geografias no onedrive e no SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Definir site do host  <br/> |HostSiteSet  <br/> |Um administrador global ou do SharePoint altera o site designado para hospedar sites pessoais ou do OneDrive for Business.  <br/> |
|Grupo atualizado  <br/> |GroupUpdated  <br/> |O administrador ou proprietário do site altera as configurações de um grupo para um site. Isso pode incluir a alteração do nome do grupo, quem pode visualizar ou editar a associação ao grupo e como as solicitações de associação são tratadas.  <br/> |
||||
  
### <a name="exchange-mailbox-activities"></a>Atividades de caixa de correio do Exchange
  
A tabela a seguir lista as atividades que podem ser registradas pelo log de auditoria de caixa de correio. As atividades de caixa de correio realizadas pelo proprietário da caixa de correio, um usuário delegado ou um administrador são registrados em log. Por padrão, a auditoria de caixa de correio no Office 365 não está ativada. O log de auditoria de caixa de correio deve ser ativado para cada caixa de correio antes que a atividade da caixa de correio seja registrada Para obter mais informações, consulte [habilitar a auditoria de caixa de correio no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionadas permissões de caixa de correio delegada  <br/> |Add-MailboxPermission  <br/> |Um administrador atribuiu a permissão de caixa de correio FullAccess a um usuário (conhecido como um representante) à caixa de correio de outra pessoa. A permissão FullAccess permite que o representante Abra a caixa de correio da outra pessoa e leia e gerencie o conteúdo da caixa de correio.  <br/> |
|Mensagem classificada como registro  <br/> |ApplyRecordLabel<br/> |Uma mensagem foi classificada como um registro. Isso ocorre quando um rótulo de retenção que classifica o conteúdo como um registro é aplicado manualmente ou automaticamente a uma mensagem.<br/> |
|Mensagens coPiadas para outra pasta  <br/> |Copiar  <br/> |Uma mensagem foi copiada a outra pasta.  <br/> |
|Item de caixa de correio criado  <br/> |Criar  <br/> |Um item é criado nas pastas Calendário, Contatos, Anotações ou Tarefas na caixa de correio; por exemplo, é criada uma nova solicitação de reunião. Observe que a criação, o envio ou o recebimento de uma mensagem não é auditado. Além disso, criar uma pasta de caixa de correio não é auditada.  <br/> |
|Nova regra de caixa de entrada criada no Outlook Web App  <br/> |NewInboxRule<br/> |<br/> |
|Mensagens excluídas da pasta itens excluídos  <br/> |SoftDelete  <br/> |Uma mensagem foi excluída permanentemente da pasta Itens Excluídos. Esses itens são movidos para a pasta itens recuperáveis. As mensagens também são movidas para a pasta itens recuperáveis quando um usuário seleciona e pressiona **Shift + Delete**.  <br/> |
|Mensagens moVidas para outra pasta  <br/> |Mover  <br/> |Uma mensagem foi movida para outra pasta.  <br/> |
|Mensagens moVidas para a pasta itens excluídos  <br/> |MoveToDeletedItems  <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |
|Permissão de pasta modificada  <br/> |UpdateFolderPermissions  <br/> |Uma permissão de pasta foi alterada. As permissões de pasta controlam quais usuários em sua organização podem acessar pastas de caixa de correio e as mensagens na pasta.  <br/> |
|Mensagens limpas da caixa de correio  <br/> |HardDelete  <br/> |Uma mensagem foi removida da pasta itens recuperáveis (excluídos permanentemente da caixa de correio).  <br/> |
|Removidos permissões de caixa de correio delegada  <br/> |Remove-MailboxPermission  <br/> |Um administrador removeu a permissão FullAccess (que foi atribuída a um representante) da caixa de correio de uma pessoa. Depois que a permissão FullAccess for removida, o representante não poderá abrir a caixa de correio da outra pessoa nem acessar qualquer conteúdo.  <br/> |
|Mensagem enviada usando permissões Enviar como  <br/> |SendAs  <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |
|Mensagem enviada usando permissões Enviar em nome de  <br/> |SendOnBehalf  <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |
|Acesso de representante atualizado à pasta calendário  <br/> |UpdateCalendarDelegation  <br/> |Uma delegação de calendário foi atribuída a uma caixa de correio. A delegação de calendário oferece a outra pessoa na mesma organização permissões para gerenciar o calendário do proprietário da caixa de correio.  <br/> |
|Mensagem atualizada  <br/> |Atualizar  <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |
|Usuário conectado à caixa de correio  <br/> |MailboxLogin  <br/> |O usuário entrou em sua caixa de correio.  <br/> |
|(nenhum)  <br/> |UpdateInboxRules  <br/> |Uma regra de caixa de entrada foi adicionada, removida ou alterada. As regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e realizar ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou excluir uma mensagem.  <br/> Para retornar entradas para atividades de regra de caixa de entrada, você precisa selecionar **Mostrar resultados de todas as atividades** na lista de **atividades** . Use as caixas intervalo de datas e lista de **usuários** para restringir os resultados da pesquisa.  <br/> |
||||

### <a name="sway-activities"></a>Atividades do Sway
  
A tabela a seguir lista as atividades de usuário e administrador no Sway. O Sway é um aplicativo do Office 365 que ajuda os usuários a reunir, Formatar e compartilhar ideias, histórias e apresentações em uma tela interativa baseada na Web. Para obter mais informações, consulte [perguntas frequentes sobre o Sway-ajuda do administrador](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Nível de compartilhamento do Sway alterado  <br/> |SwayChangeShareLevel  <br/> |O usuário altera o nível de compartilhamento de um Sway. Esse evento captura o usuário alterando o escopo de compartilhamento associado a um Sway; por exemplo, público versus dentro da organização.  <br/> |
|Sway criado  <br/> |SwayCreate  <br/> |O usuário cria um Sway.  <br/> |
|Sway excluído  <br/> |SwayDelete  <br/> |O usuário exclui um Sway.  <br/> |
|Duplicação de Sway desabilitada  <br/> |SwayDisableDuplication  <br/> |O usuário desabilita a duplicação de um Sway.  <br/> |
|Sway duplicado  <br/> |SwayDuplicate  <br/> |O usuário duplica um Sway.  <br/> |
|Sway editado  <br/> |SwayEdit  <br/> |O usuário edita um Sway.  <br/> |
|Duplicação de Sway habilitada  <br/> |EnableDuplication  <br/> |O usuário habilita a duplicação de um Sway; a capacidade de um usuário habilitar a duplicação de um Sway é habilitada por padrão.  <br/> |
|Compartilhamento de Sway revogado  <br/> |SwayRevokeShare  <br/> |O usuário para de compartilhar um Sway revogando o acesso a ele. Revogar o acesso altera os links associados a um Sway.  <br/> |
|Sway compartilhado  <br/> |SwayShare  <br/> |O usuário pretende compartilhar um Sway. Esse evento captura a ação do usuário de clicar em um destino de compartilhamento específico no menu de compartilhamento do Sway. O evento não indica se o usuário concluiu a ação de compartilhamento.  <br/> |
|DesAtivada o compartilhamento externo do Sway  <br/> |SwayExternalSharingOff  <br/> |O administrador desabilita o compartilhamento externo de Sway para toda a organização usando o centro de administração do Microsoft 365.  <br/> |
|Ativado o compartilhamento externo do Sway  <br/> |SwayExternalSharingOn  <br/> |O administrador habilita o compartilhamento externo de Sway para toda a organização usando o centro de administração do Microsoft 365.  <br/> |
|Serviço de Sway desativado  <br/> |SwayServiceOff  <br/> |O administrador desabilita o Sway para toda a organização usando o centro de administração do Microsoft 365.  <br/> |
|Ativou o serviço Sway  <br/> |SwayServiceOn  <br/> |O administrador habilita o Sway para toda a organização usando o centro de administração do Microsoft 365 (o serviço Sway é habilitado por padrão).  <br/> |
|Sway exibido  <br/> |SwayView  <br/> |O usuário exibe um Sway.  <br/> |
||||

  
### <a name="user-administration-activities"></a>Atividades de administração de usuário
  
A tabela a seguir lista as atividades de administração do usuário registradas quando um administrador adiciona ou altera uma conta de usuário usando o centro de administração do Microsoft 365 ou o portal de gerenciamento do Azure.
  
|**Atividade**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Usuário adicionado  <br/> |Adicionar usuário  <br/> |Uma conta de usuário do Office 365 foi criada.  <br/> |
|Licença de usuário alterada  <br/> |Alterar licença de usuário  <br/> |A licença atribuída a um usuário o que foi alterado. Para ver quais licenças foram alteradas, consulte a atividade do **usuário atualizada** correspondente.  <br/> |
|Senha de usuário alterada  <br/> |Alterar a senha do usuário  <br/> |O administrador alterou a senha da senha de um usuário.  <br/> |
|Usuário excluído  <br/> |Excluir usuário  <br/> |Uma conta de usuário do Office 365 foi excluída.  <br/> |
|Redefinir senha de usuário  <br/> |Redefinir senha de usuário  <br/> |Administrador redefinir a senha de um usuário.  <br/> |
|Propriedade set que força o usuário a alterar a senha  <br/> |Definir a senha de usuário de alteração forçada  <br/> |O administrador define a propriedade que força o usuário a alterar sua senha na próxima vez que o usuário entrar no Office 365.  <br/> |
|Definir propriedades da licença  <br/> |Definir propriedades da licença  <br/> |O administrador modifica as propriedades de um licenciado atribuído a um usuário.  <br/> |
|Usuário atualizado  <br/> |Atualizar usuário  <br/> |O administrador altera uma ou mais propriedades de uma conta de usuário. Para obter uma lista das propriedades de usuário que podem ser atualizadas, consulte a seção "atualizar atributos de usuário" nos [eventos de relatório de auditoria do Active Directory do Azure](https://go.microsoft.com/fwlink/p/?LinkID=616549).  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Atividades de administração de grupos do Azure AD
  
A tabela a seguir lista as atividades de administração de grupo que são registradas quando um administrador ou um usuário cria ou altera um grupo do Office 365 ou quando um administrador cria um grupo de segurança usando o centro de administração do Microsoft 365 ou o portal de gerenciamento do Azure. Para obter mais informações sobre grupos no Office 365, consulte [Exibir, criar e excluir grupos no centro de administração do Microsoft 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Grupo adicionado  <br/> |Adicionar grupo  <br/> |Um grupo foi criado.  <br/> |
|Membro adicionado ao grupo  <br/> |Adicionar membro ao grupo  <br/> |Um membro foi adicionado a um grupo.  <br/> |
|Grupo excluído  <br/> |Excluir grupo  <br/> |Um grupo foi excluído.  <br/> |
|Membro removido do grupo  <br/> |Remover membro de grupo  <br/> |Um membro foi removido de um grupo.  <br/> |
|Grupo atualizado  <br/> |Atualizar grupo  <br/> |Uma propriedade de um grupo foi alterada.  <br/> |
||||
   
### <a name="application-administration-activities"></a>Atividades de administração de aplicativos
  
A tabela a seguir lista as atividades de administração de aplicativos que são registradas quando um administrador adiciona ou altera um aplicativo registrado no Azure AD. Qualquer aplicativo que se baseia no Azure AD para autenticação deve ser registrado no diretório.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Entrada de delegação adicionada  <br/> |Adicionar entrada de delegação  <br/> |Uma permissão de autenticação foi criada/concedida a um aplicativo no Azure AD.  <br/> |
|Entidade de serviço adicionada  <br/> |Adicionar entidade de serviço  <br/> |Um aplicativo foi registrado no Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.  <br/> |
|As credenciais foram adicionadas a uma entidade de serviço  <br/> |Adicionar credenciais de entidade de serviço  <br/> |As credenciais foram adicionadas a uma entidade de serviço no Azure AD. Um princípio de serviço representa um aplicativo no diretório.  <br/> |
|Entrada de delegação reMovida  <br/> |Remover entrada de delegação  <br/> |Uma permissão de autenticação foi removida de um aplicativo no Azure AD.  <br/> |
|Foi reMovida uma entidade de serviço do diretório  <br/> |Remover entidade de serviço  <br/> |Um aplicativo foi excluído/cancelado no Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.  <br/> |
|Credenciais reMovidas de uma entidade de serviço  <br/> |Remover credenciais de entidade de serviço  <br/> |As credenciais foram removidas de uma entidade de serviço no Azure AD. Um princípio de serviço representa um aplicativo no diretório.  <br/> |
|Definir entrada de delegação  <br/> |Definir entrada de delegação  <br/> |Uma permissão de autenticação foi atualizada para um aplicativo no Azure AD.  <br/> |
||||

### <a name="role-administration-activities"></a>Atividades de administração de função
  
A tabela a seguir lista as atividades de administração de função do Azure AD que são registradas quando um administrador gerencia as funções de administrador no centro de administração do Microsoft 365 ou no portal de gerenciamento do Azure.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionar membro à função  <br/> |Adicionar membro de função à função  <br/> |Adicionado um usuário a uma função de administrador no Office 365.  <br/> |
|Removido um usuário de uma função de diretório  <br/> |Remover membro de função da função  <br/> |Removeu um usuário de uma função de administrador no Office 365.  <br/> |
|Definir informações de contato da empresa  <br/> |Definir informações de contato da empresa  <br/> |Atualização das preferências de contato de nível da empresa para sua organização do Office 365. Isso inclui endereços de email para emails relacionados à assinatura enviados pelo Office 365, bem como notificações técnicas sobre os serviços do Office 365.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>Atividades de administração de diretório
  
A tabela a seguir lista as atividades relacionadas a diretórios e domínios do Azure AD que são registradas quando um administrador gerencia sua organização do Office 365 no centro de administração do Microsoft 365 ou no portal de gerenciamento do Azure.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Domínio adicionado à empresa  <br/> |Adicionar domínio à empresa  <br/> |Adicionado um domínio à sua organização do Office 365.  <br/> |
|Adicionado um parceiro ao diretório  <br/> |Adicionar parceiro à empresa  <br/> |Adicionado um parceiro (administrador delegado) à sua organização do Office 365.  <br/> |
|Domínio removido da empresa  <br/> |Remover domínio da empresa  <br/> |Removido um domínio de sua organização do Office 365.  <br/> |
|Removido um parceiro do diretório  <br/> |Remover parceiro da empresa  <br/> |Removido um parceiro (administrador delegado) da sua organização do Office 365.  <br/> |
|Definir informações da empresa  <br/> |Definir informações da empresa  <br/> |Atualizadas as informações da empresa para sua organização do Office 365. Isso inclui endereços de email para emails relacionados à assinatura enviados pelo Office 365, bem como notificações técnicas sobre os serviços do Office 365.  <br/> |
|Definir autenticação de domínio  <br/> |Definir autenticação de domínio  <br/> |Foi alterada a configuração de autenticação de domínio para sua organização do Office 365.  <br/> |
|Atualização das configurações de Federação de um domínio  <br/> |Definir configurações de Federação no domínio  <br/> |Foram alteradas as configurações de Federação (compartilhamento externo) para sua organização do Office 365.  <br/> |
|Definir política de senha  <br/> |Definir política de senha  <br/> |Foram alteradas as restrições de comprimento e caracteres para senhas de usuário na sua organização do Office 365.  <br/> |
|Ativado sincronização do Azure AD  <br/> |Definir o sinalizador DirSyncEnabled na empresa  <br/> |Definir a propriedade que habilita um diretório para a sincronização do Azure AD.  <br/> |
|Domínio atualizado  <br/> |Atualizar domínio  <br/> |Atualização das configurações de um domínio na sua organização do Office 365.  <br/> |
|Domínio verificado  <br/> |Verificar domínio  <br/> |Verificado se sua organização é proprietária de um domínio.  <br/> |
|Verificado o domínio verificado  <br/> |Verificar o domínio verificado por email  <br/> |Usou a verificação de email para verificar se sua organização é proprietária de um domínio.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>atividades de descoberta eletrônica
  
A pesquisa de conteúdo e as atividades relacionadas à descoberta eletrônica realizadas no centro de conformidade e segurança ou executando os cmdlets do PowerShell correspondentes são registradas no log de auditoria. Isso inclui as seguintes atividades:
  
- Criar e gerenciar ocorrências de descoberta eletrônica
    
- Criar, iniciar e editar pesquisas de conteúdo
    
- Executar ações de pesquisa de conteúdo, como Visualizar, exportar e excluir resultados de pesquisa
    
- ConFigurando a filtragem de permissões para pesquisa de conteúdo
    
- Gerenciando a função de administrador de descoberta eletrônica
    
Para obter uma lista e uma descrição detalhada das atividades de descoberta eletrônica registradas, confira [Pesquisar atividades de descoberta eletrônica no log de auditoria do Office 365](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Leva até 30 minutos para que os eventos resultantes das atividades listadas em **atividades de descoberta eletrônica** na lista suspensa de **atividades** seja exibido nos resultados da pesquisa. Por outro lado, leva até 24 horas para que os eventos correspondentes das atividades de cmdlet de descoberta eletrônica apareçam nos resultados da pesquisa. 
  
### <a name="power-bi-activities"></a>Atividades do Power BI
  
Você pode pesquisar o log de auditoria para atividades no Power BI. Para obter informações sobre as atividades do Power BI, consulte a seção "atividades auditadas pelo Power Power BI" em [uso da auditoria dentro da sua organização](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
Observe que o log de auditoria do Power BI não está habilitado por padrão. Para pesquisar atividades do Power BI no log de auditoria do Office 365, você precisa habilitar a auditoria no portal de administração do Power BI. Para obter instruções, consulte a seção "logs de auditoria" no [portal de administração do Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
  
### <a name="microsoft-workplace-analytics-activities"></a>Atividades de análise do Microsoft Workplace

A análise do local de trabalho fornece informações sobre como os grupos colaboram em sua organização do Office 365. A tabela a seguir lista as atividades executadas pelos usuários atribuídos à função Administrador ou às funções de analista no local Analytics. Os usuários atribuídos à função de analista têm acesso total a todos os recursos de serviço e usam a análise de produto. Os usuários atribuídos à função de administrador podem definir configurações de privacidade e padrões do sistema, e podem preparar, carregar e verificar dados organizacionais na análise do local de trabalho. Para obter mais informações, consulte [Workplace Analytics](https://docs.microsoft.com/en-us/workplace-analytics/index-orig).

|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Link OData acEssado <br/> |AccessedOdataLink <br/> |O analista acessou o link OData para uma consulta.|
|Consulta canCelada <br/> |CanceledQuery <br/> |O analista cancelou uma consulta em execução.|
|Exclusão de reunião criada <br/> |MeetingExclusionCreated <br/> |O analista criou uma nova regra de exclusão de reunião.|
|Resultado excluído <br/> |DeletedResult <br/> |O analista excluiu um resultado de consulta.|
|Relatório baixado <br/> |DownloadedReport <br/> |Analista baixado um arquivo de resultado de consulta.|
|Consulta executada <br/> |ExecutedQuery <br/> |O analista executou uma consulta.|
|Configuração de acesso de dados atualizada <br/> |UpdatedDataAccessSetting <br/> |Configurações de acesso de dados atualizadas pelo administrador.|
|Configuração de privacidade atualizada <br/> |UpdatedPrivacySetting <br/> |Configurações de privacidade atualizadas pelo administrador; por exemplo, tamanho mínimo do grupo.|
|Dados da organização carregados <br/> |UploadedOrgData <br/> |Administrador carregou o arquivo de dados organizacionais.|
|Explorar exibição <br/> |ViewedExplore <br/> |Visualizações visualizadas pelo analista em uma ou mais guias de explorações de página.|
||||

### <a name="microsoft-teams-activities"></a>Atividades do Microsoft Teams
  
A tabela a seguir lista as atividades de usuário e de administrador no Microsoft Teams que são registradas no log de auditoria do Office 365. O Microsoft Teams é um espaço de trabalho centrado no chat no Office 365. Ele traz conversas, reuniões, arquivos e anotações de uma equipe em um só lugar. Para obter mais informações e links para tópicos da ajuda, consulte:
  
- [Perguntas frequentes sobre o Microsoft Teams-ajuda do administrador](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Ajuda do Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Foi adicionado um bot à equipe  <br/> |BotAddedToTeam  <br/> |Um usuário adiciona um bot a uma equipe.  <br/> |
|Canal adicionado  <br/> |ChannelAdded  <br/> |Um usuário adiciona um canal a uma equipe.  <br/> |
|Conector adicionado  <br/> |ConnectorAdded  <br/> |Um usuário adiciona um conector a um canal.  <br/> |
|Membros adicionados à equipe  <br/> |MemberAdded  <br/> |Um proprietário de equipe adiciona membro (s) a uma equipe.  <br/> |
|Guia adicionada  <br/> |TabAdded  <br/> |Um usuário adiciona uma guia a um canal.  <br/> |
|Configuração de canal alterada  <br/> |ChannelSettingChanged  <br/> | A operação ChannelSettingChanged é registrada quando as atividades a seguir são executadas por um membro da equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada em parêntese abaixo) é exibida na coluna **Item** nos resultados de pesquisa do log de auditoria.  <br/> <br/>– Altera o nome de um canal de equipe ( **nome do canal**).  <br/>  <br/>– Altera a descrição de um canal de equipe ( **Descrição do canal**).  <br/> |
|Configuração de organização alterada  <br/> |TeamsTenantSettingChanged  <br/> | A operação TeamsTenantSettingChanged é registrada quando as atividades a seguir são realizadas por um administrador global (usando o centro de administração do Microsoft 365); Observe que essas atividades afetam as configurações do Microsoft Teams em toda a organização. Para obter mais informações, consulte [Administrator Settings for Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).  <br/>  Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada em parêntese abaixo) é exibida na coluna **Item** nos resultados de pesquisa do log de auditoria.  <br/><br/>– Habilita ou desabilita o Microsoft Teams para a organização ( **Microsoft Teams**).  <br/><br/>– Habilita ou desabilita a interoperabilidade entre o Microsoft Teams e o Skype for Business para a organização (interoperabilidade **do Skype for Business**).<br/><br/>– Habilita ou desabilita o modo de exibição de gráfico organizacional nos clientes do Microsoft Teams ( **modo de exibição de organograma**).  <br/><br/>– Habilita ou desabilita a capacidade de os membros da equipe agendarem reuniões privadas ( **agendamento de reunião privada**).  <br/><br/>– Habilita ou desabilita a capacidade de os membros da equipe agendarem reuniões de canal ( **agendamento de reunião de canal**).  <br/><br/>– Habilita ou desabilita a chamada de vídeo em reuniões do Teams ( **vídeo para reuniões do Skype**).  <br/><br/>– Habilita ou desabilita o compartilhamento de tela no Microsoft Teams Meetups para a organização ( **compartilhamento de tela para reuniões do Skype**).  <br/><br/>– Habilita ou desabilita essa capacidade de adicionar imagens animadas (chamadas Giphys) a conversas de equipes ( **imagens animadas**).  <br/><br/>– Altera a configuração de classificação de conteúdo da organização ( **classificação de conteúdo**). A classificação de conteúdo restringe o tipo de imagem animada que pode ser exibido em conversas.  <br/><br/>– Habilita ou desabilita a capacidade de os membros da equipe adicionar imagens personalizáveis (chamadas de memes personalizadas) da Internet para conversas da equipe ( **imagens personalizáveis da Internet**).  <br/><br/>– Habilita ou desabilita a capacidade de os membros da equipe adicionarem imagens editáveis (chamadas adesivas) às conversas da equipe ( **imagens editáveis**).<br/><br/>– Habilita ou desabilita essa capacidade para que os membros da equipe usem bots em bate-papos e canais do Microsoft Teams ( **bots em toda a organização**).<br/><br/>– Habilita bots específicos para o Microsoft Teams; Isso não inclui o T-bot, que é o Microsoft Teams Help bot disponível quando os bots estão habilitados para a organização ( **bots individuais**).  <br/><br/>– Habilita ou desabilita a capacidade de os membros da equipe adicionarem extensões ou guias ( **extensões ou guias**).  <br/><br/>– Habilita ou desabilita o carregamento lateral de bots proprietários para o Microsoft Teams ( **carregamento lateral de bots**).  <br/><br/>– Habilita ou desabilita a capacidade para que os usuários enviem mensagens de email para um canal do Microsoft Teams ( **email de canal**).  <br/> |
|Função alterada de membros no Team  <br/> |MemberRoleChanged  <br/> |Um proprietário de equipe altera a função de membro (s) em uma equipe. Os valores a seguir indicam o tipo de função atribuído ao usuário.  <br/><br/><br/> **1** -indica a função do proprietário.<br/>**2** -indica a função de membro. <br/>**3** -indica a função de convidado. <br/>A propriedade Members também inclui o nome da sua organização e o endereço de email do membro.  <br/> |
|Configuração de equipe alterada  <br/> |TeamSettingChanged  <br/> | A operação TeamSettingChanged é registrada quando as atividades a seguir são executadas por um proprietário de equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada em parêntese abaixo) é exibida na coluna **Item** nos resultados de pesquisa do log de auditoria.  <br/><br/>– Altera o tipo de acesso de uma equipe. As equipes podem ser definidas como privadas ou públicas ( **tipo de acesso à equipe**). Quando uma equipe é privada (a configuração padrão), os usuários podem acessar a equipe somente por convite. Quando uma equipe é pública, ela é detectável por qualquer pessoa.  <br/><br/>– Altera a classificação de informações de uma equipe ( **classificação de equipe**).  <br/>  Por exemplo, os dados da equipe podem ser classificados como alto impacto nos negócios, impacto nos negócios médio ou baixo impacto nos negócios.<br/><br/>– Altera o nome de uma equipe ( **nome da equipe**).  <br/><br/>– Altera a descrição da equipe ( **Descrição da equipe**). <br/><br/>– Alterações feitas em qualquer uma das configurações da equipe. Um proprietário de equipe pode acessar essas configurações em um cliente do teams clicando com o botão direito do mouse em uma equipe, clicando em **Gerenciar equipe**e, em seguida, clicando na guia **configurações** . Para essas atividades, o nome da configuração que foi alterada é exibido na coluna **Item** nos resultados da pesquisa de log de auditoria.  <br/> |
|Equipe criada  <br/> |TeamCreated  <br/> |Um usuário cria uma nova equipe.  <br/> |
|Canal excluído  <br/> |ChannelDeleted  <br/> |Um usuário exclui um canal de uma equipe.  <br/> |
|Equipe excluída  <br/> |TeamDeleted  <br/> |Um proprietário de equipe exclui uma equipe.  <br/> |
|Foi removido o bot da equipe  <br/> |BotRemovedFromTeam  <br/> |Um usuário remove um bot de uma equipe.  <br/> |
|Conector removido  <br/> |ConnectorRemoved  <br/> |Um usuário remove o conector de um canal.  <br/> |
|Membros removidos da equipe  <br/> |MemberRemoved  <br/> |Um proprietário de equipe remove membro (s) de uma equipe.  <br/> |
|Guia removido  <br/> |TabRemoved  <br/> |Um usuário remove uma guia de um canal.  <br/> |
|Conector atualizado  <br/> |ConnectorUpdated  <br/> |Um usuário modificou um conector em um canal.  <br/> |
|Guia atualizado  <br/> |TabUpdated  <br/> |Um usuário modificou uma guia em um canal.  <br/> |
|Usuário conectado ao Microsoft Teams  <br/> |TeamsSessionStarted  <br/> |Um usuário entra em um cliente do Microsoft Teams.  <br/> |
||||

### <a name="yammer-activities"></a>Atividades do Yammer
  
A tabela a seguir lista as atividades de usuário e de administrador no Yammer que estão registradas no log de auditoria do Office 365. Para retornar as atividades relacionadas ao Yammer do log de auditoria do Office 365, você precisa selecionar **Mostrar resultados de todas as atividades** na lista de **atividades** . Use as caixas intervalo de datas e lista de **usuários** para restringir os resultados da pesquisa. 
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Política de retenção de dados alterada  <br/> |SoftDeleteSettingsUpdated  <br/> |Verificado se o administrador atualiza a configuração da política de retenção de dados da rede para exclusão forçada ou exclusão reVersível. Somente os administradores verificados podem executar essa operação.  <br/> |
|Configuração de rede alterada  <br/> |NetworkConfigurationUpdated  <br/> |Rede ou verificado o administrador altera a configuração da rede do Yammer. Isso inclui definir o intervalo para exportar dados e habilitar o chat.  <br/> |
|Configurações de perfil de rede alteradas  <br/> |ProcessProfileFields  <br/> |A rede ou o administrador verificado altera as informações que aparecem em perfis de membro para a rede de usuários de rede.  <br/> |
|Modo de conteúdo privado alterado  <br/> |SupervisorAdminToggled  <br/> |Verificado se o administrador ativa ou desativa o *modo de conteúdo privado* . Este modo permite que um administrador visualize postagens em grupos privados e exiba mensagens privadas entre usuários individuais (ou grupos de usuários). Somente administradores verificados podem executar essa operação.  <br/> |
|Configuração de segurança alterada  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Verificado se o administrador atualiza a configuração de segurança da rede do Yammer. Isso inclui a definição de políticas e restrições de validade de senha em endereços IP. Somente os administradores verificados podem executar essa operação.  <br/> |
|Arquivo criado  <br/> |FileCreated  <br/> |O usuário carrega um arquivo.  <br/> |
|Grupo criado  <br/> |GroupCreation  <br/> |O usuário cria um novo grupo.  <br/> |
|Grupo excluído  <br/> |GroupDeletion  <br/> |Um grupo é excluído do Yammer.  <br/> |
|Mensagem excluída  <br/> |MessageDeleted  <br/> |O usuário exclui uma mensagem.  <br/> |
|Arquivo baixado  <br/> |FileDownloaded  <br/> |O usuário baixa um arquivo.  <br/> |
|Dados exPortados  <br/> |Exportação de  <br/> |Verificado se o administrador exporta dados de rede do Yammer. Somente os administradores verificados podem executar essa operação.  <br/> |
|Arquivo compartilhado  <br/> |FileShared  <br/> |O usuário compartilha um arquivo com outro usuário.  <br/> |
|Usuário de rede suspenso  <br/> |NetworkUserSuspended  <br/> |A rede ou o administrador verificado suspende (desativa) um usuário do Yammer.  <br/> |
|Usuário suspenso  <br/> |UserSuspensão  <br/> |A conta de usuário é suspensa (desativada).  <br/> |
|Descrição do arquivo atualizado  <br/> |FileUpdateDescription  <br/> |O usuário altera a descrição de um arquivo.  <br/> |
|Nome de arquivo atualizado  <br/> |FileUpdatename  <br/> |O usuário altera o nome de um arquivo.  <br/> |
|Arquivo exibido  <br/> |FileVisitado  <br/> |O usuário exibe um arquivo.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Atividades de fluxo da Microsoft

Você pode pesquisar o log de auditoria para atividades no Microsoft Flow. Essas atividades incluem criar, editar e excluir fluxos e alterar as permissões de fluxo. Para obter informações sobre auditoria de atividades de fluxo, consulte o blog [Microsoft Flow Audit Events Now Available in Security _AMP_ Compliance Center](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Você pode pesquisar no log de auditoria por atividades relacionadas ao aplicativo no PowerApps. Essas atividades incluem criar, iniciar e publicar um aplicativo. A atribuição de permissões a aplicativos também é auditada. Para obter uma descrição de todas as atividades do PowerApps, consulte [log de atividade do powerapps](https://docs.microsoft.com/en-us/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Atividades do Microsoft Stream
  
Você pode pesquisar o log de auditoria para atividades no Microsoft Stream. Essas atividades incluem atividades de vídeo realizadas por usuários, atividades de canal de grupo e atividades administrativas, como gerenciamento de usuários, gerenciamento de configurações da organização e exportação de relatórios. Para obter uma descrição dessas atividades, consulte a seção "atividades registradas no Microsoft Stream" em [logs de auditoria no Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Log de auditoria de administração do Exchange
  
Registro em log de auditoria do administrador do Exchange, que é habilitado por padrão no Office 365 — registra um evento no log de auditoria do Office 365 quando um administrador (ou um usuário que tenha recebido permissões administrativas) faz uma alteração na sua organização do Exchange Online. As alterações feitas usando o centro de administração do Exchange ou executando um cmdlet no Windows PowerShell são registradas no log de auditoria do administrador do Exchange. Para obter informações mais detalhadas sobre o log de auditoria de administrador no Exchange, consulte [log de auditoria de administrador](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Veja algumas dicas para pesquisar atividades no log de auditoria de administração do Exchange:
  
- Para retornar entradas do log de auditoria do administrador do Exchange, você precisa selecionar **Mostrar resultados de todas as atividades** na lista de **atividades** . Use as caixas intervalo de datas e de **usuários** para restringir os resultados da pesquisa para cmdlets executados por um administrador do Exchange específico em um intervalo de datas específico. 
    
- Para exibir eventos do log de auditoria do administrador do Exchange, filtre os resultados da pesquisa **-** e digite um (travessão) na caixa filtro de **atividade** . Isso exibirá os nomes de cmdlet, que são exibidos na coluna **atividade** dos eventos de administração do Exchange. Em seguida, você pode classificar os nomes de cmdlets em ordem alfabética. 
    
    ![Digite um traço na caixa atividades para filtrar eventos de administração do Exchange](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Para obter informações sobre qual cmdlet foi executado, quais parâmetros e valores de parâmetro foram usados e quais objetos foram afetados, você precisará exportar os resultados da pesquisa e selecionar a opção **baixar todos os resultados** . 
    
- Você também pode exibir eventos no log de auditoria do administrador do Exchange usando o centro de administração do Exchange. Para obter instruções, consulte [View the Administrator Audit Log](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Perguntas frequentes

**Onde posso encontrar os recursos oferecidos pelo serviço de auditoria no Office 365?**

Para obter mais informações sobre os recursos de auditoria e relatórios disponíveis no Office 365, consulte [Auditing and Reporting in office 365](office-365-auditing-and-reporting-overview.md). 

**Quais são os diferentes serviços do Office 365 que são auditados atualmente?**

Os serviços do Office 365 mais usados, como o Exchange Online, o SharePoint Online, o OneDrive for Business, o Azure Active Directory, o Microsoft Teams, o Dynamics 365, a proteção avançada contra ameaças e o Power BI são auditados. Consulte o [início deste artigo](search-the-audit-log-in-security-and-compliance.md) para obter uma lista de serviços que são auditados.

**Quais atividades são auditadas pelo serviço de auditoria no Office 365?**

Consulte a seção [atividades auditadas](#audited-activities) neste artigo para obter uma lista e descrição das atividades que são auditadas no Office 365.

**Quanto tempo leva para que um registro de auditoria fique disponível após a ocorrência de um evento?**

A maioria dos dados de auditoria está disponível em 30 minutos, mas pode levar até 24 horas após um evento ocorrer para que a entrada de log de auditoria correspondente seja exibida nos resultados da pesquisa. Consulte a tabela na seção [antes de começar](#before-you-begin) deste artigo, que mostra o tempo que leva para eventos nos diferentes serviços do Office 365 a estar disponível.

**Por quanto tempo os registros de auditoria são mantidos?**

Conforme explicado anteriormente, o período de retenção para registros de auditoria depende da assinatura do Office 365 da sua organização.  

- **Office 365 E3** -os registros de auditoria são mantidos por 90 dias.

- **Office 365 E5** -os registros de auditoria são mantidos por 365 dias (um ano). Manter registros de auditoria por um ano também está disponível para organizações que possuem uma assinatura E3 e uma assinatura de complemento de conformidade avançada do Office 365.

     > [!NOTE]
     > Como explicado anteriormente, o período de retenção de um ano para registros de auditoria para organizações E5 (ou organizações E3 que têm licenças de complemento de conformidade avançada) atualmente está disponível apenas como parte de um programa de visualização privado. Para se inscrever neste programa de visualização, registre uma solicitação com o [suporte da Microsoft](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) e inclua o seguinte como a descrição do que você precisa ajuda com: "visualização privada do log de auditoria do Office 365 de longo prazo".

Observe também que a duração do período de retenção para registros de auditoria é baseada em licenciamento por usuário. Por exemplo, se um usuário na sua organização é atribuído a uma licença do Office 365 E3, os registros de auditoria para atividades realizadas por esse usuário são mantidos por 90 dias. Se um usuário diferente recebe uma licença do Office 365 e5, seus registros de auditoria são mantidos por um ano. 

**Posso acessar os dados de auditoria programaticamente?**

Sim. A API de atividade de gerenciamento do Office 365 é usada para buscar os logs de auditoria programaticamente.  Para começar, confira introdução [às APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Há outras maneiras de obter logs de auditoria diferentes de usar o centro de segurança e conformidade ou a API de atividade de gerenciamento do Office 365?**

Não. Estas são as duas maneiras de obter dados do serviço de auditoria do Office 365. 

**É necessário habilitar individualmente a auditoria em cada serviço para o qual desejo capturar os logs de auditoria?**

Na maioria dos serviços do Office 365, a auditoria é habilitada por padrão depois que você ativa inicialmente a auditoria para sua organização do Office 365 (conforme descrito na seção [antes de começar](#before-you-begin) neste artigo). No enTanto, é necessário habilitar a auditoria de caixa de correio no Exchange Online para cada caixa de correio que você deseja auditar.   Estamos trabalhando para habilitar a auditoria de caixa de correio por padrão para todas as caixas de correio em uma organização do Office 365. Para saber mais, confira "A auditoria de caixa de correio do Exchange ativada por padrão" no [blog de Segurança, Privacidade e Conformidade da Microsoft](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171).

**O serviço de auditoria do Office 365 oferece suporte à eliminação de duplicação de registros?**

Não. O pipeline de serviço de auditoria é quase em tempo real e, portanto, não oferece suporte à eliminação de duplicação.
 
**Os dados de auditoria do Office 365 fluem entre regiões geográficas?**

Não. Atualmente, temos implantações de pipeline de auditoria nas regiões NA (América do Norte), EMEA (Europa, Oriente Médio e África) e da Ásia (Pacífico). No enTanto, podemos transmitir os dados entre essas regiões para balanceamento de carga e apenas durante problemas do local. Quando realizamos essas atividades, os dados em trânsito são criptografados.   
 
**A auditoria de dados está criptografada?**

Os dados de auditoria são armazenados em caixas de correio do Exchange (dados em repouso) na mesma região onde o pipeline de auditoria é implantado. Esses dados não são criptografados. No enTanto, os dados em trânsito são sempre criptografados. 
