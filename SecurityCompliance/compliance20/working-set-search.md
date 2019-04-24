---
title: Consultar os dados em um conjunto de trabalho
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
ms.openlocfilehash: 3000a066bf69f71327801035e7c270cc602565ac
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263803"
---
# <a name="query-the-data-in-a-working-set"></a>Consultar os dados em um conjunto de trabalho

Na maioria dos casos, será útil ser capaz de se aprofundar em um conjunto de trabalho e organizá-los para análise mais eficiente. As consultas em um conjunto de trabalho permitem que você faça isso, permitindo que você se concentre em um subconjunto de documentos que atendem aos critérios definidos por você ao mesmo tempo.

## <a name="creating-and-running-a-query-within-a-working-set"></a>Criar e executar uma consulta dentro de um conjunto de trabalho

Para criar e executar uma consulta dentro do seu conjunto de trabalho, clique em "nova consulta" em seu conjunto de trabalho. Depois de nomear sua consulta e definir as condições, clique em "salvar" para executar a consulta. Para executar uma consulta que tenha sido salva anteriormente, basta clicar na consulta salva. Consulte os [campos de metadados do documento](document-metadata-fields.md) para obter uma lista de metadados que você pode pesquisar.

## <a name="building-your-query"></a>Criar sua consulta

Você pode criar sua consulta usando uma combinação de cartões de condição e linguagem de consulta no cartão de condição de palavras-chave. Você pode agrupar cartões de condição juntos como um bloco para criar uma consulta mais complexa.

### <a name="condition-card"></a>Cartão de condição

Cada campo pesquisável em um conjunto de trabalho tem um cartão de condição correspondente que você pode usar para criar sua consulta.

Há vários tipos de cartões de condição:
- FREETEXT: o cartão de condição do freetext é usado para campos de texto como o assunto. Você pode listar vários termos de pesquisa separando-os com uma vírgula.
- Date: o cartão de condição de data é usado para campos de data, como data da última modificação.
- Opções de pesquisa: o cartão de condição opções de pesquisa fornecerá uma lista de valores possíveis para o campo específico em seu conjunto de trabalho. Isso é usado para campos, como remetente, onde há um número finito de valores possíveis em seu conjunto de trabalho.
- Palavra-chave: cartão de condição de palavra-chave é uma instância específica do cartão de condição FREETEXT que você pode usar para pesquisar termos ou usar o idioma de consulta do KQL. Veja mais detalhes abaixo.

### <a name="query-language"></a>Linguagem de consulta

Além de cartões de condição, você pode usar um idioma de consulta do tipo KQL no cartão de palavras-chave para criar sua consulta. A linguagem de consulta oferece suporte à sintaxe KQL padrão como e, ou, não e NEAR (n). Também suporta curingas de caractere único (?) e curinga de vários caracteres (*).

## <a name="filter"></a>Filtrar

Além das consultas que você pode salvar, você pode sobrepor mais condições de imediato aos resultados da consulta usando filtros. Os filtros diferem das consultas de algumas maneiras significativas:
- Os filtros são temporários (ou seja, não persistem em diferentes sessões), enquanto as consultas são salvas no conjunto de trabalho.
- Os filtros são sempre aditivos; os filtros serão aplicados na parte superior da consulta que você tem em vigor no momento, ao passo que a aplicação de uma consulta substituirá a consulta em vigor.