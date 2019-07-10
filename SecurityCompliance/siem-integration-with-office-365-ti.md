---
title: Integração do SIEM com a proteção avançada contra ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: Integre o servidor SIEM da sua organização com a proteção avançada contra ameaças do Office 365 e eventos de ameaça relacionados na API de gerenciamento de atividades do Office 365.
ms.openlocfilehash: 4bfc82be273bb4581aa49bbbbdab613bd87b1b89
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600898"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="ac1ae-103">Integração do SIEM com a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1ae-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="ac1ae-104">Se sua organização estiver usando um servidor de gerenciamento de incidentes e eventos de segurança (SIEM), você poderá integrar a proteção avançada contra ameaças do Office 365 ao seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="ac1ae-105">A integração do SIEM permite que você visualize informações, como malware ou phishing detectado pela proteção avançada do Office 365, em seus relatórios do SIEM Server.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="ac1ae-106">Para configurar a integração do SIEM, use a [API de gerenciamento de atividades do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="ac1ae-107">A API de gerenciamento de atividades do Office 365 recupera informações sobre ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="ac1ae-108">O [esquema de proteção avançada contra ameaças do office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funciona com a proteção avançada contra ameaças, portanto, se sua organização tiver o plano de proteção avançada contra ameaças do Office 365 ou o plano 2 ou o Office 365 e5, você ainda poderá usar essa mesma API para sua integração com o Siem Server.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="ac1ae-109">O servidor SIEM ou outro sistema semelhante deve sondar a **auditoria.** carga de trabalho geral para acessar eventos de detecção.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-109">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="ac1ae-110">Para saber mais, confira [introdução às APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-110">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="ac1ae-111">Além disso, os seguintes valores de **AuditLogRecordType** são relevantes para eventos de ATP do Office 365:</span><span class="sxs-lookup"><span data-stu-id="ac1ae-111">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="ac1ae-112">Enumeração: AuditLogRecordType - Tipo: Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="ac1ae-112">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="ac1ae-113">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="ac1ae-113">AuditLogRecordType</span></span>

|<span data-ttu-id="ac1ae-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ac1ae-114">Value</span></span>|<span data-ttu-id="ac1ae-115">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="ac1ae-115">Member name</span></span>|<span data-ttu-id="ac1ae-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac1ae-116">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac1ae-117">28</span><span class="sxs-lookup"><span data-stu-id="ac1ae-117">28</span></span>|<span data-ttu-id="ac1ae-118">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="ac1ae-118">ThreatIntelligence</span></span>|<span data-ttu-id="ac1ae-119">Eventos de phishing e malware da Proteção do Exchange Online e da Proteção Avançada contra Ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-119">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="ac1ae-120">41</span><span class="sxs-lookup"><span data-stu-id="ac1ae-120">41</span></span>|<span data-ttu-id="ac1ae-121">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="ac1ae-121">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="ac1ae-122">Links seguros de ATP os eventos de tempo de bloqueio e substituição de bloqueio da proteção avançada contra ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-122">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="ac1ae-123">47</span><span class="sxs-lookup"><span data-stu-id="ac1ae-123">47</span></span>|<span data-ttu-id="ac1ae-124">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="ac1ae-124">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="ac1ae-125">Eventos de phishing e malware para arquivos no SharePoint Online, no OneDrive for Business e no Microsoft Teams da proteção avançada contra ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-125">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="ac1ae-126">Você deve ser um administrador global do Office 365 ou ter a função de administrador de segurança atribuída para o centro de conformidade de & de segurança para configurar a integração do SIEM com a proteção avançada contra ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-126">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="ac1ae-127">O log de auditoria deve estar ativado para o seu ambiente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-127">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="ac1ae-128">Para obter ajuda com isso, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-128">To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac1ae-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac1ae-129">Related topics</span></span>

[<span data-ttu-id="ac1ae-130">Investigação e resposta contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1ae-130">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)

[<span data-ttu-id="ac1ae-131">Proteção Avançada contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1ae-131">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="ac1ae-132">Relatórios inteligentes e insights no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1ae-132">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="ac1ae-133">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="ac1ae-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  
