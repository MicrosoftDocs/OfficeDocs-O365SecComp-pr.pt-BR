---
title: Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: A ação antispam padrão para os clientes do EOP é mover as mensagens de spam para a pasta lixo eletrônico dos destinatários. Para que essa ação funcione com caixas de correio locais, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou Hub no local para detectar cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover o spam para a pasta lixo eletrônico de cada caixa de correio.
ms.openlocfilehash: d0ae9637ce95a1a8f0d4d241b3aef928c84ba3fa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221021"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário

> [!IMPORTANT]
> Este tópico aplica-se apenas aos clientes do proteção do Exchange Online (EOP) que hospedam caixas de correio no local em uma implantação híbrida. Os clientes do Exchange Online cujas caixas de correio são totalmente hospedadas no Office 365 não precisam executar esses comandos. 
  
A ação antispam padrão para os clientes do EOP é mover as mensagens de spam para a pasta lixo eletrônico dos destinatários. Para que essa ação funcione com caixas de correio locais, você deve configurar as regras de transporte do Exchange em seus servidores de borda ou Hub no local para detectar cabeçalhos de spam adicionados pelo EOP. Essas regras de transporte definem o nível de confiança de spam (SCL) usado pela propriedade SclJunkThreshold do cmdlet Set-OrganizationConfig para mover o spam para a pasta lixo eletrônico de cada caixa de correio. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Para adicionar regras de transporte para garantir que o spam seja movido para a pasta lixo eletrônico usando o Windows PowerShell

1. Acessar o Shell de gerenciamento do Exchange para o Exchange Server local. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização local do Exchange, confira **abrir o Shell**.
    
2. Execute o seguinte comando para encaminhar mensagens de spam filtradas por conteúdo para a pasta Lixo Eletrônico:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkContentFilteredMail. 
    
3. Execute o seguinte comando para encaminhar mensagens marcadas como spam, antes da aplicação do filtro de conteúdo, para a pasta Lixo Eletrônico:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkMailBeforeReachingContentFilter. 
    
4. Execute o seguinte comando para garantir que as mensagens de remetentes em uma lista de bloqueios na política de filtro de spam, como a lista de bloqueios de **remetente** , sejam encaminhadas para a pasta lixo eletrônico: 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Em que _NameForRule_ é o nome da nova regra, por exemplo, JunkMailInSenderBlockList. 
    
Se você não quiser usar a ação **mover mensagem para a pasta lixo eletrônico** , você pode escolher outra ação em suas políticas de filtro de conteúdo no centro de administração do Exchange. Para obter mais informações, consulte [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Para obter mais informações sobre esses campos no cabeçalho da mensagem, consulte [anti-spam Message Headers](anti-spam-message-headers.md).
  
## <a name="see-also"></a>Confira também

[Cmdlet New-TransportRule](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

