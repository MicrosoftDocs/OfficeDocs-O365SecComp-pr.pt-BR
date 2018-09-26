---
title: Localizar e liberar mensagens em quarentena como um usuário no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
description: 'Como um usuário do Office 365, você pode gerenciar suas próprias mensagens em quarentena de spam em uma das duas maneiras: respondendo a spams notificações enviadas diretamente à você (se seu administrador tiver configurado a esse recurso,) ou usando o recurso de quarentena de spam na segurança &amp; conformidade Centro.'
ms.openlocfilehash: 728273838d9e592e17638638258f481830bc0bbe
ms.sourcegitcommit: f7fff49ae0b1c3056faa58d73c1070cb4e638fbf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018885"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Localizar e liberar mensagens em quarentena como um usuário no Office 365

Como um usuário do Office 365, você pode gerenciar mensagens que foram enviadas para quarentena em vez de enviada para você em uma das duas maneiras: por [Responder para notificações de spam enviado a você diretamente](use-spam-notifications-to-release-and-report-quarantined-messages.md) (se o seu administrador tiver configurado isso) ou usando a segurança &amp; Centro de conformidade. 
  
> [!NOTE]
> Se você for um administrador, você pode [Gerenciar mensagens em quarentena](manage-quarantined-messages-and-files.md) para outras pessoas em sua organização. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Exibir as mensagens que foram enviadas para quarentena em vez de para você

1. Entrar no Office 365 e [vá para o Centro de conformidade de segurança e](go-to-the-securitycompliance-center.md) usando sua conta do trabalho ou da escola. 
    
2. À esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **quarentena**.
    
    > [!TIP]
    > Para ir diretamente para a página de **quarentena** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Por padrão, a segurança &amp; Centro de conformidade exibe todas as mensagens de email que tenham sido colocados em quarentena como spam. As mensagens são classificadas do mais recente para o mais antigo com base na **Data** em que a mensagem foi recebida. **Remetente**, **assunto**e a data de validade (sob **expira** ) também são exibidas para cada mensagem. Você pode classificar em um campo clicando no cabeçalho da coluna correspondente; Clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação. 
  
Você pode exibir uma lista de todas as mensagens em quarentena, ou você pode pesquisar mensagens específicas filtrando. Você só pode fazer em massa operações em até 100 itens, portanto filtragem também pode ajudar a reduzir seu resultado definido se você tiver mais do que isso. Você pode filtrar mensagens rapidamente por uma razão de quarentena único, escolhendo uma opção na lista suspensa. As opções incluem:
  
- Email identificado como spam. Essas mensagens em quarentena são mostradas por padrão.
    
- Email identificado como email em massa.
    
Após localizar uma determinada mensagem em quarentena, clique na mensagem para exibir detalhes sobre ela e realizar ações. Você pode liberar a mensagem para sua caixa de correio, visualiza a mensagem, o download da mensagem ou excluir a mensagem da quarentena imediatamente.
  
> [!NOTE]
> Você deve ter permissões de administrador no Office 365 para trabalhar com mensagens em quarentena que foram enviadas para outros usuários. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Para filtrar e localizar mensagens em quarentena

Se você tiver muitos itens em quarentena, você pode reduzir o número para um conjunto gerenciável, filtrando-los.
  
1. Na página de **quarentena** , escolha se você deseja exibir **spam** ou **em massa** de mensagens em quarentena. 
    
