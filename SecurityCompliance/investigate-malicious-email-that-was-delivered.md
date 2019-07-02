---
title: Encontre e investigue emails mal-intencionados que foram fornecidos (investigação de ameaças e resposta do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Saiba como usar os recursos de investigação e resposta contra ameaças para encontrar e investigar emails mal-intencionados.
ms.openlocfilehash: febcf6704b1ba9dc23bf4e698715fb4b929b998b
ms.sourcegitcommit: d3b2bffa8af5f19d97fe9771068c80705b890e85
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2019
ms.locfileid: "35414801"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>Encontre e investigue emails mal-intencionados que foram entregues (Office 365 Advanced Threat Protection Plan 2)

A [proteção avançada contra ameaças do Office 365](office-365-atp.md) permite investigar as atividades que colocam seus usuários em risco e tomar medidas para proteger sua organização. Por exemplo, se você fizer parte da equipe de segurança da sua organização, poderá encontrar e investigar mensagens de email suspeitas que foram entregues aos seus usuários. Você pode fazer isso usando o [Explorador de ameaças (ou detecções em tempo real)](threat-explorer.md).
  
## <a name="before-you-begin"></a>Antes de começar...

Verifique se os seguintes requisitos são atendidos:
  
- Sua organização tem a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (plano 1 ou plano 2) e as [licenças são atribuídas aos usuários](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- O [log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) está ativado para sua organização. 
    
- Sua organização tem políticas definidas para antispam, anti-malware, anti-phishing e assim por diante. Confira [proteção contra ameaças no Office 365](protect-against-threats.md).
    
- Você é um administrador global do Office 365 ou tem o administrador de segurança ou a função de pesquisa e limpeza atribuída no centro de &amp; conformidade de segurança. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Lidando com emails suspeitos

Invasores mal-intencionados podem estar enviando emails aos seus usuários para tentarem e Phish suas credenciais e obter acesso aos segredos corporativos! Para evitar isso, você deve usar os serviços de proteção contra ameaças no Office 365, incluindo [proteção do Exchange Online](eop/exchange-online-protection-overview.md) e [proteção avançada contra ameaças](office-365-atp.md). No entanto, há ocasiões em que um invasor pode enviar emails para seus usuários que contenham uma URL e apenas mais tarde, fazer essa URL apontar para conteúdo mal-intencionado (malware, etc.). Como alternativa, você pode perceber muito tarde que um usuário em sua organização foi comprometido e enquanto esse usuário foi comprometido, um invasor usou essa conta para enviar emails a outros usuários da sua empresa. Como parte da limpeza desses dois cenários, talvez você queira remover mensagens de email de caixas de entrada de usuários. Em situações como essas, você pode usar o [Explorador de ameaças (ou detecções em tempo real)](threat-explorer.md) para encontrar e remover essas mensagens de email!

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a>Onde os emails redirecionados são localizados após a tomada de ações

As detecções de tempo real do explorador de ameaças adicionaram os campos de ação de entrega e local de entrega no local do status de entrega. Isso resulta em uma imagem mais completa de onde seus emails se esterram. Parte do objetivo dessa alteração é tornar a busca mais fácil para pessoas de operações de segurança, mas o resultado líquido é saber o local dos emails de problemas em um relance.

O status de entrega agora é dividido em duas colunas:

- **Ação de entrega** -Qual é o status desse email?
- **Local de entrega** -onde esse email foi roteado como resultado?

A ação de entrega é a ação realizada em um email devido a políticas ou detecções existentes. Veja a seguir as possíveis ações que um email pode executar:

1. **Entregue** – o email foi entregue à caixa de entrada ou pasta de um usuário, e o usuário pode acessá-lo diretamente.
2. **Lixo eletrônico** – o email foi enviado à pasta de lixo eletrônico ou à pasta excluída do usuário, e o usuário tem acesso a emails na pasta lixo eletrônico ou excluído.
3. **Bloqueado** – todos os emails que estão em quarentena, que falharam ou foram descartados. Isso é completamente inacessível pelo usuário!
4. **Substituído** – qualquer email onde anexos mal-intencionados são substituídos por arquivos. txt que indicam que o anexo era mal-intencionado.
 
O local de entrega mostra os resultados das políticas e detecções que executam post-Delivery. Ele está vinculado a uma ação de entrega. Este campo foi adicionado para dar informações sobre a ação tomada quando um email de problema é encontrado. Estes são os possíveis valores de local de entrega:

1. **Caixa de entrada ou pasta** – o email está na caixa de entrada ou uma pasta (de acordo com suas regras de email).
2. **Local ou externo** – a caixa de correio não existe na nuvem, mas está no local.
3. **Pasta lixo eletrônico** – o email na pasta lixo eletrônico de um usuário.
4. **Pasta itens excluídos** – o email na pasta itens excluídos de um usuário.
5. **Quarentena** – o email em quarentena e não está na caixa de correio de um usuário.
6. **Falha** – o email não pôde chegar à caixa de correio.
7. **Descartado** – o email é perdido em algum lugar no fluxo.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Localizar e excluir emails suspeitos que foram entregues

> [!TIP]
> O Gerenciador de ameaças (às vezes chamado de Explorer) é um relatório poderoso que pode servir a vários propósitos, como localizar e excluir mensagens, identificar o endereço IP de um remetente de email mal-intencionado ou iniciar um incidente para investigação adicional. O procedimento a seguir se concentra no uso do Explorer para localizar e excluir emails mal-intencionados de caixas de correio de destinatários.

Para ver as alterações no campo status da entrega anterior (agora, a ação de entrega e o local de entrega): 

1. Acesse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365. Isso leva você para o centro &amp; de conformidade de segurança. 
    
2. No painel de navegação à esquerda, escolha **Gerenciador**de **Gerenciamento** \> de ameaças.
<!--Comment>
![Threat Explorer with Delivery Action and Delivery Location fields.](media/ThreatExFields.PNG)

    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a>Tópicos relacionados

[Office 365 plano avançado de proteção contra ameaças 2](office-365-ti.md)
  
[Proteção contra ameaças no Office 365](protect-against-threats.md)
  
[Exibir relatórios para a proteção avançada contra ameaças do Office 365](view-reports-for-atp.md)
  

