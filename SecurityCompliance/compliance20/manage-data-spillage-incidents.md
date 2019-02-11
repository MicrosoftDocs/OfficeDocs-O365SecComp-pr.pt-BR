---
title: Gerenciar um incidente de algum derramamento de dados no Microsoft 365
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
description: Este artigo descreve como usar a nova ferramenta investigações (Preview) de dados no Centro de conformidade do & de segurança do Office 365 para gerenciar um incidente de algum derramamento de dados.
ms.openlocfilehash: d7adc17d01a0ae2ad6b7bfb7052862a5a6419882
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706172"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Gerenciar um incidente de algum derramamento de dados no Microsoft 365 

Algum derramamento de dados é quando um documento confidencial é liberado para um ambiente de não confiável. Quando um incidente de algum derramamento de dados é detectado, é importante avaliar rapidamente o tamanho e os locais do algum derramamento, examine as atividades do usuário ao redor dele e limpar permanentemente os dados derramados do sistema.

## <a name="scope-of-this-article"></a>Escopo deste artigo

Este artigo fornece uma lista de instruções sobre como remover permanentemente os itens de caixas de correio do Office 365 para que eles não estão mais acessível ou recuperáveis por usuários ou administradores. 

> [!NOTE]
> Quando você exclui os itens localizados em um SharePoint ou OneDrive para o site de negócios, eles são mantidos por 93 dias desde o momento em que você pode excluí-los a partir de seu local original.

## <a name="scenario"></a>Cenário

Você está informado de um incidente de algum derramamento de dados onde um funcionário inconscientemente compartilhadas um documento altamente confidenciais com várias pessoas através de email. Você deseja avaliar rapidamente quem recebidos neste documento, dentro e fora da sua organização. Depois que você tiver investigar o incidente, você planeja compartilhar suas descobertas com outros investigadores para revisar e, em seguida, remover permanentemente os dados derramados do Office 365. Quando a investigação for concluída, você deseja remover todas as evidências. 

## <a name="workflow"></a>Fluxo de trabalho

Aqui está o fluxo de trabalho para usar dados investigações (Preview) para gerenciar um incidente de algum derramamento de dados:

1.  Crie uma investigação de dados.

2.  Pesquise os dados derramados.

3.  Revise e investigar o incidente.

4.  Exclua permanentemente os dados derramados.

5.  Fechar ou excluir a investigação.


## <a name="before-you-begin"></a>Antes de começar

- Você usará a ferramenta investigações de dados (Preview) o Centro de conformidade do & de segurança do Office 365 para criar uma investigação, pesquisar dados derramados e revise e analisá-lo. Em seguida, você usará segurança & PowerShell do Centro de conformidade para excluir permanentemente os dados derramados do Office 365. 

- Para criar uma investigação, você precisa ser membro do grupo de função de administrador de conformidade no Centro de conformidade do & de segurança.

- Para excluir mensagens, você precisa ser membro do grupo de funções de gerenciamento da organização em que o Centro de conformidade do & de segurança ou a ser atribuído à função de pesquisa e limpar. Para obter informações sobre como adicionar usuários a um grupo de funções, consulte [Conceder aos usuários acesso para o Centro de conformidade do & de segurança](../grant-access-to-the-security-and-compliance-center.md). 

