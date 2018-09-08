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
ms.openlocfilehash: ff5bb010f45b0c89e08239f0e37885bd7ae5c7cd
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875783"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam

Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. 
  
Quando um remetente for bloqueado enviem mensagens de emails, eles recebem um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.
  
Não só poderão ser bloqueados usuários individuais aos domínios de serviço, mas a sites específicos, e endereços IP também podem ser bloqueados. Em alguns casos, sites ou domínios podem ser adicionados a uma lista de bloqueios só porque eles aparecem em uma mensagem de spam. Como o administrador do Office 365, você pode tentar obter usuários, sites, domínios e endereços IP removidos das listas de bloqueio de terceiros. Use os links na tabela na parte inferior deste tópico entrar em contato com cada terceiros e siga as instruções. Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ter terminado na lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar remover sozinhos da lista de remetentes bloqueados usando o [portal de autoatendimento de retirada da lista](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).
  
Você pode definir configurações de spam de saída para que você obtenha anotification quando um usuário do Office 365 é impedido de envio de email que é classificada como spam. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.
  
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

|**Nome da Lista **|**Portal para Retirada da Lista**|**Para saber mais**|
|:-----|:-----|:-----|
|URIBL  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[Site URIBL](https://uribl.com/) <br/> |
|SURBL  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[Apresentando os dados de reputação de URI de SURBLHTTP://](http://www.surbl.org/) <br/> |
|Spamhaus   <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[Entendendo a filtragem DNSBLHTTP://](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|invaluement  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[lista de anti-spam de lista](http://dnsbl.invaluement.com/) <br/> |
|Phishtank  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[PhishTank perguntas Frequentes](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> Exchange Online Protection também usa a listas de bloqueio de terceiros para filtragem de spam. 
   
## <a name="for-more-information"></a>Para saber mais

[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

