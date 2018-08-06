---
title: Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais.
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026328"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Remover um usuário, domínio ou endereço IP de uma lista de bloqueio após enviar email de spam

Se um usuário continuamente envia mensagens de email do Office 365 é classificada como spam, eles serão bloqueados enviem mensagens qualquer mais. 
  
Quando um remetente for bloqueado enviem mensagens de emails, eles recebem um relatório de não-entrega (NDR ou Falha ao enviar mensagem de email) que fornece informações específicas sobre as etapas que precisam ser executadas para desbloquear a próprios.
  
Não só poderão ser bloqueados usuários individuais aos domínios de serviço, mas a sites específicos, e endereços IP também podem ser bloqueados. Em alguns casos, sites ou domínios podem ser adicionados a uma lista de bloqueios só porque eles aparecem em uma mensagem de spam. Como o administrador do Office 365, você pode tentar obter usuários, sites, domínios e endereços IP removidos das listas de bloqueio de terceiros. Use os links na tabela na parte inferior deste tópico entrar em contato com cada terceiros e siga as instruções. Se alguém de fora do Office 365 não pode enviar mensagens à sua conta do Office 365, sua conta pode ter terminado na lista de remetentes bloqueados externo. Usuários que estão fora do Office 365 podem tentar remover sozinhos da lista de remetentes bloqueados usando o [portal de autoatendimento de retirada da lista](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).
  
Você pode definir configurações de spam de saída para que você obtenha anotification quando um usuário do Office 365 é impedido de envio de email que é classificada como spam. Depois que o problema com a caixa de correio do usuário for resolvido, você pode remover o bloco de remetente.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>Desbloquear uma conta de email do Office 365

Conclusão da tarefa no Centro de administração do Exchange (EAC). Confira [do Exchange admin center no Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) para obter detalhes sobre o EAC. 
  
> [!NOTE]
> Você não verá a Central de ações, a menos que esteja no EAC para Exchange Online. 
  
1. No EAC, navegue até **proteção** \> **Central de ações**.
    
    ![Navegar até a central de ações no Centro de administração do Exchange](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. Selecione o ícone de **pesquisa** e, em seguida, insira o endereço SMTP do usuário bloqueado. 
    
    ![Pesquisar um usuário bloqueado na central de ações](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. Clique em **Desbloquear conta** do painel de descrição. 
    
    ![Desbloquear um usuário na central de ações](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. Clique em **Sim** para confirmar a alteração. 
    
> [!NOTE]
> Há um limite no número de vezes que uma conta pode ser desbloqueada pelo administrador de locatário. Se o limite de um usuário foi excedido, uma mensagem de erro é exibida. Contate o suporte para desbloquear o usuário. 
  
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
  

  

