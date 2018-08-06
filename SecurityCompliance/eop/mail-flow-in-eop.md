---
title: Fluxo de emails no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/13/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Como um cliente do Proteção do Exchange Online (EOP), todas as mensagens enviadas para sua organização passam através de EOP antes que seus funcionários as vejam. Se você hospedar todas as suas caixas de correio na nuvem com o Exchange Online, ou se você hospedar suas caixas de correio no local (cenário autônomo), talvez para continuar aproveitando sua infraestrutura existente, você tem opções sobre como encaminhar mensagens que passarão pelo EOP para processamento antes que sejam encaminhadas para as caixas de entrada dos seus funcionários.
ms.openlocfilehash: d35e6f2fdbe7bb991ebf3d766fadae34638831ef
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027338"
---
# <a name="mail-flow-in-eop"></a>Fluxo de emails no EOP

Como um cliente do Proteção do Exchange Online (EOP), todas as mensagens enviadas para sua organização passam através de EOP antes que seus funcionários as vejam. Se você hospedar todas as suas caixas de correio na nuvem com o Exchange Online, ou se você hospedar suas caixas de correio no local (cenário autônomo), talvez para continuar aproveitando sua infraestrutura existente, você tem opções sobre como encaminhar mensagens que passarão pelo EOP para processamento antes que sejam encaminhadas para as caixas de entrada dos seus funcionários.
  
Você pode querer configurar o encaminhamento de email padrão para que seu serviço de mensagens atenda a um requisito comercial. Por exemplo, você pode passar todos os seus emails de saída através de um dispositivo de filtragem de política. 
  
## <a name="working-with-messages-and-message-access-options"></a>Trabalhando com mensagens e opções de acesso a mensagens

O EOP oferece muita flexibilidade no modo como suas mensagens são encaminhadas. Os tópicos a seguir explicam as etapas no processo de fluxo de email.
  
[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Descreve o recurso Bloqueio de Borda Baseado em Diretório, que permite rejeitar mensagens para destinatários inválidos no perímetro da rede de serviço. 
  
[View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx) descreve como gerenciar domínios que são associados ao seu serviço EOP. 
  
Se você adicionar subdomínios à sua organização, o serviço do EOP poderá ajudá-lo a gerenciá-los também. Saiba mais sobre subdomínios em [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).
  
[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) apresenta conectores de EOP e mostra como você pode usá-los para personalizar o roteamento de email. Os cenários incluem garantir uma comunicação segura com uma organização parceira e configurar um host inteligente. 
  
Para garantir que o lixo eletrônico é roteado corretamente a pasta de lixo eletrônico de cada usuário, você deve executar algumas etapas de configuração. Eles são detalhados na [Certifique-se de que o spam é roteado para a pasta de lixo eletrônico de cada usuário](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Se você não quiser mover mensagens para a pasta de lixo eletrônico de cada usuário, você pode escolher outra ação por meio da edição suas políticas de filtro de conteúdo no Centro de administração do Exchange. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](../configure-your-spam-filter-policies.md).
  
## <a name="verify-mail-flow"></a>Verificar fluxo de mensagens

Para verificar se a sua instalação do EOP, incluindo a configuração de conectores, está funcionando corretamente, consulte a seção "Como saber se esta tarefa funcionou?" em [Configurar seu serviço EOP](set-up-your-eop-service.md). 
  
[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) fornece instruções para testar se seu fluxo de email está configurado corretamente. 
  

