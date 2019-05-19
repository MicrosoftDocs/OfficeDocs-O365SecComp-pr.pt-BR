---
title: Gerenciar um site de equipe do SharePoint Online isolado
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: 'Resumo: Gerencie seu site de equipe do SharePoint Online isolado com estes procedimentos.'
ms.openlocfilehash: 1670c806c799cdbd9ffa6d3c45568a3342b88815
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155813"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a>Gerenciar um site de equipe do SharePoint Online isolado

 **Resumo:** Gerencie seu site de equipe do SharePoint Online isolado com estes procedimentos.
  
Este artigo descreve as operações de gerenciamento comuns para um site de equipe do SharePoint Online isolado.
  
## <a name="add-a-new-user"></a>Adicionar um novo usuário

Quando alguém novo ingressar no site, você deverá decidir o nível de participação no site:
  
- Administração: adicionar a nova conta de usuário ao grupo de acesso de administradores de site
    
- Colaboração ativa: adicionar a conta de usuário ao grupo de acesso de membros do site
    
- Exibindo: adicionar a conta de usuário ao grupo de acesso de visualizadores de sites
    
Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server Active Directory (AD), adicione os usuários apropriados aos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Assinatura do Office 365.
  
Se você estiver gerenciando contas de usuário e grupos através do Office 365, poderá usar o centro de administração do Office ou o Microsoft PowerShell:
  
- Para o centro de administração do Office, entre com uma conta de usuário que tenha recebido a função Administrador de conta de usuário ou administrador da empresa e use grupos para adicionar os usuários apropriados aos grupos de acesso apropriados.
    
- Para o PowerShell, primeiro [Conecte-se ao módulo do PowerShell do Azure Active Directory para Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module). Para adicionar uma conta de usuário a um grupo de acesso com seu nome de usuário principal (UPN), use o seguinte bloco de comando do PowerShell:
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> Para um arquivo de texto que contém todos os comandos do PowerShell e uma planilha de configuração do Excel que gera comandos do PowerShell com base em seus nomes de conta de usuário e de grupo, baixe o [Kit de implantação de site de equipe do SharePoint Online isolado](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907). 

Para adicionar uma conta de usuário a um grupo de acesso com seu nome de exibição, use o seguinte bloco de comando do PowerShell:

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a>Adicionar um novo grupo

Para adicionar acesso a um grupo inteiro, você deve decidir o nível de participação de todos os membros do grupo no site:
  
- Administração: Adicionar o grupo ao grupo de acesso de administradores de site
    
- Colaboração ativa: Adicionar o grupo ao grupo de acesso de membros do site
    
- Exibindo: Adicionar o grupo ao grupo de acesso visualizadores de sites
    
Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server AD, adicione os grupos apropriados aos grupos apropriados usando seus procedimentos normais de gerenciamento de usuário e grupo do Windows Server AD e aguarde a sincronização com sua assinatura do Office 365.
  
Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:
  
- Para o centro de administração do Office, entre com uma conta de usuário que tenha recebido a função Administrador de conta de usuário ou administrador da empresa e use grupos para adicionar os grupos apropriados aos grupos de acesso apropriados.
    
- Para o PowerShell, primeiro [Conecte-se ao módulo do PowerShell do Azure Active Directory para Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).
 Em seguida, use os seguintes comandos do PowerShell:
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a>Remover um usuário

Quando o acesso de alguém precisa ser removido do site, você os remove do grupo de acesso para o qual eles são membros atualmente, com base na sua participação no site:
  
- Administração: Remova a conta de usuário do grupo de acesso de administradores de site
    
- Colaboração ativa: Remova a conta de usuário do grupo de acesso de membros do site
    
- Exibição: remover a conta de usuário do grupo de acesso de visualizadores de sites
    
Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server AD, remova os usuários apropriados dos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Office 365 scriçõe.
  
Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:
  
- Para o centro de administração do Office, entre com uma conta de usuário que tenha atribuído a função Administrador de conta de usuário ou administrador da empresa e use grupos para remover os usuários apropriados dos grupos de acesso apropriados.
    
- Para o PowerShell, primeiro [Conecte-se ao módulo do PowerShell do Azure Active Directory para Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).
Para remover uma conta de usuário de um grupo de acesso com seu UPN, use o seguinte bloco de comando do PowerShell:
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

