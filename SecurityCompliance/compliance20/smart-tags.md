---
title: Configurar marcas inteligentes para detecção de privilégio de cliente de advogado na descoberta eletrônica avançada
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153963"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a>Configurar marcas inteligentes para revisão assistida por ML na descoberta eletrônica avançada

Os recursos de aprendizado de máquina em descoberta eletrônica avançada têm como objetivo ajudar a tornar o processo de decisão sobre os documentos de forma mais eficiente. Marcas inteligentes é uma maneira de trazer os recursos de aprendizado de máquina para onde as decisões são registradas: marcas e grupos de marcas. Quando você cria um grupo de marcas inteligentes, as decisões do modelo ML mapeados para o grupo serão mostradas em linha com as marcas no grupo para ajudá-lo a ver as informações em linha, onde fazem a maioria dos sentidos de forma contextual.

## <a name="how-to-set-up-a-smart-tag-group"></a>Como configurar um grupo de marcas inteligentes

1. Em um conjunto de revisão, vá para **gerenciar análise configurar** -> **gerenciar marcas**.

2. Clique na lista suspensa ao lado de **Adicionar grupo de marcas** e selecione **Adicionar grupo de marcas inteligentes**.

3. Selecione o modelo que você deseja mapear para este grupo. Isso criará uma seção de marca e N marcas filhas, onde N é o número de saídas possíveis do modelo. Por exemplo, o modelo de detecção de privilégio de cliente de advogados tem dois possíveis resultados-privilegiados e não privilegiados; selecionar esse modelo criará duas marcas filhas no conjunto de revisão, cada uma delas correspondente a uma das possíveis saídas.

4. Renomeie o grupo de marcas e as marcas conforme você vê ajustar.

## <a name="how-to-use-a-smart-tag-group"></a>Como usar um grupo de marcas inteligentes

Ao revisar um documento, os resultados do modelo serão expostos ao lado do valor de marca apropriado. Por exemplo, se você tiver um grupo de marcas inteligentes para detecção de privilégio de cliente de advogados e revisar um documento que o modelo decidiu ser potencialmente privilegiado, você verá o motivo para isso ao lado da marca apropriada. É importante observar que a marca não é aplicada automaticamente; para todos os efeitos e finalidades, as marcas dentro de um grupo de marcas inteligentes atuam exatamente como marcas normais, exceto pelo fato de que elas expõem os resultados do modelo ao lado, quando apropriado.