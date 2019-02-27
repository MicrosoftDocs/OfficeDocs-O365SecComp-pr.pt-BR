---
title: Diferenças entre resultados de pesquisa de descoberta eletrônica estimados e reais no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/13/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- SPO160
- MOE150
ms.assetid: 8f20ca4f-a908-46ec-99e6-9890d269ecf2
description: 'Entenda por que os resultados de pesquisa estimados e reais podem variar nas pesquisas executadas com as ferramentas de descoberta eletrônica no Office 365. '
ms.openlocfilehash: d3edc73d94d51c2582b6ef2077c5e4c834d1ff82
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296114"
---
# <a name="differences-between-estimated-and-actual-ediscovery-search-results-in-office-365"></a>Diferenças entre resultados de pesquisa de descoberta eletrônica estimados e reais no Office 365

Este tópico se aplica a pesquisas que podem ser executadas usando uma das seguintes ferramentas de descoberta eletrônica da Microsoft:  <br/>  
- Pesquisa de conteúdo no centro de conformidade &amp; de segurança do Office 365  <br/>  
- Descoberta eletrônica in-loco no centro de administração do Exchange (Eat)  <br/>  
- A Central de Descoberta Eletrônica no SharePoint Online  <br/> 
   
Quando você executa uma pesquisa de descoberta eletrônica, a ferramenta que você está usando retorna uma estimativa do número de itens (e seu tamanho total) que atendem aos critérios de pesquisa. Por exemplo, quando você executa uma pesquisa no centro de &amp; conformidade de segurança, os resultados estimados da pesquisa são exibidos no painel de detalhes para a pesquisa selecionada.
  
![Estimativa dos resultados exibidos no painel de detalhes da pesquisa selecionada](media/74e4ce83-40be-41a9-b60f-5ad447e79fe4.png)
  
Esta é a mesma estimativa do tamanho total e do número de itens que é exibido na ferramenta de exportação de descoberta eletrônica quando você exporta os resultados para um computador local e no relatório de Resumo de exportação que é baixado com os resultados da pesquisa.
  
**Resultados estimados na ferramenta de exportação de descoberta eletrônica**

![Resultados estimados na ferramenta de exportação de Descoberta Eletrônica](media/d34312a5-0ee6-49aa-9460-7ea0015a6e66.png)
  
**Resultados estimados no relatório de Resumo de exportação**

![Os resultados estimados da pesquisa estão incluídos no relatório de resumo de exportação](media/44b579da-86c2-4f33-81b5-84d604003eda.png)
  
No enTanto, como você observará na captura de tela anterior do relatório de Resumo de exportação, o tamanho e o número dos resultados de pesquisa reais que são realmente baixados são diferentes dos de tamanho e número de resultados de pesquisa estimados. 
  
![Diferença entre resultados de pesquisa estimados e baixados](media/84aef318-230f-430d-9d9e-02f21342d364.png)
  
Aqui estão alguns motivos para estas diferenças:
  
- **A maneira como os resultados são estimados** -uma estimativa dos resultados da pesquisa é apenas isso, uma previsão (e não uma contagem real) dos itens que atendem aos critérios de consulta de pesquisa. Para compilar a estimativa de itens do Exchange, uma lista das IDs de mensagem que atendem aos critérios de pesquisa é solicitada do banco de dados do Exchange pela ferramenta de descoberta eletrônica que você está usando. Mas quando você exporta os resultados da pesquisa, a pesquisa é executada novamente e as mensagens reais são recuperadas do banco de dados do Exchange. Portanto, essas diferenças podem ocorrer devido a como o número estimado de itens e o número real de itens são determinados. 
    
