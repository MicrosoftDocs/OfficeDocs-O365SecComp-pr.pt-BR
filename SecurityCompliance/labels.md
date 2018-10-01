---
title: Visão geral de rótulos
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Os rótulos no Office 365 podem ajudar você a executar as ações certas no conteúdo certo. Com os rótulos, você pode classificar os dados em toda a organização para prover governança e impor regras de retenção com base nessa classificação. Você também pode usar os rótulos para implementar o gerenciamento de registros no Office 365.
ms.openlocfilehash: 3a99a3e563913a11da2d9f4a2eb745cb8fa80dd2
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25342809"
---
# <a name="overview-of-labels"></a>Visão geral de rótulos

Provavelmente, há em sua organização tipos de conteúdo diferentes que exigem ações diferentes para atender às normas do setor e às políticas internas. Por exemplo, você pode ter:
  
- Formulários fiscais que precisam ser **mantidos** por um período mínimo. 
    
- Materiais de imprensa que precisam ser **excluídos permanentemente** quando atingem uma certa idade. 
    
- Pesquisa sobre a concorrência que precisa ser **mantida** e, depois, **excluída permanentemente**. 
    
- Vistos de trabalho que devem ser **marcados como um registro** para que não possam ser editados ou excluídos. 
    
Em todos esses casos, os rótulos no Office 365 podem ajudar você a executar as ações certas no conteúdo certo. Com os rótulos, você pode classificar os dados em toda a organização para prover governança e impor regras de retenção com base nessa classificação.
  
Com os rótulos, você pode:
  
- **Permitir que pessoas na sua organização apliquem um rótulo manualmente** ao conteúdo no Outlook na Web, Outlook 2010 e posterior, OneDrive, SharePoint e grupos do Office 365. Os usuários geralmente sabem melhor o tipo de conteúdo com o qual estão trabalhando, portanto, podem classificá-lo e aplicar a política apropriada. 
    
- **Aplique automaticamente os rótulos ao conteúdo** que corresponder a condições específicas, por exemplo, quando o conteúdo apresenta: 
    
  - Tipos específicos de informações confidenciais.
    
  - Palavras-chave específicas que correspondem a uma consulta criada por você.
    
    A capacidade de aplicar rótulos automaticamente ao conteúdo é importante porque:
    
  - Você não precisa treinar os usuários com relação a todas as suas classificações.
    
  - Você não precisa depender dos usuários para classificar corretamente o conteúdo.
    
  - Os usuários não precisam mais conhecer as políticas de governança de dados; em vez disso, eles podem se concentrar no próprio trabalho.
    
    Observe que os rótulos de aplicação automática exigem uma assinatura do Office 365 Enterprise E5.
    
- **Aplique um rótulo padrão a uma biblioteca de documentos** em sites de grupo do SharePoint ou do Office 365, de forma que todos os documentos nessa biblioteca recebam o rótulo padrão. 
    
- **Implemente o gerenciamento de registros no Office 365**, incluindo em emails e documentos. Você pode usar um rótulo para classificar o conteúdo como registro. Quando isso acontece, o rótulo não pode ser alterado ou removido, e o conteúdo não pode ser editado ou excluído. 
    
Crie e gerencie rótulos na página **Rótulos** no Centro de Conformidade &amp; Segurança do Office 365. 
  
![Página Rótulos](media/42d1865d-f0f5-436d-8e09-0e547302c816.png)
 
## <a name="how-labels-work-with-label-policies"></a>Como os rótulos funcionam com as políticas de rótulo

A disponibilização dos rótulos para as pessoas da sua organização, para que elas possam classificar o conteúdo, é um processo de duas etapas: primeiro você cria os rótulos e, depois, os publica nos locais escolhidos. Quando você publica os rótulos, uma política de rótulos é criada.
  
![Diagrama de funções e tarefas para rótulos](media/4082bc7d-c04c-4b9a-8a26-7f12565d3311.png)
  
Os rótulos são blocos de construção independentes e reutilizáveis, incluídos em uma política de rótulos e publicados em locais diferentes. Eles podem ser reutilizados em várias políticas. O objetivo principal da política de rótulos é agrupar os rótulos e especificar os locais nos quais você deseja exibi-los.
  
![Diagrama de rótulos, políticas de rótulo e locais](media/eee42516-adf0-4664-b5ab-76727a9a3511.png)
  
