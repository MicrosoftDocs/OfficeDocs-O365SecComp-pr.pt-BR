---
title: Monitoramento do Office 365 e acessar os controles de auditoria
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
description: 'Resumo: Um resumo das diversas monitoramento e auditoria acesso controles disponíveis no Office 365.'
ms.openlocfilehash: 7ef25d62ce3c4fa320dd0b164183c6f67be7d76d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524575"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>Monitoramento e auditoria de acessar os controles no Office 365

Microsoft realiza extensiva de monitoramento e auditoria de delegação todos, todo o uso de privilégios e todas as operações que ocorrem no Office 365. Controle do Office 365 access é um processo automatizado criado sobre o princípio de privilégio mínimo e incorporar auditorias e controles de acesso de dados:
- Todo o acesso permitido é atribuído a um usuário exclusivo, tornando os administradores responsáveis por sua tratamento de conteúdo do cliente.
- Solicitações de controle de acesso, aprovações e logs de operações administrativas são capturados para análise de ideias de segurança e eventos mal-intencionados.
- Níveis de acesso são revisados no próximo a associação de grupo de segurança com base em tempo real para garantir que somente os usuários que tenham autorizados justificativas comerciais e atendem aos requisitos de qualificação tenham acesso aos sistemas.
- O Office 365, sua acessar os controles e serviços de suportados, incluindo o Azure Active Directory e nossos centros de dados físicos sejam auditados regularmente por terceiros independentes para fins de conformidade com [ISO/IEC 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)e outros [padrões](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Engenheiros de Office 365 são necessárias para tirar anual treinamento de segurança revisando riscos e práticas recomendadas de acesso com privilégios elevados e segurança da Microsoft e as políticas de privacidade para continuar a manutenção de seus direitos para o serviço de confirmação.

Alertas automatizados são acionadas quando é detectada atividade suspeita, como vários logins com falha dentro de um curto período. A equipe de resposta de segurança do Office 365 usa o aprendizado de máquina e análise de dados grande para examinar e analisar atividade para os padrões de acesso irregular e proativamente responder às atividades anômalos e ilícitas. A Microsoft também emprega uma equipe dedicada de testadores invasão e participa de equipe vermelho periódica e equipe azul exercícios para localizar a segurança e problemas no serviço de controle de acesso. Os clientes também podem verificar a eficácia dos sistemas de controle de acesso usando os relatórios de auditoria e a atividade de gerenciamento de API fornecida pelo Office 365. 

Para obter mais informações, consulte [referência de API de atividade de gerenciamento do Office 365](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) e [auditoria e relatórios no Office 365](office-365-auditing-and-reporting-overview.md).
