---
title: Preparar um arquivo CSV para uma lista de IDs de pesquisa de conteúdo no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Use o arquivo de Results.csv ou Items.csv não indexadas a partir de uma pesquisa de conteúdo existente para criar uma pesquisa de lista de identificação que retorna um mensagens de email específicos. Pesquisas de lista de ID geralmente são usadas para devolver os itens de caixa de correio parcialmente indexados.
ms.openlocfilehash: 28e4a66e5c9be1817881004b1e4b3a3e6d4bfdb9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524450"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>Preparar um arquivo CSV para uma lista de IDs de pesquisa de conteúdo no Office 365

Você pode pesquisar mensagens de email da caixa de correio específica e outros itens de caixa de correio usando uma lista de IDs do Exchange. Para criar uma pesquisa de ID de lista (formalmente chamada de uma pesquisa de destino), você enviar um arquivo (CSV) de valores separados por vírgula que identifica os itens de caixa de correio específica a ser pesquisado. O arquivo CSV você pode usar o arquivo de **Results.csv** ou o arquivo **Não indexadas Items.csv** que estão incluídos ao exportar os resultados de pesquisa de conteúdo ou exportar um relatório de pesquisa de conteúdo de e a pesquisa de conteúdo existente. Em seguida, você editar um desses arquivos para indicar os itens específicos para pesquisa e, em seguida, criar uma nova pesquisa de lista de ID e enviar o arquivo CSV. 
  
Eis uma rápida visão geral do processo de criação de uma pesquisa de ID de lista.
  
1. Criar e executar uma pesquisa de conteúdo novo ou guiada na segurança &amp; Centro de conformidade.
    
