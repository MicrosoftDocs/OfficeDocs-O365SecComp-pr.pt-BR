---
title: Exibir atividade de auditoria de responsáveis
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f4bac6ae7a51b01ff6f9b303bb5c2f4911bdb53d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153903"
---
# <a name="view-custodian-audit-activity"></a>Exibir atividade de auditoria de responsáveis

Precisa localizar se um usuário exibir um documento específico ou limpar um item de sua caixa de correio? A descoberta eletrônica avançada agora está integrada à ferramenta de pesquisa de log de auditoria existente no centro de conformidade do & de segurança. Usando essa experiência incorporada, você pode usar a ferramenta de gerenciamento de descoberta eletrônica avançada para facilitar sua investigação, acessando e pesquisando facilmente a atividade dos responsáveis em seu caso.

## <a name="before-you-begin"></a>Antes de começar

Você precisa receber a função de logs de auditoria somente para exibição ou logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Por padrão, essas funções são atribuídas aos grupos de função gerenciamento de conformidade e gerenciamento da organização na página permissões no centro de administração do Exchange. Para permitir que um usuário pesquise o log de auditoria de descoberta eletrônica avançado com o nível mínimo de privilégios, você pode criar um grupo de função personalizado no Exchange Online, adicionar os logs de auditoria somente para exibição ou a função logs de auditoria e, em seguida, adicionar o usuário como membro do novo grupo de funções. Para obter mais informações, consulte Manage role groups in Exchange Online.

> [!IMPORTANT]
> Se você atribuir a um usuário a função logs de auditoria somente para exibição ou logs de auditoria na página permissões no centro de conformidade do & de segurança, elas não poderão pesquisar o log de auditoria do Office 365. Você precisa atribuir as permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online.

## <a name="step-1-search-the-audit-log-for-activities-performed-by-a-custodian"></a>Etapa 1: Pesquisar o log de auditoria para atividades realizadas por um responsáveis

1. Vá para descoberta eletrônica **avançada do >** e abra o caso.
  
2. Clique na guia **responsáveis** .
  
3. Selecione um dos responsáveis na lista e clique em **Exibir atividade de responsáveis** na página do menu suspenso.

    A página de pesquisa de atividades do responsáveis é exibida. Observação os responsáveis que você selecionou na etapa anterior são exibidos na caixa suspensa **responsáveis** . Você pode selecionar diferentes responsáveis na caixa suspensa, mas só pode pesquisar atividades de um único membro por vez.

    ![Página de pesquisa de atividades do responsáveis](../media/AeDCustodianActivities1.png)
   
4. Configure os seguintes critérios de pesquisa:
      
   a. **Atividades** -clique na lista suspensa para exibir as atividades que você pode pesquisar. Depois de executar a pesquisa, somente os registros de auditoria das atividades selecionadas são exibidos. Selecionar **Mostrar resultados de todas as atividades** exibirá os resultados de todas as atividades realizadas pelos responsáveis que correspondam aos outros critérios de pesquisa.

      ![Lista de atividades](../media/CustodianActivityAudit.PNG)
      
      b. **Data de início e data de término** -selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período. Os últimos sete dias são selecionados por padrão. A data e a hora são apresentadas no formato UTC (tempo Universal Coordenado). O intervalo de datas máximo que você pode especificar é um ano.
      
      c. **Responsáveis** – clique nesta caixa e selecione um ou mais responsáveis para exibir os resultados da pesquisa. Os registros de auditoria da atividade selecionada executada pelos usuários selecionados nesta caixa são exibidos na lista de resultados.
      
   5. Click   ![Botão Pesquisar](../media/SearchButton.PNG)  para executar a pesquisa usando seus critérios de pesquisa. Os resultados da pesquisa são carregados e após alguns momentos em que são exibidos em resultados na página de pesquisa de atividades do responsáveis. 

## <a name="step-2-view-the-audit-log-search-results"></a>Etapa 2: exibir os resultados da pesquisa de log de auditoria

Os resultados de uma pesquisa de log de auditoria são exibidos em resultados na página log de auditoria do responsáveis. Um máximo de 5.000 (mais recentes) eventos são exibidos em incrementos de 150 eventos. Para exibir mais eventos, você pode usar a barra de rolagem no painel de resultados ou pode pressionar Shift + End para exibir os próximos 150 eventos.

Os resultados contêm as seguintes informações sobre cada evento retornado pela pesquisa.
- **Date**: a data e hora (no formato UTC) quando o evento ocorreu.

- **Endereço IP**: o endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido em um formato de endereço IPv4 ou IPv6.

