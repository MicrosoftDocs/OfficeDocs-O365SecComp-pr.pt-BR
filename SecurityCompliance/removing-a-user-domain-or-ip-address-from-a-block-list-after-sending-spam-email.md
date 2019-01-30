---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
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
description: Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614395"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam

Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. O usuário será listado no serviço como um remetente de saída inválido e receberá um não-entrega relatório (NDR) declarando:

- Sua mensagem não pôde ser entregue porque você não foram reconhecido como um remetente válido. O motivo mais comum para que isso é que o seu endereço de email é suspeito de envio de spam e ele não tem permissão para enviar mensagens fora da sua organização. Para obter assistência, entre em contato com seu administrador de email.  Servidor remoto retornou '550 5.1.8 acesso negado, remetente saída ruim'

Os administradores de Inquilino também receberá um alerta indicando que o usuário tiver sido protegido enviem todas as mensagens de saída mais.

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a "entrada de antispam no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

O procedimento a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet Get-BlockedSenderAddress para obter a lista de usuários restritos e Remove-BlockedSenderAddress para remover a restrição. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Remova as restrições de uma conta de email do Office 365 bloqueada

Conclusão da tarefa no Centro de conformidade (SCC) do & de segurança do Office 365. Para obter mais detalhes sobre SCC, [vá para o Centro de conformidade do & de segurança do Office 365](go-to-the-securitycompliance-center.md) . Você precisa estar no **Gerenciamento da organização** ou grupo de funções de **Segurança de administrador** para executar essas funções. [Vá para permissões no Centro de conformidade do & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md) para obter mais detalhes sobre os grupos de função SCC.

1. Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365, inscreva-se no Centro de conformidade e segurança do Office 365 e na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **restrito Os usuários**.
    
    > [!TIP]
    > Para ir diretamente para a página **Usuários restritos** (anteriormente conhecida como o Centro de ação) na segurança &amp; Centro de conformidade, use esta URL: gt _[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Esta página conterá a lista de usuários que foram bloqueados de envio de e-mail para fora da sua organização.  Encontre o usuário que você deseja remover restrições em e clique em **Desbloquear**.

3. Clique em **Sim** para confirmar a alteração. 
    
> [!NOTE]
> Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Você precisará contatar o suporte para desbloquear o usuário.</br></br> Pode levar até 1 hora antes que o usuário seja desbloqueado.
  
## <a name="third-party-block-lists"></a>Listas de bloqueio de terceiros

Exchange Online Protection também usa a listas de bloqueio de terceiros para ajudar a tomar decisões na filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para que aparecem em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de softwares de terceiros se eles pertencem a você.

> [!NOTE]
> Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ficar em lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar removem-se usando o [portal de autoatendimento de retirada da lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis). 

## <a name="for-more-information"></a>Para saber mais

[Respondendo a uma conta de email comprometido](responding-to-a-compromised-email-account.md)

[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Permissões no Centro de conformidade de & de segurança do Office 365](permissions-in-the-security-and-compliance-center.md)

  

