---
title: Marcar documentos em um conjunto de trabalho
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
ms.openlocfilehash: 1183264f64a74e50f750ee13618f7532ffe04eb7
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455153"
---
# <a name="tag-documents-in-a-working-set"></a><span data-ttu-id="8b87f-102">Marcar documentos em um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="8b87f-102">Tag documents in a working set</span></span>

<span data-ttu-id="8b87f-103">Organizar o conteúdo em um conjunto de trabalho é importante para concluir vários fluxos de trabalho no processo de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="8b87f-103">Organizing content in a working set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="8b87f-104">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="8b87f-104">This includes:</span></span>

-  <span data-ttu-id="8b87f-105">Remoção de conteúdo desnecessário.</span><span class="sxs-lookup"><span data-stu-id="8b87f-105">Culling unnecessary content.</span></span>

- <span data-ttu-id="8b87f-106">Identificação de conteúdo relevante.</span><span class="sxs-lookup"><span data-stu-id="8b87f-106">Identifying relevant content.</span></span>
 
-  <span data-ttu-id="8b87f-107">Identificar o conteúdo que deve ser revisado por um especialista ou advogado.</span><span class="sxs-lookup"><span data-stu-id="8b87f-107">Identifying content that must be reviewed by an expert or an attorney.</span></span>

<span data-ttu-id="8b87f-108">Quando especialistas, advogados ou outros usuários revisam o conteúdo em um conjunto de trabalho, suas opiniões relacionadas ao conteúdo podem ser capturadas usando marcas.</span><span class="sxs-lookup"><span data-stu-id="8b87f-108">When experts, attorneys, or other users review content in a working set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="8b87f-109">Por exemplo, se a intenção é de analisar conteúdo desnecessário, um usuário pode marcar documentos com uma marca como "não responsiva".</span><span class="sxs-lookup"><span data-stu-id="8b87f-109">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as “non-responsive”.</span></span> <span data-ttu-id="8b87f-110">Após o conteúdo ter sido revisado e marcado, uma pesquisa de conjunto de trabalho pode ser criada para excluir qualquer conteúdo marcado como "não responsivo", o que elimina esse conteúdo das próximas etapas no fluxo de trabalho de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="8b87f-110">After content has been reviewed and tagged, a working set search can be created to exclude any content tagged as “non-responsive”, which eliminates this content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="8b87f-111">O painel de marcas pode ser personalizado para todos os casos, para que as marcas possam suportar o fluxo de trabalho de revisão desejado.</span><span class="sxs-lookup"><span data-stu-id="8b87f-111">The tag panel can be customized for every case so that the tags can support the intended review workflow.</span></span>

## <a name="tag-types"></a><span data-ttu-id="8b87f-112">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="8b87f-112">Tag types</span></span>

<span data-ttu-id="8b87f-113">A descoberta eletrônica avançada (visualização) fornece dois tipos de marcas:</span><span class="sxs-lookup"><span data-stu-id="8b87f-113">Advanced eDiscovery (Preview) provides two types of tags:</span></span>

- <span data-ttu-id="8b87f-114">**Marcas de escolha única** -restringe os usuários a selecionar uma única marca dentro de um grupo.</span><span class="sxs-lookup"><span data-stu-id="8b87f-114">**Single choice tags** - Restricts users to select a single tag within a group.</span></span> <span data-ttu-id="8b87f-115">Isso pode ser útil para garantir que os usuários não selecionem marcas conflitantes, como "responsiva" e "sem resposta".</span><span class="sxs-lookup"><span data-stu-id="8b87f-115">This can be useful to ensure users don’t select conflicting tags such as “responsive” and “non-responsive”.</span></span> 

- <span data-ttu-id="8b87f-116">**Marcas de múltipla escolha** : permitir que os usuários selecionem várias marcas em um grupo.</span><span class="sxs-lookup"><span data-stu-id="8b87f-116">**Multiple choice tags** - Allow users to select multiple tags within a group.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="8b87f-117">Estrutura da marca</span><span class="sxs-lookup"><span data-stu-id="8b87f-117">Tag structure</span></span>