1. Ao publicar os rótulos, eles são incluídos em uma política de rótulos. Um único rótulo pode ser incluído em muitas políticas.
    
2. As políticas de rótulo especificam os locais de publicação dos rótulos.
    
## <a name="only-one-label-at-a-time"></a>Apenas um rótulo por vez

É importante saber que um conteúdo como email ou documento só pode receber um único rótulo por vez:
  
- No caso dos rótulos atribuídos manualmente por usuários finais, as pessoas podem remover ou alterar o rótulo.
    
- Se o conteúdo tiver um rótulo de aplicação automática, um rótulo de aplicação automática pode ser substituído por um rótulo atribuído manualmente por um usuário final.
    
- Se o conteúdo tiver um rótulo atribuído manualmente por um usuário final, um rótulo de aplicação automática não poderá substituir o rótulo atribuído manualmente.
    
- Se houver várias regras que atribuem um rótulo de aplicação automática, e o conteúdo atender às condições das regras, o rótulo da regra mais antiga será atribuída.
    
Os rótulos atribuídos manualmente são explicitamente atribuídos; os rótulos aplicados automaticamente são implicitamente atribuídos; um rótulo explícito tem precedência sobre um rótulo implícito. Para saber mais, confira a seção abaixo sobre [Os princípios de retenção ou o que tem precedência?](labels.md#principles).
  
## <a name="how-long-it-takes-for-labels-to-take-effect"></a>Quanto tempo demora até os rótulos entrarem em vigor

Quando você publica ou aplica rótulos automaticamente, eles não entram em vigor imediatamente:
  
1. Primeiro, a política de rótulos precisa ser sincronizada com os locais na política no Centro de Conformidade &amp; Segurança.
    
2. Depois, o local pode precisar de algum tempo para disponibilizar os rótulos manuais para os usuários finais, ou aplicar rótulos automaticamente ao conteúdo. Quanto tempo isso demora depende do local e do tipo de rótulo.
    
### <a name="manual-labels"></a>Rótulos manuais

Se você publicar rótulos no SharePoint ou no OneDrive, talvez demore um dia para que esses rótulos apareçam para os usuários finais. Além disso, se você publicar os rótulos no Exchange, talvez demore sete dias para que eles apareçam para os usuários finais, e a caixa de correio deles deve conter pelo menos 10 MB de dados.
  
![Diagrama de quando os rótulos manuais entram em vigor](media/b19f3a10-f625-45bf-9a53-dd14df02ae7c.png)
  
### <a name="auto-apply-labels"></a>Aplicar rótulos automaticamente

Se você aplicar automaticamente os rótulos ao conteúdo que atenda a condições específicas, talvez demore sete dias para que os rótulos sejam aplicados a todo o conteúdo que corresponde às condições.
  
![Diagrama de quando os rótulos de aplicação automática entram em vigor](media/b8c00657-477a-4ade-b914-e643ef97a10d.png)
  
### <a name="how-to-check-on-the-status-of-exchange-labels"></a>Como verificar o status dos rótulos do Exchange

No Exchange Online, os rótulos são disponibilizados para os usuários finais por um processo executado a cada sete dias. Usando o Powershell, é possível ver quando esse processo foi executado pela última vez e, assim, determinar quando ele será executado novamente.
  
1. [Conectar-se ao Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=799773).
    
2. Execute estes comandos.
    
  ```
  $logProps = Export-MailboxDiagnosticLogs <user> -ExtendedProperties
  ```

  ```
  $xmlprops = [xml]($logProps.MailboxLog)
  ```

  ```
  $xmlprops.Properties.MailboxTable.Property | ? {$_.Name -like "ELC*"}
  ```

    Nos resultados, a propriedade `ELCLastSuccessTimeStamp` (UTC) mostra quando o sistema processou sua caixa de correio pela última vez. Se isso não tiver ocorrido desde quando você criou a política, os rótulos não serão exibidos. Para forçar o processamento, execute `Start-ManagedFolderAssistant -Identity <user>`.
    
    Se os rótulos não estiverem aparecendo no Outlook na Web, e você achar que deveriam aparecer, limpe o cache do navegador (CTRL + F5).
    
## <a name="label-policies-and-locations"></a>Políticas e locais de rótulo

É possível publicar tipos diferentes de rótulos em locais diferentes, dependendo do que o rótulo faz.
  
|**Se o rótulo for...**.|**A política do rótulo poderá ser aplicada a...**|
|:-----|:-----|
|Publicado para usuários finais  <br/> |Exchange, SharePoint, OneDrive, grupos do Office 365  <br/> |
|Aplicado automaticamente com base em tipos de informações confidenciais  <br/> |Exchange (somente para todas as caixas de correio), SharePoint, OneDrive  <br/> |
|Aplicado automaticamente com base em uma consulta  <br/> |Exchange, SharePoint, OneDrive, grupos do Office 365  <br/> |
   
Observe que, no Exchange, os rótulos de aplicação automática (para consultas e tipos de informações confidenciais) são aplicados apenas a mensagens recentemente enviadas (dado em trânsito), não a todos os itens na caixa de correio (dados em repouso). Além disso, a aplicação automática de rótulos para tipos de informações confidenciais só pode ocorrer para todas as caixas de correio; não é possível selecionar caixas de correio específicas.
  
As pastas públicas do Exchange e o Skype não dão suporte a rótulos.
  
## <a name="how-labels-enforce-retention"></a>Como os rótulos impõem a retenção

Os rótulos podem impor exatamente as mesmas ações de retenção que uma política de retenção. Use rótulos para implementar um plano de conteúdo sofisticado (ou plano de arquivo). Para saber mais sobre como funciona a retenção, confira [Visão geral das políticas de retenção](retention-policies.md).
  
Além disso, um rótulo tem duas opções de retenção, disponíveis apenas em um rótulo, e não em uma política de retenção. Com um rótulo, você pode:
  
- Disparar uma revisão de disposição ao final do período de retenção, de modo que os documentos do SharePoint e do OneDrive sejam revisados antes de serem excluídos. Para saber mais, confira [Visão geral das revisões de disposição](disposition-reviews.md).
    
- Iniciar o período de retenção a partir do momento de aplicação do rótulo no conteúdo, em vez da idade do conteúdo ou da última modificação.
    
![Configurações de retenção com opções específicas aos rótulos](media/c49118c9-6279-4661-94db-deffa76e27ac.png)
  
## <a name="where-published-labels-can-appear-to-end-users"></a>Onde os rótulos publicados podem aparecer aos usuários finais

Se o seu rótulo for atribuído ao conteúdo por usuários finais, você poderá publicá-lo no:
  
- Outlook na Web
    
- Outlook 2010 e posterior
    
- OneDrive
    
- SharePoint
    
- Grupos do Office 365 (o site do grupo e a caixa de correio do grupo no Outlook na Web)
    
As seções a seguir mostram como os rótulos serão exibidos em aplicativos diferentes para as pessoas em sua organização.
  
### <a name="outlook-on-the-web"></a>Outlook na Web

Para rotular um item no Outlook na Web, clique com o botão direito no item \> **Atribuir Política** \> escolha o rótulo. 
  
![Atribuir um menu de política no Outlook na Web](media/146a23cf-e478-4595-b2e8-f707fc4e6ea3.png)
  
Após a aplicação do rótulo, você poderá exibir esse rótulo e a ação necessária na parte superior do item. Se um email for classificado e tiver um período de retenção associado, você poderá saber rapidamente quando o email expirará.
  
![Rótulo atribuído ao email no Outlook na Web](media/16f6c91b-5eab-4574-9d13-6d12be00a783.png)
  
Você também pode aplicar os rótulos a pastas e, nesse caso:
  
- Todos os itens recebem automaticamente o mesmo rótulo, **exceto** itens que receberam um rótulo explicitamente aplicado. Itens rotulados explicitamente mantêm o rótulo existente. Para saber mais, confira a seção abaixo sobre os princípios de retenção. 
    
- Se você alterar ou remover o rótulo padrão de uma pasta, ele também será alterado ou removido para todos os itens na pasta, **exceto** itens com rótulos explícitos. 
    
- Se você mover um item com um rótulo padrão de uma pasta para outra com um rótulo padrão diferente, o item receberá o novo rótulo padrão.
    
- Se você mover um item com um rótulo padrão de uma pasta para outra sem um rótulo padrão, o rótulo padrão antigo será removido.
    
### <a name="outlook-2010-and-later"></a>Outlook 2010 e posterior

Para rotular um item no Outlook na Web, clique com o botão direito no item \> na **Faixa de Opções** \> **Atribuir Política** \> escolha o rótulo. 
  
![Botão Atribuir Política](media/30684dea-dd73-4e4a-9185-8e29f403b6ca.png)
  
Após a aplicação do rótulo, você poderá exibir esse rótulo e a ação necessária na parte superior do item. Se um email for classificado e tiver um período de retenção associado, você poderá saber rapidamente quando o email expirará.
  
Você também pode aplicar rótulos a pastas. Isso funciona no Outlook 2010 ou posterior da mesma maneira que funciona no Outlook na Web. Confira a seção anterior para saber mais.
  
### <a name="onedrive-and-sharepoint"></a>OneDrive e SharePoint

Para rotular um documento (incluindo arquivos do OneNote) no OneDrive ou SharePoint, selecione o item \> no canto superior direito, escolha **Abrir no painel de detalhes**![Ícone do painel de informações](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) \> **Aplicar rótulo** \> escolha o rótulo. 
  
Observe que você também pode aplicar um rótulo a uma pasta ou conjunto de documentos, e você pode definir um rótulo padrão para uma biblioteca de documentos. Confira a seção abaixo para saber mais.
  
![Aplicar lista de rótulos para um item no SharePoint](media/151cc83c-da57-45b0-9cd1-fd2f28a31083.png)
  
Após a aplicação de um rótulo a um item, será possível exibi-lo no painel de detalhes após a seleção do item.
  
![Rótulo aplicado exibido no painel Detalhes](media/d06e585e-29f7-4c8c-afef-629c97268b8e.png)
  
Também é possível criar um modo de exibição da biblioteca que contém a coluna **Rótulos** ou a coluna **Item é um Registro**, para que você possa ver rapidamente os rótulos atribuídos a todos os itens e quais itens são registros. No entanto, você não pode filtrar o modo de exibição pela coluna **Item é um Registro**. 
  
![Coluna de bibliotecas para rótulos exibidos no modo de exibição personalizado](media/e3392627-c0a3-405e-bb57-55f27c34cfdd.png)
  
### <a name="office-365-groups"></a>Grupos do Office 365

Ao publicar rótulos em um grupo do Office 365, eles aparecem no site do grupo e na caixa de correio do grupo no Outlook na Web. A experiência de aplicação de um rótulo ao conteúdo é idêntica à exibida acima para email e documentos.
  
## <a name="applying-a-label-automatically-based-on-conditions"></a>Aplicar um rótulo automaticamente com base em condições

Um dos recursos mais avançados dos rótulos é a capacidade de aplicá-los automaticamente ao conteúdo que atende a certas condições. Nesse caso, as pessoas em sua organização não precisam aplicar os rótulos, o Office 365 faz isso por elas.
  
![Diagrama de funções e tarefas para aplicação automática de rótulos](media/32f2f2fd-18a8-43fd-839d-72ad7a43e069.png)
  
Os rótulos de aplicação automática são excelentes porque:
  
- Você não precisa treinar os usuários com relação a todas as suas classificações.
    
- Você não precisa depender dos usuários para classificar corretamente o conteúdo.
    
- Os usuários não precisam mais conhecer as políticas de governança de dados; assim podem se concentrar no próprio trabalho.
    
Você pode optar por aplicar os rótulos automaticamente ao conteúdo quando esse conteúdo apresentar:
  
- Tipos específicos de informações confidenciais.
    
- Palavras-chave específicas que correspondem a uma consulta criada por você.
    
![Página Escolher condição para aplicação automática de rótulo](media/c0b7a3ef-bda0-494c-941d-f1f93753ecdd.png)
  
Observe que os rótulos de aplicação automática exigem uma assinatura do Office 365 Enterprise E5, e que pode demorar até sete dias para aplicação automática desses rótulos a todo o conteúdo que atenda às condições, conforme descrito acima.
  
### <a name="auto-apply-labels-to-content-with-specific-types-of-sensitive-information"></a>Aplicar automaticamente rótulos a conteúdo com tipos específicos de informações confidenciais

Ao criar rótulos de aplicação automática para informações confidenciais, você vê a mesma lista de modelos de política exibida quando você cria uma política DLP (prevenção contra perda de dados). Cada modelo de política é pré-configurado para procurar tipos específicos de informações confidenciais, por exemplo, o modelo mostrado aqui procura pelo ITIN (Número de identificação de contribuinte individual) dos EUA, SSN (cadastro de pessoas físicas) e números de passaporte. Para saber mais sobre DLP, confira [Visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md).
  
![Modelos de política com tipos de informações confidenciais](media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)
  
Depois de selecionar um modelo de política, você pode adicionar ou remover quaisquer tipos de informações confidenciais, e pode alterar a contagem de instâncias e precisão de correspondência. No exemplo mostrado aqui, um rótulo será aplicado automaticamente apenas quando:
  
- O conteúdo tiver entre uma e nove instâncias de qualquer um destes três tipos de informações confidenciais. Você pode excluir o valor **max** para que mude para **any**.
    
- O tipo de informação confidencial detectado tiver uma precisão de correspondência (ou nível de confiança) de pelo menos 75. Muitos tipos de informações confidenciais são definidos com vários padrões, em que um padrão de precisão de correspondência superior exige mais evidências para ser encontrado (como palavras-chave, datas ou endereços), enquanto um padrão de precisão de correspondência inferior exige menos evidências. Resumindo, quanto menor a precisão de correspondência **min**, mais fácil será para o conteúdo atender à condição. 
    
    Se você alterar a precisão de correspondência (ou o nível de confiança), deverá usar um dos níveis de confiança usados em um padrão para esse tipo de informação confidencial, conforme definido em [O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).
    
![Opções para identificar tipos de informações confidenciais](media/de255881-f596-4c8d-8359-e974e3a0819a.png)
  
### <a name="auto-apply-labels-to-content-with-keywords-or-searchable-properties"></a>Aplicar rótulos automaticamente a conteúdos com palavras-chave ou propriedades pesquisáveis

Você pode aplicar automaticamente os rótulos ao conteúdo que atenda a certas condições. As condições disponíveis agora dão suporte à aplicação de um rótulo a conteúdos que incluem palavras ou frases específicas, ou valores de propriedades pesquisáveis. Você pode refinar a consulta usando os operadores de pesquisa AND, OR e NOT. 

Para saber mais sobre sintaxe de consulta, confira:

- [Referência de sintaxe da Linguagem de Consulta de Palavra-chave (KQL)](https://docs.microsoft.com/pt-BR/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

Rótulos baseados em consultas usam o índice de pesquisa para identificar conteúdos. Para saber mais sobre propriedades pesquisáveis válidas, confira:

- [Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md)
- [Visão geral de propriedades rastreadas e gerenciadas no SharePoint Server](https://docs.microsoft.com/pt-BR/SharePoint/technical-reference/crawled-and-managed-properties-overview)
  
Consultas de exemplos:

- Exchange
    - assunto:"Finanças trimestrais"
    - recipients:garthf<!--nolink-->@contoso.com

- SharePoint e OneDrive for Business
    - contenttype:contract
    - site:https<!--nolink-->: //contoso.sharepoint.com/sites/teams/procurement E contenttype:contract
  
![Editor de consultas](media/ac5b8e5e-7453-4ec7-905c-160df57298d3.png)
  
## <a name="applying-a-default-label-to-all-content-in-a-sharepoint-library-folder-or-document-set"></a>Aplicar um rótulo padrão a todo o conteúdo em uma biblioteca do SharePoint, pasta ou conjunto de documentos

Além de permitir que as pessoas apliquem um rótulo a documentos individuais, você também pode aplicar um rótulo padrão a uma biblioteca, pasta ou conjunto de documentos do SharePoint, para que todos os documentos nesse local recebam o rótulo padrão.
  
Para uma biblioteca de documentos, isso é feito na página **Configurações da biblioteca** de uma biblioteca de documentos. Ao escolher o rótulo padrão, você também pode optar por aplicá-lo a todos os itens existentes na biblioteca. 
  
Por exemplo, se tiver uma marca para materiais de marketing, e souber que uma biblioteca de documentos específica incluirá apenas esse tipo de conteúdo, você poderá tornar padrão a marca de Materiais de Marketing para todos os documentos nessa biblioteca.
  
![Aplicar a opção de rótulo na página Configurações da biblioteca](media/0787d651-63dc-43b4-8768-716a5ecc64ec.png)
  
Se você aplicar um rótulo padrão aos itens existentes na biblioteca, pasta ou conjunto de documentos:
  
- Todos os itens na biblioteca, pasta ou conjunto de documentos recebem automaticamente o mesmo rótulo, **exceto** itens que receberam um rótulo explicitamente aplicado. Itens rotulados explicitamente mantêm o rótulo existente. Para saber mais, confira a seção abaixo sobre [Os princípios de retenção ou o que tem precedência?](labels.md#principles).
    
- Se você alterar ou remover o rótulo padrão de uma biblioteca, pasta ou conjunto de documentos, ele também será alterado ou removido para todos os itens na biblioteca, pasta ou conjunto de documentos, **exceto** itens com rótulos explícitos. 
    
- Se você mover um item com um rótulo padrão de uma biblioteca, pasta ou conjunto de documentos para outra biblioteca, pasta ou conjunto de documentos, o item manterá o rótulo padrão existente, mesmo se o novo local tiver um rótulo padrão diferente.
    
## <a name="applying-a-label-to-email-by-using-rules"></a>Aplicar um rótulo ao email usando regras

No Outlook 2010 ou posterior, você pode criar regras para aplicar um rótulo ou política de retenção.
  
Por exemplo, você pode criar uma regra que aplica um rótulo específico a todas as mensagens enviadas de ou para um grupo de distribuição específico.
  
Para criar uma regra, clique com botão direito em um item \> **Regras** \> **Criar Regra** \> **Opções Avançadas** \> **Assistente de Regras** \> **aplicar política de retenção**.
  
![Assistente de regras com opção para aplicar políticas de retenção](media/eeb2407c-15b6-4224-99cf-e0a00034d8ea.png)
  
## <a name="classifying-content-without-applying-any-actions"></a>Classificação do conteúdo sem aplicar ações

Ao criar um rótulo, é possível fazer isso sem ativar qualquer retenção ou outras ações, conforme mostrado abaixo. Nesse caso, você pode usar um rótulo simplesmente como um rótulo de texto, sem aplicar ações.
  
Por exemplo, você pode criar um rótulo chamado "Revisar depois" sem ações e, em seguida, aplicar automaticamente esse rótulo ao conteúdo com tipos de informações confidenciais ou conteúdo consultado.
  
![Página de configurações de rótulo com retenção desativada](media/17ce863b-a823-426e-aaad-83718465f762.png)
  
## <a name="using-labels-for-records-management"></a>Usar rótulos para gerenciamento de registros

Em um nível alto, o gerenciamento de registros significa que:
  
- O conteúdo importante é classificado como um registro pelos usuários.
    
- Um registro não pode ser modificado ou excluído.
    
- Os registros são descartados após o término do tempo de vida declarado.
    
Use rótulos para implementar uma estratégia de gerenciamento de registros única e consistente no Office 365, quando outros recursos de gerenciamento de registros, como a Central de Registros, se aplicarem apenas ao conteúdo do SharePoint. E imponha ações de retenção em registros, para que eles sejam descartados automaticamente ao final do ciclo de vida.
  
Quando você cria um rótulo, tem a opção de usar o rótulo para classificar o conteúdo como um registro.
  
![Caixa de seleção Classificar o conteúdo como Registro](media/9c300739-d5d0-41d2-88dd-137f1cfc9cb6.png)
  
Quando um item é rotulado como registro, ocorrem quatro coisas:
  
- Não é possível excluir o item não permanentemente.
    
- Não é possível editar o item.
    
- Não é possível alterar o rótulo.
    
- Não é possível remover o rótulo.
    
### <a name="who-can-classify-content-as-a-record"></a>Quem pode classificar o conteúdo como registro

Para o conteúdo do SharePoint, qualquer usuário do grupo padrão Membros (o nível de permissão Contribuição) pode aplicar um rótulo de registro ao conteúdo. Somente o administrador do conjunto de sites pode remover ou alterar esse rótulo após a aplicação. Além disso, um rótulo que classifica o conteúdo como registro precisa ser aplicado manualmente; ele não pode ser aplicado automaticamente.
  
### <a name="records-and-folders"></a>Registros e pastas

Você pode aplicar um rótulo a uma pasta no Exchange, SharePoint ou OneDrive. Se uma pasta for rotulada como registro, e você mover um item para a pasta, o item será rotulado como registro. Quando você move o item para fora da pasta, o item continuará rotulado como registro.
  
### <a name="records-cant-be-deleted"></a>Não é possível excluir registros

Se você tentar excluir um registro no Exchange, o item será movido para a pasta Itens Recuperáveis, conforme descrito em [Como funciona uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Se você tentar excluir um registro no SharePoint, verá um erro informando que o item não foi excluído, e o item permanecerá na biblioteca.
  
![Mensagem informando que o item não foi excluído do SharePoint](media/d0020726-1593-4a96-b07c-89b275e75c49.png)
  
Se você tentar excluir um registro no OneDrive, o item será movido para a biblioteca de Retenção para Preservação, conforme descrito em [Como funciona uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Usar um rótulo como condição em uma política DLP

Um rótulo pode impor ações de **retenção** no conteúdo. Além disso, você pode usar um rótulo como uma condição em uma política DLP (prevenção contra perda de dados). Isso significa que uma política DLP pode impor ações de **proteção**, como restringir o acesso, no conteúdo que inclui um rótulo específico. 
  
Para saber mais, confira [Usar um rótulo como condição em uma política DLP](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="using-the-label-activity-explorer-and-the-data-governance-reports"></a>Usar o Explorador de Atividade de Rótulo e os relatórios de governança de dados

Após a publicação ou aplicação automática dos rótulos, convém verificar se eles estão sendo aplicados ao conteúdo da forma pretendida. Para monitorar seus rótulos, use o:
  
- **Explorador de Atividade de Rótulo**. Com o explorador (exibido abaixo), você pode pesquisar e exibir rapidamente a atividade do rótulo para todo o conteúdo no SharePoint e OneDrive for Business nos últimos 30 dias. Para saber mais, confira [Exibir a atividade do rótulo para documentos](view-label-activity-for-documents.md).
    
- **Relatórios de governança de dados**. Com esses relatórios, você pode exibir rapidamente as tendências e atividades de rótulo para todo o conteúdo no Exchange, SharePoint e OneDrive for Business nos últimos 90 dias. Para saber mais, confira [Exibir relatórios de governança de dados](view-the-data-governance-reports.md).
    
![Explorador de Atividade de Rótulo](media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="using-content-search-to-find-all-content-with-a-specific-label-applied-to-it"></a>Usar a Pesquisa de Conteúdo para localizar todo o conteúdo com um rótulo específico aplicado

Após a atribuição dos rótulos ao conteúdo, por usuários ou automaticamente, você pode usar a pesquisa de conteúdo no Centro de Conformidade &amp; Segurança para localizar todo o conteúdo classificado com um rótulo específico.
  
![Página Pesquisa de Conteúdo](media/564d5dfe-285a-4a7e-800e-907b12a1b273.png)
  
Quando você cria uma pesquisa de conteúdo, escolha a condição **Marca de Conformidade** e, em seguida, insira o nome do rótulo completo ou parte do nome do rótulo e use um caractere curinga. Para saber mais, confira [Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md).
  
![Condição de Marca de Conformidade](media/82d6af16-59f8-462f-babb-c894b2917018.png)
  
## <a name="the-principles-of-retention-or-what-takes-precedence"></a>Os princípios de retenção ou o que tem precedência?

É possível ou até mesmo provável que o conteúdo tenha várias políticas de retenção aplicadas a ele, cada uma com uma ação diferente (manter, excluir ou ambas) e o período de retenção. O que tem precedência? No nível mais alto, esteja certo de que o conteúdo retido por uma política não pode ser excluído permanentemente por outra política.
  
![Diagrama dos princípios de retenção](media/1693d6ec-b340-4805-9da3-89aa41bc6afb.png)
  
Para entender como os rótulos diferentes são aplicados ao conteúdo, lembre-se destes princípios de retenção:
  
1. **A retenção prevalece sobre a exclusão.** Suponha que uma política de retenção diga para excluir o email do Exchange após três anos, mas outra diga para manter o email do Exchange por cinco anos e depois excluí-lo. Qualquer conteúdo que tiver três anos será excluído e ocultado dos usuários, mas ainda será mantido na pasta Itens Recuperáveis até que o conteúdo atinja cinco anos, quando ele será permanentemente excluído. 
    
2. **O período de retenção mais longo prevalece.** Se o conteúdo estiver sujeito a várias políticas que retêm o conteúdo, ele será mantido até o final do período de retenção mais longo. 
    
3. **A inclusão explícita prevalece sobre a inclusão implícita.** Isso significa que: 
    
    1. Se um rótulo com configurações de retenção for atribuído manualmente por um usuário a um item, como um email do Exchange ou um documento do OneDrive, esse rótulo terá precedência sobre uma política atribuída no nível do site ou caixa de correio e um rótulo padrão atribuído pela biblioteca de documentos. Por exemplo, se o rótulo explícito disser para manter por dez anos, mas a política atribuída ao site disser para manter por apenas cinco anos, o rótulo terá precedência. Observe que os rótulos de aplicação automática são considerados implícitos, não explícitos, pois são aplicados automaticamente pelo Office 365.
    
    2. Se uma política de retenção incluir um local específico, como a caixa de correio de um usuário específico ou conta OneDrive for Business, essa política terá precedência sobre outra política de retenção que se aplica a caixas de correio de todos os usuários ou contas do OneDrive for Business, mas não incluirá especificamente essa caixa de correio do usuário.
    
4. **O período de exclusão mais curto tem precedência.** Da mesma forma, se o conteúdo estiver sujeito a várias políticas que excluem o conteúdo (sem retenção), ele será excluído ao fim do período de retenção mais curto. 
    
Entenda que os princípios de retenção funcionam como um fluxo de desempate de cima para baixo: se as regras aplicadas por todas as políticas ou rótulos forem as mesmas em um nível, o fluxo se moverá para baixo até o próximo nível para determinar a precedência para a qual a regra será aplicada.
  
Por fim, uma política de retenção ou rótulo não pode excluir permanentemente qualquer conteúdo que esteja retido para Descoberta Eletrônica. Quando a retenção for liberada, o conteúdo estará novamente qualificado para o processo de limpeza descrito acima.
  
## <a name="use-labels-instead-of-these-features"></a>Usar rótulos em vez destes recursos

Os rótulos podem ser disponibilizados facilmente para uma organização inteira e seu conteúdo no Office 365, incluindo Exchange, SharePoint, OneDrive e grupos do Office 365. Se você precisar classificar o conteúdo ou gerenciar registros em qualquer lugar no Office 365, recomendamos o uso de rótulos.
  
Vários outros recursos eram usados anteriormente para classificar o conteúdo ou gerenciar registros no Office 365. Confira-os abaixo. Esses recursos continuarão funcionando paralelamente aos rótulos criados no Centro de Conformidade &amp; Segurança. Observe que, embora haja instâncias nas quais a implementação de rótulos difere dos recursos anteriores, a evolução dos rótulos conduzirá o futuro do gerenciamento de registros no Office 365. Portanto, a partir de agora, para governança de dados, recomendamos o uso de rótulos em vez desses recursos.
  
### <a name="exchange-online"></a>Exchange Online

- [Marcas de retenção e políticas de retenção](https://go.microsoft.com/fwlink/?linkid=846125), também conhecidas como [gerenciamento de registros de mensagens (MRM)](https://go.microsoft.com/fwlink/?linkid=846126) (apenas exclusão) 
    
### <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online e OneDrive for Business

- [Como configurar o gerenciamento de registros no local](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (retenção) 
    
- [Introdução à Central de Registros](https://support.office.com/article/bae6ca5a-7b19-40e0-b433-e3613a747c2c) (Retenção) 
    
- [Políticas de gerenciamento de informações](intro-to-info-mgmt-policies.md) (apenas exclusão) 
    
## <a name="permissions"></a>Permissões

Os membros da equipe de conformidade que criarão rótulos precisam de permissões para o &amp; Centro de Conformidade e Segurança. Por padrão, o administrador de locatário terá acesso a esse local e pode dar acesso a outras pessoas e aos responsáveis pela conformidade ao &amp; Centro de Conformidade e Segurança, sem lhes dar todas as permissões de um administrador de locatários Para fazer isso, recomendamos que você acesse a página **Permissões** do &amp; Centro de Conformidade e Segurança, edite o grupo de função **Administrador de Conformidade** e adicione membros a esse grupo de função. 
  
Para saber mais, consulte [Dê aos usuários acesso ao Centro de Conformidade e Segurança&amp; do Office 365](grant-access-to-the-security-and-compliance-center.md).
  
Essas permissões só serão necessárias para criar e aplicar rótulos. A imposição da política não exige acesso ao conteúdo.
  
## <a name="find-the-powershell-cmdlets-for-labels"></a>Encontrar os cmdlets do PowerShell para rótulos

Para usar cmdlets de rótulo, você precisa:
  
1. [Conectar ao &amp;Centro de Conformidade e Segurança do Office 365 usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Use esses [cmdlets do &amp;Centro de Conformidade e Segurança do Office 365](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
## <a name="more-information"></a>Mais informações

- [Visão geral de políticas de retenção](retention-policies.md)
    

