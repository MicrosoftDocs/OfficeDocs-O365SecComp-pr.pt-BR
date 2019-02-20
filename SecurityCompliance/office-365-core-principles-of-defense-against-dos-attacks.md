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
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="c9aa0-103">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="c9aa0-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>

<span data-ttu-id="c9aa0-p101">Os três princípios fundamentais ao se defender contra ataques de DoS baseados em rede são absorção, detecção e mitigação. A absorção ocorre antes da detecção e a detecção ocorre antes da redução. O absorção é a melhor defesa contra ataques de DoS. Se não for possível detectar o ataque, não será possível diminuí-lo. Mas, se mesmo o menor ataque de DoS não puder ser absorvido, os serviços não ficarão sobreviventes o suficiente para que o ataque seja detectado.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="c9aa0-p102">Obviamente, geralmente não é possível ser economicamente viável para a maioria das organizações comprar a capacidade em excesso necessária para absorver ataques de DoS, já que isso requer um investimento considerável em tecnologia e habilidades técnicas. Isso realça um dos benefícios de segurança do uso dos serviços de nuvem da Microsoft; a escalabilidade de nossos serviços nos permite fornecer uma forte proteção de rede para nossos clientes de nuvem de forma econômica. Mas mesmo em nossa escala, no entanto, ainda deve haver um equilíbrio entre absorção, detecção e mitigação. Para encontrar esse saldo, estudamos a taxa de crescimento de um ataque para estimar a quantidade de necessidade de absorver.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="c9aa0-p103">A detecção é um jogo de gato e mouse. Você deve procurar constantemente por novas maneiras pelas quais as pessoas estão atacando você ou tentando derrotar seus sistemas. Detect-> Atenuate-> Detect-> atenuar, etc., é um estado permanente e persistente que continuará indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="c9aa0-116">Como se proteger contra ataques de DoS</span><span class="sxs-lookup"><span data-stu-id="c9aa0-116">Defending Against DoS Attacks</span></span>

<span data-ttu-id="c9aa0-p104">Para se defender com êxito contra ataques de DoS, a detecção antecipada é essencial. Ao detectar um ataque antes que o sistema fique sobrecarregado, os defensores podem executar um plano de resposta.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="c9aa0-119">A fórmula a seguir ajudará a aproximar o tempo de impacto de um ataque de DoS:</span><span class="sxs-lookup"><span data-stu-id="c9aa0-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="c9aa0-120">**Capacidade máxima (em bytes/seg)/taxa de crescimento (em bytes/seg) = tempo de impacto (em bytes/seg)**</span><span class="sxs-lookup"><span data-stu-id="c9aa0-120">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in bytes/sec)**</span></span>

<span data-ttu-id="c9aa0-p105">Se o tempo de detecção ocorrer após o tempo de impacto, é provável que o ataque de DoS seja bem-sucedido. Se o tempo de detecção ocorrer antes do tempo de impacto, os serviços que estão sendo atacados devem permanecer online e acessíveis, se as estratégias de mitigação forem usadas. Portanto, há apenas duas coisas que podem ser realizadas para se defender contra ataques de DoS:</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="c9aa0-124">Aumente a capacidade para elevar o teto da capacidade máxima (que, por sua vez, fornece mais tempo para detectar um ataque); ou</span><span class="sxs-lookup"><span data-stu-id="c9aa0-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="c9aa0-125">Diminuir o tempo para detectar.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-125">Decrease the time to detect.</span></span>

<span data-ttu-id="c9aa0-p106">O aumento da capacidade tem um impacto fiscal direto. A Microsoft recomenda que os clientes desenvolvam pelo menos a capacidade básica de absorção, para garantir que eles possam sobreviver a algum nível de ataque de DoS. A capacidade de absorção real varia de cliente para cliente, uma vez que cada cliente tem seus próprios limites de exposição, risco e outlay financeiro. Em última análise, por motivos econômicos, os investimentos de pesquisa e tempo para reduzir o tempo de detecção normalmente são a defesa mais econômica.</span><span class="sxs-lookup"><span data-stu-id="c9aa0-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
