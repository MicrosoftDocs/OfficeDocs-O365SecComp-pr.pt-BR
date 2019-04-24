---
title: Analisar dados em um conjunto de trabalho em descoberta eletrônica avançada (visualização)
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
ms.openlocfilehash: e3f3e863423fe4312a944eb6f04a58182e11665c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243232"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="9af3b-102">Analisar dados em um conjunto de trabalho em descoberta eletrônica avançada (visualização)</span><span class="sxs-lookup"><span data-stu-id="9af3b-102">Analyze data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="9af3b-103">Quando o número de documentos coletados é grande, pode ser muito difícil examiná-los.</span><span class="sxs-lookup"><span data-stu-id="9af3b-103">When the number of collected documents is large, it can be quite difficult to review them all.</span></span> <span data-ttu-id="9af3b-104">A descoberta eletrônica avançada (prévia) fornece várias ferramentas para analisar os documentos para reduzir o volume de documentos a serem revisados sem perda de informações e para ajudá-lo a organizar os documentos de forma coerente.</span><span class="sxs-lookup"><span data-stu-id="9af3b-104">Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="9af3b-105">Para saber mais sobre esses recursos, confira:</span><span class="sxs-lookup"><span data-stu-id="9af3b-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="9af3b-106">Detecção de duplicata próxima</span><span class="sxs-lookup"><span data-stu-id="9af3b-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="9af3b-107">Conversa de email</span><span class="sxs-lookup"><span data-stu-id="9af3b-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="9af3b-108">Temas</span><span class="sxs-lookup"><span data-stu-id="9af3b-108">Themes</span></span>](themes.md)

<span data-ttu-id="9af3b-109">Para analisar dados em um conjunto de trabalho:</span><span class="sxs-lookup"><span data-stu-id="9af3b-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="9af3b-110">Defina as configurações de análise para o seu caso.</span><span class="sxs-lookup"><span data-stu-id="9af3b-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="9af3b-111">Para obter mais informações, consulte [Configurar definições de pesquisa e análise](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9af3b-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="9af3b-112">Abra o conjunto de trabalho que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="9af3b-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="9af3b-113">Vá para "gerenciar conjunto de trabalho".</span><span class="sxs-lookup"><span data-stu-id="9af3b-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="9af3b-114">Clique em "analisar".</span><span class="sxs-lookup"><span data-stu-id="9af3b-114">Click "Analyze".</span></span>

<span data-ttu-id="9af3b-115">Você pode verificar o progresso da análise na guia trabalhos em seu caso.</span><span class="sxs-lookup"><span data-stu-id="9af3b-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="9af3b-116">Após a conclusão da análise, você pode exibir o relatório de análise, executar consultas em seu conjunto de trabalho nas saídas da análise (para obter mais informações, confira [consulta em seu conjunto de trabalho](working-set-search.md)) e ver documentos relacionados de um determinado documento (para obter mais informações, consulte [ Revisão de dados no conjunto de trabalho](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="9af3b-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="9af3b-117">Relatório de análise</span><span class="sxs-lookup"><span data-stu-id="9af3b-117">Analytics report</span></span>

<span data-ttu-id="9af3b-118">Para exibir um relatório de análise para seu conjunto de trabalho:</span><span class="sxs-lookup"><span data-stu-id="9af3b-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="9af3b-119">Abra seu conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9af3b-119">Open your working set.</span></span>
2. <span data-ttu-id="9af3b-120">Vá para "gerenciar conjunto de trabalho".</span><span class="sxs-lookup"><span data-stu-id="9af3b-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="9af3b-121">Clique em "relatório".</span><span class="sxs-lookup"><span data-stu-id="9af3b-121">Click "Report".</span></span>

<span data-ttu-id="9af3b-122">O relatório tem quatro componentes da análise:</span><span class="sxs-lookup"><span data-stu-id="9af3b-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="9af3b-123">**Divisão** -quantos emails, anexos e documentos soltos foram encontrados no conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9af3b-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="9af3b-124">**Documentos (exceto anexos)** : Quantos documentos soltos foram dinâmicos, únicos duplicatas próximas de uma tabela dinâmica ou uma duplicata exata de outro documento.</span><span class="sxs-lookup"><span data-stu-id="9af3b-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="9af3b-125">**Emails** -quantos emails foram incluídos, cópias inclusivas, inclusive minuses ou nenhuma das opções acima.</span><span class="sxs-lookup"><span data-stu-id="9af3b-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="9af3b-126">**Attachments** -quantos anexos de email foram exclusivos ou duplicados de um anexo de email diferente no conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9af3b-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>