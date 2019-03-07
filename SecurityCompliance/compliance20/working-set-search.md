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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454983"
---
# <a name="query-the-data-in-a-working-set"></a>Consultar os dados em um conjunto de trabalho

Na maioria dos casos, será útil ser capaz de se aprofundar em um conjunto de trabalho e organizá-los para análise mais eficiente. As consultas em um conjunto de trabalho permitem que você faça isso, permitindo que você se concentre em um subconjunto de documentos que atendem aos critérios definidos por você ao mesmo tempo.

## <a name="creating-and-running-a-query-within-a-working-set"></a>Criar e executar uma consulta dentro de um conjunto de trabalho

Para criar e executar uma consulta dentro do seu conjunto de trabalho, clique em "nova consulta" em seu conjunto de trabalho. Depois de nomear sua consulta e definir as condições, clique em "salvar" para executar a consulta. Para executar uma consulta que tenha sido salva anteriormente, basta clicar na consulta salva. Consulte os [campos de metadados do documento](document-metadata-fields.md) para obter uma lista de metadados que você pode pesquisar.

## <a name="building-your-query"></a>Criar sua consulta

Você pode criar sua consulta usando uma combinação de cartões de condição e linguagem de consulta no cartão de condição de palavras-chave.

### <a name="condition-card"></a>Cartão de condição

Cada campo pesquisável em um conjunto de trabalho tem um cartão de condição correspondente que você pode usar para criar sua consulta.

Há vários tipos de cartões de condição:
- FREETEXT: o cartão de condição do freetext é usado para campos de texto como o assunto. Você pode listar vários termos de pesquisa separando-os com uma vírgula.
- Date: o cartão de condição de data é usado para campos de data, como data da última modificação.
- Opções de pesquisa: o cartão de condição opções de pesquisa fornecerá uma lista de valores possíveis para o campo específico em seu conjunto de trabalho. Isso é usado para campos como remetente, onde há um número finito de valores possíveis em seu conjunto de trabalho.
- Palavra-chave: cartão de condição de palavra-chave é uma instância específica do cartão de condição FREETEXT que você pode usar para pesquisar termos ou usar o idioma de consulta do KQL. Veja mais detalhes abaixo.

### <a name="query-language"></a>Linguagem de consulta

Além de cartões de condição, você pode usar um idioma de consulta do tipo KQL no cartão de palavras-chave para criar sua consulta. A linguagem de consulta oferece suporte à sintaxe KQL padrão como e, ou, não e NEAR (n). Também suporta curingas de caractere único (?) e curinga de vários caracteres (*).