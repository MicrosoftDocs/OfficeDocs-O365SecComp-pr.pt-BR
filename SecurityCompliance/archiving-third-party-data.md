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
description: Os administradores podem importar dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos para caixas de correio em sua organização do Office 365. Isso permite que você arquive dados de Facebook, Twitter e fontes de dados no Office 365. Em seguida, você pode appply recursos de conformidade do Office 365 (como retenção legal, pesquisa de conteúdo e políticas de retenção) para dados de terceiros.
ms.openlocfilehash: 0f9f8b5a4ce5b4359430a3b15acc7bf16b2f0290
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296674"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="72c93-105">Arquivamento de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="72c93-p102">O Office 365 permite que os administradores importem e arquivem dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos, para caixas de correio em sua organização do Office 365. Exemplos de fontes de dados de terceiros que podem ser importadas para o Office 365 incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="72c93-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="72c93-108">**Social** -Twitter, Facebook, Yammer e LinkedIn</span><span class="sxs-lookup"><span data-stu-id="72c93-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="72c93-109">**Mensagens instantâneas** -Yahoo Messenger, GoogleTalk e Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="72c93-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="72c93-110">Documentar a caixa de **colaboração** e o Dropbox</span><span class="sxs-lookup"><span data-stu-id="72c93-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="72c93-111">**Setores verticais** – gerenciamento de relacionamento com clientes (como o Salesforce informativo) e Finanças (como a Thomson Reuters e Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="72c93-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="72c93-112">**SMS/mensagens de texto** -BlackBerry</span><span class="sxs-lookup"><span data-stu-id="72c93-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="72c93-p103">Após a importação dos dados de terceiros, você pode aplicar recursos de conformidade do Office 365, como retenção de litígio, pesquisa de conteúdo, arquivamento in-loco, auditoria e políticas de retenção do Office 365 — para esses dados. Por exemplo, quando uma caixa de correio é colocada em retenção de litígio, os dados de terceiros serão preservados. Você pode pesquisar dados de terceiros usando a pesquisa de conteúdo. Ou você pode aplicar políticas de arquivamento e retenção a dados de terceiros da mesma forma que você pode para os dados da Microsoft. Em suma, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.</span><span class="sxs-lookup"><span data-stu-id="72c93-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="72c93-118">Veja a seguir uma visão geral do processo e as etapas necessárias para importar dados de terceiros para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="72c93-119">Etapa 1: encontrar um parceiro de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="72c93-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="72c93-120">Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="72c93-121">Etapa 3: configurar caixas de correio de usuário para dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="72c93-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="72c93-122">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="72c93-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="72c93-123">Etapa 5: registrar o conector de dados de terceiros no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="72c93-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="72c93-124">Como funciona o processo de importação de dados de terceiros works></span><span class="sxs-lookup"><span data-stu-id="72c93-124">How the third-party data import process works></span></span>

<span data-ttu-id="72c93-125">A ilustração e a descrição a seguir explicam como funciona o processo de importação de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="72c93-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Como funciona o processo de importação de dados de terceiros](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="72c93-127">O cliente trabalha com o parceiro escolhido para configurar um conector que extrairá itens da fonte de dados de terceiros e, em seguida, importará esses itens para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="72c93-p104">O conector de parceiro se conecta a fontes de dados de terceiros por meio de uma API de terceiros (em uma base agendada ou definida) e extrai itens da fonte de dados. O conector de parceiro converte o conteúdo de um item em um formato de mensagem de email. Consulte a seção [mais informações](#more-information) para obter uma descrição do esquema de formato de mensagem.</span><span class="sxs-lookup"><span data-stu-id="72c93-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="72c93-131">O conector de parceiro se conecta ao serviço do Azure no Office 365 usando o serviço Web do Exchange (EWS) por meio de um ponto de extremidade conhecido.</span><span class="sxs-lookup"><span data-stu-id="72c93-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="72c93-p105">Os itens são importados para a caixa de correio de um usuário específico ou para uma caixa de correio de dados de terceiros "pega-tudo". Os critérios a seguir definem se um item será importado para a caixa de correio de um usuário específico ou para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="72c93-p106">a. **itens que têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** -se o conector de parceiro puder mapear a ID de usuário do item na fonte de dados de terceiros para uma ID de usuário específica no Office 365, o \*\*\*\* item será copiado para a pasta de limpezas do usuário Pasta itens recuperáveis. Os usuários não podem acessar itens na pasta exPurgations. No enTanto, você pode usar as ferramentas de descoberta eletrônica do Office 365 para pesquisar itens na pasta exPurgações.</span><span class="sxs-lookup"><span data-stu-id="72c93-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="72c93-p107">b. **itens que não têm uma ID de usuário que corresponda a uma conta de usuário do Office 365** -se o conector de parceiro não puder mapear a ID de usuário de um item para uma ID de usuário específica no Office 365, o item será copiado para a pasta **caixa de entrada** da caixa de correio de dados de terceiros. A importação de itens para a caixa de entrada permite que você ou outra pessoa em sua organização entre na caixa de correio de terceiros para exibir e gerenciar esses itens e veja se algum ajuste precisa ser feito na configuração do conector de parceiro.</span><span class="sxs-lookup"><span data-stu-id="72c93-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="72c93-141">Etapa 1: encontrar um parceiro de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="72c93-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="72c93-p108">Um componente fundamental para o arquivamento de dados de terceiros no Office 365 está encontrando e trabalhando com um parceiro da Microsoft especializado na captura de dados de uma fonte de dados de terceiros e importando-os para o Office 365. Depois que os dados são importados, eles podem ser arquivados e preservados junto com outros dados da sua organização, como email do Exchange e documentos do SharePoint e do OneDrive for Business. Um parceiro cria um conector que extrai dados das fontes de dados de terceiros de sua organização (como BlackBerry, Facebook, Google +, Thomson Reuters, Twitter e YouTube) e transmite esses dados para uma API do Office 365 que importa itens para caixas de correio do Exchange como mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="72c93-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="72c93-145">As seções a seguir listam os parceiros da Microsoft e as fontes de dados de terceiros que eles dão suporte, que estão participando do programa para o arquivamento de dados de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="72c93-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="72c93-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="72c93-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="72c93-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="72c93-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="72c93-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="72c93-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="72c93-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="72c93-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="72c93-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="72c93-151">Verba</span><span class="sxs-lookup"><span data-stu-id="72c93-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="72c93-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="72c93-152">17a-4 LLC</span></span>

