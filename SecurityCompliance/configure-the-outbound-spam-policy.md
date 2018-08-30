---
title: Configurar a política de spam de saída
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
description: A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados.
ms.openlocfilehash: b6185cfded28613cb5a512882aefb1a99db158db
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002397"
---
# <a name="configure-the-outbound-spam-policy"></a>Configurar a política de spam de saída

A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados. Semelhante a filtragem de entrada, a filtragem de spam de saída é composta de filtragem de conexão e de conteúdo, porém, as configurações do filtro de saída não são configuráveis. Se uma mensagem de saída é considerada spam, ela é roteada através do pool de entrega de risco mais alto, que reduz a probabilidade do pool de IP de saída normal estar sendo adicionado a uma lista de bloqueio. Se um cliente continua a enviar spam de saída através do serviço, será impedido de enviar mensagens. Embora a filtragem de spam de saída não possa ser desabilitada nem modificada, você pode configurar várias configurações de spam de saída para toda a empresa por meio da política padrão de spam de saída. 
  
O vídeo a seguir mostra como configurar a política de spam de saída:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a "entrada de antispam no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
  
O procedimento a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) para examinar suas configurações e o [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) para editar as configurações de política de spam de saída. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a>Utilize o EAC para editar a política de spam de saída padrão
<a name="sectionSection1"> </a>

Utilize o procedimento a seguir para editar a política de spam de saída padrão.
  
### <a name="to-configure-the-default-outbound-spam-policy"></a>Para configurar a política de spam de saída padrão.

1. No centro de administração do Exchange (EAC), navegue até **Proteção** \> **Spam de saída**, e, em seguida clique duas vezes em política padrão.
    
2. Selecione a opção de menu **Preferências de saída de spam**. 
    
3. Marque as seguintes caixas de seleção referentes às mensagens de saída e, em seguida, especifique um endereço de email associado ou endereços na caixa de entrada associada (elas podem ser listas de distribuição se forem resolvidas como destinos SMTP válidos):
    
1. Envie uma cópia de todas as mensagens suspeitas de email de saída para **o(s) seguinte(s) endereço(s) de email**. Estas são as mensagens que são marcadas como spam pelo filtro (independentemente da classificação de SCL) Elas não são rejeitadas pelo filtro, mas são roteadas pelo pool de entrega de risco mais alto. Separe com ponto e vírgula os diversos endereços. Observe que os destinatários especificados receberão as mensagens como um endereço com cópia oculta (Bcc) (os campos De e Para são o remetente e o destinatário originais).
    
2. Envie uma notificação para o seguinte endereço de email quando um remetente for bloqueado por enviar **spam de saída**. Separe com ponto e vírgula os diversos endereços.
    
    Quando uma quantidade significativa de spam é provenientes de um usuário específico, o usuário está desabilitado enviem mensagens de email. O administrador do domínio, que é especificado usando essa configuração, será informado que mensagens de saída são bloqueadas para esse usuário. Para ver qual essa notificação aparência, consulte [notificação de amostra quando um remetente for bloqueado enviem spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Para obter informações sobre a obtenção reabilitado, consulte [Remover um usuário, o domínio ou o endereço IP a partir de uma lista de bloqueios após o envio de mensagens de spam](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).
    
4. Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.
    
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection2"> </a>

[Pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)
  
[Perguntas frequentes sobre a proteção antispam](anti-spam-protection-faq.md)
  

