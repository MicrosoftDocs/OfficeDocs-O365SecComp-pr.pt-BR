---
title: Analisar dados em um conjunto de trabalho em descoberta eletrônica avançada (visualização)
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
ms.openlocfilehash: e3f3e863423fe4312a944eb6f04a58182e11665c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243232"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a>Analisar dados em um conjunto de trabalho em descoberta eletrônica avançada (visualização)

Quando o número de documentos coletados é grande, pode ser muito difícil examiná-los. A descoberta eletrônica avançada (prévia) fornece várias ferramentas para analisar os documentos para reduzir o volume de documentos a serem revisados sem perda de informações e para ajudá-lo a organizar os documentos de forma coerente. Para saber mais sobre esses recursos, confira:

- [Detecção de duplicata próxima](near-duplicates.md)
- [Conversa de email](email-threading.md)
- [Temas](themes.md)

Para analisar dados em um conjunto de trabalho:

1. Defina as configurações de análise para o seu caso. Para obter mais informações, consulte [Configurar definições de pesquisa e análise](configure-search-analytics-settings.md).
2. Abra o conjunto de trabalho que você deseja analisar.
3. Vá para "gerenciar conjunto de trabalho".
4. Clique em "analisar".

Você pode verificar o progresso da análise na guia trabalhos em seu caso.

 Após a conclusão da análise, você pode exibir o relatório de análise, executar consultas em seu conjunto de trabalho nas saídas da análise (para obter mais informações, confira [consulta em seu conjunto de trabalho](working-set-search.md)) e ver documentos relacionados de um determinado documento (para obter mais informações, consulte [ Revisão de dados no conjunto de trabalho](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>Relatório de análise

Para exibir um relatório de análise para seu conjunto de trabalho:

1. Abra seu conjunto de trabalho.
2. Vá para "gerenciar conjunto de trabalho".
3. Clique em "relatório".

O relatório tem quatro componentes da análise:

- **Divisão** -quantos emails, anexos e documentos soltos foram encontrados no conjunto de trabalho.

- **Documentos (exceto anexos)** : Quantos documentos soltos foram dinâmicos, únicos duplicatas próximas de uma tabela dinâmica ou uma duplicata exata de outro documento.

- **Emails** -quantos emails foram incluídos, cópias inclusivas, inclusive minuses ou nenhuma das opções acima.

- **Attachments** -quantos anexos de email foram exclusivos ou duplicados de um anexo de email diferente no conjunto de trabalho.