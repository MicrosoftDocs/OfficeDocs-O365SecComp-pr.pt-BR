---
title: Limpeza Automática Zero Hora – proteção contra spam e malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
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
ms.openlocfilehash: dc8901dc7c1db5b323ccbeee610647b8a302fcb3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523659"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Limpeza Automática Zero Hora – proteção contra spam e malware

Limpeza automática de zero horas (ZAP) é um recurso de proteção de email que detecta mensagens com spam ou malware que já foram entregues às caixas de entrada dos usuários e processa o conteúdo mal-intencionado inofensiva. Como ZAP faz isso depende do tipo de conteúdo mal-intencionado detectado.
  
ZAP está disponível com o Exchange Online Protection for incluído com qualquer assinatura do Office 365 que contenha caixas de correio Exchange Online padrão.
  
## <a name="how-does-zap-work"></a>Como funciona o ZAP?

Atualizações de assinaturas de mecanismo e malware antispam do Office 365 em tempo real em uma base diária. No entanto, os usuários ainda podem obter mal-intencionado mensagens entregues a suas caixas de entrada para uma variedade de motivos, inclusive quando o conteúdo foi aproveitado por vez depois que ela foi entregue primeiro aos usuários. Apagar tudo isso por meio do monitoramento continuamente é atualizado para as assinaturas de spam e malware Office 365, de endereços e, portanto, encontrar e remover mensagens previamente distribuídas já nas caixas de entrada. Para email que já foi identificada como spam, ZAP move mensagens não lidas para pasta de lixo eletrônico do usuário. Para malware detectado recentemente, ZAP remove os anexos da mensagem de email, independentemente se o email foi lido ou não. O inverso é verdadeiro para mensagens que foram classificadas incorretamente como sendo maliciosas.
  
A ação ZAP é perfeita para o usuário de caixa de correio, ele ou ela não será notificada que de correio foi movida.
  
Permitir listas, [regras de fluxo de correio](https://go.microsoft.com/fwlink/p/?LinkId=722755)e regras do usuário final ou filtros adicionais têm precedência sobre ZAP.
  
 **Neste artigo:**
  
> [Definir a política de filtro de spam](zero-hour-auto-purge.md#BK_SetSpam)
    
> [Consulte se ZAP movidos sua mensagem](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [Desabilitar ZAP](zero-hour-auto-purge.md#BK_Posh)
    
> [Perguntas frequentes](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a>Trabalhando com ZAP

ZAP está ativado por padrão, mas você precisará certificar-se de que algumas das condições forem atendidas:
  
- Política de filtro de spam é definida para [mover a mensagem para a pasta Lixo eletrônico](zero-hour-auto-purge.md#BK_SetSpam).
    
    Você também pode criar uma nova política de filtro de spam que se aplica somente a um conjunto de usuários se não desejar que todas as caixas de correio a ser filtrada pelo ZAP.
    
- O usuário [opções \> lixo eletrônico](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).
    
Se você quiser [ver se ZAP movida sua mensagem](zero-hour-auto-purge.md#BK_DidZAPMove), você pode usar a ferramenta de rastreamento de mensagem do Exchange Online.
  
Os administradores também podem [Desabilitar ZAP](zero-hour-auto-purge.md#BK_Posh) usando o PowerShell. 
  
 **Para definir a política de filtro de spam**
  
1. Entrar no [Where entrar no Office 365 para empresas](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) e escolha **proteção** \> **filtro de spam**. 
    
    ![No EAC, escolha a proteção e, em seguida, o filtro de spam](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. Escolha a política de filtro que você deseja ajustar, ou escolha **Adicionar**![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) para criar um novo. 
    
    A captura de tela anterior, a política é chamada "Default", mas se você criar políticas de filtro de spam adicional podem fornecer-lhes um nome diferente. Você também pode aplicar a política a apenas um conjunto limitado de usuários.
    
3. Na janela de política, escolha **ações em massa e de spam**e certifique-se de que o **Spam** seja definido como **Mover mensagem para a pasta Lixo eletrônico**. 
    
    Se você escolher **Salvar** neste ponto, a política se aplica ao seu locatário do Office 365. 
    
    ![Conjuntos de ações em massa e de spam a mensagem Mpve para a pasta Lixo eletrônico](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. Se você criou uma nova política, e você deseja aplicar a política a apenas um conjunto de usuários, role para a seção **Aplicada a** na janela de filtro de diretiva e dos controles de menu escolher os **destinatários**, **domínio**ou **associações de grupo** você deseja aplicar a política. Você também pode definir exceções e condições adicionais. 
    
    ![Na seção aplicada a escolher os destinatários](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    Escolha **Salvar** para aplicar a política aos usuários selecionados. 
    
 **Para ver se ZAP movida sua mensagem**
  
- Você pode usar a [descobrir e corrigir problemas de entrega de email como um Office 365 para administração de empresa](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) para determinar se a mensagem foi movida pela ZAP: 
    
    Procure o texto "Zero horas automático Limpar (ZAP)" em seus detalhes de rastreamento para identificar uma mensagem que foi movida por ZAP.
    
 **Para desabilitar ZAP**
  
- Se você deseja desabilitar Apagar tudo para seu locatário do Office 365 ou um conjunto de usuários, use o parâmetro **ZapEnabled** do [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), um cmdlet do EOP.
    
    No exemplo a seguir, ZAP está desabilitado para uma política de filtro de conteúdo chamada "Test".
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a>Perguntas frequentes
<a name="BK_FAQ"> </a>

 **O que acontece se uma mensagem legítima é movida para a pasta Lixo eletrônico?**
  
Você deve seguir o processo de emissão normal de falsos positivos. A única razão seria movida a mensagem da caixa de entrada para a pasta Lixo eletrônico seria porque o serviço determinou que a mensagem foi spam ou mal intencionado.
  
 **Se usar a quarentena do Office 365 em vez da pasta de lixo eletrônico?**
  
ZAP não move mensagens em quarentena na caixa de entrada no momento.
  
 **E se eu tiver uma regra de fluxo de email personalizado (bloquear / permitir regra)?**
  
Regras criadas por administradores (regras de fluxo de email) ou regras de bloqueio e permitir têm precedência. Essas mensagens são excluídas dos critérios de recurso.
  
## <a name="related-topics"></a>Tópicos relacionados
<a name="BK_FAQ"> </a>

[Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](block-email-spam-to-prevent-false-negatives.md)
  

