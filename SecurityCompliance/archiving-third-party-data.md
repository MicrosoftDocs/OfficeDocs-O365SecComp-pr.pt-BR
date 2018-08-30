---
title: Arquivamento de dados de terceiros no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Os administradores podem importar dados de terceiros de plataformas de mídia social, as plataformas de mensagens instantâneas e plataformas de colaboração de documento para caixas de correio em sua organização do Office 365. Isso permite arquivar dados de fontes de dados, Twitter e Facebook no Office 365. Em seguida, você pode appply recursos de conformidade do Office 365 (por exemplo, retenção legal, pesquisa de conteúdo e políticas de retenção) aos dados de terceiros.
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230033"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="305d5-105">Arquivamento de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="305d5-p102">Permite os administradores importar e arquivar dados de terceiros de plataformas de mídia social, mensagens instantâneas plataformas e plataformas de colaboração de documento, a caixas de correio em sua organização do Office 365 do Office 365. Exemplos de fontes de dados de terceiros que podem ser importados para o Office 365 incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="305d5-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="305d5-108">**Social** - Twitter, Facebook, LinkedIn e Yammer</span><span class="sxs-lookup"><span data-stu-id="305d5-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="305d5-109">**Mensagens instantâneas** - Jabber Cisco, GoogleTalk e Yahoo Messenger</span><span class="sxs-lookup"><span data-stu-id="305d5-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="305d5-110">**Colaboração de documentos** - caixa e a pasta de recados</span><span class="sxs-lookup"><span data-stu-id="305d5-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="305d5-111">**Setores verticais** - Customer Relationship Management (por exemplo, a equipe de vendas instabilidade) e Financials (por exemplo, Thomson Reuters e Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="305d5-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="305d5-112">**Mensagens de SMS/texto** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="305d5-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="305d5-p103">Após a importação de dados de terceiros, você pode aplicar recursos de conformidade do Office 365 — como as políticas de retenção de litígio, pesquisa de conteúdo, arquivamento In-loco, auditoria e Office 365 — a esses dados. Por exemplo, quando uma caixa de correio for colocada em retenção de litígio, dados de terceiros serão preservados. Você pode pesquisar dados de terceiros usando a pesquisa de conteúdo. Ou você pode aplicar o arquivamento e políticas de retenção para dados de terceiros exatamente como você pode usar para dados da Microsoft. Em resumo, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização permanecer em conformidade com normas políticas e governamentais.</span><span class="sxs-lookup"><span data-stu-id="305d5-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="305d5-118">Aqui está uma visão geral do processo e as etapas necessárias para importar dados de terceiros para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="305d5-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="305d5-119">Etapa 1: encontrar um parceiro de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="305d5-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="305d5-120">Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="305d5-121">Etapa 3: configurar caixas de correio de usuário para dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="305d5-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="305d5-122">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="305d5-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="305d5-123">Como o processo de importação de dados de terceiros funciona ></span><span class="sxs-lookup"><span data-stu-id="305d5-123">How the third-party data import process works></span></span>

