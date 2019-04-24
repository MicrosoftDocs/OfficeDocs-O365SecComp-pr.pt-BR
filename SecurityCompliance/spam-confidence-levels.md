---
title: Níveis de confiança de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
ms.openlocfilehash: 48ca02bf3f6549c5acc1147ea477b9d22f1c76e1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260669"
---
# <a name="spam-confidence-levels"></a>Níveis de confiança de spam

Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
  
|**Classificação SCL**|**Interpretação de confiança de spam**|**Ação padrão**|
|:-----|:-----|:-----|
|-1|Não spam proveniente de um remetente seguro, de um destinatário seguro ou de um endereço IP listado (parceiro confiável).|Entregar a mensagem para a caixa de entrada do destinatário.|
|0, 1|Não spam porque a mensagem foi examinada e determinada como limpa.|Entregar a mensagem para a caixa de entrada do destinatário.|
|5, 6|Spam|Entregar a mensagem na pasta Lixo Eletrônico do destinatário.|
|7, 8, 9|Spam de alta confiança|Entregar a mensagem na pasta Lixo Eletrônico do destinatário.|
   
> [!TIP]
> As classificações SCL 2, 3, 4, 7 e 8 não são definidas pelo serviço. Uma classificação SCL 5 ou 6 é considerada como spam suspeito, que é menos provável de ser um spam do que uma classificação 9, considerada como determinado spam. Ações diferentes para spam e spam de alta confiança pode ser configuradas via políticas de filtro de conteúdo no Centro de administração do Exchange. Para saber mais, confira [Configure your spam filter policies](configure-your-spam-filter-policies.md). Você também pode definir a classificação de SCL para mensagens que correspondem a condições específicas usando regras de fluxo de emails (também conhecidas como regras de transporte), conforme descrito em [usar regras de fluxo de emails para definir o nível de confiança de spam (SCL) em mensagens](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Se você usar uma regra de fluxo de emails para definir SCL de 7, 8 ou 9, a mensagem será tratada como spam de alta confiança. 
  
||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning.|
   

