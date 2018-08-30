---
title: Gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9a00b9ea-33fd-4772-8ea6-9d3c65e829e6
description: Usar a segurança do Office 365 &amp; Centro de conformidade para criar pausas de descoberta eletrônica e para acessar e gerenciar casos do eDiscovery em sua organização.
ms.openlocfilehash: 5be66419e19f9703be5dde3fad82837bda249b72
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524040"
---
# <a name="manage-ediscovery-cases-in-the-office-365-security-amp-compliance-center"></a>Gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade

Você pode usar os casos de eDiscovery no Office 365 Security &amp; Centro de conformidade para controlar quem pode criar, acessar e gerenciar casos do eDiscovery em sua organização. Se sua organização tiver uma assinatura do Office 365 E5, você também pode usar os casos de eDiscovery para analisar os resultados de pesquisa usando o eDiscovery avançadas do Office 365.
  
Um caso de eDiscovery permite que você adicionar membros a um caso, controlar que tipos de ações que membros de maiusculas específicos podem executar, colocar uma isenção em locais de conteúdo relevante a um caso jurídico e associar várias pesquisas de conteúdo um único caso. Você também pode exportar os resultados de qualquer pesquisa de conteúdo que está associado um caso ou preparar os resultados da pesquisa para análise no eDiscovery avançado. casos de eDiscovery são uma boa maneira de limitar quem tem acesso ao conteúdo de pesquisa e seus resultados de pesquisa para um caso jurídico específico em sua organização.
  
Use o fluxo de trabalho a seguir para configurar e usar os casos de eDiscovery na segurança &amp; descoberta eletrônica do Centro de conformidade e Avançado.
  
