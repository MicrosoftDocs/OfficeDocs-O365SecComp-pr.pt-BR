---
title: Práticas recomendadas de segurança para Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Minimize o potencial de uma violação de dados ou uma conta comprometida seguindo estas práticas recomendadas.
ms.openlocfilehash: 0d3dc30a9975f2ed8fe6d524b4fc67918b34e51d
ms.sourcegitcommit: 49b565f6a57febe53f331b2605d6a06d11e2d0be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/18/2018
ms.locfileid: "25637995"
---
# <a name="security-best-practices-for-office-365"></a>Práticas recomendadas de segurança para Office 365

Minimize o potencial de uma violação de dados ou uma conta comprometida seguindo estas práticas recomendadas.
  
Este artigo contém uma lista rápida de práticas recomendadas. Para mais informações sobre como configurar a segurança e uma análise detalhada, consulte [mapa de segurança do Office 365: principais prioridades para os primeiros 30 dias, 90 dias e além](security-roadmap.md). Nesse artigo, você encontrará informações com base em investigações de ataques reais, onde nossos especialistas de cybersecurity superior do Microsoft Office 365 fornecem treinamento sobre como avaliar os riscos e implementar a segurança, conformidade e informações mais importantes controles de proteção para proteger seu locatário do Office 365. Você aprenderá como priorizar ameaças, traduzir ameaças em estratégia técnica e, em seguida, adotar uma abordagem sistemática para implementar os recursos e controles.
  
## <a name="use-office-365-secure-score"></a>Usar pontuação seguro do Office 365

Pontuação segura é uma ferramenta de análise de segurança que recomenda que você pode fazer para reduzir o risco. Pontuação segura analisa suas configurações do Office 365 e atividades e compará-los a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como alinhado estiver com as práticas recomendadas de segurança. Para obter mais informações sobre como obter a pontuação seguro e usá-lo para aumentar a segurança da sua organização do Office 365, consulte [apresentando a pontuação de seguro do Office 365](office-365-secure-score.md).
  
Você deseja testar pontuação seguro?
  
