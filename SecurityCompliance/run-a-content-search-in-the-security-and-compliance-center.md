---
title: Executar uma pesquisa de conteúdo com a segurança do Office 365 &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: 'Usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para pesquisar caixas de correio, sites do SharePoint Online e OneDrive para locais de negócios. '
ms.openlocfilehash: 61c6c3933a75567acb04f793cb6815322fb3fada
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523898"
---
# <a name="run-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Executar uma pesquisa de conteúdo com a segurança do Office 365 &amp; Centro de conformidade

Você pode usar a ferramenta de descoberta eletrônica de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar itens como email, documentos e conversas em sua organização do Office 365 de mensagens instantâneas. Use essa ferramenta para procurar itens nesses serviços do Office 365:
  
- Caixas de correio do Exchange Online e as pastas públicas
    
- SharePoint Online e OneDrive para sites corporativos
    
- Skype para conversas de negócios
    
- Microsoft Teams 
    
- Grupos do Office 365
    
Pesquisa de conteúdo é uma nova ferramenta de pesquisa de descoberta eletrônica com os recursos novos e aprimorados de dimensionamento e desempenho. Use a pesquisa de conteúdo para executar pesquisas de descoberta eletrônica muito grande. Você pode pesquisar todas as caixas de correio, todas as pastas públicas do Exchange e todos os sites do SharePoint Online e OneDrive para contas de negócios em uma única pesquisa de conteúdo. Não há nenhum limite no número de locais de conteúdo que você pode pesquisar. Também há nenhum limite no número de pesquisas que podem ser executados ao mesmo tempo. Depois de executar uma pesquisa de conteúdo, o número de locais de conteúdo e um número estimado dos resultados da pesquisa é exibido no painel de detalhes, na página de **pesquisa de conteúdo** . Depois de executar uma pesquisa, você pode visualizar os resultados, obtenha as estatísticas de palavra-chave para uma ou mais pesquisas, editar em massa pesquisas de conteúdo e exportar os resultados para um computador local. 
  
 **Sumário**
  
