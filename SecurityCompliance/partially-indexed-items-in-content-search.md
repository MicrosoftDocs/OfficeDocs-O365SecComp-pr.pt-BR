---
title: Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/11/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.UnindexedItemsLearnMore
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'Saiba mais sobre itens indexados no Exchange e SharePoint que você pode incluir em uma pesquisa de conteúdo executados por meio de segurança do Office 365 &amp; Centro de conformidade. '
ms.openlocfilehash: 4624985a9c80313d0222470e6cfb2c56495f2142
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523583"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365

Uma pesquisa de conteúdo que você executar a partir de segurança do Office 365 &amp; Centro de conformidade inclui automaticamente itens indexados parcialmente nos resultados da pesquisa estimados quando você executa uma pesquisa. Itens indexados parcialmente são itens de caixa de correio do Exchange e documentos no SharePoint e OneDrive para sites corporativos que, por algum motivo, não foram completamente indexadas pela pesquisa. No Exchange, um item parcialmente indexado normalmente contém um arquivo — de um tipo de arquivo que não pode ser indexado — que é anexado a uma mensagem de email. Aqui estão alguns motivos por que os itens não podem ser indexados para pesquisa e são retornados como itens indexados parcialmente quando você executa uma pesquisa: 
  
- O tipo de arquivo é não reconhecido ou sem suporte para indexação.
    
-  As mensagens têm um arquivo anexado sem um manipulador de válido, como arquivos de imagem; Esta é a causa mais comum de itens de email parcialmente indexados. 
    
- O tipo de arquivo é compatível com a indexação, mas ocorreu um erro de indexação com um arquivo específico.
    
- Muitos arquivos anexados a uma mensagem de email.
    
- Um arquivo anexado a uma mensagem de email é muito grande.
    
- Um arquivo foi criptografado com tecnologias que não são da Microsoft.
    
- Um arquivo está protegido por senha.
    
> [!NOTE]
> A maioria das organizações do Office 365 tem menos de 1% do conteúdo por volume e menor que % de 12 pelo tamanho parcialmente é indexado. O motivo para a diferença entre o tamanho e volume é que arquivos maiores têm maior probabilidade de que contém o conteúdo que não pode ser indexado completamente. 
  
