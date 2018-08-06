---
title: Notificação de amostra quando um remetente for bloqueado enviem spam de saída
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
description: 'Quando um remetente seja bloqueado para o serviço devido ao envio de spam de saída, o administrador de domínio especificado quando você configurar a política de spam de saída receberá um email de notificação semelhante ao seguinte:'
ms.openlocfilehash: c9954d3ea16582a66185d574bcb5fc8a1aeebbf9
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027458"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a>Notificação de amostra quando um remetente for bloqueado enviem spam de saída

Quando um remetente é bloqueado pelo serviço devido ao envio de saída de spam, o administrador de domínio especificado quando você [Configurar a política de spam de saída](configure-the-outbound-spam-policy.md) receberá um email de notificação semelhante ao seguinte: 
  
 **Endereço do remetente:** spamalerts@microsoft.com 
  
 **Assunto:** Notificação de spam de saída - \< *nome da conta* \> bloqueado para enviar email de saída     
  
 **Corpo:** Esta é uma resposta automática do sistema de análise de Spam do Exchange Online Protection. 
  
Você está sendo contatado porque foi detectado volumes altos de email marcadas como spam ou outro comportamento suspeito, provenientes de sua organização. As contas de email a seguir foram bloqueadas enviem email (eles ainda poderá receber email):
  
\<*nome da conta*  \> 
  
É provável que essa conta de email foi comprometida. Siga estas etapas:
  
1. Resolva esse problema no seu lado a lado:
    
  - Alterando a senha da conta.
    
  - Determinar como a conta foi comprometida.
    
  - Tomando precauções para garantir que essa vulnerabilidade não vai ser explorada novamente.
    
  - Confirmando que a sua fila de mensagens de saída foi limpa de todas as mensagens ofensivos.
    
2. Contate o suporte da Microsoft usando seu canal de contato regular.
    
3. Explique que você tenha um usuário que seja bloqueado para enviar email e que o problema tiver sido resolvido com.
    
4. O agente criará um tíquete de suporte com as informações que você forneça e escalá-lo para configurar o endereço de email ou domínio desbloqueado.
    
5. Depois que o endereço foi desbloqueado e pendentes sem outros problemas, você será contatado e alertado sobre o desbloqueando.
    
Obrigado por auxiliando conosco controlando indesejadas de email.
  
Exchange Online Protection.
  
\*\*Observação:-não responda a este email conforme ela é enviada de um endereço não monitorado\*\*
  
> [!TIP]
> Você também pode contatar o suporte via as opções documentados em [Ajuda e suporte para EOP](eop/help-and-support-for-eop.md). 
  

