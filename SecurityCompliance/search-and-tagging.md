---
title: Pesquisa e marcação
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524135"
---
# <a name="search-and-tagging"></a>Pesquisa e marcação

No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta.

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Pesquisar os documentos no seu caso

Depois que tiver processado documentos no eDiscovery avançado e, opcionalmente, executar o módulo de analisar ou o módulo de relevância, você pode usar a pesquisa e marcação para pesquisar os documentos no caso e organizá-los usando marcas específicas ao caso. Você pode definir suas consultas usando as placas de condição fornecida ou por meio de uma linguagem de consulta KQL semelhantes nas palavras-chave condição cartão. Sintaxe KQL comum, como AND, OR, NOT e NEAR(n) são compatível, bem como à direita múltiplos caractere caractere curinga (*). Essas propriedades são suportadas no nome da propriedade de linguagem de consulta:

- caselabel: marcas criado/aplicadas na pesquisa e a marcação para este caso 
- responsáveis: responsáveis atribuídos no caso - sujeitos a limitações
- Data: enviada data para email, modificado data para documentos
- FileID: ID do arquivo dentro do gabinete
- FileType: extensão de arquivo nativo
- fileclass: email, documento ou anexo
- senderauthor: remetente para e-mails, autor de documentos
- Tamanho: tamanho do arquivo no KB
- subjecttitle: assunto para e-mails, título de documentos
- bcc
- cc
- participantes: endereços de E-mail de todos os participantes em um segmento de email, incluindo para vínculos ausentes
- recebidos: data de recebimento
- destinatários: endereços (para, cc, Cco) ou os nomes dos destinatários de email
- remetente
- LastModifiedDate: data de um documento da última modificação
- enviados: enviadas a data de um email
- para
- autor: autor de um email
- título: título de um documento
- dominanttheme: dominante tema de um item\*
- themeslist: temas que estão associados um item\*
- readpercentile_ [issuenum]: Leia percentil de um item para o problema [issuenum]\*\*
- relevancescore_ [issuenum]: a pontuação de relevância de um item para o problema [issuenum]\*\*
- relevancetag_ [issuenum]: se um item foi marcado manualmente para a relevância, sua tag para [issuenum]\*\*

\*Disponível somente se o módulo de temas tiver sido executado \* \* só estará disponível se o módulo de relevância tenha sido executado.
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre avaliação na relevância](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Avaliação e marcação](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marcação e treinamento de relevância](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Análise de relevância de acompanhamento](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Decidindo com base nos resultados](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Análise de relevância de teste](test-relevance-analysis-in-advanced-ediscovery.md)

