---
title: Pesquisa de conteúdo no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: Usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar conteúdo em caixas de correio, sites do SharePoint Online, contas de OneDrive, Teams da Microsoft, os grupos de Office 365 e Skype para conversas de negócios. Você pode usar as consultas de pesquisa de palavra-chave e critérios de pesquisa para restringir os resultados da pesquisa. Em seguida, você pode visualizar e exportar os resultados da pesquisa. Pesquisa de conteúdo também é uma ferramenta eficaz para procurar conteúdo que pode estar relacionado a uma solicitação de entidade de dados GDPR.
ms.openlocfilehash: 11e96c6a11dd66c0095b7c624413e9e39036d8d6
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782078"
---
# <a name="content-search-in-office-365"></a>Pesquisa de conteúdo no Office 365

Você pode usar a ferramenta de descoberta eletrônica de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar itens in-loco, como email, documentos e conversas em sua organização do Office 365 de mensagens instantâneas. Use essa ferramenta para procurar itens nesses serviços do Office 365:
  
- Caixas de correio do Exchange Online e as pastas públicas
    
- OneDrive para contas de negócios e sites do SharePoint Online
    
- Skype para conversas de negócios
    
- Microsoft Teams 
    
- Grupos do Office 365
    
Após executar uma pesquisa de conteúdo, o número de locais de conteúdo e um número estimado dos resultados da pesquisa é exibido no perfil de pesquisa. Também rapidamente, você pode exibir estatísticas, como os locais de conteúdo que possuem a maioria dos itens que correspondem à consulta de pesquisa. Após executar uma pesquisa, você pode visualizar os resultados ou exportá-los para um computador local.


## <a name="create-a-new-search"></a>Criar uma nova pesquisa

Para ter acesso à página **pesquisa de conteúdo** para executar pesquisas e visualizar e exportar os resultados da pesquisa, um administrador, responsável pela conformidade ou gerente de descoberta eletrônica deve ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; Centro de conformidade. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entre usando seu endereço de email do Office 365 e a senha. 
    
3. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.
    
