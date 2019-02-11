---
title: Email threading
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d4328971a6b13c60c4d8b9f5b6db310d72a5b215
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29705992"
---
# <a name="email-threading"></a>Email threading

Considere a possibilidade de uma conversa de email acontecendo por algum tempo. Na maioria dos casos, o último email no thread incluirá o conteúdo de todos os emails anteriores; analisar o último email fornecerá um contexto completo da conversa que ocorreram no segmento. Email threading identifica tais emails para que os revisores podem revisar uma fração de documentos coletados sem perder nenhum contexto.

## <a name="what-does-email-threading-do"></a>O que faz threading de email?

Email threading analisa cada email e desconstructs-la para mensagens individuais; cada email é uma cadeia de mensagens individuais. Em seguida, ele analisa todos os emails no conjunto de trabalho para determinar se um email tem conteúdo exclusivo ou se a cadeia está totalmente contida em um email diferente. No final emails são divididos em quatro categorias:

- **Inclusiva**: a última mensagem no email possui conteúdo exclusivo e o email tem todos os anexos que foram incluídos em outras emails dos quais o conteúdo está totalmente contido neste email.


- **Inclusiva menos**: a última mensagem no email tem conteúdo exclusivo, mas o email não contém alguns dos anexos que foram incluídos em outras emails dos quais o conteúdo está totalmente contido neste email.

- **Inclusive cópia**: uma cópia exata de um inclusive/inclusive menos email

- **None**: O conteúdo deste e-mail está totalmente contido em pelo menos um email que está marcado como inclusive inclusive subtração.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Como ele é diferente do conversas no Outlook?
Em um relance, isso sons bastante similar às agrupamentos de conversa no Outlook. No entanto, há algumas distinções importantes. Considere a possibilidade de uma conversa de email que receber bifurcada em dois conversa; Por exemplo, alguém respondeu a um email que não seja as informações mais recentes na conversa para que os duas últimas emails na conversa que ambos tenham o conteúdo exclusivo.

Outlook ainda seria agrupar os e-mails em uma única conversa; ler somente o último email significaria faltando o contexto do segundo recente e-mail, que também contém conteúdo exclusivo. Porque o email threading analisa check-out de cada email em componentes individuais e os compara, email threading seria marcar ambas os duas últimas emails como inclusives, garantindo que você não perca nenhum contexto desde que você leia todos os e-mails marcados como inclusive.