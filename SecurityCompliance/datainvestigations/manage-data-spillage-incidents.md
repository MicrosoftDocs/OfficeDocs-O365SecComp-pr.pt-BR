---
title: Gerenciar um incidente de derramamento de dados no Microsoft 365
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
description: Este artigo descreve o uso da nova ferramenta de investigações de dados (visualização) no centro de conformidade & de segurança para gerenciar um incidente de derramamento de dados.
ms.openlocfilehash: 93a98a4e01df011b789ba2453734f093ad8c19d6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258819"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Gerenciar um incidente de derramamento de dados no Microsoft 365

Data derramamento é quando um documento que contém informações confidenciais, confidenciais ou mal-intencionadas é liberado em um ambiente não confiável. Quando um incidente de derramamento de dados é detectado, é importante conter rapidamente o ambiente, avaliar o tamanho e os locais do derramamento, examinar as atividades do usuário em torno dele e, em seguida, excluir os dados derramados do serviço. Usando a ferramenta de investigações de dados (visualização), você pode pesquisar dados confidenciais, mal-intencionados ou incorretos no Office 365, investigar para descobrir o que aconteceu e tomar as medidas apropriadas.  

## <a name="scope-of-this-article"></a>Escopo deste artigo

Este artigo fornece uma lista de instruções sobre como excluir permanentemente os itens das caixas de correio do Office 365 para que eles não sejam mais acessíveis ou recuperáveis por usuários ou administradores. 

> [!NOTE]
> Quando você exclui itens localizados em um site do SharePoint ou do OneDrive for Business, eles são mantidos por 93 dias a partir do momento em que são excluídos do local original.

## <a name="scenario"></a>Cenário

Você é informado de um incidente de derramamento de dados em que um funcionário compartilhou inadvertidamente um documento altamente confidencial com várias pessoas por email. Você deseja avaliar rapidamente quem recebeu este documento, tanto dentro e fora da sua organização. Após investigar o incidente, você planeja compartilhar suas descobertas com outros investigadores para analisar e, em seguida, remover permanentemente os dados derramados do Office 365. Após a conclusão da investigação, você deseja remover todas as evidências. 

## <a name="workflow"></a>Fluxo de trabalho

Este é o fluxo de trabalho para usar investigações de dados (visualização) para gerenciar um incidente de derramamento de dados:

1.  Criar uma investigação de dados.

2.  Pesquise dados confidenciais, mal-intencionados ou de local incorreto e colete-os como evidência.

3.  Revise e investigue as evidências.

4.  Excluir permanentemente os dados derramados.

5.  Feche ou exclua a investigação.


## <a name="before-you-begin"></a>Antes de começar

- Você usará a ferramenta de investigações de dados (visualização) no centro de conformidade do & de segurança para criar uma investigação, procurar os dados derramados e examiná-los e analisá-los. Em seguida, você usará o PowerShell do centro de conformidade do & de segurança para excluir permanentemente os dados derramados do Office 365. 

- Para criar uma investigação, você precisa ser membro do grupo de função Administrador de conformidade no centro de conformidade do & de segurança.

- Para excluir mensagens, você precisa ser membro de um grupo de função no centro de conformidade do & de segurança atribuído à função de pesquisa e limpeza. Por padrão, essa função é atribuída ao grupo de função gerenciamento da organização. Para obter informações sobre como adicionar usuários a um grupo de funções, consulte [permissões no centro de conformidade do & de segurança](../permissions-in-the-security-and-compliance-center.md). 

