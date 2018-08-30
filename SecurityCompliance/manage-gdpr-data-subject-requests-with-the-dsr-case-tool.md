---
title: Gerenciar solicitações de entidade de dados GDPR com a ferramenta de maiusculas DSR no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: Os GDPR oferece da UE cidadãos (chamados de assuntos de dados) direitos específicos para seus dados pessoais; Esses direitos incluem obtendo cópias dele, solicitando as alterações feitas nele, restringindo o processamento dele, excluí-la ou recebê-lo em formato eletrônico. Uma solicitação formal por uma dados sujeitos take uma ação em seus dados pessoais é chamada uma solicitação de entidade de dados ou o DSR. Você pode usar a segurança do Office 365 DSR casos &amp; Centro de conformidade para gerenciar investigações de DSR da sua organização.
ms.openlocfilehash: c8edee8d377865d46662ebbd7f18a5a6f3015192
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524153"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-office-365-security-amp-compliance-center"></a>Gerenciar solicitações de entidade de dados GDPR com a ferramenta de maiusculas DSR no Office 365 Security &amp; Centro de conformidade

O gerais dados proteção regulamentação (GDPR) da UE é sobre como proteger e habilitando os direitos de privacidade dos indivíduos dentro da União Europeia (UE). Pessoas GDPR oferece na União Europeia (conhecido como assuntos de dados) o direito de acessar, recuperar, corrigir, apagar e restringir o processamento de seus dados pessoais. Em GDPR, dados pessoais significa qualquer informações relacionadas a uma pessoa natural identificada ou identificável. Uma solicitação formal por uma pessoa para a sua organização para executar uma ação nos seus dados pessoais é chamada de uma solicitação de entidade de dados ou o DSR. Para obter informações detalhadas sobre como responder para os DSRs para os dados no Office 365, consulte o [Guia de solicitação do Office 365 dados assunto](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Para gerenciar investigações em resposta a um DSR enviado por uma pessoa em sua organização, você pode usar a ferramenta de maiusculas DSR no Office 365 Security &amp; Centro de conformidade para encontrar conteúdo armazenado em:
  
- Qualquer caixa de correio do usuário em sua organização. Isso inclui Skype para conversas de negócios e chats individual em Teams da Microsoft
    
- Todas as caixas de correio associadas a um grupo do Office 365 e todas as caixas de correio de equipe no Microsoft Teams
    
- Todos os sites do SharePoint Online e contas do OneDrive for Business em sua organização
    
- Todos os sites de equipes e sites de grupo do Office 365 em sua organização
    
- Todas as pastas públicas no Exchange Online
    
Usando a ferramenta de maiusculas DSR, você pode:
  
- Criar uma ocorrência separada para cada investigação de DSR.
    
- Controlar quem tem acesso ao caso DSR adicionando pessoas como membros do caso; apenas membros podem acessar o caso e só pode ver seus casos na lista de ocorrências na página **casos DSR** na segurança &amp; Centro de conformidade. Além disso, você pode atribuir permissões diferentes para diferentes membros do mesmo caso. Por exemplo, você pode permitir que alguns membros somente exiba os resultados de pesquisa e de caso e permitir que os outros membros criar pesquisas e exportar os resultados da pesquisa. 
    
- Use o pesquisa para pesquisar internos para todo o conteúdo criado ou carregados por uma entidade de dados específicos.
    
- Como opção, revisar a consulta de pesquisa internos e execute novamente a pesquisa para restringir os resultados de pesquisa.
    
- Adicione as pesquisas de conteúdo adicionais associadas à ocorrência DSR. Isso inclui a criação de pesquisas que retornam itens indexados parcialmente e logs gerada pelo sistema de análise de meu e o serviço de Roaming do Office.
    
- Exportar dados em resposta a um acesso DSR ou solicitação de exportação.
    
- Excluir casos, quando o processo de investigação DSR completo; Isso removerá todas as pesquisas e exportar trabalhos associados à ocorrência.
    
Aqui está o processo de alto nível para usar a ferramenta de maiusculas DSR para gerenciar investigações DSR:
  
[Etapa 1: atribuir permissões de Descoberta Eletrônica para possíveis membros da ocorrência](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Etapa 2: Criar um caso DSR e adicionar membros](#step-2-create-a-dsr-case-and-add-members)

[Etapa 3: Executar a consulta de pesquisa](#step-3-run-the-search-query)

[Etapa 4: Exportar os dados](#step-4-export-the-data)

[(Opcional) Etapa 5: Revisar a consulta de pesquisa internos](#optional-step-5-revise-the-built-in-search-query)

[Para obter mais informações sobre como usar a ferramenta de maiusculas DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Nossas ferramentas podem ajudar administradores executar acesso DSR ou solicitações de exportação, permitindo que eles utilizam a pesquisa interna e exportar funcionalidades encontradas na ferramenta DSR maiusculas. A ferramenta ajuda para facilitar a um método de melhor esforço para exportar os dados relevantes a uma solicitação de DSR enviada por uma entidade de dados. No entanto, é importante observar que os resultados da pesquisa podem variar com base no assunto dados ou as ações de admin realizadas que podem ser afetado se ou não um item seria considerado como "dados pessoais" para fins de exportação. Por exemplo, se a entidade de dados foi a última pessoa a modificar um arquivo não foi criado, o arquivo não pode ser retornado nos resultados da pesquisa. Da mesma forma, um administrador pode exportar os dados sem incluir itens indexados parcialmente ou todas as versões de documentos do SharePoint. Portanto, as ferramentas fornecidas podem ajudar a facilitar acessando e exportando solicitações de dados; No entanto, os resultados são sujeitos a cenários de uso específicos de assunto de admin e dados. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Etapa 1: atribuir permissões de Descoberta Eletrônica para possíveis membros da ocorrência

Por padrão, um administrador global do Office 365 pode acessar a ferramenta de maiusculas DSR na segurança &amp; Centro de conformidade. Por design, outros usuários como um diretor de privacidade de dados, um gerente de recursos humanos, ou outras pessoas envolvidas em investigações DSR não tem acesso à ferramenta de casos de DSR e terão que ser atribuídas as permissões apropriadas para acessar a ferramenta. A maneira mais fácil de fazer isso é para ir à página **permissões** de segurança &amp; Centro de conformidade e adicionar usuários ao grupo de função de Gerenciador de descoberta eletrônica. Observe que você também precisa atribuir essas permissões, portanto, você poderá adicioná-los como membros do caso DSR criadas por você na etapa 2. 
  
Para obter instruções detalhadas, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
  
> [!NOTE]
> Por padrão, um administrador global do Office 365 (ou outros membros do grupo de funções de gerenciamento da organização na segurança &amp; Centro de conformidade não têm as permissões necessárias para exportar os resultados de pesquisa de conteúdo (consulte a etapa 4 deste artigo). Para resolver isso, um administrador pode adicionar si mesmos como um membro do grupo de função de Gerenciador de descoberta eletrônica. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Etapa 2: Criar um caso DSR e adicionar membros

A próxima etapa é criar um caso DSR. Quando você cria um caso, você pode escolher iniciar a pesquisa interna ou você pode criar o caso sem iniciar a pesquisa. O procedimento a seguir instruirá para criar o caso sem iniciar a pesquisa e, em seguida, mostraremos como adicionar membros ao caso.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar no Office 365 usando sua conta do trabalho ou da escola. 
    
2. Na segurança &amp; Centro de conformidade, clique em **dados privacidade** \> **solicitações de entidade de dados**e clique ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **DSR novo caso**.
    
3. Na página **novo DSR caso** submenu, nomeie o caso, digite uma descrição opcional e clique em **Avançar**. Observe que o nome da ocorrência deve ser exclusivo na sua organização.
    
    > [!TIP]
    > Considere adicionar o nome da pessoa que enviou a solicitação DSR que você está investigando no nome de usuário e/ou a descrição do novo caso. Observe que apenas os membros deste caso (e administradores de descoberta eletrônica) poderão ver o caso na lista de ocorrências na página **solicitações de entidade de dados** . 
  
4. Na página **detalhes da solicitação** , em **(a pessoa que arquivado essa solicitação) de entidade de dados**, selecione a pessoa que você deseja localizar e exportar dados para e clique em **Avançar**.
    
5. Na página **Confirmar suas configurações de maiusculas** , você pode alterar o nome de maiusculas e a descrição e selecione uma entidade de dados diferentes. Caso contrário, basta clicar em **Salvar**.
    
    É exibida uma página que confirma que o novo caso DSR foi criado.
    
    ![Iniciar a pesquisa ou apenas fechar a página de caso de novo DSR](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    Neste ponto, você pode fazer uma das duas coisas:
    
    r. clicar em **Mostrar-me resultados de pesquisa** inicia a pesquisa. Esta é a seleção padrão. A pesquisa interna que é executada quando você seleciona essa opção e os resultados são retornados são discutidos na etapa 3.
    
    b. ao clicar em **Concluir** fecha o novo caso DSR sem iniciar a pesquisa interna. Quando você seleciona essa opção, o novo caso DSR é exibido na página **solicitações de entidade de dados** .
    
6. Clique em **Concluir** para que você possa ir ao novo caso DSR e adicionar membros a ela. 
    
7. Na página **solicitações de entidade de dados** , clique no nome do caso DSR que você acabou de criar. 
    
8. Na página **Gerenciar neste caso** submenu, em **Gerenciar membros**, clique em **Adicionar**. 
    
    Em **usuários**, é exibida uma lista de pessoas que tiverem sido atribuídas as permissões apropriadas de eDiscovery. Observe que as pessoas que você atribuiu permissões de descoberta eletrônica para na etapa 1 serão exibidas nessa lista. 
    
9. Selecione as pessoas para adicionar como membros do caso DSR, clique em **Adicionar**e salve as alterações.
    
    Observe que você também pode adicionar grupos de funções como membros de caso DSR clicando em **Adicionar** em **Gerenciar grupos de função**. 
    
## <a name="step-3-run-the-search-query"></a>Etapa 3: Executar a consulta de pesquisa

Depois de criar um caso DSR e adicionar membros, a próxima etapa é executar a pesquisa interna que está associado ao caso. Esta consulta de pesquisa padrão faz o seguinte:
  
- Procura por todas as caixas de correio em sua organização para todos os itens de email que foram enviadas ou recebidas pelo assunto de dados. Isso é realizado usando-se a propriedade de email de *participantes* , que procura o assunto de dados em todos os campos de pessoas em uma mensagem de email. Essa propriedade retorna os itens nos quais o assunto de dados está na **partir**, **para**, **CC**e **Cco** campos. Pastas públicas no Exchange Online também são pesquisadas para mensagens enviadas ou recebidas pelo assunto de dados. 
    
- Procura por todos os sites em sua organização para documentos e itens que foram criados ou carregados pelo assunto de dados. Isso é realizado usando-se as seguintes propriedades de site:
    
  - A propriedade *Author* retorna os itens em que o assunto de dados é listado no campo autor em documentos do Office. Esse valor persiste, mesmo se o documento é copiado e carregado por outra pessoa. 
    
  - A propriedade *CreatedBy* retorna itens que foram criados ou carregados pelo assunto de dados. 
    
Aqui está a aparência da consulta de palavra-chave para a pesquisa interna que obtém criada automaticamente quando você cria um caso DSR.
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Por exemplo, se o nome do assunto da dados for Ina Leonte, a consulta de palavra-chave teria esta aparência:
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Para executar a pesquisa interna para uma ocorrência DSR:**
  
1. Na segurança &amp; Centro de conformidade, clique em **dados privacidade** \> **solicitações de entidade de dados**e clique em **Abrir** , ao lado de no caso DSR que você criou na etapa 2. 
    
    Clique na guia **pesquisa** na parte superior da página e, em seguida, clique na caixa de seleção ao lado de pesquisa interna que foi criada quando você criou o novo caso DSR. Observe que a pesquisa tiver o mesmo nome conforme o caso do DSR. 
    
2. Na página de submenu da pesquisa, clique em **Abrir consulta**.
    
    Quando você abre a consulta, a pesquisa é iniciada e será concluída em alguns momentos. 
    
3. Quando a pesquisa estiver concluída, clique em **resultados de visualização** para visualizar os resultados da pesquisa. Para obter mais informações, consulte [Preview search results](content-search.md#preview-search-results).
    
    > [!TIP]
    > Também é possível exibir as estatísticas de consultas de pesquisa para ver o número de caixas de correio e itens de site que são retornados pela pesquisa e os locais de conteúdo principais que contêm os itens que correspondem à consulta de pesquisa. Para obter mais informações, consulte [Exibir informações e estatísticas sobre uma pesquisa](content-search.md#view-information-and-statistics-about-a-search). 
  
Você pode editar a consulta de pesquisa internos, alterar os locais de conteúdo que são pesquisados e, em seguida, execute novamente a pesquisa. Para obter mais informações, consulte a [etapa 5](#optional-step-5-revise-the-built-in-search-query) . 
  
## <a name="step-4-export-the-data"></a>Etapa 4: Exportar os dados

Após executar a pesquisa interna, você pode exportar os resultados da pesquisa. Como alternativa, antes de exportar os dados, convém revisar a consulta para reduzir o número de resultados da pesquisa. Para obter mais informações sobre como restringir os resultados da pesquisa, consulte a etapa 5.
  
Ao exportar os resultados da pesquisa, itens de caixa de correio podem ser baixados em arquivos PST ou como mensagens individuais. Quando você exporta o conteúdo de contas do SharePoint e OneDrive, cópias de documentos do Office nativos e outros documentos são exportadas. Um arquivo de resultados que contém informações sobre cada item que será exportado também está incluído com os resultados da pesquisa. Para obter mais informações sobre como exportar, consulte [resultados de pesquisa de conteúdo de exportação da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md).
  
> [!NOTE]
> Por padrão, um administrador global do Office 365 (ou outros membros do grupo de funções de gerenciamento da organização na segurança &amp; Centro de conformidade) não têm as permissões necessárias para exportar os resultados de pesquisa de conteúdo. Para resolver isso, um administrador pode adicionar si mesmos como um membro do grupo de função de Gerenciador de descoberta eletrônica. 
  
O computador usado para exportar dados deve satisfazer os seguintes requisitos de sistema:
  
- Versões de 32 e 64 bits do Windows 7 e versões posteriores



    
- Microsoft .NET Framework 4.7
    
- Um navegador com suporte:
    
  - Microsoft Edge
    
    Ou
    
  - Microsoft Internet Explorer 10 e versões posteriores
    
    > [!NOTE]
    > A Microsoft não fabrica extensões de terceiros ou complementos para aplicativos ClickOnce. Exportando dados usando um navegador sem suporte com extensões de terceiros ou complementos não é suportado. 
  
 **Para exportar dados de pesquisa em um caso DSR interna:**
  
1. Na segurança &amp; Centro de conformidade, clique em **dados privacidade** \> **solicitações de entidade de dados**e clique em **Abrir** , ao lado de no caso DSR que você deseja exportar os dados. 
    
2. Clique na guia **pesquisa** na parte superior da página e, em seguida, clique na caixa de seleção ao lado de pesquisa interna que foi criada quando você criou o caso do DSR. Ou clique em outra pesquisa para exportar dados de pesquisa. 
    
3. Na página de submenu da pesquisa, clique em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mais**e, então, selecione **Exportar resultados** da lista suspensa. 
    
4. Na página **Exportar resultados** , selecione as seguintes opções para solicitações de exportação do DSR recomendadas. 
    
    ![Definir as configurações de exportação](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    r. em **Opções de saída**, selecione a primeira opção ( **todos os itens, excluindo aquelas que possuírem aquelas que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos**) para exportar somente os itens indexados. O motivo pelo qual que você não deseja exportar itens indexados parcialmente da pesquisa interna é porque itens indexados parcialmente de outros usuários serão exportados. Para exportar somente os itens indexados parcialmente para o assunto de dados, recomendamos que você crie uma pesquisa separado. Para obter mais informações, consulte [exportar itens indexados parcialmente](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) na seção "Para obter mais informações sobre como usar a ferramenta de maiusculas DSR".
    
    b. em **conteúdo do Exchange exportar como**, selecione a terceira opção, o **arquivo PST um contendo todas as mensagens em uma única pasta**. Pois alguns dos resultados podem ser para itens que originou na caixa de correio de outro usuário, essa opção apenas o item em uma única pasta em listas sem indicando a caixa de correio real e é a melhor opção para usar quando os resultados conforme recomendado no próximo item eliminar a duplicação . Essa opção também permite que o assunto dados Reveja os itens em ordem cronológica (itens são classificados por data de envio) sem precisar navegar a estrutura original de pasta de caixa de correio para cada item.
    
    c. Selecione a opção de **Habilitar a eliminação da duplicação** de mensagens para exclui mensagens de email duplicadas. É recomendável essa opção, pois a pesquisa interna procura todas as caixas de correio em sua organização. Portanto, se várias cópias da mesma mensagem forem encontradas nas caixas de correio que foram pesquisadas, essa opção significa apenas uma cópia de uma mensagem será exportada. Essa opção, juntos exportar mensagens em um arquivo PST em uma única pasta resulta na melhor experiência de usuário para DSR exportará solicitações. Observe que o relatório de exportação Results.csv listará todos os locais onde mensagens duplicadas encontradas.
    
    Opcionalmente, você pode selecionar a opção de **incluir versões de documentos do SharePoint** para exportar todas as versões de documentos do SharePoint e OneDrive. Isso requer a que esse controle de versão está ativado para bibliotecas de documentos. Essa opção ajuda a garantir que todos os dados relevantes é exportada.
    
5. Depois que você escolher as configurações de exportação, clique em **Exportar**.
    
    Os resultados da pesquisa são preparados para download, o que significa que terem sido carregadas para a área de armazenamento do Azure para sua organização em nuvem da Microsoft. As próximas etapas mostram como baixar esses dados para seu computador local.
    
6. Clique na guia **Exportar** para exibir o trabalho de exportação que você acabou de criar. Observe que os trabalhos de exportação tem o mesmo nome que o correspondente de pesquisa com **_Export** acrescentados ao final do nome de pesquisa. 
    
7. Clique no trabalho de exportação que você acabou de criar para exibir a página de submenu de exportação. Esta página mostra informações sobre a pesquisa, como o tamanho e o número total de itens a serem exportados e a porcentagem dos itens que tenham sido transferidos para uma área de armazenamento do Azure. Clique em **Atualizar** para atualizar as informações de status de carregamento. 
    
8. Em **Exportar chave**, clique em **Copiar para a área de transferência**. Você usará essa chave na etapa 11 para baixar os resultados da pesquisa.
    
9. Clique em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Baixar resultados** na parte superior da página de submenu de exportação. 
    
10. Na janela pop-up, na parte inferior da página, clique em **Abrir** para abrir a **Descoberta eletrônica do Microsoft Office 365 Tool exportar**. A **ferramenta de exportação de descoberta eletrônica** será instalado na primeira vez que você baixe os resultados da pesquisa. 
    
11. Na **ferramenta de exportação de descoberta eletrônica**, cole a chave de exportação que você copiou na etapa 8 na caixa apropriada.
    
12. Clique em **Procurar** para especificar o local onde deseja baixar os arquivos de resultado da pesquisa. 
    
    > [!NOTE]
    > Devido à quantidade de atividade de disco (leituras e gravações) alta, você deve baixar os resultados da pesquisa para uma unidade de disco local; não baixá-los para uma unidade de rede mapeada ou outro local de rede. 
  
13. Clique em **Iniciar** para baixar os resultados da pesquisa em seu computador. 
    
    A **ferramenta de exportação de descoberta eletrônica** exibe informações de status sobre o processo de exportação, incluindo uma estimativa do número (e tamanho) dos itens restantes a serem baixados. Quando o processo de exportação estiver concluído, você pode acessar os arquivos no local onde elas são baixadas. Para obter mais informações sobre os relatórios que incluído quando você baixe os resultados de pesquisa de conteúdo, consulte a seção de [obter mais informações](export-search-results.md#more-information) em "resultados de pesquisa de conteúdo de exportação da segurança do Office 365 &amp; Centro de conformidade". 
    
Depois que os dados são exportados, os resultados da pesquisa e os relatórios de exportação estão localizados em uma pasta que tem o mesmo nome que o caso do DSR. Os arquivos PST que contêm os itens de caixa de correio estão localizados em uma subpasta chamada **Exchange**. Documentos e outros itens de sites estão localizados em uma subpasta chamada **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Opcional) Etapa 5: Revisar a consulta de pesquisa internos

Após executar a pesquisa interna, você pode revisá-lo para restringir o escopo para retornar menos resultados de pesquisa. Você pode fazer isso adicionando condições à consulta. Uma condição logicamente está conectada à consulta de palavra-chave pelo operador **AND** . Isso significa que a serem retornadas nos resultados da pesquisa, itens devem satisfazer a consulta de palavra-chave e de quaisquer condições que você adicionar. Isso é como ajudam a condições para reduzir os resultados. Se você adicionar duas ou mais condições exclusivas para uma consulta de pesquisa (condições que especificam as propriedades diferentes), essas condições logicamente são conectadas pelo operador **AND** . Isso significa que apenas os itens que satisfazem todas as condições (além da consulta de palavra-chave) são retornados. Se você adicionar vários valores (separados por vírgulas ou ponto e vírgula) a uma única condição, esses valores são conectados pelo operador **OR** . Isso significa que itens são retornados caso eles contenham qualquer um dos valores especificados para a propriedade da condição. 
  
Aqui estão alguns exemplos das condições que podem ser adicionados à consulta a pesquisa interna de um caso DSR. O nome da propriedade real usada em uma consulta de pesquisa é mostrado entre parênteses.
  
- **Tipo de arquivo ( `filetype`)** -Especifica a extensão de um documento ou um arquivo. Use essa condição para procurar documentos e arquivos criados pelos aplicativos específicos do Office, como Word, Excel e o OneNote. 
    
- **Tipo de mensagem ( `kind`)** -Especifica o tipo de item de email a ser pesquisado. Por exemplo, você pode usar a sintaxe `kind:email OR kind:im` para retornar somente as mensagens de email e Skype para conversas de negócios ou um-para-chats no Microsoft Teams. 
    
- **Marca de conformidade (`compliancetag`)** -Especifica um rótulo atribuído a uma mensagem de email ou um documento. Esta condição retornará os itens que são classificados com um rótulo específico. Rótulos são usados para classificar documentos governança de dados e email e impor regras de retenção com base na classificação do definidos pelo rótulo. Esta é uma condição de útil para investigações DSR porque a sua organização pode estar usando rótulos para classificar o conteúdo relacionado à privacidade de dados ou que contém dados pessoais ou informações confidenciais. Para o valor dessa condição, use o nome de rótulo completa ou a primeira parte do nome do rótulo com um caractere curinga. Para obter mais informações, consulte [Overview of rótulos no Office 365](labels.md).
    
Para obter uma lista e descrição de todas as condições disponíveis na ferramenta de maiusculas do DSR, consulte [condições de pesquisa](keyword-queries-and-search-conditions.md#search-conditions) no artigo "consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Alterando os locais de conteúdo que são pesquisados

Além das examinando a pesquisa interna para uma ocorrência DSR, você também pode alterar os locais de conteúdo que são pesquisados. Conforme explicado anteriormente, a pesquisa interna pesquisa cada caixa de correio e o site na organização e quaisquer pastas públicas do Exchange Online. Por exemplo, você pode restringir a pesquisa para pesquisar somente a caixa de correio e a conta de OneDrive o assunto de dados e selecionado sites do SharePoint. Se você optar por pesquisar sites específicos, você precisará adicionar cada site que você deseja pesquisar.
  
Para modificar os locais de conteúdo para pesquisa:
  
1. Abra a pesquisa interna que você deseja alterar os locais de conteúdo para.
    
2. Na consulta de pesquisa, em **locais**, clique em **Modificar** ao lado da opção **locais específicos** . 
    
    ![Clique em Modificar para alterar os locais de conteúdo da consulta de pesquisa internas](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    A página de submenu **modificar locais** é exibida. Aqui está uma descrição dos locais de conteúdo em pesquisa interna e algumas informações sobre como modificar os locais são pesquisados. 
    
    ![Modificar a página de submenu locais](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    r. a alternância em **Selecionar tudo** na seção de caixa de correio na parte superior da página submenu é selecionada, o que indica que todas as caixas de correio são pesquisadas. Para restringir o escopo da pesquisa, clique a alternância para desmarcá-la e, em seguida, clique em **Escolher usuários, grupos ou equipes** e escolha as caixas de correio específicas para pesquisar.
    
    b. a alternância em **Selecionar tudo** na seção sites no meio da página de submenu é selecionada, o que indica que todos os sites são pesquisados. Para restringir a pesquisa aos sites selecionados, você faria unselect a alternância e clique em **Escolher sites**. Você terá que adicionar cada site específico que você deseja pesquisar, incluindo a conta de OneDrive da entidade de dados.
    
    c. a alternância na seção de pastas públicas do Exchange é selecionada, o que significa que todas as pastas públicas do Exchange são pesquisadas. Observe que você só pode pesquisar todas as pastas públicas do Exchange ou nenhum deles. Você não pode escolher aqueles específicos a ser pesquisado.
    
3. Se você modificar os locais de conteúdo na pesquisa interna, clique em **Salvar &amp; execute** novamente a pesquisa será iniciada. 
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Para obter mais informações sobre como usar a ferramenta de maiusculas DSR

As seções a seguir contêm mais informações sobre como usar a ferramenta de maiusculas DSR para responder às solicitações de exportação do DSR.
  
[Exportando dados do MyAnalytics e o serviço de Roaming do Office](#exporting-data-from-myanalytics-and-the-office-roaming-service)

[Exportando itens indexados parcialmente](#exporting-partially-indexed-items)

[Pesquisando e exportando dados do Microsoft Teams e grupos do Office 365](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[Pesquisar pastas públicas do Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-myanalytics-and-the-office-roaming-service"></a>Exportando dados do MyAnalytics e o serviço de Roaming do Office

Você pode usar a ferramenta de maiusculas DSR para procurar e exportar dados de uso que seja gerados pelo MyAnalytics e o serviço de Roaming do Office. Aqui está uma descrição do que fazem esses serviços:
  
- **MyAnalytics** - fornece aos usuários ideias sobre como eles passam dedicação de tempo baseado nos dados de email e calendário em suas caixas de correio. Todas as ideias de MyAnalytics são derivadas dos cabeçalhos de email e de reunião na caixa de correio do usuário. Os usuários recebem uma licença MyAnalytics podem entrar no Office 365 e vá para o painel de MyAnalytics para exibir as ideias sobre como eles passam dedicação de tempo. (Os usuários podem tela capturas essas ideias em resposta a uma solicitação de acesso do DSR). A pesquisa interna no caso do DSR exportará os dados que são usados para gerar ideias MyAnalytics. 
    
- **Serviço de Roaming do office** - Roaming é um serviço que armazena as configurações relacionadas ao Office, como Office tema, dicionário personalizado, configurações de idioma, modo de desenvolvedor e correção automática. 
    
Os dados da MyAnalytics e o serviço Office Roaming são armazenados na caixa de correio de um assunto de dados em pastas ocultas localizado em uma subárvore (não-IPM) de mensagem não interpessoais de caixas de correio Exchange Online. Isso significa que os dados estão ocultos do modo de exibição do usuário quando utilizarem Outlook ou outros clientes de email para acessar suas caixas de correio. Para obter mais informações sobre pastas ocultas, consulte [Pastas ocultas de MAPI](https://go.microsoft.com/fwlink/?linkid=872758).
  
Você pode criar uma pesquisa de conteúdo separado (e associá-lo a um caso DSR) que retorna a MyAnalytics e os dados de uso do serviço de Roaming do Office na caixa de correio de assuntos dos dados. Esses dados não estão incluídos nas estatísticas da pesquisa, e ele não estará disponível para visualização. Mas você poderá exportá-lo e, em seguida, dê a ela o assunto de dados em resposta a uma solicitação de exportação do DSR.
  
Quando você exporta dados do MyAnalytics e o serviço de Roaming do Office, os dados são salvos em uma pasta separada para cada aplicativo que está localizado na pasta **ApplicationDataRoot** , que está em uma pasta que é o nome com o endereço de email da entidade de dados. Esses dados são exportados como arquivos JSON, que são arquivos de texto legíveis semelhantes aos arquivos XML ou TXT, que estejam anexados às mensagens de email. Atualmente, essas pastas são nomeadas com um identificador global exclusivo (GUID) que é atribuído a MyAnalytics e o serviço de Roaming do Office, que são listados na tabela a seguir. Em versões futuras da ferramenta DSR caso, o GUID será substituído com o nome do aplicativo real. 
  
|**Aplicativo**|**Nome da GUID/pasta**|
|:-----|:-----|
|MyAnalytics  <br/> |3c896ded-22c5-450F-91f6-3d1ef0848f6e  <br/> |
|Serviço de Roaming do Office  <br/> |1caee58f-eb14-4a6b-9339-1fe2ddf6692b  <br/> |
   
 **Para procurar e exportar dados MyAnalytics e serviço de Roaming do Office:**
  
1. Na segurança &amp; Centro de conformidade, clique em **dados privacidade** \> **solicitações de entidade de dados**e clique em **Abrir** ao lado do caso do DSR para o assunto de dados que você deseja exportar os dados de uso para. 
    
2. Clique na guia **pesquisa** na parte superior da página e, em seguida, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **pesquisa guiada**.
    
3. Clique em **Cancelar** na página **nome da sua pesquisa** . 
    
4. Na **consulta de pesquisa**, na condição de **tipo** , selecione as caixas de seleção ao lado de **MyAnalytics** e **Serviço de Roaming do Office**. 
    
    ![Marque as caixas de seleção MyAnalytics e serviço de Roaming do Office para exportar dados de uso](media/3dacbc7a-c314-492c-828c-6757fda84963.png)
  
    Observe que a condição de **Type** (que são classes de mensagens de email) deve ser o único item na consulta de pesquisa. Você pode excluir a caixa de **palavras-chave** ou deixe em branco. 
    
5. Em **locais**, certifique-se de **que locais específicos** está marcada e clique em **Modificar**.
    
6. Na parte superior da página submenu **modificar locais** (a seção de caixa de correio), clique em **Escolher usuários, grupos ou equipes**.
    
7. Na página **Editar locais** , clique em **Escolher usuários, grupos ou equipes**, escolha a caixa de correio da entidade de dados e salve sua seleção. 
    
8. Clique em **Salvar &amp; executar**e, em seguida, nomeie a pesquisa e salvá-lo.
    
    A pesquisa é iniciada.
    
 **Para exportar dados MyAnalytics e serviço de Roaming do Office:**
  
1. Quando a pesquisa que você criou na etapa anterior for concluída, clique na guia **pesquisa** na parte superior da página e, em seguida, clique na caixa de seleção ao lado de pesquisa. Talvez você precise clicar ![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Atualizar** para exibir a pesquisa. 
    
2. Na página de submenu da pesquisa, clique em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mais**e, então, selecione **Exportar resultados** da lista suspensa. 
    
3. Na página **Exportar resultados** , selecione estas opções para exportar dados de uso recomendadas. 
    
    ![Opções de exportação para exportar dados de uso de MyAnalytics e serviço de Roaming do Office](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    r. em **Opções de saída**, selecione a primeira opção ( **todos os itens, excluindo aquelas que possuírem aquelas que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos**) para exportar somente os itens indexados.
    
    b. em **conteúdo do Exchange exportar como**, selecione a segunda opção, o **arquivo PST um contendo todas as mensagens**.
    
    c. deixe as opções de exportação restantes desmarcadas.
    
4. Depois que você escolher as configurações de exportação, clique em **Exportar**.
    
    Os resultados da pesquisa são preparados para download, o que significa que terem sido carregadas para a área de armazenamento do Azure para sua organização em nuvem da Microsoft. As próximas etapas mostram como baixar esses dados para seu computador local.
    
5. Clique na guia **Exportar** para exibir o trabalho de exportação que você acabou de criar. Observe que os trabalhos de exportação tem o mesmo nome que o correspondente de pesquisa com **_Export** acrescentados ao final do nome de pesquisa. 
    
6. Clique no trabalho de exportação que você acabou de criar para exibir a página de submenu de exportação. 
    
7. Em **Exportar chave**, clique em **Copiar para a área de transferência**. Você usará essa chave na etapa 10 para baixar os resultados da pesquisa.
    
8. Clique em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Baixar resultados** na parte superior da página de submenu de exportação. 
    
9. Na janela pop-up, na parte inferior da página, clique em **Abrir** para abrir a **Descoberta eletrônica do Microsoft Office 365 Tool exportar**. A **ferramenta de exportação de descoberta eletrônica** será instalado na primeira vez que você baixe os resultados da pesquisa. 
    
10. Na **Ferramenta de Exportação de Descoberta Eletrônica**, cole na caixa apropriada a chave de exportação que você copiou na etapa 7.
    
11. Clique em **Procurar** para especificar o local onde deseja baixar os arquivos de resultado da pesquisa. 
    
    > [!NOTE]
    > Devido à quantidade de atividade de disco (leituras e gravações) alta, você deve baixar os resultados da pesquisa para uma unidade de disco local; não baixá-los para uma unidade de rede mapeada ou outro local de rede. 
  
12. Clique em **Iniciar** para baixar os resultados da pesquisa em seu computador. 
    
    A **ferramenta de exportação de descoberta eletrônica** exibe informações de status sobre o processo de exportação, incluindo uma estimativa do número (e tamanho) dos itens restantes a serem baixados. Quando o processo de exportação estiver concluído, você pode abrir o arquivo PST do Exchange no Outlook e, em seguida, vá para a pasta de **ApplicationDataRoot** para acessar as subpastas ao serviço MyAnalytics e de Roaming. 
    
    Conforme explicado anteriormente, os arquivos JSON que contém os dados de uso estão anexados às mensagens. Para exibir um arquivo JSON, clique em uma mensagem e, em seguida, abra o arquivo JSON anexado. 
  
### <a name="exporting-partially-indexed-items"></a>Exportando itens indexados parcialmente

Recomendamos que você não exportar itens indexados parcialmente (também chamados de itens indexados) de pesquisa interna que é criada quando você cria um novo caso DSR. Isso ocorre porque a pesquisa resultados mais do que provável incluirão parcialmente indexados itens para outros usuários em sua organização e não apenas parcialmente os itens indexados para a entidade de dados). Em vez disso, recomendamos que você cria uma pesquisa de conteúdo separado que possui associado com o caso do DSR elaborada para exportar somente os itens indexados parcialmente relacionados ao assunto dados. 
  
Aqui está um processo de alto nível para exportar itens indexados parcialmente. Depois que estiverem exportação, pode revisá-lo para determinar se um itens estiver respondendo a um acesso DSR ou exportar a solicitação.
  
1. Abra o caso do DSR e criar uma nova pesquisa na página de **pesquisa** . 
    
2. Use os critérios a seguir para configurar a consulta de pesquisa e os locais de conteúdo para pesquisa:
    
    - Use uma consulta de palavra-chave de empty/em branco. Isso retornará todos os itens nos locais do conteúdo que são pesquisados.
    
    - Pesquise somente do assunto de dados Exchange Online da caixa de correio e a conta do OneDrive.
    
3. Depois que você execute a pesquisa e ele for concluído, você pode exportar e baixe os resultados da pesquisa (conforme descrito na [etapa 4](#step-4-export-the-data)). Use as configurações a seguir para exportar itens indexados parcialmente. 
    
    - Em **Opções de saída**, selecione a terceira opção ( **apenas os itens que possuem um formato não reconhecido, são criptografados, ou não foram indexados por outros motivos**) para exportar itens indexados parcialmente apenas.
    
    - Em **Exchange exportar conteúdo como**, você pode selecionar qualquer opção com base em suas preferências. 
    
    - Selecionando a opção de **incluir versões de documentos do SharePoint** irá exportar versões de documentos, se uma versão parcialmente é indexada. 
    
Para obter mais informações sobre itens indexados parcialmente, consulte: 
  
- [Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365](partially-indexed-items-in-content-search.md)

- [Exportando itens indexados parcialmente](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a>Pesquisando e exportando dados do Microsoft Teams e grupos do Office 365

Conversas que fazem parte da lista de bate-papo no Teams da Microsoft (chamados de chats de equipe ou um-para-chats) são armazenadas na caixa de correio Exchange Online dos usuários que participam de bate-papos. Além disso, os arquivos de que compartilhamentos de uma pessoa em um-para-um chat são armazenados na conta OneDrive da pessoa que compartilha o arquivo. Porque a pesquisa interna procura todas as contas de OneDrive e de caixas de correio na organização, chats de equipe e documentos compartilhados em uma sessão de chat (ou o assunto de dados criadas ou carregadas) serão retornados pela pesquisa interna no caso do DSR.
  
Como alternativa, conversas que fazem parte de um canal de equipes (também chamado de mensagens de canal) são armazenadas na caixa de correio que está associado a uma equipe. Esses tipos de conversas que o assunto dados participou também são retornados pela pesquisa interna porque todas as caixas de correio associadas Teams da Microsoft são pesquisadas. Além disso, lado a lado para uma entidade de dados pode ter compartilhado em um canal de equipes é armazenada no site do SharePoint da equipe. Os arquivos criados ou uploadedby o assunto de dados será retornado pela pesquisa interna no caso do DSR porque sites associados Teams Microsoft estão incluídos na pesquisa.
  
Da mesma forma, caixas de correio e sites do SharePoint que correspondem a um grupo do Office 365 também são incluídos na pesquisa interna. Isso significa que as mensagens de email que onde enviado ou recebido pelo assunto de dados e arquivos criados ou carregados por assunto dados serão retornados. 
  
Para obter mais informações sobre como usar a pesquisa de conteúdo para procurar itens em Microsoft Teams e grupos do Office 365 ou para ver como obter uma lista de membros de um, consulte a seção "Pesquisando o Microsoft equipes e o Office 365 grupos" [Pesquisa de conteúdo no Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>Pesquisar pastas públicas do Exchange

A pesquisa interna em um caso DSR será somente retorno de emails que o assunto dos dados enviados a uma pasta pública habilitada para email ou mensagens que alguém enviadas para uma pasta pública e também copiados o assunto de dados. Ele não retornará mensagem que o assunto de dados pode ter postados para uma pasta pública. Para procurar itens que o assunto dados postado para uma pasta pública, você pode criar um separado criar uma pesquisa de conteúdo separado que procura por qualquer item postado em uma pasta pública, a entidade de dados.
  
Aqui está um processo de alto nível para procurar itens que o assunto de dados pode ter postados para uma pasta pública. 
  
1. Abra o caso do DSR e criar uma nova pesquisa na página de **pesquisa** . 
    
2. Use os critérios a seguir para configurar a consulta de pesquisa e os locais de conteúdo para pesquisa:
    
  - Na caixa **palavras-chave** , use a seguinte consulta de pesquisa: 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Pesquisar todas as pastas públicas do Exchange
    
  - Depois que você execute a pesquisa e ele for concluído, você pode exportar e baixe os resultados da pesquisa (conforme descrito na [etapa 4](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)). Use as configurações a seguir para exportar itens indexados parcialmente. 
