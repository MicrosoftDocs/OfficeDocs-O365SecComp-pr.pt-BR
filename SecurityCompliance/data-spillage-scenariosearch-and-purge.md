---
title: solução série dados algum derramamento cenário de descoberta eletrônica - pesquisa e limpar
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Use as ferramentas de descoberta eletrônica e pesquisa do Office 365 para gerenciar e responder a um incidente de algum derramamento de dados em sua organização.
ms.openlocfilehash: d2c5a0a6efcc75a38df97c7c597503e5642f83eb
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575345"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>série de solução de descoberta eletrônica: cenário de algum derramamento de dados - pesquisa e limpar

 **o que há algum derramamento de dados e por que é importante?** Algum derramamento de dados é quando um documento confidencial é liberado para um ambiente de não confiável. Quando um incidente de algum derramamento de dados é detectado, é importante avaliar rapidamente o tamanho e os locais do algum derramamento, examine as atividades do usuário ao redor dele e limpar permanentemente os dados derramados do sistema. 
  
## <a name="data-spillage-scenario"></a>Cenário de algum derramamento de dados

Você é responsável por segurança informações líder na Contoso. Você é informado de uma situação de algum derramamento de dados onde um funcionário inconscientemente compartilhadas um documento altamente confidencial com várias pessoas através de email. Você deseja avaliar rapidamente quem recebeu este documento interna e externamente. Uma vez identificado, gostaria de compartilhar descobertas maiusculas com outros investigadores para revisar e remover permanentemente os dados do Office 365. Quando a investigação for concluída, você deseja gerar um relatório com a evidência de remoção permanente e outro detalhes de caso para qualquer referência futura.
  
### <a name="scope-of-this-article"></a>Escopo deste artigo

Este documento fornece uma lista de instruções sobre como remover permanentemente uma mensagem do Office 365 para que ele não está acessível ou recuperável. Para excluir uma mensagem e torná-lo recuperáveis até o período de retenção de item excluído expira, consulte [Procurar e excluir mensagens de email em sua organização do Office 365](search-for-and-delete-messages-in-your-organization.md).
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>Fluxo de trabalho de gerenciamento de incidentes de algum derramamento de dados

Aqui está um como gerenciar um incidente de algum derramamento de dados:

