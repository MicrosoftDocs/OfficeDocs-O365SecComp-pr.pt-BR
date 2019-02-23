---
title: Editar em massa pesquisas de conteúdo no centro de &amp; conformidade de segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Use o editor de pesquisa em massa no centro de &amp; conformidade de segurança do Office 365 para alterar rapidamente os locais de consulta e conteúdo para uma ou mais pesquisas de conteúdo.
ms.openlocfilehash: ff96beacdde3192db65c5eb31d14649c6bed4afc
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214881"
---
# <a name="bulk-edit-content-searches-in-the-office-365-security-amp-compliance-center"></a>Editar em massa pesquisas de conteúdo no centro de &amp; conformidade de segurança do Office 365

Você pode usar o editor de pesquisa em massa no centro de &amp; conformidade de segurança do Office 365 para editar várias pesquisas de conteúdo ao mesmo tempo. O uso dessa ferramenta permite que você altere rapidamente os locais de consulta e conteúdo para uma ou mais pesquisas. Em seguida, você pode executar novamente as pesquisas e obter os resultados de pesquisa estimados para as pesquisas revisadas. O editor também permite copiar e colar as consultas e os locais de conteúdo de um arquivo do Microsoft Excel ou arquivo de texto. Isso significa que você pode usar a ferramenta de estatísticas de pesquisa para exibir as estatísticas de uma ou mais pesquisas, exportar as estatísticas para um arquivo CSV, onde você pode editar as consultas e os locais de conteúdo no Excel. Em seguida, use o editor de pesquisa em massa para adicionar as consultas revisadas e os locais de conteúdo às pesquisas. Após revisar uma ou mais pesquisas, você pode reiniciá-las e obter novos resultados de pesquisa estimados.
  
