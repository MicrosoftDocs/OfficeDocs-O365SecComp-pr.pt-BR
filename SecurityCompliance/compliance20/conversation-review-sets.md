---
title: Analisar conversas na descoberta eletrônica avançada
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 62f0dc9e32e89954b2838b70757d3a7c17d79cc4
ms.sourcegitcommit: 6302a43d947a908dd10a8e40550b806f491692fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2019
ms.locfileid: "35672948"
---
# <a name="review-conversations-in-advanced-ediscovery"></a><span data-ttu-id="2cd89-102">Analisar conversas na descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="2cd89-102">Review conversations in Advanced eDiscovery</span></span> 

<span data-ttu-id="2cd89-103">O sistema de mensagens instantâneas é uma maneira conveniente de fazer perguntas, compartilhar ideias ou se comunicar rapidamente entre grandes audiências.</span><span class="sxs-lookup"><span data-stu-id="2cd89-103">Instant messaging is a convenient way to ask questions, share ideas, or quickly communicate across large audiences.</span></span> <span data-ttu-id="2cd89-104">Como as plataformas de mensagens instantâneas, como o Microsoft Teams, se tornarem essenciais para a colaboração corporativa, as organizações devem avaliar como o fluxo de trabalho de descoberta eletrônica resolve essas novas formas de comunicação e colaboração.</span><span class="sxs-lookup"><span data-stu-id="2cd89-104">As instant messaging platforms, like Microsoft Teams, become core to enterprise collaboration, organizations must evaluate how their eDiscovery workflow addresses these new forms of communication and collaboration.</span></span> 

<span data-ttu-id="2cd89-105">O recurso de reconstrução de conversa na descoberta eletrônica avançada foi projetado para ajudá-lo a identificar o conteúdo contextual e produzir modos de exibição de conversa distintos.</span><span class="sxs-lookup"><span data-stu-id="2cd89-105">The Conversation Reconstruction feature in Advanced eDiscovery is designed to help you identify contextual content and produce distinct conversation views.</span></span> <span data-ttu-id="2cd89-106">Esse recurso permite que você examine de forma eficiente e rápida as conversas de mensagens instantâneas completas (também chamadas de *conversações encadeadas*) geradas em plataformas como o Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2cd89-106">This capability allows you to efficiently and rapidly review complete instant message conversations (also called *threaded conversations*) that are generated in platforms like Microsoft Teams.</span></span>

<span data-ttu-id="2cd89-107">Com a reconstrução de conversas, você pode usar recursos internos para reconstruir, revisar e exportar conversas encadeadas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-107">With Conversation Reconstruction, you can use built-in capabilities to reconstruct, review, and export threaded conversations.</span></span> <span data-ttu-id="2cd89-108">Use a reconstrução de conversa de descoberta eletrônica avançada para:</span><span class="sxs-lookup"><span data-stu-id="2cd89-108">Use Advanced eDiscovery Conversation Reconstruction to:</span></span>

- <span data-ttu-id="2cd89-109">Preservar metadados únicos em nível de mensagem em todas as mensagens de uma conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-109">Preserve unique message-level metadata across all messages within a conversation.</span></span>

- <span data-ttu-id="2cd89-110">Coletar mensagens contextuais em torno dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-110">Collect contextual messages around your search results.</span></span>

- <span data-ttu-id="2cd89-111">Revisar, anotar e redigir conversas encadeadas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-111">Review, annotate, and redact threaded conversations.</span></span>

- <span data-ttu-id="2cd89-112">Exportar mensagens individuais ou conversas encadeadas</span><span class="sxs-lookup"><span data-stu-id="2cd89-112">Export individual messages or threaded conversations</span></span>

## <a name="terminology"></a><span data-ttu-id="2cd89-113">Terminologia</span><span class="sxs-lookup"><span data-stu-id="2cd89-113">Terminology</span></span>

<span data-ttu-id="2cd89-114">Aqui estão algumas definições para ajudá-lo a começar a usar a reconstrução de conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-114">Here are few definitions to help you get start using Conversation Reconstruction.</span></span>

