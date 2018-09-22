---
title: Pesquisar o log de auditoria no Centro de Conformidade &amp; Segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365AC_AlternativeEmailAddress
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Usar a segurança do Office 365 &amp; Centro de conformidade para pesquisar o log de auditoria unificada para exibir a atividade de administrador e usuário em sua organização do Office 365. '
ms.openlocfilehash: dc673b8f52bacccfa746ad258ea91d8dd2074eeb
ms.sourcegitcommit: bf70ec8e11b3f75bf45cd4f760cd1a982593dbad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2018
ms.locfileid: "24962967"
---
# <a name="search-the-audit-log-in-the-office-365-security-amp-compliance-center"></a>Pesquisar o log de auditoria no Centro de Conformidade &amp; Segurança do Office 365

Precisa encontrar se um usuário exibido um documento específico ou removidos de um item de suas caixas de correio? Se precisar, você pode usar a segurança do Office 365 &amp; Centro de conformidade para pesquisar o log de auditoria unificada para exibir a atividade de administrador e usuário em sua organização do Office 365. Por que uma auditoria unificada efetuar? Porque você pode pesquisar os seguintes tipos de atividade do usuário e administração no Office 365:
  
- Atividade do usuário no SharePoint Online e o OneDrive for Business
    
- Atividade do usuário no Exchange Online (log de auditoria de caixa de correio do Exchange)
    
    > [!IMPORTANT]
    > Auditoria de caixa de correio log deve ser ativado para cada caixa de correio do usuário antes de atividade do usuário no Exchange Online será registrada. Para obter mais informações, consulte [Habilitar caixa de correio auditorias no Office 365](enable-mailbox-auditing.md).
  
- Atividade de administração no SharePoint Online
    
- Atividade de administração no Windows Azure Active Directory (o serviço de diretório para o Office 365)
    
- Atividade de administrador no Exchange Online (log de auditoria do administrador do Exchange)
    
- Atividade do usuário e administração no Sway
    
- atividades de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade
    
- Atividade do usuário e administração no Power BI para Office 365
    
- Atividade do administrador e usuário em Teams da Microsoft
    
- Atividade do usuário e administração no Yammer
    
- Atividade do administrador e usuário em Stream da Microsoft
    
   
## <a name="before-you-begin"></a>Antes de começar

Certifique-se de ler o log de auditoria de itens a seguir antes de você inicia a pesquisa do Office 365.
  
- Você (ou outro administrador) deve primeiro ativar log de auditoria antes de começar a pesquisar o log de auditoria do Office 365. Para ativá-lo, basta clicar em * * Iniciar gravação atividade de administrador e usuário * * na página de **pesquisa de log de auditoria** na segurança &amp; Centro de conformidade. (Se você não vir este link, auditoria já foi ativado para sua organização.) Depois que você ativá-lo, será exibida uma mensagem que informa que o log de auditoria está sendo preparado e que você pode executar uma pesquisa de duas horas após a preparação estiver concluída. Você só precisa fazer isso vez. 
    
    > [!NOTE]
    > Estamos no processo de ativação de auditoria, por padrão. Enquanto isso, você pode ativá-lo conforme descrito anteriormente. 
  
