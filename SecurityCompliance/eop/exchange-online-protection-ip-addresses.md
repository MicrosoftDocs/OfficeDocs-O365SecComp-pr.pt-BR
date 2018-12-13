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
ms.openlocfilehash: 5ea1a3df2ba1ea6853e2e44983fa7a97877c0778
ms.sourcegitcommit: 031781d0eecf33baabcd03ea53546d41076062b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2018
ms.locfileid: "27240504"
---
# <a name="exchange-online-protection-ip-addresses"></a>Endereços de IP do Exchange Online Protection

Os seguintes endereços IP do data center da Microsoft são usados pela Proteção do Exchange Online da Microsoft (EOP) ao enviar e receber emails, ou para o portal de Proteção do Exchange Online e serviços administrativos. Para enviar e receber mensagens do EOP ou para usar serviços administrativos, verifique se sua rede permite conexões desses endereços IP.
 
> [!NOTE]
> A Microsoft desenvolveu um serviço web baseado em REST para o endereço IP e as entradas de FQDN nesta página. Esse novo serviço ajuda você a configurar e atualizar os dispositivos de perímetro de rede, como firewalls e servidores proxy. Você pode baixar a lista de pontos de extremidade, a versão atual da lista, ou alterações específicas. Esse serviço substitui o documento XML, RSS feed e o endereço IP e as entradas de FQDN nesta página. Para testar esse novo serviço, vá para o [endereço de IP do Office 365 e o serviço Web de URL](https://docs.microsoft.com/office365/enterprise/office-365-ip-web-service). 
 
## <a name="eop-ip-address-ranges"></a>Intervalos de endereços IP do EOP

||||
|:-----|:-----|:-----|
|**Intervalos de endereços IPv4** <br/> |**Intervalos de endereços IPv6** <br/> |
| 23.103.132.0/22 | 2a01:111:f400:7 c 00::/ / 54 |
| 23.103.136.0/21 | 2a01:111:f400:fc00::/ / 54 |
| 23.103.144.0/20 | 2a01:111:f403::/ / 48 |
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
> Os intervalos de endereços IP fornecidos aqui são usados somente para retransmissão por meio de conectores de cliente. Alterações feitas na lista de endereços IP são raras e são comunicadas com antecedência. Para garantir que mensagens enviadas para seus parceiros de negócios, um host inteligente ou uma rota de ambiente no local através do serviço publicado intervalo de endereços IP, você deve configurar o conector correto para o roteamento para cada destino. Para obter mais informações sobre conectores, consulte [Decidir qual conector a ser usado](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). os endereços de IP neste tópico podem mudar ao longo do tempo.  
 
Para obter informações sobre endereços IP usados pela Microsoft Office 365, consulte [URLs e intervalos de endereço IP do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=324165).

