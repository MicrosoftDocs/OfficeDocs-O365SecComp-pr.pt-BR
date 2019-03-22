---
title: Investigação e resposta automatizadas (AIR) com inteligência contra ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Saiba mais sobre os recursos de investigação e resposta automatizados do Office 365 proteção avançada contra ameaças.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736199"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a>Investigação e resposta automatizadas (AIR) com inteligência contra ameaças do Office 365

A investigação e a resposta automatizadas (AIR) (em breve para os [recursos de investigação e resposta contra ameaças do Office 365](office-365-ti.md)) permitem que você execute investigação e correção automatizadas para ameaças conhecidas que existem atualmente. Leia este artigo para obter uma visão geral do AIR e como ele pode ajudar sua organização a reduzir as ameaças com maior eficácia e eficiência. Saiba mais sobre quando o AIR estará disponível, consulte o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Alertas

Os [alertas](alert-policies.md#viewing-alerts) representam disparadores de fluxos de trabalho da equipe de operações de segurança para resposta a incidentes. Priorizar o conjunto certo de alertas para investigação e, ao mesmo tempo, garantir que nenhuma ameaça seja difícil. Quando as investigações nos alertas são realizadas manualmente, as equipes de operações de segurança devem procurar e correlacionar as entidades (por exemplo, conteúdo, dispositivos e usuários) em risco de ameaças. Essas tarefas e fluxos de trabalho são muito demorados e envolvem várias ferramentas e sistemas. Com o AIR, a investigação e a resposta são automatizadas nos alertas importantes de segurança e gerenciamento de ameaças que acionam os guias estratégicos de resposta de segurança automaticamente. 

para exibir alertas, no centro de conformidade do & de segurança do Office 365, escolha **alertas** > **exibir alertas**.

![Alertas que se vinculam a investigações](media/air-alerts-page-details.png) 

Selecione um alerta para exibir seus detalhes e, em seguida, use o link **Exibir investigação** para ir para a [investigação](#investigation-graph)correspondente.

## <a name="security-playbooks"></a>Guias de segurança

Os guias de segurança são políticas de back-end que estão no coração da automação no Microsoft Threat Protection. Os guias estratégicos de segurança fornecidos no AIR são baseados em cenários comuns de segurança do mundo real. Um guia de segurança é iniciado automaticamente quando um alerta é disparado dentro da sua organização. Depois que o alerta é acionado, o manual associado é executado automaticamente. O guia estratégico executa uma investigação, examinando todos os metadados associados (incluindo mensagens de email, usuários, assuntos, remetentes, etc.) e, com base em suas descobertas, recomenda um conjunto de ações que a equipe de segurança da sua organização pode executar para controlar e reduzir a ameaça. 

Os guias de segurança que você receberá com o AIR são projetados para lidar com as ameaças mais frequentes que as organizações enfrentam hoje. Eles são baseados na entrada de operações de segurança e em equipes de resposta a incidentes, incluindo aqueles que ajudam a defender ativos da Microsoft.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Os guias de segurança estão distribuindo em fases

Como parte do AIR, os guias de segurança são implantados em fases

- **Fase 1 (abril de 2019)**: os guias estratégicos incluem recomendações que os administradores de segurança revisam e aprovam. 

- **Fase 2 (junho de 2019)**: os administradores de segurança terão a opção de permitir que os guias estratégicos de segurança executem ações automaticamente, sem interação administrativa.

A fase 1 incluirá os seguintes guias estratégicos:
- Mensagem de phishing relatada pelo usuário
- URL clique em veredicto Change e links seguros de ATP bloquear substituição
- ZAP de malware
- Phish de phishing
- Investigações manuais (usando o Explorer)

Vários outros guias estratégicos estão planejados para a fase 2.

### <a name="playbooks-include-investigation-and-recommendations"></a>Os guias estratégicos incluem investigação e recomendações

Cada manual inclui: 
- uma investigação raiz, 
- etapas para procurar outras ameaças potenciais e 
- correção de ameaça recomendada.

Cada etapa de alto nível inclui muitas subetapas executadas para fornecer uma resposta detalhada, detalhada e exaustiva às ameaças.

## <a name="example-user-reported-phish-message"></a>Exemplo: mensagem de phishing relatada pelo usuário

Quando um usuário em sua organização envia uma mensagem de email e o relata à Microsoft usando o [suplemento de mensagem de relatório para Outlook ou Outlook Web Access](enable-the-report-message-add-in.md). Isso aciona um alerta informativo baseado no sistema que inicia automaticamente o guia estratégico de investigação.

Durante a fase de investigação de raiz, vários aspectos do email são avaliados. Eles incluem:
- Uma determinação sobre o tipo de ameaça que ela pode ser;
- Quem o enviou;
- De onde o email foi enviado (infraestrutura de envio);
- Se outras instâncias do email foram entregues ou bloqueadas;
- Uma avaliação de nossos analistas;
- Se o email está associado a qualquer campanha conhecida;
- e muito mais.

Após a conclusão da investigação raiz, o guia estratégico fornece uma lista de ações recomendadas a serem executadas.
  
Em seguida, várias etapas de busca são executadas:

- Mensagens de email semelhantes em outros clusters de email são pesquisadas.
- O sinal é compartilhado com outras plataformas, como o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).
- É feita uma determinação sobre se algum usuário clicou na mensagem de email suspeita.
- Uma verificação é feita entre O Office 365 [EOP](eop/exchange-online-protection-eop.md) e a [ATP](office-365-atp.md) para ver se há outras mensagens semelhantes relatadas pelos usuários.
- Uma verificação é feita para ver se um usuário foi comprometido. Esta verificação utiliza sinais no [Microsoft Cloud app Security](https://docs.microsoft.com/cloud-app-security) e no [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlacionando qualquer evento ou alerta relacionado. 

Durante a fase de caça, riscos e ameaças são atribuídos a várias etapas de busca.  

Correção é a fase final do guia estratégico. Durante esta fase, as etapas de correção são tomadas, com base nas fases de investigação e busca.  

## <a name="getting-started"></a>Introdução

Para acessar suas investigações, como administrador global do Office 365 ou administrador de segurança, vá para o centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança do Office 365 () e entre. Em seguida, siga um destes procedimentos:

- No painel de navegação à esquerda, vá para**investigações**de **Gerenciamento** > de ameaças.

    ou

- Visite o painel de gerenciamento de ameaças (no centro de conformidade do & de segurança, vá para o**painel** **Gerenciamento** > de ameaças).

![Widgets do AIR](media/air-widgets.png)

Seus widgets do AIR serão exibidos na parte superior do [painel de segurança](security-dashboard.md). Selecione um widget para começar.

### <a name="automated-investigations"></a>Investigações automatizadas

A página de investigações automatizadas mostra as investigações da organização e seus Estados atuais.

![Página de investigação principal para AIR](media/air-maininvestigationpage.png) 
  
Você pode:
- Navegue diretamente para uma investigação (selecione uma **ID de investigação**).
- Aplicar filtros. Escolha um **tipo de investigação**, **intervalo de tempo**, **status**ou uma combinação desses.
- Exporte os dados para um arquivo CSV.

### <a name="investigation-graph"></a>Gráfico de investigação

Ao abrir uma investigação específica, você verá a página de gráfico de investigação. Esta página mostra todas as diferentes entidades: mensagens de email, usuários (e suas atividades) e dispositivos que foram investigados automaticamente como parte do alerta que foi acionado.

![Página de gráfico de investigação aérea](media/air-investigationgraphpage.png)

Você pode:
- Obtenha uma visão geral da investigação atual.
- Exibir um resumo dos intervalos de investigação.
- Selecione um nó na visualização para exibir detalhes desse nó.
- Selecione uma guia na parte superior para exibir os detalhes dessa guia.

### <a name="alert-investigation"></a>Investigação de alerta

Na guia **alertas** de uma investigação, você pode ver todos os alertas relevantes para a investigação. Os detalhes incluem o alerta que disparou a investigação e outros alertas, como entrada arriscada, download em massa, etc., que são correlacionados à investigação. A partir dessa página, um analista de segurança também pode exibir detalhes adicionais sobre alertas individuais.

![Página alertas de ar](media/air-investigationalertspage.png)

Você pode:
- Obtenha uma visão geral do alerta de acionamento atual e de todos os alertas associados.
- Selecione um alerta na lista para abrir uma página de sobrevôo que mostre detalhes completos do alerta.

### <a name="email-investigation"></a>Investigação de email

Na guia **email** de uma investigação, você pode ver todos os clusters de email identificados como parte da investigação. 

Dado o volume simples de email que os usuários de uma organização enviam e recebem, o processo de 
- agrupar mensagens de email com base em atributos semelhantes de um cabeçalho de mensagem, corpo, URL e anexo; 
- separar emails mal-intencionados do email em bom estado; e 
- executar ações em mensagens de email mal-intencionadas 

pode levar várias horas. Agora, o ar automatiza esse processo, poupando o tempo e esforço da equipe de segurança da sua organização. 

Por exemplo, considere a imagem a seguir. O primeiro cluster de três mensagens de email foi considerado como phishing. Outro cluster de mensagens semelhantes com o mesmo IP e assunto foi encontrado e é considerado mal-intencionado, pois alguns deles foram identificados como phishing durante a detecção inicial. 

![Página investigação de emails de ar](media/air-investigationemailpage.png)

Você pode:
- Obtenha uma visão geral das ameaças e dos resultados de agrupamento atuais encontrados.
- Clique em uma entidade de cluster ou uma lista de ameaças para abrir uma página de saída que mostra os detalhes completos do alerta.

![Email de investigação de ar com detalhes de submenu](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a>Investigação de usuário

Na guia **usuários** , você pode ver todos os usuários identificados como parte da investigação. 

Por exemplo, na imagem a seguir, o AIR identificou indicadores de comprometimento e anomalias com base em uma nova regra de caixa de entrada que foi criada. Detalhes adicionais (evidência) da investigação estão disponíveis por meio de exibições detalhadas nesta guia.

![Página usuários de investigação aérea](media/air-investigationuserspage.png)

Você pode:
- Obtenha uma visão geral dos resultados do usuário identificados e dos riscos encontrados.
- Selecione um usuário para abrir uma página de sobrevôo que mostre os detalhes completos do alerta.

### <a name="machine-investigation"></a>Investigação de máquina

Na guia **computadores** , você pode ver todas as máquinas identificadas como parte da investigação. 

![Página da máquina de investigação de ar](media/air-investigationmachinepage.png)

Como parte da investigação, o AIR correlaciona ameaças de email a dispositivos. Por exemplo, uma investigação passa um hash de arquivo para o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) para investigar. Isso permite a investigação automatizada de máquinas relevantes para seus usuários e ajuda a garantir que as ameaças sejam tratadas tanto na nuvem quanto em seus dispositivos. 

Você pode:
- Obtenha uma visão geral das máquinas e ameaças atuais encontradas.
- Selecione uma máquina para abrir um modo de exibição que nas [investigações ATP relacionadas do Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).

### <a name="entity-investigation"></a>Investigação de entidade

Na guia **entidades** , você pode ver todas as máquinas identificadas como parte da investigação. 

Aqui, você pode ver as entidades investigadas. Você pode ver detalhes dos tipos de entidades, como mensagens de email, clusters, endereços IP, usuários e muito mais. Você também pode ver quantas entidades foram analisadas e as ameaças que foram associadas a cada uma delas. 

![Página de entidades de investigação aérea](media/air-investigationentitiespage.png)

Você pode:
- Obtenha uma visão geral das entidades e ameaças de investigação encontradas.
- Selecione uma entidade para abrir uma página de saída que mostre os detalhes relacionados da entidade.

![Detalhes das entidades de investigação aérea](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Log do guia estratégico

Na guia **log** , você pode ver todas as etapas do guia estratégico que ocorreram durante a investigação. O log captura um inventário completo de todas as ações concluídas por recursos de inteligência de ameaças do Office 365 como parte do ar. Ele fornece uma visão clara de todas as etapas executadas, incluindo a própria ação, uma descrição e a duração do real do início ao fim. 

![Página de log de investigação de ar](media/air-investigationlogpage.png)

Você pode:
- Obtenha uma visão geral das etapas do guia estratégico.
- Exportar os resultados para um arquivo CSV.
- Filtrar o modo de exibição.

### <a name="recommended-actions"></a>Ações recomendadas

Na guia **ações** , você pode ver todas as ações do guia estratégico que são recomendadas para correção após a conclusão da investigação. 

As ações capturam uma lista completa de todas as etapas que a Microsoft recomenda que você faça no final de uma investigação. Você pode realizar ações de correção aqui selecionando uma ou mais ações. Clicar em **aprovar** permitirá que a correção seja iniciada. (As permissões apropriadas podem ser necessárias. Por exemplo, um leitor de segurança pode exibir ações, mas não aprová-las.)  

![Página de ação de investigações aéreas](media/air-investigationactionspage.png)

Você pode:
- Obtenha uma visão geral das ações recomendadas para o guia estratégico.
- Selecione uma única ação ou várias ações.
- Aprovar ações recomendadas. (Estes são iniciados imediatamente com comentários.)
- Exportar os resultados para um arquivo CSV.
- Filtrar o modo de exibição.

## <a name="how-to-get-air"></a>Como obter o AIR

No momento, o AIR está em visualização. Quando lançado, o ar será incluído nas seguintes assinaturas:

- Microsoft 365 Enterprise E5
- Office 365 Enterprise E5
- Proteção contra ameaças da Microsoft
- Office 365 plano avançado de proteção contra ameaças 2

Para saber mais sobre a disponibilidade de recursos, visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).