- **Alterações que ocorrem entre o momento ao estimar e exportar resultados de pesquisa** -quando você exporta os resultados da pesquisa, a pesquisa é reiniciada para coletar os itens mais recentes no índice de pesquisa que atendem aos critérios de pesquisa. É possível que haja itens adicionais criados, enviados ou recebidos que atendam aos critérios de pesquisa na hora entre o momento em que os resultados da pesquisa estimados foram coletados e quando os resultados da pesquisa foram exportados. Também é possível que os itens que estavam no índice de pesquisa quando os resultados da pesquisa fossem estimados não estão mais lá porque foram excluídos do local de conteúdo antes de os resultados da pesquisa serem exportados. Uma maneira de reduzir esse problema é especificar um intervalo de datas para uma pesquisa de descoberta eletrônica. Outra maneira é colocar uma retenção em locais de conteúdo para que os itens sejam preservados e não possam ser removidos. 
    
- **Itens** não indexados-itens não indexados para pesquisa podem causar diferenças entre resultados de pesquisa estimados e reais. Por exemplo, a descoberta eletrônica in-loco no Exchange e o centro de descoberta eletrônica no SharePoint não incluem itens não indexados (que não atendam aos critérios de pesquisa) quando você executa uma pesquisa para estimar os resultados da pesquisa. Mas você pode incluir itens não indexados ao exportar os resultados da pesquisa. Se você incluir itens não indexados ao exportar resultados de pesquisa, pode haver mais itens exportados. Isso causará uma diferença entre os resultados de pesquisa estimados e exportados. 
    
    Ao usar a ferramenta de pesquisa de conteúdo no &amp; centro de conformidade de segurança, você tem a opção de incluir itens não indexados na estimativa de pesquisa. O número de itens não indexados retornados pela pesquisa é listado no painel de detalhes junto com outros resultados de pesquisa estimados. Todos os itens não indexados também serão incluídos no tamanho total dos resultados estimados da pesquisa. Ao exportar os resultados da pesquisa, você tem a opção de incluir ou não itens não indexados. A maneira como você configura essas opções pode resultar em diferenças entre os resultados de pesquisa estimados e os atuais que são baixados. 
    
- **Exportar os resultados de uma pesquisa de conteúdo que inclui todos os locais de conteúdo** -se a pesquisa de que você está exportando os resultados for uma pesquisa de todos os locais de conteúdo em sua organização, somente os itens não indexados de locais de conteúdo que contêm os itens que corresponderem aos critérios de pesquisa serão exportados. Em outras palavras, se nenhum resultado de pesquisa for encontrado em uma caixa de correio ou site, todos os itens não indexados nessa caixa de correio ou site não serão exportados. No enTanto, os itens não indexados de todos os locais de conteúdo (mesmo aqueles que não contêm itens que correspondam à consulta de pesquisa) serão incluídos nos resultados de pesquisa estimados. 
    
    Como alternativa, se a pesquisa que você está exportando resultados de locais de conteúdo específicos incluídos, os itens não indexados (que não foram excluídos pelos critérios de pesquisa) de todos os locais de conteúdo especificados na pesquisa serão exportados. Nesse caso, o número estimado de itens não indexados e o número de itens não indexados realmente exportados devem ser os mesmos.
    
    O motivo para não exportar itens não indexados de todos os locais da organização é porque pode aumentar a probabilidade de erros de exportação e aumentar o tempo necessário para exportar e baixar os resultados da pesquisa.
    
- **Formatos de arquivo brutos versus formatos de arquivo** exportados-para itens do Exchange, o tamanho estimado dos resultados da pesquisa é calculado usando os tamanhos de mensagens brutos do Exchange. No enTanto, as mensagens de email são exportadas em um arquivo PST ou como mensagens individuais (que são formatadas como arquivos EML). Ambas as opções de exportação usam um formato de arquivo diferente que mensagens brutas do Exchange, o que resulta no tamanho total de arquivo exportado ser diferente do tamanho estimado do arquivo. 
    
- **Versões de documento** -para documentos do SharePoint, várias versões de um documento não estão incluídas nos resultados de pesquisa estimados. Mas você tem a opção de incluir todas as versões do documento ao exportar os resultados da pesquisa, o que aumentará o número real (e o tamanho total) dos documentos exportados. 
    
