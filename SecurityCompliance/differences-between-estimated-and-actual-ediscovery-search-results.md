---
title: Diferenças entre os resultados de pesquisa de descoberta eletrônica estimados e reais no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/13/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 8f20ca4f-a908-46ec-99e6-9890d269ecf2
description: 'Entenda por que os resultados de pesquisa estimados e reais podem variar em pesquisas executadas com as ferramentas de descoberta eletrônica no Office 365. '
ms.openlocfilehash: 15fd34fc4b2f7edaa4020043d3dd7ffc21d643ad
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523478"
---
# <a name="differences-between-estimated-and-actual-ediscovery-search-results-in-office-365"></a>Diferenças entre os resultados de pesquisa de descoberta eletrônica estimados e reais no Office 365

Este tópico se aplica às pesquisas que podem ser executadas usando uma das seguintes ferramentas de descoberta eletrônica da Microsoft:  <br/>  
- Conteúdo de pesquisa de segurança do Office 365 &amp; Centro de conformidade  <br/>  
- In-Place eDiscovery no Centro de administração do Exchange (EAC)  <br/>  
- A Central de Descoberta Eletrônica no SharePoint Online  <br/> 
   
Quando você executa uma pesquisa de descoberta eletrônica, a ferramenta que você estiver usando retornará uma estimativa do número de itens (e seu tamanho total) que atendam aos critérios de pesquisa. Por exemplo, quando você executa uma pesquisa na segurança &amp; Centro de conformidade, a pesquisa estimados os resultados são exibidos no painel de detalhes para a pesquisa selecionado.
  
![Estimativa dos resultados exibidos no painel de detalhes da pesquisa selecionada](media/74e4ce83-40be-41a9-b60f-5ad447e79fe4.png)
  
Esse é a mesma estimativa do tamanho total e o número de itens que é exibido no eDiscovery ferramenta de exportação quando você exporta os resultados para um computador local e no relatório de resumo de exportação que é baixado com os resultados da pesquisa.
  
**Estimado resulta na ferramenta de exportação de eDiscovery**

![Resultados estimados na ferramenta de exportação de Descoberta Eletrônica](media/d34312a5-0ee6-49aa-9460-7ea0015a6e66.png)
  
**Resultados estimados no relatório de resumo de exportação**

![Os resultados estimados da pesquisa estão incluídos no relatório de resumo de exportação](media/44b579da-86c2-4f33-81b5-84d604003eda.png)
  
No entanto, como você observará a captura de tela anterior do relatório de resumo de exportação, o tamanho e o número de resultados de pesquisa real que realmente são baixadas são diferentes do que o tamanho e o número de resultados de pesquisa estimados. 
  
![Diferença entre resultados de pesquisa estimados e baixados](media/84aef318-230f-430d-9d9e-02f21342d364.png)
  
Aqui estão algumas razões para essas diferenças:
  
- **Os maneira como os resultados são estimados** - uma estimativa dos resultados da pesquisa são exatamente isso, uma estimativa (e não uma contagem real) dos itens que satisfazem os critérios de consulta de pesquisa. Para compilar a estimativa de itens do Exchange, uma lista da mensagem IDs que atendam aos critérios de pesquisa é solicitada do banco de dados Exchange pela ferramenta de eDiscovery que você está usando. Mas, quando você exporta os resultados da pesquisa, a pesquisa é executada novamente e as mensagens reais são recuperadas do banco de dados do Exchange. Portanto, essas diferenças podem resultar por causa de como o número estimado de itens e o número real de itens são determinados. 
    
