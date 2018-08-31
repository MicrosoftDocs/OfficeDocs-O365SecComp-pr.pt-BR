---
title: Resiliência de dados no Office 365
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
description: Entenda a resiliência de dados no Microsoft Office 365.
ms.openlocfilehash: 7d43c766615ff1520c6529427116c42795da8565
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524331"
---
# <a name="data-resiliency-in-office-365"></a>Resiliência de dados no Office 365

## <a name="introduction"></a>Introdução
Devido à natureza complexa da computação em nuvem, a Microsoft está Lembre-se que ele não é um caso de se coisas dê erradas, mas em vez disso, quando. Criamos nossos serviços de nuvem para maximizar a confiabilidade e minimizar os efeitos negativos nos clientes quando as coisas dão errado. Podemos ultrapassou a estratégia tradicional da depender complexa infra-estrutura física e criamos redundância diretamente em nossos serviços de nuvem. Usamos uma combinação de infra-estrutura física menos complexa e de software mais inteligente que cria a resiliência de dados em nossos serviços e fornece a alta disponibilidade para os clientes. 

## <a name="resiliency-and-recoverability-are-built-in"></a>Resiliência e a capacidade de recuperação são internos 
Construção em resiliência e recuperação começa com a pressuposição de que a infra-estrutura e os processos subjacentes falhará em algum momento: hardware (infraestrutura) irá falhar, as pessoas serão cometer erros e software terá bugs. Embora seja incorreto dizer que os desenvolvedores de software não eram pensar essas coisas antes de nuvem, como esses problemas foram tratados em uma implementação típica do IT era muito diferente antes da nuvem: 
- Em primeiro lugar, proteções de hardware e infraestrutura foram significativas. Isso quer dizer tendo centros de dados com eficiência significativa de confiabilidade de 99,99% necessárias e a redundância da rede e servidores foram implementadas com baseada em hardware clustering, duas fontes de alimentação, interfaces de rede dual e assim por diante. 
- Em segundo lugar, o processo foi primordial. As equipes de operações mantido procedimentos rigorosos, alteração windows foram empregados, e geralmente era sobrecarga de gerenciamento de projeto significativo. 
- Terceiro, a implantação foi realizada em um ritmo glacial. Implantando código ao qual pertence a fonte quer dizer em espera para as versões de patch e versão principal libera a substituição do hardware envolvidos e gastos de capital significativo. Além disso, a única maneira de corrigir um problema era reversão. Assim, a maioria das organizações de TI seriam implantar versões principais apenas para evitar o trabalho se manter atualizado. 
- Finalmente, a escala de sistemas implantados, bem como o nível de sua capacidade de interconexão foi historicamente muito menor do que é agora. 

Hoje, os clientes esperam inovação contínua da Microsoft sem comprometer a qualidade, e esse é um dos motivos por que o software e os serviços da Microsoft são criadas com o resiliência e a capacidade de recuperação em mente. 

## <a name="office-365-data-resiliency-principles"></a>Princípios de resiliência de dados do Office 365 
Resiliência refere-se à capacidade de um serviço baseado em nuvem para suportar a determinados tipos de falhas e ainda permanecer totalmente funcional da perspectiva dos clientes. Resiliência de dados significa que, não importa qual falhas no Office 365, dados críticos do cliente permanecem intacta e inalterada. Para esse fim, Office 365 serviços foram projetados cerca de cinco princípios de resiliência específico: 
- Não há dados críticos e não críticas. Dados não-crítico (por exemplo, se uma mensagem foi lido) podem ser descartados em cenários de falha rara. Dados críticos (por exemplo, dados de cliente, como mensagens de email) devem ser protegidos com extremo custo. Como um objetivo do design, mensagens de email entregue sempre são críticas e coisas como se uma mensagem foi lido é não-crítica. 
- Cópias de dados do cliente devem ser separadas em zonas de falhas diferentes ou à medida que muitas falhas domínios possível (por exemplo, data centers, acessadas por credenciais único (processo, servidor ou operador)) para oferecer isolamento de falhas. 
- Dados críticos do cliente devem ser monitorados para falhando qualquer parte da atomicidade, consistência, isolamento, durabilidade (ACID). 
- Dados de cliente devem ser protegidos contra corrupção. Ele deve ser ativamente digitalizados ou monitorados, pode ser reparado e recuperáveis. 
- Portanto, a maioria dos resultados de perda de dados de ações do cliente, permitem aos clientes recuperar seus próprios usando uma interface gráfica que permite que eles restaurar itens excluídos acidentalmente. 
 
Por meio da compilação de nossos serviços de nuvem para estes princípios, juntamente com o teste robusto e validação, o Office 365 é capaz de atender e superar os requisitos de clientes, garantindo uma plataforma para inovação contínua e aperfeiçoamento. 

## <a name="related-links"></a>Links relacionados

- [Lidando com dados corrompidos](office-365-dealing-with-data-corruption.md)
- [Proteção contra ransomware e malware](office-365-malware-and-ransomware-protection.md)
- [Monitoramento e autorrecuperação](office-365-monitoring-and-self-healing.md)
- [Resiliência de dados do Exchange](office-365-exchange-data-resiliency.md)
- [Resiliência de dados do SharePoint](office-365-sharepoint-data-resiliency.md)