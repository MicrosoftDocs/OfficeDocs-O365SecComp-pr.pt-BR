---
title: Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: Os administradores podem aprender a definir o SCL de mensagens na proteção do Exchange Online.
ms.openlocfilehash: 48569087fe8455dbb5500add435430ec8e78ea30
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341342"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>Usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens

Você pode criar uma regra de fluxo de emails (também conhecida como regra de transporte) que define o nível de confiança de spam (SCL) de uma mensagem de email. O SCL é uma medida da probabilidade de uma mensagem ser spam. Spams são mensagens de email não solicitadas (e normalmente indesejadas). O serviço executa ações diferentes em uma mensagem, dependendo da classificação de SCL. Por exemplo, talvez você queira ignorar a filtragem de conteúdo de spam para mensagens enviadas de pessoas dentro da sua organização, pois você confia que uma mensagem enviada internamente por um colega não é spam. O uso de regras de fluxo de email para definir o valor de SCL de uma mensagem lhe dá maior controle no tratamento de spam. 
  
 **O que você precisa saber antes de começar?**
  
- Tempo estimado para concluir este procedimento: 10 minutos.
    
- Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o entrada "regras de fluxo de email" em [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou [permissões de recurso no EOP](eop/feature-permissions-in-eop.md). 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de administração do Exchange**.
    
### <a name="to-create-a-mail-flow-rule-that-sets-the-scl-of-a-message"></a>Para criar uma regra de fluxo de emails que define o SCL de uma mensagem

1. No centro de administração do Exchange (Eat), escolha **regras**de **fluxo** \> de emails.
    
2. Escolha **novo**![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, em seguida, selecione **criar uma nova regra**.
    
3. Especifique um nome para a regra.
    
4. Escolha **mais opções**e, em **aplicar esta regra se**, especifique uma condição que disparará a ação que será definida para esta regra (que é definir o valor de SCL).
    
    Por exemplo, você pode definir que **o remetente** \> **é interno/externo**e, em seguida, na caixa de diálogo **selecionar local do remetente** , selecione **dentro da organização**e escolha **OK**.<br/>
    ![Selecione o local do remetente](media/EOP-ETR-SetSCL-1.jpg)
  
5. Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.
  
6. Na caixa de diálogo **especificar SCL** , selecione um dos seguintes valores e escolha **OK**:
    
  - **Ignorar filtragem de spam** : define o SCL como-1, o que significa que a filtragem de conteúdo não será executada. 
    
  - **0-4** -quando você definir o SCL como um desses valores, a mensagem será passada para o filtro de conteúdo para processamento adicional. 
    
  - **5, 6** -quando você definir o SCL como um desses valores, a ação especificada para **spam** nas políticas de filtro de conteúdo aplicáveis será aplicada. Por padrão, a ação é enviar a mensagem para a pasta lixo eletrônico do destinatário. 
    
  - **7-9** -quando você definir o SCL como um desses valores, a ação especificada para **spam de alta confiança** nas políticas de filtro de conteúdo aplicáveis será aplicada. Por padrão, a ação é enviar a mensagem para a pasta lixo eletrônico do destinatário. 
    
    Para obter mais informações sobre como configurar suas políticas de filtro de conteúdo, consulte [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Para obter mais informações sobre os valores de SCL no serviço, consulte [níveis de confiança de spam](spam-confidence-levels.md).
    
7. Especifique propriedades adicionais para a regra e escolha **salvar**.
    
    > [!TIP]
    > Para obter mais informações sobre as propriedades adicionais que você pode selecionar ou especificar para esta regra, consulte [usar o Eat para criar regras de fluxo de email](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules). 
  
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se esse procedimento está funcionando corretamente, envie uma mensagem de email para alguém dentro da sua organização e verifique se a ação executada na mensagem é conforme o esperado. Por exemplo, se você **definir o nível de confiança de spam (SCL)** para **ignorar a filtragem de spam**, a mensagem deverá ser enviada para a caixa de entrada do destinatário especificado. No enTanto, se você **definir o nível de confiança de spam (SCL)** como **9**e a ação de **spam de alta confiança** para suas políticas de filtro de conteúdo aplicáveis for mover a mensagem para a pasta lixo eletrônico, a mensagem deverá ser enviada para o especificado pasta lixo eletrônico do destinatário. 
  

