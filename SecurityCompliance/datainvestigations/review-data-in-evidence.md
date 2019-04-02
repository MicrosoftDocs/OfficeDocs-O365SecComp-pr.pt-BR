---
title: Analisar dados em evidência
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31029844"
---
# <a name="review-data-in-evidence"></a><span data-ttu-id="38f4b-102">Analisar dados em evidência</span><span class="sxs-lookup"><span data-stu-id="38f4b-102">Review data in evidence</span></span>

<span data-ttu-id="38f4b-103">**Evidence** é um instantâneo dos resultados de pesquisa coletados.</span><span class="sxs-lookup"><span data-stu-id="38f4b-103">**Evidence** is a snapshot of search results that you collected.</span></span> <span data-ttu-id="38f4b-104">Quando você adiciona resultados de pesquisa a evidências, um processo é disparado para extrair arquivos, metadados e texto.</span><span class="sxs-lookup"><span data-stu-id="38f4b-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text.</span></span> <span data-ttu-id="38f4b-105">Em seguida, o sistema cria um novo índice de todos os dados e adiciona à **evidência**.</span><span class="sxs-lookup"><span data-stu-id="38f4b-105">Then, the system builds a new index of all the data and adds to **Evidence**.</span></span> 

<span data-ttu-id="38f4b-106">Para qualquer incidentes que confiram tempo, isso permite que você contenha rapidamente o ambiente, excluindo dados em locais originais ao investigar evidências recriadas em um ambiente em quarentena.</span><span class="sxs-lookup"><span data-stu-id="38f4b-106">For any time-sensitive incidents, this allows you to quickly contain the environment by deleting data at original locations while investigating re-created evidence in a quarantined environment.</span></span> <span data-ttu-id="38f4b-107">Depois que a evidência é coletada, você pode revisar documentos individuais em seu formato nativo, formato de texto ou um formato Near-Native.</span><span class="sxs-lookup"><span data-stu-id="38f4b-107">Once evidence is collected, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="38f4b-108">Além disso, você pode executar consultas para restringir os dados por intervalo de tempo, tipos de arquivo, proprietários de dados e muitas outras placas de condição.</span><span class="sxs-lookup"><span data-stu-id="38f4b-108">Additionally, you can run queries to narrow the data by time range, file types, data owners, and many other condition cards.</span></span> <span data-ttu-id="38f4b-109">Usando cartões de criação/remetente/destinatário, você pode examinar rapidamente quem está envolvido no despejo e se houve qualquer compartilhamento externo.</span><span class="sxs-lookup"><span data-stu-id="38f4b-109">Using Author/Sender/Recipient condition cards, you can quickly examine who are involved in the spill and if there have been any external shares.</span></span> <span data-ttu-id="38f4b-110">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="38f4b-110">For more information, see:</span></span>

  - [<span data-ttu-id="38f4b-111">Consultar os dados em evidência</span><span class="sxs-lookup"><span data-stu-id="38f4b-111">Query the data in evidence</span></span>](evidence-query.md)