- <span data-ttu-id="2cd89-115">**Mensagens:** Representa a menor unidade de uma conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-115">**Messages:** Represent the smallest unit of a conversation.</span></span> <span data-ttu-id="2cd89-116">As mensagens podem variar de tamanho, estrutura e metadados.</span><span class="sxs-lookup"><span data-stu-id="2cd89-116">Messages may vary in size, structure, and metadata.</span></span> 

- <span data-ttu-id="2cd89-117">**Conversa:** Representa um agrupamento de uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="2cd89-117">**Conversation:** Represents a grouping of one or more messages.</span></span> <span data-ttu-id="2cd89-118">Em diferentes aplicativos, as conversas podem ser representadas de diferentes maneiras.</span><span class="sxs-lookup"><span data-stu-id="2cd89-118">Across different applications, conversations may be represented in different ways.</span></span> <span data-ttu-id="2cd89-119">Em alguns aplicativos, há uma ação explícita que resulta da resposta a uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="2cd89-119">In some applications, there is an explicit action that results from replying to an existing message.</span></span> <span data-ttu-id="2cd89-120">As conversas são formadas explicitamente como resultado dessa ação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2cd89-120">Conversations are formed explicitly as a result of this user action.</span></span> <span data-ttu-id="2cd89-121">Por exemplo, aqui está uma captura de tela de uma conversa de canal no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2cd89-121">For example, here is a screenshot of a channel conversation in Microsoft Teams.</span></span>

   ![Conversa de canal do Microsoft Teams](../media/threadedchat.png)

   <span data-ttu-id="2cd89-123">Em outros aplicativos (como mensagens de chat do 1xN no Microsoft Teams), não há uma cadeia de resposta formal e, em vez disso, as mensagens aparecem como "Rio simples de mensagens" em um único thread.</span><span class="sxs-lookup"><span data-stu-id="2cd89-123">In other apps (such as 1xN chat messages in Teams), there is not a formal reply chain and instead messages appear as a "flat river of messages" within a single thread.</span></span> <span data-ttu-id="2cd89-124">Nesses tipos de aplicativos, as conversas são inferidas de um grupo de mensagens que ocorrem dentro de um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="2cd89-124">In these types apps, conversations are inferred from a group of messages that occur within a certain time.</span></span> <span data-ttu-id="2cd89-125">Esse "Agrupamento de mensagens" (em vez de uma cadeia de resposta) representa a conversa "frente e para trás" sobre um tópico específico de interesse.</span><span class="sxs-lookup"><span data-stu-id="2cd89-125">This "soft-grouping" of messages (as opposed to a reply chain) represent the "back and forth" conversation about a specific topic of interest.</span></span> 

## <a name="step-1-run-a-search"></a><span data-ttu-id="2cd89-126">Etapa 1: executar uma pesquisa</span><span class="sxs-lookup"><span data-stu-id="2cd89-126">Step 1: Run a search</span></span>

