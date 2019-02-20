---
title: Estratégia de defesa do DoS do Office 365 da Microsoft
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
description: Uma visão geral da estratégia de defesa da Microsoft para lidar com ataques de negação de serviço (DoS).
ms.openlocfilehash: 0b0cf20e6282c85ede05edda3979ae5a7295ac78
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090813"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Estratégia de defesa de negação de serviço da Microsoft

A estratégia da Microsoft para defesa contra ataques de negação de serviço (DoS) baseado em rede é um pouco exclusiva devido à nossa escala e ao espaço global. Essa escala permite que a Microsoft use estratégias e técnicas de que poucas organizações (provedores ou organizações de clientes) podem ser compatíveis. A base da estratégia de DoS está aproveitando nossa presença global. A Microsoft se comunica com provedores de Internet, provedores de emparelhamento (públicos e privados) e corporações privadas em todo o mundo, dando a eles uma presença de Internet significativa (que por esse texto é escrito, dobra a cada 18 meses). Ter uma presença tão grande permite que a Microsoft absorve ataques em uma área de superfície muito grande.

Considerando nossa natureza exclusiva, a Microsoft usa processos de detecção e atenuação diferentes daqueles usados por grandes empresas. Nossa estratégia é baseada em uma separação de detecção e atenuação, bem como redução global e distribuída por meio de nossas diversas bordas. Muitas empresas usam soluções de terceiros que detectam e reduzem os ataques na borda. À medida que nossa capacidade de borda cresceu, ficou claro que a significância de qualquer ataque contra bordas individuais ou específicas era muito baixa. Por causa da nossa configuração exclusiva, separamos os componentes de detecção e mitigação. Implantamos uma detecção de várias camadas que nos permite detectar ataques mais próximos de seus pontos de saturação, mantendo a redução global na borda. Essa estratégia garante que possamos lidar com vários ataques simultâneos.

Uma das defesas mais eficazes e de baixo custo empregadas pela Microsoft contra ataques de DoS é reduzir nossa superfície de ataque. Isso permite que possamos descartar tráfego indesejado na borda, em vez de analisar, processar e depurar os dados embutidos.

Na interface com a rede pública, a Microsoft usa dispositivos de segurança de uso especial para firewall, conversão de endereços de rede e funções de filtragem de IP. Também utilizamos o roteamento global de vários caminhos de custo igual (ECMP). Global ECMP Routing é uma estrutura de rede que garante que há vários caminhos globais para chegar a um serviço. Graças a esses vários caminhos, um ataque contra o serviço deve ser limitado à região da qual o ataque se originou – outras regiões devem ser não afetadas por esse ataque, já que os usuários finais usariam outros caminhos para acessar o serviço nessas regiões. Também desenvolvemos nosso próprio sistema de detecção e correlação do DoS interno que usa dados de fluxo, métricas de desempenho e outras informações. Este é um serviço de nuvem de hiperescala executado no Microsoft Azure, que analisa dados coletados de vários pontos em redes e serviços da Microsoft. Uma equipe de resposta a incidentes de um entre cargas de trabalho identifica as funções e responsabilidades entre as equipes, os critérios de escalonamento e os protocolos para envolver várias equipes e tratamento de incidentes. Essas soluções fornecem proteção baseada em rede contra ataques de DoS.

Por fim, as cargas de trabalho baseadas em nuvem são configuradas com limites otimizados com base em seu protocolo e uso de largura de banda precisa proteger exclusivamente essa carga de trabalho.
