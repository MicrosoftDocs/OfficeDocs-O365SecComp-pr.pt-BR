---
title: Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
description: 'Como um administrador, você pode exibir, liberar e relatar mensagens em quarentena falso positivas no Office 365. Você pode configurar políticas para que o Office 365 filtra mensagens e as envia para colocar em quarentena por vários motivos: porque eles foram identificados como spam, em massa, phishing, malware ou porque elas correspondem a uma regra de fluxo de email. '
ms.openlocfilehash: be6384d8937e25aec55d82d8212c49d25b64b9a1
ms.sourcegitcommit: d85fc77cba3a17d5ddf215e2f506f61b499e0cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839095"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a>Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365

Como um administrador, você pode exibir, versão e excluir mensagens em quarentena e relatório falso positivo mensagens em quarentena no Office 365. Você também pode exibir, baixar e excluir arquivos em quarentena capturados pelo proteção de ameaça antecipada (ATP) para o SharePoint Online, o OneDrive for Business e Teams da Microsoft. Você pode configurar políticas para que o Office 365 filtra mensagens e as envia para colocar em quarentena por vários motivos: porque eles foram identificados como spam, emails em massa, email de phishing, que contêm malware, ou porque elas correspondem a uma regra de fluxo de email.
  
Por padrão, o Office 365 envia mensagens de phishing e mensagens que contêm malware diretamente para a quarentena. Outras mensagens filtradas são enviadas para a pasta de lixo eletrônico dos usuários, a menos que você configurar uma política de enviá-los para a quarentena.
  
Você deve ter permissões de administrador no Office 365 para trabalhar com mensagens em quarentena que foram enviadas para outros usuários e trabalhar com arquivos em quarentena.
  
> [!IMPORTANT]
> Por padrão, as mensagens que foram colocados em quarentena porque elas correspondem a uma regra de fluxo de email, em massa, malware, phishing e spam são mantidas em quarentena por 30 dias. Você pode personalizar o tempo de quarentena em configurações antispam na segurança &amp; Centro de conformidade. Quando o Office 365 exclui uma mensagem de quarentena, não é possível recuperá-lo. Se desejar, você pode alterar o período de retenção de mensagens em quarentena em suas políticas de filtro anti-spam. Para obter mais informações, consulte [Definindo o período de retenção da quarentena](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) neste artigo. 
  
## <a name="view-your-organizations-quarantined-messages"></a>Exibir mensagens em quarentena de sua organização

1. Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global na sua organização do Office 365, entrar no Office 365 e [vá para o Centro de conformidade e segurança](go-to-the-securitycompliance-center.md).
    
2. Na lista à esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **quarentena**.
    
    > [!TIP]
    > Para ir diretamente para a página de **quarentena** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
    Por padrão, a segurança &amp; Centro de conformidade exibe todas as mensagens de email que tenham sido colocados em quarentena como spam. As mensagens são classificadas do mais recente para o mais antigo com base na **Data** em que a mensagem foi recebida. **Remetente**, **assunto**e a data de validade (sob **expira** ) também são exibidas para cada mensagem. Você pode classificar em um campo clicando no cabeçalho da coluna correspondente; Clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação. 
    
3. Você pode exibir uma lista de todas as mensagens em quarentena, ou você pode reduzir o resultado definido pela filtragem. Você só pode fazer em massa operações em até 100 itens, portanto filtragem também pode ajudar a reduzir seu resultado definido se você tiver mais do que isso. Você pode filtrar mensagens rapidamente por uma razão de quarentena único, escolhendo uma opção do filtro na parte superior da página. As opções incluem:
    
  - Email identificado como spam
    
  - Email em quarentena, pois ela correspondeu a uma política definida por uma regra de fluxo de email (também chamada de uma regra de transporte)
    
  - Email identificado como email em massa
    
  - Email identificado como o email de phishing
    
  - Emails em quarentena porque ele contém malware
    
Além disso, como um administrador, você pode optar por filtrar todas as mensagens para a sua organização ou somente as mensagens enviadas para você. Encerrar os usuários pode apenas exibir e trabalhar com as mensagens enviadas para eles.
  
Você também pode filtrar os resultados para localizar mensagens específicas. Para obter dicas, consulte [para filtrar os resultados e localizar arquivos e mensagens em quarentena](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) neste artigo. 
  
Após localizar uma determinada mensagem em quarentena, clique na mensagem para exibir detalhes sobre ela e realizar ações, como liberar a mensagem à caixa de entrada de alguém.
  
## <a name="view-your-organizations-quarantined-files"></a>Exibir arquivos em quarentena de sua organização

1. Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global na sua organização do Office 365, faça logon no Office 365 e [vá para o Centro de conformidade e segurança](go-to-the-securitycompliance-center.md).
    
2. À esquerda, expanda **Gerenciamento de ameaça**, escolha a **revisão**e escolha **quarentena**. 
    
    > [!TIP]
    > Para ir diretamente para a página de **quarentena** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
3. Por padrão, a página exibe mensagens de email em quarentena. Para exibir arquivos em quarentena, configure os filtros na parte superior da página para mostrar os **arquivos**, colocados em quarentena devido a **malware**. Você deve ter permissões de administrador no Office 365 para trabalhar com arquivos em quarentena. 
    
4. Os arquivos são classificados do mais recente para o mais antigo com base na data em que o arquivo foi colocada em quarentena. O **usuário** que fez a última modificou o arquivo, o **serviço** ao qual o arquivo foi publicado, o **Nome do arquivo**, o **local**, o **Tamanho do arquivo**, e a data de validade ( **expira**) também são listados para cada arquivo. Você pode classificar em um campo clicando em um cabeçalho. Clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação.
    
Você pode exibir uma lista de todos os arquivos em quarentena, ou você pode pesquisar pela filtragem de arquivos específicos. Assim como as mensagens, você só pode fazer operações em até 100 itens em massa. Atualmente, a segurança &amp; Centro de conformidade permite exibir e gerenciar arquivos que estão em quarentena porque eles foram identificados como contendo o malware. Para obter dicas, consulte [para filtrar os resultados e localizar arquivos e mensagens em quarentena](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) neste artigo. 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a>Para filtrar os resultados e localizar arquivos e mensagens em quarentena
<a name="BKMK_AdvSearch"> </a>

Dependendo das suas configurações, pode haver muita mensagens em quarentena e arquivos. Para localizar uma mensagem específica ou o arquivo ou o conjunto de mensagens ou arquivos, você pode filtrar itens em quarentena com base em uma variedade de informações adicionais.
  
1. Na página de **quarentena** , certifique-se de que a linha superior de filtros está definida como exibir mensagens ou arquivos conforme apropriado: 
    
  - Para pesquisar arquivos, configure os filtros para mostrar os **arquivos** em quarentena devido a **malware**.
    
    Para arquivos em quarentena, a página exibe arquivos tudo em quarentena, não apenas sua própria, independentemente do que você dizer equipe de TI para mostrar.
    
  - Para pesquisar mensagens em quarentena, definir filtros para mostrar **tudo** ou **apenas meu** **email**. Para o último filtro escolher o tipo de mensagem em quarentena que você está procurando. Você pode pesquisar mensagens em quarentena que foram identificadas como **spam**, para mensagens que correspondem a um fluxo de email ou **regra de transporte**, email **em massa** , email de **phishing** ou emails que contenham **malware**.
    
