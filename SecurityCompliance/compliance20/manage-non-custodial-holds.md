---
title: Gerenciar isenções no eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 75ddbcfb401d285dfb7a4b610e3f0709e21946f2
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607344"
---
# <a name="rename-this-page-and-md-file-to-managing-holds"></a>Renomear esta página e o arquivo de MD para "Gerenciando retenções"

# <a name="holds-in-advanced-ediscovery-preview"></a>Isenções no eDiscovery avançado (Preview)
Você pode usar um caso de eDiscovery avançado (Preview) para criar pausas para preservar o conteúdo que pode ser relevante ao seu caso. Usando o eDiscovery avançado (Preview) mantenha recursos, você pode colocar isenções em responsáveis e suas fontes de dados. Além disso, você pode colocar uma isenção não custódia em caixas de correio e OneDrive para sites corporativos. Você também pode fazer uma pausa na caixa de correio de grupo, site do SharePoint e OneDrive para o site de negócios para um grupo do Office 365. Da mesma forma, você pode colocar uma pausa no site que estão associados a Teams da Microsoft e da caixa de correio. Quando você realiza locais de conteúdo em espera, o conteúdo é retido até que você liberar dos responsáveis, remove um local de dados específicos ou excluir a política de retenção inteiramente.

## <a name="manage-custodian-based-holds"></a>Gerenciar dos responsáveis com base em isenções

Em alguns casos, você pode ter um conjunto de responsáveis de dados que você identificou e escolhidos para preservar. No eDiscovery avançado (Preview), quando esses responsáveis forem colocadas no thold, o usuário e seus dados selecionados fontes serão automaticamente adicionadas a um funcionário encarregado espera política. 

Para exibir a política de retenção dos responsáveis:

1. No **Centro de conformidade de & de segurança**, clique em **eDiscovery avançado do eDiscovery gt _ (Preview)** para exibir a lista de ocorrências em sua organização.
   
2. Navegue até a guia **responsáveis** para adicionar responsáveis dentro de seu caso. Para saber como você pode adicionar e responsáveis colocar em espera dentro de um caso de eDiscovery avançado (Preview), visite a seção **Gerenciando responsáveis dentro de um caso** . Se você já tiver adicionado responsáveis e colocou em espera, mova para a etapa 3.
   
3. Navegue até a guia **contém** e selecione a política dos responsáveis' '.
   
4. O submenu de detalhes, você pode ver as estatísticas de sua política de retenção. Você também pode executar ações como aplicar uma consulta ao seu bloqueio baseado em dos responsáveis. Para obter mais informações sobre como criar uma consulta de espera e condições de uso, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions )
 
## <a name="manage-non-custodial-holds"></a>Gerenciar isenções não custódia
Quando você cria uma pausa, você tem as seguintes opções para o conteúdo que é mantido nos locais especificados conteúdos de escopo:
  - Criar uma espera infinita, onde todo o conteúdo é colocado em espera. Como alternativa, é possível criar uma isenção baseado em consulta onde somente o conteúdo que corresponda a uma consulta de pesquisa é colocado em espera.
  - Você pode especificar um intervalo de datas para reter somente o conteúdo que foi enviado, recebido ou criado dentro desse intervalo de datas. Como alternativa, você pode manter todo o conteúdo independentemente de quando ela foi enviada, recebida ou criada.