- **Usuário**: o usuário (ou conta de serviço) que executou a ação que disparou o evento.

- **Atividade**: a atividade realizada pelo usuário. Esse valor corresponde às atividades que você selecionou na lista suspensa atividades. Para um evento do log de auditoria do administrador do Exchange, o valor desta coluna é um cmdlet do Exchange.

- **Item**: o objeto que foi criado ou modificado como resultado da atividade correspondente. Por exemplo, o arquivo que foi exibido ou modificado ou a conta de usuário que foi atualizada. Nem todas as atividades têm um valor nesta coluna.

- **Detalhe**: detalhes adicionais sobre uma atividade. Novamente, nem todas as atividades terão um valor.

## <a name="step-3-filter-the-search-results"></a>Etapa 3: filtrar os resultados da pesquisa

Além da classificação, você também pode filtrar os resultados de uma pesquisa de log de auditoria. Isso pode ajudá-lo a filtrar rapidamente os resultados de um usuário ou atividade específico. 

Para filtrar os resultados:

 1. Criar e executar uma pesquisa de log de auditoria.
  
2. Quando os resultados forem exibidos, clique em **filtrar resultados**.
 
3. As caixas de palavras-chave são exibidas sob cada cabeçalho de coluna.
  
4. Clique em uma das caixas sob um cabeçalho de coluna e digite uma palavra ou frase, dependendo da coluna que você está filtrando. Os resultados serão reajustados dinamicamente para exibir os eventos que correspondam ao seu filtro.
  
5. Para limpar um filtro, clique no **X** na caixa filtro ou clique em **ocultar filtragem**.

## <a name="export-the-search-results-to-a-file"></a>Exportar os resultados da pesquisa para um arquivo

Você pode exportar os resultados de uma pesquisa de log de auditoria para um arquivo CSV (valor separado por vírgula) no computador local. Você pode abrir esse arquivo no Microsoft Excel e usar recursos como pesquisa, classificação, filtragem e divisão de uma única coluna (que contém células de vários valores) em várias colunas.

1. Execute uma pesquisa de log de auditoria e revise os critérios de pesquisa até que você tenha os resultados desejados.
  
2. Clique em exportar resultados e selecione uma das seguintes opções:

    - **Salvar resultados carregados:** Escolha essa opção para exportar somente as entradas que são exibidas em **resultados** na página **pesquisa de log de auditoria do responsáveis** . O arquivo CSV baixado contém as mesmas colunas (e dados) exibidas na página (data, usuário, atividade, item e detalhes). Uma coluna adicional (intitulada **mais**) é incluída no arquivo CSV que contém mais informações da entrada do log de auditoria. Como você está exportando os mesmos resultados que são carregados (e exibíveis) na página pesquisa de log de auditoria, um máximo de 5.000 entradas são exportadas.
        
    - **Baixar todos os resultados:** Escolha essa opção para exportar todas as entradas do log de auditoria do Office 365 que atendam aos critérios de pesquisa. Para obter um grande conjunto de resultados de pesquisa, escolha essa opção para baixar todas as entradas do log de auditoria, além dos resultados 5.000 que podem ser exibidos na página pesquisa de **log de auditoria do responsáveis** . Essa opção baixará os dados brutos do log de auditoria para um arquivo CSV e conterá informações adicionais da entrada do log de auditoria em uma coluna chamada AuditData. Pode levar mais tempo para baixar o arquivo se você escolher essa opção de exportação porque o arquivo pode ser muito maior do que o baixado, se você escolher a outra opção.
    
      > [!IMPORTANT]
      > Você pode baixar um máximo de 50.000 entradas para um arquivo CSV de uma única pesquisa de log de auditoria. Se as entradas 50.000 forem baixadas para o arquivo CSV, provavelmente você poderá supor que há mais de 50.000 eventos que atingiram os critérios de pesquisa. Para exportar mais do que esse limite, tente usar um intervalo de datas para reduzir o número de entradas de log de auditoria. Você pode ter que executar várias pesquisas com intervalos de datas menores para exportar mais de 50.000 entradas.
        

3. Após selecionar uma opção de exportação, uma mensagem é exibida na parte inferior da janela que solicita que você abra o arquivo CSV, salve-o na pasta downloads ou salve-o em uma pasta específica

Para obter mais informações sobre como exibir, filtrar ou exportar resultados de pesquisa de log de auditoria, confira [Pesquisar o log de auditoria no centro de conformidade do & de segurança](../search-the-audit-log-in-security-and-compliance.md).
