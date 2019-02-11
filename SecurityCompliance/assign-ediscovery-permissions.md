---
title: Atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Atribuir as permissões necessárias para executar tarefas relacionadas a descoberta eletrônica usando a segurança &amp; Centro de conformidade.
ms.openlocfilehash: 95f0ed171c37ec84ca8bb8f00e69ab0318cd31cd
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29741154"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade

Se quiser que as pessoas usem qualquer uma das ferramentas relacionadas a descoberta eletrônica no Office 365 Security &amp; Centro de conformidade, você precisará atribua as permissões apropriadas. A maneira mais fácil de fazer isso é adicionar a pessoa que o grupo de função adequada na página **permissões** de segurança do Office 365 &amp; Centro de conformidade. Este tópico descreve as permissões necessárias para executar tarefas relacionadas a descoberta eletrônica usando a segurança &amp; Centro de conformidade. 
  
O grupo de funções de relacionados a descoberta eletrônica principal na segurança &amp; Centro de conformidade é chamado de **gerente de descoberta eletrônica**. Existem dois subgrupos dentro desse grupo de função. 
  
- **gerentes de descoberta eletrônica** - uma gerente de descoberta eletrônica pode usar a ferramenta de pesquisa de conteúdo na segurança &amp; Centro de conformidade para locais de conteúdo de pesquisa na organização e executar várias ações relacionados à pesquisa, como visualizar e exportar pesquisa resultados. Membros podem também criar e gerenciar casos do eDiscovery, adicionar e remover membros a um caso, criar pausas maiusculas e executar pesquisas de conteúdo associados a um caso e acesso a dados maiusculas em eDiscovery avançadas do Office 365.  Uma gerentes de descoberta eletrônica só possa acessar e gerenciar os casos em que eles criam. Eles não podem acessar ou gerenciar casos criados por outra gerentes de descoberta eletrônica. 
    