Para remover uma conta de usuário de um grupo de acesso com seu nome de exibição, use o seguinte bloco de comando do PowerShell:
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a>Remover um grupo

Para remover o acesso de um grupo inteiro, remova o grupo do grupo de acesso para o qual eles são membros atualmente com base em sua participação no site:
  
- Administração: remover o grupo do grupo de acesso de administradores de site
    
- Colaboração ativa: remover o grupo do grupo de acesso de membros do site
    
- Exibição: remover o grupo do grupo de acesso de visualizadores de sites
    
Se você estiver gerenciando contas de usuário e grupos por meio do Windows Server Active Directory, remova os grupos apropriados dos grupos de acesso apropriados usando seus procedimentos normais de gerenciamento de usuários e grupos do Windows Server AD e aguarde a sincronização com o seu Assinatura do Office 365.
  
Se estiver gerenciando contas de usuário e grupos através do Office 365, você poderá usar o centro de administração do Office ou o PowerShell:
  
- Para o centro de administração do Office, entre com uma conta de usuário que tenha atribuído a função Administrador de conta de usuário ou administrador da empresa e use grupos para remover os grupos apropriados dos grupos de acesso apropriados.
    
- Para o PowerShell, primeiro [Conecte-se ao módulo do PowerShell do Azure Active Directory para Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).    
Para remover um grupo de um grupo de acesso usando seus nomes de exibição, use o seguinte bloco de comando do PowerShell:
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a>Criar uma subpasta documentos com permissões personalizadas

Em alguns casos, um subconjunto das pessoas que trabalham dentro do site isolado precisa de um local mais privado para colaborar. Para sites do SharePoint Online, você pode criar uma subpasta na pasta documentos do site e atribuir permissões personalizadas. Aqueles sem permissões não verão a subpasta.
  
Para criar uma subpasta documentos com permissões personalizadas, faça o seguinte:
  
1. Entre no Office 365 com uma conta que seja membro do grupo de acesso de administradores para o site. Para obter ajuda, consulte [Onde entrar no Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).
    
2. Vá para o site de equipe isolado e clique em **documentos**.
    
3. Navegue até a pasta na pasta documentos que conterá a subpasta com permissões personalizadas, crie a pasta e, em seguida, abra-a.
    
4. Clique em **Compartilhar**.
    
5. Clique em **compartilhado com o _GT_ avançado**.
    
6. Clique em **parar de herdar permissões**e clique em **OK**.
    
7. Clique em **Compartilhar**.
    
8. Clique em **compartilhado com o _GT_ avançado**.
    
9. Clique em **conceder permissões _GT_ Shared com o _GT_ avançado**.
    
10. Na página permissões, clique em ** \<membros do name> de site na lista**.
    
11. Na página ** \<membros do site name>** , selecione a marca de seleção ao lado do grupo de acesso de membros do site, clique em **ações**, clique em **remover usuários do grupo**e clique em **OK**.
    
12. Para adicionar membros específicos a essa subpasta, clique em **novo _GT_ adicionar usuários**.
    
13. Na caixa de diálogo **compartilhar** , digite os nomes das contas de usuário que podem colaborar em arquivos na subpasta e, em seguida, clique em **compartilhar**.
    
14. Atualize a página da Web para ver os novos resultados.
    
15. Em **grupos** no painel de navegação à esquerda, clique no grupo ** \<visitantes do name> do site** e use as etapas 11-14 para especificar o conjunto de contas de usuário que podem exibir os arquivos na subpasta (conforme necessário).
    
16. Em **grupos** no painel de navegação à esquerda, clique no ** \<grupo proprietários do site name>** e use as etapas 11-14 para especificar o conjunto de contas de usuário que podem administrar as permissões na subpasta (conforme necessário).
    
17. Feche a guia **pessoas e grupos** no navegador.
    
## <a name="see-also"></a>Confira também

[Sites de equipe do SharePoint Online isolados](isolated-sharepoint-online-team-sites.md)
  
[Projetar um site de equipe do SharePoint Online isolado](design-an-isolated-sharepoint-online-team-site.md)

[Implantar um site de equipe do SharePoint Online isolado](deploy-an-isolated-sharepoint-online-team-site.md)



