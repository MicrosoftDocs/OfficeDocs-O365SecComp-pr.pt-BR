---
title: Atribuir permissões de descoberta eletrônica no centro de &amp; conformidade de segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Atribua as permissões necessárias para executar tarefas relacionadas à descoberta eletrônica usando o &amp; centro de conformidade de segurança.
ms.openlocfilehash: 6b79a15c631fce272c350a826ccd6b371a1672b2
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296394"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Atribuir permissões de descoberta eletrônica no centro de &amp; conformidade de segurança do Office 365

Se quiser que as pessoas usem qualquer uma das ferramentas relacionadas à descoberta eletrônica no centro de conformidade &amp; de segurança do Office 365, você precisa atribuir as permissões apropriadas. A maneira mais fácil de fazer isso é adicionar a pessoa o grupo de função apropriado na página **permissões** no centro de conformidade de segurança &amp; do Office 365. Este tópico descreve as permissões necessárias para executar tarefas relacionadas à descoberta eletrônica usando o &amp; centro de conformidade de segurança. 
  
O grupo de função principal relacionado à descoberta eletrônica &amp; no centro de conformidade de segurança é chamado de **Gerenciador de descoberta eletrônica**. Há dois subgrupos dentro desse grupo de funções. 
  
- **gerentes de descoberta** eletrônica: um gerente de descoberta eletrônica pode usar a ferramenta &amp; de pesquisa de conteúdo no centro de conformidade de segurança para pesquisar locais de conteúdo na organização e realizar várias ações relacionadas à pesquisa, como Visualizar e exportar pesquisa resultados. Os membros também podem criar e gerenciar ocorrências de descoberta eletrônica, adicionar e remover membros a uma ocorrência, criar isenções de caso e executar pesquisas de conteúdo associadas a uma ocorrência e acessar dados de ocorrências na descoberta eletrônica avançada do Office 365.  Os gerentes de descoberta eletrônica só podem acessar e gerenciar os casos que criam. Eles não podem acessar ou gerenciar casos criados por outros gerentes de descoberta eletrônica. 
    