<span data-ttu-id="72c93-153">17a-4 LLC é compatível com as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="72c93-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="72c93-154">BlackBerry</span></span>
    
- <span data-ttu-id="72c93-155">Fluxos de dados do Bloomberg</span><span class="sxs-lookup"><span data-stu-id="72c93-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="72c93-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="72c93-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="72c93-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="72c93-157">FactSet</span></span>
    
- <span data-ttu-id="72c93-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="72c93-158">HipChat</span></span>
    
- <span data-ttu-id="72c93-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="72c93-159">InvestEdge</span></span>
    
- <span data-ttu-id="72c93-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="72c93-160">LivePerson</span></span>
    
- <span data-ttu-id="72c93-161">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="72c93-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="72c93-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="72c93-162">OpenText</span></span>
    
- <span data-ttu-id="72c93-163">Oracle/ATG 'click-to-call' Live Help
</span><span class="sxs-lookup"><span data-stu-id="72c93-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="72c93-164">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="72c93-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="72c93-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="72c93-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="72c93-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="72c93-166">MindAlign</span></span>
    
- <span data-ttu-id="72c93-167">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="72c93-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="72c93-168">
Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="72c93-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="72c93-169">
Skype for Business Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="72c93-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="72c93-170">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="72c93-170">SQL Databases</span></span>
    
- <span data-ttu-id="72c93-171">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="72c93-171">Squawker</span></span>
    
- <span data-ttu-id="72c93-172">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="72c93-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="72c93-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="72c93-173">Actiance</span></span>

