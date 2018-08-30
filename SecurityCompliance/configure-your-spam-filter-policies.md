---
title: Configurar suas políticas de filtro de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
description: Configurações de filtro de spam básico incluem selecionando a ação a ser executada em mensagens que são identificadas como spam e escolha se deseja filtrar as mensagens enviadas de determinados países ou regiões ou escritas em idiomas específicos.
ms.openlocfilehash: 3e24a69dacc18272baa710c18492759f67583f4f
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002960"
---
# <a name="configure-your-spam-filter-policies"></a>Configurar suas políticas de filtro de spam
  
Configurações de filtro de spam básico incluem selecionando a ação a ser executada em mensagens que são identificadas como spam e escolha se deseja filtrar as mensagens enviadas de determinados países ou regiões ou escritas em idiomas específicos. Configurações de política de filtro de spam são apenas mensagens aplicadas a entrada. Você pode editar a política de filtro de spam padrão para definir suas configurações de filtro de spam de toda a empresa e criar políticas de filtro de spam personalizado e, em seguida, aplicá-las a usuários específicos, grupos ou domínios em sua organização. Políticas personalizadas sempre têm precedência sobre a diretiva padrão. Você pode alterar a ordem na qual suas diretivas personalizadas são executados, alterando a prioridade de cada política personalizada.
  
