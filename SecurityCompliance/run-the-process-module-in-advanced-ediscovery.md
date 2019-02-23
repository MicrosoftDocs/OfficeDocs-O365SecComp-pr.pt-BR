---
title: Executar o Módulo de processo na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Saiba mais sobre as diretrizes para preparar arquivos de caso dos dados do Office 365 para análise com a descoberta eletrônica avançada do Office 365.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216111"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="115ab-103">Executar o Módulo de processo na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="115ab-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="115ab-104">Os arquivos de caso são carregados na descoberta eletrônica avançada durante o **processo**de **preparação** \> .</span><span class="sxs-lookup"><span data-stu-id="115ab-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="115ab-p101">A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="115ab-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="115ab-107">Diretrizes: preparando dados para descoberta eletrônica avançada</span><span class="sxs-lookup"><span data-stu-id="115ab-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="115ab-108">**Qualidade**: identifique claramente o preenchimento de arquivo de caso pertinente à ocorrência.</span><span class="sxs-lookup"><span data-stu-id="115ab-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="115ab-109">**Carrega**: carregar os arquivos em um local acessível à descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="115ab-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="115ab-p102">**ID de arquivo**: um identificador de arquivo exclusivo na descoberta eletrônica avançada. Se nenhum identificador de arquivo for importado, a descoberta eletrônica avançada gerará automaticamente a ID. Se você mapear a ID em uma carga de processo subsequente e mapear um caminho diferente do que na carga de processo inicial, a descoberta eletrônica avançada substituirá o caminho (em vez de adicionar uma nova entrada de arquivo). A ID pode ser usada como referência no processo de exportação. O valor de ID não deve ser "-1".</span><span class="sxs-lookup"><span data-stu-id="115ab-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="115ab-p103">**MD5**: essa assinatura é usada para diferenciar entre arquivos (dois arquivos não são considerados duplicatas exatas, a menos que tenham o mesmo MD5). Por padrão, a descoberta eletrônica avançada calcula o MD5 de arquivos. Quando os arquivos carregados são arquivos de texto, é recomendável carregar e mapear o valor MD5 original, em vez de calcular a descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="115ab-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="115ab-118">**Nome e tipo de arquivo**:</span><span class="sxs-lookup"><span data-stu-id="115ab-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="115ab-p104">A descoberta eletrônica avançada pode processar arquivos de vários formatos e extrair arquivos nativos carregados em um formato padrão, \*como. TXT, HTML ou. XML. o processamento de arquivos de texto é mais rápido do que arquivos nativos. Arquivos de texto extraídos são armazenados na pasta de casos.</span><span class="sxs-lookup"><span data-stu-id="115ab-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="115ab-p105">Não carregue arquivos que não podem ser extraídos, como arquivos do sistema ou imagens gráficas. Esses arquivos podem atrasar o processamento.</span><span class="sxs-lookup"><span data-stu-id="115ab-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="115ab-124">Verifique se os nomes de arquivo são nomeados de forma significativa e se os caminhos estão corretos.</span><span class="sxs-lookup"><span data-stu-id="115ab-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="115ab-125">**Caminho do arquivo**: a descoberta eletrônica avançada pode carregar arquivos com comprimentos de caminho de até 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="115ab-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="115ab-p106">**Extração de texto**: ao extrair texto de arquivos nativos, além do texto normal, os seguintes itens também são extraídos: texto oculto (Excel e. doc), colunas ocultas (Excel), controles de acompanhamento (. doc), anotações do orador (. ppt), objetos incorporados (por exemplo, Objetos do Excel em um. ppt). Eles podem ser exibidos no editor de texto.</span><span class="sxs-lookup"><span data-stu-id="115ab-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="115ab-p107">**Ignorar texto**: este recurso opcional é definido após a execução do processo e antes da análise. Ignorar texto deve ser usado com cuidado porque seu uso pode reduzir o desempenho da análise de arquivo.</span><span class="sxs-lookup"><span data-stu-id="115ab-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="115ab-130">**Texto multilíngue**: a descoberta eletrônica avançada atualmente não lida com nomes multilíngues para marcas, responsáveis e problemas.</span><span class="sxs-lookup"><span data-stu-id="115ab-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="115ab-p108">**Metadados**: Determine se há metadados que você deseja salvar no banco de dados de caso para referência futura, como intervalo de datas, tamanho do arquivo, tipo de arquivo, responsáveis e assunto. Os metadados podem ser carregados depois que os arquivos já foram carregados sem a execução do inventário ou a adição de sobrecarga de reprocessamento.</span><span class="sxs-lookup"><span data-stu-id="115ab-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="115ab-p109">Se os arquivos foram originalmente carregados pelo caminho, mapeie a coluna de caminho quando importar metadados mais tarde. É possível fazer referência ao arquivo pela ID e mapear um caminho diferente. Este é um cenário útil quando os caminhos de arquivo mudam.</span><span class="sxs-lookup"><span data-stu-id="115ab-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="115ab-p110">Se os arquivos foram originalmente carregados por ID de arquivo, mapeie a coluna de ID ao carregar metadados. Fazer referência ao arquivo por caminho (em vez de ID) causará a reinicialização de arquivos com uma ID diferente. A descoberta eletrônica avançada cria cópias dos arquivos, em vez de carregar metadados dos arquivos existentes.</span><span class="sxs-lookup"><span data-stu-id="115ab-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="115ab-139">**Famílias**: não é possível carregar uma família sem o seu pai (chefe da família).</span><span class="sxs-lookup"><span data-stu-id="115ab-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="115ab-p111">**Tamanho do arquivo**: não há limitação no tamanho dos arquivos carregados para a descoberta eletrônica avançada. Para análise (análise, relevância, etc.), o limite é de 5.242.880 caracteres de texto extraído. Arquivos maiores são ignorados (por exemplo, em relevância, os arquivos não participam do processo de treinamento de relevância e não recebem uma pontuação de relevância após o cálculo em lotes).</span><span class="sxs-lookup"><span data-stu-id="115ab-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="115ab-p112">**Quantidade de arquivo**: não há limite recomendado para o número de arquivos que podem ser tratados em um único caso. O desempenho depende dos recursos do seu sistema.</span><span class="sxs-lookup"><span data-stu-id="115ab-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="115ab-145">Filtrando arquivos</span><span class="sxs-lookup"><span data-stu-id="115ab-145">Filtering files</span></span>

<span data-ttu-id="115ab-p113">Um rótulo definido pelo usuário pode ser associado a um conjunto de arquivos para excluí-los do processo ou de outras tarefas. Cada sessão de processo é associada a uma ID de lote. Embora a ID de lote não fique visível para o especialista em relevância, isso pode ser feito com o uso de um utilitário de pesquisa, adicionando um filtro para o lote atual e marcando todos os arquivos apropriados com um rótulo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="115ab-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="115ab-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="115ab-149">See also</span></span>

[<span data-ttu-id="115ab-150">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="115ab-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="115ab-151">Executando o módulo de processo e carregando dados</span><span class="sxs-lookup"><span data-stu-id="115ab-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="115ab-152">Exibir resultados do módulo de processo</span><span class="sxs-lookup"><span data-stu-id="115ab-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

