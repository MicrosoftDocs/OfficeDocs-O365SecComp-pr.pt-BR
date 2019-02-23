---
title: Configurar a política de spam de saída
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados.
ms.openlocfilehash: 095098c058a5ca5165e0ad24ef48296c980eadcf
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214521"
---
# <a name="configure-the-outbound-spam-policy"></a>Configurar a política de spam de saída

A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados. Semelhante a filtragem de entrada, a filtragem de spam de saída é composta de filtragem de conexão e de conteúdo, porém, as configurações do filtro de saída não são configuráveis. Se uma mensagem de saída é considerada spam, ela é roteada através do pool de entrega de risco mais alto, que reduz a probabilidade do pool de IP de saída normal estar sendo adicionado a uma lista de bloqueio. Se um cliente continua a enviar spam de saída através do serviço, será impedido de enviar mensagens. Embora a filtragem de spam de saída não possa ser desabilitada nem modificada, você pode configurar várias configurações de spam de saída para toda a empresa por meio da política padrão de spam de saída. 
  
O vídeo a seguir mostra como configurar a política de spam de saída:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o tópico "entrada antispam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de administração do Exchange**.
  
O procedimento a seguir também pode ser executado por meio do PowerShell remoto. Use o cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) para revisar suas configurações e o [set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) para editar suas configurações de política de spam de saída. Para saber como usar o Windows PowerShell para se conectar à proteção do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a>Utilize o EAC para editar a política de spam de saída padrão
<a name="sectionSection1"> </a>

Utilize o procedimento a seguir para editar a política de spam de saída padrão.
  
### <a name="to-configure-the-default-outbound-spam-policy"></a>Para configurar a política de spam de saída padrão.

1. No centro de administração do Exchange (EAC), navegue até **Proteção** \> **Spam de saída**, e, em seguida clique duas vezes em política padrão.
    
2. Selecione a opção de menu **Preferências de saída de spam**. 
    
3. Marque as seguintes caixas de seleção referentes às mensagens de saída e, em seguida, especifique um endereço de email associado ou endereços na caixa de entrada associada (elas podem ser listas de distribuição se forem resolvidas como destinos SMTP válidos):
    
1. Envie uma cópia de todas as mensagens suspeitas de email de saída para **o(s) seguinte(s) endereço(s) de email**. Estas são as mensagens que são marcadas como spam pelo filtro (independentemente da classificação de SCL) Elas não são rejeitadas pelo filtro, mas são roteadas pelo pool de entrega de risco mais alto. Separe com ponto e vírgula os diversos endereços. Observe que os destinatários especificados receberão as mensagens como um endereço com cópia oculta (Bcc) (os campos De e Para são o remetente e o destinatário originais).
    
2. Envie uma notificação para o seguinte endereço de email quando um remetente for bloqueado por enviar **spam de saída**. Separe com ponto e vírgula os diversos endereços.
    
    Quando uma quantidade significativa de spam é originada de um usuário específico, o usuário está desabilitado no envio de mensagens de email. O administrador do domínio, que é especificado usando essa configuração, será informado de que as mensagens de saída serão bloqueadas para este usuário. Para ver a aparência dessa notificação, confira [exemplo de notificação quando um remetente estiver bloqueado enviando spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Para obter informações sobre como habilitar novamente, consulte [removendo um usuário, domínio ou endereço IP de uma lista de bloqueios após o envio de email de spam](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).
    
4. Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.
    
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection2"> </a>

[Pool de entrega de alto risco para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)
  
[PERGUNTAS FREQUENTEs sobre proteção antispam](anti-spam-protection-faq.md)
  

