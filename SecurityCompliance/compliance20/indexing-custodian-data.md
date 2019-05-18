---
title: Indexação de dados custodiante avançados
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
ms.openlocfilehash: be163d3272dbe027cb0f4b4b4fe379bf28fa5a85
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151753"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexação de dados custodiante avançados

Quando um Objecté adicionado a um caso de descoberta eletrônica avançada, qualquer conteúdo no Office 365 que foi considerado parcialmente indexado é reprocessado para torná-lo totalmente pesquisável.  Esse processo é chamado de *indexação avançada*. O conteúdo pode ser parcialmente indexado por vários motivos, incluindo a existência de imagens, tipos de arquivos não suportados ou quando são encontrados limites de tamanho de arquivo de indexação.

Para saber mais sobre o processamento de suporte no Office 365 e itens parcialmente indexados, consulte:

- [Tipos de arquivo com suporte na descoberta eletrônica avançada](supported-filetypes-ediscovery20.md)
- [Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [Formatos de arquivo indexados pela pesquisa do Exchange](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [Extensões de nome de arquivo rastreado padrão e tipos de arquivos analisados no SharePoint Server Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Exibindo resultados avançados de indexação

Após a conclusão do processo de indexação avançada, você pode entender a eficácia da reprocessamento.  No modo de exibição de indexação de responsáveis, o gráfico lista todos os itens adicionados ao *índice híbrido*.  O índice híbrido é onde a descoberta eletrônica avançada armazena o conteúdo reprocessado.

O gráfico também inclui o número de itens que exigem correção e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [Error remediation When Processing data](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Atualizando índices avançados para os responsáveis

Quando um responsáveis é adicionado a uma caixa de descoberta eletrônica avançada, todos os itens parcialmente indexados são reprocessados. No entanto, à medida que o tempo passa, os itens mais parcialmente indexados podem ser adicionados à caixa de correio de um usuário ou a uma conta do OneDrive.  Quando necessário, você pode atualizar os índices.

> [!NOTE]
> Atualizar os índices dos responsáveis é um processo de execução longa. É recomendável que você não atualize os índices mais de uma vez por dia em um caso.
