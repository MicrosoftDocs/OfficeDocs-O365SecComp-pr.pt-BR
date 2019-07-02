---
title: API da Atividade de Gerenciamento do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Um breve resumo sobre a API da atividade de gerenciamento do Office 365.
ms.openlocfilehash: 759a8c7035c02ddf17d18080629a715a5525c4d6
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622501"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="88a05-103">API da Atividade de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="88a05-103">Office 365 Management Activity API</span></span>

<span data-ttu-id="88a05-104">A Microsoft fornece o Reporting Services que você pode usar para obter informações transacionais agregadas sobre o locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="88a05-104">Microsoft provides reporting services you can use to obtain aggregated transactional information about your Office 365 tenant.</span></span> <span data-ttu-id="88a05-105">A [API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) usa um design RESTful padrão da indústria e o OAuth v2 para autenticação.</span><span class="sxs-lookup"><span data-stu-id="88a05-105">The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication.</span></span> <span data-ttu-id="88a05-106">Isso facilita a tarefa de começar a experimentar a recuperação de dados e a inclusão em ferramentas e aplicativos de visualização.</span><span class="sxs-lookup"><span data-stu-id="88a05-106">This makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications.</span></span> <span data-ttu-id="88a05-107">A API fornece um feed de dados com informações sobre o usuário, administrador, operações e atividade de segurança no Office 365.</span><span class="sxs-lookup"><span data-stu-id="88a05-107">The API provides a data feed with information about user, administrator, operations, and security activity in Office 365.</span></span> <span data-ttu-id="88a05-108">Os dados podem ser mantidos por razões regulamentares ou combinados com os dados de log obtidos de uma infraestrutura local ou de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="88a05-108">The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources.</span></span> <span data-ttu-id="88a05-109">Isso ajuda a criar uma solução de monitoramento para operações, segurança e conformidade em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="88a05-109">This helps build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="88a05-110">A API da Atividade de Gerenciamento do Office 365 fornece informações sobre várias ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88a05-110">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="88a05-111">A API fornece um esquema de auditoria consistente com mais de 10 campos comuns em todos os serviços.</span><span class="sxs-lookup"><span data-stu-id="88a05-111">The API provides a consistent audit schema with over 10 fields common across all the services.</span></span> <span data-ttu-id="88a05-112">A API permite que as organizações façam conexões fáceis entre eventos e permite que as novas maneiras de fazer isso nos dados.</span><span class="sxs-lookup"><span data-stu-id="88a05-112">The API allows organizations to make easy connections between events, and enables new ways to reason over the data.</span></span>

<span data-ttu-id="88a05-113">Dezenas de ISVs (fornecedores independentes de software) parceiros com a Microsoft e criaram soluções com base na API.</span><span class="sxs-lookup"><span data-stu-id="88a05-113">Dozens of Independent Software Vendors (ISVs) partnered with Microsoft and have built solutions based on the API.</span></span> <span data-ttu-id="88a05-114">Algumas soluções se concentram exclusivamente nos dados do Office 365 e outros dados de origem de vários provedores de nuvem e sistemas locais para criar uma visão unificada das operações, segurança e atividade relacionada à conformidade.</span><span class="sxs-lookup"><span data-stu-id="88a05-114">Some solutions focus solely on Office 365 data and others source data from multiple cloud providers and on-premises systems to create a unified view of operations, security, and compliance-related activity.</span></span> 

<span data-ttu-id="88a05-115">Para obter mais informações, consulte a [referência da API da atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="88a05-115">For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
