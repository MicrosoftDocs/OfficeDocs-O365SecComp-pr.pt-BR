---
title: Adicionar os resultados da pesquisa a um conjunto de trabalho
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
ms.openlocfilehash: 7830b483190a69e6055fae369580064c5df42f49
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243374"
---
# <a name="add-search-results-to-a-working-set"></a><span data-ttu-id="274e1-102">Adicionar os resultados da pesquisa a um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="274e1-102">Add search results to a working set</span></span>

<span data-ttu-id="274e1-103">Depois de identificar e reinstalado as pesquisas em relação ao Exchange, SharePoint e OneDrive for Business, você pode adicionar os resultados a um conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="274e1-103">After you've identified and culled with searches against Exchange, SharePoint and OneDrive for business, you can add the results to a working set.</span></span> <span data-ttu-id="274e1-104">Os conjuntos de trabalho representam um conjunto estático de documentos que iremos indexar os resultados de pesquisa rápida do Lightning, analisar a identificação de thread de email, a detecção de duplicidades e temas próximos.</span><span class="sxs-lookup"><span data-stu-id="274e1-104">Working sets represent a static set of documents that we will index for lightning fast search results, analyze for email thread identification, near duplicate detection and themes.</span></span>  <span data-ttu-id="274e1-105">Você também pode adicionar dados de fontes de dados que não sejam do Office 365 ao vivo lado a lado com os dados coletados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="274e1-105">You can also add data from Non-Office 365 data sources to live side by side with the data you collect from Office 365.</span></span>

<span data-ttu-id="274e1-106">Para adicionar dados a um conjunto de trabalho, comece selecionando uma pesquisa, nos resultados da pesquisa sair, clique no botão *+ Adicionar resultados ao conjunto de trabalho* .</span><span class="sxs-lookup"><span data-stu-id="274e1-106">To add data to a working set, start by selecting a search, in the search results fly out, click the *+ Add results to working set* button.</span></span>

![Adicionando dados a um conjunto de trabalho](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

<span data-ttu-id="274e1-108">Você pode optar por adicionar a um conjunto de trabalho existente ou a um *novo conjunto de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="274e1-108">You can then choose to add to an existing working set or a *New working set*.</span></span>  <span data-ttu-id="274e1-109">Se estiver adicionando a um novo conjunto de trabalho, especifique o nome e finalmente clique no botão *Adicionar* .</span><span class="sxs-lookup"><span data-stu-id="274e1-109">If adding to a new working set, specify the name and finally click the *Add* button.</span></span>

![Selecionar um conjunto de trabalho](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

<span data-ttu-id="274e1-111">A adição de dados a um conjunto de trabalho é um processo de execução demorada, você pode controlar o progresso na guia trabalhos ou na coluna *status do conjunto de trabalho* na guia *pesquisas* .  O processo inclui a coleta de itens do Office 365 e, por fim, a indexação do & de inGestão.</span><span class="sxs-lookup"><span data-stu-id="274e1-111">Adding data to a working set is a long running process, you can either track the progress in the Jobs tab or in the *Working set status* column in the *Searches* tab.  The process includes gathering items from Office 365 and finally Ingestion & Indexing.</span></span>  <span data-ttu-id="274e1-112">Depois que o processamento do conjunto de trabalho for concluído, você poderá navegar até o conjunto de trabalho clicando na guia *conjuntos de trabalho* e, em seguida, clicando no conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="274e1-112">Once working set processing is completed, you can navigate to the working set by clicking on the *Working Sets* tab and then clicking on the working set.</span></span>  <span data-ttu-id="274e1-113">Você pode prosseguir para a pesquisa, revisão, marcação e exportação de quaisquer dados relevantes.</span><span class="sxs-lookup"><span data-stu-id="274e1-113">You can then move on to searching, reviewing, tagging and exporting any relevant data.</span></span>

## <a name="adding-a-sample-to-a-working-set"></a><span data-ttu-id="274e1-114">Adicionar um exemplo a um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="274e1-114">Adding a sample to a working set</span></span>

<span data-ttu-id="274e1-115">Se quiser validar seus resultados de pesquisa mais thorougly antes de coletar todos os documentos que foram recuperados por sua pesquisa, você pode adicionar uma amostra aleatória dos resultados da pesquisa a um conjunto de trabalho, em vez de adicionar tudo.</span><span class="sxs-lookup"><span data-stu-id="274e1-115">If you would like to validate your search results more thorougly before collecting all documents that were retrieved by your search, you can add a random sample of the search results to a working set instead of adding everything.</span></span>

<span data-ttu-id="274e1-116">Para adicionar um exemplo a um conjunto de trabalho, comece selecionando uma pesquisa, no submenu de resultados da pesquisa, clique em *exemplo* de botão.</span><span class="sxs-lookup"><span data-stu-id="274e1-116">To add a sample to a working set, start by selecting a search, in the search results flyout, click *Sample* button.</span></span>

<span data-ttu-id="274e1-117">Em seguida, você pode escolher o parâmetro de sua amostra.</span><span class="sxs-lookup"><span data-stu-id="274e1-117">You can then choose the parameter of your sampling.</span></span> <span data-ttu-id="274e1-118">Há duas opções:</span><span class="sxs-lookup"><span data-stu-id="274e1-118">There are two options:</span></span>
- <span data-ttu-id="274e1-119">Nível de confiança e intervalo: o tamanho da amostra será escolhido para atender aos parâmetros estatísticos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="274e1-119">Confidence level and interval: sample size will be chosen to satisfy the given statistical parameters.</span></span>
- <span data-ttu-id="274e1-120">Porcentagem: o tamanho da amostra será determinado com base no número de itens retornados pela pesquisa e no parâmetro escolhido.</span><span class="sxs-lookup"><span data-stu-id="274e1-120">Percentage: sample size will be determined based on the number of items that was returned by the search, and the chosen parameter.</span></span>

<span data-ttu-id="274e1-121">Por fim, escolha o conjunto de trabalho para o qual adicionar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="274e1-121">Finally, choose the working set to add the sample to.</span></span> <span data-ttu-id="274e1-122">A partir daí, você pode verificar o status do processo exatamente como faria para adicionar uma pesquisa inteira em um conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="274e1-122">From there, you can check the status of the process just as you would for adding a whole search into a working set.</span></span> 