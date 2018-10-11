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
ms.openlocfilehash: 63bda11afdd1e02e9e12e8c505aca7100c4deade
ms.sourcegitcommit: a36d2692396786f49c8765c65145e5093578e9a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25498087"
---
# <a name="security-best-practices-for-office-365"></a><span data-ttu-id="3f59f-103">Práticas recomendadas de segurança para Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-103">Security best practices for Office 365</span></span>

<span data-ttu-id="3f59f-104">Minimize o potencial de uma violação de dados ou uma conta comprometida seguindo estas práticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="3f59f-104">Minimize the potential of a data breach or a compromised account by following these recommended best practices.</span></span>
  
<span data-ttu-id="3f59f-p101">Este artigo contém uma lista rápida de práticas recomendadas. Para mais informações sobre como configurar a segurança e uma análise detalhada, consulte [mapa de segurança do Office 365: principais prioridades para os primeiros 30 dias, 90 dias e além](security-roadmap.md). Nesse artigo, você encontrará informações com base em investigações de ataques reais, onde nossos especialistas de cybersecurity superior do Microsoft Office 365 fornecem treinamento sobre como avaliar os riscos e implementar a segurança, conformidade e informações mais importantes controles de proteção para proteger seu locatário do Office 365. Você aprenderá como priorizar ameaças, traduzir ameaças em estratégia técnica e, em seguida, adotar uma abordagem sistemática para implementar os recursos e controles.</span><span class="sxs-lookup"><span data-stu-id="3f59f-p101">This article contains a quick list of best practices. For more in-depth analysis and information on setting up security, see [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md). In that article, you'll find information based on investigations of real-world attacks, where our top Microsoft Office 365 cybersecurity experts provide coaching on how to assess risk and implement the most critical security, compliance, and information protection controls to protect your Office 365 tenant. You'll learn how to prioritize threats, translate threats into technical strategy, and then take a systematic approach to implementing features and controls.</span></span>
  
## <a name="use-office-365-secure-score"></a><span data-ttu-id="3f59f-109">Usar pontuação seguro do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-109">Use Office 365 Secure Score</span></span>

<span data-ttu-id="3f59f-p102">Pontuação segura é uma ferramenta de análise de segurança que recomenda que você pode fazer para reduzir o risco. Pontuação segura analisa suas configurações do Office 365 e atividades e compará-los a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como alinhado estiver com as práticas recomendadas de segurança. Para obter mais informações sobre como obter a pontuação seguro e usá-lo para aumentar a segurança da sua organização do Office 365, consulte [apresentando a pontuação de seguro do Office 365](office-365-secure-score.md).</span><span class="sxs-lookup"><span data-stu-id="3f59f-p102">Secure Score is a security analytics tool that recommends what you can do to further reduce risk. Secure Score looks at your Office 365 settings and activities and compares them to a baseline established by Microsoft. You'll get a score based on how aligned you are with best security practices. For more information about how to get Secure Score and use it to increase the security of your Office 365 organization, see [Introducing the Office 365 Secure Score](office-365-secure-score.md).</span></span>
  
<span data-ttu-id="3f59f-114">Você deseja testar pontuação seguro?</span><span class="sxs-lookup"><span data-stu-id="3f59f-114">Want to try out Secure Score?</span></span>
  