- Para controlar o que um investigador pode pesquisar de contas de OneDrive e de caixas de correio de usuário, sua organização pode configurar limites de conformidade. Para obter mais informações, [Estabeleça os limites de conformidade para investigações de descoberta eletrônica](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Etapa 1: Criar uma investigação de dados

Para criar uma investigação de dados:

1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No Centro de conformidade de segurança &, clique em **Dados investigações**.
 
4. Na página **Dados investigações (Preview)** , clique em **criar uma nova investigação**.
    
5. Na página **nova investigação dados** submenu, nomeie a investigação (obrigatório) e, em seguida, digite uma descrição e um número de investigação opcional. Observe que o nome deve ser exclusivo na sua organização.

6. Sob **você deseja definir configurações adicionais depois de criar essa investigação?**, siga um destes procedimentos:

    - Clique em **Sim** para criar a investigação e exibir a página de **configurações** no caso de novo. Isso permite que você adicionar membros a investigação.
    
    - Clique em **não** para acabou de criar a investigação e exibi-la na lista de casos na página **Dados investigações (Preview)** . Se você escolher essa opção, você será adicionado como o único membro de investigação e as configurações de pesquisa e análise padrão será usado. Você pode adicionar membros ou alterar as configurações a qualquer momento depois que a investigação for criada.

7. Clique em **Salvar** para criar a investigação.

    Nova investigação é exibida na lista na página **Dados investigações (Preview)** . 

8. Para abrir uma investigação, clique no nome da investigação. 

    Na guia **página inicial** para a investigação é exibida. 

> [!TIP]
> Considere a possibilidade de estabelecer uma convenção de nomenclatura para investigações e forneça o máximo de informações possível nas nome e descrição para que você pode localizar e consulte a no futuro, se necessário.
 
## <a name="step-2-search-for-the-spilled-data"></a>Etapa 2: Pesquisa para os dados derramadas 
 
Se você souber quais usuários você deseja pesquisar dados derramados, você poderá adicioná-los como pessoas de interesse para mapear suas fontes de dados para a investigação e pesquisar rapidamente suas caixas de correio e a conta de OneDrive. Para adicionar pessoas de interesse à investigação, clique em **pessoas de interesse**e, em seguida, clique em **Adicionar pessoas de interesse**. 

Na guia **pesquisas** , você pode criar pesquisas para localizar os dados derramados. Você usará a mesma consulta de pesquisa que você usou para localizar os dados derramados para excluir as mesmas mensagens na [etapa 4](##step-4:-permanently-delete-the-spilled-data). Para obter mais informações sobre a criação de pesquisas, consulte [criar uma pesquisa para coletar dados](create-search-to-collect-data.md).

Após executar a pesquisa, você pode visualizar exemplos dos resultados de pesquisa e exibir estatísticas de pesquisa para avaliar a eficácia das sua consulta de pesquisa. Depois de identificar os itens que você deseja excluir do Office 365, você pode clique na guia **incidentes** e, em seguida, criar um incidente e adicionar os resultados de pesquisa que contêm os itens. 

Para fazer isso, clique na pesquisa que você deseja investigar. Na página submenu, clique em **Adicionar resultados a incidente** e siga as instruções. Em seguida, no incidente, você pode revisar documentos individuais, investigar quem tem acesso a documentos e exportar os documentos. Para simplesmente excluir os documentos em vez de revisá-las, vá para a [etapa 4](##step-4:-permanently-delete-the-spilled-data). 

> [!IMPORTANT]
> As palavras-chave que podem ser usados na consulta de pesquisa podem conter os dados reais derramados que você está procurando. Por exemplo, se você procurar documentos contendo um número de seguridade social e você pode usá-lo como uma palavra-chave na consulta de pesquisa, você deve excluir a consulta posteriormente para evitar a algum derramamento. Você pode excluir a pesquisa ou excluir a investigação inteira na [etapa 5](##step-5:-close-or-delete-investigation). 

## <a name="step-3-review-and-investigate"></a>Etapa 3: Revise e investigar 

Na investigação, vá para a guia de **incidentes** e clique no incidente que você criou na etapa anterior. Depois que o trabalho de processamento será concluído e os resultados da pesquisa são adicionados ao incidente, você pode analisar documentos individuais no formato nativo, formato de texto ou um formato de quase nativos. Você pode criar consultas adicionais para restringir ainda mais a lista de documentos e documentos de marca para indicar as descobertas de sua investigação.

Para agrupar documentos e obter assistência mais para sua análise, clique em **Gerenciar incidente**. No lado a lado **Analytics** , clique em **Analisar**. Isso será executado análises avançadas, como a detecção de duplicatas, email threading e análises de tema. Para obter mais informações, consulte:

- [Perto de detecção de duplicatas](near-duplicates.md)
- [Email threading](email-threading.md)
- [Temas](themes.md)

Para determinar quais usuários estão envolvidos no algum derramamento de dados, você pode criar uma nova consulta no incidente e usar o remetente/autor e condições de destinatários. Isso criará uma lista de todos os remetentes confiáveis, destinatários e autores encontrados nos dados coletados que foi adicionados ao incidente. Certifique-se de examinar a lista a fim de determinar se há qualquer usuários externos na lista. Para obter mais informações, consulte [condições de pesquisa](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-permanently-delete-the-spilled-data"></a>Etapa 4: Excluir permanentemente os dados derramados

### <a name="deleting-mailbox-items"></a>Excluindo itens de caixa de correio

Depois de revisar e validar que os resultados da pesquisa contenham somente as mensagens de email que devem ser excluídas, você pode excluí-los permanentemente executando o **New-ComplianceSearchAction-limpar - PurgeType HardDelete** command na segurança & conformidade Centro PowerShell. Para obter instruções, consulte [Procurar e excluir mensagens de email](../search-for-and-delete-messages-in-your-organization.md). 

Observe que se a recuperação de item único está habilitada para caixas de correio em sua organização, itens excluídos permanentemente será retido na pasta de itens recuperáveis do usuário (e acessível por administradores) até as extremidades de período de retenção do item excluído (o padrão é 14 dias). Além disso, se qualquer uma das caixas de correio que contêm dados derramados estiver em retenção legal ou atribuído a uma política de retenção, mensagem removida será mantida na pasta itens recuperáveis até que a suspensão seja removida ou a caixa de correio é excluída de políticas de retenção. A exclusão dura mensagens imediatamente, você precisará executar tarefas de adição. Para obter instruções, consulte [Excluir itens na pasta de caixas de correio baseadas em nuvem em espera itens recuperáveis ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Verifique com o gerenciamento de registros ou departamentos legais antes de remover uma política de retenção ou de espera. Sua organização pode ter uma política que define se uma caixa de correio em espera ou um incidente de algum derramamento de dados tem prioridade. 

### <a name="deleting-site-items"></a>Excluindo itens do site

Para excluir permanentemente um documento de um site do SharePoint ou OneDrive para negócios conta, você precisa excluí-lo e, em seguida, você precisará excluir do site e, em seguida, excluído da Lixeira do conjunto de sites. Para obter instruções, consulte [Excluir documentos no SharePoint e OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Como alternativa, você pode excluir um conjunto de sites inteiro que talvez continha derramada de dados. Para obter instruções, consulte [Excluir um conjunto de sites](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Etapa 5: Fechar ou excluir a investigação

Após a exclusão de documentos em locais de conteúdo de origem (caixas de correio ou sites), você ainda terá cópias desses documentos que você adicionou à incidentes como parte de sua investigação. Para evitar mais algum derramamento de dados, você deve considerar a investigação a exclusão.

Para excluir uma investigação:

1. Na guia **configurações** , clique em **informações de investigação**.

2. Clique em **Excluir caso**. 

Se você não precisa excluir a investigação ou se você deseja salvar a informação que você coletou durante a investigação, você pode clicar em **Fechar o caso**. Posteriormente, você pode reabrir investigações fechadas.