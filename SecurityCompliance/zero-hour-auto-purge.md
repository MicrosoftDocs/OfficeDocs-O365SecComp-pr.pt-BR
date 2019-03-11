---
title: Limpeza automática de zero horas-proteção contra spam e malware
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: A limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos seus usuários e renderiza o conteúdo mal-intencionado inofensivo. Como o ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.
ms.openlocfilehash: b28de1b05843e3f5b0f6e7fc905c96f094c277f9
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524015"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Limpeza automática de zero horas-proteção contra spam e malware

## <a name="overview"></a>Visão geral

A limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com phishing, spam ou malware que já foram entregues às caixas de entrada dos seus usuários e renderiza o conteúdo mal-intencionado inofensivo. Como o ZAP depende do tipo de conteúdo mal-intencionado detectado; os emails podem ser zapped devido a conteúdo, URLs ou anexos de email.
  
O ZAP está disponível com a proteção do Exchange Online padrão incluída em qualquer assinatura do Office 365 que contenha caixas de correio do Exchange Online.

O ZAP é ativado por padrão, mas as seguintes condições devem ser atendidas:
  
- A **ação de spam** é definida para **mover a mensagem para a pasta lixo eletrônico**. <br/>Você também pode criar uma nova política de filtro de spam que se aplique somente a um conjunto de usuários se não quiser que todas as caixas de correio sejam filtradas por ZAP.

- Os usuários mantiveram suas configurações de lixo eletrônico padrão e não desativaram a proteção de lixo eletrônico. (Consulte [alterar o nível de proteção no filtro de lixo eletrônico](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) para obter detalhes sobre as opções do usuário no Outlook.) 
  
## <a name="how-does-zap-work"></a>Como o ZAP funciona?

O Office 365 atualiza as assinaturas de malware e mecanismo antispam em tempo real diariamente. No enTanto, os usuários ainda podem obter mensagens mal-intencionadas entregues às suas caixas de entrada por vários motivos, incluindo se o conteúdo é enarmado depois de ser entregue aos usuários. O ZAP aborda isso ao monitorar atualizações continuamente nas assinaturas de spam e malware do Office 365. ZAP pode localizar e remover mensagens entregues anteriormente que já estão nas caixas de entrada dos usuários. 

- Para email identificado como spam, o ZAP move as mensagens não lidas para a pasta lixo eletrônico dos usuários. 

- Para email identificado como Phish, o ZAP move mensagens para a pasta lixo eletrônico dos usuários, independentemente se o email foi lido.

- Para malware recém detectado, ZAP remove anexos de mensagens de email, independentemente de o email ter sido lido. 
  
A ação ZAP é transparente para o usuário da caixa de correio; Eles não são notificados quando uma mensagem de email é movida.
  
As listas de permissões, [as regras de fluxo](https://go.microsoft.com/fwlink/p/?LinkId=722755)de emails e as regras de usuário final ou filtros adicionais têm precedência sobre o zap.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>Para revisar ou configurar uma política de filtro de spam
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante para o Office 365.

2. Em **Gerenciamento de ameaças**, escolha **anti-spam**.

3. Revise as configurações padrão. 

4. Se você quiser personalizar suas configurações, selecione a guia **personalizado** e ative **as configurações personalizadas**. Edite suas configurações e, se desejar, escolha **+ criar uma política** para adicionar uma nova política. 
    
## <a name="to-see-if-zap-moved-your-message"></a>Para ver se ZAP moveu sua mensagem

Se você deseja ver se ZAP moveu sua mensagem, pode usar o relatório de [status de proteção contra ameaças](view-email-security-reports.md#threat-protection-status-report) (ou o [Gerenciador de ameaças](use-explorer-in-security-and-compliance.md)).
    
## <a name="to-disable-zap"></a>Para desabilitar o ZAP
  
Se você quiser desabilitar o ZAP para o seu locatário do Office 365, ou um conjunto de usuários, use o parâmetro **ZapEnabled** de [set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet EOP.
    
No exemplo a seguir, o ZAP é desabilitado para uma política de filtro de conteúdo chamada "Test".
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>Perguntas frequentes

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>O que acontece se uma mensagem legítima for movida para a pasta lixo eletrônico?
  
Você deve seguir o processo de relatório normal para falsos positivos. A única razão pela qual a mensagem seria movida da caixa de entrada para a pasta lixo eletrônico seria porque o serviço determinou que a mensagem era spam ou mal-intencionada.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>E se eu usar a quarentena do Office 365 em vez da pasta lixo eletrônico?
  
ZAP não move mensagens para a quarentena da caixa de entrada neste momento.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>E se eu tiver uma regra de fluxo de emails personalizada (regra bloquear/permitir)?
  
Regras criadas por administradores (regras de fluxo de emails) ou regras de bloqueio e permissão têm precedência. Essas mensagens são excluídas dos critérios de recurso.
  
## <a name="related-topics"></a>Tópicos Relacionados

[Proteção anti-spam de emails do Office 365](anti-spam-protection.md)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](reduce-spam-email.md)
  

