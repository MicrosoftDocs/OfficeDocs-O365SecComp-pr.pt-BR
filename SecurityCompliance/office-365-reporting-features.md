---
title: Recursos de relatório do Office 365
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
description: Uma explicação dos relatórios de recursos no Office 365.
ms.openlocfilehash: 5a448089de5d517b81551269416c4a6f91599725
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524642"
---
# <a name="office-365-reporting-features"></a>Recursos de relatório do Office 365 

## <a name="introduction"></a>Introdução
O recurso de relatórios no Office 365 fornece uma variedade de relatórios de auditoria para Windows Azure AD (Active Directory), o Exchange Online, gerenciamento de dispositivos, análise de supervisão e prevenção de perda de dados (DLP). Estes são diferentes e separados dos relatórios de atividade do Office 365.

## <a name="office-365-reports-dashboard"></a>Painel de relatórios do Office 365
O painel de relatórios na visualização da Central de administração do Office 365 exibe a atividade de uso entre o Office 365. Administradores globais do Office 365, ou um Exchange Online, SharePoint Online ou Skype para administrador de negócios, pode obter granular ideias sobre o uso desse serviço. Relatórios podem fornecer ideias sobre como o número de usuários consumindo um serviço específico do Office 365, o número de usuários que ativou o Office Professional Plus e quanta email passam pela organização. Relatórios estão disponíveis para os últimos 7, 30, 90 e 180 dias.