[Etapa 1: atribuir permissões de Descoberta Eletrônica para possíveis membros da ocorrência](manage-ediscovery-cases.md#step1_1)
  
[Etapa 2: Criar um novo caso](manage-ediscovery-cases.md#step2_1)
  
[Etapa 3: Adicionar membros a um caso](manage-ediscovery-cases.md#step2a_1)
  
[Etapa 4: Local locais de conteúdo em espera](manage-ediscovery-cases.md#step3_1)
  
[Etapa 5: Criar e executar uma pesquisa de conteúdo associados a um caso](manage-ediscovery-cases.md#step4_1)
  
[Etapa 6: Exportar os resultados de uma pesquisa de conteúdo associados a um caso](manage-ediscovery-cases.md#step5_1)
  
[Etapa 7: Preparar resultados para eDiscovery avançada de pesquisa](manage-ediscovery-cases.md#step7_1)
  
[Etapa 8: Vá para o caso da eDiscovery avançado](manage-ediscovery-cases.md#gotoAeD_1)
  
[(Opcional) Etapa 9: Fechar um caso](manage-ediscovery-cases.md#closecase_1)
  
[(Opcional) Etapa 10: Reabrir uma ocorrência fechada](manage-ediscovery-cases.md#reopencase_1)
  
[Mais informações](manage-ediscovery-cases.md#moreinfo_1)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Etapa 1: atribuir permissões de Descoberta Eletrônica para possíveis membros da ocorrência
<a name="step1_1"> </a>

A primeira etapa é atribuir as permissões apropriadas de descoberta eletrônica relacionados a pessoas, portanto, você poderá adicioná-los a um caso de descoberta eletrônica na etapa 2. Você precisa ser membro do grupo de funções de gerenciamento da organização (ou a ser atribuído à função de gerenciamento de função) no Office 365 Security &amp; Centro de conformidade para atribuir permissões de descoberta eletrônica. A lista a seguir descreve os grupos de função relacionadas a descoberta eletrônica na segurança &amp; Centro de conformidade.
  
- **Revisor** Este grupo de funções tem as permissões mais restritivas de descoberta eletrônica relacionados. Os membros desse grupo só podem ver e abrir a lista dos casos na página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade que eles são membros. Eles não podem criar casos, adicionar membros a um caso, criar pausas, criar pesquisas, exportar resultados da pesquisa ou preparar os resultados para eDiscovery avançado. No entanto, os membros podem acessar casos de eDiscovery avançado para executar tarefas de análise. 
    
- **gerente de descoberta eletrônica** Os membros deste grupo de função podem criar e gerenciar casos do eDiscovery. Eles podem adicionar e remover membros, colocar conteúdo locais em espera, criar e editar pesquisas de conteúdo associados a um caso, exportar os resultados de uma pesquisa de conteúdo e preparar os resultados da pesquisa para análise no eDiscovery avançado. Existem dois subgrupos nesse grupo de função. A diferença entre esses subgrupos baseia-se em escopo.
    
  - **gerente de descoberta eletrônica** Pode exibir e gerenciar os casos de eDiscovery que eles criam ou serão um membro do. Se outra eDiscovery Manager cria um caso, mas não adiciona um segundo eDiscovery Manager como membro desse caso, a segunda eDiscovery Manager não será possível exibir ou abra a ocorrência na página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade. Gerentes de descoberta eletrônica também pode acessar seus casos de eDiscovery avançado para executar tarefas de análise. 
    
  - **administrador de descoberta eletrônica** Pode executar todas as tarefas de gerenciamento de casos que pode ser feito por uma gerente de descoberta eletrônica. Além disso, um administrador de eDiscovery pode:
    
  - Exibir todas as ocorrências listadas na página **Descoberta Eletrônica**. 
    
  - Depois que eles adicionam-se como um membro do caso, gerencie qualquer caso de descoberta eletrônica na organização.
    
  - Execute tarefas administrativas no eDiscovery avançado, como processamento de dados casos para análise, definindo configurações de maiusculas e exportando dados do eDiscovery avançado. Isso ocorre porque uma pessoa que é um administrador na segurança de descoberta eletrônica &amp; Centro de conformidade é adicionado automaticamente como um administrador no eDiscovery avançado.
    
    Consulte a seção [More information](manage-ediscovery-cases.md#moreinfo_1) para conhecer os motivos pelos quais convém ter um Administrador de Descoberta Eletrônica em sua organização. 
    
> [!IMPORTANT]
> Se uma pessoa não for um membro de um desses grupos de função relacionadas a descoberta eletrônica ou não é um membro de um grupo de função que atribuiu a função de revisor, você não pode adicioná-los como um membro de um caso de eDiscovery. 
  
 **Para atribuir as permissões de Descoberta Eletrônica:**
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. Na segurança &amp; Centro de conformidade, clique em **permissões**e, em seguida, siga um destes procedimentos com base nas permissões de eDiscovery que você deseja atribuir.
    
  - Para atribuir permissões de revisor, selecione o grupo de funções do **Revisor** e clique em **Editar**ao lado de **membros** . Clique em **Escolher membros**, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Adicionar** , selecione o usuário que você deseja adicionar ao grupo de funções de revisor e clique em **Adicionar**.
    
  - Para atribuir permissões de gerente de descoberta eletrônica, selecione o grupo de função de **gerente de descoberta eletrônica** e, ao lado de **eDiscovery Manager**, clique em **Editar**. Clique em **Escolher eDiscovery Manager**, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) * * Add * *, selecione o usuário que você deseja adicionar como uma gerente de descoberta eletrônica e, em seguida, clique em **Adicionar**.
    
  - Para atribuir permissões de administrador de descoberta eletrônica, selecione o grupo de função de **gerente de descoberta eletrônica** e, ao lado de **Descoberta eletrônica de administrador**, clique em **Editar**. Clique em **Escolher eDiscovery administrador**, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Adicionar**, selecione o usuário que você deseja adicionar como uma administrador de descoberta eletrônica e, em seguida, clique em **Adicionar**.
    
4. Após ter adicionado todos os usuários, clique em **concluído**, clique em **Salvar** para salvar as alterações ao grupo de funções e, em seguida, clique em **Fechar**.
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-2-create-a-new-case"></a>Etapa 2: Criar um novo caso
<a name="step2_1"> </a>

A próxima etapa é criar um novo caso de descoberta eletrônica. Você deve ser um membro do grupo de função de gerenciadores de descoberta eletrônica para criar casos de eDiscovery. Como previamente explicado, depois de criar um novo caso na segurança &amp; Centro de conformidade, você (e outros membros maiusculas) será capazes de acesso que o mesmo caso no eDiscovery avançado, se você estiver organização tem uma assinatura do Office 365 E5.
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery**e clique ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **criar um caso**.
    
4. Na página **Novo caso** , nomeie o caso, digite uma descrição opcional e clique em **Salvar**. Observe que o nome de maiusculas deve ser exclusivo na sua organização.
    
    ![Nova página de maiusculas](media/538f66b8-eb6e-4c4c-83d8-7154fd85883a.png)
  
    O novo caso é exibido na lista de casos na página de **Descoberta eletrônica** . Observe que você pode posicionar o cursor sobre um nome de maiusculas para exibir informações sobre o caso, incluindo o status do caso ( **ativo** ou **fechado**), a descrição da ocorrência (que foi criada na etapa anterior), e quando o caso foi alterado pela última e quem alterou.
    
    > [!TIP]
    > Depois de criar um novo caso, você poderá renomeá-lo a qualquer momento. Basta clicar no nome da ocorrência na página de **Descoberta eletrônica** . Na página **Gerenciar neste caso** submenu, alterar o nome exibido na caixa em **nome**e, em seguida, salvar as alterações. 
  
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-3-add-members-to-a-case"></a>Etapa 3: Adicionar membros a um caso
<a name="step2a_1"> </a>

Depois de criar um novo caso, a próxima etapa é adicionar membros ao caso. Anterior conforme explicado, somente os usuários que são membros do revisor ou grupos de função de gerente de descoberta eletrônica podem ser adicionados como um membro do caso. Observe que o gerente que criou o caso de descoberta eletrônica é adicionada automaticamente como um membro.
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique no nome do que você deseja adicionar membros ao caso.
    
    A página de submenu **Gerenciar neste caso** é exibida. 
    
    ![Clique no nome de maiusculas para exibir esta página maiusculas gerenciar](media/2364dc08-a3dc-4724-acf4-7a68c8588e6f.png)
  
3. Em **Gerenciar membros**, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Add** para adicionar membros ao caso. 
    
4. Na lista de pessoas que podem ser adicionadas como membro do caso, clique na caixa de seleção ao lado do nome das pessoas que você deseja adicionar ao caso.
    
    > [!TIP]
    > Se você tiver uma grande lista de pessoas que podem adicionadas como membros, use a caixa **Pesquisar** para procurar uma pessoa específica na lista. 
  
5. Depois que você tiver selecionado as pessoas a serem adicionados como membros do grupo, clique em **Adicionar**.
    
    Em **Gerenciar neste caso**, clique em **Salvar** para salvar a nova lista de membros de maiusculas. 
    
6. Clique em **Salvar** para salvar a nova lista de membros de maiusculas. 
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-4-place-content-locations-on-hold"></a>Etapa 4: Local locais de conteúdo em espera
<a name="step3_1"> </a>

Você pode usar um caso de eDiscovery para criar pausas para preservar o conteúdo que pode ser relevante ao caso. Você pode colocar uma isenção nas caixas de correio e OneDrive para sites corporativos das pessoas que são responsáveis no caso. Você também pode fazer uma pausa na caixa de correio de grupo, site do SharePoint e OneDrive para o site de negócios para um grupo do Office 365. Da mesma forma, você pode colocar uma pausa no site que estão associados a Teams da Microsoft e da caixa de correio. Quando você realiza locais de conteúdo em espera, o conteúdo é mantido até que você remova o bloqueio do conteúdo local ou até que você exclua isenção.
  
Quando você cria uma pausa, você tem as seguintes opções para o conteúdo que é mantido nos locais especificados conteúdos de escopo:
  
- Criar uma espera infinita, onde todo o conteúdo é colocado em espera. Como alternativa, é possível criar uma isenção baseado em consulta onde somente o conteúdo que corresponda a uma consulta de pesquisa é colocado em espera.
    
- Você pode especificar um intervalo de datas para reter somente o conteúdo que foi enviado, recebido ou criado dentro desse intervalo de datas. Como alternativa, você pode manter todo o conteúdo independentemente de quando ela foi enviada, recebida ou criada.
    
> [!NOTE]
> Você pode ter um máximo de 10.000 políticas de retenção em todos os casos de eDiscovery em sua organização. 
  
Para criar uma isenção para um caso de eDiscovery:
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja criar os bloqueios no. 
    
3. Na página **inicial** para o caso, clique em **espera**.
    
    ![Clique em espera para exibir a página de isenções maiusculas.](media/25c0300a-bd33-4443-a121-d595b1a3e00f.png)
  
4. Na página de **espera** , clique em **novo**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).
    
5. Na página **Criar uma nova retenção**, dê um nome para a retenção. O nome da retenção deve ser exclusivo na sua organização.  
    
6. Escolha os locais de conteúdo que você deseja colocar em espera. Você pode colocar pastas públicas, sites e caixas de correio em espera.
    
    ![Escolher os locais de conteúdo para colocar em espera](media/a00c952c-f91f-4708-b5a4-6213e4c413c7.png)
  
1. **Caixas de correio** Clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para especificar as caixas de correio para colocar em espera. Use a caixa Pesquisar para localizar caixas de correio de usuário e grupos de distribuição (para colocar uma isenção em caixas de correio dos membros do grupo) deve ser colocado em espera. Você também pode fazer uma pausa na caixa de correio associada para um Team Microsoft ou de um grupo do Office 365. 
    
    > [!NOTE]
    > Quando você clicar em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para especificar as caixas de correio deve ser colocado em espera, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar pessoas a essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar e clique em **Pesquisar**![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif). 
  
2. **Sites** Clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) especificar SharePoint e OneDrive para sites corporativos para colocar em espera. Digite a URL para cada site que você deseja colocar em espera. Você também pode adicionar a URL do site do SharePoint para um Team Microsoft ou de um grupo do Office 365. 
    
<<<<<<< Consulte cabeça o [gerenciar casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da#moreinfo_1) seção para obter dicas sobre a colocação de grupos do Office 365 e Teams da Microsoft em espera. === Consulte a seção de [informações adicionais](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da.aspx#moreinfo_1) para obter dicas sobre a colocação de grupos do Office 365 e Teams da Microsoft em espera. 
>>>>>>> conversão de deniseb
    
    > [!NOTE]
    > In the rare case that a person's user principal name (UPN) is changed, the URL for their OneDrive account will also be changed to incorporate the new UPN. If this happens, you'll have to modify the hold by adding the user's new OneDrive URL and removing the old one. 
  
3. **Pastas públicas** Clique em **espera todas as pastas públicas** para colocar todas as pastas públicas em sua organização em retenção Exchange Online. Observe que não é possível escolher específicos de pastas públicas para colocar em espera. Deixe a opção **não mantenha quaisquer pastas públicas** selecionada se você não deseja colocar um bloqueio em pastas públicas. 
    
7. Quando você terminar de adicionar locais de conteúdo à isenção, clique em **Avançar**.
    
8. Para criar uma isenção baseado em consulta com condições, conclua o seguinte. Caso contrário, basta clicar em **Concluir** para armazenar todo o conteúdo. 
    
    ![Criar uma isenção baseado em consulta especificando as palavras-chave e condições](media/a5bb802e-2e96-4f12-8b33-1ddd671638e4.png)
  
    Para obter mais informações sobre como criar uma consulta de pesquisa e condições de uso, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).
    
1. Na caixa em **que você deseja fazer conosco para procurar?**, digite uma consulta de pesquisa na caixa para que apenas o conteúdo que satisfaz os critérios de pesquisa é colocado em espera. Você pode especificar palavras-chave, propriedades de mensagem ou propriedades de documento, como nomes de arquivo. Você também pode usar as consultas mais complexas que usam um operador booleano, como **AND**, **OR**ou **não**. Se você deixar a caixa de palavra-chave vazia, e em seguida, todo o conteúdo localizado nos locais de conteúdo especificados será colocado em espera. 
    
2. Sob **condições**, clique em **Adicionar condição** para adicionar uma ou mais condições para restringir a consulta de pesquisa para a retenção. Cada condição adiciona uma cláusula à consulta KQL pesquisa que é criada e executada quando você cria o bloqueio. Por exemplo, você pode especificar um intervalo de datas para que os documentos de email ou site que foram criados dentro da intervalo de data são colocados em espera. Uma condição logicamente está conectada à consulta de palavra-chave (especificada na caixa de palavra-chave) pelo operador **e** . Isso significa que o item deve satisfazer ambos a consulta de palavra-chave e a condição sejam colocadas em espera. 
    
9. Depois de configurar uma consulta com base em espera, clique em **Concluir** para criar a pausa. 
    
[Return to top](manage-ediscovery-cases.md#top)
  
### <a name="hold-statistics"></a>Mantenha as estatísticas

Após algum tempo, informações sobre a nova isenção são exibidas no painel de detalhes, na página **contém** referente à isenção selecionada. Essas informações incluem o número de caixas de correio e sites em espera e estatísticas sobre o conteúdo que foi colocado em espera, como o número total e o tamanho dos itens colocados em espera e a última vez que a suspensão estatísticas foram calculadas. Mantenha a Ajuda de estatísticas que identificar a quantidade de conteúdo que está relacionada ao caso de eDiscovery está sendo mantido. 
  
![Mantenha as estatísticas são exibidas no painel de detalhes referente à isenção selecionada](media/e46359a3-cba1-4771-bbf5-bc53b4a2cb14.png)
  
Mantenha as seguintes coisas em mente sobre estatísticas de espera:
  
- O número total de itens em espera indica o número de itens de todas as fontes de conteúdo que são colocadas em espera. Se você criou uma consulta com base em espera, essa estatística indica o número de itens que correspondem à consulta.
    
- O número de itens em espera também inclui itens indexados encontrados em locais de conteúdo. Observe que, se você criar uma isenção baseado em consulta, todos os itens indexados os locais de conteúdo são colocados em espera. Isso inclui itens indexados que não correspondem aos critérios de pesquisa de uma isenção baseado em consulta e não indexadas que poderão ficar fora de uma condição de intervalo de data. Isso é diferente do que o que acontece quando você executa uma pesquisa de conteúdo, na qual os itens indexados que não correspondem à consulta de pesquisa ou são excluídos por uma condição de intervalo de data não estão incluídos nos resultados da pesquisa. Para obter mais informações sobre os itens não indexadas, consulte [itens indexados na pesquisa de conteúdo no Office 365](partially-indexed-items-in-content-search.md).
    
- Você pode obter as informações mais recentes mantenha estatísticas clicando em **Atualizar estatísticas** para executar novamente uma pesquisa estimar que calcula o número atual de itens em espera. Se necessário, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) na barra de ferramentas para atualizar as estatísticas de espera no painel de detalhes. 
    
- De TI normal para o número de itens em espera para aumentar ao longo do tempo porque os usuários cujas caixas de correio ou o site está em retenção são geralmente enviando ou recebendo a nova mensagem de email e criando novo SharePoint e OneDrive para documentos de negócios.
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>Etapa 5: Criar e executar uma pesquisa de conteúdo associados a um caso
<a name="step4_1"> </a>

Depois de um caso de eDiscovery é criado e qualquer responsáveis relacionadas ao caso são colocados em espera, você pode criar e executar uma ou mais pesquisas de conteúdo associados ao caso. Conteúdo de pesquisas associadas a um caso não estão listadas na página de **pesquisa** na segurança &amp; Centro de conformidade. Isso significa que as pesquisas de conteúdo associadas a um caso só pode ser acessada por integrantes de maiusculas, que também são membros do grupo de função de Gerenciador de descoberta eletrônica. 
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja criar uma pesquisa de conteúdo no. 
    
3. Na página **inicial** para o caso, clique em **Pesquisar**.
    
    ![Na Home page do caso, clique em Pesquisar](media/bd358eb3-12d4-4f0c-8317-d192286813d0.png)
  
4. Na página de **pesquisa** , clique em **novo**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif).
    
5. Na página **nova pesquisa** , digite um nome para a pesquisa. Pesquisas de conteúdo associadas a um caso devem ter nomes exclusivos dentro da sua organização do Office 365. 
    
6. Escolha os locais de conteúdo que você deseja pesquisar. Você pode pesquisar caixas de correio, sites e pastas públicas na mesma pesquisa.
    
    ![Pesquise maiusculas locais de conteúdo, todos os locais de conteúdo, ou selecionar locais específicos de conteúdo](media/08c523dc-cba8-4fce-aee6-f86251204393.png)
  
1. **Todo o conteúdo maiusculas** Selecione essa opção para todos os locais de conteúdo que foram colocados em espera no caso de pesquisa. Se o caso contiver várias retenções, o conteúdo de locais de todas as isenções devem ser pesquisadas quando você seleciona essa opção. Além disso, se um local de conteúdo foi colocado em uma espera baseado em consulta, somente os itens que estão em espera serão pesquisados quando você executar a pesquisa de conteúdo que você está criando nesta etapa. Por exemplo, se um usuário foi colocado em espera maiusculas baseado em consulta que preserva itens que foram enviados ou criados antes de uma data específica, somente aqueles itens ser pesquisados usando os critérios de pesquisa da pesquisa conteúdo. Isso é realizado conectando-se a consulta de espera de maiusculas e a consulta de pesquisa de conteúdo por um operador **e** . Consulte a seção [mais informações](manage-ediscovery-cases.md#moreinfo_1) no final deste artigo para obter mais detalhes sobre como pesquisar conteúdo maiusculas. 
    
2. **Pesquisa em todos os lugares** Selecione essa opção para pesquisar todos os locais de conteúdo na sua organização. Quando você seleciona essa opção, você pode optar por pesquisar todas as caixas de correio do Exchange (que inclui as caixas de correio para todos os grupos do Office 365 e Microsoft Teams), SharePoint e o OneDrive para sites corporativos (que inclui os sites para todos os grupos do Office 365 e Microsoft As equipes) e todas as pastas públicas.
    
3. **Seleção de local personalizado** Selecione essa opção para selecionar as caixas de correio e os sites que você deseja pesquisar. Quando você seleciona essa opção, a lista de caixas de correio e de sites é pré-preenchido com o conteúdo de locais que são colocados em espera dentro do caso. Você também pode optar por pesquisar todas as pastas públicas em sua organização.
    
    ![Pesquisar todo o conteúdo maiusculas, todos os locais de pesquisa ou pesquisar um local personalizado](media/7ca97ab4-52d5-46a5-9e24-e3a4d1001595.png)
  
    Mas se você selecionar essa opção e pesquisa de qualquer local do conteúdo que está em espera, um qualquer consulta de uma isenção maiusculas baseado em consulta não será aplicada à consulta de pesquisa. Em outras palavras, todo o conteúdo em um local é pesquisado, não apenas o conteúdo que é preservado por uma isenção maiusculas baseado em consulta.
    
    Você pode remover os locais de conteúdo maiusculas pré-preenchida ou adicionar novos. Se você escolher essa opção, você também tem a flexibilidade para pesquisar todos os locais de conteúdo para um serviço específico (por exemplo, pesquisar todas as caixas de correio do Exchange) ou você pode pesquisar locais de conteúdo específico para um serviço. Você também pode escolher se ou não pesquisar as pastas públicas em sua organização.
    
    Mantenha em mente ao adicionar locais de conteúdo para pesquisa:
    
  - Quando você clicar em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para especificar as caixas de correio para pesquisar, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar destinatários para essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar e clique em **Pesquisar**![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif).
    
  - Você pode adicionar caixas de correio inativas, grupos do Office 365, Teams da Microsoft e grupos de distribuição à lista de caixas de correio a ser pesquisado. Grupos dinâmicos de distribuição não são suportados. Se você adicionar grupos do Office 365 ou Teams da Microsoft, a caixa de correio de grupo ou equipe é pesquisada; as caixas de correio dos membros do grupo não são pesquisadas.
    
  - Se você não quiser incluir quaisquer sites ou caixas de correio em uma pesquisa, selecione **Escolher caixas de correio específicas para pesquisar** ou **Escolher a sites específicos para pesquisar**, mas não adicionar caixas de correio ou sites à lista.
    
  - Para adicionar sites clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e, em seguida, digite a URL para cada site que você deseja pesquisar. Você também pode adicionar a URL do site do SharePoint para o Office 365 grupos e Teams da Microsoft. 
    
7. Depois que você selecionou os locais de conteúdo para pesquisa, clique em **Avançar**.
    
8. Na página **Nova pesquisa**, você pode adicionar palavras-chave e condições para criar a consulta de pesquisa. 
    
    ![Critérios de pesquisa e condições](media/9064147e-feac-4090-bbf6-2298ad7622c6.png)
  
1. Na caixa em **que você deseja fazer conosco para procurar?**, digite uma consulta de pesquisa na caixa. Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que usam um operador booleano, como **AND**, **ou**, **não**, **NEAR**ou **ONEAR**. Você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) em documentos ou procurar documentos que foram compartilhados externamente. Se você deixar a caixa de palavra-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificados será incluído nos resultados da pesquisa. 
    
2. Você pode clicar na caixa de seleção **Mostrar lista de palavra-chave** e o tipo de uma palavra-chave em cada linha. Se você fizer isso, as palavras-chave em cada linha são conectadas pela operadora **ou** na consulta de pesquisa que é criada. 
    
    ![Palavras-chave de pesquisa](media/c3ef511a-e0a3-4b5d-9779-36803270a193.png)
  
    Por que usar a lista de palavra-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave é mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas da pesquisa, consulte [Exibir as estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
    
    Para obter mais informações sobre como usar a lista de palavras-chave, consulte [mais informações](run-a-content-search-in-the-security-and-compliance-center.md#moreinfo).
    
3. Clique em **consulta para erros de digitação de seleção** para verificar sua consulta para caracteres não suportados e operadores booleanos que não podem estar em letras maiusculas. Não há suporte para caracteres geralmente estão ocultas e geralmente causam um erro de pesquisa ou retornam resultados inesperados. Para obter mais informações sobre os caracteres não suportados que são verificados, consulte [verificar sua consulta de pesquisa de conteúdo se há erros](check-your-content-search-query-for-errors.md).
    
4. Sob **condições**, adicione condições para uma consulta de pesquisa para restringir uma pesquisa e retornar um conjunto mais refinado de resultados. Cada condição adiciona uma cláusula à consulta KQL pesquisa que é criada e executada quando você iniciar a pesquisa. Uma condição logicamente está conectada à consulta de palavra-chave (especificada na caixa de palavra-chave) pelo operador **e** . Isso significa que itens precisam satisfazer tanto a consulta de palavra-chave e a condição a ser incluído nos resultados. Isso é como ajudam a condições para restringir os resultados. 
    
    Para saber mais sobre como criar uma consulta de pesquisa e usar condições, confira [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
9. Clique em **Pesquisar** para salvar as configurações da pesquisa e iniciá-la. 
    
    A pesquisa é iniciada. Após algum tempo, uma estimativa dos resultados da pesquisa é exibida no painel de detalhes. A estimativa inclui o tamanho total e o número de itens que correspondem aos critérios de pesquisa. A estimativa de pesquisa também inclui o número de itens indexados nos locais do conteúdo que foram pesquisados. O número de itens indexados que não atendem aos critérios de pesquisa será incluído nas estatísticas da pesquisa exibidas no painel de detalhes. Se um item não indexadas corresponde à pesquisa de consulta (porque outras propriedades de mensagem ou documento atendam aos critérios de pesquisa), não será incluído o número estimado de itens indexados. Se um item não indexado for excluído pelos critérios de pesquisa, ele também não será incluído na estimativa de itens indexados.
    
    Uma vez concluída a pesquisa, você pode visualizar os resultados da pesquisa. Se necessário, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes. 
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>Etapa 6: Exportar os resultados de uma pesquisa de conteúdo associados a um caso
<a name="step5_1"> </a>

Depois que uma pesquisa for executada com êxito, você pode exportar os resultados da pesquisa. Ao exportar os resultados da pesquisa, itens de caixa de correio são baixadas em arquivos PST ou como mensagens individuais. Quando você exporta o conteúdo do SharePoint e OneDrive para sites corporativos, cópias de documentos do Office nativos e outros documentos são exportadas. Um arquivo de manifesto (no formato XML) que contém informações sobre cada resultado de pesquisa também será exportado.
  
Você pode exportar os resultados de um [exportar os resultados de uma única pesquisa associada a um caso](manage-ediscovery-cases.md#singlesearch_1) ou é possível exportar os resultados de [exportar os resultados de pesquisas de várias associados a um caso](manage-ediscovery-cases.md#multiplesearches_1).
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>Exportar os resultados de uma única pesquisa associada a um caso
<a name="singlesearch_1"> </a>

1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja exportar a pesquisa de. 
    
3. Na página **inicial** para o caso, clique em **Pesquisar**.
    
4. Na lista de pesquisas para o caso, clique em pesquisa que você deseja exportar os resultados de pesquisa, clique em **Exportar**![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)e clique em **exportar os resultados**.
    
    A página de **resultados da pesquisa de exportação** é exibida. O fluxo de trabalho para exportar os resultados de uma pesquisa de conteúdo associados a um caso é igual ao exportar os resultados da pesquisa para uma pesquisa na página de **pesquisa de conteúdo** . Para obter instruções detalhadas, consulte [resultados de pesquisa de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md).
    
    > [!NOTE]
    > Ao exportar os resultados da pesquisa, você tem a opção para habilitar a eliminação da duplicação para que apenas uma cópia de uma mensagem de email será exportada, mesmo que várias instâncias da mesma mensagem podem ter sido encontradas nas caixas de correio que foram pesquisadas. Para obter mais informações sobre desduplicação e itens duplicados como são identificados, consulte [desduplicação nos resultados da pesquisa de descoberta eletrônica](de-duplication-in-ediscovery-search-results.md). 
  
5. Depois de iniciar a exportação, clique em **Exportar** para exibir a lista de trabalhos de exportação que existem para esse caso. 
    
    ![Clique em Exportar para exibir uma lista de trabalhos de exportação](media/b7b95bf7-134e-471e-961e-f86c1bb633eb.png)
  
    Talvez você precise clicar em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar a lista de trabalhos de exportação para exibir o trabalho de exportação que você acabou de criar. Observe que os trabalhos de exportação tem o mesmo nome que o conteúdo correspondente de pesquisa com **_Export** acrescentados ao final do nome de pesquisa. 
    
6. Clique no trabalho de exportação que você acabou de criar para exibir informações de status no painel de detalhes. Essas informações incluem a porcentagem de itens que tenham sido transferidas para uma área de armazenamento do Azure na nuvem da Microsoft.
    
    Depois de tem sido transferidos todos os itens, clique em **Download exportou resultados** para baixar os resultados da pesquisa ao computador local. Para obter mais informações, consulte a etapa 2 em [resultados de pesquisa de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>Exportar os resultados de pesquisas de várias associados a um caso
<a name="multiplesearches_1"> </a>

Como uma alternativa ao exportar os resultados de uma única pesquisa de conteúdo associados a um caso, você pode exportar os resultados das pesquisas de várias de maiusculas e minúsculas mesma em uma único exportação. Exportar os resultados das pesquisas de várias é mais rápido e mais fácil do que exportando a pesquisa de resultados um por vez.
  
> [!NOTE]
> É possível exportar os resultados das pesquisas de várias se uma dessas pesquisas foi configurada para pesquisar todo o conteúdo maiusculas. Exporte somente os resultados das pesquisas de várias para pesquisas que estão associadas um caso de eDiscovery. Não é possível exportar os resultados das pesquisas de várias listados na página **pesquisa de conteúdo** na segurança &amp; Centro de conformidade. 
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja exportar a pesquisa de. 
    
3. Na página **inicial** para o caso, clique em **Pesquisar**.
    
4. Na lista de pesquisas para o caso, selecione duas ou mais pesquisas que você deseja exportar os resultados da pesquisa.
    
    > [!NOTE]
    > Para selecionar várias pesquisas, pressione **Ctrl** enquanto clica em cada pesquisa. Ou você pode selecionar várias pesquisas adjacentes clicando a primeira pesquisa, mantendo pressionada a tecla **Shift** , e, em seguida, clicando em última pesquisa. 
  
5. Depois de selecionar as pesquisas, clique em **Exportar**![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)e clique em **exportar os resultados**.
    
6. O * * exportar os resultados de pesquisa para pesquisas de *n* * * página é exibida, onde *n* é o número do qual você está exportando os resultados de pesquisas. Observe que você terá que nomeie o trabalho de exportação. 
    
    O fluxo de trabalho para exportar os resultados de várias pesquisas de conteúdo associadas a um caso é igual ao exportar os resultados da pesquisa para uma única pesquisa. Para obter instruções detalhadas, consulte [resultados de pesquisa de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md).
    
    > [!NOTE]
    > Ao exportar os resultados da pesquisa de várias pesquisas associadas a um caso, você também tem a opção para habilitar a eliminação da duplicação para que apenas uma cópia de uma mensagem de email será exportada, mesmo que várias instâncias da mesma mensagem podem ter sido encontradas no caixas de correio que foram pesquisadas em uma ou mais das pesquisas. Para obter mais informações sobre desduplicação e itens duplicados como são identificados, consulte [desduplicação nos resultados da pesquisa de descoberta eletrônica](de-duplication-in-ediscovery-search-results.md). 
  
7. Depois de iniciar a exportação, clique em **Exportar** para exibir a lista da exportação de trabalhos que para esse caso. 
    
    ![Clique em Exportar para exibir uma lista de trabalhos de exportação](media/b7b95bf7-134e-471e-961e-f86c1bb633eb.png)
  
    Talvez você precise clicar em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar a lista de trabalhos de exportação para exibir o trabalho de exportação que você acabou de criar. Observe que as pesquisas que foram incluídas no trabalho de exportação estão listadas na coluna **pesquisas** . 
    
8. Clique no trabalho de exportação que você acabou de criar para exibir informações de status no painel de detalhes. Essas informações incluem a porcentagem de itens que tenham sido transferidas para uma área de armazenamento do Azure na nuvem da Microsoft.
    
9. Depois de tem sido transferidos todos os itens, clique em **Download exportou resultados** para baixar os resultados da pesquisa ao computador local. Para obter mais informações, consulte a etapa 2 em [resultados de pesquisa de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>Para obter mais informações sobre como exportar os resultados das pesquisas de várias

- Ao exportar os resultados das pesquisas de várias, as consultas de pesquisa de todas as pesquisas são combinadas usando operadores **ou** e, em seguida, a pesquisa combinada é iniciada. Os estimado resultados da pesquisa combinada são exibidos no painel de detalhes do trabalho de exportação selecionado. Os resultados da pesquisa, em seguida, são transferidos para a área de armazenamento do Azure na nuvem da Microsoft. O status da transferência também será exibido no painel de detalhes. Conforme indicado anteriormente, depois de tem sido transferidos todos os resultados da pesquisa, você pode baixá-los ao computador local. 
    
- O número máximo de palavras-chave das consultas de pesquisa para todas as pesquisas que você deseja exportar é 500. (isto é o mesmo limite para uma única pesquisa de conteúdo). Isso acontece porque o trabalho de exportação combina todas as consultas de pesquisa usando o operador **OR** . Se você exceder esse limite, um erro será retornado. Nesse caso, você terá que exportar os resultados de pesquisas menos ou simplificar as consultas de pesquisa de pesquisas de que você deseja exportar. 
    
- Os resultados da pesquisa que são exportados serão organizados por fonte de conteúdo que o item foi encontrado no. Isso significa que uma fonte de conteúdo nos resultados da exportação pode ter itens retornados por pesquisas diferentes. Por exemplo, se você escolher exportar mensagens de email em um arquivo PST para cada caixa de correio, o arquivo PST pode ter os resultados de várias pesquisas.
    
- Se o mesmo item de email ou o documento a partir do mesmo local de conteúdo é retornado por mais de uma das pesquisas de que você exporta, apenas uma cópia do item será exportada.
    
- Você não pode editar uma exportação para várias pesquisas após criá-la. Por exemplo, você não pode adicionar ou remover pesquisas da exportação. Você precisará criar um novo trabalho de exportação para alterar os resultados da pesquisa serão exportados. Depois que um trabalho de exportação é criado, você só pode baixar os resultados para um computador, reinicie a exportação ou excluir o trabalho de exportação.
    
- Se você reiniciar a exportação, quaisquer alterações às consultas das pesquisas que compõem o trabalho de exportação não afetarão os resultados de pesquisa que serão recuperados. Quando você reiniciar uma exportação, o trabalho de consulta de pesquisa combinada mesmo que foi executado quando o trabalho de exportação foi criado será executado novamente.
    
- Se você reiniciar uma exportação da página **exportações** em um caso de eDiscovery, resultados da pesquisa que são transferidos para a área de armazenamento do Azure substituirá os resultados anteriores; os resultados anteriores havia transferidos não estará disponível para download. 
    
- Preparar os resultados das pesquisas de várias para análise no eDiscovery Avançado não está disponível. Você só pode preparar os resultados de uma única pesquisa para análise no eDiscovery avançado.
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>Etapa 7: Preparar resultados para eDiscovery avançada de pesquisa
<a name="step7_1"> </a>

Se sua organização tiver uma assinatura do Office 365 E5, você pode preparar os resultados de pesquisas de conteúdo associados a um caso para análise no eDiscovery avançado. Depois de preparar os resultados da pesquisa, você pode ir para descoberta eletrônica avançada (consulte [etapa 8: vá para o caso da eDiscovery avançado](manage-ediscovery-cases.md#gotoAeD_1)) e processar os dados de resultado de pesquisa para análise adicional no eDiscovery avançado.
  
Ao preparar os resultados da pesquisa para a descoberta eletrônica avançada, a funcionalidade de reconhecimento óptico de caracteres (OCR) extrai automaticamente texto de imagens. OCR é suportado para arquivos flexível, anexos de email e imagens incorporadas. Isso permite que você aplique as capacidades analíticas de texto de eDiscovery avançado (perto duplicatas, email threading, temas e previsão de codificação) para qualquer texto nos arquivos de imagem.
  
> [!NOTE]
> Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5. 
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja preparar os resultados da pesquisa para análise no eDiscovery avançado. 
    
3. Na página **inicial** para o caso, clique em **Pesquisar**e, em seguida, selecione a pesquisa.
    
4. No painel de detalhes, **Analisar resultados com eDiscovery avançada**, clique em **Preparar resultados para análise**.
    
5. Na página **Preparar os resultados para análise**, faça o seguinte:  
    
  - Escolha preparar itens indexados, itens indexados e não indexados ou apenas itens indexados para análise no eDiscovery avançado.
    
  - Escolha se deseja incluir todas as versões de documentos encontrados no SharePoint que atendidos os critérios de pesquisa. Essa opção aparecerá somente se as fontes de conteúdo para a pesquisa inclui sites.
    
  - Especifique se deseja que uma mensagem de notificação enviada (ou copiou) para uma pessoa quando o processo de preparação é concluído e os dados estão prontos para ser processado no eDiscovery avançado.
    
6. Clique em **Preparar**.
    
    Os resultados da pesquisa são preparados para análise com eDiscovery avançado.
    
7. No painel de detalhes, clique em **Verificar status de preparação** para exibir informações sobre o processo de preparação. Quando o processo de preparação for concluído, você pode ir para o caso da eDiscovery avançada para processar os dados para análise. 
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>Etapa 8: Vá para o caso da eDiscovery avançado
<a name="gotoAeD_1"> </a>

Depois de criar um caso na segurança &amp; Centro de conformidade, que você pode ir para o mesmo caso no eDiscovery avançado.
  
Para ir até um caso de eDiscovery avançada:
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja ir para a descoberta eletrônica avançada. 
    
3. Na página **inicial** para o caso, clique em **Alternar para descoberta eletrônica avançada**.
    
    ![Clique em Alternar para descoberta eletrônica avançada para abrir o caso no eDiscovery avançado](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    A barra de progresso **Conectando-se a descoberta eletrônica avançada** é exibida. Quando você estiver conectado ao eDiscovery avançado, uma lista dos contêineres é exibida na página. 
    
    ![O caso é exibido no eDiscovery avançado](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
    Desses contêineres representam os resultados da pesquisa que você preparou para análise no eDiscovery Avançado na etapa 7. Observe que o nome do contêiner tem o mesmo nome de pesquisa de conteúdo no caso de segurança &amp; Centro de conformidade. Os contêineres na lista são aqueles que você preparou. Se um usuário diferente preparado os resultados da pesquisa para a descoberta eletrônica avançada, os contêineres correspondentes não serão incluídos na lista.
    
4. Para carregar os dados de resultado de pesquisa de um contêiner para o caso da eDiscovery avançada, selecione um contêiner e clique em **processar**.
    
    Para obter informações sobre como contêineres de processo, consulte [executar o módulo de processo e carregar dados no eDiscovery avançadas do Office 365](run-the-process-module-and-load-data-in-advanced-ediscovery.md).
    
> [!TIP]
> Clique em **Alternar para descoberta eletrônica** para voltar para o mesmo caso na segurança &amp; Centro de conformidade. 
  
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="optional-step-9-close-a-case"></a>(Opcional) Etapa 9: Fechar um caso
<a name="closecase_1"> </a>

Quando o caso legal ou investigação compatíveis com um caso de eDiscovery for concluída, você pode fechar o caso. Aqui está o que acontece quando você fecha um caso:
  
- Se o caso contiver quaisquer locais de conteúdo em espera, essas isenções serão desativadas. Isso pode resultar no conteúdo que está sendo excluído permanentemente ou removidos, pelo usuário ou por um processo automatizado, como uma política de exclusão.
    
- Fechar um caso apenas desativa os bloqueios que estão associados esse caso. Se a outras retenções são realizadas em um local de conteúdo (por exemplo, um litígio espera. uma política de preservação ou uma espera de um caso de eDiscovery diferentes) essas isenções ainda serão mantidas.
    
- O caso ainda estiver listado na página de descoberta eletrônica na segurança &amp; Centro de conformidade. Os detalhes, isenções, pesquisas e membros de um caso de fechado são mantidos.
    
- Você pode editar um caso depois que ele é fechado. Por exemplo, você pode adicionar ou remover membros, criar pesquisas, exportar resultados da pesquisa e preparar o resultado de pesquisa para análise no eDiscovery avançado. A principal diferença entre os casos de ativos e fechados é isenções serão desativadas quando um caso for fechado.
    
Para fechar um caso:
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique no nome do caso que você deseja fechar.
    
    A página de submenu **Gerenciar neste caso** é exibida. 
    
3. Em **status do caso de gerenciar**, clique em ![remover o botão espiada no](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) **Fechar o caso**.
    
4. Na página de **detalhes** , clique em **Fechar o caso**.
    
    Será exibido um aviso dizendo que os bloqueios associados à ocorrência serão desativados.
    
5. Clique em **Sim** para fechar o caso. 
    
    O status na página **Gerenciar neste caso** submenu é alterado de **ativo** para **Fechar**.
    
6. Feche **Gerenciar neste caso**.
    
7. Na página de **Descoberta eletrônica** , clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** para atualizar o status do caso fechado. Ela pode levar até 60 minutos para concluir o processo de fechamento. 
    
    Quando o processo estiver concluído, o status do caso é alterado para **Fechar** na página de **Descoberta eletrônica** . Clique no nome do caso novamente para exibir a página de submenu **Gerenciar neste caso** , que contém informações sobre quando o caso foi fechado e a quem fechá-la. 
    
[Return to top](manage-ediscovery-cases.md#top)
  
## <a name="optional-step-10-re-open-a-closed-case"></a>(Opcional) Etapa 10: Reabrir uma ocorrência fechada
<a name="reopencase_1"> </a>

Quando você abre um caso novamente, qualquer isenções que estavam em vigor quando o caso foi fechado não restabelecidas automaticamente. Depois que o caso for reaberto, você precisará ir para a página de **espera** e ativar os bloqueios anteriores. Para ativar uma isenção, selecione-o e clique em **ativá-lo** no painel de detalhes. 
  
1. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
2. Clique no nome do caso que você deseja abrir novamente.
    
    A página de submenu **Gerenciar neste caso** é exibida. 
    
3. Sob **Gerenciar status case**, clique em **reabra caso**.
    
    Será exibido um aviso dizendo que os bloqueios que estavam associados o caso quando ele estava close não ser ativados automaticamente.
    
4. Clique em **Sim** para reabrir o caso. 
    
    O status na página **Gerenciar neste caso** submenu é alterado de **fechado** para **ativo**.
    
5. Feche **Gerenciar neste caso**.
    
6. Na página de **Descoberta eletrônica** , clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** para atualizar o status do caso aberto novamente. Ela pode levar até 60 minutos para que o processo de abertura novamente concluir. 
    
    Quando o processo estiver concluído, o status do caso é alterado para **ativo** na página de **Descoberta eletrônica** . 
    
[Voltar ao início](manage-ediscovery-cases.md#top)
  
## <a name="more-information"></a>Mais informações
<a name="moreinfo_1"> </a>

- **Há qualquer limites para casos de descoberta eletrônica ou isenções associadas a um caso de descoberta eletrônica?** A tabela a seguir lista os limites para casos de eDiscovery e retenções maiusculas.
    
|**Descrição de limite**|**Limite**|
|:-----|:-----|
|Número máximo de casos para uma organização  <br/> |Sem limite  <br/> |
|Número máximo de caso retenções para uma organização  <br/> |10.000  <br/> |
|Número máximo de caixas de correio em uma isenção de ocorrência única  <br/> |1,000  <br/> |
|Número máximo de SharePoint e OneDrive para sites corporativos em uma isenção de ocorrência única  <br/> |100  <br/> |
   
- **Que tal casos em que foram criados na página Gerenciamento de casos no eDiscovery avançado?** Você pode acessar uma lista de casos de eDiscovery avançado mais antigos clicando no link na parte inferior na página de **Descoberta eletrônica** na segurança &amp; Centro de conformidade. No entanto, para fazer qualquer trabalho em um caso mais antigo, você precisa contatar o suporte do Office 365 e solicitar que o caso ser transferido para um novo caso de descoberta eletrônica na segurança &amp; Centro de conformidade. 
    
- **Por que criar uma administrador de descoberta eletrônica?** Como previamente explicado, o administrador é membro do grupo de função Gerenciador de descoberta eletrônica que pode exibir e acessar todos os casos de eDiscovery em sua organização de eDiscovery. Essa capacidade para acessar todos os casos de eDiscovery tem duas finalidades importantes:
    
  - Se uma pessoa que é o único membro de um caso de eDiscovery sair de sua organização, ninguém (incluindo os membros do grupo de funções de gerenciamento da organização ou outro membro do grupo de função de Gerenciador de descoberta eletrônica) pode acessar essa ocorrência de descoberta eletrônica porque elas não seja um membro de um caso. Nessa situação, não deve haver nenhuma maneira de acessar os dados no caso. Mas como um administrador de eDiscovery pode acessar todos os casos de eDiscovery na organização, eles podem exibir o caso na segurança &amp; Centro de conformidade e adicione sozinhos ou outro gerente de descoberta eletrônica como um membro do caso.
    
  - Porque um administrador de eDiscovery pode exibir e acessar todos os casos de eDiscovery, eles podem auditar e acompanhar todos os casos e pesquisas de conteúdo associado. Isso pode ajudar a evitar o uso indevido do pesquisas de conteúdo ou casos de eDiscovery. E descoberta eletrônica administradores pode acessar informações potencialmente confidenciais nos resultados de uma pesquisa de conteúdo, você deve limitar o número de pessoas que são administradores de descoberta eletrônica.
    
    Finalmente, anterior conforme explicado, administradores de descoberta eletrônica na segurança &amp; Centro de conformidade são automaticamente adicionados como administradores no eDiscovery avançado. Isso significa que uma pessoa que é um administrador de descoberta eletrônica pode executar tarefas administrativas na descoberta eletrônica avançada, como configurar usuários, criando casos e adicionar dados para casos.
    
<<<<<<< HEAD
- **Quais são os requisitos de licenciamento para colocar os locais de conteúdo em espera?** Em geral, as organizações exigem uma assinatura do Office 365 E3 ou superior para colocar os locais de conteúdo em espera. Para colocar as caixas de correio em espera, uma licença do Exchange Online plano 2 é necessária. Para obter mais informações, consulte este [eDiscovery FAQ](https://support.office.com/article/9d1a29ae-b7b4-4a27-9c8c-84289023dcae#Q5). =======
- **Quais são os requisitos de licenciamento para colocar os locais de conteúdo em espera?** Em geral, as organizações exigem uma assinatura do Office 365 E3 ou superior para colocar os locais de conteúdo em espera. Para colocar as caixas de correio em espera, uma licença do Exchange Online plano 2 é necessária. Para obter mais informações, consulte este [FAQ](https://support.office.com/article/9d1a29ae-b7b4-4a27-9c8c-84289023dcae.aspx#Q5).
>>>>>>> conversão de deniseb
    
- **o que mais você deve saber sobre a pesquisa de todo o conteúdo maiusculas na etapa 5?** Conforme explicado anteriormente, você pode pesquisar o os locais de conteúdo que foram colocados em espera no caso. Quando você fizer isso, apenas o conteúdo que corresponde aos critérios de espera é pesquisa. Se não houver nenhum critério de espera, todo o conteúdo é pesquisado. Se o conteúdo está em uma consulta com base em espera, somente o conteúdo que ambas as correspondências mantém critérios (da retenção colocado na etapa 4) e os critérios de pesquisa (de pesquisa na etapa 5) é retornado com os resultados da pesquisa.
    
    Aqui estão algumas outras coisas, tenha em mente ao pesquisar todo o conteúdo caso:
    
  - Se um local de conteúdo for parte de vários bloqueios dentro do mesmo caso, as consultas de espera são combinadas por um operador **ou** quando você pesquisa esse local de conteúdo usando a opção de conteúdo todas maiusculas. Da mesma forma, se um local de conteúdo for parte de dois diferentes contém, onde um é baseado em consulta e o outro for uma espera infinita (onde todo o conteúdo é colocado em espera), e em seguida, todo o conteúdo será pesquisa devido à isenção infinita. 
    
  - Se uma pesquisa de conteúdo se destina a um caso e você configurou para pesquisar todo o conteúdo maiusculas e, em seguida, você alterar uma isenção (Adicionar ou remover um local de conteúdo ou alterar a consulta de espera), a configuração de pesquisa é atualizada com essas alterações. No entanto, você precisará executar a pesquisa novamente depois que a suspensão é alterada para atualizar os resultados da pesquisa.
    
  - Se vários bloqueios maiusculas são colocados em um local de conteúdo em um caso de eDiscovery e selecionar para pesquisar todo o conteúdo caso, o número máximo de palavras-chave de consulta de pesquisa que é 500. Isso ocorre porque a pesquisa de conteúdo combina todos os bloqueios baseado em consulta usando o operador **OR** . Se houver que mais de 500 palavras-chave no combinada retenção consultas e a consulta de pesquisa de conteúdo, em seguida, todo o conteúdo na caixa de correio é pesquisado, não apenas se o conteúdo que corresponde a qualquer um dos caso baseado em consulta contém. 
    
  - Se uma isenção maiusculas tem um status de **ativem**, você ainda pode pesquisar os locais de conteúdo maiusculas enquanto a espera está sendo ativada.
    
  - Conforme anteriormente mencionado, se uma pesquisa é configurada para pesquisar em todo o conteúdo de maiusculas, e em seguida, você não pode incluir pesquisa, se você deseja exportar os resultados das pesquisas de várias. Se uma pesquisa estiver configurada para pesquisar todo o conteúdo caso, você terá que exportar os resultados da pesquisa único.
    
- **Sobre o quê fazendo uma pausa no Office 365 grupos e Teams da Microsoft?** Microsoft Teams baseiam-se no Office 365 grupos. Portanto, colocando-os em espera em um caso de eDiscovery é muito semelhante. Mantenha as seguintes coisas em mente ao colocando grupos do Office 365 e Microsoft Teams em espera. 
    
  - Para colocar o conteúdo localizado no Office 365 grupos e Teams da Microsoft em espera, você precisa especificar a caixa de correio e o site do SharePoint que associado a um grupo ou equipe.
    
  - Execute o cmdlet **Get-UnifiedGroup** no Exchange Online para exibir as propriedades de um grupo do Office 365 ou Microsoft Team. Isso é uma boa maneira de obter a URL para o site que está associado a um grupo do Office 365 ou um Team Microsoft. Por exemplo, o comando a seguir exibe propriedades selecionadas para um grupo do Office 365 denominado sênior liderança equipe: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroup** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
  - Quando a caixa de correio do usuário é pesquisada, qualquer grupo do Office 365 ou Microsoft Team que o usuário é membro do não ser pesquisado. Da mesma forma, quando você realiza um grupo do Office 365 ou Microsoft Team espera, somente as caixas de correio de grupo e o site de grupo são colocadas em espera; as caixas de correio e OneDrive para sites corporativos membros do grupo não são colocados em espera, a menos que você os adicione explicitamente à isenção. Portanto, se você a necessidade de colocar um grupo do Office 365 ou Microsoft Team em espera por um motivos legais, considere a adição de caixas de correio e OneDrive para sites corporativos para que membros da equipe e grupo no mesmo espera.
    
  - Para obter uma lista dos membros de um grupo do Office 365 ou Microsoft Team, você pode exibir as propriedades no **inicial \> grupos** página no Centro de administração do Office 365. Como alternativa, você pode executar o seguinte comando no PowerShell do Exchange Online: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroupLinks** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
  - Conversas que fazem parte de um canal de Teams da Microsoft são armazenadas na caixa de correio que está associado a Team Microsoft. Da mesma forma, os arquivos que compartilham de membros da equipe em um canal são armazenados no site do SharePoint da equipe. Portanto, você precisa colocar a caixa de correio do Microsoft Team e site do SharePoint no armazenam para reter conversas e arquivos em um canal.
    
    Como alternativa, conversas que fazem parte da lista de bate-papo no Microsoft Teams são armazenadas na caixa de correio do usuário que participam de bate-papo. E os arquivos que um usuário compartilha em conversas de bate-papo são armazenados em OneDrive para site de negócios do usuário que compartilha o arquivo. Portanto, você precisa colocar as caixas de correio de usuário individual e OneDrive para sites corporativos em espera para reter conversas e arquivos na lista de bate-papo. É por isso que é uma boa ideia fazer uma pausa em caixas de correio dos membros de um Team Microsoft além de fazer a caixa de correio de equipe (e o site) em espera.
    
    > [!IMPORTANT]
    > Os usuários participem de conversas que fazem parte da lista de bate-papo no Microsoft Teams devem ter uma caixa de correio Exchange Online (baseado em nuvem) a fim de manter as conversas de bate-papo quando a caixa de correio é colocada em uma espera de descoberta eletrônica. Isso acontece porque conversas que fazem parte da lista de Chat são armazenadas nas caixas de correio baseadas em nuvem dos participantes bate-papo. Se um participante de bate-papo não tiver uma caixa de correio do Exchange Online, você não conseguirá reter as conversas de bate-papo. Por exemplo, em uma implantação híbrida do Exchange, os usuários com uma caixa de correio local poderá participar de conversas que fazem parte da lista de bate-papo no Microsoft Teams. No entanto nesse caso, o conteúdo desses conversa não pode ser retido porque os usuários não têm caixas de correio baseadas em nuvem. 
  
  - Cada canal Microsoft Team ou equipe contém um Wiki para colaboração e anotações. O conteúdo Wiki automaticamente é salvo em um arquivo com um formato. mht. Este arquivo é armazenado na biblioteca de documentos de equipes Wiki dados no site do SharePoint da equipe. Você pode colocar o conteúdo no Wiki em espera, colocando o site do SharePoint da equipe em espera.
    
    > [!NOTE]
    > A capacidade de reter o conteúdo de Wiki para um canal do Microsoft Team ou equipe (quando o site do SharePoint da equipe você coloca em espera) foi lançada em 22 de junho de 2017. Se um site de equipe estiver em espera, o conteúdo será retido iniciando nessa data de Wiki. No entanto, se um site de equipe está em espera e o conteúdo de Wiki foi excluído antes de 22 de junho de 2017, o conteúdo de Wiki não foi mantido. 
  
- **Como encontrar a URL do OneDrive para sites corporativos?** Para obter uma lista das URLs do OneDrive para sites corporativos em sua organização para que você possa adicioná-los a uma isenção ou de pesquisa associado a um caso de eDiscovery, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Esse script neste artigo cria um arquivo de texto que contém uma lista de todos os sites de OneDrive. Para executar esse script, você precisará instalar e usar o Shell de gerenciamento do SharePoint Online. Certifique-se de que inclua o URL para o domínio de meusite da sua organização para cada site de OneDrive que você deseja pesquisar. Este é o domínio que contém todos os seu OneDrive; Por exemplo, `https://contoso-my.sharepoint.com`. Aqui está um exemplo de URL de um site do usuário OneDrive: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
