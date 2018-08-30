---
title: Executar o Módulo de processo na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Saiba as diretrizes para preparar os arquivos casos de dados do Office 365 para análise com eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524606"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="6a27e-103">Executar o Módulo de processo na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6a27e-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="6a27e-104">Arquivos de maiusculas são carregados para o eDiscovery Avançado durante a **preparação** \> **processo**.</span><span class="sxs-lookup"><span data-stu-id="6a27e-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6a27e-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6a27e-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="6a27e-107">Diretrizes: Preparar dados para descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="6a27e-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="6a27e-108">**Qualidade**: identificar claramente a população de arquivo maiusculas pertinente ao caso.</span><span class="sxs-lookup"><span data-stu-id="6a27e-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="6a27e-109">**Cargas**: carregar os arquivos em um local que seja acessível para descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="6a27e-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="6a27e-p102">**ID do arquivo**: um identificador de arquivo exclusivo no eDiscovery avançado. Se nenhum identificador de arquivo for importado, o eDiscovery avançado gera automaticamente o ID. Se você mapear a ID de uma carga de processo subsequente e mapear um caminho diferente na carga da processo inicial, eDiscovery avançado irá substituir o caminho (em vez de adicionar uma nova entrada de arquivo). A ID pode ser usada como uma referência no processo de exportação. O valor de ID não deve ser "-1".</span><span class="sxs-lookup"><span data-stu-id="6a27e-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="6a27e-p103">**MD5**: essa assinatura é usada para diferenciar arquivos (dois arquivos não são considerados cópias exatas a menos que tenham o mesmo MD5). Por padrão, o eDiscovery avançado calcula o MD5 dos arquivos. Quando os arquivos carregados são arquivos de texto, é recomendável para carregar e mapear o valor de MD5 original em vez de calculá-lo no eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="6a27e-118">O **nome e tipo de arquivo**:</span><span class="sxs-lookup"><span data-stu-id="6a27e-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="6a27e-p104">EDiscovery avançado pode processar arquivos de vários formatos e extrair arquivos nativos carregados em um formato padrão, tais como \*. TXT, HTML, ou. XML. processamento de arquivos de texto é menor do que arquivos nativos. Arquivos de texto extraídos são armazenados na pasta maiusculas.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="6a27e-p105">Não carrega arquivos que não podem ser extraídos, como arquivos de sistema ou imagens gráficas. Esses arquivos podem atrasar.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="6a27e-124">Verifique se os nomes de arquivo são significativamente nomeados e caminhos estão corretos.</span><span class="sxs-lookup"><span data-stu-id="6a27e-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="6a27e-125">**Caminho do arquivo**: eDiscovery avançado pode carregar arquivos com comprimentos de caminho até 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6a27e-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="6a27e-p106">**Extração de texto**: quando extrair texto de arquivos nativos, bem como texto normal, o seguinte também é extraído: colunas de texto oculto (Excel e. doc), oculto (Excel), controlar alterações (. doc), objetos de notas (. ppt), incorporados de alto-falante (por exemplo, Objetos do Excel em um. ppt). Eles podem ser exibidos no editor de texto.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="6a27e-p107">**Ignorar texto**: esse recurso opcional é definido depois que o processo é executado e antes de analisar. Ignorar texto deve ser usado com cuidado porque seu uso pode reduzir o desempenho da análise de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="6a27e-130">**Texto multilíngue**: eDiscovery avançada não processa atualmente multilíngues nomes para marcas, dos responsáveis e problemas.</span><span class="sxs-lookup"><span data-stu-id="6a27e-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="6a27e-p108">**Metadados**: Determine se há metadados que você deseja salvar no banco de dados caso para referência futura, como o intervalo de datas, tamanho do arquivo, tipo de arquivo, dos responsáveis e da entidade. Metadados podem ser carregados depois arquivos já foram carregados sem executar novamente o inventário ou adicionando reprocessamento sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="6a27e-p109">Se os arquivos foram originalmente carregados pelo caminho, mapeie a coluna de caminho quando mais tarde a importação de metadados. É possível consultar o arquivo pela ID e para mapear um caminho diferente. Este cenário útil é quando os caminhos de arquivo são alterados.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="6a27e-p110">Se os arquivos foram originalmente carregados pela ID do arquivo, mapeie a coluna identificação ao carregar os metadados. Referindo-se ao arquivo pelo caminho (em vez de ID) fará com que arquivos sejam carregados novamente com um ID diferente. EDiscovery avançado cria cópias dos arquivos de preferência seja que metadados de carregamento dos arquivos existentes.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="6a27e-139">**Famílias**: não é possível carregar uma família sem seu pai (cabeça da família).</span><span class="sxs-lookup"><span data-stu-id="6a27e-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="6a27e-p111">**Tamanho do arquivo**: não há nenhuma limitação no tamanho de arquivos carregados para descoberta eletrônica avançada. Para análise (Analyze, relevância, etc.), o limite é 5,242,880 caracteres de texto extraído. Arquivos maiores são ignorados (por exemplo, em relevância, arquivos não participa do processo de treinamento de relevância em não receberá uma pontuação de relevância após o cálculo de lote).</span><span class="sxs-lookup"><span data-stu-id="6a27e-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="6a27e-p112">**Quantidade de arquivo**: não há nenhum limite recomendado no número de arquivos que podem ser administrados em um único caso. Desempenho depende dos recursos do seu sistema.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="6a27e-145">Filtragem de arquivos</span><span class="sxs-lookup"><span data-stu-id="6a27e-145">Filtering files</span></span>

<span data-ttu-id="6a27e-p113">Um rótulo definida pelo usuário pode ser associado um conjunto de arquivos para excluí-los do processo ou outras tarefas. Cada sessão de processo é associado a uma ID de lote. Embora a ID de lote não estiver visível ao especialista em relevância, isso pode ser feito usando um utilitário de pesquisa, adicionando um filtro para o lote atual e a marcação de todos os arquivos apropriados com um rótulo definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6a27e-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a27e-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a27e-149">See also</span></span>

[<span data-ttu-id="6a27e-150">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6a27e-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="6a27e-151">Executando o módulo de processo e carregamento de dados</span><span class="sxs-lookup"><span data-stu-id="6a27e-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="6a27e-152">Exibição de resultados de módulo de processo</span><span class="sxs-lookup"><span data-stu-id="6a27e-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

