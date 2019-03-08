---
title: Exportar documentos de um conjunto de trabalho
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
ms.openlocfilehash: 815b92b13ed09d8aec64f5207f1c82d910e2dce0
ms.sourcegitcommit: 9f38ba72eba0b656e507860ca228726e4199f7ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/07/2019
ms.locfileid: "30475701"
---
# <a name="export-documents-from-a-working-set"></a><span data-ttu-id="5ba81-102">Exportar documentos de um conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="5ba81-102">Export documents from a working set</span></span>

<span data-ttu-id="5ba81-103">A exportação de conteúdo de um conjunto de trabalho pode ser realizada por meio de 3 métodos diferentes:</span><span class="sxs-lookup"><span data-stu-id="5ba81-103">Exporting content from a working set can be accomplished via 3 different methods:</span></span>

## <a name="download"></a><span data-ttu-id="5ba81-104">Baixar</span><span class="sxs-lookup"><span data-stu-id="5ba81-104">Download</span></span>

<span data-ttu-id="5ba81-105">O download oferece uma maneira simples de baixar o conteúdo de um conjunto de trabalho em formato nativo.</span><span class="sxs-lookup"><span data-stu-id="5ba81-105">Download offers a simple way to download content from a working set in Native format.</span></span> <span data-ttu-id="5ba81-106">Ele aproveita os recursos de transferência de dados do navegador para que um prompt do navegador seja exibido quando um download estiver pronto.</span><span class="sxs-lookup"><span data-stu-id="5ba81-106">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="5ba81-107">Arquivos baixados usando este método serão zipados em um arquivo de contêiner e serão arquivos de nível de item.</span><span class="sxs-lookup"><span data-stu-id="5ba81-107">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="5ba81-108">Isso significa que, se você selecionar um anexo, receberá automaticamente o email com o anexo incluído.</span><span class="sxs-lookup"><span data-stu-id="5ba81-108">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="5ba81-109">Da mesma forma, se você selecionar uma planilha do Excel incorporada em um documento do Word, receberá o documento do Word com a planilha do Excel incorporada.</span><span class="sxs-lookup"><span data-stu-id="5ba81-109">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="5ba81-110">Os itens baixados preservarão a data da última modificação que pode ser exibida como uma propriedade de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ba81-110">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="5ba81-111">Para baixar o conteúdo de um conjunto de trabalho, comece selecionando os arquivos que você deseja baixar e, em seguida, selecione "download" no menu ações.</span><span class="sxs-lookup"><span data-stu-id="5ba81-111">To download content from a working set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Captura de tela de uma descrição de computador gerada automaticamente](../media/eDiscoDownload.png)

## <a name="export"></a><span data-ttu-id="5ba81-113">Exportar</span><span class="sxs-lookup"><span data-stu-id="5ba81-113">Export</span></span>

<span data-ttu-id="5ba81-114">Exportar permite que os usuários personalizem o conteúdo que está incluído no pacote de download.</span><span class="sxs-lookup"><span data-stu-id="5ba81-114">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="5ba81-115">Ele fornece uma página de configuração com as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="5ba81-115">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="5ba81-116">Arquivo de metadados</span><span class="sxs-lookup"><span data-stu-id="5ba81-116">Metadata file</span></span>

> <span data-ttu-id="5ba81-117">Isso pode ser considerado o "carregar arquivo" que contém metadados associados aos arquivos exportados.</span><span class="sxs-lookup"><span data-stu-id="5ba81-117">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="5ba81-118">Para obter uma lista de campos disponíveis no arquivo de metadados, \[consulte\]link.</span><span class="sxs-lookup"><span data-stu-id="5ba81-118">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="5ba81-119">Normalmente, esse arquivo pode ser ingerido<sup></sup> por três ferramentas de terceiros para downstream.</span><span class="sxs-lookup"><span data-stu-id="5ba81-119">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="5ba81-120">Dados de marca</span><span class="sxs-lookup"><span data-stu-id="5ba81-120">Tag data</span></span>

