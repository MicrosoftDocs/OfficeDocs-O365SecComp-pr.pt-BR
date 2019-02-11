---
title: Exibir as estatísticas de palavra-chave para resultados de Pesquisa de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Usar o recurso de estatísticas de pesquisa para exibir e comparar estatísticas para várias pesquisas de conteúdo na segurança do Office 365 &amp; Centro de conformidade. Você também pode configurar a lista de palavra-chave quando você cria ou edita uma consulta de pesquisa para obter estatísticas avançadas que mostram a quantos itens correspondem a cada palavra-chave ou frase de palavra-chave.
ms.openlocfilehash: 0f0258f228e296e48def8de16aabc068901dffc7
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27209802"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Exibir as estatísticas de palavra-chave para resultados de Pesquisa de Conteúdo

Depois de criar e executar uma pesquisa de conteúdo, você pode exibir estatísticas sobre os resultados de pesquisa estimados. Isso inclui um resumo dos resultados da pesquisa (semelhantes ao resumo dos resultados da pesquisa estimados exibido no painel de detalhes), as estatísticas de consulta, como o número de locais de conteúdo com os itens que correspondem à consulta de pesquisa e o nome de locais de conteúdo que possuem os itens mais coincidentes. Você pode exibir as estatísticas para pesquisas de conteúdo de um ou mais. Isso permite que você para comparar os resultados de pesquisas de várias rapidamente e tomar decisões sobre a eficácia das suas consultas de pesquisa.
  
Além disso, você pode configurar pesquisas de novas e existentes para retornar estatísticas para cada palavra-chave em uma consulta de pesquisa. Isso permite comparar o número de resultados para cada palavra-chave em uma consulta e para comparar as estatísticas de palavra-chave de várias pesquisas.
  
Você também pode baixar as estatísticas da pesquisa e as estatísticas de palavra-chave para um arquivo CSV. Isso permite usar os recursos de filtragem e classificação no Excel para comparar os resultados e preparação de relatórios para os resultados de pesquisa.
  
## <a name="get-statistics-for-content-searches"></a>Obtenha as estatísticas para pesquisas de conteúdo

Para exibir as estatísticas de pesquisas de conteúdo:
  
1. No Office 365 Security &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.
    
