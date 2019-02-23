---
title: Localizar e liberar mensagens em quarentena como um usuário no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
description: 'Como um usuário do Office 365, você pode gerenciar suas próprias mensagens de spam em quarentena de duas maneiras: respondendo a notificações de spam enviadas diretamente para você (se o seu administrador tiver configurado esse recurso) ou usando o recurso de quarentena de spam na conformidade com segurança &amp; Centro.'
ms.openlocfilehash: acbf862f05a9282a26444b738400d29c03d07f1f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214991"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Localizar e liberar mensagens em quarentena como um usuário no Office 365

Como um usuário do Office 365, você pode gerenciar as mensagens enviadas para a quarentena em vez de enviá-las de uma das duas maneiras: [respondendo a notificações de spam enviadas diretamente](use-spam-notifications-to-release-and-report-quarantined-messages.md) (se o seu administrador configurou isso) ou usando o centro de conformidade &amp; de segurança. 
  
> [!NOTE]
> Se você é um administrador, você pode [gerenciar as mensagens em quarentena](manage-quarantined-messages-and-files.md) para outras pessoas da sua organização. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Exibir mensagens que foram enviadas para a quarentena em vez de você

1. Entre no Office 365 e [vá para o centro de segurança e conformidade](go-to-the-securitycompliance-center.md) usando sua conta corporativa ou de estudante. 
    
2. À esquerda, expanda **Gerenciamento de ameaças**, escolha **revisão**e, em seguida, escolha **quarentena**.
    
    > [!TIP]
    > Para ir diretamente para a página **quarentena** no centro de conformidade &amp; de segurança, use esta URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Por padrão, o centro &amp; de conformidade de segurança exibe todas as mensagens de email em quarentena como spam. As mensagens são classificadas da mais nova para a mais antiga com base na **Data** em que a mensagem foi recebida. O **remetente**, o **assunto**e a data de expiração (em **vencimento** ) também são exibidos para cada mensagem. Você pode classificar em um campo clicando no cabeçalho da coluna correspondente; clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação. 
  
Você pode exibir uma lista de todas as mensagens em quarentena ou pode procurar mensagens específicas por filtragem. Você só pode realizar operações em massa em até 100 itens, então a filtragem também pode ajudar a reduzir o conjunto de resultados se você tiver mais do que isso. Você pode filtrar mensagens rapidamente por um único motivo de quarentena escolhendo uma opção na lista suspensa. As opções incluem:
  
- Email identificado como spam. Essas mensagens em quarentena são mostradas por padrão.
    
- Email identificado como email em massa.
    
Após localizar uma mensagem em quarentena específica, clique na mensagem para exibir detalhes sobre ela e realizar ações. Você pode liberar a mensagem para sua caixa de correio, Visualizar a mensagem, baixar a mensagem ou excluir a mensagem da quarentena imediatamente.
  
> [!NOTE]
> Você deve ter permissões de administrador no Office 365 para trabalhar com mensagens em quarentena que foram enviadas a outros usuários. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Para filtrar e localizar mensagens em quarentena

Se você tiver muitos itens em quarentena, poderá reduzir o número para um conjunto gerenciável filtrando-os.
  
1. Na página **quarentena** , escolha se você deseja exibir **spam** ou mensagens em quarentena **em massa** . 
    
