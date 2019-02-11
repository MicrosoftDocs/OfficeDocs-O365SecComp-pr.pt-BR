---
title: Configurar limites de conformidade para investigações de Descoberta eletrônica no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: Use os limites de conformidade para criar limites lógicos dentro de uma organização do Office 365 que controlam os locais de conteúdo do usuário que um gerente de descoberta eletrônica pode pesquisar. Limites de conformidade usam permissões de pesquisa filtragem (também chamado de conformidade segurança filtros) para controlar quais caixas de correio, os sites do SharePoint e contas do OneDrive podem ser pesquisadas por usuários específicos.
ms.openlocfilehash: 23594673e70be4b960c463ae2344c2f4b0fd0cbe
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29768012"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Configurar limites de conformidade para investigações de Descoberta eletrônica no Office 365

Limites de conformidade criar limites lógicos dentro de uma organização do Office 365 que controlam os locais de conteúdo usuário (por exemplo, caixas de correio, sites do SharePoint e contas do OneDrive) que os gerentes de descoberta eletrônica podem pesquisar. Além disso, conformidade limites controlar quem pode acessar os casos de eDiscovery usados para gerenciar o legais, recursos humanos ou outras investigações dentro da sua organização. A necessidade de limites de conformidade geralmente é necessária para várias Nações corporações que precisam respeitar hóspedes geográficas e regulamentações e para os governos, que são geralmente divididos em órgãos diferentes. No Office 365, ajuda de limites de conformidade, você atende a esses requisitos ao executar conteúdo pesquisas e gerenciando investigações com casos de eDiscovery.
  
Usaremos o exemplo na ilustração a seguir para explicam como funcionam os limites de conformidade.
  
