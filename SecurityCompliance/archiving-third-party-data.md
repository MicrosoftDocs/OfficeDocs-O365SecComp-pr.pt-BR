---
title: Arquivamento de dados de terceiros no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Os administradores podem importar dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos para caixas de correio em sua organização do Office 365. Isso permite que você arquive dados de Facebook, Twitter e fontes de dados no Office 365. Em seguida, você pode aplicar recursos de conformidade do Office 365 (como retenção legal, pesquisa de conteúdo e políticas de retenção) a dados de terceiros.
ms.openlocfilehash: 06ac436b1583187e89cb7f1beb26411ba02becec
ms.sourcegitcommit: 86ff2eba1d57b9d5288840788529e69ad9d836b6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/11/2019
ms.locfileid: "31818608"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="a81a1-105">Arquivamento de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="a81a1-106">O Office 365 permite que os administradores importem e arquivem dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos, para caixas de correio em sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-106">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization.</span></span> <span data-ttu-id="a81a1-107">Exemplos de fontes de dados de terceiros que podem ser importadas para o Office 365 incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a81a1-107">Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="a81a1-108">**Social** -Twitter, Facebook, Yammer e LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a81a1-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="a81a1-109">**Mensagens instantâneas** -Yahoo Messenger, GoogleTalk e Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="a81a1-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="a81a1-110">Documentar a caixa de **colaboração** e o Dropbox</span><span class="sxs-lookup"><span data-stu-id="a81a1-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="a81a1-111">**Setores verticais** – gerenciamento de relacionamento com o cliente (como o Salesforce informativo) e serviços financeiros (como a Thomson Reuters e Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="a81a1-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financial Services (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="a81a1-112">**SMS/mensagens de texto** -BlackBerry</span><span class="sxs-lookup"><span data-stu-id="a81a1-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="a81a1-113">Após a importação dos dados de terceiros, você pode aplicar recursos de conformidade do Office 365, como retenção de litígio, pesquisa de conteúdo, arquivamento in-loco, auditoria e políticas de retenção do Office 365 — para esses dados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-113">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data.</span></span> <span data-ttu-id="a81a1-114">Por exemplo, quando uma caixa de correio é colocada em Retenção de Litígio, os dados de terceiros são preservados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-114">For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved.</span></span> <span data-ttu-id="a81a1-115">Você pode pesquisar dados de terceiros usando a pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a81a1-115">You can search third-party data by using Content Search.</span></span> <span data-ttu-id="a81a1-116">Se preferir, você pode aplicar políticas de arquivamento e de retenção aos dados de terceiros, assim como faz com os dados da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a81a1-116">Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data.</span></span> <span data-ttu-id="a81a1-117">Em suma, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.</span><span class="sxs-lookup"><span data-stu-id="a81a1-117">In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="a81a1-118">Veja a seguir uma visão geral do processo e as etapas necessárias para importar dados de terceiros para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="a81a1-119">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="a81a1-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="a81a1-120">Step 2: Create and configure a third-party data mailbox in Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="a81a1-121">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="a81a1-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="a81a1-122">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="a81a1-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="a81a1-123">Etapa 5: registrar o conector de dados de terceiros no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a81a1-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="a81a1-124">Como funciona o processo de importação de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="a81a1-124">How the third-party data import process works</span></span>

<span data-ttu-id="a81a1-125">A ilustração e a descrição a seguir explicam como funciona o processo de importação de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Como funciona o processo de importação de dados de terceiros](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="a81a1-127">O cliente trabalha com o parceiro escolhido para configurar um conector que extrairá itens da fonte de dados de terceiros e, em seguida, importará esses itens para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="a81a1-128">O conector de parceiro se conecta a fontes de dados de terceiros por meio de uma API de terceiros (em uma base agendada ou definida) e extrai itens da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-128">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="a81a1-129">O conector do parceiro converte o conteúdo de um item em um formato de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a81a1-129">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="a81a1-130">Consulte a seção [More information](#more-information) para obter uma descrição do esquema de formato de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a81a1-130">See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="a81a1-131">O conector de parceiro se conecta ao serviço do Azure no Office 365 usando o serviço Web do Exchange (EWS) por meio de um ponto de extremidade conhecido.</span><span class="sxs-lookup"><span data-stu-id="a81a1-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="a81a1-p105">Os itens são importados para a caixa de correio de um usuário específico ou para uma caixa de correio de dados de terceiros "pega-tudo". Os critérios a seguir definem se um item será importado para a caixa de correio de um usuário específico ou para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="a81a1-134">a.</span><span class="sxs-lookup"><span data-stu-id="a81a1-134">a.</span></span> <span data-ttu-id="a81a1-135">**Itens que têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** -se o conector de parceiro puder mapear a ID de usuário do item da fonte de dados de terceiros para uma ID de usuário específica no Office 365, o \*\*\*\* item será copiado para a pasta de limpezas no grupo de usuários pasta de itens em excesso.</span><span class="sxs-lookup"><span data-stu-id="a81a1-135">**Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="a81a1-136">Os usuários não podem acessar os itens na pasta Remoções.</span><span class="sxs-lookup"><span data-stu-id="a81a1-136">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="a81a1-137">No enTanto, você pode usar as ferramentas de descoberta eletrônica do Office 365 para pesquisar itens na pasta exPurgações.</span><span class="sxs-lookup"><span data-stu-id="a81a1-137">However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="a81a1-138">b.</span><span class="sxs-lookup"><span data-stu-id="a81a1-138">b.</span></span> <span data-ttu-id="a81a1-139">**Itens que não têm uma ID de usuário que corresponda a uma conta de usuário do Office 365** -se o conector de parceiro não puder mapear a ID de usuário de um item para uma ID de usuário específica no Office 365, o item será copiado para a pasta **caixa de entrada** da caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-139">**Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="a81a1-140">Importar itens para a caixa de entrada permite que você ou alguém em sua organização entre na caixa de correio de terceiros para exibir e gerenciar esses itens e ver se os ajustes precisam ser feitos na configuração do conector do parceiro.</span><span class="sxs-lookup"><span data-stu-id="a81a1-140">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="a81a1-141">Etapa 1: encontrar um parceiro de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="a81a1-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="a81a1-142">Um componente fundamental para o arquivamento de dados de terceiros no Office 365 está encontrando e trabalhando com um parceiro da Microsoft especializado na captura de dados de uma fonte de dados de terceiros e importando-os para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-142">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365.</span></span> <span data-ttu-id="a81a1-143">Depois que os dados são importados, eles podem ser arquivados e preservados junto com outros dados da sua organização, como email do Exchange e documentos do SharePoint e do OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="a81a1-143">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="a81a1-144">Um parceiro cria um conector que extrai dados das fontes de dados de terceiros de sua organização (como BlackBerry, Facebook, Google +, Thomson Reuters, Twitter e YouTube) e transmite esses dados para uma API do Office 365 que importa itens para caixas de correio do Exchange como mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="a81a1-144">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="a81a1-145">As seções a seguir listam os parceiros da Microsoft e as fontes de dados de terceiros que eles dão suporte, que estão participando do programa para o arquivamento de dados de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="a81a1-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="a81a1-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="a81a1-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="a81a1-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="a81a1-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="a81a1-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="a81a1-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="a81a1-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="a81a1-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="a81a1-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="a81a1-151">Verba</span><span class="sxs-lookup"><span data-stu-id="a81a1-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="a81a1-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="a81a1-152">17a-4 LLC</span></span>

<span data-ttu-id="a81a1-153">17a-4 LLC é compatível com as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="a81a1-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="a81a1-154">BlackBerry</span></span>
    
- <span data-ttu-id="a81a1-155">Fluxos de dados do Bloomberg</span><span class="sxs-lookup"><span data-stu-id="a81a1-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="a81a1-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="a81a1-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="a81a1-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="a81a1-157">FactSet</span></span>
    
- <span data-ttu-id="a81a1-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="a81a1-158">HipChat</span></span>
    
- <span data-ttu-id="a81a1-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="a81a1-159">InvestEdge</span></span>
    
- <span data-ttu-id="a81a1-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="a81a1-160">LivePerson</span></span>
    
- <span data-ttu-id="a81a1-161">MessageLabs Data Streams</span><span class="sxs-lookup"><span data-stu-id="a81a1-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="a81a1-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="a81a1-162">OpenText</span></span>
    
- <span data-ttu-id="a81a1-163">Oracle/ATG 'click-to-call' Live Help</span><span class="sxs-lookup"><span data-stu-id="a81a1-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="a81a1-164">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="a81a1-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="a81a1-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="a81a1-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="a81a1-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="a81a1-166">MindAlign</span></span>
    
- <span data-ttu-id="a81a1-167">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="a81a1-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="a81a1-168">Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="a81a1-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="a81a1-169">Skype for Business Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="a81a1-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="a81a1-170">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a81a1-170">SQL Databases</span></span>
    
- <span data-ttu-id="a81a1-171">Squawker</span><span class="sxs-lookup"><span data-stu-id="a81a1-171">Squawker</span></span>
    
- <span data-ttu-id="a81a1-172">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="a81a1-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="a81a1-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="a81a1-173">Actiance</span></span>

<span data-ttu-id="a81a1-174">O [Actiance](https://www.actiance.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="a81a1-175">META</span><span class="sxs-lookup"><span data-stu-id="a81a1-175">AIM</span></span>
    
- <span data-ttu-id="a81a1-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="a81a1-176">American Idol</span></span>
    
- <span data-ttu-id="a81a1-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="a81a1-177">Apple Juice</span></span>
    
- <span data-ttu-id="a81a1-178">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="a81a1-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="a81a1-179">Ares</span><span class="sxs-lookup"><span data-stu-id="a81a1-179">Ares</span></span>
    
- <span data-ttu-id="a81a1-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="a81a1-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="a81a1-181">Bear Share</span></span>
    
- <span data-ttu-id="a81a1-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="a81a1-182">Bit Torrent</span></span>
    
- <span data-ttu-id="a81a1-183">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-184">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-185">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-186">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-187">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="a81a1-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="a81a1-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="a81a1-188">CellTrust</span></span>
    
- <span data-ttu-id="a81a1-189">Importação de bate-papo</span><span class="sxs-lookup"><span data-stu-id="a81a1-189">Chat Import</span></span>
    
- <span data-ttu-id="a81a1-190">Política e registros de bate-papo em tempo real</span><span class="sxs-lookup"><span data-stu-id="a81a1-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="a81a1-191">Instabilidade</span><span class="sxs-lookup"><span data-stu-id="a81a1-191">Chatter</span></span>
    
- <span data-ttu-id="a81a1-192">Servidor de &amp; presença de im da Cisco (v 9.0.1, v 9.1, v 9.1.1 SU1, v10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="a81a1-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="a81a1-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="a81a1-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="a81a1-194">Importação de colaboração</span><span class="sxs-lookup"><span data-stu-id="a81a1-194">Collaboration Import</span></span>
    
- <span data-ttu-id="a81a1-195">Registro de colaboração em tempo real</span><span class="sxs-lookup"><span data-stu-id="a81a1-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="a81a1-196">Conexão Direta</span><span class="sxs-lookup"><span data-stu-id="a81a1-196">Direct Connect</span></span>
    
- <span data-ttu-id="a81a1-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="a81a1-197">Facebook</span></span>
    
- <span data-ttu-id="a81a1-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="a81a1-198">FactSet</span></span>
    
- <span data-ttu-id="a81a1-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="a81a1-199">FastTrack</span></span>
    
- <span data-ttu-id="a81a1-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="a81a1-200">Gnutella</span></span>
    
- <span data-ttu-id="a81a1-201">Google +</span><span class="sxs-lookup"><span data-stu-id="a81a1-201">Google+</span></span>
    
- <span data-ttu-id="a81a1-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="a81a1-202">GoToMyPC</span></span>
    
- <span data-ttu-id="a81a1-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="a81a1-203">Hopster</span></span>
    
- <span data-ttu-id="a81a1-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="a81a1-204">HubConnex</span></span>
    
- <span data-ttu-id="a81a1-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span><span class="sxs-lookup"><span data-stu-id="a81a1-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="a81a1-206">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="a81a1-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="a81a1-207">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="a81a1-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="a81a1-208">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="a81a1-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="a81a1-209">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="a81a1-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="a81a1-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span><span class="sxs-lookup"><span data-stu-id="a81a1-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="a81a1-211">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="a81a1-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="a81a1-212">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="a81a1-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="a81a1-213">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="a81a1-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="a81a1-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="a81a1-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="a81a1-215">Importação de mensagem Instantânea</span><span class="sxs-lookup"><span data-stu-id="a81a1-215">IM Import</span></span>
    
- <span data-ttu-id="a81a1-216">Política e registro de mensagem instantânea em tempo real</span><span class="sxs-lookup"><span data-stu-id="a81a1-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="a81a1-217">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="a81a1-217">Indii Messenger</span></span>
    
- <span data-ttu-id="a81a1-218">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="a81a1-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="a81a1-219">IRC</span><span class="sxs-lookup"><span data-stu-id="a81a1-219">IRC</span></span>
    
- <span data-ttu-id="a81a1-220">Jive</span><span class="sxs-lookup"><span data-stu-id="a81a1-220">Jive</span></span>
    
- <span data-ttu-id="a81a1-221">Jive 6 Real Time Logging (v6, v7)</span><span class="sxs-lookup"><span data-stu-id="a81a1-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="a81a1-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="a81a1-222">Jive Import</span></span>
    
- <span data-ttu-id="a81a1-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="a81a1-223">JXTA</span></span>
    
- <span data-ttu-id="a81a1-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a81a1-224">LinkedIn</span></span>
    
- <span data-ttu-id="a81a1-225">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="a81a1-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="a81a1-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="a81a1-226">MFTP</span></span>
    
- <span data-ttu-id="a81a1-227">Microsoft Lync 2013 Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="a81a1-228">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="a81a1-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="a81a1-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a81a1-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="a81a1-230">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="a81a1-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="a81a1-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="a81a1-231">MindAlign</span></span>
    
- <span data-ttu-id="a81a1-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="a81a1-232">Mobile Guard</span></span>
    
- <span data-ttu-id="a81a1-233">MSN</span><span class="sxs-lookup"><span data-stu-id="a81a1-233">MSN</span></span>
    
- <span data-ttu-id="a81a1-234">My Space</span><span class="sxs-lookup"><span data-stu-id="a81a1-234">My Space</span></span>
    
- <span data-ttu-id="a81a1-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="a81a1-235">NEONetwork</span></span>
    
- <span data-ttu-id="a81a1-236">Office 365 Lync Dedicated</span><span class="sxs-lookup"><span data-stu-id="a81a1-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="a81a1-237">Office 365 Shared IM</span><span class="sxs-lookup"><span data-stu-id="a81a1-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="a81a1-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="a81a1-238">Pinterest</span></span>
    
- <span data-ttu-id="a81a1-239">Navegação dinâmica</span><span class="sxs-lookup"><span data-stu-id="a81a1-239">Pivot</span></span>
    
- <span data-ttu-id="a81a1-240">QQ</span><span class="sxs-lookup"><span data-stu-id="a81a1-240">QQ</span></span>
    
- <span data-ttu-id="a81a1-241">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="a81a1-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="a81a1-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="a81a1-242">SoftEther</span></span>
    
- <span data-ttu-id="a81a1-243">Symphony</span><span class="sxs-lookup"><span data-stu-id="a81a1-243">Symphony</span></span>
    
- <span data-ttu-id="a81a1-244">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="a81a1-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="a81a1-245">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="a81a1-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="a81a1-246">Tor</span><span class="sxs-lookup"><span data-stu-id="a81a1-246">Tor</span></span>
    
- <span data-ttu-id="a81a1-247">TTT</span><span class="sxs-lookup"><span data-stu-id="a81a1-247">TTT</span></span>
    
- <span data-ttu-id="a81a1-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="a81a1-248">Twitter</span></span>
    
- <span data-ttu-id="a81a1-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="a81a1-249">WinMX</span></span>
    
- <span data-ttu-id="a81a1-250">Winny</span><span class="sxs-lookup"><span data-stu-id="a81a1-250">Winny</span></span>
    
- <span data-ttu-id="a81a1-251">Instant</span><span class="sxs-lookup"><span data-stu-id="a81a1-251">Yahoo</span></span>
    
- <span data-ttu-id="a81a1-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="a81a1-252">Yammer</span></span>
    
- <span data-ttu-id="a81a1-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="a81a1-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="a81a1-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="a81a1-254">ArchiveSocial</span></span>

<span data-ttu-id="a81a1-255">O [ArchiveSocial](https://www.archivesocial.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="a81a1-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="a81a1-256">Facebook</span></span>
    
- <span data-ttu-id="a81a1-257">Flickr</span><span class="sxs-lookup"><span data-stu-id="a81a1-257">Flickr</span></span>
    
- <span data-ttu-id="a81a1-258">Instagram</span><span class="sxs-lookup"><span data-stu-id="a81a1-258">Instagram</span></span>
    
- <span data-ttu-id="a81a1-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a81a1-259">LinkedIn</span></span>
    
- <span data-ttu-id="a81a1-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="a81a1-260">Pinterest</span></span>
    
- <span data-ttu-id="a81a1-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="a81a1-261">Twitter</span></span>
    
- <span data-ttu-id="a81a1-262">YouTube</span><span class="sxs-lookup"><span data-stu-id="a81a1-262">YouTube</span></span>
    
- <span data-ttu-id="a81a1-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="a81a1-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="a81a1-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="a81a1-264">Globanet</span></span>

<span data-ttu-id="a81a1-265">O [Globanet](https://www.globanet.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="a81a1-266">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="a81a1-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="a81a1-267">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-268">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-269">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-270">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="a81a1-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="a81a1-271">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="a81a1-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="a81a1-272">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="a81a1-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="a81a1-273">Caixa</span><span class="sxs-lookup"><span data-stu-id="a81a1-273">Box</span></span>
    
- <span data-ttu-id="a81a1-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="a81a1-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="a81a1-275">Servidor de &amp; presença de im da Cisco (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="a81a1-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="a81a1-276">Equipes do Cisco WebEx</span><span class="sxs-lookup"><span data-stu-id="a81a1-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="a81a1-277">Compartilhamento do &amp; Citrix Workspace</span><span class="sxs-lookup"><span data-stu-id="a81a1-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="a81a1-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="a81a1-278">CrowdCompass</span></span>

- <span data-ttu-id="a81a1-279">Arquivos de texto delimitado personalizado</span><span class="sxs-lookup"><span data-stu-id="a81a1-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="a81a1-280">Arquivos XML personalizados</span><span class="sxs-lookup"><span data-stu-id="a81a1-280">Custom XML files</span></span>
    
- <span data-ttu-id="a81a1-281">Facebook (páginas)</span><span class="sxs-lookup"><span data-stu-id="a81a1-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="a81a1-282">FactSet</span><span class="sxs-lookup"><span data-stu-id="a81a1-282">Factset</span></span>
    
- <span data-ttu-id="a81a1-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="a81a1-283">FXConnect</span></span>
    
- <span data-ttu-id="a81a1-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="a81a1-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="a81a1-285">Jive</span><span class="sxs-lookup"><span data-stu-id="a81a1-285">Jive</span></span>
    
- <span data-ttu-id="a81a1-286">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="a81a1-286">Macgregor XIP</span></span>

- <span data-ttu-id="a81a1-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="a81a1-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="a81a1-288">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a81a1-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="a81a1-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a81a1-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="a81a1-290">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="a81a1-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="a81a1-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="a81a1-291">Mobile Guard</span></span>
    
- <span data-ttu-id="a81a1-292">Navegação dinâmica</span><span class="sxs-lookup"><span data-stu-id="a81a1-292">Pivot</span></span>
    
- <span data-ttu-id="a81a1-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="a81a1-293">Salesforce Chatter</span></span>

- <span data-ttu-id="a81a1-294">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="a81a1-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="a81a1-295">Skype for Business, versões 2007 R2 - 2016 (local)</span><span class="sxs-lookup"><span data-stu-id="a81a1-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="a81a1-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="a81a1-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="a81a1-297">Symphony</span><span class="sxs-lookup"><span data-stu-id="a81a1-297">Symphony</span></span>
    
- <span data-ttu-id="a81a1-298">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="a81a1-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="a81a1-299">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="a81a1-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="a81a1-300">Thomson Reuters Dealings 3000 / FX Trading</span><span class="sxs-lookup"><span data-stu-id="a81a1-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="a81a1-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="a81a1-301">Twitter</span></span>
    
- <span data-ttu-id="a81a1-302">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="a81a1-302">UBS Chat</span></span>
    
- <span data-ttu-id="a81a1-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="a81a1-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="a81a1-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="a81a1-304">OpenText</span></span>

<span data-ttu-id="a81a1-305">A [OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="a81a1-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="a81a1-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="a81a1-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="a81a1-307">Axs Exchange</span></span>
    
- <span data-ttu-id="a81a1-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="a81a1-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="a81a1-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="a81a1-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="a81a1-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="a81a1-310">Axs Signed</span></span>
    
- <span data-ttu-id="a81a1-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="a81a1-311">Bloomberg</span></span>
    
- <span data-ttu-id="a81a1-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="a81a1-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="a81a1-313">Verba</span><span class="sxs-lookup"><span data-stu-id="a81a1-313">Verba</span></span>

<span data-ttu-id="a81a1-314">O [verba](https://www.verba.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="a81a1-315">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="a81a1-316">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="a81a1-317">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="a81a1-317">Avtec Radio</span></span>
    
- <span data-ttu-id="a81a1-318">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="a81a1-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="a81a1-319">BroadSoft Vídeo</span><span class="sxs-lookup"><span data-stu-id="a81a1-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="a81a1-320">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="a81a1-321">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-321">Centile Voice</span></span>
    
- <span data-ttu-id="a81a1-322">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="a81a1-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="a81a1-323">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="a81a1-324">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="a81a1-325">Vídeo do Cisco UCCX/UCCE</span><span class="sxs-lookup"><span data-stu-id="a81a1-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="a81a1-326">Voz do Cisco UCCX/UCCE</span><span class="sxs-lookup"><span data-stu-id="a81a1-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="a81a1-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="a81a1-327">ESChat Radio</span></span>
    
- <span data-ttu-id="a81a1-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="a81a1-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="a81a1-329">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="a81a1-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="a81a1-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="a81a1-331">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="a81a1-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="a81a1-332">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="a81a1-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="a81a1-333">Oracle / Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="a81a1-334">Oracle / Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="a81a1-335">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="a81a1-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="a81a1-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="a81a1-338">Skype for Business / Lync IM</span><span class="sxs-lookup"><span data-stu-id="a81a1-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="a81a1-339">Skype for Business / Lync Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="a81a1-340">Skype for Business / Lync Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="a81a1-341">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="a81a1-342">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="a81a1-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="a81a1-343">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="a81a1-344">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="a81a1-344">Truphone Voice</span></span>
    
- <span data-ttu-id="a81a1-345">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="a81a1-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="a81a1-346">Windows Desktop Computer Screen</span><span class="sxs-lookup"><span data-stu-id="a81a1-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="a81a1-347">Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="a81a1-348">Aqui estão as etapas para criar e configurar uma caixa de correio de dados de terceiros para importar dados para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-348">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365.</span></span> <span data-ttu-id="a81a1-349">Como explicado anteriormente, os itens são importados para esta caixa de correio se o conector de parceiro não puder mapear a ID de usuário do item para uma conta de usuário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-349">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 **<span data-ttu-id="a81a1-350">Concluir estas tarefas no centro de administração do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-350">Complete these tasks in the Microsoft 365 admin center</span></span>**
  
1. <span data-ttu-id="a81a1-351">Criar uma nova conta de usuário no Office 365 e atribuí-la a uma licença do Exchange Online Plan 2; consulte [Adicionar usuários ao Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span><span class="sxs-lookup"><span data-stu-id="a81a1-351">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="a81a1-352">Uma licença do plano 2 é necessária para colocar a caixa de correio em retenção de litígio ou habilitar uma caixa de correio de arquivo morto com uma cota de armazenamento ilimitada.</span><span class="sxs-lookup"><span data-stu-id="a81a1-352">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="a81a1-353">Adicione a conta de usuário para a caixa de correio de dados de terceiros à função de administrador de **Administradores do Exchange** no Office 365; Confira [atribuir funções de administrador no Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="a81a1-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="a81a1-354">Anote as credenciais da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="a81a1-354">Write down the credentials for this user account.</span></span> <span data-ttu-id="a81a1-355">Você precisa enviá-las para o seu parceiro, conforme descrito na Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="a81a1-355">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 **<span data-ttu-id="a81a1-356">Concluir estas tarefas no centro de administração do Exchange</span><span class="sxs-lookup"><span data-stu-id="a81a1-356">Complete these tasks in the Exchange admin center</span></span>**
  
1. <span data-ttu-id="a81a1-357">Ocultar a caixa de correio de dados de terceiros no catálogo de endereços e em outras listas de endereços em sua organização; consulte [manage user Mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span><span class="sxs-lookup"><span data-stu-id="a81a1-357">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="a81a1-358">Como alternativa, você pode executar o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a81a1-358">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="a81a1-359">Atribua a permissão **FullAccess** à caixa de correio de dados de terceiros para que administradores ou gerentes de conformidade possam abrir a caixa de correio de dados de terceiros no cliente da área de trabalho do Outlook; consulte [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="a81a1-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="a81a1-360">Habilite os seguintes recursos do Office 365 relacionados à conformidade para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="a81a1-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="a81a1-361">Habilitar a caixa de correio de arquivo morto; consulte [habilitar caixas de correio de arquivo morto](enable-archive-mailboxes.md) e [habilitar o arquivamento ilimitado](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="a81a1-361">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="a81a1-362">Isso permitirá que você libere espaço de armazenamento na caixa de correio principal Configurando uma política de arquivamento que mova itens de dados de terceiros para a caixa de correio de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="a81a1-362">This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="a81a1-363">Isso fornecerá a você um armazenamento ilimitado para dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-363">This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="a81a1-364">Colocar a caixa de correio de dados de terceiros em Retenção de Litígio.</span><span class="sxs-lookup"><span data-stu-id="a81a1-364">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="a81a1-365">Você também pode aplicar uma política de retenção do Office 365 no centro de segurança e conformidade.</span><span class="sxs-lookup"><span data-stu-id="a81a1-365">You can also apply an Office 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="a81a1-366">Colocar esta caixa de correio em retenção manterá itens de dados de terceiros (indefinidamente ou por uma duração especificada) e impedirá que eles sejam excluídos da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a81a1-366">Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="a81a1-367">Consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a81a1-367">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="a81a1-368">Colocar uma caixa de correio em Retenção de Litígio</span><span class="sxs-lookup"><span data-stu-id="a81a1-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="a81a1-369">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="a81a1-370">Para habilitar o log de auditoria da caixa de correio para acesso de proprietário, representante e administrador à caixa de correio de dados de terceiros, consulte [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="a81a1-370">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="a81a1-371">Isso permitirá que você faça a auditoria de todas as atividades realizadas por qualquer usuário que tenha acesso à caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-371">This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="a81a1-372">Etapa 3: configurar caixas de correio de usuário para dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="a81a1-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="a81a1-373">A próxima etapa é configurar as caixas de correio do usuário para oferecer suporte a dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-373">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="a81a1-374">Conclua essas tarefas usando o centro de administração do Exchange ou usando os cmdlets do Windows PowerShell correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a81a1-374">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="a81a1-375">Habilitar a caixa de correio de arquivo morto para cada usuário; consulte [habilitar caixas de correio de arquivo morto](enable-archive-mailboxes.md) e [habilitar o arquivamento ilimitado](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="a81a1-375">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="a81a1-376">Coloque as caixas de correio do usuário em retenção de litígio ou aplique uma política de retenção do Office 365; consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a81a1-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="a81a1-377">Colocar uma caixa de correio em Retenção de Litígio</span><span class="sxs-lookup"><span data-stu-id="a81a1-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="a81a1-378">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="a81a1-379">Conforme mencionado anteriormente, quando você coloca as caixas de correio em retenção, é possível definir uma duração para a retenção dos itens da fonte de dados de terceiros, ou você pode optar por reter itens indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="a81a1-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="a81a1-380">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="a81a1-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="a81a1-381">A etapa final é fornecer a seu parceiro as informações a seguir, para que ele possa configurar o conector a fim de se conectar à sua organização do Office 365 e importar dados para as caixas de correio do usuário e para a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="a81a1-382">O ponto de extremidade usado para se conectar ao serviço do Azure no Office 365:</span><span class="sxs-lookup"><span data-stu-id="a81a1-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="a81a1-383">As credenciais de entrada (ID de usuário e senha do Office 365) da caixa de correio de dados de terceiros que você criou na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="a81a1-383">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="a81a1-384">Essas credenciais são necessárias para que o conector do parceiro possa acessar e importar itens para a caixa de correio do usuário e a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-384">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="a81a1-385">Etapa 5: registrar o conector de dados de terceiros no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a81a1-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="a81a1-386">Desde 30 de setembro de 2018, o serviço do Azure no Office 365 começará a usar a autenticação moderna no Exchange Online para autenticar conectores de dados de terceiros que tentam se conectar à sua organização do Office 365 para importar dados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-386">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data.</span></span> <span data-ttu-id="a81a1-387">O motivo dessa alteração é que a autenticação moderna fornece mais segurança do que o método atual, que se baseia em conectores de terceiros em lista branca que usam o ponto de extremidade descrito anteriormente para se conectar ao serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="a81a1-387">The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="a81a1-388">Para permitir que um conector de dados de terceiros se conecte ao Office 365 usando o novo método de autenticação moderna, um administrador na sua organização do Office 365 deve se concordar em registrar o conector como um aplicativo de serviço confiável no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a81a1-388">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="a81a1-389">Isso é feito aceitando uma solicitação de permissões para permitir que o conector acesse os dados da sua organização no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a81a1-389">This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="a81a1-390">Depois que você aceita essa solicitação, o conector de dados de terceiros é adicionado como um aplicativo corporativo ao Azure Active Directory e representado como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a81a1-390">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="a81a1-391">Para obter mais informações sobre o processo de consentimento, consulte [consentimento do administrador do locatário](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="a81a1-391">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="a81a1-392">Aqui estão as etapas para acessar e aceitar a solicitação de registro do conector:</span><span class="sxs-lookup"><span data-stu-id="a81a1-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="a81a1-393">Vá até [esta página](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) e entre usando as credenciais de um administrador global do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="a81a1-394">A caixa de diálogo a seguir é exibida.</span><span class="sxs-lookup"><span data-stu-id="a81a1-394">The following dialog box is displayed.</span></span> <span data-ttu-id="a81a1-395">Você pode expandir os acentos para revisar as permissões que serão atribuídas ao conector.</span><span class="sxs-lookup"><span data-stu-id="a81a1-395">You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/>![A caixa de diálogo de solicitação de permissões é exibida](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. <span data-ttu-id="a81a1-397">Clique em **Aceitar**.</span><span class="sxs-lookup"><span data-stu-id="a81a1-397">Click **Accept**.</span></span>

<span data-ttu-id="a81a1-398">Após aceitar a solicitação, o [portal do Azure](https://portal.azure.com) é exibido.</span><span class="sxs-lookup"><span data-stu-id="a81a1-398">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="a81a1-399">Para exibir a lista de aplicativos da sua organização, clique em**aplicativos corporativos** **do Azure Active Directory** > .</span><span class="sxs-lookup"><span data-stu-id="a81a1-399">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="a81a1-400">O conector de dados de terceiros do Office 365 está listado na folha **aplicativos empresariais** .</span><span class="sxs-lookup"><span data-stu-id="a81a1-400">The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a81a1-401">Após 30 de setembro de 2018, os dados de terceiros não serão mais importados para caixas de correio em sua organização se você não registrar um conector de dados de terceiros no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a81a1-401">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="a81a1-402">Observação os conectores de dados de terceiros existentes (aqueles criados antes de 30 de setembro de 2018) também devem ser registrados no Azure Active Directory seguindo o procedimento na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="a81a1-402">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="a81a1-403">Revogar o consentimento de um conector de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="a81a1-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="a81a1-404">Depois que sua organização concorda com a solicitação de permissões para registrar um conector de dados de terceiros no Azure Active Directory, sua organização pode revogar esse consentimento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a81a1-404">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="a81a1-405">No enTanto, revogar o consentimento de um conector significa que os dados da fonte de dados de terceiros não serão mais importados para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-405">However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="a81a1-406">Para revogar o consentimento de um conector de dados de terceiros, você pode excluir o aplicativo (excluindo a entidade de serviço correspondente) do Azure Active Directory usando a lâmina **aplicativos corporativos** no portal do Azure ou usando o [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) no Office 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a81a1-406">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span></span> <span data-ttu-id="a81a1-407">Você também pode usar o cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) no PowerShell do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a81a1-407">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="a81a1-408">Mais informações</span><span class="sxs-lookup"><span data-stu-id="a81a1-408">More information</span></span>

- <span data-ttu-id="a81a1-409">Conforme explicado anteriormente, os itens de fontes de dados de terceiros são importados para caixas de correio do Exchange como mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="a81a1-409">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="a81a1-410">O conector de parceiro importa o item usando um esquema exigido pela API do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-410">The partner connector imports the item using a schema required by the Office 365 API.</span></span> <span data-ttu-id="a81a1-411">A tabela a seguir descreve as propriedades de mensagem de um item de uma fonte de dados de terceiros após importá-lo para uma caixa de correio do Exchange como uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a81a1-411">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="a81a1-412">A tabela também indica se a propriedade da mensagem é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="a81a1-412">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="a81a1-413">As propriedades obrigatórias devem ser preenchidas.</span><span class="sxs-lookup"><span data-stu-id="a81a1-413">Mandatory properties must be populated.</span></span> <span data-ttu-id="a81a1-414">Se um item não tiver uma propriedade obrigatória, ele não será importado para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-414">If an item is missing a mandatory property, it won't be imported to Office 365.</span></span> <span data-ttu-id="a81a1-415">O processo de importação retorna uma mensagem de erro explicando por que um item não foi importado e qual é a propriedade ausente.</span><span class="sxs-lookup"><span data-stu-id="a81a1-415">The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |**<span data-ttu-id="a81a1-416">Propriedade da mensagem</span><span class="sxs-lookup"><span data-stu-id="a81a1-416">Message property</span></span>**|**<span data-ttu-id="a81a1-417">Obrigatório?</span><span class="sxs-lookup"><span data-stu-id="a81a1-417">Mandatory?</span></span>**|**<span data-ttu-id="a81a1-418">Descrição</span><span class="sxs-lookup"><span data-stu-id="a81a1-418">Description</span></span>**|**<span data-ttu-id="a81a1-419">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="a81a1-419">Example value</span></span>**|
    |:-----|:-----|:-----|:-----|
    |**<span data-ttu-id="a81a1-420">FROM</span><span class="sxs-lookup"><span data-stu-id="a81a1-420">FROM</span></span>** <br/> |<span data-ttu-id="a81a1-421">Sim</span><span class="sxs-lookup"><span data-stu-id="a81a1-421">Yes</span></span>  <br/> |<span data-ttu-id="a81a1-422">O usuário que criou ou enviou originalmente o item na fonte de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-422">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="a81a1-423">O conector de parceiro tentará mapear a ID de usuário do item de origem (por exemplo, uma alça do Twitter) para uma conta de usuário do Office 365 para todos os participantes (usuários nos campos de e para).</span><span class="sxs-lookup"><span data-stu-id="a81a1-423">The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="a81a1-424">Uma cópia da mensagem será importada para a caixa de correio de cada participante.</span><span class="sxs-lookup"><span data-stu-id="a81a1-424">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="a81a1-425">Se nenhum dos participantes do item puder ser mapeado para uma conta de usuário do Office 365, o item será importado para a caixa de correio de arquivamento de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="a81a1-425">If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.</span></span>  <br/> <br/> <span data-ttu-id="a81a1-426">O participante identificado como o remetente do item deve ter uma caixa de correio ativa na organização do Office 365 à qual o item está sendo importado.</span><span class="sxs-lookup"><span data-stu-id="a81a1-426">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to.</span></span> <span data-ttu-id="a81a1-427">Se o remetente não tem uma caixa de correio ativa, o seguinte erro é retornado:</span><span class="sxs-lookup"><span data-stu-id="a81a1-427">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**<span data-ttu-id="a81a1-428">TO</span><span class="sxs-lookup"><span data-stu-id="a81a1-428">TO</span></span>** <br/> |<span data-ttu-id="a81a1-429">Sim</span><span class="sxs-lookup"><span data-stu-id="a81a1-429">Yes</span></span>  <br/> |<span data-ttu-id="a81a1-430">O usuário que recebeu um item, caso seja aplicável a um item na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |**<span data-ttu-id="a81a1-431">Assunto</span><span class="sxs-lookup"><span data-stu-id="a81a1-431">SUBJECT</span></span>** <br/> |<span data-ttu-id="a81a1-432">Não</span><span class="sxs-lookup"><span data-stu-id="a81a1-432">No</span></span>  <br/> |<span data-ttu-id="a81a1-433">O assunto do item de origem.</span><span class="sxs-lookup"><span data-stu-id="a81a1-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**<span data-ttu-id="a81a1-434">PÓS-DATADOS</span><span class="sxs-lookup"><span data-stu-id="a81a1-434">DATE</span></span>** <br/> |<span data-ttu-id="a81a1-435">Sim</span><span class="sxs-lookup"><span data-stu-id="a81a1-435">Yes</span></span>  <br/> |<span data-ttu-id="a81a1-436">A data na qual o item foi originalmente criado ou publicado na fonte de dados do cliente. Por exemplo, a data quando uma mensagem do Twitter foi enviada.</span><span class="sxs-lookup"><span data-stu-id="a81a1-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |**<span data-ttu-id="a81a1-437">ÓRGÃO</span><span class="sxs-lookup"><span data-stu-id="a81a1-437">BODY</span></span>** <br/> |<span data-ttu-id="a81a1-438">Não</span><span class="sxs-lookup"><span data-stu-id="a81a1-438">No</span></span>  <br/> |<span data-ttu-id="a81a1-439">O conteúdo da mensagem ou publicação.</span><span class="sxs-lookup"><span data-stu-id="a81a1-439">The contents of the message or post.</span></span> <span data-ttu-id="a81a1-440">Para algumas fontes de dados, o conteúdo dessa propriedade pode ser o mesmo que o conteúdo da propriedade **ASSUNTO**.</span><span class="sxs-lookup"><span data-stu-id="a81a1-440">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="a81a1-441">Durante o processo de importação, o conector parceiro tentará manter fidelidade total à fonte do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a81a1-441">During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="a81a1-442">Se for possível, arquivos, gráficos ou outros tipos de conteúdo do corpo do item de origem estarão incluídos nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="a81a1-442">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="a81a1-443">Caso contrário, o conteúdo do item de origem estará incluído na propriedade **ANEXO**.</span><span class="sxs-lookup"><span data-stu-id="a81a1-443">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="a81a1-444">O conteúdo dessa propriedade dependerá do conector de parceiro e da capacidade da plataforma de origem.</span><span class="sxs-lookup"><span data-stu-id="a81a1-444">The contents of this property will depend on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**<span data-ttu-id="a81a1-445">ANEXAR</span><span class="sxs-lookup"><span data-stu-id="a81a1-445">ATTACHMENT</span></span>** <br/> |<span data-ttu-id="a81a1-446">Não</span><span class="sxs-lookup"><span data-stu-id="a81a1-446">No</span></span>  <br/> |<span data-ttu-id="a81a1-447">Se um item na fonte de dados (como um tweet no Twitter ou uma conversa de mensagem instantânea) tiver um arquivo anexado ou incluir imagens, a conexão de parceiro tentará primeiro incluir anexos na propriedade **Body** .</span><span class="sxs-lookup"><span data-stu-id="a81a1-447">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="a81a1-448">Se isso não for possível, então será adicionado à propriedade \* \* ATTACHMENT \* \*.</span><span class="sxs-lookup"><span data-stu-id="a81a1-448">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="a81a1-449">Outros exemplos de anexos incluem Curtidas no Facebook, metadados da fonte de conteúdo e respostas a uma mensagem ou publicação.</span><span class="sxs-lookup"><span data-stu-id="a81a1-449">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |**<span data-ttu-id="a81a1-450">MESSAGECLASS</span><span class="sxs-lookup"><span data-stu-id="a81a1-450">MESSAGECLASS</span></span>** <br/> |<span data-ttu-id="a81a1-451">Sim</span><span class="sxs-lookup"><span data-stu-id="a81a1-451">Yes</span></span>  <br/> | <span data-ttu-id="a81a1-452">Esta é uma propriedade com múltiplos valores, que é criada e preenchida pelo conector parceiro.</span><span class="sxs-lookup"><span data-stu-id="a81a1-452">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="a81a1-453">O formato dessa propriedade é `IPM.NOTE.Source.Event`.</span><span class="sxs-lookup"><span data-stu-id="a81a1-453">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="a81a1-454">(Essa propriedade deve começar com `IPM.NOTE`; esse formato é semelhante ao da classe de `IPM.NOTE.X` mensagens.) Esta propriedade inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="a81a1-454">(This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/>`Source` <span data-ttu-id="a81a1-455">-Indica a fonte de dados de terceiros; por exemplo, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="a81a1-455">- Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  `Event` <span data-ttu-id="a81a1-456">– Indica o tipo de atividade que foi executado na fonte de dados de terceiros que produziu os itens; por exemplo, um tweet no Twitter ou uma postagem no Facebook.</span><span class="sxs-lookup"><span data-stu-id="a81a1-456">- Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="a81a1-457">Eventos são específicos à fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a81a1-457">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="a81a1-458">Uma finalidade dessa propriedade é filtrar itens específicos com base na fonte de dados na qual um item teve origem ou com base no tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="a81a1-458">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="a81a1-459">Por exemplo, em uma pesquisa de Descoberta Eletrônica você poderia criar uma consulta de pesquisa para encontrar todos os tweets publicados por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="a81a1-459">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="a81a1-460">Quando os itens são importados com êxito para caixas de correio no Office 365, um identificador exclusivo é retornado de volta para o chamador como parte da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a81a1-460">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="a81a1-461">Esse identificador — chamado `x-IngestionCorrelationID`— pode ser usado para fins de solução de problemas subsequentes por parceiros para o controle de ponta a ponta dos itens.</span><span class="sxs-lookup"><span data-stu-id="a81a1-461">This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="a81a1-462">É recomendável que os parceiros capturem essas informações e as registrem de acordo no lado deles.</span><span class="sxs-lookup"><span data-stu-id="a81a1-462">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="a81a1-463">Veja aqui um exemplo de uma resposta HTTP que mostra esse identificador:</span><span class="sxs-lookup"><span data-stu-id="a81a1-463">Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="a81a1-464">Você pode usar a ferramenta de pesquisa de conteúdo no centro de conformidade e segurança para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-464">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="a81a1-465">Para pesquisar especificamente esses itens importados, você pode usar os seguintes pares de propriedade de mensagem-valor na caixa palavra-chave de uma pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a81a1-465">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="a81a1-466">**`kind:externaldata`**– Use este par de propriedade/valor para pesquisar todos os tipos de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-466">**`kind:externaldata`** - Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="a81a1-467">Por exemplo, para pesquisar itens que foram importados de uma fonte de dados de terceiros e continham a palavra "contoso" na propriedade Subject do item importado, você usaria a `kind:externaldata AND subject:contoso`consulta de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="a81a1-467">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="a81a1-468">**`itemclass:ipm.externaldata.<third-party data type>`**– Use este par de propriedade-valor para pesquisar apenas um tipo de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a81a1-468">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="a81a1-469">Por exemplo, para pesquisar apenas dados do Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a consulta `itemclass:ipm.externaldata.Facebook* AND subject:contoso`de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="a81a1-469">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="a81a1-470">Para obter uma lista completa de valores a serem usados para tipos de dados de terceiros `itemclass` para a propriedade, consulte [usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="a81a1-470">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="a81a1-471">Veja mais informações sobre como usar a Pesquisa de Conteúdo e criar consultas de pesquisa de palavra-chave em:</span><span class="sxs-lookup"><span data-stu-id="a81a1-471">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="a81a1-472">Pesquisa de conteúdo no Office 365</span><span class="sxs-lookup"><span data-stu-id="a81a1-472">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="a81a1-473">Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="a81a1-473">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