- **Administradores** de descoberta eletrônica: um administrador de descoberta eletrônica é um membro do grupo de funções Gerenciador de descoberta eletrônica e pode executar as mesmas tarefas relacionadas ao gerenciamento de casos e pesquisa de conteúdo que um gerente de descoberta eletrônica pode executar. Além disso, um administrador de descoberta eletrônica pode: 
    
  - Acessar todas as ocorrências listadas na página ocorrências de **descoberta eletrônica** no centro de conformidade de segurança &amp; . 

  - Acessar dados de caso na descoberta eletrônica avançada para qualquer caso na organização.
    
  - Gerenciar qualquer ocorrência de Descoberta Eletrônica após adicionarem a si mesmos como membro da ocorrência.
  
  Consulte a seção [mais informações](#more-information) por razões pelas quais você pode querer administradores de descoberta eletrônica em sua organização. 

> [!NOTE]
> Para analisar os dados de um usuário usando a descoberta eletrônica avançada, o usuário (o responsáveis dos dados) deve receber uma licença do Office 365 e5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem receber uma licença autônoma de descoberta eletrônica avançada. Administradores e gerentes de conformidade atribuídos aos casos e usar a descoberta eletrônica avançada para analisar os dados não precisam de uma licença e5.  
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser membro do grupo de função gerenciamento da organização (ou receber a função de gerenciamento de função) para atribuir permissões de descoberta eletrônica no &amp; centro de conformidade de segurança.
    
- Você pode usar o cmdlet [Add-RoleGroupMember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) no PowerShell &amp; do centro de conformidade de segurança para adicionar um grupo de segurança habilitado para email como membro do subgrupo gerenciadores de descoberta eletrônica no grupo de funções Gerenciador de descoberta eletrônica. No enTanto, não é possível adicionar um grupo de segurança habilitado para email ao subgrupo administradores de descoberta eletrônica. Consulte a seção [mais informações](#more-information) para obter mais detalhes. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>Atribuir permissões de descoberta eletrônica no &amp; centro de conformidade de segurança

1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel esquerdo do centro de conformidade &amp; de segurança, clique em **permissões**e, em seguida, clique na caixa de seleção ao lado de **Gerenciador de descoberta eletrônica**.
    
4. Na página do submenu **Gerenciador de descoberta eletrônica** , siga um destes procedimentos com base nas permissões de descoberta eletrônica que você deseja atribuir. 
    
  - **Para tornar um usuário um gerente de descoberta eletrônica** Ao lado de **Gerenciador de descoberta eletrônica**, clique em **Editar**. Em **gerentes de descoberta eletrônica selecionada**, clique em **Editar**e, em seguida, clique em ![adicionar ícone](media/ITPro-EAC-AddIcon.gif) **Adicionar**. Selecione o usuário (ou usuários) que você deseja adicionar como um Gerenciador de descoberta eletrônica e clique em **Adicionar**. Quando terminar de adicionar usuários, clique em **concluído**. Em seguida, na página **edição escolha o Gerenciador de descoberta eletrônica** , clique em **salvar** para salvar as alterações feitas na associação do Gerenciador de descoberta eletrônica. 
    
  - **Para tornar um usuário administrador de descoberta eletrônica** Ao lado de **administrador de descoberta eletrônica**, clique em **Editar**. Em **Administradores de descoberta eletrônica selecionados**, clique em **Editar**e ![, em](media/ITPro-EAC-AddIcon.gif) seguida, clique em Adicionar ícone **Adicionar**. Selecione o usuário (ou usuários) que você deseja adicionar como administrador de descoberta eletrônica e clique em **Adicionar**. Quando terminar de adicionar usuários, clique em **concluído**. Em seguida, na página **edição escolha administrador de descoberta eletrônica** , clique em **salvar** para salvar as alterações feitas na associação do administrador de descoberta eletrônica. 
    
> [!NOTE]
> Você também pode usar o cmdlet **Add-eDiscoveryCaseAdmin** para tornar um usuário um administrador de descoberta eletrônica. No enTanto, o usuário deve ter a função de gerenciamento de casos atribuída para que você possa usar este cmdlet para torná-los um administrador de descoberta eletrônica. Para obter mais informações, consulte [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Na página **permissões** no centro de conformidade &amp; de segurança, você também pode atribuir permissões relacionadas a descoberta eletrônica aos usuários, adicionando-as aos grupos de função Administrador de conformidade, gerenciamento de organização e revisor. Para obter uma descrição das funções RBAC relacionadas à descoberta eletrônica atribuídas a cada um desses grupos de função, consulte a seção [funções RBAC relacionadas a descoberta eletrônica](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>Funções RBAC relacionadas à descoberta eletrônica

A tabela a seguir lista as funções RBAC relacionadas à descoberta eletrônica no centro de conformidade do & de segurança e indica os grupos de função internos aos quais cada função é atribuída por padrão. 
    
|**Função**|**Administrador de conformidade**|**Administrador & do Gerenciador de descoberta eletrônica**|**Gerenciamento da Organização**|**Revisor**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Gerenciamento de casos <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Pesquisa de Conformidade <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exportação <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Bloqueio <br/>  |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Visualização <br/>  | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Revisão  <br/>  | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|DesCriptografia do RMS <br/>  ||![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Pesquisa e limpeza <br/> | <br/> | <br/> |![Marca de seleção](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
As seções a seguir descrevem cada uma das funções RBAC relacionadas à descoberta eletrônica listadas na tabela anterior.

### <a name="case-management"></a>Gerenciamento de casos

Essa função permite que os usuários criem, editem, excluam e controlem o acesso a casos de descoberta eletrônica no centro de conformidade do & de segurança. Para obter mais informações, consulte [gerenciar casos de descoberta eletrônica no centro &amp; de conformidade de segurança do Office 365](manage-ediscovery-cases.md). Como explicado anteriormente, um usuário deve ter a função de gerenciamento de casos atribuída antes que você possa usar o cmdlet **Add-eDiscoveryCaseAdmin** para torná-los um administrador de descoberta eletrônica. 

### <a name="compliance-search"></a>Pesquisa de Conformidade

Essa função permite que os usuários executem a ferramenta de pesquisa de conteúdo no centro de conformidade do & de segurança para pesquisar caixas de correio e pastas públicas, sites do SharePoint Online, sites do OneDrive for Business, conversas do Skype for Business, grupos do Office 365 e Microsoft Teams. Essa função permite que um usuário obtenha uma estimativa dos resultados da pesquisa e crie relatórios de exportação, mas as funções adicionais são necessárias para iniciar as ações de pesquisa de conteúdo, como visualização, exportação ou exclusão de resultados de pesquisa.

Observe que os usuários atribuíam a função de pesquisa de conformidade, mas não têm a função de visualização podem visualizar os resultados de uma pesquisa na qual a ação de visualização tenha sido iniciada por um usuário que foi atribuído à função de visualização. O usuário sem a função Preview pode visualizar os resultados por até 2 semanas após a criação da ação de visualização inicial.

Da mesma forma, os usuários atribuíam a função de pesquisa de conformidade, mas não a função de exportação pode baixar os resultados de uma pesquisa na qual a ação de exportação iniciou por um usuário que foi atribuído à função de exportação. O usuário sem a função de exportação pode baixar os resultados de uma pesquisa por até duas semanas após a criação da ação de exportação inicial. Após isso, não será possível baixar os resultados, a menos que alguém com a função exportar reinicie a exportação.

Para obter mais informações, consulte [pesquisa de conteúdo no Office 365](content-search.md). 

### <a name="export"></a>Exportação

A função permite que os usuários exportem os resultados de uma pesquisa de conteúdo para um computador local. Ele também permite que eles preparam resultados de pesquisa para análise na descoberta eletrônica avançada. 

Para obter mais informações sobre como exportar resultados de pesquisa, consulte [Exportar resultados de pesquisa do centro de conformidade do & de segurança do Office 365](export-search-results.md).

### <a name="hold"></a>Bloqueio

Essa função permite que os usuários coloquem conteúdo em caixas de correio, pastas públicas, sites, conversas do Skype for Business e grupos do Office 365 em espera. Quando o conteúdo estiver em espera, os proprietários do conteúdo ainda poderão modificar ou excluir o conteúdo original, mas o conteúdo será preservado até que a retenção seja removida ou até que a duração da retenção expire. 

Para obter mais informações sobre isenções, consulte:

- [ocorrências de descoberta eletrônica no centro de conformidade do & de segurança do Office 365](ediscovery-cases.md) 
- [Visão geral de políticas de retenção](retention-policies.md)

### <a name="preview"></a>Visualização

Essa função permite que os usuários exibam uma lista de itens que foram retornados de uma pesquisa de conteúdo. Eles também poderão abrir e exibir cada item da lista para exibir seu conteúdo.

### <a name="review"></a>Revisão 

Essa função permite que os usuários acessem os dados de ocorrência na descoberta eletrônica avançada do Office 365. O principal objetivo dessa função é fornecer aos usuários acesso à descoberta eletrônica avançada. Os usuários atribuídos a essa função podem ver e abrir a lista de casos na página descoberta eletrônica no centro de conformidade do & de segurança para os quais eles são membros. Depois que o usuário acessa um caso no centro de conformidade do & de segurança, ele pode clicar em **alternar para descoberta eletrônica avançada** para acessar e analisar os dados do caso na descoberta eletrônica avançada. Essa função não permite que o usuário visualize os resultados de uma pesquisa de conteúdo associada ao caso ou realize outras tarefas de gerenciamento de caso ou de pesquisa de conteúdo.

### <a name="rms-decrypt"></a>DesCriptografia do RMS

Essa função permite que os usuários descriptografem mensagens de email criptografadas por RMS ao exportar resultados de pesquisa ou preparar resultados de pesquisa para análise na descoberta eletrônica avançada. Para obter mais informações sobre como descriptografar resultados de pesquisa durante a exportação, consulte [Exportar resultados de pesquisa do centro de conformidade do & de segurança do Office 365](export-search-results.md).

### <a name="search-and-purge"></a>Pesquisa e limpeza

Essa função permite que os usuários realizem a remoção em massa de dados que correspondam aos critérios de uma pesquisa de conteúdo. Para saber mais, confira [Pesquisar e excluir mensagens de email em sua organização do Office 365](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Mais informações

- **Por que criar um administrador de descoberta eletrônica?** Como explicado anteriormente, um administrador de descoberta eletrônica é membro do grupo de funções Gerenciador de descoberta eletrônica que pode exibir e acessar todos os casos de descoberta eletrônica em sua organização. Essa capacidade de acessar todos os casos de descoberta eletrônica tem duas finalidades importantes: 
    
  - Se uma pessoa que é o único membro de um caso de descoberta eletrônica sair da sua organização, ninguém (incluindo membros do grupo de função gerenciamento da organização ou outro membro do grupo de funções do Gerenciador de descoberta eletrônica) poderá acessar esse caso de descoberta eletrônica, pois eles não são membros de uma ocorrência. Nessa situação, não haveria como acessar os dados no caso. No enTanto, como um administrador de descoberta eletrônica pode acessar todos os casos de descoberta eletrônica na organização, eles &amp; podem ver o caso no centro de conformidade de segurança e adicioná-los ou outro gerenciador de descoberta eletrônica como membro do caso.
    
  - Como um administrador de descoberta eletrônica pode exibir e acessar todos os casos de descoberta eletrônica, eles podem auditar e supervisionar todos os casos e pesquisas de conformidade associadas. Isso pode ajudar a evitar qualquer mau uso de pesquisas de conformidade ou ocorrências de descoberta eletrônica. E como os administradores de eDiscovery podem acessar informações potencialmente confidenciais nos resultados de uma pesquisa de conformidade, você deve limitar o número de pessoas que são administradores de descoberta eletrônica.
    
    Além disso, os administradores de descoberta &amp; eletrônica no centro de conformidade de segurança são automaticamente adicionados como administradores na descoberta eletrônica avançada. Isso significa que uma pessoa deve ser um administrador de descoberta eletrônica para executar tarefas administrativas em descoberta eletrônica avançada, como configurar usuários, criar ocorrências e importar dados em um caso.
    
- **Posso adicionar um grupo como membro do grupo de função Gerenciador de descoberta eletrônica no centro de &amp; conformidade de segurança?** Como explicado anteriormente, você pode adicionar um grupo de segurança habilitado para email como membro do subgrupo gerenciadores de descoberta eletrônica no grupo de função Gerenciador de descoberta eletrônica usando o cmdlet **Add-RoleGroupMember** no PowerShell do centro de conformidade de segurança &amp; . Por exemplo, você pode executar o seguinte comando para adicionar um grupo de segurança habilitado para email ao grupo de funções Gerenciador de descoberta eletrônica. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Observe que não há suporte para um grupo de distribuição do Exchange ou um grupo do Office 365. Você deve usar um grupo de segurança habilitado para email, que pode ser criado no PowerShell do Exchange Online usando ` New-DistributionGroup -Type Security ` o comando. Você também pode criar um grupo de segurança habilitado para email (e adicionar membros) no centro de administração do Exchange ou no centro de administração do Office 365. Observe que pode levar até 60 minutos depois de criá-lo para que uma nova segurança habilitada para email fique disponível para ser adicionada ao grupo de função gerenciadores de descoberta eletrônica. 
    
    Também como declarado anteriormente, você não pode tornar um grupo de segurança habilitado para email em um administrador de descoberta eletrônica usando o cmdlet **Add-eDiscoveryCaseAdmin** no PowerShell do centro de conformidade de segurança &amp; . Você só pode adicionar usuários individuais como administradores de descoberta eletrônica. 
    
    Observe que você também não pode adicionar um grupo de segurança habilitado para email como um membro de uma ocorrência.
