---
title: Exportar documentos de um conjunto de revisão
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
ms.openlocfilehash: ea9db6d95b003b5a741ae8a235fc5f06087f87d6
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527096"
---
# <a name="export-documents-from-a-review-set"></a>Exportar documentos de um conjunto de revisão

A exportação de conteúdo de um conjunto de revisão pode ser realizada por meio de 3 métodos diferentes:

## <a name="download"></a>Baixar

O download oferece uma maneira simples de baixar o conteúdo de uma revisão definida no formato nativo. Ele aproveita os recursos de transferência de dados do navegador para que um prompt do navegador seja exibido quando um download estiver pronto. Arquivos baixados usando este método serão zipados em um arquivo de contêiner e serão arquivos de nível de item. Isso significa que, se você selecionar um anexo, receberá automaticamente o email com o anexo incluído. Da mesma forma, se você selecionar uma planilha do Excel incorporada em um documento do Word, receberá o documento do Word com a planilha do Excel incorporada. Os itens baixados preservarão a data da última modificação que pode ser exibida como uma propriedade de arquivo.

Para baixar o conteúdo de um conjunto de revisão, comece selecionando os arquivos que você deseja baixar e, em seguida, selecione "download" no menu ações.

![Captura de tela de uma descrição de computador gerada automaticamente](../media/eDiscoDownload.png)

## <a name="export"></a>Exportar

Exportar permite que os usuários personalizem o conteúdo que está incluído no pacote de download. Ele fornece uma página de configuração com as seguintes configurações:

### <a name="metadata-file"></a>Arquivo de metadados

> Isso pode ser considerado o "carregar arquivo" que contém metadados associados aos arquivos exportados. Para obter uma lista de campos disponíveis no arquivo de metadados, \[consulte\]link. Normalmente, esse arquivo pode ser ingerido<sup></sup> por três ferramentas de terceiros para downstream.

### <a name="tag-data"></a>Dados de marca

> Esse conteúdo seria adicionado como campos no arquivo de metadados. Ele contém todas as informações de marca aplicadas nos conjuntos de revisão.

### <a name="text-files"></a>Arquivos de texto

> Arquivos de texto podem ser gerados para cada arquivo exportado de um conjunto de revisão. Muitas vezes, esses arquivos são necessários para parceiros de serviço como parte da inclusão de dados em uma área de 3<sup>RD</sup> ferramentas de terceiros.

### <a name="redacted-files"></a>Arquivos reredigidos

> Se PDFs redigidos forem gerados durante a revisão, esses arquivos estarão disponíveis durante a exportação. Os usuários podem decidir se serão exportados apenas arquivos nativos ou para substituir os nativos que têm redaçãos com o gravado em PDFs.

### <a name="export-location"></a>Local de exportação

> O conteúdo exportado é entregue a um blob do Azure fornecido pela Microsoft ou o blob de um cliente pode ser usado se os detalhes forem fornecidos na exportação.

## <a name="export-structure"></a>Exportar estrutura

Quando o conteúdo é exportado de um conjunto de revisão, o conteúdo é organizado na estrutura a seguir.

  - Pasta raiz – ID de download
    
      - Exportar\_arquivo\_de carregamento. csv = arquivo de metadados
    
      - Summary. txt = um arquivo de resumo com estatísticas de exportação
    
      - Entrada\_ou arquivos\_nativos = contém todos os arquivos nativos
    
      - Arquivos\_de erro = contém qualquer arquivo de erro incluído na exportação
        
          - ExtractionError – um CSV que contém metadados disponíveis de arquivos que não foram extraídos corretamente de arquivos pai
        
          - ProcessingError – conteúdo com erros de processamento. Esse conteúdo é o nível do item se um anexo sofreu um erro de processamento, o email que contém o anexo será incluído nessa pasta.
    
      - Arquivos\_de\_texto extraídos = contém todos os arquivos de texto extraídos gerados no processamento.

## <a name="review-set"></a>conjunto de revisão

O conteúdo pode ser adicionado a outro conjunto de revisão.