2. Na lista de pesquisas, selecione uma ou mais pesquisas e, em seguida, clique em **estatísticas da pesquisa**![botão estatísticas da pesquisa](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).
    
    ![Selecione várias pesquisas e clique em estatísticas da pesquisa](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. Na página **estatísticas da pesquisa** , clique em um dos links a seguir para exibir estatísticas sobre as pesquisas selecionadas. 
    
    **Resumo**
    
    Esta página exibe estatísticas semelhantes àquelas exibidas no painel de detalhes, na página de **pesquisa de conteúdo** . As estatísticas para todas as pesquisas selecionadas são exibidas. Observe que você pode também executar novamente as pesquisas selecionadas dessa página para atualizar as estatísticas. 
    
    ![Resumo das estatísticas para as pesquisas selecionadas](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    r. o nome da pesquisa conteúdo. Conforme indicado anteriormente, você pode exibir e comparar estatísticas para várias pesquisas.
    
    b. o tipo de local do conteúdo que foi pesquisado. Cada linha exibe estatísticas para caixas de correio, sites e as pastas públicas de pesquisa especificado.
    
    c. o número de locais de conteúdo que contém itens que correspondem à consulta de pesquisa. Para caixas de correio, essa estatística também inclui o número de caixas de correio de arquivamento que contêm os itens que correspondem à consulta de pesquisa.
    
    d. o número total de itens de todos os especificados locais de conteúdo que correspondem à consulta de pesquisa. Documentos, itens de calendário e mensagens de email são exemplos de tipos de item. Se um item contiver várias instâncias de uma palavra-chave que está sendo procurado, ele só é contado uma vez no número total de itens. Por exemplo, se você estiver procurando por palavras "stock" ou "fraude" e uma mensagem de email contém três instâncias da palavra "stock", ele é contado apenas uma vez na coluna **itens** . 
    
    e. o tamanho total de todos os itens encontrados no local especificado conteúdo que correspondem à consulta de pesquisa. 
    
    **Consultas**
    
    Esta página exibe estatísticas sobre a consulta de pesquisa.
    
    ![Estatísticas de consulta de pesquisa para as pesquisas selecionadas](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    r. o nome da pesquisa de conteúdo que a linha contém as estatísticas de consulta para.
    
    b. o tipo de conteúdo local que as estatísticas de consulta são aplicáveis a.
    
    c. essa coluna indica qual parte da consulta de pesquisa, as estatísticas são aplicáveis a. **Principal** indica a consulta de pesquisa inteira. Se você usar uma lista de palavra-chave quando você cria ou edita uma consulta de pesquisa, as estatísticas para cada componente da consulta estão incluídas nesta tabela. Consulte a seção [obter estatísticas de palavra-chave para pesquisas de conteúdo](#get-keyword-statistics-for-content-searches) deste artigo para obter mais informações. 
    
    d. essa coluna contenha a pesquisa real de consulta que executam a ferramenta de pesquisa de conteúdo. Observe que a ferramenta adiciona automaticamente alguns componentes adicionais à consulta que você criar. 

    - Quando você procura de todo o conteúdo em caixas de correio (especificando não qualquer palavra-chave), a consulta de palavra-chave real é `size>=0` para que todos os itens são retornados. 
    
     - Quando você pesquisa do SharePoint Online e OneDrive para sites corporativos, os dois seguintes componentes são adicionados:
    
          **Não IsExternalContent:1** - exclui qualquer conteúdo de uma organização local do SharePoint. 
    
          **Não IsOneNotePage:1** - exclui todos os arquivos do OneNote porque estes seriam duplicatas de qualquer documento que corresponde à consulta de pesquisa. 

    
    e. o número de locais de conteúdo (especificações de HttpCachePolicy o * * o tipo de local * * coluna) que contêm os itens que correspondem à consulta de pesquisa listada na coluna da **consulta** . 
    
    f. o número de itens que correspondem à consulta de pesquisa listada na coluna da **consulta** (a partir do seu local de conteúdo especificado). Conforme explicado anteriormente, se um item contiver várias instâncias de uma palavra-chave que está sendo pesquisado, ela será somente contada uma vez nesta coluna. 
    
    g. o tamanho total de todos os itens encontrados (no local especificado conteúdo) que correspondem à consulta de pesquisa na coluna da **consulta** . 
    
    **Locais principais**
    
    Esta página exibe estatísticas sobre o número de itens que correspondem à consulta de pesquisa em cada local de conteúdo que foi pesquisada. Os locais da parte superior a 1.000 são exibidos. Se você exibir estatísticas de várias pesquisas, os locais de 1.000 superior de cada pesquisa serão exibidos. Observe que um local de conteúdo não está incluído nesta página, se ele não contiver quaisquer itens que correspondem à consulta de pesquisa.
    
    ![Estatísticas sobre o número de itens encontrados em locais de conteúdo que foram pesquisados](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    r. o nome do local do conteúdo.
    
    b. o tipo de conteúdo local que as estatísticas de local são aplicáveis a.
    
    c. há colunas para cada que você estiver exibindo as estatísticas para pesquisa. Esta coluna mostra o número (e o tamanho total) de itens que correspondem à consulta de pesquisa em cada local de conteúdo. Observe que, quando você estiver exibindo as estatísticas para várias pesquisas, "NA" nessa coluna indica que o conteúdo local não foi incluído na pesquisa. 

## <a name="get-keyword-statistics-for-content-searches"></a>Obtenha as estatísticas de palavra-chave para pesquisas de conteúdo

Anterior conforme explicado, a página de **consultas** mostra a consulta de pesquisa e o número (e tamanho) de itens que correspondem à consulta. Se você usar uma lista de palavra-chave quando você cria ou edita uma consulta de pesquisa, você pode obter estatísticas avançadas que mostram a quantos itens correspondem a cada palavra-chave ou frase de palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais partes da consulta são mais (e menos) eficientes. Por exemplo, se uma palavra-chave retorna um grande número de itens, você pode escolher refinar a consulta de palavra-chave para restringir os resultados de pesquisa. Você pode configurar uma lista de palavra-chave quando você cria ou editar uma pesquisa de conteúdo. 




  
Para criar uma lista de palavra-chave e exibir estatísticas de palavra-chave para uma pesquisa de conteúdo:
  
1. No Office 365 Security &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.
    
2. Na lista de pesquisas de conteúdo, clique em e uma pesquisa e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Clique em **consulta** e, em seguida, fazer o seguinte: 
    
    ![Clique na caixa de seleção Mostrar palavra-chave lista e digite uma palavra-chave em cada linha](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    r. Clique na caixa de seleção **Mostrar lista de palavra-chave** . 
    
    b. Digite uma palavra-chave ou a fase de palavra-chave em uma linha da tabela de palavras-chave. Por exemplo, digite **orçamento** na primeira linha e digite **segurança** na segunda linha. 
    
4. Depois de adicionar as palavras-chave que você deseja pesquisar e obter as estatísticas para, clique em **pesquisa** para executar a pesquisa revisada. 
    
5. Quando a pesquisa for concluída, selecione-o na lista de pesquisas e, em seguida, clique em **estatísticas da pesquisa** ![botão estatísticas da pesquisa](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png). Você também pode exibir e comparar estatísticas de palavra-chave para várias pesquisas.
    
6. Na página **estatísticas da pesquisa** , clique em **consulta** para exibir as estatísticas de palavra-chave para as pesquisas selecionadas. 
    
    ![As estatísticas para cada palavra-chave para as pesquisas selecionadas são exibidas](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Conforme mostrado na captura de tela anterior, as estatísticas para cada palavra-chave são exibidas; Isso inclui: 
    
    - As estatísticas de palavra-chave para cada tipo de conteúdo local incluída na pesquisa.
    
    - A consulta de pesquisa real para cada palavra-chave, que inclui qualquer condições de consulta de pesquisa. 
    
    - A consulta de pesquisa completa (identificado como **principal** na coluna **parte** ) e as estatísticas para a consulta completa. Observe que essas são as mesmas estatísticas exibidas na página de **Resumo** . 

> [!NOTE]
> Para ajudar a reduzir problemas causados por palavra-chave grandes listas, agora você está limitado a um máximo de 20 linhas na lista de palavra-chave de uma consulta de pesquisa.
