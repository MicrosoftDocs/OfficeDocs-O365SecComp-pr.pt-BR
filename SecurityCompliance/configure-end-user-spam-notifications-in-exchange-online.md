---
title: Configurar notificações de spam do usuário final no Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
ms.collection:
- M365-security-compliance
description: Você pode configurar as notificações de spam para o usuário final para a política de filtro de spam padrão para toda a empresa ou para políticas de filtro de spam personalizadas que são aplicadas a domínios.
ms.openlocfilehash: e3e5ce044879318dab55f5d08ec2ee0e3379dfb2
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341362"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Configurar notificações de spam do usuário final no Exchange Online

> [!IMPORTANT]
> Este tópico é para os clientes do Exchange Online que estão protegendo caixas de correio hospedadas na nuvem. Os clientes autônomos do Exchange Online Protection (EOP) que estão protegendo caixas de correio locais devem ler o seguinte tópico em vez disso: [configurar notificações de spam para o usuário final no EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Você pode configurar as notificações de spam para o usuário final para a política de filtro de spam padrão para toda a empresa ou para políticas de filtro de spam personalizadas que são aplicadas a domínios. Habilitar mensagens de notificação de spam do usuário final permite que os usuários finais gerenciem automaticamente suas próprias mensagens de spam em quarentena. As notificações de spam do usuário final não podem ser usadas com políticas aplicadas a usuários ou grupos, ou a uma política com exceções.
  
As notificações de spam do usuário final contém uma lista de todas as mensagens de spam em quarentena que o usuário final recebeu durante um período de tempo que você configurou (você pode especificar um valor entre 1 e 15 dias). Você também pode configurar o idioma no qual a mensagem de notificação será escrita.
  
Após receber uma mensagem de notificação, os usuários finais podem escolher entre as seguintes opções:

**Visualize** a mensagem se quiser visualizar o conteúdo ou o cabeçalho antes de executar a ação.

**Baixe** a mensagem se quiser revisar a mensagem e os anexos (se houver) no dispositivo antes de executar a ação.

**Versão** se a mensagem não for spam e se você quiser que o Office 365 envie a mensagem para sua caixa de correio.

**Release _AMP_ Allow Sender** se a mensagem não for spam e se você quiser que o Office 365 adicione o remetente à sua lista de remetentes e destinatários confiáveis para futuros emails. Tenha em mente que seu administrador pode ter outras configurações de permissão/bloqueio de toda a organização que substituem sua lista de remetentes seguros.

**Release _AMP_ Report**, se a mensagem não for spam e você deseja enviar a mensagem para sua caixa de correio e relatá-la para a Microsoft para análise.

**Bloquear** se você quiser que o Office 365 adicione o remetente à sua lista de remetentes bloqueados.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

Tempo estimado para conclusão: 2 minutos
  
Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o entrada "anti-spam" no tópico [permissões de recursos no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Use o EAC para configurar as notificações de spam do usuário final

1. No Centro de Administração do Exchange (EAC), navegue até **Proteção** \> **Filtro de conteúdo**.
    
2. Selecione a política de filtro de spam para a qual você deseja habilitar as notificações de spam do usuário final (elas estão desabilitadas por padrão).
    
3. No painel direito, onde as informações resumidas sobre política aparecem, clique no link **Configurar notificações de spam para o usuário final**. 
    
4. Na caixa de diálogo posterior, você pode configurar as seguintes opções:
    
1. **Habilitar notificações de spam para o usuário final** Marque esta caixa de seleção para habilitar notificações de spam para o usuário final para esta política. (De outra forma, se esta política estiver habilitada, você pode desmarcar esta caixa de seleção para desabilitar as notificações de spam para usuário final para esta política.) 
    
2. **Envie notificações de spam para o usuário final a cada (dias)** Especifique a frequência com a qual as notificações de spam para o usuário final são enviadas. O padrão é 3 dias. Você pode especificar entre 1 e 15 dias. Se você especificar 7 dias, por exemplo, a notificação incluirá uma lista de todas as mensagens para aquele usuários dos últimos 7 dias que foram enviadas para a quarentena de spam. 
    
3. **Idioma da notificação** Usando a lista suspensa, escolha o idioma de escrita das notificações de spam para o usuário final para esta diretiva. 
    
5. Clique em **salvar**. Um resumo das configurações de política de filtro de spam, incluindo as configurações de notificação de spam do usuário final, aparece no painel direito.
    
> [!NOTE]
>  As notificações de spam do usuário final só serão funcionais para políticas de filtro de spam habilitadas. > as notificações de spam do usuário final são enviadas apenas uma vez por dia. O tempo de entrega da notificação não pode ser garantido para qualquer cliente específico e não é configurável. 
  
 **Dica:** Se você quiser testar as notificações de spam do usuário final enviando-as a um conjunto limitado de usuários antes de implementá-las totalmente, crie uma política de filtro de spam personalizada que permite as notificações de spam do usuário final para os domínios nos quais os usuários residem. Em seguida, no Eat, em **regras de \> fluxo**de emails, crie uma regra de fluxo de emails (também conhecida como regra de transporte) para bloquear mensagens do Quarantine@messaging.microsoft.com (o endereço de email que envia notificações) com exceções para os usuários que você deseja para receber notificações. A imagem a seguir é um exemplo de criação de uma exceção para dois usuários (em Sara e Alex) do domínio Contoso.com: 
  
![Regra de transporte para testar notificações de spam do usuário final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Para obter mais informações

[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
