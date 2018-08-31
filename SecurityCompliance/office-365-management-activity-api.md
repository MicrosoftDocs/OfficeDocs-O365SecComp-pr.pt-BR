---
title: API da Atividade de Gestão do Office 365
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
description: Um breve resumo sobre a API de atividade de gerenciamento do Office 365.
ms.openlocfilehash: 4753be89c008676d5244b5c659c3dd1a545975b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523551"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="80d08-103">API da Atividade de Gestão do Office 365</span><span class="sxs-lookup"><span data-stu-id="80d08-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="80d08-p101">A Microsoft fornece serviços de relatórios que permitem que administradores obter informações de transacionais agregadas sobre seu locatário do Office 365. A [API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) usa um design de padrão do setor por REST e OAuth v2 para autenticação, o que torna mais fácil começar a experimentar com recuperação de dados e a inclusão em aplicativos e ferramentas de visualização. A API fornece dados de um feed que inclui informações sobre atividades do usuário, administrador, operações e segurança no Office 365. Os dados podem ser mantidos para fins normativos ou combinados com dados de log comprados de uma infraestrutura local ou outras fontes para criar uma solução de monitoramento de operações, segurança e conformidade em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="80d08-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="80d08-p102">A API de atividade de gerenciamento do Office 365 fornece informações sobre vários usuário, admin, sistema e ações de política e eventos do Office 365 e logs de atividade do Azure Active Directory. A API fornece um esquema de auditoria consistente com mais de 10 campos que estão em comum entre todos os serviços. Isso permite que as organizações a fazer conexões fácil entre os eventos, e ela permite novas maneiras de motivo sobre os dados. Dezenas de fornecedores independentes de Software (ISVs) têm uma parceria com a Microsoft e construído soluções com base na API. Algumas soluções concentram-se exclusivamente nos dados do Office 365, enquanto outros fornecem a capacidade de incluir os dados de diversos sistemas locais e provedores de nuvem para criar uma exibição unificada de todas as operações, segurança e atividades relacionadas à conformidade. Para obter mais informações, consulte a [referência de API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="80d08-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
