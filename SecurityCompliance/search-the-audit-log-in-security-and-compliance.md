---
title: Pesquisar o log de auditoria no Centro de Conformidade e Segurança
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: Use o Centro de Conformidade e Segurança para pesquisar o log de auditoria unificada para exibir a atividade do usuário e do administrador na sua organização do Office 365.
ms.openlocfilehash: f10c6b488683201a2980702cc83efe97bf54f046
ms.sourcegitcommit: 50a2654d6d56249c3f836607f436446049be7833
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36838161"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Pesquisar o log de auditoria no Centro de Conformidade e Segurança

## <a name="introduction"></a>Introdução

Precisa descobrir se um usuário visualizou um documento específico ou apagou um item de sua caixa de correio? Nesse caso, você pode usar o Centro de Conformidade &amp; Segurança do Office 365 para pesquisar o log de auditoria unificada para exibir a atividade do usuário e do administrador na sua organização do Office 365.
 Por que usar um log de auditoria unificada? Porque você pode procurar os seguintes tipos de atividades de usuários e administradores do Office 365:

- Atividade do usuário do SharePoint Online e do OneDrive for Business

- Atividade do usuário do Exchange Online (log de auditoria da caixa de correio do Exchange)

- Atividade de administração do SharePoint Online

- Atividade de administração do Azure Active Directory (o serviço de diretório para o Office 365)

- Atividade de administradores do Exchange Online (log de auditoria de administradores do Exchange)

- Atividade de usuários e administradores do Sway

- atividades de descoberta eletrônica no centro de conformidade e segurança

- Atividade de usuários e administradores do Power BI

- Atividade de usuários e administradores do Microsoft Teams

- Atividade de usuários e administradores do Dynamics 365

- Atividade de usuários e administradores do Yammer

- Atividade de usuários e administradores do Microsoft Flow

- Atividade de usuários e administradores do Microsoft Stream

- Atividade de administradores e analistas do Microsoft Workplace Analytics

- Atividade de usuários e administradores do Microsoft PowerApps

## <a name="before-you-begin"></a>Antes de começar

Leia os seguintes itens antes de começar a pesquisar o log de auditoria do Office 365.

- Você (ou outro administrador) deve ativar primeiro o log de auditoria antes de começar a pesquisar no log de auditoria do Office 365. Para ativá-lo, clique em **Iniciar a gravação das atividades dos usuários e administradores** na página **Pesquisar log de auditoria** no Centro de Conformidade e Segurança. (Se você não vir esse link, a auditoria já está ativada na sua organização). Depois de ativá-lo, será exibida uma mensagem informando que o log de auditoria está sendo preparado e que você pode executar uma pesquisa dentro de algumas horas após concluir a preparação. Isso só precisa ser feito uma vez.

  > [!NOTE]
  > Estamos em processo de ativar a auditoria por padrão. Até lá, ative-a conforme descrevemos anteriormente.

