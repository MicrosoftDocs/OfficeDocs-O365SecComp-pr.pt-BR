---
title: Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/11/2018
ms.audience: Admin
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.UnindexedItemsLearnMore
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'Saiba mais sobre itens não indexados no Exchange e no SharePoint que você pode incluir em uma pesquisa de conteúdo executada por meio do centro de conformidade do & de segurança. '
ms.openlocfilehash: da51788b3f017811756c3c07294bf6e2712e2e2c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262313"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365

Uma pesquisa de conteúdo que você executa do centro de conformidade do & de segurança no Office 365 inclui automaticamente itens parcialmente indexados nos resultados estimados da pesquisa quando você executa uma pesquisa. Itens parcialmente indexados são itens de caixa de correio do Exchange e documentos em sites do SharePoint e do OneDrive for Business que por algum motivo não foram completamente indexados para pesquisa. No Exchange, um item parcialmente indexado normalmente contém um arquivo — de um tipo de arquivo que não pode ser indexado, que é anexado a uma mensagem de email. Veja algumas outras razões pelas quais os itens não podem ser indexados para pesquisa e são retornados como itens parcialmente indexados quando você executa uma pesquisa: 
  
- O tipo de arquivo não é reconhecido ou não é suportado para indexação.
    
-  As mensagens têm um arquivo anexado sem um manipulador válido, como arquivos de imagem; Essa é a causa mais comum de itens de email parcialmente indexados. 
    
- O tipo de arquivo é compatível com a indexação, mas ocorreu um erro de indexação com um arquivo específico.
    
- Muitos arquivos anexados a uma mensagem de email.
    
- Um arquivo anexado a uma mensagem de email é muito grande.
    
- Um arquivo foi criptografado com tecnologias que não são da Microsoft.
    
- Um arquivo está protegido por senha.
    
> [!NOTE]
> A maioria das organizações do Office 365 tem menos de 1% de conteúdo por volume e menos de 12% por tamanho parcialmente indexado. O motivo para a diferença entre o volume e o tamanho é que os arquivos maiores têm uma maior probabilidade de conteúdo que não pode ser completamente indexado. 
  
