---
title: Limites de recursos do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: informações sobre os limites de recursos para os vários aplicativos no Office 365.'
ms.openlocfilehash: ee44bde8bd93d3628ed3f31f5bbbce024a3056b5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220211"
---
# <a name="resource-limits"></a><span data-ttu-id="3fa8a-103">Limites de recurso</span><span class="sxs-lookup"><span data-stu-id="3fa8a-103">Resource Limits</span></span>

<span data-ttu-id="3fa8a-p101">Os limites de recursos são impostos usando cotas (limites) e limitação. O Azure Active Directory e os serviços individuais do Office 365 usam ambos. Os limites são específicos de serviço e mudam com o tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites atuais para os vários serviços, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3fa8a-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="3fa8a-108">Limites e restrições de serviços do Active Directory do Azure</span><span class="sxs-lookup"><span data-stu-id="3fa8a-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="3fa8a-109">Limites do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3fa8a-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="3fa8a-110">Limites do Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="3fa8a-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="3fa8a-111">Limites e limites de software do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3fa8a-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="3fa8a-112">Limites do Skype for Business</span><span class="sxs-lookup"><span data-stu-id="3fa8a-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="3fa8a-113">API REST do Yammer e limites de taxa</span><span class="sxs-lookup"><span data-stu-id="3fa8a-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="3fa8a-114">Limites de tamanho de arquivo no Sway</span><span class="sxs-lookup"><span data-stu-id="3fa8a-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="3fa8a-p102">Além desses limites, vários mecanismos de limitação são usados no Azure Active Directory e no Office 365. A limitação do serviço é especialmente importante, Considerando que os recursos de rede nos datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Os mecanismos de limitação incluem:</span><span class="sxs-lookup"><span data-stu-id="3fa8a-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="3fa8a-118">O Azure Active Directory e o Office 365 recurso de limitação de nível de usuário, que limitam o número de transações ou chamadas simultâneas (por script ou código) que podem ser realizadas por um único usuário.</span><span class="sxs-lookup"><span data-stu-id="3fa8a-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="3fa8a-p103">Uma política padrão de limitação do PowerShell é atribuída a cada locatário na criação de locatário. Essas configurações afetam outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertas por um único administrador.</span><span class="sxs-lookup"><span data-stu-id="3fa8a-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="3fa8a-121">Cada cliente do Exchange Online tem uma política de serviços Web do Exchange (EWS) padrão ajustada para operações do cliente EWS e limitação que se aplica a todos os clientes do Outlook.</span><span class="sxs-lookup"><span data-stu-id="3fa8a-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