- Para controlar quais caixas de correio de usuário e contas do OneDrive podem pesquisar, sua organização pode configurar os limites de conformidade. Para obter mais informações, [Configure os limites de conformidade para investigações de descoberta eletrônica](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Etapa 1: criar uma investigação de dados

Para criar uma investigação na ferramenta de investigações de dados (visualização):

1. Acesse [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No centro de conformidade, clique em **investigações de dados**.
 
4. Na página **investigações de dados (visualização)** , clique em **criar nova investigação**.
    
5. Na nova página de submenu de **investigação de dados** , dê um nome à investigação (obrigatório) e digite um número de investigação e uma descrição opcionais. Observe que o nome deve ser exclusivo em sua organização.

6. Em **você deseja definir configurações adicionais depois de criar esta investigação?**, siga um destes procedimentos:

    - Clique em **Sim** para criar a investigação e exiba a página **configurações** no novo caso. Isso permite adicionar membros à investigação.
    
    - Clique em **não** para apenas criar a investigação e exibi-la na lista de casos na página **investigações de dados (visualização)** . Se você escolher essa opção, será adicionado como o único membro da investigação, e as configurações padrão de pesquisa e análise serão usadas. Você pode adicionar membros ou alterar as configurações a qualquer momento após a criação da investigação.

7. Clique em **salvar** para criar a investigação.

    A nova investigação é exibida na lista na página **investigações de dados (visualização)** . 

8. Para abrir uma investigação, clique no nome da investigação. 

    A guia **página inicial** da investigação é exibida. 

> [!TIP]
> Considere o estabelecimento de uma Convenção de nomenclatura para investigações e forneça tantas informações quantas forem necessárias no nome e na descrição para que você possa localizar e consultar no futuro, se necessário.
 
## <a name="step-2-search-for-the-spilled-data"></a>Etapa 2: Pesquisar os dados derramados 
 
Se você souber quais usuários você deseja pesquisar por dados derramados, você pode adicioná-los como pessoas de interesse para mapear suas fontes de dados para a investigação e pesquisar rapidamente a sua caixa de correio e a conta do OneDrive. Para adicionar pessoas de interesse à investigação, clique em **pessoas de interesse**e, em seguida, clique em **adicionar pessoas de interesse**. Para obter mais informações, consulte [gerenciar pessoas de interesse](manage-people-of-interest.md).

Na guia **pesquisas** , você pode criar pesquisas para localizar os dados derramados. Você usará a mesma consulta de pesquisa que usou para localizar os dados derramados para excluir essas mesmas mensagens na [etapa 4](#step-4-delete-the-spilled-data). Para obter mais informações sobre como criar pesquisas, confira [Pesquisar dados em uma investigação](search-for-data.md).

Depois de executar a pesquisa, você pode Visualizar amostras de resultados de pesquisa e exibir estatísticas de pesquisa para avaliar a eficácia da consulta de pesquisa. Depois de identificar os itens que você deseja excluir do Office 365, você pode clicar na guia **evidência** e, em seguida, criar um conjunto de evidências e adicionar resultados de pesquisa que contenham esses itens. 

Para fazer isso, clique na pesquisa que você deseja investigar. Na página do menu suspenso, clique em **Adicionar resultados a evidências** e siga as instruções. Em seguida, nas evidências, você pode revisar documentos individuais, investigar quem teve acesso aos documentos e exportar os documentos. Para simplesmente excluir os documentos em vez de analisá-los, vá para a [etapa 4](#step-4-delete-the-spilled-data). 

> [!IMPORTANT]
> As palavras-chave que você usa na consulta de pesquisa podem conter os dados reais derramados que você está pesquisando. Por exemplo, se você procurar documentos que contenham um número de seguro social e usá-lo como uma palavra-chave na consulta de pesquisa, você deverá excluir a consulta posteriormente para evitar mais derramamento. Você pode excluir a pesquisa ou excluir toda a investigação na [etapa 5](#step-5-close-or-delete-the-investigation). 

## <a name="step-3-review-and-investigate"></a>Etapa 3: analisar e investigar 

Na investigação, vá para a guia **evidência** e clique no conjunto de evidências que você criou na etapa anterior. Após o trabalho de processamento ser concluído e os resultados da pesquisa serem adicionados à evidência, você pode revisar documentos individuais em seu formato nativo, formato de texto ou um formato Near-Native. Você pode criar consultas adicionais para restringir a lista de documentos e marcar documentos para indicar resultados de sua investigação. Para obter mais informações, consulte [Review data in Evidence](review-data-in-evidence.md)

Para agrupar documentos e obter mais assistência para revisão, clique em **gerenciar evidência**. No bloco de **análise** , clique em **analisar**. Isso executará análises avançadas, como detecção de duplicidades, encadeamento de emails e análise de tema. Para obter mais informações, consulte:

- [Executar análise para investigar mais rápido](run-analytics-to-investigate-faster.md)
- [Detecção de duplicata próxima](near-duplicates.md)
- [Conversa de email](email-threading.md)
- [Temas](themes.md)

Para determinar quais usuários estão envolvidos no derramamento de dados, você pode criar uma nova consulta no conjunto de evidências e, em seguida, usar as condições remetente/autor e destinatários. Isso criará uma lista de todos os remetentes, destinatários e autores encontrados nos dados coletados que foram adicionados à evidência. Certifique-se de examinar a lista para determinar se há usuários externos. Para obter mais informações sobre como usar condições para restringir os resultados da pesquisa, consulte [Search Conditions](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-delete-the-spilled-data"></a>Etapa 4: excluir os dados derramados

### <a name="deleting-mailbox-items"></a>Excluir itens de caixa de correio

Após revisar e validar que os resultados da pesquisa contenham apenas as mensagens de email que devem ser excluídas, você pode excluí-las permanentemente executando o comando **New-ComplianceSearchAction-remove-purge HardDelete** em Security & Compliance Central do PowerShell. Para obter instruções, confira [Pesquisar e excluir mensagens de email](../search-for-and-delete-messages-in-your-organization.md). 

Se a recuperação de item único estiver habilitada para caixas de correio em sua organização, os itens excluídos permanentemente serão mantidos na pasta itens recuperáveis do usuário (e acessíveis por administradores) até que o período de retenção de item excluído termine (o padrão é 14 dias). Além disso, se qualquer caixa de correio que contenha dados derramados estiver em um bloqueio legal ou atribuída a uma política de retenção, as mensagens limpas serão mantidas na pasta itens recuperáveis até que a duração da retenção do item expire. Para excluir mensagens de forma rígida imediatamente, você precisa executar tarefas de adição. Para obter instruções, consulte [excluir itens da pasta itens recuperáveis das caixas de correio baseadas em nuvem em espera](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Consulte o gerenciamento de registros ou os departamentos legais antes de remover uma política de retenção ou bloqueio. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de derramamento de dados tem prioridade. 

### <a name="deleting-site-items"></a>Excluindo itens de site

Para excluir permanentemente um documento de um site do SharePoint ou de uma conta do OneDrive, você precisa excluir o documento e, em seguida, excluir da lixeira do site e excluí-lo da lixeira do conjunto de sites. Para obter mais informações, consulte [Excluir documentos no SharePoint e no onedrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Como alternativa, você pode excluir um conjunto de sites inteiro que pode conter dados derramados. Para obter instruções, consulte [excluir um conjunto de sites](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Etapa 5: fechar ou excluir a investigação

Após excluir documentos nos locais de conteúdo de origem (caixas de correio ou sites) no serviço Live, você ainda terá cópias desses documentos que você adicionou às evidências como parte da sua investigação. Para evitar mais dados derramamento, considere a possibilidade de excluir a própria investigação.

Para excluir uma investigação:

1. Na guia **configurações** , clique em **informações de investigação**.

2. Clique em **excluir investigação**. 

Se você não precisar excluir a investigação ou se quiser salvar as informações coletadas durante a investigação, clique em **fechar caso**. Depois, em uma data posterior, você pode reabrir investigações fechadas.