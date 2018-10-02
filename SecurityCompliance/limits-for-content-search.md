---
title: Limites para a pesquisa de conteúdo de segurança do Office 365 &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/30/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: 'Saiba mais sobre os limites em vigor para o recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, como o número máximo de pesquisas simultâneas. '
ms.openlocfilehash: 917351f380c81ebfabfd4b3ff05a534c65c8f318
ms.sourcegitcommit: b6473cd6ba3f9ac79dc6a2040fc148020dfbe464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2018
ms.locfileid: "25358370"
---
# <a name="limits-for-content-search-in-the-office-365-security-amp-compliance-center"></a>Limites para a pesquisa de conteúdo de segurança do Office 365 &amp; Centro de conformidade

> [!NOTE]
> Os limites neste tópico são diferentes dos limites atuais para In-Place eDiscovery no Exchange Online e para o Centro de descoberta eletrônica no SharePoint Online. 
  
Vários limites são aplicados ao recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade. Este pesquisas de incluir executadas na página de **pesquisa de conteúdo** e pesquisas que estão associadas um caso de eDiscovery. Esses limites ajudam a manter a integridade e a qualidade dos serviços fornecidos para organizações do Office 365. Também há limites relacionados para a indexação de mensagens de email no Exchange Online para pesquisa. Você não pode modificar o conteúdo de pesquisa ou indexação limites de email, mas você deve estar ciente deles para que você possa tirar esses limites em consideração ao planejamento, execução e pesquisas de conteúdo de solução de problemas. 
  
 **Sumário**
  
