---
title: Indexação avançada de dados para uma investigação
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
ms.openlocfilehash: 9537cf743b89da7167ce3a37a5915027f4eb717a
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31029854"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a>Indexação avançada de dados para uma investigação

O conteúdo no sistema ativo pode ser parcialmente indexado por vários motivos, incluindo a existência de imagens, tipos de arquivos não suportados ou quando são encontrados limites de tamanho de arquivo de indexação. Ao lidar com o despejo de dados de alto risco, você deseja garantir que sua pesquisa tenha capturado todos os dados que você deseja investigar. Quando uma pessoa de interesse é adicionada a uma investigação de dados, qualquer conteúdo no Office 365 que foi considerado parcialmente indexado é processado novamente para torná-lo totalmente pesquisável. Esse processo é chamado de *indexAção avançada*. 

Para saber mais sobre o processamento de suporte no Office 365 e itens parcialmente indexados, consulte:

- [Tipos de arquivo com suporte em investigações de dados](supported-filetypes-datainvestigations.md)

- [Itens parcialmente indexados na Pesquisa de Conteúdo do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)

- [Formatos de arquivo indexados pela pesquisa do Exchange](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [Extensões de nome de arquivo rastreado padrão e tipos de arquivos analisados no SharePoint Server Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Exibindo resultados avançados de indexação

Após a conclusão do processo de indexação avançada, você pode entender a eficácia da reprocessamento.  Na exibição de indexação de pessoas de interesse, o gráfico lista todos os itens adicionados ao *índice híbrido*.  O índice híbrido é onde as investigações de dados (prévia) armazenam o conteúdo reprocessado.

O gráfico também inclui o número de itens que exigem correção e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [Error remediation When Processing data](error-remediation.md).

## <a name="updating-advanced-indexes-for-people-of-interest"></a>Atualizando índices avançados para pessoas de interesse

Quando uma pessoa de interesse é adicionada a uma investigação de dados, todos os itens parcialmente indexados são processados novamente. No enTanto, à medida que o tempo passa, os itens mais parcialmente indexados podem ser adicionados à caixa de correio de um usuário ou a uma conta do OneDrive.  Quando necessário, você pode atualizar os índices.

> [!NOTE]
> A atualização de pessoas de índices de interesse é um processo de execução demorada. É recomendável que você não atualize os índices mais de uma vez por dia em uma investigação.