<span data-ttu-id="305d5-124">A ilustração e a descrição a seguir explicam como funciona o processo de importação de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="305d5-124">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Como funciona o processo de importação de dados de terceiros](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="305d5-126">Cliente trabalha com seus parceiros de escolha para configurar um conector que irá extrair itens da fonte de dados de terceiros e depois importar os itens para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="305d5-126">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="305d5-p104">O conector de parceiro conecta-se às fontes de dados de terceiros por meio de uma API de terceiros (em uma base agendada ou configurado como) e extrai itens da fonte de dados. O conector de parceiro converte o conteúdo de um item em um formato de mensagem de email. Consulte a seção de [informações adicionais](#more-information) para obter uma descrição do esquema de formato de mensagem.</span><span class="sxs-lookup"><span data-stu-id="305d5-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="305d5-130">Conector de parceiro conecta-se ao serviço Azure no Office 365 usando o serviço Web do Exchange (EWS) por meio de um ponto de extremidade conhecido.</span><span class="sxs-lookup"><span data-stu-id="305d5-130">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="305d5-p105">Os itens são importados para a caixa de correio de um usuário específico ou para uma caixa de correio de dados de terceiros "pega-tudo". Os critérios a seguir definem se um item será importado para a caixa de correio de um usuário específico ou para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="305d5-p106">r. **itens que têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** - se o conector de parceiro pode mapear a ID de usuário do item na fonte de dados de terceiros para um usuário específico que ID no Office 365, o item é copiado para a pasta em que o usuário **limpa** Pasta de itens recuperáveis. Os usuários não podem acessar os itens na pasta limpezas. No entanto, você pode usar as ferramentas de descoberta eletrônica do Office 365 para procurar itens na pasta limpezas.</span><span class="sxs-lookup"><span data-stu-id="305d5-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="305d5-p107">b. **itens que não têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** - se o conector de parceiro não pode mapear a ID de usuário de um item para um usuário específico que ID no Office 365, o item é copiado para a pasta de **caixa de entrada** da caixa de correio de dados de terceiros. Importação de itens na caixa de entrada permite a você ou alguém em sua organização para entrar na caixa de correio de terceiros para exibir e gerenciar esses itens e veja se qualquer ajustes precisam ser feitas na configuração do conector de parceiro.</span><span class="sxs-lookup"><span data-stu-id="305d5-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="305d5-140">Etapa 1: encontrar um parceiro de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="305d5-140">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="305d5-p108">Um componente essencial para arquivar dados de terceiros no Office 365 está encontrando e como trabalhar com um parceiro da Microsoft especializada na captura de dados de uma fonte de dados de terceiros e importá-lo para o Office 365. Depois que os dados são importados, podem ser arquivado e preservada juntamente com outros dados da Microsoft, como o email do Exchange e documentos do SharePoint e o OneDrive for Business da sua organização. Um parceiro cria um conector que extrai dados de fontes de dados de terceiros da sua organização (por exemplo, BlackBerry, Facebook, Google +, Reuters Thomson, Twitter e YouTube) e transmite dados para uma API do Office 365 que importa itens para caixas de correio do Exchange como mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="305d5-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="305d5-144">As seções a seguir listam os parceiros da Microsoft — e as fontes de dados de terceiros que eles suportam — que estão participando do programa para arquivar dados de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="305d5-144">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="305d5-145">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="305d5-145">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="305d5-146">Actiance</span><span class="sxs-lookup"><span data-stu-id="305d5-146">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="305d5-147">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="305d5-147">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="305d5-148">Globanet</span><span class="sxs-lookup"><span data-stu-id="305d5-148">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="305d5-149">OpenText</span><span class="sxs-lookup"><span data-stu-id="305d5-149">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="305d5-150">Verba</span><span class="sxs-lookup"><span data-stu-id="305d5-150">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="305d5-151">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="305d5-151">17a-4 LLC</span></span>

<span data-ttu-id="305d5-152">17a-4 LLC é compatível com as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-152">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="305d5-153">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="305d5-153">BlackBerry</span></span>
    
- <span data-ttu-id="305d5-154">Fluxos de dados do Bloomberg</span><span class="sxs-lookup"><span data-stu-id="305d5-154">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="305d5-155">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="305d5-155">Cisco Jabber</span></span>
    
- <span data-ttu-id="305d5-156">FactSet</span><span class="sxs-lookup"><span data-stu-id="305d5-156">FactSet</span></span>
    
- <span data-ttu-id="305d5-157">HipChat</span><span class="sxs-lookup"><span data-stu-id="305d5-157">HipChat</span></span>
    
- <span data-ttu-id="305d5-158">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="305d5-158">InvestEdge</span></span>
    
- <span data-ttu-id="305d5-159">LivePerson</span><span class="sxs-lookup"><span data-stu-id="305d5-159">LivePerson</span></span>
    
- <span data-ttu-id="305d5-160">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="305d5-160">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="305d5-161">OpenText</span><span class="sxs-lookup"><span data-stu-id="305d5-161">OpenText</span></span>
    
- <span data-ttu-id="305d5-162">Oracle/ATG 'click-to-call' Live Help
</span><span class="sxs-lookup"><span data-stu-id="305d5-162">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="305d5-163">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="305d5-163">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="305d5-164">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="305d5-164">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="305d5-165">MindAlign</span><span class="sxs-lookup"><span data-stu-id="305d5-165">MindAlign</span></span>
    
- <span data-ttu-id="305d5-166">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="305d5-166">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="305d5-167">
Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="305d5-167">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="305d5-168">
Skype for Business Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="305d5-168">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="305d5-169">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="305d5-169">SQL Databases</span></span>
    
- <span data-ttu-id="305d5-170">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="305d5-170">Squawker</span></span>
    
- <span data-ttu-id="305d5-171">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="305d5-171">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="305d5-172">Actiance</span><span class="sxs-lookup"><span data-stu-id="305d5-172">Actiance</span></span>

<span data-ttu-id="305d5-173">[Actiance](https://www.actiance.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-173">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="305d5-174">OBJETIVO</span><span class="sxs-lookup"><span data-stu-id="305d5-174">AIM</span></span>
    
- <span data-ttu-id="305d5-175">American Idol</span><span class="sxs-lookup"><span data-stu-id="305d5-175">American Idol</span></span>
    
- <span data-ttu-id="305d5-176">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="305d5-176">Apple Juice</span></span>
    
- <span data-ttu-id="305d5-177">
AOL with Pivot Client
</span><span class="sxs-lookup"><span data-stu-id="305d5-177">AOL with Pivot client</span></span>
    
- <span data-ttu-id="305d5-178">Ares</span><span class="sxs-lookup"><span data-stu-id="305d5-178">Ares</span></span>
    
- <span data-ttu-id="305d5-179">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="305d5-179">Bazaar Voice</span></span>
    
- <span data-ttu-id="305d5-180">Bear Share</span><span class="sxs-lookup"><span data-stu-id="305d5-180">Bear Share</span></span>
    
- <span data-ttu-id="305d5-181">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="305d5-181">Bit Torrent</span></span>
    
- <span data-ttu-id="305d5-182">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-182">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-183">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-183">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-184">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-184">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-185">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-185">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-186">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="305d5-186">Bloomberg Mail</span></span>
    
- <span data-ttu-id="305d5-187">CellTrust</span><span class="sxs-lookup"><span data-stu-id="305d5-187">CellTrust</span></span>
    
- <span data-ttu-id="305d5-188">Importação de bate-papo
</span><span class="sxs-lookup"><span data-stu-id="305d5-188">Chat Import</span></span>
    
- <span data-ttu-id="305d5-189">Política e registros de bate-papo em tempo real
</span><span class="sxs-lookup"><span data-stu-id="305d5-189">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="305d5-190">Instabilidade
</span><span class="sxs-lookup"><span data-stu-id="305d5-190">Chatter</span></span>
    
- <span data-ttu-id="305d5-191">Cisco IM &amp; servidor de presença (v9.0.1, v 9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="305d5-191">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="305d5-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="305d5-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="305d5-193">Importação de colaboração
</span><span class="sxs-lookup"><span data-stu-id="305d5-193">Collaboration Import</span></span>
    
- <span data-ttu-id="305d5-194">Registro de colaboração em tempo real
</span><span class="sxs-lookup"><span data-stu-id="305d5-194">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="305d5-195">Conexão Direta</span><span class="sxs-lookup"><span data-stu-id="305d5-195">Direct Connect</span></span>
    
- <span data-ttu-id="305d5-196">Facebook</span><span class="sxs-lookup"><span data-stu-id="305d5-196">Facebook</span></span>
    
- <span data-ttu-id="305d5-197">FactSet</span><span class="sxs-lookup"><span data-stu-id="305d5-197">FactSet</span></span>
    
- <span data-ttu-id="305d5-198">FastTrack</span><span class="sxs-lookup"><span data-stu-id="305d5-198">FastTrack</span></span>
    
- <span data-ttu-id="305d5-199">Gnutella</span><span class="sxs-lookup"><span data-stu-id="305d5-199">Gnutella</span></span>
    
- <span data-ttu-id="305d5-200">Google+
</span><span class="sxs-lookup"><span data-stu-id="305d5-200">Google+</span></span>
    
- <span data-ttu-id="305d5-201">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="305d5-201">GoToMyPC</span></span>
    
- <span data-ttu-id="305d5-202">Hopster</span><span class="sxs-lookup"><span data-stu-id="305d5-202">Hopster</span></span>
    
- <span data-ttu-id="305d5-203">HubConnex</span><span class="sxs-lookup"><span data-stu-id="305d5-203">HubConnex</span></span>
    
- <span data-ttu-id="305d5-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="305d5-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="305d5-205">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="305d5-205">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="305d5-206">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="305d5-206">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="305d5-207">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="305d5-207">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="305d5-208">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="305d5-208">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="305d5-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="305d5-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="305d5-210">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="305d5-210">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="305d5-211">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="305d5-211">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="305d5-212">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="305d5-212">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="305d5-213">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="305d5-213">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="305d5-214">Importação de mensagem Instantânea
</span><span class="sxs-lookup"><span data-stu-id="305d5-214">IM Import</span></span>
    
- <span data-ttu-id="305d5-215">Política e registro de mensagem instantânea em tempo real
</span><span class="sxs-lookup"><span data-stu-id="305d5-215">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="305d5-216">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="305d5-216">Indii Messenger</span></span>
    
- <span data-ttu-id="305d5-217">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="305d5-217">Instant Bloomberg</span></span>
    
- <span data-ttu-id="305d5-218">IRC</span><span class="sxs-lookup"><span data-stu-id="305d5-218">IRC</span></span>
    
- <span data-ttu-id="305d5-219">Jive
</span><span class="sxs-lookup"><span data-stu-id="305d5-219">Jive</span></span>
    
- <span data-ttu-id="305d5-220">Jive 6 Real Time Logging (v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="305d5-220">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="305d5-221">Jive Import</span><span class="sxs-lookup"><span data-stu-id="305d5-221">Jive Import</span></span>
    
- <span data-ttu-id="305d5-222">JXTA</span><span class="sxs-lookup"><span data-stu-id="305d5-222">JXTA</span></span>
    
- <span data-ttu-id="305d5-223">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="305d5-223">LinkedIn</span></span>
    
- <span data-ttu-id="305d5-224">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="305d5-224">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="305d5-225">MFTP</span><span class="sxs-lookup"><span data-stu-id="305d5-225">MFTP</span></span>
    
- <span data-ttu-id="305d5-226">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-226">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="305d5-227">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="305d5-227">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="305d5-228">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="305d5-228">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="305d5-229">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="305d5-229">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="305d5-230">MindAlign</span><span class="sxs-lookup"><span data-stu-id="305d5-230">MindAlign</span></span>
    
- <span data-ttu-id="305d5-231">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="305d5-231">Mobile Guard</span></span>
    
- <span data-ttu-id="305d5-232">MSN</span><span class="sxs-lookup"><span data-stu-id="305d5-232">MSN</span></span>
    
- <span data-ttu-id="305d5-233">My Space</span><span class="sxs-lookup"><span data-stu-id="305d5-233">My Space</span></span>
    
- <span data-ttu-id="305d5-234">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="305d5-234">NEONetwork</span></span>
    
- <span data-ttu-id="305d5-235">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="305d5-235">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="305d5-236">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="305d5-236">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="305d5-237">Pinterest</span><span class="sxs-lookup"><span data-stu-id="305d5-237">Pinterest</span></span>
    
- <span data-ttu-id="305d5-238">Tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="305d5-238">Pivot</span></span>
    
- <span data-ttu-id="305d5-239">QQ</span><span class="sxs-lookup"><span data-stu-id="305d5-239">QQ</span></span>
    
- <span data-ttu-id="305d5-240">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="305d5-240">Skype for Business 2015</span></span>
    
- <span data-ttu-id="305d5-241">SoftEther</span><span class="sxs-lookup"><span data-stu-id="305d5-241">SoftEther</span></span>
    
- <span data-ttu-id="305d5-242">Symphony
</span><span class="sxs-lookup"><span data-stu-id="305d5-242">Symphony</span></span>
    
- <span data-ttu-id="305d5-243">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="305d5-243">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="305d5-244">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="305d5-244">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="305d5-245">Tor</span><span class="sxs-lookup"><span data-stu-id="305d5-245">Tor</span></span>
    
- <span data-ttu-id="305d5-246">TTT</span><span class="sxs-lookup"><span data-stu-id="305d5-246">TTT</span></span>
    
- <span data-ttu-id="305d5-247">Twitter</span><span class="sxs-lookup"><span data-stu-id="305d5-247">Twitter</span></span>
    
- <span data-ttu-id="305d5-248">WinMX</span><span class="sxs-lookup"><span data-stu-id="305d5-248">WinMX</span></span>
    
- <span data-ttu-id="305d5-249">Winny</span><span class="sxs-lookup"><span data-stu-id="305d5-249">Winny</span></span>
    
- <span data-ttu-id="305d5-250">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="305d5-250">Yahoo</span></span>
    
- <span data-ttu-id="305d5-251">Yammer</span><span class="sxs-lookup"><span data-stu-id="305d5-251">Yammer</span></span>
    
- <span data-ttu-id="305d5-252">YouTube</span><span class="sxs-lookup"><span data-stu-id="305d5-252">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="305d5-253">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="305d5-253">ArchiveSocial</span></span>

<span data-ttu-id="305d5-254">[ArchiveSocial](https://www.archivesocial.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-254">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="305d5-255">Facebook</span><span class="sxs-lookup"><span data-stu-id="305d5-255">Facebook</span></span>
    
- <span data-ttu-id="305d5-256">Flickr
</span><span class="sxs-lookup"><span data-stu-id="305d5-256">Flickr</span></span>
    
- <span data-ttu-id="305d5-257">Instagram
</span><span class="sxs-lookup"><span data-stu-id="305d5-257">Instagram</span></span>
    
- <span data-ttu-id="305d5-258">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="305d5-258">LinkedIn</span></span>
    
- <span data-ttu-id="305d5-259">Pinterest</span><span class="sxs-lookup"><span data-stu-id="305d5-259">Pinterest</span></span>
    
- <span data-ttu-id="305d5-260">Twitter</span><span class="sxs-lookup"><span data-stu-id="305d5-260">Twitter</span></span>
    
- <span data-ttu-id="305d5-261">YouTube</span><span class="sxs-lookup"><span data-stu-id="305d5-261">YouTube</span></span>
    
- <span data-ttu-id="305d5-262">Vimeo</span><span class="sxs-lookup"><span data-stu-id="305d5-262">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="305d5-263">Globanet</span><span class="sxs-lookup"><span data-stu-id="305d5-263">Globanet</span></span>

<span data-ttu-id="305d5-264">[Globanet](https://www.globanet.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-264">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="305d5-265">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="305d5-265">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="305d5-266">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-266">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-267">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-267">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-268">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-268">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-269">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="305d5-269">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="305d5-270">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="305d5-270">Bloomberg Chat</span></span>
    
- <span data-ttu-id="305d5-271">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="305d5-271">Bloomberg Mail</span></span>
    
- <span data-ttu-id="305d5-272">Box
</span><span class="sxs-lookup"><span data-stu-id="305d5-272">Box</span></span>
    
- <span data-ttu-id="305d5-273">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="305d5-273">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="305d5-274">Cisco IM &amp; (v10, v10.5.1 SU1, v11.0, v11.5 SU2) do servidor de presença</span><span class="sxs-lookup"><span data-stu-id="305d5-274">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="305d5-275">Cisco Webex equipes</span><span class="sxs-lookup"><span data-stu-id="305d5-275">Cisco Webex Teams</span></span>

- <span data-ttu-id="305d5-276">Espaço de trabalho do Citrix &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="305d5-276">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="305d5-277">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="305d5-277">CrowdCompass</span></span>

- <span data-ttu-id="305d5-278">Arquivos de texto delimitado personalizado
</span><span class="sxs-lookup"><span data-stu-id="305d5-278">Custom delimited text files</span></span>
    
- <span data-ttu-id="305d5-279">Arquivos XML personalizados
</span><span class="sxs-lookup"><span data-stu-id="305d5-279">Custom XML files</span></span>
    
- <span data-ttu-id="305d5-280">Facebook (páginas)</span><span class="sxs-lookup"><span data-stu-id="305d5-280">Facebook (Pages)</span></span>
    
- <span data-ttu-id="305d5-281">Factset
</span><span class="sxs-lookup"><span data-stu-id="305d5-281">Factset</span></span>
    
- <span data-ttu-id="305d5-282">FXConnect</span><span class="sxs-lookup"><span data-stu-id="305d5-282">FXConnect</span></span>
    
- <span data-ttu-id="305d5-283">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="305d5-283">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="305d5-284">Jive
</span><span class="sxs-lookup"><span data-stu-id="305d5-284">Jive</span></span>
    
- <span data-ttu-id="305d5-285">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="305d5-285">Macgregor XIP</span></span>

- <span data-ttu-id="305d5-286">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="305d5-286">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="305d5-287">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="305d5-287">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="305d5-288">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="305d5-288">Microsoft Teams</span></span>
       
- <span data-ttu-id="305d5-289">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="305d5-289">Microsoft Yammer</span></span>
    
- <span data-ttu-id="305d5-290">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="305d5-290">Mobile Guard</span></span>
    
- <span data-ttu-id="305d5-291">Tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="305d5-291">Pivot</span></span>
    
- <span data-ttu-id="305d5-292">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="305d5-292">Salesforce Chatter</span></span>

- <span data-ttu-id="305d5-293">Skype for Business online</span><span class="sxs-lookup"><span data-stu-id="305d5-293">Skype for Business Online</span></span>
    
- <span data-ttu-id="305d5-294">Skype for Business, versões 2007 R2 - 2016 (local)
</span><span class="sxs-lookup"><span data-stu-id="305d5-294">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="305d5-295">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="305d5-295">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="305d5-296">Symphony
</span><span class="sxs-lookup"><span data-stu-id="305d5-296">Symphony</span></span>
    
- <span data-ttu-id="305d5-297">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="305d5-297">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="305d5-298">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="305d5-298">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="305d5-299">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="305d5-299">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="305d5-300">Twitter</span><span class="sxs-lookup"><span data-stu-id="305d5-300">Twitter</span></span>
    
- <span data-ttu-id="305d5-301">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="305d5-301">UBS Chat</span></span>
    
- <span data-ttu-id="305d5-302">YouTube</span><span class="sxs-lookup"><span data-stu-id="305d5-302">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="305d5-303">OpenText</span><span class="sxs-lookup"><span data-stu-id="305d5-303">OpenText</span></span>

<span data-ttu-id="305d5-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="305d5-305">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="305d5-305">Axs Encrypted</span></span>
    
- <span data-ttu-id="305d5-306">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="305d5-306">Axs Exchange</span></span>
    
- <span data-ttu-id="305d5-307">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="305d5-307">Axs Local Archive</span></span>
    
- <span data-ttu-id="305d5-308">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="305d5-308">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="305d5-309">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="305d5-309">Axs Signed</span></span>
    
- <span data-ttu-id="305d5-310">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="305d5-310">Bloomberg</span></span>
    
- <span data-ttu-id="305d5-311">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="305d5-311">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="305d5-312">Verba</span><span class="sxs-lookup"><span data-stu-id="305d5-312">Verba</span></span>

<span data-ttu-id="305d5-313">[Verba](https://www.verba.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-313">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="305d5-314">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="305d5-314">Avaya Aura Video</span></span>
    
- <span data-ttu-id="305d5-315">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-315">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="305d5-316">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="305d5-316">Avtec Radio</span></span>
    
- <span data-ttu-id="305d5-317">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="305d5-317">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="305d5-318">BroadSoft Vídeo
</span><span class="sxs-lookup"><span data-stu-id="305d5-318">BroadSoft Video</span></span>
    
- <span data-ttu-id="305d5-319">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-319">BroadSoft Voice</span></span>
    
- <span data-ttu-id="305d5-320">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-320">Centile Voice</span></span>
    
- <span data-ttu-id="305d5-321">Cisco Jabber IM
</span><span class="sxs-lookup"><span data-stu-id="305d5-321">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="305d5-322">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="305d5-322">Cisco UC Video</span></span>
    
- <span data-ttu-id="305d5-323">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-323">Cisco UC Voice</span></span>
    
- <span data-ttu-id="305d5-324">Vídeo UCCX/UCCE Cisco</span><span class="sxs-lookup"><span data-stu-id="305d5-324">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="305d5-325">Cisco UCCX/UCCE voz</span><span class="sxs-lookup"><span data-stu-id="305d5-325">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="305d5-326">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="305d5-326">ESChat Radio</span></span>
    
- <span data-ttu-id="305d5-327">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="305d5-327">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="305d5-328">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-328">IP Trade Voice</span></span>
    
- <span data-ttu-id="305d5-329">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="305d5-329">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="305d5-330">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="305d5-330">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="305d5-331">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="305d5-331">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="305d5-332">Oracle / Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="305d5-332">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="305d5-333">Oracle / Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-333">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="305d5-334">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-334">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="305d5-335">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="305d5-335">SIPREC Video</span></span>
    
-  <span data-ttu-id="305d5-336">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="305d5-336">SIPREC Voice</span></span> 
    
- <span data-ttu-id="305d5-337">Skype for Business / Lync IM
</span><span class="sxs-lookup"><span data-stu-id="305d5-337">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="305d5-338">Skype for Business / Lync Video
</span><span class="sxs-lookup"><span data-stu-id="305d5-338">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="305d5-339">Skype for Business / Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-339">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="305d5-340">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-340">Speakerbus Voice</span></span>
    
- <span data-ttu-id="305d5-341">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="305d5-341">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="305d5-342">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="305d5-342">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="305d5-343">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="305d5-343">Truphone Voice</span></span>
    
- <span data-ttu-id="305d5-344">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="305d5-344">TwistedPair Radio</span></span>
    
- <span data-ttu-id="305d5-345">Windows Desktop Computer Screen 
</span><span class="sxs-lookup"><span data-stu-id="305d5-345">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="305d5-346">Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-346">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="305d5-p109">Aqui estão as etapas para criar e configurar uma caixa de correio de dados de terceiros para importar dados para o Office 365. Anterior conforme explicado, itens são importados para esta caixa de correio se o conector de parceiro não pode mapear a ID de usuário do item para uma conta de usuário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="305d5-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="305d5-349">**Concluir essas tarefas no Centro de administração do Office 365**</span><span class="sxs-lookup"><span data-stu-id="305d5-349">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="305d5-p110">Criar uma nova conta de usuário no Office 365 e atribuí-lo uma licença do Exchange Online plano 2; consulte [Adicionar usuários para o Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). É necessária uma licença de plano 2 para colocar a caixa de correio em retenção de litígio ou habilitar uma caixa de correio de arquivamento que tem uma cota de armazenamento ilimitado.</span><span class="sxs-lookup"><span data-stu-id="305d5-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="305d5-352">Adicione a conta de usuário para a caixa de correio de dados de terceiros para a função de administrador do **Exchange administrator** no Office 365; consulte [atribuir funções de administrador no Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="305d5-352">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="305d5-p111">Anote as credenciais da conta do usuário. Você precisa enviá-las para o seu parceiro, conforme descrito na Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="305d5-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="305d5-355">**Concluir essas tarefas no Centro de administração do Exchange**</span><span class="sxs-lookup"><span data-stu-id="305d5-355">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="305d5-p112">Ocultar a caixa de correio de dados de terceiros do catálogo de endereços e outras listas de endereços na organização; consulte [gerenciar caixas de correio do usuário](https://go.microsoft.com/fwlink/p/?LinkId=616058). Como alternativa, você pode executar o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="305d5-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="305d5-358">Atribuir a permissão **FullAccess** para a caixa de correio de dados de terceiros para que os administradores ou oficiais de conformidade podem abrir a caixa de correio de dados de terceiros no cliente de desktop do Outlook; consulte [Manage permissions para destinatários](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="305d5-358">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="305d5-359">Habilite os seguintes recursos do Office 365 relacionados à conformidade para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="305d5-359">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="305d5-p113">Habilitar a caixa de correio de arquivo morto; consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md). Isso permitirá que você espaço de armazenamento de livre-up, na caixa de correio principal, configurando uma política de arquivamento que move itens de dados de terceiros para a caixa de correio de arquivo morto. Isso fornecerá com armazenamento ilimitado para dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="305d5-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="305d5-p114">Coloque a caixa de correio de dados de terceiros em retenção de litígio. Você também pode aplicar uma política de retenção do Office 365 no Office 365 Security &amp; Centro de conformidade. Fazer esta caixa de correio em espera reter itens de dados de terceiros (indefinidamente ou por um período especificado) e impedi-los de serem removidos da caixa de correio. Consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="305d5-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="305d5-367">Colocar uma caixa de correio em Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="305d5-367">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="305d5-368">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-368">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="305d5-p115">Habilitar a caixa de correio log de auditoria para acesso de proprietário, representante e admin na caixa de correio de dados de terceiros; consulte [Habilitar caixa de correio auditorias no Office 365](enable-mailbox-auditing.md). Isso permitirá a auditoria de todas as atividades realizadas por qualquer usuário que tenha acesso à caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="305d5-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="305d5-371">Etapa 3: configurar caixas de correio de usuário para dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="305d5-371">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="305d5-p116">A próxima etapa é configurar caixas de correio de usuário para oferecer suporte aos dados de terceiros. Conclua essas tarefas usando o Centro de administração do Exchange ou usando os cmdlets do Windows PowerShell correspondentes.</span><span class="sxs-lookup"><span data-stu-id="305d5-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="305d5-374">Habilitar a caixa de correio de arquivamento para cada usuário; consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="305d5-374">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="305d5-375">Colocar caixas de correio do usuário em litígio ou aplicar uma política de retenção do Office 365; Consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="305d5-375">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="305d5-376">Colocar uma caixa de correio em Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="305d5-376">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="305d5-377">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-377">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="305d5-378">Conforme mencionado anteriormente, quando você coloca as caixas de correio em retenção, é possível definir uma duração para a retenção dos itens da fonte de dados de terceiros, ou você pode optar por reter itens indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="305d5-378">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="305d5-379">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="305d5-379">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="305d5-380">A etapa final é fornecer a seu parceiro as informações a seguir, para que ele possa configurar o conector a fim de se conectar à sua organização do Office 365 e importar dados para as caixas de correio do usuário e para a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="305d5-380">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="305d5-381">O ponto de extremidade usado para conectar ao serviço do Windows Azure no Office 365:</span><span class="sxs-lookup"><span data-stu-id="305d5-381">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="305d5-p117">Entrar no credenciais (ID de usuário do Office 365 e senha) da caixa de correio dados de terceiros que você criou na etapa 2. Essas credenciais são necessárias para que o conector de parceiro possa acessar e importar itens para caixas de correio do usuário e a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="305d5-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
    

  
## <a name="more-information"></a><span data-ttu-id="305d5-384">Mais informações</span><span class="sxs-lookup"><span data-stu-id="305d5-384">More information</span></span>

- <span data-ttu-id="305d5-p118">Anterior conforme explicado, itens de dados de terceiros fontes são importados para caixas de correio do Exchange como mensagens de email. O conector de parceiro importa o item usando um esquema necessário para a API do Office 365. A tabela a seguir descreve as propriedades de mensagem de um item de uma fonte de dados de terceiros depois que ela é importada para uma caixa de correio do Exchange como uma mensagem de email. A tabela também indica se a propriedade de mensagem é obrigatória. Propriedades obrigatórias devem ser preenchidas. Se um item estiver faltando uma propriedade obrigatória, ele não será importado para o Office 365. O processo de importação retornará uma mensagem de erro que explica por que um item não foi importado e qual propriedade está ausente.</span><span class="sxs-lookup"><span data-stu-id="305d5-p118">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="305d5-392">**Propriedade da mensagem**</span><span class="sxs-lookup"><span data-stu-id="305d5-392">**Message property**</span></span>|<span data-ttu-id="305d5-393">**Obrigatório?**</span><span class="sxs-lookup"><span data-stu-id="305d5-393">**Mandatory?**</span></span>|<span data-ttu-id="305d5-394">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="305d5-394">**Description**</span></span>|<span data-ttu-id="305d5-395">**Valor de exemplo**</span><span class="sxs-lookup"><span data-stu-id="305d5-395">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="305d5-396">**DE **</span><span class="sxs-lookup"><span data-stu-id="305d5-396">**FROM**</span></span> <br/> |<span data-ttu-id="305d5-397">Sim</span><span class="sxs-lookup"><span data-stu-id="305d5-397">Yes</span></span>  <br/> |<span data-ttu-id="305d5-p119">O usuário que originalmente criada ou enviado o item na fonte de dados de terceiros. O conector de parceiro tentará mapear a ID de usuário do item fonte (por exemplo, uma alça Twitter) para uma conta de usuário do Office 365 para todos os participantes (usuários nos campos FROM e TO). Uma cópia da mensagem será importada para a caixa de correio de cada participante. Se nenhum dos participantes do item pode ser mapeado para uma conta de usuário do Office 365, o item será importado para a caixa de correio de arquivamento de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="305d5-p119">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="305d5-p120">O participante que é identificado como o remetente do item deve ter uma caixa de correio ativa em que o item que está sendo importado para a organização do Office 365. Se o remetente não tem uma caixa de correio ativa, o seguinte erro será retornado:</span><span class="sxs-lookup"><span data-stu-id="305d5-p120">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="305d5-404">**PARA**</span><span class="sxs-lookup"><span data-stu-id="305d5-404">**TO**</span></span> <br/> |<span data-ttu-id="305d5-405">Sim</span><span class="sxs-lookup"><span data-stu-id="305d5-405">Yes</span></span>  <br/> |<span data-ttu-id="305d5-406">O usuário que recebeu um item, caso seja aplicável a um item na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="305d5-406">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="305d5-407">**ASSUNTO**</span><span class="sxs-lookup"><span data-stu-id="305d5-407">**SUBJECT**</span></span> <br/> |<span data-ttu-id="305d5-408">Não</span><span class="sxs-lookup"><span data-stu-id="305d5-408">No</span></span>  <br/> |<span data-ttu-id="305d5-409">O assunto do item de origem.</span><span class="sxs-lookup"><span data-stu-id="305d5-409">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="305d5-410">**DATA**</span><span class="sxs-lookup"><span data-stu-id="305d5-410">**DATE**</span></span> <br/> |<span data-ttu-id="305d5-411">Sim</span><span class="sxs-lookup"><span data-stu-id="305d5-411">Yes</span></span>  <br/> |<span data-ttu-id="305d5-412">A data na qual o item foi originalmente criado ou publicado na fonte de dados do cliente. Por exemplo, a data quando uma mensagem do Twitter foi enviada.</span><span class="sxs-lookup"><span data-stu-id="305d5-412">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="305d5-413">**CORPO**</span><span class="sxs-lookup"><span data-stu-id="305d5-413">**BODY**</span></span> <br/> |<span data-ttu-id="305d5-414">Não</span><span class="sxs-lookup"><span data-stu-id="305d5-414">No</span></span>  <br/> |<span data-ttu-id="305d5-p121">O conteúdo da mensagem ou postagem. Para algumas fontes de dados, o conteúdo desta propriedade pode ser o mesmo que o conteúdo para a propriedade **SUBJECT** . Durante o processo de importação, o conector de parceiro tenta manter com fidelidade total da fonte de conteúdo possível. Se possível arquivos, gráficos ou outros conteúdos do corpo do item de origem está incluído nesta propriedade. Caso contrário, o conteúdo do item fonte é incluído na propriedade **anexo** . O conteúdo dessa propriedade será dependem do conector de parceiro e a capacidade da plataforma do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="305d5-p121">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="305d5-421">**ANEXO**</span><span class="sxs-lookup"><span data-stu-id="305d5-421">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="305d5-422">Não</span><span class="sxs-lookup"><span data-stu-id="305d5-422">No</span></span>  <br/> |<span data-ttu-id="305d5-p122">Se um item na fonte de dados (por exemplo, uma tweet no Twitter ou uma conversa de mensagem instantânea) tem um arquivo anexado ou incluir imagens, o parceiro conecte-se a primeira tentativa será incluir anexos na propriedade **BODY** . Se isso não é possível, então ela será adicionada ao * * anexo * * propriedade. Outros exemplos de anexos incluem Curtições no Facebook, metadados da fonte de conteúdo e as respostas a uma mensagem ou postagem.</span><span class="sxs-lookup"><span data-stu-id="305d5-p122">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="305d5-426">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="305d5-426">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="305d5-427">Sim</span><span class="sxs-lookup"><span data-stu-id="305d5-427">Yes</span></span>  <br/> | <span data-ttu-id="305d5-p123">Esta é uma propriedade de valor múltiplos, que é criada e preenchida pelo conector de parceiro. O formato dessa propriedade é `IPM.NOTE.Source.Event`. (Esta propriedade deve começar com `IPM.NOTE`; esse formato é similar para o `IPM.NOTE.X` classe de mensagem.) Essa propriedade inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="305d5-p123">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="305d5-431">`Source`-Indica a fonte de dados de terceiros; Por exemplo, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="305d5-431">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="305d5-p124">`Event`-Indica o tipo de atividade foi executada na fonte de dados de terceiros que produzidos os itens; Por exemplo, uma tweet no Twitter ou uma postagem em Facebook. Eventos são específicos para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="305d5-p124">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="305d5-p125">Uma finalidade dessa propriedade é filtrar itens específicos com base na fonte de dados em que um item foi originada ou com base no tipo de evento. Por exemplo, em uma pesquisa de descoberta eletrônica, você pode criar uma consulta de pesquisa para localizar todas as tweets publicadas por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="305d5-p125">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="305d5-p126">Quando os itens são importados com êxito a caixas de correio no Office 365, um identificador exclusivo é retornado de volta para o chamador como parte da resposta HTTP. Esse identificador — chamado `x-IngestionCorrelationID`— pode ser usado para fins de solução de problemas subsequentes por parceiros para o rastreamento de ponta a ponta de itens. É recomendável que os parceiros capturam essas informações e faça o logon adequadamente no seu lado. Aqui está um exemplo de uma resposta HTTP mostrando esse identificador:</span><span class="sxs-lookup"><span data-stu-id="305d5-p126">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="305d5-p127">Você pode usar a ferramenta de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Para pesquisar especificamente para esses itens importados, você pode usar os seguintes pares de valor da propriedade de mensagem na caixa de palavra-chave para uma pesquisa de conteúdo. .</span><span class="sxs-lookup"><span data-stu-id="305d5-p127">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="305d5-p128">**`kind:externaldata`**-Use este par de valor de propriedade para pesquisa todos os tipos de dados de terceiros. Por exemplo, para pesquisar itens que tenham sido importados de uma fonte de dados de terceiros e contêm a palavra "contoso" na propriedade assunto do item importado, você usaria a consulta de palavra-chave `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="305d5-p128">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="305d5-p129">**`itemclass:ipm.externaldata.<third-party data type>`**-Use este par de valor da propriedade à pesquisa somente um tipo de especificar de dados de terceiros. Por exemplo, para pesquisar somente dados de Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a consulta de palavra-chave `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="305d5-p129">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="305d5-447">Para obter uma lista completa dos valores a serem usados para tipos de dados de terceiros para o `itemclass` propriedade, consulte [Use pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="305d5-447">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="305d5-448">Veja mais informações sobre como usar a Pesquisa de Conteúdo e criar consultas de pesquisa de palavra-chave em:</span><span class="sxs-lookup"><span data-stu-id="305d5-448">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="305d5-449">Pesquisa de conteúdo no Office 365</span><span class="sxs-lookup"><span data-stu-id="305d5-449">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="305d5-450">Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="305d5-450">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
