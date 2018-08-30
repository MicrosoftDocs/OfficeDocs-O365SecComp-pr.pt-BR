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
description: Se você quiser Certifique-se que você recebe o email de um remetente específico, pois você confia-los e suas mensagens, você poderá ajustar sua lista de permissões em uma política de filtro de spam no Centro de administração do Exchange.
ms.openlocfilehash: a90679fc900ca5695904898af3627fc1900a8545
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003160"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Criar listas de remetentes confiáveis ou remetentes bloqueados para toda a organização no Office 365
  
Se você quiser Certifique-se que você recebe o email de um remetente específico, pois você confia-los e suas mensagens, você poderá ajustar sua lista de permissões em uma política de filtro de spam no Centro de administração do Exchange (EAC) em **proteção** \> **filtro de Spam**. Saiba mais sobre isso em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Outra opção seria criar uma regra de transporte do Exchange que funciona como o domínio ou baseada em usuário lista de permissões do filtro de spam. Você pode bloquear mensagens enviadas de um determinado domínio ou usuário de maneira semelhante muito.
  
Uma regra de transporte seria útil nessa situação, se você precisar filtro para critérios complexos, como verificar cabeçalhos de mensagem ou os nomes de anexos ou se você deseja adicionar ações complexas, como adicionar um aviso de isenção à mensagem ou a aplicação de um período de tempo em que a regra EA está ativa. No entanto, o método preferencial para certificar-se de emails de um remetente específico ou domínio ignorar o filtro de spam é adicioná-los à sua política de filtro de spam. Introdução a isso no EAC, indo para **proteção** \> **filtro de Spam**. Saiba mais em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
  
> [!TIP]
> Uma lista baseada no domínio em uma regra de transporte não é tão segura como uma lista com base no endereço IP, porque os domínios podem ser falsificados. Além disso, se o endereço IP de envio estiver em uma lista de bloqueios, ele ainda será bloqueado, mesmo se o filtro para o domínio ou o usuário está sendo ignorado. Isso ocorre porque uma regra de transporte em um domínio ou usuário não substitui a lista de bloqueios de IP global. É recomendável usar uma lista com base no endereço IP na maioria dos casos. Para criar uma lista com base no endereço IP, você pode usar a lista de IPS permitidos ou a lista de bloqueios de IP do filtro de conexão. Todas as mensagens enviadas desses endereços IP não são verificadas pelo filtro de conteúdo. Para obter instruções sobre como configurar a política de filtro de conexão, adicionando endereços IP à lista de IPS permitidos ou lista de bloqueios de IP, consulte [Configure a política de filtro de conexão](configure-the-connection-filter-policy.md). 
  
