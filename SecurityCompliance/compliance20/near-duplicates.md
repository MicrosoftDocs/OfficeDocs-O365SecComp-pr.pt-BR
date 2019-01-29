---
title: Perto de detecção de duplicatas
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
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607324"
---
# <a name="near-duplicate-detection"></a>Perto de detecção de duplicatas

Considere a possibilidade de um conjunto de documentos seja revisada na qual um subconjunto baseia-se no mesmo modelo e tem principalmente o mesmo texto padronizado idioma, com algumas diferenças aqui e ali. Se um revisor pode identificar este subconjunto, revisar um deles inteiro e revise as diferenças para o restante, eles seriam não ter perdido quaisquer informações exclusivas enquanto aproveitando apenas uma fração do tempo que teria levado-los para ler todos os documentos na íntegra. Detecção de duplicatas quase agrupa documentos textualmente semelhantes juntos para ajudá-lo a tornar seu processo de revisão mais eficiente.

## <a name="how-does-it-work"></a>Como funciona?

Quando perto de detecção de duplicatas é executado, o sistema analisa todos os documentos com texto. Em seguida, ele se compara todos os documentos contra uns aos outros para determinar se os seu semelhança é maior que o limite estabelecido. Se for, os documentos são agrupados. Depois que todos os documentos foram comparados e agrupados, um documento a partir de cada grupo está marcado como "pivot"; na revisão seus documentos, você pode revisar um pivô primeiro e revise os outros documentos na mesma quase duplicado set, concentrando-se a diferença entre o pivot e o documento que está em revisão.