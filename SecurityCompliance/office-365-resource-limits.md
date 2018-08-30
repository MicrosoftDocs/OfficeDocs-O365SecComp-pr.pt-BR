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
# <a name="resource-limits"></a><span data-ttu-id="02fc3-103">Limites de recurso</span><span class="sxs-lookup"><span data-stu-id="02fc3-103">Resource Limits</span></span>

<span data-ttu-id="02fc3-p101">Limites de recursos são impostos usando cotas (limites) e limitação. Azure Active Directory e os serviços individuais do Office 365 usam ambos. Limites são específicos do serviço e inalterados ao longo do tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites de atuais para os vários serviços, consulte os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="02fc3-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="02fc3-108">Restrições e limites de serviço do Active Directory do Azure</span><span class="sxs-lookup"><span data-stu-id="02fc3-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="02fc3-109">Limites do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="02fc3-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="02fc3-110">Limites do Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="02fc3-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="02fc3-111">Limites de software do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="02fc3-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="02fc3-112">Skype dos limites corporativos</span><span class="sxs-lookup"><span data-stu-id="02fc3-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="02fc3-113">API REST de Yammer e limites de taxa</span><span class="sxs-lookup"><span data-stu-id="02fc3-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="02fc3-114">Limites de tamanho de arquivo no Sway</span><span class="sxs-lookup"><span data-stu-id="02fc3-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="02fc3-p102">Além desses limites, diversos mecanismos de limitação são usados em todo o Azure Active Directory e o Office 365. Limitação dentro do serviço é especialmente importante, visto que os recursos de rede em datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Otimização de mecanismos incluem:</span><span class="sxs-lookup"><span data-stu-id="02fc3-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="02fc3-118">Azure Active Directory e limitação de nível de usuário do recurso de Office 365, que limita o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.</span><span class="sxs-lookup"><span data-stu-id="02fc3-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="02fc3-p103">Um padrão política de limitação do PowerShell é atribuído a cada locatário na criação de locatário. Essas configurações afetam a outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertos por um único administrador.</span><span class="sxs-lookup"><span data-stu-id="02fc3-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="02fc3-121">Cada cliente Exchange Online tem uma política de serviços Web do Exchange (EWS) padrão que é ajustada para operações de cliente do EWS e limitação que se aplica a todos os clientes do Outlook.</span><span class="sxs-lookup"><span data-stu-id="02fc3-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
