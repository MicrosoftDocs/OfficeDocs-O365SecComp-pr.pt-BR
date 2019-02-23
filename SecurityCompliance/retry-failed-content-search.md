---
title: Repetir uma pesquisa de conteúdo para resolver um erro de localização de conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Use o botão repetir para resolver pesquisas de conteúdo que têm erros de local de conteúdo.
ms.openlocfilehash: 032d93ef0990ed1dd7c1ea7bf2ba16653b3a862f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218851"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Repetir uma pesquisa de conteúdo para resolver um erro de localização de conteúdo

Ao usar a pesquisa de conteúdo no centro de conformidade do & de segurança do Office 365 para pesquisar um número muito grande de caixas de correio (por exemplo, Pesquisar em 100.000 caixas de correio ou mais em uma única pesquisa de conteúdo), você pode receber erros de pesquisa semelhantes aos seguintes:

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Esses erros (com códigos de erro de CS008-009 e CS012-002) indicam que a pesquisa de conteúdo falhou ao pesquisar locais de conteúdo específicos; Neste exemplo, duas caixas de correio não foram pesquisadas. Esses erros são exibidos na página do menu de detalhes de status da pesquisa de conteúdo.

## <a name="cause-of-content-location-errors"></a>Causa de erros de localização de conteúdo

Ao pesquisar um grande número de caixas de correio, a pesquisa é distribuída entre milhares de servidores em um datacenter da Microsoft. A qualquer momento, os servidores específicos podem estar no estado de reinicialização ou no processo de failover para cópias redundantes. Em qualquer um desses casos, a solicitação de pesquisa de conteúdo para recuperar dados irá expirar. No exemplo anterior, os erros para as caixas de correio que falharam foram o resultado da pesquisa com tempo limite.

## <a name="resolving-content-location-errors"></a>Resolvendo erros de localização de conteúdo

A reinicialização da pesquisa geralmente resultará em erros semelhantes em servidores diferentes. Em vez de reiniciar a pesquisa, clique no botão **repetir** que é exibido na parte superior da página de resultados da pesquisa.

![Clique no botão repetir para resolver erros de localização de conteúdo](media/retrycontentsearch3.png)

Isso resultará na repetição da pesquisa apenas para as caixas de correio que falharam. Quando você repetir a pesquisa, os outros resultados retornados com êxito serão mantidos.

## <a name="tips-to-avoid-content-location-errors"></a>Dicas para evitar erros de localização de conteúdo

Aqui estão algumas causas de adição de erros de local de conteúdo e algumas dicas para ajudá-lo a evitá-los ao pesquisar grandes números de caixas de correio.

- A caixa de correio que está sendo pesquisada pode estar ocupada devido à atividade do usuário. Nesse caso, o serviço de pesquisa pode se limitar a impedir que a caixa de correio fique indisponível. Para evitar isso, tente executar pesquisas fora do horário comercial.

- A consulta de pesquisa pode recuperar muito conteúdo da caixa de correio. Se possível, tente restringir o escopo da pesquisa usando palavras-chave, intervalos de datas e condições de pesquisa.

- Excesso de palavras-chave ou frases de palavra-chave quando você cria uma consulta de pesquisa usando a [lista de palavras-chave](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Quando você executa uma consulta de pesquisa que usa a lista de palavras-chave, o serviço essencialmente executa uma pesquisa separada para cada linha na lista de palavras-chave para que as estatísticas possam ser geradas. Se você estiver usando a lista de palavras-chave em consultas de pesquisa, minimize o número de linhas na lista de palavras-chave ou divida as palavras-chave do número em listas menores e crie uma pesquisa diferente para cada lista de palavras-chave.

  > [!NOTE]
  > Para ajudar a reduzir os problemas causados por listas de palavras-chave grandes, agora você está limitado a um máximo de 20 linhas na lista de palavras-chave de uma consulta de pesquisa.

- Muitas pesquisas estão sendo realizadas na mesma caixa de correio ao mesmo tempo. Se possível, tente executar uma pesquisa de cada vez em uma caixa de correio.

- Pesquisar muitas caixas de correio em uma única pesquisa. A probabilidade de erros de localização de conteúdo aumenta ao pesquisar um número muito grande de caixas de correio. Se possível, tente executar várias pesquisas para que cada pesquisa inclua um subconjunto de caixas de correio em sua organização.

- A manutenção necessária está sendo executada na caixa de correio. Embora essa causa provavelmente ocorra com frequência, espere um pouco antes de receber o erro de localização do conteúdo e repita a pesquisa.
