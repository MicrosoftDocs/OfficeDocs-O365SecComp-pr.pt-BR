---
title: Criar um aviso de isenção legal
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
ms.openlocfilehash: 8db5a21f60a1d73c11e28bc2765a95c23646115d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706072"
---
# <a name="create-a-legal-hold-notice"></a>Criar um aviso de isenção legal

Usando as comunicações do eDiscovery avançado (Preview) dos responsáveis, as organizações podem gerenciar seu fluxo de trabalho em torno de comunicação com responsáveis. Por meio da ferramenta de comunicações, as equipes jurídicas sistemática podem enviar, coletar e controlar notificações de retenção legal. O processo de criação flexível também permite que as equipes personalizar o fluxo de trabalho de notificação de espera e o conteúdo nos avisos enviadas aos responsáveis. 

O artigo descreve as etapas do fluxo de trabalho de notificação de espera.

## <a name="step-1-specify-communication-details"></a>Etapa 1: Especificar detalhes de comunicação

A primeira etapa é especificar os detalhes do apropriados de avisos de isenção legal ou outras comunicações dos responsáveis. 

1. No Centro de conformidade de segurança &, vá para **eDiscovery avançado do eDiscovery gt _ (Preview)** para exibir a lista de ocorrências em sua organização.
   
2. Clique na guia **comunicações** e clique em **nova comunicação**.
   
3. Na página de **comunicação de nome** , especifique os seguintes detalhes de comunicação (obrigatório).

    - **Nome**: esse é o nome para a comunicação.
    
    - **Responsável de emissão**: A lista suspensa exibe uma lista de membros um caso. Cada aviso enviado aos responsáveis será enviado em nome responsável pela emissora especificado.

4. Clique em **Avançar**.

## <a name="step-2-define-the-portal-content"></a>Etapa 2: Definir o conteúdo do portal

Em seguida, você pode criar e adicionar o conteúdo do aviso de isenção. Na página **definir conteúdo do portal** no Assistente de **comunicação de criar** , especifique o conteúdo do aviso de isenção. Esse conteúdo será automaticamente acrescentado aos avisos de emissão, emita novamente, lembrete e escalonamento. Além disso, esse conteúdo aparecerá no Portal de conformidade de responsáveis. 

Para criar o conteúdo do portal:

1. Tipo (ou recortar e paster de outro documento) sua espera aviso na caixa de texto para o conteúdo do portal. 

2. Inserir variáveis direta em seu aviso para personalizar o aviso e compartilhar o Portal de conformidade dos responsáveis.

3. Clique em **Avançar**.

  >[!Tip]
  >Para saber que mais sobre como podem personalizar o conteúdo e o formato do conteúdo do portal, consulte [usar o Editor de comunicações](using-communications-editor.md).

## <a name="step-3-set-the-required-notifications"></a>Etapa 3: Definir as notificações necessárias

Depois de definir o conteúdo do aviso de isenção, você pode configurar os fluxos de trabalho em torno de envio e gerenciar o processo de notificação. As notificações são mensagens de email que são enviadas para notificar e acompanhamento de pacientes com responsáveis. Cada dos responsáveis adicionado à comunicação receberá a mesma notificação. 

Para configurar e enviar um aviso de isenção, você deve incluir a emissão, Re-emissão e liberar notificações.

### <a name="issuance-notification"></a>Notificação de publicação 

Depois que a comunicação é criada, a **Notificação de emissão** é iniciada pelo responsável pela emitindo especificado. A notificação de emissão é a primeira comunicação enviada para dos responsáveis para informá-los sobre suas obrigações de preservação. 

Para criar uma notificação de publicação:

1. Em blocos de **emissão** , clique em **Editar**.
   
2. Se necessário, adicione membros de maiusculas adicionais ou equipe aos campos **Cc** e **Cco** . Para adicionar vários usuários a esses campos, separe os endereços de email com um ponto e vírgula.
   
3. Especifique o **assunto** para o aviso (obrigatório).
   
4. Especifique o conteúdo ou instruções adicionais que você gostaria de fornecer ao dos responsáveis (obrigatório). Observe que o conteúdo de portal que você definiu na etapa 2 é adicionado ao final do aviso de emissão. 
   
5. Clique em **Salvar** 

### <a name="re-issuance-notification"></a>Notificação de re-emissão 

Como o andamento de maiusculas, responsáveis podem ser necessários para preservar dados adicionais ou que anteriormente era instruído. Depois de atualizar o conteúdo do aviso de isenção, a notificação de re-emissão alertas os responsáveis sobre as alterações para suas obrigações de preservação.

Para criar uma notificação de re-emissão: 

1. Em blocos **emita novamente** , clique em **Editar**.
   
2. Se necessário, adicione membros de maiusculas adicionais ou equipe aos campos **Cc** e **Cco** . Para adicionar vários usuários a esses campos, separe os endereços de email com um ponto e vírgula.
   
3. Especifique o **assunto** para o aviso (obrigatório).
   
4. Especifique o conteúdo ou instruções adicionais que você gostaria de fornecer ao dos responsáveis (obrigatório). Observe que o conteúdo de portal que você definiu na etapa 2 é adicionado ao final do aviso re-emissão.
   
5. Clique em **Salvar**.

>[!Note]
>Se uma notificação de espera é modificada, a notificação de re-emissão será enviada automaticamente para todos os responsáveis atribuídos para o aviso. Depois que a notificação é enviada, responsáveis serão solicitados a confirmar novamente sua aviso de isenção. Se você tiver configurado a qualquer lembrete ou escalonamento fluxos de trabalho, eles também serão iniciado novamente. 