Usando uma conta de trabalho ou da escola que tenha sido atribuída a função do Office 365 [funções de administrador do Office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [entrar no Office 365](https://www.office.com/signin).
  
Acesso seguro a pontuação no [https://SecureScore.office.com](https://SecureScore.office.com).
  
## <a name="use-multi-factor-authentication-mfa"></a>Use a autenticação multifator (MFA)

MFA adiciona uma camada adicional de proteção para a estratégia de senha forte por exigir que os usuários de agradecer uma chamada telefônica, uma notificação de aplicativo em seu telefone inteligente após inserir corretamente suas senhas ou mensagem de texto. Com MFA in-loco, contas de usuário do Office 365 ainda estão protegidas contra acesso não autorizado, mesmo se uma senha de usuário for comprometida. Contas são protegidas porque o access não é concedido a uma conta até após o desafio adicional foram atendido. Uma senha comprometida ou furtada não é suficiente.
  
- [Plano para a autenticação multifator para Implantações do Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurar a autenticação multifator para usuários do Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a>Use a segurança de aplicativo de nuvem do Office 365

Configure políticas com base em suas necessidades comerciais para acompanhar a atividade anormal e agir contidas nela. Configurar alertas com segurança de aplicativo de nuvem do Office 365, de modo que os administradores podem examinar a atividade do usuário incomum ou riscado, como baixar grandes quantidades de dados, vários Falha ao entrar tentativas ou entradas de um endereço IP desconhecido ou perigoso. Para organizações com um plano do Office 365 Enterprise E5, você pode iniciar usando a segurança de aplicativo de nuvem do Office 365 imediatamente. Se você tiver um plano de diferentes enterprise, você pode adquirir a segurança de aplicativo de nuvem do Office 365 como um complemento.
  
- [Visão geral da segurança de aplicativo de nuvem do O365](office-365-cas-overview.md)
    
- [Ativar o Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>Fluxo de email seguro

Implementar o rich conjunto no Exchange Online Protection de recursos e obter maior garantia sobre a identidade do remetente de cada mensagem de email e protege contra malware desconhecido, vírus e URLs mal-intencionadas transmitidos por meio de emails.
  
- Configure políticas de [Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md) para sua organização. 
    
- Saiba mais sobre e use [proteção contra ameaças avançadas para anexos seguros e links de seguros](https://technet.microsoft.com/library/mt148491.aspx).
    
- [Proteção antimalware de adicionar à sua organização](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).
    
- Saiba mais sobre e habilitar [Safety dicas em mensagens de email no Office 365](safety-tips-in-office-365.md) para seus usuários. 
    
- Se você estiver usando um domínio personalizado para sua organização no Office 365, configure SPF, DKIM e DMARC para validar emails enviados por sua organização e para ajudar a impedir a falsificação:
    
  - [Configurar SPF no Office 365 para ajudar a impedir a falsificação](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Verificação de uso para validar emails de saída enviados a partir de seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Use DMARC para validar emails no Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
## <a name="enable-mailbox-audit-logging"></a>Habilitar log de auditoria de caixas de correio

Alguns logs de auditoria é ativado automaticamente para você no Office 365; No entanto, log de auditoria de caixa de correio não está ativado por padrão. Você pode ativar o log de auditoria para todas as caixas de correio do usuário no Office 365 usando o PowerShell do Exchange Online. Para obter informações, consulte [Habilitar caixa de correio auditorias no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Depois que você habilitou a auditoria de log que você pode [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md) para descobrir quem entrou no suas caixas de correio do usuário, mensagens enviadas e outras atividades realizadas pelo proprietário da caixa de correio, um usuário delegado, ou um administrador. Para obter uma lista de atividades de caixa de correio que estão incluídos no Office 365 log de auditoria por padrão, consulte [atividades de caixa de correio do Exchange](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Para obter informações sobre outras ações que você pode executar com o log de auditoria, como alterar o período de tempo para salvar as entradas no log de auditoria, consulte o [log no Exchange 2016 de auditoria de caixa de correio](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Configurar a prevenção de perda de dados (DLP)

DLP permite identificar dados confidenciais e criar políticas que ajuda a impedir que os usuários acidentalmente ou intencionalmente compartilhamento de dados. DLP funciona entre o Office 365, incluindo o Exchange Online, SharePoint Online e OneDrive para que os usuários podem permanecer em conformidade sem interromper o fluxo de trabalho. Para obter mais informações, consulte [Visão geral das políticas de prevenção de perda de dados](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Use o cliente Lockbox

Como um administrador do Office 365, você pode usar o cliente Lockbox para controlar como um engenheiro de suporte da Microsoft acessa os dados durante uma sessão de Ajuda. Em casos onde o engenheiro exige acesso aos seus dados para solucionar problemas e corrigir um problema, Lockbox do cliente permite que você aprovar ou rejeitar a solicitação de acesso. Se você aprová-la, o engenheiro pode acessar os dados. Cada solicitação possui um tempo de expiração e depois que o problema for resolvido, a solicitação é fechada e o acesso será revogado. Cliente Lockbox está incluído no plano do Office 365 Enterprise E5 ou você pode adquirir uma assinatura separada com outro plano de enterprise do Office 365. Para obter informações, consulte [Solicitações de Lockbox do cliente do Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).
  
## <a name="try-it-yourself"></a>Experimente você mesmo
<a name="SecureScore"> </a>

Consulte esses recursos de segurança trabalhando em uma assinatura de avaliação do Office 365 antes da adoção-los em produção.
  
- [Criar uma assinatura de avaliação do Office 365](https://technet.microsoft.com/library/mt736406.aspx)
    
- [Configurar e testar MFA para uma conta de usuário](https://technet.microsoft.com/library/mt492459.aspx)
    
- [Configurar e testar a segurança de aplicativo de nuvem do Office 365 para notificá-lo da atividade de administrador global](https://technet.microsoft.com/library/mt757250.aspx)
    
- [Configurar e testar ATP de email suspeita](https://technet.microsoft.com/library/mt490479.aspx)
    
- A [Pontuação de seguro do Office 365](https://securescore.office.com/) para sua assinatura de avaliação para cada uma das etapas acima da seleção 
    