Para investigações legais, sua organização pode ser necessária para revisar itens parcialmente indexados. Você também pode especificar se deseja incluir itens parcialmente indexados ao exportar os resultados da pesquisa para um computador local ou ao preparar os resultados para análise com a descoberta eletrônica avançada do Office 365. Para obter mais informações, consulte [investigando itens parcialmente indexados na descoberta eletrônica do Office 365](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Tipos de arquivo não indexados para pesquisa

Determinados tipos de arquivos, como arquivos Bitmap ou MP3, não têm conteúdo que possa ser indexado. Como resultado, os servidores de indexação de pesquisa no Exchange e no SharePoint não realizam indexação de texto completo nesses tipos de arquivos. Estes tipos de arquivo são considerados como tipos de arquivo incompatíveis. Também existem tipos de arquivo para os quais a indexação de texto completo foi desabilitada, por padrão ou por um administrador. Os tipos de arquivo não suportados e desabilitados são rotulados como itens não indexados em pesquisas de conteúdo. Conforme mencionado anteriormente, os itens parcialmente indexados podem ser incluídos no conjunto de resultados de pesquisa quando você executa uma pesquisa, exporta os resultados da pesquisa para um computador local ou prepara os resultados da pesquisa para descoberta eletrônica avançada. 
  
Para obter uma lista de formatos de arquivo com suporte ou desabilitados, confira os tópicos a seguir:
  
- **** - [Formatos de arquivo do Exchange indexados pela pesquisa do Exchange](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **** - [Get-SearchDocumentFormat](https://go.microsoft.com/fwlink/p/?LinkID=724037) do Exchange
    
- **** - [Extensões de nome de arquivo rastreado padrão do SharePoint e tipos de arquivo analisados no SharePoint](https://go.microsoft.com/fwlink/p/?LinkID=404033)
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Mensagens e documentos com tipos de arquivo parcialmente indexados podem ser retornados nos resultados da pesquisa

Nem toda mensagem de email com um anexo de arquivo parcialmente indexado ou cada documento do SharePoint parcialmente indexado é retornado automaticamente como um item parcialmente indexado. Isso ocorre porque outras propriedades de mensagem ou de documento, como a propriedade **Subject** nas mensagens de email e as propriedades **title** ou **Author** para documentos estão indexadas e disponíveis para pesquisa. Por exemplo, uma pesquisa de palavra-chave para "financeiro" retornará itens com um anexo de arquivo parcialmente indexado, se essa palavra-chave aparecer no assunto de uma mensagem de email ou no nome de arquivo ou no título de um documento. No enTanto, se a palavra-chave aparecer somente no corpo do arquivo, a mensagem ou o documento seria retornado como um item parcialmente indexado. 
  
Da mesma forma, as mensagens com anexos de arquivo parcialmente indexados e documentos de um tipo de arquivo parcialmente indexado são incluídas nos resultados da pesquisa quando outras propriedades de mensagem ou documento, que são indexadas e pesquisáveis, atendem aos critérios de pesquisa. Propriedades de mensagem indexadas para pesquisa incluem datas enviadas e recebidas, remetente e destinatário, o nome do arquivo de um anexo e o texto no corpo da mensagem. Propriedades do documento indexadas para pesquisa incluem datas criadas e modificadas. Assim, mesmo que um anexo de mensagem possa ser um item parcialmente indexado, a mensagem será incluída nos resultados de pesquisa regulares se o valor de outras propriedades de mensagem ou de documento corresponder aos critérios de pesquisa.
  
Para obter uma lista de propriedades de email e de documento que você pode pesquisar usando o recurso de pesquisa no centro de conformidade do & de segurança, consulte [keyword queries and Search Conditions for Content Search](keyword-queries-and-search-conditions.md).
  

  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Itens parcialmente indexados incluídos nos resultados da pesquisa
<a name="unindexeditemsresults"> </a>

Sua organização pode ser necessária para identificar e realizar análises adicionais sobre itens parcialmente indexados para determinar o que eles são, o que eles contêm e se são relevantes para uma investigação específica. Como explicado anteriormente, os itens parcialmente indexados nos locais de conteúdo pesquisados são incluídos automaticamente nos resultados de pesquisa estimados. Você tem a opção de incluir esses itens parcialmente indexados ao exportar os resultados da pesquisa ou preparar os resultados da pesquisa para descoberta eletrônica avançada. Para incluir itens parcialmente indexados quando você estiver exportando resultados de pesquisa ou preparando-os para descoberta eletrônica avançada, selecione uma das opções para incluir itens que tenham um formato não reconhecido, sejam criptografadas ou não foram indexadas por outros motivos.
  
Tenha em mente o seguinte sobre itens parcialmente indexados:
  
- Quando você executa uma pesquisa de conteúdo, o número total e o tamanho de itens parcialmente indexados (retornados pela consulta de pesquisa) são exibidos em estatísticas de pesquisa no painel de detalhes, como rotulado como "itens não indexados".
    
- Quando você exporta os resultados da pesquisa e inclui itens parcialmente indexados, os itens do Exchange parcialmente indexados são exportados para um arquivo PST separado para cada caixa de correio na qual eles estão localizados, ou como mensagens individuais, se você selecionar a opção para baixar itens do Exchange como enviadas. os itens do SharePoint parcialmente indexados são exportados para uma pasta chamada não **rastreável**.
    
- Se a pesquisa de que você está exportando os resultados for uma pesquisa de locais de conteúdo específicos ou de todos os locais de conteúdo em sua organização, somente os itens não indexados de locais de conteúdo que contêm itens que correspondam aos critérios de pesquisa serão exportados. In other words, if no search results are found in a mailbox or site, then any unindexed items in that mailbox or site won't be exported. O motivo disso é que exportar itens parcialmente indexados de muitos locais na organização pode aumentar a probabilidade de erros de exportação e aumentar o tempo necessário para exportar e baixar os resultados da pesquisa.
    
    Para exportar itens parcialmente indexados de todos os locais de conteúdo para uma pesquisa, configure a pesquisa para retornar todos os itens (removendo palavras-chave da consulta de pesquisa) e exporte apenas itens parcialmente indexados ao exportar os resultados da pesquisa (clicando **somente em os itens que têm um formato não reconhecido, são criptografados ou não foram indexados por outros motivos** em **Opções de saída**.
    
- Se você optar por incluir todos os itens de caixa de correio nos resultados da pesquisa, ou se uma consulta de pesquisa não especificar nenhuma palavra-chave ou apenas especificar um intervalo de datas, os itens parcialmente indexados podem não ser copiados para o arquivo PST que contém os itens parcialmente indexados. Isso ocorre porque todos os itens, incluindo qualquer item parcialmente indexado, serão automaticamente incluídos nos resultados normais da pesquisa.
    
- Os itens parcialmente indexados não estão disponíveis para visualização. Você precisa exportar os resultados da pesquisa para exibir itens parcialmente indexados retornados pela pesquisa.

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Itens parcialmente indexados excluídos dos resultados da pesquisa

Se um item for parcialmente indexado, mas não atender aos critérios de consulta de pesquisa, ele não será incluído como um item parcialmente indexado nos resultados da pesquisa. Em outras palavras, o item é excluído nos resultados da pesquisa. Por exemplo, digamos que você executa uma pesquisa e não inclui quaisquer palavras-chave ou propriedades porque você deseja incluir todo o conteúdo. Mas você inclui uma condição de intervalo de data para a consulta. Se um item parcialmente indexado estiver fora desse intervalo de datas, ele não será incluído como um item parcialmente indexado. Os intervalos de datas são uma maneira eficaz de excluir itens parcialmente indexados dos resultados da pesquisa.
  
Da mesma forma, se você optar por incluir itens parcialmente indexados ao exportar os resultados de uma pesquisa, os itens parcialmente indexados excluídos dos resultados da pesquisa não serão exportados.
  
Uma exceção a essa regra é quando você cria uma retenção baseada em consulta que está associada a um caso de descoberta eletrônica. Se você criar uma retenção baseada em consulta, todos os itens parcialmente indexados serão colocados em espera. Isso inclui itens parcialmente indexados que não coincidem com os critérios de consulta de pesquisa e itens parcialmente indexados que podem ficar fora de uma condição de intervalo de datas. Para obter mais informações sobre como criar retenções baseadas em consulta, consulte a etapa 4 em [casos de descoberta eletrônica](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>Indexando limites para mensagens na pesquisa de conteúdo

A tabela a seguir descreve os limites de indexação que podem resultar em uma mensagem de email sendo retornada como um item parcialmente indexado em uma pesquisa de conteúdo no Office 365.
  
Para obter uma lista de limites de indexação para documentos do SharePoint, confira [limites de pesquisa do SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Limite de indexação**|**Observações**|**Descrição**|
|:-----|:-----|:-----|
|Tamanho máximo do anexo (excluindo arquivos do Excel)  <br/> |150 MB  <br/> |O tamanho máximo de um anexo de email que será analisado para indexação. Qualquer anexo maior do que esse limite não será analisado para indexação, e a mensagem com o anexo será marcada como parcialmente indexada.  <br/><br/> **Observação:** A análise é o processo em que o serviço de indexação extrai texto do anexo, remove caracteres desnecessários, como pontuação e espaços, e divide o texto em palavras (em um processo chamado geração de tokens), que são armazenados no índice.           |
|Tamanho máximo de arquivos do Excel  <br/> |4 MB  <br/> |O tamanho máximo de um arquivo do Excel localizado em um site ou anexado a uma mensagem de email que será analisada para indexação. Qualquer arquivo do Excel que seja maior do que esse limite não será analisado e o arquivo ou o email que a mensagem com o anexo de arquivo será marcado como não indexado.  <br/> |
|Número máximo de anexos  <br/> |250  <br/> |O número máximo de arquivos anexados a uma mensagem de email que será analisado para indexação. Se uma mensagem tiver mais de 250 anexos, os primeiros 250 anexos serão analisados e indexados, e a mensagem será marcada como parcialmente indexada porque tinha anexos adicionais que não foram analisados.  <br/> |
|Profundidade máxima do anexo  <br/> |até  <br/> |O número máximo de anexos aninhados que são analisados. Por exemplo, se uma mensagem de email tiver outra mensagem anexada a ela e a mensagem anexada tiver um documento do Word anexado, o documento do Word e a mensagem anexada serão indexados. Esse comportamento vai continuar até 30 anexos aninhados.  <br/> |
|Número máximo de imagens anexadas  <br/> |,0  <br/> |Uma imagem anexada a uma mensagem de email é ignorada pelo analisador e não é indexado.  <br/> |
|Tempo máximo gasto na análise de um item  <br/> |30 segundos  <br/> |Um máximo de 30 segundos é gasto em análise de um item para indexação. Se o tempo de análise exceder 30 segundos, o item será marcado como parcialmente indexado.  <br/> |
|Saída de análise máxima  <br/> |2 milhões de caracteres  <br/> |A quantidade máxima de saída de texto do analisador indexado. Por exemplo, se o analisador extrair 8 milhões caracteres de um documento, somente os primeiros 2 milhões de caracteres serão indexados.  <br/> |
|Tokens de anotação máximo  <br/> |2 milhões  <br/> |Quando uma mensagem de email é indexada, cada palavra é anotada com instruções de processamento diferentes que especificam como essa palavra deve ser indexada. Cada conjunto de instruções de processamento é chamado de token de anotação. Para manter a qualidade do serviço no Office 365, há um limite de 2 milhões tokens de anotação para uma mensagem de email.  <br/> |
|Tamanho máximo do corpo no índice  <br/> |67 milhões caracteres  <br/> |O número total de caracteres no corpo de uma mensagem de email e todos os seus anexos. Quando uma mensagem de email é indexada, todo o texto no corpo da mensagem e em todos os anexos é concatenado em uma única cadeia de caracteres. O tamanho máximo dessa cadeia de caracteres indexada é de 67 milhões caracteres.  <br/> |
|Máximo de tokens exclusivos no corpo  <br/> |1 milhão  <br/> |Como explicado anteriormente, os tokens são o resultado da extração de texto do conteúdo, da remoção de Pontuação e de espaços e da divisão em palavras (chamados Tokens) que são armazenadas no índice. Por exemplo, a frase `"cat, mouse, bird, dog, dog"` contém 5 tokens. Mas apenas 4 desses tokens são exclusivos. Há um limite de 1 milhão tokens exclusivos por mensagem de email, o que ajuda a evitar que o índice fique muito grande com tokens aleatórios.  <br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Mais informações sobre itens parcialmente indexados
<a name="moreinfo"> </a>

- Conforme mencionado anteriormente, como as propriedades message e Document e seus metadados são indexados, uma pesquisa de palavra-chave poderá retornar resultados se essa palavra-chave aparecer nos metadados indexados. No entanto, essa mesma pesquisa de palavra-chave poderá não retornar o mesmo item se a palavra-chave só aparece no conteúdo de um item com um tipo de arquivo sem suporte. Nesse caso, o item seria retornado como um item parcialmente indexado.
    
- Se um item parcialmente indexado estiver incluído nos resultados da pesquisa porque ele atende aos critérios de consulta de pesquisa (e não foi excluído), ele não será incluído como um item parcialmente indexado nas estatísticas de pesquisa estimadas. Além disso, ele não será incluído em itens parcialmente indexados quando você exportar os resultados da pesquisa.
    
- Embora um tipo de arquivo tenha suporte para indexação e esteja indexado, pode haver erros de indexação ou de pesquisa que farão com que um arquivo seja retornado como um item parcialmente indexado. Por exemplo, pesquisar um arquivo do Excel muito grande pode ser parcialmente bem-sucedido (porque os primeiros 4 MB são indexados), mas falha porque o limite de tamanho do arquivo foi excedido. Nesse caso, é possível que o mesmo arquivo seja retornado com os resultados da pesquisa e como um item parcialmente indexado.
    
- Arquivos anexados criptografados com tecnologias da Microsoft são indexados e podem ser pesquisados. Arquivos criptografados com tecnologias que não são da Microsoft são parcialmente indexados.
    
- As mensagens de email criptografadas com S/MIME são parcialmente indexadas. Isto inclui mensagens criptografadas com ou sem anexos de arquivo.
    
- As mensagens protegidas usando o Gerenciamento de Direitos de Informação (IRM) são indexadas e são incluídas nos resultados da pesquisa se corresponderem aos parâmetros de pesquisa.

## <a name="see-also"></a>Confira também

[Investigar itens parcialmente indexados na Descoberta Eletrônica do Office 365](investigating-partially-indexed-items-in-ediscovery.md)

