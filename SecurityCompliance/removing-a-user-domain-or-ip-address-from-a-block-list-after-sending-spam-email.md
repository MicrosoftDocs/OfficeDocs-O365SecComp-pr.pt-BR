---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: 8dcd6c8f55d867e1c2e249ec71a3a5c6b78ac76a
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955433"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam

Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. O usuário será listado no serviço como um remetente de saída inválido e receberá um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.

Você pode configurar as configurações de política de spam de saída para que você receber uma notificação quando um usuário do Office 365 é impedido de envio de email. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>Desbloquear uma conta de email do Office 365

Conclusão da tarefa no Centro de conformidade (SCC) & segurança do Office 365. [Vá para o Centro de conformidade & segurança do Office 365](go-to-the-securitycompliance-center.md) para obter mais detalhes sobre SCC.

1. Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365, inscreva-se no Centro de conformidade e segurança do Office 365 e na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **restrito Os usuários**.
    
    > [!TIP]
    > Para ir diretamente para a página **Usuários restritos** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Esta página conterá a lista de usuários que foram bloqueados de envio de e-mail para fora da sua organização.  Encontre o usuário que você deseja remover restrições em e clique em **Desbloquear**.

3. Clique em **Sim** para confirmar a alteração. 
    
> [!NOTE]
> Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Você precisará contatar o suporte para desbloquear o usuário.
  
## <a name="third-party-block-lists"></a>Listas de bloqueio de terceiros

Exchange Online Protection também usa a listas de bloqueio de terceiros para ajudar a tomar decisões na filtragem de spam. Usuários, sites, domínios e endereços IP podem ser adicionados para bloquear listas apenas para que aparecem em uma mensagem de spam. Como o administrador do Office 365, você deve tentar obter esses objetos removidos dos provedores de lista de softwares de terceiros se eles pertencem a você. Use os links a tabela a seguir para cada terceiros entre em contato e siga suas instruções.

|**Nome da Lista **|**Portal para Retirada da Lista**|**Para saber mais**|
|:-----|:-----|:-----|
|URIBL  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[Site URIBL](https://uribl.com/) <br/> |
|SURBL  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[Apresentando os dados de reputação de URI de SURBLHTTP://](http://www.surbl.org/) <br/> |
|Spamhaus   <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[Entendendo a filtragem DNSBLHTTP://](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|invaluement  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[lista de anti-spam de lista](http://dnsbl.invaluement.com/) <br/> |
|Phishtank  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[PhishTank perguntas Frequentes](https://www.phishtank.com/faq.php) <br/> |

> [!NOTE]
> Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ficar em lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar removem-se usando o [portal de autoatendimento de retirada da lista](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis). 

## <a name="for-more-information"></a>Para saber mais

[Respondendo a uma conta de email comprometido](responding-to-a-compromised-email-account.md)

[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

  

  

