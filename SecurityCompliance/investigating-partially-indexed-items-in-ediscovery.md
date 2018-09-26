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
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a>Investigar itens parcialmente indexados na Descoberta Eletrônica do Office 365

Uma pesquisa de conteúdo que você executar a partir de segurança do Office 365 &amp; Centro de conformidade inclui automaticamente itens indexados parcialmente nos resultados da pesquisa estimados quando você executa uma pesquisa. Itens indexados parcialmente são itens de caixa de correio do Exchange e documentos no SharePoint e OneDrive para sites corporativos que, por algum motivo, não foram completamente indexadas pela pesquisa. A maioria das mensagens de email e documentos do site são indexados com êxito porque eles ficarem dentro dos [limites de indexação para mensagens de email](limits-for-content-search.md#indexinglimits). No entanto, alguns itens podem exceder esses limites de indexação e serão indexados parcialmente. Aqui estão os outros motivos por que os itens não podem ser indexados para pesquisa e são retornados como itens indexados parcialmente quando você executa uma pesquisa de conteúdo:
  
- Mensagens de email têm um arquivo anexado de um tipo de arquivo que não pode ser indexado; Na maioria dos casos, o tipo de arquivo é [desconhecida ou não suportados para indexação](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)
    
- Mensagens de email têm um arquivo anexado sem um manipulador de válido, como arquivos de imagem; Essa é a causa mais comum de itens de email parcialmente indexados
    
- Muitos arquivos anexados a uma mensagem de email
    
- Um arquivo anexado a uma mensagem de email é muito grande
    
- O tipo de arquivo é suportado para indexação, mas ocorreu um erro de indexação para um arquivo específico
    
Embora isso varia, a maioria dos clientes do Office 365 organizações ter menos de 1% do conteúdo por volume e menor que 12% do conteúdo pelo tamanho parcialmente é indexado. O motivo para a diferença entre o volume versus tamanho é que arquivos maiores têm maior probabilidade de que contém o conteúdo que não pode ser indexado completamente.
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a>Por que a contagem de itens indexados parcialmente altera para uma pesquisa?

Depois de executar uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, o número total e o tamanho dos itens indexados parcialmente nos locais que foram pesquisados estão listados nas estatísticas de resultado de pesquisa que são exibidas nas estatísticas detalhadas para a pesquisa. Observe que esses são chamados *itens indexados* nas estatísticas da pesquisa. Aqui estão algumas coisas que afetarão o número de itens indexados parcialmente que são retornadas nos resultados da pesquisa: 
  
- Se um item é indexado parcialmente e corresponde à consulta de pesquisa, ela é incluída nas count (e tamanho) de itens de resultado de pesquisa e itens indexados parcialmente. No entanto, quando os resultados da pesquisa mesmo são exportados, o item é incluído apenas com o conjunto de resultados de pesquisa; ele não tiver incluído como um item parcialmente indexado.
    
- Se você especificar um intervalo de datas para uma consulta de pesquisa (incluindo a ele na consulta de palavra-chave) ou usando uma condição, qualquer item parcialmente indexado que não coincidem com o intervalo de datas não está incluído na contagem de itens indexados parcialmente. Apenas os itens indexados parcialmente que ficam dentro do intervalo de datas são incluídos na contagem de itens indexados parcialmente.
    
 **Observação:** Parcialmente indexada itens localizados no SharePoint e OneDrive sites *não estão* incluídos na estimativa de itens indexados parcialmente que é exibida nas estatísticas detalhadas para a pesquisa. No entanto, os itens indexados parcialmente podem ser exportados quando você exportar os resultados de uma pesquisa de conteúdo. Por exemplo, se você somente sites de pesquisa em uma pesquisa de conteúdo, o número estimado parcialmente itens indexados será zero. 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a>Calcula a proporção entre itens indexados parcialmente na sua organização

Para entender a exposição da sua organização para itens indexados parcialmente, você pode executar uma pesquisa de todo o conteúdo em todas as caixas de correio (usando uma consulta de palavra-chave em branco). No exemplo a seguir abaixo, há 56,208 (4,830 MB) totalmente indexados 470 (316 MB) e itens indexados parcialmente itens.
  
![Exemplo de mostrando de estatísticas de pesquisa itens indexados parcialmente](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
Você pode determinar a porcentagem de itens indexados parcialmente usando os seguintes cálculos.
  
 **Para calcular a taxa de itens indexados parcialmente em sua organização:**

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
Usando os resultados da pesquisa do exemplo anterior,. 84% de todos os itens de caixas de correio parcialmente são indexados.
  
 **Para calcular o percentual do tamanho dos itens indexados parcialmente na sua organização:**

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

Portanto, no exemplo anterior, 6.54% do tamanho total dos itens de caixa de correio são de itens indexados parcialmente. Conforme anteriormente mencionado, a maioria das organizações do Office 365, os clientes têm menos de 1% do conteúdo por volume e menor que 12% do conteúdo pelo tamanho parcialmente é indexado.

## <a name="working-with-partially-indexed-items"></a>Trabalhando com parcialmente itens indexados

Em casos quando você precisa ser examinado parcialmente itens para validar que elas não contêm informações relevantes, você pode [Exportar um relatório de pesquisa de conteúdo](export-a-content-search-report.md) que contém informações sobre itens indexados parcialmente. Quando você exporta um relatório de pesquisa de conteúdo, certifique-se de escolher uma das opções de exportação inclui itens indexados parcialmente. 
  
![Escolha a opção de segunda ou terceira para exportar itens indexados parcialmente](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
Ao exportar os resultados de pesquisa de conteúdo ou um relatório de pesquisa de conteúdo usando uma destas opções, a exportação inclui um relatório denominado Items.csv não indexados. Este relatório inclui a maioria das mesmas informações que o arquivo ResultsLog.csv; No entanto, o arquivo não indexadas Items.csv também inclui dois campos relacionados a itens indexados parcialmente: **Marcas de erro** e **Propriedades de erro**. Esses campos contêm informações sobre o erro de indexação para cada item parcialmente indexado. Usando as informações nestes dois campos pode ajudá-lo a determinar se ou não o erro de indexação para um determinado afeta sua investigação. Em caso afirmativo, você pode realizar uma pesquisa de conteúdo direcionada e recuperar e exportar mensagens de email específica e documentos do SharePoint ou OneDrive para que você possa examiná-los para determinar se elas são relevantes para a investigação. Para obter instruções detalhadas, consulte [Prepare um arquivo CSV para uma pesquisa de conteúdo direcionado no Office 365](csv-file-for-an-id-list-content-search.md).
  
 **Observação:** O arquivo não indexadas Items.csv também contém campos denominados **Tipo de erro** e a **Mensagem de erro**. Esses são herdados campos que contêm informações semelhantes às informações dos campos de **Marcas de erro** e **Propriedades de erro** , mas com informações menos detalhadas. Você pode ignorar esses campos herdados com segurança. 
  
## <a name="errors-related-to-partially-indexed-items"></a>Erros relacionados a itens indexados parcialmente

Marcas de erro são compostas de duas partes de informações, o erro e o tipo de arquivo. Por exemplo, em par este erro/filetype:

```
 parseroutputsize_xls
```

   
 `parseroutputsize`é o erro e `xls` é o tipo de arquivo do arquivo ocorreu o erro. Em casos foram o tipo de arquivo não foi reconhecido ou o tipo de arquivo foi não se aplica ao erro, você verá o valor `noformat` no lugar do tipo de arquivo. 
  
A seguir está uma lista de erros e uma descrição da causa do erro de indexação.
  
|**Marca de erro**|**Descrição**|
|:-----|:-----|
| `attachmentcount` <br/> |Uma mensagem de email tiveram muitos anexos e alguns desses anexos não foram processados.  <br/> |
| `attachmentdepth` <br/> |O analisador de recuperador e documento conteúdo encontrado muitos níveis de anexos aninhados dentro de outros anexos. Alguns desses anexos não foram processadas.  <br/> |
| `attachmentrms` <br/> |Um anexo falha decodificação porque foi protegido por RMS.  <br/> |
| `attachmentsize` <br/> |Um arquivo anexado a uma mensagem de email era muito grande e não pôde ser processado.  <br/> |
| `indexingtruncated` <br/> |Ao gravar a mensagem de email processado o índice, uma das propriedades indexáveis era muito grande e foi truncada. As propriedades truncadas estão listadas no campo de propriedades de erro.  <br/> |
| `invalidunicode` <br/> |Uma mensagem de email contidos texto que não puderam ser processado como Unicode válido. A indexação deste item pode estar incompleta.  <br/> |
| `parserencrypted` <br/> |O conteúdo de anexo ou mensagem de email é criptografado e Office 365 não pôde decodificar o conteúdo.  <br/> |
| `parsererror` <br/> |Ocorreu um erro desconhecido durante a análise. Normalmente, isso é resultado de um bug de software ou uma falha no serviço.  <br/> |
| `parserinputsize` <br/> |Um anexo era muito grande para o analisador para manipular e a análise de que o anexo não acontece ou não foi concluída.  <br/> |
| `parsermalformed` <br/> |Um anexo foi mal formado e não pôde ser manipulado pelo analisador. Esse resultado do arquivo antigo de can formatos, arquivos criados por um software incompatível ou vírus tentando se algo diferente de solicitadas.  <br/> |
| `parseroutputsize` <br/> |A saída devido a uma análise de um anexo era muito grande e foram truncados.  <br/> |
| `parserunknowntype` <br/> |Um anexo tinha um tipo de arquivo que não puderam ser detectados pelo Office 365.  <br/> |
| `parserunsupportedtype` <br/> |Um anexo tinha um tipo de arquivo Office 365could detectar, mas análise desse tipo de arquivo não é suportado.  <br/> |
| `propertytoobig` <br/> |O valor de uma propriedade de email no Exchange repositório era muito grande para ser recuperado e a mensagem não pôde ser processada. Isso geralmente ocorre apenas à propriedade corpo de uma mensagem de email.  <br/> |
| `retrieverrms` <br/> |O conteúdo recuperador falha decodificar uma mensagem protegida por RMS.  <br/> |
| `wordbreakertruncated` <br/> |Muitas palavras foram identificadas no documento durante a indexação. Processamento da propriedade interrompido quando está atingindo o limite e a propriedade será truncada.  <br/> |
   
Campos de erro descrevem quais campos são afetados pelo erro processamento listado no campo marcas de erro. Se estiver pesquisando como uma propriedade `subject` ou `participants`, erros no corpo da mensagem não afetam os resultados da pesquisa. Isso pode ser útil ao determinar exatamente quais itens indexados parcialmente talvez seja necessário investigar.
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a>Usando um script do PowerShell para determinar a exposição da sua organização para itens de email parcialmente indexados

As etapas a seguir mostram como executar um script do PowerShell que procura todos os itens em todas as caixas de correio do Exchange e, em seguida, gera um relatório sobre proporção da sua organização itens de email parcialmente indexados (pela contagem e pelo tamanho) e exibe o número de itens (e o tipo de arquivo) para cada erro de indexação que ocorre. Use as descrições de marca de erro, na seção anterior, para identificar o erro de indexação.
  
1. Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `PartiallyIndexedItems.ps1`.

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
   
2. [Conectar-se à segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://go.microsoft.com/fwlink/p/?linkid=627084).
    
3. Em segurança &amp; PowerShell do Centro de conformidade, vá para a pasta onde você salvou o script na etapa 1 e, em seguida, execute o script; Por exemplo:

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
Aqui está um exemplo fo a saída retornada pelo script.
  
![Exemplo de saída do script que gera um relatório sobre exposição da sua organização parcialmente indexados itens de email](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
Observe o seguinte:
  
1. O número total e o tamanho dos itens de email e a proporção da sua organização parcialmente indexados itens de email (por contagem e pelo tamanho)
    
2. As marcas de erro de lista e os tipos de arquivo correspondentes para os quais o erro ocorreu.
  
## <a name="see-also"></a>Confira também

[Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365](partially-indexed-items-in-content-search.md)
