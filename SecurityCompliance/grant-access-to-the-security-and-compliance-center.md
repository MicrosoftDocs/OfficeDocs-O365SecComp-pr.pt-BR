---
title: Fornecer acesso aos usuários para a segurança do Office 365 &amp; Centro de conformidade
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Os usuários precisam ter permissões de segurança do Office 365 &amp; Centro de conformidade antes que eles possam gerenciar qualquer um dos seus recursos de segurança ou conformidade.
ms.openlocfilehash: 976c4e21351e352672f3075d0f713e63a634ce42
ms.sourcegitcommit: da4aa7335b577148ecd61e09bbb11039b817b287
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2018
ms.locfileid: "26539103"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Fornecer acesso aos usuários para a segurança do Office 365 &amp; Centro de conformidade

Os usuários precisam ter permissões de segurança do Office 365 &amp; Centro de conformidade antes que eles possam gerenciar qualquer um dos seus recursos de segurança ou conformidade. Como um administrador global do Office 365 ou um membro do grupo de função OrganizationManagement na segurança &amp; Centro de conformidade, você pode conceder essas permissões aos usuários. Os usuários somente poderão gerenciar os recursos de segurança ou conformidade que você conceda acesso a. 
  
Para obter mais informações sobre as permissões diferentes, você pode conceder aos usuários na segurança &amp; Centro de conformidade, check-out [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Você precisa ser um administrador global do Office 365 ou um membro do grupo de funções OrganizationManagement na segurança &amp; Centro de conformidade, conclua as etapas neste artigo.
    
- Grupos de função para a segurança &amp; Centro de conformidade podem ter nomes semelhantes aos grupos de função no Exchange Online, mas eles não são os mesmos. 
    
- Associações de grupo de função não são compartilhadas entre o Exchange Online e a segurança &amp; Centro de conformidade.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Use o Centro de administração do Office 365 para fornecer outro acesso de usuário de segurança &amp; Centro de conformidade

1. [Entrar no Office 365 e vá para o Centro de administração](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
2. No Centro de administração do Office 365, abra a **centrais de administração** e clique **segurança &amp; conformidade**. 
    
3. Na segurança &amp; Centro de conformidade, vá para **permissões**.
    
4. Na lista, escolha o grupo de função que você deseja adicionar o usuário e clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
5. Na página de propriedades do grupo de funções em **membros**, clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione o nome do usuário (ou usuários) para o qual você deseja adicionar. 
    
6. Quando você tiver selecionado todos os usuários que você deseja adicionar ao grupo de funções, clique em **Adicionar-\> ** e **Okey**.
    
7. Clique em **Salvar** para salvar as alterações feitas no grupo de funções. 
    
### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

1. Na segurança &amp; Centro de conformidade, vá para **permissões**.
    
2. Na lista, selecione o grupo de funções para exibir os membros.
    
3. À direita, nos detalhes do grupo de função, você pode exibir os membros do grupo de função.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Use o PowerShell para fornecer outro acesso de usuário de segurança &amp; Centro de conformidade

1. [Conectar-se a segurança do Office 365 & PowerShell do Centro de conformidade](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).
    
2. Use o comando **Add-RoleGroupMember** para adicionar um usuário à função de Gerenciamento de Organização, conforme mostrado no exemplo a seguir. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Parâmetros**
  
-  _-Identity_ é o grupo de funções ao qual adicionar um membro. 
    
- - _Membro_ é a caixa de correio, o grupo de segurança universal (USG) ou computador para adicionar ao grupo de funções. Você pode especificar somente um membro ao mesmo tempo. 
    
Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar que você tiver concedido aos usuários acesso à segurança &amp; Centro de conformidade, use o cmdlet **Get-RoleGroupMember** para exibir os membros no grupo de função de gerenciamento da organização, conforme mostrado no exemplo a seguir. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  

