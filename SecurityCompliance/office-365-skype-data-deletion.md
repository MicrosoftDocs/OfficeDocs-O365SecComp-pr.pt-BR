---
title: O Office 365 Skype para exclusão de dados corporativos
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
description: Uma explicação de exclusão de dados em Skype para negócios.
ms.openlocfilehash: f3ddd0ad0797c465857919e8f7b28341492769ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524308"
---
# <a name="skype-for-business-data-deletion-in-office-365"></a>Skype para exclusão de dados corporativos no Office 365

O Skype for Business oferece arquivamento de mensagens instantâneas ponto a ponto, mensagens instantâneas entre várias pessoas e atividades de carregamento de conteúdo em reuniões. O recurso de arquivamento requer o Exchange e é controlado pelo atributo de Bloqueio In-loco da caixa de correio do Exchange do usuário, que arquiva tanto o email quanto o conteúdo do Skype for Business.

Todo o arquivamento no Skype for Business é considerado "arquivamento de nível do usuário" porque é possível habilitá-lo ou desabilitá-lo para um ou mais usuários ou grupos de usuários específicos criando, configurando e aplicando uma política de arquivamento de nível do usuário para esses usuários. Não há controle direto das configurações de arquivamento de dentro do Centro de administração do Skype for Business.

Os seguintes tipos de conteúdo não são arquivados no Skype para negócios: 
- Transferências de arquivos de ponto a ponto
- Áudio/vídeo para mensagens instantâneas de ponto a ponto e conferências
- Compartilhamento de aplicativo para mensagens instantâneas ponto a ponto e conferências
- Anotações de conferência 

## <a name="meeting-content-retention"></a>Retenção de conteúdo de reunião
Clientes que usam o Skype para negócios podem carregar conteúdo para um Skype para reunião de negócios como anexos, como apresentações do PowerPoint, OneNote arquivos e outros arquivos. O período de retenção de conteúdo que foram carregado para uma reunião é o seguinte:
- **Reunião única** - conteúdo é retido por 15 dias começando a partir de quando a última pessoa deixou a reunião.
- **Reunião recorrente** - conteúdo é retido por 15 dias após a última pessoa deixou a última sessão da reunião. O timer de retenção redefine se alguém ingressar a mesma sessão de reunião em 15 dias. Por exemplo, suponha que um Skype para reunião de negócios está programada para ocorrer semanalmente por um ano, e um arquivo carregado para a reunião durante a primeira instância. Se pelo menos uma pessoa ingressar na sessão de reunião toda semana, o arquivo é mantido no Skype para servidores corporativos Online para o ano inteiro plus 15 dias após a última pessoa deixou a última reunião da série.
- Conteúdo da **reunião reunir agora** - é mantido por 8 horas após a hora de término da reunião.

> [!NOTE]
> Se um usuário não licenciado ou desabilitado (por exemplo, se **msRTCSIP-userenabled** estiver definida como *False*) e é licenciado novamente ou reabilitada, conteúdo da reunião não é mantido.

## <a name="meeting-expiration"></a>Expiração de reunião
Os usuários podem acessar uma reunião específica, após a reunião ter terminado, sujeitos aos seguinte períodos de expiração:
- **Reunião única** - reunião expira 14 dias após a reunião agendada hora de término.
- **Reunião recorrente com data de término** - reunião expira 14 dias após a hora de término agendada da última ocorrência de reunião.
- A **reunião reunir agora** - reunião expira após 8 horas.

## <a name="whiteboard-collaboration"></a>Colaboração de quadro de comunicações
As anotações feitas em quadros de comunicações serão vistas por todos os participantes. Ao salvar um quadro de comunicações, o quadro de comunicações e todas as anotações serão armazenadas em um Skype para Business server, e ele será retido no servidor de acordo com as diretivas de expiração de conteúdo de reunião definida pelo administrador.

## <a name="audio-test-service"></a>Serviço de teste de áudio
Uma amostra de short (aproximadamente 5 segundos) da sua voz é registrada durante a chamada do serviço de teste de áudio. O exemplo de voz é usado por você para verificar e/ou verificar a qualidade do som de sua Skype para chamada de negócios com base na qualidade da gravação. Quando a chamada de serviço de teste de áudio for encerrada, a amostra de voz é excluída.

## <a name="persistent-group-chat"></a>Chat de grupo persistente
O Chat de grupo persistente armazena o conteúdo das conversas de bate-papo de grupo. Se for habilitada, o administrador pode controlar o período de retenção, o servidor no qual essas informações são armazenadas, se o histórico de Chat de grupo será arquivado para conformidade ou outras finalidades e gerenciar/modificar quaisquer propriedades em uma sala. Os usuários com funções diferentes têm acesso diferente para os dados persistentes, da seguinte maneira:
- Os administradores podem excluir conteúdo mais antigo (por exemplo, o conteúdo publicado antes de uma determinada data) de qualquer sala de chat para evitar que crescendo significativamente o tamanho do banco de dados. Ou, podem remover ou substituir mensagens consideradas inadequados para uma determinada sala de chat (ou considerado inadequada).
- Os usuários finais, incluindo os autores das mensagens, não é possível excluir o conteúdo de qualquer sala de chat.
- Gerentes de sala de chat podem desabilitar salas, mas não é possível excluir salas. Apenas administradores podem excluir uma sala de bate-papo após sua criação.