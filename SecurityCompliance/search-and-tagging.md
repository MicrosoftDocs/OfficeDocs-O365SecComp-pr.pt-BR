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
# <a name="search-and-tagging"></a><span data-ttu-id="4c2a8-104">Pesquisa e marcação</span><span class="sxs-lookup"><span data-stu-id="4c2a8-104">Search and Tagging</span></span>

<span data-ttu-id="4c2a8-p102">No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta.</span></span>

> [!NOTE]
> <span data-ttu-id="4c2a8-p103">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="4c2a8-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="4c2a8-109">Pesquisar os documentos no seu caso</span><span class="sxs-lookup"><span data-stu-id="4c2a8-109">Search the documents in your case</span></span>

<span data-ttu-id="4c2a8-p104">Depois que tiver processado documentos no eDiscovery avançado e, opcionalmente, executar o módulo de analisar ou o módulo de relevância, você pode usar a pesquisa e marcação para pesquisar os documentos no caso e organizá-los usando marcas específicas ao caso. Você pode definir suas consultas usando as placas de condição fornecida ou por meio de uma linguagem de consulta KQL semelhantes nas palavras-chave condição cartão. Sintaxe KQL comum, como AND, OR, NOT e NEAR(n) são compatível, bem como à direita múltiplos caractere caractere curinga (\*). Essas propriedades são suportadas no nome da propriedade de linguagem de consulta:</span><span class="sxs-lookup"><span data-stu-id="4c2a8-p104">Once you have processed documents in Advanced eDiscovery and optionally run the Analyze module or the Relevance module, you can use Search and Tagging to search through the documents in the case and organize them using case-specific tags. You can define your queries using the provided condition cards, or through a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*). These properties are supported in the query language property name:</span></span>

- <span data-ttu-id="4c2a8-114">caselabel: marcas criado/aplicadas na pesquisa e a marcação para este caso</span><span class="sxs-lookup"><span data-stu-id="4c2a8-114">caselabel: tags created/applied in Search and Tagging for this case</span></span> 
- <span data-ttu-id="4c2a8-115">responsáveis: responsáveis atribuídos no caso - sujeitos a limitações</span><span class="sxs-lookup"><span data-stu-id="4c2a8-115">custodians: custodians assigned in the case - subject to limitations</span></span>
- <span data-ttu-id="4c2a8-116">Data: enviada data para email, modificado data para documentos</span><span class="sxs-lookup"><span data-stu-id="4c2a8-116">date: sent date for email, modified date for documents</span></span>
- <span data-ttu-id="4c2a8-117">FileID: ID do arquivo dentro do gabinete</span><span class="sxs-lookup"><span data-stu-id="4c2a8-117">fileid: file ID within the case</span></span>
- <span data-ttu-id="4c2a8-118">FileType: extensão de arquivo nativo</span><span class="sxs-lookup"><span data-stu-id="4c2a8-118">filetype: native file extension</span></span>
- <span data-ttu-id="4c2a8-119">fileclass: email, documento ou anexo</span><span class="sxs-lookup"><span data-stu-id="4c2a8-119">fileclass: email, document, or attachment</span></span>
- <span data-ttu-id="4c2a8-120">senderauthor: remetente para e-mails, autor de documentos</span><span class="sxs-lookup"><span data-stu-id="4c2a8-120">senderauthor: sender for emails, author for documents</span></span>
- <span data-ttu-id="4c2a8-121">Tamanho: tamanho do arquivo no KB</span><span class="sxs-lookup"><span data-stu-id="4c2a8-121">size: size of the file in KB</span></span>
- <span data-ttu-id="4c2a8-122">subjecttitle: assunto para e-mails, título de documentos</span><span class="sxs-lookup"><span data-stu-id="4c2a8-122">subjecttitle: subject for emails, title for documents</span></span>
- <span data-ttu-id="4c2a8-123">bcc</span><span class="sxs-lookup"><span data-stu-id="4c2a8-123">bcc</span></span>
- <span data-ttu-id="4c2a8-124">cc</span><span class="sxs-lookup"><span data-stu-id="4c2a8-124">cc</span></span>
- <span data-ttu-id="4c2a8-125">participantes: endereços de E-mail de todos os participantes em um segmento de email, incluindo para vínculos ausentes</span><span class="sxs-lookup"><span data-stu-id="4c2a8-125">participants: Email addresses of all participants in an email thread, including for missing links</span></span>
- <span data-ttu-id="4c2a8-126">recebidos: data de recebimento</span><span class="sxs-lookup"><span data-stu-id="4c2a8-126">received: received date</span></span>
- <span data-ttu-id="4c2a8-127">destinatários: endereços (para, cc, Cco) ou os nomes dos destinatários de email</span><span class="sxs-lookup"><span data-stu-id="4c2a8-127">recipients: email recipient names or addresses (to, cc, bcc)</span></span>
- <span data-ttu-id="4c2a8-128">remetente</span><span class="sxs-lookup"><span data-stu-id="4c2a8-128">sender</span></span>
- <span data-ttu-id="4c2a8-129">LastModifiedDate: data de um documento da última modificação</span><span class="sxs-lookup"><span data-stu-id="4c2a8-129">lastmodifieddate: last modified date of a document</span></span>
- <span data-ttu-id="4c2a8-130">enviados: enviadas a data de um email</span><span class="sxs-lookup"><span data-stu-id="4c2a8-130">sent: sent date of an email</span></span>
- <span data-ttu-id="4c2a8-131">para</span><span class="sxs-lookup"><span data-stu-id="4c2a8-131">to</span></span>
- <span data-ttu-id="4c2a8-132">autor: autor de um email</span><span class="sxs-lookup"><span data-stu-id="4c2a8-132">author: author of an email</span></span>
- <span data-ttu-id="4c2a8-133">título: título de um documento</span><span class="sxs-lookup"><span data-stu-id="4c2a8-133">title: title of a document</span></span>
- <span data-ttu-id="4c2a8-134">dominanttheme: dominante tema de um item\*</span><span class="sxs-lookup"><span data-stu-id="4c2a8-134">dominanttheme: dominant theme of an item\*</span></span>
- <span data-ttu-id="4c2a8-135">themeslist: temas que estão associados um item\*</span><span class="sxs-lookup"><span data-stu-id="4c2a8-135">themeslist: themes that are associated with an item\*</span></span>
- <span data-ttu-id="4c2a8-136">readpercentile_ [issuenum]: Leia percentil de um item para o problema [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="4c2a8-136">readpercentile_[issuenum]: read percentile of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="4c2a8-137">relevancescore_ [issuenum]: a pontuação de relevância de um item para o problema [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="4c2a8-137">relevancescore_[issuenum]: relevance score of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="4c2a8-138">relevancetag_ [issuenum]: se um item foi marcado manualmente para a relevância, sua tag para [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="4c2a8-138">relevancetag_[issuenum]: if an item has been manually tagged for relevance, its tag for [issuenum]\*\*</span></span>

<span data-ttu-id="4c2a8-139">\*Disponível somente se o módulo de temas tiver sido executado \* \* só estará disponível se o módulo de relevância tenha sido executado.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-139">\* Only available if the Themes module has been run \*\* Only available if the Relevance module has been run</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c2a8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c2a8-140">See also</span></span>

[<span data-ttu-id="4c2a8-141">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="4c2a8-141">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-142">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="4c2a8-142">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-143">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="4c2a8-143">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-144">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="4c2a8-144">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-145">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="4c2a8-145">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-146">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="4c2a8-146">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4c2a8-147">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="4c2a8-147">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

