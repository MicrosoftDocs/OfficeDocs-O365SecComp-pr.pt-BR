---
title: Monitoramento do Office 365 e testar os limites de locatário
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
description: 'Resumo: Uma explicação sobre como Microsoft monitora e testes locatários limites para o Office 365.'
ms.openlocfilehash: 4d57c7497bfe8bf9939f3ae785ab9fbc670bd0ae
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523789"
---
# <a name="monitoring-and-testing-tenant-boundaries"></a>Monitorando e testando limites do locatário
Microsoft monitora continuamente e testa explicitamente para os pontos fracos e vulnerabilidades nos limites de locatário, incluindo monitoramento para invasão, tentativas de violação de permissão e consumo do recurso. Usamos também vários sistemas internos para monitorar continuamente para utilização de recursos inadequado que se detectado, dispara a limitação internas.

O Office 365 tem sistemas internos de monitoramento que continuamente monitoram para qualquer falha e a recuperação automática de unidade quando a falha é detectada. Sistemas de Office 365 analisar desvios no comportamento de serviço e iniciam processos de AutoCorreção que são internos do sistema. O Office 365 também usa a parte externa de monitoramento no qual a monitoração é realizada de vários locais ambas dos serviços de terceiros confiáveis (para verificação de SLA independente) e nossos próprios data centers que eleve alertas. Para fins de diagnóstico, temos o rastreamento, auditoria e log extensivo. Rastreamento granular e ajuda a conosco isolar problemas e executar raiz rápida e eficaz de monitoramento causar análise.

Enquanto o Office 365 tem ações de recuperação automatizadas onde for possível, os engenheiros de chamada no Microsoft estão disponíveis 24 x 7 para examinar todos os escalonamentos de segurança de gravidade 1 e post-mortem analisa de incidente cada serviço contribui para o aprendizado contínuo e aperfeiçoamento. Essa equipe inclui liderança sênior, os desenvolvedores de produtos, gerentes de programa, gerentes de produto e engenheiros de suporte. Nossos profissionais na chamada fornecem backup em tempo hábil e geralmente podem automatizar as ações de recuperação, para que a próxima vez que um evento ocorre, ele pode ser corrigido Self.

