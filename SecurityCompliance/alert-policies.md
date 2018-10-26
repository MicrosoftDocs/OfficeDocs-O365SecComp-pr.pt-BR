---
title: Políticas de segurança do Office 365 de alerta &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Criar políticas de alerta de segurança do Office 365 &amp; Centro de conformidade para monitorar o problema de permissões, perda de dados e possíveis ameaças. Em seguida, você pode exibir e gerenciar os alertas que são gerados quando os usuários realizam atividades que correspondam às condições de uma política de alerta.
ms.openlocfilehash: 99025d4a3064e845358ad542d0bfd456d7669dcd
ms.sourcegitcommit: a07b91723bae9ecee2cb092bfbc5b208b30b11a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2018
ms.locfileid: "25793566"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Políticas de segurança do Office 365 de alerta &amp; Centro de conformidade

Você pode usar as ferramentas de alerta de painel e uma política de alerta de nova no Office 365 Security &amp; Centro de conformidade para criar políticas de alerta e, em seguida, exiba os alertas que são gerados quando os usuários realizam atividades que correspondam às condições de uma política de alerta. Alerta políticas basear e expanda a funcionalidade de alertas de atividade, permitindo que você categorizar a política de alerta, aplicar a política a todos os usuários em sua organização, definir um nível de limite para quando um alerta é acionado e decidir se ou não receber emails notificações. Há também uma página **Exibir alertas** na segurança &amp; Centro de conformidade, onde você pode exibir e filtrar alertas, definir um status de alerta para ajudá-lo a gerenciar alertas e, em seguida, descartar alertas depois endereçada ou resolvido o incidente subjacente. Também expandimos o tipo de eventos que você pode criar alertas para. Por exemplo, você pode criar políticas de alerta para acompanhar a atividade de malware e incidentes de perda de dados. Finalmente, também incluímos um número de políticas de alerta padrão que o ajudarão a monitor atribuindo privilégios de administrador no Exchange Online, ataques de malware e incomuns níveis de exclusões de arquivos e compartilhamento externo. 
  
> [!NOTE]
> Políticas de alerta estão disponíveis para organizações com um Office 365 Enterprise e planos do Office 365 conosco governamentais E1/G1, E3/G3 ou E5/G5. No entanto, algumas funcionalidades avançadas só estão disponível para organizações com um planos E5/G5, ou para as organizações que possuem uma E1/G1 ou inscrição E3/G3 e uma assinatura de complemento de inteligência de dados do Office 365 ameaça ou conformidade avançados do Office 365. A funcionalidade que requer assinatura E5/G5 ou complemento é realçada neste tópico. 
  
## <a name="how-alert-policies-work"></a>Trabalho de alerta como diretivas

Aqui está uma visão geral rápida do trabalho de alerta como as políticas e os alertas que são disparadores quando a atividade do usuário ou administrador correspondam às condições de uma política de alerta.
  
