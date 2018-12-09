---
title: Repetir uma pesquisa de conteúdo para resolver um erro de local do conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Use o botão de repetição para resolver pesquisas de conteúdo que possuem erros de localização do conteúdo.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210174"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Repetir uma pesquisa de conteúdo para resolver um erro de local do conteúdo

Quando você usa a pesquisa de conteúdo no Centro de conformidade & segurança do Office 365 para pesquisar um número muito grande de caixas de correio (por exemplo, a pesquisa de caixas de 100.000 correio ou mais em uma única pesquisa de conteúdo), você pode obter erros de pesquisa que são semelhantes ao seguinte:

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Esses erros (com códigos de erro de CS008-009 e CS012-002) indicam que a pesquisa de conteúdo não pôde ser pesquisar em locais específicos de conteúdo; Neste exemplo, duas caixas de correio não foram pesquisadas. Esses erros são exibidos na página status detalhes submenu da pesquisa conteúdo.

## <a name="cause-of-content-location-errors"></a>Causa de erros de localização do conteúdo

Quando um grande número de caixas de correio de recursos de pesquisa, a pesquisa é distribuída entre milhares de servidores em um datacenter da Microsoft. A qualquer momento, os servidores específicos poderia ser em estado de reinicialização ou no processo de failover para cópias redundantes. Em qualquer um desses casos, a solicitação de pesquisa de conteúdo para recuperar dados atinja o tempo limite. No exemplo anterior, os erros para as caixas de correio que falharam eram o resultado do cronograma do pesquisa check-out.

## <a name="resolving-content-location-errors"></a>Resolvendo erros de localização do conteúdo

Reiniciando a pesquisa frequentemente resultará em erros semelhantes em servidores diferentes. Em vez de reiniciar a pesquisa, clique no botão **de repetição** é exibido na parte superior da página de resultados da pesquisa.

![Clique no botão de repetição para resolver erros do local do conteúdo](media/retrycontentsearch3.png)

Isso resultará no repetindo a pesquisa somente para as caixas de correio que falharam. Quando você tentar novamente a pesquisa, os resultados foram retornados com êxito serão mantidos.

## <a name="tips-to-avoid-content-location-errors"></a>Dicas para evitar erros de localização do conteúdo

Aqui estão algumas causas de adição de erros de localização do conteúdo e algumas dicas para ajudá-lo a evitá-los ao pesquisar grandes números de caixas de correio.

- A caixa de correio que estão sendo pesquisada pode estar ocupada devido à atividade do usuário. Nesse caso, o serviço de pesquisa pode acelerar próprio para impedir que a caixa de correio ficar indisponível. Para evitar esse problema, tente executar pesquisas durante o horário não comercial.

- A consulta de pesquisa pode ser muito conteúdo recuperação da caixa de correio. Se possível, tente restringir o escopo da pesquisa usando palavras-chave, intervalos de data e condições de pesquisa.

- Muitas palavras-chave ou frases de palavra-chave quando você cria uma consulta de pesquisa usando a [lista de palavras-chave](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Quando você executa uma consulta de pesquisa que usa a lista de palavras-chave, o serviço executa essencialmente uma pesquisa separado para cada linha na lista de palavra-chave, para que as estatísticas podem ser geradas. Se você estiver usando a lista de palavras-chave em consultas de pesquisa, minimizar o número de linhas na lista de palavra-chave ou dividir as palavras-chave números em listas menores e criar uma pesquisa de diferente para cada lista de palavra-chave.

  > [!NOTE]
  > Para ajudar a reduzir problemas causados por palavra-chave grandes listas, agora você está limitado a um máximo de 20 linhas na lista de palavra-chave de uma consulta de pesquisa.

- Número excessivo de pesquisas estão sendo executadas na mesma caixa de correio ao mesmo tempo. Se possível, tente executar uma pesquisa por vez em uma caixa de correio.

- Pesquisando o excesso de caixas de correio em uma única pesquisa. A probabilidade de erros de localização do conteúdo aumenta ao pesquisar um número muito grande de caixas de correio. Se possível, tente executar várias pesquisas de forma que cada pesquisa inclui um subconjunto de caixas de correio em sua organização.

- Manutenção necessária está sendo executada na caixa de correio. Embora essa causa provavelmente ocorre raramente, espere um pouco enquanto depois de receber o erro de local de conteúdo e tente novamente a pesquisa.
