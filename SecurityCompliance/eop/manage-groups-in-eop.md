---
title: Gerenciar grupos no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Você pode usar o Proteção do Exchange Online (EOP) para criar grupos habilitados para email para uma organização do Exchange. Você também pode usar o EOP para definir ou atualizar propriedades de grupo que especificam associação, endereços de email e outros aspectos de grupos.
ms.openlocfilehash: db649e4fd955d13e50e96007e8e38fe2c1de5b4d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693291"
---
# <a name="manage-groups-in-eop"></a>Gerenciar grupos no EOP

 Você pode usar o Proteção do Exchange Online (EOP) para criar grupos habilitados para email para uma organização do Exchange. Você também pode usar o EOP para definir ou atualizar propriedades de grupo que especificam associação, endereços de email e outros aspectos de grupos. Você pode criar grupos de distribuição e grupos de segurança, dependendo das suas necessidades. Esses grupos podem ser criados usando o Centro de administração do Exchange (EAC) ou pelo Windows PowerShell remoto. 
  
## <a name="types-of-mail-enabled-groups"></a>Tipos de grupos habilitados para email

Você pode criar dois tipos de grupos para sua organização do Exchange:
  
- [Criar um grupo no EAC](manage-groups-in-eop.md) (também conhecidos como grupos de distribuição) são coleções de usuários de email, como uma equipe ou outro grupo ad hoc, que precisam receber ou enviar emails sobre uma área comum de interesse. Os grupos de distribuição destinam-se exclusivamente à distribuição de mensagens de email. No EOP, um grupo de distribuição refere-se a qualquer grupo habilitado para email, esteja ou não em um contexto de segurança.
    
- [Editar ou remover um grupo no EAC](manage-groups-in-eop.md) (também conhecidos como grupos de segurança) são coleções de usuários de email que precisam de permissões de acesso para funções de Administrador. Por exemplo, talvez você queira fornecer permissões de função de administrador a um grupo específico de usuários para que eles possam definir configurações antispam e antimalware.
    
    > [!NOTE]
    > Por padrão, todos os novos grupos de segurança habilitados para email exigem que todos os remetentes sejam autenticados. Isso evita que remetentes externos enviem mensagens para grupos de segurança habilitados para email. 
  
## <a name="before-you-begin"></a>Antes de você começar

- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Grupos de Distribuição e Grupos de Segurança" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md). 
    
- Lembre-se de que quando estiver criando e gerenciando grupos usando cmdlets do PowerShell remoto, você pode encontrar limitações.
    
- Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis.
    
- Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Conectar-se ao Exchange Online Protection usando o PowerShell Remoto](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="create-a-group-in-the-eac"></a>Criar um grupo no EAC

1. No Centro de administração do Exchange (EAC), vá para **Destinatários** \> **Grupos**.
    
2. Clique em **Novo**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.gif) e em **Grupo de distribuição**, ou em **Grupo de segurança**, dependendo das suas necessidades. Consulte [Tipos de grupos habilitados para email](manage-groups-in-eop.md) para ver a diferença. 
    
3. Na página **Novo grupo de distribuição** ou **Novo grupo de segurança**, preencha os seguintes campos: 
    
  - **Nome para exibição** Digite um nome para exibição que seja exclusivo em sua organização e significativo para usuários do EOP. É necessário fornecer o nome para exibição. 
    
  - **Alias** Digite um alias de grupo de até 64 caracteres que seja exclusivo em sua organização. Os usuários do EOP digitam o alias na linha Para: de uma mensagem de email; então ele é convertido para o nome para exibição do grupo. Se você alterar o alias, o endereço SMTP principal do grupo também será alterado e conterá o novo alias. O alias é obrigatório. 
    
  - **Descrição** Digite uma descrição do grupo de forma que as pessoas saibam qual é a finalidade do grupo. 
    
  - **Proprietários** Por padrão, a pessoa que cria um grupo é o proprietário. Você pode adicionar um proprietário escolhendo **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.gif). Todos os grupos devem ter no mínimo um proprietário.
    
    > [!NOTE]
    > Os proprietários do grupo não precisam ser membros do grupo. 
  
  - **Membros** Use esta seção para adicionar membros e especificar se é necessário obter aprovação para que as pessoas ingressem ou saiam do grupo. Para adicionar membros ao grupo, clique em **Adicionar**![Ícone Adicionar](../media/ITPro-EAC-AddIcon.gif).
    
