---
title: Configurar detecção de privilégio de cliente de advogado na descoberta eletrônica avançada
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
ms.openlocfilehash: ee5f2257e73467c50a0ecc296d8d3b70b7c3d0f8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155183"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a>Configurar a detecção de privilégio de cliente de advogado (visualização) na descoberta eletrônica avançada

Um aspecto importante e dispendioso da parte de revisão de qualquer processo de descoberta é a análise de conteúdo privilegiado. A descoberta eletrônica avançada fornece uma detecção baseada em AI de conteúdo privilegiado no seu caso, para que você possa tornar esse processo mais eficiente. Como este recurso está atualmente na versão beta, um administrador de descoberta eletrônica precisa optar pelo recurso para usá-lo.

## <a name="how-does-it-work"></a>Como funciona?

Com o recurso ativado, quando você analisa um conjunto de revisão em um caso, todos os documentos são executados por meio do modelo de detecção de privilégio de cliente advogado. O modelo examina duas coisas:

- Conteúdo: o modelo ML determina a probabilidade de que o conteúdo do documento seja legal por natureza.

- Participantes: se houver uma lista de advogados para o locatário, o modelo compara os participantes do documento com a lista para determinar se o documento tem pelo menos um participante advogado.
O modelo produz três valores para todos os documentos, que poderão ser pesquisados em um conjunto de revisão:

- Pontuação de conteúdo: a probabilidade de o documento ser legal por natureza (Pontuação entre 0 e 1)

- O advogado é verdadeiro se um dos participantes for encontrado na lista advogado carregado, caso contrário, false ou se não houver nenhuma lista de advogados.

-  Possivelmente privilegiado: true se a pontuação de conteúdo estiver acima do limite ou tiver um participante advogado; caso contrário, false.

## <a name="opting-into-attorney-client-privilege-detection"></a>Optando por detecção de privilégio de cliente advogado

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a>Etapa 1: optar pela detecção de privilégio de cliente do advogado (administrador de descoberta eletrônica)

Como a detecção de privilégio de cliente do advogado é um recurso de visualização, o administrador de descoberta eletrônica precisa optar por permitir que o recurso fique disponível em seus casos.

- Vá para "configurar recursos experimentais" da página de descoberta eletrônica avançada

- Clique em "gerenciar detecção de privilégio de cliente do advogado".

- Clique no botão de alternância para ativar o recurso.

### <a name="step-2-upload-a-list-of-attorneys-optional"></a>Etapa 2: carregar uma lista de advogados (opcional)

Para aproveitar ao máximo a detecção de privilégio de cliente de advogado, recomendamos fornecer uma lista de endereços de email de advogados ou pessoas jurídicas que trabalham na empresa. A lista deve ser um CSV sem cabeçalho, com um endereço de email por linha.

## <a name="leveraging-attorney-client-privilege-detection"></a>Aproveitamento da detecção de privilégio de cliente do advogado 

### <a name="step-1-analyze-a-review-set"></a>Etapa 1: analisar um conjunto de revisão

Quando você analisa o conjunto de análise, a detecção de privilégio de cliente também será executada. Para saber mais sobre a análise de dados no conjunto de revisão, consulte [analisar dados em uma revisão definida em descoberta eletrônica avançada](analyzing-data-in-review-set.md).

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a>Etapa 2: criar um grupo de marcas inteligentes com modelo de detecção de privilégio de cliente advogado

Uma das principais maneiras de consumir os resultados da detecção de privilégio de cliente de advogados no processo de revisão é usar um grupo de marcas inteligentes. Os grupos de marcas inteligentes usam os resultados de um modelo de ML e mostram os resultados do modelo em linha ao lado das marcas, para que você possa consumir facilmente os resultados do modelo, quando for relevante, e usar as marcas no processo de revisão, como faria com qualquer outra marca no painel de marcação. Confira [Configurar marcas inteligentes para revisão de suporte para ml na descoberta eletrônica avançada](smart-tags.md) para obter mais informações.

- Em "gerenciar marcas", clique em "Adicionar seção de marca inteligente".

- Selecione "detecção de privilégio de cliente advogado". Você verá que um grupo de marcas e duas marcas, correspondendo aos possíveis resultados do modelo, foram criados.

- Renomeie o grupo de marcas e as marcas conforme você vê o ajuste para sua análise.

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a>Etapa 3: usar o grupo de marcas inteligentes para revisão de privilégio

Quando você revisar um documento, se o modelo tiver determinado que o documento é potencialmente privilegiado, a marca inteligente correspondente exibirá o resultado:

- Se o documento tiver conteúdo que possa ser legal, um rótulo de "conteúdo legal" será exibido ao lado da marca inteligente correspondente.

- Se o documento tiver um participante encontrado na lista de advogados carregados, um rótulo "advogado" será exibido ao lado da marca inteligente correspondente.