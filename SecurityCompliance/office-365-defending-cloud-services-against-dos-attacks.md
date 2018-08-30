---
title: Serviços de nuvem do Office 365 defesa contra ataques de negação de serviço
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
description: Como a Microsoft protege seus serviços de nuvem de ataques de negação de serviço (DoS).
ms.openlocfilehash: f11a4293a35de4d36fd38fce892a4e59919111cc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524167"
---
# <a name="defending-microsoft-cloud-services-against-denial-of-service-attacks"></a>Defesa contra os serviços de nuvem da Microsoft contra ataques de negação de serviço

## <a name="introduction"></a>Introdução
Data centers da Microsoft são protegidos por segurança de defesa em camadas que inclui a instalação da cerca perímetro, câmeras de vídeo, pessoal de segurança e as entradas de seguras que usam biométrica, cartão inteligente e a autenticação multifator. A segurança de defesa em camadas continua através de cada área do recurso de e para cada unidade de servidor físico. A [infraestrutura de nuvem da Microsoft e no grupo operações](https://www.microsoft.com/en-us/cloud-platform/global-datacenters) fornece a infraestrutura principal e tecnologias básicas de nossos serviços de nuvem. Nossos data centers cumprir os padrões do setor para segurança física e a confiabilidade e são gerenciados, monitorados e administrados pela equipe de operações da Microsoft.

Para proteger ainda mais nossos serviços em nuvem, a Microsoft fornece um sistema de defesa DDoS que faz parte dos processos de teste de invasão e monitoramento contínuo do Microsoft Azure. O sistema de defesa Azure DDoS foi projetado não apenas para suportar ataques de fora, mas também de outros tenants Azure. Azure usa detecção standard e técnicas de redução de risco como SYN cookies, limitação de taxa e limites de conexão para proteger contra ataques de DDoS.

Os serviços de nuvem da Microsoft estão sujeitos a ameaça de ataque de várias fontes. Para atenuar e proteger contra as ameaças DoS vários, uma detecção de ameaça altamente escalonável e dinâmicas baseada no Windows Azure e redução de risco sistema foi desenvolvido e implementado com o objetivo principal de proteger a infra-estrutura subjacente de ataques DoS e os clientes de serviços de ajuda a evitar interrupções de serviço para a nuvem. O sistema de mitigação DoS Azure protege o tráfego de entrada, saído e a região.

A maioria dos ataques DoS é iniciado contra as metas na rede (L3) e transporte (L4) camadas do modelo de [Interconexão de sistemas abertos](https://docs.microsoft.com/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI). Ataques direcionados para as camadas L3 e camada 4 são projetados para uma interface de rede ou o serviço com o tráfego de ataque para negar a capacidade de responder ao tráfego legítimo e prejudicar os recursos de inundação. Especificamente, L3 e camada 4 ataques tentativa saturados a capacidade de links de rede, dispositivos ou serviços ou sobrecarregar as CPUs dos servidores ou máquinas virtuais com suporte para um aplicativo.

Para se proteger contra ataques L3 e camada 4 Microsoft tem projetado, desenvolvido e implantado uma solução voltada especificamente protegendo as metas de infraestrutura e do cliente que vêm sob ataque, protegendo a essas camadas. Protegendo a infra-estrutura garante que o tráfego de ataque destinado a um cliente não resultar em dano material adicional ou diminuído qualidade de rede do serviço para outros clientes. A solução usa dados de amostragem de tráfego do datacenter roteadores. Esses dados são analisados por uma rede de serviço para detectar ataques de monitoramento. Quando um ataque é detectado, mecanismos de defesa automatizados levada a efeito.

## <a name="application-level-defenses"></a>Defesas de nível de aplicativo
Equipes de engenharia do Microsoft sigam os mesmos padrões rigorosos definidos pelo [Microsoft operacionais garantia de segurança](https://www.microsoft.com/en-us/SDL/OperationalSecurityAssurance) para ajudar a proteger os dados do cliente. Os serviços de nuvem da Microsoft intencionalmente são criados para suportar uma carga muito alta, bem como para proteger e a atenuar contra ataques de nível de aplicativo. Podemos implementou uma arquitetura de escalada onde os serviços são distribuídos em vários datacenters global com recursos em algumas das cargas de trabalho de aceleração e isolamento regional.

País ou região, que identifica de administrador do cliente durante a configuração inicial dos serviços, de cada cliente determina o local de armazenamento primário para os dados do cliente. Dados de cliente são replicados entre data centers redundantes de acordo com uma estratégia de backup/primário. Um data center principal hospeda o software de aplicativo, juntamente com todos os dados de cliente primário em execução no software. Um backup datacenter fornece failover automático. Se o datacenter primário parar de funcionar por qualquer motivo, solicitações serão redirecionadas para a cópia dos dados do cliente e de software no datacenter backup. A qualquer momento determinado, os dados do cliente podem ser processados em primário ou o Centro de dados de backup. Distribuição dos dados em vários datacenters reduz a área de superfície afetada no caso de um data center é atacado. Além disso, os serviços no datacenter afetado podem ser rapidamente redirecionados para o datacenter secundário como um dos mecanismos de recuperação e Bento vice-versa (redirecionada volta para o datacenter primário depois que o serviço é restaurado).

Cargas de trabalho individuais incluem recursos internos que gerenciam a utilização de recursos. Por exemplo, a limitação mecanismos no Exchange Online e o SharePoint Online fazem parte de uma abordagem de várias camada de defesa contra ataques DoS. Limitação para usuários do Exchange Online é baseado no nível de recursos consumidos pelo usuário final, se os recursos estão no Active Directory, o armazenamento de informações do Exchange Online ou para outro lugar. Um orçamento que é alocado para cada cliente para limitar os recursos consumidos por um usuário. O Exchange Online de limitação para componentes de sistema e a atividade do usuário é baseado no [gerenciamento de carga de trabalho](http://technet.microsoft.com/en-us/library/jj150503(v=exchg.150).aspx). Uma carga de trabalho do Exchange Online é um recurso, protocolo ou serviço que tenha sido definido explicitamente para fins de gerenciamento de recursos do Exchange Online sistema Exchange Online. Cada carga de trabalho do Exchange Online requer recursos do sistema, como a CPU, operações de banco de dados de caixa de correio, ou solicitações de Active Directory para executar solicitações de usuário ou o trabalho de plano de fundo. Exemplos de cargas de trabalho do Exchange Online: Outlook na web, o Exchange ActiveSync, migração de caixa de correio e assistentes de caixa de correio. Os administradores dos locatários podem gerenciar as configurações para usuários com o Shell de gerenciamento do Exchange de limitação de gerenciamento do Exchange workload. Existem várias formas de limitação que foram implementadas no Exchange Online, incluindo o PowerShell, serviços Web do Exchange e POP e IMAP, do Exchange ActiveSync, conexões de dispositivo móvel, os destinatários e mais. Enquanto os administradores das implantações do Exchange local podem configurar políticas de limitação, os administradores não podem configurar políticas de limitação para o Exchange Online.

O gatilho mais comuns de limitação no SharePoint Online é um código de modelo (CSOM) do objeto do cliente que executa o excesso de ações a uma frequência muito alta. Com o CSOM, muitas ações podem ser executadas com uma única solicitação, que pode exceder os limites de uso e causar a limitação de por usuário.

Independentemente da atividade que pode resultar em limitação, quando um usuário excede os limites de uso, SharePoint Online limites qualquer ainda mais solicitações de conta de usuário, geralmente por um curto período de tempo. Enquanto uma limitação de usuário estiver em vigor, todas as ações que o usuário são limitadas até que a aceleração expire, de acordo com os seguintes critérios:
- Solicitações de executada pelo usuário diretamente em um navegador, redireciona SharePoint Online para uma página de informações de limitação e as solicitações falharem.
- Para todas as solicitações, incluindo chamadas do CSOM, SharePoint Online retorna o código de status HTTP 429 ("muitas solicitações") e as solicitações falharem.

Se o processo incorreto continua a exceder os limites de uso, SharePoint Online pode completamente bloquear o processo e retornar o código de status HTTP 503 ("serviço indisponível").

## <a name="vulnerability-and-penetration-testing"></a>Vulnerabilidade e teste de invasão
A Microsoft usa muitas [tecnologias de segurança e práticas recomendadas](https://www.microsoft.com/en-us/trustcenter/security/threatmanagement) para [proteger sua infraestrutura de nuvem](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) e no local redes contra ameaças modernas, sofisticadas, incluindo o uso de componentes de antimalware e serviços para serviços de nuvem, virtuais máquinas (VMs) e outros sistemas; Ameaça análises avançadas, que monitora os padrões de uso normal para usuários, sistemas e redes e emprega máquina de aprendizado para sinalizar qualquer comportamento que está fora do teste de invasão de comum e regular.

Além dos executando nossos próprios testes de invasão e oferecendo aos nossos clientes um [programa Microsoft Cloud unificada testes de invasão](https://technet.microsoft.com/en-us/mt784683), podemos também se comprometer com profissionais de segurança de terceiros que executam avaliações de vulnerabilidade regular dos e invasão testes com nossos serviços de nuvem. Fazemos os relatórios dessas avaliações de vulnerabilidade de terceiros disponível para download da [Confiança de serviço](https://aka.ms/STP) e portais de [Garantia de serviço](https://aka.ms/ServiceAssurance) .
