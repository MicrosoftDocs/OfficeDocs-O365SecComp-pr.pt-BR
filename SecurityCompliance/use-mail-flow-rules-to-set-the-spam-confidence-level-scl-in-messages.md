---
title: Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: Você pode criar uma regra de transporte que define o nível de confiança de spam (SCL) de uma mensagem de email. O SCL é que uma medida de uma mensagem como provavelmente é spam. Spam é mensagens de email não solicitadas (e normalmente indesejadas). O serviço age diferentes em uma mensagem, dependendo de sua classificação do SCL. Por exemplo, você talvez queira ignorar spam filtragem de conteúdo de mensagens que são enviadas de pessoas dentro da organização, pois você confia que uma mensagem enviada internamente de um colega não é spam. Você usando regras de transporte para definir o valor SCL de uma mensagem dá maior controle na manipulação de spam.
ms.openlocfilehash: 97b9a62e76efea134af5bb1bb7bd25a98bb466d2
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972273"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens

Você pode criar uma regra de transporte que define o nível de confiança de spam (SCL) de uma mensagem de email. O SCL é que uma medida de uma mensagem como provavelmente é spam. Spam é mensagens de email não solicitadas (e normalmente indesejadas). O serviço age diferentes em uma mensagem, dependendo de sua classificação do SCL. Por exemplo, você talvez queira ignorar spam filtragem de conteúdo de mensagens que são enviadas de pessoas dentro da organização, pois você confia que uma mensagem enviada internamente de um colega não é spam. Você usando regras de transporte para definir o valor SCL de uma mensagem dá maior controle na manipulação de spam. 
  
 **O que você precisa saber antes de começar?**
  
- Tempo estimado para concluir este procedimento: 10 minutos.
    
- Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Regras de transporte" em [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou [permissões de recursos no EOP](eop/feature-permissions-in-eop.md). 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de administração do Exchange**.
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a>Para criar uma regra de transporte que define o SCL de uma mensagem

1. No Centro de administração do Exchange (EAC), escolha o **fluxo de email** \> **regras**.
    
2. Escolha **novo**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e, em seguida, selecione **criar uma nova regra**.
    
3. Especifique um nome para a regra.
    
4. Escolha **mais opções**e, em seguida, em **Aplicar esta regra se**, especifique uma condição que acionará a ação que você vai definir para essa regra (que é para definir o valor SCL).
    
    Por exemplo, você pode definir **o remetente** \> **é interno/externo**e, em seguida, na caixa de diálogo **Selecionar local do remetente** , selecione **dentro da organização**e escolha **okey**.<br/>
    ![Selecione o local do remetente](media/EOP-ETR-SetSCL-1.jpg)
  
5. Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.
  
6. Na caixa de diálogo **especificar SCL** , selecione um dos seguintes valores e escolha **okey**:
    
  - **Filtragem de spam de desvio** - este define o SCL como -1, que significa que a filtragem de conteúdo não será realizado. 
    
  - **0-4** - quando você definir o SCL como um desses valores, a mensagem será passada ao longo para o filtro de conteúdo para processamento adicional. 
    
  - **5, 6** - quando você definir o SCL como um desses valores, a ação especificada de **Spam** nas políticas de filtro de conteúdo aplicáveis serão aplicadas. Por padrão, a ação é para enviar a mensagem para a pasta de lixo eletrônico do destinatário. 
    
  - **7-9** - quando você definir o SCL como um desses valores, a ação especificada de **spam de alta confiabilidade** nas políticas de filtro de conteúdo aplicáveis serão aplicadas. Por padrão, a ação é para enviar a mensagem para a pasta de lixo eletrônico do destinatário. 
    
    Para obter mais informações sobre como configurar suas políticas de filtro de conteúdo, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Para obter mais informações sobre valores SCL no serviço, veja [Spam confidence levels](spam-confidence-levels.md).
    
7. Especificar propriedades adicionais para a regra e escolha **Salvar**.
    
    > [!TIP]
    > Para obter mais informações sobre as propriedades adicionais que você pode selecionar ou especificar para esta regra, consulte [usar o EAC para criar uma regra de transporte](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC). 
  
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se esse procedimento está funcionando corretamente, enviar uma mensagem de email a alguém de dentro de sua organização e verifique se a ação executada na mensagem é conforme o esperado. Por exemplo, se você **definir o nível de confiança de spam (SCL)** para **filtragem de spam de desvio**, em seguida, a mensagem deve ser enviada à caixa de entrada do destinatário especificado. No entanto, se você **definir o nível de confiança de spam (SCL)** **9**e a ação de **spam de alta confiabilidade** para suas políticas de filtro de conteúdo aplicável for mover a mensagem para a pasta Lixo eletrônico, em seguida, a mensagem deve ser enviada para o especificado pasta de lixo eletrônico do destinatário. 
  

