---
title: Endereços de IP do Exchange Online Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Os seguintes endereços IP do data center da Microsoft são usados pela Proteção do Exchange Online da Microsoft (EOP) ao enviar e receber emails, ou para o portal de Proteção do Exchange Online e serviços administrativos. Para enviar e receber mensagens do EOP ou para usar serviços administrativos, verifique se sua rede permite conexões desses endereços IP.
ms.openlocfilehash: 6c7d8c78a012be3928317eac1e9b6fcdeab64a24
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222820"
---
# <a name="exchange-online-protection-ip-addresses"></a>Endereços de IP do Exchange Online Protection

Os seguintes endereços IP do data center da Microsoft são usados pela Proteção do Exchange Online da Microsoft (EOP) ao enviar e receber emails, ou para o portal de Proteção do Exchange Online e serviços administrativos. Para enviar e receber mensagens do EOP ou para usar serviços administrativos, verifique se sua rede permite conexões desses endereços IP.
 
> [!NOTE]
> A Microsoft desenvolveu um serviço Web baseado em REST para as entradas de endereço IP e FQDN nesta página. Este novo serviço ajuda você a configurar e atualizar dispositivos de perímetro de rede, como firewalls e servidores proxy. Você pode baixar a lista de pontos de extremidade, a versão atual da lista ou alterações específicas. Este serviço substitui o documento XML, o RSS feed e as entradas de endereço IP e FQDN nesta página. Para experimentar esse novo serviço, vá para o [endereço IP do Office 365 e o serviço Web de URL](https://docs.microsoft.com/office365/enterprise/office-365-ip-web-service). 
 
## <a name="eop-ip-address-ranges"></a>Intervalos de endereços IP do EOP

||||
|:-----|:-----|:-----|
|**Intervalos de endereços IPv4** <br/> |**Intervalos de endereços IPv6** <br/> |
| 23.103.132.0/22 | 2a01:111: F400:7c00:/! 54 |
| 23.103.136.0/21 | 2a01:111: F400: fc00:/! 54 |
| 23.103.144.0/20 | 2a01:111: f403::/48 |
| 23.103.198.0/23 |  |
| 23.103.200.0/22 |  |
| 40.92.0.0/14 |  |
| 40.107.0.0/17 |  |
| 52.100.0.0/14 |  |
| 52.238.78.88/32 |  |
| 65.55.88.0/24 |  |
| 65.55.169.0/24 |  |
| 94.245.120.64/26 |  |
| 104.47.0.0/17 |  |
| 157.55.234.0/24 |  |
| 157.56.110.0/23 |  |
| 157.56.112.0/24 |  |
| 207.46.100.0/24 |  |
| 207.46.163.0/24 |  |
| 213.199.154.0/24 |  |
| 213.199.180.128/26 |  |
| 216.32.180.0/23 |  |
||||
 
> [!IMPORTANT]
> Os intervalos de endereços IP fornecidos aqui são usados apenas para retransmissão por meio de conectores do cliente. As alterações na lista de endereços IP são raras e são comunicadas com antecedência. Para garantir que as mensagens enviadas para seus parceiros comerciais, um host inteligente ou um ambiente local circulem o intervalo de endereços IP do serviço publicado, você deve configurar o conector correto para roteamento para cada destino. Para obter mais informações sobre conectores, consulte [decidir qual conector usar](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). os endereços IP neste tópico podem mudar com o tempo.  
 
Para obter informações sobre endereços IP usados pela Microsoft Office 365, consulte [URLs e intervalos de endereço IP do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=324165).

