---
title: Visão geral dos recursos de pesquisa e de descoberta eletrônica do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Visão geral do recurso Descoberta eletrônica e outros recursos de pesquisa no Office 365 para uso de auditoria e transparência.
ms.openlocfilehash: 2d5cc2533c195b51f685aebd8da4462518116905
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524087"
---
# <a name="ediscovery-and-search-features"></a>Recursos de pesquisa e descoberta eletrônica 

## <a name="ediscovery"></a>Descoberta Eletrônica
O recurso de descoberta eletrônica oferece um lugar único para os administradores, oficiais de conformidade, e outros autorizado aos usuários conduzir uma investigação abrangente sobre a atividade de usuário do Office 365. Os agentes de segurança com as permissões apropriadas podem realizar pesquisas e retenções locais no conteúdo. Os resultados da pesquisa são os mesmos resultados que você obteve de uma pesquisa de conteúdo, exceto pelo fato de um caso de eDiscovery é criado para qualquer isenções que são aplicadas. Os resultados de pesquisas de descoberta eletrônica são criptografados para segurança e os dados exportados podem ser analisados [eDiscovery avançado](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4).

## <a name="content-search"></a>Pesquisa de Conteúdo
[Pesquisa de conteúdo](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) é uma nova ferramenta de pesquisa de descoberta eletrônica na segurança & Centro de conformidade que fornece o dimensionamento aprimorada e recursos de desempenho sobre as ferramentas de pesquisa de descoberta eletrônica anterior. Você pode usar a pesquisa de conteúdo para pesquisar caixas de correio, pastas públicas, sites do SharePoint Online e OneDrive para locais de negócios. Pesquisa de conteúdo é projetada especificamente para pesquisas muito grandes. Não há nenhum limite no número de caixas de correio e de sites que você pode pesquisar. Também há nenhum limite no número de pesquisas que podem ser executados ao mesmo tempo. Depois de executar uma pesquisa, o número de fontes de conteúdo e um número estimado de pesquisa, os resultados são exibidos no painel de detalhes, na página de pesquisa, onde você pode visualizar os resultados ou exportá-los para um computador local. Se sua organização tiver uma assinatura do Office 365 Enterprise E5, você também pode [preparar os resultados](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) para análise usando os recursos de análise poderosa do [eDiscovery avançadas do Office 365](http://go.microsoft.com/fwlink/p/?LinkID=620116).

## <a name="audit-log-search"></a>Pesquisa de Log de auditoria
Além de controlar alterações em suas organizações do Office 365, os clientes também podem exibir relatórios de auditoria e exportar logs de auditoria. Depois de auditoria está habilitado para um locatário do Office 365, usuário e atividades administrativas para esse inquilino é registrada nos logs de eventos e tornar pesquisáveis. Por exemplo, você pode usar para rastrear as ações executadas em uma caixa de correio por usuários que não seja o proprietário da caixa de correio do log de auditoria de caixa de correio. Além disso, os oficiais de conformidade podem usar os recursos de pesquisa e filtro para ver se um usuário tiver visualizado ou baixado um documento específico, ou se um administrador tiver executado atividades de gerenciamento do usuário ou fazer alterações na configuração do inquilino nos últimos 90 dias. Os resultados da pesquisa podem conter informações jurídicas valiosas sobre atividades específicas que foram conduzidos por um usuário ou um administrador. Consulte [auditadas atividades no Office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) para obter uma descrição do usuário e atividades administrativas que são registradas no Office 365.

Eventos do SharePoint Online e o OneDrive for Business são exibidos no log de 30 minutos do sua ocorrência. Eventos do Exchange Online aparecem nos logs de auditoria dentro de 24 horas de ocorrência. Eventos de logon do Windows Azure AD estão disponíveis em questão de minutos da ocorrência e outros eventos de diretório do Windows Azure AD estão disponíveis dentro de 24 horas de ocorrência. Eventos nos resultados de pesquisa de log de auditoria também podem ser exportados para análise adicional. (Um máximo de 50.000 entradas pode ser exportado de uma pesquisa de log de auditoria único. Para exportar as entradas mais que isso limitar, reduza o intervalo de datas, ou executar várias pesquisas de log de auditoria.)

A tabela a seguir detalha algumas das informações que são exibidas em relatórios de atividade. Consulte o [log de auditoria de propriedades detalhadas no Office 365](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) para obter mais informações sobre quais propriedades são coletadas por cada carga de trabalho do Office 365.

| Propriedade | Descrição |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Data | Data e hora do evento |
| Usuário | Usuário que executou a ação |
| ClientIP | Endereço IPv4 ou IPv6 do dispositivo que foi usado quando a atividade foi registrada. |
| CreationTime | Data e hora no tempo Universal Coordenado (UTC) quando o usuário desempenhou a atividade. |
| EventSource | Identifica que um evento ocorreu. Valores possíveis são SharePoint e ObjectModel. |
| ID | ID da entrada do relatório. A ID identifica exclusivamente a entrada do relatório. |
| Operation | Nome do usuário ou da atividade, que corresponde ao valor selecionado nos resultados da exibição para esta atividade do usuário. |
| ID da organização | GUID do serviço do Office 365 da organização onde o evento ocorreu. |
| UserAgent | Informações sobre o navegador do usuário conforme fornecido pelo navegador. |
| UserId | Usuário que executou a ação (especificada na propriedade operação) que resultou no registro que está sendo registrado. |
| UserType | Tipo de usuário que executou a operação. Os valores a seguir indicam o tipo de usuário. |
|  | 0 indica que um usuário regular. |
|  | 2 indica que um administrador em sua organização do Office 365. |
|  | 3 indica uma datacenter administrador ou datacenter sistema conta da Microsoft. |
| Carga de trabalho | Em que ocorreu a atividade do serviço do Office 365. Os valores possíveis para essa propriedade são: |
|  | Exchange Online |
|  | SharePoint Online |
|  | OneDrive for Business |
|  | Relatórios do Azure Active Directory |


Para obter etapas detalhadas pesquisar o Office 365 logs de auditoria, consulte [os logs de auditoria de pesquisando no Office 365 Security & Centro de conformidade](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c).

## <a name="search-unified-audit-log"></a>Pesquisar o Log de auditoria unificada
O recurso de pesquisa de Log de auditoria na segurança & Centro de conformidade pode ser usado para pesquisar o log de auditoria unificada. O Office 365 também fornece a capacidade de pesquisar desse log usando o PowerShell remoto. Especificamente, o [cmdlet Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) no PowerShell do Exchange Online pode ser usado para pesquisar no log de auditoria unificada de eventos relacionadas às operações de usuário do Exchange Online, SharePoint Online, OneDrive for Business e Azure AD. Você pode pesquisar todos os eventos em um intervalo de datas especificado ou, você pode filtrar os resultados com base em critérios específicos, como uma ação específica, o usuário que executou a ação, ou o objeto de destino. Os administradores podem usar até 3 executados simultaneamente sessões do PowerShell do Exchange Online para dividir as pesquisas de intervalo de data grande.
