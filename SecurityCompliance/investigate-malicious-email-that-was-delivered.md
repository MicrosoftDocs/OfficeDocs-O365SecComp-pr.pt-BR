---
title: Localizar e investigar email mal-intencionado que foi entregue (Office 365 Threat Intelligence)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/6/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
description: Aprenda a usar inteligência de ameaça para localizar e investigar email mal-intencionado.
ms.openlocfilehash: 4440b4d1503b9a13977ef773b95fa64873662b85
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706035"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Localizar e investigar email mal-intencionado que foi entregue (Office 365 Threat Intelligence)

[Office 365 Threat Intelligence](office-365-ti.md) permite investigar atividades que colocam seus usuários em risco e ações para proteger sua organização. Por exemplo, se você fazem parte da equipe de segurança da sua organização, poderá localizar e investigar mensagens de email suspeitas que foram entregues aos seus usuários. Você pode fazer isso usando o [Gerenciador de ameaça](get-started-with-ti.md#threat-explorer).
  
> [!NOTE]
> O Office 365 Threat Intelligence está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, inteligência de dados do Office 365 ameaça pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="before-you-begin"></a>Antes de começar...

Verifique se os seguintes requisitos são atendidos:
  
- Sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md) e [Atribuir licenças aos usuários no Office 365 para empresas](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- [Log de auditoria do Office 365](turn-audit-log-search-on-or-off.md) é ativada para sua organização. 
    
- Sua organização tem políticas definidas para antispam, antimalware, antiphishing e assim por diante. Consulte [gerenciamento de segurança do Office 365 de ameaça &amp; Centro de conformidade](threat-management.md).
    
- Você é um administrador global do Office 365 ou você tem o administrador de segurança ou a função de pesquisa e limpar atribuída na segurança &amp; Centro de conformidade. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Lidando com emails suspeitos

Invasores mal-intencionados podem ser enviar email aos seus usuários para testar e phishing suas credenciais e acessar os seus segredos corporativos! Para impedir isso, você deve usar os serviços de proteção de ameaça oferecidos pelo Office 365, incluindo o Exchange Online Protection e proteção avançada de ameaça. No entanto, há ocasiões quando um invasor pode enviar emails para seus usuários contendo uma URL e apenas no futuro fazer esse ponto de URL conteúdo mal-intencionado (malware, etc.). Como alternativa, você pode perceber muito depois que um usuário em sua organização foi comprometido e enquanto o usuário foi comprometido, o invasor usados essa conta para enviar email para outros usuários da sua empresa. Como parte do limpando esses dois cenários, convém remover mensagens de email de entrada dos usuários. Em situações como essas, você pode aproveitar o Explorer de ameaça para encontrar e remover essas mensagens de email!
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Localizar e excluir email suspeita que foi entregue

> [!TIP]
> [Gerenciador de ameaça](get-started-with-ti.md#threat-explorer) (também conhecido como Explorer) é um relatório poderoso que pode atender a vários propósitos, como Localizando e excluindo mensagens, que identifica o endereço IP de um remetente do email maliciosa ou iniciar um incidente para uma investigação detalhada. O procedimento a seguir se concentra em usando o Explorer para localizar e excluir email maliciosa de caixas de correio de destinatários. 
  
1. Vá para [https://security.microsoft.com](https://security.microsoft.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. Isso leva você para a segurança &amp; Centro de conformidade. 
    
2. No painel de navegação esquerdo, escolha **gerenciamento de ameaça** \> **Explorer**.
    
3. No menu Exibir, escolha **todos os emails**.<br/>![Use o menu Exibir para escolher entre eletrônico e conteúdo de relatórios](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Observe os rótulos que aparecem no relatório, como **entregues**, **desconhecido**ou **entregue ao lixo**.<br/>![Gerenciador de ameaça mostrando dados para todos os emails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Dependendo das ações que foram feitas em mensagens de email para sua organização, você poderá ver rótulos adicionais, como **bloqueado** ou **foi substituído**.)
    
5. No relatório, escolha **entregue** para exibir somente os emails que terminou nas caixas de entrada dos usuários.<br/>![Clicando em "Entregue ao lixo" remove dados de modo de exibição](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. O gráfico abaixo, revise a lista de **Email** abaixo do gráfico.<br/>![O gráfico abaixo, exibir uma lista de mensagens de email que foram detectados](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Na lista, escolha um item para exibir mais detalhes sobre essa mensagem de email. Por exemplo, você pode clicar a linha de assunto para exibir informações sobre o remetente, recipients, anexos e outras semelhantes mensagens de email.<br/>![Você pode exibir informações adicionais sobre um item, incluindo detalhes e todos os anexos](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Depois de exibir informações sobre as mensagens de email, selecione um ou mais itens na lista para ativar **+ ações**.
    
9. Use a lista **+ ações** para aplicar uma ação, como itens de **Mover para excluído** . Isso excluirá as mensagens selecionadas de caixas de correio dos destinatários.<br/>![Quando você seleciona uma ou mais mensagens de email, você poderá escolher entre várias ações disponíveis](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  
[Proteção contra ameaças do Office 365](protect-against-threats.md)
  
[Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)
  

