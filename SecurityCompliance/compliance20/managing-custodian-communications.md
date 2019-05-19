---
title: Trabalhar com comunicações na descoberta eletrônica avançada
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: A descoberta eletrônica avançada facilita o gerenciamento do fluxo de trabalho de notificação de retenção legal para notificar os responsáveis pelas investigações legais.
ms.openlocfilehash: cf5c8f5e932993255bda2cb959657c2c6ded3163
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154903"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a>Trabalhar com comunicações na descoberta eletrônica avançada

A descoberta eletrônica avançada permite que os departamentos jurídicos simplifiquem seus processos em torno de rastreamento e distribuição de notificações de retenção legal. A ferramenta de comunicações do bloqueador permite que os departamentos jurídicos gerenciem e automatizem todo o processo de retenção legal, de notificações iniciais, lembretes e escalações, tudo em um único local.

## <a name="what-is-a-legal-hold-notification"></a>O que é uma notificação de retenção legal?

Um aviso legal (também conhecido como uma *retenção de litígio*) é uma notificação enviada do departamento jurídico de uma organização para funcionários, funcionários contingentes ou responsáveis por dados que podem ser relevantes para uma investigação legal. Essas notificações instruem os responsáveis a preservar informações armazenadas eletronicamente, bem como qualquer conteúdo que possa ser relevante para uma questão legal ativa ou iminente. As equipes jurídicas devem saber que cada um deles recebeu, leu, entendeu e concordou em cumprir as instruções fornecidas.

## <a name="the-legal-hold-notification-process"></a>O processo de notificação de retenção legal

Uma organização tem uma obrigação de preservar as informações relevantes quando aprende sobre uma investigação legal ou litígio iminente. Para atender aos requisitos de preservação de uma investigação, a organização deve informar imediatamente os possíveis responsáveis sobre sua obrigação de preservar as informações relevantes.

Com a descoberta eletrônica avançada, as equipes jurídicas podem criar e personalizar o fluxo de trabalho de notificação de retenção legal. A ferramenta de comunicações de responsáveis permite que as equipes jurídicas configurem os seguintes avisos e fluxos de trabalho:

1. **Aviso de emissão**: um aviso de retenção legal é emitido (ou iniciado) por uma notificação do departamento jurídico para os responsáveis que podem ter informações relevantes sobre o caso. Este aviso instrui os responsáveis a preservar qualquer informação que possa ser necessária para descoberta.
   
2.  **Aviso**de reemissão: durante um caso, os responsáveis podem ser necessários para preservar conteúdo adicional (ou menos conteúdo) do que foi solicitado anteriormente. Para este cenário, você pode atualizar o aviso de bloqueio existente e reemitir-o para os responsáveis.

3.  **Aviso de lançamento**: quando uma questão é resolvida e o desejo não está mais sujeito a um requisito de preservação, os responsáveis podem ser liberados do caso. Além disso, você pode notificar os responsáveis de que eles não são mais necessários para preservar o conteúdo e fornecem instruções sobre como retomar a atividade de trabalho normal com relação aos seus dados.

4. **Remententes e escalonamentos**: em alguns casos, apenas a emissão de um aviso não é suficiente para atender aos requisitos de descoberta legal. Com cada notificação, as equipes jurídicas podem agendar um conjunto de fluxos de trabalho de lembrete e escalonamento para acompanhar automaticamente os responsáveis que não respondem.

    - **Lembretes**: após um aviso de retenção legal ter sido emitido ou emitido novamente para um conjunto de responsáveis, uma organização pode configurar lembretes para alertar os responsáveis por não responder.

    - **Escalonamentos**: em alguns casos, se um dos responsáveis permanecer sem resposta, mesmo após um conjunto de lembretes por um período de tempo, a equipe jurídica poderá configurar um fluxo de trabalho de escalonamento para notificar os responsáveis sem resposta e seu gerente.

## <a name="role-groups-and-permissions"></a>Grupos de funções e permissões 

As equipes jurídicas podem controlar e separar suas atividades de caso usando grupos de função e permissões de descoberta eletrônica no centro de conformidade do & de segurança. 

Para criar e gerenciar notificações de retenção legal, um usuário deve fazer parte dos seguintes grupos de função:

- **Gerenciador de descoberta eletrônica** -os membros desse grupo de funções podem criar e gerenciar ocorrências de descoberta eletrônica. Eles podem adicionar e remover membros, colocar os responsáveis e os locais de conteúdo em espera, gerenciar notificações de retenção legal, criar e editar pesquisas de conteúdo associadas a uma ocorrência, exportar os resultados de uma pesquisa de conteúdo e preparar os resultados da pesquisa para análise no Advanced descobertas. Há dois subgrupos nesse grupo de função. A diferença entre esses subgrupos está no escopo.

  - **Gerenciador de descoberta eletrônica** – pode exibir e gerenciar os casos de descoberta eletrônica que eles criam ou são membros de. Se outro gerenciador de descoberta eletrônica criar uma ocorrência, mas não adicionar um segundo Gerenciador de descoberta eletrônica como membro desse caso, o segundo Gerenciador de descoberta eletrônica não poderá exibir ou abrir o caso na página descoberta eletrônica no centro de conformidade do & de segurança. Os gerentes de descoberta eletrônica também podem acessar seus casos na descoberta eletrônica avançada para executar tarefas de análise.

  - **administrador de descoberta eletrônica** – pode executar todas as tarefas de gerenciamento de caso que um gerente de descoberta eletrônica possa fazer. Além disso, um Administrador de Descoberta Eletrônica pode:
    
    - Exibir todas as ocorrências listadas na página Descoberta Eletrônica.
    - Gerencie qualquer caso na organização depois que eles se adicionarem como um membro do caso.
    - Acessar dados de caso na descoberta eletrônica avançada para qualquer caso na organização.

Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no centro de conformidade do & de segurança](../assign-ediscovery-permissions.md).