Para criar uma isenção para um caso de eDiscovery:
  1. No **Centro de conformidade de & de segurança**, clique em **eDiscovery avançado do eDiscovery gt _ (Preview)** para exibir a lista de ocorrências em sua organização.
  
  2. Ao lado do que você deseja criar os bloqueios no caso, clique em Abrir.
  
  3. Na guia**início** para o caso, clique na guia **contém** .
  
  4. Na guia **contém** , clique em **criar**.
  
  5. No nome de sua página de retenção, nomeie a suspensão. O nome da isenção deve ser exclusivo na sua organização.
 
  6. (Opcional) Na caixa Descrição, adicione uma descrição da isenção.
  
  7. Clique em **Avançar**.
  
  8. Escolha os locais de conteúdo que você deseja colocar em espera. Você pode colocar pastas públicas, sites e caixas de correio em espera. r. de **email do Exchange** – clique em **Escolher usuários, grupos ou equipes** e, em seguida, clique em **Escolher usuários, grupos ou equipes** novamente. para especificar as caixas de correio para colocar em espera. Use a caixa Pesquisar para localizar caixas de correio de usuário e grupos de distribuição (para colocar uma isenção em caixas de correio dos membros do grupo) deve ser colocado em espera. Você também pode fazer uma pausa na caixa de correio associada para um Team Microsoft ou de um grupo do Office 365. Selecione o usuário, grupo, caixa de seleção de equipe, clique em **Escolher**e, em seguida, clique em **concluído**.
 
    [!NOTE]
    Quando você clica **Escolher usuários, grupos ou equipes** para especificar as caixas de correio deve ser colocado em espera, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar pessoas a essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar.


    b. **Sites do SharePoint** - clique em **sites de escolha** e clique em **Escolher sites** novamente para especificar SharePoint e OneDrive para sites corporativos para colocar em espera. Digite a URL para cada site que você deseja colocar em espera. Você também pode adicionar a URL do site do SharePoint para um Team Microsoft ou de um grupo do Office 365. Clique em **Escolher**e, em seguida, clique em **concluído**.
    
     Consulte a seção de **perguntas Frequentes** para obter dicas sobre a colocação de grupos do Office 365 e Teams da Microsoft em espera.

    [!NOTE]
    No caso raro que mudou o nome principal de usuário de uma pessoa (UPN), a URL para a sua conta de OneDrive também será alterada para incorporar o UPN novo. Se isso acontecer, você terá que modificar a retenção a nova URL do usuário de OneDrive de adicionando e removendo o antigo.

     c. **pastas públicas do Exchange** - mover o switch de alternância para a posição de todos os colocar todas as pastas públicas em seu Exchange Online organização em espera. Observe que não é possível escolher específicos de pastas públicas para colocar em espera. Deixe o switch de alternância definido como **Nenhuma** , se não desejar colocar um bloqueio em pastas públicas.

  9. Quando você terminar de adicionar locais de conteúdo à isenção, clique em **Avançar**.
  
  10. Para criar uma isenção baseado em consulta com condições, conclua o seguinte. Caso contrário, basta clicar em **Avançar**. 1.1 na caixa em palavras-chave, tipo de uma consulta de pesquisa na caixa de modo que somente o conteúdo que satisfaz os critérios de pesquisa é colocado em espera. Você pode especificar palavras-chave, propriedades de mensagem ou propriedades de documento, como nomes de arquivo. Você também pode usar as consultas mais complexas que usam um operador booleano, como AND, OR ou não. Se você deixar a caixa de palavra-chave vazia, e em seguida, todo o conteúdo localizado nos locais de conteúdo especificados será colocado em espera.

    1.2 Clique em **Adicionar** condições para adicionar uma ou mais condições para restringir a consulta de pesquisa para a retenção. Cada condição adiciona uma cláusula à consulta KQL pesquisa que é criada e executada quando você cria o bloqueio. Por exemplo, você pode especificar um intervalo de datas para que os documentos de email ou site que foram criados dentro da intervalo de data são colocados em espera. Uma condição logicamente está conectada à consulta de palavra-chave (especificada na caixa de palavra-chave) pelo operador AND. Isso significa que o item deve satisfazer ambos a consulta de palavra-chave e a condição sejam colocadas em espera.

     Para obter mais informações sobre como criar uma consulta de pesquisa e condições de uso, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

  11. Depois de configurar uma consulta com base em espera, clique em **Avançar**.
 
  12. Revise suas configurações e clique em **criar esta isenção**.


## <a name="view-hold-statistics"></a>Exibir estatísticas de espera
Após algum tempo, informações sobre a nova isenção são exibidas no painel de detalhes, na guia **contém** referente à isenção selecionada. Essas informações incluem o número de caixas de correio e sites em espera e estatísticas sobre o conteúdo que foi colocado em espera, como o número total e o tamanho dos itens colocados em espera e a última vez que a suspensão estatísticas foram calculadas. Mantenha a Ajuda de estatísticas que identificar a quantidade de conteúdo que está relacionada ao caso de eDiscovery está sendo mantido.

