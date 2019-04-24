---
title: Gerenciar trabalhos em investigações de dados
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
ms.openlocfilehash: 3b144fbf5f00f3dbb017ac176c75677970f2f7f2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258179"
---
# <a name="manage-jobs-in-data-investigations-preview"></a>Gerenciar trabalhos em investigações de dados (versão prévia)

Veja a seguir uma lista dos trabalhos (que geralmente são processos de longa duração) que são controlados na guia **trabalhos** de uma investigação em investigações de dados (versão prévia). Esses trabalhos são disparados por ações do usuário ao usar e gerenciar investigações.

| Tipo de trabalho           | Descrição     |
| :----------------- | :----------     |
|Adicionando dados a um conjunto de evidência | Um usuário adiciona os resultados de uma pesquisa a um conjunto de evidências.  Para saber mais, confira [Pesquisar dados em uma investigação](search-for-data.md). |
|Adicionar dados a outro conjunto de evidência | Um usuário adiciona documentos de um conjunto de evidências a um conjunto diferente de evidências no mesmo caso.|
|Adição de dados que não sejam do Office 365 a um conjunto de evidências | Um usuário carrega dados que não são do Office 365 em um conjunto de evidências. Os dados também são indexados durante esse processo. Por exemplo, os arquivos de um servidor de arquivos local ou de um computador cliente são carregados em um conjunto de evidências. Para obter mais informações, consulte [carregar dados não-Office 365 em evidência](load-non-office365-data.md).| 
|Adicionando dados corrigidos a um conjunto de evidências | Dados com erros de processamento são corrigidos e carregados novamente em um conjunto de evidências. Confira mais informações em [correção de erros ao processar dados para uma investigação](error-remediation.md). | 
|ComParando conjuntos de carregamento | Um usuário examina as diferenças entre diferentes conjuntos de carga em um conjunto de evidências. Um conjunto de carga é uma instância de adição de dados a um conjunto de evidências. Por exemplo, se você adicionar os resultados de duas pesquisas diferentes ao mesmo conjunto de evidência, cada uma delas representaria um conjunto de carga. Para obter mais informações, consulte [Manage Load sets](manage-load-sets.md). |
|Convertendo documentos redigidos em PDF|Após um usuário anotar um documento em um conjunto de evidência e redigir uma parte dele, ele poderá optar por converter o documento redigido em um arquivo PDF. Isso garante que a parte redigida não será visível quando o documento for exportado para apresentação. Para obter mais informações, consulte reVisar [dados em evidência](review-data-in-evidence.md). |
|Estimando resultados de pesquisa | Após um usuário criar e executar uma nova pesquisa (ou executar novamente uma pesquisa existente), a ferramenta de pesquisa pesquisa o índice de itens que correspondem à consulta de pesquisa e prepara uma estimativa que inclui o número e o tamanho total de todos os itens pela pesquisa e o número de fontes de dados Sea rched.  Para saber mais, confira [Pesquisar dados em uma investigação](search-for-data.md). | 
|Preparando dados para exportação | Um usuário exporta documentos de um conjunto de evidências. Quando o processo de exportação é concluído, ele pode baixar os dados exportados para um computador local. Para obter mais informações, consulte [exportar dados de uma investigação](export-data.md). | 
|Preparando para a resolução de erros |Quando um usuário seleciona um arquivo e cria uma nova correção de erro no modo de exibição de erro na guia **processamento** de uma investigação, a primeira etapa no processo é carregar o arquivo que tem o erro de processamento para um local de armazenamento do Azure na nuvem da Microsoft. Este trabalho acompanha o andamento do processo de carregamento. Para obter mais informações sobre o fluxo de trabalho de correção de erro, consulte [Error remediation When Processing data for](error-remediation.md)a Investigation.| 
|Preparando visualização de pesquisa | Após um usuário criar e executar uma nova pesquisa (ou executar novamente uma pesquisa existente), a ferramenta de pesquisa prepara um subconjunto de itens de exemplo (que correspondem à consulta de pesquisa) que pode ser visualizado. A visualização dos resultados da pesquisa pode ajudá-lo a determinar a eficácia da pesquisa.  Para saber mais, confira [Pesquisar dados em uma investigação](search-for-data.md). | 
|Indexar novamente os dados de pessoas de interesse | Quando você adiciona uma pessoa de interesse a uma investigação, todos os itens parcialmente indexados na pessoa de fontes de dados selecionadas de interesse são re-indexados por um processo chamado *indexAção avançada*. Esse trabalho também é acionado quando você clica em **Atualizar índice** no modo de exibição de índice na guia **processamento** de uma investigação. Para obter mais informações, consulte [indexAção avançada de dados para uma investigação](index-data-people-of-interest.md).
|Executando o Analytics | Um usuário analisa dados em um conjunto de evidências executando ferramentas de análise, como detecção de duplicidades, análise de threads de email e análise de temas. Para obter mais informações, consulte [executar análise para investigar mais rápido](run-analytics-to-investigate-faster.md). | 
|Marcando documentos | Esse trabalho é acionado quando um usuário clica em **Iniciar trabalho de marcação** no **painel de marcação** ao revisar documentos em um conjunto de evidências. Um usuário pode iniciar esse trabalho depois de marcar documentos em um conjunto de evidências e, em seguida, selecioná-los em massa no painel Exibir documento. Para obter mais informações, consulte [tag Documents in Evidence](tag-documents.md). | 
|||
