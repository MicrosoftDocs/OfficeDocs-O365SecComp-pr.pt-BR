---
title: Use a pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Use a ferramenta de descoberta eletrônica de pesquisa de conteúdo para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para procurar todos os itens importados ou criar uma consulta para pesquisar por tipos de dados específicos de terceiros. Este artigo lista os valores que você pode usar em uma consulta de palavra-chave para pesquisar os tipos de dados de terceiros que podem ser importados para o Office 365.
ms.openlocfilehash: 6829e894ba687fb09184c32201f76394e37bbbf8
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037964"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="568c1-105">Use a pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365</span><span class="sxs-lookup"><span data-stu-id="568c1-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="568c1-p102">Você pode usar a [ferramenta de pesquisa de conteúdo de descoberta eletrônica](content-search.md) no Office 365 Security &amp; Centro de conformidade para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para pesquisar importados todos os itens de dados de terceiros ou você pode criar uma consulta para pesquisar somente itens de dados específicos de terceiros. Além disso, você também pode criar uma política de preservação baseado em consulta ou uma descoberta eletrônica baseado em consulta espera preservar dados de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="568c1-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="568c1-109">Para obter mais informações sobre a importação de dados de terceiros e uma lista dos tipos de dados de terceiros que podem ser importados para o Office 365, consulte [arquivamento dados de terceiros no Office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="568c1-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="568c1-110">Criando uma consulta para pesquisar todos os dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="568c1-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="568c1-p103">Para pesquisar (ou colocada em espera) qualquer tipo de dados de terceiros que você importou para o Office 365, é possível que você pode usar o `kind:externaldata` par de mensagens do valor da propriedade na caixa de palavra-chave para uma pesquisa de conteúdo ou ao criar uma isenção baseado em consulta. Por exemplo, para procurar itens que tenham sido importados de qualquer fonte de dados de terceiros e contêm a palavra "contoso" na propriedade assunto do item importado, você usaria a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="568c1-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="568c1-p104">O exemplo anterior de consulta de palavra-chave inclui a propriedade subject. Para obter uma lista das outras propriedades para itens de dados de terceiros que podem incluído em uma consulta de palavra-chave, consulte a seção "Mais informações" em [arquivamento de dados de terceiros no Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="568c1-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="568c1-p105">Ao criar consultas para pesquisar e manter os dados de terceiros, você também pode usar condições para restringir os resultados da pesquisa. Para obter mais informações sobre como criar consultas de pesquisa de conteúdo, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="568c1-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="568c1-117">Criando uma consulta para pesquisar tipos específicos de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="568c1-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="568c1-118">Em vez de pesquisar todos os tipos de dados de terceiros, você pode criar consultas de pesquisa somente para um tipo de dados de terceiros de especificar usando o seguinte par de valor de propriedade de mensagem na caixa de palavra-chave para uma pesquisa de conteúdo:</span><span class="sxs-lookup"><span data-stu-id="568c1-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="568c1-119">Por exemplo, para pesquisar somente dados de Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="568c1-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="568c1-p106">A tabela a seguir lista os tipos de dados de terceiros que você pode pesquisar e o valor a ser usado para o `itemclass:` propriedade especificamente pesquisar por esse tipo de dados de terceiros message. Observe que a sintaxe de consulta não diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="568c1-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="568c1-122">**Tipo de dados de terceiros**</span><span class="sxs-lookup"><span data-stu-id="568c1-122">**Third-party data type**</span></span>|<span data-ttu-id="568c1-123">**O valor para `itemclass:` propriedade**</span><span class="sxs-lookup"><span data-stu-id="568c1-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="568c1-124">OBJETIVO</span><span class="sxs-lookup"><span data-stu-id="568c1-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="568c1-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="568c1-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="568c1-126">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="568c1-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="568c1-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="568c1-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="568c1-128">Ares</span><span class="sxs-lookup"><span data-stu-id="568c1-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="568c1-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="568c1-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="568c1-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="568c1-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="568c1-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="568c1-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="568c1-132">Espaço reservado do AXs</span><span class="sxs-lookup"><span data-stu-id="568c1-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="568c1-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="568c1-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="568c1-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="568c1-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="568c1-135">Bearshare</span><span class="sxs-lookup"><span data-stu-id="568c1-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="568c1-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="568c1-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="568c1-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="568c1-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="568c1-138">Logs de chamada do blackBerry</span><span class="sxs-lookup"><span data-stu-id="568c1-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="568c1-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="568c1-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="568c1-140">BlackBerry PIN</span><span class="sxs-lookup"><span data-stu-id="568c1-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="568c1-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="568c1-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="568c1-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="568c1-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="568c1-143">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="568c1-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="568c1-144">Mensagens Bloomberg</span><span class="sxs-lookup"><span data-stu-id="568c1-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="568c1-145">Box
</span><span class="sxs-lookup"><span data-stu-id="568c1-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="568c1-146">Cisco IM &amp; servidor de presença</span><span class="sxs-lookup"><span data-stu-id="568c1-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="568c1-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="568c1-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="568c1-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="568c1-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="568c1-149">Conexão Direta</span><span class="sxs-lookup"><span data-stu-id="568c1-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="568c1-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="568c1-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="568c1-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="568c1-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="568c1-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="568c1-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="568c1-153">Flickr
</span><span class="sxs-lookup"><span data-stu-id="568c1-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="568c1-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="568c1-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="568c1-155">Google+
</span><span class="sxs-lookup"><span data-stu-id="568c1-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="568c1-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="568c1-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="568c1-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="568c1-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="568c1-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="568c1-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="568c1-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="568c1-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="568c1-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="568c1-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="568c1-161">Conexões da IBM</span><span class="sxs-lookup"><span data-stu-id="568c1-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="568c1-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="568c1-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="568c1-163">Bate-papo do ICE</span><span class="sxs-lookup"><span data-stu-id="568c1-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="568c1-164">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="568c1-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="568c1-165">Instagram
</span><span class="sxs-lookup"><span data-stu-id="568c1-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="568c1-166">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="568c1-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="568c1-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="568c1-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="568c1-168">IRC</span><span class="sxs-lookup"><span data-stu-id="568c1-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="568c1-169">Jive
</span><span class="sxs-lookup"><span data-stu-id="568c1-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="568c1-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="568c1-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="568c1-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="568c1-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="568c1-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="568c1-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="568c1-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="568c1-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="568c1-174">Comunicação unificada da Microsoft</span><span class="sxs-lookup"><span data-stu-id="568c1-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="568c1-175">Alinhar mente</span><span class="sxs-lookup"><span data-stu-id="568c1-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="568c1-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="568c1-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="568c1-177">MSN</span><span class="sxs-lookup"><span data-stu-id="568c1-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="568c1-178">Meu espaço</span><span class="sxs-lookup"><span data-stu-id="568c1-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="568c1-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="568c1-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="568c1-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="568c1-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="568c1-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="568c1-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="568c1-182">Tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="568c1-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="568c1-183">QQ</span><span class="sxs-lookup"><span data-stu-id="568c1-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="568c1-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="568c1-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="568c1-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="568c1-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="568c1-186">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="568c1-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="568c1-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="568c1-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="568c1-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="568c1-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="568c1-189">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="568c1-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="568c1-190">Symphony
</span><span class="sxs-lookup"><span data-stu-id="568c1-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="568c1-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="568c1-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="568c1-192">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="568c1-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="568c1-193">Tor</span><span class="sxs-lookup"><span data-stu-id="568c1-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="568c1-194">TTT</span><span class="sxs-lookup"><span data-stu-id="568c1-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="568c1-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="568c1-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="568c1-196">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="568c1-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="568c1-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="568c1-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="568c1-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="568c1-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="568c1-199">Winny</span><span class="sxs-lookup"><span data-stu-id="568c1-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="568c1-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="568c1-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="568c1-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="568c1-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="568c1-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="568c1-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="568c1-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="568c1-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