Mantenha as seguintes coisas em mente sobre estatísticas de espera:

  - O número total de itens em espera indica o número de itens de todas as fontes de conteúdo que são colocadas em espera. Se você criou uma consulta com base em espera, essa estatística indica o número de itens que correspondem à consulta.
  - O número de itens em espera também inclui itens indexados encontrados em locais de conteúdo. Observe que, se você criar uma isenção baseado em consulta, todos os itens indexados os locais de conteúdo são colocados em espera. Isso inclui itens indexados que não correspondem aos critérios de pesquisa de uma isenção baseado em consulta e não indexadas que poderão ficar fora de uma condição de intervalo de data. Isso é diferente do que o que acontece quando você executa uma pesquisa de conteúdo, na qual os itens indexados que não correspondem à consulta de pesquisa ou são excluídos por uma condição de intervalo de data não estão incluídos nos resultados da pesquisa. Para obter mais informações sobre os itens não indexadas, consulte [itens parcialmente indexados na pesquisa de conteúdo no Office 365] (https://docs.microsoft.com/en-us/office365/SecurityCompliance/partially-indexed-items-in-content-search). 
  - Você pode obter as estatísticas de espera mais recentes clicando em estatísticas de atualização para executar novamente uma estimativa de pesquisa que calcula o número atual de itens em espera.
  - Se necessário, clique em Atualizar na barra de ferramentas para atualizar as estatísticas de espera no painel de detalhes.
  - De TI normal para o número de itens em espera para aumentar ao longo do tempo porque os usuários cujas caixas de correio ou o site está em retenção são geralmente enviando ou recebendo a nova mensagem de email e criando novo SharePoint e OneDrive para documentos de negócios.

[!NOTE]
Se um site do SharePoint ou a conta do OneDrive for movida para uma região diferente em um ambiente multi-geo, as estatísticas para esse site não serão incluídas nas estatísticas de espera. No entanto, o conteúdo do site ainda estará em espera. Além disso, se um site é movido para uma região diferente a URL que é exibida na isenção não será atualizada. Você terá que editar a retenção e atualizar a URL.

## <a name="faq"></a>Perguntas frequentes
- Como mapear um site do Office 365 grupos ou Microsoft Teams adicional para um funcionário encarregado de **? Sobre o quê colocar um não-custódia pressionada nos grupos do Office 365 e Microsoft Teams?** Microsoft Teams baseiam-se no Office 365 grupos. Portanto, colocando-os em espera em um caso de eDiscovery é muito semelhante. Mantenha as seguintes coisas em mente ao colocando grupos do Office 365 e Microsoft Teams em espera.
  - Para colocar o conteúdo localizado no Office 365 grupos e Teams da Microsoft em espera, você precisa especificar a caixa de correio e o site do SharePoint que associado a um grupo ou equipe.
  
  - Execute o cmdlet **Get-UnifiedGroup** no Exchange Online para exibir as propriedades de um grupo do Office 365 ou Microsoft Team. Isso é uma boa maneira de obter a URL para o site que está associado a um grupo do Office 365 ou um Team Microsoft. Por exemplo, o comando a seguir exibe propriedades selecionadas para um grupo do Office 365 denominado sênior liderança equipe:

' ' powershell

    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    '''

 [!NOTE]
 Para executar o cmdlet Get-UnifiedGroup, você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição.

 - Quando a caixa de correio do usuário é pesquisada, qualquer grupo do Office 365 ou Microsoft Team que o usuário é membro do não ser pesquisado. Da mesma forma, quando você realiza um grupo do Office 365 ou Microsoft Team espera, somente as caixas de correio de grupo e o site de grupo são colocadas em espera; as caixas de correio e OneDrive para sites corporativos membros do grupo não são colocados em espera, a menos que você explicitamente adicioná-los como responsáveis ou coloca seu espera de fontes de dados. Portanto, se você a necessidade de colocar um grupo do Office 365 ou Microsoft Team em espera para dos responsáveis específico, considere a possibilidade de mapear o site de grupo e a caixa de correio de grupo para dos responsáveis (consulte Gerenciando responsáveis no eDiscovery avançado (Preview)). Se o grupo do Office 365 ou Microsoft Team não for atribuído a dos responsáveis único, considere a adição de espera a fonte de um não-custódia. 
 
 - Para obter uma lista dos membros de um grupo do Office 365 ou Microsoft Team, você pode exibir as propriedades na página Home gt _ grupos no Centro de administração do Office 365. Como alternativa, você pode executar o seguinte comando no PowerShell do Exchange Online:

    ' ' powershell
    
        Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
        '''

[!NOTE]
Para executar o cmdlet Get-UnifiedGroupLinks, você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição.

- Conversas de canal que fazem parte de um canal de Teams da Microsoft são armazenadas na caixa de correio que está associado a equipe. Da mesma forma, os arquivos que compartilham de membros da equipe em um canal são armazenados no site do SharePoint da equipe. Portanto, você precisa colocar a caixa de correio do Microsoft Team e site do SharePoint no armazenam para reter conversas e arquivos em um canal.
  
- Como alternativa, conversas que fazem parte da lista de bate-papo no Microsoft Teams são armazenadas na caixa de correio do usuário que participam de bate-papo.  Arquivos que um usuário compartilha em conversas de bate-papo são armazenados em OneDrive para site de negócios do usuário que compartilha o arquivo. Portanto, você precisa colocar as caixas de correio de usuário individual e OneDrive para sites corporativos em espera para reter conversas e arquivos na lista de bate-papo. 
  
- Cada canal Microsoft Team ou equipe contém um Wiki para colaboração e anotações. O conteúdo Wiki automaticamente é salvo em um arquivo com um formato. mht. Este arquivo é armazenado na biblioteca de documentos de equipes Wiki dados no site do SharePoint da equipe. Você pode colocar o conteúdo no Wiki em espera, colocando o site do SharePoint da equipe em espera.

[!Note]
A capacidade de reter o conteúdo de Wiki para um canal do Microsoft Team ou equipe (quando o site do SharePoint da equipe você coloca em espera) foi lançada em 22 de junho de 2017. Se um site de equipe estiver em espera, o conteúdo será retido iniciando nessa data de Wiki. No entanto, se um site de equipe está em espera e o conteúdo de Wiki foi excluído antes de 22 de junho de 2017, o conteúdo de Wiki não foi mantido.
   