<span data-ttu-id="38f4b-112">Para agrupar documentos e obter mais assistência para revisão, clique em **gerenciar evidência**.</span><span class="sxs-lookup"><span data-stu-id="38f4b-112">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="38f4b-113">No bloco de **análise** , clique em **analisar**.</span><span class="sxs-lookup"><span data-stu-id="38f4b-113">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="38f4b-114">Isso executará análises avançadas, como detecção de duplicidades, encadeamento de emails e análise de tema.</span><span class="sxs-lookup"><span data-stu-id="38f4b-114">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="38f4b-115">Posteriormente, você pode ver os temas gerais dos dados e também organizar documentos por threads de email, duplicatas exatas e quase duplicatas para facilitar sua investigação.</span><span class="sxs-lookup"><span data-stu-id="38f4b-115">Afterwards, you can see the general themes of the data and also organize documents by email threads, exact duplicates and near duplicates to facilitate your investigation.</span></span> <span data-ttu-id="38f4b-116">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="38f4b-116">For more information, see:</span></span>

  - [<span data-ttu-id="38f4b-117">Executar a análise para investigar mais rápido</span><span class="sxs-lookup"><span data-stu-id="38f4b-117">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a><span data-ttu-id="38f4b-118">Exibir documentos em evidência</span><span class="sxs-lookup"><span data-stu-id="38f4b-118">View documents in evidence</span></span>

<span data-ttu-id="38f4b-119">A investigação de dados (visualização) exibe o conteúdo através de vários visualizadores, cada um com finalidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="38f4b-119">Data investigation (Preview) displays content via several viewers each with different purposes.</span></span> <span data-ttu-id="38f4b-120">Os vários visualizadores podem ser usados clicando em qualquer documento em **evidência**.</span><span class="sxs-lookup"><span data-stu-id="38f4b-120">The various viewers can be used by clicking on any document in **Evidence**.</span></span> <span data-ttu-id="38f4b-121">Os visualizadores atualmente fornecidos são:</span><span class="sxs-lookup"><span data-stu-id="38f4b-121">The viewers currently provided are:</span></span>

- <span data-ttu-id="38f4b-122">Metadados de arquivo</span><span class="sxs-lookup"><span data-stu-id="38f4b-122">File metadata</span></span>
- <span data-ttu-id="38f4b-123">Modo de exibição nativo</span><span class="sxs-lookup"><span data-stu-id="38f4b-123">Native view</span></span>
- <span data-ttu-id="38f4b-124">Exibição de texto</span><span class="sxs-lookup"><span data-stu-id="38f4b-124">Text view</span></span>
- <span data-ttu-id="38f4b-125">Modo de anotações</span><span class="sxs-lookup"><span data-stu-id="38f4b-125">Annotate view</span></span>
- <span data-ttu-id="38f4b-126">Exibição conVertida</span><span class="sxs-lookup"><span data-stu-id="38f4b-126">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="38f4b-127">Metadados de arquivo</span><span class="sxs-lookup"><span data-stu-id="38f4b-127">File metadata</span></span>

<span data-ttu-id="38f4b-128">Este painel pode ser ativado/desativado para exibir vários metadados associados ao documento.</span><span class="sxs-lookup"><span data-stu-id="38f4b-128">This panel can be toggled on/off to display various metadata associated with the document.</span></span> <span data-ttu-id="38f4b-129">Embora a grade de resultados de pesquisa possa ser personalizada para exibir metadados específicos, há situações nas quais rolar horizontalmente pode ser difícil durante a análise de dados.</span><span class="sxs-lookup"><span data-stu-id="38f4b-129">Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data.</span></span> <span data-ttu-id="38f4b-130">O painel metadados de arquivo permite que um usuário alterne em um modo de exibição no visualizador.</span><span class="sxs-lookup"><span data-stu-id="38f4b-130">The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="38f4b-131">Painel metadados de arquivo</span><span class="sxs-lookup"><span data-stu-id="38f4b-131">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="38f4b-132">Modo de exibição nativo</span><span class="sxs-lookup"><span data-stu-id="38f4b-132">Native view</span></span>

<span data-ttu-id="38f4b-133">O visualizador nativo exibe o modo de exibição mais avançado de um documento.</span><span class="sxs-lookup"><span data-stu-id="38f4b-133">The Native viewer displays the richest view of a document.</span></span> <span data-ttu-id="38f4b-134">Ele oferece suporte a centenas de tipos de arquivo e deve exibir a experiência nativa mais verdadeira possível.</span><span class="sxs-lookup"><span data-stu-id="38f4b-134">It supports hundreds of file types and is meant to display the truest to native experience possible.</span></span> <span data-ttu-id="38f4b-135">Para arquivos do Microsoft Office, por exemplo, o visualizador aproveita o Office Online para exibir conteúdo como comentários de documento, fórmulas do Excel, linhas/colunas ocultas, anotações do PowerPoint, etc. Para obter mais informações sobre os visualizadores do Office Online \[, visite aqui é necessário vincular\]</span><span class="sxs-lookup"><span data-stu-id="38f4b-135">For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="38f4b-136">Modo de exibição nativo</span><span class="sxs-lookup"><span data-stu-id="38f4b-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="38f4b-137">Exibição de texto</span><span class="sxs-lookup"><span data-stu-id="38f4b-137">Text view</span></span>

<span data-ttu-id="38f4b-138">O Visualizador de texto fornece um modo de exibição do texto extraído de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="38f4b-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="38f4b-139">Ele ignora todas as imagens e formatação inseridas, mas será um modo de exibição de alto desempenho se um usuário estiver tentando entender o conteúdo rapidamente.</span><span class="sxs-lookup"><span data-stu-id="38f4b-139">It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly.</span></span> <span data-ttu-id="38f4b-140">O modo de exibição de texto também inclui outros recursos:</span><span class="sxs-lookup"><span data-stu-id="38f4b-140">Text view also includes other features:</span></span>

  - <span data-ttu-id="38f4b-141">O contador de linhas facilita a referência a partes específicas de um documento</span><span class="sxs-lookup"><span data-stu-id="38f4b-141">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="38f4b-142">Realce de visitas de pesquisa que realçará os termos no documento, bem como o ScrollBar</span><span class="sxs-lookup"><span data-stu-id="38f4b-142">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="38f4b-143">O modo de exibição de comparação fornece um modo de exibição de comparação que realça diferenças textuais ao exibir documentos próximos duplicados</span><span class="sxs-lookup"><span data-stu-id="38f4b-143">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="38f4b-144">Exibição de texto</span><span class="sxs-lookup"><span data-stu-id="38f4b-144">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="38f4b-145">Exibição de comparação</span><span class="sxs-lookup"><span data-stu-id="38f4b-145">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="38f4b-146">Modo de anotações</span><span class="sxs-lookup"><span data-stu-id="38f4b-146">Annotate view</span></span>

<span data-ttu-id="38f4b-147">O modo de anotações fornece recursos que permitem que os usuários apliquem marcações em um documento durante a investigação, incluindo:</span><span class="sxs-lookup"><span data-stu-id="38f4b-147">The Annotate view provides features that allow users to apply markup on a document during investigation including:</span></span>

  - <span data-ttu-id="38f4b-148">Redação de área – os usuários podem desenhar uma caixa no documento para ocultar conteúdo confidencial</span><span class="sxs-lookup"><span data-stu-id="38f4b-148">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="38f4b-149">Lápis – os usuários podem fazer o desenho de forma livre em um documento para dar atenção a certas partes de um documento</span><span class="sxs-lookup"><span data-stu-id="38f4b-149">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="38f4b-150">Selecionar anotações-os usuários podem selecionar anotações em um documento para excluir</span><span class="sxs-lookup"><span data-stu-id="38f4b-150">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="38f4b-151">Alternar transparência da anotação – torna as anotações semitransparentes para exibir o conteúdo por trás da anotação</span><span class="sxs-lookup"><span data-stu-id="38f4b-151">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="38f4b-152">Página anterior – navega para a página anterior</span><span class="sxs-lookup"><span data-stu-id="38f4b-152">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="38f4b-153">Próxima página – navega para a próxima página</span><span class="sxs-lookup"><span data-stu-id="38f4b-153">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="38f4b-154">Ir para página – o usuário pode inserir um número de página específico para navegar até</span><span class="sxs-lookup"><span data-stu-id="38f4b-154">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="38f4b-155">Zoom – definir o nível de zoom para o modo de anotações</span><span class="sxs-lookup"><span data-stu-id="38f4b-155">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="38f4b-156">Girar – o usuário pode girar o documento no sentido horário</span><span class="sxs-lookup"><span data-stu-id="38f4b-156">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="38f4b-157">Pesquisa: o usuário pode pesquisar dentro de um documento e navegar até os vários acertos no documento</span><span class="sxs-lookup"><span data-stu-id="38f4b-157">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="38f4b-158">Modo de anotações</span><span class="sxs-lookup"><span data-stu-id="38f4b-158">Annotate view</span></span>
    ](../media/Reviewimage1.png)