> <span data-ttu-id="5ba81-121">Esse conteúdo seria adicionado como campos no arquivo de metadados.</span><span class="sxs-lookup"><span data-stu-id="5ba81-121">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="5ba81-122">Ele contém todas as informações de marca aplicadas nos conjuntos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5ba81-122">It contains all of the tag information applied in working sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="5ba81-123">Arquivos de texto</span><span class="sxs-lookup"><span data-stu-id="5ba81-123">Text files</span></span>

> <span data-ttu-id="5ba81-124">Arquivos de texto podem ser gerados para cada arquivo exportado de um conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5ba81-124">Text files can be generated for each file exported from a working set.</span></span> <span data-ttu-id="5ba81-125">Muitas vezes, esses arquivos são necessários para parceiros de serviço como parte da inclusão de dados em uma área de 3<sup>RD</sup> ferramentas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="5ba81-125">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="5ba81-126">Arquivos reRedigidos</span><span class="sxs-lookup"><span data-stu-id="5ba81-126">Redacted files</span></span>

> <span data-ttu-id="5ba81-127">Se PDFs redigidos forem gerados durante a revisão, esses arquivos estarão disponíveis durante a exportação.</span><span class="sxs-lookup"><span data-stu-id="5ba81-127">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="5ba81-128">Os usuários podem decidir se serão exportados apenas arquivos nativos ou para substituir os nativos que têm redaçãos com o gravado em PDFs.</span><span class="sxs-lookup"><span data-stu-id="5ba81-128">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="5ba81-129">Local de exportação</span><span class="sxs-lookup"><span data-stu-id="5ba81-129">Export Location</span></span>

> <span data-ttu-id="5ba81-130">O conteúdo exPortado é entregue a um blob do Azure fornecido pela Microsoft ou o blob de um cliente pode ser usado se os detalhes forem fornecidos na exportação.</span><span class="sxs-lookup"><span data-stu-id="5ba81-130">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

## <a name="export-structure"></a><span data-ttu-id="5ba81-131">Exportar estrutura</span><span class="sxs-lookup"><span data-stu-id="5ba81-131">Export Structure</span></span>

<span data-ttu-id="5ba81-132">Quando o conteúdo é exportado de um conjunto de trabalho, o conteúdo é organizado na estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ba81-132">When content is exported from a working set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="5ba81-133">Pasta raiz – ID de download</span><span class="sxs-lookup"><span data-stu-id="5ba81-133">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="5ba81-134">Exportar\_arquivo\_de carregamento. csv = arquivo de metadados</span><span class="sxs-lookup"><span data-stu-id="5ba81-134">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="5ba81-135">Summary. txt = um arquivo de resumo com estatísticas de exportação</span><span class="sxs-lookup"><span data-stu-id="5ba81-135">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="5ba81-136">Entrada\_ou arquivos\_nativos = contém todos os arquivos nativos</span><span class="sxs-lookup"><span data-stu-id="5ba81-136">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="5ba81-137">Arquivos\_de erro = contém qualquer arquivo de erro incluído na exportação</span><span class="sxs-lookup"><span data-stu-id="5ba81-137">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="5ba81-138">ExtractionError – um CSV que contém metadados disponíveis de arquivos que não foram extraídos corretamente de arquivos pai</span><span class="sxs-lookup"><span data-stu-id="5ba81-138">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="5ba81-139">ProcessingError – conteúdo com erros de processamento.</span><span class="sxs-lookup"><span data-stu-id="5ba81-139">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="5ba81-140">Esse conteúdo é o nível do item se um anexo sofreu um erro de processamento, o email que contém o anexo será incluído nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="5ba81-140">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="5ba81-141">Arquivos\_de\_texto extraídos = contém todos os arquivos de texto extraídos gerados no processamento.</span><span class="sxs-lookup"><span data-stu-id="5ba81-141">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>

## <a name="working-set"></a><span data-ttu-id="5ba81-142">Conjunto de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5ba81-142">Working Set</span></span>

<span data-ttu-id="5ba81-143">O conteúdo pode ser adicionado a outro conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5ba81-143">Content can be added to another working set.</span></span>