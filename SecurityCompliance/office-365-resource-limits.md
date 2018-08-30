---
title: Limites de recursos do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Informações sobre o recurso limita dos vários aplicativos dentro do Office 365.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524720"
---
# <a name="resource-limits"></a>Limites de recurso

Limites de recursos são impostos usando cotas (limites) e limitação. Azure Active Directory e os serviços individuais do Office 365 usam ambos. Limites são específicos do serviço e inalterados ao longo do tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites de atuais para os vários serviços, consulte os tópicos a seguir:
- [Restrições e limites de serviço do Active Directory do Azure](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [Limites do Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [Limites do Exchange Online Protection](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [Limites de software do SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype dos limites corporativos](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [API REST de Yammer e limites de taxa](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de tamanho de arquivo no Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Além desses limites, diversos mecanismos de limitação são usados em todo o Azure Active Directory e o Office 365. Limitação dentro do serviço é especialmente importante, visto que os recursos de rede em datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Otimização de mecanismos incluem:
- Azure Active Directory e limitação de nível de usuário do recurso de Office 365, que limita o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.
- Um padrão política de limitação do PowerShell é atribuído a cada locatário na criação de locatário. Essas configurações afetam a outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertos por um único administrador.
- Cada cliente Exchange Online tem uma política de serviços Web do Exchange (EWS) padrão que é ajustada para operações de cliente do EWS e limitação que se aplica a todos os clientes do Outlook.
