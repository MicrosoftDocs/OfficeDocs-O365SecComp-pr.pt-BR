---
title: Analisar dados em um conjunto de trabalho no eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
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
ms.openlocfilehash: 68a8b7586700a9bffe78f2b3a4ff419a1f85ba8a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695137"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a>Analisar dados em um conjunto de trabalho no eDiscovery avançado (Preview)

Quando o número de documentos coletados for muito grande, pode ser muito difícil revisar todas elas. EDiscovery avançado (Preview) fornece várias ferramentas para analisar os documentos para reduzir o volume de documentos seja revisada sem que ocorra perda em informações e para ajudá-lo a organizar os documentos de maneira coerente. Para saber mais sobre esses recursos, consulte:

- [Perto de detecção de duplicatas](near-duplicates.md)
- [Email threading](email-threading.md)
- [Temas](themes.md)

Para analisar os dados em um conjunto de trabalho:

1. Defina configurações de análise para seu caso. Para obter mais informações, consulte [Configurar definições de pesquisa e análise](configure-search-analytics-settings.md).
2. Abra o conjunto de trabalho que deseja analisar.
3. Vá para "Gerenciar o conjunto de trabalho".
4. Clique em "Analisar".

Você pode verificar o andamento da análise na guia trabalhos no seu caso.

 Depois que a análise for concluída, você pode exibir o relatório de análise, executar consultas em seu trabalho definir em saídas da análise (para obter mais informações, consulte [consulta dentro de seu trabalho definido](working-set-search.md)) e ver os documentos relacionados de um certo documento (para mais informações, consulte [ Analisando dados no conjunto de trabalho](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>Relatório de análise

Para exibir um relatório de análise para seu conjunto de trabalho:

1. Abra o conjunto de trabalho.
2. Vá para "Gerenciar o conjunto de trabalho".
3. Clique em "Relatório".

O relatório tem quatro componentes de análise:

- **Divisão** - quantos emails, anexos e afastados documentos foram encontrados no conjunto de trabalho.

- **Documentos (excluindo anexos)** - quantos documentos afastados foram dinamização, exclusiva próximo duplicatas de uma tabela dinâmica ou uma duplicata exata de outro documento.

- **Emails** - quantos emails foram inclusives, inclusive cópias, inclusive desvantagens ou nenhuma das perguntas acima.

- **Anexos** - quantos anexos de email foram exclusivos ou duplica de um anexo de email diferentes dentro do conjunto de trabalho.