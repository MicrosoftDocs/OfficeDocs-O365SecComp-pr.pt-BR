---
title: Configurar as notificações de spam do usuário final no Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Você pode configurar as notificações de spam do usuário final para a política de filtro de spam de toda a empresa padrão ou para políticas de filtro de spam personalizadas que são aplicadas aos domínios.
ms.openlocfilehash: 4a4c7c6b139fe0f8b0a1f6b69c1b95e321293af5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027528"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Configurar as notificações de spam do usuário final no Exchange Online

> [!IMPORTANT]
> Este tópico é para clientes Exchange Online que estão protegendo as caixas de correio hospedadas em nuvem. Clientes do Exchange Online Protection (EOP) que estão protegendo as caixas de correio locais em vez disso, devem ler o tópico a seguir: [Configure notificações de spam do usuário final no EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Você pode configurar as notificações de spam do usuário final para a política de filtro de spam de toda a empresa padrão ou para políticas de filtro de spam personalizadas que são aplicadas aos domínios. Habilitar mensagens de notificação de spam do usuário final permite que os usuários finais autogerenciar suas próprias mensagens em quarentena de spam. Notificações de spam do usuário final não podem ser usadas com políticas aplicadas a usuários ou grupos ou a uma diretiva com exceções.
  
As notificações de spam do usuário final contém uma lista de todas as mensagens de spam em quarentena que o usuário final recebeu durante um período de tempo que você configurou (você pode especificar um valor entre 1 e 15 dias). Você também pode configurar o idioma no qual a mensagem de notificação será escrita.
  
Após receber uma mensagem de notificação, os usuários dinais podem clicar para mover o email de spam para a caixa de entrada ou relatar o email de spam como Não é Lixo Eletrônico, neste caso será enviado para a Equipe de Análise de Spam do Microsoft. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

Tempo estimado para conclusão: 2 minutos
  
Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Antispam" no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Use o EAC para configurar as notificações de spam do usuário final

1. No Centro de Administração do Exchange (EAC), navegue até **Proteção** \> **Filtro de conteúdo**.
    
2. Selecione a política de filtro de spam para o qual você deseja habilitar as notificações de spam do usuário final (elas são desabilitadas por padrão).
    
3. No painel direito, onde as informações resumidas sobre política aparecem, clique no link **Configurar notificações de spam para o usuário final**. 
    
4. Na caixa de diálogo posterior, você pode configurar as seguintes opções:
    
1. **Habilitar notificações de spam para o usuário final** Marque esta caixa de seleção para habilitar notificações de spam para o usuário final para esta política. (De outra forma, se esta política estiver habilitada, você pode desmarcar esta caixa de seleção para desabilitar as notificações de spam para usuário final para esta política.) 
    
2. **Envie notificações de spam para o usuário final a cada (dias)** Especifique a frequência com a qual as notificações de spam para o usuário final são enviadas. O padrão é 3 dias. Você pode especificar entre 1 e 15 dias. Se você especificar 7 dias, por exemplo, a notificação incluirá uma lista de todas as mensagens para aquele usuários dos últimos 7 dias que foram enviadas para a quarentena de spam. 
    
3. **Idioma da notificação** Usando a lista suspensa, escolha o idioma de escrita das notificações de spam para o usuário final para esta diretiva. 
    
5. Clique em **Salvar**. Um resumo das suas configurações de política de filtro de spam, incluindo as configurações de notificação de spam do usuário final, é exibida no painel direito.
    
> [!NOTE]
>  Notificações de spam do usuário final só serão funcionais para as políticas de filtro de spam que estão habilitadas. > Notificações de spam usuário final são enviadas apenas uma vez por dia. O tempo de entrega da notificação não pode ser garantido para qualquer cliente específico e não é configurável. 
  
 **Dica:** Se você deseja testar as notificações de spam do usuário final, enviando a um conjunto limitado de usuários antes de implementá-las de totalmente, crie uma política de filtro de spam personalizada que permite que as notificações de spam do usuário final para os domínios nos quais os usuários residem. Em seguida, no EAC, em **fluxo de email \> regras**, criar uma regra de transporte para bloquear mensagens de quarantine@messaging.microsoft.com (o endereço de email que envia notificações), com exceções para os usuários que você deseja receber notificações. A imagem a seguir está um exemplo de como criar uma exceção para dois usuários (SaraD e Antoniot) do domínio Contoso.com: 
  
![Regra de transporte para testar notificações de spam do usuário final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Para obter mais informações

[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
