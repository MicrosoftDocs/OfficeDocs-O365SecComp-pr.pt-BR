---
title: Remover um usuário do portal de usuários restritos após o envio de email de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: 61d52ad1f25dc3767ad51da5b3a217ace59303ce
ms.sourcegitcommit: 9918411c01e962d5c67d53dd30a8a9c28c547397
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2019
ms.locfileid: "30654548"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Remover um usuário do portal de usuários restritos após o envio de email de spam

Se um usuário enviar continuamente emails do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens de saída. O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:

- Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido. O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não é mais permitido enviar mensagens fora da sua organização. Entre em contato com seu administrador de email para obter assistência. O servidor remoto retornou ' 550 5.1.8 acesso negado, remetente de saída inválido '

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

O procedimento a seguir também pode ser realizado pelo PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Remover restrições para uma conta de email bloqueada do Office 365

Você conclui essa tarefa no centro de conformidade do & de segurança do Office 365 (SCC). [Vá para o centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC. Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções. [Vá até permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.

1. Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.
    
    > [!TIP]
    > Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Esta página conterá a lista de usuários que foram impedidos de enviar emails para fora da sua organização.  Localize o usuário para o qual deseja remover as restrições e clique em **desbloquear**.

3. Um surgimento entrará nos detalhes sobre a conta cujo envio é restrito. Você deve percorrer as recomendações para garantir que você esteja tomando as ações adequadas caso a conta seja realmente comprometida. Clique em **Avançar** quando terminar.

4. A próxima tela tem recomendações para ajudar a evitar o comprometimento futuro. Habilitar a MFA (autenticação multifator) e alterar as senhas é uma boa defesa. Clique em **desbloquear usuário** quando concluído.

5. Clique em **Sim** para confirmar a alteração.

    > [!NOTE]
    > Pode levar até 30 minutos para que as restrições sejam removidas. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>Garantir que os administradores sejam alertados quando isso acontecer

Os administradores de locatários também receberão um alerta informando que o usuário foi impedido de enviar mais mensagens de saída. É um alerta padrão que é fornecido para todos os locatários e está listado na página políticas de alerta SCC, intitulado "usuário restrito a enviar email". Vá para [políticas de alerta no centro de conformidade do & de segurança do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) para obter mais informações sobre o alerta.

## <a name="for-more-information"></a>Para obter mais informações

[Respondendo a uma conta de email comprometida](responding-to-a-compromised-email-account.md)

[Noções básicas sobre o usuário impedido de enviar alerta de email](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[Pool de entrega de alto risco para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md)
