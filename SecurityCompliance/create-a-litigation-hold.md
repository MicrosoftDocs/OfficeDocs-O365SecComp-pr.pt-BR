---
title: Criar um litígio no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037954"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Criar um litígio no Office 365

Você pode colocar uma caixa de correio em retenção de litígio para reter todo o conteúdo de caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Quando você realiza uma caixa de correio do usuário na retenção de litígio, conteúdo, na caixa de correio de arquivo morto do usuário (se ele estiver habilitado) também é mantido. Quando você cria uma pausa, você pode especificar uma duração de espera (também chamada de uma *baseadas em tempo de espera*) para que excluído e itens modificados são mantidos por um período especificado e excluídos permanentemente da caixa de correio. Ou você pode apenas reter conteúdo indefinidamente (chamado uma *espera infinita*) ou até que a retenção de litígio foi removida. Se você especificar uma período de duração de espera, ele é calculado a partir da data de uma mensagem é recebida ou um item de caixa de correio é criado. 
  
Aqui está o que acontece quando você cria um litígio.
  
- Itens que são excluídos permanentemente pelo usuário são mantidos na pasta itens recuperáveis na caixa de correio do usuário para a duração da retenção.
    
- Itens que são removidos da pasta itens recuperáveis pelo usuário são retidos para a duração da retenção.
    
- A cota de armazenamento para a pasta itens recuperáveis é aumentada de 30 GB para 110 GB.
    
- Itens em primário do usuário e as caixas de correio de arquivo morto são mantidos
    
## <a name="before-you-begin"></a>Antes de começar

- Para colocar uma caixa de correio do Exchange Online em litígio, ele deve ser atribuído a uma licença do Exchange Online plano 2. Se uma caixa de correio for atribuída a uma licença do Exchange Online plano 1, você teria atribuí-lo de uma licença separada de arquivamento do Exchange Online para colocá-la em espera.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Colocar uma caixa de correio em retenção de litígio no Centro de administração do Office 365

Aqui estão as etapas para colocar um maibox em retenção de litígio usando o Centro de administração do Office 365.

1. Vá para https://portal.office.com/adminportal/home e entrar usando sua conta de administrador global.
2. Clique em **usuários** > **usuários ativos** no painel de navegação à esquerda.
3. Selecione o usuário cuja caixa de correio que você deseja colocar em retenção de litígio.
4. Na página dinamicamente-out, clique em **configurações de email**e clique em **Editar** ao lado de **litígio**.
5. Na página de **litígio** , clique na alternância para ativar litígio e concluir as seguintes configurações opcionais que são exibidas:
 
    ![O365_LitigationHold1.PNG](media/O365-LitigationHold1.png)

    r. **duração da retenção (dias)** -Use esta caixa para criar uma pausa baseadas em tempo e especifique por quanto tempo os itens de caixa de correio são mantidos quando a caixa de correio for colocada em retenção de litígio. A duração é calculada a partir da data de um item de caixa de correio é recebido ou criado. Se você deixar essa caixa em branco, os itens são mantidos indefinidamente ou até que a suspensão seja removida. Use dias para especificar a duração.
    
    b. **Nota** - Use esta caixa para informar ao usuário suas caixas de correio está em retenção de litígio. A nota será exibida na página informações da conta na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior. Para acessar esta página, os usuários podem clicar o **arquivo** no Outlook.
     
    c. a **página da Web** - Use esta caixa para direcionar o usuário para um site para obter mais informações sobre retenção de litígio. Essa URL aparece na página informações da conta na caixa de correio do usuário, se estiver usando o Outlook 2010 ou posterior. Para acessar esta página, os usuários podem clicar o **arquivo** no Outlook.
 
6. Clique em **Salvar** para criar o litígio.

Depois de criar a retenção, as configurações de email na página dinamicamente-out mostra que litígio esteja ativado para o usuário selecionado.

![O365_LitigationHold2.PNG](media/O365-LitigationHold2.png)

Para obter mais informações sobre como criar e gerenciar retenções de litígio e usando o PowerShell do Exchange Online para criação em massa litígio contém, consulte [colocar uma caixa de correio em retenção de litígio](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).
