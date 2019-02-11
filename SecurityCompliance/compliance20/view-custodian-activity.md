---
title: Atividade de auditoria do modo de exibição dos responsáveis
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
ms.openlocfilehash: 34e3fe207cf440c5992cdba7186e919a3968db22
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706142"
---
# <a name="view-custodian-audit-activity"></a>Atividade de auditoria do modo de exibição dos responsáveis

Precisa encontrar se um usuário exibido um documento específico ou removidos de um item de suas caixas de correio? EDiscovery avançado (Preview) agora é integrado com a ferramenta de pesquisa de log de auditoria existente no Centro de conformidade do & de segurança. Usando essa experiência incorporada, você pode usar a ferramenta de gerenciamento dos responsáveis eDiscovery avançado (Preview) para facilitar sua investigação facilmente acessando e pesquisar a atividade responsáveis dentro de seu caso.

## <a name="before-you-begin"></a>Antes de começar

Você precisa ter a função Logs de auditoria somente para exibição ou Logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de funções de gerenciamento da organização na página permissões no Centro de administração do Exchange e gerenciamento de conformidade. Para conceder a um usuário a capacidade de pesquisar o log de auditoria de eDiscovery avançado (Preview) com o nível mínimo de privilégios, você pode criar um grupo de função personalizada no Exchange Online, adicionar a função Logs de auditoria somente para exibição ou Logs de auditoria e, em seguida, adicionar o usuário como membro do novo GA de função grupo. Para obter mais informações, consulte gerenciar grupos de função no Exchange Online.

> [!IMPORTANT]
> Se você atribuir um usuário a função Logs de auditoria somente para exibição ou Logs de auditoria na página permissões no Centro de conformidade do & de segurança, eles não possam pesquisar no log de auditoria do Office 365. Você precisa atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online.

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a>Etapa 1: Criar uma pesquisa de log de auditoria de eDiscovery avançado (Preview)

   1. Selecione uma ocorrência existente a **segurança & Centro de conformidade gt _ avançado descoberta eletrônica (Preview)**.
   
   2. Navegue até a guia **responsáveis** e selecione dos responsáveis.
   
   3. Uma vez que você selecionou um funcionário encarregado, clique em **Exibir dos responsáveis atividade** do painel de detalhes.
   
   4. Configure os seguintes critérios de pesquisa:
      
      r. **atividades** - clique na lista suspensa para exibir as atividades que você pode pesquisar. Depois de executar a pesquisa, somente os registros de auditoria para as atividades selecionadas são exibidos. A seleção de **Mostrar os resultados de todas as atividades** exibirá resultados para todas as atividades que atendem aos critérios de pesquisa.
      
      b. a **Data de início e data de término** - selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. Últimos sete dias são marcados por padrão. A data e hora são apresentados no formato Tempo Universal Coordenado (UTC). O intervalo de datas máximo que você pode especificar é um ano.
      
      resultados para mais c. **responsáveis** - Click nesta caixa e selecione um funcionário encarregado de específico para exibir a pesquisa. Registros de auditoria da atividade selecionada executadas pelos usuários que você selecionar nesta caixa são exibidos na lista de resultados.
    
    1. Clique em **pesquisa** para executar a pesquisa usando os critérios de pesquisa. Os resultados da pesquisa são carregados e, após alguns momentos são exibidas em resultados na página de pesquisa dos responsáveis atividades. 

## <a name="step-2-view-the-audit-log-search-results"></a>Etapa 2: Exibir os resultados da pesquisa de log de auditoria

Os resultados de uma pesquisa de log de auditoria são exibidos em resultados na página log de auditoria dos responsáveis. Um máximo de 5.000 eventos (mais recentes) são exibidos em incrementos de 150 eventos. Para exibir mais eventos você pode usar a barra de rolagem no painel de resultados ou você pode pressionar Shift + End para exibir os eventos de 150 Avançar.

Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa.
- **Data**: A data e hora (no formato UTC) quando o evento ocorreu.

- **Endereço IP**: O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido no formato de endereço de um IPv4 ou IPv6.