<span data-ttu-id="8b87f-118">Além dos tipos de marca, a estrutura de como as marcas são organização no painel de marcas pode ser usada para tornar os documentos de marcação mais intuitivos.</span><span class="sxs-lookup"><span data-stu-id="8b87f-118">In addition to the tag types, the structure of how tags are organization in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="8b87f-119">As marcas são agrupadas por seções.</span><span class="sxs-lookup"><span data-stu-id="8b87f-119">Tags are grouped by sections.</span></span> <span data-ttu-id="8b87f-120">A pesquisa do conjunto de trabalho oferece suporte à capacidade de Pesquisar por marca e seção de marca.</span><span class="sxs-lookup"><span data-stu-id="8b87f-120">Working set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="8b87f-121">Isso significa que você pode criar uma pesquisa de conjunto de trabalho para recuperar documentos marcados com qualquer marca em uma seção.</span><span class="sxs-lookup"><span data-stu-id="8b87f-121">This means you can create a working set search to retrieve documents tagged with any tag in a section.</span></span>

![Seções de marcas no painel de marcas](../media/Tagtypes.png)

<span data-ttu-id="8b87f-123">As marcas podem ser organizadas com o aninhamento de uma seção.</span><span class="sxs-lookup"><span data-stu-id="8b87f-123">Tags can be further organized by nesting them within a section.</span></span> <span data-ttu-id="8b87f-124">Por exemplo, se a intenção é identificar e marcar conteúdo privilegiado, o aninhamento pode ser usado para tornar claro que um usuário pode marcar um documento como "privilegiado" e selecionar o tipo de privilégio, verificando a marca aninhada apropriada.</span><span class="sxs-lookup"><span data-stu-id="8b87f-124">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a user can tag a document as “Privileged” and select the type of privilege by checking the appropriate nested tag.</span></span>

![Marcas aninhadas em uma seção tag](../media/Nestingtags.png)

## <a name="applying-tags"></a><span data-ttu-id="8b87f-126">Aplicando marcas</span><span class="sxs-lookup"><span data-stu-id="8b87f-126">Applying tags</span></span>

<span data-ttu-id="8b87f-127">Há várias maneiras de aplicar uma marca ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8b87f-127">There are several ways to apply a tag to content.</span></span>

### <a name="tagging-a-single-document"></a><span data-ttu-id="8b87f-128">Marcando um único documento</span><span class="sxs-lookup"><span data-stu-id="8b87f-128">Tagging a single document</span></span>

<span data-ttu-id="8b87f-129">Ao exibir um documento em um conjunto de trabalho, você pode exibir as marcas que uma revisão pode usar clicando em **painel de codificação**.</span><span class="sxs-lookup"><span data-stu-id="8b87f-129">When viewing a document in a working set, you can display the tags that a review can use by clicking **Coding panel**.</span></span>

![Clique no painel de marcas para exibir o painel de marcas](../media/Singledoctag.png)

<span data-ttu-id="8b87f-131">Isso permitirá que você aplique marcas ao documento exibido no visualizador.</span><span class="sxs-lookup"><span data-stu-id="8b87f-131">This will enable you to apply tags to the document displayed in the viewer.</span></span>

### <a name="bulk-tagging"></a><span data-ttu-id="8b87f-132">Marcação em massa</span><span class="sxs-lookup"><span data-stu-id="8b87f-132">Bulk tagging</span></span>

<span data-ttu-id="8b87f-133">A marcação em massa pode ser feita selecionando vários arquivos na grade de resultados e, em seguida, usando as marcas no **painel de codificação** , semelhante a marcação de documentos únicos.</span><span class="sxs-lookup"><span data-stu-id="8b87f-133">Bulk tagging can be done by selecting multiple files in the results grid and then using the tags in the **Coding panel** similar to tagging single documents.</span></span> <span data-ttu-id="8b87f-134">A desmarcação em massa pode ser feita selecionando marcas duas vezes; o primeiro clique irá aplicar a marca e a segunda será garantir que a marca seja desmarcada para todos os arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="8b87f-134">Bulk un-tagging can be done by selecting tags twice; the first click will apply the tag, and the second selection will ensure that tag is cleared for all selected files.</span></span>

