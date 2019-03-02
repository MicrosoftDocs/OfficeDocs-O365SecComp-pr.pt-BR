---
title: Integração do SIEM com o Office 365 Threat Intelligence e proteção avançada contra ameaças
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.collection:
- M365-security-compliance
description: Integre o servidor SIEM da sua organização com o Office 365 Threat Intelligence e proteção avançada contra ameaças com a API de gerenciamento de atividades do Office 365.
ms.openlocfilehash: 68d2b4387c1af2363fbb67d0671edeaaa4dc652d
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357432"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="2b2ad-103">Integração do SIEM com o Office 365 Threat Intelligence e proteção avançada contra ameaças</span><span class="sxs-lookup"><span data-stu-id="2b2ad-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="2b2ad-p101">Se sua organização estiver usando um servidor de gerenciamento de incidentes e eventos de segurança (SIEM), você poderá integrar o Office 365 Threat Intelligence e a proteção avançada contra ameaças ao seu servidor SIEM. A integração do SIEM permite que você visualize informações, como malware detectado pelo Office 365 Advanced Protection and Threat Intelligence, em seus relatórios do SIEM Server. Para configurar a integração do SIEM, use a [API de gerenciamento de atividades do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="2b2ad-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="2b2ad-p102">A API de gerenciamento de atividades do Office 365 recupera informações sobre ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory da sua organização. O [esquema de proteção avançada contra ameaças e inteligência](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) contra ameaças do Office 365 funciona com inteligência de ameaças e/ou proteção avançada contra ameaças, portanto, se sua organização tiver proteção avançada contra ameaças, mas não inteligência de ameaças (ou vice-versa), você poderá ainda use essa mesma API para sua integração com o servidor do SIEM.</span><span class="sxs-lookup"><span data-stu-id="2b2ad-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="2b2ad-p103">O servidor SIEM ou outro sistema semelhante deve sondar a **auditoria.** carga de trabalho geral para acessar eventos de detecção. Para saber mais, confira [introdução às APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="2b2ad-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2b2ad-111">Você deve ser um administrador global do Office 365 ou ter a função de administrador de segurança atribuída para o centro de conformidade do & de segurança para configurar a integração do SIEM com a proteção avançada contra ameaças do Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b2ad-111">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="2b2ad-p104">O log de auditoria deve estar ativado para o seu ambiente do Office 365. Para obter ajuda com isso, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="2b2ad-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b2ad-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b2ad-114">Related topics</span></span>

[<span data-ttu-id="2b2ad-115">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b2ad-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

<span data-ttu-id="2b2ad-116">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="2b2ad-116">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>

[<span data-ttu-id="2b2ad-117">Relatórios inteligentes e insights no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b2ad-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="2b2ad-118">Permissões no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b2ad-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

