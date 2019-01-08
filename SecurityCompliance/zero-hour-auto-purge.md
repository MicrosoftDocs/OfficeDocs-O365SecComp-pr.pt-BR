---
title: Limpeza Automática Zero Hora – proteção contra spam e malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749315"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Limpeza Automática Zero Hora – proteção contra spam e malware

## <a name="overview"></a>Visão geral

Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com malware, spam ou phishing que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado; email pode ser zapped devido ao conteúdo de email, URLs ou anexos.
  
ZAP está disponível com o Exchange Online Protection for incluído com qualquer assinatura do Office 365 que contenha caixas de correio Exchange Online padrão.

ZAP está ativado por padrão, mas as seguintes condições devem ser atendidas:
  
- **Ação de spam** é definido para **mover a mensagem para a pasta Lixo eletrônico**. <br/>Você também pode criar uma nova política de filtro de spam que se aplica somente a um conjunto de usuários se não desejar que todas as caixas de correio a ser filtrada pelo ZAP.

- Os usuários têm mantidos seu padrão configurações de lixo eletrônico e não tem desativado de proteção de lixo eletrônico. (Consulte [alterar o nível de proteção em que o filtro de lixo eletrônico](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) para obter detalhes sobre as opções de usuário no Outlook.) 
  
## <a name="how-does-zap-work"></a>Como funciona o ZAP?

Atualizações de assinaturas de mecanismo e malware antispam do Office 365 em tempo real em uma base diária. No entanto, os usuários ainda podem obter mal-intencionado mensagens entregues a suas caixas de entrada para uma variedade de motivos, incluindo se o conteúdo é aproveitado depois de ser entregue aos usuários. Apagar tudo isso por meio do monitoramento continuamente atualiza e as assinaturas do Office 365 spam e malware de endereços. ZAP pode encontrar e remover mensagens entregues anteriormente que já estão nas caixas de entrada dos usuários. 

- Para email que é identificado como spam, ZAP move mensagens não lidas para a pasta Lixo eletrônico dos usuários. 

- Para email que é identificado como spam, ZAP move mensagens para a pasta de lixo eletrônico dos usuários, independentemente se o email foi lido.

- Para malware detectado recentemente, ZAP remove anexos das mensagens de email, independentemente se o email foi lido. 
  
A ação ZAP é perfeita para o usuário de caixa de correio; eles não são notificados se uma mensagem de email for movida.
  
Permitir listas, [regras de fluxo de correio](https://go.microsoft.com/fwlink/p/?LinkId=722755)e regras do usuário final ou filtros adicionais têm precedência sobre ZAP.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>Para revisar ou definir uma política de filtro de spam
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365.

2. Em **gerenciamento de ameaça**, escolha **anti-spam**.

3. Revise as configurações padrão. 

4. Se desejar personalizar suas configurações, selecione a guia **personalizada** e ativar **configurações personalizadas**. Editar suas configurações e, se desejar, escolha **+ criar uma política** para adicionar uma nova diretiva. 
    
## <a name="to-see-if-zap-moved-your-message"></a>Para ver se ZAP movida sua mensagem

Se você quiser ver se ZAP movida sua mensagem, você pode usar o [relatório de Status de proteção de ameaça](view-email-security-reports.md#threat-protection-status-report) (tanto na [Ameaça Explorer](use-explorer-in-security-and-compliance.md)).
    
## <a name="to-disable-zap"></a>Para desabilitar ZAP
  
Se você deseja desabilitar Apagar tudo para seu locatário do Office 365 ou um conjunto de usuários, use o parâmetro **ZapEnabled** do [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet do EOP.
    
No exemplo a seguir, ZAP está desabilitado para uma política de filtro de conteúdo chamada "Test".
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>Perguntas frequentes

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>O que acontece se uma mensagem legítima é movida para a pasta Lixo eletrônico?
  
Você deve seguir o processo de emissão normal de falsos positivos. A única razão seria movida a mensagem da caixa de entrada para a pasta Lixo eletrônico seria porque o serviço determinou que a mensagem foi spam ou mal intencionado.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Se usar a quarentena do Office 365 em vez da pasta de lixo eletrônico?
  
ZAP não move mensagens em quarentena na caixa de entrada no momento.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>E se eu tiver uma regra de fluxo de email personalizado (bloquear / permitir regra)?
  
Regras criadas por administradores (regras de fluxo de email) ou regras de bloqueio e permitir têm precedência. Essas mensagens são excluídas dos critérios de recurso.
  
## <a name="related-topics"></a>Tópicos Relacionados

[Proteção antispam de emails do Office 365](anti-spam-protection.md)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](block-email-spam-to-prevent-false-negatives.md)
  

