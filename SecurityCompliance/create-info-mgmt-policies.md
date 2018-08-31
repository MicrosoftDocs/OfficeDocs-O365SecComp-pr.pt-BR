---
title: Criar e aplicar políticas de gerenciamento de informações
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
description: Políticas de gerenciamento de informações permitem que sua organização para controlar quanto tempo reter conteúdo, o que as pessoas que fazer com o conteúdo de auditoria e adicionar códigos de barras ou rótulos aos documentos. Uma política pode ajudar a impor a conformidade com normas legais e governamentais ou processos de negócios internos. Como administrador, você pode configurar uma política para controlar como controlar documentos e quanto tempo reter os documentos.
ms.openlocfilehash: cc15b7d830e6c13e00045f7e4b672ac4a755a70e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523741"
---
# <a name="create-and-apply-information-management-policies"></a>Criar e aplicar políticas de gerenciamento de informações

Políticas de gerenciamento de informações permitem que sua organização para controlar quanto tempo reter conteúdo, o que as pessoas que fazer com o conteúdo de auditoria e adicionar códigos de barras ou rótulos aos documentos. Uma política pode ajudar a impor a conformidade com normas legais e governamentais ou processos de negócios internos. Como administrador, você pode configurar uma política para controlar como controlar documentos e quanto tempo reter os documentos.
  
É possível criar uma can de política de gerenciamento de informações em três locais diferentes na hierarquia de sites, sejam o mais amplo para o mais estreita:
  
- Crie uma política para usar em vários tipos de conteúdo dentro de um conjunto de sites.
    
- Crie uma política para um tipo de conteúdo do site.
    
- Crie uma política para uma lista ou biblioteca.
    