> [!IMPORTANT]
> Para clientes do Exchange Online Protection (EOP) autônomo: por padrão, os filtros de spam EOP enviam mensagens de spam detectado para pasta de lixo eletrônico de cada destinatário. No entanto, para garantir que a ação de **mover a mensagem para a pasta Lixo eletrônico** funciona para caixas de correio local, você deve configurar regras de transporte do Exchange em seus servidores locais para detectar os cabeçalhos de spam que são adicionados pelo EOP. Para obter detalhes, consulte [Certifique-se de que o spam é roteado para a pasta de lixo eletrônico de cada usuário](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
## <a name="what-you-must-know-before-you-begin"></a>Você deve saber antes de começar

Tempo estimado para conclusão: 30 minutos
  
Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada de antispam no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-exchange-admin-center-eac-to-configure-spam-filter-policies"></a>Usar o Centro de administração do Exchange (EAC) para configurar as políticas de filtro de spam

1. No Centro de Administração do Exchange (EAC), navegue até **Proteção** \> **Filtro de conteúdo**.
    
2. Faça uma das duas coisas a seguir na página **geral**: 
    
  - Clique duas vezes na política padrão de forma a editá-la para toda a empresa.
    
  - Clique no ícone ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Novo** para criar uma nova política de filtro de spam personalizada que pode ser aplicada a usuários, grupos e domínios em sua organização. Também é possível editar políticas personalizadas existentes clicando nelas duas vezes. 
    
3. Para apenas diretivas personalizadas, especifique um nome para esta diretiva. Opcionalmente, você também pode especificar uma descrição mais detalhada. Não é possível renomear a política padrão.
    
    > [!NOTE]
    > Quando você cria uma política, todas as definições de configuração aparecem em uma única tela. Por outro lado, quando você edita uma diretiva, você deve navegar pelas várias telas. As configurações são os mesmos em ambos os casos, mas o restante deste procedimento descreve como acessar essas configurações quando você edita uma diretiva. 
  
4. Na página **ações de email em massa e spam**, em **Spam** e **Spam de alta confiabilidade**, selecione a ação a ser realizada para spam e emails em massa recebidos. Via de regra, **Mover mensagens para a pasta Lixo eletrônico** está selecionado. Os outros valores possíveis são: 
    
  - **Excluir mensagem** Exclui a mensagem inteira, incluindo todos os anexos. 
    
  - **Mensagem em quarentena** Envia a mensagem para a quarentena em vez de para os destinatários pretendidos. Se você selecionar essa opção, na caixa de entrada **Manter spam por (dias)**, especifique a quantidade de dias durante os quais a mensagem de spam ficará em quarentena. (Ela será automaticamente excluída após o tempo decorrido. O valor padrão é de 15 dias, que é o valor máximo. O valor mínimo é 1 dia). 
    
    > [!TIP]
    >  Para obter informações sobre como os administradores podem gerenciar mensagens de email residem na quarentena no EAC, consulte [quarentena](quarantine.md) e [Localizar e liberar mensagens em quarentena como um administrador](find-and-release-quarantined-messages-as-an-administrator.md). > Para obter informações sobre como configurar mensagens de notificação de spam sejam enviadas aos usuários, consulte [Configure End-User spam notificações no EOP](configure-end-user-spam-notifications-in-eop.md) ou [Configure End-User spam notificações no Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
  - **Mover mensagem para a pasta Lixo Eletrônico** Envia a mensagem para a pasta Lixo Eletrônico dos destinatários especificados. Essa é a ação padrão para ambos os níveis de limite de confiança. 
    
    > [!IMPORTANT]
    > Somente para clientes do Exchange Online Protection (EOP): Para essa ação funcionar com as caixas de correio locais, é necessário configurar duas regras de Transporte do Exchange nos seus servidores locais para detectar cabeçalhos de spam adicionados pelo EOP. Para obter detalhes, consulte [Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
  - **Adicionar cabeçalho X** Envia a mensagem para os destinatários especificados, mas adiciona texto de cabeçalho X ao cabeçalho da mensagem para identificar a mensagem como spam. Usando esse texto como identificador, opcionalmente você pode criar regras de caixa de entrada ou usar um dispositivo de downstream para agir na mensagem. O texto de cabeçalho X padrão é **essa mensagem é exibida como spam**.
    
    Você pode personalizar o texto de cabeçalho X usando a caixa de entrada **Adicionar este texto de cabeçalho X** . Se você personalizar o texto de cabeçalho X, esteja ciente das seguintes condições: 
    
  - Se você especificar somente o cabeçalho no formato \< *cabeçalho*\>, onde há sem espaços dentro do \< *cabeçalho*\>, dois-pontos serão acrescentados ao texto personalizado, seguido do texto padrão. Por exemplo, se você especificar "Esta é-meu-custom-cabeçalho", o texto de cabeçalho X aparecerá como "Esta é-meu-custom-cabeçalho: essa mensagem é exibida como spam."       
    
  - Se você incluir espaços dentro do texto de cabeçalho personalizado, ou se você adicionar os dois-pontos sozinho (tal como "X este é o meu cabeçalho personalizado" ou "X-This-is-my-custom-header:"), o texto de cabeçalho X reverte para o padrão como "X deste-for-Spam: essa mensagem é exibida como spam."
    
  - Você não pode especificar o texto do cabeçalho no formato \< *cabeçalho*  \>:\<  *valor*  \>. Se fizer isso, os dois valores antes e depois dos dois-pontos serão ignorado e o texto de cabeçalho X padrão é exibida: "X deste-for-Spam: essa mensagem é exibida como spam." 
    
  - **Linha de assunto prepend com texto** Envia a mensagem para os destinatários pretendidos mas precede a linha de assunto com o texto que você especificar na caixa de entrada **a linha de assunto com este texto de prefixo** . Usando esse texto como identificador, opcionalmente, você pode criar regras para filtrar ou encaminhar mensagens conforme necessário. 
    
  - **Redirecionar a mensagem para o endereço de email** Envia a mensagem para um endereço de email designados em vez de para os destinatários pretendidos. Especifique o endereço de "redirecionar" na caixa de entrada **Redirecionar para este endereço de email** . 
    
    > [!NOTE]
    > Para obter mais informações sobre níveis de confiança de spam, consulte [Níveis de confiança de spam](spam-confidence-levels.md). 
  
5. Em **emails em massa**, você pode selecionar um limite para tratar de email em massa como spam. Esse limite é baseado no nível compatível com em massa da mensagem. Você pode escolher uma configuração de limite de 1 a 9, onde 1 indica que a maioria dos emails em massa como spam e 9 permite que a maioria dos emails em massa ao ser entregue. O serviço, em seguida, executa a ação configurada, por exemplo, enviar a mensagem para a pasta de lixo eletrônico do destinatário. Consulte [os valores em massa compatível com nível](bulk-complaint-level-values.md) e [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) para obter mais detalhes. 
    
6. Na página **Listas de Bloqueios**, você pode especificar as entradas, como remetentes ou domínios, que sempre serão marcadas como spam. O serviço aplicará a ação de spam de alta confiança configurada nos emails que corresponderem a essas entradas. 
    
  - Adicione remetentes indesejados à lista de Bloqueios de Remetentes. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os endereços dos remetentes que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
  - Adicione domínios indesejados à lista de Bloqueio de domínios. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os domínios que deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **Ok** para retornar à página **Listas de Bloqueios**. 
    
    > [!CAUTION]
    > Se você bloquear domínios de primeiro nível, é provável que emails não bloqueados sejam marcados como spam. 
  
7. Na página **Listas de Permissões**, você pode especificar as entradas, como remetentes ou domínios, que sempre serão entregues à caixa de entrada. Os emails dessas entradas não são processados pelo filtro de spam. 
    
  - Adicione remetentes confiáveis à Lista de permissões de remetentes. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os endereços dos remetentes que deseja permitir. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em OK para retornar à página **Listas de Permissões**. 
    
  - Adicione domínios confiáveis à Lista de permissões de domínios. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, na caixa de diálogo de seleção, adicione os domínios que deseja permitir. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em OK para retornar à página **Listas de Permissões**. 
    
    > [!CAUTION]
    > Se você permitir domínios de nível superior, é provável que emails não desejados sejam entregues na caixa de entrada. 
  
8. Na página de **Spam internacional** , você pode filtrar as mensagens de email enviadas de determinados países ou regiões ou escritas em idiomas específicos. Você pode configurar até 250 diferentes regiões e de 86 idiomas diferentes. O serviço se aplicarão a ação configurada de spam de alta confiabilidade. 
    
1. Marque a caixa de seleção **filtrar mensagens de email gravadas nos seguintes idiomas** para habilitar essa funcionalidade. Clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e, na caixa de diálogo de seleção, faça suas escolhas (há suporte para várias seleções). Por exemplo, se você selecionar para filtrar mensagens escritas em árabe (AR), e a **mensagem em quarentena** é sua ação configurada para mensagens de spam de alta confiabilidade, todas as mensagens escritas em árabe serão ser colocada em quarentena. Clique em **okey** para retornar ao painel de **Spam internacional** . 
    
2. Marque a caixa de seleção **filtrar mensagens de email enviadas dos seguintes países ou regiões** para habilitar essa funcionalidade. Clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e, na caixa de diálogo de seleção, faça suas escolhas (há suporte para várias seleções). Por exemplo, se você selecionar para filtrar todas as mensagens que são enviadas a partir da Austrália (AU), e a **mensagem em quarentena** é sua ação configurada para mensagens de spam de alta confiabilidade e, em seguida, todas as mensagens enviadas a partir da Austrália serão ser colocada em quarentena. Clique em **okey** para retornar ao painel de **Spam internacional** . 
    
    > [!NOTE]
    > Por padrão, se não houver qualquer opção de spam internacional selecionada, o serviço filtrará normalmente o spam em mensagens enviadas, em todos os idiomas e de todas as regiões. As mensagens são analisadas e, se definidas como spam ou spam de alta confiança, as ações configuradas são aplicadas. 
  
9. Na página **Opções avançadas** , **em**, **desativado**ou **teste** podem ser selecionados para cada opção de filtragem de spam avançada. 
    
1. **Em** Mensagens ativamente são filtradas de acordo com a regra que está associada essa opção. As mensagens são marcadas como spam ou serão suas pontuações de spam aumentaram, dependendo das opções que você ativar. 
    
2. **Desativado** Nenhuma ação é tomada em mensagens que atendem aos critérios do filtro de spam. Todas as opções estão desativadas por padrão. 
    
3. **Teste** Nenhuma ação é executada em mensagens que atendam aos critérios de filtro de spam. No entanto, as mensagens podem ser identificadas com a adição de um cabeçalho X antes que sejam entregues ao destinatário pretendido. Este cabeçalho X permite saber qual opção ASF correspondida. Se você especificou o **teste** para qualquer uma dessas opções avançadas, você pode configurar as seguintes configurações de modo de teste a serem aplicadas quando uma correspondência é feita de uma opção de teste-habilitado: 
    
  - **Nenhuma** Não tomar ação de modo de teste na mensagem. Esse é o padrão. 
    
  - **Adicionar o padrão de texto de cabeçalho X de teste** Esta opção envia a mensagem para os destinatários especificados, mas também adiciona um cabeçalho X especial à mensagem para identificá-lo como tendo correspondente a um opção de filtragem de spam avançada específico. 
    
  - **Enviar uma mensagem Cco para este endereço** Esta opção envia uma cópia carbono oculta da mensagem para o endereço de email que você especificar na caixa de entrada. 
    
    > [!TIP]
    > Para obter mais informações sobre a opções, incluindo descrições sobre cada opção e o texto de cabeçalho X associado a cada um, de filtragem de spam avançadas, consulte [Opções de filtragem de spam avançada](advanced-spam-filtering-asf-options.md). 
  
10. Para políticas personalizadas apenas, clique no item de menu de **Aplicar a** e, em seguida, crie uma regra de condição para especificar os usuários, grupos e domínios ao qual será aplicada a esta política. Você pode criar várias condições, se eles são exclusivos. 
    
  - Para selecionar usuários, selecione **o destinatário é**. Na caixa de diálogo posterior, selecione um ou mais remetentes da sua empresa da lista do seletor de usuário e, em seguida, clique em **Adicionar**. Para adicionar remetentes que não estão na lista, digite seus endereços de email e, em seguida, clique em **Verificar nomes**. Nessa caixa, você também pode usar caracteres curinga para vários endereços de email (por exemplo: \* @  _domainname_). Quando você terminar faz suas seleções, clique em **okey** para retornar à tela principal. 
    
  - Para selecionar grupos, selecione **o destinatário é um membro de**. Em seguida, na caixa de diálogo posterior, selecione ou especificar os grupos. Clique em **okey** para retornar à tela principal. 
    
  - Para selecionar os domínios, selecione **o domínio do destinatário é**. Em seguida, na caixa de diálogo posterior, adicione os domínios. Clique em **okey** para retornar à tela principal. 
    
    Você pode criar exceções dentro da regra. Por exemplo, você pode filtrar mensagens de todos os domínios, com exceção de um determinado domínio. Clique em **Adicionar exceção**e crie as condições de exceção semelhante à forma que você criou as outras condições.
    
    > [!TIP]
    > Aplicar uma política de spam para um grupo é suportado somente para **Grupos de segurança habilitado para email**. 
  
11. Clique em **salvar**. Um resumo das configurações de política aparecerá no painel direito.
    
> [!TIP]
>  Você pode marque ou desmarque as caixas de seleção na coluna **habilitado** para habilitar ou desabilitar suas diretivas personalizadas. Por padrão, todas as diretivas estão habilitadas. A política padrão não pode ser desabilitada. > Para excluir uma política personalizada, selecione a política, clique no ![ícone Excluir](media/ITPro-EAC-DeleteIcon.gif) ícone **Excluir** e confirme que você deseja excluir a diretiva. A política padrão não pode ser excluída. > Políticas personalizadas sempre têm precedência sobre a diretiva padrão. Políticas personalizadas são executados na ordem inversa em que você criou (do mais antigo para o mais recente), mas você pode alterar a prioridade (ordem de execução) das suas diretivas personalizadas clicando o ![ícone de seta para cima](media/ITPro-EAC-UpArrowIcon.gif) seta para cima e ![ícone de seta para baixo](media/ITPro-EAC-DownArrowIcon.gif) para baixo seta. A política que possui uma **prioridade** **0** será executado primeira, seguido de **1**, e em seguida, **2**e assim por diante. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Usar o PowerShell remoto para configurar políticas de filtro de spam

Você também pode configurar e aplicar políticas de filtro de spam no PowerShell. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
- [Get-HostedContentFilterPolicy](http://technet.microsoft.com/library/d510471a-dda5-4df7-b3f8-2ee7a1948436.aspx) Exibir suas configurações de filtro de spam. 
    
- [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) Editar suas configurações de filtro de spam. 
    
- [New-HostedContentFilterPolicy](http://technet.microsoft.com/library/4d15128d-9e16-42a1-8ac5-36f07d4bbbf0.aspx) Criar uma nova política personalizada de filtro de spam. 
    
- [Remove-HostedContentFilterPolicy](http://technet.microsoft.com/library/9fe1fe03-8f83-41e3-9bf5-084a392784d6.aspx) Excluir uma política personalizada de filtro de spam. 
    
Para aplicar uma política personalizada de filtro de spam a usuários, grupos e/ou domínios, use o cmdlet do [New-HostedContentFilterRule](http://technet.microsoft.com/library/2df13ba9-1eb0-4da3-bd72-a79d5fa15e26.aspx) (para criar uma nova regra de filtragem que possa ser aplicada a políticas personalizadas) ou o cmdlet [Set-HostedContentFilterRule](http://technet.microsoft.com/library/ba259260-ffd3-43f3-8ef4-9d8659679d02.aspx) (para editar uma regra de filtro existente que possa ser aplicada a políticas personalizadas). Para habilitar ou desabilitar a regra aplicada à política, use o cmdlet [Enable-HostedContentFilterRule](http://technet.microsoft.com/library/354ece28-dcde-4b5f-88ed-475115e7ea78.aspx) ou o cmdlet do [Disable-HostedContentFilterRule](http://technet.microsoft.com/library/c1f8dafc-ef5d-47e3-b0fb-71a88e145fc5.aspx). 
  
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para garantir que o spam esteja sendo adequadamente detectado e tratado, você pode enviar uma mensagem GTUBE por meio do serviço. Semelhante ao arquivo de teste de antivírus EICAR, o GTUBE oferece um teste pelo qual você pode verificar se o serviço está detectando spam de entrada. Uma mensagem GTUBE sempre deverá ser detectada como spam pelo filtro de spam, e as ações executadas na mensagem deverão corresponder às suas configurações.
  
Inclua o seguinte texto do GTUBE em uma mensagem de email em uma única linha, sem espaços ou quebras de linha:
  
```
XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
```

## <a name="fine-tuning-your-spam-filter-policy-to-prevent-false-positives-and-false-negatives"></a>Otimizar sua política de filtro de spam para evitar falsos positivos e falsos negativos

Você também pode habilitar as opções avançadas de filtragem de spam, caso queira adotar uma abordagem mais agressiva de filtragem de spam. Para configurações gerais de spam que se apliquem a toda a organização, consulte [Prevenir email falso positivo marcado como spam com uma lista segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkId=534224) ou [Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225). Elas serão úteis se você tiver o controle de nível de administrador e quiser impedir falsos positivos ou falsos negativos.
   
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection6"> </a>

[Configurar a política do filtro de conexão](configure-the-connection-filter-policy.md)
  
[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Quarentena](quarantine.md)
  
[Impedir email falso positivo marcado como spam com uma lista de segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

