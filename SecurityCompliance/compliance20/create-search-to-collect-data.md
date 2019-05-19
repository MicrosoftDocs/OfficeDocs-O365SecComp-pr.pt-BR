---
title: Criar uma pesquisa para coletar dados
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
ms.openlocfilehash: 360ba6a67d43a0b78b1104ae64885697009bb222
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155103"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="d66fe-102">Criar uma pesquisa para coletar dados</span><span class="sxs-lookup"><span data-stu-id="d66fe-102">Create a search to collect data</span></span>

<span data-ttu-id="d66fe-103">Na guia **pesquisas** do seu caso, você pode criar uma nova pesquisa clicando em **nova pesquisa** e seguindo o assistente.</span><span class="sxs-lookup"><span data-stu-id="d66fe-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="d66fe-104">Nomear sua pesquisa e dar descrição</span><span class="sxs-lookup"><span data-stu-id="d66fe-104">Name your search and give description</span></span>

<span data-ttu-id="d66fe-105">Cada pesquisa com uma ocorrência deve ter um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d66fe-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="d66fe-106">Opcionalmente, você pode fornecer uma descrição para sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d66fe-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="d66fe-107">Definir suas condições</span><span class="sxs-lookup"><span data-stu-id="d66fe-107">Define your conditions</span></span>

<span data-ttu-id="d66fe-108">Você pode definir as condições para sua pesquisa usando os cartões de condição pré-criados ou usando a linguagem de consulta de palavra-chave (KQL).</span><span class="sxs-lookup"><span data-stu-id="d66fe-108">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="d66fe-109">Para obter mais informações, consulte [Build Search queries](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="d66fe-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="d66fe-110">Escolha os responsáveis pela pesquisa</span><span class="sxs-lookup"><span data-stu-id="d66fe-110">Choose the custodians to search from</span></span>

<span data-ttu-id="d66fe-111">Depois de definir suas condições, você precisará escolher quais locais deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="d66fe-112">Uma maneira de fazer isso é especificando quais responsáveis você já adicionou à ocorrência que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="d66fe-113">Ao selecionar um responsáveis, você executará a pesquisa em todas as fontes de dados mapeadas para os responsáveis.</span><span class="sxs-lookup"><span data-stu-id="d66fe-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="d66fe-114">Confira [trabalhar com os responsáveis](managing-custodians.md) para obter mais informações sobre como adicionar os responsáveis ao seu caso e gerenciar suas fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="d66fe-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="d66fe-115">Escolher locais não custodial</span><span class="sxs-lookup"><span data-stu-id="d66fe-115">Choose non-custodial locations</span></span>

<span data-ttu-id="d66fe-116">Em alguns casos, talvez você queira Pesquisar fontes de dados que não estão mapeadas para um determinado.</span><span class="sxs-lookup"><span data-stu-id="d66fe-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="d66fe-117">Nesse caso, você pode especificar os locais que deseja pesquisar ou optar por pesquisar todos os locais de conteúdo de um serviço específico do Office 365 (como pesquisar todas as caixas de correio do Exchange ou todos os sites do SharePoint e do OneDrive for Business).</span><span class="sxs-lookup"><span data-stu-id="d66fe-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>