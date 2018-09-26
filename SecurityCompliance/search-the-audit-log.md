---
title: Pesquisar no log de auditoria para atividade de administrador e usuário no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'O log de auditoria do Office 365 é um log de auditoria unificada. Por que uma auditoria unificada efetuar? Porque os eventos da maioria dos serviços do Office 365 que você esteja organização pode assinar são registradas em um log de auditoria único que você pode pesquisar. Isso significa que você pode procurar por usuário e a atividade de admin nesses serviços:'
ms.openlocfilehash: 230502f331babeef8f89eacce0d19a7756cb96fc
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038024"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="e8a17-106">Pesquisar no log de auditoria para atividade de administrador e usuário no Office 365</span><span class="sxs-lookup"><span data-stu-id="e8a17-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="e8a17-p102">O log de auditoria do Office 365 é um log de auditoria unificada. Por que uma auditoria unificada efetuar? Porque os eventos da maioria dos serviços do Office 365 que você esteja organização pode assinar são registradas em um log de auditoria único que você pode pesquisar. Isso significa que você pode procurar por usuário e a atividade de admin nesses serviços:</span><span class="sxs-lookup"><span data-stu-id="e8a17-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="e8a17-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="e8a17-111">SharePoint</span></span>
- <span data-ttu-id="e8a17-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="e8a17-112">OneDrive</span></span>
- <span data-ttu-id="e8a17-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="e8a17-113">Exchange</span></span>
- <span data-ttu-id="e8a17-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8a17-114">Azure Active Directory</span></span>
- <span data-ttu-id="e8a17-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e8a17-115">Microsoft Teams</span></span>
- <span data-ttu-id="e8a17-116">Descoberta Eletrônica</span><span class="sxs-lookup"><span data-stu-id="e8a17-116">eDiscovery</span></span>
- <span data-ttu-id="e8a17-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="e8a17-117">Power BI</span></span>
- <span data-ttu-id="e8a17-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="e8a17-118">Yammer</span></span>
- <span data-ttu-id="e8a17-119">Sway</span><span class="sxs-lookup"><span data-stu-id="e8a17-119">Sway</span></span>
- <span data-ttu-id="e8a17-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="e8a17-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="e8a17-121">Configurar a auditoria</span><span class="sxs-lookup"><span data-stu-id="e8a17-121">Set up auditing</span></span>
  
<span data-ttu-id="e8a17-122">Há algumas coisas que você deve fazer antes de você pode pesquisar o log de auditoria do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8a17-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="e8a17-123">[Ativar a pesquisa de log de auditoria](turn-audit-log-search-on-or-off.md) para iniciar o registro de eventos que você pode pesquisar</span><span class="sxs-lookup"><span data-stu-id="e8a17-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="e8a17-124">[Habilitar a auditoria de caixa de correio](enable-mailbox-auditing.md) de forma que você pode pesquisar eventos relacionados à caixa de correio; como quando um usuário entra no seus itens de caixa de correio ou limpezas da sua pasta de itens recuperáveis</span><span class="sxs-lookup"><span data-stu-id="e8a17-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="e8a17-125">Pesquisas o log de auditoria</span><span class="sxs-lookup"><span data-stu-id="e8a17-125">Search the audit log</span></span>
  
<span data-ttu-id="e8a17-126">Depois que você ative a auditoria, procure centenas de individuais tipos de eventos de vários serviços do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8a17-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="e8a17-127">[Pesquisa o log de auditoria](search-the-audit-log-in-security-and-compliance.md) para atividades de administrador e usuário</span><span class="sxs-lookup"><span data-stu-id="e8a17-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="e8a17-128">[Compreender as propriedades detalhadas](detailed-properties-in-the-office-365-audit-log.md) de cada registro de auditoria incluído nos resultados da pesquisa</span><span class="sxs-lookup"><span data-stu-id="e8a17-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="e8a17-129">[Procure atividades relacionadas a descoberta eletrônica](search-for-ediscovery-activities-in-the-audit-log.md) realizada por gerentes de conformidade e administradores</span><span class="sxs-lookup"><span data-stu-id="e8a17-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
