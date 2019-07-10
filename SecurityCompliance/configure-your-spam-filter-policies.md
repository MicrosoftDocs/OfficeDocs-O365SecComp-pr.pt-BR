---
title: Configurar suas políticas de filtro de spam
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/05/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: As configurações básicas de filtro de spam incluem selecionar a ação a ser executada em mensagens identificadas como spam.
ms.openlocfilehash: a59311ae6bccb1bcb1e949eb825cafc1a740c5da
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600097"
---
# <a name="configure-your-spam-filter-policies"></a>Configurar suas políticas de filtro de spam
As configurações de filtro de spam incluem selecionar a ação a ser executada em mensagens identificadas como spam. As configurações de política de filtro de spam são aplicadas somente a mensagens de entrada e há dois tipos:

  - Padrão: a política padrão de filtro de spam é usada para definir configurações de filtro de spam para toda a empresa. Essa política não pode ser renomeada e está sempre ativada.

  - Personalizado: as políticas de filtro de spam personalizadas podem ser detalhadas e aplicadas a usuários, grupos ou domínios específicos em sua organização. Políticas personalizadas sempre têm precedência sobre a política padrão. Você pode alterar a ordem na qual suas políticas personalizadas são executadas, alterando a prioridade de cada política personalizada; no entanto, somente a política de maior prioridade (ou seja, número mais próximo a 0) será aplicada se várias políticas atenderem ao conjunto de critérios.

## <a name="what-you-must-know-before-you-begin"></a>O que você precisa saber antes de começar

