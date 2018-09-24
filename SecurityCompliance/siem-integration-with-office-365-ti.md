---
title: Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Integre o servidor SIEM da sua organização com inteligência de ameaça do Office 365 e avançadas de proteção de ameaça com a API de gerenciamento de atividade do Office 365.
ms.openlocfilehash: 057d8ac101b96f37846ac751645934279d45dc88
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972253"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="515db-103">Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas</span><span class="sxs-lookup"><span data-stu-id="515db-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="515db-p101">Se sua organização estiver usando um servidor de gerenciamento (SIEM) de incidente e eventos de segurança, você poderá integrar o Office 365 Threat Intelligence e proteção avançada de ameaça com seu servidor SIEM. Integração de SIEM permite que você exiba informações, como malware detectado pelo proteção avançada do Office 365 e inteligência de ameaça, em seus relatórios do servidor SIEM. Para configurar a integração de SIEM, você deve usar a [API de gerenciamento de atividade do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="515db-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="515db-p102">A API de gerenciamento de atividade do Office 365 recupera informações sobre o usuário, admin, sistema e ações de política e eventos do Office 365 e os logs de atividade do Azure Active Directory da sua organização. O [esquema de inteligência de ameaça e a proteção de ameaça avançadas do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funciona com inteligência de ameaça e/ou avançada contra ameaças, portanto, se sua organização tiver avançada proteção contra ameaças mas não inteligência de ameaça (ou vice-versa), você pode ainda use essa mesma API para sua integração do servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="515db-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="515db-p103">O servidor SIEM ou outro sistema semelhante deve sondar a carga de trabalho **audit.general** eventos de detecção de acesso. Para saber mais, consulte [Introdução ao APIs de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="515db-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="515db-111">Você deve ser um administrador global do Office 365 ou ter a função de administrador de segurança atribuída no Centro de conformidade & segurança ao configurar a integração de SIEM com inteligência de ameaça do Office 365 e proteção avançada de ameaça.</span><span class="sxs-lookup"><span data-stu-id="515db-111">You must be an Office 365 global administrator or have the security administrator role assigned in the Security & Compliance Center to set up SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection.</span></span><br/><span data-ttu-id="515db-p104">Log de auditoria deve ser ativado para o seu ambiente do Office 365. Para obter ajuda com isso, consulte [Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="515db-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="515db-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="515db-114">Related topics</span></span>

[<span data-ttu-id="515db-115">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="515db-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

<span data-ttu-id="515db-116">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="515db-116">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>

[<span data-ttu-id="515db-117">Inteligente de relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="515db-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="515db-118">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="515db-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

