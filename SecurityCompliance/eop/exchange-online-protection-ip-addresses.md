---
title: Endereços de IP do Exchange Online Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Os seguintes endereços IP do data center da Microsoft são usados pela Proteção do Exchange Online da Microsoft (EOP) ao enviar e receber emails, ou para o portal de Proteção do Exchange Online e serviços administrativos. Para enviar e receber mensagens do EOP ou para usar serviços administrativos, verifique se sua rede permite conexões desses endereços IP.
ms.openlocfilehash: 1b5dad69fb300f36bc94c9d264492f9c9be8948f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026318"
---
# <a name="exchange-online-protection-ip-addresses"></a>Endereços de IP do Exchange Online Protection

Os seguintes endereços IP do data center da Microsoft são usados pela Proteção do Exchange Online da Microsoft (EOP) ao enviar e receber emails, ou para o portal de Proteção do Exchange Online e serviços administrativos. Para enviar e receber mensagens do EOP ou para usar serviços administrativos, verifique se sua rede permite conexões desses endereços IP.
 
> [!NOTE]
> A Microsoft está desenvolvendo um serviço web baseado em REST para o endereço IP e as entradas de FQDN nesta página. Esse novo serviço ajudará você a configurar e atualizar os dispositivos de perímetro de rede, como firewalls e servidores proxy. Você pode baixar a lista de pontos de extremidade, a versão atual da lista, ou alterações específicas. Esse serviço eventualmente substituirão o documento XML, RSS feed e o endereço IP e as entradas de FQDN nesta página. Para testar esse novo serviço, vá para o [serviço Web](https://support.office.com/article/managing-office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#webservice). 
 
## <a name="eop-ip-address-ranges"></a>Intervalos de endereços IP do EOP

O exemplo a seguir é uma lista completa de intervalos de endereços IP do EOP a partir de **2/7/2018**. 

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
> Os intervalos de endereços IP fornecidos aqui são usados somente para retransmissão por meio de conectores de cliente. Alterações feitas na lista de endereços IP são raras e são comunicadas com antecedência. Para garantir que mensagens enviadas para seus parceiros de negócios, um host inteligente ou uma rota de ambiente no local através do serviço publicado intervalo de endereços IP, você deve configurar o conector correto para o roteamento para cada destino. Para obter mais informações sobre conectores, consulte [Decidir qual conector a ser usado](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). os endereços de IP neste tópico podem mudar ao longo do tempo. Para um registro de IP de todos os endereços que foram adicionados, alterados ou preteridos no ano passado, consulte a [notificação de alteração de endereços IP do EOP](change-notification-for-eop-ip-addresses.md). 
 
Para obter informações sobre endereços IP usados pela Microsoft Office 365, consulte [URLs e intervalos de endereço IP do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=324165).
 
## <a name="ip-ranges-by-region"></a>Intervalos IP por região

O Exchange Online Protection faz o roteamento dos emails da maneira mais eficiente, mantendo a conformidade com nossas obrigações contratuais para com nossos clientes. Nesse contexto, os pontos de extremidade do EOP abaixo são a lista atual de intervalos de IPv4 regionais; no entanto, esses endereços IP podem ser provisionados novamente, sem aviso prévio, para outra função dentro do EOP, a fim de dar suporte à capacidade e à eficiência. Nesses eventos, os emails ainda continuam em fluxo com base em nossas obrigações contratuais e faremos o melhor possível para atualizar essa lista de pontos de extremidade em tempo hábil, após a realização das alterações. Nesse momento, não mantemos listas de pontos de extremidade regionais para outras partes do Office 365.
 
||||
|:-----|:-----|:-----|
|**Américas** <br/> |**EMEA** <br/> |**APAC** <br/> |
| 23.103.132.0/22 | 23.103.132.0/22 |23.103.136.0/21 |
| 23.103.136.0/21 | 23.103.144.0/22 |23.103.152.0/22 |
| 23.103.148.0/22 | 40.92.0.0/18 |40.92.128.0/17 |
| 23.103.152.0/21 | 40.93.0.0/18 |40.93.128.0/17 |
| 23.103.156.0/22 | 40.94.0.0/18 |40.94.128.0/17 |
| 23.103.198.0/24 | 40.95.0.0/18 |40.95.128.0/17 |
| 23.103.200.0/22 | 40.107.0.0/18 |52.100.128.0/17 |
| 40.92.64.0/18 | 52.100.0.0/18 |52.101.128.0/17 |
| 40.93.64.0/18 | 52.101.0.0/18 |52.102.128.0/17 |
| 40.94.64.0/18 | 52.102.0.0/18 |52.103.128.0/17 |
| 40.95.64.0/18 | 52.103.0.0/18 |65.55.88.0/24 |
| 40.107.64.0/18 | 94.245.120.64/27 |104.47.64.0/18 |
| 52.100.64.0/18 | 104.47.0.0/19 |2a01:111:f400:7 c 00::/ / 54 |
| 52.101.64.0/18 | 157.55.234.0/24 |  |
| 52.102.64.0/18 | 157.56.112.0/24 | |
| 52.103.64.0/18 | 213.199.154.0/24 | |
| 65.55.169.0/24 | 213.199.180.128/26 | |
| 104.47.32.0/19 | 2a01:111:f400:7e00::/ / 56 | |
| 157.56.110.0/23 | 2a01:111:f400:fe00::/ / 56 | |
| 207.46.100.0/24 |  | |
| 207.46.163.0/24 |  | |
| 216.32.180.0/23 |  | |
| 2a01:111:f400:7 c 00::/ / 54 |  | |
||||
