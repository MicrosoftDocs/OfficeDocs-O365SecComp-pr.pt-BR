---
title: Análise de dados em um conjunto de trabalho no eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a6284204fd709bcf936688f36f38f6b3283b1f98
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607309"
---
# <a name="analyzing-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="e3ffd-102">Análise de dados em um conjunto de trabalho no eDiscovery avançado (Preview)</span><span class="sxs-lookup"><span data-stu-id="e3ffd-102">Analyzing data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="e3ffd-p101">Quando o número de documentos coletados for muito grande, pode ser muito difícil revisar todas elas. EDiscovery avançado (Preview) fornece várias ferramentas para analisar os documentos para reduzir o volume de documentos seja revisada sem que ocorra perda em informações e para ajudá-lo a organizar os documentos de maneira coerente. Para saber mais sobre esses recursos, consulte:</span><span class="sxs-lookup"><span data-stu-id="e3ffd-p101">When the number of collected documents is large, it can be quite difficult to review them all. Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner. To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="e3ffd-106">Perto de detecção de duplicatas</span><span class="sxs-lookup"><span data-stu-id="e3ffd-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="e3ffd-107">Email threading</span><span class="sxs-lookup"><span data-stu-id="e3ffd-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="e3ffd-108">Temas</span><span class="sxs-lookup"><span data-stu-id="e3ffd-108">Themes</span></span>](themes.md)

<span data-ttu-id="e3ffd-109">Para analisar os dados em um conjunto de trabalho:</span><span class="sxs-lookup"><span data-stu-id="e3ffd-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="e3ffd-p102">Defina configurações de análise para seu caso. Para obter mais informações, consulte [Configurar definições de pesquisa e análise](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e3ffd-p102">Configure analytics settings for your case. For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="e3ffd-112">Abra o conjunto de trabalho que deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="e3ffd-113">Vá para "Gerenciar o conjunto de trabalho".</span><span class="sxs-lookup"><span data-stu-id="e3ffd-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="e3ffd-114">Clique em "Analisar".</span><span class="sxs-lookup"><span data-stu-id="e3ffd-114">Click "Analyze".</span></span>

<span data-ttu-id="e3ffd-115">Você pode verificar o andamento da análise na guia trabalhos no seu caso.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="e3ffd-116">Depois que a análise for concluída, você pode exibir o relatório de análise, executar consultas em seu trabalho definir em saídas da análise (para obter mais informações, consulte [consulta dentro de seu trabalho definido](working-set-search.md)) e ver os documentos relacionados de um certo documento (para mais informações, consulte [ Analisando dados no conjunto de trabalho](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="e3ffd-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="e3ffd-117">Relatório de análise</span><span class="sxs-lookup"><span data-stu-id="e3ffd-117">Analytics report</span></span>

<span data-ttu-id="e3ffd-118">Para exibir um relatório de análise para seu conjunto de trabalho:</span><span class="sxs-lookup"><span data-stu-id="e3ffd-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="e3ffd-119">Abra o conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-119">Open your working set.</span></span>
2. <span data-ttu-id="e3ffd-120">Vá para "Gerenciar o conjunto de trabalho".</span><span class="sxs-lookup"><span data-stu-id="e3ffd-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="e3ffd-121">Clique em "Relatório".</span><span class="sxs-lookup"><span data-stu-id="e3ffd-121">Click "Report".</span></span>

<span data-ttu-id="e3ffd-122">O relatório tem quatro componentes de análise:</span><span class="sxs-lookup"><span data-stu-id="e3ffd-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="e3ffd-123">**Divisão** - quantos emails, anexos e afastados documentos foram encontrados no conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="e3ffd-124">**Documentos (excluindo anexos)** - quantos documentos afastados foram dinamização, exclusiva próximo duplicatas de uma tabela dinâmica ou uma duplicata exata de outro documento.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="e3ffd-125">**Emails** - quantos emails foram inclusives, inclusive cópias, inclusive desvantagens ou nenhuma das perguntas acima.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="e3ffd-126">**Anexos** - quantos anexos de email foram exclusivos ou duplica de um anexo de email diferentes dentro do conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3ffd-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>