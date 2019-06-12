---
title: Remoção de um usuário do portal de Usuários Restritos após o envio de email de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: 3e05b250d5a3cdca79c7cf494b84be02ce3ecdc9
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857621"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Remoção de um usuário do portal de Usuários Restritos após o envio de email de spam

Se um usuário enviar continuamente emails classificados como spam do Office 365, eles serão impedidos de enviar emails, mas ainda poderão recebê-lo. O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:

> "Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido. O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não tem mais permissão para enviar emails.  Entre em contato com seu administrador de email para obter assistência. O servidor remoto retornou ' 550 5.1.8 acesso negado, emissor de saída incorreto. "

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

O procedimento a seguir também pode ser realizado pelo PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Remover restrições para uma conta de email bloqueada do Office 365

Você conclui essa tarefa no centro de conformidade & segurança (SCC). [Vá para o centro de conformidade & segurança](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC. Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções. [Vá até permissões no centro de conformidade & segurança](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.

1. Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.
    
    > [!TIP]
    > Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Esta página conterá a lista de usuários que foram impedidos de enviar emails.  Localize o usuário para o qual você deseja remover as restrições e selecione **desbloquear**.

3. Um surgimento entrará nos detalhes sobre a conta cujo envio é restrito. Você deve percorrer as recomendações para garantir que você esteja tomando as ações adequadas caso a conta seja realmente comprometida. Clique em **Avançar** quando terminar.

4. A próxima tela tem recomendações para ajudar a evitar o comprometimento futuro. Habilitar a MFA (autenticação multifator) e alterar as senhas é uma boa defesa. Clique em **desbloquear usuário** quando concluído.

5. Clique em **Sim** para confirmar a alteração.

    > [!NOTE]
    > Pode levar 30 minutos ou mais antes de as restrições serem removidas. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>Garantir que os administradores sejam alertados quando isso acontecer

Um alerta "usuário restrito a enviar emails" está disponível como uma política na página políticas de alerta de conformidade do Office 365 Security &. Isso era anteriormente a política de spam de saída, mas agora é nativa para a plataforma de alerta do Office 365. Vá para [políticas de alerta no centro de conformidade & segurança](alert-policies.md) para obter mais informações sobre alertas.

> [!IMPORTANT]
> Para que os alertas funcionem, a pesquisa de log de auditoria deve ser ativada. Confira como [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) para obter mais informações.

A política para este alerta é um padrão e vem com cada locatário do Office 365 e não precisa ser configurada. É considerado um alerta de alta gravidade e enviará um email para o grupo TenantAdmins configurado quando o alerta for acionado sempre que um usuário tiver sido restringido do envio de email. Os administradores podem atualizar o grupo notificado quando esse alerta acontecer indo para o alerta sob o portal SCC > alertas > políticas de alerta > usuários restritos a enviar emails.

Você poderá editar o alerta para:
- Ativar/desativar notificações por email
- Enviar por email os destinatários necessários
- Limitar as notificações obtidas por dia

## <a name="for-more-information"></a>Para saber mais

[Respondendo a uma conta de email comprometida](responding-to-a-compromised-email-account.md)

[Noções básicas sobre o usuário impedido de enviar alerta de email](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[Pool de entrega de alto risco para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Permissões no centro de conformidade & segurança](permissions-in-the-security-and-compliance-center.md)

[Políticas de alerta no centro de conformidade & segurança](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)
