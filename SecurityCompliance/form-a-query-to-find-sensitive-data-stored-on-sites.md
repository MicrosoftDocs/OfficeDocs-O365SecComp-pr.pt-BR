---
title: Criar uma consulta para encontrar dados confidenciais armazenados em sites
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: Com a prevenção de perda de dados (DLP) no SharePoint Online, você pode descobrir os documentos que contêm dados confidenciais em todo o seu locatário. Depois de descobrir os documentos, você pode trabalhar com os proprietários do documento para proteger os dados. Este tópico pode ajudá-lo a formar uma consulta para pesquisar dados confidenciais.
ms.openlocfilehash: 13954a856dd265e3b735d940c7d334d922713637
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013855"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>Criar uma consulta para encontrar dados confidenciais armazenados em sites

Os usuários costumam armazenam dados confidenciais, como números de cartão de crédito, números do seguro social, ou pessoal, em seus sites e ao longo do tempo isso pode expor a organização para um risco significativo de perda de dados. Documentos armazenados em sites — incluindo OneDrive para sites corporativos — poderão ser compartilhadas com pessoas fora da organização que não devem ter acesso às informações. Com a prevenção de perda de dados (DLP) no SharePoint Online, você pode descobrir os documentos que contêm dados confidenciais em todo o seu locatário. Depois de descobrir os documentos, você pode trabalhar com os proprietários do documento para proteger os dados. Este tópico pode ajudá-lo a formar uma consulta para pesquisar dados confidenciais.
  
