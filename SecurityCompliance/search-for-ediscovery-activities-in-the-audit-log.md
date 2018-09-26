---
title: Procure atividades de descoberta eletrônica no log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: Aprenda como pesquisar o log de auditoria do Office 365 para eventos que são registrados quando os administradores de conformidade executam tarefas de casos de pesquisa de conteúdo e descoberta eletrônica na segurança &amp; Centro de conformidade.
ms.openlocfilehash: a4cc3a6b5030a6412d739236e4c534f36948d57f
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038344"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Procure atividades de descoberta eletrônica no log de auditoria do Office 365

Pesquisa e atividades relacionadas a descoberta eletrônica que são executadas na segurança do Office 365 conteúdo &amp; Centro de conformidade ou executando o Windows PowerShell correspondente cmdlets são registrados no log de auditoria do Office 365. Os eventos são registrados quando os administradores ou administradores de conformidade (ou qualquer usuário que é descoberta eletrônica atribuídas permissões) executa a seguir pesquisa de conteúdo e as tarefas relacionadas a descoberta eletrônica no Office 365 Security &amp; Centro de conformidade:
  
- Criando e gerenciando casos de eDiscovery
    
- Criando, iniciar e editando pesquisas de conteúdo
    
- Realizando ações de pesquisa de conteúdo, como visualizar, exportação e exclusão de resultados da pesquisa
    
- Configurar permissões de filtragem para a pesquisa de conteúdo
    
- Gerenciando a função de administrador de descoberta eletrônica
    
> [!IMPORTANT]
> As atividades descritas neste artigo são apenas o resultado das tarefas de descoberta eletrônica realizadas usando a segurança &amp; Centro de conformidade. tarefas de descoberta eletrônica que foram realizadas usando a ferramenta de descoberta eletrônica In-loco no Exchange Online ou a Central de descoberta eletrônica no SharePoint Online não são incluídas. 
  
Para obter mais informações sobre como pesquisar no log de auditoria do Office 365, as permissões que são necessárias e exportar os resultados da pesquisa, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>Como pesquisar por e atividades de descoberta eletrônica do modo de exibição

Atualmente, você precisará fazer algumas coisas específicas para exibir as atividades de descoberta eletrônica no log de auditoria do Office 365. Aqui está como.
  
1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel esquerdo, clique em **pesquisa &amp; investigação**e clique em **pesquisa de log de auditoria**.
    
4. Na lista suspensa de **atividades** , **as atividades de descoberta eletrônica**, clique em uma ou mais atividades para procurar. Ou você pode clicar em **atividades de eDiscovery** para pesquisar todas as atividades relacionadas a descoberta eletrônica. 
    
    > [!NOTE]
    > A lista suspensa de atividades também inclui um grupo de atividades denominado **eDiscovery cmdlet atividades** que retornará os registros do log de auditoria do cmdlet. 
  
5.  Selecione um intervalo de data e hora para exibir eventos de descoberta eletrônica que ocorreram nesse período. 
    
6. Na caixa **usuários** , selecione um ou mais usuários para exibir resultados de pesquisa para. Deixe esta caixa em branco para retornar as entradas para todos os usuários. 
    
7. Clique em **pesquisa** para executar a pesquisa usando os critérios de pesquisa. 
    
8. Depois que os resultados da pesquisa são exibidos, você pode clicar **resultados de filtro** para filtrar ou classificar os registros resultantes de atividade. Infelizmente, você não pode usar a filtragem para excluir explicitamente determinadas atividades. 
    
