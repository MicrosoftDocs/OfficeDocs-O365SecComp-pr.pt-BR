---
title: Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Integre o servidor SIEM da sua organização com inteligência de ameaça do Office 365 e avançadas de proteção de ameaça com a API de gerenciamento de atividade do Office 365.
ms.openlocfilehash: 40c84b9d7b7ec4c9b15383e3ffbbabf839294def
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782138"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas

Se sua organização estiver usando um servidor de gerenciamento (SIEM) de incidente e eventos de segurança, você poderá integrar o Office 365 Threat Intelligence e proteção avançada de ameaça com seu servidor SIEM. Integração de SIEM permite que você exiba informações, como malware detectado pelo proteção avançada do Office 365 e inteligência de ameaça, em seus relatórios do servidor SIEM. Para configurar a integração de SIEM, você deve usar a [API de gerenciamento de atividade do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

A API de gerenciamento de atividade do Office 365 recupera informações sobre o usuário, admin, sistema e ações de política e eventos do Office 365 e os logs de atividade do Azure Active Directory da sua organização. O [esquema de inteligência de ameaça e a proteção de ameaça avançadas do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funciona com inteligência de ameaça e/ou avançada contra ameaças, portanto, se sua organização tiver avançada proteção contra ameaças mas não inteligência de ameaça (ou vice-versa), você pode ainda use essa mesma API para sua integração do servidor SIEM. 

O servidor SIEM ou outro sistema semelhante deve sondar a carga de trabalho **audit.general** eventos de detecção de acesso. Para saber mais, consulte [Introdução ao APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou ter a função de administrador de segurança atribuída no Centro de conformidade & segurança ao configurar a integração de SIEM com inteligência de ameaça do Office 365 e proteção avançada de ameaça.</br>Log de auditoria deve ser ativado para o seu ambiente do Office 365. Para obter ajuda com isso, consulte [Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 

[Inteligente de relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md)
  
[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  