<span data-ttu-id="2cd89-127">Após identificar os responsáveis e locais de conteúdo relevantes, você poderá criar uma pesquisa para localizar conteúdo potencialmente relevante.</span><span class="sxs-lookup"><span data-stu-id="2cd89-127">After you have identified relevant custodians and content locations, you can create a search to find potentially relevant content.</span></span> <span data-ttu-id="2cd89-128">Na guia **pesquisas** da caixa de descoberta eletrônica avançada, você pode criar uma pesquisa clicando em **nova pesquisa** e seguindo o assistente.</span><span class="sxs-lookup"><span data-stu-id="2cd89-128">On the **Searches** tab in the Advanced eDiscovery case, you can create a search by clicking **New search** and following the wizard.</span></span> <span data-ttu-id="2cd89-129">Para obter informações sobre como você pode criar uma pesquisa, criar uma consulta de pesquisa e exibir os resultados da pesquisa, consulte [coletar dados por um caso](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="2cd89-129">For information about how you can create a search, build a search query, and view the search results, see [Collect data for a case](create-search-to-collect-data.md).</span></span>

## <a name="step-2-create-a-conversation-review-set"></a><span data-ttu-id="2cd89-130">Etapa 2: criar um conjunto de revisão de conversa</span><span class="sxs-lookup"><span data-stu-id="2cd89-130">Step 2: Create a conversation review set</span></span>

<span data-ttu-id="2cd89-131">Em um conjunto de revisão, você pode pesquisar, marcar, anotar e redigir documentos, mensagens de email e conversas de chat.</span><span class="sxs-lookup"><span data-stu-id="2cd89-131">In a review set, you can search, tag, annotate, and redact documents, email messages, and chat conversations.</span></span> <span data-ttu-id="2cd89-132">Na descoberta eletrônica avançada, você pode personalizar a revisão de conversas, com base em mensagens individuais ou conversas encadeadas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-132">In Advanced eDiscovery, you can customize your review of conversations, based in individual messages or threaded conversations.</span></span> <span data-ttu-id="2cd89-133">Isso é determinado pelo tipo de conjunto de revisão que você adiciona os resultados da pesquisa criada na etapa 1 para.</span><span class="sxs-lookup"><span data-stu-id="2cd89-133">This is determined by the type of review set that you add the results of the search created in Step 1 to.</span></span> <span data-ttu-id="2cd89-134">Há dois tipos diferentes de conjuntos de revisão:</span><span class="sxs-lookup"><span data-stu-id="2cd89-134">There are two different types of review sets:</span></span> 
  
  - <span data-ttu-id="2cd89-135">**Conjuntos de revisão padrão:** As mensagens em conversas são processadas e exibidas como itens individuais.</span><span class="sxs-lookup"><span data-stu-id="2cd89-135">**Standard review sets:** Messages in conversations are processed and displayed as individual items.</span></span> 
  
  -  <span data-ttu-id="2cd89-136">**Conjuntos de revisão de conversa:** As mensagens em conversas são processadas individualmente, mas exibidas em um modo de exibição de conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-136">**Conversation review sets:** Messages in conversations are processed individually but displayed in a conversation view.</span></span> <span data-ttu-id="2cd89-137">Em um conjunto de revisão de conversa, você pode anotar, marcar e redigir mensagens em um modo de exibição de conversa encadeado.</span><span class="sxs-lookup"><span data-stu-id="2cd89-137">In a conversation review set, you can annotate, tag, and redact messages in a threaded conversation view.</span></span> 

<span data-ttu-id="2cd89-138">Para obter mais informações sobre como revisar e gerenciar o conteúdo em um conjunto de revisão, consulte [Manage Review sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="2cd89-138">For more information about how to review and manage content in a review set, see [Manage review sets](managing-review-sets.md).</span></span> 

## <a name="step-3-enable-conversation-retrieval-options"></a><span data-ttu-id="2cd89-139">Etapa 3: habilitar as opções de recuperação de conversa</span><span class="sxs-lookup"><span data-stu-id="2cd89-139">Step 3: Enable conversation retrieval options</span></span>

<span data-ttu-id="2cd89-140">Depois de revisar e finalizar a consulta de pesquisa, você pode adicionar os resultados da pesquisa a um conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-140">After you have reviewed and finalized your search query, you can add the search results to a review set.</span></span> <span data-ttu-id="2cd89-141">Quando você adiciona os resultados da pesquisa em um conjunto de revisão, os dados originais são copiados para uma área de armazenamento do Azure para facilitar o processo de revisão e análise.</span><span class="sxs-lookup"><span data-stu-id="2cd89-141">When you add your search results into a review set, the original data is copied to an Azure Storage area to facilitate the review and analysis process.</span></span> <span data-ttu-id="2cd89-142">Para obter mais informações sobre como adicionar resultados de pesquisa a um conjunto de revisão, consulte [Add Search Results to a Review Set](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="2cd89-142">For more information about adding search results to a review set, see [Add search results to a review set](add-data-to-review-set.md).</span></span> 

<span data-ttu-id="2cd89-143">Ao adicionar dados de conversas a um conjunto de revisão, você pode usar as opções de recuperação de conversa para expandir sua pesquisa e incluir mensagens contextuais.</span><span class="sxs-lookup"><span data-stu-id="2cd89-143">When you add data from conversations to a review set, you can use the conversation retrieval options to expand your search and include contextual messages.</span></span> <span data-ttu-id="2cd89-144">Após definir as opções de recuperação de conversa, as seguintes coisas podem ocorrer:</span><span class="sxs-lookup"><span data-stu-id="2cd89-144">After you set the conversation retrieval options, the following things can happen:</span></span>

  ![Recuperação de conversa](../media/messagesandconversations.png)
  
1. <span data-ttu-id="2cd89-146">Usando uma consulta de intervalo de datas e palavras-chave, a pesquisa retornou uma ocorrência na *mensagem 3*.</span><span class="sxs-lookup"><span data-stu-id="2cd89-146">Using a keyword and date range query, the search returned a hit on *Message 3*.</span></span> <span data-ttu-id="2cd89-147">Esta mensagem faz parte de uma conversa maior, ilustrada por *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="2cd89-147">This message was part of a larger conversation, illustrated by *CRC1*.</span></span> 
  
2. <span data-ttu-id="2cd89-148">Quando você adiciona os dados em um conjunto de revisão e habilita as opções de recuperação de conversa, a descoberta eletrônica avançada volta e coleta outros itens no *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="2cd89-148">When you add the data into a review set and enable the conversation retrieval options, Advanced eDiscovery will go back and collect other items in *CRC1*.</span></span> 
  
3. <span data-ttu-id="2cd89-149">Depois que os itens tiverem sido adicionados ao conjunto de revisão, você poderá revisar todas as mensagens individuais do *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="2cd89-149">After the items have been added to the review set, you can review all the individual messages from *CRC1*.</span></span> 



<span data-ttu-id="2cd89-150">Para habilitar a recuperação de conversas:</span><span class="sxs-lookup"><span data-stu-id="2cd89-150">To enable conversation retrieval:</span></span>
  
1. <span data-ttu-id="2cd89-151">Na guia **pesquisas** da caixa de descoberta eletrônica avançada, selecione uma pesquisa e, em seguida, clique em **Adicionar a revisão definida** na página do menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="2cd89-151">On the **Searches** tab in the Advanced eDiscovery case, select a search, and then click **Add to review set** on the flyout page.</span></span>
  
2. <span data-ttu-id="2cd89-152">Selecione um conjunto de revisão existente ou crie um conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-152">Select an existing review set or create a review set.</span></span> <span data-ttu-id="2cd89-153">Você pode configurar opções de recuperação ao adicionar resultados de pesquisa a um conjunto de análise de conversa padrão ou padrão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-153">You can configure retrieval options when adding search results to a standard or a conversation review set.</span></span>
  
3. <span data-ttu-id="2cd89-154">Configure as opções de recuperação de conversa para as fontes de conteúdo que você gostaria de expandir em sua pesquisa e, em seguida, clique em **Adicionar** para iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="2cd89-154">Configure the conversation retrieval options for the content sources that you would like to expand in your search, and then click **Add** to start the process.</span></span>  
  
4. <span data-ttu-id="2cd89-155">Após a conclusão do trabalho de **adição à revisão** do trabalho na guia **trabalhos** , você poderá começar a revisar as conversas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-155">After the **Add to review set** job on the **Jobs** tab has finished, you can start reviewing the conversations.</span></span>

## <a name="step-4-review-conversations-in-the-review-set"></a><span data-ttu-id="2cd89-156">Etapa 4: examinar as conversas no conjunto de revisão</span><span class="sxs-lookup"><span data-stu-id="2cd89-156">Step 4: Review conversations in the review set</span></span>

<span data-ttu-id="2cd89-157">Após o conteúdo ter sido processado e adicionado ao conjunto de revisão, você pode começar a revisar os dados no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-157">After the content has been processed and added to the review set, you can start reviewing the data in the review set.</span></span> <span data-ttu-id="2cd89-158">Os recursos de revisão são diferentes dependendo se o conteúdo foi adicionado a um conjunto de revisão padrão ou um conjunto de revisão de conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-158">The review capabilities are different depending on whether the content was added to a standard review set or a conversation review set.</span></span> 

### <a name="reviewing-conversations-in-a-standard-review-set"></a><span data-ttu-id="2cd89-159">Revisando conversas em um conjunto de análise padrão</span><span class="sxs-lookup"><span data-stu-id="2cd89-159">Reviewing conversations in a standard review Set</span></span>

<span data-ttu-id="2cd89-160">Em um conjunto de revisão padrão, as mensagens são processadas e exibidas como itens individuais, semelhante à forma como estão armazenadas em uma pasta de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2cd89-160">In a standard review set, messages are processed and displayed as individual items, similar to how they're stored in a mailbox folder.</span></span> <span data-ttu-id="2cd89-161">Neste fluxo de trabalho, cada mensagem é processada como um item separado.</span><span class="sxs-lookup"><span data-stu-id="2cd89-161">In this workflow, each message is processed as a separate item.</span></span> <span data-ttu-id="2cd89-162">Como resultado, o resumo segmentado e as opções de exportação não estão disponíveis em um conjunto de análise padrão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-162">As a result, the threaded summary and export options aren't available in a standard review set.</span></span> 

### <a name="reviewing-conversations-in-a-conversation-review-set"></a><span data-ttu-id="2cd89-163">Analisar conversas em um conjunto de revisão de conversa</span><span class="sxs-lookup"><span data-stu-id="2cd89-163">Reviewing conversations in a conversation review set</span></span>

<span data-ttu-id="2cd89-164">Em um conjunto de revisão de conversa, as mensagens individuais são encadeadas e apresentadas como conversas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-164">In a conversation review set, individual messages are threaded together and presented as conversations.</span></span> <span data-ttu-id="2cd89-165">Isso permite que você revise e exporte conversas contextuais.</span><span class="sxs-lookup"><span data-stu-id="2cd89-165">This lets you review and export contextual conversations.</span></span> <span data-ttu-id="2cd89-166">As seções a seguir descrevem a revisão e exportação de conversas em um conjunto de análise de conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-166">The following sections describe reviewing and exporting conversations in a conversation review set.</span></span>

#### <a name="reviewing-conversations"></a><span data-ttu-id="2cd89-167">Revisando conversas</span><span class="sxs-lookup"><span data-stu-id="2cd89-167">Reviewing conversations</span></span>

<span data-ttu-id="2cd89-168">Em um conjunto de revisão de conversa, você pode usar as seguintes opções para facilitar o processo de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-168">In a conversation review set, you can use the following options to facilitate the review process.</span></span>

- <span data-ttu-id="2cd89-169">**Agrupar por conversa:** Agrupa as mensagens dentro da mesma conversa para ajudar os usuários a simplificar e agilizar o processo de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-169">**Group by conversation:** Groups messages within the same conversation together to help users simplify and expedite their review process.</span></span> 

- <span data-ttu-id="2cd89-170">**Exibição de Resumo:** Exibe a conversa encadeada.</span><span class="sxs-lookup"><span data-stu-id="2cd89-170">**Summary view:** Displays the threaded conversation.</span></span> <span data-ttu-id="2cd89-171">Nesse modo de exibição, você pode ver toda a conversa e também acessar os metadados de cada mensagem individual.</span><span class="sxs-lookup"><span data-stu-id="2cd89-171">In this view, you can see the entire conversation and also access the metadata for each individual message.</span></span>  
  
   - <span data-ttu-id="2cd89-172">Exibir metadados para mensagens individuais</span><span class="sxs-lookup"><span data-stu-id="2cd89-172">View metadata for individual messages</span></span>
   
   - <span data-ttu-id="2cd89-173">Baixar mensagens individuais</span><span class="sxs-lookup"><span data-stu-id="2cd89-173">Download individual messages</span></span>

- <span data-ttu-id="2cd89-174">**Exibição de texto:** Fornece o texto extraído da conversa inteira.</span><span class="sxs-lookup"><span data-stu-id="2cd89-174">**Text view:** Provides the extracted text for the entire conversation.</span></span> 

- <span data-ttu-id="2cd89-175">**Modo de anotações:** Permite marcar um modo de exibição segmentado da conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-175">**Annotate view:** Lets you markup a threaded view of the conversation.</span></span> <span data-ttu-id="2cd89-176">Todas as mensagens na conversa compartilham o mesmo documento anotado.</span><span class="sxs-lookup"><span data-stu-id="2cd89-176">All messages in the conversation share the same annotated document.</span></span>

- <span data-ttu-id="2cd89-177">**Marca:** Ao exibir conversas em um conjunto de revisão, você pode exibir e aplicar marcas clicando no **painel de codificação**.</span><span class="sxs-lookup"><span data-stu-id="2cd89-177">**Tag:** When viewing conversations in a review set, you can view and apply tags by clicking the **Coding panel**.</span></span>

- <span data-ttu-id="2cd89-178">**Executar a conversão de conversa novamente:** Quando as mensagens são adicionadas a um conjunto de revisão de conversa, um trabalho de conversão é executado automaticamente para criar os modos de exibição de resumo e anotações encadeados.</span><span class="sxs-lookup"><span data-stu-id="2cd89-178">**Rerun conversation conversion:** When messages are added to a conversation review set, a conversion job is automatically run to create the threaded summary and annotate views.</span></span> <span data-ttu-id="2cd89-179">Se o trabalho de reconstrução da conversa falhar, você poderá executar novamente o trabalho de conversão clicando em **ação > criar PDFs de conversa** no conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-179">If the Conversation Reconstruction job fails, you can rerun the conversion job by clicking **Action > Create conversation PDFs** in the review set.</span></span>


#### <a name="exporting-conversations"></a><span data-ttu-id="2cd89-180">Exportando conversas</span><span class="sxs-lookup"><span data-stu-id="2cd89-180">Exporting conversations</span></span>

<span data-ttu-id="2cd89-181">Em um conjunto de revisão de conversa, você pode definir as seguintes opções para exportar conversas:</span><span class="sxs-lookup"><span data-stu-id="2cd89-181">In a conversation review set, you can set the following options to export conversations:</span></span>

![Exportar](../media/export.png)

<span data-ttu-id="2cd89-183">a.</span><span class="sxs-lookup"><span data-stu-id="2cd89-183">a.</span></span> <span data-ttu-id="2cd89-184">Opções de metadados</span><span class="sxs-lookup"><span data-stu-id="2cd89-184">Metadata options</span></span>

   - <span data-ttu-id="2cd89-185">**Carregar arquivo:** Os metadados são incluídos para cada mensagem, email e documento individual.</span><span class="sxs-lookup"><span data-stu-id="2cd89-185">**Load file:** Metadata is included for each individual message, email, and document.</span></span> <span data-ttu-id="2cd89-186">Há uma linha para cada mensagem em uma conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-186">There is one row for each message in a conversation.</span></span> 

   - <span data-ttu-id="2cd89-187">**Marcas:** As marcas do processo de revisão são incluídas no arquivo de metadados.</span><span class="sxs-lookup"><span data-stu-id="2cd89-187">**Tags:** Tags from your review process are included in the metadata file.</span></span> <span data-ttu-id="2cd89-188">As mensagens em uma conversa compartilham as mesmas marcas.</span><span class="sxs-lookup"><span data-stu-id="2cd89-188">Messages in a conversation share the same tags.</span></span> 

<span data-ttu-id="2cd89-189">b.</span><span class="sxs-lookup"><span data-stu-id="2cd89-189">b.</span></span> <span data-ttu-id="2cd89-190">Opções de conversa</span><span class="sxs-lookup"><span data-stu-id="2cd89-190">Conversation options</span></span>
  
   - <span data-ttu-id="2cd89-191">**Arquivos de conversa:** Quando você exporta arquivos de conversa, o modo de exibição anotado é convertido em um arquivo PDF e baixado para a pasta de exportação.</span><span class="sxs-lookup"><span data-stu-id="2cd89-191">**Conversation files:** When you export conversation files, the annotated view is converted to a PDF file and downloaded to the export folder.</span></span> <span data-ttu-id="2cd89-192">As mensagens em um arquivo de conversa apontam para a versão do PDF do mesmo arquivo de conversa.</span><span class="sxs-lookup"><span data-stu-id="2cd89-192">Messages in one conversation file point to the PDF version of the same conversation file.</span></span>  
  
   - <span data-ttu-id="2cd89-193">**Mensagens de chat individuais:** Quando você exporta mensagens individuais, cada mensagem exclusiva na conversa é exportada como um item autônomo.</span><span class="sxs-lookup"><span data-stu-id="2cd89-193">**Individual chat messages:** When you export individual messages, each unique message in the conversation is exported as a standalone item.</span></span> <span data-ttu-id="2cd89-194">O arquivo é exportado no mesmo formato em que foi salvo na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2cd89-194">The file is exported in the same format that it was saved as in the mailbox.</span></span> <span data-ttu-id="2cd89-195">Para uma conversa específica, você recebe vários arquivos. msg.</span><span class="sxs-lookup"><span data-stu-id="2cd89-195">For a specific conversation, you receive multiple .msg files.</span></span> 

     >[!NOTE]
     > <span data-ttu-id="2cd89-196">Se você aplicou anotações ao arquivo de conversa, essas anotações não serão transferidas para as mensagens individuais.</span><span class="sxs-lookup"><span data-stu-id="2cd89-196">If you applied annotations to the conversation file, these annotations won't be transferred to the individual messages.</span></span> 

<span data-ttu-id="2cd89-197">c.</span><span class="sxs-lookup"><span data-stu-id="2cd89-197">c.</span></span> <span data-ttu-id="2cd89-198">Outras opções</span><span class="sxs-lookup"><span data-stu-id="2cd89-198">Other options</span></span>

   - <span data-ttu-id="2cd89-199">**Gerar arquivos de texto para todo o conteúdo exportado:** Gera um arquivo de texto para cada conversa exportada do conjunto de revisão.</span><span class="sxs-lookup"><span data-stu-id="2cd89-199">**Generate text files for all exported content:** Generates a text file for each conversation exported from the review set.</span></span> 

   - <span data-ttu-id="2cd89-200">**Substitua o conteúdo exportado por PDFs redigidos:** Se os arquivos de conversa redigidos forem gerados durante o processo de revisão, esses arquivos estarão disponíveis durante a exportação.</span><span class="sxs-lookup"><span data-stu-id="2cd89-200">**Replace exported content with redacted PDFs:** If redacted conversation files are generated during the review process, then these files are available during export.</span></span> <span data-ttu-id="2cd89-201">Você pode decidir se deseja exportar somente os arquivos nativos (sem selecionar essa opção) ou substituir os arquivos nativos pelas versões redigidas dos arquivos nativos (selecionando essa opção), que são exportadas como arquivos PDF.</span><span class="sxs-lookup"><span data-stu-id="2cd89-201">You can decided whether to export only the native files (by not selecting this option) or to replace the native files with the redacted versions of the native files (by selecting this option), which are exported as PDF files.</span></span>

## <a name="more-information"></a><span data-ttu-id="2cd89-202">Mais informações</span><span class="sxs-lookup"><span data-stu-id="2cd89-202">More information</span></span>

<span data-ttu-id="2cd89-203">Para saber mais sobre como revisar os dados do caso na descoberta eletrônica avançada, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="2cd89-203">To learn more about how to review case data in Advanced eDiscovery, see the following articles:</span></span>

- [<span data-ttu-id="2cd89-204">Exibir dados de caso</span><span class="sxs-lookup"><span data-stu-id="2cd89-204">View case data</span></span>](view-documents-in-review-set.md) 

- [<span data-ttu-id="2cd89-205">Analisar dados de ocorrências</span><span class="sxs-lookup"><span data-stu-id="2cd89-205">Analyze case data</span></span>](analyzing-data-in-review-set.md)

- [<span data-ttu-id="2cd89-206">Exportar dados de ocorrência</span><span class="sxs-lookup"><span data-stu-id="2cd89-206">Export case data</span></span>](exporting-data-ediscover20.md)