> [!NOTE]
> Descoberta eletrônica, ou eDiscovery e DLP são recursos premium que exigem o [SharePoint Online plano 2](https://go.microsoft.com/fwlink/?LinkId=510080). 
  
## <a name="forming-a-basic-dlp-query"></a>Criando uma consulta básica de DLP

Existem três partes que compõem uma consulta básica de DLP: SensitiveType, contar o intervalo e o intervalo de confiança. Conforme ilustrado no gráfico a seguir, **SensitiveType: "\<tipo\>"** é necessário e ambas**|\<contar intervalo\> ** e**|\<o intervalo de confiança\> ** são opcionais. 
  
![Consulta de exemplo dividida em necessária e opcional](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>Tipo confidencial - necessário

O que é cada parte? Consultas de SharePoint DLP geralmente começam com a propriedade `SensitiveType:"` e um tipo de informação nome do [inventário de tipos de informações confidenciais](https://go.microsoft.com/fwlink/?LinkID=509999)e terminam com um `"`. Você também pode usar o nome de um [tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md) que você criou para sua organização. Por exemplo, você pode estar procurando por documentos que contenham números de cartão de crédito. Na instância, você usaria o seguinte formato: `SensitiveType:"Credit Card Number"`. Porque você não incluiu o intervalo de contagem ou intervalo de confiança, a consulta retorna todos os documentos em que um número de cartão de crédito é detectado. Esta é a consulta mais simples que podem ser executados, e retorna a maioria dos resultados. Tenha em mente que importa a ortografia e o espaçamento do tipo confidencial. 
  
### <a name="ranges---optional"></a>Intervalos - opcionais

Ambas as próximas duas partes são intervalos, vamos examinar rapidamente a aparência de um intervalo. Em consultas de SharePoint DLP, um intervalo básico é representado por dois números separados por dois pontos, que tem esta aparência: `[number]..[number]`. Por exemplo, se `10..20` é usado, aquele intervalo seria capturar números de 10 a 20. Há muitas combinações de intervalo diferente e várias são abordadas neste tópico. 
  
Vamos adicionar um intervalo de contagem à consulta. Você pode usar o intervalo de contagem para definir o número de ocorrências de um documento precisa conter antes que ele está incluído nos resultados da consulta de informações confidenciais. Por exemplo, se desejar que a sua consulta para retornar apenas os documentos que contenham exatamente cinco números de cartão de crédito, use isso: `SensitiveType:"Credit Card Number|5"`. Intervalo de contagem pode ajudá-lo a identificar documentos que impõem alto grau de risco. Por exemplo, sua organização pode considerar documentos com cinco ou mais números de cartão de crédito um alto risco. Para localizar documentos ajustando a esse critério, você usaria esta consulta: `SensitiveType:"Credit Card Number|5.."`. Como alternativa, você pode localizar documentos com cinco ou menos números de cartão de crédito usando esta consulta: `SensitiveType:"Credit Card Number|..5"`. 
  
#### <a name="confidence-range"></a>Intervalo de confiança

Finalmente, o intervalo de confiança é o nível de confiança que o tipo de confidencial detectado é realmente uma correspondência. Os valores para o intervalo de confiança funcionam da mesma forma, para contar o intervalo. É possível formar uma consulta sem incluir um intervalo de contagem. Por exemplo, para pesquisar documentos com qualquer número de cartão de crédito números — desde o intervalo de confiança é de 85 por cento ou superior — você usaria esta consulta: `SensitiveType:"Credit Card Number|*|85.."`. 
  
> [!IMPORTANT]
> O asterisco ( `*`) é um caractere curinga que significa works qualquer valor. Você pode usar o caractere curinga ( `*`) do intervalo de contagem ou do intervalo de confiança mas não em um tipo confidencial. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>Propriedades de pesquisa e operadores de consulta adicionais disponíveis no Centro de Descoberta Eletrônica

DLP no SharePoint também introduz o LastSensitiveContentScan propriedade, que pode ajudá-lo procurar arquivos verificados dentro de um período específico. Para obter exemplos de consulta com o `LastSensitiveContentScan` propriedade, consulte os [exemplos de consultas complexas](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) na próxima seção. 
  
Você pode usar não apenas propriedades específicas de DLP para criar uma consulta, mas também propriedades padrão de pesquisa de descoberta eletrônica do SharePoint como `Author` ou `FileExtension`. Você pode usar os operadores para construir consultas complexas. Para lista de operadores e propriedades disponíveis, consulte a postagem do blog do [usando propriedades de pesquisa e operadores com eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093) . 
  
## <a name="examples-of-complex-queries"></a>Exemplos

Os exemplos a seguir usam tipos diferentes de confidenciais, propriedades e operadores para ilustrar como você pode refinar suas consultas para localizar exatamente o que você está procurando.
  
|**Consulta**|**Explicação**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |O nome pode parecer estranho porque ele é tão grande, mas é o nome correto para aquele tipo confidencial. Certifique-se de usar nomes exatos do [inventário de tipos de informações confidenciais](https://go.microsoft.com/fwlink/?LinkID=509999). Você também pode usar o nome de um [tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md) que você criou para sua organização.<br/> |
| ' SensitiveType: "número de cartão de crédito|1..4294967295|1..100"' <br/> |Isso retornará documentos com pelo menos uma correspondência para o tipo de confidencial "Número de cartão de crédito." Os valores para cada intervalo são os respectivos valores mínimos e máximo. É uma maneira mais simples para gravar esta consulta `SensitiveType:"Credit Card Number"`, mas onde é a diversão nisso?<br/> |
| ' SensitiveType: "número de cartão de crédito| 5..25" e LastSensitiveContentScan:"8/11/2018..8/13/2018 "' <br/> |Isso retornará documentos com 5-25 números de cartão de crédito que foram verificados de 11 de agosto de 2018 por meio de 13 de agosto de 2018.  <br/> |
| ' SensitiveType: "número de cartão de crédito| 5..25" e LastSensitiveContentScan:"8/11/2018..8/13/2018 "não FileExtension:XLSX' <br/> |Isso retornará documentos com 5-25 números de cartão de crédito que foram verificados de 11 de agosto de 2018 por meio de 13 de agosto de 2018. Arquivos com uma extensão XLSX não são incluídos nos resultados da consulta.  `FileExtension` é uma das muitas propriedades que você pode incluir em uma consulta. Para obter mais informações, consulte [usando propriedades de pesquisa e operadores com eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093).<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |Isso retornará documentos que contenham um número de cartão de crédito ou um número de previdência social.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>Exemplos

Nem todas as consultas são criadas iguais. A tabela a seguir fornece exemplos de consultas que não funcionam com DLP no SharePoint e descreve o motivo.
  
|**Consulta incompatível**|**Motivo**|
|:-----|:-----|
| ' SensitiveType: "número de cartão de crédito|.." ` <br/> |Você deve adicionar pelo menos um serviço.  <br/> |
| `SensitiveType:"NotARule"` <br/> |"NotARule" não é um nome válido de tipo confidenciais. Somente os nomes do [inventário de tipos de informações confidenciais](https://go.microsoft.com/fwlink/?LinkID=509999) funcionam em consultas DLP.<br/> |
| ' SensitiveType: "número de cartão de crédito|0"' <br/> |Zero não é válido como o valor mínimo ou o valor máximo em um intervalo.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |É pode ser difícil ver, mas não há espaço em branco extra entre "Crédito" e "Placa", o que faz com que a consulta inválida. Use nomes de tipo confidenciais exato do [inventário de tipos de informações confidenciais](https://go.microsoft.com/fwlink/?LinkID=509999).<br/> |
| ' SensitiveType: "número de cartão de crédito|1.. 3"' <br/> |A parte de dois períodos não deve ser separada por um espaço.  <br/> |
| ' SensitiveType: "número de cartão de crédito| |1..|"80... ' <br/> |Há muitas (delimitadores de pipe|). Siga esse formato em vez disso: ' SensitiveType: "número de cartão de crédito|1..|"80... ' <br/> |
| ' SensitiveType: "número de cartão de crédito|1..|80..101"' <br/> |Como os valores de confiança representam uma porcentagem, eles não podem exceder 100. Em vez disso, escolha um número entre 1 e 100.  <br/> |
   
## <a name="for-more-information"></a>Para saber mais

[Localizar dados confidenciais armazenados em sites do SharePoint Online](https://support.office.com/article/ef788d8f-9748-4025-bfe4-40541ca4cfb2)
  
[Inventário de tipos de informações confidenciais](https://go.microsoft.com/fwlink/?LinkID=509999)
  
[Executar uma pesquisa de conteúdo com a segurança do Office 365 &amp; Centro de conformidade](run-a-content-search-in-the-security-and-compliance-center.md)
  
[Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md)
  

