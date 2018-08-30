---
title: Gerenciar permissões do grupo de funções de administrador no EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: No Microsoft Proteção do Exchange Online (EOP), é possível usar o Centro de administração do Exchange (EAC) para tornar um usuário membro de um grupo ou de grupos de funções a fim de atribuir a ele permissões de execução de tarefas administrativas específicas. Também é possível remover um usuário de um grupo ou grupo de funções usando o EAC.
ms.openlocfilehash: b773b541b85288b4cb4deaa075cc0346d6bcc646
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002970"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a>Gerenciar permissões do grupo de funções de administrador no EOP
  
No Microsoft Proteção do Exchange Online (EOP), é possível usar o Centro de administração do Exchange (EAC) para tornar um usuário membro de um grupo ou de grupos de funções a fim de atribuir a ele permissões de execução de tarefas administrativas específicas. Também é possível remover um usuário de um grupo ou grupo de funções usando o EAC.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Tempo estimado para conclusão: 5 a 10 minutos
    
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e funções de grupo" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md). 
    
- Determinadas permissões no Office 365 mapeiam para as permissões do grupo de funções de administração do EOP. Para obter mais informações, consulte a coluna "Função no Exchange Online" na seção "Para quais serviços minhas permissões do Office 365 se estendem?" em [Atribuição de funções de administração](https://go.microsoft.com/fwlink/p/?LinkId=286708).
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="what-do-you-want-to-do"></a>O que você deseja fazer?

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a>Usar o EAC para atribuir membros a grupos de funções de administração

1. No EAC, navegue até **permissões** \> **Funções de administrador**, clique no grupo de função que você deseja adicionar o usuário ou usuários e, em seguida, clique em **Editar** ![ícone Editar](../media/ITPro-EAC-EditIcon.gif).
    
2. Em Membros, clique em **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.gif). A janela Selecionar Membros será exibida.
    
3. Procure o usuário ou usuários que você deseja adicionar ou selecione-os na lista.
    
4. Depois de selecionar o usuário ou usuários que você deseja adicionar, clique em **Adicionar** e clique em **OK**. A janela Selecionar Membros será fechada.
    
5. Você verá que o usuário foi adicionado ao painel **Membros**. Clique em **Salvar**.
    
    > [!NOTE]
    > Os usuários precisam sair e entrar novamente para ver a alteração em seus diretos administrativos após a adição ou remoção de membros do grupo de funções. 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a>Usar o EAC para remover membros de grupos de funções de administração

1. No EAC, navegue até **permissões** \> **Funções de administrador**, clique no grupo de função que você deseja remover um usuário ou usuários e, em seguida, clique em **Editar** ![ícone Editar](../media/ITPro-EAC-EditIcon.gif).
    
2. Em Membros, selecione o usuário ou usuários que você deseja remover e clique em **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.gif).
    
3. Clique em **Salvar** para salvar a alteração no grupo e retornar à página **Funções de Administração**. Para verificar se você removeu o usuário do grupo de funções de administrador, verifique se o membro não está mais sendo exibido em Membros no painel de detalhes do grupo de funções selecionado. 
    
    > [!NOTE]
    > Os usuários precisam sair e entrar novamente para ver a alteração em seus diretos administrativos após a adição ou remoção de membros do grupo de funções. 
  
## <a name="for-more-information"></a>Para obter mais informações

[Permissões de recurso no EOP](feature-permissions-in-eop.md)
  