Tempo estimado para conclusão: 30 minutos
  
Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o entrada anti-spam no tópico [permissões de recurso no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

As configurações de política de filtro de spam estão todas no centro de conformidade e segurança & (SCC). É possível encontrar mais informações em [vá para o centro de conformidade & segurança do Office 365](go-to-the-securitycompliance-center.md). A página configurações antispam está dentro da seção **anti-spam** da **política** \> de **Gerenciamento** \> de ameaças SCC \> .

## <a name="access-and-create-spam-filter-policies"></a>Acessar e criar políticas de filtro de spam

Dentro da página configurações antispam, as configurações padrão podem ser exibidas na guia padrão. Para alterar essas configurações, alterne para a guia **personalizado** . Você poderá ver e definir algumas das configurações padrão dentro da política de filtro de spam padrão.

Para habilitar mais configurações personalizadas ou adicionar políticas personalizadas, altere o seletor de **configurações personalizadas** para **ativado** para habilitar políticas personalizadas de filtro de spam. Você pode exibir as políticas personalizadas existentes expandindo-as daqui.

## <a name="configure-custom-spam-filter-policy-settings"></a>Definir configurações personalizadas de política de filtro de spam

1. Selecione e clique em **Editar política** se você estiver editando uma política; caso contrário, clique em **criar uma política**

2. Você pode especificar um nome exclusivo para políticas personalizadas, mas não pode renomear o padrão. Opcionalmente, você também pode especificar uma descrição mais detalhada para qualquer política.

3. Na seção **ações de spam e em massa** :

  - Selecione uma ação para spam ****, **spam de alta confiança**, **email de phishing**e tipos de **email em massa** . Os valores disponíveis são: 

    - **Mover mensagem para a pasta de lixo eletrônico:** Envia a mensagem para a pasta lixo eletrônico dos destinatários especificados. Esta é a ação padrão para spam, spam de alta confiança e massa.<br/><br/>

    > [!NOTE]
    > Para que essa ação funcione com caixas de correio locais, você deve configurar duas regras de fluxo de mensagens do Exchange (também conhecidas como regras de transporte) em seus servidores locais para detectar cabeçalhos de spam adicionados pelo EOP. Para obter detalhes, consulte como [garantir que o spam seja roteado para a pasta lixo eletrônico de cada usuário](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Esta etapa é crítica para clientes autônomos do Exchange Online Protection (EOP).

    - **Adicionar cabeçalho X:** Envia a mensagem para os destinatários especificados, mas adiciona o texto do cabeçalho X ao cabeçalho da mensagem para identificar a mensagem como spam. Usando esse texto como um identificador, você pode, opcionalmente, criar regras de caixa de entrada ou usar um dispositivo downstream para atuar na mensagem. O texto do cabeçalho X padrão é **Esta mensagem parece ser spam**.<br/>Você pode personalizar o texto do cabeçalho X usando a caixa de entrada **Adicionar este texto do cabeçalho x** . Se você personalizar o texto do cabeçalho X, esteja ciente das seguintes condições: 
    
      - Se você especificar apenas o cabeçalho no \< *cabeçalho*\>do formato, onde não há espaços no \< *cabeçalho*\>, dois-pontos serão acrescentados ao texto personalizado, seguido do texto padrão.       Por exemplo, se você especificar "This-Is-My-Custom-Header", o texto do cabeçalho X será exibido como "This-Is-My-Custom-header: esta mensagem parece ser spam." 
        
      - Se você incluir espaços dentro do texto do cabeçalho personalizado, ou se você adicionar os dois-pontos (como "X este é o meu cabeçalho personalizado" ou "X-This-Is-My-Custom-header:"), o texto do cabeçalho X será revertido para o padrão como "X-this-spam: esta mensagem parece ser spam."
    
      - Você não pode especificar o texto do cabeçalho no formato \< *cabeçalho*  \>:\<  *valor*  \>. Se você fizer isso, os dois valores antes e depois dos dois-pontos serão ignorados, e o texto padrão do cabeçalho X será exibido em seu lugar: "X-this-is-spam: esta mensagem parece ser spam." 
      
      - Lembre-se de que as mensagens com esse cabeçalho X podem ainda ser movidas para a pasta de lixo eletrônico da caixa de correio devido à configuração de lixo eletrônico. Você pode alterar isso desabilitando esse recurso com Set-MailboxJunkEmailConfiguration.

    - **Ceder a linha de assunto com o texto:** Envia a mensagem para os destinatários pretendidos, mas precede a linha de assunto com o texto especificado na **linha de assunto do prefixo com esta caixa de entrada de texto** . Usando esse texto como um identificador, você pode opcionalmente criar regras para filtrar ou rotear as mensagens, conforme necessário. 

    - **Redirecionar mensagem para endereço de email:** Envia a mensagem para um endereço de email designado em vez de para os destinatários pretendidos. Especifique o endereço "redirecionar" na caixa de entrada redirecionar **para este endereço de email** .

    - **Excluir mensagem:** Exclui a mensagem inteira, incluindo todos os anexos. 
        
    - **Mensagem de quarentena:** Envia a mensagem para quarentena em vez de para os destinatários pretendidos. Esta é a ação padrão para Phish. Se você selecionar essa opção, na caixa de entrada **Manter spam por (dias)**, especifique a quantidade de dias durante os quais a mensagem de spam ficará em quarentena. (Ela será automaticamente excluída após o tempo decorrido. O valor padrão é 30 dias, que é o valor máximo. O valor mínimo é 1 dia).<br/><br/>Dica: para obter informações sobre como os administradores podem gerenciar mensagens de email residentes na quarentena no Eat, confira [quarentena](quarantine.md) e [Localizar e liberar mensagens em quarentena como um administrador](find-and-release-quarantined-messages-as-an-administrator.md). > para obter informações sobre como configurar as mensagens de notificação de spam a serem enviadas aos usuários, consulte [Configure End-User spam Notifications no EOP](configure-end-user-spam-notifications-in-eop.md) ou [Configure End-User spam Notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 

  - Configurar **Selecione o limite** para determinar como você deseja tratar emails em massa como spam, com base no nível de reclamação de massa (BCL) da mensagem. Você pode escolher uma configuração de limite de 1 a 9, em que 1 indica a maioria dos emails em massa como spam, e 9 permite que a maioria dos emails em massa seja entregue. O serviço então executa a ação configurada; por exemplo, enviar a mensagem para a pasta Lixo Eletrônico do destinatário. Veja [valores de nível de reclamação em massa](bulk-complaint-level-values.md) e [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) para obter mais detalhes. 

4. Na página **Propriedades de spam** , você pode definir as opções de modo de teste para a política Configurando: 
    
      - **Nenhuma** Não tomar ação de modo de teste na mensagem. Esse é o padrão. 
        
      - **Adicionar o texto do cabeçalho X de teste padrão** Selecionar essa opção envia a mensagem para os destinatários especificados, mas também adiciona um cabeçalho X especial à mensagem para identificá-lo como tendo correspondência com uma opção específica de filtragem de spam avançada. 
        
      - **Enviar uma mensagem Cco para este endereço** Selecionar essa opção envia uma cópia carbono oculta da mensagem para o endereço de email especificado na caixa de entrada. <br/><br/>Para obter mais informações sobre as opções avançadas de filtragem de spam, incluindo descrições sobre cada opção e o texto do cabeçalho X associado a cada uma, consulte [Advanced spam Filtering Options](advanced-spam-filtering-asf-options.md).

5. Somente para políticas personalizadas, clique no item de menu **aplicar a** e crie uma regra baseada em condição para especificar os usuários, grupos e domínios aos quais aplicar essa política. Você pode criar várias condições, se elas forem exclusivas. 
    
      - Para selecionar usuários, selecione **O destinatário é**. Na caixa de diálogo subsequente, selecione um ou mais remetentes da sua empresa na lista seletor de usuário e clique em **Adicionar**. Para adicionar remetentes que não estão na lista, digite seus endereços de email e clique em **verificar nomes**. Nessa caixa, também é possível usar caracteres curinga para vários endereços de email (por exemplo: \*@ _domainname_). Quando terminar de fazer suas seleções, clique em **OK** para retornar à tela principal. 
        
      - Para selecionar grupos, selecione **o destinatário é um membro**. Em seguida, na caixa de diálogo subsequente, selecione ou especifique os grupos. Clique em **ok** para retornar à tela principal. 
        
      - Para selecionar domínios, selecione **o domínio do destinatário**. Em seguida, na caixa de diálogo subsequente, adicione os domínios. Clique em **ok** para retornar à tela principal. <br/><br/>Você pode criar exceções dentro da regra. Por exemplo, você pode filtrar mensagens de todos os domínios, exceto para um determinado domínio. Clique em **Adicionar exceção**e crie suas condições de exceção de forma semelhante à maneira como você criou as outras condições.<br/><br/>A aplicação de uma política de spam a um grupo só é suportada para **grupos de segurança habilitados para email**. 
  
6. Clique em **Salvar**. Um resumo das configurações de política aparecerá no painel direito.

A política padrão não pode ser desabilitada ou excluída, e as políticas personalizadas sempre têm precedência sobre a política padrão. Para políticas personalizadas, você pode marcar ou desmarcar as caixas de seleção na coluna **habilitado** para habilitá-las ou desabilitá-las. Por padrão, todas as políticas estão habilitadas. Para excluir uma política personalizada, selecione a política, clique no ![ícone Excluir](media/ITPro-EAC-DeleteIcon.gif) ícone **excluir** e confirme que você deseja excluir a política.

> [!TIP]
> Você pode alterar a prioridade (ordem de execução) de suas políticas personalizadas clicando na ![](media/ITPro-EAC-UpArrowIcon.gif) seta para cima e ![para baixo](media/ITPro-EAC-DownArrowIcon.gif) ícone de seta para baixo. A política com **prioridade** **0** será executada primeiro, seguida por **1**, depois **2**e assim por diante. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Usar o PowerShell remoto para configurar políticas de filtro de spam

Você também pode configurar e aplicar políticas de filtro de conteúdo no PowerShell. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Para saber como usar o Windows PowerShell para se conectar à proteção do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
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

Você pode habilitar técnicas avançadas de filtragem de spam se quiser buscar uma abordagem mais agressiva para a filtragem de spam. Para configurações gerais de spam que se apliquem a toda a organização, consulte [Prevenir email falso positivo marcado como spam com uma lista segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkId=534224) ou [Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](reduce-spam-email.md). Elas serão úteis se você tiver o controle de nível de administrador e quiser impedir falsos positivos ou falsos negativos.

## <a name="allowblock-lists"></a>Listas de permissões/bloqueios

Haverá momentos em que nossos filtros perderão a mensagem ou levará tempo para que os nossos sistemas se ajustem. Nesse caso, a política antispam possui uma lista permitir e bloquear disponível para substituir o veredicto atual. Essa opção deve ser usada com moderação, já que as listas podem se tornar não gerenciáveis e temporariamente, pois nossa pilha de filtragem deve estar fazendo o que deveria estar fazendo.

As listas de permissões e bloqueios são configuradas como parte de qualquer política antispam do cliente:

1. Na seção **permitir listas** , você pode especificar entradas, como remetentes ou domínios, que sempre serão entregues na caixa de entrada. Os emails dessas entradas não são processados pelo filtro de spam. 
    
      - Adicione remetentes confiáveis à Lista de permissões de remetentes. Clique em **Editar**![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, na caixa de diálogo de seleção, adicione os endereços de remetente que você deseja permitir. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **salvar** para retornar à página de **lista de permissões** . 
        
      - Adicione domínios confiáveis à Lista de permissões de domínios. Clique em **Editar**![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, na caixa de diálogo de seleção, adicione os domínios que você deseja permitir. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **salvar** para retornar à página de **lista de permissões** . 

> [!CAUTION]
> Você nunca deve listar domínios aceitos (domínios que você possui) ou domínios comuns como Microsoft.com, office.com, etc para uma lista de permissões. Isso permitiria que falsificadores enviem emails sem restrições para sua organização.

2. Na página **Listas de Bloqueios**, você pode especificar as entradas, como remetentes ou domínios, que sempre serão marcadas como spam. O serviço aplicará a ação de spam de alta confiança configurada nos emails que corresponderem a essas entradas. 
    
      - Adicione remetentes indesejados à lista de Bloqueios de Remetentes. Clique em **Editar**![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, na caixa de diálogo de seleção, adicione os endereços de remetente que você deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **salvar** para retornar à página **Bloquear listas** . 
        
      - Adicione domínios indesejados à lista de Bloqueio de domínios. Clique em **Editar**![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, na caixa de diálogo de seleção, adicione os domínios que você deseja bloquear. Você pode separar várias entradas usando ponto-e-vírgula ou uma nova linha. Clique em **salvar** para retornar à página **Bloquear listas** .

> [!TIP]
>  Pode haver situações em que sua organização pode não concordar com o veredicto que o serviço fornece. Nesse caso, talvez você queira manter a listagem permitir ou bloquear permanentemente. No entanto, se você for colocar um domínio na lista de permissões por longos períodos de tempo, deverá informar ao remetente para garantir que seu domínio seja autenticado e definido como DMARC rejeitar se não for.

## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection6"> </a>

[Configurando seu domínio para DMARC](use-dmarc-to-validate-email.md)
  
[Quarentena](quarantine.md)
  
[Impedir email falso positivo marcado como spam com uma lista de segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)

[Níveis de confiança de spam](spam-confidence-levels.md)
  

