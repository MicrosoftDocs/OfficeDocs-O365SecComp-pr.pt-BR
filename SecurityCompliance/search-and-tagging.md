---
title: Pesquisa e marcação
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666141"
---
# <a name="search-and-tagging"></a>Pesquisa e marcação

No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta. Para uma demonstração em breve de pesquisa e a marcação, consulte o vídeo de [gerenciar seus dados com o eDiscovery avançado](https://www.youtube.com/watch?v=VaPYL3DHP6I) .

> [!NOTE]
> A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Pesquisar os documentos no seu caso

Depois de ter processado documentos em um caso de eDiscovery avançado (e, opcionalmente, execute o módulo analisar ou relevância), você pode usar a pesquisa e a marcação para pesquisar documentos e, em seguida, organizá-los aplicando marcas caso específico (também chamadas de rótulos). Você pode definir uma consulta de pesquisa usando as placas de condição fornecida ou por meio de uma linguagem de consulta KQL semelhantes nas palavras-chave condição cartão. Sintaxe KQL comum, como AND, OR, NOT e NEAR(n) são compatível, bem como à direita múltiplos caractere caractere curinga (*). 

A tabela a seguir lista as propriedades que você pode pesquisar usando uma consulta de palavra-chave KQL. Como alternativa, você pode usar um cartão de condição para na ferramenta de pesquisa do eDiscovery avançada para adicionar uma condição (para propriedades selecionadas) para uma consulta de pesquisa.

|**Propriedade**|**Descrição**|
|:-----|:-----|
|**caselabel** <br/> | O nome da marca criado/aplicada quando um documento marcado. <br/> |
|**dos responsáveis** <br/> | Dos responsáveis associado a um documento. está sujeito às limitações. <br/> |
|**Data** <br/> | Enviada data para email; a data de modificação de documentos do site. <br/> |
|**FileID** <br/> | A identificação do arquivo dentro do caso. <br/> |
|**FileType** <br/> | A extensão de arquivo nativo. <br/> |
|**fileclass** <br/> | Email, documento ou anexo. <br/> |
|**senderauthor** <br/> | O remetente do email; o autor para documentos do site. <br/> |
|**tamanho** <br/> | O tamanho do arquivo no KB. <br/> |
|**subjecttitle** <br/> | O assunto de email; o título de documentos do site. <br/> |
|**bcc** <br/> | O campo Cco de um email. <br/> |
|**cc** <br/> | O campo Cc de um email. <br/> |
|**participantes** <br/> | O endereço de email de todos os participantes em um segmento de email, incluindo para vínculos ausentes. <br/> |
|**recebido** <br/> | A data em que um email foi recebido. <br/> |
|**destinatários** <br/> | Destinatários de um email, incluídos em para, Cc ou Cco, campos. <br/> |
|**remetente** <br/> | O remetente de um email. <br/> |
|**LastModifiedDate** <br/> | A última data de um documento do site da modificação. <br/> |
|**enviado** <br/> | A data enviada de um email. <br/> |
|**Para** <br/> | O destinatário listado no campo para de um email. <br/> |
|**autor** <br/> | O autor de um documento do site. <br/> |
|**título** <br/> | O título de um documento do site. <br/> |
|**dominanttheme**\* <br/> | O tema dominante de um item. <br/> |
|**themeslist**\* <br/> | Temas que estão associados um item. <br/> |
|**readpercentile_ [issuenum]**\*\* <br/> | O percentil de leitura de um item, para o problema definido pela [issuenum]. <br/> |
|**relevancescore_ [issuenum]**\*\* <br/> | A pontuação de relevância de um item, para o problema definido pela [issuenum]. <br/> |
|**relevancetag_ [tagname]**\*\* <br/> | Se um item tiver sido marcados manualmente para a relevância, a marca definida pela [tagname]. <br/> |
|||

\*Disponível somente se o módulo de temas tiver sido executado.

\*\*Disponível somente se o módulo de relevância tiver sido executado.

Como alternativa, você pode usar um cartão de condição na ferramenta de pesquisa do eDiscovery avançada para adicionar uma condição (para propriedades selecionadas) para uma consulta de pesquisa. A captura de tela a seguir mostra as condições que podem ser adicionadas a uma consulta. A coluna **grupo** indica se a propriedade se aplica a email, documentos de site ou ambos (indicado pelo valor *comum*). Essa coluna também identifica as propriedades pesquisáveis que estão disponíveis depois de executar o módulo de relevância.

![Condições de pesquisa na ferramenta de pesquisa de descoberta eletrônica avançada](media/AeDSearchConditions.png)

Para obter mais informações sobre propriedades pesquisáveis, consulte [consultas de palavra-chave e condições de pesquisa](keyword-queries-and-search-conditions.md).
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

