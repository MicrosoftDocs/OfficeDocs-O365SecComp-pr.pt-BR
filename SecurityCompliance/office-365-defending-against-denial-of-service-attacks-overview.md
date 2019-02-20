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
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Como se proteger contra ataques de negação de serviço no Office 365

## <a name="introduction"></a>Introdução
A Microsoft fornece uma infraestrutura confiável para mais de 200 serviços em nuvem, incluindo Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype e Xbox Live que são hospedados em nossa nuvem global infraestrutura de mais de 100 datacenters.

Como uma organização global com uma presença de Internet significativa e muitas propriedades proeminentes da Internet que oferecem serviços em nuvem, a Microsoft é um grande alvo comum para hackers e outras pessoas mal-intencionadas. A rede – a camada de comunicação entre os clientes e a nuvem da Microsoft – é um dos maiores alvos de ataques mal-intencionados. Na verdade, há muitos anos, a Microsoft foi continuamente e persistente sob alguma forma de cyberattack baseados em rede. Quase todos os momentos, pelo menos uma das propriedades da Internet da Microsoft está enfrentando alguma forma de ataque. Sem sistemas de mitigação confiáveis e persistentes que podem se defender contra esses ataques, os serviços de nuvem da Microsoft ficarão offline e indisponíveis para os clientes.

A Microsoft usa princípios de segurança de proteção em camadas para proteger seus serviços e redes de nuvem. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Definição e sintomas de ataques de negação de serviço
Uma maneira de atacar os serviços de rede é criar muitas solicitações em relação aos hosts de um serviço para sobrecarregar a rede e os servidores para negar o serviço a usuários legítimos. Isso é conhecido como um ataque de negação de serviço (DoS). Quando o ataque é executado por vários atores, pontos de extremidade e/ou vetores, ele é conhecido como um ataque de negação de serviço distribuído (DDoS). Embora os meios, motivos e metas variem, os ataques DoS e DDoS geralmente consistem nos esforços de uma pessoa ou de pessoas para impedir que um site ou serviço da Internet funcione corretamente ou de forma temporária ou indefinida.

A [equipe de preparação para emergências dos Estados Unidos](https://www.us-cert.gov/) (US-CERT) define sintomas de ataques de dos para incluir:
- Desempenho de rede excepcionalmente lento (ao abrir arquivos ou acessar sites da Internet)
- Indisponibilidade de um site da Web
- Incapacidade de acessar um site da Web
- Aumento considerável no spam recebido
- Desconexão de uma conexão com a Internet sem fio ou com fio
- Perda de longo prazo do acesso à Web ou a qualquer serviço de Internet

## <a name="related-topics"></a>Tópicos Relacionados
- [Princípios básicos de defesa contra ataques de negação de serviço](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Estratégia de defesa de negação de serviço da Microsoft](office-365-microsoft-dos-defense-strategy.md)
- [Defendendo os serviços de nuvem da Microsoft contra ataques de negação de serviço](office-365-defending-cloud-services-against-dos-attacks.md)