2. Em **resultados de classificar por**, escolha qualquer combinação das condições, definindo o filtro apropriado ou filtros (é possível usar curingas no momento). Há várias condições, que você pode escolher, incluindo o seguinte:
    
  - **ID da mensagem** Use esta opção para selecionar uma mensagem específica quando você souber a ID de mensagem. 
    
    Por exemplo, se uma mensagem específica é enviada pelo ou destinada a um usuário em sua organização, mas nunca atingiu seu destino, você pode pesquisar a mensagem usando um rastreamento da mensagem (consulte [executar um rastreamento da mensagem e exibir resultados](https://go.microsoft.com/fwlink/?LinkId=799737)). Se você descobrir que a mensagem foi enviada para quarentena, talvez porque ele corresponde a uma regra de fluxo de email ou foi identificado como spam, você pode facilmente Localize essa mensagem em quarentena especificando-se a sua ID de mensagem. Certifique-se de incluir a cadeia de caracteres de ID da mensagem completa. Isso pode incluir colchetes angulares (\<\>), por exemplo:
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Endereço de email do remetente** Escolha esta opção para filtrar por um endereço de email do remetente único. 
    
  - **Endereço de email do destinatário** Escolha esta opção para filtrar por um endereço de email do destinatário único. 
    
  - **Assunto** Insira o assunto de um endereço de email que você deseja localizar. 
    
  - **Intervalo de datas** Você pode optar por filtrar pela data em que a mensagem foi enviada para quarentena. Você pode especificar a data ou um intervalo de datas, incluindo o tempo. 
    
  - **Data de validade** Para filtrar por data de expiração, escolha **filtro avançado**. Você pode selecionar mensagens que serão excluídas da quarentena dentro das próximas 24 horas ( **hoje**) dentro das próximas 48 horas ( **próximo 2 dias**), na próxima semana ( **próximo 7 dias**), ou você pode selecionar um intervalo de tempo personalizada.
    
    > [!IMPORTANT]
    > Por padrão, as mensagens de spam e em massa são mantidas em quarentena por 30 dias. Entretanto, esse período é configurável e seu administrador pode ter definido um período de retenção da quarentena diferentes. Quando o Office 365 exclui uma mensagem de quarentena, não é possível recuperá-lo. 
  
## <a name="view-details-for-a-specific-message"></a>Exibir detalhes de uma mensagem específica

Depois de selecionar uma mensagem, você verá um resumo das propriedades de mensagem em um painel no lado direito da página.
  
- **ID da mensagem:** O identificador exclusivo para a mensagem. 
    
- **Endereço do remetente:** Que enviou a mensagem. 
    
- **Recebido:** A data em que a mensagem foi recebida. 
    
- **Assunto:** O texto da linha de assunto da mensagem. 
    
- **Motivo de quarentena:** Mostra se uma mensagem foi identificada como **Spam** ou **em massa**.
    
- **Expira:** A data quando a mensagem será excluída da quarentena. 
    
- **Lançados até:** Todos os endereços de email (se houver) para o qual a mensagem foi liberada. 
    
- **Ainda não foi liberada em:** Todos os endereços de email (se houver) para o qual a mensagem não foi liberada. Você pode escolher **versão** se você deseja liberar a mensagem para sua caixa de correio (mais informações sobre a liberação de mensagens na próxima seção). 
    
Você pode obter ainda mais detalhes sobre a mensagem, escolhendo uma das seguintes opções:
  
- **Cabeçalho da mensagem de modo de exibição** Escolha esta opção para ver o texto do cabeçalho da mensagem. Para analisar o cabeçalho em profundidade, copie o texto do cabeçalho da mensagem para sua área de transferência e escolha o **Analisador de cabeçalho de mensagem do Microsoft** para ir até a Remote Connectivity Analyzer (com o botão direito e escolha Abrir em uma nova guia se você não deseja deixar o Office 365 Execute essa tarefa). Cole o cabeçalho da mensagem para a página na seção analisador de cabeçalho de mensagem e escolha analisar cabeçalhos. 
    
- **Visualizar a mensagem** Permite que você consulte bruto ou versões HTML do texto do corpo da mensagem. Na exibição de HTML, links estão desabilitadas. 
    
## <a name="manage-your-quarantined-messages"></a>Gerenciar suas mensagens em quarentena

Depois de selecionar uma mensagem ou um grupo de mensagens, você tem várias opções para gerenciar mensagens em quarentena.
  
- Nada a fazer. Se você optar por fazer nada, a mensagem será excluída pelo Office 365 automaticamente após o vencimento. Lembre-se de que quando o Office 365 exclui uma mensagem da quarentena, você não é possível recuperá-lo.
    
- **Liberar a mensagem** Libere uma mensagem em quarentena (ou conjunto de mensagens) para que a mensagem é enviada para sua caixa de correio. Quando você solta uma mensagem, você tem a opção para relatar a mensagem à Microsoft para análise. 
    
    Quando você opta por relatar uma mensagem, também chamada de relatar uma mensagem como um falso positivo, a mensagem é relatada à equipe de análise de Spam da Microsoft. A equipe avalia e analisa as mensagens de falsos positivas e, dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir que essas mensagens por meio.
    
- **Baixar mensagem** Permite que você baixe a mensagem como um arquivo. eml. Depois de fazer o download de uma mensagem, você pode analisar o arquivo. eml usando seu cliente de email antes de liberar a mensagem. 
    
- **Remover da quarentena** Exclui a mensagem imediatamente da quarentena sem liberar a mensagem para sua caixa de correio. 
    

