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
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Defesa contra ataques de negação de serviço no Office 365

## <a name="introduction"></a>Introdução
A Microsoft oferece uma infra-estrutura confiável para mais de 200 serviços em nuvem, incluindo o Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype e Xbox Live hospedadas na nuvem nosso global infraestrutura de data centers mais de 100.

Como uma organização global com uma presença de Internet significativa e muitos destaque propriedades da Internet que oferecem serviços de nuvem, Microsoft é um destino grande e comuns para hackers e outros indivíduos mal-intencionados. Rede-- a camada de comunicação entre clientes e o Microsoft Cloud – é uma das maiores alvos de ataques mal-intencionados. Na verdade, faz muitos anos, Microsoft foi continuamente e persistentemente em alguma forma de cibernético baseada em rede. Em quase todos os momentos, pelo menos uma das propriedades da Internet da Microsoft está enfrentando alguma forma de ataque. Sem sistemas de redução de risco confiável e persistente que podem proteger contra esses ataques, os serviços de nuvem da Microsoft seria offline e indisponível para os clientes.

A Microsoft usa os princípios de segurança de defesa em camadas para proteger suas redes e serviços em nuvem. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Definição e sintomas de ataques de negação de serviço
Uma maneira de ataques de serviços de rede é criar muitas solicitações contra hosts do serviço para saturem a rede e os servidores para negar serviço aos usuários legítimos. Isso é conhecido como um ataque de negação de serviço (DoS). Quando o ataque é executado por vários atores, pontos de extremidade e/ou vetores, ela é conhecida como um ataque de (DDoS) de negação de serviço distribuído. Embora os meios, motivos e destinos variam, ataques DoS e DDoS geralmente consistem os esforços de uma pessoa ou nas pessoas podem impedir que a um site de Internet ou o serviço funcionando corretamente ou é que mudaram temporariamente ou indefinidamente.

[Estados Unidos Computer Emergency Readiness Team](https://www.us-cert.gov/) -CERT (US) define os sintomas de ataques para incluir:
- Incomum diminuir o desempenho de rede (quando abrir arquivos ou ao acessar sites da Internet)
- Indisponibilidade de um site
- Incapacidade de acessar um site da Web
- Aumento notável no spam recebido
- Desconexão de uma conexão de Internet ou sem fio
- Perda de longo prazo de acesso à Web ou de quaisquer serviços de Internet

## <a name="related-topics"></a>Tópicos relacionados
- [Princípios básicos de defesa contra ataques de negação de serviço](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Estratégia de defesa de negação de serviço da Microsoft](office-365-microsoft-dos-defense-strategy.md)
- [Defesa contra os serviços de nuvem da Microsoft contra ataques de negação de serviço](office-365-defending-cloud-services-against-dos-attacks.md)