4. Na página de **pesquisa** , clique na seta ao lado de ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nova pesquisa**. 
    
    ![A nova lista suspensa de pesquisa](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Você pode escolher uma destas opções:
    
  - **Pesquisa guiada** - essa opção inicia um assistente que o orienta durante a criação da pesquisa. A interface do usuário para selecionar locais de conteúdo e construa a consulta de pesquisa são iguais a opção **nova pesquisa** . 
    
  - **Nova pesquisa** - essa opção exibe uma interface de usuário atualizada para criar uma nova pesquisa. Esta é a opção padrão, se você clicar em **Pesquisar New**.
    
  - **Pesquisa por lista ID** - essa opção permite procurar mensagens de email específicos e outros itens de caixa de correio usando uma lista de IDs do Exchange. Para criar uma pesquisa de ID de lista (formalmente chamada de uma pesquisa de destino), você enviar um arquivo (CSV) de valores separados por vírgula que identifica os itens de caixa de correio específica a ser pesquisado. Para obter instruções, consulte [Prepare um arquivo CSV para uma lista de IDs de pesquisa de conteúdo no Office 365](csv-file-for-an-id-list-content-search.md).
    
    O restante das etapas neste procedimento seguirão o fluxo de trabalho de pesquisa novo padrão.
    
5. Na lista suspensa, clique em **nova pesquisa** . 
    
6. Na **consulta de pesquisa**, especifique as ações a seguintes.
    
    ![Especificar palavras-chave, condições e locais para pesquisa](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
- **Palavras-chave para procurar** - tipo de consulta de uma pesquisa na caixa **palavras-chave** . Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que usam um operador booleano, como **AND**, **ou**, **não**e **NEAR**. Você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) em documentos ou procurar documentos que foram compartilhados externamente. Se você deixar a caixa de palavra-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificados será incluído nos resultados da pesquisa.
    
    Como alternativa, você pode clicar na caixa de seleção **Mostrar lista de palavra-chave** e o tipo de uma palavra-chave em cada linha. Se você fizer isso, as palavras-chave em cada linha são conectadas por um operador lógico ( **c:s**) que é semelhante em funcionalidade ao operador **OR** na consulta de pesquisa que é criado. 
    
    Por que usar a lista de palavra-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave é mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas da pesquisa, consulte [Exibir as estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
    
- **Condições** - você pode adicionar condições para limitar a pesquisa e retornar um conjunto mais refinado de resultados de pesquisa. Cada condição adiciona uma cláusula a consulta de pesquisa que é criado e executados quando você iniciar a pesquisa. Uma condição logicamente é conectada a consulta de palavra-chave (especificada na caixa de palavra-chave) por um operador lógico ( **c:c**) que é semelhante em funcionalidade ao operador **e** . Isso significa que os itens têm que satisfazer a consulta de palavra-chave e uma ou mais condições a serem incluídos nos resultados. Isso é como ajudam a condições para restringir os resultados. Para obter uma lista e descrição das condições que podem ser usados em uma consulta de pesquisa, consulte a seção "Critérios de pesquisa" em [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md#search-conditions).
    
- **Locais** - escolher os locais de conteúdo para pesquisa.
    
  - **Todos os locais** - Use essa opção para pesquisar todos os locais de conteúdo na sua organização. Isso inclui email em todas as caixas postais do Exchange (incluindo todas as caixas de correio inativas, caixas de correio para todos os grupos do Office 365, caixas de correio for todos Teams da Microsoft), todos os Skype para conversas de negócios, SharePoint e o OneDrive para sites corporativos (incluindo os sites para todos os grupos do Office 365 e Microsoft Teams) e itens em todas as pastas públicas do Exchange.
    
  - **Locais específicos** - Use essa opção para pesquisar locais de conteúdo específico. Você pode pesquisar todos os locais de conteúdo para um serviço específico do Office 365 (como pesquisar todas as caixas de correio do Exchange ou pesquisar todos os sites do SharePoint) ou você pode pesquisar locais específicos em qualquer um dos serviços do Office 365 que são exibidos. 
    
    ![Interface do usuário para escolher locais de conteúdo para pesquisa](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
    Observe que você também pode adicionar grupos de distribuição à lista de caixas de correio do Exchange para pesquisar. Para grupos de distribuição, as caixas de correio de membros de grupo são pesquisadas. Observe que os grupos dinâmicos de distribuição não são suportados.
    
    **Importante:** Quando você procura todos os locais de caixa de correio ou caixas de correio específicas apenas, dados de MyAnalytics e outros aplicativos do Office 365 que salvou a caixas de correio do usuário serão incluídos ao exportar os resultados de uma pesquisa de conteúdo. Esses dados não serão incluídos nos resultados da pesquisa estimados e ele não estará disponível para visualização. Ele só será incluído quando você exporta e baixe os resultados de pesquisa; consulte [dados de exportação de MyAnalytics e outros aplicativos do Office 365](#exporting-data-from-myanalytics-and-other-office-365-applications) na seção "Para obter mais informações sobre a pesquisa de conteúdo". 
    
7. Depois de configurar a consulta de pesquisa, clique em **Salvar &amp; executar**.
    
8. Na página **Salvar pesquisa** , digite um nome para a pesquisa e uma descrição opcional que ajuda a identificar a pesquisa. Observe que o nome da pesquisa deve ser exclusivo na sua organização. 
    
9. Clique em **Salvar** para iniciar a pesquisa. 
    
    Depois de salvar e executar a pesquisa, quaisquer resultados retornados pela pesquisa são exibidos no painel de resultados. Dependendo de como você instalou a configuração de visualização configurada, os resultados da pesquisa são exibição ou você deve clicar em **resultados da visualização** para exibi-los. Consulte a próxima seção para obter detalhes. 
    
Para acessar esta pesquisa de conteúdo novamente ou acessar outras pesquisas de conteúdo listadas na página **pesquisa de conteúdo** , selecione a pesquisa e clique em **Abrir**. 
  
Para limpar os resultados ou criar uma nova pesquisa, clique em ![ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif) **nova pesquisa**. 

  
## <a name="preview-search-results"></a>Visualização de resultados de pesquisa

Há duas configurações para visualização de resultados da pesquisa. Depois de executar uma nova uma nova pesquisa ou abrir uma pesquisa existente, clique em * * resultados individuais * * para exibir as configurações de visualização a seguir: 
  
![Configurações de resultados de pesquisa de visualização](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Visualizar resultados automaticamente** - essa configuração exibe os resultados da pesquisa depois de uma execução de uma pesquisa.
    
2. **Visualizar os resultados da manualmente** - essa configuração exibe espaços reservados no painel de resultados da pesquisa e exibe o botão de **resultados de visualização** que você precise clicar para exibir os resultados da pesquisa. Esta é a configuração padrão; Ele ajuda a aprimorar o desempenho de pesquisa não automaticamente exibindo os resultados da pesquisa quando você abre uma pesquisa existente. 
    
Há limites relacionados ao quantos itens estão disponível a ser visualizado. Para obter mais informações, consulte [limites para pesquisa no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md). 
  
Para obter uma lista dos tipos de arquivo com suporte que pode ser visualizado, consulte [Previewing resultados de pesquisa](#previewing-search-results) na seção "Para obter mais informações sobre a pesquisa de conteúdo". Se um tipo de arquivo não é suportado para visualizar ou baixar uma cópia de um documento, clique em **baixar o arquivo original** para baixá-lo ao computador local. Para. aspx páginas da Web, a URL da página é incluída, embora talvez você não tenha permissões para acessar a página. 
  
Observe também que os itens indexados não estão disponíveis para visualização.
  
## <a name="view-information-and-statistics-about-a-search"></a>Exibir informações e estatísticas sobre uma pesquisa

Depois de criar e executar uma pesquisa de conteúdo, você pode exibir estatísticas sobre os resultados de pesquisa estimados. Isso inclui um resumo dos resultados da pesquisa, as estatísticas de consulta, como o número de locais de conteúdo com os itens que correspondem à consulta de pesquisa e o nome de locais de conteúdo que possuem os itens mais coincidentes. Você pode exibir as estatísticas para pesquisas de conteúdo de um ou mais. Isso permite que você para comparar os resultados de pesquisas de várias rapidamente e tomar decisões sobre a eficácia das suas consultas de pesquisa.
  
Você também pode baixar as estatísticas da pesquisa e as estatísticas de palavra-chave para um arquivo CSV. Isso permite usar os recursos de filtragem e classificação no Excel para comparar os resultados e preparação de relatórios para os resultados de pesquisa.
  
Para exibir estatísticas de pesquisa:
  
1. Na página de **pesquisa de conteúdo** na segurança &amp; Centro de conformidade, clique em **Abrir** e clique em que você deseja exibir a estatística para pesquisa. 
    
2. Dinamicamente-out de página, clique em **Abrir consulta**. 
    
3. Na lista suspensa **resultados individuais** , clique em **perfil de pesquisa**.
    
4. Na lista suspensa **tipo** , clique em uma das opções a seguir, dependendo das estatísticas de pesquisa que você deseja exibir. 
    
  - **Resumo** : exibe as estatísticas para cada tipo de locais de conteúdo é pesquisado. Isso o número de locais de conteúdo que continha os itens que correspondem a consulta de pesquisa de conteúdo e o número total e o tamanho dos itens de resultado de pesquisa. Esta é a configuração padrão.
    
  - **Consultas** - exibe estatísticas sobre a consulta de pesquisa. Isso inclui o tipo de conteúdo local, as estatísticas de consulta são aplicáveis ao, parte da consulta de pesquisa, as estatísticas são aplicáveis para (Observe que o **principal** indica a consulta de pesquisa toda), o número de locais de conteúdo que contêm os itens corresponder a consulta de pesquisa e o número total e o tamanho e a itens encontrados (no local especificado conteúdo) que correspondem à consulta de pesquisa. Observe que as estatísticas de itens indexados (também chamados de itens indexados parcialmente) também são exibidas. No entanto, os únicos itens indexados parcialmente das caixas de correio estão incluídos nas estatísticas. Itens indexados parcialmente do SharePoint e OneDrive não são incluídos nas estatísticas.
    
  - **Locais principais** - exibe estatísticas sobre o número de itens que correspondem à consulta de pesquisa em cada local de conteúdo que foi pesquisada. Os locais da parte superior a 1.000 são exibidos.
    
Para obter informações mais detalhadas sobre as estatísticas da pesquisa, consulte [Exibir as estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exportar resultados de pesquisa

Depois que uma pesquisa for executada com êxito, você pode exportar os resultados da pesquisa para um computador local. Quando você exporta os resultados de email, eles podem ser baixados em seu computador, como arquivos PST ou mensagens individuais (arquivos. msg). Quando você exporta o conteúdo de sites do SharePoint e OneDrive, cópias de documentos do Office nativos são exportadas. Há também documentos adicionais e relatórios que estão incluídos com os resultados da pesquisa exportado. Você pode também apenas exportar o relatório de resultados de pesquisa e não os itens reais.
  
Para exportar os resultados da pesquisa:
  
1. Na página de **pesquisa de conteúdo** na segurança &amp; Centro de conformidade, clique em **Abrir** e clique em que você deseja exportar os resultados de pesquisa. 
    
2. Dinamicamente-out de página, clique em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mais**e clique em **exportar os resultados**. Observe que você também pode exportar um relatório de resultados de pesquisa.
    
3. Conclua as seções na página do submenu **Exportar resultados**. Certifique-se de usar a barra de rolagem para exibir todas as opções de exportação. 
    
Para obter instruções mais detalhadas e dicas de solução de problemas, consulte:
  
- [Exportar resultados da pesquisa da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
- [Exportar um relatório da Pesquisa de Conteúdo](export-a-content-search-report.md)
    

  
## <a name="more-information-about-content-search"></a>Para obter mais informações sobre a pesquisa de conteúdo

Consulte as seções a seguir para obter mais informações sobre as pesquisas de conteúdo.
  
[Limites de pesquisa de conteúdo](#content-search-limits)
  
[Criar uma consulta de pesquisa](#building-a-search-query)
  
[Pesquisando contas do OneDrive](#searching-onedrive-accounts)
  
[Recursos de pesquisa equipes da Microsoft e grupos do Office 365](#searching-microsoft-teams-and-office-365-groups)
  
[A pesquisa de caixas de correio inativas](#searching-inactive-mailboxes)
  
[Visualização de resultados da pesquisa](#previewing-search-results)
  
[Itens indexados parcialmente](#partially-indexed-items)
  
[Exportando dados do MyAnalytics e outros aplicativos do Office 365](#exporting-data-from-myanalytics-and-other-office-365-applications)
  
### <a name="content-search-limits"></a>Limites de pesquisa de conteúdo

- Para obter uma descrição dos limites que são aplicadas ao recurso de pesquisa de conteúdo, consulte [limites para pesquisa no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md).
    
- Microsoft coleta informações de desempenho para pesquisas de conteúdo executados por todas as organizações do Office 365. Enquanto a complexidade da consulta de pesquisa pode afetar os tempos de pesquisa, o maior fator que afeta quanto tempo take pesquisas é o número de caixas de correio pesquisadas. Embora a Microsoft não oferece um contrato de nível de serviço para tempos de pesquisa, a seguinte tabela lista os tempos de médio de pesquisa para uma pesquisa de conteúdo com base no número de caixas de correio incluídas na pesquisa.
    
|**Número de caixas de correio**|**Tempo médio de pesquisa**|
|:-----|:-----|
|100  <br/> |30 segundos  <br/> |
|1,000  <br/> |45 segundos  <br/> |
|10.000  <br/> |4 minutos  <br/> |
|25.000  <br/> |10 minutos  <br/> |
|50.000  <br/> |20 minutos  <br/> |
|100.000  <br/> |25 minutos  <br/> |
  
### <a name="building-a-search-query"></a>Criar uma consulta de pesquisa

Para obter informações detalhadas sobre como criar uma consulta de pesquisa, usando operadores de pesquisa booleana e condições de pesquisa e pesquisa para tipos de informações confidenciais e conteúdo compartilhado com usuários fora da sua organização, consulte [consultas de palavra-chave e critérios de pesquisa Pesquisa de conteúdo ](keyword-queries-and-search-conditions.md).
  
Manter as seguintes coisas em mente ao usar a lista de palavra-chave para criar uma consulta de pesquisa.
  
- Você precisa selecionar a caixa de seleção **Mostrar lista de palavra-chave** e, em seguida, digite cada palavra-chave em uma linha separada para criar uma consulta de pesquisa onde as palavras-chave (ou frases de palavra-chave) em cada linha são conectadas pelo operador **OR** . Se você simplesmente cola uma lista de palavras-chave na caixa de palavra-chave ou pressione a tecla **Enter** depois de digitar uma palavra-chave, eles não estar conectados pelo operador **ou** . Eis um exemplo correto e incorreto da adição de uma lista de palavras-chave. 
    
    **Incorreto**
    
    ![A maneira incorreta para formatar uma lista de palavra-chave (por colando a lista na caixa palavras-chave)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Corrigir**
    
    ![A maneira correta para formatar uma lista de palavra-chave (selecionando checkbox e, em seguida, colando lista)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Você pode também preparar uma lista de palavras-chave ou frases de palavra-chave em um arquivo do Excel ou em um arquivo de texto sem formatação e, em seguida, em seguida, copie e cole sua lista à lista de palavra-chave. Para fazer isso, você precisará selecionar a caixa de seleção **Mostrar lista de palavra-chave** . Em seguida, clique na primeira linha na lista de palavra-chave e cole sua lista. Cada linha do arquivo de texto ou Excel será colada em separar linha da lista de palavra-chave. 
    
- Depois de criar uma consulta usando a lista de palavra-chave, é uma boa ideia para verificar a sintaxe de consulta de pesquisa para fazer a consulta de pesquisa é o que você pretendia. Na consulta de pesquisa que é exibida na **consulta** no painel de detalhes, as palavras-chave são separadas pelo texto **(c:s)**. Isso indica que as palavras-chave são conectadas por um operador lógico semelhante em funcionalidade ao operador **OR** . Da mesma forma, se a consulta de pesquisa inclui condições, as palavras-chave e as condições são separadas pelo texto **(c:c)**. Isso indica que as palavras-chave estão conectadas às condições com um operador lógico semelhante em funcionalidade ao **e** operador. Aqui está um exemplo de consulta de pesquisa (exibido no painel de detalhes) que resulta ao usar a lista de palavra-chave e uma condição. 
    
    ![Exemplo da consulta é criado ao usar a lista de palavra-chave e uma condição](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Quando você executa uma pesquisa de conteúdo, o Office 365 verifica automaticamente a consulta de pesquisa para caracteres não suportados e operadores booleanos que não podem estar em letras maiusculas. Não há suporte para caracteres geralmente estão ocultas e geralmente causam um erro de pesquisa ou retornam resultados inesperados. Para obter mais informações sobre os caracteres não suportados que são verificados, consulte [verificar sua consulta de pesquisa de conteúdo se há erros](check-your-content-search-query-for-errors.md).
    
- Se você tiver uma consulta de pesquisa que contém as palavras-chaves para os caracteres do inglês (por exemplo, caracteres chineses), você pode clicar em **consulta idioma-país/região**![ícone de idioma-país/região de consulta na pesquisa de conteúdo](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) e selecione um valor de código de cultura do idioma-país para a pesquisa. Observe que o idioma/região padrão é neutro. Como saber se você precisa alterar a configuração de idioma para uma pesquisa de conteúdo? Se você tiver certeza de locais de conteúdo contêm os caracteres do inglês que estiver pesquisando, mas a pesquisa não retorna nenhum resultado, a causa pode estar relacionada a configuração de idioma. 
  
### <a name="searching-onedrive-accounts"></a>Pesquisando contas do OneDrive

- Para coletar a uma lista de URLs para os sites de OneDrive na sua organização, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Esse script neste artigo cria um arquivo de texto que contém uma lista de todos os sites de OneDrive. Para executar esse script, você precisará instalar e usar o Shell de gerenciamento do SharePoint Online. Certifique-se de que inclua o URL para o domínio de meusite da sua organização para cada site de OneDrive que você deseja pesquisar. Este é o domínio que contém todos os seu OneDrive; Por exemplo, `https://contoso-my.sharepoint.com`. Aqui está um exemplo de URL de um site do usuário OneDrive: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    
    No caso raro que o nome principal de usuário de uma pessoa (UPN) é alterado, a URL para seu local de OneDrive também será alterada para incorporar o UPN novo. Se isso acontecer, você terá que modificar uma pesquisa de conteúdo, adicionando a nova URL de OneDrive do usuário e remover o antigo.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>Recursos de pesquisa equipes da Microsoft e grupos do Office 365

Você pode pesquisar a caixa de correio que está associado a um grupo do Office 365 ou um Team Microsoft. Pesquisar-las porque Teams Microsoft baseiam-se no Office 365 grupos, é muito semelhante. Em ambos os casos, apenas, a caixa de correio grupo ou equipe é pesquisada; as caixas de correio dos membros da equipe ou de grupo não são pesquisadas. Para pesquisá-los, você precisará especificamente adicioná-los à pesquisa.
  
Mantenha as seguintes coisas em mente ao pesquisar por conteúdo em Microsoft Teams e grupos do Office 365.
  
- Para procurar conteúdo localizado no Microsoft Teams e grupos do Office 365, você precisa especificar a caixa de correio e o site do SharePoint que estão associados uma equipe ou um grupo.
    
- Execute o cmdlet **Get-UnifiedGroup** no Exchange Online para exibir as propriedades para um Team Microsoft ou um grupo do Office 365. Isso é uma boa maneira de obter a URL para o site que está associado a uma equipe ou um grupo. Por exemplo, o comando a seguir exibe propriedades selecionadas para um grupo do Office 365 denominado sênior liderança equipe: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroup** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
- Quando a caixa de correio do usuário é pesquisada, qualquer Team Microsoft ou um grupo do Office 365 que o usuário é membro do não ser pesquisado. Da mesma forma, quando você pesquisa um Team Microsoft ou um grupo de 365 Office, somente as caixas de correio de grupo e o site de grupo que você especificar é pesquisado; as caixas de correio e OneDrive para contas de negócios dos membros do grupo não são pesquisados, a menos que você os adicione explicitamente à pesquisa.
    
- Para obter uma lista dos membros de um Team Microsoft ou um grupo do Office 365, você pode exibir as propriedades no **inicial \> grupos** página no Centro de administração do Office 365. Como alternativa, você pode executar o seguinte comando no PowerShell do Exchange Online: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroupLinks** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
- Conversas que fazem parte de um canal de Teams da Microsoft são armazenadas na caixa de correio que está associado a Team Microsoft. Da mesma forma, os arquivos que compartilham de membros da equipe em um canal são armazenados no site do SharePoint da equipe. Portanto, você precisará adicionar a caixa de correio do Microsoft Team e o site do SharePoint como um local de conteúdo para pesquisar arquivos e conversas em um canal.
    
- Como alternativa, conversas que fazem parte da lista de bate-papo no Microsoft Teams são armazenadas na caixa de correio Exchange Online dos usuários que participam do bate-papo. E os arquivos que um usuário compartilha em conversas de bate-papo são armazenados em OneDrive para a conta comercial do usuário que compartilha o arquivo. Portanto, você precisará adicionar caixas de correio de usuário individual e OneDrive para contas de negócios, como locais de conteúdo para pesquisar conversas e arquivos na lista de bate-papo.
    
    > [!NOTE]
    > Os usuários participem de conversas que fazem parte da lista de bate-papo no Microsoft Teams devem ter uma caixa de correio (baseado em nuvem) Exchange Online na ordem a procura de conversas de bate-papo. Isso acontece porque conversas que fazem parte da lista de Chat são armazenadas nas caixas de correio baseadas em nuvem dos participantes bate-papo. Se um participante de bate-papo não tiver uma caixa de correio do Exchange Online, você não conseguirá conversas de bate-papo de pesquisa. Por exemplo, em uma implantação híbrida do Exchange, os usuários com uma caixa de correio local poderá participar de conversas que fazem parte da lista de bate-papo no Microsoft Teams. No entanto nesse caso, o conteúdo desses conversa não pesquisáveis porque os usuários não têm caixas de correio baseadas em nuvem. 
  
- Cada canal Microsoft Team ou equipe contém um Wiki para colaboração e anotações. O conteúdo Wiki automaticamente é salvo em um arquivo com um formato. mht. Este arquivo é armazenado na biblioteca de documentos de equipes Wiki dados no site do SharePoint da equipe. Você pode usar a ferramenta de pesquisa de conteúdo para pesquisar o Wiki, especificando o site do SharePoint da equipe como o local do conteúdo a ser pesquisado. 
    
    > [!NOTE]
    > A capacidade de pesquisar o Wiki um Microsoft Team ou canal (quando você pesquisar o site do SharePoint da equipe) foi lançada em 22 de junho de 2017. Páginas wiki que foram salvas ou atualizadas na data ou após estão disponíveis a serem pesquisados. Páginas wiki última salvo ou atualizado antes desta data não estão disponíveis para pesquisa. 
 
- Informações de resumo para reuniões e chamadas em um canal de Teams da Microsoft também são armazenados nas caixas de correio de usuários que discaram para a reunião ou chamada. Isso significa que você pode usar a pesquisa de conteúdo para pesquisar esses registros de resumo. Informações de resumo incluem: 
  - Data, hora de início, hora de término e duração de uma reunião ou chamada

  - A data e hora quando cada participante entrou ou a reunião ou chamada da esquerda

  - Chamadas enviadas para a caixa postal

  - Chamadas perdidas ou não atendidas

  - Transferências de chamada, que são representadas como duas chamadas separadas

  Observe que pode levar até oito horas para registros de resumo de reunião e chamada esteja disponível a ser pesquisado.

  Nos resultados da pesquisa, resumos de reunião são identificados como **reunião** no **campo tipo**; resumos de chamada são identificados como **chamar**. Além disso, conversas que fazem parte de um chats de canal e 1xN equipes são identificadas como **mensagens Instantâneas** no campo **tipo** .
  
  ![As equipes de reuniões, chamadas e chats 1xN são identificadas no campo tipo de](media/O365-ContentSearch-Teams-MessageKind.png)

- Você pode usar a propriedade de email do **tipo** ou a condição de pesquisa de **tipo de mensagem** para procurar especificamente por conteúdo em Teams da Microsoft. 
  - Para usar a propriedade **Kind** como parte da consulta de pesquisa de palavra-chave, na caixa **palavras-chave** de uma consulta de pesquisa, digite `kind:microsoftteams`.

    ![Usar o tipo: microsoftteams na caixa palavras-chave](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Para usar um critério de pesquisa, adicione a condição de **tipo de mensagem** e use o valor `microsoftteams`. 

    ![Use a condição kind de mensagem com o valor microsoftteams.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Observe que condições logicamente estão conectadas a consulta de palavra-chave pelo operador **e** . Isso significa que um item deve corresponder a consulta de palavra-chave e o critério de pesquisa a serem retornadas nos resultados da pesquisa. Para obter mais informações, consulte a seção "Diretrizes para usar condições" [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)

  
### <a name="searching-inactive-mailboxes"></a>A pesquisa de caixas de correio inativas

Você pode pesquisar caixas de correio inativas em uma pesquisa de conteúdo. Para obter uma lista das caixas de correio inativas em sua organização, execute o comando `Get-Mailbox -InactiveMailboxOnly` no PowerShell do Exchange Online. Como alternativa, você pode ir para **governança de dados** \> **retenção** na segurança &amp; Centro de conformidade e clique em **mais**![elipses da barra de navegação](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **caixas de correio inativas**.
  
Aqui estão algumas coisas ter em mente ao pesquisar caixas de correio inativas.
  
- Se uma pesquisa de conteúdo inclui uma caixa de correio do usuário e essa caixa de correio, em seguida, será feita inativa, continuará a pesquisa de conteúdo pesquisar a caixa de correio inativa quando você executar a pesquisa novamente depois que ele fique inativo.
    
- Em alguns casos, um usuário pode ter uma caixa de correio ativa e uma caixa de correio inativa que têm o mesmo endereço SMTP. Nesse caso, somente a caixa de correio específica que você selecionar como um local para uma pesquisa de conteúdo devem ser pesquisada. Em outras palavras, se você adicionar caixa de correio de um usuário a uma pesquisa, você não pode assumir que ambas as suas ativas e inativas caixas de correio devem ser pesquisadas; somente a caixa de correio que você os adicione explicitamente à pesquisa devem ser pesquisada.
    
- É altamente recomendável que você evite ter uma caixa de correio ativa e a caixa de correio inativa com o mesmo endereço SMTP. Se você precisar reutilizar o endereço SMTP que está atualmente atribuído a uma caixa de correio inativa, recomendamos que você recupere a caixa de correio inativa ou restaura o conteúdo de uma caixa de correio inativa para uma caixa de correio ativa (ou o arquivo morto de uma caixa de correio ativa) e exclua o caixa de correio inativa. Para obter mais informações, consulte um dos seguintes tópicos:
    
  - [Recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md)
    
  - [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a>Visualização de resultados da pesquisa

Você pode visualizar os tipos de arquivo suportados no painel de visualização. Se não há suporte para um tipo de arquivo, você terá que baixar uma cópia do arquivo para o computador local para exibi-lo. Os seguintes tipos de arquivo são suportados e podem ser visualizados no painel de resultados da pesquisa.
  
- . txt,. HTML,. mhtml
    
- . eml
    
- . doc,. docx,. docm
    
- . pptm,. pptx
    
- .pdf
    
Além disso, há suporte para os seguintes tipos de contêiner de arquivo. Você pode exibir a lista de arquivos no contêiner no painel de visualização.
  
- .zip
    
- .gzip
    
### <a name="partially-indexed-items"></a>Itens indexados parcialmente

- Conforme explicadas anteriormente, parcialmente indexados itens em caixas de correio são incluídos nos resultados da pesquisa estimados; itens indexados parcialmente do SharePoint e OneDrive não são incluídos nos resultados da pesquisa estimados. 
    
- Se um parcialmente item corresponde à consulta de pesquisa (porque outras propriedades de mensagem ou documento atendam aos critérios de pesquisa), não será incluído o número estimado de itens indexados. Se um item é excluído pelos critérios de pesquisa, ele também não será incluído entre o número de itens indexados parcialmente estimado de parcialmente. Para obter mais informações, consulte [parcialmente indexados itens na pesquisa de conteúdo no Office 365](partially-indexed-items-in-content-search.md).
    
### <a name="exporting-data-from-myanalytics-and-other-office-365-applications"></a>Exportando dados do MyAnalytics e outros aplicativos do Office 365

- Dados de MyAnalytics (por exemplo, ideias sobre como os usuários gastam dedicação de tempo com base nos dados de email e calendário em suas caixas de correio) e dados de outros aplicativos do Office 365 são salvo em um local oculto (em uma subárvore não-IPM) na caixa de correio do usuário baseada na nuvem. Após executar uma pesquisa de conteúdo, esses dados não estão incluídos nos resultados da pesquisa estimados, as estatísticas de consulta, e ele não está disponível para visualização. No entanto esses dados serão exportados ao exportar os resultados de uma pesquisa.
    
- Os dados MyAnalytics e os dados de outros aplicativos do Office 365 é exportada para uma pasta denominada "Outros dados do Office 365". Essa pasta inclui subpastas para cada usuário.
  