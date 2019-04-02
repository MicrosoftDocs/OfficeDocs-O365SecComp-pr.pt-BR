---
title: Pesquisar dados em uma investigação
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5f52f26c4443addd0e108794e1d3635a9b8efb98
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31029850"
---
# <a name="search-for-data-in-an-investigation"></a>Pesquisar dados em uma investigação

Na guia **Pesquisar** em uma investigação de dados, você pode pesquisar dados incorretos, confidenciais ou confidenciais em locais de conteúdo no Office 365 usando palavras-chave e condições. 

Após executar uma pesquisa, você pode exibir estatísticas sobre os itens retornados pela pesquisa, como os locais de conteúdo que tinham a maioria dos itens que corresponderam à consulta de pesquisa. Você também pode visualizar um subconjunto dos resultados. Depois de identificar o conjunto de documentos que deseja investigar, você pode adicionar os resultados da pesquisa a um conjunto de evidências para processar e analisar ainda mais.

## <a name="create-a-search"></a>Create a search

1. Em uma investigação, clique na guia **pesquisas** e, em seguida, clique em **nova pesquisa**. 

    É exibido um assistente que orientará você durante o processo de criação de uma pesquisa.

2. Insira um nome de pesquisa e uma descrição opcional para a pesquisa.

3. Defina seus critérios de pesquisa. Você pode adicionar condições para a pesquisa usando os cartões de condição pré-criados ou usando nomes de propriedades de pesquisa na consulta de palavra-chave. Para obter mais informações, consulte [Build Search queries](build-search-queries.md).

