---
title: Analisar dados em um conjunto de revisão na descoberta eletrônica avançada
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: cfed07d473f2af367de4cb2e9fe924a29e4123cd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155203"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a>Analisar dados em um conjunto de revisão na descoberta eletrônica avançada

Quando o número de documentos coletados é grande, pode ser muito difícil examiná-los. A descoberta eletrônica avançada fornece várias ferramentas para analisar os documentos para reduzir o volume de documentos a serem revisados sem perda de informações e para ajudá-lo a organizar os documentos de forma coerente. Para saber mais sobre esses recursos, confira:

- [Detecção de duplicata próxima](near-duplicates.md)

- [Conversa de email](email-threading.md)

- [Temas](themes.md)

Para analisar dados em um conjunto de revisão:

1. Defina as configurações de análise para o seu caso. Para obter mais informações, consulte [Configurar definições de pesquisa e análise](configure-search-analytics-settings.md).

2. Abra o conjunto de revisão que você deseja analisar.

3. Clique em **gerenciar análise definida**.

4. Clique em **analisar**.

Você pode verificar o progresso da análise na guia **trabalhos** da ocorrência.

 Após a conclusão da análise, você pode exibir o relatório de análise, executar consultas em seu conjunto de análise em saídas da análise (consulte [consulta dentro de seu conjunto de análise](review-set-search.md)) e ver documentos relacionados de um determinado documento (consulte revisando [dados no conjunto de revisão](reviewing-data-in-review-set.md)).

## <a name="analytics-report"></a>Relatório de análise

Para exibir um relatório de análise para um conjunto de análise:

1. Abra o conjunto de revisão.

2. Clique em **gerenciar análise definida**.

3. Clique em **relatório**.

O relatório tem quatro componentes da análise:

- **Divisão** -quantas mensagens de email, anexos e documentos soltos foram encontrados no conjunto de revisão.

- **Documentos (exceto anexos)** : Quantos documentos soltos foram dinâmicos, únicos duplicatas próximas de uma tabela dinâmica ou uma duplicata exata de outro documento.

- **Emails** -quantas mensagens de email foram inclusivas, cópias inclusivas, inclusive minuses ou nenhuma das opções acima.

- **Attachments** -quantos anexos de email são exclusivos ou duplicados de um outro anexo de email no conjunto de revisão.