- Você precisa ter a função Logs de auditoria somente para exibição ou Logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de função de gerenciamento de conformidade e gerenciamento da organização na página **permissões** no Centro de administração do Exchange. Para conceder a um usuário a capacidade de pesquisar o log de auditoria do Office 365 com o nível mínimo de privilégios, você pode criar um grupo de função personalizada no Exchange Online, adicionar a função Logs de auditoria somente para exibição ou Logs de auditoria e, em seguida, adicionar o usuário como um membro do novo grupo de função. Para obter mais informações, consulte a [função de gerenciar grupos no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Se você atribuir um usuário a função Logs de auditoria somente para exibição ou Logs de auditoria na página **permissões** na segurança &amp; Centro de conformidade, eles não poderão pesquisar o log de auditoria do Office 365. Você precisa atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online. 
  
- Se você deseja desativar a pesquisa de log de auditoria no Office 365 para sua organização, você pode executar o seguinte comando no PowerShell remoto conectado à sua organização do Exchange Online:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Para ativar novamente a pesquisa de auditoria, você pode executar o seguinte comando no PowerShell do Exchange Online:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Para obter mais informações, consulte [desativar a pesquisa de log de auditoria no Office 365](turn-audit-log-search-on-or-off.md).
    
- Conforme indicado anteriormente, o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online, que é **UnifiedAuditLog de pesquisa**. Isso significa que você pode usar esse cmdlet para pesquisar o log de auditoria do Office 365 em vez de usar a página de **pesquisa de log de auditoria** na segurança &amp; Centro de conformidade. Você precisa executar esse cmdlet do PowerShell remoto conectado à sua organização do Exchange Online. Para obter mais informações, consulte [UnifiedAuditLog de pesquisa](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Se você deseja baixar programaticamente os dados do log de auditoria do Office 365, é recomendável que você usar a API de atividade de gerenciamento do Office 365 em vez de usar um script do PowerShell. A API de atividade de gerenciamento do Office 365 é um serviço web REST que você pode usar para desenvolver soluções de monitoramento de conformidade para sua organização, segurança e operações. Para obter mais informações, consulte [referência de API de atividade de gerenciamento do Office 365](https://go.microsoft.com/fwlink/?linkid=852309).
    
- Você pode pesquisar o log de auditoria do Office 365 para atividades que foram executadas nos últimos 90 dias.
    
- Ele pode levar até 30 minutos ou backup de 24 horas após um evento ocorre para a entrada de log de auditoria correspondente a ser exibido nos resultados da pesquisa. A tabela a seguir mostra o tempo que leva para os diferentes serviços no Office 365.
    
|**Serviço do Office 365**|**30 minutos**|**24 horas**|
|:-----|:-----|:-----|
|Azure Active Directory (admin events)  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Azure Active Directory (eventos de logon do usuário)  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Exchange Online  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Microsoft Teams  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Power BI  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Segurança &amp; Centro de conformidade  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|SharePoint Online e OneDrive for Business  <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Sway  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Yammer  <br/> ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (AD Azure) é o serviço de diretório para o Office 365. O log de auditoria unificada contém o usuário, grupo, aplicativo, domínio e atividades de diretório realizadas no Centro de administração do Office 365 ou no Azure no portal de gerenciamento. Para obter uma lista completa de eventos do Windows Azure AD, consulte [Eventos de relatório de auditoria do Active Directory do Windows Azure](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Logs de auditoria Exchange Online consistem em dois tipos de eventos: eventos de administração (ações executadas pelos administradores) e eventos de caixa de correio (ações tomadas pelos usuários em caixas de correio) do Exchange. Observe que a auditoria de caixa de correio não está habilitado por padrão. Ela deve ser ativar para cada caixa de correio do usuário antes de eventos de caixa de correio podem ser pesquisados no log de auditoria do Office 365. Para obter mais informações sobre a auditoria de caixa de correio e a caixa de correio auditoria de ações que serão registradas, consulte [Habilitar caixa de correio auditorias no Office 365](enable-mailbox-auditing.md).
    
- Log de auditoria para Power BI não está habilitado por padrão. Para procurar atividades Power BI no log de auditoria do Office 365, você precisa habilitar a auditoria no portal de administração do Power BI. Para obter instruções, consulte [Power BI de auditoria](https://docs.microsoft.com/power-bi/service-admin-auditing#enabling-auditing-functionality-in-the-power-bi-admin-portal).
    
    
## <a name="search-the-audit-log"></a>Pesquisas o log de auditoria

Aqui é o processo para pesquisar o log de auditoria no Office 365.
  
[Etapa 1: Executar uma pesquisa de log de auditoria](#step-1-run-an-audit-log-search)
  
[Etapa 2: Exibir os resultados da pesquisa](#step-2-view-the-search-results)

[Etapa 3: Filtrar os resultados de pesquisa](#step-3-filter-the-search-results)

[Etapa 4: Exportar os resultados da pesquisa para um arquivo](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Etapa 1: Executar uma pesquisa de log de auditoria

1. Acesse [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Usar uma sessão de navegação privada (não uma sessão normal) para acessar a segurança do Office 365 &amp; conformidade centraliza porque isso impedirá que as credenciais que você está conectado atualmente com sejam usados. Para abrir uma sessão de Navegação InPrivate no Internet Explorer ou Microsoft Edge, basta pressione CTRL + SHIFT + P. Para abrir uma sessão de navegação privada no Google Chrome (chamados de uma janela incognito), pressione CTRL + SHIFT + N. 
  
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação**e clique em **pesquisa de log de auditoria**.
    
    A página de **pesquisa de log de auditoria** é exibida. 
    
    ![Configurar critérios e, em seguida, clique em Pesquisar para executar o relatório](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Você deve primeiro ativar o log de auditoria antes de executar uma pesquisa de log de auditoria. Se o link **Iniciar gravação atividade de administrador e usuário** for exibido, clique para ativar a auditoria. Se você não vir este link, auditoria já foi ativado para sua organização. 
  
4. Configure os seguintes critérios de pesquisa:
    
1. **Atividades** Clique na lista suspensa para exibir as atividades que você pode pesquisar. Atividades de administrador e usuário são organizadas em grupos de atividades relacionadas. Você pode selecionar atividades específicas ou você pode clicar no nome do grupo de atividade para selecionar todas as atividades no grupo. Você também pode clicar uma atividade selecionada para limpar a seleção. Após executar a pesquisa, apenas as entradas de log de auditoria para as atividades selecionadas são exibidas. A seleção de **Mostrar os resultados de todas as atividades** exibirá resultados para todas as atividades realizadas pelo usuário selecionado ou grupo de usuários. 
    
    Mais de 100 atividades de administrador e usuário são registradas no log de auditoria do Office 365. Clique na guia **atividades auditadas** , no tópico deste artigo para ver as descrições de cada atividade em cada um dos serviços do Office 365 diferentes. 
    
2. **Data de início** e **Data de término** últimos sete dias são marcadas por padrão. Selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. A data e hora são apresentados no formato Tempo Universal Coordenado (UTC). O intervalo de datas máximo que você pode especificar é 90 dias. Um erro será exibido se o intervalo de datas selecionado é maior que 90 dias. 
    
    > [!TIP]
    > Se você estiver usando o intervalo de datas máximo de 90 dias, selecione a hora atual para a **Data de início**. Caso contrário, você receberá uma mensagem de erro informando que a data de início é anterior à data de término. Se você tiver ativado a auditoria nos últimos 90 dias, o intervalo de datas máximo não pode iniciar antes da data em que a auditoria foi ativada. 
  
3. **Usuários** Clique nesta caixa e selecione um ou mais usuários para exibir resultados de pesquisa para. As entradas do log de auditoria da atividade selecionada executadas pelos usuários que você selecionar nesta caixa são exibidas na lista de resultados. Deixe esta caixa em branco para retornar as entradas para todos os usuários (e contas de serviço) em sua organização. 
    
4. **Arquivo ou pasta** Digite parte ou todo um nome de arquivo ou pasta para procurar a atividade relacionada ao arquivo da pasta que contém a palavra-chave especificada. Você também pode especificar uma URL de um arquivo ou pasta. Se você usar uma URL, certifique-se de que o tipo o caminho completo do URL, ou se você digitar apenas uma parte da URL, não inclua quaisquer caracteres especiais ou espaços. 
    
    Deixe esta caixa em branco para retornar as entradas para todos os arquivos e pastas em sua organização.
    
5. Clique em **pesquisa** para executar a pesquisa usando os critérios de pesquisa. 
    
    Os resultados da pesquisa são carregados e, após alguns momentos, eles são exibidos em **resultados**. Quando a pesquisa for concluída, o número de resultados encontrados é exibido. Observe que um máximo de 5.000 eventos será exibido no painel de **resultados** , em incrementos de 150 eventos; Se mais de 5.000 eventos atendam aos critérios de pesquisa, os eventos de 5.000 mais recentes serão exibidos. 
    
    ![O número de resultados é exibido após o término da pesquisa](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Dicas para pesquisar o log de auditoria

- Você pode selecionar atividades específicas para procurar clicando no nome da atividade. Ou você pode pesquisar todas as atividades em um grupo (por exemplo, **as atividades de arquivos e pastas**), clicando no nome do grupo. Se uma atividade for selecionada, você pode clicar para cancelar a seleção. Você também pode usar a caixa de pesquisa para exibir as atividades que contêm a palavra-chave que você digita.
    
    ![Clique no nome do grupo de atividade para selecionar todas as atividades](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Você precisa selecionar **Mostrar resultados para todas as atividades** na lista de **atividades** para exibir eventos de log de auditoria do administrador do Exchange. Eventos de log de auditoria este exibem um nome de cmdlet (por exemplo, **Set-Mailbox** ) na coluna nos resultados da **atividade** . Para obter mais informações, clique na guia **atividades auditadas** neste tópico e clique em **atividades de administração do Exchange**.
    
    Da mesma forma, há algumas atividades de auditoria que não têm um item correspondente na lista de **atividades** . Se você souber o nome da operação para essas atividades, você pode pesquisar todas as atividades e filtrar os resultados, digitando o nome da operação na caixa para a coluna de **atividade** . Consulte [etapa 3: filtrar os resultados de pesquisa](#step-3-filter-the-search-results) para obter mais informações sobre como filtrar os resultados. 
    
- Clique em **Limpar** para limpar os critérios de pesquisa atual. O intervalo de datas retorna o valor padrão de últimos sete dias. Também é possível clicar **Limpar tudo para mostrar os resultados de todas as atividades** para cancelar todas as atividades selecionadas. 
    
- Se forem encontrados 5.000 resultados, você pode assumir provavelmente há mais de 5.000 eventos que atendidos os critérios de pesquisa. Você pode refinar os critérios de pesquisa e execute novamente a pesquisa para retornar resultados menos ou você pode exportar todos os resultados de pesquisa, selecionando **exportar os resultados da** \> **Baixe todos os resultados**.

  
### <a name="step-2-view-the-search-results"></a>Etapa 2: Exibir os resultados da pesquisa

Os resultados de uma pesquisa de log de auditoria são exibidos em **resultados** na página de **pesquisa de log de auditoria** . Conforme anteriormente mencionado um máximo de 5.000 eventos (mais recentes) são exibidos em incrementos de 150 eventos. Para exibir mais eventos você pode usar a barra de rolagem no painel de **resultados** ou você pode pressionar **Shift + End** para exibir os eventos de 150 Avançar. 
  
Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa.
  
- **Data:** A data e a hora (no formato UTC) quando o evento ocorreu. 
    
- **Endereço IP:** O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido no formato de endereço de um IPv4 ou IPv6. 
    
- **Usuário:** A conta de usuário (ou serviço) que executou a ação que acionou o evento. 
    
- **Atividade:** A atividade foi executada pelo usuário. Esse valor corresponde às atividades selecionado na lista suspensa **atividades** . Para um evento do log de auditoria do administrador do Exchange, o valor nessa coluna é um cmdlet do Exchange. 
    
- **Item:** O objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta de usuário que foi atualizada. Nem todas as atividades têm um valor nessa coluna. 
    
- **Detalhes:** Detalhes adicionais sobre uma atividade. Novamente, nem todas as atividades terá um valor. 
    
> [!TIP]
> Clique em um cabeçalho de coluna em **resultados** para classificar os resultados. Você pode classificar os resultados de À Z ou Z a. Clique o cabeçalho de **Data** para classificar os resultados do mais antigo mais recente para o mais antiga ou mais recente. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Exibir os detalhes de um evento específico

Você pode exibir mais detalhes sobre um evento clicando o registro de evento na lista de resultados da pesquisa. É exibida uma página de **detalhes** que contém as propriedades detalhadas do registro de eventos. As propriedades que são exibidas dependem do serviço do Office 365 no qual o evento ocorre. Para exibir esses detalhes, clique em **obter mais informações**. Para obter descrições, consulte o [log de auditoria de propriedades detalhadas no Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
![Clique em obter mais informações para exibir as propriedades detalhadas sobre o registro de eventos de log de auditoria](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Etapa 3: Filtrar os resultados de pesquisa

Além de classificar, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Este é um ótimo recurso que pode ajudar você a filtrar rapidamente os resultados para um usuário específico ou atividade. Você pode criar inicialmente uma ampla pesquisa e então rapidamente filtrar os resultados para ver eventos específicos. Em seguida, você pode restringir os critérios de pesquisa e execute novamente a pesquisa para retornar um conjunto menor, mais conciso de resultados.
  
Para filtrar os resultados:
  
1. Execute uma pesquisa de log de auditoria.
    
2. Quando os resultados são exibidos, clique em **filtrar os resultados**.
    
    Caixas de palavra-chave serão exibidas em cada cabeçalho de coluna.
    
3. Clique em uma das caixas em um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna que você está filtrando. Os resultados serão reajustar dinamicamente para exibir os eventos que correspondem ao seu filtro.
    
    ![Digite uma palavra no filtro para exibir os eventos que correspondem ao filtro](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Para limpar um filtro, clique em **X** na caixa filtro ou basta clicar em **ocultar a filtragem**.
    
> [!TIP]
> Para exibir eventos de log de auditoria do administrador do Exchange, digite um **-** (traço) na caixa de filtro de **atividade** . Isso exibirá os nomes de cmdlet, que são exibidos na coluna **atividade** para eventos de administração do Exchange. Em seguida, você pode classificar os nomes de cmdlet em ordem alfabética. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Etapa 4: Exportar os resultados da pesquisa para um arquivo

Você pode exportar os resultados de uma pesquisa de log de auditoria para um arquivo de (CSV) de valores separados por vírgulas no computador local. Você pode abrir este arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e a divisão de uma única coluna (que contém as células de valores múltiplos) em várias colunas.
  
1. Executar uma pesquisa de log de auditoria e posteriormente revisar os critérios de pesquisa até que você tenha os resultados desejados.
    
2. Clique em **exportar os resultados** e selecione uma das seguintes opções: 
    
  - **Salvar resultados carregados** Escolher esta opção para exportar apenas as entradas que são exibidas em **resultados** no * * pesquisa de log de auditoria * * página. O arquivo CSV que é baixado contém as mesmas colunas (e dados) exibidos na página (data, usuário, atividade, Item e detalhes). Uma coluna adicional (chamada **mais**) está incluída no arquivo CSV que contém mais informações da entrada de log de auditoria. Porque você está exportando os mesmos resultados que são carregados (e visualizável) na página de **pesquisa de log de auditoria** , um máximo de 5.000 entradas são exportados. 
    
  - **Baixe todos os resultados** Escolha esta opção para exportar todas as entradas de log de auditoria do Office 365 que atendam aos critérios de pesquisa. Para um grande conjunto de resultados da pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além de 5.000 resultados que podem ser exibidos na página de **pesquisa de log de auditoria** . Essa opção baixar os dados brutos do log de auditoria para um arquivo CSV e contém informações adicionais da entrada de log de auditoria em uma coluna chamada **AuditData**. Pode levar mais tempo para baixar o arquivo, se você escolher essa opção de exportação porque o arquivo pode ser muito maior daquela que é baixado se você escolher a opção outra.
    
    > [!IMPORTANT]
    > Você pode baixar um máximo de 50.000 entradas para um arquivo CSV de uma pesquisa de log de auditoria único. Se 50.000 entradas são baixadas para o arquivo CSV, você pode assumir provavelmente há mais de 50.000 eventos que atendidos os critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas de log de auditoria. Você pode precisar executar várias pesquisas com menores intervalos de data para exportar entradas mais de 50.000. 
  
3. Depois de selecionar uma opção de exportação, uma mensagem é exibida na parte inferior da janela solicitando que você abra o arquivo CSV, salve-o na pasta Downloads ou salvá-lo em uma pasta específica.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>Para obter mais informações sobre como exportar os resultados de pesquisa do log de auditoria

- A opção **Baixar todos os resultados de** baixa os dados brutos do log de auditoria do Office 365 para um arquivo CSV. Esse arquivo contém os nomes de coluna diferentes (CreationDate, UserIds, operação, AuditData) que o arquivo é baixado, se você selecionar a opção **Salvar resultados carregados** . Os valores nos dois arquivos CSV diferentes para a mesma atividade também podem ser diferentes. Por exemplo, a atividade na coluna **ação** no CSV do arquivo e pode ter um valor diferente do que a versão "amigável" é exibido na coluna **atividade** na página de **pesquisa de log de auditoria** ; Por exemplo, MailboxLogin versus usuário conectado à caixa de correio.
    
- Se você baixe todos os resultados, o arquivo CSV contém uma coluna chamada **AuditData**, que contém informações adicionais sobre cada evento. Conforme indicado anteriormente, esta coluna contém uma propriedade de múltiplos valor para várias propriedades do registro de log de auditoria. Cada um dos pares de **valor da propriedade:** nessa propriedade de valores múltiplos são separados por uma vírgula. Você pode usar a consulta de energia no Excel para dividir essa coluna em várias colunas, de modo que cada propriedade terá sua própria coluna. Isso permitirá que você classificar e filtrar em uma ou mais dessas propriedades. Para saber como fazer isso, consulte a seção "Dividir uma coluna por delimitador" em [uma coluna de texto (Power consulta) de divisão](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662).
    
    Depois de dividir a coluna **AuditData** , você pode filtrar a coluna de **operações** para exibir as propriedades detalhadas para um tipo específico de atividade. 
    
- Há um limite de caracteres 3,060 para os dados que são exibidos no campo **AuditData** para um registro de auditoria. Se o limite de caracteres 3,060 for excedido, os dados neste campo serão truncados. 
    
- Quando você baixe todos os resultados de uma consulta de pesquisa que contém eventos de serviços diferentes do Office 365, a coluna **AuditData** no arquivo CSV contém propriedades diferentes, dependendo de qual serviço a ação foi realizado no. Por exemplo, as entradas de logs de auditoria do Exchange e o Azure AD incluem uma propriedade denominada **ResultStatus** que indica se a ação foi bem-sucedida ou não. Essa propriedade não está incluída para eventos no SharePoint. Da mesma forma, o SharePoint eventos possuem uma propriedade que identifica o site de atividades relacionadas à URL para arquivos e pastas. Para atenuar esse comportamento, considere o uso de pesquisas diferentes para exportar os resultados para atividades de um único serviço. 
    
    Para obter uma descrição das propriedades listadas na coluna **AuditData** no arquivo CSV quando você baixe todos os resultados e o serviço de cada uma se aplica ao, consulte o [log de auditoria de propriedades detalhadas no Office 365](detailed-properties-in-the-office-365-audit-log.md).

  
## <a name="audited-activities"></a>Atividades auditadas

As tabelas desta seção descrevem as atividades que são auditadas no Office 365. Você pode pesquisar por esses eventos pesquisando a auditoria, faça logon na segurança &amp; Centro de conformidade. Clique na guia **pesquisa o log de auditoria** para obter instruções detalhadas. 
  
Nestas tabelas Agrupar atividades relacionadas ou as atividades de um serviço específico do Office 365. As tabelas incluem o nome amigável que é exibido na lista suspensa de **atividades** e o nome da operação correspondente que aparece nas informações detalhadas de um registro de auditoria e no arquivo CSV ao exportar os resultados da pesquisa. Para obter descrições das informações detalhadas, consulte o [log de auditoria de propriedades detalhadas no Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
Clique em um dos seguintes links para ir para uma tabela específica.
  
||||
|:-----|:-----|:-----|
|[Atividades de arquivo e página](#file-and-page-activities)<br/> |[Atividades de pasta](#folder-activities)<br/> |[Atividades de solicitação de compartilhamento e acesso](#sharing-and-access-request-activities)<br/> |
|[Atividades de sincronização](#synchronization-activities)<br/> |[Atividades de administração de site](#site-administration-activities)<br/> |[Atividades de caixa de correio do Exchange](#exchange-mailbox-activities)<br/> |
|[Atividades de sway](#sway-activities) <br/> |[Atividades de administração do usuário](#user-administration-activities) <br/> |[Atividades de administração de grupo do Windows Azure AD](#azure-ad-group-administration-activities) <br/> |
|[Atividades de administração do aplicativo](#application-administration-activities) <br/> |[Atividades de administração de função](#role-administration-activities) <br/> |[Atividades de administração de diretório](#directory-administration-activities) <br/> |
|[atividades de descoberta eletrônica](#ediscovery-activities) <br/> |[Atividades do Power BI](#power-bi-activities) <br/> |[Atividades de Teams da Microsoft](#microsoft-teams-activities) <br/> |
|[Atividades do Yammer](#yammer-activities) <br/> |[Microsoft Stream](#microsoft-stream) <br/> |[Log de auditoria de administração do Exchange](#exchange-admin-audit-log) <br/> |
   
  
### <a name="file-and-page-activities"></a>Atividades de arquivo e página
  
A tabela a seguir descreve as atividades de página e o arquivo no SharePoint Online e o OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Arquivos acessados  <br/> |FileAccessed  <br/> |Conta de usuário ou o sistema acessa um arquivo.  <br/> |
|(nenhum)  <br/> |FileAccessedExtended  <br/> |Isso está relacionado ao "arquivo acessado" atividade (FileAccessed). Um evento FileAccessedExtended é registrado quando a mesma pessoa continuamente acessa um arquivo por um longo período de tempo (até 3 horas). A finalidade do log de eventos FileAccessedExtended é reduzir o número de eventos de FileAccessed que são registrados quando um arquivo é acessado continuamente. Isso ajuda a reduzir o ruído de vários registros de FileAccessed para o que é essencialmente a mesma atividade do usuário e permite que você se concentrar no evento FileAccessed inicial (e mais importante).  <br/> |
|Check-in do arquivo  <br/> |FileCheckedIn  <br/> |Verificações de usuário em um documento que eles check-out de uma biblioteca de documentos.  <br/> |
|Check-out do arquivo  <br/> |FileCheckedOut  <br/> |Usuário fizer o check-out de um documento localizado em uma biblioteca de documentos. Os usuários podem fazer check-out e fazer alterações em documentos que foram compartilhados com eles.  <br/> |
|Arquivo copiado  <br/> |FileCopied  <br/> |Usuário copia um documento de um site. Pode ser salvo o arquivo copiado para outra pasta no site.  <br/> |
|Arquivo excluído  <br/> |FileDeleted  <br/> |Usuário exclui um documento de um site.  <br/> |
|Arquivo excluído da Lixeira  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Usuário exclui um arquivo da Lixeira de um site.  <br/> |
|Arquivo excluído da Lixeira de segundo estágio  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Usuário exclui um arquivo da Lixeira de segundo estágio de um site.  <br/> |
|Malware detectado no arquivo  <br/> |FileMalwareDetected  <br/> |Mecanismo de antivírus do SharePoint detecta malware em um arquivo.  <br/> |
|Check-out do arquivo descartada  <br/> |FileCheckOutDiscarded  <br/> |O usuário descarta (ou desfaz) o check-out de um arquivo. Isso significa que as alterações feitas no arquivo no momento do check-out serão descartadas e não serão salvas na versão do documento na biblioteca de documentos.  <br/> |
|Arquivo baixado  <br/> |FileDownloaded  <br/> |Usuário baixa um documento de um site.  <br/> |
|Arquivo modificado  <br/> |FileModified  <br/> |Conta de usuário ou sistema modifica o conteúdo ou as propriedades de um documento localizado em um site.  <br/> |
|(nenhum)  <br/> |FileModifiedExtended  <br/> |Isso está relacionado ao "arquivo modificado" atividade (FileModified). Um evento FileModifiedExtended é registrado quando a mesma pessoa continuamente modifica um arquivo por um longo período de tempo (até 3 horas). A finalidade do log de eventos FileModifiedExtended é reduzir o número de eventos de FileModified que são registrados quando um arquivo é modificado continuamente. Isso ajuda a reduzir o ruído de vários registros de FileModified para o que é essencialmente a mesma atividade do usuário e permite que você se concentrar no evento FileModified inicial (e mais importante).  <br/> |
|Arquivo movido  <br/> |FileMoved  <br/> |Usuário move um documento de seu local atual em um site para um novo local.  <br/> |
|Reciclado, todas as versões secundárias do arquivo  <br/> |FileVersionsAllMinorsRecycled  <br/> |Usuário exclui todas as versões secundárias do histórico de versão de um arquivo. As versões excluídas são movidas para o Lixeira do site.  <br/> |
|Reciclado, todas as versões do arquivo  <br/> |FileVersionsAllRecycled  <br/> |Usuário exclui todas as versões do histórico de versão de um arquivo. As versões excluídas são movidas para o Lixeira do site.  <br/> |
|Versão reciclado do arquivo.  <br/> |FileVersionRecycled  <br/> |Usuário exclui uma versão do histórico de versão de um arquivo. A versão excluída será movida para a Lixeira do site.  <br/> |
|Arquivo renomeado  <br/> |FileRenamed  <br/> |Usuário renomeia um documento em um site.  <br/> |
|Arquivo restaurado  <br/> |FileRestored  <br/> |Usuário restaura um documento da Lixeira de um site.  <br/> |
|Arquivo carregado  <br/> |FileUploaded  <br/> |Usuário carrega um documento em uma pasta em um site.  <br/> |
|Página exibida  <br/> |PageViewed  <br/> |Usuário exibe uma página em um site. Isso não inclui usando um navegador da Web para exibir arquivos localizados em uma biblioteca de documentos.  <br/> |
|(nenhum)  <br/> |PageViewedExtended  <br/> |Isso está relacionado à "página exibido" atividade (PageViewed). Um evento PageViewedExtended é registrado quando a mesma pessoa continuamente exibe uma página da web por um longo período de tempo (até 3 horas). A finalidade do log de eventos PageViewedExtended é reduzir o número de eventos de PageViewed que são registrados quando uma página continuamente é exibida. Isso ajuda a reduzir o ruído de vários registros de PageViewed para o que é essencialmente a mesma atividade do usuário e permite que você se concentrar no evento PageViewed inicial (e mais importante).  <br/> |
  
### <a name="folder-activities"></a>Atividades de pasta
  
A tabela a seguir descreve as atividades de pasta no SharePoint Online e o OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Pasta copiada  <br/> |FolderCopied  <br/> |Usuário copia uma pasta de um site para outro local no SharePoint ou OneDrive for Business.  <br/> |
|Pasta criada  <br/> |FolderCreated  <br/> |Usuário cria uma pasta em um site.  <br/> |
|Pasta excluída  <br/> |FolderDeleted  <br/> |Usuário exclui uma pasta de um site.  <br/> |
|Pasta excluída da Lixeira  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Usuário exclui uma pasta da Lixeira em um site.  <br/> |
|Pasta excluída da Lixeira de segundo estágio  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Usuário exclui uma pasta da Lixeira de segundo estágio em um site.  <br/> |
|Pasta modificada  <br/> |FolderModified  <br/> |Usuário modifica uma pasta em um site. Isso inclui alterando os metadados de pasta, como a alteração de marcas e propriedades.  <br/> |
|Pasta movida  <br/> |FolderMoved  <br/> |Usuário move uma pasta em um local diferente em um site.  <br/> |
|Pasta renomeada  <br/> |FolderRenamed  <br/> |Usuário renomeia uma pasta em um site.  <br/> |
|Pasta restaurada  <br/> |FolderRestored  <br/> |Usuário restaura uma pasta excluída da Lixeira em um site.  <br/> |
  
### <a name="sharing-and-access-request-activities"></a>Atividades de solicitação de compartilhamento e acesso
  
A tabela a seguir descreve as compartilhamento e acesso solicitação atividades dos usuários no SharePoint Online e o OneDrive for Business. Para eventos de compartilhamento, a coluna de **detalhes** em **resultados da** identifica o nome do usuário ou grupo que o item foi compartilhado com e se esse usuário ou grupo é um membro ou convidado em sua organização. Para obter mais informações, consulte [Use compartilhamento auditorias no log de auditoria do Office 365](use-sharing-auditing.md).
  
> [!NOTE]
> Os usuários podem ser *membros* ou *convidados* com base na propriedade UserType do objeto de usuário. Membro é geralmente um funcionário e um convidado normalmente é um colaborador fora da sua organização. Quando um usuário aceita um convite de compartilhamento (e já não fizer parte de sua organização), uma conta de convidado é criada para eles no diretório da sua organização. Depois que o usuário convidado tiver uma conta em seu diretório, os recursos podem ser compartilhados diretamente com elas (sem exigir um convite). 
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Aceita a solicitação de acesso  <br/> |AccessRequestAccepted  <br/> |Uma solicitação de acesso a um site, uma pasta ou um documento foi aceita e o usuário solicitante recebeu acesso.  <br/> |
|Aceita o convite de compartilhamento  <br/> |SharingInvitationAccepted  <br/> |Usuário (membro ou convidado) aceita um convite de compartilhamento e concedeu acesso a um recurso. Esse evento inclui informações sobre o usuário convidado e o endereço de email que foi usado para aceitar o convite (eles poderia ser diferentes). Esta atividade geralmente vem acompanhada de um segundo evento que descreve como o usuário concedeu acesso ao recurso, por exemplo, adicione o usuário a um grupo que tenha acesso ao recurso.  <br/> |
|Nível de permissão adicionadas ao conjunto de sites  <br/> |PermissionLevelAdded  <br/> |Um nível de permissão foi adicionado a um conjunto de sites.  <br/> |
|Usuário adicionado a link seguro  <br/> |AddedToSecureLink  <br/> |Um usuário foi adicionado à lista de entidades que pode usar este link seguro de compartilhamento.  <br/> |
|Bloqueado o convite de compartilhamento  <br/> |SharingInvitationBlocked  <br/> | Um convite de compartilhamento enviado por um usuário em sua organização estiver bloqueado por conta de uma política de compartilhamento externa que permita ou nega compartilhamento externo com base no domínio do usuário de destino. Nesse caso, o convite de compartilhamento foi bloqueado, pois:<br/>  Domínio do usuário de destino não está incluído na lista de domínios permitidos.  <br/>  Ou  <br/>  Domínio do usuário de destino está incluído na lista de domínios bloqueados.  <br/>  Para obter mais informações sobre permitindo ou bloqueando compartilhamento externo com base em domínios, consulte [domínios restritos compartilhamento no SharePoint Online e o OneDrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Violou a herança de nível de permissão  <br/> |PermissionLevelsInheritanceBroken  <br/> |Um item foi alterado para que ele não é mais herda níveis de permissão de seu pai.  <br/> |
|Violou a herança de compartilhamento  <br/> |SharingInheritanceBroken  <br/> |Um item foi alterado para que ele não é mais herda permissões de compartilhamento de seu pai.  <br/> |
|Criou um link compartilhável da empresa  <br/> |CompanyLinkCreated  <br/> |Um link de toda a empresa para um recurso de criado pelo usuário. links de toda a empresa só pode ser usado pelos membros em sua organização. Eles não podem ser usados por convidados.  <br/> |
|Criou a solicitação de acesso  <br/> |AccessRequestCreated  <br/> |Usuário solicita acesso a um site, a pasta ou o documento não terem permissões para acessar.  <br/> |
|Criou um link anônimo  <br/> |AnonymousLinkCreated  <br/> |Um link anônimo a um recurso de criado pelo usuário. Qualquer pessoa com esse link pode acessar o recurso sem precisar ser autenticado.  <br/> |
|Criou um link seguro  <br/> |SecureLinkCreated  <br/> |Um link seguro de compartilhamento foi criado para esse item.  <br/> |
|Criado o convite de compartilhamento  <br/> |SharingInvitationCreated  <br/> |Usuário compartilhou um recurso no SharePoint Online ou OneDrive for Business com um usuário que não estiver no diretório da sua organização.  <br/> |
|Link seguro excluído  <br/> |SecureLinkDeleted  <br/> |Um link seguro de compartilhamento foi excluído.  <br/> |
|Negou a solicitação de acesso  <br/> |AccessRequestDenied  <br/> |Uma solicitação de acesso a um site, uma pasta ou um documento foi negada.  <br/> |
|Nível de permissão modificadas no conjunto de sites  <br/> |PermissionLevelModified  <br/> |Um nível de permissão foi alterado em um conjunto de sites.  <br/> |
|Removido um link compartilhável da empresa  <br/> |CompanyLinkRemoved  <br/> |Usuário removido um link de toda a empresa para um recurso. O link não possa mais ser usado para acessar o recurso.  <br/> |
|Removido um link anônimo  <br/> |AnonymousLinkRemoved  <br/> |Usuário removido um link anônimo a um recurso. O link não possa mais ser usado para acessar o recurso.  <br/> |
|Removido o nível de permissão do conjunto de sites  <br/> |PermissionLevelRemoved  <br/> |Um nível de permissão foi removido de um conjunto de sites.  <br/> |
|Restaurado compartilhamento herança  <br/> |SharingInheritanceReset  <br/> |Uma alteração foi feita para que um item herda as permissões de compartilhamento de seu pai.  <br/> |
|Arquivo compartilhado, pasta ou site  <br/> |SharingSet  <br/> |Usuário (membro ou convidado) compartilhadas um arquivo, pasta ou site no SharePoint ou OneDrive for Business com um usuário no diretório da sua organização. O valor na coluna **detalhes** para esta atividade identifica o nome do usuário com que o recurso foi compartilhado, e se esse usuário é um membro ou um convidado. Geralmente, essa atividade vem acompanhada de um segundo evento que descreve como o usuário concedeu acesso ao recurso; Por exemplo, adicione o usuário a um grupo que tenha acesso ao recurso.<br/> |
|Solicitação de acesso atualizados  <br/> |AccessRequestUpdated  <br/> |Uma solicitação de acesso a um item foi atualizada.  <br/> |
|Atualizado um link anônimo  <br/> |AnonymousLinkUpdated  <br/> |Usuário atualizado um link anônimo a um recurso. O campo atualizado está incluído na propriedade EventData ao exportar os resultados da pesquisa.  <br/> |
|Atualizado o convite de compartilhamento  <br/> |SharingInvitationUpdated  <br/> |Um convite de compartilhamento externo foi atualizado.  <br/> |
|Usado um link anônimo  <br/> |AnonymousLinkUsed  <br/> |Um usuário anônimo acessado um recurso usando um link anônimo. A identidade do usuário pode ser desconhecida, mas você pode obter outros detalhes como o endereço IP do usuário.  <br/> |
|Arquivo não compartilhado, pasta ou site  <br/> |SharingRevoked  <br/> |Usuário (membro ou convidado) descompartilhado um arquivo, pasta ou site previamente compartilhado com outro usuário.  <br/> |
|Usado um link compartilhável da empresa  <br/> |CompanyLinkUsed  <br/> |Usuário acessado um recurso usando um link de toda a empresa.  <br/> |
|Usado o link seguro  <br/> |SecureLinkUsed  <br/> |Um usuário usado um link seguro.  <br/> |
|Usuário adicionado a link seguro  <br/> |AddedToSecureLink  <br/> |Um usuário foi adicionado à lista de entidades que pode usar um link seguro de compartilhamento.  <br/> |
|Usuário removido do link seguro  <br/> |RemovedFromSecureLink  <br/> |Um usuário foi removido da lista de entidades que pode usar um link seguro de compartilhamento.  <br/> |
|Withdrew convite de compartilhamento  <br/> |SharingInvitationRevoked  <br/> |Usuário withdrew um convite de compartilhamento para um recurso.  <br/> |
  
### <a name="synchronization-activities"></a>Atividades de sincronização
  
A tabela a seguir lista as atividades de sincronização de arquivo no SharePoint Online e o OneDrive for Business.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Permissão de computador para sincronizar arquivos  <br/> |ManagedSyncClientAllowed  <br/> |Com êxito, o usuário estabelece uma relação de sincronização com um site. A relação de sincronização for bem-sucedida, porque o computador do usuário é um membro de um domínio que foi adicionado à lista de domínios (chamado de *lista de destinatários confiáveis* ) que pode acessar as bibliotecas de documentos em sua organização.<br/> Para obter mais informações sobre esse recurso, consulte [Use Windows PowerShell cmdlets para habilitar a sincronização do OneDrive para domínios que estão na lista de destinatários confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Bloqueado o computador de sincronização de arquivos  <br/> |UnmanagedSyncClientBlocked  <br/> |Usuário tentar estabelecer uma relação de sincronização com um site de um computador que não seja um membro do domínio da sua organização ou é um membro de um domínio que não foi adicionado à lista de domínios (chamado de *lista de destinatários confiáveis)* que pode acessar o documento bibliotecas em sua organização. A relação de sincronização não é permitida e o computador do usuário seja bloqueado para sincronização, baixando ou carregando arquivos em uma biblioteca de documentos.<br/> Para obter informações sobre esse recurso, consulte [Use Windows PowerShell cmdlets para habilitar a sincronização do OneDrive para domínios que estão na lista de destinatários confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Arquivos baixados para o computador  <br/> |FileSyncDownloadedFull  <br/> |Usuário estabelece uma relação de sincronização e com êxito baixa arquivos pela primeira vez em seus computadores em uma biblioteca de documentos.  <br/> |
|Arquivo baixado alterações no computador  <br/> |FileSyncDownloadedPartial  <br/> |Usuário com êxito downloads quaisquer alterações para arquivos de uma biblioteca de documentos. Essa atividade indica que quaisquer alterações feitas aos arquivos na biblioteca de documentos foram baixadas para o computador do usuário. Somente as alterações que foram baixadas porque a biblioteca de documentos foi baixada anteriormente pelo usuário (conforme indicado pela atividade **baixou os arquivos para o computador** ).<br/> |
|Arquivos carregados para a biblioteca de documentos  <br/> |FileSyncUploadedFull  <br/> |Usuário estabelece uma relação de sincronização e carrega com êxito os arquivos pela primeira vez a partir de seus computadores em uma biblioteca de documentos.  <br/> |
|Arquivo carregado alterações à biblioteca de documentos  <br/> |FileSyncUploadedPartial  <br/> |Com êxito, o usuário carrega as alterações em arquivos de uma biblioteca de documentos. Esse evento indica que quaisquer alterações feitas a versão local de um arquivo de uma biblioteca de documentos sejam carregadas com êxito a biblioteca de documentos. Somente as alterações são descarregadas porque esses arquivos foram carregados anteriormente pelo usuário (conforme indicado pelo * * arquivos carregados para a biblioteca de documentos * * atividade).  <br/> |
  
### <a name="site-administration-activities"></a>Atividades de administração de site
  
A tabela a seguir lista os eventos que resultam de tarefas de administração do site do SharePoint Online.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionado o agente de usuários isentos  <br/> |ExemptUserAgentSet  <br/> |Um administrador global ou o SharePoint adiciona um agente de usuário à lista de agentes de usuários isentos no Centro de administração do SharePoint.  <br/> |
|Administrador do conjunto de sites adicionados  <br/> |SiteCollectionAdminAdded  <br/> |Administrador de conjunto de sites ou proprietário adiciona uma pessoa como um administrador de conjunto de sites para um site. Os administradores de conjunto de sites tem permissões de controle total para o conjunto de sites e todos os subsites.  <br/> |
|Adicionados pelo usuário ou grupo ao grupo do SharePoint  <br/> |AddedToGroup  <br/> |Usuário adicionado a um membro ou convidado a um grupo do SharePoint. Isso pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento de compartilhamento.  <br/> |
|Permissão de usuário criar grupos  <br/> |AllowGroupCreationSet  <br/> |Administrador de site ou proprietário adiciona um nível de permissão a um site que permite que um usuário atribuído a essa permissão para criar um grupo para esse site.  <br/> |
|Mover sites cancelado geo  <br/> |SiteGeoMoveCancelled  <br/> |Um administrador global ou o SharePoint com êxito cancela uma lista do SharePoint ou OneDrive site geo mover. O recurso de Multi-Geo permite que uma organização do Office 365 abranger várias regiões de datacenter para Office 365, que são chamados geos. Para obter mais informações, consulte [Os recursos de Multi-Geo no OneDrive e SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Alterado uma política de compartilhamento  <br/> |SharingPolicyChanged  <br/> |Um administrador global ou o SharePoint alterado a uma lista do SharePoint a política de compartilhamento usando o portal de administração do Office 365, portal de administração do SharePoint ou o Shell de gerenciamento do SharePoint Online. Qualquer alteração nas configurações na política de compartilhamento em sua organização será registrada. A política que foi alterada é identificada no campo **ModifiedProperties** nas propriedades detalhadas do registro do evento.<br/> |
|Alterado a política de acesso de dispositivo  <br/> |DeviceAccessPolicyChanged  <br/> |Um administrador global ou SharePoint alterou a diretiva de dispositivos não gerenciados para sua organização. Essa diretiva controla o acesso ao SharePoint, o OneDrive e o Office 365 de dispositivos que não estão associadas à sua organização. Configurar essa diretiva exige uma empresa mobilidade + a assinatura de segurança. Para obter mais informações, consulte [controlar o acesso de dispositivos não gerenciados](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).<br/> |
|Agentes de usuários isentos alterados  <br/> |CustomizeExemptUsers  <br/> |Um administrador global ou SharePoint personalizados a lista de agentes de usuários isentos no Centro de administração do SharePoint. Você pode especificar quais agentes de usuário para isentos de recebimento de uma página da web inteira ao índice. Isso significa que quando um agente de usuário que você tiver especificado como isentos encontrar um formulário do InfoPath, o formulário será retornado como um arquivo XML, em vez de uma página da web inteira. Isso torna mais rápido a indexação formulários do InfoPath.  <br/> |
|Alterado a política de acesso de rede  <br/> |NetworkAccessPolicyChanged  <br/> |Um administrador global ou SharePoint alterado a política de acesso baseado no local (também chamada de um limite de rede de perímetro) no Centro de administração do SharePoint ou usando o PowerShell do SharePoint Online. Esse tipo de política controla quem pode acessar os recursos do SharePoint e OneDrive na sua organização com base em autorizado intervalos de endereços IP que você especificar. Para obter mais informações, consulte [controlar o acesso ao SharePoint Online e dados de OneDrive com base no local de rede](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).<br/> |
|Mover sites concluído geo  <br/> |SiteGeoMoveCompleted  <br/> |Uma movimentação de geo do site que foi agendada por um administrador global na sua organização foi concluída com êxito. O recurso de Multi-Geo permite que uma organização do Office 365 abranger várias regiões de datacenter para Office 365, que são chamados geos. Para obter mais informações, consulte [Os recursos de Multi-Geo no OneDrive e SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Grupo criado  <br/> |GroupAdded  <br/> |Administrador de site ou proprietário cria um grupo para um site ou executa uma tarefa que resulte em um grupo que está sendo criado. Por exemplo, na primeira vez que um usuário cria um link para compartilhar um arquivo, um grupo de sistema é adicionado ao OneDrive do usuário para o site de negócios. Esse evento também pode ser um resultado de um usuário criar um vínculo com editar permissões para um arquivo compartilhado.  <br/> |
|Criado enviado para conexão  <br/> |SendToConnectionAdded  <br/> |Um administrador global ou o SharePoint cria uma nova conexão Enviar para, na página de gerenciamento de registros no Centro de administração do SharePoint. Uma conexão Enviar para especifica configurações para um repositório de documentos ou uma central de registros. Quando você cria uma conexão Enviar para, um organizador de conteúdo podem enviar documentos para o local especificado.  <br/> |
|Conjunto de sites criados  <br/> |SiteCollectionCreated  <br/> |Um administrador global ou o SharePoint cria um novo conjunto de sites em sua organização do SharePoint Online ou um usuário provisiona seu OneDrive para o site de negócios.  <br/> |
|Grupo excluído  <br/> |GroupRemoved  <br/> |Usuário exclui um grupo de um site.  <br/> |
|Excluído enviado para conexão  <br/> |SendToConnectionRemoved  <br/> |Um administrador global ou SharePoint exclui uma conexão Enviar para, na página de gerenciamento de registros no Centro de administração do SharePoint.  <br/> |
|Site excluído  <br/> |SiteDeleted  <br/> |Administrador de site exclui um site.  <br/> |
|Habilitado a visualização do documento  <br/> |PreviewModeEnabledSet  <br/> |Administrador do site permite a visualização de documentos para um site.  <br/> |
|Habilitado para o fluxo de trabalho herdado  <br/> |LegacyWorkflowEnabledSet  <br/> |O administrador ou proprietário do site adiciona o tipo de conteúdo Tarefa de fluxo de trabalho do SharePoint 2013 ao site. Os administradores globais também podem ativar fluxos de trabalho para toda a organização no Centro de Administração do SharePoint.  <br/> |
|Habilitado o Office on Demand  <br/> |OfficeOnDemandSet  <br/> |Administrador do site permite que o Office on Demand, que permite ao usuário acessar a versão mais recente dos aplicativos de área de trabalho do Office. O Office on Demand está habilitado no Centro de administração do SharePoint e requer uma assinatura do Office 365 que inclui os aplicativos do Office completos, instalados.  <br/> |
|Enabled RSS feeds  <br/> |NewsFeedEnabledSet  <br/> |Administrador de site ou proprietário habilita feeds RSS para um site. Os administradores globais podem habilitar RSS feeds para toda a organização no Centro de administração do SharePoint.  <br/> |
|A definição de solicitação de acesso modificado  <br/> |WebRequestAccessModified  <br/> |As configurações de solicitação de acesso foram modificadas em um site.  <br/> |
|Configuração de membros podem compartilhar modificada  <br/> |WebMembersCanShareModified  <br/> |A configuração de **Membros podem compartilhar** foi modificada em um site.  <br/> |
|Permissões de site modificada  <br/> |SitePermissionsModified  <br/> |Administrador de sites ou proprietário (ou a conta do sistema) altera o nível de permissão que são atribuídos a um grupo em um site. Esta atividade é registrada também se todas as permissões forem removidas de um grupo.<br/> > [!NOTE]> Essa operação foi preterida no SharePoint Online. Para localizar os eventos relacionados, você pode procurar por outras atividades relacionadas a permissão como **administrador do conjunto de sites foi adicionado**, **foram adicionados usuário ou grupo ao grupo do SharePoint**, **usuário permitidos para criar grupos**, **grupo criado**e **Deleted grupo.**         |
|Removido o usuário ou grupo do grupo do SharePoint  <br/> |RemovedFromGroup  <br/> |Usuário removido um membro ou convidado de um grupo do SharePoint. Isso pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento descompartilhando.  <br/> |
|Site renomeado  <br/> |SiteRenamed  <br/> |Administrador de site ou proprietário renomeia um site  <br/> |
|Permissões de administrador do site solicitado  <br/> |SiteAdminChangeRequest  <br/> |Solicitações de usuário a ser adicionado como um administrador de conjunto de sites para um conjunto de sites. Os administradores de conjunto de sites tem permissões de controle total para o conjunto de sites e todos os subsites.  <br/> |
|Mover sites agendada geo  <br/> |SiteGeoMoveScheduled  <br/> |Um administrador global ou SharePoint agenda com êxito uma lista do SharePoint ou OneDrive site geo mover. O recurso de Multi-Geo permite que uma organização do Office 365 abranger várias regiões de datacenter para Office 365, que são chamados geos. Para obter mais informações, consulte [Os recursos de Multi-Geo no OneDrive e SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Conjunto de sites de host  <br/> |HostSiteSet  <br/> |Um administrador global ou SharePoint altera o local designado para hospedar pessoal ou OneDrive para sites corporativos.  <br/> |
|Grupo atualizado  <br/> |GroupUpdated  <br/> |Administrador de site ou proprietário altera as configurações de um grupo para um site. Isso pode incluir alterando o nome do grupo, que pode exibir ou editar a associação de grupo e como as solicitações de associação são manipuladas.  <br/> |
  
### <a name="exchange-mailbox-activities"></a>Atividades de caixa de correio do Exchange
  
A tabela a seguir lista as atividades que podem ser registradas por caixa de correio do log de auditoria. Atividades de caixa de correio realizadas por um administrador, um usuário delegado ou o proprietário da caixa de correio são registradas. Por padrão, a auditoria de caixa de correio no Office 365 não está ativado. Auditoria de caixa de correio log deve ser ativado para cada caixa de correio antes de atividade de caixa de correio será registrada. Para obter mais informações, consulte [Habilitar caixa de correio auditorias no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Permissões de caixa de correio de representante adicionado  <br/> |Adicionar-MailboxPermission  <br/> |Um administrador atribuído a permissão de caixa de correio de FullAccess a um usuário (conhecido como um representante) à caixa de correio de outra pessoa. A permissão FullAccess permite ao delegado abrir a caixa de correio da outra pessoa e ler e gerenciar o conteúdo da caixa de correio.  <br/> |
|Mensagens copiadas para outra pasta  <br/> |Copiar  <br/> |Uma mensagem foi copiada a outra pasta.  <br/> |
|Item de caixa de correio criada  <br/> |Criar  <br/> |Um item é criado na pasta Calendário, contatos, anotações ou tarefas na caixa de correio; Por exemplo, uma nova solicitação de reunião é criada. Observe que a criação, enviando ou recebendo uma mensagem não sofre auditoria. Além disso, não é auditado criando uma pasta de caixa de correio.  <br/> |
|Mensagens excluídas da pasta Itens excluídos  <br/> |SoftDelete  <br/> |Uma mensagem foi permanentemente excluída ou excluída da pasta Itens excluídos. Estes itens são movidos para a pasta itens recuperáveis. As mensagens também são movidas para a pasta itens recuperáveis quando o usuário seleciona e pressiona **Shift + Delete**.<br/> |
|Movido mensagens para outra pasta  <br/> |Move  <br/> |Uma mensagem foi movida para outra pasta.  <br/> |
|Movido mensagens para a pasta Itens excluídos  <br/> |MoveToDeletedItems  <br/> |Uma mensagem foi excluída e movida para a pasta Itens Excluídos.  <br/> |
|Permissão de pasta modificada  <br/> |UpdateFolderPermissions  <br/> |Uma permissão de pasta foi alterada. Controle de permissões de pasta quais usuários em sua organização podem acessar pastas de caixa de correio e as mensagens na pasta.  <br/> |
|Mensagens limpas da caixa de correio  <br/> |HardDelete  <br/> |Uma mensagem foi removida da pasta itens recuperáveis (permanentemente excluída da caixa de correio).  <br/> |
|Permissões de caixa de correio de representante removidos  <br/> |Remove-MailboxPermission  <br/> |Um administrador removido a permissão FullAccess (o que foi atribuída a um representante) da caixa de correio de uma pessoa. Depois que a permissão FullAccess for removida, o representante não é possível abrir a caixa de correio da outra pessoa ou acessar nenhum conteúdo nela.  <br/> |
|Enviada usando permissões Enviar como de mensagem  <br/> |SendAs  <br/> |Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem apesar de ter vindo do proprietário da caixa de correio.  <br/> |
|Enviada usando permissões Enviar em nome de mensagem  <br/> |SendOnBehalf  <br/> |Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem na verdade enviou a mensagem.  <br/> |
|Acesso de representante atualizado para a pasta de calendário  <br/> |UpdateCalendarDelegation  <br/> |Uma representação de calendário foi atribuída a uma caixa de correio. Delegação de calendário oferece a outra pessoa nas mesmas permissões de organização para gerenciar o calendário do proprietário da caixa de correio.  <br/> |
|Mensagem atualizada  <br/> |Atualizar  <br/> |Uma mensagem ou suas propriedades foram alteradas.  <br/> |
|Usuário se conectou à caixa de correio  <br/> |MailboxLogin  <br/> |O usuário entrou em sua caixa de correio.  <br/> |
|(nenhum)  <br/> |UpdateInboxRules  <br/> |Uma regra de caixa de correio foram adicionada, removida ou alterada. Regras de caixa de entrada são usadas para processar mensagens na caixa de entrada do usuário com base nas condições especificadas e execute as ações quando as condições de uma regra são atendidas, como mover uma mensagem para uma pasta especificada ou exclusão de uma mensagem.<br/> Para retornar as entradas para atividades de regra de caixa de entrada, você precisará selecionar **Mostrar resultados para todas as atividades** na lista de **atividades** . Use as caixas de intervalo de data e a lista de **usuários** para restringir os resultados da pesquisa.<br/> |
  
### <a name="sway-activities"></a>Atividades de sway
  
A tabela a seguir lista as atividades de administrador e usuário em Sway. Sway é um aplicativo do Office 365 que ajuda os usuários a coletar, formatar e compartilhar ideias, histórias e apresentações em uma tela de interativa, baseado na web. Para obter mais informações, consulte [Perguntas frequentes sobre Sway - ajuda de Admin](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Nível de compartilhamento de Sway alterado  <br/> |SwayChangeShareLevel  <br/> |Usuário altera o nível de compartilhamento de um Sway. Esse evento captura o usuário alterar o escopo de compartilhamento associado a um Sway; Por exemplo, público versus dentro da organização.  <br/> |
|Sway criado  <br/> |SwayCreate  <br/> |Usuário cria um Sway.  <br/> |
|Sway excluído  <br/> |SwayDelete  <br/> |Usuário exclui um Sway.  <br/> |
|Duplicação de Sway desabilitada  <br/> |SwayDisableDuplication  <br/> |Usuário desabilita a duplicação de um Sway.  <br/> |
|Sway duplicado  <br/> |SwayDuplicate  <br/> |Usuário duplica um Sway.  <br/> |
|Sway editada  <br/> |SwayEdit  <br/> |Usuário edita um Sway.  <br/> |
|Duplicação de Sway habilitada  <br/> |EnableDuplication  <br/> |Usuário permite que a duplicação de um Sway; a capacidade de um usuário para permitir a duplicação de um Sway é habilitada por padrão.  <br/> |
|Compartilhamento de Sway revogadas  <br/> |SwayRevokeShare  <br/> |Usuário interrompe o compartilhamento de um Sway por revogar acesso a ele. Revogação de acesso altera os links associados a um Sway.  <br/> |
|Sway compartilhado  <br/> |SwayShare  <br/> |Usuário pretende compartilhar um Sway. Esse evento captura a ação do usuário clicar em um destino de compartilhamento específicos dentro do menu de compartilhamento de Sway. O evento não indica se o usuário foi concluída a ação de compartilhamento.  <br/> |
|Desativado o compartilhamento externo de Sway  <br/> |SwayExternalSharingOff  <br/> |Administrador desabilita Sway compartilhamento externo para toda a organização usando o Centro de administração do Office 365.  <br/> |
|Ativado o compartilhamento externo de Sway  <br/> |SwayExternalSharingOn  <br/> |Administrador habilita Sway compartilhamento externo para toda a organização usando o Centro de administração do Office 365.  <br/> |
|Desativado o serviço de Sway  <br/> |SwayServiceOff  <br/> |Administrador desabilita Sway para toda a organização usando o Centro de administração do Office 365.  <br/> |
|Ativado o serviço de Sway  <br/> |SwayServiceOn  <br/> |Administrador habilita Sway para toda a organização usando o Centro de administração do Office 365 (Sway serviço está habilitado por padrão).  <br/> |
|Sway visualizado  <br/> |SwayView  <br/> |Usuário exibe um Sway.  <br/> |

  
### <a name="user-administration-activities"></a>Atividades de administração do usuário
  
A tabela a seguir lista as atividades de administração do usuário que são registradas quando um administrador adiciona ou altera uma conta de usuário usando o Centro de administração do Office 365 ou o portal de gerenciamento do Windows Azure.
  
|**Atividade**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionados pelo usuário  <br/> |Adicionar usuário  <br/> |Uma conta de usuário do Office 365 foi criada.  <br/> |
|Licença de usuário alterados  <br/> |Licença de usuário de alteração  <br/> |A licença atribuída a um usuário o que foi alterado. Para ver quais licenças foram alterações, consulte a atividade do **usuário atualizado** correspondente.<br/> |
|Senha do usuário alterados  <br/> |Alterar a senha do usuário  <br/> |Administrador alterou a senha a senha de um usuário.  <br/> |
|Usuário excluído  <br/> |Excluir o usuário  <br/> |Uma conta de usuário do Office 365 foi excluída.  <br/> |
|Redefinir senha de usuário  <br/> |Redefinir senha de usuário  <br/> |Administrador redefinir a senha de um usuário.  <br/> |
|Definir a propriedade que força o usuário a alteração de senha  <br/> |Force set alterar senha do usuário  <br/> |Administrador defina a propriedade que força o usuário a alterar sua senha na próxima vez que o usuário entrar para o Office 365.  <br/> |
|Definir propriedades de licença  <br/> |Definir propriedades de licença  <br/> |Administrador modifica as propriedades de licenciada atribuída a um usuário.  <br/> |
|Usuário atualizada  <br/> |Usuário de atualização  <br/> |O administrador altera uma ou mais propriedades de uma conta de usuário. Para obter uma lista das propriedades do usuário que pode ser atualizada, consulte a seção "Atualizar atributos do usuário" [Eventos de relatório de auditoria do Active Directory do Windows Azure](https://go.microsoft.com/fwlink/p/?LinkID=616549).<br/> |
  
### <a name="azure-ad-group-administration-activities"></a>Atividades de administração de grupo do Windows Azure AD
  
A tabela a seguir lista as atividades de administração de grupo que são registradas quando um administrador ou um usuário cria ou altera um grupo do Office 365 ou quando um administrador cria um grupo de segurança por meio do Centro de administração do Office 365 ou o portal de gerenciamento do Windows Azure. Para obter mais informações sobre grupos no Office 365, consulte [Exibir, criar e excluir grupos no Centro de administração do Office 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Grupo adicionado  <br/> |Adicionar um grupo  <br/> |Um grupo foi criado.  <br/> |
|Membro adicionado ao grupo  <br/> |Adicionar um membro ao grupo  <br/> |Um membro foi adicionado a um grupo.  <br/> |
|Grupo excluído  <br/> |Excluir grupo  <br/> |Um grupo foi excluído.  <br/> |
|Removidos membro do grupo  <br/> |Remover um membro do grupo  <br/> |Um membro foi removido de um grupo.  <br/> |
|Grupo atualizado  <br/> |Grupo de atualização  <br/> |Uma propriedade de um grupo foi alterada.  <br/> |
   
### <a name="application-administration-activities"></a>Atividades de administração do aplicativo
  
A tabela a seguir lista as atividades de admin do aplicativo que são registradas quando um administrador adiciona ou altera um aplicativo que está registrado no Azure AD. Qualquer aplicativo que depende do Azure AD para autenticação deve ser registrado no diretório.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Entrada de delegação adicionados  <br/> |Adicionar entrada de delegação  <br/> |Uma permissão de autenticação foi criado/concedido a um aplicativo no Azure AD.  <br/> |
|Entidade de serviço adicionado  <br/> |Adicionar a entidade de serviço  <br/> |Um aplicativo foi registrado no Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.  <br/> |
|Credenciais adicionadas a uma entidade de serviço  <br/> |Adicionar credenciais de serviço principal  <br/> |Credenciais foram adicionadas a um serviço principal no Azure AD. Um princípio de serviço representa um aplicativo no diretório.  <br/> |
|Entrada de delegação removidos  <br/> |Remover a entrada de delegação  <br/> |Uma permissão de autenticação foi removida de um aplicativo no Azure AD.  <br/> |
|Removido de uma entidade de serviço do diretório  <br/> |Remover a entidade de serviço  <br/> |Um aplicativo foi excluído/não registrada do Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.  <br/> |
|Removidos credenciais a partir de um serviço principal  <br/> |Remover credenciais de serviço principal  <br/> |Credenciais foram removidas de um serviço principal no Azure AD. Um princípio de serviço representa um aplicativo no diretório.  <br/> |
|Entrada de delegação do conjunto  <br/> |Entrada de delegação do conjunto  <br/> |Uma permissão de autenticação foi atualizado para um aplicativo no Azure AD.  <br/> |

### <a name="role-administration-activities"></a>Atividades de administração de função
  
A tabela a seguir lista as atividades de administração de função do Azure AD registrados quando um administrador gerencia as funções de administrador no Centro de administração do Office 365 ou no portal de gerenciamento do Windows Azure.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Adicionar membro à função  <br/> |Adicionar um membro da função à função  <br/> |Adicionado um usuário a uma função de administrador no Office 365.  <br/> |
|Removido de um usuário de uma função de diretório  <br/> |Remova a função de membro da função  <br/> |Removida a um usuário a partir de uma função de administrador no Office 365.  <br/> |
|Definir informações de contato de empresa  <br/> |Definir informações de contato de empresa  <br/> |Atualizadas as preferências de contato de nível de empresa para sua organização do Office 365. Isso inclui os endereços de email para email relacionados à assinatura enviada pelo Office 365, bem como notificações técnicas sobre serviços do Office 365.  <br/> |
   
### <a name="directory-administration-activities"></a>Atividades de administração de diretório
  
A seguinte tabela lista Azure AD diretório e domínio relacionados atividades que são registradas quando um administrador gerencia suas organizações do Office 365 no Centro de administração do Office 365 ou no portal de gerenciamento do Windows Azure.
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Domínio adicionado à empresa  <br/> |Adicionar domínio à empresa  <br/> |Adicionando um domínio à sua organização do Office 365.  <br/> |
|Adicionado um parceiro para o diretório  <br/> |Adicionar parceiro para empresa  <br/> |Adicionado um parceiro (administrador delegado) à sua organização do Office 365.  <br/> |
|Domínio removido da empresa  <br/> |Remover o domínio da empresa  <br/> |Um domínio foi removido da sua organização do Office 365.  <br/> |
|Removido de um parceiro do diretório  <br/> |Remover o parceiro da empresa  <br/> |Removido um parceiro (administrador delegado) da sua organização do Office 365.  <br/> |
|Definir informações da empresa  <br/> |Definir informações da empresa  <br/> |Atualizadas as informações da empresa para sua organização do Office 365. Isso inclui os endereços de email para email relacionados à assinatura enviada pelo Office 365, bem como notificações técnicas sobre serviços do Office 365.  <br/> |
|Definir a autenticação de domínio  <br/> |Definir a autenticação de domínio  <br/> |Alterado a configuração de autenticação de domínio para sua organização do Office 365.  <br/> |
|Atualizadas as configurações de federação para um domínio  <br/> |Definir configurações de federação no domínio  <br/> |Alteradas as configurações de Federação (compartilhamento externo) para sua organização do Office 365.  <br/> |
|Política de conjunto de senha  <br/> |Política de conjunto de senha  <br/> |Alteradas as restrições de tamanho e caractere de senhas de usuário em sua organização do Office 365.  <br/> |
|Ativado a sincronização do Azure AD  <br/> |Definir o sinalizador de DirSyncEnabled na empresa  <br/> |Defina a propriedade que habilita um diretório para a sincronização do Azure AD.  <br/> |
|Domínio atualizado  <br/> |Domínio de atualização  <br/> |Atualizadas as configurações de um domínio em sua organização do Office 365.  <br/> |
|Domínio verificado  <br/> |Verifique se o domínio  <br/> |Verificado se a sua organização é o proprietário de um domínio.  <br/> |
|Domínio de email verificado verificado  <br/> |Verifique se o domínio verificado de email  <br/> |Verificação de email usado para verificar se a sua organização é o proprietário de um domínio.  <br/> |
   
### <a name="ediscovery-activities"></a>atividades de descoberta eletrônica
  
Pesquisa e atividades relacionadas a descoberta eletrônica que são executadas na segurança do Office 365 conteúdo &amp; Centro de conformidade ou executando o Windows PowerShell correspondente cmdlets são registrados no log de auditoria do Office 365. Isso inclui as seguintes atividades:
  
- Criando e gerenciando casos de eDiscovery
    
- Criando, iniciar e editando pesquisas de conteúdo
    
- Realizando ações de pesquisa de conteúdo, como visualizar, exportação e exclusão de resultados da pesquisa
    
- Configurar permissões de filtragem para a pesquisa de conteúdo
    
- Gerenciando a função de administrador de descoberta eletrônica
    
Para uma lista e uma descrição detalhada das atividades de descoberta eletrônica que são registrados, consulte [Search para atividades de descoberta eletrônica no Office 365 log de auditoria](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Leva até 30 minutos de eventos que resultam de atividades listadas em **atividades de descoberta eletrônica** na lista suspensa de **atividades** a serem exibidos nos resultados da pesquisa. Por outro lado, que leva até 24 horas para os eventos correspondentes do eDiscovery atividades de cmdlet apareça nos resultados da pesquisa. 
  
### <a name="power-bi-activities"></a>Atividades do Power BI
  
A tabela a seguir lista as atividades de admin no Power BI que são registradas no log de auditoria do Office 365 e de usuário.
  
 **Importante:** Log de auditoria para Power BI não está habilitado por padrão. Para procurar atividades Power BI no log de auditoria do Office 365, você precisa habilitar a auditoria no portal de administração do Power BI. Para obter instruções, consulte [Power BI de auditoria](https://docs.microsoft.com/power-bi/service-admin-auditing#enabling-auditing-functionality-in-the-power-bi-admin-portal).
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Membros do grupo Power BI adicionados  <br/> |AddGroupMembers  <br/> |Um membro é adicionado a um espaço de trabalho de grupo do Power BI.  <br/> |
|Conjunto de dados analisado Power BI  <br/> |AnalyzedByExternalApplication  <br/> |Um conjunto de dados é analisado por um aplicativo externo.  <br/> |
|Painel criado do Power BI  <br/> |CreateDashboard  <br/> |Um novo painel é criado.  <br/> |
|Grupo criado do Power BI  <br/> |CreateGroup  <br/> |Um grupo é criado.  <br/> |
|Criado organizacional pacote de conteúdo do Power BI  <br/> |CreateOrgApp  <br/> |Um pacote de conteúdo organizacional é criado.  <br/> |
|Painel excluído do Power BI  <br/> |DeleteDashboard  <br/> |Um painel é excluído.  <br/> |
|Conjunto de dados excluído Power BI  <br/> |DeleteDataset  <br/> |Um conjunto de dados é excluído.  <br/> |
|Relatório excluído do Power BI  <br/> |DeleteReport  <br/> |Um relatório é excluído.  <br/> |
|Relatório baixado do Power BI  <br/> |DownloadReport  <br/> |Um usuário baixa um relatório do Power BI do serviço de seus computadores.  <br/> |
|Painel editada do Power BI  <br/> |EditDashboard  <br/> |Um painel é renomeado.  <br/> |
|Dados exportados da visuais de relatório do Power BI  <br/> |ExportReport  <br/> |Dados são exportados a partir de um bloco de relatório.  <br/> |
|Dados exportados de blocos Power BI  <br/> |ExportTile  <br/> |Dados são exportados de um lado do painel.  <br/> |
|Painel do Power BI impressa  <br/> |PrintDashboard  <br/> |Um painel é impressa.  <br/> |
|Página de relatório impressa Power BI  <br/> |PrintReport  <br/> |Um relatório é impresso.  <br/> |
|Relatório do Power BI publicado web  <br/> |PublishToWebReport  <br/> |Um relatório é publicado na Web.  <br/> |
|Painel compartilhado do Power BI  <br/> |ShareDashboard  <br/> |Um painel é compartilhado.  <br/> |
|Avaliação do Power BI Introdução  <br/> |OptInForProTrial  <br/> |Um usuário inicia uma assinatura de avaliação para profissionais Power BI.  <br/> |
|Configurações do Power BI da organização atualizados  <br/> |UpdatedAdminFeatureSwitch  <br/> |Um administrador alterado uma definição organizacional no portal de administração do Power BI.  <br/> |
|Painel visualizado do Power BI  <br/> |ViewDashboard  <br/> |Um painel é exibido.  <br/> |
|Relatório exibido do Power BI  <br/> |ViewReport  <br/> |Um relatório é visualizado.  <br/> |
  
### <a name="microsoft-teams-activities"></a>Atividades de Teams da Microsoft
  
A tabela a seguir lista o usuário e o log de auditoria de atividades de administração no Microsoft Teams que são registrados no Office 365. Teams da Microsoft é um espaço de trabalho centralizada de bate-papo no Office 365. Ele reúne as conversas de uma equipe, reuniões, arquivos e anotações em um único lugar. Para obter mais informações e links para tópicos da Ajuda, consulte:
  
- [Perguntas frequentes sobre o Microsoft Teams - ajuda de Admin](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Ajuda do Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Bot adicionado à equipe  <br/> |BotAddedToTeam  <br/> |Um usuário adiciona um bot para uma equipe.  <br/> |
|Adicionado de canal  <br/> |ChannelAdded  <br/> |Um usuário adiciona um canal para uma equipe.  <br/> |
|Conector adicionado  <br/> |ConnectorAdded  <br/> |Um usuário adiciona um conector a um canal.  <br/> |
|Adicionado membros da equipe  <br/> |MemberAdded  <br/> |Um proprietário de equipe adiciona membro (s) para uma equipe.  <br/> |
|Guia adicionado  <br/> |TabAdded  <br/> |Um usuário adiciona um tab a um canal.  <br/> |
|Alterado a configuração de canal  <br/> |ChannelSettingChanged  <br/> | A operação ChannelSettingChanged é registrada quando as seguintes atividades são realizadas por um membro da equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada na parêntese abaixo) é exibida na coluna **Item** nos resultados da pesquisa de log de auditoria.<br/> <br/>-Altera o nome de um canal de equipe ( **nome de canal**).  <br/>  <br/>-Altera a descrição de um canal de equipe ( **Descrição do canal**).  <br/> |
|Alterado a configuração da organização  <br/> |TeamsTenantSettingChanged  <br/> | A operação TeamsTenantSettingChanged é registrada quando as seguintes atividades são realizadas por um administrador global (usando o Centro de administração do Office 365); Observe que essas atividades afetam as configurações do Microsoft Teams toda a organização. Para obter mais informações, consulte [configurações de administrador para equipes da Microsoft](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).<br/>  Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada na parêntese abaixo) é exibida na coluna **Item** nos resultados da pesquisa de log de auditoria.  <br/><br/>-Habilita ou desabilita o Teams da Microsoft para a organização ( **As equipes da Microsoft**).  <br/><br/>-Habilita ou desabilita a interoperabilidade entre o Microsoft Teams e Skype for Business para a organização ( **Skype para a interoperabilidade de negócios**).<br/><br/>-Habilita ou desabilita o modo de exibição de organograma nos clientes do Microsoft Teams ( **modo de exibição de gráfico de organização**).  <br/><br/>-Habilita ou desabilita a capacidade dos membros da equipe agendar reuniões privadas ( **agendamento de reunião particular**).  <br/><br/>-Habilita ou desabilita a capacidade dos membros da equipe agendar reuniões de canal ( **canal agendamento de reuniões**).  <br/><br/>-Habilita ou desabilita a chamar vídeo em equipes nas reuniões ( **vídeo para reuniões do Skype**).  <br/><br/>-Habilita ou desabilita a tela de compartilhamento do meetups Teams da Microsoft para a organização ( **compartilhamento de tela para reuniões do Skype**).  <br/><br/>-Habilita ou desabilita a essa capacidade de adicionar imagens animadas (chamadas Giphys) para conversas de equipes ( **animado imagens**).  <br/><br/>-Altera o configuração para a organização ( **classificação de conteúdo**) de classificação do conteúdo. A classificação de conteúdo restringe o tipo de imagem animada que pode ser exibido em conversas.<br/><br/>-Habilita ou desabilita a capacidade de adicionar imagens personalizáveis (chamadas memes personalizado) membros da equipe da Internet para conversas de equipe ( **personalizáveis imagens da Internet**).  <br/><br/>-Habilita ou desabilita a capacidade dos membros da equipe adicionar imagens editáveis (chamadas adesivos) para conversas de equipe ( **imagens editáveis**).<br/><br/>-Habilita ou desabilita que permita a membros da equipe usar bots no Microsoft Teams chats e canais ( **bots de toda a organização**).<br/><br/>-Permite bots específicos for Microsoft Teams; Isso não inclui o T-Bot, que é um bot de ajuda as equipes que está disponível quando bots estão habilitados para a organização ( **bots individuais**).  <br/><br/>-Habilita ou desabilita a capacidade dos membros da equipe adicionar extensões ou guias ( **extensões ou guias**).  <br/><br/>-Habilita ou desabilita o carregamento de lado de Bots proprietários for Microsoft Teams ( **carregamento do lado do Bots**).  <br/><br/>-Habilita ou desabilita a capacidade dos usuários enviar emails a um canal de Teams da Microsoft ( **email de canal**).  <br/> |
|Função alterada de membros da equipe  <br/> |MemberRoleChanged  <br/> |Um proprietário de equipe altera a função de membro (s) em uma equipe. Os valores a seguir indicam o tipo de função atribuído ao usuário.<br/><br/><br/> **1** - indica a função de proprietário.<br/>**2** - indica a função de membro. <br/>**3** - indica a função de convidado. <br/>A propriedade Members também inclui o nome da sua organização e o endereço de email do membro.  <br/> |
|Alterado a configuração de equipe  <br/> |TeamSettingChanged  <br/> | A operação TeamSettingChanged é registrada quando as seguintes atividades são realizadas por um proprietário de equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada na parêntese abaixo) é exibida na coluna **Item** nos resultados da pesquisa de log de auditoria.<br/><br/>-Altera o tipo de acesso para uma equipe. As equipes podem ser definido como particular ou público ( **tipo de acesso equipe**). Quando uma equipe é particular (a configuração padrão), os usuários podem acessar a equipe somente por convite. Quando uma equipe é pública, é detectável por qualquer pessoa.<br/><br/>-Altera a classificação de informações de uma equipe ( **classificação da equipe**).  <br/>  Por exemplo, dados de equipe podem ser classificados como alto impacto nos negócios, impacto nos negócios médio ou baixo impacto nos negócios.<br/><br/>-Altera o nome de uma equipe ( **nome da equipe**).  <br/><br/>-Altera a descrição da equipe ( **Descrição da equipe**). <br/><br/>-Alterações feitas por qualquer uma das configurações de equipe. Um proprietário de equipe pode acessar essas configurações em um cliente de equipes clicando duas vezes uma equipe, clicando em **equipe gerenciar**e, em seguida, clicando na guia **configurações** . Para essas atividades, o nome da configuração que foi alterada é exibido na coluna **Item** nos resultados da pesquisa de log de auditoria.<br/> |
|Equipe de criação  <br/> |TeamCreated  <br/> |Um usuário cria uma nova equipe.  <br/> |
|Canal excluído  <br/> |ChannelDeleted  <br/> |Um usuário exclui um canal de uma equipe.  <br/> |
|Equipe excluído  <br/> |TeamDeleted  <br/> |Um proprietário de equipe exclui uma equipe.  <br/> |
|Bot removidos da equipe  <br/> |BotRemovedFromTeam  <br/> |Um usuário remove um bot de uma equipe.  <br/> |
|Conector removido  <br/> |ConnectorRemoved  <br/> |Um usuário remove o conector de um canal.  <br/> |
|Membros removidos da equipe  <br/> |MemberRemoved  <br/> |Um proprietário de equipe remove membro (s) de uma equipe.  <br/> |
|Guia removido  <br/> |TabRemoved  <br/> |Um usuário remove uma guia um canal.  <br/> |
|Conector atualizado  <br/> |ConnectorUpdated  <br/> |Um usuário modificado um conector em um canal.  <br/> |
|Guia atualizada  <br/> |TabUpdated  <br/> |Um usuário modificado uma guia em um canal.  <br/> |
|Usuário se conectou a equipes  <br/> |TeamsSessionStarted  <br/> |Um usuário entra um cliente do Microsoft Teams.  <br/> |

### <a name="yammer-activities"></a>Atividades do Yammer
  
A tabela a seguir lista o usuário e o log de auditoria de atividades de administração no Yammer que são registradas no Office 365. Para retornar o log de auditoria de atividades relacionadas a Yammer do Office 365, você precisa selecionar **Mostrar resultados para todas as atividades** na lista de **atividades** . Use as caixas de intervalo de data e a lista de **usuários** para restringir os resultados da pesquisa. 
  
|**Nome amigável**|**Operation**|**Descrição**|
|:-----|:-----|:-----|
|Política de retenção de dados alterados  <br/> |SoftDeleteSettingsUpdated  <br/> |Admin verificado atualiza a configuração para a política de retenção de dados de rede excluir disco rígido ou exclua suave. Apenas administradores verificados podem executar essa operação.  <br/> |
|Configuração de rede alterados  <br/> |NetworkConfigurationUpdated  <br/> |Rede ou admin verificado altera a configuração da rede do Yammer. Isso inclui a definição do intervalo para exportação de dados e a habilitação de bate-papo.  <br/> |
|Configurações de perfil de rede alterados  <br/> |ProcessProfileFields  <br/> |Rede ou admin verificado altera as informações sobre perfis de membro para a rede de usuários de rede.  <br/> |
|Alterado de modo particular de conteúdo  <br/> |SupervisorAdminToggled  <br/> |Admin verificado ativa ou desativa a *Modo de conteúdo particular* . Este modo permite um modo de exibição de admin postagens em grupos privados e exibir mensagens privadas entre usuários individuais (ou grupos de usuários). Apenas administradores verificados só podem executar essa operação.<br/> |
|Configuração de segurança alterado  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Admin verificado atualiza a configuração de segurança da rede Yammer. Isso inclui a configuração de diretivas de expiração de senha e restrições em endereços IP. Apenas administradores verificados podem executar essa operação.  <br/> |
|Arquivo criado  <br/> |FileCreated  <br/> |Usuário carrega um arquivo.  <br/> |
|Grupo criado  <br/> |GroupCreation  <br/> |Usuário cria um novo grupo.  <br/> |
|Grupo excluído  <br/> |GroupDeletion  <br/> |Um grupo é excluído do Yammer.  <br/> |
|Mensagem excluída  <br/> |MessageDeleted  <br/> |Usuário exclui uma mensagem.  <br/> |
|Arquivo baixado  <br/> |FileDownloaded  <br/> |Usuário baixa um arquivo.  <br/> |
|Dados exportados  <br/> |DataExport  <br/> |Admin verificado exporta os dados de rede do Yammer. Apenas administradores verificados podem executar essa operação.  <br/> |
|Arquivo compartilhado  <br/> |FileShared  <br/> |Usuário compartilha um arquivo com outro usuário.  <br/> |
|Usuário de rede suspenso  <br/> |NetworkUserSuspended  <br/> |Rede ou admin verificado suspende (desativa) um usuário do Yammer.  <br/> |
|Usuário suspenso  <br/> |UserSuspension  <br/> |Conta de usuário é suspenso (desativado).  <br/> |
|Descrição do arquivo atualizado  <br/> |FileUpdateDescription  <br/> |Usuário altera a descrição de um arquivo.  <br/> |
|Nome do arquivo atualizado  <br/> |FileUpdateName  <br/> |Usuário altera o nome de um arquivo.  <br/> |
|Arquivo visualizado  <br/> |FileVisited  <br/> |Usuário exibe um arquivo.  <br/> |
   
### <a name="microsoft-stream"></a>Microsoft Stream
  
Você pode pesquisar o log de auditoria para atividades em Microsoft Stream. Essas atividades incluem vídeos atividades executadas pelos usuários, atividades de canal de grupo e as atividades de admin como gerenciar usuários, gerenciar as configurações da organização e exportação de relatórios. Para obter uma descrição dessas atividades, consulte a seção "Atividades registradas em Microsoft Stream" nos [Logs de auditoria no Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).
  
### <a name="exchange-admin-audit-log"></a>Log de auditoria de administração do Exchange
  
Log de auditoria do administrador do Exchange — que é habilitado por padrão no Office 365 — registra um evento no log de auditoria do Office 365, quando um administrador (ou um usuário que tenha sido atribuído permissões administrativas) faz uma alteração na sua organização do Exchange Online. Alterações feitas usando o Centro de administração do Exchange ou a execução de um cmdlet do Windows PowerShell são registradas no log de auditoria do administrador do Exchange. Para informações mais detalhadas sobre a administração no Exchange de log de auditoria, consulte o [log de auditoria do administrador](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Aqui estão algumas dicas para a procura de atividade no log de auditoria do administrador do Exchange:
  
- Para retornar as entradas de log de auditoria do administrador do Exchange, você precisará selecionar **Mostrar resultados para todas as atividades** na lista de **atividades** . Use as caixas de intervalo de data e a lista de **usuários** para restringir os resultados da pesquisa para os cmdlets executados por um administrador do Exchange específico dentro de um intervalo de data específica. 
    
- Para exibir eventos de log de auditoria do administrador do Exchange, filtrar os resultados da pesquisa e o tipo de uma **-** (traço) na caixa de filtro de **atividade** . Isso exibirá os nomes de cmdlet, que são exibidos na coluna **atividade** para eventos de administração do Exchange. Em seguida, você pode classificar os nomes de cmdlet em ordem alfabética. 
    
    ![Digite um traço na caixa atividades filtrar eventos de administração do Exchange](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Para obter informações sobre qual cmdlet foi executado, quais parâmetros e valores de parâmetro foram usados e quais objetos foram afetados, você precisará exportar os resultados da pesquisa e selecione a opção de **Baixar todos os resultados** . 
    
- Você também pode exibir os eventos no log de auditoria do administrador do Exchange usando o Centro de administração do Exchange. Para obter instruções, consulte o [log de auditoria do administrador do modo de exibição](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Perguntas frequentes

**Onde encontrar sobre os recursos oferecidos pelo serviço de auditoria no Office 365?**

Para obter mais informações sobre os recursos de auditoria e relatórios disponíveis no Office 365, consulte [auditoria e relatórios no Office 365](office-365-auditing-and-reporting-overview.md). 

**Cite diferentes serviços do Office 365 que são auditados no momento.**

O Office 365 Services usado mais como o Exchange Online, SharePoint, OneDrive, Azure Active Directory, Teams da Microsoft, CRM, proteção avançada de ameaça e prevenção de perda de dados sejam auditadas. Consulte a seção [Intro](#search-the-audit-log-in-the-office-365-security-amp-compliance-center) neste artigo para obter uma lista completa.

**Que atividades sejam auditadas fazendo auditoria de serviço no Office 365?**

Consulte a seção de [atividades auditadas](#audited-activities) neste artigo para obter uma lista e descrição das atividades que são auditados no Office 365.

**Quanto tempo leva para um registro de auditoria esteja disponível depois que um evento ocorreu?**

A maioria dos dados de auditoria está disponível em até 30 minutos, mas pode levar até 24 horas após a ocorrência de um evento para a entrada de log de auditoria correspondente a ser exibido nos resultados da pesquisa. Consulte a tabela na seção deste artigo que mostra o tempo que leva para eventos nos serviços diferentes do Office 365 para estar disponíveis [antes de começar](#before-you-begin) .

**Quanto tempo são os registros de auditoria retidos por?**

Atualmente, os registros de log de auditoria são mantidos por 90 dias. Microsoft está trabalhando ativamente em um plano para aumentar esse limite. 

**Posso acessar os dados de auditoria programaticamente?**

Sim. A API de atividade de gerenciamento do Office 365 é usada para buscar os logs de auditoria programaticamente.  Para começar, consulte [Introdução ao APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Existem outras maneiras de fazer auditoria logs que não seja suing a segurança do Office 365 & Centro de conformidade ou a API de atividade de gerenciamento do Office 365?**

Não. Esses são apenas duas maneiras de obter dados de serviço de auditoria do Office 365. 

**É necessário habilitar individualmente a auditoria no cada serviço que eu quiser capturar logs de auditoria para?**

Na maioria dos serviços do Office 365, o auditoria está habilitado por padrão depois que você inicialmente ative a auditoria para sua organização do Office 365 (conforme descrito na seção [antes de começar](#before-you-begin) , neste artigo). No entanto, você precisa habilitar auditoria no Exchange Online para cada caixa de correio que você deseja fazer auditoria de caixa de correio.   Estamos trabalhando em Habilitar a auditoria de caixa de correio por padrão para todas as caixas de correio em uma organização do Office 365. Para obter mais informações, consulte "auditoria de caixa de correio do Exchange será habilitada por padrão" no [blog de segurança da Microsoft, privacidade e conformidade](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171).

**O suporte para Office 365 auditoria serviço eliminação da duplicação de registros?**

Não. O pipeline de serviço de auditoria é quase em tempo real e, portanto, não oferece suporte a eliminação da duplicação.
 
**Fluxo de dados de auditoria do Office 365 entre regiões geográficas?**

Não. No momento, temos auditoria implantações de pipeline no NA (América do Norte), EMEA (Europa, Oriente Médio e África) e regiões APAC (Ásia Pacífico). No entanto, podemos talvez flow os dados entre essas regiões para balanceamento de carga e somente durante o site live problemas. Quando executamos essas atividades, os dados em trânsito são criptografados.   
 
**Auditoria de dados criptografados?**

Auditoria de dados é armazenado em do caixas de correio do Exchange (dados em repouso) na mesma região onde o pipeline de auditoria está implantado. Esses dados não são criptografados. No entanto, os dados em trânsito sempre são criptografados. 












