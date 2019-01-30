---
title: Trabalhando com a comunicação no eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b27d6cca0382b18123cae4106f77ce0dcdf5e525
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607383"
---
# <a name="working-with-communications-in-advanced-ediscovery-preview"></a>Trabalhando com a comunicação no eDiscovery avançado (Preview)

EDiscovery avançado (Preview) permite que os departamentos legais simplificar seus processos em torno de acompanhamento e distribuir as notificações de retenção legal. O recurso de comunicação dos responsáveis permite que os departamentos legais gerenciar e automatizar seus processos de retenção legal inteira – de notificações e lembretes escalonamentos – tudo em um único local.

## <a name="what-is-a-legal-hold-notification"></a>O que é uma notificação de retenção legal?

Um aviso de isenção legal (também conhecido como um *bloqueio de litígio*) é uma notificação enviada do departamento jurídico de uma organização para os funcionários, a equipe contingente ou outros responsáveis de dados. Essas notificações instruem responsáveis para preservar as informações armazenadas eletronicamente (ESI), bem como qualquer material que pode ser relevante para uma questão legal ativo ou iminente. As equipes jurídicas devem saber que cada responsável recebeu, ler e compreendidos e acordado em conformidade com as instruções de determinado.

## <a name="the-legal-hold-notification-process"></a>O departamento jurídico mantenha o processo de notificação

Uma organização tem um imposto para preservar as informações relevantes quando ele aprende sobre um litígio iminente ou investigação normas. Para atender aos seus requisitos de preservação, a organização deve informar imediatamente responsáveis potenciais sobre seu dever para preservar as informações relevantes. 

Com o eDiscovery avançado (Preview), as equipes jurídicas podem criar e personalizar seu fluxo de trabalho de notificação de retenção legal. O recurso de comunicação dos responsáveis permite que as equipes jurídicas definir as seguintes avisos e fluxos de trabalho:

1. **Aviso de publicação**: um aviso de isenção legal é emitido (ou iniciado) por uma notificação do departamento jurídico aos responsáveis que podem ter informações relevantes sobre o tópico de caso. Este aviso instrui os responsáveis para preservar todas as informações que podem ser necessários para descoberta. 
   
2.  **Aviso de re-emissão**: responsáveis durante um caso, talvez seja necessário para preservar adicionais ou menos informações que anteriormente era instruídas. Para este cenário, você pode atualizar o aviso de isenção existente e retransmite aos seus responsáveis.

3.  **Aviso de versão**: depois que uma questão for resolvida e dos responsáveis não são mais estão sujeito a um imposto preservação, dos responsáveis poderão ser liberados para que informações é não são mais retidas se não for necessário. Além disso, seu dos responsáveis serão notificado de que eles não estão mais em dever preservação e com excelentes instruções sobre como retomar suas atividades.

4. **Escalonamentos e lembretes**: em alguns casos, apenas um aviso de emissão não é suficiente para satisfazer exigências legais de descoberta. Com cada notificação, as equipes jurídicas podem agendar um conjunto de fluxos de trabalho de lembrete e escalonamento para automaticamente o acompanhamento de pacientes com responsáveis não responde.

    - **Lembretes**: depois que foi emitido um aviso de isenção legal ou novamente emitido para um conjunto de responsáveis, uma organização pode configurar lembretes para alertar os responsáveis não responde. 

    - **Escalonamentos**: em alguns casos, se um funcionário encarregado permanecer não responde mesmo após um conjunto de lembretes, a equipe jurídica pode configurar um fluxo de trabalho de escalonamento para notificar dos responsáveis e dele manager.

## <a name="role-groups-and-permissions"></a>Grupos de funções e permissões 

As equipes jurídicas podem controlar e suas atividades maiusculas usando grupos de funções relacionadas a descoberta eletrônica e permissões no Centro de conformidade do & de segurança do segmento. 

Para criar e gerenciar notificações de retenção legal, um usuário deve fazer parte do grupo de função a seguir:

- **gerente de descoberta eletrônica** - membros desse grupo de função pode criar e gerenciar casos do eDiscovery. Eles podem adicionar e remover membros, coloque os responsáveis e locais de conteúdo em espera, gerenciar notificações de retenção legal, criar e editar pesquisas de conteúdo associados a um caso, exportar os resultados de uma pesquisa de conteúdo e preparar os resultados da pesquisa para análise em Avançado descoberta eletrônica (Preview). Existem dois subgrupos nesse grupo de função. A diferença entre esses subgrupos baseia-se em escopo.

  - **gerente de descoberta eletrônica** - pode exibir e gerenciar os casos de eDiscovery que eles criam ou serão um membro do. Se outra eDiscovery Manager cria um caso, mas não adiciona um segundo eDiscovery Manager como membro desse caso, a segunda eDiscovery Manager não conseguirá exibir ou abrir o caso na página de descoberta eletrônica no Centro de conformidade do & de segurança. Gerentes de descoberta eletrônica também pode acessar seus casos de eDiscovery avançado (Preview) para executar tarefas de análise.

  - **administrador de descoberta eletrônica** - pode executar todas as tarefas de gerenciamento de casos que pode ser feito por uma gerente de descoberta eletrônica. Além disso, um administrador de eDiscovery pode:
    
    - Exibir todas as ocorrências listadas na página Descoberta Eletrônica.
    - Depois que eles adicionam-se como um membro do caso, gerencie qualquer caso na organização.
    - Acesse os dados maiusculas no eDiscovery avançado (Preview) para qualquer caso na organização.

Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Centro de conformidade do & de segurança do Office 365](../assign-ediscovery-permissions.md).