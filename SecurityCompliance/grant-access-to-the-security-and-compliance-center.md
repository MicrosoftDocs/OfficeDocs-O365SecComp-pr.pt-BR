---
title: Conceder aos usuários acesso ao Centro de Conformidade e Segurança do Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Os usuários precisam receber permissões no centro de conformidade & segurança do Office 365 antes de poderem gerenciar qualquer um dos seus recursos de segurança ou conformidade.
ms.openlocfilehash: 7963a8c3db64e83566960abe9298b9a2d636ae53
ms.sourcegitcommit: 6302a43d947a908dd10a8e40550b806f491692fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2019
ms.locfileid: "35645116"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a>Conceder aos usuários acesso ao Centro de Conformidade e Segurança do Office 365

Os usuários precisam receber permissões no centro de conformidade & segurança do Office 365 antes de poderem gerenciar qualquer um dos seus recursos de segurança ou conformidade. Como um administrador global do Office 365 ou membro do grupo de função gerenciamento no centro de conformidade & segurança, você pode conceder essas permissões aos usuários. Os usuários só podem gerenciar os recursos de segurança ou de conformidade para os quais você conceder acesso. 
  
Para obter mais informações sobre as diferentes permissões que você pode dar aos usuários no centro de conformidade & segurança, confira [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Você precisa ser um administrador global do Office 365 ou um membro do grupo de função gerenciamento no centro de conformidade & segurança, para concluir as etapas neste artigo.

- Grupos de função para o centro de conformidade & segurança podem ter nomes semelhantes aos grupos de função no Exchange Online, mas eles não são os mesmos.

- As associações do grupo de funções não são compartilhadas entre o Exchange Online e o centro de conformidade & segurança.

- Permissão de acesso delegado (DAP) parceiros com permissões de administração em nome de (AOBO) não podem acessar o centro de conformidade & segurança.

## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a>Usar o centro de administração do Office 365 para conceder a outro usuário acesso ao centro de conformidade & segurança

1. [Entre no Office 365 e vá para o centro de administração](https://go.microsoft.com/fwlink/p/?LinkId=525275).

2. No centro de administração do Office 365, abra **centros de administração** e clique em **segurança & conformidade**.

3. No centro de conformidade & segurança, acesse **permissões**.

4. Na lista, escolha o grupo de funções ao qual você deseja adicionar o usuário e clique em **Editar** ![ícone](media/O365-MDM-CreatePolicy-EditIcon.gif)de edição.

5. Na página de propriedades do grupo de funções, em **Membros**, clique em](media/ITPro-EAC-AddIcon.gif) **Adicionar**![ícone de adição e selecione o nome do usuário (ou usuários) que você deseja adicionar.

6. Depois de selecionar todos os usuários que você deseja adicionar ao grupo de funções, clique em **Adicionar\> ** e em **OK**.

7. Clique em **Salvar** para salvar as alterações feitas no grupo de funções.

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

1. No centro de conformidade & segurança, acesse **permissões**.

2. Na lista, selecione o grupo de funções para exibir os membros.

3. No lado direito, nos detalhes do grupo de função, você pode exibir os membros do grupo de função.

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a>Usar o PowerShell para conceder a outro usuário acesso ao centro de conformidade de & de segurança

1. [Conecte-se ao PowerShell do centro de conformidade & segurança do Office 365](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Use o comando **Add-RoleGroupMember** para adicionar um usuário à função de Gerenciamento de Organização, conforme mostrado no exemplo a seguir.

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   **Parâmetros**:
  
   - _Identity_ é o grupo de funções ao qual adicionar um membro.

   - _Member_ é a caixa de correio, grupo de segurança universal (USG) ou computador a ser adicionado ao grupo de funções. Você só pode especificar um membro por vez.

Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se você concedeu aos usuários acesso ao centro de conformidade de & de segurança, use o cmdlet **Get-RoleGroupMember** para exibir os membros no grupo de função gerenciamento da organização, conforme mostrado no exemplo a seguir.
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