2. Exportar os resultados de pesquisa de conteúdo ou exportar o relatório de pesquisa de conteúdo. Para obter mais informações, consulte:
    
    - [Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
    - [Exportar um relatório da Pesquisa de Conteúdo](export-a-content-search-report.md)
    
3. Editar o arquivo **Results.csv** ou o **Items.csv não indexadas** e identificar os itens de caixa de correio específica que você deseja incluir na lista pesquisa ID. Consulte as [instruções](#prepare-the-csv-file-for-an-id-list-search) para preparar um arquivo CSV para uma pesquisa de ID de lista. 
    
4. Criar uma nova lista de ID Pesquisar (veja as [instruções](#create-an-id-list-search)) e enviar o arquivo CSV que você preparou. A consulta de pesquisa que é criada pesquisará apenas para os itens selecionados no arquivo CSV.
    
> [!NOTE]
> Pesquisas de lista de ID são permitidas apenas aos itens de caixa de correio. Não é possível pesquisar para SharePoint e pesquisa de lista de documentos do OneDrive em uma ID. 
  
 **Por que criar uma pesquisa de lista de ID?** Se você for capaz de determinar que se um item estiver respondendo a uma solicitação de descoberta eletrônica baseada nos metadados nos arquivos de **Results.csv** ou **Items.csv não indexados** , você pode usar uma pesquisa de ID de lista para localizar, visualize e exporte esse item para determinar se ele tiver sido definido respondendo ao caso de forma que você está investigando. Pesquisas de lista de ID são geralmente usadas para pesquisar e retornar um conjunto específico de itens indexados. 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>Preparar o arquivo CSV para uma pesquisa de ID de lista

Após exportar os resultados de pesquisa ou o relatório para uma pesquisa de conteúdo, você pode executar as seguintes etapas para preparar o arquivo CSV para uma pesquisa de ID de lista. Este arquivo CSV identificará cada item na pesquisa de ID de lista.
  
Observe que você pode usar um arquivo CSV de uma pesquisa que incluía contas do OneDrive e sites do SharePoint, mas você pode selecionar *apenas* os itens de caixa de correio para uma pesquisa de ID de lista. Se você selecionar um documento no SharePoint ou OneDrive, o arquivo CSV falhará validação quando você criar uma pesquisa de ID de lista. 
  
1. Abra o arquivo **Results.csv** ou **Items.csv não indexados** no Excel. 
    
2. Inserir uma nova coluna e nomeie-o **selecionados**. Não importa onde inserir a coluna. Para sua conveniência, considere a possibilidade de inseri-lo à esquerda da primeira coluna.
    
3. Na coluna **selecionado** , digite **Sim** na célula que corresponde ao item que você deseja pesquisar. Repita essa etapa para cada item que você deseja pesquisar. 
    
    > [!IMPORTANT]
    > Quando você abre o arquivo CSV no Excel, o formato de dados para a coluna de **ID de documento** é alterado para **Geral**. Isso resulta na exibição a ID de documento para um item no científico notação. Por exemplo, o documento que ID de "481037338205" é exibido como "4.81037E + 11" você precisará executar as próximas etapas para alterar o formato dos dados da coluna de **ID de documento** para o **número** para restaurar o formato correto para a ID do documento. Se você não fizer isso, haverá falha na pesquisa de lista de identificação que usa o arquivo CSV. 
  
4. Clique com o botão toda a coluna de **ID de documento** e selecione **Formatar células**.
    
5. Na caixa **categoria** , clique em **número**.
    
6. Alterar o número de casas decimais como **0**e clique em **Okey** para salvar suas alterações. Observe que os valores na coluna ID do documento são alterados para números. 
    
    Aqui está um exemplo da um arquivo CSV que está pronto para ser enviada para uma pesquisa de conteúdo de lista de ID.
    
    ![Exemplo de um arquivo CSV para uma pesquisa de conteúdo direcionado](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. Salve o arquivo CSV ou usar **Salvar como** para salvar o arquivo com o nome de arquivo diferente. Em ambos os casos, certifique-se de salvar o arquivo com o formato CSV. 
  
## <a name="create-an-id-list-search"></a>Criar uma pesquisa de ID de lista

A próxima etapa é criar uma nova pesquisa de conteúdo de lista ID e enviar o arquivo CSV que você preparou na etapa anterior.
  
> [!IMPORTANT]
> Você deve criar uma pesquisa de lista ID não mais de 2 dias após exportar os resultados ou o relatório de uma pesquisa de conteúdo. Se a pesquisa de resultados ou relatar onde exportados há mais de 2 dias, você deve exportar novamente os resultados de pesquisa ou relatório para gerar os arquivos CSV atualizados. Então, você pode preparar um dos arquivos CSV atualizados e usá-lo para criar uma pesquisa de ID de lista. 
  
1. Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**.
    
2. Na página de **pesquisa** , clique na seta ao lado de ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nova pesquisa**e clique em **Pesquisar por ID de lista**.
    
    ![Clique em Pesquisar por ID de lista, na lista suspensa de pesquisa novo](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. No submenu **Pesquisar por lista ID** , nomeie a pesquisa (e, opcionalmente, descreva-) e, em seguida, clique em **Procurar** e selecione o arquivo CSV que você preparou na etapa anterior. 
    
    O Office 365 tenta validar o arquivo CSV. Se a validação falhar, será exibida uma mensagem de erro que podem ajudá-lo a solucionar problemas de erros de validação. O arquivo CSV deve ser validado com êxito para criar uma pesquisa de ID de lista.
    
4. Após o CSV arquivo é validado com êxito, clique em **pesquisa** para criar a pesquisa de ID de lista. 
    
    Aqui está um exemplo de como os resultados de pesquisa estimados e a consulta que é gerada para uma pesquisa de ID de lista.
    
    ![Consulta de pesquisa para uma pesquisa de conteúdo direcionada no painel de detalhes](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    Observe que o número de itens estimados exibido em estatísticas para a pesquisa de ID deve corresponder o número de itens que você selecionou no arquivo CSV.
    
5. Visualizar ou exportar os itens retornados pela pesquisa lista ID.
    
> [!NOTE]
> Se você mover uma caixa de correio depois de criar uma pesquisa de ID de lista, a consulta para a pesquisa não devolvem os itens especificados. Isso ocorre porque a propriedade **DocumentId** para itens de caixa de correio são alteradas quando uma caixa de correio forem movida. Na instância rara quando uma caixa de correio é movida depois de criar uma pesquisa de ID de lista, você deve criar uma nova pesquisa de conteúdo (ou atualizar os resultados de pesquisa para a pesquisa de conteúdo existente) e, em seguida, exportar a pesquisa resulta ou relatar para gerar os arquivos CSV atualizados que podem ser usados  para criar uma nova pesquisa de lista de ID. 
