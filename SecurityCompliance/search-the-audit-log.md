---
title: Pesquisar o log de auditoria para a atividade de usuário e administrador no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'O log de auditoria do Office 365 é um log de auditoria unificado. Por que um log de auditoria unificado? Como os eventos da maioria dos serviços do Office 365 que você é assinante são registrados em um único log de auditoria que você pode pesquisar. Isso significa que você pode pesquisar o usuário e a atividade de administrador nesses serviços:'
ms.openlocfilehash: d964a1404dd022ba9b56e5d86766c5fc6eabf10a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265853"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="ecc83-106">Pesquisar o log de auditoria para a atividade de usuário e administrador no Office 365</span><span class="sxs-lookup"><span data-stu-id="ecc83-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="ecc83-107">O log de auditoria do Office 365 é um log de auditoria unificado.</span><span class="sxs-lookup"><span data-stu-id="ecc83-107">The Office 365 audit log is a unified audit log.</span></span> <span data-ttu-id="ecc83-108">Por que um log de auditoria unificado?</span><span class="sxs-lookup"><span data-stu-id="ecc83-108">Why a unified audit log?</span></span> <span data-ttu-id="ecc83-109">Como os eventos da maioria dos serviços do Office 365 que você é assinante são registrados em um único log de auditoria que você pode pesquisar.</span><span class="sxs-lookup"><span data-stu-id="ecc83-109">Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search.</span></span> <span data-ttu-id="ecc83-110">Isso significa que você pode pesquisar o usuário e a atividade de administrador nesses serviços:</span><span class="sxs-lookup"><span data-stu-id="ecc83-110">That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="ecc83-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="ecc83-111">SharePoint</span></span>
- <span data-ttu-id="ecc83-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="ecc83-112">OneDrive</span></span>
- <span data-ttu-id="ecc83-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="ecc83-113">Exchange</span></span>
- <span data-ttu-id="ecc83-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ecc83-114">Azure Active Directory</span></span>
- <span data-ttu-id="ecc83-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ecc83-115">Microsoft Teams</span></span>
- <span data-ttu-id="ecc83-116">Descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="ecc83-116">eDiscovery</span></span>
- <span data-ttu-id="ecc83-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="ecc83-117">Power BI</span></span>
- <span data-ttu-id="ecc83-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="ecc83-118">Yammer</span></span>
- <span data-ttu-id="ecc83-119">Sway</span><span class="sxs-lookup"><span data-stu-id="ecc83-119">Sway</span></span>
- <span data-ttu-id="ecc83-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="ecc83-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="ecc83-121">Configurar a auditoria</span><span class="sxs-lookup"><span data-stu-id="ecc83-121">Set up auditing</span></span>
  
<span data-ttu-id="ecc83-122">Há algumas coisas que você precisa fazer antes de Pesquisar o log de auditoria do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ecc83-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="ecc83-123">[Ativar a pesquisa de log de auditoria](turn-audit-log-search-on-or-off.md) para iniciar a gravação de eventos que podem ser pesquisados</span><span class="sxs-lookup"><span data-stu-id="ecc83-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="ecc83-124">[Habilitar a auditoria de caixa de correio](enable-mailbox-auditing.md) para que você possa procurar eventos relacionados à caixa de correio; como quando um usuário entra na caixa de correio ou exclui itens da pasta itens recuperáveis</span><span class="sxs-lookup"><span data-stu-id="ecc83-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="ecc83-125">Pesquisar o log de auditoria</span><span class="sxs-lookup"><span data-stu-id="ecc83-125">Search the audit log</span></span>
  
<span data-ttu-id="ecc83-126">Depois de ativar a auditoria, você pesquisa centenas de tipos individuais de eventos de vários serviços do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ecc83-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="ecc83-127">[Pesquisar o log de auditoria](search-the-audit-log-in-security-and-compliance.md) para atividades de usuário e de administrador</span><span class="sxs-lookup"><span data-stu-id="ecc83-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="ecc83-128">[Entender as propriedades detalhadas](detailed-properties-in-the-office-365-audit-log.md) em cada registro de auditoria incluído nos resultados da pesquisa</span><span class="sxs-lookup"><span data-stu-id="ecc83-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="ecc83-129">[Pesquisa de atividades relacionadas à descoberta eletrônica](search-for-ediscovery-activities-in-the-audit-log.md) realizadas por administradores e gerentes de conformidade</span><span class="sxs-lookup"><span data-stu-id="ecc83-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