- É preciso atribuir a função Logs de Auditoria Somente para Exibição ou Logs de Auditoria do Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de funções Gerenciamento de Conformidade e Gerenciamento de Organização na página **Permissões** do centro de administração do Exchange. Note que os administradores globais do Office 365 e do Microsoft 365 são automaticamente adicionados como membros do grupo de função Gerenciamento da Organização no Exchange Online. Para que um usuário tenha a capacidade de pesquisar o log de auditoria do Office 365 com o nível mínimo de privilégios, você pode criar um grupo de funções personalizado no Exchange Online, adicionar a função Logs de Auditoria Somente para Exibição ou Logs de Auditoria e, em seguida, adicionar o usuário como um membro do novo grupo de funções. Para saber mais, confira [Gerenciar Grupos de Funções do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

  > [!IMPORTANT]
  > Se você atribuir a um usuário a função Logs de Auditoria Somente para Exibição ou Logs de Auditoria na página **Permissões** do Centro de Conformidade e Segurança, eles não poderão pesquisar o log de auditoria do Office 365. Você deve atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet Exchange Online.

- Quando uma atividade auditada é realizada por um usuário ou administrador, um registro de auditoria é gerado e armazenado no log de auditoria do Office 365 para a sua organização. O período de tempo em que um registro de auditoria é mantido (e pesquisável no log de auditoria) depende da sua assinatura do Office 365 e, especificamente, do tipo de licença atribuída a um usuário específico.

  - **Office 365 E3:** Os registros de auditoria são mantidos por 90 dias. Isso significa que você pode pesquisar o log de auditoria para atividades que foram realizadas nos últimos 90 dias.

  - **Office 365 E5:** Os registros de auditoria também são mantidos por 90 dias. Manter registros de auditoria por um ano pode estar disponível para usuários do E5 e usuários com uma licença do E3 e uma licença do complemento de Conformidade Avançada do Office 365.

    > [!NOTE]
    > O programa de visualização particular com período de retenção de um ano para registros de auditoria para organizações do E5 (ou para usuários em organizações do E3 que têm licenças complementares de Conformidade Avançada) é fechada para um novo registro. Esse artigo será atualizado quando o período de retenção de um ano estiver disponível na visualização pública ou lançado para disponibilidade geral.

- Caso pretenda desativar a pesquisa de log de auditoria do Office 365 da sua organização, execute o comando a seguir no PowerShell remoto conectado à sua organização do Exchange Online:

  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Para ativar a pesquisa de auditoria novamente, execute o seguinte comando no PowerShell do Exchange Online:

  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

  Para saber mais, confira [Desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).

- Como mencionado anteriormente, o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet Exchange Online, que é **Search-UnifiedAuditLog**. Isso significa que você pode usar esse cmdlet para pesquisar o log de auditoria do Office 365, em vez de usar a página **pesquisa de log de Auditoria** no Centro de Conformidade e Segurança. Você precisa executar esse cmdlet no PowerShell remoto conectado à sua organização do Exchange Online. Para saber mais, confira [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).

  Para obter informações sobre como exportar os resultados da pesquisa retornados pelo cmdlet **Search-UnifiedAuditLog** para um arquivo CSV, confira a seção "Dicas para exportar e exibir o log de auditoria" em [Exportar, configurar e exibir registros de log de auditoria](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Se quiser baixar dados programaticamente do log de auditoria do Office 365, recomendamos que você use a API de Atividades de Gerenciamento do Office 365 em vez de usar um script do PowerShell. A API de Atividades de Gerenciamento do Office 365 é um serviço Web REST que você pode usar para desenvolver soluções de monitoramento de operações, segurança e conformidade para sua organização. Para mais informações, confira [referência da API de Atividade de Gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).

- Pode levar de 30 minutos a 24 horas após a ocorrência de um evento para que a entrada do log de auditoria correspondente seja exibida nos resultados de pesquisa. A tabela a seguir mostra o tempo necessário para os vários serviços do Office 365.

  |**Serviço do Office 365**|**30 minutos**|**24 horas**|
  |:-----|:-----:|:-----:|
  |Proteção Avançada contra Ameaças e Inteligência contra Ameaças|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Azure Active Directory (eventos de logon do usuário)||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Azure Active Directory (eventos de administração)||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Prevenção contra Perda de Dados|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Dynamics 365 CRM|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Descoberta eletrônica|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Exchange Online|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Flow|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Project|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Stream|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Teams|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Power BI|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Centro de Conformidade e Segurança|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |SharePoint Online e OneDrive for Business|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Sway||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Workplace Analytics|![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Yammer||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|

- O Azure Active Directory (Azure AD) é o serviço de diretório do Office 365. O log de auditoria unificado contém atividades de usuários, grupos, aplicativos, domínios e atividades de diretórios realizadas no Microsoft 365 ou no portal de gerenciamento do Azure. Para obter uma lista completa de eventos do Azure AD, confira [Eventos de Relatório de Auditoria do Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).

- O log de auditoria do Power BI não está habilitado por padrão. Para pesquisar as atividades do Power BI no log de auditoria do Office 365, habilite o recurso de auditoria no portal de administração do Power BI. Para obter instruções, confira a seção "logs de auditoria" no [portal de administração do Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).

## <a name="search-the-audit-log"></a>Pesquisar o log de auditoria

A seguir, veja o processo para pesquisar o log de auditoria do Office 365. 

[Etapa 1: Executar uma pesquisa de log de auditoria](#step-1-run-an-audit-log-search)

[Etapa 2: Exibir os resultados da pesquisa](#step-2-view-the-search-results)

[Etapa 3: Filtrar os resultados da pesquisa](#step-3-filter-the-search-results)

[Etapa 4: Exportar os resultados da pesquisa para um arquivo](#step-4-export-the-search-results-to-a-file)

### <a name="step-1-run-an-audit-log-search"></a>Etapa 1: Executar uma pesquisa de log de auditoria

1. Acesse [https://protection.office.com](https://protection.office.com).

    > [!TIP]
    > Use uma sessão de navegação particular (não uma sessão regular) para acessar o Centro de Conformidade e Segurança, pois isso impedirá que a credencial com a qual você está conectado no momento seja usada. Para abrir uma sessão de Navegação InPrivate no Internet Explorer ou no Microsoft Edge, basta pressionar CTRL+SHIFT+P. Para abrir uma sessão de navegação privada no Google Chrome (chamado de janela incógnita), pressione CTRL+SHIFT+N.

2. Entre no Office 365 usando a sua conta corporativa ou de estudante.

3. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisar** e, em seguida, clique em **Pesquisa de Log de Auditoria**.

    É exibida a página **Pesquisa de log de auditoria**.

    ![Configure os critérios e clique em Pesquisar para executar o relatório](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)

    > [!NOTE]
    > Você primeiro precisa ativar o log de auditoria para poder executar uma pesquisa de log de auditoria. Se o link **Iniciar gravação de atividade de usuários e administradores** for exibido, clique nele para ativar a auditoria. Se você não vir esse link, significa que a auditoria já está ativada na sua organização.

4. Configure os seguintes critérios de pesquisa: 

    a. **Atividades**: Clique na lista suspensa para exibir as atividades que você pode procurar. As atividades de usuários e administradores são organizadas em grupos de atividades relacionadas. Você pode selecionar atividades específicas ou pode clicar no nome do grupo de atividades para selecionar todas as atividades que ele contém. Você também pode clicar em uma atividade selecionada para limpar a seleção. Após a execução da pesquisa, apenas as entradas do log de auditoria das atividades selecionadas serão exibidas. Ao selecionar **Mostrar resultados para todas as atividades** os resultados para todas as atividades executadas pelo usuário ou grupo de usuários selecionado será exibido.

    Mais de 100 atividades de usuários e administradores são registradas no log de auditoria do Office 365. Clique na guia **Atividades auditadas**, no tópico deste artigo, para ver as descrições de cada atividade em cada um dos diferentes serviços do Office 365.

    b. **Data de início** e **Data de término**: Os últimos sete dias são selecionados por padrão. Selecione um intervalo de datas e horas para exibir os eventos ocorridos durante esse período. A data e a hora são apresentadas no formato UTC (Tempo Universal Coordenado). O intervalo de datas máximo que você pode especificar é de 90 dias. Um erro será exibido se o período selecionado for superior a 90 dias.

    > [!TIP]
    > Se você estiver usando o intervalo máximo de datas de 90 dias, selecione a hora atual para a **Data de início**. Caso contrário, você receberá um erro afirmando que a data de início é anterior à data de término. Se você tiver ativado a auditoria nos últimos 90 dias, o intervalo máximo de datas não poderá começar antes da data em que a auditoria foi ativada.

    c. **Usuários**: Clique nessa caixa e selecione um ou mais usuários para os quais deseja exibir resultados. As entradas do log de auditoria para a atividade selecionada realizada pelos usuários que você seleciona nessa caixa são exibidas na lista de resultados. Deixe essa caixa em branco para retornar entradas para todos os usuários (e contas de serviço) na sua organização.

    d. **Arquivo, pasta ou site**: Digite alguns ou todos os nome de arquivo ou pasta para pesquisar atividades relacionadas ao arquivo de pasta que contenha a palavra-chave especificada. Você também pode especificar uma URL de um arquivo ou pasta. Se você usar uma URL, certifique-se, ao digitar o caminho completo ou apenas uma parte da URL, não incluir espaços ou caracteres especiais.

    Deixe essa caixa em branco para retornar entradas para todos os arquivos e pastas em sua organização.

   **DICAS**

   - Se você estiver procurando por todas as atividades relacionadas a um **site**, adicione o símbolo curinga (\*) após a URL para retornar todas as entradas para esse site. por exemplo, **"https://contoso-my.sharepoint.com/personal/*"**.

   - Se você estiver procurando por todas as atividades relacionadas a um **arquivo**, adicione o símbolo curinga (\*) antes do nome do arquivo para retornar todas as entradas desse arquivo, por exemplo, **"*Customer_Profitability_Sample.csv"**.

5. Clique em **Pesquisar** para executar a pesquisa usando seus critérios de pesquisa. 

   Os resultados da pesquisa são carregados e, depois de alguns momentos, são exibidos em **Resultados**. Quando a pesquisa estiver concluída, o número de resultados encontrados será exibido. Um máximo de 5.000 eventos serão exibidos no painel **Resultados** em incrementos de 150 eventos. Se mais de 5.000 eventos atenderem aos critérios de pesquisa, os 5.000 mais recentes serão exibidos.

   ![O número de resultados é exibido após a conclusão da pesquisa](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)

#### <a name="tips-for-searching-the-audit-log"></a>Dicas para pesquisar o log de auditoria

- É possível selecionar atividades específicas para procurar clicando no nome da atividade. Também é possível procurar todas as atividades em um grupo (como **Atividades de arquivos e pastas**) clicando no nome do grupo. Se uma atividade estiver selecionada, você poderá clicar nela para cancelar a seleção. Você também pode usar a caixa de pesquisa para exibir as atividades que contêm a palavra-chave digitada.

  ![Clique no nome do grupo de atividade para selecionar todas as atividades](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)

- É necessário selecionar **Mostrar resultados para todas as atividades**, na lista **Atividades** para exibir eventos do log de auditoria de administradores do Exchange. Os eventos desse log de auditoria exibem um nome de cmdlet (por exemplo, **Set-Mailbox**) na coluna **Atividade** dos resultados. Para obter mais informações, clique na guia **Atividades auditadas** neste tópico e, em seguida, clique em **Atividades de administração do Exchange**.

  Da mesma forma, existem algumas atividades de auditoria que não possuem um item correspondente na lista **Atividades**. Se souber o nome da operação dessas atividades, você poderá procurar todas as atividades e, em seguida, filtrar os resultados, digitando o nome da operação na caixa da coluna **Atividade**. Confira a [Etapa 3: filtrar os resultados da pesquisa](#step-3-filter-the-search-results) para saber mais sobre como filtrar os resultados.

- Clique em **Limpar** para limpar os critérios de pesquisa atuais. O intervalo de datas retorna para os últimos sete dias padrão. Você também pode clicar em **Limpar tudo para mostrar resultados de todas as atividades** para cancelar todas as atividades selecionadas.

- Se 5.000 resultados forem encontrados, você poderá supor que existam provavelmente mais de 5.000 eventos que corresponderam aos critérios de pesquisa. É possível restringir os critérios de pesquisa e executar a pesquisa novamente para retornar menos resultados ou exportar todos os resultados da pesquisa selecionando **Exportar resultados** \> **Baixar todos os resultados**.

### <a name="step-2-view-the-search-results"></a>Etapa 2: Exibir os resultados da pesquisa

Os resultados de uma pesquisa de log de auditoria são exibidos em **Resultados**, na página **Pesquisa de log de auditoria**. Conforme mencionado anteriormente, um máximo de 5.000 eventos (mais recentes) é exibido em incrementos de 150 eventos. Para exibir mais eventos, use a barra de rolagem no painel **Resultados** ou pressione **Shift+End** para exibir os próximos 150 eventos.

Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa:

- **Data:**: A data e a hora (no formato UTC) de ocorrência do evento.

- **Endereço IP**: O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido em um formato de endereço IPv4 ou IPv6.

- **Usuário**: O usuário (ou a conta de serviço) que realizou a ação que disparou o evento.

- **Atividade**: A atividade realizada pelo usuário. Esse valor corresponde às atividades que você selecionou na lista suspensa **Atividades**. Para um evento do log de auditoria de administradores do Exchange, o valor nessa coluna é um cmdlet do Exchange.

- **Item**: O objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta do usuário que foi atualizada. Nem todas as atividades têm um valor nesta coluna.

- **Detalhe**: Informações adicionais sobre uma atividade. Novamente, nem todas as atividades têm um valor.

> [!TIP]
> Clique em um cabeçalho de coluna em **Resultados** para classificar os resultados. Você pode classificar os resultados da A até Z ou de Z até A. Clique no cabeçalho **Data** para classificar os resultados do mais antigo para o mais recente, ou vice-versa.

#### <a name="view-the-details-for-a-specific-event"></a>Exibir os detalhes de um evento específico

É possível visualizar mais detalhes sobre o evento clicando no registro de evento na lista de resultados da pesquisa. É exibida uma página **Detalhes** que contém as propriedades detalhadas do registro do evento. As propriedades exibidas dependem do serviço do Office 365 em que o evento ocorre. Para exibir esses detalhes, clique em **Mais informações**. Para obter descrições, confira [Propriedades detalhadas no log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md).

![Clique em Mais informações para exibir as propriedades detalhadas do registro de eventos do log de auditoria](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

### <a name="step-3-filter-the-search-results"></a>Etapa 3: Filtrar os resultados da pesquisa

Além de classificar, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Este é um ótimo recurso que pode ajudá-lo a filtrar rapidamente os resultados para um usuário ou atividade específica. Você pode criar inicialmente uma pesquisa ampla e depois filtrar rapidamente os resultados para ver eventos específicos. Em seguida, você pode restringir os critérios de pesquisa e executar a pesquisa novamente para retornar um conjunto de resultados menor e mais conciso.

Para filtrar os resultados:

1. Execute uma pesquisa de logs de auditoria.

2. Quando os resultados forem exibidos, clique em **Filtrar resultados**.

   Caixas de palavras-chave são exibidas em cada cabeçalho de coluna.

3. Clique em uma das caixas sob um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna na qual você está filtrando. Os resultados serão reajustados dinamicamente para exibir os eventos que correspondem ao seu filtro.

   ![Digite uma palavra no filtro para exibir os eventos que correspondam ao filtro](media/542dc323-a997-402c-934b-cc5e218e50bc.png)

4. Para limpar um filtro, clique em **X** na caixa de filtro ou clique em **Ocultar filtragem**.

> [!TIP]
> Para exibir eventos do log de auditoria de administradores do Exchange, digite um **-** (traço) na caixa de filtro **Atividade**. Isto exibirá nomes de cmdlets, que aparecem na coluna **Atividade** para eventos de administradores do Exchange. Em seguida, você pode classificar os nomes de cmdlets em ordem alfabética.

### <a name="step-4-export-the-search-results-to-a-file"></a>Etapa 4: Exportar os resultados da pesquisa para um arquivo

É possível exportar os resultados de uma pesquisa de logs de auditoria para um arquivo CSV (valores separados por vírgula) no seu computador local. Você pode abrir esse arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e divisão de uma única coluna (que contém várias propriedades) em várias colunas.

1. Execute uma pesquisa de logs de auditoria e, em seguida, reveja os critérios de pesquisa até ter os resultados desejados.

2. Clique em **Exportar resultados** e selecione uma das seguintes opções:

   - **Salvar resultados carregados**: Escolha essa opção para exportar somente as entradas exibidas em **Resultados**, na página **Pesquisa de log de auditoria**. O arquivo CSV baixado contém as mesmas colunas (e dados) exibidos na página (Data, Usuário, Atividade, Item e Detalhes). Uma coluna extra (chamado **Mais**) é incluída no arquivo CSV que contém mais informações da entrada do log de auditoria. Como você está exportando os mesmos resultados que estão carregados (e visíveis) na página **Pesquisa de log de auditoria**, no máximo 5.000 entradas são exportadas.

   - **Baixar todos os resultados**: Escolha essa opção para exportar todas as entradas do log de auditoria do Office 365 que correspondem aos critérios de pesquisa. Para um grande conjunto de resultados de pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além das 5.000 registros de auditoria que podem ser exibidos na página de **Pesquisa de log de auditoria**. Essa opção baixa os dados brutos do log de auditoria para um arquivo CSV e contém informações adicionais da entrada do log de auditoria em uma coluna chamada **AuditData**. O download do arquivo poderá ser mais demorado se você escolher essa opção de exportação, pois o arquivo pode ser muito maior do que o baixado com a outra opção.

     > [!IMPORTANT]
     > É possível baixar no máximo 50 mil entradas para um arquivo CSV de uma única pesquisa de logs de auditoria. Se 50 mil entradas forem baixadas para o arquivo CSV, você poderá supor que existem provavelmente mais de 50 mil eventos que corresponderam aos critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas do log de auditoria. Talvez seja necessário executar várias pesquisas com intervalos de datas menores para exportar mais de 50 mil entradas.

3. Após a seleção de uma opção de exportação, é exibida uma mensagem na parte inferior da janela solicitando que você abra o arquivo CSV, salve-o na pasta Downloads ou salve-o em uma pasta específica.

#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>Informações adicionais sobre como exportar e exibir resultados de pesquisa de log de auditoria

- Se você baixar todos os resultados da pesquisa, o arquivo CSV incluirá uma coluna chamada **AuditData**, que contém informações adicionais sobre cada evento. Os dados dessa coluna consistem em um objeto JSON contendo várias propriedades do registro de log de auditoria. Cada par *propriedade: valor* no objeto JSON é separado por uma vírgula. Você pode usar a ferramenta transformação JSON no editor do Power Query do Excel para dividir a coluna **AuditData** em várias colunas, de modo que cada propriedade no objeto JSON tenha sua própria coluna. Isso permitirá que você classifique e filtre uma ou mais dessas propriedades. Para obter instruções passo a passo sobre como usar o editor do Power Query para transformar o objeto JSON, confira [Exportar, configurar e exibir registros de log de auditoria](export-view-audit-log-records.md).

  Depois de dividir a coluna **AuditData**, você pode filtrar a coluna **Operações** para exibir as propriedades detalhadas de um tipo específico de atividade.

- A opção **Baixar todos os resultados** baixa os dados brutos do log de auditoria do Office 365 em um arquivo CSV. Esse arquivo contém nomes de coluna diferentes (CreationDate, userIds, Operação, AuditData) que o arquivo que será baixado se você selecionar a opção **Salvar resultados carregados**. Os valores nos dois arquivos CSV diferentes para a mesma atividade também podem ser diferentes. Por exemplo, a atividade da coluna **Ação** no arquivo CSV e pode ter um valor diferente do nome "amigável" que é exibido na coluna **Atividade** da página **Pesquisa de log de auditoria**. Por exemplo, MailboxLogin vs. Usuário conectado à caixa de correio.

- Quando você baixa todos os resultados de uma consulta de pesquisa que contém eventos de diferentes serviços do Office 365, a coluna **AuditData** do arquivo CSV contém propriedades diferentes, dependendo do serviço no qual a ação foi realizada. Por exemplo, as entradas do Exchange e os logs de auditoria do Azure AD incluem uma propriedade chamada **ResultStatus** que indica se a ação teve êxito ou não. Essa propriedade não está incluída para eventos do SharePoint. Da mesma forma, os eventos do SharePoint têm uma propriedade que identifica a URL do site para atividades relacionadas a arquivos pastas. Para atenuar esse comportamento, considere usar diferentes pesquisas para exportar os resultados de atividades de um único serviço.

  Para obter uma descrição das propriedades listadas na coluna **AuditData** do arquivo CSV quando você baixa todos os resultados e o serviço ao qual cada uma se aplica, veja [Propriedades detalhadas no log de auditoria do Office 365 ](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Atividades auditadas

As tabelas nesta seção descrevem as atividades que são auditadas no Office 365. Você pode procurar esses eventos pesquisando o log de auditoria no centro de segurança e conformidade.

Essas tabelas agrupam atividades relacionadas ou as atividades de um serviço específico do Office 365. As tabelas incluem o nome amigável que é exibido na lista suspensa **Atividades** e o nome da operação correspondente exibida nas informações detalhadas de um registro de auditoria e no arquivo CSV quando você exporta o resultados da pesquisa. Para obter descrições das informações detalhadas, confira [Propriedades detalhadas no log de auditoria do Office 365](detailed-properties-in-the-office-365-audit-log.md).

Clique em um dos links a seguir para ir até uma tabela específica.

||||
|:-----|:-----|:-----|
|[Atividades de arquivo e página](#file-and-page-activities)|[Atividades de pasta](#folder-activities)|[Atividades de lista do SharePoint](#sharepoint-list-activities)|
|[Atividades de compartilhamento e solicitação de acesso](#sharing-and-access-request-activities)|[Atividades de sincronização](#synchronization-activities)|[Atividades de permissões de site](#site-permissions-activities)|
|[Atividades de administração de site](#site-administration-activities)|[Atividades de caixa de correio do Exchange](#exchange-mailbox-activities)|[Atividades do Sway](#sway-activities)|
|[Atividades de administração de usuários](#user-administration-activities)|[Atividades de administração de grupos do Azure AD](#azure-ad-group-administration-activities)|[Atividades de administração de aplicativos](#application-administration-activities)|
|[Atividades de administração de funções](#role-administration-activities)|[Atividades de administração de diretórios](#directory-administration-activities)|[Atividades de Descoberta Eletrônica](#ediscovery-activities)|
|[Atividades de Descoberta Eletrônica Avançada](#advanced-ediscovery-activities)|[Atividades do Power BI](#power-bi-activities)|[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)|
|[Atividades do Microsoft Teams](#microsoft-teams-activities)|[Atividades do Yammer](#yammer-activities)|[Atividades do Fluxo da Microsoft](#microsoft-flow-activities)|
|[Atividades do Microsoft PowerApps](#microsoft-powerapps)|[Atividades do Microsoft Stream](#microsoft-stream-activities)|[Atividades de administradores do Exchange](#exchange-admin-audit-log)|
||||

### <a name="file-and-page-activities"></a>Atividades de arquivo e página

A tabela a seguir descreve as atividades de arquivo e página do SharePoint Online e do OneDrive for Business.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Arquivo acessado|FileAccessed|O usuário ou a conta do sistema acessa um arquivo.|
|(nenhuma)|FileAccessedExtended|Isso está relacionado à atividade "Arquivo acessado" (FileAccessed). Um evento FileAccessedExtended é registrado em log quando a mesma pessoa acessa continuamente um arquivo por um longo período (até 3 horas). <br/><br/> O propósito de registrar eventos FileAccessedExtended em log é reduzir o número de eventos FileAccessed registrados quando um arquivo é acessado continuamente. Isso ajuda a reduzir o ruído de vários registros de FileAccessed para, basicamente, a mesma atividade do usuário e permite que você se concentre no evento FileAccessed inicial (e mais importante).|
|Rótulos de política de conformidade alterados|ComplianceSettingChanged|Um rótulo de retenção foi aplicado ou removido de um documento. Este evento é acionado quando uma etiqueta de retenção é aplicada manualmente ou automaticamente a uma mensagem.|
|Status de registro alterado para bloqueado|LockRecord|O status do registro de um rótulo de retenção que classifica um documento como um registro foi bloqueado. Isso significa que o documento não pode ser modificado ou excluído. Somente os usuários que possuem pelo menos a permissão de colaborador de um site podem alterar o status do registro de um documento.|
|Status de registro alterado para desbloqueado|UnlockRecord|O status do registro de um rótulo de retenção que classifica um documento como um registro foi debloqueado. Isso significa que o documento pode ser modificado ou excluído. Somente os usuários que possuem pelo menos a permissão de colaborador de um site podem alterar o status do registro de um documento.|
|Arquivo com check-in|FileCheckedIn|O usuário faz check-in de um documento que estava em check-out em uma biblioteca de documentos.|
|Arquivo em check-out|FileCheckedOut|O usuário faz check-out de um documento localizado em uma biblioteca de documentos. Os usuários podem fazer check-out e alterações nos documentos que foram compartilhados com eles.|
|Arquivo copiado|FileCopied|O usuário copia um documento de um site. O arquivo copiado pode ser salvo em outra pasta no site.|
|Arquivo excluído|FileDeleted|O usuário exclui um documento de um site.|
|Arquivo excluído da Lixeira|FileDeletedFirstStageRecycleBin|O usuário exclui um arquivo da lixeira de um site.|
|Arquivo excluído da Lixeira de segundo estágio|FileDeletedSecondStageRecycleBin|O usuário exclui um arquivo da lixeira de segundo estágio de um site.|
|Rótulos de política de conformidade excluídos|ComplianceRecordDelete|Um documento que foi classificado como um registro foi excluído. Um documento é considerado um registro quando uma etiqueta de retenção que classifica o conteúdo como um registro é aplicada ao documento.|
|Incompatibilidade de confidencialidade em documento detectada|DocumentSensitivityMismatchDetected|O usuário carrega um documento classificado com um rótulo de sensibilidade que tem uma prioridade mais alta do que o rótulo de sensibilidade aplicada ao site para o qual o documento foi carregado. <br/><br/> Esse evento não será disparado se o rótulo de sensibilidade aplicado a um site tiver uma prioridade mais alta do que o rótulo de sensibilidade aplicada a um documento carregado no site. Para obter mais informações sobre a prioridade de rótulos de sensibilidade, confira a seção "prioridade de rótulo” em [Visão geral de rótulos de sensibilidade.](sensitivity-labels.md#label-priority-order-matters).|
|Malware detectado no arquivo|FileMalwareDetected|O mecanismo de antivírus do SharePoint detecta malwares em um arquivo.|
|Check-out de arquivo descartado|FileCheckOutDiscarded|O usuário descarta (ou desfaz) um arquivo em check-out. Isso significa que todas as alterações que ele tiver feito nesse arquivo durante o estado de check-out serão descartados, e não salvas na versão do documento localizada na biblioteca de documentos.|
|Arquivo baixado|FileDownloaded|O usuário baixa um documento de um site.|
|Arquivo modificado|FileModified|O usuário ou a conta do sistema modifica o conteúdo ou as propriedades de um documento em um site.|
|(nenhum)|FileModifiedExtended|Isso está relacionado à atividade "Arquivo modificado" (FileModified). Um evento FileModifiedExtended é registrado em log quando a mesma pessoa modifica continuamente um arquivo por um longo período (até 3 horas). <br/><br/> O propósito de registrar eventos FileModifiedExtended em log é reduzir o número de eventos FileModified registrados quando um arquivo é modificado continuamente. Isso ajuda a reduzir o ruído de vários registros de FileModified para o que é essencialmente a mesma atividade do usuário e permite que você se concentre no evento FileModified inicial (e mais importante).|
|Arquivo movido|FileMoved|O usuário move um documento de sua localização atual em um site até uma nova localização.|
|(nenhum)|FilePreviewed|O usuário visualiza documentos em um site do SharePoint ou OneDrive for Business. Esses eventos geralmente ocorrem em grandes volumes com base em uma única atividade, como a exibição de uma galeria de imagens.|
|Todas as versões secundárias do arquivo foram recicladas|FileVersionsAllMinorsRecycled|O usuário exclui todas as versões secundárias do histórico de versões de um arquivo. As versões excluídas são movidas para a lixeira do site.|
|Todas as versões do arquivo foram recicladas|FileVersionsAllRecycled|O usuário exclui todas as versões do histórico de versões de um arquivo. As versões excluídas são movidas para a lixeira do site.|
|Versão do arquivo reciclada|FileVersionRecycled|O usuário exclui uma versão do histórico de versões de um arquivo. A versão excluída é movida para a lixeira do site.|
|Arquivo renomeado|FileRenamed|O usuário renomeia um documento em um site.|
|Arquivo restaurado|FileRestored|O usuário restaura um documento da lixeira de um site. |
|Arquivo carregado|FileUploaded|O usuário carrega um documento em uma pasta em um site.|
|Página exibida|PageViewed|O usuário exibe uma página no site. Isso não inclui usar um navegador da Web para exibir arquivos localizados em uma biblioteca de documentos.|
|(nenhum)|PageViewedExtended|Isso está relacionado à atividade "Página exibida" (PageViewed). Um evento PageViewedExtended é registrado em log quando a mesma pessoa exibe continuamente uma página da Web por um longo período (até 3 horas). <br/><br/> O propósito de registrar eventos PageViewedExtended em log é reduzir o número de eventos PageViewed registrados quando uma página é exibida continuamente. Isso ajuda a reduzir o ruído de vários registros de PageViewed para o que é essencialmente a mesma atividade do usuário e permite que você se concentre no evento PageViewed inicial (e mais importante).|
|Exibição sinalizada pelo cliente|ClientViewSignaled|Um cliente do usuário (por exemplo, site ou aplicativo móvel) sinalizou que a página indicada foi exibida pelo usuário. Essa atividade geralmente é registrada após um evento PagePrefetched para uma página. <br/><br/>**OBSERVAÇÃO**: Como os eventos ClientViewSignaled são sinalizados pelo cliente, em vez do servidor, é possível que ele não seja registrado pelo servidor e, portanto, pode não aparecer no log de auditoria. Também é possível que as informações do registro de auditoria não sejam confiáveis. No entanto, como a identidade do usuário é validada por um token usado para criar o sinal, a identidade do usuário listada no registro de auditoria correspondente é precisa. |
|(nenhum)|PagePrefetched|O cliente do usuário (por exemplo, site ou aplicativo móvel) solicitou a página indicada para ajudar a melhorar o desempenho se o usuário navegar por ela. Este evento é registrado para indicar que o conteúdo da página foi servido ao cliente do usuário. Esse evento não é um indício definitivo de que o usuário navegou pela página. <br/><br/> Quando o conteúdo da página é renderizado pelo cliente (conforme a solicitação do usuário), um evento ClientViewSignaled deve ser gerado. Nem todos os clientes oferecem suporte para indicar uma pré-busca e, portanto, algumas atividades pré-buscadas podem ser registradas como eventos PageViewed.|
||||

### <a name="folder-activities"></a>Atividades de pasta

A tabela a seguir descreve as atividades de pasta do SharePoint Online e do OneDrive for Business.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Pasta copiada|FolderCopied|O usuário copia uma pasta de um site para outro local do SharePoint ou do OneDrive for Business.|
|Pasta criada|FolderCreated|O usuário cria uma pasta no site.|
|Pasta excluída|FolderDeleted|O usuário exclui uma pasta do site.|
|Pasta excluída da Lixeira|FolderDeletedFirstStageRecycleBin|O usuário exclui uma pasta da Lixeira no site.|
|Pasta excluída da Lixeira de segundo estágio|FolderDeletedSecondStageRecycleBin|O usuário exclui uma pasta da Lixeira de segundo estágio no site.|
|Pasta modificada|FolderModified|O usuário modifica uma pasta no site. Isso inclui alterar os metadados da pasta, como propriedades e marcas.|
|Pasta movida|FolderMoved|O usuário move uma pasta para um local diferente no site.|
|Pasta renomeada|FolderRenamed|O usuário renomeia uma pasta no site.|
|Pasta restaurada|FolderRestored|O usuário restaura uma pasta da lixeira de um site.|
||||

### <a name="sharepoint-list-activities"></a>Atividades de lista do SharePoint

A tabela a seguir descreve as atividades relacionadas quando os usuários interagem com listas e itens de lista do SharePoint Online.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Lista criada|ListCreated|Um usuário criou uma lista do SharePoint.|
|Coluna de lista criada|ListColumnCreated|Um usuário criou uma coluna de lista do SharePoint. Uma coluna de lista é uma coluna anexada a uma ou mais listas do SharePoint.|
|Tipo de conteúdo de lista criado|ListContentTypeCreated|Um usuário criou um tipo de conteúdo de lista. Um tipo de conteúdo de lista é um tipo de conteúdo anexado a uma ou mais listas do SharePoint.|
|Item de lista criado|ListItemCreated|Um usuário criou um item em uma lista do SharePoint existente.|
|Coluna de site criada|SiteColumnCreated|Um usuário criou uma coluna de site do SharePoint. Uma coluna de site é uma coluna que não está anexada a uma lista. Uma coluna de site é também uma estrutura de metadados que pode ser usada por qualquer lista em uma determinada Web.|
|Tipo de conteúdo de site criado|ContentType do site criado|Um usuário criou um tipo de conteúdo de site. Um tipo de conteúdo de site é um tipo de conteúdo anexado ao site primário.|
|Lista excluída|ListDeleted|Um usuário excluiu uma lista do SharePoint.|
|Coluna de lista excluída|Coluna de Lista Excluída|Um usuário excluiu uma coluna de lista do SharePoint.|
|Tipo de conteúdo de lista excluído|ListContentTypeDeleted|Um usuário excluiu um tipo de conteúdo de lista.|
|Item de lista excluído|Item de Lista Excluído|Um usuário excluiu um item de lista do SharePoint.|
|Coluna de site excluída|SiteColumnDeleted|Um usuário excluiu uma coluna de site do SharePoint.|
|Tipo de conteúdo de site excluído|SiteContentTypeDeleted|Um usuário excluiu um tipo de conteúdo de site.|
|Item de lista reciclado|ListItemRecycled|Um usuário moveu um item de lista do SharePoint para a Lixeira.|
|Lista restaurada|ListRestored|Um usuário restaurou uma lista do SharePoint da Lixeira.|
|Item de lista restaurado|ListItemRestored|Um usuário restaurou um item de lista do SharePoint da Lixeira.|
|Lista atualizada|ListUpdated|Um usuário atualizou uma lista do SharePoint modificando uma ou mais propriedades.|
|Coluna da lista atualizada|ListColumnUpdated|Um usuário atualizou uma coluna de lista do SharePoint modificando uma ou mais propriedades.|
|Tipo de conteúdo de lista atualizado|ListContentTypeUpdated|Um usuário atualizou um tipo de conteúdo de lista modificando uma ou mais propriedades.|
|Item de lista atualizado|ListItemUpdated|Um usuário atualizou um item de lista do SharePoint modificando uma ou mais propriedades.|
|Coluna de site atualizada|SiteColumnUpdated|Um usuário atualizou uma coluna de site do SharePoint modificando uma ou mais propriedades.|
|Tipo de conteúdo de site atualizado|SiteContentTypeUpdated|Um usuário atualizou um tipo de conteúdo de site modificando uma ou mais propriedades.|
||||

### <a name="sharing-and-access-request-activities"></a>Atividades de compartilhamento e solicitação de acesso

A tabela a seguir descreve as atividades de compartilhamento e solicitação de acesso do usuário no SharePoint Online e no OneDrive for Business. Para eventos de compartilhamento, a coluna **Detalhes** em **Resultados** identifica o nome do usuário ou do grupo com o qual o item foi compartilhado e se esse usuário ou grupo é um membro ou convidado na sua organização. Para saber mais, veja [Usar a auditoria de compartilhamento no log de auditoria do Office 365](use-sharing-auditing.md).

> [!NOTE]
> Os usuários podem ser *membros* ou *convidados* com base na propriedade UserType do objeto de usuário. Um membro é geralmente um funcionário, enquanto um convidado é geralmente um colaborador fora da sua organização. Quando um usuário aceita um convite de compartilhamento (e ainda não faz parte da sua organização), uma conta de convidado é criada para ele no diretório da sua organização. Quando esse usuário convidado tem uma conta no seu diretório, recursos podem ser compartilhados diretamente com ele (sem a necessidade de um convite).

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Nível de permissão adicionado ao conjunto de sites|PermissionLevelAdded|Um nível de permissão foi adicionado a um conjunto de sites.|
|Solicitação de acesso aceita|AccessRequestAccepted|Uma solicitação de acesso a um site, pasta ou documento foi aceita, e o usuário solicitante recebeu acesso.|
|Convite de compartilhamento aceito|SharingInvitationAccepted|O usuário (membro ou convidado) aceitou um convite de compartilhamento e recebeu acesso a um recurso. Esse evento inclui informações sobre o usuário que foi convidado e sobre o endereço de email que foi usado para aceitar o convite (eles podem ser diferentes). Com frequência, essa atividade é acompanhada por um segundo evento que descreve como o usuário obteve acesso ao recurso; por exemplo, a adição do usuário a um grupo com acesso ao recurso.|
|Convite de compartilhamento bloqueado|SharingInvitationBlocked|Um convite de compartilhamento enviado por um usuário em sua organização é bloqueado devido a uma política de compartilhamento externo que permite ou nega o compartilhamento externo com base no domínio do usuário de destino. Nesse caso, o convite de compartilhamento foi bloqueado porque: <br/> O domínio do usuário de destino não está incluído na lista de domínios permitidos. <br/> Ou <br/> O domínio do usuário de destino está incluído na lista de domínios bloqueados. <br/> Confira mais informações sobre como permitir ou bloquear o compartilhamento externo com base em domínios em [Compartilhamento de domínios restritos no SharePoint Online e no OneDrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).|
|Solicitação de acesso criada|AccessRequestCreated|O usuário solicita acesso a um site, pasta ou documento que ele não tem permissões para acessar.|
|Link compartilhável da empresa criado |CompanyLinkCreated|O usuário criou um link de toda a empresa para um recurso. os links de toda a empresa só podem ser usados pelos membros da sua organização. Eles não podem ser usados por convidados.|
|Um link anônimo criado|AnonymousLinkCreated|O usuário criou um link anônimo para um recurso. Qualquer pessoa com esse link pode acessar o recurso sem ter que se autenticar.|
|Link seguro criado|SecureLinkCreated|Um link de compartilhamento seguro foi criado para esse item.|
|Convite de compartilhamento criado|SharingInvitationCreated|O usuário compartilhou um recurso do SharePoint Online ou do OneDrive for Business com um usuário que não está no diretório da sua organização.|
|Link seguro excluído|SecureLinkDeleted|Um link de compartilhamento seguro foi excluído.|
|Solicitação de acesso negada |AccessRequestDenied|Uma solicitação de acesso a um site, pasta ou documento foi negada.|
|Link compartilhável da empresa removido|CompanyLinkRemoved|O usuário removeu um link de empresa para um recurso. O link não pode mais ser usado para acessar o recurso.|
|Link anônimo removido|AnonymousLinkRemoved|O usuário removeu um link anônimo para um recurso. O link não pode mais ser usado para acessar o recurso.|
|Arquivo, pasta ou site compartilhado|SharingSet|O usuário (membro ou convidado) compartilhou um arquivo, uma pasta ou um site no SharePoint ou no OneDrive for Business com um usuário no diretório da sua organização. O valor na coluna **Detalhes** dessa atividade identifica o nome do usuário com o qual o recurso foi compartilhado e se esse usuário é um membro ou convidado. <br/><br/> Geralmente, essa atividade é acompanhada por um segundo evento que descreve como o usuário recebeu o acesso ao recurso. Por exemplo, a adição do usuário a um grupo com acesso ao recurso.|
|Solicitação de acesso atualizado|AccessRequestUpdated|Uma solicitação de acesso a um item foi atualizada.|
|Link anônimo atualizado |AnonymousLinkUpdated|O usuário atualizou um link anônimo para um recurso. O campo atualizado é incluído na propriedade EventData quando você exporta os resultados da pesquisa.|
|Convite de compartilhamento atualizado|SharingInvitationUpdated|Um convite de compartilhamento externo foi atualizado.|
|Link anônimo usado|AnonymousLinkUsed|Um usuário anônimo acessou um recurso usando um link anônimo. A identidade do usuário pode ser desconhecida, mas você pode obter outros detalhes, como seu endereço IP.|
|Arquivo, pasta ou site não compartilhado|SharingRevoked|O usuário (membro ou convidado) cancelou o compartilhamento de um arquivo, pasta ou site que havia sido compartilhado com outro usuário.|
|Link compartilhável da empresa usado|CompanyLinkUsed|O usuário acessou um recurso usando um link de empresa.|
|Link seguro usado|SecureLinkUsed|Um usuário usou um link seguro.|
|Usuário adicionado a um link seguro|AddedToSecureLink|Um usuário foi adicionado à lista de entidades que podem usar um link de compartilhamento seguro.|
|Usuário removido do link seguro|RemovedFromSecureLink|Um usuário foi removido da lista de entidades que podem usar um link de compartilhamento seguro.|
|Convite de compartilhamento retirado|SharingInvitationRevoked|O usuário retirou um convite de compartilhamento para um recurso. |
||||

### <a name="synchronization-activities"></a>Atividades de sincronização

A tabela a seguir lista as atividades de sincronização de arquivos no SharePoint Online e no OneDrive for Business.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Computador com permissão para sincronizar arquivos|ManagedSyncClientAllowed|O usuário estabelece com êxito uma relação de sincronização com um site. A relação de sincronização é bem-sucedida porque o computador do usuário é membro de um domínio que foi adicionado à lista de domínios (chamada de *lista de lista de destinatários seguros*) que podem acessar bibliotecas de documentos em sua organização. <br/><br/> Para obter mais informações sobre esse recurso, confira [Usar os cmdlets do Windows PowerShell para habilitar a sincronização do OneDrive para domínios que estão na Lista de Destinatários Confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).|
|Computador impedido de sincronizar arquivos|UnmanagedSyncClientBlocked|O usuário tenta estabelecer uma relação de sincronização com um site em um computador que não é membro do domínio da sua organização ou que é membro de um domínio que não foi adicionado à lista de domínios (chamada de *lista de destinatários seguros*) que podem acessar bibliotecas de documentos na sua organização. A relação de sincronização não é permitida e o computador do usuário é impedido de sincronizar, fazer download ou fazer upload de arquivos em uma biblioteca de documentos. <br/><br/> Para obter informações sobre esse recurso, confira [Usar os cmdlets do Windows PowerShell para habilitar a sincronização do OneDrive para domínios que estão na Lista de Destinatários Confiáveis](https://go.microsoft.com/fwlink/p/?LinkID=534609).|
|Arquivos baixados no computador|FileSyncDownloadedFull|O usuário estabelece uma relação de sincronização e baixa arquivos de uma biblioteca de documentos com êxito pela primeira vez em seu computador.|
|Alterações de arquivo baixadas no computador|FileSyncDownloadedPartial|O usuário baixa com êxito quaisquer alterações nos arquivos de uma biblioteca de documentos. Essa atividade indica que todas as alterações que foram feitas nos arquivos da biblioteca de documentos foram baixadas no computador do usuário. Apenas as alterações foram baixadas porque a biblioteca de documentos já foi baixada pelo usuário (conforme indicado pela atividade **Arquivos baixados no computador**).|
|Arquivos carregados na biblioteca de documentos|FileSyncUploadedFull|O usuário estabelece uma relação de sincronização e carrega arquivos em uma biblioteca de documentos com êxito pela primeira vez em seu computador.|
|Alterações de arquivo carregadas na biblioteca de documentos|FileSyncUploadedPartial|O usuário carrega com êxito em uma biblioteca de documentos as alterações feitas em arquivos. Esse evento indica que quaisquer alterações feitas na versão local de um arquivo de uma biblioteca de documentos foram carregadas com êxito para a biblioteca de documentos. Apenas alterações são carregadas porque esses arquivos já foram carregados pelo usuário (conforme indicado pela atividade **Arquivos carregados na biblioteca de documentos**).|
||||

### <a name="site-permissions-activities"></a>Atividades de permissões de site

A tabela a seguir lista os eventos relacionados para atribuir permissões no SharePoint e usar grupos para conceder (e revogar) acesso aos sites.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Administrador de conjunto de sites adicionado|SiteCollectionAdminAdded|O proprietário ou administrador do conjunto de sites adiciona uma pessoa como administrador de conjunto de sites para um site. Os administradores do conjunto de sites têm permissões de controle total para o conjunto de sites e todos os subsites. Essa atividade também será registrada quando um administrador conceder acesso a uma conta do usuário do Onedrive (editando o perfil do usuário no centro de administração do SharePoint ou [usando o centro de administração do Microsoft 365](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)).|
|Usuário ou grupo adicionado ao grupo do SharePoint|AddedToGroup|O usuário adicionou um membro ou convidado a um grupo do SharePoint. Esta pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento de compartilhamento.|
|Herança de nível de permissão interrompida|PermissionLevelsInheritanceBroken|Um item foi alterado para que ele não mais herde os níveis de permissão de seu pai.|
|Compartilhamento de herança interrompido|SharingInheritanceBroken|Um item foi alterado para que não herde mais as permissões de compartilhamento de seu pai.|
|Grupo criado|GroupAdded|O proprietário ou administrador do site cria um grupo para um site ou realiza uma tarefa que resulta na criação de um grupo. Por exemplo, na primeira vez que um usuário cria um link para compartilhar um arquivo, um grupo de sistemas é adicionado ao site do OneDrive for Business do usuário. Esse evento também pode ser o resultado de um usuário ter criado um link com permissões de edição para um arquivo compartilhado.|
|Grupo excluído|GroupRemoved|O usuário exclui um grupo de um site.|
|Configuração da solicitação de acesso modificada|WebRequestAccessModified|As configurações de solicitação de acesso foram modificadas em um site.|
|Configuração “Membros Podem Compartilhar" modificado|WebMembersCanShareModified|A configuração **Membros Podem Compartilhar** foi modificada em um site.|
|Nível de permissão modificado no conjunto de sites|PermissionLevelModified|Um nível de permissão foi alterado em um conjunto de sites.|
|Permissões de site modificadas|SitePermissionsModified|O proprietário ou administrador do site (ou a conta do sistema) altera o nível de permissão que é atribuído a um grupo em um site. Essa atividade também será registrada se todas as permissões forem removidas de um grupo. <br/><br/> **OBSERVAÇÃO**: Esta operação foi preterida no SharePoint Online. Para localizar os eventos relacionados, você pode procurar outras atividades relacionadas à permissão, como **Administrador do conjunto de sites adicionado**, **Usuário ou grupo adicionado ao grupo do SharePoint**, **Usuário permitido para criar grupo**, **Grupo criado**, e **Grupo excluído.**|
|Nível de permissão removido do conjunto de sites|PermissionLevelRemoved|Um nível de permissão foi removido de um conjunto de sites.|
|Administrador de conjunto de sites removido|SiteCollectionAdminRemoved|O proprietário ou administrador do conjunto de sites remove uma pessoa como administrador de conjunto de sites para um site. Essa atividade também será registrada quando um administrador remover a si mesmo da lista de administradores de conjunto de sites para a conta do usuário do OneDrive (editando o perfil de usuário no centro de administração do SharePoint).  Para retornar essa atividade nos resultados de pesquisa do log de auditoria, é preciso procurar todas as atividades.|
|Usuário ou grupo removido do grupo do SharePoint|RemovedFromGroup|O usuário removeu um membro ou convidado de um grupo do SharePoint. Essa pode ter sido uma ação intencional ou o resultado de outra atividade, como um evento de cancelamento de compartilhamento.|
|Permissões de administrador de site solicitadas|SiteAdminChangeRequest|O usuário solicita ser adicionado como administrador do conjunto de sites para um conjunto de sites. Os administradores do conjunto de sites têm permissões de controle total para o conjunto de sites e todos os subsites.|
|Herança de compartilhamento restaurada|SharingInheritanceReset|Uma alteração foi feita para que um item herde permissões de compartilhamento de seu pai.|
|Grupo atualizado|GroupUpdated|O proprietário ou administrador do site altera as configurações de um grupo para um site. Isso pode incluir a alteração do nome do grupo, quem pode visualizar ou editar os membros do grupo e como as solicitações de associação são tratadas.|
||||

### <a name="site-administration-activities"></a>Atividades de administração do site

A tabela a seguir lista os eventos decorrentes de tarefas de administração de sites no SharePoint Online.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Local de dados permitido adicionado|AllowedDataLocationAdded|Um administrador global ou do SharePoint adicionou um local de dados permitido em um ambiente multigeográfico.|
|Agente de usuário isento adicionado|ExemptUserAgentSet|Um administrador global ou do SharePoint adicionou um agente de usuário à lista de agentes de usuário isentos no centro de administração do SharePoint.|
|Administrador de localização geográfica adicionado|GeoAdminAdded|Um administrador global ou do SharePoint adicionou um usuário como um administrador geográfico de um local.|
|Usuário com permissão para criar grupos|AllowGroupCreationSet|O proprietário ou administrador do site adiciona um nível de permissão a um site, que permite que um usuário com essa permissão crie um grupo para esse site.|
|Movimento geográfico do site cancelado|SiteGeoMoveCancelled|Um administrador global ou do SharePoint cancela com êxito uma movimentação geográfica do site do SharePoint ou do OneDrive. As funcionalidades multigeográficas permitem que uma organização do Office 365 abranja várias regiões geográficas do datacenter do Office 365 chamadas de áreas geográficas. Para obter mais informações, confira [Funcionalidades multigeográficas do Onedrive e do SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Política de compartilhamento alterada|SharingPolicyChanged|Um administrador global ou do SharePoint alterou uma política de compartilhamento do SharePoint usando o portal de administração do Office 365, o portal de administração do SharePoint ou o Shell de Gerenciamento do SharePoint Online. Qualquer alteração nas configurações da política de compartilhamento na sua organização será registrada. A política que foi alterada é identificada no campo **ModifiedProperties** nas propriedades detalhadas do registro de evento.|
|Política de acesso a dispositivo alterada|DeviceAccessPolicyChanged|Um administrador global ou do SharePoint alterou a política de dispositivos não gerenciados para sua organização. Esta política controla o acesso ao SharePoint, OneDrive e ao Office 365 de dispositivos que não estão associados à sua organização. Configurar esta política requer uma assinatura do Enterprise Mobility + Security. Para obter informações, consulte [Controlar o acesso de dispositivos gerenciados](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).|
|Agentes de usuário isentos alterados|CustomizeExemptUsers|Um administrador global ou do SharePoint personalizou a lista de agentes de usuário isentos no centro de administração do SharePoint. Você pode especificar quais agentes de usuário devem ficar isentos de receber uma página da Web inteira para indexar. Isso significa que, quando um agente do usuário que você especificou como isento encontrar um formulário do InfoPath, o formulário será retornado como um arquivo XML em vez de uma página da Web completa. Isso torna a indexação de formulários do InfoPath mais rápida.|
|Política de acesso à rede alterada|NetworkAccessPolicyChanged|Um administrador global do ou do SharePoint alterou a política de acesso baseado no local (também chamada de limite de rede confiável) no centro de administração do SharePoint ou usando o PowerShell do SharePoint Online. Esse tipo de política controla quem pode acessar os recursos do SharePoint e do OneDrive em sua organização com base em intervalos de endereços IP autorizados, especificados por você. Para saber mais, confira [Controlar o acesso aos dados do SharePoint Online e do Onedrive com base no local de rede](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).|
|Movimentação geográfica do site concluída|SiteGeoMoveCompleted|Uma movimentação geográfica do site que foi agendada por um administrador global em sua organização foi concluído com sucesso.  As funcionalidades multigeográficas permitem que uma organização do Office 365 abranja várias regiões geográficas do datacenter do Office 365 chamadas de áreas geográficas. Para obter mais informações, confira [Funcionalidades multigeográficas do Onedrive e do SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Conexão Enviar Para criada|SendToConnectionAdded|Um administrador global ou do SharePoint cria uma nova conexão Enviar Para na página de gerenciamento de Registros no centro de administração do SharePoint. Uma conexão Enviar para especifica configurações para um repositório de documentos ou um centro de registros. Quando você cria uma conexão Enviar para, um Organizador de Conteúdo pode enviar documentos à localização especificada.|
|Conjunto de sites criado|SiteCollectionCreated|Um administrador global ou do SharePoint cria um conjunto de sites na sua organização do SharePoint Online ou um usuário provisiona seu site do OneDrive for Business.|
|Site do hub órfão excluído|HubSiteOrphanHubDeleted|Um administrador global ou do SharePoint excluiu um site do hub órfão, que é um site do hub que não tem sites associados a ele. Um hub órfão provavelmente é causado pela exclusão do site do hub original.|
|Conexão Enviar Para excluída|SendToConnectionRemoved|Um administrador global ou do SharePoint exclui uma conexão Enviar Para na página de gerenciamento de Registros no centro de administração do SharePoint.|
|Site excluído|SiteDeleted|O administrador do site exclui um arquivo.|
|Visualização de documentos habilitada|PreviewModeEnabledSet|O administrador do site habilita a visualização de documentos para um site.|
|Fluxo de trabalho legado habilitado|LegacyWorkflowEnabledSet|O proprietário ou administrador do site adiciona o tipo de conteúdo da Tarefa de Fluxo de Trabalho do SharePoint 2013 ao site. Os administradores globais também podem ativar fluxos de trabalho para toda a organização no centro de administração do SharePoint.|
|Office on Demand habilitado|OfficeOnDemandSet|O administrador do site habilita o Office on Demand, que permite aos usuários acessar a versão mais recente dos aplicativos da área de trabalho do Office. O Office on Demand está habilitado no Centro de administração do SharePoint e exige uma assinatura do Office 365 que inclua aplicativos completos do Office instalados.|
|Fonte de resultados habilitada para Pesquisas de Pessoas|PeopleResultsScopeSet|O administrador do site cria a fonte de resultado para Pesquisas de Pessoas em um site.|
|RSS feeds habilitados|NewsFeedEnabledSet|O proprietário ou administrador do site habilita RSS feeds para um site. Os administradores globais podem ativar RSS feeds para toda a organização no centro de administração do SharePoint.|
|Site associado ao site do hub|HubSiteJoined|Um proprietário de site associa seus sites a um site do hub.|
|Site do hub registrado|HubSiteRegistered|Um administrador global ou do SharePoint cria um site do hub. Os resultados são que o site é registrado para ser um site do hub.|
|Local de dados permitido removido|AllowedDataLocationDeleted|Um administrador global ou do SharePoint removeu um local de dados permitido em um ambiente multigeográfico.|
|Administrador de localização geográfica removido|GeoAdminDeleted|Um administrador global ou do SharePoint removeu um usuário como um administrador geográfico de um local.|
|Site renomeado|SiteRenamed|O proprietário ou administrador do site renomeia um site|
|Movimentação geográfica do site agendada|SiteGeoMoveScheduled|Um administrador global ou do SharePoint agenda com êxito uma movimentação geográfica do site do SharePoint ou do OneDrive. As funcionalidades multigeográficas permitem que uma organização do Office 365 abranja várias regiões geográficas do datacenter do Office 365 chamadas de áreas geográficas. Para obter mais informações, confira [Funcionalidades multigeográficas do Onedrive e do SharePoint Online no Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Definir site do host|HostSiteSet|Um administrador global ou do SharePoint altera o site designado para hospedar sites pessoais ou do OneDrive for Business.|
|Definir a cota de armazenamento para uma localização geográfica|GeoQuotaAllocated|Um administrador global ou do SharePoint configurou a cota de armazenamento para uma localização geográfica em um ambiente multigeográfico.|
|Site desvinculado do site do hub|HubSiteUnjoined|Um proprietário de site dissocia o site de um site do hub.|
|Site do hub não registrado|HubSiteUnregistered|Um administrador global ou do SharePoint cancela registro de um site como um site do hub. Quando o registro de um site do hub é cancelado, ele não funciona mais como um site do hub.|
||||

### <a name="exchange-mailbox-activities"></a>Atividades de caixa de correio do Exchange

A tabela a seguir lista as atividades que podem ser registradas pelo log de auditoria da caixa de correio. As atividades de caixa de correio executadas pelo proprietário da caixa de correio, por um usuário delegado ou por um administrador do são automaticamente registradas no log de auditoria do Office 365 por até 90 dias. É possível que um administrador desabilite o registro em log de auditoria da caixa de correio para todos os usuários em sua organização. Nesse caso, nenhuma ação da caixa de correio do usuário será registrada. Para saber mais, consulte [Gerenciar a auditoria da caixa de correio](enable-mailbox-auditing.md).

 Você também pode procurar atividades de caixa de correio usando o cmdlet [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) no PowerShell do Exchange Online.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Permissões de caixa de correio delegada adicionadas|AddMailboxPermissions|Um administrador atribuiu a um usuário (conhecido como um representante) a permissão da caixa de correio FullAccess para a caixa de correio de outra pessoa. A permissão FullAccess permite que o representante abra a caixa de correio de outra pessoa e leia e gerencie o conteúdo da caixa de correio.|
|Adicionado ou removido usuário com acesso delegado à pasta de calendário|UpdateCalendarDelegation|Um usuário foi adicionado ou removido como um representante para o calendário da caixa de correio de outro usuário. A delegação de calendário concede a outra pessoa na mesma organização permissões para gerenciar o calendário do proprietário da caixa de correio.|
|Permissões adicionadas à pasta|AddFolderPermissions|Uma permissão da pasta foi adicionada. As permissões de pasta controlam quais usuários da sua organização podem acessar as pastas em uma caixa de correio e as mensagens localizadas nessas pastas.|
|Mensagens copiadas para outra pasta|Copiar|Uma mensagem foi copiada para outra pasta.|
|Criação de item de caixa de correio|Criar|Um item é criado nas pastas Calendário, Contatos, Anotações ou Tarefas da caixa de correio. Por exemplo, uma nova solicitação de reunião é criada. Criar, enviar ou receber uma mensagem não é auditada. Criar pastas de caixa de correio também não é uma ação auditada.|
|Criada nova regra da caixa de entrada do Outlook Web App|New-InboxRule|Um proprietário da caixa de correio ou outro usuário com acesso à caixa de correio criou uma regra da caixa de entrada do Outlook Web App.|
|Mensagens excluídas da pasta Itens Excluídos|SoftDelete|Uma mensagem foi permanentemente excluída ou foi excluída da pasta Itens Excluídos. Esses itens são movidos para a pasta Itens Recuperáveis. As mensagens também são movidas para a pasta Itens Recuperáveis quando um usuário as seleciona e pressiona **Shift+Delete**.|
|Mensagem rotulada como um registro|ApplyRecordLabel|Uma mensagem foi classificada como um registro. Isso ocorre quando um rótulo de retenção que classifica o conteúdo como um registro é automaticamente aplicado a uma mensagem.|
|Mensagens movidas para outra pasta|Mover|Uma mensagem foi movida para outra pasta.|
|Mensagens movidas para a pasta Itens Excluídos|MoveToDeletedItems|Uma mensagem foi excluída e movida para a pasta Itens Excluídos.|
|Permissão de pasta modificada|UpdateFolderPermissions|Uma permissão da pasta foi alterada. As permissões de pasta controlam quais usuários da organização podem acessar as pastas de uma caixa de correio e as mensagens incluídas nessas pastas.|
|Modificada regra de caixa de entrada do Outlook Web App|Set-InboxRule|Um proprietário da caixa de correio ou outro usuário com acesso à caixa de correio modificou uma regra da caixa de entrada usando o Outlook Web App.|
|Mensagens limpas da caixa de correio|HardDelete|Uma mensagem foi limpa da pasta Itens Recuperáveis (permanentemente excluída da caixa de correio).|
|Permissões de caixa de correio do representante removidas|Remove-MailboxPermission|Um administrador removeu a permissão FullAccess (que foi atribuída a um representante) da caixa de correio de uma pessoa. Depois que a permissão FullAccess for removida, o representante não pode abrir a caixa de correio de outra pessoa ou acessar nenhum conteúdo dela.|
|Permissões removidas da pasta|RemoveFolderPermissions|Uma permissão da pasta foi removida. As permissões de pasta controlam quais usuários da sua organização podem acessar as pastas em uma caixa de correio e as mensagens localizadas nessas pastas.|
|Mensagem enviada com permissões Enviar Como|SendAs|Uma mensagem foi enviada usando a permissão SendAs. Isto significa que outro usuário enviou a mensagem como se ela tivesse vindo do proprietário da caixa de correio.|
|Mensagem enviada com permissões Enviar em Nome de|SendOnBehalf|Uma mensagem foi enviada usando a permissão SendOnBehalf. Isto significa que outro usuário enviou a mensagem em nome do proprietário da caixa de correio. A mensagem indica ao destinatário em nome de quem a mensagem foi enviada e quem realmente a enviou.|
|Regras atualizadas da caixa de entrada do cliente do Outlook|UpdateInboxRules|Um proprietário da caixa de correio ou outro usuário com acesso à caixa de correio modificou uma regra da caixa de entrada no cliente do Outlook.|
|Mensagem atualizada|Atualizar|Uma mensagem ou suas propriedades foram alteradas.|
|Usuário entrou na caixa de correio|MailboxLogin|O usuário entrou em sua caixa de correio.|
||||

### <a name="sway-activities"></a>Atividades do Sway

A tabela a seguir lista as atividades de usuários e administradores no Sway. O Sway é um aplicativo do Office 365 que ajuda os usuários a reunirem, formatarem e compartilharem ideias, histórias e apresentações em uma tela interativa baseada na Web. Para saber mais, confira [Perguntas frequentes sobre o Sway – Ajuda do administrador](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Nível de compartilhamento do Sway alterado|SwayChangeShareLevel|O usuário altera o nível de compartilhamento de um Sway. Esse evento captura o usuário alterando o escopo de compartilhamento associado a um Sway, por exemplo, público versus dentro da organização.|
|Sway criado|SwayCreate|O usuário cria um Sway.|
|Sway excluído|SwayDelete|O usuário exclui um Sway.|
|Duplicação do Sway desabilitada|SwayDisableDuplication|O usuário desabilita a duplicação de um Sway.|
|Sway duplicado|SwayDuplicate|O usuário duplica um Sway.|
|Sway editado|SwayEdit|O usuário edita um Sway.|
|Duplicação do Sway habilitada|EnableDuplication|O usuário habilita a duplicação de um Sway. A capacidade de um usuário habilitar a duplicação de um Sway habilitada por padrão.|
|Compartilhamento do Sway revogado|SwayRevokeShare|O usuário para de compartilhar um Sway revogando o acesso a ele. Revogar o acesso altera os links associados a um Sway.|
|Sway compartilhado|SwayShare|O usuário pretende compartilhar um Sway. Esse evento captura a ação do usuário de clicar em um destino de compartilhamento específico no menu de compartilhamento do Sway. O evento não indica se o usuário concluiu a ação de compartilhamento.|
|Compartilhamento externo do Sway desativado|SwayExternalSharingOff|O administrador desabilita o compartilhamento externo do Sway para toda a organização usando o centro de administração do Microsoft 365.|
|Compartilhamento externo do Sway ativado|SwayExternalSharingOn|O administrador habilita o compartilhamento externo do Sway para toda a organização usando o centro de administração do Microsoft 365.|
|Serviço do Sway desativado|SwayServiceOff|O administrador desabilita o Sway para toda a organização usando o centro de administração do Microsoft 365.|
|Serviço do Sway ativado|SwayServiceOn|O administrador habilita o Sway para toda a organização usando o centro de administração do Microsoft 365 (o serviço do Sway está habilitado por padrão).|
|Sway visualizado|SwayView|O usuário exibe um Sway.|
||||

### <a name="user-administration-activities"></a>Atividades de administração de usuários

A tabela a seguir lista as atividades de administração de usuários que são registradas quando um administrador adiciona ou altera uma conta de usuário usando o Microsoft 365 ou o portal de gerenciamento do Azure.

|**Atividade**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Usuário adicionado|Adicionar usuário|Uma conta de usuário do Office 365 foi criada.|
|Licença de usuário alterada|Alterar licença de usuário|A licença atribuída a um usuário foi alterada. Para ver quais licenças foram alteradas, veja a atividade **Usuário atualizado** correspondente.|
|Senha do usuário alterada|Alterar senha do usuário|O administrador alterou a senha de um usuário.|
|Usuário excluído|Excluir usuário|Uma conta de usuário do Office 365 foi excluída.|
|Redefinir senha do usuário|Redefinir senha do usuário|O administrador redefiniu a senha de um usuário.|
|Propriedade definida que força o usuário a alterar a senha|Definir alteração forçada de senha do usuário|O administrador definiu a propriedade que força o usuário a redefinir a senha da próxima vez que esse usuário entrar no Office 365.|
|Definir propriedades de licenças|Definir propriedades de licenças|O administrador modifica as propriedades de uma licença atribuída a um usuário.|
|Usuário atualizado|Atualizar usuário|O administrador altera uma ou mais propriedades de uma conta de usuário. Para obter uma lista de propriedades do usuário que podem ser atualizadas, veja a seção "Atualizar atributos do usuário" em [Eventos de relatório de auditoria do Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).|
||||

### <a name="azure-ad-group-administration-activities"></a>Atividades de administração de grupos do Azure AD

A tabela a seguir lista as atividades de administração de grupos que são registradas quando um administrador ou um usuário cria ou altera um grupo do Office 365 ou quando um administrador cria um grupo de segurança usando o Microsoft 365 ou o portal de gerenciamento do Azure. Para saber mais sobre grupos no Office 365, confira [Exibir, criar e excluir Grupos no centro de administração do Microsoft 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Grupo adicionado|Adicionar grupo|Um grupo foi criado.|
|Membro adicionado ao grupo|Adicionar membro ao grupo|Um membro foi adicionado a um grupo.|
|Grupo excluído|Excluir grupo|Um grupo foi excluído.|
|Membro removido do grupo|Remover membro do grupo|Um membro foi removido de um grupo.|
|Grupo atualizado|Atualizar grupo|Uma propriedade de um grupo foi alterada.|
||||

### <a name="application-administration-activities"></a>Atividades de administração de aplicativos

A tabela a seguir lista atividades de administração de aplicativos que são registradas quando um administrador adiciona ou altera um aplicativo que está registrado no Azure AD. Qualquer aplicativo que depende do Azure AD para autenticação deve ser registrado no diretório.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Entrada da delegação adicionada|Adicionar entrada de delegação|Uma permissão de autenticação foi criada/concedida a um aplicativo no Azure AD.|
|Entidade de serviço adicionada|Adicionar entidade de serviço|Um aplicativo foi registrado no Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.|
|Credenciais adicionadas a uma entidade de serviço |Adicionar credenciais de entidade de serviço|Credenciais foram adicionadas a uma entidade de serviço no Azure AD. Uma entidade de serviço representa um aplicativo no diretório.|
|Entrada de delegação removida|Remover entrada de delegação|Uma permissão de autenticação foi removida de um aplicativo no Azure AD.|
|Entidade de serviço removida do diretório|Remover entidade de serviço|Um aplicativo foi excluído/teve o registro cancelado do Azure AD. Um aplicativo é representado por uma entidade de serviço no diretório.|
|Credenciais removidas de uma entidade de serviço |Remover credenciais da entidade de serviço|Credenciais foram removidas de uma entidade de serviço no Azure AD. Uma entidade de serviço representa um aplicativo no diretório.|
|Definir entrada de delegação|Definir entrada de delegação|Uma permissão de autenticação foi atualizada para um aplicativo no Azure AD.|
||||

### <a name="role-administration-activities"></a>Atividades de administração de funções

A tabela a seguir lista as atividades de administração de funções do Azure AD registradas quando um administrador gerencia funções de administração no Microsoft 365 ou no portal de gerenciamento do Azure.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Adicionar membro à função|Adicionar membro de função à função|Usuário adicionado a uma função de administração no Office 365.|
|Usuário removido de uma função de diretório|Remover membro de função da função|Usuário removido de uma função de administração no Office 365.|
|Definir informações de contato da empresa|Definir informações de contato da empresa|Preferências de contato no nível da empresa atualizadas para a sua organização do Office 365. Isso inclui endereços de email para emails relacionados a assinaturas enviados pelo Office 365 e notificações técnicas sobre os serviços do Office 365.|
||||

### <a name="directory-administration-activities"></a>Atividades de administração de diretórios

A tabela a seguir lista as atividades relacionadas a diretórios e domínios do Azure AD que são registradas quando um administrador gerencia sua organização do Office 365 no centro de administração do Microsoft 365 ou no portal de gerenciamento do Azure.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Domínio adicionado à empresa|Adicionar domínio à empresa|Adicionado um domínio à sua organização do Office 365.|
|Parceiro adicionado ao diretório|Parceiro adicionado à empresa|Parceiro (administrador delegado) adicionado à sua organização do Office 365.|
|Domínio removido da empresa|Remover domínio da empresa|Domínio removido da sua organização do Office 365.|
|Parceiro removido do diretório|Remover parceiro da empresa|Parceiro (administrador delegado) removido da sua organização do Office 365.|
|Definir informações da empresa|Definir informações da empresa|Informações da empresa atualizadas para a sua organização do Office 365. Isso inclui endereços de email para emails relacionados a assinaturas enviados pelo Office 365 e notificações técnicas sobre os serviços do Office 365.|
|Definir autenticação de domínio|Definir autenticação de domínio|Configuração de autenticação de domínio alterada para a sua organização do Office 365.|
|Configurações de federação atualizadas para um domínio|Definir configurações de federação no domínio|Configurações de federação (compartilhamento externo) alteradas para a sua organização do Office 365.|
|Definir política de senha|Definir política de senha|As restrições de comprimento e caracteres alteradas para senhas de usuário na sua organização do Office 365.|
|Sincronização do Azure AD ativada|Definir sinalizador DirSyncEnabled ativado na empresa|Definir a propriedade que habilita um diretório para sincronização do Azure AD.|
|Domínio atualizado|Atualizar domínio|Configurações de um domínio atualizadas na sua organização do Office 365.|
|Domínio verificado|Verificar domínio|Foi verificado que a sua organização é a proprietária de um domínio.|
|Domínio confirmado de email verificado|Verificar domínio confirmado de email|Verificação de email usada para confirmar que a sua organização é proprietária de um domínio.|
||||

### <a name="ediscovery-activities"></a>Atividades de Descoberta Eletrônica

Atividades relacionadas a Pesquisa de Conteúdo e Descoberta Eletrônica que são realizadas no centro de segurança e conformidade ou ao executar os cmdlets do PowerShell correspondentes são registradas no log de auditoria. Isso inclui as seguintes atividades:

- Criar e gerenciar casos de Descoberta Eletrônica

- Criar, iniciar e editar pesquisas de conteúdo

- Executar ações de pesquisa de conteúdo, como visualização, exportação e exclusão de resultados de pesquisa

- Configurar a filtragem de permissões para pesquisa de conteúdo

- Gerenciar a função de administrador de Descoberta Eletrônica

Para obter uma lista e uma descrição detalhada das atividades de Descoberta Eletrônica que são registradas, veja [Procurar atividades de Descoberta Eletrônica no log de auditoria do Office 365](search-for-ediscovery-activities-in-the-audit-log.md).

> [!NOTE]
> Demora até 30 minutos para os eventos resultantes das atividades listadas em **Atividades de Descoberta Eletrônica** na lista suspensa das **Atividades** serem exibidos nos resultados da pesquisa. Por outro lado, leva até 24 horas para que os eventos correspondentes das atividades de cmdlet de Descoberta Eletrônica apareçam nos resultados da pesquisa.

### <a name="advanced-ediscovery-activities"></a>Atividades de Descoberta Eletrônica Avançada

A tabela a seguir lista as atividades resultantes de profissionais de TI e profissionais legais que realizam tarefas de Descoberta Eletrônica Avançada no Microsoft 365. Para obter mais informações, confira [Visão geral da solução de Descoberta Eletrônica Avançada no Microsoft 365](compliance20/overview-ediscovery-20.md).

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Adicionar dados a outro conjunto de revisão|AddWorkingSetQueryToWorkingSet|O usuário adicionou documentos de uma revisão definida para outro conjunto de revisão.|
|Dados adicionados ao conjunto de revisão|AddQueryToWorkingSet|O usuário adicionou os resultados da pesquisa de uma pesquisa de conteúdo associada a um caso de Descoberta Eletrônica Avançada a um conjunto de revisão.|
|Dados que não são do Office 365 a conjunto de revisão|AddNonOffice365DataToWorkingSet|O usuário adicionou dados que não são do Office 365 a um conjunto de revisão.|
|Documentos remedidos adicionados ao conjunto de revisão|AddRemediatedData|O usuário carrega documentos com erros de indexação corrigidos em um conjunto de revisão.|
|Dados analisados no conjunto de revisão|RunAlgo|O usuário realizou a análise nos documentos em um conjunto de revisão.|
|Documento com anotações no conjunto de revisão|AnnotateDocument|O usuário anota um documento em um conjunto de revisão. As anotações incluem a redação de conteúdo em um documento.|
|Conjuntos de carga comparados|LoadComparisonJob|O usuário comparou dois conjuntos de carga diferentes em um conjunto de revisão. Um conjunto de carga é quando os dados de uma pesquisa de conteúdo que estão associados ao caso são adicionados a um conjunto de revisão.|
|Documentos redigidos convertidos em PDF|BurnJob|O usuário converteu todos os documentos redigidos em uma revisão definida como arquivos PDF.|
|Conjunto de revisão criado|CreateWorkingSet|O usuário criou um conjunto de revisão.|
|Pesquisa de conjunto de revisão criada|CreateWorkingSetSearch|O usuário criou uma consulta de pesquisa que procura os documentos em um conjunto de revisão.|
|Marca criada|CreateTag|O usuário criou um grupo de marcas em um conjunto de revisão. Um grupo de marcas pode conter uma ou mais marcas filho. Essas marcas são usadas para marcar documentos no conjunto de revisão.|
|Pesquisa do conjunto de revisão excluído|DeleteWorkingSetSearch|O usuário excluiu uma consulta de pesquisa em um conjunto de revisão.|
|Marca excluída|DeleteTag|O usuário excluiu um grupo de marcas em um conjunto de revisão.|
|Documento baixado|DownloadDocument|O usuário baixou um documento de um conjunto de revisão.|
|Marca editada|DownloadDocument|O usuário alterou uma marca em um conjunto de revisão.|
|Documentos exportados do conjunto de revisão|ExportJob|O usuário exporta documentos de um conjunto de revisão.|
|Configuração de caso modificado|UpdateCaseSettings|O usuário modifica as configurações de uma ocorrência. As configurações da ocorrência incluem informações sobre o caso, permissões de acesso e configurações que controlam o comportamento da pesquisa e da análise.|
|Pesquisa do conjunto de revisão modificada|UpdateWorkingSetSearch|O usuário editou uma consulta de pesquisa em um conjunto de revisão.|
|Pesquisa do conjunto de revisão vizualizada|PreviewWorkingSetSearch|O usuário visualizou os resultados de uma consulta de pesquisa em um conjunto de revisão.|
|Documentos de erro corrigidos|ErrorRemediationJob|O usuário corrige os arquivos que contêm erros de indexação.|
|Documento marcado|TagFiles|O usuário marca um documento em um conjunto de revisão.|
|Resultados marcados de uma consulta|TagJob|O usuário marca todos os documentos que correspondem aos critérios da consulta de pesquisa em um conjunto de revisão.|
|Documento exibido no conjunto de revisão|ViewDocument|O usuário visualiza um documento em um conjunto de revisão.|
|||

### <a name="power-bi-activities"></a>Atividades do Power BI

Você pode pesquisar o log de auditoria das atividades do Power BI. Para saber mais sobre as atividades do Power bi, confira a seção "Atividades auditadas pelo Power bi" em [Usando a auditoria dentro da sua organização](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).

O log de auditoria do Power BI não está habilitado por padrão. Para pesquisar as atividades do Power BI no log de auditoria do Office 365, habilite o recurso de auditoria no portal de administração do Power BI. Para obter instruções, confira a seção "logs de auditoria" no [portal de administração do Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).

### <a name="microsoft-workplace-analytics-activities"></a>Atividades do Microsoft Workplace Analytics

O Workplace Analytics fornece informação de como os grupos colaboram em sua organização do Office 365. A tabela a seguir lista as atividades executadas pelos usuários que recebem a função de Administrador ou as funções de Analista no Workplace Analytics. Os usuários que receberam a função de Analista têm acesso total a todos os recursos de serviço e usam o produto para fazer análise. Os usuários que receberam a função de Administrador podem definir as configurações de privacidade e os padrões do sistema, além de poder preparar, carregar e verificar dados organizacionais no Workplace Analytics. Para saber mais, confira [Workplace Analytics](https://docs.microsoft.com/pt-BR/workplace-analytics/index-orig).

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Link OData acessado|AccessedOdataLink|O analista acessou o link OData para uma consulta.|
|Consulta cancelada|CanceledQuery|O analista cancelou uma consulta em execução.|
|Exclusão de reunião criada|MeetingExclusionCreated|O analista criou uma regra de exclusão de reunião.|
|Resultado excluído|DeletedResult|O analista excluiu um resultado de consulta.|
|Relatório baixado|DownloadedReport|O analista baixou um arquivo de resultado da consulta.|
|Consulta executada|ExecutedQuery|O analista executou uma consulta.|
|Configuração do acesso a dados atualizada|UpdatedDataAccessSetting|O administrador atualizou as configurações de acesso a dados.|
|Configuração de privacidade atualizada|UpdatedPrivacySetting|O administrador atualizou as configurações de privacidade; por exemplo, tamanho mínimo do grupo.|
|Dados da organização carregados|UploadedOrgData|O administrador carregou um arquivo de dados organizacional.|
|Exploração Exibida|ViewedExplore|O analista exibiu as visualizações em uma ou mais guias da página de Exploração.|
||||

### <a name="microsoft-teams-activities"></a>Atividades do Microsoft Teams

A tabela a seguir lista as atividades de usuários e de administradores no Microsoft Teams que estejam conectados ao log de auditoria do Office 365. O Microsoft Teams é um espaço de trabalho centralizado em chat no Office 365. Ele reúne as conversas, reuniões, arquivos e anotações da equipe em um único lugar. Para obter mais informações e links para os tópicos da Ajuda, confira:

- [Perguntas frequentes sobre o Microsoft Teams – Ajuda para Administradores](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)

- [Ajuda do Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Bot adicionado à equipe|BotAddedToTeam|Um usuário adiciona um bot a uma equipe.|
|Canal adicionado|ChannelAdded|Um usuário adiciona um canal a uma equipe.|
|Conector adicionado|ConnectorAdded|Um usuário adiciona um conector a um canal.|
|Membros adicionados à equipe|MemberAdded|Um proprietário da equipe adiciona membros à uma equipe.|
|Guia adicionada|TabAdded|Um usuário adiciona uma guia a um canal.|
|Configuração de canal alterada|ChannelSettingChanged|A operação ChannelSettingChanged é registrada em log quando as seguintes atividades são realizadas por um membro da equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada entre parênteses abaixo) é exibida na coluna **Item** nos resultados da pesquisa do log de auditoria. <br/><br/>• Altera o nome de um canal de equipe (**Nome do canal**). <br/><br/>• Altera a descrição de um canal de equipe (**Descrição do canal**).|
|Configuração da organização alterada|TeamsTenantSettingChanged|A operação TeamsTenantSettingChanged é registrada em log quando as seguintes atividades são executadas por um administrador global (usando o centro de administração do Microsoft 365). Observe que essas atividades afetam as configurações do Microsoft Teams em toda a organização. Para obter mais informações, confira [Configurações do administrador para Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2). <br/> Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada entre parênteses abaixo) é exibida na coluna **Item** nos resultados da pesquisa do log de auditoria. <br/><br/>• Habilita ou desabilita o Microsoft Teams da organização (**Microsoft Teams**). <br/><br/>• Habilita ou desabilita a interoperabilidade entre o Microsoft Teams e o Skype for Business da organização (**Interoperabilidade do Skype for Business**). <br/><br/>• Habilita ou desabilita o modo de exibição de organograma em clientes do Microsoft Teams (Modo de exibição de organograma **). <br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de agendar reuniões particulares (** Agendamento de reunião particular **). <br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de agendar reuniões de canal (Agendamento de reunião de canal**). <br/><br/>• Habilita ou desabilita a chamada de vídeo em reuniões do Teams (vídeo para reuniões do Skype **). <br/><br/>• Habilita ou desabilita o compartilhamento de tela nas reuniões da organização do Microsoft Teams (** Compartilhamento de tela das reuniões do Skype **). <br/><br/>• Ativa ou desativa a capacidade de adicionar imagens animadas (chamadas Giphys) a conversas do Teams (Imagens animadas**). <br/><br/>• Altera a configuração de classificação de conteúdo da organização (**Classificação de conteúdo**). A classificação de conteúdo restringe o tipo de imagem animada que pode ser exibido em conversas. <br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de adicionar imagens personalizáveis (chamadas memes personalizados) da Internet a conversas da equipe (imagens personalizáveis da Internet **). <br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de adicionar imagens editáveis (chamadas adesivos) a conversas de equipe (** Imagens editáveis **).<br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de usar bots em conversas e canais do Microsoft Teams (bots de toda a organização**). <br/><br/>• Habilita bots específicos para o Microsoft Teams. Isso não inclui o T-Bot, que é o bot de ajuda do Teams, que está disponível quando os bots estão habilitados para a organização (**Bots individuais**). <br/><br/>• Habilita ou desabilita a capacidade dos membros da equipe de adicionar extensões ou guias (**Extensões ou guias**). <br/><br/>• Habilita ou desabilita o carregamento lateral de bots proprietários do Microsoft Teams (**Carregamento lateral de bots**). <br/><br/>• Habilita ou desabilita a capacidade dos usuários de enviar mensagens de email a um canal do Microsoft Teams (**Email do canal**).|
|Função de membros alterada na equipe|MemberRoleChanged|Um proprietário altera a função dos membros de uma equipe. Os valores a seguir indicam o tipo de função atribuída ao usuário. <br/><br/> **1** – Indica a função de Proprietário.<br/>**2** – Indica a função de Membro. <br/>**3** – Indica a função de Convidado. <br/><br/> A propriedade Membros inclui também o nome da sua organização e o endereço de email do membro.|
|Configuração da equipe alterada|TeamSettingChanged|A operação ChannelSettingChanged é registrada em log quando as seguintes atividades são realizadas por um proprietário da equipe. Para cada uma dessas atividades, uma descrição da configuração que foi alterada (mostrada entre parênteses abaixo) é exibida na coluna **Item** nos resultados da pesquisa do log de auditoria. <br/><br/>• Altera o tipo de acesso para uma equipe. As equipes podem ser definidas como Públicas ou Particulares (**Tipo de acesso de equipe**). Quando uma equipe é particular (a configuração padrão), os usuários podem acessá-la apenas por convite. Quando uma equipe é pública, ela fica visível para qualquer pessoa. <br/><br/>• Altera a classificação das informações de uma equipe (**Classificação da equipe**). <br/> Por exemplo, os dados da equipe podem ser classificados como alto impacto sobre os negócios, médio impacto sobre os negócios ou baixo impacto sobre os negócios.<br/><br/>• Altera o nome de uma equipe (**Nome da equipe**). <br/><br/>• Altera a descrição da equipe (Descrição da equipe**). <br/><br/>• Alterações feitas em qualquer uma das configurações da equipe. Um proprietário da equipe pode acessar essas configurações em um cliente do Teams, clicando com o botão direito do mouse em uma equipe, clicando em **Gerenciar equipe** e, em seguida, clicando na guia **Configurações**. Para essas atividades, o nome da configuração que foi alterada é exibido na coluna **Item** nos resultados da pesquisa do log de auditoria.|
|Equipe criada|TeamCreated|O usuário cria uma equipe.|
|Canal excluído|ChannelDeleted|Um usuário exclui um canal de uma equipe.|
|Equipe excluída|TeamDeleted|Um proprietário de equipe exclui uma equipe.|
|Bot removido da equipe|BotRemovedFromTeam|Um usuário remove um bot de uma equipe.|
|Conector removido|ConnectorRemoved|Um usuário remove um conector de um canal.|
|Membros removidos da equipe|MemberRemoved|Um proprietário remove membros de uma equipe.|
|Guia removida|TabRemoved|Um usuário remove uma guia de um canal.|
|Conector atualizado|ConnectorUpdated|Um usuário modificou um conector em um canal.|
|Guia atualizada|TabUpdated|Usuário modificou uma guia no canal.|
|Usuário entrou nas Equipes|TeamsSessionStarted|Um usuário entra em um cliente do Microsoft Teams.|
||||

### <a name="yammer-activities"></a>Atividades do Yammer

A tabela a seguir lista as atividades de usuários e de administradores no Yammer que estão conectadas no log de auditoria do Office 365. Para retornar atividades relacionadas ao Yammer do log de auditoria do Office 365, você precisa selecionar **Mostrar resultados para todas as atividades** na lista **Atividades**. Use as caixas de intervalo de datas e a lista de **Usuários** para restringir os resultados da pesquisa.

|**Nome amigável**|**Operação**|**Descrição**|
|:-----|:-----|:-----|
|Política de retenção de dados alterada|SoftDeleteSettingsUpdated|O administrador verificado atualiza a configuração da política de retenção de dados da rede para Exclusão Irreversível ou Exclusão Temporária. Somente administradores verificados podem realizar essa operação.|
|Configuração de rede alterada|NetworkConfigurationUpdated|O administrador de rede ou administrador verificado altera as configurações da rede do Yammer. Isso inclui a definição do intervalo de exportação de dados e de habilitação do chat.|
|Configurações de perfil de rede alteradas|ProcessProfileFields|O administrador de rede ou verificado altera as informações que aparecem em perfis de membro para a rede de usuários da rede.|
|Modo de Conteúdo Particular modificado|SupervisorAdminToggled|O administrador verificado ativa ou desativa o *Modo de Conteúdo Particular*. Esse modo permite que um administrador visualize postagens em grupos particulares e visualize mensagens particulares entre usuários individuais (ou grupos de usuários). Somente administradores verificados podem realizar essa operação.|
|Configurações de segurança alteradas|NetworkSecurityConfigurationUpdated|O administrador verificado atualiza as configurações de segurança da rede do Yammer. Isso inclui a definição de políticas de expiração de senha e restrições de endereços IP. Somente administradores verificados podem realizar essa operação.|
|Arquivo criado|FileCreated|O usuário carrega um arquivo.|
|Grupo criado|GroupCreation|O usuário cria um grupo.|
|Grupo excluído|GroupDeletion|Um grupo é excluído do Yammer.|
|Mensagem excluída|MessageDeleted|O usuário exclui uma mensagem.|
|Arquivo baixado|FileDownloaded|O usuário baixa um arquivo.|
|Dados exportados|DataExport|O administrador verificado exporta dados de rede do Yammer. Somente administradores verificados podem realizar essa operação.|
|Arquivo compartilhado|FileShared|O usuário compartilha um arquivo com outros usuários.|
|Usuário de rede suspenso|NetworkUserSuspended|O administrador de rede ou verificado suspende ou desativa um usuário no Yammer.|
|Usuário suspenso|UserSuspension|A conta de usuário é suspensa ou desativada.|
|Descrição de arquivo atualizada|FileUpdateDescription|O usuário modifica a descrição de um arquivo.|
|Nome de arquivo atualizado|FileUpdateName|O usuário modifica o nome de um arquivo.|
|Arquivo exibido|FileVisited|O usuário exibe um arquivo.|
||||

### <a name="microsoft-flow-activities"></a>Atividades do Fluxo da Microsoft

Você pode pesquisar o log de auditoria para atividades no Microsoft Flow. Essas atividades incluem criar, editar e excluir fluxos, e alterar as permissões de fluxo. Para obter informações sobre auditoria de atividades de Fluxo, confira o blog [eventos de auditoria do Microsoft Flow já estão disponíveis no Centro de Conformidade e Segurança](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Você pode pesquisar o log de auditoria de atividades relacionadas a aplicativos no PowerApps. Essas atividades incluem criar, iniciar e publicar um aplicativo. Atribuir permissões a aplicativos também é auditado. Para obter uma descrição de todas as atividades do PowerApps, confira [Log de atividades do PowerApps](https://docs.microsoft.com/pt-BR/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Atividades do Microsoft Stream

Você pode pesquisar o log de auditoria para atividades no Microsoft Stream. Essas atividades incluem atividades de vídeo executadas por usuários, atividades de canal de grupo e atividades de administração, como gerenciar usuários, gerenciar as configurações da organização e exportar relatórios. Para obter uma descrição dessas atividades, confira a seção "Atividades registradas no Microsoft Stream em [Logs de auditoria do Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Log de auditoria de administradores do Exchange

O log de auditoria de administradores do Exchange (que está habilitado por padrão no Office 365) registra um evento no log de auditoria do Office 365 quando um administrador (ou um usuário que recebeu permissões administrativas) faz uma alteração na sua organização do Exchange Online. As alterações feitas usando o centro de administração do Exchange ou executando um cmdlet no PowerShell do Exchange Online são registradas no log de auditoria de administradores do Exchange. Os cmdlets que começam com os verbos **Obter-**, **Pesquisar**, ou **Testar –** não estão registrados no log de auditoria do Office 365. Para obter informações mais detalhadas sobre o log de auditoria de administradores do Exchange, confira [Log de auditoria de administradores](https://go.microsoft.com/fwlink/p/?LinkID=619225).

> [!IMPORTANT]
> Alguns cmdlets do Exchange Online que não estão registrados no log de auditoria de administradores do Exchange (ou no log de auditoria do Office 365). Muitos desses cmdlets estão relacionados à manutenção do serviço do Exchange Online e são executados pela equipe do datacenter da Microsoft ou por contas de serviços. Esses cmdlets não são registrados porque resultariam em um grande número de eventos de auditoria "ruidosa". Se houver um cmdlet do Exchange Online que não está sendo auditado, envie uma sugestão para o [fórum de Voz do Usuário de Conformidade e Segurança do Office 365](https://office365.uservoice.com/forums/289138-office-365-security-compliance) e solicite que ele seja habilitado para auditoria. Você também pode enviar uma solicitação de alteração de design (DCR) para o suporte da Microsoft.

Aqui estão algumas dicas para pesquisar atividades de administração do Exchange ao pesquisar o log de auditoria do Office 365:

- Para retornar entradas do log de auditoria de administradores do Exchange, você precisa selecionar **Mostrar resultados para todas as atividades** na lista de **Atividades**. Use as caixas de intervalo de datas e a lista de **Usuários** para restringir os resultados da pesquisa para cmdlets executados por um administrador específico do Exchange dentro de um intervalo de datas específico.

- Para exibir eventos do log de auditoria de administradores do Exchange, filtre os resultados da pesquisa e digite um **-** (traço) na caixa de filtro **Atividade**. São mostrados os nomes de cmdlets, que são exibidos na coluna **Atividade** para eventos de administradores do Exchange. Em seguida, você pode classificar os nomes de cmdlets em ordem alfabética.

  ![Digite um traço na caixa Atividades para filtrar os eventos de administração do Exchange](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)

- Para obter informações sobre qual cmdlet foi executado, quais parâmetros e valores de parâmetros foram usados e quais objetos foram afetados, você pode exportar os resultados da pesquisa selecionando a opção **Baixar todos os resultados**. Para saber mais, confira [Exportar, configurar e exibir registros de log de auditoria](export-view-audit-log-records.md).

- Você também pode usar o comando `Search-UnifiedAuditLog -RecordType ExchangeAdmin` no PowerShell do Exchange Online para retornar somente registros de auditoria do log de auditoria de administradores do Exchange. Pode levar até 30 minutos após a execução de um cmdlet do Exchange para que a entrada do log de auditoria correspondente seja retornada nos resultados da pesquisa. Para saber mais, confira [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog). Para obter informações sobre como exportar os resultados da pesquisa retornados pelo cmdlet **Search-UnifiedAuditLog** para um arquivo CSV, confira a seção "Dicas para exportar e exibir o log de auditoria" em [Exportar, configurar e exibir registros de log de auditoria](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Você também pode exibir os eventos no log de auditoria de administradores do Exchange usando o centro de administração do Exchange ou executando o **Search-AdminAuditLog** no PowerShell do Exchange Online. Esta é uma ótima maneira de procurar especificamente atividades executadas por administradores do Exchange Online. Para obter instruções, veja:

  - [Exibir o log de auditoria do administrador](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx)

  - [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-adminauditlog)

   Lembre-se de que as mesmas atividades de administradores do Exchange estão registradas no log de auditoria de administradores do Exchange e no log de auditoria do Office 365.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**Onde posso encontrar os recursos oferecidos pelo serviço de auditoria do Office 365?**

Para obter mais informações sobre os recursos de auditoria e de relatório disponíveis no Office 365, confira [Auditoria e relatórios do Office 365](office-365-auditing-and-reporting-overview.md).

**Quais são os diferentes serviços do Office 365 que atualmente são auditados?**

Os serviços mais usados do Office 365, como o Exchange Online, o SharePoint Online, o OneDrive for Business, o Azure Active Directory, o Microsoft Teams, o Dynamics 365, a Proteção Avançada Contra Ameaças e o Power BI são auditados. Confira o [Início deste artigo](search-the-audit-log-in-security-and-compliance.md) para obter uma lista de serviços que são auditados.

**Quais atividades são auditadas por serviço de auditoria no Office 365?**

Consulte a seção [Atividades auditadas](#audited-activities) neste artigo para obter uma lista e uma descrição das atividades que são auditadas no Office 365.

**Quanto tempo leva para um registro de auditoria estar disponível após um evento ter ocorrido?**

A maioria dos dados de auditoria está disponível em 30 minutos, mas pode levar até 24 horas após a ocorrência de um evento para que a entrada do log de auditoria correspondente seja exibida nos resultados da pesquisa. Veja a tabela na seção [Antes de começar](#before-you-begin) deste artigo, que mostra o tempo necessário para que os eventos nos diferentes serviços do Office 365 estejam disponíveis.

**Por quanto tempo os registros de auditoria são mantidos?**

Como explicado anteriormente, o período de retenção para registros de auditoria depende da assinatura do Office 365 da sua organização.

- **Office 365 E3:** Os registros de auditoria são mantidos por 90 dias.

- **Office 365 E5:** Os registros de auditoria também são mantidos por 90 dias. Manter registros de auditoria por um ano pode estar disponível para usuários do E5 e usuários com uma licença do E3 e uma licença do complemento de Conformidade Avançada do Office 365.

  > [!NOTE]
  > Como explicado anteriormente, o programa de visualização particular para o período de retenção de um ano dos registros de auditoria para organizações E5 (ou organizações E3 que têm licenças complementares de Conformidade Avançada) é fechada para o novo registro. Esse artigo será atualizado quando o período de retenção de um ano estiver disponível na visualização pública ou lançado para disponibilidade geral.

Observe também que a duração do período de retenção para registros de auditoria baseia-se no licenciamento por usuário. Por exemplo, se um usuário da sua organização tiver uma licença do Office 365 E3 ou e5, os registros de auditoria para atividades executadas por esse usuário serão mantidos por 90 dias.

**Posso acessar os dados de auditoria de forma programática?**

Sim. A API de atividade de gerenciamento do Office 365 é usada para buscar os logs de auditoria por programação.  Para saber mais, confira [Introdução às APIs de Gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Existem outras maneiras de obter logs de auditoria além de usar o centro de segurança e conformidade ou a API da Atividade de Gerenciamento do Office 365?**

Não. Estas são as duas únicas maneiras de obter dados do serviço de auditoria do Office 365.

**Preciso habilitar individualmente a auditoria em cada serviço para o qual quero capturar os logs de auditoria?**

Na maioria dos serviços do Office 365, a auditoria está habilitada por padrão, depois de ativar a auditoria para a sua organização do Office 365 (conforme descrito na seção [Antes de começar](#before-you-begin) deste artigo).

**O serviço de auditoria do Office 365 oferece suporte para a duplicação de registros?**

Não. O pipeline do serviço de auditoria está quase em tempo real, portanto não é compatível com a duplicação.

**O Office 365 faz auditoria de dados entre regiões geográficas?**

Não. Atualmente, temos implantações de pipeline de auditoria nas regiões da América do Norte, Europa, Oriente Médio, África e Pacífico Asiático. No entanto, podemos transmitir os dados entre essas regiões para balancear a carga e apenas durante problemas no site ao vivo. Quando realizamos essas atividades, os dados em trânsito são criptografados.

**Os dados de auditoria são criptografados?**

Os dados de auditoria são armazenados nas caixas de correio do Exchange (dados em repouso) na mesma região em que o pipeline de auditoria é implantado. Esses dados não são criptografados. No entanto, os dados em trânsito sempre são criptografados.