9. Para exibir detalhes sobre uma atividade, clique no registro de atividade na lista de resultados da pesquisa. 
    
    É exibida uma dinamicamente **detalhes** da página que contém as propriedades detalhadas do registro de eventos. Para exibir detalhes adicionais, clique em **obter mais informações**. Para obter uma descrição dessas propriedades, consulte a seção de [Propriedades detalhadas para atividades de descoberta eletrônica](#detailed-properties-for-ediscovery-activities) . 

  
## <a name="ediscovery-activities"></a>atividades de descoberta eletrônica

A tabela a seguir descreve a pesquisa de conteúdo e atividades relacionadas a descoberta eletrônica que são registradas quando um administrador ou usuário realiza uma atividade relacionada à descoberta eletrônica usando a segurança &amp; Centro de conformidade ou executando o cmdlet correspondente no o PowerShell remoto que esteja conectado a segurança da sua organização &amp; Centro de conformidade. 
  
> [!NOTE]
> As atividades de descoberta eletrônica descritas nesta seção fornecem informações semelhantes às atividades cmdlet eDiscovery descrito na próxima seção. Recomendamos que você use as atividades de descoberta eletrônica descritas nesta seção porque eles serão exibidos nos resultados da pesquisa de log de auditoria em até 30 minutos. Leva até 24 horas para o eDiscovery atividades de cmdlet apareça nos resultados da pesquisa de log de auditoria. 
  
|**Nome amigável**|**Operation**|**Cmdlet correspondente**|**Descrição**|
|:-----|:-----|:-----|:-----|
|Membro adicionado ao caso de descoberta eletrônica  <br/> |CaseMemberAdded  <br/> |Adicionar-ComplianceCaseMember  <br/> |Um usuário foi adicionado como um membro de um caso de eDiscovery. Como membro de um caso, um usuário pode realizar várias tarefas relacionadas ao caso, dependendo se eles tiverem sido atribuídos as permissões necessárias.  <br/> |
|Pesquisa de conteúdo alterada  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |Uma pesquisa de conteúdo existente foi alterada. Alterações podem incluir adicionando ou removendo locais de conteúdo ou editar a consulta de pesquisa.  <br/> |
|Associação de administrador de descoberta eletrônica alterados  <br/> |CaseAdminUpdated  <br/> |Update-eDiscoveryCaseAdmin  <br/> |A lista de descoberta eletrônica administradores em sua organização foi alterada. Esta atividade é registrada quando a lista de administradores de descoberta eletrônica é substituída por um grupo de novos usuários. Se um único usuário é adicionado ou removido, a operação CaseAdminAdded é registrada.  <br/> |
|Caso de descoberta eletrônica alterados  <br/> |CaseUpdated  <br/> |Set-ComplianceCase  <br/> |Um caso de eDiscovery foi alterado. Alterações incluem o fechamento de um caso aberto ou abrindo novamente uma ocorrência fechada.  <br/> |
|Associação de casos de eDiscovery alterados  <br/> |CaseMemberUpdated  <br/> |Update-ComplianceCaseMember  <br/> |A lista de membros de um caso de eDiscovery foi alterada. Esta atividade é registrada quando todos os membros são substituídos por um grupo de novos usuários. Se um único membro é adicionado ou removido, a operação CaseMemberAdded ou CaseMemberRemoved é registrada.  <br/> |
|Alterado o filtro de permissões de pesquisa  <br/> |SearchPermissionUpdated  <br/> |Set-ComplianceSecurityFilter  <br/> |Um filtro de permissões de pesquisa foi alterado.  <br/> |
|Consulta de pesquisa alterados para retenção de casos de eDiscovery  <br/> |HoldUpdated  <br/> |Set-CaseHoldRule  <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery foi alterada. Alterações possíveis incluem editando a consulta ou o intervalo de datas para uma consulta com base em espera.  <br/> |
|Item de visualização de pesquisa de conteúdo baixado  <br/> |PreviewItemDownloaded  <br/> |N/D  <br/> |Um usuário baixado um item para seus computadores locais (clicando no link **Baixar item original** ) quando a visualização de resultados da pesquisa.  <br/> |
|Item de visualização de pesquisa de conteúdo listado  <br/> |PreviewItemListed  <br/> |N/D  <br/> |Um usuário clicou em **resultados da pesquisa de visualização** para exibir a página de resultados de pesquisa de visualização, que lista até 1.000 itens dos resultados de uma pesquisa de conteúdo.  <br/> |
|Item de visualização de pesquisa de conteúdo exibido  <br/> |PreviewItemRendered  <br/> |N/D  <br/> |Um gerente de descoberta eletrônica exibidos um item clicando ao visualizar os resultados da pesquisa.  <br/> |
|Pesquisa de conteúdo criada  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |Uma nova pesquisa de conteúdo que foi criada.  <br/> |
|Administrador de descoberta eletrônica criada  <br/> |CaseAdminAdded  <br/> |Adicionar-eDiscoveryCaseAdmin  <br/> |Um usuário foi adicionado como um administrador de eDiscovery na organização.  <br/> |
|Caso de descoberta eletrônica criada  <br/> |CaseAdded  <br/> |New-ComplianceCase  <br/> |Um caso de eDiscovery que foi criado. Quando um caso é criado, você só precisa dar um nome. Outras tarefas relacionadas ao caso como adicionando membros, criando isenções e criar pesquisas de conteúdo associadas com o resultado de maiusculas em outros eventos sendo registrados.  <br/> |
|Criado o filtro de permissões de pesquisa  <br/> |SearchPermissionCreated  <br/> |New-ComplianceSecurityFilter  <br/> |Um filtro de permissões de pesquisa foi criado.  <br/> |
|Consulta de pesquisa criado para retenção de casos de eDiscovery  <br/> |HoldCreated  <br/> |New-CaseHoldRule  <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery que foi criada.  <br/> |
|Pesquisa de conteúdo excluída  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |Uma pesquisa de conteúdo existente foi excluída.  <br/> |
|Administrador de descoberta eletrônica excluído  <br/> |CaseAdminRemoved  <br/> |Remove-eDiscoveryCaseAdmin  <br/> |Uma administrador de descoberta eletrônica foi excluída da sua organização.  <br/> |
|Caso de descoberta eletrônica excluído  <br/> |CaseRemoved  <br/> |Remove-ComplianceCase  <br/> |Um caso de eDiscovery foi excluído. Observe que qualquer associada à ocorrência de espera deve ser removido antes do caso pode ser excluído.  <br/> |
|Filtro de permissões de pesquisa excluídos  <br/> |SearchPermissionRemoved  <br/> |Remove-ComplianceSecurityFilter  <br/> |Um filtro de permissões de pesquisa foi excluído.  <br/> |
|Consulta de pesquisa excluídos para retenção de casos de eDiscovery  <br/> |HoldRemoved  <br/> |Remove-CaseHoldRule  <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery foi excluída. Removendo a consulta da retenção é geralmente o resultado da exclusão de uma isenção. Quando uma isenção ou uma consulta de espera forem excluídas, os locais de conteúdo que estavam em espera sejam liberados.  <br/> |
|Baixado exportação de conteúdo de pesquisa  <br/> |SearchResultDownloaded  <br/> |N/D  <br/> |Um usuário baixado os resultados de uma pesquisa de conteúdo para seus computadores locais. Observe que uma atividade **iniciado exportar de pesquisa de conteúdo** deve ser iniciada antes que os resultados da pesquisa podem ser baixados.<br/> |
|Visualizados resultados da pesquisa de conteúdo  <br/> |SearchPreviewed  <br/> |N/D  <br/> |Um usuário visualizados os resultados de uma pesquisa de conteúdo.  <br/> |
|Removidos resultados da pesquisa de conteúdo  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |Um usuário removidos os resultados de uma pesquisa de conteúdo executando o **New-ComplianceSearchAction-limpar** comando.  <br/> |
|Análise removido da pesquisa de conteúdo  <br/> |RemovedSearchResultsSentToZoom  <br/> |Remove-ComplianceSearchAction  <br/> |Uma pesquisa de conteúdo preparar ação (para preparar os resultados da pesquisa avançada do Office 365 eDiscovery) foi excluído. Se a ação de preparação era menor que duas semanas, resultados da pesquisa que foram preparados para o eDiscovery avançado foram excluídos da área de armazenamento do Microsoft Azure. Se a ação de preparação foi mais antiga do que 2 semanas, esse evento indica que somente a ação de preparação correspondente foi excluída.  <br/> |
|Exportação removida da pesquisa de conteúdo  <br/> |RemovedSearchExported  <br/> |Remove-ComplianceSearchAction  <br/> |Uma ação de exportação de conteúdo de pesquisa foi excluída. Se a ação de exportação foi menos de duas semanas, os resultados da pesquisa que foram carregados para a área de armazenamento do Microsoft Azure foram excluídos. Se a ação de exportação foi mais antiga do que 2 semanas, esse evento indica que somente a ação de exportação correspondente foi excluída.  <br/> |
|Membros removidos do caso de descoberta eletrônica  <br/> |CaseMemberRemoved  <br/> |Remove-ComplianceCaseMember  <br/> |Um usuário foi removido como um membro de um caso de eDiscovery.  <br/> |
|Removida a visualização de resultados de pesquisa de conteúdo  <br/> |RemovedSearchPreviewed  <br/> |Remove-ComplianceSearchAction  <br/> |Uma ação de visualização de pesquisa de conteúdo foi excluída.  <br/> |
|Ação de limpeza removidos executada na pesquisa de conteúdo  <br/> |RemovedSearchResultsPurged  <br/> |Remove-ComplianceSearchAction  <br/> |Uma ação de limpeza de pesquisa de conteúdo foi excluída.  <br/> |
|Removido o relatório de pesquisa  <br/> |SearchReportRemoved  <br/> |Remove-ComplianceSearchAction  <br/> |Uma pesquisa de conteúdo Exportar relatório ação foi excluída.  <br/> |
|Análise de introdução da pesquisa de conteúdo  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |Os resultados de uma pesquisa de conteúdo foram preparados para análise no eDiscovery avançado.  <br/> |
|Pesquisa de conteúdo de Introdução  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |Uma pesquisa de conteúdo foi iniciada. Quando você criar ou alterar uma pesquisa de conteúdo usando a segurança &amp; GUI do Centro de conformidade, a pesquisa é iniciado automaticamente. Se você cria ou altera uma pesquisa usando o **New-ComplianceSearch** ou o cmdlet **Set-ComplianceSearch** , você precisará executar o cmdlet **Start-ComplianceSearch** para iniciar a pesquisa.<br/> |
|Introdução de exportação de conteúdo de pesquisa  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |Um usuário exportou os resultados de uma pesquisa de conteúdo.  <br/> |
|Relatório de exportação de Introdução  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |Um usuário exportado um relatório de pesquisa de conteúdo.  <br/> |
|Pesquisa de conteúdo parada  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |Um usuário interrompido uma pesquisa de conteúdo.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>atividades de cmdlet do eDiscovery

A tabela a seguir lista os registros de log de auditoria de cmdlet que são registrados quando um administrador ou usuário realiza uma atividade relacionada à descoberta eletrônica usando a segurança &amp; Centro de conformidade ou executando o cmdlet correspondente no PowerShell remoto do conectado a segurança da sua organização &amp; Centro de conformidade. Observe que as informações detalhadas sobre o registro de log de auditoria são diferentes para as atividades de cmdlet listadas nesta tabela e as atividades de descoberta eletrônica descritas na seção anterior. 
  
Conforme indicado anteriormente, que leva até 24 horas para eDiscovery atividades de cmdlet apareça nos resultados da pesquisa de log de auditoria.
  
> [!TIP]
> Os cmdlets na coluna **operação** na tabela a seguir são vinculados ao tópico da Ajuda cmdlet correspondente no TechNet. Vá para o tópico de Ajuda do cmdlet para obter uma descrição dos parâmetros disponíveis para cada cmdlet. O parâmetro e o valor do parâmetro que foram usadas com um cmdlet estão incluídos na entrada do log de auditoria para cada atividade do cmdlet de descoberta eletrônica que está conectada. 
  
|**Nome amigável**|**Operação (cmdlet)**|**Descrição**|
|:-----|:-----|:-----|
|Espera criada no caso de descoberta eletrônica  <br/> |[New-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |Uma isenção foi criada para um caso de eDiscovery. Uma isenção pode ser criada com ou sem a especificação de uma fonte de conteúdo. Se as fontes de conteúdo forem especificadas, vai ser identificados na entrada do log de auditoria.  <br/> |
|Espera excluída do caso de descoberta eletrônica  <br/> |[Remove-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |Uma isenção que está associada um caso de eDiscovery foi excluída. Excluir uma isenção libera todos os locais de conteúdo da isenção. Excluir isenção também resulta em excluindo as regras de maiusculas espera associadas a isenção (consulte **Remove-CaseHoldRule** abaixo).<br/> |
|Espera alterada no caso de descoberta eletrônica  <br/> |[Set-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |Uma isenção que está associada um eDiscovery foi alterada. Alterações possíveis incluem a adição ou remoção de locais de conteúdo ou desligamento (desabilitação) isenção.  <br/> |
|Consulta de pesquisa criado para retenção de casos de eDiscovery  <br/> |[New-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery que foi criada.  <br/> |
|Consulta de pesquisa excluídos para retenção de casos de eDiscovery  <br/> |[Remove-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery foi excluída. Removendo a consulta da retenção é geralmente o resultado da exclusão de uma isenção. Quando uma isenção ou uma consulta de espera forem excluídas, os locais de conteúdo que estavam em espera sejam liberados.  <br/> |
|Consulta de pesquisa alterados para retenção de casos de eDiscovery  <br/> |[Set-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |Uma isenção baseado em consulta associada a um caso de eDiscovery foi alterada. Alterações possíveis incluem editando a consulta ou o intervalo de datas para uma consulta com base em espera.  <br/> |
|Caso de descoberta eletrônica criada  <br/> |[New-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |Um caso de eDiscovery que foi criado. Quando um caso é criado, você só precisa dar um nome. Outras tarefas relacionadas ao caso como adicionando membros, criando isenções e criar pesquisas de conteúdo associadas com o resultado de maiusculas em outros eventos sendo registrados.  <br/> |
|Caso de descoberta eletrônica excluído  <br/> |[Remove-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |Um caso de eDiscovery foi excluído. Observe que qualquer associada à ocorrência de espera deve ser removido antes do caso pode ser excluído.  <br/> |
|Caso de descoberta eletrônica alterados  <br/> |[Set-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |Um caso de eDiscovery foi alterado. Alterações incluem o fechamento de um caso aberto ou abrindo novamente uma ocorrência fechada.  <br/> |
|Membro adicionado ao caso de descoberta eletrônica  <br/> |[Adicionar-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |Um usuário foi adicionado como um membro de um caso de eDiscovery. Como membro de um caso, um usuário pode realizar várias tarefas relacionadas ao caso, dependendo se eles tiverem sido atribuídos as permissões necessárias.  <br/> |
|Membros removidos do caso de descoberta eletrônica  <br/> |[Remove-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |Um usuário foi removido como um membro de um caso de eDiscovery.  <br/> |
|Associação de casos de eDiscovery alterados  <br/> |[Update-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |A lista de membros de um caso de eDiscovery foi alterada. Esta atividade é registrada quando todos os membros são substituídos por um grupo de novos usuários. Se um único membro é adicionado ou removido, a operação **ComplianceCaseMember de adicionar** ou **Remover-ComplianceCaseMember** é registrada.<br/> |
|Pesquisa de conteúdo criada  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |Uma nova pesquisa de conteúdo que foi criada.  <br/> |
|Pesquisa de conteúdo excluída  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |Uma pesquisa de conteúdo existente foi excluída.  <br/> |
|Pesquisa de conteúdo alterada  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |Uma pesquisa de conteúdo existente foi alterada. Alterações podem incluir a adição ou remoção de locais de conteúdo que são pesquisados e editando a consulta de pesquisa.  <br/> |
|Pesquisa de conteúdo de Introdução  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |Uma pesquisa de conteúdo foi iniciada. Quando você criar ou alterar uma pesquisa de conteúdo usando a segurança &amp; GUI do Centro de conformidade, a pesquisa é iniciado automaticamente. Se você cria ou altera uma pesquisa usando o **New-ComplianceSearch** ou o cmdlet **Set-ComplianceSearch** , você precisará executar o cmdlet **Start-ComplianceSearch** para iniciar a pesquisa.<br/> |
|Pesquisa de conteúdo parada  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |Uma pesquisa de conteúdo que estava em execução foi interrompida.  <br/> |
|Criou a ação de pesquisa de conteúdo  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |Uma ação de pesquisa de conteúdo que foi criada. Ações de pesquisa de conteúdo incluem a visualização de resultados da pesquisa, exportar os resultados da pesquisa, Preparando os resultados da pesquisa para análise no eDiscovery avançadas do Office 365 e excluir permanentemente os itens que correspondem aos critérios de pesquisa de uma pesquisa de conteúdo.  <br/> |
|Ação de pesquisa de conteúdo excluído  <br/> |[Remove-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |Uma ação de pesquisa de conteúdo foi excluída.  <br/> |
|Criado o filtro de permissões de pesquisa  <br/> |[New-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |Um filtro de permissões de pesquisa foi criado.  <br/> |
|Filtro de permissões de pesquisa excluídos  <br/> |[Remove-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |Um filtro de permissões de pesquisa foi excluído.  <br/> |
|Alterado o filtro de permissões de pesquisa  <br/> |[Set-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |Um filtro de permissões de pesquisa foi alterado.  <br/> |
|Administrador de descoberta eletrônica criada  <br/> |[Adicionar-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |Um usuário foi adicionado como um administrador de eDiscovery em sua organização.  <br/> |
|Administrador de descoberta eletrônica excluído  <br/> |[Remove-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |Uma administrador de descoberta eletrônica foi excluída da sua organização.  <br/> |
|Associação de administrador de descoberta eletrônica alterados  <br/> |[Update-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |A lista de descoberta eletrônica administradores em sua organização foi alterada. Esta atividade é registrada quando a lista de administradores de descoberta eletrônica é substituída por um grupo de novos usuários. Se um único usuário é adicionado ou removido, a operação **eDiscoveryCaseAdmin de adicionar** ou **Remover-eDiscoveryCaseAdmin** é registrada.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>Propriedades detalhadas para atividades de descoberta eletrônica

A tabela a seguir descreve as propriedades que são incluídas quando você clicar em **obter mais informações** , na página de **detalhes** de uma atividade de descoberta eletrônica listada nos resultados da pesquisa. Essas propriedades também são incluídas no arquivo CSV ao exportar os resultados da pesquisa de log de auditoria. Observe que um registro de log de auditoria para uma atividade de descoberta eletrônica não incluir cada propriedade detalhada listada abaixo. 
  
> [!TIP]
> Ao exportar os resultados da pesquisa, o arquivo CSV contém uma coluna chamada **detalhe**, que contém as propriedades detalhadas descritas na tabela a seguir em uma propriedade de valor múltiplos. Você pode usar o recurso de consulta de energia no Excel para dividir essa coluna em várias colunas, de modo que cada propriedade terá sua própria coluna. Isso permitirá que você classificar e filtrar em uma ou mais dessas propriedades. Para obter mais informações, consulte a seção "Exportar os resultados da pesquisa para um arquivo" na [pesquisa da auditoria, faça logon no Centro de conformidade & segurança do Office 365 ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file). 
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|Caso  <br/> |A identidade (GUID) do caso de eDiscovery que foi criado, alterado ou excluído.  <br/> |
|ClientApplication  <br/> |atividades de cmdlet do eDiscovery têm um valor de **EMC** para essa propriedade. Isso indica que a atividade foi realizada usando a segurança &amp; GUI do Centro de conformidade ou executando o cmdlet do PowerShell.<br/> |
|ClientIP  <br/> |O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido no formato de endereço de um IPv4 ou IPv6.  <br/> |
|ClientRequestId  <br/> | Para atividades de descoberta eletrônica, essa propriedade é normalmente em branco.  <br/> |
|CmdletVersion  <br/> |O número de compilação da versão da segurança &amp; Centro de conformidade em execução na organização.  <br/> |
|CreationTime  <br/> |A data e hora no tempo Universal Coordenado (UTC) quando a atividade de descoberta eletrônica foi concluída.  <br/> |
|EffectiveOrganization  <br/> |O nome da sua organização do Office 365.  <br/> |
|ExchangeLocations  <br/> |As caixas de correio do Exchange Online que são incluídas em uma pesquisa de conteúdo ou colocadas em espera em um caso de eDiscovery.  <br/> |
|Exclusões  <br/> |Locais de caixa de correio ou de site são excluídos de uma pesquisa de conteúdo ou uma isenção em um caso de eDiscovery.  <br/> |
|ExtendedProperties  <br/> |Propriedades adicionais de um conteúdo de pesquisa, uma ação de pesquisa de conteúdo, ou espera em um caso de eDiscovery, como a GUID do objeto e o cmdlet correspondente e os parâmetros de cmdlet que foram usados quando a atividade foi executada.  <br/> |
|Id  <br/> |A identificação da entrada do relatório. A ID identifica exclusivamente a entrada de log de auditoria.  <br/> |
|NonPIIParameters  <br/> |Uma lista dos parâmetros (sem quaisquer valores) que foram usados com o cmdlet identificado na propriedade operação. Os parâmetros listados nessa propriedade são os mesmos listados na propriedade Parameters.  <br/> |
|ObjectId  <br/> |O GUID ou o nome do objeto (por exemplo, uma pesquisa de conteúdo ou um caso de descoberta eletrônica) que tiver sido criado, alterado ou excluído pela atividade listada na propriedade operação. Este objeto também é identificado na coluna Item nos resultados da pesquisa de log de auditoria.  <br/> |
|ObjectType  <br/> |O tipo de objeto de descoberta eletrônica que o usuário criado, excluído ou modificado; Por exemplo uma ação de pesquisa de conteúdo (visualização, exportar ou limpar), um caso de descoberta eletrônica ou uma pesquisa de conteúdo.  <br/> |
|Operation  <br/> |O nome da operação que corresponde à atividade de descoberta eletrônica que foi executada.  <br/> |
|ID da organização  <br/> |O GUID para sua organização do Office 365.  <br/> |
|Parâmetros  <br/> |O nome e o valor para os parâmetros que foram usados com o cmdlet correspondente.  <br/> |
|PublicFolderLocations  <br/> |Os locais de pasta pública no Exchange Online que são incluídas em uma pesquisa de conteúdo ou colocados em espera em um caso de eDiscovery.  <br/> |
|Consulta  <br/> |A consulta de pesquisa associada à atividade, como uma pesquisa de conteúdo ou uma isenção baseado em consulta.  <br/> |
|RecordType  <br/> |O tipo de operação indicada pelo record. O valor de **18** indica um evento relacionado a uma atividade listada na seção de [atividades do cmdlet de descoberta eletrônica](#ediscovery-cmdlet-activities) . Um valor de **24** indica um evento relacionado a uma atividade listada na seção [como pesquisar por e atividades de descoberta eletrônica do modo de exibição](#how-to-search-for-and-view-ediscovery-activities) .<br/> |
|ResultStatus  <br/> |Indica se a ação (especificada na propriedade operação) foi bem-sucedida ou não.  <br/> |
|SecurityComplianceCenterEventType  <br/> |Indica que a atividade foi um título &amp; evento do Centro de conformidade. Todas as atividades de descoberta eletrônica terá um valor **0** para essa propriedade.<br/> |
|SharepointLocations  <br/> |Os sites do SharePoint Online que são incluídos em uma pesquisa de conteúdo ou colocados em espera em um caso de eDiscovery.  <br/> |
|StartTime  <br/> |A data e hora no tempo Universal Coordenado (UTC) quando a atividade de descoberta eletrônica foi iniciada.  <br/> |
|UserId  <br/> |O usuário que executou a atividade (especificada na propriedade operação) que resultou no registro que está sendo registrado. Observe que os registros de atividade de descoberta eletrônica realizada por contas do sistema (por exemplo, Autoridade NT\Sistema) também são incluídos no log de auditoria.  <br/> |
|UserKey  <br/> |Uma ID alternativa para o usuário identificado na propriedade UserId. Para as atividades de descoberta eletrônica, o valor dessa propriedade é normalmente o mesmo que a propriedade UserId.  <br/> |
|UserServicePlan  <br/> |Assinatura do Office 365 usada por sua organização. Para atividades de descoberta eletrônica, essa propriedade é normalmente em branco.  <br/> |
|UserType  <br/> |O tipo de usuário que executou a operação. Os valores a seguir indicam o tipo de usuário.  <br/> 0 um usuário regular. 2 um administrador na sua organização do Office 365. 3 um datacenter administrador ou datacenter sistema conta da Microsoft. 4 uma conta do sistema. 5 um aplicativo. 6 uma entidade de serviço. |
|Versão  <br/> |Indica o número de versão da atividade (identificado pela propriedade operação) que está conectado.  <br/> |
|Carga de trabalho  <br/> |O serviço do Office 365 onde a atividade ocorreu. Para atividades de descoberta eletrônica, o valor é **SecurityComplianceCenter**.<br/> |