![Limites de conformidade consistem de filtros de permissões de pesquisa que os grupos de controlar o acesso às agências e a função de administrador que controlam o acesso aos casos de eDisocovery](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
Neste exemplo, a Contoso LTD é uma organização do Office 365 que consiste em duas subsidiárias, Fourth Coffee e Vinícola Coho. A empresa exigir que os investigadores e gerentes de descoberta eletrônica somente podem pesquisar as caixas de correio do Exchange, contas de OneDrive e sites do SharePoint em seu agência. Além disso, os gerentes de descoberta eletrônica e investigadores só podem ver os casos de eDiscovery no em seu agência, e eles podem acessar apenas os casos que eles estão um membro de. Aqui está como limites de conformidade atendem a esses requisitos.
  
- As permissões de pesquisa funcionalidade em controles de conteúdo de pesquisa de filtragem os locais de conteúdo que investigadores e gerentes de descoberta eletrônica podem pesquisar. Isso significa que os gerentes de descoberta eletrônica e investigadores na agência Fourth Coffee somente podem pesquisar locais de conteúdo das subsidiárias Fourth Coffee. A mesma restrição se aplica a subsidiária Vinícola Coho.
    
    Grupos de função controlar quem pode ver os casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade. Isso significa que investigadores e gerentes de descoberta eletrônica só podem ver os casos de eDiscovery em seu agência.
    
- Grupos de função também controlam quem pode atribuir membros a um caso de eDiscovery. Isso significa que investigadores e gerentes de descoberta eletrônica só podem atribuir membros a casos que eles próprios serão um membro do.
    
Aqui está o processo para configurar limites de conformidade:
  
[Etapa 1: Identificar um atributo de usuário para definir suas agências](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Etapa 2: Uma solicitação com o Microsoft Support para sincronizar o atributo do usuário às contas de OneDrive do arquivo](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Etapa 3: Criar um grupo de funções para cada agência](#step-3-create-a-role-group-for-each-agency)

[Etapa 4: Criar um filtro de permissões de pesquisa para impor o limite de conformidade](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Etapa 5: Criar um caso de eDiscovery para investigações uma agência da UE](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Etapa 1: Identificar um atributo de usuário para definir suas agências

A primeira etapa é escolher um atributo do Active Directory do Azure para usá-la definirá seus agências. Este atributo será ser usado para criar o filtro de permissões de pesquisa que limita o eDiscovery manager para pesquisar apenas os locais de conteúdo de usuários que estão atribuídos a um valor específico para esse atributo. Por exemplo, digamos que Contoso decida utilizar o atributo do **departamento** . O valor para este atributo para os usuários na subsidiária de Fourth Coffee seria `FourthCoffee` e o valor para os usuários na subsidiária da Coho Winery seria `CohoWinery`. Na etapa 4, você usará esse `attribute:value` par (por exemplo, o *Departamento: FourthCoffee* ) para limitar o usuário que os gerentes de descoberta eletrônica podem pesquisar locais de conteúdo. 
  
Aqui está uma lista de atributos de usuário do Windows Azure Active Directory que você pode usar os limites de conformidade de:
  
- Empresa
    
- CustomAttribute1 - CustomAttribute15
    
- Departamento
    
- Escritório
    
Embora mais atributos de usuário estão disponíveis, especialmente para caixas de correio do Exchange, os atributos listados acima são os únicos suportados atualmente pelo OneDrive.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Etapa 2: Uma solicitação com o Microsoft Support para sincronizar o atributo do usuário às contas de OneDrive do arquivo

A próxima etapa é uma solicitação ao Microsoft Support para sincronizar o atributo do Azure Active Directory que você escolheu na etapa 1 para todas as contas de OneDrive na sua organização. Depois que essa sincronização ocorre, o atributo (e seu valor) que você escolheu na etapa 1 será mapeada para uma propriedade gerenciada oculta no SharePoint denominado `ComplianceAttribute`. Você usará esse atributo para criar o filtro de permissões de pesquisa onedrive na etapa 4.
  
Quando você envia a solicitação para o suporte da Microsoft, inclua as seguintes informações:
  
- O nome de domínio padrão da sua organização do Office 365
    
- O nome do atributo do Active Directory do Windows Azure (da etapa 1)
    
- O título ou a descrição do objetivo da solicitação de suporte a seguir: "Habilitar OneDrive para Business sincronização com o Azure Active Directory para conformidade filtros de segurança". Isso ajudará a rotear a solicitação para a equipe de engenharia de descoberta eletrônica de Office 365 que implementará a solicitação.
    
Após a alteração de engenharia é feita e o atributo é sincronizado com o OneDrive, o Microsoft Support o enviará o número de compilação que a alteração ser feita no e uma data de implantação estimado. Observe que, em geral, o processo de implantação leva de 4 a 6 semanas após enviar a solicitação de suporte.
  
 **Importante:** Você pode concluir a etapa 3, a etapa 5 antes que a alteração seja implantada. Mas executar pesquisas de conteúdo não devolvem documentos de sites de OneDrive especificados no filtro de permissões de pesquisa até depois que a alteração seja implantada. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Etapa 3: Criar um grupo de funções para cada agência

A próxima etapa é criar os grupos de função no Office 365 Security &amp; Centro de conformidade que irá se alinhem à suas agências. Recomendamos que você crie um novo grupo de função copiando o grupo gerentes de descoberta eletrônica internas, adicionando os membros apropriados e Removendo funções que podem não ser aplicáveis às suas necessidades. Para obter mais informações sobre funções de descoberta eletrônica, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
  
Para criar os grupos de função, vá para a página de **permissões** na segurança &amp; Centro de conformidade e criar um grupo de funções para cada equipe em cada agência que usarão os limites de conformidade e casos de eDiscovery para gerenciar investigações. 
  
Usando o cenário de limites de conformidade Contoso, quatro grupos de função precisam ser criadas e os membros apropriados adicionados a cada um deles.
  
- Gerentes de Fourth Coffee eDiscovery
    
- Quarto investigadores Coffee
    
- Coho Winery eDiscovery gerentes
    
- Coho Winery investigadores
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Etapa 4: Criar um filtro de permissões de pesquisa para impor o limite de conformidade
<a name="step4"> </a>

Depois que você criou a grupos de funções para cada agência, a próxima etapa é criar os filtros de permissões de pesquisa que associar cada grupo de funções ao seu agência específica e define o limite de conformidade em si. Você precisa criar um filtro de permissões de pesquisa para cada agência. Para obter mais informações sobre como criar filtros de permissões de segurança, consulte [Configure permissions filtragem para a pesquisa de conteúdo](permissions-filtering-for-content-search.md).
  
Aqui está a sintaxe usada para criar um filtro de permissões de pesquisa usado para os limites de conformidade.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
Aqui está uma descrição de cada parâmetro no comando:
  
-  `FilterName`-Especifica o nome do filtro. Use um nome que descreve ou identifica a agência que filtram será usado no. 
    
-  `Users`-Especifica os usuários ou grupos que obtém esse filtro aplicado para as ações de pesquisa de conteúdo que eles executam. Limites de conformidade deste parâmetro especifica os grupos de função (que você criou na etapa 3) na agência que você está criando o filtro para. Observe que este é um parâmetro de valor múltiplos, para que você possa incluir um ou mais grupos de função, separados por vírgulas. 
    
-  `Filters`-Especifica os critérios de pesquisa para o filtro. Para os limites de conformidade, você irá definir os seguintes filtros. Cada um deles se aplica a um local de conteúdo do usuário. 
    
  -  `Mailbox`-Especifica as caixas de correio que os grupos de função definidos no `Users` parâmetro pode pesquisar. Limites de conformidade, *ComplianceAttribute* é o mesmo atributo que você identificou na etapa 1 e *valor de atributo* Especifica a agência. Esse filtro permite que os membros do grupo de função para pesquisar somente as caixas de correio em uma agência específica; Por exemplo, `"Mailbox_Department -eq 'FourthCoffee'"` . 
    
  -  `Site`-Especifica as contas de OneDrive que os grupos de função definidos no `Users` parâmetro pode pesquisar. Para o filtro de OneDrive, use a cadeia de caracteres real `ComplianceAttribute`; Isso irá mapear para o mesmo atributo que você identificou na etapa 1 e que é sincronizado com o OneDrive contas como resultado da solicitação de suporte que você enviados na etapa 2;  *Valor de atributo* Especifica a agência. Esse filtro permite que os membros do grupo de função para pesquisar somente as contas de OneDrive em uma agência específica; Por exemplo, `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
  -  `Site_Path`-Especifica os sites do SharePoint que os grupos de função definidos no `Users` parâmetro pode pesquisar. O *SharePointURL* Especifica os sites em agência que membros do grupo de função podem pesquisar; Por exemplo,`"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`
    
-  `Action`-Especifica o tipo de ação de pesquisa de conformidade que o filtro é aplicado à. Por exemplo, `-Action Search` se aplica apenas ao filtro quando membros dos grupos de função definidos no `Users` parâmetro executa uma pesquisa de conteúdo. Nesse caso, o filtro não seria ser aplicado ao exportar os resultados da pesquisa. Limites de conformidade, use `-Action All` para o filtro se aplica a todas as ações de pesquisa. 
    
    Para obter uma lista das ações a pesquisa de conteúdo, consulte a seção "New-ComplianceSecurityFilter" em [Configure permissions filtragem para a pesquisa de conteúdo](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).
    
Estes são exemplos dos filtros de duas pesquisa permissões que pode ser criados para suportar o cenário de limites de conformidade de Contoso.
  
 **A Fourth Coffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Vinícola Coho**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a>Etapa 5: Criar um caso de eDiscovery para investigações uma agência da UE

A etapa final é criar um novo caso de descoberta eletrônica na segurança &amp; Centro de conformidade e, em seguida, adicione o grupo de função — que você criou na etapa 3 — como membro do caso. Isso resulta em duas características importantes do uso de limites de conformidade:
  
- Somente membros do grupo de função adicionado ao caso poderão ver e acessar o caso na segurança &amp; Centro de conformidade. Por exemplo, se o grupo de funções investigadores de Fourth Coffee é o único membro de um caso, em seguida, os membros do grupo de função de gerentes de descoberta eletrônica Fourth Coffee (ou membros de qualquer outro grupo de função) não conseguirá ver ou acessar o caso.
    
- Quando um membro do grupo de funções atribuído a um caso executa uma pesquisa associada com o caso, eles somente poderão pesquisar os conteúdo locais dentro de sua agência (que é definida pelo filtro de permissões de pesquisa que você criou na etapa 4.)


Para criar um novo caso e atribuir membros:
    
1. Vá para a página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade e criar um novo caso. 
    
2. Na lista de casos de eDiscovery, clique no nome do caso que você acabou de criar.
    
3. Na página **Gerenciar neste caso** submenu, em **grupos de função de gerenciar**, clique em ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Add**.
    
    ![Adicionar um grupo de funções como um membro de um caso de eDiscovery](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Na lista de grupos de função, selecione um dos grupos da função que você criou na etapa 3 e clique em **Adicionar**.
    
5. Clique em **Salvar** no submenu a **Gerenciar neste caso** para salvar a alteração. 

## <a name="compliance-boundary-limitations"></a>Limitações de limite de conformidade

Lembre-se as seguintes limitações ao gerenciar casos do eDiscovery e investigações que usam dos limites de conformidade.
  
- Ao criar e executar uma pesquisa de conteúdo, você pode selecionar os locais de conteúdo que estão fora da sua agência. No entanto, devido ao filtro de permissões de pesquisa, o conteúdo a partir desses locais não será incluído nos resultados da pesquisa.
    
- Limites de conformidade não se aplicam ao isenções em casos de eDiscovery. Isso significa que um gerente de descoberta eletrônica em uma agência pode colocar um usuário em uma agência diferente em espera. No entanto, o limite de conformidade será imposto se o gerente de descoberta eletrônica pesquisará os locais de conteúdo do usuário que foi colocada em espera. Isso significa que o gerente de descoberta eletrônica não ser capaz de pesquisa locais de conteúdo do usuário, mesmo que eles conseguiram colocar o usuário em espera.
    
    Além disso, espera estatísticas serão aplicadas somente ao conteúdo locais no agência.
    
- Filtros de permissões de pesquisa não são aplicados para pastas públicas do Exchange.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>Pesquisando e exportação de conteúdo em ambientes de Multi-Geo

Filtros de permissões de pesquisa também permitem que você controle a que o conteúdo é roteado para a exportação e qual datacenter pode ser pesquisada durante a pesquisa de contas do OneDrive e sites do SharePoint em um [ambiente do SharePoint Multi-Geo](https://go.microsoft.com/fwlink/?linkid=860840):
  
- Exporte resultados da pesquisa de um data center específico. Isso significa que você pode especificar o que local do centro os dados serão exportados resultados da pesquisa.
    
- Pesquisas de rota de sites do SharePoint e contas de OneDrive para um data center de satélite. Isso significa que você pode especificar o local do data center em que as pesquisas serão executadas.
    
Use o parâmetro **Region** para os cmdlets **New-ComplianceSecurityFilter** ou **Set-ComplianceSecurityFilter** para criar ou alterar o qual a exportação será roteada através de datacenter.
  
|**Valor do parâmetro**|**Localização do data center**|
|:-----|:-----|
|NAM  <br/> |América do Norte (dados reais centers estão nos EUA)  <br/> |
|EUR  <br/> |Europa  <br/> |
|APC  <br/> |Ásia Pacífico  <br/> |
|CAN <br/> |Canadá
   
Da mesma forma, você pode usar os seguintes valores para os valores de parâmetro de **região** para controlar qual data center que as pesquisas de conteúdo será executado durante a pesquisa locais do SharePoint e OneDrive. Observe que a tabela a seguir também mostra qual exportações serão roteadas através do Centro de dados. 
  
|**Valor do parâmetro**|**Locais de roteamento para exportação de data center**|
|:-----|:-----|
|NAM  <br/> |EUA  <br/> |
|EUR  <br/> |Europa  <br/> |
|APC  <br/> |Ásia Pacífico  <br/> |
|CAN  <br/> |EUA  <br/> |
|AUS  <br/> |Ásia Pacífico  <br/> |
|KOR  <br/> |Centro de dados padrão da organização  <br/> |
|GBR  <br/> |Europa  <br/> |
|JPN  <br/> |Ásia Pacífico  <br/> |
|IND  <br/> |Ásia Pacífico  <br/> |
|LAM  <br/> |EUA  <br/> |
   
 **Observação:** Se você não especificar o parâmetro Region para um filtro de permissões de pesquisa, a região de SharePoint organizações padrão devem ser pesquisada, então os resultados da pesquisa são exportados para o Centro de dados mais próximo. 
  
Estes são exemplos de como usar o **-região** parâmetro ao criar filtros de permissão de pesquisa para os limites de conformidade. Isso pressupõe que o subsidiária de Fourth Coffee está localizada na América do Norte e que a Vinícola Coho está na Europa. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Mantenha as seguintes coisas em mente ao pesquisar e exportação de conteúdo em ambientes de multi-geo.
  
- O parâmetro **Region** não controlar pesquisas de caixas de correio do Exchange; todos os centros de dados devem ser pesquisados quando você pesquisa de caixas de correio. Para limitar o escopo do qual Exchange caixas de correio podem ser pesquisadas, use o parâmetro de **filtros** ao criar ou alterar um filtro de permissões de pesquisa. 
    
- Se for necessário para um gerente para pesquisar em várias regiões SharePoint eDiscovery, você precisará criar uma conta de usuário diferente para que o eDiscovery manager que pode ser usado no filtro de permissões de pesquisa para especificar a região alternativa onde o Sites do SharePoint ou as contas do OneDrive estão localizadas.
    
- Durante a pesquisa de conteúdo no SharePoint e OneDrive, o parâmetro **Region** direciona pesquisas para qualquer um dos principal ou satélite local onde o gerente de descoberta eletrônica conduzirá investigações de descoberta eletrônica. Se um gerente de descoberta eletrônica pesquisar sites SharePoint e OneDrive fora da região que é especificado no filtro de permissões de pesquisa, nenhum resultado de pesquisa será retornado. 
    
- Ao exportar os resultados da pesquisa, conteúdo de todos os locais de conteúdo (incluindo o Exchange, Skype onedrive de negócios, SharePoint e outros serviços do Office 365 que você pode pesquisar usando a ferramenta de pesquisa de conteúdo) será carregado para o local de armazenamento do Azure na Centro de dados que é especificado pelo parâmetro **região** . Isso ajuda as organizações a ficar dentro conformidade não permitindo que o conteúdo a ser exportado entre as fronteiras controladas. Se nenhuma região é especificado no filtro de permissões de pesquisa, o conteúdo é carregado a região de padrão da organização. 
    
- Você pode editar um filtro existente de permissões de pesquisa para adicionar ou alterar a região executando o seguinte comando:

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Perguntas frequentes

 **Quem pode criar e gerenciar filtros de permissões de pesquisa (usando New-ComplianceSecurityFilter e cmdlets Set-ComplianceSecurityFilter)?**
  
Para criar, visualizar e modificar os filtros de permissões de pesquisa, você precisa ser membro do grupo de funções de gerenciamento da organização na segurança &amp; Centro de conformidade.
  
 **Se um gerente de descoberta eletrônica é atribuído a mais de um grupo de função que abrange várias agências, como eles para pesquisar por conteúdo em uma agência ou outra?**
  
O gerente de descoberta eletrônica pode adicionar parâmetros à sua consulta de pesquisa que restringe a pesquisa para uma agência específica. Por exemplo, se uma organização especificou a propriedade **CustomAttribute10** para diferenciar os órgãos, eles podem acrescentar o seguinte à sua consulta de pesquisa para pesquisar caixas de correio e contas do OneDrive em uma agência específica: `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.
  
 **O que acontece se o valor do atributo que é usado como o atributo de conformidade em um filtro de permissões de pesquisa for alterado?**
  
Leva até 3 dias para um filtro de permissões de pesquisa para impor o limite de conformidade, se o valor do atributo que é usado no filtro é alterado. Por exemplo, no cenário Contoso digamos que um usuário nos agência Fourth Coffee é transferido para a agência da Coho Winery. Como resultado, o valor do atributo **Department** no objeto do usuário é alterado de *FourthCoffee* para *CohoWinery* . Nessa situação, investidores e eDiscovery Fourth Coffee poderá obter resultados de pesquisa para esse usuário para o backup de 3 dias após o atributo é alterado. Da mesma forma, levará até 3 dias antes de gerentes de descoberta eletrônica da Coho Winery e investigadores receberá os resultados da pesquisa para o usuário. 
  
 **Um gerente de descoberta eletrônica pode ver o conteúdo de dois limites de conformidade separado?**
  
Sim. Isso pode ser feito adicionando o usuário a grupos de funções que têm a visibilidade para ambas as agências.
  
 **A pesquisa funciona de filtros de permissões para DLP, as políticas de retenção do Office 365 ou isenções casos de descoberta eletrônica?**
  
Não, não desta vez
  
 **Se eu especificar uma região para controlar onde o conteúdo será exportado, mas não tenho uma organização do SharePoint na região, podem ainda pesquisar SharePoint?**
  
Se a região especificada no filtro de permissões de pesquisa não existir na sua organização, a região padrão devem ser pesquisada.
  
 **O que é o número máximo de filtros de permissões de pesquisa que podem ser criados em uma organização?**
  
Não há nenhum limite ao número de filtros de permissões de pesquisa que podem ser criados em uma organização. No entanto, o desempenho de pesquisa será afetado quando há mais de 100 filtros de permissões de pesquisa. Para manter o número de filtros de permissões de pesquisa em sua organização tão pequeno quanto possível, crie filtros que combinam regras para Exchange, SharePoint e OneDrive em um filtro de permissões de pesquisa único sempre que possível.