### <a name="release-notification"></a>Notificação de versão

Depois que uma questão for resolvida ou se um funcionário encarregado não está mais sujeito às preserve conteúdo, você pode liberar dos responsáveis de um caso. Se dos responsáveis anteriormente foi emitido um aviso de isenção, a notificação de versão pode ser usada para alertar responsáveis que eles foram liberados da sua obrigação.

Para criar uma notificação de versão: 

1. No lado a lado de **versão** , clique em **Editar**.
   
2. Se necessário, adicione membros de maiusculas adicionais ou equipe aos campos **Cc** e **Cco** . Para adicionar vários usuários a esses campos, separe os endereços de email com um ponto e vírgula.
   
3. Especifique o **assunto** para o aviso (obrigatório).
   
4. Especifique o conteúdo ou instruções adicionais que você gostaria de fornecer ao dos responsáveis (obrigatório).
   
5. Clique em **Salvar** e vá para a próxima etapa. 

## <a name="optional-step-4-set-the-optional-notifications"></a>(Opcional) Etapa 4: Configurar as notificações opcionais

Opcionalmente, você pode simplificar o fluxo de trabalho para acompanhar com não responde responsáveis pela criação e agendamento de lembrete automatizado e escalonamento notificações.

### <a name="reminders"></a>Lembretes

Depois que você enviou uma notificação de espera, você pode acompanhamento de pacientes com responsáveis não responde definindo-se um fluxo de trabalho do lembrete. 

Para agendar lembretes:

1. No lado a lado do **lembrete** , clique em **Editar**.
   
2. Ative o fluxo de trabalho do **lembrete** , ativando a alternância de **Status** (obrigatória).
   
3. Especifique o **intervalo do lembrete (em dias)** (obrigatório). Esse é o número de dias de espera antes de enviar as notificações de lembrete primeiro e acompanhamento. Por exemplo, se você definir o intervalo de lembrete para 7 dias, em seguida, primeiro lembrete seria enviado 7 dias após a notificação de isenção inicialmente foi emitida. Todos os lembretes subsequentes também seriam enviados a cada 7 dias.
   
4. Especifique o **número de lembretes** (obrigatório). Este campo especifica quantos lembretes para enviar aos responsáveis não responsivos. Por exemplo, se você definir o número de lembretes como 3, um funcionário encarregado receberiam um máximo de 3 lembretes. Depois que um funcionário encarregado reconhece a notificação de isenção, lembretes não mais serão enviados para o usuário.
   
5. Especifique o **assunto** para o aviso (obrigatório). 
   
6. Especifique o conteúdo ou instruções adicionais que você gostaria de fornecer ao dos responsáveis (obrigatório). Observe que o conteúdo de portal que você definiu na etapa 2 é adicionado ao final do aviso de lembrete.
   
7. Clique em **Salvar** e acesse a próxima etapa.

### <a name="escalations"></a>Escalonamentos 

Em alguns casos, talvez seja necessário descobrir outras maneiras de acompanhamento de pacientes com responsáveis não responde. Se um funcionário encarregado não confirmar uma notificação de espera após receber o número especificado de lembretes, a equipe jurídica pode especificar um fluxo de trabalho para enviar automaticamente um aviso de escalonamento para dos responsáveis e seu gerente.

Para agendar escalonamentos:

1. No lado a lado **escalonamento** , clique em **Editar**.
   
2. Ative o fluxo de trabalho de **escalonamento** , ativando a alternância de **Status** .
   
3. Especifique o **intervalo de escalonamento (em dias)** (obrigatório). 
   
4. Especifique o **número de escalonamentos** (obrigatório). Este campo especifica quantos escalonamentos para enviar aos responsáveis não responsivos. Por exemplo, se você definir o número de escalonamentos como 3, em seguida, um aviso de escalonamento seria ser enviado ao dos responsáveis e seu gerente um máximo de vezes que 3. Depois que um funcionário encarregado reconhece a notificação de isenção, escalonamentos não serão enviados. 
   
5. Especifique o **assunto** para o aviso (obrigatório). 
   
6. Especifique o conteúdo ou instruções adicionais que você gostaria de fornecer ao dos responsáveis (obrigatório). Observe que o conteúdo de portal que você definiu na etapa 2 é adicionado ao final do aviso de escalonamento.
   
7. Clique em **Salvar** e acesse a próxima etapa.
   
## <a name="step-5-assign-custodians"></a>Etapa 5: Atribuir responsáveis 

Depois de finalizar o conteúdo para notificações, selecione os responsáveis aos quais enviar as notificações. 

Para adicionar responsáveis:

1. Atribua responsáveis à comunicação clicando na caixa de seleção ao lado do nome dele.

    Depois que a comunicação é criada, o fluxo de trabalho de notificação se aplicará automaticamente aos responsáveis selecionados.
   
2. Clique em **próximo** para revisar as configurações de comunicação e os detalhes.
 
>[!NOTE]
>Você só pode adicionar responsáveis que foram adicionados ao caso e ainda não foi enviados outra notificação dentro o caso.

## <a name="step-6-review-settings"></a>Etapa 6: Configurações de revisão

Depois de revisar as configurações e clique em **Enviar** para concluir a comunicação, o sistema iniciará automaticamente o fluxo de trabalho de comunicação enviando o aviso de emissão.