4. Escolha os locais de conteúdo (fontes de dados) a serem pesquisados. Você pode fazer o escopo da pesquisa selecionando os locais de conteúdo de pessoas de interesse específicas (se você adicionou qualquer uma à investigação). Se você tiver adicionado pessoas de interesse para a investigação, poderá adicioná-las seguindo as etapas em [gerenciar pessoas de interesse](manage-people-of-interest.md#add-people-of-interest).
 
    Em alguns casos, você pode precisar pesquisar todos os locais de conteúdo em sua organização. Como alternativa, talvez seja necessário pesquisar locais que não pertencem a uma pessoa específica. Nesses cenários, você pode optar por Pesquisar toda a organização ou todos os locais de serviços específicos do Office 365 (como o Exchange, o SharePoint, o OneDrive of Business ou o Teams.

5. Salve e execute a pesquisa.

Após a criação da pesquisa, uma página de submenu é exibida com detalhes sobre a pesquisa. Observe que os botões **estatísticas** e **Visualização** estão esmaecidos inicialmente porque a pesquisa não foi concluída. Você pode acompanhar o progresso do ao monitorar a coluna **status** na guia **pesquisas** .

## <a name="view-statistics-and-search-results"></a>Exibir estatísticas e resultados de pesquisa

Depois de criar e iniciar uma pesquisa de investigação de dados, a ferramenta usará os critérios de pesquisa (a consulta de pesquisa e os locais de conteúdo) que você definiu e pesquisará um índice no serviço ativo para itens que correspondam aos critérios de pesquisa. Há três componentes de uma pesquisa que são retornados quando a pesquisa é concluída: 

- **Estimativa** -como a pesquisa procura apenas um índice (e não os locais de conteúdo real), os resultados de uma pesquisa são uma estimativa (com base no que foi encontrado no índice que corresponde aos resultados da pesquisa). Um resumo da estimativa é exibido na página de submenu de pesquisa em **status**. Observe que o status do processo de previsão de uma pesquisa é exibido na guia **pesquisas** da coluna **status da estimativa** . Quando a previsão de pesquisa é concluída, esse status é definido como **bem-sucedido**.

- **Estatísticas** -estatísticas fornecem informações mais detalhadas sobre os resultados da pesquisa. Isso inclui:

    - Resumo-estatísticas semelhantes aos resultados da estimativa de pesquisa exibidos na página do menu de atalho.
    - Principais locais-estatísticas sobre o número de itens que correspondem à consulta de pesquisa em cada local de conteúdo pesquisado. 
    - Consultas – estatísticas detalhadas sobre a consulta de pesquisa, incluindo o número de itens que correspondem a cada condição em uma consulta de pesquisa.

    Clique em **estatísticas** na página do menu de atalho para exibir essas estatísticas. Observe que esse botão está inativo até que o valor do **status estimado** na guia **pesquisas** seja definido como **bem-sucedido**. Para obter mais informações sobre estatísticas de pesquisa, confira [Estatísticas de pesquisa](search-statistics.md).

- **Visualização** -quando a pesquisa estiver concluída, você poderá exibir os itens reais de um subconjunto de exemplo dos resultados da pesquisa retornados pela pesquisa. Você pode exibir no modo de exibição nativo do tipo de item, qualquer um você também pode exibir metadados sobre o item. Essa é uma boa maneira de determinar rapidamente se os resultados da pesquisa são o que você esperava ou se precisa editar a pesquisa e executá-la novamente. Clique em **Visualizar** na página do menu de atalho para exibir itens dos resultados da pesquisa. Observe que esse botão está inativo até que o valor do **status de visualização** na guia **pesquisas** seja definido como **bem-sucedido**.
 
> [!NOTE]
> Os valores de status das colunas status da **previsão** e **status da visualização** na guia **pesquisas** são **enviados**, **em andamento**e **com êxito**. Se houver um erro com a pesquisa, o status de **falha** será exibido.

## <a name="add-search-results-to-evidence"></a>Adicionar resultados de pesquisa a evidências

Quando estiver satisfeito com os resultados de uma pesquisa e estiver pronto para analisar e corrigir os resultados da pesquisa, você poderá adicioná-los a uma evidência definida na investigação. Quando você adiciona itens a uma evidência definida na guia **evidência** , ocorrem as duas ações a seguir:

- Todos os itens nos resultados da pesquisa são copiados da fonte de dados no serviço Live e copiados para um local seguro de armazenamento do Azure na nuvem da Microsoft.

- Todos os itens (incluindo o conteúdo e os metadados) são re-indexados para que todos os dados do conjunto de evidências sejam totalmente pesquisáveis durante a investigação. A reindexação dos dados resulta em pesquisas completas e muito rápidas quando você pesquisa os dados no conjunto de evidências durante sua investigação.

Uma vantagem de copiar os dados dinâmicos para um conjunto de evidências no Azure é que, para incidentes críticos ou temporais, você pode facilmente conter os danos, excluindo imediatamente o conteúdo suspeito na fonte de dados original no serviço Live e, em seguida, investigando o incidente analisando as evidências que foram copiadas para o ambiente em quarentena do local de armazenamento do Azure. 

Copiar os dados originais para o conjunto de evidências também facilita sua investigação, fornecendo ferramentas avançadas de análise, como detecção de temas, detecção de duplicidade próxima e identificação de thread de email.

Se necessário, você também pode adicionar dados de fontes de dados que não sejam do Office 365 a um conjunto de evidências para que ele seja armazenado junto com os dados coletados do Office 365.

Para adicionar dados a um conjunto de evidências, selecione uma pesquisa na guia **pesquisas** e, em seguida, clique em **Adicionar resultados a evidências** na página do menu suspenso. Observe que você pode adicionar dados a um conjunto de evidência existente ou criar um novo conjunto de evidências imediatamente.

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a>Acompanhar o progresso de adição de resultados de pesquisa a evidências

A adição de dados a um conjunto de evidências é um processo de execução demorada. O processo inclui coletar os itens da fonte de dados original do Office 365 (por exemplo, de caixas de correio e sites), copiá-los para o local de armazenamento do Azure (esse processo de cópia também é chamado de *inclusão*) e, em seguida, indexar novamente os itens. Você pode controlar o progresso na guia **trabalhos** ou na guia **pesquisas** da coluna **Adicionar dados à evidência** . Depois que o processamento do processamento de evidências estiver concluído, você poderá ir para a guia **evidência** , clicar no conjunto de evidências e, em seguida, iniciar sua investigação pesquisando, revisando, marcando e exportando os dados relevantes conforme necessário.