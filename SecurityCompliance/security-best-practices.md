---
title: Práticas recomendadas de segurança para Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Minimize o potencial de uma violação de dados ou uma conta comprometida seguindo estas práticas recomendadas.
ms.openlocfilehash: ff91721569aae5a4982e3f1dd054575d00c278d8
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276121"
---
# <a name="security-best-practices-for-office-365"></a>Práticas recomendadas de segurança para Office 365

Minimize o potencial de uma violação de dados ou uma conta comprometida seguindo estas práticas recomendadas.
  
Este artigo contém uma lista rápida de práticas recomendadas. Para obter uma análise mais detalhada e informações sobre como configurar a segurança, confira [o mapa de segurança do Office 365: principais prioridades para os primeiros 30 dias, 90 dias e além](security-roadmap.md)de. Neste artigo, você encontrará informações com base em investigações de ataques do mundo real, onde nossos especialistas do Microsoft Office 365 cybersecurity fornecem treinamento sobre como avaliar o risco e implementar a segurança, a conformidade e as informações mais importantes controles de proteção para proteger seu locatário do Office 365. Você aprenderá como priorizar ameaças, traduzir as ameaças para a estratégia técnica e, em seguida, adotar uma abordagem sistemática para implementar recursos e controles.
  
## <a name="use-office-365-secure-score"></a>Usar a pontuação segura do Office 365

A pontuação segura é uma ferramenta de análise de segurança que recomenda o que você pode fazer para reduzir ainda mais o risco. A pontuação segura examina suas configurações e atividades do Office 365 e as compara a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como o alinhamento está com as práticas recomendadas de segurança. Para obter mais informações sobre como obter uma pontuação segura e usá-la para aumentar a segurança da sua organização do Office 365, consulte [Introducing The office 365 Secure Score](office-365-secure-score.md).
  
Deseja experimentar a pontuação segura?
  