- **As alterações que ocorrem entre o momento quando estimando e exportar resultados da pesquisa** - ao exportar os resultados da pesquisa, a pesquisa será reiniciada para coletar que mais recente itens no índice de pesquisa que atendam aos critérios de pesquisa. É possível há adicionais itens foram criados, enviados ou recebidos que atendam aos critérios de pesquisa no tempo entre quando os resultados de pesquisa estimados foram coletados e quando os resultados da pesquisa foram exportados. Também é possível que os itens que estavam no índice de pesquisa quando os resultados da pesquisa foram estimados não estão mais lá porque eles foram removidos do conteúdo local antes dos resultados da pesquisa são exportados. Uma maneira para atenuar esse problema é para especificar um intervalo de datas para uma pesquisa de descoberta eletrônica. Outra maneira é colocar uma isenção em locais de conteúdo, para que os itens são preservadas e não podem ser removidos. 
    
- **Itens indexados** - itens que estão indexados para pesquisa podem causar diferenças entre os resultados da pesquisa estimados e reais. Por exemplo, In-Place eDiscovery no Exchange e no Centro de descoberta eletrônica no SharePoint não incluir itens indexados (que não atendem aos critérios de pesquisa) quando você executa uma pesquisa para estimar os resultados da pesquisa. Mas você pode incluir itens indexados quando você exporta os resultados da pesquisa. Se você incluir itens indexados ao exportar os resultados da pesquisa, pode haver mais itens que são exportados. Isso fará com que uma diferença entre os resultados da pesquisa estimados e exportado. 
    
    Ao utilizar a ferramenta de pesquisa de conteúdo na segurança &amp; Centro de conformidade, você tem a opção para incluir itens indexados na estimativa de pesquisa. O número de itens indexados retornados pela pesquisa está listado no painel de detalhes, em conjunto com os outros resultados de pesquisa estimados. Todos os itens indexados também seriam incluídos no tamanho total dos resultados da pesquisa estimados. Ao exportar os resultados da pesquisa, você tem a opção para incluir ou não itens indexados. Como configurar essas opções pode resultar em diferenças entre estimado e a real de resultados da pesquisa que são baixados. 
    
- **Exportando os resultados de uma pesquisa de conteúdo que inclui todos os locais de conteúdo** - se a qual você está exportando os resultados de pesquisa foi uma pesquisa de todos os locais de conteúdo na sua organização e, em seguida, apenas os itens não indexados a partir de locais de conteúdo que contêm itens que correspondem aos critérios de pesquisa serão exportados. Em outras palavras, se nenhum resultado de pesquisa forem encontrado em uma caixa de correio ou de um site, em seguida, todos os itens indexados nessa caixa de correio ou de um site não exportados. No entanto, não indexadas itens de todos os locais de conteúdo (mesmo aqueles que não contêm itens que correspondem à consulta de pesquisa) serão incluídos nos resultados da pesquisa estimados. 
    
    Como alternativa, se a qual você está exportando os resultados de pesquisa incluído locais de conteúdo específico, em seguida, itens indexados (que não são excluídas com os critérios de pesquisa) de todos os locais de conteúdo especificados na pesquisa serão exportados. Nesse caso, o número estimado de itens indexados e o número de itens indexados realmente exportados devem ser os mesmos.
    
    O motivo para a exportação não itens indexados de cada local na organização é porque ele pode aumentar a probabilidade de erros de exportação e aumentar o tempo que leva para exportar e baixe os resultados da pesquisa.
    
- **Formatos de arquivo raw versus formatos de arquivo exportado** - itens para o Exchange, o tamanho estimado dos resultados da pesquisa é calculado usando os brutos tamanhos de mensagem do Exchange. No entanto, as mensagens de email são exportadas em um arquivo PST ou como mensagens individuais (que estão formatadas como arquivos EML). Ambas essas opções de exportação usam um arquivo diferente que brutos mensagens do Exchange, que resulta em tamanho total do arquivo exportado sendo diferente do que o tamanho estimado do arquivo de formato. 
    
- **Versões de documentos** - documentos para o SharePoint, várias versões de um documento não são incluídos nos resultados da pesquisa estimados. Mas você tem a opção para incluir todas as versões de documento ao exportar os resultados de pesquisa, que vai aumentar o número real (e o tamanho total) dos documentos exportados. 
    
