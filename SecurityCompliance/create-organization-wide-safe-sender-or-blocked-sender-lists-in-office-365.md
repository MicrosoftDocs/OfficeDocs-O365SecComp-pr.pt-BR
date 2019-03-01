---
title: Criar listas de remetentes confiáveis ou remetentes bloqueados para toda a organização no Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: Se você quiser ter certeza de que recebeu emails de um remetente específico, porque confia neles e suas mensagens, é possível ajustar a lista de permissões em uma política de filtro de spam no centro de administração do Exchange.
ms.openlocfilehash: 0759d054f270cae03b98d9da7e2e2dcfe442d68f
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341592"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Criar listas de remetentes confiáveis ou remetentes bloqueados para toda a organização no Office 365
  
Se você quiser ter certeza de que recebeu emails de um remetente específico, porque confia neles e suas mensagens, é possível ajustar a lista de permissões em uma política de filtro de spam no centro de administração do Exchange (Eat) no **filtro de spam**de **proteção** \> . Saiba mais sobre isso em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Outra opção seria criar uma regra de fluxo de emails do Exchange (também conhecida como regra de transporte) que funciona como o domínio ou a lista de permissões baseada no usuário no filtro de spam. Você pode bloquear mensagens enviadas de um determinado domínio ou usuário de uma forma semelhante.
  
Uma regra de fluxo de emails seria útil nessa situação se você precisar filtrar por critérios complexos, como a verificação de cabeçalhos de mensagens ou os nomes de anexos ou se você quiser adicionar ações complexas, como adicionar um aviso de isenção de responsabilidade à mensagem ou aplicar um período de tempo em que o regra o e está ativo. No enTanto, o método preferencial para garantir que os emails de um remetente ou domínio específico ignorem o filtro de spam é adicioná-los à sua política de filtro de spam. Comece a usar o **filtro de spam**de **proteção** \> . Saiba mais em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
  
> [!TIP]
> Uma lista baseada em domínio em uma regra de fluxo de emails não é tão segura quanto uma lista baseada em endereço IP, pois os domínios podem ser falsificados. Além disso, se o endereço IP de envio estiver em uma lista de bloqueios, ele ainda será bloqueado mesmo se a filtragem do domínio ou do usuário estiver sendo ignorada. Isso ocorre porque uma regra de fluxo de emails em um domínio ou usuário não substitui a lista de bloqueios de IP global. Recomendamos usar uma lista baseada em endereço IP na maioria dos casos. Para criar uma lista baseada em endereço IP, você pode usar a lista de IPs permitidos ou a lista de IPs bloqueados no filtro de conexão. Qualquer mensagem enviada desses endereços IP não é verificada pelo filtro de conteúdo. Para obter instruções sobre como configurar a política de filtro de conexão adicionando endereços IP à lista de IPs permitidos ou à lista de IPs bloqueados, consulte [Configurar a política de filtro de conexão](configure-the-connection-filter-policy.md). 
  
