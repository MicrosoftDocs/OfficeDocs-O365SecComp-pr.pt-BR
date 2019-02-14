---
title: Integração do servidor SIEM com Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
- M365-security-compliance
description: 'Resumo: Leia este artigo para obter uma visão geral da integração do servidor SIEM com Microsoft 365.'
ms.openlocfilehash: a6e139d14a7ea3625b2d2fffec5ad5d913ea9184
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995192"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="bfd12-103">Integração do SIEM server com aplicativos e serviços da Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bfd12-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="bfd12-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bfd12-104">Overview</span></span>

<span data-ttu-id="bfd12-p101">Se sua organização estiver usando um servidor de informações de segurança e gerenciamento de evento (SIEM), ou se você estiver planejando obter um servidor SIEM em breve, talvez você queira saber como que vai integre sua 365 da Microsoft, incluindo o Office 365 Enterprise. Se você precisa de um servidor SIEM depende de vários fatores, como os requisitos de segurança da sua organização. Microsoft 365 oferece uma variedade de recursos de segurança; No entanto, se sua organização tiver conteúdo e aplicativos no local e na nuvem (como no caso de uma implantação de nuvem híbrida), considere adicionar um servidor SIEM para proteção extra. Ou, se sua organização tem requisitos de segurança particularmente rígidas que devem ser atendidos, considere a adição de um servidor SIEM ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="bfd12-p101">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 Enterprise. Whether you need a SIEM server depends on many factors, such as your organization's security requirements. Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection. Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="bfd12-109">Integração do servidor SIEM 365 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="bfd12-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="bfd12-p102">Um servidor SIEM pode receber dados de uma ampla variedade de aplicativos e serviços da Microsoft 365. A tabela a seguir lista as várias Microsoft 365 serviços e aplicativos, juntamente com entradas de servidor SIEM e aonde ir para saber mais sobre a integração do servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="bfd12-p102">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications. The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="bfd12-112">Serviço Microsoft 365 ou aplicativo</span><span class="sxs-lookup"><span data-stu-id="bfd12-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="bfd12-113">Entradas de servidor SIEM</span><span class="sxs-lookup"><span data-stu-id="bfd12-113">SIEM server inputs</span></span> | <span data-ttu-id="bfd12-114">Recursos para saber mais</span><span class="sxs-lookup"><span data-stu-id="bfd12-114">Resources to learn more</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bfd12-115">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="bfd12-115">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span> <br/>   <span data-ttu-id="bfd12-116">ou</span><span class="sxs-lookup"><span data-stu-id="bfd12-116">or</span></span>   <br/>[<span data-ttu-id="bfd12-117">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="bfd12-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="bfd12-118">Logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="bfd12-118">Audit logs</span></span> | [<span data-ttu-id="bfd12-119">Integração de SIEM com inteligência de ameaça do Office 365 e proteção de ameaça avançadas</span><span class="sxs-lookup"><span data-stu-id="bfd12-119">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="bfd12-120">Segurança no Aplicativo da Nuvem da Microsoft</span><span class="sxs-lookup"><span data-stu-id="bfd12-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="bfd12-121">Integração de log</span><span class="sxs-lookup"><span data-stu-id="bfd12-121">Log integration</span></span> | [<span data-ttu-id="bfd12-122">Integração de SIEM com segurança de aplicativo de nuvem Microsoft</span><span class="sxs-lookup"><span data-stu-id="bfd12-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="bfd12-123">Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bfd12-123">Office 365 Cloud App Security</span></span>](office-365-cas-overview.md) | <span data-ttu-id="bfd12-124">Integração de log</span><span class="sxs-lookup"><span data-stu-id="bfd12-124">Log integration</span></span> | [<span data-ttu-id="bfd12-125">Integrar seu servidor SIEM ao Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bfd12-125">Integrate your SIEM server with Office 365 Cloud App Security</span></span>](integrate-your-siem-server-with-office-365-cas.md) |
| [<span data-ttu-id="bfd12-126">Proteção Avançada Contra Ameaças do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="bfd12-126">Windows Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="bfd12-127">Integração de log</span><span class="sxs-lookup"><span data-stu-id="bfd12-127">Log integration</span></span> | [<span data-ttu-id="bfd12-128">Alertas de recepção para suas ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="bfd12-128">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| <span data-ttu-id="bfd12-129">[Central de segurança do Windows Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Proteção contra ameaças e detecção de ameaça)</span><span class="sxs-lookup"><span data-stu-id="bfd12-129">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="bfd12-130">Alertas</span><span class="sxs-lookup"><span data-stu-id="bfd12-130">Alerts</span></span> | [<span data-ttu-id="bfd12-131">Exportação de dados de segurança Azure SIEM - configuração de Pipeline - Preview</span><span class="sxs-lookup"><span data-stu-id="bfd12-131">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [<span data-ttu-id="bfd12-132">Proteção de identidade do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bfd12-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | <span data-ttu-id="bfd12-133">Logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="bfd12-133">Audit logs</span></span> | [<span data-ttu-id="bfd12-134">Integrar os logs de auditoria do Active Directory do Azure</span><span class="sxs-lookup"><span data-stu-id="bfd12-134">Integrate Azure Active Directory audit logs</span></span>](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [<span data-ttu-id="bfd12-135">Análise de ameaça avançado Azure</span><span class="sxs-lookup"><span data-stu-id="bfd12-135">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="bfd12-136">Integração de log</span><span class="sxs-lookup"><span data-stu-id="bfd12-136">Log integration</span></span> | [<span data-ttu-id="bfd12-137">Referência de log do ATA SIEM</span><span class="sxs-lookup"><span data-stu-id="bfd12-137">ATA SIEM log reference</span></span>](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="bfd12-138">Log de auditoria deve ser ativado</span><span class="sxs-lookup"><span data-stu-id="bfd12-138">Audit logging must be turned on</span></span>

<span data-ttu-id="bfd12-139">Verifique se o log de auditoria está ativado antes de configurar a integração do servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="bfd12-139">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="bfd12-140">SharePoint Online, OneDrive for Business e Windows Azure Active Directory, [os logs de auditoria está ativado o Centro de conformidade do & de segurança](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="bfd12-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="bfd12-141">Para Exchange Online, [o log de auditoria está ativado com o Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="bfd12-141">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="bfd12-142">Confira também
</span><span class="sxs-lookup"><span data-stu-id="bfd12-142">See Also</span></span>

[<span data-ttu-id="bfd12-143">Adoção da nuvem e soluções híbridas</span><span class="sxs-lookup"><span data-stu-id="bfd12-143">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="bfd12-144">Guias do Laboratório de Teste (TLGs) para adoção de nuvem</span><span class="sxs-lookup"><span data-stu-id="bfd12-144">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


