---
title: Gerenciar trabalhos na descoberta eletrônica avançada (versão prévia)
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
ms.openlocfilehash: 9898e3c4861da8dbd90168622395981f34aaa510
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240896"
---
# <a name="manage-jobs-in-advanced-ediscovery-preview"></a>Gerenciar trabalhos na descoberta eletrônica avançada (versão prévia)

Veja a seguir uma lista dos trabalhos (que geralmente são processos de longa duração) que são controlados na guia **trabalhos** de um caso na descoberta eletrônica avançada (visualização). Esses trabalhos são disparados por ações do usuário ao usar e gerenciar ocorrências.

| Tipo de trabalho           | Descrição     |
| :----------------- | :----------     |
|Adicionando dados a um conjunto de trabalho | Um usuário adiciona os resultados de uma pesquisa a um conjunto de trabalho.  Para obter mais informações, consulte [Add Search Results to a Working Set](add-data-to-working-set.md). |
|Adicionando dados a outro conjunto de trabalho | Um usuário adiciona documentos de um conjunto de trabalho a um conjunto de trabalho diferente no mesmo caso.|
|Adicionando dados que não sejam do Office 365 a um conjunto de trabalho | Um usuário carrega dados que não são do Office 365 em um conjunto de trabalho. Os dados também são indexados durante esse processo. Por exemplo, os arquivos de um servidor de arquivos local ou de um computador cliente são carregados em um conjunto de trabalho. Para obter mais informações, consulte [carregar dados não-Office 365 em um conjunto de trabalho](load-non-office365-data.md).| 
|Adicionando dados corrigidos a um conjunto de trabalho | Dados com erros de processamento são corrigidos e carregados novamente em um conjunto de trabalho. Para obter mais informações, consulte [Error remediation When Processing data](error-remediation.md). | 
|ComParando conjuntos de carregamento | Um usuário examina as diferenças entre diferentes conjuntos de carga em um conjunto de trabalho. Um conjunto de carga é uma instância de adição de dados a um conjunto de trabalho. Por exemplo, se você adicionar os resultados de duas pesquisas diferentes ao mesmo conjunto de trabalho, cada uma delas representaria um conjunto de carga. Para obter mais informações, consulte [Manage Load sets](manage-load-sets.md). |
|Convertendo documentos redigidos em PDF|Após um usuário anotar um documento em um conjunto de trabalho e redigir uma parte dele, ele poderá optar por converter o documento redigido em um arquivo PDF. Isso garante que a parte redigida não será visível se o documento for exportado para apresentação. Para obter mais informações, consulte [exibir documentos em um conjunto de trabalho](annotating-and-redacting-documents.md). |
|Estimando resultados de pesquisa | Após um usuário criar e executar uma nova pesquisa (ou executar novamente uma pesquisa existente), a ferramenta de pesquisa pesquisa o índice de itens que correspondem à consulta de pesquisa e prepara uma estimativa que inclui o número e o tamanho total de todos os itens pela pesquisa e o número de fontes de dados sear CHEd.  Para obter mais informações, consulte [coletar dados por um caso](collecting-data-for-ediscovery.md). | 
|Preparando dados para exportação | Um usuário exporta documentos de um conjunto de trabalho. Quando o processo de exportação é concluído, ele pode baixar os dados exportados para um computador local. Para obter mais informações, consulte [exportar dados de caso](exporting-data-ediscover20.md). | 
|Preparando para a resolução de erros |Quando um usuário seleciona um arquivo e cria uma nova correção de erro no modo de exibição de erro na guia **processamento** de um caso, a primeira etapa no processo é carregar o arquivo que tem o erro de processamento para um local de armazenamento do Azure na nuvem da Microsoft. Este trabalho acompanha o andamento do processo de carregamento. Para obter mais informações sobre o fluxo de trabalho de correção de erro, consulte [Error remediation When Processing data](error-remediation.md). | 
|Preparando visualização de pesquisa | Após um usuário criar e executar uma nova pesquisa (ou executar novamente uma pesquisa existente), a ferramenta de pesquisa prepara um subconjunto de itens de exemplo (que correspondem à consulta de pesquisa) que pode ser visualizado. A visualização dos resultados da pesquisa o ajuda a determinar a eficácia da pesquisa.  Para obter mais informações, consulte [coletar dados por um caso](collecting-data-for-ediscovery.md#view-search-results-and-statistics). | 
|Reindexar dados de responsáveis | Quando você adiciona um dos responsáveis, todos os itens parcialmente indexados nas fontes de dados selecionadas do responsáveis são re-indexados por um processo chamado *indexAção avançada*. Esse trabalho também é acionado quando você clica em **Atualizar índice** no modo de exibição de índice na guia **processamento** de uma ocorrência. Para saber mais, confira [indexAção avançada de dados de responsáveis](indexing-custodian-data.md).
|Executando o Analytics | Um usuário analisa dados em um conjunto de trabalho executando ferramentas avançadas de análise de descoberta eletrônica, como detecção de duplicidades, análise de threads de email e análise de temas. Para obter mais informações, consulte [analisar dados em um conjunto de trabalho](analyzing-data-in-working-set.md). | 
|Marcando documentos | Esse trabalho é acionado quando um usuário clica em **Iniciar trabalho de marcação** no **painel de marcação** ao revisar documentos em um conjunto de trabalho. Um usuário pode iniciar esse trabalho depois de marcar documentos em um conjunto de trabalho e, em seguida, selecioná-los em massa no painel Exibir documento. Para obter mais informações, consulte [tag Documents in a Working Set](tagging-documents.md). | 
|||


## <a name="job-status"></a>Status do trabalho

A tabela a seguir descreve os diferentes Estados de status dos trabalhos.

| Status           | Descrição     |
| :----------------- | :----------     |
| Enviado | Um novo trabalho foi criado.  A data e a hora em que o trabalho foi enviado é exibida na coluna **criado** na guia **trabalhos** . |
| Falha no envio | Falha no envio do trabalho.  Você deve tentar executar novamente a ação que disparou o trabalho. |
| Em andamento | O trabalho está em andamento, você pode monitorar o andamento do trabalho na guia **trabalhos** . |
| Foi | O trabalho foi concluído com êxito. A data e hora em que o trabalho foi concluído é exibida na coluna **concluído** da guia **trabalhos** . |
| Parcialmente bem-sucedido | O trabalho foi parcialmente bem-sucedido. |
| Falhou | O trabalho falhou.  Você deve tentar executar novamente a ação que disparou o trabalho. Se o trabalho falhar uma segunda vez, recomendamos que você entre em contato com o suporte da Microsoft e forneça as informações de suporte do trabalho. |
