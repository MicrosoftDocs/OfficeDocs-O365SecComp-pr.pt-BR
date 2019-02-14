---
title: Visão geral do painel de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection: M365-security-compliance
description: Use o novo painel de segurança para examinar o Status de proteção de ameaça do Office 365 e exibir e agir em alertas de segurança.
ms.openlocfilehash: 403c47ed09e9652a66abeafb93be02589c9b1702
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995122"
---
# <a name="security-dashboard"></a>Painel de segurança

## <a name="overview"></a>Visão geral

O [segurança &amp; Centro de conformidade](go-to-the-securitycompliance-center.md) permite que sua organização gerenciar a conformidade e proteção de dados. Supondo que você tem as permissões necessárias, o painel de segurança permite que você revise seu Status de proteção de ameaça, bem como exibir e agir em alertas de segurança. 
  
Assista ao vídeo para obter uma visão geral e, em seguida, leia este artigo para saber mais.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
Dependendo de qual inclui assinatura do Office 365 da sua organização, o painel de segurança inclui várias widgets, como Resumo do gerenciamento de ameaça, o Status de proteção de ameaça, Global detecções de ameaça semanal, Malware e mais algumas, conforme descrito no seções a seguir.
  
Para exibir o painel de segurança, na [a segurança do Office 365 &amp; Centro de conformidade](go-to-the-securitycompliance-center.md), vá para o **gerenciamento de ameaça** \> **painel**.
  
> [!NOTE]
> Você deve ser um administrador global do Office 365, um administrador de segurança ou um leitor de segurança para exibir o painel de segurança. Alguns widgets requerem permissões adicionais para exibir. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="threat-management-summary"></a>Resumo do gerenciamento de ameaça

O widget resumo do gerenciamento de ameaça informa num relance como sua organização foi protegida contra ameaças nos últimos sete (7) dias.

![Painel de segurança - widget resumo do gerenciamento de ameaça](media/SecDash-ThreatMgmtSummary.png)

As informações que você verá no resumo de gerenciamento de ameaça dependem do que inclui a assinatura de você. A tabela a seguir descreve quais informações são incluídas para Office 365 Enterprise E3 e Office 365 Enterprise E5.


|Office 365 Enterprise E3  |Office 365 Enterprise E5  |
|---------|---------|
|Mensagens de malware bloqueadas<br/>Mensagens de phishing bloqueadas<br>Relatado por usuários de mensagens<br><br><br><br> |Mensagens de malware bloqueadas<br>Mensagens de phishing bloqueadas<br>Relatado por usuários de mensagens<br>Bloqueado de malware de dia zero<br>Mensagens de phishing avançadas detectadas<br>URLs mal-intencionadas bloqueados |