- **Eliminação da duplicação** - itens para o Exchange, eliminação da duplicação reduz o número de itens que são exportados. Você tem a opção de eliminação da duplicação os resultados da pesquisa quando você exportá-los. Para mensagens do Exchange, isso significa que apenas uma única instância de uma mensagem é exportada, mesmo que a mensagem pode ser encontrada em várias caixas de correio. Os resultados de pesquisa estimados incluem cada instância de uma mensagem. Portanto, se você escolher a opção de eliminação da duplicação ao exportar os resultados da pesquisa, o número real de itens que são exportados pode ser consideravelmente menor do que o número estimado de itens. 
    
    Outra coisa deve ter em mente, se você escolher a opção de eliminação da duplicação é que todos os itens do Exchange são exportados em um único arquivo PST e a estrutura de pastas das caixas de correio de origem não é preservada. O arquivo PST exportado contém apenas os itens de email. No entanto, um relatório de resultados de pesquisa contém uma entrada para cada mensagem exportada que identifica a caixa de correio de origem onde a mensagem está localizada. Isso ajuda a identificar todas as caixas de correio que contenham uma mensagem duplicada. Se você não habilitar a eliminação da duplicação, um arquivo PST separado é exportado para cada caixa de correio incluída na pesquisa. 
    
## <a name="exporting-unindexed-items-from-the-ediscovery-center-in-sharepoint-online"></a>Exportando itens indexados do Centro de descoberta eletrônica no SharePoint Online

Na Central de descoberta eletrônica no SharePoint Online, você tem a opção para incluir conteúdo não indexado (do Exchange e SharePoint) ao exportar os resultados de uma pesquisa de descoberta eletrônica. Para fazer isso, selecionando a opção de **incluir itens que são criptografados ou ter um formato não reconhecido** . Itens indexados (também chamados de uncrawlable no SharePoint) são itens no Exchange e SharePoint que, por algum motivo, não foram indexado para pesquisa. Não indexadas itens do Exchange são listados no relatório de **Erros de índice do Exchange** que tem incluídos ao exportar os resultados da pesquisa. Da mesma forma, não indexadas itens do SharePoint são listados no relatório de **Erros de índice do SharePoint** . Quando você exportar itens não indexadas, serem transferidas para uma pasta denominada **Uncrawlable**. Itens indexados do Exchange são incluídos em um arquivo PST; cada dos documentos do SharePoint não indexado é baixado muito. O número de itens indexados (se houver alguma) são listados em cada relatório de erros de índice. O número de itens indexados nos relatórios deve corresponder o número de itens indexados que são baixados. 
  
 **Cite alguns motivos, se o número de itens indexados exportados não coincidir com o número de itens no relatório de erros de índice?** Conforme explicado anteriormente, é possível que itens foram removidos do Office 365 entre o momento em que a estimativa de pesquisa foi executada e o momento em que os resultados da pesquisa foram exportados. Discrepância semelhante pode ocorrer para itens indexados. Por exemplo, o índice de pesquisa pode ser check-out data quando os resultados da pesquisa serão exportados. Isso significa que um item não indexado que foi exportado com os resultados da pesquisa talvez não estejam listado no relatório de erros de índice porque o item não foi indexado no momento em que os resultados da pesquisa foram exportados. Isso resultará em itens indexados mais sendo exportado, além dos listados no relatório de erros de índice. Da mesma forma, um item não indexado listado no relatório de erros de índice poderia foram removido do Office 365 antes que o índice de pesquisa foi atualizado. Isso resultará em menos itens indexados sendo exportado, além dos listados no relatório de erros de índice. 
  
> [!NOTE]
> Se você não selecionar a opção de **incluir itens que são criptografados ou ter um formato não reconhecido** ao exportar resultados de pesquisa ou baixar apenas os relatórios, os relatórios de erro de índice são baixados mas não têm todas as entradas. Isso não significa que haja algum erro de indexação. Ela apenas significa que não indexadas itens não foram incluídos na exportação. 
  