![O fluxo de trabalho de 8-etapa de gerenciamento de incidentes de algum derramamento de dados](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[(Opcional) Etapa 1: Gerenciar quem pode acessar o caso e definir limites de conformidade](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[Etapa 2: Criar um caso de eDiscovery](#step-2-create-an-ediscovery-case)<br/>
[Etapa 3: Pesquisa para os dados derramadas](#step-3-search-for-the-spilled-data)<br/>
[Etapa 4: Revisar e validar as descobertas de maiusculas](#step-4-review-and-validate-case-findings)<br/>
[Etapa 5: Log de rastreamento de mensagem de uso para verificar os dados como derramados foi compartilhada](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[Etapa 6: Preparar as caixas de correio](#step-6-prepare-the-mailboxes)<br/>
[Etapa 7: Excluir permanentemente os dados derramados](#step-7-permanently-delete-the-spilled-data)<br/>
[Etapa 8: Verificar, fornecer uma prova de exclusão e auditoria](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>Coisas que você deve saber antes de começar

- Quando uma caixa de correio estiver em espera, uma mensagem excluída permanece na pasta itens recuperáveis até o período de retenção expira ou a suspensão seja removida. [Etapa 6](#step-6-prepare-the-mailboxes) descreve como remover a retenção de caixas de correio. Verifique com o gerenciamento de registros ou departamentos legais antes de remover o bloqueio. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de algum derramamento de dados tem prioridade. 
    
- Para controlar quais caixas de correio do usuário um investigador algum derramamento de dados pode pesquisar e gerenciar quem pode acessar o caso, você pode configurar limites de conformidade e criar um grupo de função personalizada, que é descrito na [etapa 1](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries). Para fazer isso, você precisa ser membro do grupo de funções de gerenciamento da organização ou ser atribuída a função de gerenciamento de função. Se você ou no administrador na sua organização já possui limites de conformidade de conjunto, ignore a etapa 1.
    
- Para criar um caso, você deve ser membro do grupo de função de Gerenciador de descoberta eletrônica ou ser membro de um grupo de função personalizada que tiver atribuído a função de gerenciamento de caso. Se você não for um membro, pergunte ao administrador do Office 365 para [adicioná-lo ao grupo de função de Gerenciador de descoberta eletrônica](assign-ediscovery-permissions.md).
    
- Para excluir dados que é derramou em sua organização, você precisará usar o comando de [Search-Mailbox-DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) no PowerShell do Exchange Online. Além disso, para usar o parâmetro *DeleteContent* , você também precisa ser um membro de um grupo de função no Exchange Online que atribuiu a função caixa de correio importar e exportar. Consulte a seção "Adicionar uma função a um grupo de funções" em [Gerenciar grupos de função](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx).
    
- Para pesquisar as atividades de descoberta eletrônica de log de auditoria de Office 365 na etapa 8, auditoria deve ser ativado para a sua organização. Você pode pesquisar atividades que foram executadas nos últimos 90 dias. Para saber mais sobre como habilitar e usar a auditoria, consulte a seção [auditoria o processo de investigação de algum derramamento de dados](#auditing-the-data-spillage-investigation-process) na etapa 8. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>(Opcional) Etapa 1: Gerenciar quem pode acessar o caso e definir limites de conformidade

Dependendo da sua prática organizacional, você precisa controlar quem pode acessar o caso de descoberta eletrônica usado para investigar um incidente de algum derramamento de dados e estabeleça os limites de conformidade. A maneira mais fácil de fazer isso é adicionar investigadores como membros de um grupo de função existente no Centro de conformidade & segurança do Office 365 e, em seguida, adicione o grupo de funções como um membro do caso de eDiscovery. Para obter informações sobre os grupos de função de descoberta eletrônica internas e como adicionar membros a um caso de eDiscovery, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
  
Você também pode criar um novo grupo de função que se alinha com suas necessidades organizacionais. Por exemplo, você pode querer um grupo de investigadores algum derramamento de dados na organização para acessar e colaborar em todos os casos de algum derramamento de dados. Você pode fazer isso criando um grupo de funções de "Dados algum derramamento investigador", atribuindo funções adequadas (exportação, descriptografar RMS, revisão, visualização, pesquisa de conformidade e gerenciamento de casos), adicionando os investigadores algum derramamento de dados ao grupo de funções e, em seguida, adicionando a grupo de funções como membro do caso de descoberta eletrônica de algum derramamento dados. Para obter instruções detalhadas sobre como fazer isso, consulte [Configurar limites de conformidade para investigações de descoberta eletrônica no Office 365](set-up-compliance-boundaries.md) . 
  
## <a name="step-2-create-an-ediscovery-case"></a>Etapa 2: Criar um caso de eDiscovery

Um caso de eDiscovery oferece uma maneira eficaz para gerenciar sua investigação de algum derramamento de dados. Você pode adicionar membros ao grupo de funções que você criou na etapa 1, adicione o grupo de função como membro do novo um caso de eDiscovery, realizar pesquisas de repetitivo para localizar os dados derramados, exportar um relatório para compartilhar, controlar o status do caso e, em seguida, consultá-os detalhes do c ASE se necessário. Considere a possibilidade de estabelecer uma convenção de nomenclatura para os casos de eDiscovery usado para incidentes de algum derramamento de dados e forneça o máximo de informações possível nas maiusculas nome e descrição para que você pode localizar e consulte a no futuro, se necessário.
  
Para criar um novo caso, você pode usar a descoberta eletrônica na segurança &amp; Centro de conformidade. Consulte "Criar um novo caso" em [casos de descoberta eletrônica no Centro de conformidade & segurança do Office 365](ediscovery-cases.md#step-2-create-a-new-case).
  
## <a name="step-3-search-for-the-spilled-data"></a>Etapa 3: Pesquisa para os dados derramadas

Agora que você criou um caso e acesso gerenciado, você pode usar o caso iterativamente Pesquisar para localizar os dados derramados e identificam as caixas de correio que contêm os dados derramados. Você usará a mesma consulta de pesquisa que você usou para encontrar as mensagens de email para excluir as mesmas mensagens na [etapa 7](#step-7-permanently-delete-the-spilled-data).
  
Para criar um conteúdo pesquisas associados com um caso de eDiscovery, consulte "Criar e executar que uma pesquisa de conteúdo associada a um caso" em [casos de descoberta eletrônica no Centro de conformidade & segurança do Office 365](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case).
  
 **Importante:** As palavras-chave que podem ser usados na consulta de pesquisa podem conter os dados reais derramados que você está procurando. Por exemplo, se você procurar documentos contendo um número de seguridade social e você utilizá-lo como palavra-chave de pesquisa, você deve excluir a consulta posteriormente para evitar a algum derramamento. Consulte [excluindo a consulta de pesquisa](#deleting-the-search-query) na etapa 8. 
  
## <a name="step-4-review-and-validate-case-findings"></a>Etapa 4: Revisar e validar as descobertas de maiusculas

Depois de criar uma pesquisa de conteúdo, você precisará revisar e validar que a pesquisa de resultados e verificar que consistem em somente as mensagens de email que devem ser excluídas. Em uma pesquisa de conteúdo, você pode visualizar uma amostragem aleatória de 1.000 mensagens de email sem exportar os resultados da pesquisa para evitar a algum derramamento de dados. Você pode ler mais sobre as limitações de visualização em [limites para pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade](limits-for-content-search.md).
  
Se você tiver mais de 100 mensagens de email ou mais de 1.000 caixas de correio por caixa de correio para analisar, você pode dividir a pesquisa inicial em várias pesquisas usando palavras-chave adicionais ou condições como remetente/destinatário ou o intervalo de datas e revise os resultados de pesquisa de cada individualmente. Certifique-se observar para baixo de todas as consultas de pesquisa para usar quando você exclui mensagens na [etapa 7](#step-7-permanently-delete-the-spilled-data).

Se dos responsáveis ou o usuário final é atribuído a uma licença do Office 36 E5, você pode examinar os resultados da pesquisa até 10.000 ao mesmo tempo usando o eDiscovery avançadas do Office 365. Se houver mais de 10.000 mensagens de email para examinar, você pode dividir a consulta de pesquisa pelo intervalo de datas e examinar cada resultado individualmente, como pesquisa, os resultados são classificados por data. EDiscovery avançado, você pode marcar os resultados de pesquisa usando o recurso de **rótulo como** no painel Visualização e filtrar o resultado de pesquisa por marca que você rotulados. Isso é útil quando você colabora com um revisor secundário. Usando ferramentas de análise adicional no eDiscovery avançado, como reconhecimento óptico de caracteres, threading de email e previsão de codificação, você pode rapidamente processar e revisar milhares de mensagens e marcá-los para revisão posterior. Consulte [setup rápida para eDiscovery avançadas do Office 365](quick-setup-for-advanced-ediscovery.md).

Quando você encontrar uma mensagem de email que contém dados derramados, verifique os destinatários da mensagem para determinar se ela foi compartilhada externamente. Para rastrear mais uma mensagem, você pode coletar informações sobre o remetente e o intervalo de datas para que você possa usar os logs de rastreamento de mensagem, que é descrito na [etapa 5](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared).

Após você verificou os resultados da pesquisa, convém compartilhar suas descobertas com outras pessoas para uma revisão secundária. Pessoas que você atribuiu ao caso na etapa 1 podem revisar o conteúdo de maiusculas na descoberta eletrônica e descoberta eletrônica avançada e aprovar descobertas maiusculas. Você também pode gerar um relatório sem exportar o conteúdo real. Você também pode usar este relatório mesmo como uma prova de exclusão, que é descrito na [etapa 8](#step-8-verify-provide-a-proof-of-deletion-and-audit).
  
 **Para gerar um relatório de estatístico:**
  
1. Vá para a página de **pesquisa** no caso de descoberta eletrônica e clique em que você deseja gerar um relatório de pesquisa. 
    
2. Na página de submenu, clique em **mais > Exportar relatório**.
 
      A página de relatório de exportação é exibida.

    ![Selecione a pesquisa e, em seguida, clique em mais > Exportar relatório na página submenu](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. Selecione **todos os itens, incluindo aquelas que têm o formato não reconhecido, são criptografados, ou não foram indexados por outros motivos** e clique em **Gerar relatório**.

4. No caso de descoberta eletrônica, clique em **Exportar** para exibir a lista de trabalhos de exportação. Talvez você precise clicar em **Atualizar** para atualizar a lista para exibir o trabalho de exportação que você acabou de criar.

5. Clique no trabalho de exportação e, em seguida, clique em **Baixar** relatório na página submenu.
 
    ![Na página Exportar, clique em Exportar e clique em "Baixar relatório"](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

O relatório de **Resumo da exportação** contém o número de locais encontrada com os resultados e o tamanho dos resultados da pesquisa. Você pode usar isso em comparação com o relatório gerado após exclusão e fornecer como uma prova de exclusão. O relatório de **resultados** contém um resumo mais detalhado dos resultados da pesquisa, incluindo o assunto, remetente, destinatários, se o email foi lido, datas e o tamanho de cada mensagem. Se qualquer um dos detalhes neste relatório contém dados derramados reais, certifique-se de excluir permanentemente o arquivo Results.csv quando a investigação for concluída.

Para obter mais informações sobre como exportar relatórios, consulte [Exportar um relatório de pesquisa de conteúdo](export-a-content-search-report.md).
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>Etapa 5: Log de rastreamento de mensagem de uso para verificar os dados como derramados foi compartilhada

Para investigar melhor se email com dados derramados foi compartilhada, você pode opcionalmente consultar os logs de rastreamento de mensagem com as informações de remetente e as informações de intervalo de datas coletadas na etapa 4. Observe que o período de retenção para rastreamento de mensagens é 30 dias de dados em tempo real e 90 dias de dados de histórico.
  
Você pode usar o rastreamento de mensagens no Centro de conformidade & segurança ou usar os cmdlets correspondentes o PowerShell no Exchange Online. É importante observar que o rastreamento de mensagem não oferece garantias completos na abrangência dos dados retornados. Para obter mais informações sobre como usar o rastreamento de mensagens, consulte: 
  
- [Rastreamento de segurança do Office 365 de mensagem &amp; Centro de conformidade](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Novo rastreamento de mensagem na segurança do Office 365 &amp; Centro de conformidade](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>Etapa 6: Preparar as caixas de correio

Depois de revisar e validar que os resultados da pesquisa contém somente as mensagens que devem ser excluídas, você precisa coletar uma lista de endereços de email das caixas de correio afetadas para usar na etapa 7, quando você executar o comando **Search-Mailbox-DeleteContent** . Você também pode ter que preparar as caixas de correio antes de você pode excluir permanentemente mensagens de email, dependendo se a recuperação de item único está habilitada nas caixas de correio que contêm os dados derramados ou se qualquer uma dessas caixas de correio estão em espera.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>Obter uma lista de endereços das caixas de correio com dados derramadas

Há duas maneiras de coletar uma lista de endereços de email de caixas de correio com dados derramadas.

**Opção 1: Obtenha uma lista de endereços de caixas de correio com dados derramadas**

1. Abra a ocorrência de descoberta eletrônica, vá para a página de **pesquisa** e selecione a pesquisa de conteúdo apropriada. 
    
2. Na página submenu, clique em **Exibir resultados**.
    
3. Na lista suspensa **resultados individuais** , clique em **estatísticas da pesquisa**.
    
4. Na lista suspensa **tipo** , clique em **locais de superior**.
    
    ![Obtenha uma lista de caixas de correio que contêm os resultados da pesquisa, na página locais principais nas estatísticas da pesquisa](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    É exibida uma lista de caixas de correio que contêm os resultados da pesquisa. O número de itens em cada caixa de correio que correspondem à consulta de pesquisa também é exibido.
    
5. Copie as informações na lista e salvá-lo em um arquivo ou clique em **Baixar** para baixar as informações para um arquivo CSV. 
    
**Opção 2: Obter locais de caixa de correio a partir do relatório de exportação**

Abra o relatório de resumo de exportação que você baixou na [etapa 4](#step-4-review-and-validate-case-findings). Na primeira coluna no relatório, o endereço de email de cada caixa de correio está listado em **locais**.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>Preparar as caixas de correio, assim você pode excluir os dados derramados

Se a recuperação de item único está habilitada ou uma caixa de correio é colocada em espera, uma mensagem (limpas) permanentemente excluída será mantida na pasta itens recuperáveis. Isso antes de você pode limpar dados derramados, você precisará verificar as configurações de caixa de correio existente e desabilitar a recuperação de item único e remover qualquer espera ou a política de retenção do Office 365. Tenha em mente que você pode preparar uma caixa de correio por vez e, em seguida, executar o mesmo comando em caixas de correio diferentes ou crie um script do PowerShell para preparar a várias caixas de correio ao mesmo tempo.

- Consulte "etapa 1: coletar informações sobre a caixa de correio" no [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) para obter instruções sobre como verificar se a recuperação de item único está habilitada ou se a caixa de correio é colocada em espera ou é atribuído a um política de retenção. 
    
- Consulte "etapa 2: preparar a caixa de correio" no [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) para obter instruções sobre como desabilitar a recuperação de item único. 
    
- Consulte "etapa 3: remover todas as isenções da caixa de correio" no [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) para obter instruções sobre como remover uma política de retenção ou retenção de uma caixa de correio. 

- Consulte "etapa 4: remover o atraso de espera da caixa de correio" no [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) para obter instruções sobre como remover a retenção de atraso é colocada na caixa de correio depois de qualquer tipo de espera é removido.
    
 **Importante:** Verifique com o gerenciamento de registros ou departamentos legais antes de remover uma política de retenção ou de espera. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de algum derramamento de dados tem prioridade. 
  
Certifique-se de reverter configurações anteriores a caixa de correio depois de verificar se os dados derramados foi excluídos permanentemente. Ver os detalhes na [etapa 7](#step-7-permanently-delete-the-spilled-data).

## <a name="step-7-permanently-delete-the-spilled-data"></a>Etapa 7: Excluir permanentemente os dados derramados

Usando os locais de caixa de correio que você coletadas e preparado na etapa 6 e a consulta de pesquisa que foi criada e refinada na etapa 3 para encontrar as mensagens de email que contêm os dados derramados, você pode agora excluir permanentemente os dados derramados. Conforme explicado anteriormente, você precisa ter a função caixa de correio importar e exportar no Exchange Online para excluir mensagens usando o procedimento a seguir.
  
1. [Conectar-se ao Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. Execute o seguinte comando:
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Execute novamente o comando anterior para cada caixa de correio que contém os dados derramados, substituindo o valor do parâmetro de identidade; Por exemplo:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
Conforme indicado anteriormente, você também pode criar um [script do powershell](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) e executá-lo em relação a uma lista de caixas de correio para que o script exclui os dados derramados em cada caixa de correio.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>Etapa 8: Verificar, fornecer uma prova de exclusão e auditoria

A etapa final do fluxo de trabalho para gerenciar um incidente de algum derramamento de dados é para verificar se os dados derramados foi removidos permanentemente da caixa de correio, indo para o caso de descoberta eletrônica e executar novamente a consulta de pesquisa mesmo que foi usada para não excluir dados para confirmar que nenhum ar de resultados f é retornado. Depois de confirmar que os dados derramados foi removidos permanentemente, você pode exportar um relatório e incluí-lo (juntamente com o relatório original) como uma prova de exclusão. Em seguida, você pode [Fechar o caso](ediscovery-cases.md#optional-step-9-close-a-case), que permitirá que você abra novamente se você tiver consultá-lo no futuro. Além disso, você também pode reverter as caixas de correio ao estado anterior, exclua a consulta de pesquisa usada para localizar os dados derramados e para auditar registros das tarefas realizadas ao gerenciar o incidente algum derramamento de dados de pesquisa. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>Revertendo as caixas de correio ao estado anterior

Se você alterou a qualquer configuração de caixa de correio na etapa 6 para preparar as caixas de correio antes que os dados derramados foi excluídos, você precisará revertê-los ao seu estado anterior. Consulte "etapa 6: reverter a caixa de correio ao estado anterior" em [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state).
  
### <a name="deleting-the-search-query"></a>Excluir a consulta de pesquisa

Se as palavras-chave na consulta de pesquisa que você criou e usada na etapa 3 contém algumas das todos os dados derramados reais, você deve excluir a consulta de pesquisa para impedir a algum derramamento de dados.
  
1. Em Centro de conformidade e segurança, abra a ocorrência de descoberta eletrônica, vá para a página de **pesquisa** e selecione a pesquisa de conteúdo apropriada.
    
2. Na página submenu, clique em **Excluir**.

    ![Selecione a pesquisa e clique em Excluir na página submenu](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>O processo de investigação de algum derramamento de dados de auditoria

Você pode pesquisar o log de auditoria do Office 365 para as atividades de descoberta eletrônica que foram executadas durante a investigação. Você também pode pesquisar o log de auditoria para retornar os registros de auditoria que foram criados quando você executou o comando **Search-Mailbox-DeleteContent** para excluir os dados derramados. Para obter mais informações, consulte:

- [Pesquisar o log de auditoria no Centro de Conformidade &amp; Segurança do Office 365](search-the-audit-log-in-security-and-compliance.md)

- [Procure atividades de descoberta eletrônica no log de auditoria do Office 365](search-for-ediscovery-activities-in-the-audit-log.md)

- Consulte a seção "Auditadas atividades - log de auditoria de administração do Exchange" na [pesquisa da auditoria, faça logon no Centro de conformidade & segurança do Office 365](search-the-audit-log-in-security-and-compliance.md#audited-activities) para obter orientação sobre como pesquisar por registros de auditoria relacionados à execução de cmdlets no Exchange Online.
  

