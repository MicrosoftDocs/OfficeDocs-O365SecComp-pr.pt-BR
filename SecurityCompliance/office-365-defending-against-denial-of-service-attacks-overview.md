---
title: Defesa contra ataques de negação de serviço no Office 365
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
description: Visão geral de ataques de negação de serviço (DoS).
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523448"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="b8ff4-103">Defesa contra ataques de negação de serviço no Office 365</span><span class="sxs-lookup"><span data-stu-id="b8ff4-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="b8ff4-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="b8ff4-104">Introduction</span></span>
<span data-ttu-id="b8ff4-105">A Microsoft oferece uma infra-estrutura confiável para mais de 200 serviços em nuvem, incluindo o Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype e Xbox Live hospedadas na nuvem nosso global infraestrutura de data centers mais de 100.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="b8ff4-p101">Como uma organização global com uma presença de Internet significativa e muitos destaque propriedades da Internet que oferecem serviços de nuvem, Microsoft é um destino grande e comuns para hackers e outros indivíduos mal-intencionados. Rede-- a camada de comunicação entre clientes e o Microsoft Cloud – é uma das maiores alvos de ataques mal-intencionados. Na verdade, faz muitos anos, Microsoft foi continuamente e persistentemente em alguma forma de cibernético baseada em rede. Em quase todos os momentos, pelo menos uma das propriedades da Internet da Microsoft está enfrentando alguma forma de ataque. Sem sistemas de redução de risco confiável e persistente que podem proteger contra esses ataques, os serviços de nuvem da Microsoft seria offline e indisponível para os clientes.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="b8ff4-111">A Microsoft usa os princípios de segurança de defesa em camadas para proteger suas redes e serviços em nuvem.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="b8ff4-112">Definição e sintomas de ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="b8ff4-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="b8ff4-p102">Uma maneira de ataques de serviços de rede é criar muitas solicitações contra hosts do serviço para saturem a rede e os servidores para negar serviço aos usuários legítimos. Isso é conhecido como um ataque de negação de serviço (DoS). Quando o ataque é executado por vários atores, pontos de extremidade e/ou vetores, ela é conhecida como um ataque de (DDoS) de negação de serviço distribuído. Embora os meios, motivos e destinos variam, ataques DoS e DDoS geralmente consistem os esforços de uma pessoa ou nas pessoas podem impedir que a um site de Internet ou o serviço funcionando corretamente ou é que mudaram temporariamente ou indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="b8ff4-117">[Estados Unidos Computer Emergency Readiness Team](https://www.us-cert.gov/) -CERT (US) define os sintomas de ataques para incluir:</span><span class="sxs-lookup"><span data-stu-id="b8ff4-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="b8ff4-118">Incomum diminuir o desempenho de rede (quando abrir arquivos ou ao acessar sites da Internet)</span><span class="sxs-lookup"><span data-stu-id="b8ff4-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="b8ff4-119">Indisponibilidade de um site</span><span class="sxs-lookup"><span data-stu-id="b8ff4-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="b8ff4-120">Incapacidade de acessar um site da Web</span><span class="sxs-lookup"><span data-stu-id="b8ff4-120">Inability to access a Web site</span></span>
- <span data-ttu-id="b8ff4-121">Aumento notável no spam recebido</span><span class="sxs-lookup"><span data-stu-id="b8ff4-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="b8ff4-122">Desconexão de uma conexão de Internet ou sem fio</span><span class="sxs-lookup"><span data-stu-id="b8ff4-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="b8ff4-123">Perda de longo prazo de acesso à Web ou de quaisquer serviços de Internet</span><span class="sxs-lookup"><span data-stu-id="b8ff4-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8ff4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8ff4-124">Related Topics</span></span>
- [<span data-ttu-id="b8ff4-125">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="b8ff4-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="b8ff4-126">Estratégia de defesa de negação de serviço da Microsoft</span><span class="sxs-lookup"><span data-stu-id="b8ff4-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="b8ff4-127">Defesa contra os serviços de nuvem da Microsoft contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="b8ff4-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