Os seguintes relatórios estão disponíveis:
- [Relatório de atividade de email](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Relatório de ativações do Microsoft Office](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [Relatório de uso do Site do SharePoint Online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive para relatório de uso de negócios](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Relatório de atividades do Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype para relatório de atividade de negócios](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype para relatório de atividade de negócios ponto a ponto](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype para relatório de negócios organizador da conferência](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype para relatório de atividade de participante de conferência de negócios](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Para obter mais informações, consulte [Relatórios de atividade no Centro de administração do Office 365](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).


## <a name="azure-active-directory-reports"></a>Relatórios do Azure Active Directory
O Office 365 usa o Azure AD para autenticação e gerenciamento de identidade. Administradores do Office 365 podem usar os relatórios gerados pelo Windows Azure para procurar uma atividade incomum e acesso não autorizado aos dados. Você pode usar os relatórios de uso e de acesso no Azure AD para ganhar visibilidade sobre a integridade e a segurança de diretório da sua organização. Com essa informação, um administrador pode determinar melhor onde os possíveis riscos de segurança pode ser para que eles possam se planejar atenuar esses riscos adequadamente.

Relatórios do Azure AD podem ser exportados para o Microsoft Excel e correlacionados com outros dados do Office 365, como os resultados de uma pesquisa de log de auditoria, para fornecer a percepção de acesso, autenticação e atividades de nível de aplicativo. Relatórios de uso de anomalias e recursos avançados estão disponíveis quando o Azure AD Premium está habilitado. Essas avançadas de relatórios que ajudam a melhorar a organizações de Ajuda e condições de segurança da organização responde possíveis ameaças aproveitando a análise de uso de acesso e o aplicativo do dispositivo. Para obter mais informações, consulte [relatórios do Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Relatórios de auditoria on-line do Exchange
Os relatórios de auditoria Exchange Online incluem detalhes sobre o acesso de caixa de correio e as alterações feitas pelos administradores de Inquilino de uma organização Exchange Online. Depois que a auditoria de caixa de correio estiver habilitada, você pode usar as tarefas na tabela a seguir para executar relatórios e exportar logs de auditoria Exchange Online.

>**Observação**: você deve habilitar a caixa de correio log de auditoria de cada caixa de correio de forma que os eventos auditados são salvos no log de auditoria para essa caixa de correio. Se a auditoria de caixa de correio log não está habilitado para uma caixa de correio, os eventos para essa caixa de correio não serão salvas no log de auditoria e não aparecerão em relatórios de auditoria de caixa de correio. Para obter mais informações, consulte [Habilitar a auditoria de caixa de correio](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Tarefa | Descrição |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Executar um relatório de acesso não proprietário da caixa de correio](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Exibe a lista de caixas de correio que foram acessados por alguém que não seja o proprietário da caixa de correio. O relatório contém informações sobre quem acessou a caixa de correio, as ações que faziam na caixa de correio, e se as ações foram bem-sucedidas. |
| [Exportar logs de auditoria de caixas de correio](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Logs de auditoria de caixas de correio contêm informações sobre ações em uma caixa de correio ocupado por um usuário que não seja o proprietário da caixa de correio e acesso. Os administradores podem especificar as caixas de correio, juntamente com um intervalo de datas para gerar relatórios. Os logs são exportados em XML, anexados a uma mensagem e enviados a usuários específicos, conforme determinado pelo administrador. |
| [Executar relatório do grupo de funções de administrador](https://docs.microsoft.com/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | O grupo de funções de administrador é usado para atribuir privilégios administrativos aos usuários. Esses privilégios permitir que os usuários executar tarefas administrativas, como redefinir senhas, criar ou modificar caixas de correio e atribuem privilégios de administrador para outros usuários. O relatório do grupo de função admin mostra as alterações a grupos de funções, incluindo a adição ou remoção de membros. |
| [Exibir o log de auditoria do administrador](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | As listas de relatório de log do admin auditoria todos criar, atualizar e excluir as funções executadas pelos administradores no Exchange Online. Entradas de log fornecem informações sobre qual cmdlet foi executado, quais parâmetros foram usados, quem a executou o cmdlet e quais objetos foram afetados. |
| [Em espera e pesquisa de conteúdo de caixa de correio](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Fornece detalhes de todas as alterações para descoberta eletrônica In-loco ou retenção In-loco configurações em caixas de correio. |
| [Exportar o log de auditoria do administrador](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Os registros de log de auditoria do administrador ações administrativas específicas, como criar, atualizar e excluir no Exchange Online. Os resultados do log de são exportados para o XML e os administradores podem optar por enviar esse log para um conjunto de usuários. |
| [Executar um relatório de suspensão de litígio por caixa de correio](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Fornece detalhes de todas as alterações a litígios mantenha as configurações em caixas de correio. |
| [Exibir e exportar o log de auditoria do administrador externo](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contém detalhes das ações executadas pelos administradores externos. As entradas fornecem informações no qual o cmdlet foi executar, quais parâmetros foram usados e nenhuma ação que cria, modificar ou excluir objetos no Exchange Online. |

## <a name="device-compliance-reports"></a>Relatórios de conformidade do dispositivo
Você pode gerenciar e proteger dispositivos móveis se estivessem conectados à sua organização do Office 365 usando o Office 365 Mobile Device Management (MDM). Dispositivos móveis, como smartphones e tablets que são usados para acessar o trabalho de email, calendário, contatos e documentos reproduzir uma grande parte na certificando-se de que os funcionários sejam capazes de funcionar a qualquer momento e de qualquer lugar. Como resultado, é essencial que você proteja as informações da sua organização. Você pode usar o Office 365 MDM para definir regras de acesso e políticas de segurança de dispositivo e apagar dispositivos móveis se eles estiver perdidos ou roubados.

Relatórios de conformidade do MDM fornecem uma visão geral das políticas que tenha sido configurado por uma organização para proteger os dispositivos móveis que estão acessando dados do Office 365. O relatório permite a filtragem de dispositivos por status de conformidade, reportadas violações, dispositivos bloqueados e quantos dispositivos foram apagados como resultado de diretivas de segurança. Para obter mais informações, consulte [Visão geral do gerenciamento de dispositivos móveis para o Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Prevenção contra perda de dados
Políticas de DLP ajudam a gerenciar a segurança e o fluxo de informações em uma organização. Você pode configurar políticas para bloquear o acesso a conteúdo, criptografar dados ou notificar os usuários de política e violações de política usa dicas de política de DLP no aplicativo. Relatórios de DLP fornecem informações sobre o número de política e à regra de correspondências, substituições e falsos positivos.

Você pode usar o Centro de administração do Office 365 para exibir informações sobre o número de mensagens que são detectados pelas suas políticas de DLP em formato de tabela ou gráfico gráfico. Especificamente, correspondências de política DLP para enviados e recebidos emails e correspondências de regra DLP para email enviado e recebido. Também é possível exibir o número de correspondências, substituições e falsos positivos para cada política dentro das últimas 24 horas usando o Centro de administração do Exchange. No entanto, esses dados não estão disponíveis como um gráfico. Se você baixar um relatório para uso no Excel, você pode exibir ainda mais detalhes, como quem enviou qual mensagem, em que dia, e corresponde a qual política foram acionadas. Para obter mais informações, consulte [Exibir relatórios sobre detecções de política DLP](https://technet.microsoft.com/en-us/library/jj889415(v=exchg.150).aspx).

## <a name="auditing-in-yammer-enterprise"></a>Auditorias no Yammer Enterprise
Yammer que Enterprise fornece aos administradores com a capacidade de exportar dados de atividade do usuário de suas redes de Yammer por meio da [API de exportação de dados do Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)ou manualmente por meio da página de administração de rede do Yammer. A capacidade de exportar logs é restrita aos administradores de rede no Yammer. (Todos os administradores globais do Office 365 são os administradores de rede do Yammer.)

Os seguintes dados podem ser exportados:

| Nome do arquivo | Descrição |
|----------------------------|-------------------------------------------------------------------------|
| Users | Todos os usuários novos, pendentes e suspensos na rede |
| Messages.csv | Todas as mensagens na rede |
| Files.csv (metadados) | Metadados, como o nome do arquivo, arquivo API URL, o carregador ID, carregado no, etc. |
| Files.csv (arquivos originais) | Arquivo zip dos arquivos originais que foram carregados por usuários no Yammer |
| Topics.csv | Tópicos criados na rede |
| Pages.csv | Páginas (notes) criadas pelos usuários na rede |
| Admins.csv | Todos verificado administradores na rede |
| Networks.csv | Todas as redes externas do Yammer |

*Tabela 3 - Yammer dados arquivos de rede disponíveis para exportação pelos clientes*

Dados do Yammer da empresa também estão disponíveis por meio dos relatórios de atividade do Office 365. Além disso, Yammer está trabalhando ativamente na expondo adicional log via a API de atividade de gerenciamento do Office 365 e a capacidade de motivo sobre os dados usando o Power BI. Consulte o [Mapa do Office](https://fasttrack.microsoft.com/roadmap?filters=yammer) para obter mais informações sobre esses recursos.
