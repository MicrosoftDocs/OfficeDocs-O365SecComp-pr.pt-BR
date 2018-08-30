---
title: Estratégia de defesa do Microsoft Office 365
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
description: Visão geral da estratégia de defesa da Microsoft para lidar com ataques de negação de serviço (DoS).
ms.openlocfilehash: f172db5080ef73402c7e9bc61720eb0f87e844ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523458"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Estratégia de defesa de negação de serviço da Microsoft

Estratégia da Microsoft para defesa contra ataques (dos negação) de negação de serviço baseados em rede é relativamente exclusiva devido aos nossos escala e pegada de global. Essa escala permite que a Microsoft utilizam estratégias e técnicas que correspondam a algumas organizações (provedores ou organizações do cliente). A base de nossa estratégia DoS está aproveitando nossa presença global. Microsoft emprega com provedores de Internet, provedores de correspondência (pública e privada) e privadas corporações em todo o mundo, proporcionando uma presença significativa de Internet (que, quando este artigo foi escrito, dobra ao redor de cada 18 meses). Ter uma presença dessas grande possibilita à Microsoft absorver ataques em uma área de superfície muito grande.

Dado nossa natureza exclusiva, a Microsoft usa os processos de detecção e redução de risco diferentes das usadas por grandes empresas. Nossa estratégia se baseia em uma separação de detecção e redução de risco, bem como mitigação global e distribuída por meio de nossas muitas bordas. Muitas empresas usam as soluções de terceiros que detectam e a atenuar ataques da borda. Como nossa capacidade de borda cresceu, tornou-se claro que o significado de qualquer ataque contra bordas individuais ou determinadas era muito baixo. Devido à nossa configuração exclusiva, podemos ter separado os componentes de detecção e redução de risco. Implantamos detecção de várias camadas que nos permite detectar ataques quase como seus pontos de saturação enquanto preservam a redução de risco global da borda. Essa estratégia garante que podemos manipular vários ataques simultâneas.

Uma das defesas mais eficientes e econômica empregadas pelo Microsoft contra ataques DoS é reduzir a superfície de ataque nosso. Isso permite que descarta o tráfego indesejado da borda, em vez de análise, processamento e varredura para o embutido de dados.

Na interface com a rede pública, a Microsoft usa dispositivos de objetivos especiais de segurança para funções de filtragem de IP, conversão de endereço de rede e firewall. Usamos também roteamento global custo igual multi-path (ECMP). Roteamento de ECMP global é uma estrutura de rede que garante que existem diversos caminhos globais para chegar a um serviço. Graças esses vários caminhos, um ataque contra o serviço deve ser limitado à região do qual o ataque originado – outras regiões devem ser afetadas por esse ataque, como os usuários finais usaria outros caminhos para alcançar o serviço nessas áreas. Também podemos ter desenvolvido nossa própria DoS correlação e detecção de sistema interno que usa o fluxo de dados, as métricas de desempenho e outras informações. Este é um serviço de nuvem hyperscale executados no Microsoft Azure que analisa os dados coletados a partir de vários pontos em redes Microsoft e serviços. Uma equipe de resposta a incidentes entre cargas de trabalho DoS identifica as funções e responsabilidades entre equipes, os critérios para escalonamentos e os protocolos para envolver várias equipes e tratamento de incidentes. Essas soluções oferecem proteção baseada em rede contra ataques DoS.

Finalmente, as cargas de trabalho baseado em nuvem são configuradas com limites otimizados com base em sua protocolo e uso de largura de banda precisa proteger exclusivamente essa carga de trabalho.
