---
title: Monitoramento do Office 365 e autorecuperação
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
description: Informações sobre o Office 365, monitoramento e reparo automático de recursos.
ms.openlocfilehash: ff9471eaa6117ca3d7761549bca9ab629020fe79
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523655"
---
# <a name="office-365-monitoring-and-self-healing"></a>Monitoramento do Office 365 e autorecuperação
Considerando a escala do Office 365, seria impossível manter os dados do cliente resiliente e protegidos contra malware sem monitoramento interno que seja abrangente, alertando que é inteligente e autorecuperação que é rápida e confiável. O monitoramento de um conjunto de serviços na escala do Office 365 é muito desafiador. Novos pensamentos e metodologias necessária para que sejam introduzidos e toda novos conjuntos de tecnologia necessária a ser criado para operar e gerenciar o serviço em um ambiente global conectado. Podemos ter movido fora do tradicional abordagem de coleta de dados de monitoramento e filtragem para criar alertas para uma abordagem que baseia-se na análise de dados; aproveitando sinais e Criando confiança em que os dados e, em seguida, usando automação para recuperar ou resolver o problema. Essa abordagem ajuda a tomar as pessoas fora da equação de recuperação, por sua vez que faz com que as operações menor erro caro, mais rápido e menos propenso. 

Fundamentais para o Office 365 monitoring é uma coleção de tecnologias que compõe o nosso mecanismo de ideias de dados, que é baseado no Windows Azure, SQL Azure e [tecnologia de banco de dados de streaming do código-fonte aberto](http://cassandra.apache.org/). Ele foi projetado para coletar e agregar dados e chegar a conclusões. Atualmente, processa mais de 500 milhões de eventos por hora dos servidores mais de 100.000 (~ 15 TB por dia) espalhados dezenas de data centers em muitos regiões e esses números estão crescendo. 

O Office 365 usa *fora de monitoramento*, que envolve a criação de transações sintéticas para testar tudo o que é importante. Por exemplo, no Exchange Online cada cenário está testando cada banco de dados em todo o mundo a cada cinco minutos de maneira espalhada, fornecendo perto cobertura contínua de tudo que reside no sistema. Vários locais, as transações de teste de 250 milhões por dia são realizadas para criar uma linha de base robusta ou pulsação para o serviço. 

O Office 365 também usa o conceito de *Alerta vermelho*, que é reduzido para baixo de todos os sinais de monitoramento de todas as máquinas em nossos centros de dados para algo gerenciável por um humano. O conceito é muito simple: se algo está acontecendo entre vários sinais, deve haver algo em andamento. Não é sobre a criação de confiança em um sinal, trata-se de ter razoável fidelidade para cada sinal para que você obter maior precisão. Este sistema de monitoramento, é tão poderoso que não possuem equipe 24 x 7 assistindo nossos monitores; tudo o que temos é o mecanismo que torna-se ativo se ele detecta um problema, caso em que ele página o pessoal na chamada apropriado serão ou com mais frequência conforme for o caso, ele será apenas prossiga e resolver o problema. Uma vez iniciamos coletando sinais e criando alertas vermelhos desativa-los, podemos começar triangulação entre todas as partições de nosso serviço. 

Com base na combinação de alerta de falha e os alertas de vermelho, este alerta indica exatamente quais componentes podem estar tendo problemas e que o sistema será tentar corrigir o problema sozinho reiniciando um servidor de caixa de correio. 

Além dos recursos, como a restauração de página única autorecuperação, o Exchange Online inclui vários recursos que adotar uma abordagem ao monitoramento e autorecuperação que enfatiza a preservar a experiência do usuário final. Esses recursos incluem *Disponibilidade gerenciada*, que fornece ações internas de monitoramento e recuperação e AutoReseed, que automaticamente restaura a redundância de banco de dados após uma falha de disco. 

## <a name="managed-availability"></a>Disponibilidade Gerenciada 
Disponibilidade gerenciada fornece uma solução de verificação e recuperação de integridade nativo que monitora e protege a experiência do usuário final por meio de ações orientado a recuperação. Disponibilidade gerenciada é a integração das ações internas de monitoramento e a recuperação com a plataforma de alta disponibilidade do Exchange. Ele foi projetado para detectar e a recuperação de problemas assim que eles ocorrem e descobertos pelo sistema. Diferentemente das soluções anteriores de monitoramento externas e técnicas para Exchange, disponibilidade gerenciada não tente identificar ou se comunicar a causa raiz de um problema. Em vez disso, ele é focado em aspectos de recuperação que abordam três áreas principais da experiência do usuário final: 
- **Disponibilidade** - os usuários podem acessar o serviço? 
- **Latência** - como é a experiência dos usuários? 
- **Erros** - os usuários podem obter aquilo que querem? 

Disponibilidade gerenciada é um recurso interno que é executado em cada servidor do Office 365 executando o Exchange Online. Ela sonda e analisa centenas de métricas de integridade de cada segundo. Se algo é considerada errado, na maioria das vezes ele seja corrigido automaticamente. Mas sempre haverá problemas que a disponibilidade gerenciada não será possível corrigir seu próprio. Nesses casos, a disponibilidade gerenciada encaminhará o problema para uma equipe de suporte do Office 365 por meio do log de eventos. 

## <a name="autoreseed"></a>Propagação automática 
Servidores Exchange Online são implantados em uma configuração que armazena vários bancos de dados e seus fluxos de log no mesmo disco não-RAID. Essa configuração é conhecida como *apenas um monte de discos* (JBOD) porque nenhum mecanismos de redundância de armazenamento, como RAID, estão sendo usados para duplicar os dados no disco. Quando um disco falha em um ambiente de JBOD, os dados nesse disco serão perdidos. 

Determinados o tamanho do Exchange Online e o fato de que implantados dentro dele milhões de unidades de disco, falhas de unidade de disco são uma ocorrência regular no Exchange Online. Na verdade, mais de 100 falhar todos os dias. Quando um disco falha em uma implantação do enterprise no local, um administrador deve substituir o disco defeituoso manualmente e restaurar os dados afetados. Em uma implantação de nuvem o tamanho do Office 365, ter operadores (administradores de nuvem) manualmente a substituição de discos é viável ou economicamente possível. 

Nova propagação automática ou *AutoReseed*, é um recurso que é o substituto do que é normalmente controlado pelo operador ação em resposta a uma falha de disco, evento de corrupção do banco de dados ou outro problema que necessita de uma propagação de uma cópia do banco de dados. AutoReseed foi projetado para restaurar automaticamente a redundância de banco de dados após uma falha de disco usando discos sobressalentes que tenham sido configurados no sistema. Se um disco falhar, as cópias de banco de dados armazenadas naquele disco são propagadas para um disco sobressalente pré-configurado no servidor, assim, a restauração de redundância. 