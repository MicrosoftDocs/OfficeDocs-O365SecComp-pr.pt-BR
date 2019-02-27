---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Se um usuário envia continuamente mensagens de email do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens.
ms.openlocfilehash: 870e5eabca9e799dfca1e99846a5bfe845f65df4
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275931"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam

Se um usuário envia continuamente mensagens de email do Office 365 classificados como spam, eles serão impedidos de enviar mais mensagens. O usuário será listado no serviço como um remetente de saída incorreto e receberá uma notificação de falha na entrega (NDR) que diz:

- Sua mensagem não pôde ser entregue porque você não foi reconhecido como um remetente válido. O motivo mais comum para isso é que seu endereço de email é suspeito de enviar spam e não é mais permitido enviar mensagens fora da sua organização. Entre em contato com seu administrador de email para obter assistência.  O servidor remoto retornou ' 550 5.1.8 acesso negado, remetente de saída inválido '

Os administradores de locatários também receberão um alerta informando que o usuário foi impedido de enviar mais mensagens de saída.

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

O procedimento a seguir também pode ser executado por meio do PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Remover restrições para uma conta de email bloqueada do Office 365

Você conclui essa tarefa no centro de conformidade do & de segurança do Office 365 (SCC). [Vá para o centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC. Você precisa estar no grupo de função **Gerenciamento da organização** ou administrador de **segurança** para executar essas funções. [Vá até permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre grupos de função SCC.

1. Usando uma conta corporativa ou de estudante que tenha privilégios de administrador global do Office 365, entre no centro de conformidade e segurança do Office 365 e, na lista à esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **restrito Usuários**.
    
    > [!TIP]
    > Para ir diretamente para a página **usuários restritos** (anteriormente conhecida como central de ações) no centro &amp; de conformidade de segurança, use esta URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Esta página conterá a lista de usuários que foram impedidos de enviar emails para fora da sua organização.  Localize o usuário para o qual deseja remover as restrições e clique em **desbloquear**.

3. Clique em **Sim** para confirmar a alteração. 
    
> [!NOTE]
> Há um limite para o número de vezes que uma conta pode ser desbloqueada pelo administrador de locatários. Se o limite de um usuário foi excedido, uma mensagem de erro será exibida. Em seguida, será necessário entrar em contato com o suporte para desbloquear o usuário.<br/><br/> Pode levar até 1 hora para que o usuário seja desbloqueado.
  
## <a name="third-party-block-lists"></a>Listas de bloqueio de terceiros

O Exchange Online Protection também usa listas de bloqueio de terceiros para ajudar a tomar decisões sobre filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para aparecer em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de terceiros se eles pertencem a você.

> [!NOTE]
> Se alguém fora do Office 365 não puder enviar mensagens para a sua conta do Office 365, sua conta poderá estar na lista de remetentes bloqueados externos. Os usuários fora do Office 365 podem tentar remover a si próprios usando o [portal de Can-lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)de autoatendimento. 

## <a name="for-more-information"></a>Para saber mais

[Respondendo a uma conta de email comprometida](responding-to-a-compromised-email-account.md)

[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Pool de entrega de alto risco para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Permissões no centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md)

  

