---
title: API da Atividade de Gerenciamento do Office 365
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
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Um breve resumo sobre a API da atividade de gerenciamento do Office 365.
ms.openlocfilehash: ca5517d3049830cd7be912b2e2e47a34a866aca0
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090553"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="145dd-103">API da Atividade de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="145dd-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="145dd-p101">A Microsoft fornece o Reporting Services que permite que os administradores obtenham informações transacionais agregadas sobre o locatário do Office 365. A [API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) usa um design RESTful padrão da indústria e o OAuth v2 para autenticação, o que facilita o início da experimentação com a recuperação de dados e sua inclusão em ferramentas e aplicativos de visualização. A API fornece um feed de dados que inclui informações sobre o usuário, administrador, operações e atividade de segurança no Office 365. Os dados podem ser mantidos por razões regulamentares ou combinados com os dados de log adquiridos de uma infraestrutura local ou de outras fontes para criar uma solução de monitoramento para operações, segurança e conformidade em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="145dd-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="145dd-p102">A API de atividade de gerenciamento do Office 365 fornece informações sobre várias ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory. A API fornece um esquema de auditoria consistente com mais de 10 campos que são comuns em todos os serviços. Isso permite que as organizações façam conexões fáceis entre eventos e permite que as novas maneiras de se deparam com os dados. Dezenas de ISVs (fornecedores de software independentes) fizeram parceria com a Microsoft e criaram soluções com base na API. Algumas soluções estão concentradas exclusivamente nos dados do Office 365, enquanto outras oferecem a capacidade de incluir dados de vários provedores de nuvem e sistemas locais para criar uma visão unificada de todas as operações, segurança e atividade relacionada à conformidade. Para obter mais informações, consulte a [referência da API da atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="145dd-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
