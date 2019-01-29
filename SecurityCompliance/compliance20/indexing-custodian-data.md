---
title: Indexação dos dados dos responsáveis avançada
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
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607306"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexação dos dados dos responsáveis avançada

Quando um funcionário encarregado é adicionado a um caso de eDiscovery avançado (Preview), qualquer conteúdo no Office 365 foi considerada como parcialmente indexado é re-processado para torná-la totalmente pesquisável.  Esse processo é chamado de *indexação avançada*. O conteúdo pode ser indexado parcialmente para vários motivos, inclusive a existência de imagens, tipos de arquivo incompatíveis ou quando os limites de tamanho de arquivo indexação forem encontrados.  Para saber mais sobre itens indexados parcialmente, consulte [parcialmente indexados itens na pesquisa de conteúdo no Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Exibição de resultados avançados de indexação

Quando o processo de indexação avançado for concluído, você pode obter uma compreensão da eficácia do processamento novamente.  Na exibição de indexação dos responsáveis, o gráfico lista todos os itens adicionados ao *índice híbrida*.  O índice de híbrido é onde o eDiscovery avançado (Preview) armazena o conteúdo de re-processado.

O gráfico também inclui o número de itens que exigem remediação e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [correção de erro durante o processamento de dados](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Atualização de índices avançadas para responsáveis

Quando um funcionário encarregado é adicionado a um caso de eDiscovery avançado (Preview), todos os itens indexados parcialmente são processados novamente. No entanto, como passar do tempo, itens indexados mais parcialmente podem ser adicionados à caixa de correio de um usuário ou conta de OneDrive.  Quando necessário, você poderá atualizar os índices.

> [!NOTE]
> Atualização de índices dos responsáveis é um processo em tempo de execução. É recomendável que você não atualizar índices mais de uma vez por dia em um caso.
