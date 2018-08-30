---
title: Princípios de núcleo do Office 365 de defesa contra ataques de negação de serviço
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Como a Microsoft usa os princípios fundamentais de absorção, detecção e redução de risco em sua defesa contra ataques (dos negação) de negação de serviço.
ms.openlocfilehash: 8355a7897c788241092363a23e198423e81c587a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523450"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="98387-103">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="98387-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>
<span data-ttu-id="98387-p101">Os três principais princípios quando defesa contra ataques DoS baseada em rede é absorção, detecção e redução de risco. Absorção ocorre antes da detecção, e a detecção acontece antes de redução de risco. Absorção é a melhor defesa contra um ataques DoS. Se o ataque não pode ser detectado, ele não pode ser atenuado. Mas se até mesmo o menor ataque DoS não pode ser absorver acordo, em seguida, serviços não são irá sobreviver tempo suficiente para que o ataque seja detectada.</span><span class="sxs-lookup"><span data-stu-id="98387-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="98387-p102">Obviamente, geralmente não é economicamente possível para a maioria das organizações adquirir o excesso de capacidade necessário absorver ataques DoS, pois isso requer um investimento considerável em tecnologia e habilidades técnicas. Isso realça um dos benefícios do uso de serviços de nuvem da Microsoft; segurança a escala enorme de nossos serviços nos permite oferecer proteção de rede forte a nossos clientes de nuvem de forma econômica. Mas, até mesmo em nossa escala, porém, deve existir um equilíbrio entre a absorção, detecção e redução de risco. Para localizar esse equilíbrio, podemos estudar a taxa de crescimento do ataque para estimar quanto precisamos absorver.</span><span class="sxs-lookup"><span data-stu-id="98387-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="98387-p103">Detecção é um jogo cat-and-mouse. Você deve constantemente olhar para as novas pessoas maneiras são ataque a você ou tentando vencer seus sistemas. Detectar -> minimizar -> detectar -> minimizar, etc., é um estado perpétua persistente que continuará indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="98387-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="98387-116">Defesa contra ataques DoS</span><span class="sxs-lookup"><span data-stu-id="98387-116">Defending Against DoS Attacks</span></span>
<span data-ttu-id="98387-p104">Para obter êxito proteção contra um ataque DoS, detecção antecipada é essencial. Detectando um ataque antes que o sistema está sobrecarregado, defensores podem executar um plano de resposta.</span><span class="sxs-lookup"><span data-stu-id="98387-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="98387-119">A fórmula a seguir ajudarão aproximado o tempo de impacto de um ataque DoS:</span><span class="sxs-lookup"><span data-stu-id="98387-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="98387-120">**Capacidade máxima / (taxa de crescimento de capacidade máxima X) = tempo até o impacto**</span><span class="sxs-lookup"><span data-stu-id="98387-120">**Maximum Capacity / (Maximum Capacity X Growth Rate) = Time to Impact**</span></span>

<span data-ttu-id="98387-p105">Se o tempo para detecção ocorre após o tempo para impacto, e em seguida, é provável que o ataque DoS será aprovado. Se o tempo para detecção ocorre antes do impacto no tempo, os serviços que está sendo atacados devem permanecer online e acessível, se as estratégias de redução de risco são usadas. Assim, há apenas duas coisas que podem ser feitas para se proteger contra ataques DoS:</span><span class="sxs-lookup"><span data-stu-id="98387-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="98387-124">Aumentar a capacidade que eleve o teto da capacidade máxima (que por sua vez, fornece mais tempo para detectar um ataque); ou</span><span class="sxs-lookup"><span data-stu-id="98387-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="98387-125">Reduza o tempo para detectar.</span><span class="sxs-lookup"><span data-stu-id="98387-125">Decrease the time to detect.</span></span>

<span data-ttu-id="98387-p106">Aumento da capacidade tem um impacto fiscal direto. A Microsoft recomenda que os clientes desenvolvem absorção básica pelo menos capacidade, para garantir que eles podem sobreviver algum nível de ataque DoS. A capacidade de absorção real irá variar de cliente para cliente, como cada cliente tem seus próprios limites de gastos financeiros, riscos e exposição. Por fim, por razões econômicas, investimentos de pesquisas e tempo de maneiras de reduzir o tempo para detecção geralmente são a defesa mais econômica.</span><span class="sxs-lookup"><span data-stu-id="98387-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