Para investigações legais, a sua organização pode ser necessária revisar itens indexados parcialmente. Você também pode especificar se deseja incluir itens indexados parcialmente ao exportar os resultados da pesquisa para um computador local ou quando você preparar os resultados para análise com eDiscovery avançadas do Office 365. Para obter mais informações, consulte [Investigating parcialmente indexados itens no eDiscovery do Office 365](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Tipos de arquivo não indexados para pesquisa

Certos tipos de arquivos, como um Bitmap ou arquivos MP3, não contêm o conteúdo que pode ser indexado. Como resultado, a pesquisa de servidores de indexação no Exchange e SharePoint não realize a indexação de texto completo sobre esses tipos de arquivos. Esses tipos de arquivos são considerados tipos de arquivo incompatíveis. Também há tipos de arquivo para o qual a indexação de texto completo foi desabilitada, por padrão, ou por um administrador. Tipos de arquivo não suportado, mas desabilitado são rotulados como itens indexados em pesquisas de conteúdo. Conforme indicadas anteriormente, parcialmente indexados itens podem ser incluídos no conjunto de resultados da pesquisa quando você executa uma pesquisa, exportar os resultados da pesquisa para um computador local ou preparar os resultados da pesquisa do eDiscovery avançado. 
  
Para obter uma lista de formatos de arquivo com suporte ou desabilitados, confira os tópicos a seguir:
  
- **Exchange** - [formatos de arquivo indexados pela pesquisa do Exchange](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **Exchange** - [Get-SearchDocumentFormat](https://go.microsoft.com/fwlink/p/?LinkID=724037)
    
- **SharePoint** - [padrão extensões de nome de arquivo rastreado e tipos de arquivo no SharePoint analisados](https://go.microsoft.com/fwlink/p/?LinkID=404033)
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Mensagens e documentos com parcialmente indexados tipos que podem ser retornados nos resultados da pesquisa de arquivo

Não todas as mensagens de email com um anexo de arquivo indexados parcialmente ou todos os documentos do SharePoint parcialmente indexado automaticamente é retornado como um item parcialmente indexado. Isso ocorre porque a outra mensagem ou propriedades de documento, como a propriedade **Subject** em mensagens de email e as propriedades de **título** ou **autor** de documentos são indexados e estão disponíveis a serem pesquisados. Por exemplo, uma pesquisa de palavra-chave para "financeiro" retornarão itens com um anexo de arquivo indexados parcialmente se essa palavra-chave for exibida no campo assunto de uma mensagem de email ou o nome de arquivo ou o título de um documento. No entanto, se a palavra-chave for exibida somente no corpo do arquivo, a mensagem ou documento seria retornado como um item parcialmente indexado. 
  
Da mesma forma, as mensagens com anexos de arquivos indexados parcialmente e documentos de um tipo de arquivo indexados parcialmente são incluídas nos resultados da pesquisa quando outras propriedades de mensagem ou documento, que são indexados e pesquisável, atendam aos critérios de pesquisa. Propriedades de mensagem que são indexadas pela pesquisa incluem datas enviadas e recebidas, remetente e destinatário, o nome do arquivo de um anexo e texto no corpo da mensagem. Propriedades de documento indexadas para pesquisa incluem datas criadas e modificadas. Portanto, mesmo que um anexo da mensagem pode ser um item parcialmente indexado, a mensagem será incluída nos resultados da pesquisa regular se o valor das outras propriedades de mensagem ou documento corresponder os critérios de pesquisa.
  
Para obter uma lista das propriedades de email e documentos que você pode pesquisar usando o recurso de pesquisa na segurança &amp; Centro de conformidade, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).
  

  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Itens indexados parcialmente incluídos nos resultados da pesquisa
<a name="unindexeditemsresults"> </a>

Sua organização pode ser necessária identificar e executar análises adicionais em itens indexados parcialmente para determinar quais elas são, o que eles contêm e se eles são relevantes para uma investigação específica. Conforme explicado anteriormente, os itens indexados parcialmente em locais de conteúdo que são pesquisados são incluídos automaticamente com os resultados de pesquisa estimados. Você tem a opção para incluir esses itens indexados parcialmente quando você exporta os resultados da pesquisa ou preparar os resultados da pesquisa do eDiscovery avançado. Para incluir itens indexados parcialmente quando você está exportando os resultados da pesquisa ou Preparando-los para descoberta eletrônica avançada, selecione uma das opções para incluir itens que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos.
  
Lembre-se sobre itens indexados parcialmente o seguinte:
  
- Quando você executa uma pesquisa de conteúdo, o número total e o tamanho dos itens indexados parcialmente (retornado pela consulta de pesquisa) são exibidas nas estatísticas de pesquisa no painel de detalhes, como rotulados como "itens indexados".
    
- Quando você exporta os resultados da pesquisa e incluir itens indexados parcialmente, itens indexados parcialmente do Exchange são exportados para um arquivo PST separado para cada caixa de correio no qual eles estão localizados, ou como mensagens individuais, se você selecionar a opção de baixar itens do Exchange como mensagens. itens indexados parcialmente do SharePoint são exportados para uma pasta denominada **Uncrawlable**.
    
- Se a pesquisa para o qual você está exportando os resultados de uma pesquisa de locais de conteúdo específico ou todos os locais de conteúdo na sua organização, apenas os itens não indexados a partir de locais de conteúdo que contêm os itens que correspondem aos critérios de pesquisa serão exportados. Em outras palavras, se nenhum resultado de pesquisa forem encontrado em uma caixa de correio ou de um site, em seguida, todos os itens indexados nessa caixa de correio ou de um site não exportados. O motivo para isso é que exportar itens indexados parcialmente de muitos dos locais na organização pode aumentar a probabilidade de erros de exportação e aumentar o tempo que leva para exportar e baixe os resultados da pesquisa.
    
    Para exportar itens indexados parcialmente de todos os locais de conteúdo para uma pesquisa, configurar a pesquisa para retornar todos os itens (removendo qualquer palavra-chave da consulta de pesquisa) e clique em seguida exportar apenas parcialmente itens indexados quando você exporta os resultados da pesquisa (clicando **apenas itens que tenham um formato não reconhecido, são criptografados ou não foram indexados por outros motivos** em **Opções de saída**).
    
- Se você optar por incluir todos os itens de caixa de correio nos resultados da pesquisa, ou se uma consulta de pesquisa não especifica qualquer palavra-chave ou apenas Especifica um intervalo de datas, itens indexados parcialmente não podem ser copiados para o arquivo PST que contém os itens indexados parcialmente. Isso acontece porque todos os itens, incluindo quaisquer itens indexados parcialmente, serão incluídos automaticamente nos resultados da pesquisa regular.
    
- Itens indexados parcialmente não estão disponíveis a ser visualizado. Você precisa exportar os resultados de pesquisa para exibir itens indexados parcialmente retornados pela pesquisa.

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Parcialmente indexados itens excluídos dos resultados da pesquisa

Se um item é indexado parcialmente, mas não atender aos critérios de consulta de pesquisa, ele não será incluído como um item parcialmente indexado nos resultados da pesquisa. Em outras palavras, o item é excluído dos resultados da pesquisa. Por exemplo, digamos que você executa uma pesquisa e não incluir quaisquer palavras-chave ou propriedades porque você deseja incluir todo o conteúdo. Mas incluir uma condição de intervalo de data para a consulta. Se um item parcialmente indexado cair fora esse intervalo de datas, ele não será incluído como um item parcialmente indexado. Os intervalos de data são uma maneira eficaz para excluir itens indexados parcialmente de resultados da pesquisa.
  
Da mesma forma, se você optar por incluir itens indexados parcialmente ao exportar os resultados de uma pesquisa, parcialmente indexados itens que foram excluídos dos resultados da pesquisa não ser exportados.
  
Uma exceção a essa regra é quando você cria uma isenção baseado em consulta que está associado a um caso de eDiscovery. Se você criar uma isenção baseado em consulta, todos os itens indexados parcialmente são colocados em espera. Isso inclui itens indexados parcialmente que não correspondem aos critérios de consulta de pesquisa e parcialmente indexados que poderão ficar fora de uma condição de intervalo de data. Para obter mais informações sobre a criação baseada em consulta contém, consulte a etapa 4 em [casos de descoberta eletrônica no Centro de conformidade & segurança do Office 365](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>Limites de indexação para mensagens na pesquisa de conteúdo

A tabela a seguir descreve os limites de indexação que possam resultar em uma mensagem de email que está sendo retornada como um item indexado parcialmente em uma pesquisa de conteúdo no Office 365.
  
Para obter uma lista de indexação limites para documentos do SharePoint, consulte [limites de pesquisa do SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Limite de indexação**|**Observações**|**Descrição**|
|:-----|:-----|:-----|
|Tamanho máximo de anexo (excluindo arquivos do Excel)  <br/> |150 MB  <br/> |O tamanho máximo de um anexo de email que analisa para indexação. Qualquer anexo que for maior do que esse limite não ser analisado para indexação e a mensagem com o anexo será marcada como parcialmente indexados.<br/><br/> **Observação:** Analisar é o processo de onde o serviço de indexação extrai o texto do anexo, remove caracteres desnecessários como pontuação e espaços e divide o texto em palavras (em um processo de geração de tokens de chamada), que são armazenados no índice.           |
|Tamanho máximo de arquivos do Excel  <br/> |4 MB  <br/> |O tamanho máximo de um arquivo do Excel localizado em um site ou anexado a uma mensagem de email que será analisada para indexação. Qualquer arquivo do Excel que é maior do que esse limite não ser analisado e o arquivo ou o email que a mensagem com o anexo de arquivo será marcada como não indexados.  <br/> |
|Número máximo de anexos  <br/> |250  <br/> |O número máximo de arquivos anexados a uma mensagem de email que será analisada para indexação. Se uma mensagem tiver mais de 250 anexos, os primeiros 250 anexos são analisados e indexados, e a mensagem é marcada como parcialmente indexados porque ele tinha adicionais anexos que não foram analisados.  <br/> |
|Profundidade máxima de anexo  <br/> |30  <br/> |O número máximo de anexos aninhados, que são analisados. Por exemplo, se uma mensagem de email tem outra mensagem anexada a ele e a mensagem anexada tem um documento do Word anexado, o documento do Word e a mensagem anexada serão indexados. Esse comportamento continuará até 30 anexos aninhados.  <br/> |
|Número máximo de imagens anexados  <br/> |0  <br/> |Uma imagem que é anexada a uma mensagem de email é ignorada pelo analisador e não é indexada.  <br/> |
|Tempo máximo gasto um item de análise  <br/> |30 segundos  <br/> |Um máximo de 30 segundos é gasto na análise de um item para indexação. Se o tempo de análise excede 30 segundos, o item está marcado como parcialmente indexados.  <br/> |
|Saída do analisador de máximo  <br/> |2 milhões de caracteres  <br/> |A quantidade máxima de saída de texto do analisador da é indexada. Por exemplo, se o analisador extraído 8 milhões de caracteres de um documento, apenas os primeiro 2 milhões de caracteres são indexados.  <br/> |
|Tokens de anotação máximo  <br/> |2 milhões  <br/> |Quando uma mensagem de email é indexada, cada palavra é anotada com instruções de processamento de diferentes que especificam como o que o word deve ser indexado. Cada conjunto de instruções de processamento é chamado um token de anotação. Para manter a qualidade do serviço no Office 365, há um limite de tokens de anotação 2 milhões para uma mensagem de email.  <br/> |
|Tamanho máximo do corpo no índice  <br/> |67 milhões de caracteres  <br/> |O número total de caracteres no corpo de uma mensagem de email e todos os seus respectivos anexos. Quando uma mensagem de email é indexada, todo o texto no corpo da mensagem e em todos os anexos é concatenado em uma única cadeia de caracteres. O tamanho máximo dessa cadeia de caracteres que é indexada é 67 milhões de caracteres.  <br/> |
|Máximo tokens exclusivos no corpo  <br/> |1 milhão  <br/> |Explicado como previamente, tokens são o resultado de extrair texto de conteúdo, removendo a pontuação e espaços e, em seguida, dividindo-la em palavras (chamadas de tokens) que são armazenadas no índice. Por exemplo, a frase `"cat, mouse, bird, dog, dog"` contém 5 tokens. Mas apenas 4 dessas tokens exclusivos. Não há um limite de 1 milhão de tokens exclusivo por mensagem de email, o que ajuda a impedir que o índice obtendo muito grande com tokens aleatórios.<br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Para obter mais informações sobre itens indexados parcialmente
<a name="moreinfo"> </a>

- Conforme indicado anteriormente, como as propriedades de mensagem e o documento e seus metadados estão indexados, uma pesquisa de palavra-chave pode retornar resultados se essa palavra-chave aparecer nos metadados indexados. No entanto, essa mesma pesquisa de palavra-chave não pode retornar o mesmo item se a palavra-chave só aparece no conteúdo de um item com um tipo de arquivo incompatíveis. Nesse caso, o item será retornado como um item parcialmente indexado.
    
- Se um item parcialmente indexado está incluído nos resultados da pesquisa, porque ele atendidos os critérios de consulta de pesquisa (e não tenha sido excluído), em seguida, ele não será incluído como um item parcialmente indexado nas estatísticas de pesquisa estimados. Além disso, ele não será incluído com itens indexados parcialmente ao exportar os resultados da pesquisa.
    
- Embora um tipo de arquivo é suportado para indexação e é indexado, pode haver erros de indexação ou de pesquisa que fará com que um arquivo a ser retornada como um item parcialmente indexado. Por exemplo, a pesquisa de um arquivo do Excel muito grande pode ser parcialmente bem-sucedida (porque são indexados dos primeiros 4 MB), mas, em seguida, falha porque o limite de tamanho de arquivo é excedido. Nesse caso, é possível que o mesmo arquivo será retornado com os resultados da pesquisa e como um item parcialmente indexado.
    
- Arquivos anexados criptografados com tecnologias Microsoft são indexados e podem ser pesquisados. Arquivos criptografados com tecnologias de não-Microsoft parcialmente são indexados.
    
- Emails criptografados com S/MIME parcialmente são indexados. Isso inclui mensagens criptografadas com ou sem anexos de arquivo.
    
- As mensagens protegidas usando o Gerenciamento de Direitos de Informação (IRM) são indexadas e são incluídas nos resultados da pesquisa se corresponderem aos parâmetros de pesquisa.

## <a name="see-also"></a>Confira também

[Investigar itens parcialmente indexados na Descoberta eletrônica do Office 365](investigating-partially-indexed-items-in-ediscovery.md)