- **Descoberta eletrônica administradores** - uma administrador de descoberta eletrônica é um membro do grupo de função de Gerenciador de descoberta eletrônica e pode executar a mesma pesquisa de conteúdo e as tarefas relacionadas ao gerenciamento de casos que pode ser executadas por uma gerente de descoberta eletrônica. Além disso, um administrador de eDiscovery pode: 
    
  - Acessar todos os casos que estão listados na página **casos de eDiscovery** na segurança &amp; Centro de conformidade. 

  - Acesse os dados maiusculas no eDiscovery avançada para qualquer caso na organização.
    
  - Gerenciar qualquer ocorrência de Descoberta Eletrônica após adicionarem a si mesmos como membro da ocorrência.
  
  Consulte a seção [informações adicionais](#more-information) por motivos por que você pode querer administradores de descoberta eletrônica em sua organização. 

> [!NOTE]
> Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5.  
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de funções de gerenciamento da organização (ou a ser atribuído à função de gerenciamento de função) para atribuir permissões de descoberta eletrônica na segurança &amp; Centro de conformidade.
    
- Você pode usar o cmdlet [Add-RoleGroupMember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) na segurança &amp; PowerShell do Centro de conformidade para adicionar um grupo de segurança habilitados para email como membro do subgrupos de gerentes de descoberta eletrônica no grupo de função de Gerenciador de descoberta eletrônica. No entanto, é possível adicionar um grupo de segurança habilitados para email a subgrupos de administradores de descoberta eletrônica. Consulte a seção de [informações adicionais](#more-information) para obter mais detalhes. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>Atribuir permissões de descoberta eletrônica na segurança &amp; Centro de conformidade

1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **permissões**e clique em caixa de seleção ao lado de **gerente de descoberta eletrônica**.
    
4. Na página **Gerenciador de descoberta eletrônica** submenu, siga um destes procedimentos com base nas permissões de eDiscovery que você deseja atribuir. 
    
  - **Para tornar um usuário de uma gerente de descoberta eletrônica** Ao lado de **eDiscovery Manager**, clique em **Editar**. Em **Selected eDiscovery gerentes**, clique em **Editar**e, em seguida, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Add**. Selecione o usuário (ou usuários) você deseja adicionar como um gerente de descoberta eletrônica e, em seguida, clique em **Adicionar**. Quando você terminar de adicionar usuários, clique em **concluído**. Na página submenu **edição escolha eDiscovery Manager** , clique em **Salvar** para salvar as alterações para a associação do Gerenciador de eDiscovery. 
    
  - **Para tornar um usuário administrador de eDiscovery** Ao lado de **Descoberta eletrônica de administrador**, clique em **Editar**. Em **Selected eDiscovery administradores**, clique em **Editar**e, em seguida, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Add**. Selecione o usuário (ou usuários) você deseja adicionar como uma administrador de descoberta eletrônica e, em seguida, clique em **Adicionar**. Quando você terminar de adicionar usuários, clique em **concluído**. Na página submenu **eDiscovery edição escolha administrador** , clique em **Salvar** para salvar as alterações para a associação de administrador de eDiscovery. 
    
> [!NOTE]
> Você também pode usar o cmdlet **Add-eDiscoveryCaseAdmin** para tornar um usuário administrador de eDiscovery. No entanto, o usuário deve ser atribuído a função de gerenciamento de caso para poder usar esse cmdlet para torná-los uma administrador de descoberta eletrônica. Para obter mais informações, consulte [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Na página **permissões** na segurança &amp; Centro de conformidade, você poderá também atribuir aos usuários permissões relacionadas a descoberta eletrônica, adicionando-os para os grupos de função de administrador de conformidade, gerenciamento da organização e revisor. Para obter uma descrição das funções de RBAC relacionados a descoberta eletrônica atribuídos a cada um desses grupos de função, consulte a seção de [funções RBAC relacionadas à descoberta eletrônica](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>Funções de RBAC relacionadas à descoberta eletrônica

A tabela a seguir lista as funções RBAC relacionados a descoberta eletrônica no Centro de conformidade do & de segurança e indica os grupos de função internos que cada função é atribuída por padrão. 
    
|**Função**|**Administrador de conformidade**|**Administrador de & Gerenciador de descoberta eletrônica**|**Gerenciamento da Organização**|**Revisor**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Gerenciamento de casos <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Pesquisa de Conformidade <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exportar <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Bloqueio <br/>  |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Visualização <br/>  | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Revisão  <br/>  | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|Descriptografia do RMS <br/>  ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Pesquisar e limpar <br/> | <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
As seções a seguir descrevem cada uma das funções RBAC relacionados a descoberta eletrônica listadas na tabela anterior.

### <a name="case-management"></a>Gerenciamento de casos

Essa função permite que os usuários de criar, editar, excluir e controlar o acesso aos casos de eDiscovery in a & de segurança Centro de conformidade. Para obter mais informações, consulte [gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](manage-ediscovery-cases.md). Conforme explicado anteriormente, um usuário deve ser atribuído a função de gerenciamento de caso para poder usar o cmdlet **Add-eDiscoveryCaseAdmin** para torná-los uma administrador de descoberta eletrônica. 

### <a name="compliance-search"></a>Pesquisa de Conformidade

Essa função permite que os usuários executam a ferramenta de pesquisa de conteúdo no Centro de conformidade para pesquisar caixas de correio e pastas públicas, sites do SharePoint Online, OneDrive para sites corporativos, Skype para conversas, grupos do Office 365 e Teams Microsoft Business de & de segurança. Esta função permite que um usuário fazer uma estimativa dos resultados da pesquisa e criar relatórios de exportação, mas funções adicionais são necessários para iniciar as ações de pesquisa de conteúdo, como visualizar, exportar ou excluindo os resultados da pesquisa.

Observe que os usuários atribuídos à função de pesquisa de conformidade, mas não possuem a função de visualização pode visualizar os resultados de uma pesquisa na qual a ação de visualização foi iniciada por um usuário que tenha atribuída a função de visualização. O usuário sem a função de visualização pode visualizar os resultados para até 2 semanas após a ação inicial preview foi criada.

Da mesma forma, os usuários atribuídos à função de pesquisa de conformidade, mas não possui a função pode baixar os resultados de uma pesquisa na qual a ação de exportação tem iniciada por um usuário que tiver atribuído a função de exportação de exportação. O usuário sem a função de exportação pode baixar os resultados de uma pesquisa por até 2 semanas após a ação inicial de exportação foi criada. Depois que eles não poderão baixar os resultados, a menos que alguém com a função de exportação reinicia a exportação.

Para obter mais informações, consulte a [Pesquisa de conteúdo no Office 365](content-search.md). 

### <a name="export"></a>Exportar

A função permite que os usuários exportar os resultados de uma pesquisa de conteúdo para um computador local. Ele também permite que eles preparar os resultados da pesquisa para análise no eDiscovery avançado. 

Para obter mais informações sobre como exportar os resultados da pesquisa, consulte [Exportar resultados da pesquisa do Centro de conformidade do & de segurança do Office 365](export-search-results.md).

### <a name="hold"></a>Bloqueio

Essa função permite que os usuários colocar o conteúdo em caixas de correio, pastas públicas, sites, Skype para conversas de negócios, e os grupos do Office 365 em espera. Quando o conteúdo estiver em espera, os proprietários de conteúdo ainda será possível modificar ou excluir o conteúdo original, mas o conteúdo será preservado até que a suspensão seja removida ou a duração da retenção expira. 

Para obter mais informações sobre isenções, consulte:

- [casos de descoberta eletrônica no Centro de conformidade do & de segurança do Office 365](ediscovery-cases.md) 
- [Visão geral de políticas de retenção](retention-policies.md)

### <a name="preview"></a>Visualização

Essa função permite aos usuários exibir uma lista de itens que foram retornados de uma pesquisa de conteúdo. Eles também poderá abrir e exibir cada item da lista para exibir seu conteúdo.

### <a name="review"></a>Revisão 

Essa função permite que os usuários acessam dados de maiusculas no eDiscovery avançadas do Office 365. A principal finalidade desta função é conceder aos usuários acesso à descoberta eletrônica avançada. Os usuários atribuídos a essa função podem consulte e abra a lista de ocorrências na página de descoberta eletrônica no & de segurança Centro de conformidade que eles são membros de. Depois que o usuário acessa um caso do Centro de conformidade do & de segurança, eles podem clicar **mudança para o eDiscovery avançada** para acessar e analisar os dados de casos de eDiscovery avançado. Essa função não permite que o usuário para visualizar os resultados da pesquisa de conteúdo que está associado o caso ou realizar outras pesquisa de conteúdo ou as tarefas de gerenciamento de casos.

### <a name="rms-decrypt"></a>Descriptografia do RMS

Essa função permite que usuários descriptografar RMS criptografadas mensagens de email quando exportando Pesquisar resultados ou Preparando os resultados da pesquisa para análise no eDiscovery avançado. Para obter mais informações sobre a descriptografia de resultados de pesquisa durante a exportação, consulte [Exportar resultados da pesquisa do Centro de conformidade do & de segurança do Office 365](export-search-results.md).

### <a name="search-and-purge"></a>Pesquisar e limpar

Essa função permite que os usuários a executar em massa de remoção de dados que correspondem aos critérios de uma pesquisa de conteúdo. Para obter mais informações, consulte [Procurar e excluir mensagens de email em sua organização do Office 365](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Mais informações

- **Por que criar uma administrador de descoberta eletrônica?** Como previamente explicado, o administrador é membro do grupo de função Gerenciador de descoberta eletrônica que pode exibir e acessar todos os casos de eDiscovery em sua organização de eDiscovery. Essa capacidade para acessar todos os casos de eDiscovery tem duas finalidades importantes: 
    
  - Se uma pessoa que é o único membro de um caso de eDiscovery sair de sua organização, ninguém (incluindo os membros do grupo de funções de gerenciamento da organização ou outro membro do grupo de função de Gerenciador de descoberta eletrônica) pode acessar essa ocorrência de descoberta eletrônica porque elas não seja um membro de um caso. Nessa situação, não deve haver nenhuma maneira de acessar os dados no caso. Mas como um administrador de eDiscovery pode acessar todos os casos de eDiscovery na organização, eles podem exibir o caso na segurança &amp; Centro de conformidade e adicione sozinhos ou outro gerente de descoberta eletrônica como um membro do caso.
    
  - Como um administrador de eDiscovery pode exibir e acessar todos os casos de eDiscovery, eles podem auditar e acompanhar todos os casos e associada pesquisas de conformidade. Isso pode ajudar a evitar o uso indevido do pesquisas de conformidade ou casos de eDiscovery. E descoberta eletrônica administradores pode acessar informações potencialmente confidenciais nos resultados de uma pesquisa de conformidade, você deve limitar o número de pessoas que são administradores de descoberta eletrônica.
    
    Além disso, o eDiscovery administradores na segurança &amp; Centro de conformidade são automaticamente adicionados como administradores no eDiscovery avançado. Isso significa que uma pessoa deve ser um administrador para executar tarefas administrativas na descoberta eletrônica avançada, como configurar usuários, criando casos e importar dados para um caso de eDiscovery.
    
- **Posso adicionar um grupo como membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade?** Explicado como anteriormente, você pode adicionar um grupo de segurança habilitados para email como membro do subgrupos de gerentes de descoberta eletrônica no grupo de função de Gerenciador de descoberta eletrônica usando o cmdlet **Add-RoleGroupMember** na segurança &amp; PowerShell do Centro de conformidade. Por exemplo, você pode executar o comando a seguir para adicionar um grupo de segurança habilitados para email para o grupo de função de Gerenciador de descoberta eletrônica. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Observe que um grupo de distribuição do Exchange ou um grupo do Office 365 não são suportados. Você deve usar um grupo de segurança habilitados para email, que você pode criar no PowerShell do Exchange Online usando o ` New-DistributionGroup -Type Security ` comando. Você também pode criar um grupo de segurança habilitados para email (e adicionar membros) no Centro de administração do Exchange ou no Centro de administração do Office 365. Observe que poderá levar até 60 minutos após criá-la de um título habilitados para email novo esteja disponível para adicionar ao grupo de função de gerentes de descoberta eletrônica. 
    
    Também conforme anteriormente mencionado, você não pode fazer um título habilitados para email uma administrador de descoberta eletrônica de grupo usando o cmdlet **Add-eDiscoveryCaseAdmin** na segurança &amp; PowerShell do Centro de conformidade. Você só pode adicionar usuários individuais, como os administradores de descoberta eletrônica. 
    
    Observe que você também não é possível adicionar um grupo de segurança habilitados para email como um membro de um caso.