2. Em **resultados de classificar por**, selecione o filtro ou os filtros que você deseja usar para pesquisar nas listas suspensas. As opções variam com base em se você estiver procurando por arquivos ou mensagens. Curingas não são suportados nos campos de pesquisa neste momento.
    
    Para arquivos e mensagens, você pode optar por filtrar pela data da mensagem ou arquivo foi enviado para quarentena. Você pode especificar a data ou um intervalo de datas, incluindo o tempo. Você também pode filtrar os resultados de pesquisa pela data de validade no qual o arquivo ou a mensagem será excluída da quarentena, ou você pode usar uma combinação de filtros. Para pesquisar por data de expiração, escolha **filtro avançado**. Em **expira**, você pode selecionar mensagens que serão excluídas da quarentena dentro das próximas 24 horas ( **hoje**) dentro das próximas 48 horas ( **próximo 2 dias**), na próxima semana ( **próximo 7 dias**), ou você pode selecionar um intervalo de tempo personalizada.
    
    Para mensagens, você tem as seguintes opções adicionais:
    
  - **ID da mensagem**. Use esta opção para identificar uma mensagem específica quando você souber a ID de mensagem. 
    
    Por exemplo, se uma mensagem específica é enviada pelo ou destinada a um usuário em sua organização, mas nunca atingiu seu destino, você pode pesquisar a mensagem usando um rastreamento da mensagem (consulte [executar um rastreamento da mensagem e exibir resultados](https://go.microsoft.com/fwlink/?LinkId=799737)). Se você descobrir que a mensagem foi enviada para quarentena, talvez porque ele corresponde a uma regra de fluxo de email ou foi identificado como spam, você pode, em seguida, facilmente encontrar essa mensagem em quarentena especificando seu ID de mensagem. Certifique-se de incluir a cadeia de caracteres de ID de mensagem completa. Isso pode incluir colchetes angulares (\<\>), por exemplo:
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Endereço de email do remetente**. Escolha esta opção para filtrar por um endereço de email do remetente único. 
    
  - **Endereço de email do destinatário**. Escolha esta opção para filtrar por um endereço de email do destinatário único. 
    
  - **Assunto**. Insira o assunto de um endereço de email que você deseja localizar. Desde que não há suporte para a pesquisa de caractere curinga, você deve usar o assunto da mensagem inteiro na ordem de pesquisa para retornar a mensagem nos resultados da. A pesquisa não diferencia maiusculas de minúsculas. 
    
## <a name="view-details-about-quarantined-messages-and-files"></a>Exibir detalhes sobre mensagens em quarentena e arquivos
<a name="BKMK_ViewDetails"> </a>

Quando você seleciona um item exibido na lista de quarentena, você verá um resumo das suas propriedades no painel de **detalhes** no lado direito da segurança &amp; Centro de conformidade. 
  
 **Detalhes exibidas para mensagens em quarentena**
  
- **ID da mensagem**. O identificador exclusivo para a mensagem. 
    
- **Endereço do remetente**. Que enviou a mensagem. 
    
- **Recebida**. A data e hora que a mensagem foi recebida. 
    
- **Assunto**. O texto da linha de assunto da mensagem. 
    
- **Tipo**. Mostra se uma mensagem foi identificada como **Spam**, **em massa**, **phishing**, correspondem a uma regra de fluxo de email ( **regra de transporte**) ou foi identificada como que contêm **Malware**.
    
- **Expira**. A data e hora que a mensagem será excluída automaticamente da quarentena. 
    
- **Liberado para**. Todos os endereços de email (se houver) para o qual a mensagem foi liberada. 
    
- **Ainda não foram lançadas para**. Todos os endereços de email (se houver) para o qual a mensagem ainda não foi liberada. 
    
 **Detalhes exibidos para arquivos em quarentena**
  
- **Nome do arquivo** O nome do arquivo em quarentena. 
    
- **Caminho do site** URL que define o local do arquivo no Office 365. 
    
- **Detectada data / hora** A data e hora que o arquivo foi colocada em quarentena. 
    
- **Expira** A data quando a mensagem será excluída da quarentena. 
    
- **Detectada pelo** O método usado para detectar o malware no arquivo. Isso pode ser ATP (proteção de ameaça avançado) ou mecanismo de antimalware da Microsoft. 
    
- **Lançada** Descreve se ou não o arquivo foi liberado. 
    
- **Nome do malware** Família e o nome do malware detectado no arquivo. 
    
- **ID de documento** Um identificador exclusivo para o documento. 
    
- **Tamanho do arquivo** O tamanho do arquivo no KB. 
    
- **Organização** ID exclusiva de sua organização no Office 365. 
    
- **Modificado por** A conta do usuário que o arquivo da última modificação trabalho ou da escola. 
    
- **Tamanho do arquivo** O tamanho do arquivo no KB. 
    
- **SHA256 Hash** O hash do arquivo. Você pode usar isso para procurar outros repositórios de reputação tenha ou investigar else onde o arquivo pode estar em seu ambiente. 
    
## <a name="managing-messages-and-files-in-quarantine"></a>Gerenciamento de arquivos e mensagens em quarentena
<a name="BKMK_ManageQuarantinedItem"> </a>

Depois de selecionar uma mensagem ou um grupo de mensagens, você tem várias opções para gerenciar mensagens em quarentena.
  
- Nada a fazer. Se você optar por fazer nada, a mensagem será excluída pelo Office 365 automaticamente após o vencimento. Por padrão, as mensagens em quarentena porque elas correspondem a uma regra de fluxo de email, em massa, malware, phishing e spam são mantidas em quarentena por 30 dias. Quando o Office 365 exclui uma mensagem de quarentena, não é possível recuperá-lo. Se desejar, você pode alterar o período de retenção de mensagens em quarentena, definindo a configuração de **reter spam de (dias)** em suas políticas contra spam. Para obter mais informações, consulte [Definindo o período de retenção da quarentena](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) neste artigo. 
    
- **Cabeçalho da mensagem de modo de exibição** Escolha este link para ver o texto do cabeçalho da mensagem. Para analisar o cabeçalho em profundidade, copie o texto do cabeçalho da mensagem para sua área de transferência e escolha o **Analisador de cabeçalho de mensagem do Microsoft** para ir até a Remote Connectivity Analyzer (com o botão direito e escolha **Abrir em uma nova guia** se você não deseja deixar o Office 365 para completar esta tarefa). Cole o cabeçalho da mensagem para a página na seção analisador de cabeçalho de mensagem e escolha **Analisar cabeçalhos**.
    
- **Visualizar a mensagem** Permite que você consulte bruto ou versões HTML do texto do corpo da mensagem. Na exibição de HTML, links estão desabilitadas. 
    
- **Baixar mensagem** ou **baixar o arquivo**. Escolha esta opção para baixar uma cópia da mensagem ou do arquivo para seu dispositivo local. Você precisará confirmar que você entende os riscos associados com o download de itens da quarentena antes que você tenha permissão para fazê-lo. As mensagens são salvas no formato. eml para uma pasta especificada. Arquivos em quarentena são salvos no formato original.
    
- **Excluir** Se desejar, você pode excluir imediatamente um item em quarentena (ou conjunto de itens) em vez de aguardar a data de expiração definida pelo Office 365. Para excluir uma mensagem ou arquivo, na lista de quarentena, selecione o item e escolha **Excluir**. Para excluir vários itens ao mesmo tempo, marque a caixa de seleção à esquerda dos itens na lista de quarentena e, na página **ações em massa** que aparece, escolha **Excluir mensagens selecionadas** ou **Excluir arquivos selecionados**.
    
- **Versão** Liberar um item em quarentena (ou conjunto de itens) e relatar os itens como erroneamente em quarentena (falsos positivos) à Microsoft. 
    
    Para liberar e relatar uma única mensagem ou arquivo, na lista de quarentena, selecione o item, escolha **arquivo versão** ou **liberar mensagem**. Na próxima página, certifique-se de que **as mensagens de relatório para a Microsoft para análise** ou **arquivos de relatório para a Microsoft para análise** está selecionado. 
    
    Para liberar vários itens ao mesmo tempo, marque a caixa de seleção à esquerda dos itens na lista de quarentena e, na página **ações em massa** que aparece, escolha **liberar arquivos** ou **liberar as mensagens**. Na próxima página, certifique-se de que **as mensagens de relatório para a Microsoft para análise** ou **arquivos de relatório para a Microsoft para análise** está selecionado. 
    
Quando você lançando com mensagens, esteja ciente das seguintes opções:
  
- Quando você executa uma versão em massa de várias mensagens ao mesmo tempo, as mensagens são liberadas para todos os destinatários identificados originalmente. Se você deseja liberar as mensagens somente a destinatários específicos, você precisará liberar as mensagens, um por vez e identificar os destinatários individualmente.
    
- Uma mensagem não pode ser liberada em mais de uma vez para o mesmo destinatário.
    
- Quando você lançando com uma mensagem para mais de um destinatário, somente os destinatários que não receberam anteriormente a mensagem aparecerá na lista de destinatários possíveis.
    
- Quando você opta por reportar falsos positivos, se a mensagem ou mensagens que seja liberada foram colocados em quarentena como spam, em massa, phishing, ou que contêm malware, a mensagem também será relatada à equipe de análise de Spam da Microsoft. A equipe será avaliar e analisar a mensagem e, dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir que a mensagem pelo.
    
## <a name="setting-the-quarantine-retention-period"></a>Definindo o período de retenção da quarentena
<a name="BKMK_ModQuarantineTime"> </a>

Você pode configurar quanto tempo mensagens e arquivos permanecerão em quarentena antes que expirem. Por padrão, os itens em quarentena são mantidos por 30 dias. Você definir essa configuração para cada política que você criar. Você também pode modificar o valor para a política padrão, conforme descrito neste artigo. 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a>Para modificar o período de retenção da quarentena para a política de filtro de spam padrão no Centro de conformidade de segurança e

1. Usando uma conta de trabalho ou da escola que tenha privilégios de administrador global na sua organização do Office 365, faça logon no Office 365 e [vá para o Centro de conformidade e segurança](go-to-the-securitycompliance-center.md).
    
2. À esquerda, expanda **Gerenciamento de ameaça**, escolha **política**e escolha **anti-spam**. 
    
    > [!TIP]
    > Para ir diretamente para a página de **antispam** na segurança &amp; Centro de conformidade, use esta URL: >[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)
  
3. Escolha **personalizado** para exibir a guia **configurações personalizadas** . 
    
4. Expanda a linha de **política de filtro de spam do padrão (sempre Diante)** . 
    
5. Escolha **Editar política**. As configurações para a política de filtro de spam do padrão aparecem em uma nova página.
    
6. Expanda **Spam e massa ações**.
    
7. Em **quarentena**, na caixa de texto de **spam de reter de (dias)** , insira a quantidade de tempo que você deseja que o Office 365 para reter os arquivos e mensagens em quarentena. O padrão é 30 dias. Isso também é o valor máximo. 
    
8. Escolha **Salvar**.
    