Para tarefas de gerenciamento adicionais relacionadas a regras de fluxo de emails, consulte [regras de fluxo de emails (regras de transporte) no Exchange Online](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>Use o Eat para personalizar uma lista de bloqueio ou de permissão para impedir ou receber emails de um domínio ou usuário

1. No Eat, vá para o **** \> **filtro de spam**de proteção. 
    
2. Na página **geral** , siga um destes procedimentos: 
    
  - Clique duas vezes na política padrão ou em uma política existente para começar a editá-la.
    
  - Clique em **novo** para criar uma nova política personalizada de filtro de spam que possa ser aplicada a usuários, grupos e domínios em sua organização. 
    
3. Na página **permitir listas** , você pode especificar entradas, como remetentes ou domínios, que sempre serão entregues na caixa de entrada. O email dessas entradas não é processado pelo filtro de spam. Faça o seguinte: 
    
  - Adicione remetentes confiáveis à lista de permissões do remetente. Clique em **Adicionar**e, na caixa de diálogo de seleção, adicione os endereços de remetente que você deseja permitir. Você pode separar várias entradas usando um ponto-e-vírgula ou uma nova linha. Clique em OK para retornar à página de **lista de permissões** . 
    
  - Adicione domínios confiáveis à lista de permissões de domínio. Clique em **Adicionar**e, na caixa de diálogo de seleção, adicione os domínios que você deseja permitir. Você pode separar várias entradas usando um ponto-e-vírgula ou uma nova linha. Clique em OK para retornar à página de **lista de permissões** . 
    
    > [!CAUTION]
    > Se você permitir domínios de nível superior, é provável que emails não desejados sejam entregues na caixa de entrada. 
  
4. Na página **Listas de Bloqueios**, você pode especificar as entradas, como remetentes ou domínios, que sempre serão marcadas como spam. O serviço aplicará a ação de spam de alta confiança configurada nos emails que corresponderem a essas entradas. 
    
  - Adicione remetentes indesejados à lista de Bloqueios de Remetentes. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os endereços dos remetentes que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
  - Adicione domínios indesejados à lista de Bloqueio de domínios. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os domínios que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
    > [!CAUTION]
    > Se você bloquear domínios de primeiro nível, é provável que emails não bloqueados sejam marcados como spam. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-mail-flow-rule"></a>O que você precisa saber antes de começar a criar uma regra de fluxo de emails?
    
- Você não precisa criar uma regra de fluxo de emails para ignorar a filtragem de spam ou marcar email como spam para um remetente ou domínio. Use as listas de permissões e bloqueio de proteção do Exchange Online em uma política de spam, em vez desta regra de fluxo de emails, se você simplesmente deseja bloquear ou permitir um remetente ou domínio específico e não anexar nenhuma condição extra. Saiba mais sobre isso em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
    
- Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o entrada "regras de fluxo de emails" no tópico [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) . 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está com problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns no [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), no [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542)ou no [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>Use o Eat para criar uma regra de fluxo de emails para ignorar a filtragem de spam para um domínio ou usuário

1. No Eat, navegue até **regras**de **fluxo** \> de emails. Escolha **Adicionar** ![ícone](media/ITPro-EAC-AddIcon.gif) de adição e escolha **ignorar filtragem de spam**.
    
2. Dê um nome à regra. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione uma destas condições: 
    
  - Se você quiser especificar um domínio, escolha **domínio é**. Na caixa de diálogo **especificar domínio** , digite o domínio do remetente que você deseja designar como seguro, como contoso.com. **Adicionar** ![Adicionar ícone](media/ITPro-EAC-AddIcon.gif) para movê-lo para a lista de frases. Repita essa etapa se quiser adicionar mais domínios e clique em **OK** quando terminar. 
    
  - Se quiser especificar um usuário, escolha **é esta pessoa**. Na caixa de diálogo **Selecionar membros**, adicione o usuário à lista ou digite o usuário e clique em **Verificar nomes**. Repita essa etapa se quiser adicionar outros usuários e clique em **OK** quando terminar. 
    
3. Marque a caixa de seleção **parar de processar mais regras** para garantir que nenhuma outra regra possa reverter a ação bypass 
    
4. Para a opção **corresponder endereço do remetente na mensagem** , selecione **cabeçalho ou envelope**.
    
5. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções.
    
6. Clique em **Salvar** para salvar a regra. 
    
Depois de criar e impor a regra, a filtragem de spam será ignorada para o domínio ou usuário especificado.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>Use o Eat para criar uma regra de fluxo de emails que bloqueie as mensagens enviadas de um domínio ou usuário

1. No Eat, navegue até **regras**de **fluxo** \> de emails. Escolha **Adicionar** ![ícone](media/ITPro-EAC-AddIcon.gif) de adição e, em seguida, escolha **criar uma nova regra**.
    
2. Dê um nome à regra e então clique em **Mais opções**. 
    
3. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione uma destas condições: 
    
  - Se você quiser especificar um domínio, escolha **domínio é**. Na caixa de diálogo especificar domínio, digite o domínio do remetente a partir do qual você deseja bloquear mensagens, como contoso.com. Clique em **Adicionar** ![ícone](media/ITPro-EAC-AddIcon.gif) de adição para movê-lo para a lista de frases. Repita essa etapa se quiser adicionar mais domínios e clique em **OK** quando terminar. 
    
  - Se quiser especificar um usuário, escolha **é esta pessoa**. Na caixa de diálogo **Selecionar membros**, adicione o usuário à lista ou digite o usuário e clique em **Verificar nomes**. Repita essa etapa se quiser adicionar outros usuários e clique em **OK** quando terminar. 
    
4. Em **Faça o seguinte**, escolha **Bloquear a mensagem** e, em seguida, clique em uma das outras opções, como ** Excluir a mensagem sem notificar ninguém**.
    
5. Clique em **mais opções**e, em seguida, para a opção **corresponder endereço do remetente na mensagem** , selecione **cabeçalho ou envelope**.
    
6. Se quiser, você pode fazer seleções para auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. Recomendamos testar a regra por um período de tempo antes de forçá-la em sua organização.
    
7. Clique em **Salvar** para salvar a regra. 
    
Depois de criar e impor a regra, todas as mensagens enviadas do domínio ou do usuário especificado serão bloqueadas.
  
## <a name="see-also"></a>Confira também

[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Usar regras de fluxo de email para configurar a filtragem de email em massa](use-transport-rules-to-configure-bulk-email-filtering.md)

