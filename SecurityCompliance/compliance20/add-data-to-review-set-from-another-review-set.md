---
title: Adicionar dados de um conjunto de revisão para outro conjunto de revisão
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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527099"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a>Adicionar dados a um conjunto de revisão de outro conjunto de revisão

Em alguns casos, pode ser necessário distribuir uma parte dos documentos de um conjunto de análise e trabalhar com eles individualmente em outro conjunto de revisão.  Isso é especialmente útil se você tiver escolhido conteúdo em um conjunto de revisão e quiser executar a análise no subconjunto de dados.

Use o fluxo de trabalho a seguir para adicionar conteúdo de uma análise definida para outra.

## <a name="before-you-begin"></a>Antes de começar

Antes de começar, você precisará criar uma nova revisão configurada para adicionar os dados a.  Um novo conjunto de revisão pode ser adicionado à guia **conjuntos de revisão** da ocorrência. Para obter mais informações, consulte [Manage Review sets](managing-review-sets.md).

## <a name="step-1-identify-content-to-add-to-another-review-set"></a>Etapa 1: identificar o conteúdo a ser adicionado a outro conjunto de revisão

Você pode adicionar conteúdo a um conjunto de revisão selecionando emails e documentos na grade do documento ou todos os itens em um resultado de pesquisa.  Se escolher Adicionar itens selecionados, selecione os itens, clique em **ação**e, em seguida, clique em **Adicionar a outro conjunto de revisão**.

![Adicionar a outro conjunto de revisão](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a>Etapa 2: especificar as opções para adicionar a outro conjunto de revisão

Na página **Adicionar a outro conjunto de revisão** , escolha o conjunto de revisão ao qual você deseja adicionar os itens. Escolha se deseja adicionar **todos os resultados de pesquisa** ou os **itens selecionados**.  Informações adicionais fornecem opções para incluir todos os metadados dos itens e, por fim, se as marcas de documento devem ou não ser incluídas no novo conjunto de revisão.  Após clicar em **OK** , um novo trabalho será criado para adicionar o conteúdo a um conjunto de revisão; Você pode monitorar o andamento desse trabalho na guia **trabalho** . Para obter mais informações, consulte [Manage Jobs](managing-jobs-ediscovery20.md).

![Adicionar a outro conjunto de revisão](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