Usando uma conta corporativa ou de estudante que tenha sido atribuída a função de funções de administrador do Office 365 [sobre o office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [entre no Office 365](https://www.office.com/signin).
  
Pontuação segura de acesso [https://SecureScore.office.com](https://SecureScore.office.com)em.
  
## <a name="use-multi-factor-authentication-mfa"></a>Usar a protocolo de autenticação multifator (MFA)

A MFA adiciona uma camada adicional de proteção a uma estratégia de senha forte, exigindo que os usuários reconheçam uma chamada telefônica, uma mensagem de texto ou uma notificação de aplicativo em seu telefone inteligente após a inserção correta da senha. Com a MFA pronta, as contas de usuário do Office 365 ainda estão protegidas contra o acesso não autorizado, mesmo se a senha de um usuário for comprometida. As contas são protegidas porque o acesso não é concedido a uma conta até que o desafio adicional tenha sido satisfeito. Uma senha comprometida ou roubada não é suficiente.
  
- [Plano para a autenticação multifator para Implantações do Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurar a autenticação multifator para usuários do Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a>Usar o Office 365 Cloud app Security

Configurar políticas com base em suas necessidades de negócios para acompanhar a atividade anômala e agir sobre ela. Configurar alertas com o Office 365 Cloud app Security para que os administradores possam examinar atividades de usuário incomuns ou arriscadas, como baixar grandes quantidades de dados, várias tentativas de entrada com falha ou entradas de um endereço IP desconhecido ou perigoso. Para organizações com um plano Office 365 Enterprise e5, você pode começar a usar o Office 365 Cloud app Security imediatamente. Se você tiver um plano corporativo diferente, poderá adquirir o Office 365 Cloud app Security como um complemento.
  
- [Visão geral do O365 Cloud app Security](office-365-cas-overview.md)
    
- [Ativar o Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>Fluxo de email seguro

Implemente o conjunto de recursos avançados na proteção do Exchange Online e ganhe mais garantias sobre a identidade do remetente de cada mensagem de email e proteja contra malware, vírus e URLs mal-intencionados desconhecidos transmitidos por emails.
  
- Configure as políticas de proteção antispam de [email do Office 365](anti-spam-protection.md) para sua organização. 
    
- Saiba mais e use [proteção avançada contra ameaças para anexos seguros e links seguros](https://technet.microsoft.com/library/mt148491.aspx).
    
- [Adicione proteção Antimalware à sua organização](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).
    
- Saiba mais sobre e habilite [dicas de segurança em mensagens de email no Office 365](safety-tips-in-office-365.md) para seus usuários. 
    
- Se você estiver usando um domínio personalizado para sua organização no Office 365, configure o SPF, DKIM e, em seguida, DMARC para validar emails enviados pela sua organização e para ajudar a evitar falsificação:
    
  - [Configurar o SPF no Office 365 para ajudar a evitar a falsificação](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Use DKIM para validar emails de saída enviados do seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Use o DMARC para validar emails no Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
## <a name="enable-mailbox-audit-logging"></a>Habilitar log de auditoria de caixas de correio

Alguns logs de auditoria são automaticamente habilitados para você no Office 365; no entanto, o log de auditoria de caixa de correio não está ativado por padrão. Você ativa o log de auditoria para todas as caixas de correio de usuário no Office 365 usando o PowerShell do Exchange Online. Para saber mais, confira [habilitar a auditoria de caixa de correio no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Depois de habilitar o log de auditoria, você pode [Pesquisar o log de auditoria no centro &amp; de conformidade de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md) para descobrir quem fez logon em suas caixas de correio de usuário, mensagens enviadas e outras atividades realizadas pelo proprietário da caixa de correio, um usuário delegado ou um administrador. Para obter uma lista de atividades de caixa de correio incluídas no log de auditoria do Office 365 por padrão, consulte [Exchange Mailbox Activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Para obter informações sobre outras ações que você pode executar com o log de auditoria, como alterar a quantidade de tempo para salvar entradas no log de auditoria, consulte [Mailbox Audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Configurar a DLP (prevenção contra perda de dados)

O DLP permite identificar dados confidenciais e criar políticas que ajudam a evitar que os usuários compartilhem acidentalmente ou intencionalmente os dados. A DLP funciona no Office 365, incluindo o Exchange Online, o SharePoint Online e o OneDrive para que os usuários possam permanecer em conformidade sem interromper o fluxo de trabalho. Para obter mais informações, consulte [visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Usar Lockbox de cliente

Como um administrador do Office 365, você pode usar o Lockbox do cliente para controlar como um engenheiro de suporte da Microsoft acessa seus dados durante uma sessão de ajuda. Nos casos em que o engenheiro exige acesso aos seus dados para solucionar problemas e corrigir um problema, o cliente de lockbox permite aprovar ou rejeitar a solicitação de acesso. Se você aprová-la, o engenheiro poderá acessar os dados. Cada solicitação tem um tempo de expiração e, depois que o problema é resolvido, a solicitação é fechada e o acesso é revogado. O Lockbox do cliente está incluído no plano do Office 365 Enterprise E5 ou você pode adquirir uma assinatura separada com qualquer outro plano do Office 365 Enterprise. Confira mais informações em [solicitações de lockbox de cliente do Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).
  
## <a name="try-it-yourself"></a>Experimentar sozinho
<a name="SecureScore"> </a>

Consulte estes recursos de segurança que funcionam em uma assinatura de avaliação do Office 365 antes de adotá-los em produção.
  
- [Criar uma assinatura de avaliação do Office 365](https://technet.microsoft.com/library/mt736406.aspx)
    
- [Configurar e testar a MFA de uma conta de usuário](https://technet.microsoft.com/library/mt492459.aspx)
    
- [Configurar e testar o Office 365 Cloud app Security para notificá-lo da atividade de administração global](https://technet.microsoft.com/library/mt757250.aspx)
    
- [Configurar e testar a ATP para email suspeito](https://technet.microsoft.com/library/mt490479.aspx)
    
- Verifique a [Pontuação segura do Office 365](https://securescore.office.com/) para sua assinatura de avaliação para cada uma das etapas acima 
    

