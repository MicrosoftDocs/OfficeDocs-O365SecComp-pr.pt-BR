---
title: Princípios de núcleo do Office 365 de defesa contra ataques de negação de serviço
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Como a Microsoft usa os princípios fundamentais de absorção, detecção e redução de risco em sua defesa contra ataques (dos negação) de negação de serviço.
ms.openlocfilehash: e313d5514e9bc493db78bebffca24a0fae4cbca7
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741094"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Princípios básicos de defesa contra ataques de negação de serviço

Os três principais princípios quando defesa contra ataques DoS baseada em rede é absorção, detecção e redução de risco. Absorção ocorre antes da detecção, e a detecção acontece antes de redução de risco. Absorção é a melhor defesa contra um ataques DoS. Se o ataque não pode ser detectado, ele não pode ser atenuado. Mas se até mesmo o menor ataque DoS não pode ser absorver acordo, em seguida, serviços não são irá sobreviver tempo suficiente para que o ataque seja detectada.

Obviamente, geralmente não é economicamente possível para a maioria das organizações adquirir o excesso de capacidade necessário absorver ataques DoS, pois isso requer um investimento considerável em tecnologia e habilidades técnicas. Isso realça um dos benefícios do uso de serviços de nuvem da Microsoft; segurança a escala enorme de nossos serviços nos permite oferecer proteção de rede forte a nossos clientes de nuvem de forma econômica. Mas, até mesmo em nossa escala, porém, deve existir um equilíbrio entre a absorção, detecção e redução de risco. Para localizar esse equilíbrio, podemos estudar a taxa de crescimento do ataque para estimar quanto precisamos absorver.

Detecção é um jogo cat-and-mouse. Você deve constantemente olhar para as novas pessoas maneiras são ataque a você ou tentando vencer seus sistemas. Detectar - gt _ atenuar - gt _ detectar - gt _ minimizar, etc., é um estado perpétua persistente que continuará indefinidamente.

## <a name="defending-against-dos-attacks"></a>Defesa contra ataques DoS

Para obter êxito proteção contra um ataque DoS, detecção antecipada é essencial. Detectando um ataque antes que o sistema está sobrecarregado, defensores podem executar um plano de resposta.

A fórmula a seguir ajudarão aproximado o tempo de impacto de um ataque DoS:

   **Capacidade máxima (em bytes/seg) / taxa de crescimento (em bytes/seg) = tempo até o impacto (em bytes/seg)**

Se o tempo para detecção ocorre após o tempo para impacto, e em seguida, é provável que o ataque DoS será aprovado. Se o tempo para detecção ocorre antes do impacto no tempo, os serviços que está sendo atacados devem permanecer online e acessível, se as estratégias de redução de risco são usadas. Assim, há apenas duas coisas que podem ser feitas para se proteger contra ataques DoS:
- Aumentar a capacidade que eleve o teto da capacidade máxima (que por sua vez, fornece mais tempo para detectar um ataque); ou
- Reduza o tempo para detectar.

Aumento da capacidade tem um impacto fiscal direto. A Microsoft recomenda que os clientes desenvolvem absorção básica pelo menos capacidade, para garantir que eles podem sobreviver algum nível de ataque DoS. A capacidade de absorção real irá variar de cliente para cliente, como cada cliente tem seus próprios limites de gastos financeiros, riscos e exposição. Por fim, por razões econômicas, investimentos de pesquisas e tempo de maneiras de reduzir o tempo para detecção geralmente são a defesa mais econômica.