![Visão geral do trabalho de alerta como diretivas](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Cria um administrador em sua organização, configura e ativa uma política de alerta, usando a página de **políticas de alerta** na segurança &amp; Centro de conformidade. Você também pode criar políticas de alerta usando o cmdlet **New-ProtectionAlert** no PowerShell. 
    
2. Um usuário realiza uma atividade que corresponde às condições de uma política de alerta. No caso de ataques de malware, mensagens de email infectados enviadas aos usuários em sua organização irá disparar um alerta.
    
3. O Office 365 gera um alerta que é exibido na página **Exibir alertas** na segurança &amp; Centro de conformidade. Além disso, se as notificações de email estão habilitadas para a política de alerta, o Office 365 envia uma notificação para destinatários uma lista. 
    
4. Um administrador gerencia alertas na segurança &amp; Centro de conformidade. Gerenciando alertas consiste em atribuir um status de alerta para ajudar a controlar e gerenciar qualquer investigação.
    

  
## <a name="alert-policy-settings"></a>Configurações de política de alerta

Uma política de alerta consiste em um conjunto de regras e condições que definem a atividade do usuário ou administrador que irá gerar um alerta, uma lista de usuários que iniciará o alerta se eles executarem a atividade, e o limite que define quantas vezes a atividade tem ocorra antes de um alerta n é acionado. Você também categorizar a política e atribuí-lo um nível de severidade. Estas duas configurações ajudarão-lo a gerenciar políticas de alerta (e os alertas que são acionados quando as condições da diretiva são comparadas) porque você pode filtrar essas configurações quando o gerenciamento das políticas e exibição de alertas na segurança &amp; Centro de conformidade. Por exemplo, você pode exibir alertas que correspondam às condições da mesma categoria ou alertas de modo de exibição com o mesmo nível de severidade.
  
Para exibir e criar políticas de alerta, vá para **alertas** \> **políticas de alerta** na segurança &amp; Centro de conformidade. 
  
![Na segurança &amp; Complinace Center, clique em alertas e clique em políticas de visualizar e criar políticas de alerta de alerta](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Uma política de alerta consiste as configurações e as condições a seguir.
  
- **O alerta de atividade está acompanhando** - você criar uma diretiva para controlar uma atividade ou em alguns casos, algumas das atividades relacionadas, tais um compartilhamento de um arquivo com um usuário externo por compartilhá-lo, atribuindo permissões de acesso ou criando um link anônimo. Quando um usuário realiza a atividade definida pela diretiva, um alerta é acionado com base nas configurações de limite de alerta.
    
    > [!NOTE]
    > As atividades que você pode rastrear dependem de assinatura do Office 365 Enterprise da sua organização. Em geral, as atividades relacionadas a campanhas de malware e ataques de phishing requerem uma assinatura E5 ou uma assinatura E1 ou E3 com uma assinatura de complemento de inteligência de ameaça. 
  
- **Condições de atividade** - maioria das atividades, é possível definir condições adicionais que devem ser atendidas para um alerta seja disparado. Condições comuns incluem IP lida (de forma que um alerta é acionado quando o usuário executa a atividade em um computador com um endereço IP específico ou dentro de um intervalo de endereços IP), se um alerta será acionado se um usuário específico ou usuários executam essa atividade e se a atividade é executada em um nome de arquivo específico ou URL. Você também pode configurar uma condição que dispara um alerta quando a atividade é executada por qualquer usuário em sua organização. Observe que as condições disponíveis dependem da atividade selecionada.
    
- **Quando o alerta for disparado** - você pode definir uma configuração que define a frequência uma atividade pode ocorrer antes que um alerta é acionado. Isso permite que você configure uma política para gerar um alerta sempre que uma atividade corresponde às condições de política, quando um certo limite for excedido, ou quando a ocorrência da atividade de que alerta está acompanhando fica incomum nossa organização. 
    
    ![Configurar como os alertas são disparados, com base em quando a atividade ocorre, um limite ou atividade incomum para sua organização](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Se você selecionar a configuração com base em uma atividade incomum, o Office 365 estabelece um valor de linha de base que define a frequência normal para a atividade selecionada; leva até sete dias para estabelecer essa linha de base, durante o qual os alertas não ser geradas. Depois que a linha de base é estabelecida, um alerta será acionado quando a frequência da atividade controlada pela política de alerta significativamente excede o valor de linha de base. Para atividades relacionadas a auditoria (por exemplo, arquivos e pastas atividades), é possível estabelecer uma linha de base com base em um único usuário ou em todos os usuários em sua organização; para atividades relacionadas a malware, é possível estabelecer uma linha de base com base em uma família de malware único, um único destinatário ou todas as mensagens em sua organização.
    
    > [!NOTE]
    > A capacidade de configurar as políticas de alerta com base em um limite ou com base em uma atividade incomum requer uma assinatura E5 ou uma assinatura E1 ou E3 com uma assinatura de complemento de inteligência de ameaça ou conformidade avançadas. Organizações com uma assinatura E1 e E3 só podem criar uma política de alerta onde um alerta é disparado sempre que ocorre uma atividade. 
  
- **Categoria de alerta** - para ajudá-lo a controlar e gerenciar os alertas gerados por uma política, você pode atribuir uma das seguintes categorias a uma política.
    
  - Governança de dados
    
  - Prevenção contra perda de dados

  - Fluxo de mensagens
    
  - Permissões
    
  - Gerenciamento de ameaças
    
  - Outras pessoas
    
    Quando uma atividade ocorre que corresponde às condições da política de alerta, o alerta que seja gerado marcado com a categoria definida nessa configuração. Isso permite controlar e gerenciar alertas que tenham a mesma configuração de categoria na página **Exibir alertas** na segurança &amp; Centro de conformidade pois você pode classificar e filtrar alertas com base na categoria. 
    
- **Alerta gravidade** - semelhante à categoria de alerta, atribua um atributo de gravidade ( **baixa**, **média**ou **alta**) políticas de alerta. Como a categoria de alerta, quando uma atividade ocorre que corresponde às condições da diretiva de alerta, o alerta que seja gerado é marcado com o mesmo nível de severidade que está definido para a política de alerta. Novamente, isso permite controlar e gerenciar alertas que tenham a mesma configuração de severidade na página **Exibir alertas** . Por exemplo, você pode filtrar a lista de alertas para que somente os alertas com severidade **alta** sejam exibidos. 
    
    > [!TIP]
    > Ao configurar uma política de alerta, considere a atribuição de severidade superior a atividades que podem resultar em consequências está seriamente negativas, como detecção de malware após a entrega aos usuários, a visualização dos dados sigilosos ou confidenciais, compartilhamento de dados com usuários externos, ou outras atividades que podem resultar em ameaças de segurança ou de perda de dados. Isso pode ajudá-lo a priorizar os alertas e as ações relacionadas a investigar e resolver as causas subjacentes. 
  
- **Notificações de email** - você pode configurar a política para que as notificações de email são enviadas (ou não enviadas) para uma lista de usuários quando um alerta é acionado. Você também pode definir um limite de notificação diária para que quando o número máximo de notificações for atingido, nenhuma notificação mais sejam enviadas para o alerta durante o dia. Na adicionais para as notificações de email outros administradores ou você podem exibir os alertas que são acionados por uma política na página **Exibir alertas** . Considere habilitar as notificações por email de alertas políticas de uma categoria específica ou que tenham uma configuração de severidade maior. 
  
## <a name="default-alert-policies"></a>Políticas de alerta padrão

O Office 365 fornece diretivas de alerta internas que ajudam a identificar mau uso de permissões de administrador do Exchange, a atividade de malware e riscos de governança de dados. Na página de **políticas de alerta** , o nome dessas políticas internas estão em negrito e o tipo de política é definido como **sistema**. Essas diretivas são ativadas por padrão. Você pode desativar essas diretivas (ou logon novamente), configure uma lista de destinatários aos quais enviar notificações de email e definir um limite de notificação de diário. As outras configurações para essas diretivas não podem ser editadas.
  
A tabela a seguir lista e descreve as políticas de alerta padrão disponíveis e indica os planos do Office 365 Enterprise e Govenment 365 Office conosco necessários para cada uma delas. Observe que algumas políticas de alerta padrão estão disponíveis se a sua organização tenha a assinatura de complemento apropriado, além de uma inscrição E1/G1 ou E3/G3. 
  
|**Política de alerta padrão**|**Descrição**|**Planos do Office 365**|
|:-----|:-----|:-----|
|**Criação da regra de encaminhamento/redirecionamento** <br/> |Gera um alerta quando alguém em sua organização cria uma regra de caixa de entrada para suas caixas de correio que encaminha ou redireciona as mensagens para outra conta de email. Essa diretiva controla somente as regras de entrada que são criadas usando o Outlook Web App ou do PowerShell do Exchange Online. Essa diretiva tem uma configuração de gravidade de **baixo** . Para obter mais informações usando regras de caixa de entrada para encaminhar e redirecionar o email no Outlook Web App, consulte [Use regras no Outlook Web App para encaminhar automaticamente mensagens para outra conta](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).<br/> |/ G1 de E1, E3/G3 ou E5/G5  <br/> |
|**pesquisa de descoberta eletrônica iniciada ou exportados** <br/> |Gera um alerta quando alguém utiliza a ferramenta de pesquisa de conteúdo no Centro de conformidade & segurança. Um alerta é acionado quando as seguintes atividades de pesquisa de conteúdo são realizadas:<br/><br/>• Uma pesquisa de conteúdo é iniciado<br/>• Os resultados de uma pesquisa de conteúdo são exportados<br/>• Um relatório de pesquisa de conteúdo é exportado<br/><br/>Alertas são também trigged quando as atividades de pesquisa de conteúdo anterior são realizadas em associação com um caso de eDiscovery. Essa diretiva tem uma configuração de severidade **média** . Para obter mais informações sobre atividades de pesquisa de conteúdo, consulte [Search para atividades de descoberta eletrônica no Office 365 log de auditoria](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities).<br/> |/ G1 de E1, E3/G3 ou E5/G5  <br/> |
|**Elevação do privilégio de administração do Exchange** <br/> |Gera um alerta quando alguém recebe permissões administrativas em sua organização do Exchange Online; Por exemplo, se um usuário é adicionado à função de gerenciamento da organização grupo no Exchange Online. Essa diretiva tem uma configuração de gravidade de **baixo** .<br/> |/ G1 de E1, E3/G3 ou E5/G5  <br/> |
|**As mensagens foram adiadas** <br/> |Gera um alerta quando o Office 365 não pode enviar mensagens de email para sua organização local ou de um parceiro de servidores usando um conector. Quando isso acontecer, a mensagem está na fila no Office 365. Esse alerta é disparado quando há 2.000 mensagens ou mais enfileirados para mais de uma hora. Essa diretiva tem uma configuração de severidade **alta** .<br/> |/ G1 de E1, E3/G3 ou E5/G5  <br/> |
|**Campanha de malware detectada após a entrega** <br/> |Gera um alerta quando um grande número incomum de mensagens que contêm malware é entregues às caixas de correio em sua organização. Se esse evento ocorrer, o Office 365 removerá as mensagens infectadas das caixas postais do Exchange Online. Essa diretiva tem uma configuração de severidade **alta** .<br/> |Assinatura de complemento E5/G5 ou inteligência de ameaça do Office 365  <br/> |
|**Campanha de malware detectadas e bloqueadas** <br/> |Gera um alerta quando alguém tentou enviar um grande número incomum de mensagens de email contendo um determinado tipo de malware aos usuários em sua organização. Se esse evento ocorrer, as mensagens infectadas são bloqueadas pelo Office 365 e não entregue às caixas de correio. Essa diretiva tem uma configuração de gravidade de **baixo** .<br/> |Assinatura de complemento E5/G5 ou inteligência de ameaça do Office 365  <br/> |
|**Campanha de malware detectada no SharePoint e OneDrive** <br/> |Gera um alerta quando um alto volume de malware ou vírus forem detectados nos arquivos localizados em sites do SharePoint ou contas de OneDrive em sua organização. Essa diretiva tem uma configuração de severidade **alta** .<br/> |Assinatura de complemento E5/G5 ou inteligência de ameaça do Office 365  <br/> |
|**Atividade de arquivo incomum de usuário externo** <br/> |Gera um alerta quando um geralmente grande número de atividades é realizado em arquivos no SharePoint ou OneDrive por usuários fora da sua organização. Isso inclui atividades como acessar arquivos de download de arquivos e excluindo os arquivos. Essa diretiva tem uma configuração de severidade **alta** .<br/> |E5/G5 ou inscrição de complemento de inteligência de dados do Office 365 ameaça ou conformidade avançadas  <br/> |
|**Volume incomum de compartilhamento de arquivo externo** <br/> |Gera um alerta quando um geralmente grande número de arquivos no SharePoint ou OneDrive é compartilhado com usuários fora da sua organização. Essa diretiva tem uma configuração de severidade **média** .<br/> |E5/G5 ou inscrição de complemento de inteligência de dados do Office 365 ameaça ou conformidade avançadas  <br/> |
|**Volume incomum de exclusão de arquivo** <br/> |Gera um alerta quando um grande número incomum de arquivos é excluído no SharePoint ou OneDrive em um período curto período de tempo. Essa diretiva tem uma configuração de severidade **média** .<br/> |E5/G5 ou inscrição de complemento de inteligência de dados do Office 365 ameaça ou conformidade avançadas  <br/> |
|**Aumento incomum no email relatado como phishing** <br/> |Gera um alerta quando há um aumento significativo no número de pessoas da sua organização usando o suplemento de mensagem de relatório no Outlook às mensagens de relatório, como o email de phishing. Essa diretiva tem uma configuração de severidade **alta** . Para obter mais informações sobre este suplemento, consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).<br/> |Assinatura de complemento E5/G5 ou inteligência de ameaça do Office 365  <br/> |
   
Observe que a atividade incomum monitorada pelo algumas das diretivas internas se baseia no mesmo processo conforme o limite de alerta configuração que foi descrito anteriormente. O Office 365 estabelece um valor de linha de base que define a frequência normal para a atividade "normal". Alertas, em seguida, são acionadas quando a frequência de atividades controladas pela política de alerta interna significativamente excede o valor de linha de base.
 
## <a name="viewing-alerts"></a>Exibição de alertas

Quando uma atividade realizada por usuários em sua organização coincidem com as configurações de uma política de alerta, um alerta é gerado e exibido na página **Exibir alertas** na segurança &amp; Centro de conformidade. Dependendo das configurações de uma política de alerta, uma notificação de e-mail também é enviada para uma lista de usuários especificados quando um alerta é acionado. Para cada alerta, o painel na página **Exibir alertas** exibe o nome da diretiva de alerta correspondente, a gravidade e a categoria para o alerta (definido na política de alerta) e o número de vezes que ocorreu uma atividade que resultou no alerta que está sendo gerado; Esse valor baseia-se na configuração da política de alerta de limite. O painel também mostra o status de todos os alertas. Consulte a seção [Gerenciando alertas](#managing-alerts) para obter mais informações sobre como usar a propriedade status para gerenciar alertas. 
  
Para exibir alertas, vá para **alertas** \> **Exibir alertas** na segurança &amp; Centro de conformidade. 
  
![Na segurança &amp; Complinace Center, clique em alertas e clique em Exibir alertas para exibir alertas](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Você pode usar os seguintes filtros para exibir um subconjunto de todos os alertas na página **Exibir alertas** . 
  
- **Status** - Use este filtro para mostrar os alertas que são atribuídas a um determinado status; o status padrão está **ativa**. Outros administradores ou você podem alterar o valor de status.
    
- **Política** - Use este filtro para mostrar os alertas que correspondem a configuração de uma ou mais políticas de alerta. Ou então, você apenas poderá exibir todos os alertas para todas as políticas de alerta.
    
- **Intervalo de tempo** - Use este filtro para mostrar os alertas que foram gerados dentro de uma data específica e um intervalo de tempo.
    
- **Gravidade** - Use este filtro para mostrar alertas que são atribuídas a severidade específica.
    
- **Categoria** - Use este filtro para mostrar os alertas de uma ou mais categorias de alerta.
    

  
## <a name="managing-alerts"></a>Gerenciando alertas
<a name="managingalerts"> </a>

Depois que os alertas foram geradas e exibidas na página **Exibir alertas** na segurança &amp; Centro de conformidade, você pode triagem, investigar e resolvê-los. Aqui estão algumas tarefas que podem ser executadas para gerenciar alertas. 
  
- **Atribuir um status alertas** - você pode atribuir um dos seguintes status alertas: **ativo** (o valor padrão), **Investigating**, **Resolved**ou **Dismissed**. Em seguida, você pode filtrar essa configuração para exibir alertas com a mesma configuração de status. Essa configuração de status pode ajudar a controlar o processo de gerenciamento de alertas.
    
- **Exibir detalhes de alerta** - você pode clicar em um alerta para exibir uma página de submenu com detalhes sobre o alerta. As informações detalhadas dependem da diretiva de alerta correspondente, mas normalmente inclui o seguinte: nome da operação real que disparou o alerta (por exemplo, um cmdlet), uma descrição da atividade que disparou o alerta, o usuário (ou lista de usuários) que disparou o alerta e o nome (e um link para) de correspondente de política de alerta.
    
  - O nome da operação real que disparou o alerta, como um cmdlet ou uma operação de log de auditoria.
    
  - Uma descrição da atividade que disparou o alerta.
    
  - O usuário que disparou o alerta; Isso é incluído apenas para as políticas de alerta que estão configuradas para rastrear um único usuário ou uma única atividade.
    
  - O número de vezes que a atividade controlada pelo alerta foi executado. Observe que esse número não pode corresponder a esse número real de alertas relacionados listado na página Exibir alertas porque alertas adicionais acionadas.
    
  - Um link para uma lista de atividade que inclui um item para cada atividade foi executada que disparou o alerta. Cada entrada nessa lista identifica quando a atividade ocorreu, o nome da operação real, (por exemplo, "FileDeleted") e o usuário que executou a atividade, o objeto (por exemplo, um arquivo, um caso de descoberta eletrônica ou uma caixa de correio) que a atividade foi executada em e o IP endereço do computador do usuário. Para malware relacionadas a alertas, esta contém links para uma lista de mensagens.
    
  - O nome (e um link para) da política de alerta correspondente.
    
- **Suprimir notificações de email** - você pode desativar (ou suprimir) notificações de email da página do submenu para um alerta. Quando você suprime notificações de email, o Office 365 não enviar notificações quando atividades ou eventos que coincidem com as condições da política de alerta. No entanto, alertas continuarão a ser gatilho quando atividades realizadas pelos usuários coincidem com as condições da política de alerta. Você também pode desativar as notificações de email editando a política de alerta.
    
- **Resolver alertas** - você pode marcar um alerta como resolvido na página de submenu para um alerta (que define o status do alerta para **Resolved**). A menos que você altera o filtro, alertas resolvidos não são exibidos na página **Exibir alertas** . 
    

  

