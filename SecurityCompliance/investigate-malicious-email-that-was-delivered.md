---
title: Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection: M365-security-compliance
description: Saiba como usar a inteligência de ameaças para localizar e investigar emails mal-intencionados.
ms.openlocfilehash: adf4066b5119f131b90dc88b99be4011582931c2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215491"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)

O [Office 365 Threat Intelligence](office-365-ti.md) permite investigar as atividades que colocam seus usuários em risco e tomar medidas para proteger sua organização. Por exemplo, se você fizer parte da equipe de segurança da sua organização, poderá encontrar e investigar mensagens de email suspeitas que foram entregues aos seus usuários. Você pode fazer isso usando o [Explorador de ameaças](get-started-with-ti.md#threat-explorer).
  
> [!IMPORTANT]
> A partir de fevereiro de 2019 e saindo dos próximos meses, o Office 365 Threat Intelligence está se tornando o Office 365 Advanced Threat Protection Plan 2, com recursos adicionais de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
  
## <a name="before-you-begin"></a>Antes de começar...

Verifique se os seguintes requisitos são atendidos:
  
- Sua organização tem a [inteligência contra ameaças do office 365](office-365-ti.md) e [atribui licenças aos usuários no Office 365 para empresas](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- O [log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) está ativado para sua organização. 
    
- Sua organização tem políticas definidas para antispam, anti-malware, anti-phishing e assim por diante. Consulte [Gerenciamento de ameaças no centro de conformidade &amp; de segurança do Office 365](threat-management.md).
    
- Você é um administrador global do Office 365 ou tem o administrador de segurança ou a função de pesquisa e limpeza atribuída no centro de &amp; conformidade de segurança. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Lidando com emails suspeitos

Invasores mal-intencionados podem estar enviando emails aos seus usuários para tentarem e Phish suas credenciais e obter acesso aos segredos corporativos! Para evitar isso, você deve usar os serviços de proteção contra ameaças oferecidos pelo Office 365, incluindo proteção do Exchange Online e proteção avançada contra ameaças. No enTanto, há ocasiões em que um invasor pode enviar emails para seus usuários que contenham uma URL e apenas mais tarde, fazer essa URL apontar para conteúdo mal-intencionado (malware, etc.). Como alternativa, você pode perceber muito tarde que um usuário em sua organização foi comprometido e enquanto esse usuário foi comprometido, um invasor usou essa conta para enviar emails a outros usuários da sua empresa. Como parte da limpeza desses dois cenários, talvez você queira remover mensagens de email de caixas de entrada de usuários. Em situações como essas, você pode usar o explorador de ameaças para encontrar e remover essas mensagens de email!
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Localizar e excluir emails suspeitos que foram entregues

> [!TIP]
> [Explorador de ameaças](get-started-with-ti.md#threat-explorer) (também chamado de Explorer), é um relatório poderoso que pode servir a vários propósitos, como localizar e excluir mensagens, identificar o endereço IP de um remetente de email mal-intencionado ou iniciar um incidente para investigação adicional. O procedimento a seguir se concentra no uso do Explorer para localizar e excluir emails mal-intencionados de caixas de correio de destinatários. 
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365. Isso leva você para o centro &amp; de conformidade de segurança. 
    
2. No painel de navegação à esquerda, escolha **Gerenciador**de **Gerenciamento** \> de ameaças.
    
3. No menu Exibir, escolha **todos os emails**.<br/>![Usar o menu Exibir para escolher entre relatórios de email e conteúdo](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Observe os rótulos que aparecem no relatório, como **entregue**, **desconhecido**ou **entregue ao lixo eletrônico**.<br/>![Explorador de ameaças mostrando dados para todos os emails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Dependendo das ações que foram tomadas nas mensagens de email de sua organização, você poderá ver rótulos adicionais, como bloqueados **** ou **substituídos**.)
    
5. No relatório, escolha **entregue** para exibir apenas os emails que acabaram nas caixas de entrada dos usuários.<br/>![Clicar em "entregue a lixo eletrônico" remove esses dados da exibição](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Abaixo do gráfico, revise **** a lista de emails abaixo do gráfico.<br/>![Abaixo do gráfico, exiba uma lista de mensagens de email que foram detectadas](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Na lista, escolha um item para exibir mais detalhes sobre a mensagem de email. Por exemplo, você pode clicar na linha de assunto para exibir informações sobre o remetente, destinatários, anexos e outras mensagens de email semelhantes.<br/>![Você pode visualizar informações adicionais sobre um item, incluindo detalhes e todos os anexos](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Após exibir informações sobre mensagens de email, selecione um ou mais itens na lista para ativar **+ ações**.
    
9. Use a lista de **ações +** para aplicar uma ação, como **mover para itens excluídos** . Isso excluirá as mensagens selecionadas das caixas de correio dos destinatários.<br/>![Ao selecionar uma ou mais mensagens de email, você pode escolher entre várias ações disponíveis](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  
[Proteção contra ameaças do Office 365](protect-against-threats.md)
  
[Exibir relatórios para a proteção avançada contra ameaças do Office 365](view-reports-for-atp.md)
  

