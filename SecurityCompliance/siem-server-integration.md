---
title: Integração do servidor SIEM com Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
description: 'Resumo: Leia este artigo para obter uma visão geral da integração do servidor SIEM com Microsoft 365.'
ms.openlocfilehash: bd512ca6d75928712e3444581a78610a0869123d
ms.sourcegitcommit: 63ed467fc3e1ab1ab9ee122df97c64737169834e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2018
ms.locfileid: "25842673"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Integração do SIEM server com aplicativos e serviços da Microsoft 365

## <a name="overview"></a>Visão geral

Se sua organização estiver usando um servidor de informações de segurança e gerenciamento de evento (SIEM), ou se você estiver planejando obter um servidor SIEM em breve, talvez você queira saber como que vai integre sua 365 da Microsoft, incluindo o Office 365 Enterprise. Se você precisa de um servidor SIEM depende de vários fatores, como os requisitos de segurança da sua organização. Microsoft 365 oferece uma variedade de recursos de segurança; No entanto, se sua organização tiver conteúdo e aplicativos no local e na nuvem (como no caso de uma implantação de nuvem híbrida), considere adicionar um servidor SIEM para proteção extra. Ou, se sua organização tem requisitos de segurança particularmente rígidas que devem ser atendidos, considere a adição de um servidor SIEM ao seu ambiente.

## <a name="siem-server-integration-microsoft-365"></a>Integração do servidor SIEM 365 da Microsoft

Um servidor SIEM pode receber dados de uma ampla variedade de aplicativos e serviços da Microsoft 365. A tabela a seguir lista as várias Microsoft 365 serviços e aplicativos, juntamente com entradas de servidor SIEM e aonde ir para saber mais sobre a integração do servidor SIEM. 

| Serviço Microsoft 365 ou aplicativo | Entradas de servidor SIEM | Recursos para saber mais |
| --- | --- | --- |
| [Proteção Avançada contra Ameaças do Office 365](office-365-atp.md)  <br/>   ou   <br/>[Inteligência Contra Ameaças do Office 365](office-365-ti.md) | Logs de auditoria | [Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Integração de log | [Integração de SIEM com segurança de aplicativo de nuvem Microsoft](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | Integração de log | [Integrar seu servidor SIEM ao Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md) |
| [Proteção Avançada Contra Ameaças do Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/) | Integração de log | [Alertas de recepção para suas ferramentas SIEM](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Central de segurança do Windows Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Proteção contra ameaças e detecção de ameaça) | Alertas | [Exportação de dados de segurança Azure SIEM - configuração de Pipeline - Preview](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Proteção de identidade do Azure Active Directory](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Logs de auditoria | [Integrar os logs de auditoria do Active Directory do Azure](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Análise de ameaça avançado Azure](https://docs.microsoft.com/azure/security/azure-threat-detection) | Integração de log | [Referência de log do ATA SIEM](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>Log de auditoria deve ser ativado

Verifique se o log de auditoria está ativado antes de configurar a integração do servidor SIEM. 

- SharePoint Online, OneDrive for Business e Windows Azure Active Directory, o [log de auditoria está ativado no Centro de conformidade & segurança](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Para Exchange Online, [o log de auditoria está ativado com o Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>Confira também

[Adoção da nuvem e soluções híbridas](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Guias do Laboratório de Teste (TLGs) para adoção de nuvem](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


