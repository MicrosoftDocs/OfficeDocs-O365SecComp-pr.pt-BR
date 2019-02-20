---
title: Princípios básicos do Office 365 de defesa contra ataques de negação de serviço
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Como a Microsoft utiliza os princípios fundamentais de absorção, detecção e atenuação em sua defesa contra ataques de negação de serviço (DoS).
ms.openlocfilehash: 17dc583258cdb4781dbe2a715e1ce153ee769ed3
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091003"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Princípios básicos de defesa contra ataques de negação de serviço

Os três princípios fundamentais ao se defender contra ataques de DoS baseados em rede são absorção, detecção e mitigação. A absorção ocorre antes da detecção e a detecção ocorre antes da redução. O absorção é a melhor defesa contra ataques de DoS. Se não for possível detectar o ataque, não será possível diminuí-lo. Mas, se mesmo o menor ataque de DoS não puder ser absorvido, os serviços não ficarão sobreviventes o suficiente para que o ataque seja detectado.

Obviamente, geralmente não é possível ser economicamente viável para a maioria das organizações comprar a capacidade em excesso necessária para absorver ataques de DoS, já que isso requer um investimento considerável em tecnologia e habilidades técnicas. Isso realça um dos benefícios de segurança do uso dos serviços de nuvem da Microsoft; a escalabilidade de nossos serviços nos permite fornecer uma forte proteção de rede para nossos clientes de nuvem de forma econômica. Mas mesmo em nossa escala, no entanto, ainda deve haver um equilíbrio entre absorção, detecção e mitigação. Para encontrar esse saldo, estudamos a taxa de crescimento de um ataque para estimar a quantidade de necessidade de absorver.

A detecção é um jogo de gato e mouse. Você deve procurar constantemente por novas maneiras pelas quais as pessoas estão atacando você ou tentando derrotar seus sistemas. Detect-> Atenuate-> Detect-> atenuar, etc., é um estado permanente e persistente que continuará indefinidamente.

## <a name="defending-against-dos-attacks"></a>Como se proteger contra ataques de DoS

Para se defender com êxito contra ataques de DoS, a detecção antecipada é essencial. Ao detectar um ataque antes que o sistema fique sobrecarregado, os defensores podem executar um plano de resposta.

A fórmula a seguir ajudará a aproximar o tempo de impacto de um ataque de DoS:

   **Capacidade máxima (em bytes/seg)/taxa de crescimento (em bytes/seg) = tempo de impacto (em bytes/seg)**

Se o tempo de detecção ocorrer após o tempo de impacto, é provável que o ataque de DoS seja bem-sucedido. Se o tempo de detecção ocorrer antes do tempo de impacto, os serviços que estão sendo atacados devem permanecer online e acessíveis, se as estratégias de mitigação forem usadas. Portanto, há apenas duas coisas que podem ser realizadas para se defender contra ataques de DoS:
- Aumente a capacidade para elevar o teto da capacidade máxima (que, por sua vez, fornece mais tempo para detectar um ataque); ou
- Diminuir o tempo para detectar.

O aumento da capacidade tem um impacto fiscal direto. A Microsoft recomenda que os clientes desenvolvam pelo menos a capacidade básica de absorção, para garantir que eles possam sobreviver a algum nível de ataque de DoS. A capacidade de absorção real varia de cliente para cliente, uma vez que cada cliente tem seus próprios limites de exposição, risco e outlay financeiro. Em última análise, por motivos econômicos, os investimentos de pesquisa e tempo para reduzir o tempo de detecção normalmente são a defesa mais econômica.