- Eliminação **de duplicação** – para itens do Exchange, a eliminação de duplicação reduz o número de itens exportados. Você tem a opção de eliminar a duplicação dos resultados da pesquisa ao exportá-los. Para mensagens do Exchange, isso significa que apenas uma única instância de uma mensagem é exportada, mesmo que essa mensagem possa ser encontrada em várias caixas de correio. Os resultados de pesquisa estimados incluem todas as instâncias de uma mensagem. Portanto, se você escolher a opção de eliminação de duplicação ao exportar resultados de pesquisa, o número real de itens exportados poderá ser consideravelmente menor do que o número estimado de itens. 
    
    Outra coisa a ter em mente se você escolher a opção de eliminação de duplicação é que todos os itens do Exchange são exportados em um único arquivo PST e a estrutura de pastas das caixas de correio de origem não é preservada. O arquivo PST exportado contém apenas os itens de email. No enTanto, um relatório de resultados de pesquisa contém uma entrada para cada mensagem exportada que identifica a caixa de correio de origem onde a mensagem está localizada. Isso ajuda a identificar todas as caixas de correio que contêm uma mensagem duplicada. Se você não habilitar a eliminação de duplicação, um arquivo PST separado será exportado para cada caixa de correio incluída na pesquisa. 
    
## <a name="exporting-unindexed-items-from-the-ediscovery-center-in-sharepoint-online"></a>ExPortando itens não indexados do centro de descoberta eletrônica no SharePoint Online

No centro de descoberta eletrônica no SharePoint Online, você tem a opção de incluir conteúdo não indexado (do Exchange e do SharePoint) quando exporta os resultados de uma pesquisa de descoberta eletrônica. Para fazer isso, selecione a opção **incluir itens que estão criptografados ou com um formato não reconhecido** . Itens não indexados (também chamados de não rastreáveis no SharePoint) são itens no Exchange e no SharePoint que por algum motivo não foram indexados para pesquisa. Itens não indexados do Exchange são listados no relatório de **erros de índice do Exchange** que é incluído quando você exporta os resultados da pesquisa. Da mesma forma, itens não indexados do SharePoint são listados no relatório de **erros de índice do SharePoint** . Quando você exporta itens não indexados, eles são baixados para uma pasta **** chamada não rastreável. Itens não indexados do Exchange são incluídos em um arquivo PST; cada documento não indexado do SharePoint também é baixado. O número de itens não indexados (se houver algum) são listados em cada relatório de erros de índice. O número de itens não indexados nos relatórios deve coincidir com o número de itens não indexados baixados. 
  
 **Quais são as razões nas quais o número de itens não indexados exportados não corresponde ao número de itens no relatório de erros de índice?** Conforme explicado anteriormente, é possível que os itens tenham sido removidos do Office 365 entre o momento em que a estimativa de pesquisa foi executada e a hora em que os resultados da pesquisa foram exportados. Uma discrepância semelhante pode ocorrer para itens não indexados. Por exemplo, o índice de pesquisa pode estar fora da data em que os resultados da pesquisa são exportados. Isso significa que um item não indexado que foi exportado com os resultados da pesquisa pode não estar listado no relatório de erros de índice porque o item não foi indexado no momento em que os resultados da pesquisa foram exportados. Isso resultaria em mais itens não indexados sendo exportados do que os listados no relatório de erros de índice. Da mesma forma, um item não indexado listado no relatório de erro de indexação pode ter sido removido do Office 365 antes do índice de pesquisa ser atualizado. Isso resultaria em menos itens não indexados sendo exportados do que estão listados no relatório de erros de índice. 
  
> [!NOTE]
> Se você não marcar a opção **incluir itens que estão criptografados ou com um formato não reconhecido** ao exportar os resultados da pesquisa ou apenas baixar os relatórios, os relatórios de erros de índice serão baixados, mas não terão entradas. Isso não significa que não há nenhum erro de indexação. Apenas significa que itens não indexados não foram incluídos na exportação. 
  

