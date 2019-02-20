---
title: Integração do SIEM com o Office 365 Threat Intelligence e proteção avançada contra ameaças
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
description: Integre o servidor SIEM da sua organização com o Office 365 Threat Intelligence e proteção avançada contra ameaças com a API de gerenciamento de atividades do Office 365.
ms.openlocfilehash: 854f763b72dfac1a5dc1442b1d9d123ed5439257
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087240"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Integração do SIEM com o Office 365 Threat Intelligence e proteção avançada contra ameaças

Se sua organização estiver usando um servidor de gerenciamento de incidentes e eventos de segurança (SIEM), você poderá integrar o Office 365 Threat Intelligence e a proteção avançada contra ameaças ao seu servidor SIEM. A integração do SIEM permite que você visualize informações, como malware detectado pelo Office 365 Advanced Protection and Threat Intelligence, em seus relatórios do SIEM Server. Para configurar a integração do SIEM, use a [API de gerenciamento de atividades do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

A API de gerenciamento de atividades do Office 365 recupera informações sobre ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory da sua organização. O [esquema de proteção avançada contra ameaças e inteligência](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) contra ameaças do Office 365 funciona com inteligência de ameaças e/ou proteção avançada contra ameaças, portanto, se sua organização tiver proteção avançada contra ameaças, mas não inteligência de ameaças (ou vice-versa), você poderá ainda use essa mesma API para sua integração com o servidor do SIEM. 

O servidor SIEM ou outro sistema semelhante deve sondar a **auditoria.** carga de trabalho geral para acessar eventos de detecção. Para saber mais, confira [introdução às APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou ter a função de administrador de segurança atribuída para o centro de conformidade do & de segurança para configurar a integração do SIEM com a proteção avançada contra ameaças do Office 365.<br/>O log de auditoria deve estar ativado para o seu ambiente do Office 365. Para obter ajuda com isso, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 

[Relatórios inteligentes e insights no centro de conformidade de &amp; segurança do Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md)
  

