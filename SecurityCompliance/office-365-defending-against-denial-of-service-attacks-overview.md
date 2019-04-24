---
title: Como se proteger contra ataques de negação de serviço no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Uma visão geral dos ataques de negação de serviço (DoS).
ms.openlocfilehash: a7e67fcc87867190f345c5dad14e38a473420eab
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262813"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="d7cf4-103">Como se proteger contra ataques de negação de serviço no Office 365</span><span class="sxs-lookup"><span data-stu-id="d7cf4-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="d7cf4-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="d7cf4-104">Introduction</span></span>
<span data-ttu-id="d7cf4-105">A Microsoft fornece uma infraestrutura confiável para mais de 200 serviços em nuvem, incluindo Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype e Xbox Live que são hospedados em nossa nuvem global infraestrutura de mais de 100 datacenters.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="d7cf4-106">Como uma organização global com uma presença de Internet significativa e muitas propriedades proeminentes da Internet que oferecem serviços em nuvem, a Microsoft é um grande alvo comum para hackers e outras pessoas mal-intencionadas.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-106">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="d7cf4-107">A rede – a camada de comunicação entre os clientes e a nuvem da Microsoft – é um dos maiores alvos de ataques mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-107">The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="d7cf4-108">Na verdade, há muitos anos, a Microsoft foi continuamente e persistente sob alguma forma de cyberattack baseados em rede.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-108">In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="d7cf4-109">Quase todos os momentos, pelo menos uma das propriedades da Internet da Microsoft está enfrentando alguma forma de ataque.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-109">At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack.</span></span> <span data-ttu-id="d7cf4-110">Sem sistemas de mitigação confiáveis e persistentes que podem se defender contra esses ataques, os serviços de nuvem da Microsoft ficarão offline e indisponíveis para os clientes.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-110">Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="d7cf4-111">A Microsoft usa princípios de segurança de proteção em camadas para proteger seus serviços e redes de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="d7cf4-112">Definição e sintomas de ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="d7cf4-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="d7cf4-113">Uma maneira de atacar os serviços de rede é criar muitas solicitações em relação aos hosts de um serviço para sobrecarregar a rede e os servidores para negar o serviço a usuários legítimos.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-113">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="d7cf4-114">Isso é conhecido como um ataque de negação de serviço (DoS).</span><span class="sxs-lookup"><span data-stu-id="d7cf4-114">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="d7cf4-115">Quando o ataque é executado por vários atores, pontos de extremidade e/ou vetores, ele é conhecido como um ataque de negação de serviço distribuído (DDoS).</span><span class="sxs-lookup"><span data-stu-id="d7cf4-115">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="d7cf4-116">Embora os meios, motivos e metas variem, os ataques DoS e DDoS geralmente consistem nos esforços de uma pessoa ou de pessoas para impedir que um site ou serviço da Internet funcione corretamente ou de forma temporária ou indefinida.</span><span class="sxs-lookup"><span data-stu-id="d7cf4-116">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="d7cf4-117">A [equipe de preparação para emergências dos Estados Unidos](https://www.us-cert.gov/) (US-CERT) define sintomas de ataques de dos para incluir:</span><span class="sxs-lookup"><span data-stu-id="d7cf4-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="d7cf4-118">Desempenho de rede excepcionalmente lento (ao abrir arquivos ou acessar sites da Internet)</span><span class="sxs-lookup"><span data-stu-id="d7cf4-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="d7cf4-119">Indisponibilidade de um site da Web</span><span class="sxs-lookup"><span data-stu-id="d7cf4-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="d7cf4-120">Incapacidade de acessar um site da Web</span><span class="sxs-lookup"><span data-stu-id="d7cf4-120">Inability to access a Web site</span></span>
- <span data-ttu-id="d7cf4-121">Aumento considerável no spam recebido</span><span class="sxs-lookup"><span data-stu-id="d7cf4-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="d7cf4-122">Desconexão de uma conexão com a Internet sem fio ou com fio</span><span class="sxs-lookup"><span data-stu-id="d7cf4-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="d7cf4-123">Perda de longo prazo do acesso à Web ou a qualquer serviço de Internet</span><span class="sxs-lookup"><span data-stu-id="d7cf4-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7cf4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7cf4-124">Related Topics</span></span>
- [<span data-ttu-id="d7cf4-125">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="d7cf4-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="d7cf4-126">Estratégia de defesa de negação de serviço da Microsoft</span><span class="sxs-lookup"><span data-stu-id="d7cf4-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="d7cf4-127">Defendendo os serviços de nuvem da Microsoft contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="d7cf4-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
