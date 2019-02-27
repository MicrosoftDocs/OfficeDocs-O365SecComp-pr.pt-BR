---
title: Como controlar spam de saída no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Se sua organização enviar muitas mensagens em massa marcadas como spam, você poderá ter impedido de enviar emails com o Office 365. Leia este artigo para saber mais sobre por que isso acontece e o que você pode fazer sobre ele.
ms.openlocfilehash: 2cfcb7016b0c0d11117f6d78af2632229c70aa1d
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275921"
---
# <a name="controlling-outbound-spam-in-office-365"></a>Como controlar spam de saída no Office 365

Adotamos o gerenciamento de spam de saída seriamente porque nosso é um serviço compartilhado.  Há muitos clientes por trás de um pool compartilhado de recursos, onde um cliente envia spams de saída, pode degradar a reputação de IP de saída do serviço e afeta a entrega bem-sucedida de emails para outros clientes. Não é justo para o cliente A se o cliente B spam e vários IPs de terceiros listas listar o endereço IP que ele usa.

## <a name="what-admins-can-do-to-control-outbound-spam"></a>O que os administradores podem fazer para controlar o spam de saída

- **Habilitar notificações quando uma conta estiver enviando spam ou**desligada. Os administradores podem obter estava sempre que uma mensagem é marcada como spam de saída e enviada através do pool de alto risco. Ao monitorar esta caixa de correio, um administrador pode detectar se eles têm uma conta comprometida em sua rede ou se o filtro de spam está marcando incorretamente o email como spam.  É possível encontrar mais informações sobre como configurar a política de spam [](configure-the-outbound-spam-policy.md)de saída.
 
- **ReviSe manualmente as reclamações de spam de provedores de email de terceiros**. Muitos serviços de email de terceiros, como o Outlook.com, o Yahoo e o AOL, fornecem um loop de feedback em que se qualquer usuário em seu serviço marcar um email de nosso serviço como spam, a mensagem será empacotada e enviada de volta para nós para análise. Para saber mais sobre o suporte do remetente para o Outlook.com, clique [aqui](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).

## <a name="what-eop-does-to-control-outbound-spam"></a>O que o EOP faz para controlar o spam de saída 

1. **Diferenciação de tráfego de saída em pools de IPS separados**. Todas as mensagens que os clientes enviam saída por meio do serviço são verificadas quanto ao spam. Se a mensagem for spam, ela será roteada através do pool de entrega de alto risco. Este pool de IPS contém notificações de status e spam não entregues. A entrega ao destinatário pretendido não é garantida, pois muitos terceiros não aceitarão emails, pois a qualidade do email emite.

Dividir o tráfego dessa forma garante que o email de qualidade inferior (spam, NDRs de inspersão) não arraste para baixo a reputação dos pools de email de saída normais. O pool de alto risco geralmente tem baixa reputação de muitos receptores pela Internet, embora isso não seja universal. 

2. **Monitoramento da reputação do IP**. O Office 365 consulta vários IP de terceiros listas e gera alertas se qualquer um dos nossos IPs de saída estiverem listados neles. Isso nos permite reagir rapidamente quando o spam causa a degradação da nossa reputação. Quando um alerta é gerado, temos documentação interna contratando quais etapas devem ser executadas para serem deslistadas. 

3. **Desabilitação de contas incorretas quando eles enviam muitos emails marcados como spam**. Embora segrego nosso spam e não spam em dois pools de IP de saída separados, as contas de email não podem enviar spam indefinidamente. Monitoramos quais contas estão enviando spam e se elas excedem um limite não divulgado, a conta é impedida de enviar spam.

Uma única mensagem marcada como spam pode ser uma classificação inválida pelo mecanismo de spam e também conhecida como falso positivo. Nós o enviamos pelo pool de alto risco para dar a chance de sair; no entanto, um grande número de mensagens em um curto período de tempo indica um problema e, quando isso ocorre, impede que a conta envie mais email. Há diferentes limites que existem para contas de email individuais, bem como em agregação para o locatário inteiro.

4. **Desabilitar as contas incorretas quando eles enviam muito email em um período de tempo muito curto**. Além dos limites acima que procuram uma proporção de mensagens marcadas como spam, também há limites que as contas de bloqueio quando atingem um limite geral independentemente de as mensagens estarem marcadas como spam. O motivo pelo qual esse limite existe é porque uma conta comprometida pode enviar spam de zero dias que não foi perdido pelo filtro de spam. Como é difícil, se não for impossível, para às vezes dizer a diferença entre uma campanha de email em massa legítima e uma campanha de spam maciça, esses limites são ativados para limitar qualquer dano em potencial.

> [!NOTE]
> Para #3 e #4, não anunciamos os limites exatos.  Isso é para evitar que os remetentes de spam coterem o sistema e para garantir que possamos alterar os limites quando precisarmos. Os limites são altos o suficiente, de forma que um usuário de negócios médio nunca o acessará e o suficiente para que ele contenha a maior parte dos danos que um spammer pode fazer. 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a>Soluções alternativas recomendadas para clientes que desejam enviar uma grande quantidade de emails por meio do EOP

É difícil fazer um equilíbrio entre os clientes que desejam enviar um grande volume de emails versus proteger o serviço de contas comprometidas e emails em massa com práticas de aquisição de lista deficiente. Novamente, o custo de um início de IP de saída em uma barra de bloqueio de terceiros é maior do que impedir que um cliente envie emails de saída. Conforme descrito na [Descrição do serviço do Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits), o uso do EOP para enviar emails em massa não é um uso com suporte do serviço e só é permitido em uma base de "melhor esforço". Para clientes que desejam enviar email em massa, recomendamos o seguinte:

a. **envie o email em massa por meio de seus próprios servidores de email locais**. Isso significa que o cliente terá que manter sua própria infraestrutura de email para esse tipo de email.

b. **use um email em massa de terceiros para enviar a comunicação em massa**. Há vários emails em massa de terceiros cujo único negócio é enviar email em massa. Eles podem trabalhar com os clientes para garantir que eles tenham boas práticas de email e que tenham recursos dedicados à imposição. 

O grupo de trabalho do MAAWG (mensagens antiAbuso, móvel e malware) publica sua lista de associação [aqui](http://www.maawg.org/about/roster). Vários provedores de email em massa estão na lista e são conhecidos como cidadãos da Internet responsáveis. 
  
## <a name="for-more-information"></a>Para saber mais

[Notificação de exemplo quando um remetente é bloqueado enviando spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[Proteção antispam de emails do Office 365](anti-spam-protection.md)

[Proteção antifalsificação no Office 365](anti-spoofing-protection.md)

[Níveis de confiança de spam](spam-confidence-levels.md)