- **Usuário**: A conta de usuário (ou serviço) que executou a ação que acionou o evento.

- **Atividade**: A atividade executada pelo usuário. Esse valor corresponde às atividades selecionado na lista suspensa atividades. Para um evento do log de auditoria do administrador do Exchange, o valor nessa coluna é um cmdlet do Exchange.

- **Item**: O objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta de usuário que foi atualizada. Nem todas as atividades têm um valor nessa coluna.

- **Detalhes**: detalhes adicionais sobre uma atividade. Novamente, nem todas as atividades terá um valor.

## <a name="step-3-filter-the-search-results"></a>Etapa 3: Filtrar os resultados de pesquisa

Além de classificar, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Isso pode ajudá-lo a rapidamente filtrar os resultados para um usuário específico ou atividade. 

Para filtrar os resultados:

 1. Criar e executar uma pesquisa de log de auditoria.
  
2. Quando os resultados são exibidos, clique em **filtrar os resultados**.
 
3. Caixas de palavra-chave serão exibidas em cada cabeçalho de coluna.
  
4. Clique em uma das caixas em um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna que você está filtrando. Os resultados serão reajustar dinamicamente para exibir os eventos que correspondem ao seu filtro.
  
5. Para limpar um filtro, clique em **X** na caixa filtro ou basta clicar em **ocultar a filtragem**.

## <a name="export-the-search-results-to-a-file"></a>Exportar resultados da pesquisa para um arquivo

Você pode exportar os resultados de uma pesquisa de log de auditoria para um arquivo de (CSV) de valores separados por vírgulas no computador local. Você pode abrir este arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e a divisão de uma única coluna (que contém as células de valores múltiplos) em várias colunas.

1. Executar uma pesquisa de log de auditoria e posteriormente revisar os critérios de pesquisa até que você tenha os resultados desejados.
  
2. Clique em Exportar resultados e selecione uma das seguintes opções:

    - **Salvar carregado resultados:** Escolha esta opção para exportar apenas as entradas que são exibidas em **resultados** na página de **pesquisa de log de auditoria dos responsáveis** . O arquivo CSV que é baixado contém as mesmas colunas (e dados) exibidos na página (data, usuário, atividade, Item e detalhes). Uma coluna adicional (intitulada **mais**) está incluída no arquivo CSV que contém mais informações da entrada de log de auditoria. Porque você está exportando os mesmos resultados que são carregados (e visualizável) na página de pesquisa de log de auditoria, um máximo de 5.000 entradas são exportados.
        
    - **Baixe todos os resultados:** Escolha esta opção para exportar todas as entradas de log de auditoria do Office 365 que atendam aos critérios de pesquisa. Para um grande conjunto de resultados da pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além de 5.000 resultados que podem ser exibidos na página de pesquisa de **log de auditoria dos responsáveis** . Essa opção baixar os dados brutos do log de auditoria para um arquivo CSV e contém informações adicionais da entrada de log de auditoria em uma coluna chamada AuditData. Pode levar mais tempo para baixar o arquivo, se você escolher essa opção de exportação porque o arquivo pode ser muito maior daquela que é baixado se você escolher a opção outra.
    
      > [!IMPORTANT]
      > Você pode baixar um máximo de 50.000 entradas para um arquivo CSV de uma pesquisa de log de auditoria único. Se 50.000 entradas são baixadas para o arquivo CSV, você pode assumir provavelmente há mais de 50.000 eventos que atendidos os critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas de log de auditoria. Você pode precisar executar várias pesquisas com menores intervalos de data para exportar entradas mais de 50.000.
        

3. Depois de selecionar uma opção de exportação, uma mensagem é exibida na parte inferior da janela solicitando que você abra o arquivo CSV, salve-o na pasta Downloads ou salvá-lo em uma pasta específica

Para obter mais informações sobre como visualizar, a filtragem ou exportar os resultados de pesquisa de log de auditoria, consulte [Search a auditoria efetuar login do Centro de conformidade do & de segurança do Office 365](../search-the-audit-log-in-security-and-compliance.md).