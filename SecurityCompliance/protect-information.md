---
title: Proteger informações
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/26/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: página de aterrissagem para proteção de informações
ms.openlocfilehash: 1c673c2417b399c57ca7ac7e5c5a7b7351de1edd
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33472990"
---
# <a name="protect-information"></a>Proteger informações

O Microsoft 365 e o Office 365 incluem recursos que podem ser aplicados a tipos específicos de dados para proteger as informações. 


|**Funcionalidade**|**Mais informações**|
|:-----|:-----|
|[Rótulos de confidencialidade](sensitivity-labels.md) <br/> |Com rótulos de confidencialidade, você pode classificar e ajudar a proteger o conteúdo confidencial. As opções de proteção incluem rótulos, marcas d' água e criptografia. Os rótulos de confidencialidade usam a proteção de informações do Azure. Se você estiver usando os rótulos de proteção de informações do Azure, por ora, recomendamos que você evite criar novos rótulos em outros centros de Administração até concluir a migração. ConFira [migração de proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> Os [Rótulos de retenção](retention-policies.md) são diferentes dos rótulos de confidencialidade. Os rótulos de retenção ajudam você a reter ou excluir o conteúdo com base em políticas definidas por você. Essas organizações ajudam a cumprir as normas do setor e as políticas internas.|
|[Prevenção contra perda de dados](data-loss-prevention-policies.md) DLP  <br/> |Com as políticas de DLP, você pode identificar, monitorar e proteger automaticamente as informações confidenciais no Office 365. As políticas de prevenção contra perda de dados podem usar rótulos de confidencialidade e tipos de informações confidenciais para identificar informações confidenciais. <br/> |
|[Tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md)  <br/> |O DLP inclui muitos tipos de informações confidenciais que estão prontos para serem usados em políticas de DLP. Os tipos de informações confidenciais definem como o processo automatizado reconhece tipos de informações específicos, como números de serviço de integridade e números de cartão de crédito.   <br/> |
|[Criptografia de mensagem do Office 365](ome.md) OME  <br/> |Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas dentro e fora da sua organização. A criptografia de mensagem do Office 365 funciona com o Outlook.com, Yahoo!, Gmail e outros serviços de email. A criptografia de mensagens de email ajuda a garantir que somente os destinatários pretendidos possam exibir o conteúdo da mensagem.  <br/> |
|[Proteção de Informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Se você estiver usando rótulos de sensibilidade ou criptografia de mensagem do Office, você já está usando a proteção de informações do Azure. Se você ainda não tiver migrado os rótulos de proteção de informações do Azure para o Office 365, continue a gerenciá-los na proteção de informações do Azure.  <br/>O [verificaDor de proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) pode ser executado no local para classificar e proteger arquivos no Windows Server, compartilhamentos de rede e bibliotecas e sites do SharePoint Server. Isso pode ser uma primeira etapa para identificar dados para migrar para o Office 365.
|Proteção de informações do Azure com soluções do BYOK ou do HYOK <br/> |Algumas organizações têm uma necessidade de negócios ou requisito de conformidade para manter o controle de uma chave do encyption no local ou na nuvem. Isso não é comum. Para saber mais, confira [reter sua própria chave (HYOK) para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions) e [traga sua chave (BYOK) para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). <br/> |
    

