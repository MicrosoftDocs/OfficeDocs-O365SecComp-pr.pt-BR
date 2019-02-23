---
title: Visão geral dos recursos de pesquisa e descoberta eletrônica do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Uma visão geral do recurso de descoberta eletrônica e outros recursos de pesquisa no Office 365 para o uso de auditoria e transparência.
ms.openlocfilehash: 0d1d0341407546659f4efffac8409edd46312810
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214849"
---
# <a name="ediscovery-and-search-features"></a>Recursos de pesquisa e descoberta eletrônica 

## <a name="ediscovery"></a>Descoberta Eletrônica
O recurso de descoberta eletrônica fornece um único local para administradores, responsáveis pela conformidade e outros usuários autorizados a realizar uma investigação abrangente na atividade do usuário do Office 365. Os responsáveis pela segurança com as permissões apropriadas podem realizar pesquisas e armazenar bloqueios de conteúdo. Os resultados da pesquisa são os mesmos resultados obtidos de uma pesquisa de conteúdo, exceto pelo fato de que um caso de descoberta eletrônica é criado para qualquer retenção aplicada. Os resultados das pesquisas de descoberta eletrônica são criptografados por segurança e os dados exportados podem ser analisados usando a [descoberta eletrônica avançada](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4).

## <a name="content-search"></a>Pesquisa de Conteúdo
A [pesquisa de conteúdo](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) é uma nova ferramenta de pesquisa de descoberta eletrônica no centro de conformidade do _AMP_ de segurança que oferece recursos aprimorados de escala e desempenho em relação às ferramentas de pesquisa de descoberta eletrônica anteriores Você pode usar a pesquisa de conteúdo para pesquisar caixas de correio, pastas públicas, sites do SharePoint Online e locais do OneDrive for Business. A pesquisa de conteúdo foi projetada especificamente para pesquisas muito grandes. Não há limites para o número de caixas de correio e sites que você pode pesquisar. Também não há limites para o número de pesquisas que podem ser executadas ao mesmo tempo. Após executar uma pesquisa, o número de fontes de conteúdo e um número estimado de resultados de pesquisa são exibidos no painel de detalhes na página de pesquisa, onde você pode visualizar os resultados ou exportá-los para um computador local. Se sua organização tiver uma assinatura do Office 365 Enterprise e5, você também poderá [preparar os resultados](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) para análise usando os recursos avançados de análise da [descoberta eletrônica avançada do Office 365](http://go.microsoft.com/fwlink/p/?LinkID=620116).

## <a name="audit-log-search"></a>Pesquisa de Log de Auditoria
Além de controlar as alterações na sua organização do Office 365, os clientes também podem exibir relatórios de auditoria e exportar logs de auditoria. Depois que a auditoria estiver habilitada para um locatário do Office 365, as atividades administrativas e de usuário desse locatário serão registradas nos logs de eventos e tornadas pesquisáveis. Por exemplo, você pode usar o registro em log de auditoria de caixa de correio para rastrear ações executadas em uma caixa de correio por usuários diferentes do proprietário da caixa de correio. Além disso, os gerentes de conformidade podem usar os recursos de pesquisa e filtro para ver se um usuário exibiu ou baixou um documento específico ou se um administrador realizou atividades de gerenciamento de usuário ou fez alterações na configuração do locatário nos últimos 90 dias. Os resultados da pesquisa podem conter informações legais valiosas sobre atividades específicas que foram conduzidas por um usuário ou um administrador. Consulte [atividades auditadas no Office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) para obter uma descrição das atividades administrativas e de usuário registradas no Office 365.

Os eventos do SharePoint Online e do OneDrive for Business são exibidos no log dentro de 30 minutos de sua ocorrência. Os eventos do Exchange Online aparecem nos logs de auditoria dentro de 24 horas de ocorrência. Eventos de logon do Azure AD estão disponíveis em minutos de ocorrência e outros eventos de diretório do Azure AD estão disponíveis dentro de 24 horas de ocorrência. Os eventos nos resultados de pesquisa do log de auditoria também podem ser exportados para análise adicional. (No máximo 50.000 entradas podem ser exportadas de uma única pesquisa de log de auditoria. Para exportar mais entradas desse limite, reduza o intervalo de datas ou execute várias pesquisas de log de auditoria.

A tabela a seguir detalha algumas das informações exibidas nos relatórios de atividades. Consulte as [propriedades detalhadas no log de auditoria do Office 365](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) para obter mais informações sobre quais propriedades são coletadas por cada carga de trabalho do Office 365.

| Propriedade | Descrição |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Data | Data e hora do evento |
| Usuário | Usuário que executou a ação |
| ClientIP | Endereço IPv4 ou IPv6 do dispositivo que foi usado quando a atividade foi registrada. |
| CreationTime | Data e hora no tempo universal coordenado (UTC) quando o usuário realizou a atividade. |
| EventSource | Identifica se um evento ocorreu. Os valores possíveis são SharePoint e ObjectModel. |
| ID | ID da entrada de relatório. A identificação identifica exclusivamente a entrada de relatório. |
| Operation | Nome do usuário ou atividade, que corresponde ao valor selecionado em exibir resultados para esta atividade do usuário. |
| ID | GUID do serviço do Office 365 da organização onde o evento ocorreu. |
| UserAgent | Informações sobre o navegador do usuário, conforme fornecido pelo navegador. |
| ID | O usuário que executou a ação (especificado na Propriedade Operation) que resultou no registro que está sendo registrado em log. |
| UserType | Tipo de usuário que executou a operação. Os valores a seguir indicam o tipo de usuário. |
|  | 0 indica um usuário regular. |
|  | 2 indica um administrador na sua organização do Office 365. |
|  | 3 indica um administrador de datacenter da Microsoft ou uma conta de sistema de datacenter. |
| Carga de trabalho | Serviço do Office 365 no qual a atividade ocorreu. Os valores possíveis para esta propriedade são: |
|  | Exchange Online |
|  | SharePoint Online |
|  | OneDrive for Business |
|  | Relatórios do Azure Active Directory |


Para obter etapas detalhadas para pesquisar logs de auditoria do Office 365, consulte [Searching Audit Logs in the office 365 Security _AMP_ Compliance Center](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c).

## <a name="search-unified-audit-log"></a>Pesquisar log de auditoria uniFicada
O recurso pesquisa de log de auditoria no centro de conformidade do & de segurança pode ser usado para pesquisar o log de auditoria unificada. O Office 365 também oferece a capacidade de Pesquisar esse log usando o PowerShell remoto. Especificamente, o [cmdlet Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) no PowerShell do Exchange Online pode ser usado para pesquisar o log de auditoria unificada de eventos relacionados às operações do usuário do Exchange Online, do SharePoint Online, do onedrive for Business e do Azure AD. Você pode pesquisar todos os eventos em um intervalo de datas especificado ou pode filtrar os resultados com base em critérios específicos, como uma ação específica, o usuário que executou a ação ou o objeto de destino. Os administradores podem usar até 3 executando simultaneamente sessões do PowerShell do Exchange Online para dividir pesquisas de intervalo de datas grandes.