Para obter mais informações, consulte [Introdução às diretivas de gerenciamento de informações](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Criar uma política para vários tipos de conteúdo dentro de um conjunto de sites
<a name="__toc261001590"> </a>

Para garantir que uma política de informações é aplicada a todos os documentos de um determinado tipo em um conjunto de sites, considere a criação da política no nível do conjunto de sites e depois aplicar a política para tipos de conteúdo. Elas são referidas como políticas de conjunto de sites. 
  
1. Na home page do conjunto de sites \> **configurações**![botão Configurações de 2016 do SharePoint, na barra de título. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Configurações do site**.
    
    Em um site conectado por grupo do SharePoint, clique em **configurações**, clique em **Conteúdo do Site**e clique em **Configurações do Site**. 
    
2. Na página Configurações do Site, em **Administração do conjunto de sites** \> **Modelos de política de tipo de conteúdo**. 
  
![Link de modelo de política de tipo de conteúdo na página Configurações do Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Na página diretivas \> **criar**. 
    
4. Insira um nome e descrição para a política e, em seguida, escrever uma declaração de política breve que explica aos usuários, o que é a política por.
    
5. Consulte a próxima seção sobre a criação de políticas para um tipo de conteúdo de site saber como configurar os recursos que você deseja associar a política. 
    
6. Selecione **OK**.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Criar uma política para um tipo de conteúdo de site
<a name="__create_a_policy"> </a>

Adicionando uma política de gerenciamento de informações a um tipo de conteúdo facilita associar recursos de política com várias listas ou bibliotecas. Você pode optar por adicionar uma política de gerenciamento de informações existente a um tipo de conteúdo ou criar uma diretiva exclusiva específica para um tipo de conteúdo individual.
  
 Você também pode adicionar uma política de gerenciamento de informações a um tipo de conteúdo que é específico para listas. Isso tem o efeito de aplicar a diretiva apenas aos itens nessa lista que estão usando o tipo de conteúdo. 
  
1. Na home page do conjunto de sites \> **configurações**![botão Configurações de 2016 do SharePoint, na barra de título. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Configurações do site**.
    
    Em um site conectado por grupo do SharePoint, clique em **configurações**, clique em **Conteúdo do Site**e clique em **Configurações do Site**. 
    
2. Na página Configurações do Site, em **Galerias de Web Designer** \> **tipos de conteúdo de Site**.
  
![Link de tipos de conteúdo de site na página Configurações do Site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. Na página Configurações de tipo de conteúdo do Site, selecione o tipo de conteúdo que você deseja adicionar uma política para.
    
4. Na página tipo de conteúdo do Site, em **configurações** \> **configurações de política de gerenciamento de informações**.
    
5. Na página Editar política, digite um nome e descrição para a política e, em seguida, escreva uma breve descrição que explica a usuários, o que é a política por.
    
6. Nas próximas seções, selecione os recursos de diretiva individuais que você deseja adicionar à sua política de gerenciamento de informações. 
  
![Tipos de políticas de conteúdo](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Para especificar um período de retenção para documentos e itens que estão sujeitos a essa política, escolha **Habilitar retenção**e, em seguida, especifique o período de retenção e as ações que você deseja que ocorra quando os itens expiram.
    
    Para especificar um período de retenção
    
||||||**1.**|* * Escolha * * adicione um estágio de retenção de registros … * * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Selecione uma opção de período de retenção para especificar quando os documentos ou itens estão definidos para expirar. Siga um destes procedimentos:<br/>  Para definir a data de validade com base em uma propriedade de data, sob o **evento** \> **esse estágio é baseado em uma propriedade de data no item**e selecione a ação de documento ou item (por exemplo, criado ou modificado) e o incremento de tempo depois (essa ação Por exemplo, o número de dias, meses ou anos) quando quiser que o item para expirar.  <br/>  Para usar uma fórmula de retenção personalizada para determinar a expiração, escolha **definido por uma fórmula de retenção personalizada instalada neste servidor**.  <br/> > [!NOTE]> Essa opção só estará disponível se uma fórmula personalizada foi configurada pelo administrador.           |
||||||3.  <br/> |A opção de **Iniciar um fluxo de trabalho** está disponível somente se você estiver definindo uma política para uma lista, biblioteca ou tipo de conteúdo que já tenha um fluxo de trabalho associado a ela. Você terá uma opção de fluxos de trabalho à sua escolha.<br/> |
||||||4.  <br/> |Na seção de **Recorrência** , selecione **Repetir a ação deste estágio …** e insira a frequência desejada para a ação a ocorrer novamente.  <br/> > [!NOTE]> Essa opção só estará disponível se a ação que você selecionou pode ser repetida. Por exemplo, você não pode definir a recorrência para a ação **Excluir permanentemente**.           |
||||||5.  <br/> |Escolher **Okey**.  <br/> |
   
1. Para habilitar a auditoria para os documentos e itens que estão sujeitos a essa política, escolha **Habilitar auditoria**e, em seguida, especifique os eventos que você deseja fazer auditoria.
    
    Para habilitar a auditoria
    
||||||1.* * *|Na página Editar política, * * **em** **auditoria** **\>** **Habilitar auditoria** * *, e selecione as caixas de seleção ao lado dos eventos que você deseja manter uma auditoria rastros for.* * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Para solicitar aos usuários para inserir esses códigos de barras em documentos,** **Escolha** **Avisa aos usuários para inserir um código de barras antes de salvar ou imprimir** **.** <br/> |
||||||**3.** <br/> |**Escolha** **Okey** * * para aplicar o recurso de auditoria para a política. ** <br/> |
|||||||O recurso de política de auditoria permite que as organizações a criar e analisar trilhas de auditoria para documentos e itens de lista, como listas de tarefas, listas de problemas, grupos de discussão e calendários. Esse recurso de diretiva fornece um arquivo de log de auditoria que registra eventos, como quando conteúdo é exibido, editado ou excluído.  <br/> |
|||||||Quando a auditoria está habilitada como parte de uma política de gerenciamento de informações, os administradores podem exibir os dados de auditoria em relatórios de uso de política que são baseados no Microsoft Excel e que resumir uso atual. Os administradores podem usar esses relatórios para determinar como as informações está sendo usadas dentro da organização. Esses relatórios também podem ajudar as organizações para verificar e documentar sua conformidade a normas ou investigar possíveis preocupações.  <br/> |
|||||||O log de auditoria registra as seguintes informações: nome do evento, data e hora do evento e nome do sistema do usuário que executou a ação.  <br/> |
   
1. Quando códigos de barras são ativados como parte de uma política, eles são adicionados às propriedades do documento e exibidos na área de cabeçalho do documento ao qual o código de barras é aplicado. Como rótulos, códigos de barras podem também ser removidos manualmente de um documento. Você pode especificar se os usuários devem receber uma solicitação para incluir o código de barras ao imprimir ou salvar um item ou se o código de barras deve ser inserido manualmente usando a guia **Inserir** no 2010 Office release programas. 
    
    Para habilitar códigos de barras
    
||||||1.* * *|**Na página Editar política, em **códigos de barras** \> **Habilitar códigos de barras**.**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Para solicitar que os usuários insiram esses códigos nos documentos, escolha **avisa aos usuários para inserir um código de barras antes de salvar ou imprimir**.  <br/> |
||||||**3.** <br/> |Escolha **Okey** para aplicar o recurso de código de barras à diretiva.  <br/> |
|||||||
 A política de código de barras gera código 39 standard códigos de barras. Cada imagem de código de barras inclui o texto abaixo do símbolo de código de barras que representa o valor de código de barras. Isso permite que os dados de código de barras a ser usado, mesmo quando a verificação de hardware não está disponível. Os usuários podem digitar manualmente o número de código de barras na caixa Pesquisar para localizar o item em um site.  <br/> |
   
1. Para exigir que os documentos que estão sujeitos a essa política têm rótulos, escolha **Habilitar rótulos**e, em seguida, especifique as configurações que você deseja para os rótulos.
    
    Para habilitar os rótulos
    
||||||**1.**|* * Para exigir que os usuários adicionem um rótulo a um documento, escolha **avisa aos usuários para inserir um rótulo antes de salvar ou imprimir**.  <br/> > [!NOTE]> Se desejar que os rótulos sejam opcionais, não marque essa caixa de seleção.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Para bloquear um rótulo, de modo que ele não pode ser alterado após ele ter sido inserido, escolha **impedir alterações aos rótulos depois de adicionados**.  <br/>  Essa configuração impede que o texto do rótulo atualizando depois que o rótulo foi inserido em um item em um aplicativo cliente, como Word, PowerPoint ou Excel. Se desejar que o rótulo de ser atualizados quando as propriedades desse documento ou item são atualizadas, não marque essa caixa de seleção.<br/> |
||||||3.  <br/> |Na caixa formato de rótulo, insira o texto do rótulo de como você deseja exibi-lo. Rótulos podem conter até 10 referências de coluna, cada um deles pode ter até 255 caracteres. Para criar o formato para seu rótulo, faça o seguinte:  <br/> Digite os nomes das colunas que você deseja incluir no rótulo na ordem na qual você deseja que apareçam. Coloque os nomes de coluna entre chaves ({}), conforme mostrado no exemplo na página Editar política.  <br/> Digite palavras para identificar as colunas fora dos colchetes, conforme mostrado no exemplo na página Editar política.  <br/> |
||||||4.  <br/> |Para adicionar uma quebra de linha, insira **\n.** onde deseja que a quebra de linha apareça.  <br/> |
||||||5.  <br/> |Selecione o tamanho da fonte e o estilo que você deseja e especifique se deseja que o rótulo posicionado à esquerda, centro ou direita dentro do documento.  <br/>  Selecione uma fonte e o estilo que estão disponíveis nos computadores dos usuários. O tamanho da fonte afeta a quantidade de texto pode ser exibida no rótulo.  <br/> |
||||||6.  <br/> |Insira a altura e a largura do rótulo. Altura do rótulo pode variar de 25 polegadas em 20 polegadas e largura do rótulo pode variar de 25 polegadas em 20 polegadas. Texto do rótulo é centralizado sempre verticalmente dentro da image do rótulo.  <br/> |
||||||7.  <br/> |Escolha **Atualizar** para visualizar o conteúdo do rótulo.  <br/> |
   
1. Selecione **OK**.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Criar uma política para uma lista, biblioteca ou pasta (política de retenção com base em local)
<a name="__create_a_policy"> </a>

Você pode definir uma política de retenção se aplica somente a uma lista específica, biblioteca ou pasta. No entanto, se você criar uma política de retenção dessa maneira, você não pode reutilizar essa diretiva em outras listas, bibliotecas, pastas ou em sites e você não pode aplicar uma política de conjunto de sites para uma política de local com base.
  
Se você deseja aplicar uma única política de retenção a todos os tipos de conteúdo em um único local, provavelmente você desejará usar retenção baseada no local. Na maioria dos casos, convém Verifique se uma política de retenção é especificada para todos os tipos de conteúdo.
  
 Cada subpasta herda a política de retenção de seu pai, a menos que você optar por interromper a herança e definir uma nova política de retenção no nível filho. 
  
Se você deseja definir uma política de gerenciamento de informações que não seja de retenção a uma lista ou biblioteca, você precisará definir uma política de gerenciamento de informações para cada tipo de conteúdo de lista individuais associado a essa lista ou biblioteca.
  
 Se a qualquer momento que você decide mudar de tipo de conteúdo para diretivas baseadas no local para uma lista ou biblioteca, apenas a política de retenção será usada como a diretiva de local. Todas as outras políticas de gerenciamento (auditorias, códigos de barras e códigos de barras) serão herdadas dos tipos de conteúdo associados. 
  
 Políticas de local com base podem ser desabilitadas para um conjunto de sites ao desativar o recurso retenção baseada em pasta e de biblioteca. Isso permite que os administradores do conjunto de sites garantir que suas políticas de tipo de conteúdo não são substituídas pelas políticas de local com base de um administrador lista. 
  
Você precisa pelo menos a permissão Gerenciar listas para alterar as configurações de política de gerenciamento de informações para uma lista ou biblioteca.
  
1. Navegue até a lista ou biblioteca para a qual você deseja especificar uma política de gerenciamento de informações. 
    
2. Na faixa de opções, escolha a guia **biblioteca** ou **lista** \> **As configurações de biblioteca** ou **Lista**.
    
    No SharePoint Online, clique em **configurações** e clique em **definições da lista** ou **definições da biblioteca**. 
    
3. Em **permissões e gerenciamento** \> **configurações de política de gerenciamento de informações**.
  
![Link de políticas de gerenciamento de informações na página de configurações de biblioteca de documentos](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Na página Configurações de política de gerenciamento de informações, certifique-se de que a origem da retenção para a lista ou biblioteca está definida como biblioteca e pastas. 
  
Se o **Tipo de conteúdo** é exibida como a fonte, clique em **Alterar fonte**e, em seguida, clique em **biblioteca e pastas**. Você é alertado que as políticas de retenção de tipo de conteúdo serão ignoradas. Escolha **Okey**. 
    
5. Na página Editar política, em um **Agendamento de retenção com base da biblioteca**, insira uma breve descrição para a política que você está criando. 
    
6. Escolha **Adicionar um estágio de retenção …**
    
     Observe que em registros, você pode optar por definir políticas de retenção diferente para registros selecionando os estágios de retenção diferente de definir opção de registros. 
    
7. Na caixa de diálogo Propriedades estágio, selecione uma opção de período de retenção para especificar quando os documentos ou itens estiver configuradas para expirar. Siga um destes procedimentos:
    
  - Para definir a data de validade com base em uma propriedade de data, sob o **evento** \> **esse estágio é baseado em uma propriedade de data no item**e selecione a ação de documento ou item (por exemplo, criado ou modificado) e o incremento de tempo depois (essa ação Por exemplo, o número de dias, meses ou anos) quando quiser que o item para expirar. 
    
  - Para usar uma fórmula de retenção personalizada para determinar a expiração, escolha **definido por uma fórmula de retenção personalizada instalada neste servidor**. 
    
    > [!NOTE]
    >  Essa opção só estará disponível se uma fórmula personalizada foi configurada pelo administrador. 
  
  - Em **ação**, especifique o que você deseja que aconteça quando o documento ou item expira. Para habilitar uma ação específica ocorra para o documento ou item (por exemplo, exclusão), selecione uma ação na lista. 
    
8. A opção de **Iniciar um fluxo de trabalho** está disponível somente se você estiver definindo uma política para uma lista, biblioteca ou tipo de conteúdo que já tenha um fluxo de trabalho associado a ela. Você terá uma opção de fluxos de trabalho à sua escolha. 
    
9. Em **Recorrência**, escolha **Repita a ação deste estágio …** e insira a frequência desejada para a ação a ocorrer novamente. 
    
    > [!NOTE]
    >  Essa opção só estará disponível se a ação que você selecionou pode ser repetida. Por exemplo, você não pode definir a recorrência para a ação **Excluir permanentemente**. 
  
10. Selecione **OK**.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Aplicar uma política de conjunto de sites a um tipo de conteúdo
<a name="__apply_a_site"> </a>

Se as políticas de gerenciamento de informações já tiverem sido criadas para o seu site, como políticas de conjunto de sites, você pode aplicar uma das políticas a um tipo de conteúdo. Ao fazer isso, você pode aplicar a mesma diretiva a vários tipos de conteúdo em um conjunto de sites que não compartilham o mesmo tipo de conteúdo pai.
  
 Se você deseja aplicar políticas para vários tipos de conteúdo em um conjunto de sites e você tiver configurado um serviço de metadados gerenciados, você pode usar o tipo de conteúdo de publicação para publicar o check-out políticas de gerenciamento de informações para vários conjuntos de sites. Consulte a seção [Aplicar uma política para tipos de conteúdo entre conjuntos de sites](create-info-mgmt-policies.md#__apply_a_policy) para obter mais informações. 
  
1. Navegue até a lista ou biblioteca que contém o tipo de conteúdo ao qual você deseja aplicar uma política.
    
2. Na faixa de opções, escolha a guia **biblioteca** ou **lista** \> **As configurações de biblioteca** ou **Lista**.
    
    No SharePoint Online, clique em **configurações** e clique em **definições da lista** ou **definições da biblioteca**. 
    
3. Em **permissões e gerenciamento** \> **configurações de política de gerenciamento de informações**.
  
![Link de políticas de gerenciamento de informações na página de configurações de biblioteca de documentos](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Verifica se a origem da diretiva está definida para **Tipos de conteúdo**e em **Políticas de tipo de conteúdo** , selecione o tipo de conteúdo que você deseja aplicar a política. 
    
5. Em **Especifique a política** \> **usar uma política de conjunto de sites**e selecione a política que você deseja aplicar da lista. 
    
    > [!NOTE]
    >  Se a opção **usar uma política de conjunto de sites** não estiver disponível, nenhuma política de conjunto de sites tiverem sido definida para o conjunto de sites. 
  
6. Selecione **OK**.
    
     Se a lista ou biblioteca que você estiver trabalhando com suporta o gerenciamento de vários tipos de conteúdo, em **Tipos de conteúdo** , você pode escolher o tipo de conteúdo para o qual você deseja especificar uma política de gerenciamento de informações. Você será levado diretamente para a etapa 5 acima. 
    
## <a name="apply-a-policy-across-site-collections"></a>Aplicar uma política entre conjuntos de sites
<a name="__toc260646789"> </a>

Compartilhar tipos de conteúdo entre conjuntos de sites, usando um aplicativo de serviço de metadados gerenciados para configurar a publicação de tipo de conteúdo. Publicação de tipo de conteúdo ajuda a gerenciar conteúdo e metadados consistentemente entre seus sites porque os tipos de conteúdo podem ser criados e atualizados centralmente e atualizações podem ser publicadas check-out em vários conjuntos de sites inscritos ou aplicativos da Web.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Criar um modelo de uma política existente para usar nos conjuntos de sites
<a name="__toc262125409"> </a>

Você pode definir uma política de gerenciamento de informações e, em seguida, criar um modelo de-la para utilizar conforme necessário entre vários conjuntos de sites. Este método pode ser usado se você quiser ter um backup de suas políticas de informações ou também pode ser usado como um método alternativo ao uso de publicação de tipo de conteúdo para a aplicação de uma política entre conjuntos de sites. Você cria um modelo ou o backup da diretiva de exportação a política de um conjunto de sites e importá-lo para um local salvo ou para outro conjunto de sites.
  
> [!IMPORTANT]
>  Se estiver usando a exportação e importação de recursos como uma maneira de fazer um conjunto de modelos de política, tenha em mente que existe de um identificador exclusivo do arquivo. XML de política. Dessa forma, você não pode importar essa diretiva para um site mais de uma vez sem alterar este identificador exclusivo. 
  
### <a name="export-a-policy"></a>Exportar uma política
<a name="__toc260646790"> </a>

1. Na home page do conjunto de sites, escolha **configurações**![engrenagem pequenas configurações que ocorreu das configurações do Site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Configurações do site**.
    
    Em um site conectado por grupo do SharePoint, clique em **configurações**, clique em **Conteúdo do Site**e clique em **Configurações do Site**. 
    
2. Na página Configurações do Site, em **Administração do conjunto de sites** \> **Modelos de política de tipo de conteúdo**. 
  
![Link de modelo de política de tipo de conteúdo na página Configurações do Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Escolha a política que você deseja exportar \> rolagem na parte inferior \> **Exportar**.
    
4. No prompt de salvar ou abrir o arquivo, escolha **Salvar**e selecione um local para salvar o arquivo. Certifique-se de selecionar um local que está disponível para os conjuntos de sites que estiver importando a política.
    
5. Quando a caixa de diálogo Download concluído for exibida, escolha **Fechar**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Importar uma política para um conjunto de sites diferentes
<a name="__toc260646791"> </a>

Importar uma política de gerenciamento de informações permite aplicá-la a vários tipos de conteúdo no nível de site ou lista dentro de qualquer conjunto de sites especificado. Os benefícios de se fazer isso são dois: não é necessário definir novamente e aplicar a política em cada tipo de conteúdo, e você pode gerenciar mais facilmente modificações de política, fazendo as alterações a política em apenas um local.
  
1. Na home page do conjunto de sites ao qual você deseja aplicar a política, escolha **configurações**![engrenagem pequenas configurações que ocorreu das configurações do Site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Configurações do site**.
    
    Em um site conectado por grupo do SharePoint, clique em **configurações**, clique em **Conteúdo do Site**e clique em **Configurações do Site**. 
    
2. Na página Configurações do Site, em **Administração do conjunto de sites** \> **Modelos de política de tipo de conteúdo**.
    
3. Na página diretivas \> **importação** \> **Procurar** para localizar o arquivo XML para a política. 
    
4. Selecione o arquivo XML no qual a política tiver sido salvo \> **Open**. 
    
5. Na página Importar uma política de conjunto de sites de página \> **importação** para adicionar a política ao conjunto de sites. 
    
Sua política importada agora pode ser aplicada a um ou vários tipos de conteúdo no nível do site ou lista. 
  
[Políticas de gerenciamento de informações permitem que sua organização para controlar quanto tempo reter conteúdo, o que as pessoas que fazer com o conteúdo de auditoria e adicionar códigos de barras ou rótulos aos documentos. Uma política pode ajudar a impor a conformidade com normas legais e governamentais ou processos de negócios internos. Como administrador, você pode configurar uma política para controlar como controlar documentos e quanto tempo reter os documentos. É possível criar uma can de política de gerenciamento de informações em três locais diferentes na hierarquia de sites, sejam o mais amplo para o mais estreita: criar uma política para usar em vários tipos de conteúdo dentro de um conjunto de sites. Crie uma política para um tipo de conteúdo do site. Crie uma política para uma lista ou biblioteca. Para obter mais informações, consulte Introdução a políticas de gerenciamento de informações.](create-info-mgmt-policies.md#__top)
  