Para obter mais informações sobre como usar a ferramenta de estatísticas de pesquisa, consulte [exibir estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Usar o editor de pesquisa em massa para alterar consultas

1. No centro de &amp; conformidade de segurança, vá para pesquisa de \> **conteúdo**de **investigação de pesquisa &amp; ** .
    
2. Na lista de pesquisas, selecione uma ou mais pesquisas e, em seguida, clique em editor de **pesquisa em massa** ![no botão](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png)editor de pesquisa em massa.
    
    ![Selecione uma ou mais pesquisas e clique em editor de pesquisa em massa](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    As informações a seguir são exibidas na página **consultas** do editor de pesquisa em massa. 
    
    ![A página do editor de pesquisa em massa exibe as consultas para as pesquisas selecionadas](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a. a coluna de **pesquisa** exibe o nome da pesquisa de conteúdo. Conforme mencionado anteriormente, você pode editar a consulta para várias pesquisas. 
    
    b. a coluna **consulta** exibe a consulta para a pesquisa de conteúdo listada na coluna **pesquisa** . Se a consulta foi criada usando o recurso de lista de palavras-chave, as palavras-chave são separadas pelo `(c:s)`texto * * **. Isso indica que as palavras-chave estão conectadas pelo operador **or** . Além disso, se a consulta incluir condições, as palavras-chave e as condições serão separadas pelo texto * * `(c:c)` **. Isso indica que as palavras-chave (ou fases da palavra-chave) estão conectadas às condições pelo operador **and** . Por exemplo, na captura de tela anterior da ContosoSearch1 de pesquisa, a consulta KQL que é equivalente `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` a seria `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`.
    
3. Para editar uma consulta, clique na célula da consulta que você deseja alterar e siga um destes procedimentos. Observe que a célula é borda por uma caixa azul quando você clica nela.
    
   - Digite a nova consulta na célula. Observe que não é possível editar uma parte da consulta. Você precisa digitar a consulta inteira.
    
      Ou
    
    - Colar uma nova consulta na célula. Isso pressupõe que você tenha copiado o texto da consulta de um arquivo, como um arquivo de texto ou um arquivo do Excel.
    
4. Após editar uma ou mais consultas na página **consultas** , clique em **salvar**.
    
    A consulta revisada é exibida na coluna de **consulta** para a pesquisa selecionada. 
    
5. Clique em **fechar** para fechar o editor de pesquisa em massa. 
    
6. Na página **pesquisa de conteúdo** , selecione a pesquisa que você editou e clique em **Iniciar** pesquisa para reiniciar a pesquisa usando a consulta revisada. 
    
Veja algumas dicas para editar consultas usando o editor de pesquisa em massa:
  
- Copie a consulta existente (usando **Ctrl C** ) para um arquivo de texto. Edite a consulta no arquivo de texto e, em seguida, copie a consulta revisada e Cole (usando **Ctrl V** ) novamente na célula da página **consultas** . 
    
- Você também pode copiar consultas de outros aplicativos (como o Microsoft Word ou o Microsoft Excel). No enTanto, lembre-se de que você pode adicionar inadvertidamente caracteres não suportados a uma consulta usando o editor de pesquisa em massa. A melhor maneira de evitar que os caracteres não suportados seja apenas digitar a consulta em uma célula na página **consultas** . Como alternativa, você pode copiar uma consulta do Word ou Excel e colá-la no arquivo em um editor de texto sem formatação, como o bloco de notas da Microsoft. Em seguida, salve o arquivo de texto e selecione **ANSI** na lista suspensa **codificação** . Isso removerá qualquer formatação e caractere sem suporte. Em seguida, você pode copiar e colar a consulta do arquivo de texto para a página **consultas** . 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Usar o editor de pesquisa em massa para alterar locais de conteúdo

1. No editor de pesquisa em massa para uma ou mais pesquisas selecionadas, clique em **habilitar editor de local em massa**e, em seguida, clique no link **locais** que é exibido na página. 
    
    As informações a seguir são exibidas na página **locais** do editor de pesquisa em massa. 
    
    ![Clique em Habilitar editor de local em massa e, em seguida, clique em locais para adicionar ou remover locais de conteúdo](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **caixas de correio para pesquisar**esta seção exibe uma coluna para cada pesquisa de conteúdo selecionada e linha para cada caixa de correio incluída na pesquisa. Uma marca de marca indica que a caixa de correio está incluída na pesquisa. Você pode adicionar caixas de correio adicionais a uma pesquisa digitando o endereço de email da caixa de correio em uma linha em branco e, em seguida, clicando na caixa de seleção da pesquisa de conteúdo à qual deseja adicioná-lo. Ou você pode remover uma caixa de correio de uma pesquisa desmarcando a caixa de seleção.
    
    b. os **sites do SharePoint para pesquisar**esta seção exibe uma linha para cada site do SharePoint e do onedrive incluído em cada pesquisa de conteúdo selecionada. Uma marca de marca indica que o site está incluído na pesquisa. Você pode adicionar outros sites a uma pesquisa digitando a URL do site em uma linha em branco e, em seguida, clicando na caixa de seleção da pesquisa de conteúdo à qual deseja adicioná-lo. Ou você pode remover um site de uma pesquisa desmarcando a caixa de seleção.
    
    c. **outras opções de pesquisa**esta seção indica se itens não indexados e pastas públicas estão incluídos na pesquisa. Para incluí-los, certifique-se de que a caixa de seleção está marcada. Para removê-los, desmarque a caixa de seleção.
    
2. Após editar uma ou mais seções na página **locais** , clique em **salvar**.
    
    Os locais de conteúdo revisados são exibidos na seção apropriada para as pesquisas selecionadas.
    
3. Clique em **fechar** para fechar o editor de pesquisa em massa. 
    
4. Na página **pesquisa de conteúdo** , selecione a pesquisa que você editou e clique em **Iniciar** pesquisa para reiniciar a pesquisa usando os locais de conteúdo revisado. 
    
Veja algumas dicas para editar locais de conteúdo usando o editor de pesquisa em massa:
  
- Você pode editar pesquisas de conteúdo para pesquisar todas as caixas de correio ou sites na organização digitando **todos** em uma linha em branco na seção **caixas de correio para pesquisar** ou **sites do SharePoint para pesquisar** e clicando na caixa de seleção. 
    
- Você pode adicionar vários locais de conteúdo a uma ou mais pesquisas copiando várias linhas de um arquivo de texto ou de um arquivo do Excel e, em seguida, colando-as em uma seção na página **locais** . Após adicionar novos locais, certifique-se de marcar a caixa de seleção para cada pesquisa à qual deseja adicionar o local. 
    
    > [!TIP]
    > Para gerar uma lista de endereços de email para todos os usuários em sua organização, execute o comando do PowerShell na etapa 2 em [usar a pesquisa de conteúdo para pesquisar a caixa de correio e o site do onedrive for Business para obter uma lista de usuários](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Ou use o script em [criar uma lista de todos os locais do onedrive em sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) para gerar uma lista de todos os sites do onedrive for Business em sua organização. Observe que você terá que acrescentar a URL do seu domínio de meusite do organization's (por exemplo, https://contoso-my.sharepoint.com) para os sites do onedrive for Business criados pelo script. Depois de ter uma lista de endereços de email ou sites do OneDrive for Business, você pode copiá-los e colá-los na página **locais** no editor de pesquisa em massa. 
  
- Depois que você clicar em **salvar** para salvar as alterações no editor de pesquisa em massa, o endereço de email para caixas de correio adicionadas a uma pesquisa será validado. Se o endereço de email não existir, será exibida uma mensagem de erro dizendo que a caixa de correio não pode ser localizada. Observe que as URLs para sites não são validadas. 
  