<span data-ttu-id="3f59f-115">Usando uma conta de trabalho ou da escola que tenha sido atribuída a função do Office 365 [funções de administrador do Office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [entrar no Office 365](https://www.office.com/signin).</span><span class="sxs-lookup"><span data-stu-id="3f59f-115">Using a work or school account that has been assigned the Office 365 [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) role, [sign in to Office 365](https://www.office.com/signin).</span></span>
  
<span data-ttu-id="3f59f-116">Acesso seguro a pontuação no [https://SecureScore.office.com](https://SecureScore.office.com).</span><span class="sxs-lookup"><span data-stu-id="3f59f-116">Access Secure Score at [https://SecureScore.office.com](https://SecureScore.office.com).</span></span>
  
## <a name="use-multi-factor-authentication-mfa"></a><span data-ttu-id="3f59f-117">Use a autenticação multifator (MFA)</span><span class="sxs-lookup"><span data-stu-id="3f59f-117">Use multi-factor authentication (MFA)</span></span>

<span data-ttu-id="3f59f-p103">MFA adiciona uma camada adicional de proteção para a estratégia de senha forte por exigir que os usuários de agradecer uma chamada telefônica, uma notificação de aplicativo em seu telefone inteligente após inserir corretamente suas senhas ou mensagem de texto. Com MFA in-loco, contas de usuário do Office 365 ainda estão protegidas contra acesso não autorizado, mesmo se uma senha de usuário for comprometida. Contas são protegidas porque o access não é concedido a uma conta até após o desafio adicional foram atendido. Uma senha comprometida ou furtada não é suficiente.</span><span class="sxs-lookup"><span data-stu-id="3f59f-p103">MFA adds an additional layer of protection to a strong password strategy by requiring users to acknowledge a phone call, text message, or an app notification on their smart phone after correctly entering their password. With MFA in place, Office 365 user accounts are still protected against unauthorized access even if a user's password is compromised. Accounts are protected because access is not granted to an account until after the additional challenge has been satisfied. A compromised or stolen password is not enough.</span></span>
  
- [<span data-ttu-id="3f59f-122">Planejar a autenticação multifator para implantações do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-122">Plan for multi-factor authentication for Office 365 Deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="3f59f-123">Configurar a autenticação multifator para usuários do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-123">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a><span data-ttu-id="3f59f-124">Use a segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-124">Use Office 365 Cloud App Security</span></span>

<span data-ttu-id="3f59f-p104">Configure políticas com base em suas necessidades comerciais para acompanhar a atividade anormal e agir contidas nela. Configurar alertas com segurança de aplicativo de nuvem do Office 365, de modo que os administradores podem examinar a atividade do usuário incomum ou riscado, como baixar grandes quantidades de dados, vários Falha ao entrar tentativas ou entradas de um endereço IP desconhecido ou perigoso. Para organizações com um plano do Office 365 Enterprise E5, você pode iniciar usando a segurança de aplicativo de nuvem do Office 365 imediatamente. Se você tiver um plano de diferentes enterprise, você pode adquirir a segurança de aplicativo de nuvem do Office 365 como um complemento.</span><span class="sxs-lookup"><span data-stu-id="3f59f-p104">Set up policies based on your business needs to track anomalous activity and act on it. Set up alerts with Office 365 Cloud App Security so that admins can review unusual or risky user activity, such as downloading large amounts of data, multiple failed sign-in attempts, or sign-ins from an unknown or dangerous IP address. For organizations with an Office 365 Enterprise E5 plan, you can start using Office 365 Cloud App Security right away. If you have a different enterprise plan, you can purchase Office 365 Cloud App Security as an add-on.</span></span>
  
- [<span data-ttu-id="3f59f-129">Visão geral da segurança de aplicativo de nuvem do O365</span><span class="sxs-lookup"><span data-stu-id="3f59f-129">Overview of O365 Cloud App Security</span></span>](office-365-cas-overview.md)
    
- [<span data-ttu-id="3f59f-130">Ativar o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3f59f-130">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a><span data-ttu-id="3f59f-131">Fluxo de email seguro</span><span class="sxs-lookup"><span data-stu-id="3f59f-131">Secure mail flow</span></span>

<span data-ttu-id="3f59f-132">Implementar o rich conjunto no Exchange Online Protection de recursos e obter maior garantia sobre a identidade do remetente de cada mensagem de email e protege contra malware desconhecido, vírus e URLs mal-intencionadas transmitidos por meio de emails.</span><span class="sxs-lookup"><span data-stu-id="3f59f-132">Implement the rich feature set in Exchange Online Protection and gain greater assurance about the identity of the sender of each email message, and protect against unknown malware, viruses, and malicious URLs transmitted through emails.</span></span>
  
- <span data-ttu-id="3f59f-133">Configure políticas de [Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md) para sua organização.</span><span class="sxs-lookup"><span data-stu-id="3f59f-133">Configure [Office 365 Email Anti-Spam Protection](anti-spam-protection.md) policies for your organization.</span></span> 
    
- <span data-ttu-id="3f59f-134">Saiba mais sobre e use [proteção contra ameaças avançadas para anexos seguros e links de seguros](https://technet.microsoft.com/library/mt148491.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f59f-134">Learn about and then use [Advanced threat protection for safe attachments and safe links](https://technet.microsoft.com/library/mt148491.aspx).</span></span>
    
- <span data-ttu-id="3f59f-135">[Proteção antimalware de adicionar à sua organização](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f59f-135">[Add anti-malware protection to your organization](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span></span>
    
- <span data-ttu-id="3f59f-136">Saiba mais sobre e habilitar [Safety dicas em mensagens de email no Office 365](safety-tips-in-office-365.md) para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="3f59f-136">Learn about and enable [Safety tips in email messages in Office 365](safety-tips-in-office-365.md) for your users.</span></span> 
    
- <span data-ttu-id="3f59f-137">Se você estiver usando um domínio personalizado para sua organização no Office 365, configure SPF, DKIM e DMARC para validar emails enviados por sua organização e para ajudar a impedir a falsificação:</span><span class="sxs-lookup"><span data-stu-id="3f59f-137">If you're using a custom domain for your organization in Office 365, set up SPF, DKIM, and then DMARC to validate mail sent by your organization and to help prevent spoofing:</span></span>
    
  - <span data-ttu-id="3f59f-138">[Configurar SPF no Office 365 para ajudar a impedir a falsificação](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span><span class="sxs-lookup"><span data-stu-id="3f59f-138">[Set up SPF in Office 365 to help prevent spoofing](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="3f59f-139">[Verificação de uso para validar emails de saída enviados a partir de seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span><span class="sxs-lookup"><span data-stu-id="3f59f-139">[Use DKIM to validate outbound email sent from your custom domain in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="3f59f-140">[Use DMARC para validar emails no Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f59f-140">[Use DMARC to validate email in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>
    
## <a name="enable-mailbox-audit-logging"></a><span data-ttu-id="3f59f-141">Habilitar log de auditoria de caixas de correio</span><span class="sxs-lookup"><span data-stu-id="3f59f-141">Enable mailbox audit logging</span></span>

<span data-ttu-id="3f59f-p105">Alguns logs de auditoria é ativado automaticamente para você no Office 365; No entanto, log de auditoria de caixa de correio não está ativado por padrão. Você pode ativar o log de auditoria para todas as caixas de correio do usuário no Office 365 usando o PowerShell do Exchange Online. Para obter informações, consulte [Habilitar caixa de correio auditorias no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span><span class="sxs-lookup"><span data-stu-id="3f59f-p105">Some audit logging is automatically enabled for you in Office 365; however, mailbox audit logging is not turned on by default. You turn on audit logging for all user mailboxes in Office 365 by using Exchange Online PowerShell. For information, see [Enable mailbox auditing in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span></span>
  
<span data-ttu-id="3f59f-p106">Depois que você habilitou a auditoria de log que você pode [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md) para descobrir quem entrou no suas caixas de correio do usuário, mensagens enviadas e outras atividades realizadas pelo proprietário da caixa de correio, um usuário delegado, ou um administrador. Para obter uma lista de atividades de caixa de correio que estão incluídos no Office 365 log de auditoria por padrão, consulte [atividades de caixa de correio do Exchange](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span><span class="sxs-lookup"><span data-stu-id="3f59f-p106">After you've enabled audit logging you can [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) to find out who has logged into your user mailboxes, sent messages, and other activities performed by the mailbox owner, a delegated user, or an administrator. For a list of mailbox activities that are included in the Office 365 audit log by default, see [Exchange mailbox activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span></span>
  
<span data-ttu-id="3f59f-147">Para obter informações sobre outras ações que você pode executar com o log de auditoria, como alterar o período de tempo para salvar as entradas no log de auditoria, consulte o [log no Exchange 2016 de auditoria de caixa de correio](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f59f-147">For information about other actions you can perform with the audit log, such as changing the amount of time to save entries in the audit log, see [Mailbox audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span></span>
  
## <a name="configure-data-loss-prevention-dlp"></a><span data-ttu-id="3f59f-148">Configurar a prevenção de perda de dados (DLP)</span><span class="sxs-lookup"><span data-stu-id="3f59f-148">Configure Data Loss Prevention (DLP)</span></span>

<span data-ttu-id="3f59f-p107">DLP permite identificar dados confidenciais e criar políticas que ajuda a impedir que os usuários acidentalmente ou intencionalmente compartilhamento de dados. DLP funciona entre o Office 365, incluindo o Exchange Online, SharePoint Online e OneDrive para que os usuários podem permanecer em conformidade sem interromper o fluxo de trabalho. Para obter mais informações, consulte [Visão geral das políticas de prevenção de perda de dados](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3f59f-p107">DLP allows you to identify sensitive data and create policies that help prevent your users from accidentally or intentionally sharing the data. DLP works across Office 365 including Exchange Online, SharePoint Online, and OneDrive so that your users can stay compliant without interrupting their workflow. For more information, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
## <a name="use-customer-lockbox"></a><span data-ttu-id="3f59f-152">Use o cliente Lockbox</span><span class="sxs-lookup"><span data-stu-id="3f59f-152">Use Customer Lockbox</span></span>

<span data-ttu-id="3f59f-p108">Como um administrador do Office 365, você pode usar o cliente Lockbox para controlar como um engenheiro de suporte da Microsoft acessa os dados durante uma sessão de Ajuda. Em casos onde o engenheiro exige acesso aos seus dados para solucionar problemas e corrigir um problema, Lockbox do cliente permite que você aprovar ou rejeitar a solicitação de acesso. Se você aprová-la, o engenheiro pode acessar os dados. Cada solicitação possui um tempo de expiração e depois que o problema for resolvido, a solicitação é fechada e o acesso será revogado. Cliente Lockbox está incluído no plano do Office 365 Enterprise 5 ou você pode adquirir uma assinatura separada com outro plano de enterprise do Office 365. Para obter informações, consulte [Solicitações de Lockbox do cliente do Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span><span class="sxs-lookup"><span data-stu-id="3f59f-p108">As an Office 365 admin, you can use Customer Lockbox to control how a Microsoft support engineer accesses your data during a help session. In cases where the engineer requires access to your data to troubleshoot and fix an issue, Customer Lockbox allows you to approve or reject the access request. If you approve it, the engineer can access the data. Each request has an expiration time, and once the issue is resolved, the request is closed and access is revoked. Customer Lockbox is included in the Office 365 Enterprise 5 plan, or you can purchase a separate subscription with any other Office 365 enterprise plan. For information, see [Office 365 Customer Lockbox Requests](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span></span>
  
## <a name="try-it-yourself"></a><span data-ttu-id="3f59f-159">Experimente você mesmo</span><span class="sxs-lookup"><span data-stu-id="3f59f-159">Try it yourself</span></span>
<span data-ttu-id="3f59f-160"><a name="SecureScore"> </a></span><span class="sxs-lookup"><span data-stu-id="3f59f-160"></span></span>

<span data-ttu-id="3f59f-161">Consulte esses recursos de segurança trabalhando em uma assinatura de avaliação do Office 365 antes da adoção-los em produção.</span><span class="sxs-lookup"><span data-stu-id="3f59f-161">See these security features working in an Office 365 trial subscription prior to adopting them in production.</span></span>
  
- [<span data-ttu-id="3f59f-162">Criar uma assinatura de avaliação do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f59f-162">Create an Office 365 trial subscription</span></span>](https://technet.microsoft.com/library/mt736406.aspx)
    
- [<span data-ttu-id="3f59f-163">Configurar e testar MFA para uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="3f59f-163">Configure and test MFA for a user account</span></span>](https://technet.microsoft.com/library/mt492459.aspx)
    
- [<span data-ttu-id="3f59f-164">Configurar e testar a segurança de aplicativo de nuvem do Office 365 para notificá-lo da atividade de administrador global</span><span class="sxs-lookup"><span data-stu-id="3f59f-164">Configure and test Office 365 Cloud App Security to notify you of global admin activity</span></span>](https://technet.microsoft.com/library/mt757250.aspx)
    
- [<span data-ttu-id="3f59f-165">Configurar e testar ATP de email suspeita</span><span class="sxs-lookup"><span data-stu-id="3f59f-165">Configure and test ATP for suspicious email</span></span>](https://technet.microsoft.com/library/mt490479.aspx)
    
- <span data-ttu-id="3f59f-166">A [Pontuação de seguro do Office 365](https://securescore.office.com/) para sua assinatura de avaliação para cada uma das etapas acima da seleção</span><span class="sxs-lookup"><span data-stu-id="3f59f-166">Check the [Office 365 Secure Score](https://securescore.office.com/) for your trial subscription for each of the above steps</span></span> 
    

