---
title: Trabalhar com comunicações na descoberta eletrônica avançada (visualização)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 916691e1f2470ef9e9e54d9dfe06c5277a92ba53
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296084"
---
# <a name="work-with-communications-in-advanced-ediscovery-preview"></a>Trabalhar com comunicações na descoberta eletrônica avançada (visualização)

A descoberta eletrônica avançada (visualização) permite que os departamentos jurídicos simplifiquem seus processos em torno de rastreamento e distribuição de notificações de retenção legal. O recurso de comunicações de responsáveis permite que os departamentos jurídicos gerenciem e automatizem todos os processos de retenção legal, de notificações, lembretes e escalonamentos em um só lugar.

## <a name="what-is-a-legal-hold-notification"></a>O que é uma notificação de retenção legal?

Um aviso legal (também conhecido como uma *retenção de litígio*) é uma notificação enviada do departamento jurídico de uma organização para funcionários, funcionários contingentes ou outros responsáveis por dados. Essas notificações instruem os responsáveis a preservar as ESI (electronicly Stored Information), bem como qualquer material que possa ser relevante para uma questão jurídica ativa ou iminente. As equipes jurídicas devem saber que cada um deles recebeu, leu e entendeu e concordou em cumprir as instruções fornecidas.

## <a name="the-legal-hold-notification-process"></a>O processo de notificação de retenção legal

Uma organização tem uma obrigação de preservar as informações relevantes quando aprende sobre uma investigação legal ou litígio iminente. Para atender aos requisitos de preservação, a organização deve informar imediatamente os possíveis responsáveis sobre sua obrigação de preservar as informações relevantes. 

Com a descoberta eletrônica avançada (visualização), as equipes jurídicas podem criar e personalizar o fluxo de trabalho de notificação de retenção legal. O recurso de comunicações de responsáveis permite que as equipes jurídicas configurem os seguintes avisos e fluxos de trabalho:

1. **Aviso de emissão**: um aviso de retenção legal é emitido (ou iniciado) por uma notificação do departamento jurídico para os responsáveis que podem ter informações relevantes sobre o caso. Este aviso instrui esses responsáveis a preservar qualquer informação que possa ser necessária para descoberta. 
   
2.  **Aviso**de reemissão: durante um caso, os responsáveis podem ser necessários para preservar informações adicionais ou menos do que foram instruídos anteriormente. Para este cenário, você pode atualizar o aviso de isenção existente e reemitir-o para seus responsáveis.

3.  **Aviso de lançamento**: quando uma questão é resolvida e o responsável não está mais sujeito a um imposto de preservação, os responsáveis podem ser liberados para que as informações não sejam mais mantidas, se não forem necessárias. Além disso, seus responsáveis serão notificados de que não estão mais sob o imposto de preservação e com instruções notáveis sobre como retomar suas atividades.

4. **Remententes e escalonamentos**: em alguns casos, apenas a emissão de um aviso não é suficiente para atender aos requisitos de descoberta legal. Com cada notificação, as equipes jurídicas podem agendar um conjunto de fluxos de trabalho de lembrete e escalonamento para acompanhar automaticamente os responsáveis que não respondem.

    - **Lembretes**: após um aviso de retenção legal ter sido emitido ou emitido novamente para um conjunto de responsáveis, uma organização pode configurar lembretes para alertar os responsáveis por não responder. 

    - **Escalonamentos**: em alguns casos, se um adversário permanecer sem resposta, mesmo depois de um conjunto de lembretes, a equipe jurídica pode configurar um fluxo de trabalho de escalonamento para notificar os responsáveis e seu gerente.

## <a name="role-groups-and-permissions"></a>Grupos de funções e permissões 

As equipes jurídicas podem controlar e segmentar a atividade de casos usando grupos de função e permissões de descoberta eletrônica no centro de conformidade do & de segurança. 

Para criar e gerenciar notificações de retenção legal, um usuário deve fazer parte dos seguintes grupos de função:

- **Gerenciador de descoberta eletrônica** -os membros desse grupo de funções podem criar e gerenciar ocorrências de descoberta eletrônica. Eles podem adicionar e remover membros, colocar os responsáveis e os locais de conteúdo em espera, gerenciar notificações de retenção legal, criar e editar pesquisas de conteúdo associadas a uma ocorrência, exportar os resultados de uma pesquisa de conteúdo e preparar os resultados da pesquisa para análise no Advanced Descoberta eletrônica (prévia). Há dois subgrupos nesse grupo de função. A diferença entre esses subgrupos baseia-se no escopo.

  - **Gerenciador de descoberta eletrônica** – pode exibir e gerenciar os casos de descoberta eletrônica que eles criam ou são membros de. Se outro gerenciador de descoberta eletrônica criar uma ocorrência, mas não adicionar um segundo Gerenciador de descoberta eletrônica como membro desse caso, o segundo Gerenciador de descoberta eletrônica não poderá exibir ou abrir o caso na página descoberta eletrônica no centro de conformidade do & de segurança. Os gerentes de descoberta eletrônica também podem acessar seus casos na descoberta eletrônica avançada (visualização) para realizar tarefas de análise.

  - **administrador de descoberta eletrônica** – pode executar todas as tarefas de gerenciamento de caso que um gerente de descoberta eletrônica possa fazer. Além disso, um administrador de descoberta eletrônica pode:
    
    - Exibir todas as ocorrências listadas na página Descoberta Eletrônica.
    - Gerencie qualquer caso na organização depois que eles se adicionarem como um membro do caso.
    - Acessar dados de caso na descoberta eletrônica avançada (visualização) para qualquer caso na organização.

Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no centro de conformidade do & de segurança do Office 365](../assign-ediscovery-permissions.md).