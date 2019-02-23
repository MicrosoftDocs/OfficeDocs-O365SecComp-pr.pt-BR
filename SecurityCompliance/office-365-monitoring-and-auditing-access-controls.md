---
title: Controles de acesso de monitoramento e auditoria do Office 365
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
description: 'Resumo: um resumo dos vários controles de acesso de monitoramento e auditoria disponíveis no Office 365.'
ms.openlocfilehash: 91d78ba3de41554755a7c19799eb1f7b25933b05
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217731"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>Monitoramento e auditoria de controles de acesso no Office 365

A Microsoft executa monitoramento e auditoria abrangentes de toda delegação, todo o uso de privilégios e todas as operações que ocorrem no Office 365. O controle de acesso do Office 365 é um processo automatizado desenvolvido com base no princípio de privilégios mínimos e para incorporar auditorias e controles de acesso a dados:
- Todo o acesso permitido é rastreável para um usuário exclusivo, tornando os administradores responsáveis por lidar com o conteúdo do cliente.
- Solicitações de controle de acesso, aprovações e logs de operações administrativas são capturadas para análise de informações de segurança e eventos mal-intencionados.
- Os níveis de acesso são analisados quase em tempo real com base na associação de grupo de segurança para garantir que apenas usuários com justificativas de negócios autorizadas e atendam aos requisitos de qualificação tenham acesso aos sistemas.
- O Office 365, seus controles de acesso e serviços de suporte, incluindo o Active Directory do Azure e nossos data centers físicos, são auditados regularmente por terceiros independentes para conformidade com [ISO/iec 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)e outros [padrões](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Os engenheiros do Office 365 são necessários para o treinamento de segurança anual, revisando as práticas recomendadas de acesso elevado e riscos e confirmar as políticas de segurança e privacidade da Microsoft para continuar mantendo suas titularidades com o serviço.

Os alertas automatizados são disparados quando uma atividade suspeita é detectada, como vários logons com falha dentro de um curto período de tempo. A equipe de resposta de segurança do Office 365 usa o Machine Learning e a grande análise de dados para analisar e analisar a atividade de padrões de acesso irregular e responder proativamente a atividades anômalas e ilícitas. A Microsoft também emprega uma equipe dedicada de testadores de penetração e participa da equipe vermelha periódica e de exercícios de equipe azuis para encontrar problemas de segurança e controle de acesso no serviço. Os clientes também podem verificar a eficácia dos sistemas de controle de acesso usando os relatórios de auditoria e a API de atividade de gerenciamento fornecida pelo Office 365. 

Para obter mais informações, consulte referência e auditoria da [API de atividade de gerenciamento do office 365](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) e [relatórios no Office 365](office-365-auditing-and-reporting-overview.md).
