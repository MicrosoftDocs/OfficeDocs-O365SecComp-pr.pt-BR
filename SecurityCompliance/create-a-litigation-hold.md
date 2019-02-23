---
title: Criar uma retenção de litígio no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218651"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Criar uma retenção de litígio no Office 365

Você pode colocar uma caixa de correio em retenção de litígio para reter todo o conteúdo da caixa de correio, incluindo itens excluídos e as versões originais de itens modificados. Quando você coloca uma caixa de correio de usuário em retenção de litígio, o conteúdo da caixa de correio de arquivo morto do usuário (se estiver habilitado) também é mantido. Ao criar uma retenção, você pode especificar uma duração de retenção (também chamada de *retenção baseada em tempo*) para que os itens excluídos e modificados sejam mantidos por um período especificado e, em seguida, excluídos permanentemente da caixa de correio. Ou você pode simplesmente reter o conteúdo indefinidamente (chamado de *retenção infinita*) ou até que a retenção de litígio seja removida. Se você especificar um período de duração de retenção, ele é calculado a partir da data em que uma mensagem é recebida ou de um item de caixa de correio é criado. 
  
Veja o que acontece quando você cria uma retenção de litígio.
  
- Os itens excluídos permanentemente pelo usuário são mantidos na pasta itens recuperáveis na caixa de correio do usuário para a duração da retenção.
    
- Os itens que são removidos da pasta itens recuperáveis pelo usuário são mantidos pela duração da retenção.
    
- A cota de armazenamento da pasta itens recuperáveis aumentou de 30 GB para 110 GB.
    
- Os itens nas caixas de correio principal e de arquivo morto do usuário são mantidos
    
## <a name="before-you-begin"></a>Antes de começar

- Para colocar uma caixa de correio do Exchange Online em retenção de litígio, é necessário atribuir uma licença do Exchange Online Plan 2. Se uma licença do Exchange Online plano 1 for atribuída a uma caixa de correio, você precisará atribuí-la a uma licença de arquivamento do Exchange Online separada para colocá-la em espera.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Colocar uma caixa de correio em retenção de litígio no centro de administração do Office 365

Aqui estão as etapas para colocar um Maibox em retenção de litígio usando o centro de administração do Office 365.

1. AcEsse https://portal.office.com/adminportal/home e entre usando sua conta de administrador global.
2. Clique em usuários**ativos** do painel de navegação à esquerda. **** > 
3. Selecione o usuário cuja caixa de correio você deseja colocar em retenção de litígio.
4. Na página de saída, clique em **configurações de email**e, em seguida, clique em **Editar** ao lado de **retenção de litígio**.
5. Na página **retenção de litígio** , clique no botão de alternância para ativar a retenção de litígio e conclua as seguintes configurações opcionais exibidas:
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    a. **duração da retenção (dias)** : Use esta caixa para criar uma retenção baseada em tempo e especificar quanto tempo os itens de caixa de correio serão mantidos quando a caixa de correio for colocada em retenção de litígio. A duração é calculada a partir da data em que um item de caixa de correio é recebido ou criado. Se você deixar essa caixa em branco, os itens serão mantidos indefinidamente ou até que a retenção seja removida. Use dias para especificar a duração.
    
    b. **Observação** : Use esta caixa para informar ao usuário que a caixa de correio está em retenção de litígio. A nota aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook.
     
    **página da Web** c: Use esta caixa para direcionar o usuário para um site para obter mais informações sobre a retenção de litígio. Essa URL aparecerá na página informações da conta na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. Para acessar essa página, os usuários podem clicar em **arquivo** no Outlook.
 
6. Clique em **salvar** para criar a retenção de litígio.

Após criar a isenção, as configurações de email na página de saída mostrarão que a retenção de litígio está ativada para o usuário selecionado.

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

Para obter mais informações sobre como criar e gerenciar isenções de litígio e usar o PowerShell do Exchange Online para criar uma retenção de litígio em massa, consulte [colocar uma caixa de correio em retenção de litígio](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).
