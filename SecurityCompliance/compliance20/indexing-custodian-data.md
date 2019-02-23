---
title: Indexação avançada de dados de responsáveis
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218661"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexação avançada de dados de responsáveis

Quando um qualificador é adicionado a um caso de descoberta eletrônica avançada (visualização), qualquer conteúdo no Office 365 que foi considerado parcialmente indexado é reprocessado para torná-lo totalmente pesquisável.  Esse processo é chamado de *indexAção avançada*. O conteúdo pode ser parcialmente indexado por vários motivos, incluindo a existência de imagens, tipos de arquivos não suportados ou quando são encontrados limites de tamanho de arquivo de indexação.  Para saber mais sobre itens parcialmente indexados, confira [itens parcialmente indexados na pesquisa de conteúdo no Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Exibindo resultados avançados de indexação

Após a conclusão do processo de indexação avançada, você pode entender a eficácia da reprocessamento.  No modo de exibição de indexação de responsáveis, o gráfico lista todos os itens adicionados ao *índice híbrido*.  O índice híbrido é onde a descoberta eletrônica avançada (visualização) armazena o conteúdo reprocessado.

O gráfico também inclui o número de itens que exigem correção e outro gráfico de erros por tipo de arquivo. Para obter mais informações, consulte [Error remediation When Processing data](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Atualizando índices avançados para os responsáveis

Quando um responsáveis é adicionado a uma descoberta eletrônica avançada (visualização), todos os itens parcialmente indexados são processados novamente. No enTanto, à medida que o tempo passa, os itens mais parcialmente indexados podem ser adicionados à caixa de correio de um usuário ou a uma conta do OneDrive.  Quando necessário, você pode atualizar os índices.

> [!NOTE]
> Atualizar os índices dos responsáveis é um processo de execução longa. É recomendável que você não atualize os índices mais de uma vez por dia em um caso.
