---
title: Criar uma pesquisa para coletar dados
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
ms.openlocfilehash: 14f90b29cbff9c1a588b816563178039c7af7da6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243409"
---
# <a name="create-a-search-to-collect-data"></a>Criar uma pesquisa para coletar dados

Na guia **pesquisas** do seu caso, você pode criar uma nova pesquisa clicando em **nova pesquisa** e seguindo o assistente.

## <a name="name-your-search-and-give-description"></a>Nomear sua pesquisa e dar descrição

Cada pesquisa com uma ocorrência deve ter um nome exclusivo. Opcionalmente, você pode fornecer uma descrição para sua pesquisa. 

## <a name="define-your-conditions"></a>Definir suas condições

Você pode definir as condições para sua pesquisa usando os cartões de condição pré-criados ou usando a linguagem de consulta de palavra-chave (KQL). Para obter mais informações, consulte [Build Search queries](building-search-queries.md).

## <a name="choose-the-custodians-to-search-from"></a>Escolha os responsáveis pela pesquisa

Depois de definir suas condições, você precisará escolher quais locais deseja pesquisar. Uma maneira de fazer isso é especificando quais responsáveis você já adicionou à ocorrência que você deseja pesquisar. Ao selecionar um responsáveis, você executará a pesquisa em todas as fontes de dados mapeadas para os responsáveis. ConFira [trabalhar com os responsáveis](managing-custodians.md) para obter mais informações sobre como adicionar os responsáveis ao seu caso e gerenciar suas fontes de dados.

## <a name="choose-non-custodial-locations"></a>Escolher locais não custodial

Em alguns casos, talvez você queira Pesquisar fontes de dados que não estão mapeadas para um determinado. Nesse caso, você pode especificar os locais que deseja pesquisar ou optar por pesquisar todos os locais de conteúdo de um serviço específico do Office 365 (como pesquisar todas as caixas de correio do Exchange ou todos os sites do SharePoint e do OneDrive for Business).