Microsoft realiza uma revisão pós-incidente cuidadosa cada vez que um incidente de segurança do Office 365 ocorre independentemente da magnitude do impacto. Uma revisão pós-incidente consiste em uma análise do que aconteceu, como podemos respondeu e como podemos evitar incidentes semelhantes no futuro. Com o intuito de transparência e responsabilidade, podemos compartilhar revisão pós-incidente para qualquer incidentes de serviço principal com clientes afetados. Para obter detalhes específicos, consulte [Gerenciamento de incidentes de segurança do Office 365](http://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Assumir a metodologia de violação
Com base em uma análise detalhada das tendências de segurança, o Microsoft advogados e destaca a necessidade de investimentos adicionais em processos de segurança problemas reativos e as tecnologias que enfocam detecção e resposta a ameaças emergentes, em vez de exclusivamente a prevenção de essas ameaças. Devido às alterações no cenário de ameaças e uma análise detalhada, Microsoft refinado sua estratégia de segurança além apenas impedindo violações de segurança para um melhor equipado para lidar com as violações quando ocorrem – uma estratégia que considera principais eventos de segurança não como uma questão de if, mas quando.

Embora as práticas de [Violação pressupõem](https://www.microsoft.com/en-us/TrustCenter/Security/default.aspx) pela Microsoft tenham sido in-loco faz muitos anos, muitos clientes ainda não sabem do trabalho que está sendo feito nos bastidores para proteger a nuvem da Microsoft. Pressuponha que violação é um pensamento que orienta os investimentos em segurança, as decisões de design e práticas recomendadas de segurança operacional. Suponha limites de violação a confiança é colocada em aplicativos, serviços, identidades e redes tratando todos eles — internos e externos — como inseguros e já comprometido. Embora a estratégia de violação pressupõem que não foi protegerem de uma violação real de quaisquer serviços de nuvem ou corporativa da Microsoft, um reconhecimento que muitas organizações, entre o setor, estavam sendo violadas apesar todas as tentativas de impedir que ele era. Enquanto impedir violações é uma parte importante de operações da organização, qualquer, essas práticas devem ser continuamente testadas e aumentadas para lidar com eficiência os adversários modernos e avançadas ameaças persistentes. Para qualquer organização para se preparar para uma violação, eles devem primeiro criar e manter procedimentos de resposta de segurança robusta, repetível e testada amplamente.

Enquanto os processos de segurança impedir violação, como a modelagem de ameaças, análises de código e teste de segurança são muito úteis como parte do [Security Development Lifecycle](http://www.microsoft.com/security/sdl/default.aspx), violação pressupõem que oferece várias vantagens que ajudam a conta para a segurança geral exercitar e medindo reativos recursos se houver uma violação.

Na Microsoft, definimos out para realizar isso por meio de em andamento war-games exercícios e o teste do site ao vivo invasão de nossos planos de resposta de segurança com o objetivo de melhorar nossos recursos de detecção e resposta. Microsoft regularmente simula as violações reais, conduz segurança contínua monitoramento e gerenciamento de incidentes de segurança práticas para validar e melhorar a segurança do Office 365, Windows Azure e outros serviços de nuvem da Microsoft.

Microsoft executa sua estratégia de segurança de violação pressupõem usando dois grupos principais:
- Equipes de vermelho (invasores)
- Azuis equipes (defensores)

Equipe do Microsoft Azure e o Office 365 separe equipes em tempo integral de vermelhas e equipes azuis.

Conhecida como "[Vermelho agrupamento](http://go.microsoft.com/fwlink/?linkid=518599)", a abordagem é sistemas Windows Azure e o Office 365 e operações usando as mesmas táticas, técnicas e procedimentos como os adversários reais, em relação a infra-estrutura de produção em tempo real, sem o foreknowledge de teste a Engenharia ou equipes de operações. Testa a detecção de segurança da Microsoft e os recursos de resposta e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas e outros problemas de segurança de uma maneira controlada. Cada violação de equipe vermelho é seguida por divulgação completa entre as duas equipes identificar lacunas, as descobertas de endereços e melhorar a resposta de violação.

**Observação**: nenhum dado de cliente está direcionado deliberadamente durante o agrupamento de vermelho ou o teste de invasão do site ao vivo. Os testes são contra a infra-estrutura do Office 365 e Windows Azure e plataformas, bem como inquilinos da Microsoft, aplicativos e dados. Nunca direcionadas Inquilinos do cliente, aplicativos e conteúdo hospedado no Office 365 ou no Windows Azure.

## <a name="red-teams"></a>Equipes de vermelho
A equipe de vermelha é um grupo de pessoal em tempo integral dentro da Microsoft que se concentra em infraestrutura da Microsoft violar, plataforma e inquilinos da Microsoft e aplicativos. Eles são o adversário dedicado (um grupo de hackers éticos) executando direcionados e persistentes ataques contra Online Services (infraestrutura da Microsoft, plataformas e aplicativos, mas não dos clientes finais aplicativos ou conteúdo).

A função da equipe de vermelho é ataques e entrar na ambientes usando as mesmas etapas como um adversário:
 
![Estágios de violação](media/office-365-isolation-breach-stages.png)

Entre outras funções, equipes vermelhas tentarem especificamente violar os limites de isolamento de Inquilino para encontrar bugs ou falhas em nosso projeto de isolamento.

## <a name="blue-teams"></a>Equipes azuis
A equipe de azul é composta de um conjunto dedicado respondentes de segurança ou membros de entre a resposta de incidentes de segurança, engenharia e operações organizações. Independentemente de suas características, eles são independentes e operam separadamente da equipe do vermelha. Segue a equipe azul estabelecida segurança processa e usa as ferramentas e as tecnologias mais recentes para detectar e responder a ataques e invasão. Assim como ataques reais, a equipe de azul não sabe quando ou como ataques da equipe vermelho ocorrerá ou quais métodos podem ser usados. Seu trabalho, seja um ataque de equipe vermelho ou ataques aos real, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a equipe de azul é continuamente na chamada e deve reagir à violações de equipe vermelho da mesma forma que fariam para qualquer outra violação.

Quando um adversário, como uma equipe de vermelho, tem violada um ambiente, a equipe de azul deve:
- Coletar evidências deixadas pelo adversário
- Detectar a evidência como uma indicação de comprometimento
- Alerta apropriado continuar engenharia e operação
- Triagem os alertas para determinar se eles ainda mais garantem investigação
- Colete o contexto do ambiente de fazer o escopo da violação
- Um plano de remediação para conter ou remover o adversário de formulário
- Execute o plano de remediação e recuperar de violação

A resposta de incidentes de segurança que executa em paralela com o adversário, conforme mostrado abaixo de formulário estas etapas:
 
![Estágios de resposta de violação](media/office-365-isolation-breach-response-stages.png)

As violações de equipe vermelho permitem exercer a azul capacidade da equipe para detectar e responder a ataques reais de ponta a ponta. Mais importante, ele permite uma resposta incidentes praticado segurança antes de uma violação autêntico. Além disso, devido a violações de equipe vermelho, a equipe de azul aprimora sua percepção da situação que pode ser valioso quando lidando com as violações futuras (seja de equipe de vermelho ou outro adversário). Em todo o processo de resposta e detecção, a equipe azul produz inteligência acionável e ganhos de visibilidade às condições reais a ambientes que eles estão tentando defesa. Frequentemente, isso é realizado por meio de análise de dados e judiciais, realizada pela equipe de azul ao responder a ataques de equipe vermelha e estabelecendo indicadores de ameaça, como indicadores de comprometimento. Muito semelhante como a equipe de vermelha identifica lacunas no bloco de segurança, equipes azuis identificam lacunas em sua capacidade de detectar e responder. Além disso, já que as equipes vermelhas ataques reais do modelo, a equipe da blue pode ser precisamente avaliada na capacidade, ou incapacidade, para lidar com os adversários determinados e persistentes. Finalmente, violações de equipe vermelho medem o impacto da nossa resposta violação e preparação.