Para exibir ou acessar o widget resumo do gerenciamento de ameaça, você deve ter permissões para exibir relatórios de proteção avançada de ameaça. Para saber mais, consulte [quais permissões são necessárias para exibir os relatórios de ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="threat-protection-status"></a>Status de proteção de ameaça

O widget do Status de proteção de ameaça mostra eficácia de proteção de ameaça com uma exibição detalhada e tendência de phishing e malware. 

![Widget de status de proteção de ameaça](media/tpswidget.png)

Os detalhes dependem se a sua assinatura do Office 365 inclui o [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP), com ou sem [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP).


|Se sua assinatura incluir … |Você verá esses detalhes |
|---------|---------|
|EOP, mas não ATP do Office 365     |Email mal-intencionado que foi detectado e bloqueada pelo EOP<br> Consulte [o relatório de Status de proteção de ameaça (EOP)](view-email-security-reports.md#threat-protection-status-report).| |
|O Office 365 ATP |Email de conteúdo e mal-intencionado maliciosa detectadas e bloqueadas pelo EOP e ATP do Office 365<br>Contagem de agregados exclusivo de mensagens de email com conteúdo mal-intencionado bloqueado pelo mecanismo antimalware, [Limpeza automática de zero horas](zero-hour-auto-purge.md)e recursos ATP (incluindo [Links seguros](atp-safe-links.md), [Anexos seguros](atp-safe-attachments.md)e [antiphishing ATP](atp-anti-phishing.md)).<br>Consulte [o relatório de Status de proteção de ameaça (ATP)](view-reports-for-atp.md#threat-protection-status-report). | 

Para exibir ou acessar o widget do Status de proteção de ameaça, você deve ter permissões para exibir relatórios de proteção avançada de ameaça. Para saber mais, consulte [quais permissões são necessárias para exibir os relatórios de ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="global-weekly-threat-detections"></a>Detecções de ameaça semanal global
 
O widget Global detecções de ameaça semanal mostra quantos ameaças detectadas nos emails nos últimos sete (7) dias.

![Widget de semanal detecções de ameaça global](media/globalweeklythreatdetections.png)

As métricas são calculadas conforme descrito na tabela a seguir:

|Indicador  |Como ele é calculado  |
|---------|---------|
|Mensagens verificadas |Número de mensagens de email verificadas multiplicado pelo número de destinatários |
|Ameaças interrompidas  |Número de mensagens de email identificado como contendo multiplicado pelo número de destinatários de malware |
|Bloqueado pelo [ATP](office-365-atp.md) |Número de mensagens de email bloqueadas pelo ATP multiplicado pelo número de destinatários |
|Removido após a entrega |Número de mensagens removido por [zero horas automático limpar](zero-hour-auto-purge.md) multiplicado pelo número de destinatários |

## <a name="malware"></a>Malware

Widgets malware mostram detalhes sobre as tendências de malware e tipos de família de malware nos últimos sete (7) dias.

![Tendências de malware e tipos de família](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>Percepções

Ideias não apenas desvendar principais questões que você deve examinar, eles também incluem recomendações e ações a serem considerados. 

![Ideias inteligentes](media/smartinsights.png)

Por exemplo, você pode ver que as mensagens de email de phishing estão sendo entregues, pois alguns usuários desabilitou suas opções de lixo eletrônico. Para saber mais sobre como insights funcionam, consulte [relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md).
  
## <a name="threat-intelligence"></a>Inteligência de ameaça

Se a assinatura da sua organização inclui [recursos de inteligência de ameaça](office-365-ti.md), seu painel de segurança tem uma seção de **Inteligência de ameaça** que inclui ferramentas avançadas. Equipe de segurança da sua organização pode usar as informações nesta seção para entender campanhas emergentes, investigue as ameaças e gerenciar incidentes. 
  
![Inteligência de ameaça ajuda você a entender destinadas a sua organização de ataques](media/threatintelwidget.png)
  
  
## <a name="trends"></a>Tendências

Na parte inferior do painel de controle de segurança é uma seção de **tendências** , que resume as tendências de fluxo de email para sua organização. Relatórios fornecem informações sobre o e-mail categorizado como spam, malware, tentativas de phishing e bom email. Clique em um lado para exibir informações mais detalhadas no relatório. 
  
![A seção de tendências resume as tendências de fluxo de email para a organização](media/trends.png)
  
E, se a assinatura do Office 365 da sua organização inclui [recursos de inteligência de ameaça](office-365-ti.md), você também terá um relatório de **alertas de gerenciamento de ameaça recentes** nesta seção que permite que sua equipe de segurança exibir e agir em alertas de segurança de alta prioridade. 

Para exibir ou acessar o widget enviados e recebidos de Email, você deve ter permissões para exibir relatórios de proteção avançada de ameaça. Para saber mais, consulte [quais permissões são necessárias para exibir os relatórios de ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

Para exibir ou acessar o widget alertas de gerenciamento de ameaça recentes, você deve ter permissões para exibir alertas. Para saber mais, consulte [permissões de RBAC necessárias para exibir alertas](alert-policies.md#rbac-permissions-required-to-view-alerts).
  
## <a name="related-topics"></a>Tópicos relacionados

[Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade](view-email-security-reports.md)
  
[Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)
  
[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  

