---
title: Controlando o spam de saída no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: Se sua organização envia muita de email em massa que está marcado como spam, você poderia obter bloqueado para envio de email com o Office 365. Leia este artigo para saber mais sobre por que isso acontece e o que você pode fazer sobre ele.
ms.openlocfilehash: 916a062d08e01954e7736b6f22d297aea04baf28
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977576"
---
# <a name="controlling-outbound-spam-in-office-365"></a>Controlando o spam de saída no Office 365

Pegamos Gerenciando spam de saída seriamente porque nossa é um serviço compartilhado.  Há muitos clientes atrás de um pool compartilhado de recursos, onde se um cliente envia spam de saída, ele pode prejudicar a reputação de IP de saída do serviço e afeta a deliverability bem-sucedida de email para outros clientes. É desleal ao cliente A se cliente B envia spam e vários 3º terceiros IP listas de bloqueio de listam o endereço IP que ele usa.

## <a name="what-admins-can-do-to-control-outbound-spam"></a>O que os administradores podem fazer para controlar o spam de saída

- **Habilite as notificações quando uma conta está enviando spam ou desligado**. Os administradores podem obter bcc'ed sempre que uma mensagem é marcada como spam de saída e enviada através do pool de alto risco. Monitorando esta caixa de correio, um administrador pode detectar se eles tiverem uma conta comprometida em sua rede ou se o filtro de spam é por engano marcação seus emails como spam.  Para obter mais informações sobre como configurar a política de spam de saída podem ser encontradas [aqui](configure-the-outbound-spam-policy.md).
 
- **Revise manualmente reclamações de spam de 3º provedores de email de terceiros**. Muitos serviços de email de terceiros 3º como Outlook.com, Yahoo! e AOL fornecem um Loop de Feedback onde se qualquer usuário em seu serviço marca um email de nosso serviço como spam, a mensagem é empacotada e enviada de volta para nós para revisão. Para saber mais sobre o suporte do remetente para o Outlook.com, clique [aqui](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).

## <a name="what-eop-does-to-control-outbound-spam"></a>O que significa a EOP para controlar o spam de saída 

1. **Segregação de tráfego de saída em pools separados de IPs**. Todas as mensagens que os clientes enviam saídos através do serviço é verificada de spam. Se a mensagem de spam, ela é encaminhada pelo pool de entrega de risco alto. Este pool IP contém spam e notificações de status não entregues. Entrega ao destinatário pretendido não é garantida conforme muitos de terceiros não aceitará email porque a qualidade do email emite.

O tráfego a divisão desta forma garante que o email de qualidade inferior (spam, backscatter NDRs) não arrastar para baixo a reputação dos pools de emails de saída regular. O pool de alto risco geralmente tem reputação baixa em muitos receptores em torno da Internet, embora isso não seja universal. 

2. **Reputação de monitoramento do IP**. O Office 365 consultas vários 3º terceiros IP listas de bloqueio e gerará alertas se qualquer um dos nossos IPs saída estão listado neles. Isso permite reagir rapidamente quando spam causou nossa reputação a ser prejudicado. Quando um alerta é gerado, temos documentação interna externos quais etapas a serem executadas para obter removido da lista. 

3. **Desabilitando das contas ofensivos quando eles enviam uma quantidade excessiva email marcada como spam**. Mesmo que podemos segregar os nossos e não spam em dois pools separados de IP de saída, as contas de email não podem enviar spam indefinidamente. Podemos monitorar quais contas estão enviando spam e se ele excede o limite de um, a conta seja bloqueada para envio de spam.

Uma única mensagem marcada como spam pode ser uma misclassification pelo mecanismo de spam e também conhecido como um falso positivo. Podemos enviá-la por meio do pool de alto risco dar-lhe uma chance de saindo; No entanto, um grande número de mensagens em um quadro de hora curta é indicar um problema e que ocorre, podemos bloquear a conta do envio de qualquer email mais. Há limites diferentes que existem para contas de email individuais, bem como aggregate para o locatário inteiro.

4. **Desabilitando das contas ofensivos quando eles enviam uma quantidade excessiva email no muito curto um período de tempo**. Além dos limites acima desse aparência para uma proporção de mensagens marcadas como spam, também há limites que bloqueiam contas quando atingirem um limite total, independentemente de estarem ou não as mensagens são marcadas como spam. O motivo pelo qual que esse limite existe é porque uma conta comprometida poderia enviem spam de dia zero que é perdida pelo filtro de spam. Como é difícil, se não impossível, às vezes dizer a diferença entre uma campanha de envio em massa legítima e uma campanha de spam em massa, esses limites ativar para limitar os danos potenciais.

> [!NOTE]
> Para #3 e 4 #, podemos não anuncie os limites exatos.  Isso é para impedir que os autores de spam jogos do sistema e certifique-se de que podemos alterar os limites quando precisarmos. Os limites são alta o suficiente para que um usuário de empresas de médio porte nunca atingirá-los e baixa o suficiente para que ele contém a maioria dos danos que pode ser feito por um remetente de spam. 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a>Soluções alternativas recomendadas para os clientes que desejam enviar saída muita de email por meio do EOP

É difícil obter um equilíbrio entre os clientes que desejam enviar um grande volume de email versus protegendo o serviço de contas comprometidas e emailers em massa com as práticas de aquisição de lista ruim. Novamente, o custo de uma saída IP inicial em uma lista de bloqueios de terceiros 3º é maior que o bloqueio de um cliente de enviar emails de saída. Conforme descrito no [Exchange Online Service Description](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits), usando o EOP para enviar emails em massa não é um com suporte ao uso do serviço e é permitido somente em uma base "melhor esforço". Para clientes que desejam enviar email em massa, recomendamos o seguinte:

r. **enviar o email em massa por meio de seus próprios servidores de email no local**. Isso significa que o cliente terá que manter sua própria infra-estrutura de email para esse tipo de email.

b. **emailer de em massa de terceiros de uso um 3rd para enviar a comunicação em massa**. Há várias 3º participante em massa emailers cujo negócio único é enviar emails em massa. Eles podem trabalhar com os clientes para garantir que eles têm boas práticas enviando e eles têm recursos dedicados ao impô-la. 

As mensagens, Mobile, Malware antiabuso Working Group (MAAWG) publica sua lista de participação de associação [aqui](http://www.maawg.org/about/roster). Vários provedores de email em massa estão na lista e são conhecidos como ser responsáveis cidadãos de Internet. 
  
## <a name="for-more-information"></a>Para saber mais

[Notificação de amostra quando um remetente for bloqueado enviem spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[Proteção antispam de emails do Office 365](anti-spam-protection.md)

[Proteção antifalsificação no Office 365](anti-spoofing-protection.md)

[Níveis de confiança de spam](spam-confidence-levels.md)
