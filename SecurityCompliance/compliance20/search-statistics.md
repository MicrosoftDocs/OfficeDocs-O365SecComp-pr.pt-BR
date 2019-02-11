---
title: Estatísticas de pesquisa
ms.author: markjjo
author: esclee
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 0cfc1e5f04887cbdbcc0be8854fc50d6f9b5f1f2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706002"
---
# <a name="search-statistics"></a>Estatísticas de pesquisa

Uma maneira é possível validar os resultados de pesquisa é examinar as estatísticas em torno de seus resultados para certificar-se de que eles se alinham com suas expectativas. Quando uma pesquisa é concluída, as estatísticas de alto nível são mostradas no submenu de detalhes de pesquisa:
- Número e o volume de itens recuperados pela pesquisa
- Número e o volume de parcialmente indexados/não indexadas itens encontrados nos locais de pesquisa
- Número de caixas de correio e locais é pesquisado. Para exibir estatísticas mais detalhadas, clique em "Estatísticas" de submenu detalhes da pesquisa.

## <a name="summary"></a>Resumo

No modo de exibição de resumo, você pode ver os resultados da pesquisa classificados por tipo de local (por exemplo, Exchange). Para cada tipo de local, você pode ver:
- Número de locais que tiveram os itens que correspondem os critérios de pesquisa
- Número de itens a partir desses locais que correspondem os critérios de pesquisa
- Volume total de itens que correspondem os critérios de pesquisa.

## <a name="top-locations"></a>Locais principais

No modo de exibição de locais principais, você verá os locais individuais com mais correspondências. Para cada local, você verá:
- Nome do local (por exemplo, o URL do SharePoint)
- Tipo de local
- Número de itens que correspondem os critérios de pesquisa
- Volume total de itens que correspondem os critérios de pesquisa.

## <a name="queries"></a>Consultas

Se você tiver usado a palavra-chave de (c:s) ou linhas de palavra-chave em sua consulta, você pode ver a divisão da sua consulta no modo de exibição de consultas por tipo de local. Para cada tipo de local, você verá:

- Parte: essa coluna será têm a palavra "Principal" ou "Palavra-chave". "Principal" significa que a linha apresenta estatísticas em toda a consulta, enquanto "Palavra-chave" significa que um dos componentes de consulta.

- Consulta: o componente de consulta real na linha se refere ao. Se a parte é "Principal", esse será toda a consulta; Se a parte era "Palavra-chave", você verá um dos componentes de consulta aqui.
  
  - Quando você procura todas as caixas de correio conteúdoedição (especificando não qualquer palavra-chave), a consulta real é ( gt _ do tamanho = 0) para que todos os itens sejam retornados
  
  - Quando você pesquisa do SharePoint Online e OneDrive para sites corporativos, os dois seguintes componentes são adicionados:
    
    - NÃO IsExternalContent:1 - exclui qualquer conteúdo de uma organização local do SharePoint
    
    - NÃO isOneNotePage: 1 - exclui todos os arquivos do OneNote porque estes seriam duplicatas de qualquer documento que corresponde à consulta de pesquisa.

- Número de locais que tiveram os itens que correspondem os critérios de pesquisa.

- Número de itens a partir desses locais que correspondem os critérios de pesquisa.

- Volume total de itens que correspondem os critérios de pesquisa.

## <a name="refiners"></a>Refinadores

Para caixas de correio do Exchange, modo de exibição de refinadores proporciona divisões adicionais ItemClass, remetente e destinatário. Para cada valor refinador e local, você pode ver quantos documentos foram retornados na pesquisa.