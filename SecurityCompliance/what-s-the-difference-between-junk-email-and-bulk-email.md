---
title: Qual é a diferença entre lixo eletrônico e email em massa?
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
description: Os clientes às vezes askwhat da diferença entre lixo eletrônico e mensagens de email em massa? O objetivo deste tópico é explicar a diferença e fornecem informações sobre as diferentes opções disponíveis para ambos no Exchange Online e Exchange Online Protection (EOP).
ms.openlocfilehash: 87f946c7309589595efd3e11e998e0a9f503b651
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003150"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a>Qual é a diferença entre lixo eletrônico e email em massa?

Às vezes, os clientes perguntam "qual é a diferença entre lixo eletrônico e mensagens de email em massa?" O objetivo deste tópico é explicar a diferença e fornecer informações sobre as várias opções disponíveis no Exchange Online e no Proteção do Exchange Online (EOP).
  
 **O que é lixo eletrônico?**
  
As mensagens de lixo eletrônico são mensagens de "spam", significando emails não solicitados (e geralmente indesejados) que são filtrados pelo serviço. Por padrão, o serviço rejeita a mensagem de spam com base na reputação do endereço IP de envio. Entretanto, se ele passa pela inspeção de IP, mas é classificado como spam pelos filtros de conteúdo, a mensagem é enviada para a pasta Lixo Eletrônico dos destinatários pretendidos. 
  
> [!NOTE]
> A ação executada em mensagens de conteúdo filtrado é configurável por meio de políticas de filtro de conteúdo no Centro de administração do Exchange (EAC), conforme descrito em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Além disso, se você concorda com a classificação de spam, é possível denunciar mensagens que você considera spam ou não spam à Microsoft de várias maneiras, conforme descrito em [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). 
  
 **O que é email em massa?**
  
Email em massa é um tipo de mensagem de email mais difícil de classificar. Embora o lixo eletrônico seja uma ameaça constante, o email em massa geralmente é composto por uma mensagem publicitária ou de marketing que, muito provavelmente, não será enviada repetidas vezes. O email em massa é de interesse de alguns usuários e, de fato, eles podem ter deliberadamente concordado em receber essas mensagens, embora outros usuários talvez considerem esse tipo de mensagem como spam. Por exemplo, alguns usuários querem receber emails publicitários da Contoso Corporation ou convites para uma conferência futura sobre segurança cibernética; já outros usuários consideram tais emails como spam.
  
## <a name="how-to-manage-bulk-email"></a>Como gerenciar o email em massa

A maneira de gerenciar o email em massa não é uma decisão clara - afinal, se todos os emails em massa forem classificados como spam, os usuários interessados poderão reclamar e enviá-los como um falso positivo (mensagem de não spam e que foi incorretamente marcada como spam). Por outro lado, se todos os emails em massa forem liberados, os usuários não interessados poderão reclamar e enviá-los como uma mensagem de spam que escapou à inspeção (falso negativo) e chegou inadvertidamente à caixa de entrada deles.
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a>Habilitar o controle de sensibilidade de email em massa na política de filtro de conteúdo

Dependendo da política da sua empresa em mensagens de email em massa, os administradores podem selecionar um limite para atribuir o email em massa. A configuração é é configurável por meio de políticas de filtro de conteúdo no EAC. Confira [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)) para as etapas. Você pode escolher uma configuração de limite de 1 a 9, onde 1 marca a maioria dos emails em massa como spam e 9 permite que a maioria dos emails em massa ao ser entregue. O serviço, em seguida, executa a ação configurada, por exemplo, enviar a mensagem para a pasta de lixo eletrônico do destinatário. 
  