4. Clique em **OK** para retornar à página original. 
    
5. Quando você tiver terminado, clique em **Salvar** para criar o grupo. O novo grupo deve aparecer na lista de grupos. 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a>Editar ou remover um grupo no EAC

1. No EAC, navegue até **Destinatários** \> **Grupos**.
    
2. Siga um destes procedimentos:
    
  - Para editar um grupo: na lista de grupos, clique no grupo de distribuição ou segurança que você deseja exibir ou alterar e, em seguida, **** ![clique em Editar](../media/ITPro-EAC-EditIcon.gif)ícone de edição. Você pode atualizar configurações gerais, adicionar ou remover proprietários de grupo e adicionar ou remover membros de grupo, conforme necessário.
    
  - Para remover um grupo: Selecione o grupo e clique em **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.gif).
    
3. Ao terminar de fazer as alterações, clique em **Salvar**.
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>Criar, editar ou remover um grupo usando o Windows PowerShell remoto

Esta seção fornece informações sobre a criação de grupos e alterações em suas propriedades usando o Windows PowerShell remoto. Também mostra como remover um grupo existente. 
  
 **Para criar um grupo usando o Windows PowerShell remoto**
  
Este exemplo usa o cmdlet [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) para criar um grupo de distribuição com um alias itadmin e o nome IT Administrators (Administradores de TI). Também adiciona usuários como membros do grupo. 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

Para criar um grupo de segurança em vez de um grupo de distribuição, especifique  `-Type "Security"`. 
  
Para verificar se você criou o grupo Administradores de TI com êxito, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) para exibir informações sobre o novo grupo: 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

Para obter uma lista dos membros no grupo, execute o cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) da seguinte maneira: 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

Para obter uma lista completa de todos os seus grupos, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira: 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 **Para alterar as propriedades de um grupo usando o Windows PowerShell remoto**
  
Use os cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) e [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) para visualizar e alterar propriedades para grupos. Uma das vantagens de usar o PowerShell remoto, em vez do EAC, é a capacidade de alterar as propriedades de vários grupos. 
  
Aqui estão alguns exemplos de uso do Windows PowerShell remoto para alterar as propriedades do grupo.
  
Esse exemplo usa o cmdlet [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) para alterar o endereço SMTP principal (também chamado de endereço de resposta) do grupo de Seattle Employees (Funcionários de Seattle) para sea.employees@contoso.com. 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

Para verificar se você alterou com êxito as propriedades de um grupo, use o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx). Uma vantagem de usar o PowerShell remoto é que você pode exibir várias propriedades de vários grupos. No exemplo anterior, em que o endereço SMTP principal do grupo foi alterado, execute este comando para verificar o novo valor: 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

Este exemplo usa o cmdlet [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) para atualizar todos os membros do grupo de Seattle Employees (Funcionários de Seattle). Use uma vírgula para separar todos os membros. 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

Para obter a lista de todos os membros no grupo de Seattle Employees (Funcionários de Seattle), use o cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) da seguinte maneira: 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 **Para remover um grupo usando o Windows PowerShell remoto**
  
Este exemplo usa o cmdlet [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) para remover um grupo de distribuição chamado IT Administrators (Administradores de TI). 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

Para verificar se o grupo foi removido, execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira e confirme que o grupo (nesse caso "IT Administrators") foi excluído. 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


