---
title: Gerenciar isenções na descoberta eletrônica avançada (versão prévia)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe6ab3a1e1108e9ab2e4fc201357b72a77453d38
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295714"
---
# <a name="manage-holds-in-advanced-ediscovery-preview"></a>Gerenciar isenções na descoberta eletrônica avançada (versão prévia)

Você pode usar um caso de descoberta eletrônica avançada (visualização) para criar isenções para preservar o conteúdo que pode ser relevante para seu caso. Usando os recursos de descoberta eletrônica avançada (visualização), você pode colocar suspensões em responsáveis e em suas fontes de dados. Além disso, você pode colocar um bloqueio não custodial em caixas de correio e sites do OneDrive for Business. Você também pode colocar uma retenção na caixa de correio de grupo, site do SharePoint e no OneDrive for Business para um grupo do Office 365. Da mesma forma, você pode colocar uma retenção na caixa de correio e no site associados ao Microsoft Teams. Quando você coloca os locais de conteúdo em espera, o conteúdo é mantido até que você libere os responsáveis, remova um local de dados específico ou exclua a política de retenção totalmente.

## <a name="manage-custodian-based-holds"></a>Gerenciar bloqueios baseados em responsáveis

Em alguns casos, você pode ter um conjunto de responsáveis por dados identificados e optar por preservá-los. Na descoberta eletrônica avançada (visualização), quando esses responsáveis são colocados em espera, o usuário e suas fontes de dados selecionadas são adicionados automaticamente a uma política de retenção de responsáveis. 

Para exibir a política de retenção de responsáveis:

1. No **centro de conformidade do & de segurança**, clique em descoberta eletrônica avançada do **> (visualização)** para exibir a lista de casos em sua organização.
   
2. Vá para a guia **responsáveis** para adicionar os responsáveis dentro do seu caso. Para saber como adicionar e colocar os responsáveis em espera em um caso de descoberta eletrônica avançada (visualização), confira [Adicionar responsáveis a uma descoberta eletrônica avançada (visualização)](add-custodians-to-case.md). Se você já tiver adicionado os responsáveis e os colocou em espera, vá para a etapa 3.
   
3. Vá até a guia **isenções** e selecione "política de responsáveis".
   
4. Na página do menu suspenso, você pode ver estatísticas de retenção da política. Você também pode executar ações como aplicar uma consulta à sua retenção baseada em responsáveis. Para obter mais informações sobre como criar uma consulta de retenção e usar condições, consulte [keyword queries and Search Conditions for Content Search](../keyword-queries-and-search-conditions.md).
 
## <a name="manage-non-custodial-holds"></a>Gerenciar suspensões não custodial

Ao criar uma isenção, você tem as seguintes opções para fazer o escopo do conteúdo mantido nos locais de conteúdo especificado:

  - Você cria uma retenção infinita onde todo o conteúdo é colocado em espera. Como alternativa, você pode criar uma isenção baseada em consulta, onde somente o conteúdo que corresponde a uma consulta de pesquisa é colocado em espera.
  - Você pode especificar um intervalo de datas para armazenar somente o conteúdo que foi enviado, recebido ou criado dentro desse intervalo de datas. Como alternativa, você pode manter todo o conteúdo independentemente de quando ele foi enviado, recebido ou criado.

Para criar uma retenção para um caso de descoberta eletrônica avançada (visualização):

1. No **centro de conformidade do & de segurança**, clique em descoberta eletrônica avançada do **> (visualização)** para exibir a lista de casos em sua organização.
  
2. Clique em **abrir** ao lado do caso para o qual você deseja criar as isenções.
  
3. Na home page do caso, clique na guia **isenções** .
  
4. Na guia **isenções** , clique em **criar**.
  
5. Na página **nomear sua suspensão** , dê um nome à isenção. O nome da retenção deve ser exclusivo em sua organização.
 
6. Opcion Na caixa **Descrição** , adicione uma descrição da isenção.
  
7. Clique em **Avançar**.
  
