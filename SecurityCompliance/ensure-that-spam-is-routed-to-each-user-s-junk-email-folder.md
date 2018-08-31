---
title: Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
description: A ação de antispam padrão para clientes do EOP é mover mensagens de spam para a pasta de lixo eletrônico dos destinatários. Para esta ação trabalhar com caixas de correio local, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou de Hub local para detectar os cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover de spam para a pasta Lixo eletrônico de cada caixa de correio.
ms.openlocfilehash: 1b0a9e5ee39820baade714612ca0b0bdb7a81bb9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002850"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário

> [!IMPORTANT]
> Este tópico se aplica somente aos clientes do Exchange Online Protection (EOP) que hospedam as caixas de correio local em uma implantação híbrida. Clientes do Exchange Online cujas caixas de correio são totalmente hospedado no Office 365 não precisará executar esses comandos. 
  
A ação de antispam padrão para clientes do EOP é mover mensagens de spam para a pasta de lixo eletrônico dos destinatários. Para esta ação trabalhar com caixas de correio local, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou de Hub local para detectar os cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover de spam para a pasta Lixo eletrônico de cada caixa de correio. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Para adicionar transporte regras para garantir que spam é movido para a pasta Lixo eletrônico usando o Windows PowerShell

1. Acesse o Shell de gerenciamento do Exchange para seu servidor do Exchange local. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização do Exchange local, consulte **Abrir o Shell**.
    
2. Execute o seguinte comando para encaminhar mensagens de spam filtradas por conteúdo para a pasta Lixo Eletrônico:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkContentFilteredMail. 
    
3. Execute o seguinte comando para encaminhar mensagens marcadas como spam, antes da aplicação do filtro de conteúdo, para a pasta Lixo Eletrônico:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkMailBeforeReachingContentFilter. 
    
4. Execute o seguinte comando para garantir que as mensagens de remetentes em uma lista de bloqueios na política de filtro de spam, como a lista de **bloqueio de remetente** , são roteadas para a pasta Lixo eletrônico: 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Onde _NameForRule_ é o nome para a nova regra, por exemplo, JunkMailInSenderBlockList. 
    
Se você não quiser usar a ação de **mover a mensagem para a pasta Lixo eletrônico** , você pode escolher outra ação em suas políticas de filtro de conteúdo no Centro de administração do Exchange. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Para obter mais informações sobre esses campos no cabeçalho da mensagem, consulte [cabeçalhos de mensagem antispam](anti-spam-message-headers.md).
  
## <a name="see-also"></a>Confira também

[Cmdlet New-TransportRule.](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