[Criar uma pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[Exportar resultados de pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[Visualização de resultados de pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[Atualizar os resultados da pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[Editar uma pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[Repetir uma pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>Antes de começar

- Para informações e orientação sobre a criação de consultas de pesquisa e usando operadores de pesquisa booleana, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md). Este artigo também contém informações sobre como pesquisar tipos de informações confidenciais e procura por conteúdo que é compartilhado com pessoas de dentro e fora da sua organização.
    
- Para ter acesso à página **pesquisa de conteúdo** para realizar pesquisas e visualizar e exportar os resultados da pesquisa, um administrador, responsável pela conformidade ou gerente de descoberta eletrônica deve ser membro do grupo de função do Gerenciador de descoberta eletrônica na segurança &amp; conformidade Centro. Você não precisa atribuir permissões de pesquisa adicionais no Exchange Online, SharePoint Online, ou onedrive para sites corporativos. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
    
- Há limites aplicados a pesquisa de conteúdo para manter a integridade e a qualidade dos serviços fornecidos para organizações do Office 365. Na maioria dos casos, você não pode modificar esses limites, mas você deve estar ciente deles para que você possa tirar esses limites em consideração ao planejamento, execução e pesquisas de solução de problemas. Para obter mais informações, consulte [limites para pesquisa no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md).
    
- Consulte a seção para tempos de pesquisa estimados com base no número de caixas de correio pesquisadas em uma única pesquisa de conteúdo. 
    
- Conforme indicado anteriormente, você pode usar a pesquisa de conteúdo para procurar conteúdo em grupos do Office 365 e Microsoft Teams. Isso significa que você pode pesquisar a caixa de correio de grupo, calendário compartilhado e sites do SharePoint associados a um grupo do Office 365 e um Team Microsoft. Além disso, você pode pesquisar as conversas de canal no Team Microsoft. Para obter informações sobre grupos do Office 365 e Teams da Microsoft, consulte:
    
  - [Saiba mais sobre os grupos do Office 365](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [Ajuda do Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Consulte a seção para obter dicas sobre a pesquisa de conteúdo no Office 365 grupos e Teams da Microsoft. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>Criar uma pesquisa
<a name="create"> </a>

1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisa&amp; investigação** \> **Pesquisa de Conteúdo**.
    
4. Clique em **Novo**![Ícone Adicionar](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
5. Na página **Nova pesquisa**, digite um nome para a Pesquisa de Conteúdo. O nome deve ser exclusivo em sua organização. 
    
6. Escolha os locais de conteúdo que você deseja pesquisar. Você pode pesquisar caixas de correio, sites e pastas públicas na mesma pesquisa.
    
    ![Escolher os locais de conteúdo que você deseja pesquisar](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **Pesquisa em todos os lugares** Selecione essa opção para pesquisar todos os locais de conteúdo na sua organização. Quando você seleciona essa opção, você pode optar por pesquisar todas as caixas de correio (incluindo as caixas de correio e de caixas de correio inativas para todos os grupos do Office 365 e Microsoft Teams), SharePoint e o OneDrive para sites corporativos (que inclui os sites para todos os grupos do Office 365 e Equipes da Microsoft) e todas as pastas públicas.
    
    ![Clique em todos os lugares, a pesquisa opção para pesquisar todos os locais de conteúdo](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **Seleção de local personalizado** Selecione essa opção para selecionar as caixas de correio e os sites que você deseja pesquisar. Se você escolher essa opção, você tem a flexibilidade para pesquisar todos os locais de conteúdo para um serviço específico (por exemplo, pesquisar todas as caixas de correio do Exchange) ou você pode pesquisar locais de conteúdo específico para um serviço do Office 365.
    
    Lembre-se do seguinte ao adicionar locais de conteúdo para pesquisa:
    
    **Caixas de correio**
    
  - Quando você clicar em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para especificar as caixas de correio para pesquisar, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar destinatários para essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar e clique em **Pesquisar**![ícone de busca](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif).
    
  - Você pode adicionar caixas de correio inativas e grupos de distribuição à lista de caixas de correio a ser pesquisado. Para grupos de distribuição, as caixas de correio de membros de grupo são pesquisadas. Observe que os grupos dinâmicos de distribuição não são suportados.
    
  - Para obter uma lista das caixas de correio inativas em sua organização, execute o comando `Get-Mailbox -InactiveMailboxOnly` no PowerShell do Exchange Online. Como alternativa, você pode ir para **governança de dados** \> **retenção** na segurança &amp; Centro de conformidade e clique em **mais**![elipses da barra de navegação](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **caixas de correio inativas**.
    
  - Você também pode adicionar a caixa de correio que está associado a um grupo do Office 365 ou um Team Microsoft. Nesse caso, apenas, a caixa de correio grupo ou equipe é pesquisada; as caixas de correio dos membros da equipe ou de grupo não são pesquisadas. Para pesquisá-los, você precisará especificamente adicioná-los à pesquisa.
    
  - Se você não quiser incluir qualquer caixas de correio para a pesquisa, selecione **Escolher caixas de correio específicas para pesquisar**, mas não adicionar uma caixa de correio à lista.
    
    **Sites**
    
  - Clique em **Adicionar**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para adicionar sites à pesquisa. Digite a URL para cada site que você deseja pesquisar. A ferramenta de pesquisa de conteúdo será validar a URL e, em seguida, adicioná-lo à lista de sites a ser pesquisado. 
    
  - Você pode adicionar o que está associado a um grupo do Office 365 ou Team um Microsoft SharePoint. Consulte a seção para obter orientação sobre como localizar a URL para o grupo ou equipe. 
    
  - Se você não quiser incluir todos os sites em uma pesquisa, selecione **Escolher a sites específicos para pesquisar**, mas não adicionar um site à lista.
    
    **Pastas públicas**
    
    Para pastas públicas, você pode optar por pesquisar todas as pastas públicas em sua organização do Exchange Online ou não a pesquisa de pastas públicas.
    
7. Clique em **Avançar**.
    
8. Na página **Nova pesquisa**, você pode adicionar palavras-chave e condições para criar a consulta de pesquisa. 
    
    ![Criar uma consulta de pesquisa com palavras-chave e condições](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. Na caixa em **que você deseja fazer conosco para procurar?**, digite uma consulta de pesquisa na caixa. Você pode especificar palavras-chave, mensagem propriedades tais como enviados e recebidos datas, ou propriedades de documento, como nomes de arquivo ou a data em que um documento foi alterada pela última vez. Você pode usar um consultas mais complexas que usam um operador booleano, como **AND**, **ou**, **não**, **NEAR**ou **ONEAR**. Você também pode pesquisar informações confidenciais (por exemplo, números do seguro social) em documentos ou procurar documentos que foram compartilhados externamente. Se você deixar a caixa de palavra-chave vazia, todo o conteúdo localizado nos locais de conteúdo especificados será incluído nos resultados da pesquisa. 
    
2. Você pode clicar na caixa de seleção **Mostrar lista de palavra-chave** e o tipo de uma palavra-chave em cada linha. Se você fizer isso, as palavras-chave em cada linha são conectadas pela operadora **ou** na consulta de pesquisa que é criada. 
    
    ![Você pode digitar uma palavra-chave ou a fase de palavra-chave em uma linha na lista de palavras-chave](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    Por que usar a lista de palavra-chave? Você pode obter estatísticas que mostram quantos itens correspondem a cada palavra-chave. Isso pode ajudá-lo a identificar rapidamente quais palavras-chave é mais (e menos) eficientes. Você também pode usar uma frase de palavra-chave (entre parênteses) em uma linha. Para obter mais informações sobre estatísticas da pesquisa, consulte [Exibir as estatísticas de palavra-chave para resultados de pesquisa de conteúdo](view-keyword-statistics-for-content-search.md).
    
    Consulte a seção para obter orientação sobre como usar a lista de palavra-chave. 
    
3. Clique em **consulta para erros de digitação de seleção** para verificar sua consulta para caracteres não suportados e operadores booleanos que não podem estar em letras maiusculas. Não há suporte para caracteres geralmente estão ocultas e geralmente causam um erro de pesquisa ou retornam resultados inesperados. Para obter mais informações sobre os caracteres não suportados que são verificados, consulte [verificar sua consulta de pesquisa de conteúdo se há erros](check-your-content-search-query-for-errors.md).
    
4. Sob **condições**, adicione condições para uma consulta de pesquisa para restringir uma pesquisa e retornar um conjunto mais refinado de resultados. Cada condição adiciona uma cláusula à consulta KQL pesquisa que é criada e executada quando você iniciar a pesquisa. Uma condição logicamente está conectada à consulta de palavra-chave (especificada na caixa de palavra-chave) pelo operador **e** . Isso significa que itens precisam satisfazer tanto a consulta de palavra-chave e a condição a ser incluído nos resultados. Isso é como ajudam a condições para restringir os resultados. 
    
||
|:-----|
|Para obter mais informações sobre como criar uma consulta de pesquisa e condições de uso, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo ](keyword-queries-and-search-conditions.md). |
   
9. Clique em **Pesquisar** para salvar as configurações da pesquisa e iniciá-la. 
    
    A pesquisa é iniciada. Quando a pesquisa for concluída, a seguinte informação é exibida no painel de detalhes.
    
    ![Estatísticas da pesquisa são mostradas no painel de detalhes da pesquisa conteúda selecionada](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. A data e hora em que a pesquisa foi executada pela última vez.
    
2. O número (e tamanho total) de itens encontrados que correspondem à consulta de pesquisa. Documentos, itens de calendário e mensagens de email são exemplos de tipos de item. Se um item contiver várias instâncias de uma palavra-chave que está sendo procurado, ele só é contado uma vez no número total de itens. Por exemplo, se você estiver procurando por palavras "stock" ou "dica" e uma mensagem de email contém três instâncias da palavra "stock", ele é contado apenas uma vez no campo **itens** . 
    
3. O número e o tamanho total dos itens indexados nos locais do conteúdo que foram pesquisados. O número de itens indexados que não atendem aos critérios de pesquisa será incluído nas estatísticas da pesquisa exibidas no painel de detalhes. Se um item não indexadas corresponde à pesquisa de consulta (porque outras propriedades de mensagem ou documento atendam aos critérios de pesquisa), não será incluído o número estimado de itens indexados. No entanto, se um item não indexado for excluído pelos critérios de pesquisa, ele não será incluído na estimativa de itens indexados.
    
4. O número de cada tipo de local do conteúdo que foi pesquisado. Para caixas de correio, observe que caixas de correio de arquivo morto são incluídas no número total de caixas de correio que foram pesquisadas. No exemplo anterior, quatro caixas de correio do usuário foram pesquisadas e a caixa de correio de arquivamento para cada um desses usuários é ativada. É por isso que oito caixas de correio são citadas nas estatísticas da pesquisa.
    
5. Links para visualizar a pesquisa de resultados ou execute a pesquisa novamente para atualizar as estatísticas da pesquisa.
    
    Se necessário, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes para a pesquisa selecionado. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>Exportar resultados de pesquisa
<a name="export"> </a>

Depois que uma pesquisa for executada com êxito, você pode exportar os resultados da pesquisa para um computador local. Quando você exporta os resultados de email, serem transferidas para seu computador como arquivos PST. Quando você exporta o conteúdo do SharePoint e OneDrive para sites corporativos, cópias de documentos do Office nativos são exportadas. Há também documentos adicionais e relatórios que estão incluídos com os resultados da pesquisa exportado. Para obter mais informações, consulte [resultados de pesquisa de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md).
  
## <a name="preview-search-results"></a>Visualização de resultados de pesquisa
<a name="preview"> </a>

Quando uma pesquisa for concluída com êxito, você pode visualizar os resultados da pesquisa. Há um número de limites relacionados à visualização de resultados de pesquisa de conteúdo. Para obter mais informações, consulte [limites para pesquisa no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md). Observe que não indexadas itens não estão disponíveis para visualização.
  
1. Na página de **pesquisa de conteúdo** , selecione uma pesquisa. 
    
2. No painel de detalhes, em **Resultados**, clique em **Visualizar resultados da pesquisa**. A página **Visualizar resultados da pesquisa** é exibida contendo uma lista de itens de resultado da pesquisa. 
    
    Você pode clicar em um cabeçalho de coluna para classificar os resultados com base no assunto, tipo, remetente ou a data em que um item foi recebido na caixa de correio de origem.
    
3. Clique em um item para visualizar.
    
    O item é aberto no painel de visualização.
    
4. Se um tipo de arquivo não é suportado para visualizar ou baixar uma cópia de um documento, clique em **baixar o arquivo original** para baixá-lo ao computador local. Para. aspx páginas da Web, a URL da página é incluída, embora talvez você não tenha permissões para acessar a página. 
    
> [!NOTE]
> Se você visualizar os resultados da pesquisa para uma pesquisa última execução há mais de 7 dias, você deverá atualizar os resultados da pesquisa. A pesquisa é executada novamente para obter os resultados mais recentes que atendam a consulta de pesquisa. 
  
### <a name="file-types-that-can-be-previewed"></a>Tipos de arquivo que podem ser visualizados

Você pode visualizar os tipos de arquivo suportados no painel de visualização. Se não há suporte para um tipo de arquivo, você terá que baixar uma cópia do arquivo para o computador local para exibi-lo. Os seguintes tipos de arquivo são suportados e podem ser visualizados na página de **resultados de pesquisa de visualização** . 
  
- . txt,. HTML,. mhtml
    
- . eml
    
- . doc,. docx,. docm
    
- . pptm,. pptx
    
- .pdf
    
Além disso, há suporte para os seguintes tipos de contêiner de arquivo. Você pode exibir a lista de arquivos no contêiner no painel de visualização.
  
- .zip
    
- .gzip
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>Atualizar os resultados da pesquisa
<a name="restart"> </a>

Quando você atualiza os resultados de uma pesquisa de conteúdo existente, a consulta de pesquisa é executada novamente em todos os locais de conteúdo especificados. O motivo óbvio para atualizar os resultados da pesquisa é obter os dados mais recentes.
  
1. Na página **Pesquisa de Conteúdo**, selecione a pesquisa para a qual você deseja atualizar os resultados. 
    
2. No painel de detalhes, em **Resultados**, clique em **Atualizar resultados da pesquisa**.
    
    Uma mensagem de status é exibida informando que os resultados estão sendo recuperados. Quando a pesquisa for concluída, as informações atualizadas são exibidas em **resultados** no painel de detalhes. Observe que a data no campo **pesquisadas** no painel de detalhes é atualizada para a data atual e a hora. Para atualizar as informações na lista de pesquisas de conteúdo, clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>Editar uma pesquisa
<a name="edit"> </a>

Você pode alterar as caixas de correio de origem e a consulta de pesquisa de uma pesquisa de conteúdo existente.
  
1. Na página de **pesquisa de conteúdo** , selecione uma pesquisa. 
    
2. No painel de detalhes, em **Consulta**, clique em **Editar a pesquisa**.
    
3. Na página **locais** , você pode alterar quais caixas de correio, grupos, sites do SharePoint ou OneDrive para sites corporativos para pesquisar. Você também pode selecionar (ou desmarque) para pesquisar todas as pastas públicas no Exchange. 
    
4. Na página de **consulta** , você pode editar a consulta de pesquisa. 
    
5. Para iniciar a pesquisa revisada, clique em **Pesquisar** na página a **fontes** ou **locais** . 
    
    A pesquisa revista é iniciada. Quando o sistema conclui a pesquisa, os resultados esperados da pesquisa revista são exibidos no painel de detalhes.
    
## <a name="retry-a-search"></a>Repetir uma pesquisa
<a name="retry"> </a>

Se uma pesquisa retorna quaisquer erros, você não precisa novamente todos os locais de conteúdo de pesquisa. Você pode executar novamente a pesquisa para que apenas os locais de conteúdo que falharam fiquem pesquisa novamente. Para pesquisar novamente todos os locais de conteúdo, você poderá atualizar os resultados da pesquisa.
  
1. Na página de **pesquisa de conteúdo** , selecione a pesquisa que contém os locais de conteúdo que você deseja pesquisar novamente. 
    
2. No painel de detalhes, em **Erro**, clique em **Repetir a pesquisa**.
    
    Uma mensagem de status é exibida informando que os resultados estão sendo recuperados. Quando a pesquisa estiver concluída, as informações atualizadas são exibidas em **resultados** no painel de detalhes. Observe que a data no campo **pesquisadas** no painel de detalhes é atualizada para a data atual e a hora. Clique em **Atualizar**para atualizar as informações na lista de pesquisas,![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Voltar ao início](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>Mais informações
<a name="moreinfo"> </a>

Eis aqui para obter mais informações sobre as pesquisas de conteúdo.
  
[Limites e desempenho](run-a-content-search-in-the-security-and-compliance-center.md#limits)
  
[Itens não indexados](run-a-content-search-in-the-security-and-compliance-center.md#unindexeditems)
  
[As equipes da Microsoft e grupos do Office 365](run-a-content-search-in-the-security-and-compliance-center.md#teams)
  
[OneDrive for Business](run-a-content-search-in-the-security-and-compliance-center.md#onedrive)
  
[Consultas de pesquisa](run-a-content-search-in-the-security-and-compliance-center.md#queries)
  
[A pesquisa de caixas de correio inativas](run-a-content-search-in-the-security-and-compliance-center.md#inactivemailboxes)
  
[Diversos](run-a-content-search-in-the-security-and-compliance-center.md#misc)
  
[(Voltar ao início)](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
 **Limites e desempenho**
  
- Para obter uma descrição dos limites que são aplicadas ao recurso de pesquisa de conteúdo, consulte [limites para pesquisa no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md).
    
- Microsoft coleta informações de desempenho para pesquisas de conteúdo executados por todas as organizações do Office 365. Enquanto a complexidade da consulta de pesquisa pode afetar os tempos de pesquisa, o maior fator que afeta quanto tempo take pesquisas é o número de caixas de correio pesquisadas. Embora a Microsoft não oferece um contrato de nível de serviço para tempos de pesquisa, a seguinte tabela lista os tempos de médio de pesquisa para uma pesquisa de conteúdo com base no número de caixas de correio incluídas na pesquisa.
    
|**Número de caixas de correio**|**Tempo médio de pesquisa**|
|:-----|:-----|
|100  <br/> |30 segundos  <br/> |
|1,000  <br/> |45 segundos  <br/> |
|10.000  <br/> |4 minutos  <br/> |
|25.000  <br/> |10 minutos  <br/> |
|50.000  <br/> |20 minutos  <br/> |
|100.000  <br/> |25 minutos  <br/> |
   

  
 **Itens não indexados**
  
- Como explicadas anteriormente, não indexadas itens em locais de conteúdo que são pesquisados são incluídos nos resultados da pesquisa estimados. Se um item não indexadas corresponde à pesquisa de consulta (porque outras propriedades de mensagem ou documento atendam aos critérios de pesquisa), não será incluído o número estimado de itens indexados. Se um item não indexado for excluído pelos critérios de pesquisa, ele também não será incluído no número estimado de itens indexados. Para obter mais informações, consulte [itens indexados na pesquisa de conteúdo](https://go.microsoft.com/fwlink/p/?LinkId=780739).
    

  
 **As equipes da Microsoft e grupos do Office 365**
  
- Microsoft Teams baseiam-se no Office 365 grupos. Portanto, é muito semelhante pesquisar-los. Mantenha as seguintes coisas em mente ao pesquisar por conteúdo em Microsoft Teams e grupos do Office 365.
    
  - Para procurar conteúdo localizado no Microsoft Teams e grupos do Office 365, você precisa especificar a caixa de correio e o site do SharePoint que estão associados uma equipe ou um grupo.
    
  - Execute o cmdlet **Get-UnifiedGroup** no Exchange Online para exibir as propriedades para um Team Microsoft ou um grupo do Office 365. Isso é uma boa maneira de obter a URL para o site que está associado a uma equipe ou um grupo. Por exemplo, o comando a seguir exibe propriedades selecionadas para um grupo do Office 365 denominado sênior liderança equipe: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroup** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
  - Quando a caixa de correio do usuário é pesquisada, qualquer Team Microsoft ou um grupo do Office 365 que o usuário é membro do não ser pesquisado. Da mesma forma, quando você pesquisa um Team Microsoft ou um grupo de 365 Office, somente as caixas de correio de grupo e o site de grupo que você especificar é pesquisado; as caixas de correio e OneDrive para contas de negócios dos membros do grupo não são pesquisados, a menos que você os adicione explicitamente à pesquisa.
    
  - Para obter uma lista dos membros de um Team Microsoft ou um grupo do Office 365, você pode exibir as propriedades no **inicial \> grupos** página no Centro de administração do Office 365. Como alternativa, você pode executar o seguinte comando no PowerShell do Exchange Online: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Para executar o cmdlet **Get-UnifiedGroupLinks** , você precisa ter a função de destinatários somente para exibição no Exchange Online ou ser membro de um grupo de função que tiver atribuído a função de destinatários somente para exibição. 
  
  - Conversas que fazem parte de um canal de Teams da Microsoft são armazenadas na caixa de correio que está associado a Team Microsoft. Da mesma forma, os arquivos que compartilham de membros da equipe em um canal são armazenados no site do SharePoint da equipe. Portanto, você precisará adicionar a caixa de correio do Microsoft Team e o site do SharePoint como um local de conteúdo para pesquisar arquivos e conversas em um canal.
    
  - 
    
    Como alternativa, conversas que fazem parte da lista de bate-papo no Microsoft Teams são armazenadas na caixa de correio Exchange Online dos usuários que participam do bate-papo. E os arquivos que um usuário compartilha em conversas de bate-papo são armazenados em OneDrive para a conta comercial do usuário que compartilha o arquivo. Portanto, você precisará adicionar caixas de correio de usuário individual e OneDrive para contas de negócios, como locais de conteúdo para pesquisar conversas e arquivos na lista de bate-papo.
    
    > [!NOTE]
    > Os usuários participem de conversas que fazem parte da lista de bate-papo no Microsoft Teams devem ter uma caixa de correio (baseado em nuvem) Exchange Online na ordem a procura de conversas de bate-papo. Isso acontece porque conversas que fazem parte da lista de Chat são armazenadas nas caixas de correio baseadas em nuvem dos participantes bate-papo. Se um participante de bate-papo não tiver uma caixa de correio do Exchange Online, você não conseguirá conversas de bate-papo de pesquisa. Por exemplo, em uma implantação híbrida do Exchange, os usuários com uma caixa de correio local poderá participar de conversas que fazem parte da lista de bate-papo no Microsoft Teams. No entanto nesse caso, o conteúdo desses conversa não pesquisáveis porque os usuários não têm caixas de correio baseadas em nuvem. 
  
  - Cada canal Microsoft Team ou equipe contém um Wiki para colaboração e anotações. O conteúdo Wiki automaticamente é salvo em um arquivo com um formato. mht. Este arquivo é armazenado na biblioteca de documentos de equipes Wiki dados no site do SharePoint da equipe. Você pode usar a ferramenta de pesquisa de conteúdo para pesquisar o Wiki, especificando o site do SharePoint da equipe como o local do conteúdo a ser pesquisado. 
    
    > [!NOTE]
    > A capacidade de pesquisar o Wiki um Microsoft Team ou canal (quando você pesquisar o site do SharePoint da equipe) foi lançada em 22 de junho de 2017. Páginas wiki que foram salvas ou atualizadas na data ou após estão disponíveis a serem pesquisados. Páginas wiki última salvo ou atualizado antes desta data não estão disponíveis para pesquisa. 
  

  
 **OneDrive for Business **
  
- Para coletar uma lista das URLs do OneDrive para sites corporativos em sua organização, consulte [criar uma lista de todos os locais de OneDrive na sua organização](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). O script neste artigo cria um arquivo de texto que contém uma lista de todos os OneDrive para sites corporativos. Para executar esse script, você precisará instalar e usar o Shell de gerenciamento do SharePoint Online. Certifique-se de que inclua o URL para o domínio de meusite da sua organização para cada OneDrive para site de negócios que você deseja pesquisar. Este é o domínio que contém todos os seu OneDrive for Business; Por exemplo, `https://contoso-my.sharepoint.com`. Aqui está um exemplo de URL de OneDrive um usuário para o site de negócios: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    

  
 **Consultas de pesquisa**
  
- Manter as seguintes coisas em mente ao usar a lista de palavra-chave para criar uma consulta de pesquisa.
    
  - Você precisa selecionar a caixa de seleção **Mostrar lista de palavra-chave** e, em seguida, digite cada palavra-chave em uma linha separada para criar uma consulta de pesquisa onde as palavras-chave (ou frases de palavra-chave) em cada linha são conectadas pelo operador **OR** . Se você simplesmente cola uma lista de palavras-chave na caixa de palavra-chave ou pressione a tecla **Enter** depois de digitar uma palavra-chave, eles não estar conectados pelo operador **ou** . Eis um exemplo correto e incorreto da adição de uma lista de palavras-chave. 
    
    **Incorreto**
    
    ![A maneira incorreta para formatar uma lista de palavra-chave (por colando a lista na caixa palavras-chave)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Corrigir**
    
    ![A maneira correta para formatar uma lista de palavra-chave (selecionando checkbox e, em seguida, colando lista)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - Você pode também preparar uma lista de palavras-chave ou frases de palavra-chave em um arquivo do Excel ou em um arquivo de texto sem formatação e, em seguida, em seguida, copie e cole sua lista à lista de palavra-chave. Para fazer isso, você precisará selecionar a caixa de seleção **Mostrar lista de palavra-chave** . Em seguida, clique na primeira linha na lista de palavra-chave e cole sua lista. Cada linha do arquivo de texto ou Excel será colada em separar linha da lista de palavra-chave. 
    
  - Depois de criar uma consulta usando a lista de palavra-chave, ela é uma boa ideia para verificar a sintaxe de consulta de pesquisa (no painel de detalhes da pesquisa selecionado) para fazer a pesquisa a consulta é o que você pretendia. Na consulta de pesquisa que é exibida na **consulta** no painel de detalhes, as palavras-chave são separadas pelo texto **(c:s)**. Isso indica que as palavras-chave estão conectadas pelo operador **OR** . Da mesma forma, se a consulta de pesquisa inclui condições, as palavras-chave e as condições são separadas pelo texto **(c:c)**. Isso indica que as palavras-chave estão conectadas às condições pelo operador **e** . Aqui está um exemplo de consulta de pesquisa (exibido no painel de detalhes) que resulta ao usar a lista de palavra-chave e uma condição. 
    
    ![Exemplo da consulta é criado ao usar a lista de palavra-chave e uma condição](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - Se você tiver uma consulta de pesquisa que contém as palavras-chaves para os caracteres do inglês (por exemplo, caracteres chineses), você pode precisar usar o cmdlet **Set-ComplianceSearch** para configurar a propriedade de idioma para a pesquisa de conteúdo. Quando você cria uma pesquisa de conteúdo usando a GUI de segurança &amp; Centro de conformidade, o idioma padrão é neutro. 
    
    Como saber se você precisa alterar a configuração de idioma para uma pesquisa de conteúdo? Se você tiver certeza de locais de conteúdo contêm os caracteres do inglês que estiver pesquisando, mas a pesquisa não retorna nenhum resultado, a causa pode estar relacionada a configuração de idioma.
    
    Para alterar a configuração de idioma para uma pesquisa de conteúdo existente, execute o seguinte comando na segurança &amp; PowerShell do Centro de conformidade:
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    Por exemplo, para alterar a configuração de idioma para chinês, você usaria `zh-CN` para o valor de código de cultura. Depois de alterar a configuração de idioma, você terá que executar a pesquisa novamente. Para obter uma lista de valores de código de cultura possíveis, consulte [Classe CultureInfo](https://go.microsoft.com/fwlink/p/?LinkID=184859). Para pesquisas de conteúdo, recomendamos que você use códigos de cultura de duas partes para o valor da configuração de idioma; Por exemplo, `ja-JP` e não `ja`.
    

  
 **A pesquisa de caixas de correio inativas**
  
Conforme indicado anteriormente, você pode pesquisar caixas de correio inativas em uma pesquisa de conteúdo. Aqui estão algumas coisas ter em mente ao pesquisar caixas de correio inativas.
  
- Se uma pesquisa de conteúdo inclui uma caixa de correio do usuário e essa caixa de correio, em seguida, será feita inativa, continuará a pesquisa de conteúdo pesquisar a caixa de correio inativa quando você executar a pesquisa novamente depois que ele fique inativo.
    
- Em alguns casos, um usuário pode ter uma caixa de correio ativa e uma caixa de correio inativa que têm o mesmo endereço SMTP. Nesse caso, somente a caixa de correio específica que você selecionar como um local para uma pesquisa de conteúdo devem ser pesquisada. Em outras palavras, se você adicionar caixa de correio de um usuário a uma pesquisa, você não pode assumir que ambas as suas ativas e inativas caixas de correio devem ser pesquisadas; somente a caixa de correio que você os adicione explicitamente à pesquisa devem ser pesquisada.
    
- É altamente recomendável que você evite ter uma caixa de correio ativa e a caixa de correio inativa com o mesmo endereço SMTP. Se você precisar reutilizar o endereço SMTP que está atualmente atribuído a uma caixa de correio inativa, recomendamos que você recupere a caixa de correio inativa ou restaura o conteúdo de uma caixa de correio inativa para uma caixa de correio ativa (ou o arquivo morto de uma caixa de correio ativa) e exclua o caixa de correio inativa. Para obter mais informações, consulte um dos seguintes tópicos:
    
  - [Recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md)
    
  - [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md)
    

  
 **Diversos**
  
- Conteúdo criadas na página **pesquisa de conteúdo** na segurança de pesquisas &amp; Centro de conformidade não são exibidos na **Descoberta eletrônica In-loco &amp; mantenha** página no Centro de administração do Exchange. Isso ocorre porque a arquitetura de pesquisa de conteúdo e pesquisa nos objetos criados na segurança &amp; Centro de conformidade são totalmente diferente do que o recurso de descoberta eletrônica In-loco no Exchange Online. 
    
    Pela mesma razão, pesquisas criadas na página **pesquisa de conteúdo** não são exibidas na página de **pesquisas** de um caso de eDiscovery na segurança &amp; Centro de conformidade. 
    
- O que é a diferença entre reinício e tentar novamente uma pesquisa? Quando você reiniciar uma pesquisa, todos os locais de conteúdo que são especificados na pesquisa são pesquisados novamente em uma nova pesquisa de visualização. No entanto, quando você tentar novamente uma pesquisa, apenas os locais de conteúdo que falhou quando a pesquisa foi executada pela última vez são pesquisados novamente.
   

