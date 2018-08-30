---
title: Configurar políticas de supervisão da sua organização
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Configure um diretivas de supervisão de revisão para capturar comunicações de funcionários para revisão.
ms.openlocfilehash: a919d65f5c0967a44ac12b7e02d477dac2113704
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524732"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurar políticas de supervisão da sua organização

Use diretivas de supervisão para capturar comunicações de funcionários para exame por revisores internos ou externos.
  
> [!NOTE]
> Usando diretivas de supervisão requer uma assinatura do Office 365 E5 para sua organização. Se você não tiver que plano e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Siga estas etapas para configurar e usar supervisão em sua organização do Office 365: 
  
- [Configurar grupos de supervisão](configure-supervision-policies.md#exampledist)
    
    Antes de começar a usar supervisão, determine quem serão suas comunicações revisou e quem executará as revisões. Se você deseja começar com apenas alguns usuários para ver como funciona a supervisão, você pode ignorar a configuração grupos por enquanto.
    
- [Disponibilizar supervisão em sua organização](configure-supervision-policies.md#SRavailable)
    
    Adicione si mesmo ao grupo de funções de análise de supervisão, portanto, você pode configurar políticas. Qualquer pessoa que tenha essa função atribuída pode acessar a página de **supervisão** sob um **Governança de dados** na segurança &amp; Centro de conformidade. 
    
- [Definir uma política de supervisão](configure-supervision-policies.md#setupsuper)
    
    Você vai criar diretivas de supervisão na segurança &amp; Centro de conformidade. Essas diretivas definem quais comunicações estão sujeitos a revisão na sua organização e especifica que deve executar as revisões. Comunicações incluem email, bem como as comunicações de plataforma de terceiros 3rd (por exemplo, Facebook, Twitter, etc.)
    
- [Usar o Outlook web app para analisar identificadas por uma política de supervisão de comunicações](configure-supervision-policies.md#UseOutlook)
    
    O suplemento de supervisão oferece revisores acesso à funcionalidade de supervisão direita dentro do Outlook web app para que eles possam avaliar e categorizar cada item. Suporte para a versão da área de trabalho do Outlook disponíveis em breve.
    
- **Executar o relatório de supervisão**
    
    Use os relatórios de supervisão para ver a atividade de revisão no nível de política e revisor. Para cada diretiva, você também pode exibir live estatísticas sobre o estado atual da atividade de revisão. Para obter detalhes, consulte [relatórios de supervisão](supervision-reports.md).
    
## <a name="set-up-groups-for-supervision"></a>Configurar grupos de supervisão
<a name="exampledist"> </a>

 Quando você cria uma diretiva de supervisão, você determinará que terão suas comunicações analisadas e quem executará as revisões. Na política, você usará endereços de email para identificar indivíduos ou grupos de pessoas. Para simplificar sua instalação, crie grupos para as pessoas que terão sua comunicação analisada e grupos para as pessoas que analisará essas comunicações. Se você estiver usando grupos, talvez seja necessário várias — por exemplo, se você deseja monitorar as comunicações entre os dois grupos distintos de pessoas, ou se você deseja especificar um grupo que não vai ser supervisionados. Consulte [grupos de distribuição de exemplo](configure-supervision-policies.md#GroupExample) para obter detalhes sobre como isso funciona. 
  
Para comunicações entre ou dentro de grupos na sua organização for o Supervisor, configurar os grupos de distribuição no Centro de administração do Exchange (vá em **destinatários** \> **grupos**). Para obter mais informações sobre como configurar grupos de distribuição, consulte [Gerenciar grupos de distribuição](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Você também pode usar grupos dinâmicos de distribuição ou grupos de segurança para supervisão se você preferir. Para ajudá-lo a decidir se essas se ajuste melhor sua organização precisa, consulte [Gerenciar grupos de segurança habilitados para email](http://go.microsoft.com/fwlink/?LinkId=627033)e [Gerenciar grupos de distribuição dinâmica](http://go.microsoft.com/fwlink/?LinkId=627058). 
  
### <a name="example-distribution-groups"></a>Exemplos de grupos de distribuição
<a name="GroupExample"> </a>

Este exemplo inclui um grupo de distribuição que foi configurado para uma organização financeira chamada internacional financeiro da Contoso. 
  
Na Contoso Financial International, uma amostra das comunicações entre agentes nos Estados Unidos deve ser supervisionada. No entanto, os agentes de conformidade dentro desse grupo não exigem supervisão. Neste exemplo, podemos criar os seguintes grupos:
  
|**Configurar esse grupo de distribuição**|**Endereço do grupo (alias)**|**Descrição**|
|:-----|:-----|:-----|
|Todos os agentes dos EUA  <br/> |US_Brokers@contoso.com  <br/> |Esse grupo inclui endereços de email para todos os agentes dos EUA que trabalham para a Contoso.  <br/> |
|Todos os agentes de conformidade dos EUA  <br/> |US_Compliance@contoso.com  <br/> |Esse grupo inclui os endereços de email para todos os oficiais de conformidade com base nos EUA que trabalham para Contoso. Como este grupo é um subconjunto de todos os agentes baseada nos EUA, você pode usar este alias para responsáveis pela conformidade isentos de uma política de supervisão.  <br/> |
   
A seção [Configurar uma política de supervisão](configure-supervision-policies.md#setupsuper) descreve como você pode usar esses grupos ao configurar a política. 
  
## <a name="make-supervision-available-in-your-organization"></a>Disponibilizar supervisão em sua organização
<a name="SRavailable"> </a>

Para disponibilizar **supervisão** como uma opção de menu na segurança &amp; Centro de conformidade, você deve ser atribuído a função de administrador de revisão de supervisão. 
  
Para fazer isso, você pode adicionar si mesmo como membro do grupo de função da análise de supervisão, ou você pode criar um novo grupo de função.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Adicionar membros ao grupo de funções de análise de supervisão

1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365. 
    
2. Na segurança &amp; Centro de conformidade, vá para **permissões**.
    
3. Selecione o grupo de funções de **Análise de supervisão** e, em seguida, clique no ícone Editar. 
    
4. Na seção **membros** , adicione as pessoas que você deseja gerenciar supervisão para sua organização. 
    
### <a name="create-a-new-role-group"></a>Criar um novo grupo de função

1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365. 
    
2. Na segurança &amp; Centro de conformidade, vá para **permissões** e clique em Adicionar ( **+**).
    
3. Na seção **funções** , clique em Adicionar ( **+**) e role para baixo até **Administrador supervisão de revisão**. Adicione essa função ao grupo de funções.
    
4. Na seção **membros** , adicione as pessoas que você deseja gerenciar supervisão para sua organização. 
    
Para obter mais informações sobre grupos de funções e permissões, consulte [permissões no Office 365 Security &amp; Centro de conformidade ](permissions-in-the-security-and-compliance-center.md).
  
## <a name="set-up-a-supervision-policy"></a>Definir uma política de supervisão
<a name="setupsuper"> </a>

> [!IMPORTANT]
> Antes de criar uma política de supervisão, você deve primeiro remover quaisquer políticas existentes da análise de supervisão. 
  
1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365. 
    
2. Na segurança &amp; Centro de conformidade, vá para o clique **governança de dados** \> **supervisão**.
    
    > [!NOTE]
    > A versão anterior do recurso pode mostrar no painel de navegação esquerdo como **análise de supervisão (retirada em breve)**. Esta versão em breve será preterida e removida. A nova versão chamada **supervisão** levarão seu lugar. 
  
3. Clique em **criar** e, em seguida, siga o Assistente para configurar as seguintes páginas da política. 
    
### <a name="policy-name-and-description"></a>Nome e descrição da política.

Insira um nome e uma descrição para a diretiva. Para fins de exemplo, chamaremos a política de Contoso conosco agentes.
  
### <a name="choose-users-to-supervise"></a>Escolha os usuários for o Supervisor

- Na caixa **Supervise estes usuários ou grupos** , escolha os usuários ou grupos cuja comunicação quiser for o Supervisor. Projetando-se com o nosso exemplo para Contoso conosco agentes, iremos escolher o grupo US_Brokers@Contoso.com aqui. 
    
- Se você escolher um grupo para for o Supervisor, você pode usar a caixa **excluir esses usuários** para escolher os membros do grupo que são isentos de supervisão. Usando o exemplo, podemos vai excluir o grupo US_Compliance@Contoso.com aqui. 
    
### <a name="choose-communications-to-review"></a>Escolha as comunicações para revisar
<a name="CommsToReview"> </a>

Por padrão, a condição de **direção é** é exibida e não pode ser removida. Se desejar fazer o escopo da revisão (por exemplo, apenas revisar o conteúdo que contenha certas palavras ou frases), clique em **Adicionar uma condição**. Você pode especificar várias condições, se necessário.
  
As condições que você escolher serão aplicadas à comunicação de fontes de email e de terceiros 3rd em sua organização (como do Facebook ou pasta de recados). Para obter detalhes sobre como importar 3rd terceiros communications para sua organização do Office 365, consulte [arquivamento dados de terceiros no Office 365](https://technet.microsoft.com/EN-US/library/mt621583.aspx).
  
A tabela a seguir explica mais sobre cada condição.
  
|**Condição**|**Como usar essa condição**|
|:-----|:-----|
|Direção é  <br/> |Escolha a **entrada** para examinar comunicações que são enviadas **para** as pessoas que você escolher for o Supervisor **de** pessoas não incluídas na política.  <br/> Escolha a **saída** se desejar examinar as comunicações são enviadas **das** pessoas que você escolher for o Supervisor * * para * * pessoas não incluídas na política.  <br/> Escolha **Internal** para analisar comunicações enviadas **entre** as pessoas que você identificou na política.  <br/> |
|Mensagem contém qualquer uma destas palavras  <br/> Mensagem contém nenhuma dessas palavras  <br/> |Para aplicar a política quando determinadas palavras ou frases são incluídas ou excluídas em uma mensagem, insira cada palavra ou frase em uma linha separada. Cada linha de palavras inseridas será aplicada separadamente (apenas um dessas linhas deve aplicar para a política seja aplicada à mensagem). Para obter mais informações sobre como inserir palavras ou frases, consulte a próxima seção [correspondência de palavras e frases para emails ou anexos](configure-supervision-policies.md#Matchwords).<br/> |
|O anexo contém qualquer uma destas palavras  <br/> O anexo contém nenhuma dessas palavras  <br/> |Para aplicar a política quando determinadas palavras ou frases são incluídas ou excluídas no anexo de uma mensagem (por exemplo, um documento do Word), insira cada palavra ou frase em uma linha separada. Cada linha de palavras inseridas será aplicada separadamente (somente uma linha deve se aplicam para a política seja aplicada ao anexo). Para obter mais informações sobre como inserir palavras ou frases, consulte a próxima seção [correspondência de palavras e frases para emails ou anexos](configure-supervision-policies.md#Matchwords).<br/> |
|Anexo é qualquer um desses tipos de arquivo  <br/> Anexo é nenhum desses tipos de arquivo  <br/> |Para for o Supervisor de comunicações que incluem ou exclua tipos específicos de anexos, insira as extensões de arquivo (por exemplo, .exe ou. PDF). Se desejar incluir ou excluir várias extensões de arquivo, digite em linhas separadas. Extensão de apenas um anexo precisa corresponder para aplicar a política.  <br/> |
|O tamanho da mensagem é maior do que  <br/> Tamanho de mensagem não for maior que  <br/> |Para revisar as mensagens com base em um determinado tamanho, use essas condições para especificar o tamanho máximo ou mínimo, que uma mensagem pode ser antes que ele está sujeito a revisão. Por exemplo, se você especificar o **tamanho da mensagem for maior que** \> **1.0 MB**, todas as mensagens que são 1.01 MB e maior vão estar sujeitos a revisão. Você pode escolher bytes, kilobytes, megabytes ou gigabytes para essa condição.<br/> |
|Anexo é maior que  <br/> Anexo não for maior que  <br/> |Para revisar as mensagens com base no tamanho dos seus anexos, especifique o tamanho máximo ou mínimo um anexo pode ser antes da mensagem e seus respectivos anexos estão sujeitos a revisão. Por exemplo, se você especificar o **anexo é maior do que** \> **MB 2.0**, todas as mensagens com anexos 2.01 MB e o failover não serão sujeitos a revisão. Você pode escolher bytes, kilobytes, megabytes ou gigabytes para essa condição.<br/> |
   
#### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Palavras e frases correspondentes a emails ou anexos
<a name="Matchwords"> </a>

Cada linha de palavras inseridas será aplicada separadamente (somente uma linha deve se aplicam para a condição de política a ser aplicado ao email ou anexo). Por exemplo, vamos usar a condição, a **que mensagem contém qualquer uma dessas palavras**, com o bancário"palavras-chave" e "insider comercialização" em linhas separadas. A política será aplicada a todas as mensagens que inclui "bancário" ou a frase "insider comercialização". Apenas uma dessas palavras ou frases deve ocorrer para essa condição de política a ser aplicado. Palavras na mensagem ou no anexo devem corresponder exatamente o que você digita.
  
#### <a name="entering-multiple-conditions"></a>Inserindo várias condições
<a name="Matchwords"> </a>

Se você inserir várias condições, o Office 365 usa todas as condições juntos para determinar quando aplicar a política aos itens de comunicação. Quando você configura várias condições, eles devem todos ser atendidos para a política seja aplicada, a menos que você insira uma exceção. Por exemplo, digamos que você precisa criar uma política que deve ser aplicadas se uma mensagem contendo a palavra "comércio" e for maior que 2MB. No entanto, se a mensagem também contém as palavras "Aprovado pelo financeiro da Contoso", a diretiva não deve aplicar. Assim, nesse caso, as três condições seria da seguinte maneira: 
  
- **Mensagem contém qualquer uma dessas palavras**, com as palavras-chave "comercial"
    
- **Tamanho da mensagem for maior que**, com o valor de 2 MB
    
- **Mensagem contém nenhuma dessas palavras**, com as palavras-chave "Aprovado pela equipe financeiro da Contoso".
    
### <a name="specify-percentage-to-review"></a>Especifique a porcentagem para analisar
<a name="CommsToReview"> </a>

Se você deseja reduzir a quantidade de conteúdo para examinar, especifique uma porcentagem. Podemos selecionará aleatoriamente essa quantidade de conteúdo do total que correspondem às condições que você escolheu. Se você quiser revisores para examinar todos os itens, insira **100%**.
  
### <a name="choose-reviewers"></a>Escolha os revisores
<a name="CommsToReview"> </a>

Os usuários e grupos que você escolher usará o aplicativo de supervisão no Outlook web app para examinar as comunicações que são retornadas por essa política. Você pode incluir os endereços de email para revisores internos ou externos. 
  
### <a name="review-your-settings"></a>Revise suas configurações
<a name="CommsToReview"> </a>

Depois de concluir todas as seções da diretiva de supervisão, revise suas configurações e clique em **Concluir** para salvar a política. Poderá demorar algumas horas para a política iniciar a captura de comunicações. Supervisão apresenta todas as comunicações para revisão em uma pasta compartilhada que revisores podem acessar no Outlook web app. 
  
## <a name="use-outlook-web-app-to-review-communications-identified-by-a-supervision-policy"></a>Usar o Outlook web app para analisar identificadas por uma política de supervisão de comunicações
<a name="UseOutlook"> </a>

Revisores usará o suplemento de supervisão para o Outlook web app para examinar comunicações. O suplemento é instalado automaticamente no Outlook web app para todos os revisores que você especificou na política. Suporte para a versão da área de trabalho do Outlook disponíveis em breve.
  
 **Revisando communications no Outlook web app**
  
1. No Outlook web app, expanda o **supervisão - \<nome da política\> ** pasta. 
    
2. No ** \<nome da política\> ** subpasta, revisores verá todas as comunicações identificadas por essa diretiva de supervisão. 
    
    ![Suplemento de supervisão no Outlook web app mostrando a subpasta de diretiva de supervisão selecionada](media/eef329bf-2bd0-477e-a715-76ca19b3347f.jpg)
  
3. Abra um item para examinar e clique no suplemento de **supervisão** . 
    
4. Use o suplemento para classificar o item como **compatível**, **Não-compatível**, **Questionable** ou **resolvido**. Depois que você tiver classificado um item, ele será movido para a subpasta correspondente sob o ** \<nome da política\> ** pasta. 
    

