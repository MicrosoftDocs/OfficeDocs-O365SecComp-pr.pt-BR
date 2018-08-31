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
# <a name="office-365-management-activity-api"></a>API da Atividade de Gestão do Office 365
A Microsoft fornece serviços de relatórios que permitem que administradores obter informações de transacionais agregadas sobre seu locatário do Office 365. A [API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) usa um design de padrão do setor por REST e OAuth v2 para autenticação, o que torna mais fácil começar a experimentar com recuperação de dados e a inclusão em aplicativos e ferramentas de visualização. A API fornece dados de um feed que inclui informações sobre atividades do usuário, administrador, operações e segurança no Office 365. Os dados podem ser mantidos para fins normativos ou combinados com dados de log comprados de uma infraestrutura local ou outras fontes para criar uma solução de monitoramento de operações, segurança e conformidade em toda a empresa.

A API de atividade de gerenciamento do Office 365 fornece informações sobre vários usuário, admin, sistema e ações de política e eventos do Office 365 e logs de atividade do Azure Active Directory. A API fornece um esquema de auditoria consistente com mais de 10 campos que estão em comum entre todos os serviços. Isso permite que as organizações a fazer conexões fácil entre os eventos, e ela permite novas maneiras de motivo sobre os dados. Dezenas de fornecedores independentes de Software (ISVs) têm uma parceria com a Microsoft e construído soluções com base na API. Algumas soluções concentram-se exclusivamente nos dados do Office 365, enquanto outros fornecem a capacidade de incluir os dados de diversos sistemas locais e provedores de nuvem para criar uma exibição unificada de todas as operações, segurança e atividades relacionadas à conformidade. Para obter mais informações, consulte a [referência de API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).