8. Escolha os locais de conteúdo que você deseja colocar em espera. Você pode colocar caixas de correio, sites e pastas públicas em espera.

   a. **email do Exchange** -clique em **escolher usuários, grupos ou equipes** e, em seguida, clique em **escolher usuários, grupos ou equipes** novamente para especificar as caixas de correio a serem colocadas em espera. Use a caixa de pesquisa para localizar caixas de correio de usuários e grupos de distribuição (para colocar uma retenção nas caixas de correio dos membros do grupo) para colocar em espera. Você também pode colocar uma retenção na caixa de correio associada para um grupo do Office 365 ou uma equipe da Microsoft. Marque a caixa de seleção usuário, grupo, equipe, clique em **escolher**e em **concluído**.
 
    > [!NOTE]
    > Ao clicar em **escolher usuários, grupos ou equipes** para especificar as caixas de correio que serão colocadas em espera, o seletor de caixa de correio exibido estará vazio. Isso é projetado para melhorar o desempenho. Para adicionar pessoas a esta lista, digite um nome (no mínimo 3 caracteres) na caixa de pesquisa.

    b. **sites do SharePoint** -clique em **escolher sites** e clique em **escolher sites** novamente para especificar o SharePoint e os sites do onedrive for Business para colocar em espera. Digite a URL de cada site que você deseja colocar em espera. Você também pode adicionar a URL do site do SharePoint para um grupo do Office 365 ou uma equipe da Microsoft. Clique em **escolher**e em **concluído**.
    
     Consulte a seção **perguntas frequentes** para obter dicas sobre como colocar grupos do Office 365 e o Microsoft Teams em espera.

    > [!NOTE]
    > No caso raro que o UPN (nome principal de usuário) de uma pessoa tenha mudado, a URL de sua conta do OneDrive também será alterada para incorporar o novo UPN. Se isso acontecer, você terá que modificar a retenção adicionando a nova URL do OneDrive do usuário e removendo a antiga.

     c. **pastas públicas do Exchange** -mova o comutador alternar para a posição All para colocar todas as pastas públicas em sua organização do Exchange Online em espera. Observe que você não pode escolher pastas públicas específicas para colocar em espera. Deixe a opção de alternância definida como **nenhuma** se você não quiser colocar uma retenção em pastas públicas.

9. Quando você terminar de adicionar locais de conteúdo à isenção, clique em **Avançar**.
  
