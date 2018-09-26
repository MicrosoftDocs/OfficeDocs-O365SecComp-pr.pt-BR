---
title: Investigar itens parcialmente indexados na Descoberta Eletrônica do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Parcialmente indexados itens (também chamada não indexada itens) são itens de caixa de correio do Exchange e documentos no SharePoint e OneDrive sites que, por algum motivo não foram completamente indexado para pesquisa de conteúdo. Neste artigo, você pode Saiba por que os itens não podem ser indexados para pesquisa e são retornados como itens indexados parcialmente, identificar erros de pesquisa para itens indexados parcialmente e usar um script do PowerShell para determinar a exposição da sua organização para emails parcialmente indexados itens.
ms.openlocfilehash: 98f794e80ea8a6016887ff139bc5b546c438f093
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038074"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a><span data-ttu-id="e1b2c-104">Investigar itens parcialmente indexados na Descoberta Eletrônica do Office 365</span><span class="sxs-lookup"><span data-stu-id="e1b2c-104">Investigating partially indexed items in Office 365 eDiscovery</span></span>

<span data-ttu-id="e1b2c-p102">Uma pesquisa de conteúdo que você executar a partir de segurança do Office 365 &amp; Centro de conformidade inclui automaticamente itens indexados parcialmente nos resultados da pesquisa estimados quando você executa uma pesquisa. Itens indexados parcialmente são itens de caixa de correio do Exchange e documentos no SharePoint e OneDrive para sites corporativos que, por algum motivo, não foram completamente indexadas pela pesquisa. A maioria das mensagens de email e documentos do site são indexados com êxito porque eles ficarem dentro dos [limites de indexação para mensagens de email](limits-for-content-search.md#indexinglimits). No entanto, alguns itens podem exceder esses limites de indexação e serão indexados parcialmente. Aqui estão os outros motivos por que os itens não podem ser indexados para pesquisa e são retornados como itens indexados parcialmente quando você executa uma pesquisa de conteúdo:</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p102">A Content Search that you run from the Office 365 Security &amp; Compliance Center automatically includes partially indexed items in the estimated search results when you run a search. Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search. Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexinglimits). However, some items may exceed these indexing limits, and will be partially indexed. Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="e1b2c-110">Mensagens de email têm um arquivo anexado de um tipo de arquivo que não pode ser indexado; Na maioria dos casos, o tipo de arquivo é [desconhecida ou não suportados para indexação](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span><span class="sxs-lookup"><span data-stu-id="e1b2c-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="e1b2c-111">Mensagens de email têm um arquivo anexado sem um manipulador de válido, como arquivos de imagem; Essa é a causa mais comum de itens de email parcialmente indexados</span><span class="sxs-lookup"><span data-stu-id="e1b2c-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="e1b2c-112">Muitos arquivos anexados a uma mensagem de email</span><span class="sxs-lookup"><span data-stu-id="e1b2c-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="e1b2c-113">Um arquivo anexado a uma mensagem de email é muito grande</span><span class="sxs-lookup"><span data-stu-id="e1b2c-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="e1b2c-114">O tipo de arquivo é suportado para indexação, mas ocorreu um erro de indexação para um arquivo específico</span><span class="sxs-lookup"><span data-stu-id="e1b2c-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="e1b2c-p103">Embora isso varia, a maioria dos clientes do Office 365 organizações ter menos de 1% do conteúdo por volume e menor que 12% do conteúdo pelo tamanho parcialmente é indexado. O motivo para a diferença entre o volume versus tamanho é que arquivos maiores têm maior probabilidade de que contém o conteúdo que não pode ser indexado completamente.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p103">Although it varies, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed. The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="e1b2c-117">Por que a contagem de itens indexados parcialmente altera para uma pesquisa?</span><span class="sxs-lookup"><span data-stu-id="e1b2c-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="e1b2c-p104">Depois de executar uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, o número total e o tamanho dos itens indexados parcialmente nos locais que foram pesquisados estão listados nas estatísticas de resultado de pesquisa que são exibidas nas estatísticas detalhadas para a pesquisa. Observe que esses são chamados *itens indexados* nas estatísticas da pesquisa. Aqui estão algumas coisas que afetarão o número de itens indexados parcialmente que são retornadas nos resultados da pesquisa:</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p104">After you run a Content Search in the Office 365 Security &amp; Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search. Note these are called  *unindexed items*  in the search statistics. Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="e1b2c-p105">Se um item é indexado parcialmente e corresponde à consulta de pesquisa, ela é incluída nas count (e tamanho) de itens de resultado de pesquisa e itens indexados parcialmente. No entanto, quando os resultados da pesquisa mesmo são exportados, o item é incluído apenas com o conjunto de resultados de pesquisa; ele não tiver incluído como um item parcialmente indexado.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p105">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items. However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="e1b2c-p106">Se você especificar um intervalo de datas para uma consulta de pesquisa (incluindo a ele na consulta de palavra-chave) ou usando uma condição, qualquer item parcialmente indexado que não coincidem com o intervalo de datas não está incluído na contagem de itens indexados parcialmente. Apenas os itens indexados parcialmente que ficam dentro do intervalo de datas são incluídos na contagem de itens indexados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p106">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items. Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="e1b2c-p107">**Observação:** Parcialmente indexada itens localizados no SharePoint e OneDrive sites *não estão* incluídos na estimativa de itens indexados parcialmente que é exibida nas estatísticas detalhadas para a pesquisa. No entanto, os itens indexados parcialmente podem ser exportados quando você exportar os resultados de uma pesquisa de conteúdo. Por exemplo, se você somente sites de pesquisa em uma pesquisa de conteúdo, o número estimado parcialmente itens indexados será zero.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p107">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search. However, partially indexed items can be exported when you export the results of a Content Search. For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="e1b2c-128">Calcula a proporção entre itens indexados parcialmente na sua organização</span><span class="sxs-lookup"><span data-stu-id="e1b2c-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="e1b2c-p108">Para entender a exposição da sua organização para itens indexados parcialmente, você pode executar uma pesquisa de todo o conteúdo em todas as caixas de correio (usando uma consulta de palavra-chave em branco). No exemplo a seguir abaixo, há 56,208 (4,830 MB) totalmente indexados 470 (316 MB) e itens indexados parcialmente itens.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p108">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query). In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Exemplo de mostrando de estatísticas de pesquisa itens indexados parcialmente](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="e1b2c-132">Você pode determinar a porcentagem de itens indexados parcialmente usando os seguintes cálculos.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="e1b2c-133">**Para calcular a taxa de itens indexados parcialmente em sua organização:**</span><span class="sxs-lookup"><span data-stu-id="e1b2c-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="e1b2c-134">Usando os resultados da pesquisa do exemplo anterior,. 84% de todos os itens de caixas de correio parcialmente são indexados.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="e1b2c-135">**Para calcular o percentual do tamanho dos itens indexados parcialmente na sua organização:**</span><span class="sxs-lookup"><span data-stu-id="e1b2c-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="e1b2c-p109">Portanto, no exemplo anterior, 6.54% do tamanho total dos itens de caixa de correio são de itens indexados parcialmente. Conforme anteriormente mencionado, a maioria das organizações do Office 365, os clientes têm menos de 1% do conteúdo por volume e menor que 12% do conteúdo pelo tamanho parcialmente é indexado.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p109">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items. As previously stated, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="e1b2c-138">Trabalhando com parcialmente itens indexados</span><span class="sxs-lookup"><span data-stu-id="e1b2c-138">Working with partially indexed items</span></span>

<span data-ttu-id="e1b2c-p110">Em casos quando você precisa ser examinado parcialmente itens para validar que elas não contêm informações relevantes, você pode [Exportar um relatório de pesquisa de conteúdo](export-a-content-search-report.md) que contém informações sobre itens indexados parcialmente. Quando você exporta um relatório de pesquisa de conteúdo, certifique-se de escolher uma das opções de exportação inclui itens indexados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p110">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items. When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![Escolha a opção de segunda ou terceira para exportar itens indexados parcialmente](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="e1b2c-p111">Ao exportar os resultados de pesquisa de conteúdo ou um relatório de pesquisa de conteúdo usando uma destas opções, a exportação inclui um relatório denominado Items.csv não indexados. Este relatório inclui a maioria das mesmas informações que o arquivo ResultsLog.csv; No entanto, o arquivo não indexadas Items.csv também inclui dois campos relacionados a itens indexados parcialmente: **Marcas de erro** e **Propriedades de erro**. Esses campos contêm informações sobre o erro de indexação para cada item parcialmente indexado. Usando as informações nestes dois campos pode ajudá-lo a determinar se ou não o erro de indexação para um determinado afeta sua investigação. Em caso afirmativo, você pode realizar uma pesquisa de conteúdo direcionada e recuperar e exportar mensagens de email específica e documentos do SharePoint ou OneDrive para que você possa examiná-los para determinar se elas são relevantes para a investigação. Para obter instruções detalhadas, consulte [Prepare um arquivo CSV para uma pesquisa de conteúdo direcionado no Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p111">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv. This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**. These fields contain information about the indexing error for each partially indexed item. Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation. If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation. For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="e1b2c-p112">**Observação:** O arquivo não indexadas Items.csv também contém campos denominados **Tipo de erro** e a **Mensagem de erro**. Esses são herdados campos que contêm informações semelhantes às informações dos campos de **Marcas de erro** e **Propriedades de erro** , mas com informações menos detalhadas. Você pode ignorar esses campos herdados com segurança.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p112">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**. These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information. You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="e1b2c-151">Erros relacionados a itens indexados parcialmente</span><span class="sxs-lookup"><span data-stu-id="e1b2c-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="e1b2c-p113">Marcas de erro são compostas de duas partes de informações, o erro e o tipo de arquivo. Por exemplo, em par este erro/filetype:</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p113">Error tags are made up of two pieces of information, the error and the file type. For example, in this error/filetype pair:</span></span>

```
 parseroutputsize_xls
```

   
 <span data-ttu-id="e1b2c-p114">`parseroutputsize`é o erro e `xls` é o tipo de arquivo do arquivo ocorreu o erro. Em casos foram o tipo de arquivo não foi reconhecido ou o tipo de arquivo foi não se aplica ao erro, você verá o valor `noformat` no lugar do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p114">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on. In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="e1b2c-156">A seguir está uma lista de erros e uma descrição da causa do erro de indexação.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="e1b2c-157">**Marca de erro**</span><span class="sxs-lookup"><span data-stu-id="e1b2c-157">**Error tag**</span></span>|<span data-ttu-id="e1b2c-158">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e1b2c-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="e1b2c-159">Uma mensagem de email tiveram muitos anexos e alguns desses anexos não foram processados.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="e1b2c-p115">O analisador de recuperador e documento conteúdo encontrado muitos níveis de anexos aninhados dentro de outros anexos. Alguns desses anexos não foram processadas.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p115">The content retriever and document parser found too many levels of attachments nested inside other attachments. Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="e1b2c-162">Um anexo falha decodificação porque foi protegido por RMS.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="e1b2c-163">Um arquivo anexado a uma mensagem de email era muito grande e não pôde ser processado.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="e1b2c-p116">Ao gravar a mensagem de email processado o índice, uma das propriedades indexáveis era muito grande e foi truncada. As propriedades truncadas estão listadas no campo de propriedades de erro.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p116">When writing the processed email message to the index, one of the indexable properties was too large and was truncated. The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="e1b2c-p117">Uma mensagem de email contidos texto que não puderam ser processado como Unicode válido. A indexação deste item pode estar incompleta.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p117">An email message contained text that couldn't be processed as valid Unicode. Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="e1b2c-168">O conteúdo de anexo ou mensagem de email é criptografado e Office 365 não pôde decodificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-168">The content of attachment or email message is encrypted, and Office 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="e1b2c-p118">Ocorreu um erro desconhecido durante a análise. Normalmente, isso é resultado de um bug de software ou uma falha no serviço.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p118">An unknown error occurred during parsing. This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="e1b2c-171">Um anexo era muito grande para o analisador para manipular e a análise de que o anexo não acontece ou não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="e1b2c-p119">Um anexo foi mal formado e não pôde ser manipulado pelo analisador. Esse resultado do arquivo antigo de can formatos, arquivos criados por um software incompatível ou vírus tentando se algo diferente de solicitadas.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p119">An attachment was malformed and couldn't be handled by the parser. This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="e1b2c-174">A saída devido a uma análise de um anexo era muito grande e foram truncados.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="e1b2c-175">Um anexo tinha um tipo de arquivo que não puderam ser detectados pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-175">An attachment had a file type that Office 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="e1b2c-176">Um anexo tinha um tipo de arquivo Office 365could detectar, mas análise desse tipo de arquivo não é suportado.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="e1b2c-p120">O valor de uma propriedade de email no Exchange repositório era muito grande para ser recuperado e a mensagem não pôde ser processada. Isso geralmente ocorre apenas à propriedade corpo de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p120">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed. This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="e1b2c-179">O conteúdo recuperador falha decodificar uma mensagem protegida por RMS.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="e1b2c-p121">Muitas palavras foram identificadas no documento durante a indexação. Processamento da propriedade interrompido quando está atingindo o limite e a propriedade será truncada.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p121">Too many words were identified in the document during indexing. Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="e1b2c-p122">Campos de erro descrevem quais campos são afetados pelo erro processamento listado no campo marcas de erro. Se estiver pesquisando como uma propriedade `subject` ou `participants`, erros no corpo da mensagem não afetam os resultados da pesquisa. Isso pode ser útil ao determinar exatamente quais itens indexados parcialmente talvez seja necessário investigar.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p122">Error fields describe which fields are affected by the processing error listed in the Error Tags field. If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search. This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="e1b2c-185">Usando um script do PowerShell para determinar a exposição da sua organização para itens de email parcialmente indexados</span><span class="sxs-lookup"><span data-stu-id="e1b2c-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="e1b2c-p123">As etapas a seguir mostram como executar um script do PowerShell que procura todos os itens em todas as caixas de correio do Exchange e, em seguida, gera um relatório sobre proporção da sua organização itens de email parcialmente indexados (pela contagem e pelo tamanho) e exibe o número de itens (e o tipo de arquivo) para cada erro de indexação que ocorre. Use as descrições de marca de erro, na seção anterior, para identificar o erro de indexação.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-p123">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs. Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="e1b2c-188">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `PartiallyIndexedItems.ps1`.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. <span data-ttu-id="e1b2c-189">[Conectar-se à segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="e1b2c-189">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="e1b2c-190">Em segurança &amp; PowerShell do Centro de conformidade, vá para a pasta onde você salvou o script na etapa 1 e, em seguida, execute o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e1b2c-190">In Security &amp; Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
<span data-ttu-id="e1b2c-191">Aqui está um exemplo fo a saída retornada pelo script.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-191">Here's an example fo the output returned by the script.</span></span>
  
![Exemplo de saída do script que gera um relatório sobre exposição da sua organização parcialmente indexados itens de email](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="e1b2c-193">Observe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1b2c-193">Note the following:</span></span>
  
1. <span data-ttu-id="e1b2c-194">O número total e o tamanho dos itens de email e a proporção da sua organização parcialmente indexados itens de email (por contagem e pelo tamanho)</span><span class="sxs-lookup"><span data-stu-id="e1b2c-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="e1b2c-195">As marcas de erro de lista e os tipos de arquivo correspondentes para os quais o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e1b2c-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1b2c-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1b2c-196">See also</span></span>

[<span data-ttu-id="e1b2c-197">Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365</span><span class="sxs-lookup"><span data-stu-id="e1b2c-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
