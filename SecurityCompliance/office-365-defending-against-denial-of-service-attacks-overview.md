---
title: Como se proteger contra ataques de negação de serviço no Office 365
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Uma visão geral dos ataques de negação de serviço (DoS).
ms.openlocfilehash: cd099bcb225cfa5dd1f44f14d4b7813bef8f7442
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091013"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="37507-103">Como se proteger contra ataques de negação de serviço no Office 365</span><span class="sxs-lookup"><span data-stu-id="37507-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="37507-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="37507-104">Introduction</span></span>
<span data-ttu-id="37507-105">A Microsoft fornece uma infraestrutura confiável para mais de 200 serviços em nuvem, incluindo Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype e Xbox Live que são hospedados em nossa nuvem global infraestrutura de mais de 100 datacenters.</span><span class="sxs-lookup"><span data-stu-id="37507-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="37507-p101">Como uma organização global com uma presença de Internet significativa e muitas propriedades proeminentes da Internet que oferecem serviços em nuvem, a Microsoft é um grande alvo comum para hackers e outras pessoas mal-intencionadas. A rede – a camada de comunicação entre os clientes e a nuvem da Microsoft – é um dos maiores alvos de ataques mal-intencionados. Na verdade, há muitos anos, a Microsoft foi continuamente e persistente sob alguma forma de cyberattack baseados em rede. Quase todos os momentos, pelo menos uma das propriedades da Internet da Microsoft está enfrentando alguma forma de ataque. Sem sistemas de mitigação confiáveis e persistentes que podem se defender contra esses ataques, os serviços de nuvem da Microsoft ficarão offline e indisponíveis para os clientes.</span><span class="sxs-lookup"><span data-stu-id="37507-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="37507-111">A Microsoft usa princípios de segurança de proteção em camadas para proteger seus serviços e redes de nuvem.</span><span class="sxs-lookup"><span data-stu-id="37507-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="37507-112">Definição e sintomas de ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="37507-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="37507-p102">Uma maneira de atacar os serviços de rede é criar muitas solicitações em relação aos hosts de um serviço para sobrecarregar a rede e os servidores para negar o serviço a usuários legítimos. Isso é conhecido como um ataque de negação de serviço (DoS). Quando o ataque é executado por vários atores, pontos de extremidade e/ou vetores, ele é conhecido como um ataque de negação de serviço distribuído (DDoS). Embora os meios, motivos e metas variem, os ataques DoS e DDoS geralmente consistem nos esforços de uma pessoa ou de pessoas para impedir que um site ou serviço da Internet funcione corretamente ou de forma temporária ou indefinida.</span><span class="sxs-lookup"><span data-stu-id="37507-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="37507-117">A [equipe de preparação para emergências dos Estados Unidos](https://www.us-cert.gov/) (US-CERT) define sintomas de ataques de dos para incluir:</span><span class="sxs-lookup"><span data-stu-id="37507-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="37507-118">Desempenho de rede excepcionalmente lento (ao abrir arquivos ou acessar sites da Internet)</span><span class="sxs-lookup"><span data-stu-id="37507-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="37507-119">Indisponibilidade de um site da Web</span><span class="sxs-lookup"><span data-stu-id="37507-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="37507-120">Incapacidade de acessar um site da Web</span><span class="sxs-lookup"><span data-stu-id="37507-120">Inability to access a Web site</span></span>
- <span data-ttu-id="37507-121">Aumento considerável no spam recebido</span><span class="sxs-lookup"><span data-stu-id="37507-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="37507-122">Desconexão de uma conexão com a Internet sem fio ou com fio</span><span class="sxs-lookup"><span data-stu-id="37507-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="37507-123">Perda de longo prazo do acesso à Web ou a qualquer serviço de Internet</span><span class="sxs-lookup"><span data-stu-id="37507-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="37507-124">Tópicos Relacionados</span><span class="sxs-lookup"><span data-stu-id="37507-124">Related Topics</span></span>
- [<span data-ttu-id="37507-125">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="37507-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="37507-126">Estratégia de defesa de negação de serviço da Microsoft</span><span class="sxs-lookup"><span data-stu-id="37507-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="37507-127">Defendendo os serviços de nuvem da Microsoft contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="37507-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