Para conhecer tarefas de gerenciamento adicionais relacionadas a regras de transporte, consulte [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>Usar o EAC para personalizar um bloco ou permitir lista evitar ou recebam email de um domínio ou usuário

1. No EAC, vá para a **proteção** \> **filtro de Spam**. 
    
2. Na página **Geral** , siga um destes procedimentos: 
    
  - Clique duas vezes a política padrão ou uma política existente para iniciar a editá-lo.
    
  - Clique em **novo** para criar uma nova política personalizada de filtro de spam que pode ser aplicada a usuários, grupos e domínios em sua organização. 
    
3. Na página **Permitir listas** , você pode especificar entradas, como remetentes ou domínios, que sempre serão entregues na caixa de entrada. Email dessas entradas não é processado pelo filtro de spam. Faça o seguinte: 
    
  - Adicione a lista de permissões de remetentes confiáveis para o remetente. Clique em **Adicionar**e, em seguida, na caixa de diálogo de seleção, adicione os endereços do remetente que deseja permitir. Você pode separar várias entradas usando um ponto e vírgula ou uma nova linha. Clique em okey para retornar à página **Permitir listas** . 
    
  - Adicione a lista de permissões de domínios confiáveis para o domínio. Clique em **Adicionar**e, em seguida, na caixa de diálogo de seleção, adicione os domínios que você deseja permitir. Você pode separar várias entradas usando um ponto e vírgula ou uma nova linha. Clique em okey para retornar à página **Permitir listas** . 
    
    > [!CAUTION]
    > Se você permitir domínios de nível superior, é provável que emails não desejados sejam entregues na caixa de entrada. 
  
4. Na página **Listas de Bloqueios**, você pode especificar as entradas, como remetentes ou domínios, que sempre serão marcadas como spam. O serviço aplicará a ação de spam de alta confiança configurada nos emails que corresponderem a essas entradas. 
    
  - Adicione remetentes indesejados à lista de Bloqueios de Remetentes. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os endereços dos remetentes que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
  - Adicione domínios indesejados à lista de Bloqueio de domínios. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os domínios que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
    > [!CAUTION]
    > Se você bloquear domínios de primeiro nível, é provável que emails não bloqueados sejam marcados como spam. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-transport-rule"></a>O que você precisa saber antes de começar a criar uma regra de transporte?
    
- Não é necessário criar uma regra de transporte para ignorar a filtragem de spam ou marcará e-mails como spam para um remetente ou domínio. Use o bloco de Exchange Online Protection e listas de permissões em uma política de spam, em vez desta regra de transporte se você deseja simplesmente bloquear ou permitir que um remetente específico ou um domínio e não anexe quaisquer condições extras. Saiba mais sobre isso em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
    
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Regras de transporte" no tópico [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está com problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns no [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [O Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542)ou [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-create-a-transport-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>Usar o EAC para criar uma regra de transporte para ignorar a filtragem de spam para um domínio ou usuário

1. No EAC, navegue até **fluxo de emails** \> **regras**. Escolha **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e escolha **Ignorar a filtragem de spam**.
    
2. Dê um nome à regra. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione uma destas condições: 
    
  - Se você deseja especificar um domínio, escolha o **domínio é**. Na caixa de diálogo **Especificar domínio** , insira o domínio do remetente que deseja designar como seguros, por exemplo, contoso.com. **Adicionar** ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para movê-lo à lista de frases. Repita essa etapa se desejar adicionar domínios adicionais e, em seguida, clique em **Okey** quando terminar. 
    
  - Se quiser especificar um usuário, escolha **é esta pessoa**. Na caixa de diálogo **Selecionar membros**, adicione o usuário à lista ou digite o usuário e clique em **Verificar nomes**. Repita essa etapa se quiser adicionar outros usuários e clique em **OK** quando terminar. 
    
3. Marque a caixa de seleção **Parar o processamento de mais regras** para garantir que nenhuma outra regra pode reverter a ação de desvio 
    
4. Para a opção de **endereço de remetente de correspondência da mensagem** , selecione **cabeçalho ou envelope**.
    
5. Se você quiser, você pode fazer as seleções para a regra de auditoria, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. É recomendável testar a regra por um período de tempo antes de impô-la em sua organização. Para obter mais informações sobre essas seleções, consulte [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).
    
6. Clique em **Salvar** para salvar a regra. 
    
Depois de criar e impor a regra, a filtragem de spam será ignorada para o domínio ou usuário especificado.
  
## <a name="use-the-eac-to-create-a-transport-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>Usar o EAC para criar uma regra de transporte que bloqueia as mensagens enviadas de um domínio ou usuário

1. No EAC, navegue até **fluxo de emails** \> **regras**. Escolha **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e então escolha **criar uma nova regra**.
    
2. Dê um nome à regra e então clique em **Mais opções**. 
    
3. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione uma destas condições: 
    
  - Se você deseja especificar um domínio, escolha o **domínio é**. Na caixa de diálogo Especificar domínio, insira o domínio do remetente do qual você deseja bloquear mensagens, por exemplo, contoso.com. Clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para movê-lo à lista de frases. Repita essa etapa se desejar adicionar domínios adicionais e, em seguida, clique em **Okey** quando terminar. 
    
  - Se quiser especificar um usuário, escolha **é esta pessoa**. Na caixa de diálogo **Selecionar membros**, adicione o usuário à lista ou digite o usuário e clique em **Verificar nomes**. Repita essa etapa se quiser adicionar outros usuários e clique em **OK** quando terminar. 
    
4. Em **Faça o seguinte**, escolha **Bloquear a mensagem** e, em seguida, clique em uma das outras opções, como ** Excluir a mensagem sem notificar ninguém**.
    
5. Clique em **mais opções**e, em seguida, para a opção de **endereço de remetente de correspondência da mensagem** , selecione **cabeçalho ou envelope**.
    
6. Se você quiser, você pode fazer as seleções para a regra de auditoria, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. É recomendável testar a regra por um período de tempo antes de impô-la em sua organização. Para obter mais informações sobre essas seleções, consulte [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).
    
7. Clique em **Salvar** para salvar a regra. 
    
Depois de criar e impor a regra, todas as mensagens enviadas do domínio ou do usuário especificado serão bloqueadas.
  
## <a name="see-also"></a>Confira também

[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Usar regras de transporte para configurar a filtragem de email em massa](use-transport-rules-to-configure-bulk-email-filtering.md)