[Limites de pesquisa de conteúdo](limits-for-content-search.md#searchlimits)
  
[Limites de indexação para mensagens de email](limits-for-content-search.md#indexinglimits)
  
[Mais informações](limits-for-content-search.md#moreinfo)
  
## <a name="content-search-limits"></a>Limites de pesquisa de conteúdo
<a name="searchlimits"> </a>

A tabela a seguir lista os limites de pesquisa na segurança &amp; Centro de conformidade.
  
|**Descrição de limite**|**Limite**|
|:-----|:-----|
|O número máximo de caixas de correio ou sites que podem ser pesquisadas em uma única pesquisa de conteúdo  <br/> |Sem limites  <br/> |
|O número máximo de pesquisas de conteúdo que podem ser executados ao mesmo tempo em sua organização.  <br/> |Sem limites  <br/> |
|O número máximo de pesquisas de conteúdo que pode ser iniciada por um único usuário ao mesmo tempo. Observe que esse limite mais provável é atingido quando o usuário tentar iniciar várias pesquisas usando o **Get-ComplianceSearch \| Start-ComplianceSearch** command no PowerShell do Centro de conformidade & segurança.<br/> |10   <br/> |
|O número máximo de itens por caixa de correio de usuário que são exibidos na página visualização ao visualizar resultados de pesquisa de conteúdo.  <br/> |100  <br/> |
|O número máximo de itens encontrados em todas as caixas de correio do usuário que são exibidas na página visualização ao visualizar resultados de pesquisa de conteúdo. Os itens mais recentes são exibidos.  <br/> |1.000  <br/> |
|O número máximo de caixas de correio de usuário que pode ser visualizado para resultados de pesquisa. Se houver mais de 1000 caixas de correio que contém conteúdo que corresponde à consulta de pesquisa, somente as principais 1000 caixas de correio com a maioria dos resultados de pesquisa será disponíveis para visualização.  <br/> |1.000  <br/> |
|O número máximo de itens encontrados no SharePoint e OneDrive para sites corporativos que são exibidos na página visualização ao visualizar resultados de pesquisa de conteúdo. Os itens mais recentes são exibidos.  <br/> |200  <br/> |
|O número máximo de sites (no SharePoint e o OneDrive for Business) que pode ser visualizado para resultados de pesquisa. Se houver mais de 200 sites total que contém conteúdo que corresponde à consulta de pesquisa, somente os principais 200 sites com a maioria dos resultados de pesquisa será disponíveis para visualização.  <br/> |200  <br/> |
|O número máximo de itens por caixa de correio de pasta pública que são exibidos na página visualização ao visualizar resultados de pesquisa de conteúdo.  <br/> |100  <br/> |
|O número máximo de itens encontrados em todas as caixas de correio de pasta pública que são exibidas na página visualização ao visualizar resultados de pesquisa de conteúdo.  <br/> |200  <br/> |
|O número máximo de caixas de correio públicas que pode ser visualizado para resultados de pesquisa. Se houver mais de 500 caixas de correio de pasta pública que contém conteúdo que corresponde à consulta de pesquisa, somente as principais 500 pasta pública caixas de correio com a maioria dos resultados de pesquisa será disponíveis para visualização.  <br/> |500  <br/> |
|O número máximo de caracteres para consulta de pesquisa (incluindo operadores e condições) para uma pesquisa de conteúdo.  <br/><br/> **Observação:** Esse limite entrará em vigor depois que a consulta é expandida, o que significa que a consulta irá obter expandida em relação a cada uma das palavras-chave. Por exemplo, se uma consulta de pesquisa tiver 15 palavras-chave e parâmetros adicionais e condições, a consulta obtém expandida 15 vezes, cada um com os outros parâmetros e condições da consulta. Portanto, mesmo que o número de caracteres da consulta de pesquisa pode ser abaixo do limite, é a consulta expandida que pode contribuir para exceder esse limite.<br/> |**Caixas de correio:** 10.000  <br/> **Sites:** 4.000 ao pesquisar todos os sites ou 2.000 durante a pesquisa de sites até 20 <sup>1</sup> <br/> |
|Número máximo de variants retornados ao usar um curinga no prefixo para procurar uma frase exata em uma consulta de pesquisa ou ao usar um curinga prefixo e o operador booleano **NEAR** ou **ONEAR** .  <br/> |10.000 <sup>2</sup> <br/> |
|O número mínimo de caracteres alfa para curingas de prefixo; Por exemplo, `time*`, `one*`, ou `set*`.  <br/> |3   <br/> |
|O número máximo de caixas de correio em uma pesquisa de conteúdo que você pode excluir itens fazendo uma ação "Pesquisar e limpar" (usando o **New-ComplianceSearchAction-limpar** comando). Se a pesquisa de conteúdo que você estiver fazendo uma ação de limpeza para tem mais caixas de correio de origem que esse limite, a ação de limpeza falhará. Para obter mais informações sobre a pesquisa e limpar, consulte [Procurar e excluir mensagens de email em sua organização do Office 365](search-for-and-delete-messages-in-your-organization.md).<br/> |50.000  <br/> |
   
> [!NOTE]
> <sup>1</sup> durante a pesquisa do SharePoint e OneDrive para locais de negócios, os caracteres nas URLs dos sites que estão sendo pesquisados são contados contra esse limite.<br/> <sup>2</sup> para consultas de não-frase (um valor de palavra-chave que não usa aspas duplas) usamos um índice de prefixo especiais. Esse procedimento informa que uma palavra ocorre em um documento, mas não onde ele ocorre no documento. Para fazer uma consulta de frase (um valor de palavra-chave com sinais de aspas duplas), precisamos comparar a posição dentro do documento para as palavras na frase. Isso significa que não podemos usar o índice de prefixo para consultas de frase. Nesse caso, a consulta com todas as palavras que o prefixo expande; que expandimos internamente Por exemplo, `"time*"` podem expandir a `"time OR timer OR times OR timex OR timeboxed OR …"`. 10.000 é o número máximo de variants que a palavra pode expandir a, não o número de documentos que correspondem a consulta. Não há nenhum limite superior para os termos de não-frase. 
  
[Return to top](limits-for-content-search.md#top)
  
## <a name="indexing-limits-for-email-messages"></a>Limites de indexação para mensagens de email
<a name="indexinglimits"> </a>

A tabela a seguir descreve os limites de indexação que possam resultar em uma mensagem de email que está sendo retornada como um item não indexado ou um item parcialmente indexado nos resultados de uma pesquisa de conteúdo.
  
|**Limite de indexação**|**Observações**|**Descrição**|
|:-----|:-----|:-----|
|Tamanho máximo de anexo (excluindo arquivos do Excel)  <br/> |150 MB  <br/> |O tamanho máximo de um anexo de email que analisa para indexação. Qualquer anexo que for maior do que esse limite não ser analisado para indexação e a mensagem com o anexo será marcada como parcialmente indexados.<br/> <br/>**Observação:** Analisar é o processo de onde o serviço de indexação extrai o texto do anexo, remove caracteres desnecessários como pontuação e espaços e divide o texto em palavras (em um processo de geração de tokens de chamada), que são armazenados no índice.           |
|Tamanho máximo de arquivos do Excel  <br/> |4 MB  <br/> |O tamanho máximo de um arquivo do Excel localizado em um site ou anexado a uma mensagem de email que será analisada para indexação. Qualquer arquivo do Excel que é maior do que esse limite não ser analisado e o arquivo ou o email que a mensagem com o anexo de arquivo será marcada como não indexados.  <br/> |
|Número máximo de anexos  <br/> |250  <br/> |O número máximo de arquivos anexados a uma mensagem de email que será analisada para indexação. Se uma mensagem tiver mais de 250 anexos, os primeiros 250 anexos são analisados e indexados, e a mensagem é marcada como parcialmente indexados porque ele tinha adicionais anexos que não foram analisados.  <br/> |
|Profundidade máxima de anexo  <br/> |30  <br/> |O número máximo de anexos aninhados, que são analisados. Por exemplo, se uma mensagem de email tem outra mensagem anexada a ele e a mensagem anexada tem um documento do Word anexado, o documento do Word e a mensagem anexada serão indexados. Esse comportamento continuará até 30 anexos aninhados.  <br/> |
|Número máximo de imagens anexados  <br/> |0  <br/> |Uma imagem que é anexada a uma mensagem de email é ignorada pelo analisador e não é indexada.  <br/> |
|Tempo máximo gasto um item de análise  <br/> |30 segundos  <br/> |Um máximo de 30 segundos é gasto na análise de um item para indexação. Se o tempo de análise excede 30 segundos, o item está marcado como parcialmente indexados.  <br/> |
|Saída do analisador de máximo  <br/> |2 milhões de caracteres  <br/> |A quantidade máxima de saída de texto do analisador da é indexada. Por exemplo, se o analisador extraído 8 milhões de caracteres de um documento, apenas os primeiro 2 milhões de caracteres são indexados.  <br/> |
|Tokens de anotação máximo  <br/> |2 milhões  <br/> |Quando uma mensagem de email é indexada, cada palavra é anotada com instruções de processamento de diferentes que especificam como o que o word deve ser indexado. Cada conjunto de instruções de processamento é chamado um token de anotação. Para manter a qualidade do serviço no Office 365, há um limite de tokens de anotação 2 milhões para uma mensagem de email.  <br/> |
|Tamanho máximo do corpo no índice  <br/> |67 milhões de caracteres  <br/> |O número total de caracteres no corpo de uma mensagem de email e todos os seus respectivos anexos. Quando uma mensagem de email é indexada, todo o texto no corpo da mensagem e em todos os anexos é concatenado em uma única cadeia de caracteres. O tamanho máximo dessa cadeia de caracteres que é indexada é 67 milhões de caracteres.  <br/> |
|Máximo tokens exclusivos no corpo  <br/> |1 milhão  <br/> |Explicado como previamente, tokens são o resultado de extrair texto de conteúdo, removendo a pontuação e espaços e, em seguida, dividindo-la em palavras (chamadas de tokens) que são armazenadas no índice. Por exemplo, a frase `"cat, mouse, bird, dog, dog"` contém 5 tokens. Mas apenas 4 dessas tokens exclusivos. Não há um limite de 1 milhão de tokens exclusivo por mensagem de email, o que ajuda a impedir que o índice obtendo muito grande com tokens aleatórios.<br/> |
   
[Voltar ao início](limits-for-content-search.md#top)
  
## <a name="more-information"></a>Mais informações
<a name="moreinfo"> </a>

Há aspectos de limites adicionais relacionadas a diferentes da pesquisa de conteúdo, como exportar os resultados da pesquisa e indexação de conteúdo. Para obter uma descrição desses limites, consulte os tópicos a seguir:
  
- 
    
- [Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365](partially-indexed-items-in-content-search.md)
    
- [Investigar itens parcialmente indexados na Descoberta Eletrônica do Office 365](investigating-partially-indexed-items-in-ediscovery.md)
    
- [Limites de pesquisa do SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
Para obter informações sobre pesquisas de conteúdo, consulte:
  
- [Pesquisa de conteúdo no Office 365](content-search.md)
    
- [Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md)
    
[Return to top](limits-for-content-search.md#top)
  