2. Em **classificar resultados por**, escolha qualquer combinação de condições Configurando o filtro ou filtros apropriados (você não pode usar curingas neste momento). Há várias condições que você pode escolher, incluindo as seguintes:
    
  - **ID da mensagem** Use essa ação para selecionar uma mensagem específica quando você souber a ID da mensagem. 
    
    Por exemplo, se uma mensagem específica é enviada por ou destinada a um usuário em sua organização, mas nunca atingiu seu destino, você pode pesquisar a mensagem usando um rastreamento de mensagem (consulte [executar um rastreamento de mensagem e exibir resultados](https://go.microsoft.com/fwlink/?LinkId=799737)). Se você descobrir que a mensagem foi enviada para a quarentena, talvez porque correspondeu a uma regra de fluxo de emails ou tenha sido identificada como spam, você pode facilmente localizar essa mensagem em quarentena, especificando sua ID de mensagem. Certifique-se de incluir a cadeia de ID de mensagem completa. Isso pode incluir colchetes angulares\<\>(), por exemplo:
    
    \<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Endereço de email do remetente** Escolha filtrar por um único endereço de email do remetente. 
    
  - **Endereço de email do destinatário** Escolha filtrar por um único endereço de email de destinatário. 
    
  - **Assunto** Insira o assunto de um endereço de email que você deseja localizar. 
    
  - **Intervalo de datas** Você pode optar por filtrar pela data em que a mensagem foi enviada para quarentena. Você pode especificar a data ou um intervalo de datas, incluindo a hora. 
    
  - **Data de vencimento** Para filtrar por data de expiração, escolha **filtro avançado**. Você pode selecionar mensagens que serão excluídas da quarentena nas próximas 24 horas ( **hoje**), nas próximas 48 horas ( **próximos 2 dias**), na próxima semana ( **próximos 7 dias**) ou você pode selecionar um intervalo de tempo personalizado.
    
    > [!IMPORTANT]
    > Por padrão, as mensagens de spam e em massa são mantidas em quarentena por 30 dias. No enTanto, esse período de tempo é configurável e seu administrador pode ter definido um período diferente de retenção de quarentena. Quando o Office 365 exclui uma mensagem da quarentena, não é possível obtê-la novamente. 
  
## <a name="view-details-for-a-specific-message"></a>Exibir detalhes de uma mensagem específica

Depois de selecionar uma mensagem, você verá um resumo das propriedades da mensagem em um painel no lado direito da página.
  
- **ID da mensagem:** O identificador exclusivo da mensagem. 
    
- **Endereço do remetente:** Quem enviou a mensagem. 
    
- **Recebidos:** A data em que a mensagem foi recebida. 
    
- **Assunto:** O texto da linha de assunto da mensagem. 
    
- **Motivo da quarentena:** Mostra se uma mensagem foi identificada como **spam** ou **em massa**.
    
- **Expira:** A data em que a mensagem será excluída da quarentena. 
    
- **Liberado para:** Todos os endereços de email (se houver) para os quais a mensagem foi liberada. 
    
- **Ainda não liberado para:** Todos os endereços de email (se houver) aos quais a mensagem não foi liberada. Você pode escolher **liberar** se quiser liberar a mensagem para sua caixa de correio (Saiba mais sobre como liberar mensagens na próxima seção). 
    
Você pode obter ainda mais detalhes sobre a mensagem escolhendo uma das seguintes opções:
  
- **Exibir cabeçalho da mensagem** Escolha esta botão para ver o texto do cabeçalho da mensagem. Para analisar o cabeçalho em camadas, copie o texto do cabeçalho da mensagem para a área de transferência e escolha analisador de **cabeçalho de mensagem da Microsoft** para ir para o analisador de conectividade remota (clique com o botão direito do mouse e escolha abrir em uma nova guia se não quiser deixar o Office 365 para concluir esta tarefa). Cole o cabeçalho da mensagem na página na seção analisador de cabeçalho de mensagem e escolha analisar cabeçalhos. 
    
- **Visualizar mensagem** Permite que você veja versões brutas ou de HTML do texto do corpo da mensagem. No modo de exibição HTML, os links estão desabilitados. 
    
## <a name="manage-your-quarantined-messages"></a>Gerenciar as mensagens em quarentena

Após selecionar uma mensagem ou grupo de mensagens, você tem várias opções para gerenciar mensagens em quarentena.
  
- Não faça nada. Se você optar por não fazer nada, a mensagem será excluída pelo Office 365 automaticamente após a expiração. Lembre-se de que, quando o Office 365 exclui uma mensagem da quarentena, não é possível obtê-la novamente.
    
- **Mensagem de liberação** Liberar uma mensagem em quarentena (ou conjunto de mensagens) para que a mensagem seja enviada à sua caixa de correio. Ao liberar uma mensagem, você tem a opção de relatar a mensagem para a Microsoft para análise. 
    
    Quando você opta por relatar uma mensagem, também chamada de relatar uma mensagem como um falso positivo, a mensagem é relatada para a equipe de análise de spam da Microsoft. A equipe avalia e analisa mensagens falsas positivas e, dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir essas mensagens.
    
- **Mensagem de download** Permite baixar a mensagem como um arquivo. eml. Depois de baixar uma mensagem, você pode revisar o arquivo. eml usando seu cliente de email antes de liberar a mensagem. 
    
- **Remover da quarentena** Exclui a mensagem imediatamente da quarentena sem liberar a mensagem para sua caixa de correio. 
    

