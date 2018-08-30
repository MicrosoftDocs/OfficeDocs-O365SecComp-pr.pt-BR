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
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a>Executar o Módulo de processo na Descoberta Eletrônica Avançada do Office 365

Arquivos de maiusculas são carregados para o eDiscovery Avançado durante a **preparação** \> **processo**. 
  
> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a>Diretrizes: Preparar dados para descoberta eletrônica avançada

- **Qualidade**: identificar claramente a população de arquivo maiusculas pertinente ao caso.
    
- **Cargas**: carregar os arquivos em um local que seja acessível para descoberta eletrônica avançada.
    
- **ID do arquivo**: um identificador de arquivo exclusivo no eDiscovery avançado. Se nenhum identificador de arquivo for importado, o eDiscovery avançado gera automaticamente o ID. Se você mapear a ID de uma carga de processo subsequente e mapear um caminho diferente na carga da processo inicial, eDiscovery avançado irá substituir o caminho (em vez de adicionar uma nova entrada de arquivo). A ID pode ser usada como uma referência no processo de exportação. O valor de ID não deve ser "-1".
    
- **MD5**: essa assinatura é usada para diferenciar arquivos (dois arquivos não são considerados cópias exatas a menos que tenham o mesmo MD5). Por padrão, o eDiscovery avançado calcula o MD5 dos arquivos. Quando os arquivos carregados são arquivos de texto, é recomendável para carregar e mapear o valor de MD5 original em vez de calculá-lo no eDiscovery avançado.
    
- O **nome e tipo de arquivo**:
    
  - EDiscovery avançado pode processar arquivos de vários formatos e extrair arquivos nativos carregados em um formato padrão, tais como \*. TXT, HTML, ou. XML. processamento de arquivos de texto é menor do que arquivos nativos. Arquivos de texto extraídos são armazenados na pasta maiusculas.
    
  - Não carrega arquivos que não podem ser extraídos, como arquivos de sistema ou imagens gráficas. Esses arquivos podem atrasar.
    
  - Verifique se os nomes de arquivo são significativamente nomeados e caminhos estão corretos.
    
- **Caminho do arquivo**: eDiscovery avançado pode carregar arquivos com comprimentos de caminho até 400 caracteres.
    
- **Extração de texto**: quando extrair texto de arquivos nativos, bem como texto normal, o seguinte também é extraído: colunas de texto oculto (Excel e. doc), oculto (Excel), controlar alterações (. doc), objetos de notas (. ppt), incorporados de alto-falante (por exemplo, Objetos do Excel em um. ppt). Eles podem ser exibidos no editor de texto.
    
- **Ignorar texto**: esse recurso opcional é definido depois que o processo é executado e antes de analisar. Ignorar texto deve ser usado com cuidado porque seu uso pode reduzir o desempenho da análise de arquivo.
    
- **Texto multilíngue**: eDiscovery avançada não processa atualmente multilíngues nomes para marcas, dos responsáveis e problemas.
    
- **Metadados**: Determine se há metadados que você deseja salvar no banco de dados caso para referência futura, como o intervalo de datas, tamanho do arquivo, tipo de arquivo, dos responsáveis e da entidade. Metadados podem ser carregados depois arquivos já foram carregados sem executar novamente o inventário ou adicionando reprocessamento sobrecarga. 
    
  - Se os arquivos foram originalmente carregados pelo caminho, mapeie a coluna de caminho quando mais tarde a importação de metadados. É possível consultar o arquivo pela ID e para mapear um caminho diferente. Este cenário útil é quando os caminhos de arquivo são alterados.
    
  - Se os arquivos foram originalmente carregados pela ID do arquivo, mapeie a coluna identificação ao carregar os metadados. Referindo-se ao arquivo pelo caminho (em vez de ID) fará com que arquivos sejam carregados novamente com um ID diferente. EDiscovery avançado cria cópias dos arquivos de preferência seja que metadados de carregamento dos arquivos existentes.
    
- **Famílias**: não é possível carregar uma família sem seu pai (cabeça da família). 
    
- **Tamanho do arquivo**: não há nenhuma limitação no tamanho de arquivos carregados para descoberta eletrônica avançada. Para análise (Analyze, relevância, etc.), o limite é 5,242,880 caracteres de texto extraído. Arquivos maiores são ignorados (por exemplo, em relevância, arquivos não participa do processo de treinamento de relevância em não receberá uma pontuação de relevância após o cálculo de lote).
    
- **Quantidade de arquivo**: não há nenhum limite recomendado no número de arquivos que podem ser administrados em um único caso. Desempenho depende dos recursos do seu sistema. 
    
## <a name="filtering-files"></a>Filtragem de arquivos

Um rótulo definida pelo usuário pode ser associado um conjunto de arquivos para excluí-los do processo ou outras tarefas. Cada sessão de processo é associado a uma ID de lote. Embora a ID de lote não estiver visível ao especialista em relevância, isso pode ser feito usando um utilitário de pesquisa, adicionando um filtro para o lote atual e a marcação de todos os arquivos apropriados com um rótulo definida pelo usuário. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Executando o módulo de processo e carregamento de dados](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[Exibição de resultados de módulo de processo](view-process-module-results-in-advanced-ediscovery.md)

