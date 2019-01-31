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
# <a name="search-and-tagging"></a><span data-ttu-id="a6fab-104">Pesquisa e marcação</span><span class="sxs-lookup"><span data-stu-id="a6fab-104">Search and Tagging</span></span>

<span data-ttu-id="a6fab-p102">No eDiscovery avançado, o módulo de pesquisa e marcação permite pesquisar, visualizar e organizar documentos no seu caso. Atualmente, este módulo está na versão beta. Para uma demonstração em breve de pesquisa e a marcação, consulte o vídeo de [gerenciar seus dados com o eDiscovery avançado](https://www.youtube.com/watch?v=VaPYL3DHP6I) .</span><span class="sxs-lookup"><span data-stu-id="a6fab-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="a6fab-p103">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a6fab-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="a6fab-110">Pesquisar os documentos no seu caso</span><span class="sxs-lookup"><span data-stu-id="a6fab-110">Search the documents in your case</span></span>

<span data-ttu-id="a6fab-p104">Depois de ter processado documentos em um caso de eDiscovery avançado (e, opcionalmente, execute o módulo analisar ou relevância), você pode usar a pesquisa e a marcação para pesquisar documentos e, em seguida, organizá-los aplicando marcas caso específico (também chamadas de rótulos). Você pode definir uma consulta de pesquisa usando as placas de condição fornecida ou por meio de uma linguagem de consulta KQL semelhantes nas palavras-chave condição cartão. Sintaxe KQL comum, como AND, OR, NOT e NEAR(n) são compatível, bem como à direita múltiplos caractere caractere curinga (\*).</span><span class="sxs-lookup"><span data-stu-id="a6fab-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="a6fab-p105">A tabela a seguir lista as propriedades que você pode pesquisar usando uma consulta de palavra-chave KQL. Como alternativa, você pode usar um cartão de condição para na ferramenta de pesquisa do eDiscovery avançada para adicionar uma condição (para propriedades selecionadas) para uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a6fab-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="a6fab-116">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="a6fab-116">**Property**</span></span>|<span data-ttu-id="a6fab-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a6fab-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6fab-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="a6fab-118">**caselabel**</span></span> <br/> | <span data-ttu-id="a6fab-119">O nome da marca criado/aplicada quando um documento marcado.</span><span class="sxs-lookup"><span data-stu-id="a6fab-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="a6fab-120">**dos responsáveis**</span><span class="sxs-lookup"><span data-stu-id="a6fab-120">**custodian**</span></span> <br/> | <span data-ttu-id="a6fab-121">Dos responsáveis associado a um documento. está sujeito às limitações.</span><span class="sxs-lookup"><span data-stu-id="a6fab-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="a6fab-122">**Data**</span><span class="sxs-lookup"><span data-stu-id="a6fab-122">**date**</span></span> <br/> | <span data-ttu-id="a6fab-123">Enviada data para email; a data de modificação de documentos do site.</span><span class="sxs-lookup"><span data-stu-id="a6fab-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="a6fab-124">**FileID**</span><span class="sxs-lookup"><span data-stu-id="a6fab-124">**fileid**</span></span> <br/> | <span data-ttu-id="a6fab-125">A identificação do arquivo dentro do caso.</span><span class="sxs-lookup"><span data-stu-id="a6fab-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="a6fab-126">**FileType**</span><span class="sxs-lookup"><span data-stu-id="a6fab-126">**filetype**</span></span> <br/> | <span data-ttu-id="a6fab-127">A extensão de arquivo nativo.</span><span class="sxs-lookup"><span data-stu-id="a6fab-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="a6fab-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="a6fab-128">**fileclass**</span></span> <br/> | <span data-ttu-id="a6fab-129">Email, documento ou anexo.</span><span class="sxs-lookup"><span data-stu-id="a6fab-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="a6fab-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="a6fab-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="a6fab-131">O remetente do email; o autor para documentos do site.</span><span class="sxs-lookup"><span data-stu-id="a6fab-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="a6fab-132">**tamanho**</span><span class="sxs-lookup"><span data-stu-id="a6fab-132">**size**</span></span> <br/> | <span data-ttu-id="a6fab-133">O tamanho do arquivo no KB.</span><span class="sxs-lookup"><span data-stu-id="a6fab-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="a6fab-134">**subjecttitle**</span><span class="sxs-lookup"><span data-stu-id="a6fab-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="a6fab-135">O assunto de email; o título de documentos do site.</span><span class="sxs-lookup"><span data-stu-id="a6fab-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="a6fab-136">**bcc**</span><span class="sxs-lookup"><span data-stu-id="a6fab-136">**bcc**</span></span> <br/> | <span data-ttu-id="a6fab-137">O campo Cco de um email.</span><span class="sxs-lookup"><span data-stu-id="a6fab-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="a6fab-138">**cc**</span><span class="sxs-lookup"><span data-stu-id="a6fab-138">**cc**</span></span> <br/> | <span data-ttu-id="a6fab-139">O campo Cc de um email.</span><span class="sxs-lookup"><span data-stu-id="a6fab-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="a6fab-140">**participantes**</span><span class="sxs-lookup"><span data-stu-id="a6fab-140">**participants**</span></span> <br/> | <span data-ttu-id="a6fab-141">O endereço de email de todos os participantes em um segmento de email, incluindo para vínculos ausentes.</span><span class="sxs-lookup"><span data-stu-id="a6fab-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="a6fab-142">**recebido**</span><span class="sxs-lookup"><span data-stu-id="a6fab-142">**received**</span></span> <br/> | <span data-ttu-id="a6fab-143">A data em que um email foi recebido.</span><span class="sxs-lookup"><span data-stu-id="a6fab-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="a6fab-144">**destinatários**</span><span class="sxs-lookup"><span data-stu-id="a6fab-144">**recipients**</span></span> <br/> | <span data-ttu-id="a6fab-145">Destinatários de um email, incluídos em para, Cc ou Cco, campos.</span><span class="sxs-lookup"><span data-stu-id="a6fab-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="a6fab-146">**remetente**</span><span class="sxs-lookup"><span data-stu-id="a6fab-146">**sender**</span></span> <br/> | <span data-ttu-id="a6fab-147">O remetente de um email.</span><span class="sxs-lookup"><span data-stu-id="a6fab-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="a6fab-148">**LastModifiedDate**</span><span class="sxs-lookup"><span data-stu-id="a6fab-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="a6fab-149">A última data de um documento do site da modificação.</span><span class="sxs-lookup"><span data-stu-id="a6fab-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="a6fab-150">**enviado**</span><span class="sxs-lookup"><span data-stu-id="a6fab-150">**sent**</span></span> <br/> | <span data-ttu-id="a6fab-151">A data enviada de um email.</span><span class="sxs-lookup"><span data-stu-id="a6fab-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="a6fab-152">**Para**</span><span class="sxs-lookup"><span data-stu-id="a6fab-152">**to**</span></span> <br/> | <span data-ttu-id="a6fab-153">O destinatário listado no campo para de um email.</span><span class="sxs-lookup"><span data-stu-id="a6fab-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="a6fab-154">**autor**</span><span class="sxs-lookup"><span data-stu-id="a6fab-154">**author**</span></span> <br/> | <span data-ttu-id="a6fab-155">O autor de um documento do site.</span><span class="sxs-lookup"><span data-stu-id="a6fab-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="a6fab-156">**título**</span><span class="sxs-lookup"><span data-stu-id="a6fab-156">**title**</span></span> <br/> | <span data-ttu-id="a6fab-157">O título de um documento do site.</span><span class="sxs-lookup"><span data-stu-id="a6fab-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="a6fab-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="a6fab-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="a6fab-159">O tema dominante de um item.</span><span class="sxs-lookup"><span data-stu-id="a6fab-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="a6fab-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="a6fab-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="a6fab-161">Temas que estão associados um item.</span><span class="sxs-lookup"><span data-stu-id="a6fab-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="a6fab-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="a6fab-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="a6fab-163">O percentil de leitura de um item, para o problema definido pela [issuenum].</span><span class="sxs-lookup"><span data-stu-id="a6fab-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="a6fab-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="a6fab-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="a6fab-165">A pontuação de relevância de um item, para o problema definido pela [issuenum].</span><span class="sxs-lookup"><span data-stu-id="a6fab-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="a6fab-166">**relevancetag_ [tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="a6fab-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="a6fab-167">Se um item tiver sido marcados manualmente para a relevância, a marca definida pela [tagname].</span><span class="sxs-lookup"><span data-stu-id="a6fab-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="a6fab-168">\*Disponível somente se o módulo de temas tiver sido executado.</span><span class="sxs-lookup"><span data-stu-id="a6fab-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="a6fab-169">\*\*Disponível somente se o módulo de relevância tiver sido executado.</span><span class="sxs-lookup"><span data-stu-id="a6fab-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="a6fab-p106">Como alternativa, você pode usar um cartão de condição na ferramenta de pesquisa do eDiscovery avançada para adicionar uma condição (para propriedades selecionadas) para uma consulta de pesquisa. A captura de tela a seguir mostra as condições que podem ser adicionadas a uma consulta. A coluna **grupo** indica se a propriedade se aplica a email, documentos de site ou ambos (indicado pelo valor *comum*). Essa coluna também identifica as propriedades pesquisáveis que estão disponíveis depois de executar o módulo de relevância.</span><span class="sxs-lookup"><span data-stu-id="a6fab-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Condições de pesquisa na ferramenta de pesquisa de descoberta eletrônica avançada](media/AeDSearchConditions.png)

<span data-ttu-id="a6fab-175">Para obter mais informações sobre propriedades pesquisáveis, consulte [consultas de palavra-chave e condições de pesquisa](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="a6fab-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6fab-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6fab-176">See also</span></span>

[<span data-ttu-id="a6fab-177">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="a6fab-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-178">Noções básicas sobre avaliação na relevância</span><span class="sxs-lookup"><span data-stu-id="a6fab-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-179">Avaliação e marcação</span><span class="sxs-lookup"><span data-stu-id="a6fab-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-180">Marcação e treinamento de relevância</span><span class="sxs-lookup"><span data-stu-id="a6fab-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-181">Análise de relevância de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="a6fab-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-182">Decidindo com base nos resultados</span><span class="sxs-lookup"><span data-stu-id="a6fab-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a6fab-183">Análise de relevância de teste</span><span class="sxs-lookup"><span data-stu-id="a6fab-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

