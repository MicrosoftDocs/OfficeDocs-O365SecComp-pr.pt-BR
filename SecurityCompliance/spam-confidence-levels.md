---
title: Níveis de confiança de spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
description: Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
ms.openlocfilehash: cd33f440828761ab8cb496d9eff07288d974514c
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026278"
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
> Classificações de SCL de 2, 3, 4, 7 e 8 não são definidas pelo serviço. Uma classificação de SCL de 5 ou 6 é considerada spam suspeito, o que é o menor determinado como spam que uma classificação de SCL de 9, que é considerada determinado spam. Ações diferentes de spam e spam de alta confiabilidade podem ser configuradas por meio de suas políticas de filtro de conteúdo no Centro de administração do Exchange. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Você também pode definir a classificação de SCL para mensagens que correspondam às condições específicas usando regras de transporte, conforme descrito em [usar regras de fluxo de email para definir o nível de confiança de spam (SCL) em mensagens](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Se você usar uma regra de transporte para definir o SCL de 7, 8 ou 9 a mensagem será tratada como spam de alta confiabilidade. 
  
||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning. |
   

