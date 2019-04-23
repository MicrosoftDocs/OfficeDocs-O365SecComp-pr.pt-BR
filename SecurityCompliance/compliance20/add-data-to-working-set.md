---
title: Adicionar os resultados da pesquisa a um conjunto de trabalho
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
ms.openlocfilehash: 7830b483190a69e6055fae369580064c5df42f49
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958282"
---
# <a name="add-search-results-to-a-working-set"></a>Adicionar os resultados da pesquisa a um conjunto de trabalho

Depois de identificar e reinstalado as pesquisas em relação ao Exchange, SharePoint e OneDrive for Business, você pode adicionar os resultados a um conjunto de trabalho. Os conjuntos de trabalho representam um conjunto estático de documentos que iremos indexar os resultados de pesquisa rápida do Lightning, analisar a identificação de thread de email, a detecção de duplicidades e temas próximos.  Você também pode adicionar dados de fontes de dados que não sejam do Office 365 ao vivo lado a lado com os dados coletados do Office 365.

Para adicionar dados a um conjunto de trabalho, comece selecionando uma pesquisa, nos resultados da pesquisa sair, clique no botão *+ Adicionar resultados ao conjunto de trabalho* .

![Adicionando dados a um conjunto de trabalho](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

Você pode optar por adicionar a um conjunto de trabalho existente ou a um *novo conjunto de trabalho*.  Se estiver adicionando a um novo conjunto de trabalho, especifique o nome e finalmente clique no botão *Adicionar* .

![Selecionar um conjunto de trabalho](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

A adição de dados a um conjunto de trabalho é um processo de execução demorada, você pode controlar o progresso na guia trabalhos ou na coluna *status do conjunto de trabalho* na guia *pesquisas* .  O processo inclui a coleta de itens do Office 365 e, por fim, a indexação do & de inGestão.  Depois que o processamento do conjunto de trabalho for concluído, você poderá navegar até o conjunto de trabalho clicando na guia *conjuntos de trabalho* e, em seguida, clicando no conjunto de trabalho.  Você pode prosseguir para a pesquisa, revisão, marcação e exportação de quaisquer dados relevantes.

## <a name="adding-a-sample-to-a-working-set"></a>Adicionar um exemplo a um conjunto de trabalho

Se quiser validar seus resultados de pesquisa mais thorougly antes de coletar todos os documentos que foram recuperados por sua pesquisa, você pode adicionar uma amostra aleatória dos resultados da pesquisa a um conjunto de trabalho, em vez de adicionar tudo.

Para adicionar um exemplo a um conjunto de trabalho, comece selecionando uma pesquisa, no submenu de resultados da pesquisa, clique em *exemplo* de botão.

Em seguida, você pode escolher o parâmetro de sua amostra. Há duas opções:
- Nível de confiança e intervalo: o tamanho da amostra será escolhido para atender aos parâmetros estatísticos fornecidos.
- Porcentagem: o tamanho da amostra será determinado com base no número de itens retornados pela pesquisa e no parâmetro escolhido.

Por fim, escolha o conjunto de trabalho para o qual adicionar o exemplo. A partir daí, você pode verificar o status do processo exatamente como faria para adicionar uma pesquisa inteira em um conjunto de trabalho. 