<span data-ttu-id="72c93-174">O [Actiance](https://www.actiance.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="72c93-175">OBJETIVO</span><span class="sxs-lookup"><span data-stu-id="72c93-175">AIM</span></span>
    
- <span data-ttu-id="72c93-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="72c93-176">American Idol</span></span>
    
- <span data-ttu-id="72c93-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="72c93-177">Apple Juice</span></span>
    
- <span data-ttu-id="72c93-178">
AOL with Pivot Client
</span><span class="sxs-lookup"><span data-stu-id="72c93-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="72c93-179">Ares</span><span class="sxs-lookup"><span data-stu-id="72c93-179">Ares</span></span>
    
- <span data-ttu-id="72c93-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="72c93-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="72c93-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="72c93-181">Bear Share</span></span>
    
- <span data-ttu-id="72c93-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="72c93-182">Bit Torrent</span></span>
    
- <span data-ttu-id="72c93-183">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-184">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-185">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-186">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-187">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="72c93-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="72c93-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="72c93-188">CellTrust</span></span>
    
- <span data-ttu-id="72c93-189">Importação de bate-papo
</span><span class="sxs-lookup"><span data-stu-id="72c93-189">Chat Import</span></span>
    
- <span data-ttu-id="72c93-190">Política e registros de bate-papo em tempo real
</span><span class="sxs-lookup"><span data-stu-id="72c93-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="72c93-191">Instabilidade
</span><span class="sxs-lookup"><span data-stu-id="72c93-191">Chatter</span></span>
    
- <span data-ttu-id="72c93-192">Servidor de &amp; presença de im da Cisco (v 9.0.1, v 9.1, v 9.1.1 SU1, v10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="72c93-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="72c93-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="72c93-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="72c93-194">Importação de colaboração
</span><span class="sxs-lookup"><span data-stu-id="72c93-194">Collaboration Import</span></span>
    
- <span data-ttu-id="72c93-195">Registro de colaboração em tempo real
</span><span class="sxs-lookup"><span data-stu-id="72c93-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="72c93-196">Conexão Direta</span><span class="sxs-lookup"><span data-stu-id="72c93-196">Direct Connect</span></span>
    
- <span data-ttu-id="72c93-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="72c93-197">Facebook</span></span>
    
- <span data-ttu-id="72c93-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="72c93-198">FactSet</span></span>
    
- <span data-ttu-id="72c93-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="72c93-199">FastTrack</span></span>
    
- <span data-ttu-id="72c93-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="72c93-200">Gnutella</span></span>
    
- <span data-ttu-id="72c93-201">Google+
</span><span class="sxs-lookup"><span data-stu-id="72c93-201">Google+</span></span>
    
- <span data-ttu-id="72c93-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="72c93-202">GoToMyPC</span></span>
    
- <span data-ttu-id="72c93-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="72c93-203">Hopster</span></span>
    
- <span data-ttu-id="72c93-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="72c93-204">HubConnex</span></span>
    
- <span data-ttu-id="72c93-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="72c93-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="72c93-206">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="72c93-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="72c93-207">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="72c93-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="72c93-208">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="72c93-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="72c93-209">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="72c93-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="72c93-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="72c93-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="72c93-211">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="72c93-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="72c93-212">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="72c93-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="72c93-213">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="72c93-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="72c93-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="72c93-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="72c93-215">Importação de mensagem Instantânea
</span><span class="sxs-lookup"><span data-stu-id="72c93-215">IM Import</span></span>
    
- <span data-ttu-id="72c93-216">Política e registro de mensagem instantânea em tempo real
</span><span class="sxs-lookup"><span data-stu-id="72c93-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="72c93-217">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="72c93-217">Indii Messenger</span></span>
    
- <span data-ttu-id="72c93-218">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="72c93-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="72c93-219">IRC</span><span class="sxs-lookup"><span data-stu-id="72c93-219">IRC</span></span>
    
- <span data-ttu-id="72c93-220">Jive
</span><span class="sxs-lookup"><span data-stu-id="72c93-220">Jive</span></span>
    
- <span data-ttu-id="72c93-221">Jive 6 Real Time Logging (v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="72c93-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="72c93-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="72c93-222">Jive Import</span></span>
    
- <span data-ttu-id="72c93-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="72c93-223">JXTA</span></span>
    
- <span data-ttu-id="72c93-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="72c93-224">LinkedIn</span></span>
    
- <span data-ttu-id="72c93-225">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="72c93-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="72c93-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="72c93-226">MFTP</span></span>
    
- <span data-ttu-id="72c93-227">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="72c93-228">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="72c93-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="72c93-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="72c93-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="72c93-230">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="72c93-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="72c93-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="72c93-231">MindAlign</span></span>
    
- <span data-ttu-id="72c93-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="72c93-232">Mobile Guard</span></span>
    
- <span data-ttu-id="72c93-233">MSN</span><span class="sxs-lookup"><span data-stu-id="72c93-233">MSN</span></span>
    
- <span data-ttu-id="72c93-234">My Space</span><span class="sxs-lookup"><span data-stu-id="72c93-234">My Space</span></span>
    
- <span data-ttu-id="72c93-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="72c93-235">NEONetwork</span></span>
    
- <span data-ttu-id="72c93-236">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="72c93-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="72c93-237">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="72c93-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="72c93-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="72c93-238">Pinterest</span></span>
    
- <span data-ttu-id="72c93-239">Tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="72c93-239">Pivot</span></span>
    
- <span data-ttu-id="72c93-240">QQ</span><span class="sxs-lookup"><span data-stu-id="72c93-240">QQ</span></span>
    
- <span data-ttu-id="72c93-241">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="72c93-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="72c93-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="72c93-242">SoftEther</span></span>
    
- <span data-ttu-id="72c93-243">Symphony
</span><span class="sxs-lookup"><span data-stu-id="72c93-243">Symphony</span></span>
    
- <span data-ttu-id="72c93-244">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="72c93-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="72c93-245">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="72c93-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="72c93-246">Tor</span><span class="sxs-lookup"><span data-stu-id="72c93-246">Tor</span></span>
    
- <span data-ttu-id="72c93-247">TTT</span><span class="sxs-lookup"><span data-stu-id="72c93-247">TTT</span></span>
    
- <span data-ttu-id="72c93-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="72c93-248">Twitter</span></span>
    
- <span data-ttu-id="72c93-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="72c93-249">WinMX</span></span>
    
- <span data-ttu-id="72c93-250">Winny</span><span class="sxs-lookup"><span data-stu-id="72c93-250">Winny</span></span>
    
- <span data-ttu-id="72c93-251">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="72c93-251">Yahoo</span></span>
    
- <span data-ttu-id="72c93-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="72c93-252">Yammer</span></span>
    
- <span data-ttu-id="72c93-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="72c93-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="72c93-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="72c93-254">ArchiveSocial</span></span>

<span data-ttu-id="72c93-255">O [ArchiveSocial](https://www.archivesocial.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="72c93-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="72c93-256">Facebook</span></span>
    
- <span data-ttu-id="72c93-257">Flickr
</span><span class="sxs-lookup"><span data-stu-id="72c93-257">Flickr</span></span>
    
- <span data-ttu-id="72c93-258">Instagram
</span><span class="sxs-lookup"><span data-stu-id="72c93-258">Instagram</span></span>
    
- <span data-ttu-id="72c93-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="72c93-259">LinkedIn</span></span>
    
- <span data-ttu-id="72c93-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="72c93-260">Pinterest</span></span>
    
- <span data-ttu-id="72c93-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="72c93-261">Twitter</span></span>
    
- <span data-ttu-id="72c93-262">YouTube</span><span class="sxs-lookup"><span data-stu-id="72c93-262">YouTube</span></span>
    
- <span data-ttu-id="72c93-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="72c93-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="72c93-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="72c93-264">Globanet</span></span>

<span data-ttu-id="72c93-265">O [Globanet](https://www.globanet.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="72c93-266">AOL with Pivot Client</span><span class="sxs-lookup"><span data-stu-id="72c93-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="72c93-267">BlackBerry Call Logs (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-268">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-269">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-270">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="72c93-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="72c93-271">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="72c93-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="72c93-272">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="72c93-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="72c93-273">Caixa</span><span class="sxs-lookup"><span data-stu-id="72c93-273">Box</span></span>
    
- <span data-ttu-id="72c93-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="72c93-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="72c93-275">Servidor de &amp; presença de im da Cisco (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="72c93-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="72c93-276">Equipes do Cisco WebEx</span><span class="sxs-lookup"><span data-stu-id="72c93-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="72c93-277">Compartilhamento do &amp; Citrix Workspace</span><span class="sxs-lookup"><span data-stu-id="72c93-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="72c93-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="72c93-278">CrowdCompass</span></span>

- <span data-ttu-id="72c93-279">Arquivos de texto delimitado personalizado
</span><span class="sxs-lookup"><span data-stu-id="72c93-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="72c93-280">Arquivos XML personalizados
</span><span class="sxs-lookup"><span data-stu-id="72c93-280">Custom XML files</span></span>
    
- <span data-ttu-id="72c93-281">Facebook (páginas)</span><span class="sxs-lookup"><span data-stu-id="72c93-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="72c93-282">Factset
</span><span class="sxs-lookup"><span data-stu-id="72c93-282">Factset</span></span>
    
- <span data-ttu-id="72c93-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="72c93-283">FXConnect</span></span>
    
- <span data-ttu-id="72c93-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="72c93-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="72c93-285">Jive
</span><span class="sxs-lookup"><span data-stu-id="72c93-285">Jive</span></span>
    
- <span data-ttu-id="72c93-286">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="72c93-286">Macgregor XIP</span></span>

- <span data-ttu-id="72c93-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="72c93-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="72c93-288">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="72c93-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="72c93-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="72c93-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="72c93-290">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="72c93-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="72c93-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="72c93-291">Mobile Guard</span></span>
    
- <span data-ttu-id="72c93-292">Tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="72c93-292">Pivot</span></span>
    
- <span data-ttu-id="72c93-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="72c93-293">Salesforce Chatter</span></span>

- <span data-ttu-id="72c93-294">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="72c93-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="72c93-295">Skype for Business, versões 2007 R2 - 2016 (local)
</span><span class="sxs-lookup"><span data-stu-id="72c93-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="72c93-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="72c93-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="72c93-297">Symphony
</span><span class="sxs-lookup"><span data-stu-id="72c93-297">Symphony</span></span>
    
- <span data-ttu-id="72c93-298">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="72c93-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="72c93-299">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="72c93-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="72c93-300">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="72c93-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="72c93-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="72c93-301">Twitter</span></span>
    
- <span data-ttu-id="72c93-302">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="72c93-302">UBS Chat</span></span>
    
- <span data-ttu-id="72c93-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="72c93-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="72c93-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="72c93-304">OpenText</span></span>

<span data-ttu-id="72c93-305">A [OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="72c93-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="72c93-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="72c93-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="72c93-307">Axs Exchange</span></span>
    
- <span data-ttu-id="72c93-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="72c93-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="72c93-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="72c93-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="72c93-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="72c93-310">Axs Signed</span></span>
    
- <span data-ttu-id="72c93-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="72c93-311">Bloomberg</span></span>
    
- <span data-ttu-id="72c93-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="72c93-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="72c93-313">Verba</span><span class="sxs-lookup"><span data-stu-id="72c93-313">Verba</span></span>

<span data-ttu-id="72c93-314">O [verba](https://www.verba.com) suporta as seguintes fontes de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="72c93-315">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="72c93-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="72c93-316">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="72c93-317">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="72c93-317">Avtec Radio</span></span>
    
- <span data-ttu-id="72c93-318">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="72c93-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="72c93-319">BroadSoft Vídeo
</span><span class="sxs-lookup"><span data-stu-id="72c93-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="72c93-320">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="72c93-321">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-321">Centile Voice</span></span>
    
- <span data-ttu-id="72c93-322">Cisco Jabber IM
</span><span class="sxs-lookup"><span data-stu-id="72c93-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="72c93-323">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="72c93-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="72c93-324">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="72c93-325">Vídeo do Cisco UCCX/UCCE</span><span class="sxs-lookup"><span data-stu-id="72c93-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="72c93-326">Voz do Cisco UCCX/UCCE</span><span class="sxs-lookup"><span data-stu-id="72c93-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="72c93-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="72c93-327">ESChat Radio</span></span>
    
- <span data-ttu-id="72c93-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="72c93-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="72c93-329">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="72c93-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="72c93-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="72c93-331">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="72c93-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="72c93-332">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="72c93-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="72c93-333">Oracle / Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="72c93-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="72c93-334">Oracle / Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="72c93-335">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="72c93-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="72c93-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="72c93-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="72c93-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="72c93-338">Skype for Business / Lync IM
</span><span class="sxs-lookup"><span data-stu-id="72c93-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="72c93-339">Skype for Business / Lync Video
</span><span class="sxs-lookup"><span data-stu-id="72c93-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="72c93-340">Skype for Business / Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="72c93-341">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="72c93-342">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="72c93-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="72c93-343">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="72c93-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="72c93-344">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="72c93-344">Truphone Voice</span></span>
    
- <span data-ttu-id="72c93-345">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="72c93-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="72c93-346">Windows Desktop Computer Screen 
</span><span class="sxs-lookup"><span data-stu-id="72c93-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="72c93-347">Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="72c93-p109">Aqui estão as etapas para criar e configurar uma caixa de correio de dados de terceiros para importar dados para o Office 365. Como explicado anteriormente, os itens são importados para esta caixa de correio se o conector de parceiro não puder mapear a ID de usuário do item para uma conta de usuário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="72c93-350">**Concluir estas tarefas no centro de administração do Office 365**</span><span class="sxs-lookup"><span data-stu-id="72c93-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="72c93-p110">Criar uma nova conta de usuário no Office 365 e atribuí-la a uma licença do Exchange Online Plan 2; consulte [Adicionar usuários ao Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Uma licença do plano 2 é necessária para colocar a caixa de correio em retenção de litígio ou habilitar uma caixa de correio de arquivo morto com uma cota de armazenamento ilimitada.</span><span class="sxs-lookup"><span data-stu-id="72c93-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="72c93-353">Adicione a conta de usuário para a caixa de correio de dados de terceiros à função de administrador de **Administradores do Exchange** no Office 365; Confira [atribuir funções de administrador no Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="72c93-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="72c93-p111">Anote as credenciais da conta do usuário. Você precisa enviá-las para o seu parceiro, conforme descrito na Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="72c93-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="72c93-356">**Concluir estas tarefas no centro de administração do Exchange**</span><span class="sxs-lookup"><span data-stu-id="72c93-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="72c93-p112">Ocultar a caixa de correio de dados de terceiros no catálogo de endereços e em outras listas de endereços em sua organização; consulte [manage user Mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Como alternativa, você pode executar o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="72c93-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="72c93-359">Atribua a permissão **FullAccess** à caixa de correio de dados de terceiros para que administradores ou gerentes de conformidade possam abrir a caixa de correio de dados de terceiros no cliente da área de trabalho do Outlook; consulte [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="72c93-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="72c93-360">Habilite os seguintes recursos do Office 365 relacionados à conformidade para a caixa de correio de dados de terceiros:</span><span class="sxs-lookup"><span data-stu-id="72c93-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="72c93-p113">Habilitar a caixa de correio de arquivo morto; consulte [habilitar caixas de correio de arquivo morto no centro &amp; de conformidade de segurança do Office 365](enable-archive-mailboxes.md) e [habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md). Isso permitirá que você libere espaço de armazenamento na caixa de correio principal Configurando uma política de arquivamento que mova itens de dados de terceiros para a caixa de correio de arquivo morto. Isso lhe fornecerá armazenamento ilimitado para dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="72c93-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="72c93-p114">Coloque a caixa de correio de dados de terceiros em retenção de litígio. Você também pode aplicar uma política de retenção do Office 365 no centro de &amp; conformidade de segurança do Office 365. Colocar esta caixa de correio em retenção manterá itens de dados de terceiros (indefinidamente ou por uma duração especificada) e impedirá que eles sejam excluídos da caixa de correio. Consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="72c93-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="72c93-368">Colocar uma caixa de correio em Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="72c93-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="72c93-369">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="72c93-p115">Habilitar o log de auditoria de caixa de correio para proprietário, representante e acesso de administrador à caixa de correio de dados de terceiros; consulte [habilitar a auditoria de caixa de correio no Office 365](enable-mailbox-auditing.md). Isso permitirá que você faça a auditoria de todas as atividades realizadas por qualquer usuário que tenha acesso à caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="72c93-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="72c93-372">Etapa 3: configurar caixas de correio de usuário para dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="72c93-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="72c93-p116">A próxima etapa é configurar caixas de correio de usuário para dar suporte a dados de terceiros. Conclua essas tarefas usando o centro de administração do Exchange ou usando os cmdlets do Windows PowerShell correspondentes.</span><span class="sxs-lookup"><span data-stu-id="72c93-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="72c93-375">Habilitar a caixa de correio de arquivo morto para cada usuário; consulte [habilitar caixas de correio de arquivo morto no centro &amp; de conformidade de segurança do Office 365](enable-archive-mailboxes.md) e [habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="72c93-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="72c93-376">Coloque as caixas de correio do usuário em retenção de litígio ou aplique uma política de retenção do Office 365; consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="72c93-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="72c93-377">Colocar uma caixa de correio em Retenção de litígio</span><span class="sxs-lookup"><span data-stu-id="72c93-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="72c93-378">Visão geral das políticas de retenção no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="72c93-379">Conforme mencionado anteriormente, quando você coloca as caixas de correio em retenção, é possível definir uma duração para a retenção dos itens da fonte de dados de terceiros, ou você pode optar por reter itens indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="72c93-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="72c93-380">Etapa 4: fornecer informações ao seu parceiro</span><span class="sxs-lookup"><span data-stu-id="72c93-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="72c93-381">A etapa final é fornecer a seu parceiro as informações a seguir, para que ele possa configurar o conector a fim de se conectar à sua organização do Office 365 e importar dados para as caixas de correio do usuário e para a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="72c93-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="72c93-382">O ponto de extremidade usado para se conectar ao serviço do Azure no Office 365:</span><span class="sxs-lookup"><span data-stu-id="72c93-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="72c93-p117">As credenciais de entrada (ID de usuário e senha do Office 365) da caixa de correio de dados de terceiros que você criou na etapa 2. Essas credenciais são necessárias para que o conector de parceiro possa acessar e importar itens para caixas de correio de usuário e para a caixa de correio de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="72c93-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="72c93-385">Etapa 5: registrar o conector de dados de terceiros no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="72c93-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="72c93-p118">Desde 30 de setembro de 2018, o serviço do Azure no Office 365 começará a usar a autenticação moderna no Exchange Online para autenticar conectores de dados de terceiros que tentam se conectar à sua organização do Office 365 para importar dados. O motivo dessa alteração é que a autenticação moderna fornece mais segurança do que o método atual, que se baseia em conectores de terceiros em lista branca que usam o ponto de extremidade descrito anteriormente para se conectar ao serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="72c93-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="72c93-p119">Para permitir que um conector de dados de terceiros se conecte ao Office 365 usando o novo método de autenticação moderna, um administrador na sua organização do Office 365 deve se concordar em registrar o conector como um aplicativo de serviço confiável no Azure Active Directory. Isso é feito aceitando uma solicitação de permissões para permitir que o conector acesse os dados da sua organização no Azure Active Directory. Depois que você aceita essa solicitação, o conector de dados de terceiros é adicionado como um aplicativo corporativo ao Azure Active Directory e representado como uma entidade de serviço. Para obter mais informações sobre o processo de consentimento, consulte [consentimento do administrador do locatário](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="72c93-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="72c93-392">Aqui estão as etapas para acessar e aceitar a solicitação de registro do conector:</span><span class="sxs-lookup"><span data-stu-id="72c93-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="72c93-393">Vá até [esta página](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) e entre usando as credenciais de um administrador global do Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="72c93-p120">A caixa de diálogo a seguir é exibida. Você pode expandir os acentos para revisar as permissões que serão atribuídas ao conector.</span><span class="sxs-lookup"><span data-stu-id="72c93-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="72c93-396">![A caixa de diálogo de solicitação de permissões é exibida](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="72c93-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="72c93-397">Clique em **aceitar**.</span><span class="sxs-lookup"><span data-stu-id="72c93-397">Click **Accept**.</span></span>

<span data-ttu-id="72c93-p121">Após aceitar a solicitação, o [portal do Azure](https://portal.azure.com) é exibido. Para exibir a lista de aplicativos da sua organização, clique em**aplicativos corporativos** **do Azure Active Directory** > . O conector de dados de terceiros do Office 365 está listado na folha **aplicativos empresariais** .</span><span class="sxs-lookup"><span data-stu-id="72c93-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72c93-p122">Após 30 de setembro de 2018, os dados de terceiros não serão mais importados para caixas de correio em sua organização se você não registrar um conector de dados de terceiros no Azure Active Directory. Observação os conectores de dados de terceiros existentes (aqueles criados antes de 30 de setembro de 2018) também devem ser registrados no Azure Active Directory seguindo o procedimento na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="72c93-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="72c93-403">Revogar o consentimento de um conector de dados de terceiros</span><span class="sxs-lookup"><span data-stu-id="72c93-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="72c93-p123">Depois que sua organização concorda com a solicitação de permissões para registrar um conector de dados de terceiros no Azure Active Directory, sua organização pode revogar esse consentimento a qualquer momento. No enTanto, revogar o consentimento de um conector significa que os dados da fonte de dados de terceiros não serão mais importados para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="72c93-p124">Para revogar o consentimento de um conector de dados de terceiros, você pode excluir o aplicativo (excluindo a entidade de serviço correspondente) do Azure Active Directory usando a lâmina **aplicativos corporativos** no portal do Azure ou usando o [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) no Office 365 PowerShell. Você também pode usar o cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) no PowerShell do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="72c93-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="72c93-408">Mais informações</span><span class="sxs-lookup"><span data-stu-id="72c93-408">More information</span></span>

- <span data-ttu-id="72c93-p125">Como explicado anteriormente, os itens de fontes de dados de terceiros são importados para caixas de correio do Exchange como mensagens de email. O conector de parceiro importa o item usando um esquema exigido pela API do Office 365. A tabela a seguir descreve as propriedades de mensagem de um item de uma fonte de dados de terceiros após sua importação para uma caixa de correio do Exchange como uma mensagem de email. A tabela também indica se a propriedade da mensagem é obrigatória. As propriedades obrigatórias devem ser preenchidas. Se um item não tiver uma propriedade obrigatória, ele não será importado para o Office 365. O processo de importação retornará uma mensagem de erro explicando por que um item não foi importado e qual propriedade está ausente.</span><span class="sxs-lookup"><span data-stu-id="72c93-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="72c93-416">**Propriedade da mensagem**</span><span class="sxs-lookup"><span data-stu-id="72c93-416">**Message property**</span></span>|<span data-ttu-id="72c93-417">**Alguma?**</span><span class="sxs-lookup"><span data-stu-id="72c93-417">**Mandatory?**</span></span>|<span data-ttu-id="72c93-418">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="72c93-418">**Description**</span></span>|<span data-ttu-id="72c93-419">**Valor de exemplo**</span><span class="sxs-lookup"><span data-stu-id="72c93-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="72c93-420">\*\*DE \*\*</span><span class="sxs-lookup"><span data-stu-id="72c93-420">**FROM**</span></span> <br/> |<span data-ttu-id="72c93-421">Sim</span><span class="sxs-lookup"><span data-stu-id="72c93-421">Yes</span></span>  <br/> |<span data-ttu-id="72c93-p126">O usuário que criou ou enviou originalmente o item na fonte de dados de terceiros. O conector de parceiro tentará mapear a ID de usuário do item de origem (por exemplo, uma alça do Twitter) para uma conta de usuário do Office 365 para todos os participantes (usuários nos campos de e para). Uma cópia da mensagem será importada para a caixa de correio de cada participante. Se nenhum dos participantes do item puder ser mapeado para uma conta de usuário do Office 365, o item será importado para a caixa de correio de arquivamento de terceiros no Office 365.</span><span class="sxs-lookup"><span data-stu-id="72c93-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="72c93-p127">O participante identificado como o remetente do item deve ter uma caixa de correio ativa na organização do Office 365 à qual o item está sendo importado. Se o remetente não tiver uma caixa de correio ativa, o seguinte erro será retornado:</span><span class="sxs-lookup"><span data-stu-id="72c93-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="72c93-428">**PARA**</span><span class="sxs-lookup"><span data-stu-id="72c93-428">**TO**</span></span> <br/> |<span data-ttu-id="72c93-429">Sim</span><span class="sxs-lookup"><span data-stu-id="72c93-429">Yes</span></span>  <br/> |<span data-ttu-id="72c93-430">O usuário que recebeu um item, caso seja aplicável a um item na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="72c93-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="72c93-431">**ASSUNTO**</span><span class="sxs-lookup"><span data-stu-id="72c93-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="72c93-432">Não</span><span class="sxs-lookup"><span data-stu-id="72c93-432">No</span></span>  <br/> |<span data-ttu-id="72c93-433">O assunto do item de origem.</span><span class="sxs-lookup"><span data-stu-id="72c93-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="72c93-434">**PÓS-DATADOS**</span><span class="sxs-lookup"><span data-stu-id="72c93-434">**DATE**</span></span> <br/> |<span data-ttu-id="72c93-435">Sim</span><span class="sxs-lookup"><span data-stu-id="72c93-435">Yes</span></span>  <br/> |<span data-ttu-id="72c93-436">A data na qual o item foi originalmente criado ou publicado na fonte de dados do cliente. Por exemplo, a data quando uma mensagem do Twitter foi enviada.</span><span class="sxs-lookup"><span data-stu-id="72c93-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="72c93-437">**CORPO**</span><span class="sxs-lookup"><span data-stu-id="72c93-437">**BODY**</span></span> <br/> |<span data-ttu-id="72c93-438">Não</span><span class="sxs-lookup"><span data-stu-id="72c93-438">No</span></span>  <br/> |<span data-ttu-id="72c93-p128">O conteúdo da mensagem ou postagem. Para algumas fontes de dados, o conteúdo dessa propriedade pode ser o mesmo que o conteúdo da propriedade **Subject** . Durante o processo de importação, o conector de parceiro tentará manter a fidelidade total da fonte de conteúdo possível. Se forem possíveis arquivos, elementos gráficos ou outros conteúdos do corpo do item de origem serão incluídos nessa propriedade. Caso contrário, o conteúdo do item de origem será incluído na propriedade **Attachment** . O conteúdo dessa propriedade dependerá do conector de parceiro e da capacidade da plataforma de origem.</span><span class="sxs-lookup"><span data-stu-id="72c93-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="72c93-445">**ANEXO**</span><span class="sxs-lookup"><span data-stu-id="72c93-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="72c93-446">Não</span><span class="sxs-lookup"><span data-stu-id="72c93-446">No</span></span>  <br/> |<span data-ttu-id="72c93-p129">Se um item na fonte de dados (como um tweet no Twitter ou uma conversa de mensagem instantânea) tiver um arquivo anexado ou incluir imagens, a conexão de parceiro tentará primeiro incluir anexos na propriedade **Body** . Se isso não for possível, então será adicionado à propriedade \* \* ATTACHMENT \* \*. Outros exemplos de anexos incluem curtidas no Facebook, metadados da fonte de conteúdo e respostas a uma mensagem ou postagem.</span><span class="sxs-lookup"><span data-stu-id="72c93-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="72c93-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="72c93-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="72c93-451">Sim</span><span class="sxs-lookup"><span data-stu-id="72c93-451">Yes</span></span>  <br/> | <span data-ttu-id="72c93-p130">Esta é uma propriedade de vários valores, que é criada e preenchida pelo Partner Connector. O formato dessa propriedade é `IPM.NOTE.Source.Event`. (Essa propriedade deve começar com `IPM.NOTE`; esse formato é semelhante ao da classe de `IPM.NOTE.X` mensagens.) Esta propriedade inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="72c93-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="72c93-455">`Source`-Indica a fonte de dados de terceiros; por exemplo, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="72c93-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="72c93-p131">`Event`– Indica o tipo de atividade que foi executado na fonte de dados de terceiros que produziu os itens; por exemplo, um tweet no Twitter ou uma postagem no Facebook. Os eventos são específicos da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="72c93-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="72c93-p132">Uma finalidade dessa propriedade é filtrar itens específicos com base na fonte de dados onde um item foi originado ou com base no tipo de evento. Por exemplo, em uma pesquisa de descoberta eletrônica, você pode criar uma consulta de pesquisa para localizar todos os tweets postados por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="72c93-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="72c93-p133">Quando os itens são importados com êxito para caixas de correio no Office 365, um identificador exclusivo é retornado de volta para o chamador como parte da resposta HTTP. Esse identificador — chamado `x-IngestionCorrelationID`— pode ser usado para fins de solução de problemas subsequentes por parceiros para o controle de ponta a ponta dos itens. É recomendável que os parceiros capturem essas informações e as registrem de acordo com suas finalidades. Veja um exemplo de uma resposta HTTP que mostra esse identificador:</span><span class="sxs-lookup"><span data-stu-id="72c93-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="72c93-p134">Você pode usar a ferramenta de pesquisa de conteúdo no centro de &amp; conformidade de segurança do Office 365 para pesquisar itens que foram importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Para pesquisar especificamente esses itens importados, você pode usar os seguintes pares de propriedade de mensagem-valor na caixa palavra-chave de uma pesquisa de conteúdo. .</span><span class="sxs-lookup"><span data-stu-id="72c93-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="72c93-p135">**`kind:externaldata`**– Use este par de propriedade/valor para pesquisar todos os tipos de dados de terceiros. Por exemplo, para pesquisar itens que foram importados de uma fonte de dados de terceiros e continham a palavra "contoso" na propriedade Subject do item importado, você usaria a `kind:externaldata AND subject:contoso`consulta de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="72c93-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="72c93-p136">**`itemclass:ipm.externaldata.<third-party data type>`**– Use este par de propriedade-valor para pesquisar apenas um tipo de dados de terceiros. Por exemplo, para pesquisar apenas dados do Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a consulta `itemclass:ipm.externaldata.Facebook* AND subject:contoso`de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="72c93-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="72c93-471">Para obter uma lista completa de valores a serem usados para tipos de dados de terceiros `itemclass` para a propriedade, consulte [usar a pesquisa de conteúdo para pesquisar dados de terceiros que foram importados para o Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="72c93-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="72c93-472">Veja mais informações sobre como usar a Pesquisa de Conteúdo e criar consultas de pesquisa de palavra-chave em:</span><span class="sxs-lookup"><span data-stu-id="72c93-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="72c93-473">Pesquisa de conteúdo no Office 365</span><span class="sxs-lookup"><span data-stu-id="72c93-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="72c93-474">Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="72c93-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