![Uma captura de tela de uma descrição de telefone de célula gerada automaticamente](../media/Bulktag.png)

> [!NOTE]
> <span data-ttu-id="8b87f-136">Quando a marcação em massa, o painel de marcação exibirá uma contagem de arquivos que estão marcados para cada marca no painel.</span><span class="sxs-lookup"><span data-stu-id="8b87f-136">When bulk tagging, the tagging panel will display a count of files that are tagged for each tag in the panel.</span></span>

### <a name="tagging-in-other-review-panels"></a><span data-ttu-id="8b87f-137">Marcação em outros painéis de revisão</span><span class="sxs-lookup"><span data-stu-id="8b87f-137">Tagging in other review panels</span></span>

<span data-ttu-id="8b87f-138">Ao revisar documentos, você pode usar os outros painéis de revisão para examinar outras características de documentos na grade de resultados.</span><span class="sxs-lookup"><span data-stu-id="8b87f-138">When reviewing documents, you can use the other review panels to review other characteristics of documents in the results grid.</span></span> <span data-ttu-id="8b87f-139">Isso inclui a revisão de outros documentos relacionados, segmentos de email, duplicatas próximas e hash duplicados.</span><span class="sxs-lookup"><span data-stu-id="8b87f-139">This includes reviewing other related documents, email threads, near duplicates, and hash duplicates.</span></span> <span data-ttu-id="8b87f-140">Por exemplo, ao revisar documentos relacionados (usando o painel de revisão **da família de documentos** ), você pode reduzir significativamente o tempo de análise ao marcar documentos relacionados em massa.</span><span class="sxs-lookup"><span data-stu-id="8b87f-140">For example, when your reviewing related documents (by using the **Document family** review panel), you can significantly reduce review time by bulk tagging related documents.</span></span> <span data-ttu-id="8b87f-141">Por exemplo, se uma mensagem de email tiver vários anexos e você quiser garantir que toda a família seja marcada de forma consistente.</span><span class="sxs-lookup"><span data-stu-id="8b87f-141">For example, if an email message has several attachments and you want to ensure that the entire family is tagged consistently.</span></span>

<span data-ttu-id="8b87f-142">Por exemplo, veja como exibir o painel de **codificação** ao usar o documento painel revisão **da família** :</span><span class="sxs-lookup"><span data-stu-id="8b87f-142">For example, here's how to display the **Coding panel** when using the **Document family** review panel:</span></span>

1. <span data-ttu-id="8b87f-143">Com o painel de revisão aberto para um documento selecionado (por exemplo, exibindo a lista de conteúdo relacionado no painel de revisão **da família de documentos** , clique em **documentos de código** na parte superior do painel de revisão atual.</span><span class="sxs-lookup"><span data-stu-id="8b87f-143">With the review panel open for a selected document (for example, displaying the list of related content in the **Document family** review panel, click **Code documents** at the top of the current review panel.</span></span>

   <span data-ttu-id="8b87f-144">O painel de codificação é exibido é uma janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="8b87f-144">The Coding panel is displayed is a pop-up window.</span></span>

2. <span data-ttu-id="8b87f-145">Escolha uma ou mais marcas para aplicar o documento selecionado.</span><span class="sxs-lookup"><span data-stu-id="8b87f-145">Choose one or more tags to apply the selected document.</span></span> 

3. <span data-ttu-id="8b87f-146">Para marcar todos os documentos, selecione todos os documentos no painel **família** de documentos, clique em **documentos de código**e escolha as marcas a serem aplicadas a toda a família de documentos.</span><span class="sxs-lookup"><span data-stu-id="8b87f-146">To tag all documents, select all documents in the **Document family** panel, click **Code documents**, and then choose the tags to apply to the entire family of documents.</span></span>

![Uma captura de tela de uma descrição de postagem de mídia social gerada automaticamente](../media/Relatedtag.png)
