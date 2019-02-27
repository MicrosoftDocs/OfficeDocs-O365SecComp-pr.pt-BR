---
title: Níveis de confiança de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275641"
---
# <a name="spam-confidence-levels"></a>Níveis de confiança de spam

Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
  
|**Classificação SCL**|**Interpretação de confiança de spam**|**Ação padrão**|
|:-----|:-----|:-----|
|-1  <br/> |Não spam vindo de um remetente seguro, destinatário seguro ou endereço IP listado seguro (parceiro confiável)  <br/> |Entregar a mensagem para a caixa de entrada do destinatário.  <br/> |
|0, 1  <br/> |Não spam porque a mensagem foi verificada e considerada como limpa  <br/> |Entregar a mensagem para a caixa de entrada do destinatário.  <br/> |
|5, 6  <br/> | Spam  <br/> |Entregar a mensagem na pasta Lixo Eletrônico do destinatário.  <br/> |
|7, 8, 9  <br/> |Spam de alta confiança  <br/> |Entregar a mensagem na pasta Lixo Eletrônico do destinatário.  <br/> |
   
> [!TIP]
> As classificações de SCL de 2, 3, 4, 7 e 8 não são definidas pelo serviço. Uma classificação de SCL de 5 ou 6 é considerada um spam suspeito, que é menos certo de ser spam do que a classificação de SCL 9, que é considerada determinados spam. Ações diferentes para spam e spam de alta confiança podem ser configuradas por meio de políticas de filtro de conteúdo no centro de administração do Exchange. Para obter mais informações, consulte [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Você também pode definir a classificação de SCL para mensagens que correspondem a condições específicas usando regras de transporte, conforme descrito em [usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Se você usar uma regra de transporte para definir SCL de 7, 8 ou 9, a mensagem será tratada como spam de alta confiança. 
  
||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning. |
   

