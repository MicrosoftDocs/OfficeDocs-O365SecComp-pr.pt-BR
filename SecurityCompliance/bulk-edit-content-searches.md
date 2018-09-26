---
title: Pesquisas de conteúdo de segurança do Office 365 de editar em massa &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Use o Editor de pesquisa em massa no Office 365 Security &amp; Centro de conformidade para rapidamente alterar os locais de conteúdo e consulta de pesquisa de conteúdo de um ou mais.
ms.openlocfilehash: 9d6d48ff42bb3c99a30b9da1020253a5af24679b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038174"
---
# <a name="bulk-edit-content-searches-in-the-office-365-security-amp-compliance-center"></a>Pesquisas de conteúdo de segurança do Office 365 de editar em massa &amp; Centro de conformidade

Você pode usar o Editor de pesquisa em massa no Office 365 Security &amp; Centro de conformidade para editar várias pesquisas de conteúdo ao mesmo tempo. Usando essa ferramenta permite alterar rapidamente os locais de conteúdo e de consulta para um ou mais pesquisas. Em seguida, você pode executar novamente as pesquisas e obtenha novos resultados de pesquisa estimados para as pesquisas revisadas. O editor também permite que você copie e cole consultas e locais de conteúdo de um arquivo do Microsoft Excel ou o arquivo de texto. Isso significa que você pode usar a ferramenta de estatísticas de pesquisa para exibir as estatísticas de uma ou mais pesquisas, exportar as estatísticas para um arquivo CSV onde você pode editar as consultas e locais de conteúdo no Excel. Em seguida, você deve usar o Editor de pesquisa em massa para adicionar as consultas revisadas e os locais de conteúdo para as pesquisas. Após você ter revisado pesquisas de um ou mais, você pode novamente iniciá-los e obtenha novos resultados de pesquisa estimados.
  