<span data-ttu-id="38f4b-159">Observe que essas anotações estão nos dados coletados como evidência, e não em seu local original no sistema ativo.</span><span class="sxs-lookup"><span data-stu-id="38f4b-159">Note that these annotations are on data collected as evidence, not at its original location in live system.</span></span> 

## <a name="more-information"></a><span data-ttu-id="38f4b-160">Mais informações</span><span class="sxs-lookup"><span data-stu-id="38f4b-160">More information</span></span>

<span data-ttu-id="38f4b-161">A tabela a seguir lista os limites para evidências em investigações de dados (prévia).</span><span class="sxs-lookup"><span data-stu-id="38f4b-161">The following table lists the limits for evidence in Data Investigations (Preview).</span></span>  <span data-ttu-id="38f4b-162">Todos os itens que excederem os máximos de arquivo serão exibidos como erros de processamento.</span><span class="sxs-lookup"><span data-stu-id="38f4b-162">Any items that exceed the single file maximums will show up as processing errors.</span></span>
    
  |<span data-ttu-id="38f4b-163">**Descrição do limite**</span><span class="sxs-lookup"><span data-stu-id="38f4b-163">**Description of limit**</span></span>|<span data-ttu-id="38f4b-164">**Limite**</span><span class="sxs-lookup"><span data-stu-id="38f4b-164">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="38f4b-165">Número máximo de coletas de evidências</span><span class="sxs-lookup"><span data-stu-id="38f4b-165">Maximum number of evidence collections</span></span>  <br/> |<span data-ttu-id="38f4b-166">50</span><span class="sxs-lookup"><span data-stu-id="38f4b-166">50</span></span>  <br/> |
  |<span data-ttu-id="38f4b-167">Número total de documentos que podem ser incluídos em um caso (para todas as coleções de evidências na investigação)</span><span class="sxs-lookup"><span data-stu-id="38f4b-167">Total number of documents that can be ingested into a case (for all evidence collections in the investigation)</span></span>  <br/> |<span data-ttu-id="38f4b-168">1 milhão</span><span class="sxs-lookup"><span data-stu-id="38f4b-168">1 million</span></span>  <br/> |
  |<span data-ttu-id="38f4b-169">Tamanho total do arquivo por carga</span><span class="sxs-lookup"><span data-stu-id="38f4b-169">Total file size per load</span></span>  <br/> |<span data-ttu-id="38f4b-170">100 GB</span><span class="sxs-lookup"><span data-stu-id="38f4b-170">100 GB</span></span>  <br/> |
  |<span data-ttu-id="38f4b-171">Tamanho máximo de um único arquivo</span><span class="sxs-lookup"><span data-stu-id="38f4b-171">Maximum size of single file</span></span>   <br/> |<span data-ttu-id="38f4b-172">100 MB</span><span class="sxs-lookup"><span data-stu-id="38f4b-172">100 MB</span></span>  <br/> |
  |<span data-ttu-id="38f4b-173">Número máximo de caracteres extraídos de um único arquivo</span><span class="sxs-lookup"><span data-stu-id="38f4b-173">Maximum number of characters extracted from a single file</span></span>  <br/> |<span data-ttu-id="38f4b-174">10 milhões</span><span class="sxs-lookup"><span data-stu-id="38f4b-174">10 million</span></span>  <br/> |
  |<span data-ttu-id="38f4b-175">Profundidade de itens incorporados em um documento</span><span class="sxs-lookup"><span data-stu-id="38f4b-175">Depth of embedded items in a document</span></span>  <br/> |<span data-ttu-id="38f4b-176">25</span><span class="sxs-lookup"><span data-stu-id="38f4b-176">25</span></span>  <br/> |
  