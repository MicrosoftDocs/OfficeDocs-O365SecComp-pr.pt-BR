---
title: Analisar dados em evidência
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
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31029844"
---
# <a name="review-data-in-evidence"></a>Analisar dados em evidência

**Evidence** é um instantâneo dos resultados de pesquisa coletados. Quando você adiciona resultados de pesquisa a evidências, um processo é disparado para extrair arquivos, metadados e texto. Em seguida, o sistema cria um novo índice de todos os dados e adiciona à **evidência**. 

Para qualquer incidentes que confiram tempo, isso permite que você contenha rapidamente o ambiente, excluindo dados em locais originais ao investigar evidências recriadas em um ambiente em quarentena. Depois que a evidência é coletada, você pode revisar documentos individuais em seu formato nativo, formato de texto ou um formato Near-Native. Além disso, você pode executar consultas para restringir os dados por intervalo de tempo, tipos de arquivo, proprietários de dados e muitas outras placas de condição. Usando cartões de criação/remetente/destinatário, você pode examinar rapidamente quem está envolvido no despejo e se houve qualquer compartilhamento externo. Para obter mais informações, consulte:

  - [Consultar os dados em evidência](evidence-query.md)

Para agrupar documentos e obter mais assistência para revisão, clique em **gerenciar evidência**. No bloco de **análise** , clique em **analisar**. Isso executará análises avançadas, como detecção de duplicidades, encadeamento de emails e análise de tema. Posteriormente, você pode ver os temas gerais dos dados e também organizar documentos por threads de email, duplicatas exatas e quase duplicatas para facilitar sua investigação. Para obter mais informações, consulte:

  - [Executar a análise para investigar mais rápido](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a>Exibir documentos em evidência

A investigação de dados (visualização) exibe o conteúdo através de vários visualizadores, cada um com finalidades diferentes. Os vários visualizadores podem ser usados clicando em qualquer documento em **evidência**. Os visualizadores atualmente fornecidos são:

- Metadados de arquivo
- Modo de exibição nativo
- Exibição de texto
- Modo de anotações
- Exibição conVertida

## <a name="file-metadata"></a>Metadados de arquivo

Este painel pode ser ativado/desativado para exibir vários metadados associados ao documento. Embora a grade de resultados de pesquisa possa ser personalizada para exibir metadados específicos, há situações nas quais rolar horizontalmente pode ser difícil durante a análise de dados. O painel metadados de arquivo permite que um usuário alterne em um modo de exibição no visualizador.

![Painel metadados de arquivo
](../media/Reviewimage2.png)

## <a name="native-view"></a>Modo de exibição nativo

O visualizador nativo exibe o modo de exibição mais avançado de um documento. Ele oferece suporte a centenas de tipos de arquivo e deve exibir a experiência nativa mais verdadeira possível. Para arquivos do Microsoft Office, por exemplo, o visualizador aproveita o Office Online para exibir conteúdo como comentários de documento, fórmulas do Excel, linhas/colunas ocultas, anotações do PowerPoint, etc. Para obter mais informações sobre os visualizadores do Office Online \[, visite aqui é necessário vincular\]

![Modo de exibição nativo
](../media/Reviewimage3.png)

## <a name="text-view"></a>Exibição de texto

O Visualizador de texto fornece um modo de exibição do texto extraído de um arquivo. Ele ignora todas as imagens e formatação inseridas, mas será um modo de exibição de alto desempenho se um usuário estiver tentando entender o conteúdo rapidamente. O modo de exibição de texto também inclui outros recursos:

  - O contador de linhas facilita a referência a partes específicas de um documento

  - Realce de visitas de pesquisa que realçará os termos no documento, bem como o ScrollBar

  - O modo de exibição de comparação fornece um modo de exibição de comparação que realça diferenças textuais ao exibir documentos próximos duplicados

![Exibição de texto
](../media/Reviewimage4.png)

![Exibição de comparação
](../media/Reviewimage5.png)

## <a name="annotate-view"></a>Modo de anotações

O modo de anotações fornece recursos que permitem que os usuários apliquem marcações em um documento durante a investigação, incluindo:

  - Redação de área – os usuários podem desenhar uma caixa no documento para ocultar conteúdo confidencial

  - Lápis – os usuários podem fazer o desenho de forma livre em um documento para dar atenção a certas partes de um documento

  - Selecionar anotações-os usuários podem selecionar anotações em um documento para excluir

  - Alternar transparência da anotação – torna as anotações semitransparentes para exibir o conteúdo por trás da anotação

  - Página anterior – navega para a página anterior

  - Próxima página – navega para a próxima página

  - Ir para página – o usuário pode inserir um número de página específico para navegar até

  - Zoom – definir o nível de zoom para o modo de anotações

  - Girar – o usuário pode girar o documento no sentido horário

  - Pesquisa: o usuário pode pesquisar dentro de um documento e navegar até os vários acertos no documento
    
    ![Modo de anotações
    ](../media/Reviewimage1.png)

Observe que essas anotações estão nos dados coletados como evidência, e não em seu local original no sistema ativo. 

## <a name="more-information"></a>Mais informações

A tabela a seguir lista os limites para evidências em investigações de dados (prévia).  Todos os itens que excederem os máximos de arquivo serão exibidos como erros de processamento.
    
  |**Descrição do limite**|**Limite**|
  |:-----|:-----|
  |Número máximo de coletas de evidências  <br/> |50  <br/> |
  |Número total de documentos que podem ser incluídos em um caso (para todas as coleções de evidências na investigação)  <br/> |1 milhão  <br/> |
  |Tamanho total do arquivo por carga  <br/> |100 GB  <br/> |
  |Tamanho máximo de um único arquivo   <br/> |100 MB  <br/> |
  |Número máximo de caracteres extraídos de um único arquivo  <br/> |10 milhões  <br/> |
  |Profundidade de itens incorporados em um documento  <br/> |25  <br/> |
  