Para obter mais informações sobre como usar a ferramenta de estatísticas da pesquisa, consulte [Exibir as estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Use o Editor de pesquisa em massa para alterar consultas

1. Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.
    
2. Na lista de pesquisas, selecione uma ou mais pesquisas e, em seguida, clique em **Editor de pesquisa em massa** ![botão Editor de pesquisa em massa](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png).
    
    ![Selecione uma ou mais pesquisas e clique em editor de pesquisa em massa](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    A seguinte informação é exibida na página de **consultas** do Editor de pesquisa em massa. 
    
    ![A página do editor de pesquisa em massa exibe as consultas para as pesquisas selecionadas](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    r. a coluna de **pesquisa** exibe o nome da pesquisa conteúdo. Conforme indicado anteriormente, você pode editar a consulta para várias pesquisas. 
    
    b. coluna o **consulta** exibe a consulta para a pesquisa de conteúdo listados na coluna de **pesquisa** . Se a consulta foi criada usando o recurso de lista de palavra-chave, as palavras-chave são separadas pelo texto * * `(c:s)` **. Isso indica que as palavras-chave estão conectadas pelo operador **OR** . Além disso, se a consulta incluir condições, as palavras-chave e as condições são separadas pelo texto * * `(c:c)` **. Isso indica que o keywords (ou fases de palavra-chave) estão conectados às condições pelo operador **e** . Por exemplo, na captura de tela anterior a para pesquisa ContosoSearch1, a consulta KQL que é equivalente a `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` seria `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`.
    
3. Para editar uma consulta, clique na célula da consulta que você deseja alterar e executando um dos aspectos a seguir. Observe que a célula é com borda por uma caixa azul quando você clicar nele.
    
   - Digite a nova consulta na célula. Observe que você não pode editar uma parte da consulta. Você precisa digitar a consulta inteira.
    
      Ou
    
    - Cole uma nova consulta na célula. Isso pressupõe que você tiver copiado o texto da consulta de um arquivo, como um arquivo de texto ou um arquivo do Excel.
    
4. Depois que você tiver editado uma ou mais consultas na página de **consultas** , clique em **Salvar**.
    
    A consulta revisada é exibida na coluna **consulta** para a pesquisa selecionada. 
    
5. Clique em **Fechar** para fechar o Editor de pesquisa em massa. 
    
6. Na página de **pesquisa de conteúdo** , selecione a pesquisa que você editou e clique em **Iniciar** a pesquisa para reiniciar a pesquisa usando a consulta revisada. 
    
Aqui estão algumas dicas para consultas usando o Editor de pesquisa em massa de edição:
  
- Copie a consulta existente (usando **Ctrl C** ) para um arquivo de texto. Editar a consulta no arquivo de texto e, em seguida, copie a consulta revisada e cole-(usando **Ctrl V** ) volta para a célula na página de **consultas** . 
    
- Você também pode copiar consultas de outros aplicativos (por exemplo, Microsoft Word ou Microsoft Excel). No entanto, lembre-se de que você pode adicionar inadvertidamente caracteres não aceitos para uma consulta usando o Editor de pesquisa em massa. Basta digitar a consulta em uma célula na página **consultas** é a melhor maneira de impedir que os caracteres não suportados. Como alternativa, você pode copiar uma consulta do Word ou Excel e colá-lo no arquivo em um editor de texto sem formatação, como o Microsoft Notepad. Em seguida, salve o arquivo de texto e selecione **ANSI** na lista suspensa **codificação** . Isto irá remover quaisquer caracteres não suportados e formatação. Você pode, em seguida, copie e cole a consulta do arquivo de texto para a página de **consultas** . 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Use o Editor de pesquisa em massa para alterar locais de conteúdo

1. Em massa pesquisa Editor para um ou mais pesquisas selecionadas, clique em **Habilitar o editor de local em massa**e, em seguida, clique no link de **locais** que é exibido na página. 
    
    A seguinte informação é exibida na página **locais** do Editor de pesquisa em massa. 
    
    ![Clique em editor de local Enable em massa e clique em locais para adicionar ou remover locais de conteúdo](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    r. **caixas de correio para pesquisar**esta seção exibe uma coluna para cada pesquisa de conteúdo selecionado e linha para cada caixa de correio que está incluída na pesquisa. Uma marca de seleção indica que a caixa de correio é incluída na pesquisa. Você pode adicionar caixas de correio adicionais para uma pesquisa digitando o endereço de email da caixa de correio em uma linha em branco e em seguida, clicando na caixa de seleção para a pesquisa de conteúdo que você deseja adicioná-lo ao. Ou você pode remover uma caixa de correio de uma pesquisa desmarcando a caixa de seleção.
    
    b. **sites do SharePoint para pesquisar**esta seção exibe uma linha para cada site do SharePoint e OneDrive incluídos em cada selecionado a pesquisa de conteúdo. Uma marca de seleção indica que o site é incluído na pesquisa. Você pode adicionar sites adicionais para uma pesquisa digitando a URL para o site em uma linha em branco e então e clicar na caixa de seleção para a pesquisa de conteúdo que você deseja adicioná-lo ao. Ou você pode remover um site de uma pesquisa desmarcando a caixa de seleção.
    
    c. **outras opções de pesquisa**nesta seção indica se os itens indexados e as pastas públicas estão incluídas na pesquisa. Para incluí-las, verifique se a caixa de seleção está selecionada. Para removê-los, desmarque a caixa de seleção.
    
2. Depois que você tiver editado um ou mais das seções na página **locais** , clique em **Salvar**.
    
    Os locais de conteúdo revisados são exibidos na seção apropriada para as pesquisas selecionadas.
    
3. Clique em **Fechar** para fechar o Editor de pesquisa em massa. 
    
4. Na página de **pesquisa de conteúdo** , selecione a pesquisa que você editou e clique em **Iniciar** a pesquisa para reiniciar a pesquisa usando os locais de conteúdo revisados. 
    
Aqui estão algumas dicas para locais de conteúdo usando o Editor de pesquisa em massa de edição:
  
- Você pode editar as pesquisas de conteúdo para pesquisar todas as caixas de correio ou sites na organização digitando **todos** em uma linha em branco na seção de **caixas de correio para pesquisar** ou **sites do SharePoint para pesquisar** e em seguida, clicando na caixa de seleção. 
    
- Você pode adicionar vários locais de conteúdo para uma ou mais pesquisas copiando várias linhas de um arquivo de texto ou de um arquivo do Excel e, em seguida, colando-las a uma seção na página **locais** . Depois de adicionar novos locais, certifique-se de selecionar a caixa de seleção para cada pesquisa que você deseja adicionar o local a ser. 
    
    > [!TIP]
    > Para gerar uma lista de endereços de email para todos os usuários em sua organização, execute o comando PowerShell na etapa 2 no [Uso de pesquisa de conteúdo para pesquisar a caixa de correio e OneDrive para site de negócios para obter uma lista de usuários](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Ou, use o script em [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) para gerar uma lista de todos os OneDrive para sites corporativos em sua organização. Observe que você vai ter que inclua o URL para seu do domínio de meusite da organização (por exemplo, https://contoso-my.sharepoint.com) para o OneDrive for sites corporativos que é criado pelo script. Depois que a lista de endereços de email ou OneDrive para sites corporativos, você pode copiar e colá-los à página **locais** no Editor de pesquisa em massa. 
  
- Após você clicar em **Salvar** para salvar alterações no Editor de pesquisa em massa, o endereço de email para caixas de correio que você adicionou a uma pesquisa será validado. Se o endereço de email não existir, será exibida uma mensagem de erro dizendo que a caixa de correio não pode ser localizada. Observe que as URLs para sites não são validados. 
  