10. Para criar uma retenção baseada em consulta com condições, conclua o seguinte. Caso contrário, basta clicar em **Avançar**.
    
    - Na caixa em **palavras-chave**, digite uma consulta de pesquisa na caixa para que apenas o conteúdo que atende aos critérios de pesquisa seja colocado em espera. Você pode especificar palavras-chave, propriedades de mensagem ou propriedades do documento, como nomes de arquivo. Você também pode usar consultas mais complexas que usam um operador Boolean, como e, ou ou não. Se você deixar a caixa de palavras-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificado será colocado em espera.

    - Clique em **Adicionar** condições para adicionar uma ou mais condições para restringir a consulta de pesquisa para a isenção. Cada condição adiciona uma cláusula à consulta de pesquisa KQL que é criada e executada quando você cria a retenção. Por exemplo, você pode especificar um intervalo de datas para que os documentos de email ou de site criados dentro do intervalo de datas sejam colocados em espera. Uma condição é conectada logicamente à consulta de palavra-chave (especificada na caixa palavra-chave) pelo operador AND. Isso significa que os itens precisam satisfazer a consulta de palavra-chave e a condição a ser colocada em espera.

     Para obter mais informações sobre como criar uma consulta de pesquisa e usar condições, consulte [keyword queries and Search Conditions for Content Search](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

12. Depois de configurar um bloqueio baseado em consulta, clique em **Avançar**.
 
13. Revise suas configurações e clique em **criar esta isenção**.


## <a name="view-hold-statistics"></a>Exibir estatísticas de retenção

Após algum tempo, as informações sobre a nova retenção são exibidas no painel de detalhes na guia **isenções** para a isenção selecionada. Essas informações incluem o número de caixas de correio e sites em espera e estatísticas sobre o conteúdo que foi colocado em espera, como o número total e o tamanho de itens colocados em retenção e a última vez que as estatísticas de retenção foram calculadas. Essas estatísticas de isenção ajudam você a identificar quanto conteúdo relacionado à ocorrência de descoberta eletrônica está sendo mantido.

Tenha em mente as seguintes coisas em relação a estatísticas de retenção:

- O número total de itens em retenção indica o número de itens de todas as fontes de conteúdo que são colocadas em espera. Se você tiver criado uma retenção baseada em consulta, essa estatística indicará o número de itens que correspondem à consulta.
  
- O número de itens em retenção também inclui itens não indexados encontrados nos locais de conteúdo. Observe que, se você criar uma retenção baseada em consulta, todos os itens não indexados nos locais de conteúdo serão colocados em espera. Isso inclui itens não indexados que não correspondem aos critérios de pesquisa de um bloqueio baseado em consulta e itens não indexados que podem ficar fora de uma condição de intervalo de datas. Isso é diferente do que acontece quando você executa uma pesquisa de conteúdo, na qual os itens não indexados que não correspondem à consulta de pesquisa ou são excluídos por uma condição de intervalo de datas não são incluídos nos resultados da pesquisa. Para obter mais informações sobre itens não indexados, confira [itens parcialmente indexados na pesquisa de conteúdo no Office 365](../partially-indexed-items-in-content-search.md). 

- Você pode obter as estatísticas de retenção mais recentes clicando em atualizar estatísticas para executar novamente uma estimativa de pesquisa que calcula o número atual de itens em retenção.

- Se necessário, clique em atualizar na barra de ferramentas para atualizar as estatísticas de retenção no painel de detalhes.

- É normal para o número de itens em espera aumentar ao longo do tempo, pois os usuários cuja caixa de correio ou site está em espera geralmente estão enviando ou recebendo novas mensagens de email e criando novos documentos do SharePoint e do OneDrive for Business.

- Se um site do SharePoint ou uma conta do OneDrive for movido para uma região diferente em um ambiente multigeográfico, as estatísticas desse site não serão incluídas nas estatísticas de retenção. No enTanto, o conteúdo do site permanecerá em espera. Além disso, se um site for movido para uma região diferente, a URL exibida na retenção não será atualizada. Você terá que editar a isenção e atualizar a URL.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

- **Como mapear outros grupos do Office 365 ou site do Microsoft Teams para um? E como colocar um bloqueio não custodial nos grupos do Office 365 e no Microsoft Teams?** O Microsoft Teams é desenvolvido em grupos do Office 365. Portanto, colocá-los em espera em um caso de descoberta eletrônica é muito semelhante. Lembre-se do seguinte ao colocar grupos do Office 365 e do Microsoft Teams em espera.
  - Para colocar o conteúdo localizado nos grupos do Office 365 e no Microsoft Teams em espera, você precisa especificar a caixa de correio e o site do SharePoint que estão associados a um grupo ou a uma equipe.
  
  - Execute o cmdlet **Get-** unificado no Exchange Online para exibir as propriedades de um grupo do Office 365 ou equipe da Microsoft. Essa é uma boa maneira de obter a URL do site que está associado a um grupo do Office 365 ou a uma equipe da Microsoft. Por exemplo, o comando a seguir exibe as propriedades selecionadas de um grupo do Office 365 chamado equipe de liderança sênior:


    ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > Para executar o cmdlet Get-uniFicado, você deve receber a função de destinatários somente para exibição no Exchange Online ou ser um membro de um grupo de função atribuído à função de destinatários somente para exibição.

 - Quando a caixa de correio de um usuário é pesquisada, qualquer grupo do Office 365 ou Microsoft Team do qual o usuário é membro não será pesquisado. Da mesma forma, quando você coloca um grupo do Office 365 ou um bloqueio de equipe da Microsoft, somente a caixa de correio de grupo e o site de grupo são colocados em espera; as caixas de correio e os sites do OneDrive for Business de membros do grupo não são colocados em espera, a menos que você os adicione explicitamente como responsáveis ou coloque suas fontes de dados em espera. Portanto, se você precisar colocar um grupo do Office 365 ou o Microsoft Team em espera para um determinado local, considere o mapeamento do site de grupo e da caixa de correio de grupo para os responsáveis (consulte Gerenciando os responsáveis em descoberta eletrônica avançada (prévia)). Se o grupo do Office 365 ou a equipe da Microsoft não puder ser atribuído a um único membro, considere a adição da origem a um bloqueio não custodial. 
 
 - Para obter uma lista dos membros de um grupo do Office 365 ou de uma equipe da Microsoft, você pode exibir as propriedades na página de grupos de > domésticos no centro de administração do Office 365. Como alternativa, você pode executar o seguinte comando no PowerShell do Exchange Online:

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroupLinks** , você deve ser atribuído à função de destinatários somente para exibição no Exchange Online ou ser um membro de um grupo de função atribuído à função de destinatários somente para exibição.

- As conversas de canal que fazem parte de um canal do Microsoft Teams são armazenadas na caixa de correio que está associada à equipe. Da mesma forma, os arquivos que os membros da equipe compartilham em um canal são armazenados no site do SharePoint da equipe. Portanto, você precisa colocar a caixa de correio do Microsoft Team e o site do SharePoint em espera para reter conversas e arquivos em um canal.
  
- Como alternativa, as conversas que fazem parte da lista de chat no Microsoft Teams são armazenadas na caixa de correio do usuário que participa do chat.  Os arquivos que um usuário compartilha em conversas de chat são armazenados no site do OneDrive for Business do usuário que compartilha o arquivo. Portanto, você precisa colocar as caixas de correio de usuários individuais e os sites do OneDrive for Business em retenção para reter conversas e arquivos na lista de chat. 
  
- Cada equipe do Microsoft ou canal de equipe contém um wiki para anotações e colaboração. O conteúdo wiki é automaticamente salvo em um arquivo com um formato. mht. Esse arquivo é armazenado na biblioteca de documentos de dados wiki do teams no site do SharePoint da equipe. Você pode colocar o conteúdo do wiki em espera, colocando o site do SharePoint da equipe em espera.

  > [!NOTE]
  > A capacidade de manter o conteúdo do wiki para uma equipe do Microsoft ou um canal de equipe (quando você coloca o site do SharePoint da equipe em espera) foi lançada em 22 de junho de 2017. Se um site de equipe estiver em espera, o conteúdo wiki será retido a partir dessa data. No enTanto, se um site de equipe estiver em espera e o conteúdo wiki tiver sido excluído antes de 22 de junho de 2017, o conteúdo wiki não foi mantido.
