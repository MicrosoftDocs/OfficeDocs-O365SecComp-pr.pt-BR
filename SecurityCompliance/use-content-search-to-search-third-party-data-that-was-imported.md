---
title: Usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Use a ferramenta de descoberta eletrônica de pesquisa de conteúdo para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Você pode criar uma consulta para pesquisar todos os itens importados ou criar uma consulta para Pesquisar tipos de dados específicos de terceiros. Este artigo lista os valores que podem ser usados em uma consulta de palavra-chave para pesquisar os tipos de dados de terceiros que podem ser importados para o Office 365.
ms.openlocfilehash: 361ead435d397464452c5b58ecf251a7322ced05
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999704"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="74bc7-105">Usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365</span><span class="sxs-lookup"><span data-stu-id="74bc7-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="74bc7-106">Você pode usar a [ferramenta de descoberta eletrônica de pesquisa de conteúdo](content-search.md) no centro de conformidade do _AMP_ de segurança para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="74bc7-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="74bc7-107">Você pode criar uma consulta para pesquisar todos os itens importados de dados de terceiros ou pode criar uma consulta para pesquisar apenas itens de dados de terceiros específicos.</span><span class="sxs-lookup"><span data-stu-id="74bc7-107">You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items.</span></span> <span data-ttu-id="74bc7-108">Além disso, você também pode criar uma política de preservação baseada em consulta ou uma descoberta eletrônica baseada em consulta para preservar dados de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="74bc7-108">Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="74bc7-109">Para obter mais informações sobre a importação de dados de terceiros e uma lista dos tipos de dados de terceiros que podem ser importados para o Office 365, consulte arquivamento de dados de terceiros [no office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="74bc7-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="74bc7-110">Criar uma consulta para pesquisar todos os dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="74bc7-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="74bc7-111">Para pesquisar (ou colocar em espera) qualquer tipo de dados de terceiros que você importou para o Office 365, é possível usar o `kind:externaldata` par propriedade-valor da mensagem na caixa palavra-chave para uma pesquisa de conteúdo ou ao criar uma retenção baseada em consulta.</span><span class="sxs-lookup"><span data-stu-id="74bc7-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="74bc7-112">Por exemplo, para pesquisar itens que foram importados de qualquer fonte de dados de terceiros e que contenham a palavra "contoso" na propriedade Subject do item importado, você usaria a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="74bc7-112">For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="74bc7-113">O exemplo de consulta de palavra-chave anterior inclui a propriedade Subject.</span><span class="sxs-lookup"><span data-stu-id="74bc7-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="74bc7-114">Para obter uma lista de outras propriedades dos itens de dados de terceiros que podem ser incluídos em uma consulta de palavra-chave, consulte a seção "mais informações" em arquivamento de [dados de terceiros no Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="74bc7-114">For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="74bc7-115">Ao criar consultas para pesquisar e manter dados de terceiros, você também pode usar condições para restringir os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="74bc7-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="74bc7-116">Para obter mais informações sobre a criação de consultas de pesquisa de conteúdo, consulte [keyword queries and Search Conditions for Content Search](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="74bc7-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="74bc7-117">Criar uma consulta para Pesquisar tipos específicos de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="74bc7-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="74bc7-118">Em vez de Pesquisar todos os tipos de dados de terceiros, você pode criar consultas que só pesquisem um tipo especificado de dados de terceiros usando o par de valor de propriedade de mensagem a seguir na caixa de palavra-chave de uma pesquisa de conteúdo:</span><span class="sxs-lookup"><span data-stu-id="74bc7-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="74bc7-119">Por exemplo, para pesquisar apenas dados do Facebook que contenham a palavra "contoso" na propriedade Subject, você deve usar a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="74bc7-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="74bc7-120">A tabela a seguir lista os tipos de dados de terceiros que podem ser pesquisados e o valor a ser usado `itemclass:` para a propriedade Message para pesquisar especificamente o tipo de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="74bc7-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="74bc7-121">Observe que a sintaxe de consulta não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="74bc7-121">Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="74bc7-122">**Tipo de dados de terceiros**</span><span class="sxs-lookup"><span data-stu-id="74bc7-122">**Third-party data type**</span></span>|<span data-ttu-id="74bc7-123">**Valor da `itemclass:` Propriedade**</span><span class="sxs-lookup"><span data-stu-id="74bc7-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74bc7-124">META</span><span class="sxs-lookup"><span data-stu-id="74bc7-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="74bc7-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="74bc7-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="74bc7-126">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="74bc7-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="74bc7-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="74bc7-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="74bc7-128">Ares</span><span class="sxs-lookup"><span data-stu-id="74bc7-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="74bc7-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="74bc7-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="74bc7-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="74bc7-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="74bc7-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="74bc7-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="74bc7-132">Espaço reservado do AXS</span><span class="sxs-lookup"><span data-stu-id="74bc7-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="74bc7-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="74bc7-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="74bc7-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="74bc7-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="74bc7-135">BearShare</span><span class="sxs-lookup"><span data-stu-id="74bc7-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="74bc7-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="74bc7-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="74bc7-137">Rim</span><span class="sxs-lookup"><span data-stu-id="74bc7-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="74bc7-138">Logs de chamadas do BlackBerry</span><span class="sxs-lookup"><span data-stu-id="74bc7-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="74bc7-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="74bc7-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="74bc7-140">PIN do BlackBerry</span><span class="sxs-lookup"><span data-stu-id="74bc7-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="74bc7-141">SMS BlackBerry</span><span class="sxs-lookup"><span data-stu-id="74bc7-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="74bc7-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="74bc7-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="74bc7-143">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="74bc7-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="74bc7-144">Mensagens do Bloomberg</span><span class="sxs-lookup"><span data-stu-id="74bc7-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="74bc7-145">Caixa</span><span class="sxs-lookup"><span data-stu-id="74bc7-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="74bc7-146">Servidor de &amp; presença de im da Cisco</span><span class="sxs-lookup"><span data-stu-id="74bc7-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="74bc7-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="74bc7-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="74bc7-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="74bc7-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="74bc7-149">Conexão Direta</span><span class="sxs-lookup"><span data-stu-id="74bc7-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="74bc7-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="74bc7-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="74bc7-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="74bc7-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="74bc7-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="74bc7-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="74bc7-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="74bc7-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="74bc7-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="74bc7-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="74bc7-155">Google +</span><span class="sxs-lookup"><span data-stu-id="74bc7-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="74bc7-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="74bc7-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="74bc7-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="74bc7-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="74bc7-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="74bc7-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="74bc7-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="74bc7-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="74bc7-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="74bc7-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="74bc7-161">Conexões IBM</span><span class="sxs-lookup"><span data-stu-id="74bc7-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="74bc7-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="74bc7-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="74bc7-163">Chat de gelo</span><span class="sxs-lookup"><span data-stu-id="74bc7-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="74bc7-164">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="74bc7-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="74bc7-165">Instagram</span><span class="sxs-lookup"><span data-stu-id="74bc7-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="74bc7-166">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="74bc7-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="74bc7-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="74bc7-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="74bc7-168">IRC</span><span class="sxs-lookup"><span data-stu-id="74bc7-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="74bc7-169">Jive</span><span class="sxs-lookup"><span data-stu-id="74bc7-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="74bc7-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="74bc7-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="74bc7-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="74bc7-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="74bc7-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="74bc7-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="74bc7-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="74bc7-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="74bc7-174">UC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="74bc7-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="74bc7-175">Alinhamento de mentalidade</span><span class="sxs-lookup"><span data-stu-id="74bc7-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="74bc7-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="74bc7-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="74bc7-177">MSN</span><span class="sxs-lookup"><span data-stu-id="74bc7-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="74bc7-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="74bc7-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="74bc7-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="74bc7-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="74bc7-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="74bc7-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="74bc7-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="74bc7-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="74bc7-182">Navegação dinâmica</span><span class="sxs-lookup"><span data-stu-id="74bc7-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="74bc7-183">QQ</span><span class="sxs-lookup"><span data-stu-id="74bc7-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="74bc7-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="74bc7-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="74bc7-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="74bc7-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="74bc7-186">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="74bc7-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="74bc7-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="74bc7-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="74bc7-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="74bc7-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="74bc7-189">Squawker</span><span class="sxs-lookup"><span data-stu-id="74bc7-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="74bc7-190">Symphony</span><span class="sxs-lookup"><span data-stu-id="74bc7-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="74bc7-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="74bc7-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="74bc7-192">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="74bc7-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="74bc7-193">Tor</span><span class="sxs-lookup"><span data-stu-id="74bc7-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="74bc7-194">TTT</span><span class="sxs-lookup"><span data-stu-id="74bc7-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="74bc7-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="74bc7-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="74bc7-196">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="74bc7-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="74bc7-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="74bc7-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="74bc7-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="74bc7-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="74bc7-199">Winny</span><span class="sxs-lookup"><span data-stu-id="74bc7-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="74bc7-200">Toolbar</span><span class="sxs-lookup"><span data-stu-id="74bc7-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="74bc7-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="74bc7-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="74bc7-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="74bc7-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="74bc7-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="74bc7-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
