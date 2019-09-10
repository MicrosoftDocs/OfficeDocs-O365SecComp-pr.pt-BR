---
title: Investigar automaticamente e responder a ameaças no Office 365
keywords: AIR, autoIR, ATP, automatizado, investigação, resposta, correção, ameaças, avançado, ameaça, proteção
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Comece a usar os recursos de investigação e resposta automatizados no Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 45fea46a591aac88a8d92c7a67d024d1446e9124
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822491"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="dd20f-104">Investigar automaticamente e responder a ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="dd20f-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="dd20f-105">Overview</span></span>

<span data-ttu-id="dd20f-106">[Proteção avançada contra ameaças do Office 365](office-365-atp.md) O plano 2 inclui recursos de resposta de incidentes automatizados (ar) que podem economizar tempo e esforço da equipe de operações de segurança em lidar com alertas e ameaças.</span><span class="sxs-lookup"><span data-stu-id="dd20f-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 includes automated incident response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span> <span data-ttu-id="dd20f-107">Leia este artigo para começar a usar os recursos de ar no Office 365.</span><span class="sxs-lookup"><span data-stu-id="dd20f-107">Read this article to get started using AIR capabilities in Office 365.</span></span> <span data-ttu-id="dd20f-108">Para saber mais sobre como funciona o AIR, confira o [Air (resposta de incidente automatizado) no Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="dd20f-108">To learn more about how AIR works, see [Automated incident response (AIR) in Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="dd20f-109">Com o AIR, quando determinados alertas são acionados, um ou mais guias estratégicos de segurança iniciam e a investigação automatizada é iniciada.</span><span class="sxs-lookup"><span data-stu-id="dd20f-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="dd20f-110">Durante e após um processo de investigação automatizado, a equipe de administradores e operações de segurança pode:</span><span class="sxs-lookup"><span data-stu-id="dd20f-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="dd20f-111">Exibir os detalhes de uma investigação</span><span class="sxs-lookup"><span data-stu-id="dd20f-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)

- [<span data-ttu-id="dd20f-112">Revisar e aprovar ações como resultado de uma investigação</span><span class="sxs-lookup"><span data-stu-id="dd20f-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 

- [<span data-ttu-id="dd20f-113">Exibir detalhes sobre um alerta relacionado a uma investigação</span><span class="sxs-lookup"><span data-stu-id="dd20f-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="dd20f-114">Você deve ser um administrador global, administrador de segurança, operador de segurança ou leitor de segurança para executar as tarefas descritas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="dd20f-114">You must be a global administrator, security administrator, security operator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="dd20f-115">Para saber mais, veja [centro de segurança do Microsoft 365: funções e permissões](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="dd20f-115">To learn more, see [Microsoft 365 security center: roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="dd20f-116">Exibir detalhes de uma investigação</span><span class="sxs-lookup"><span data-stu-id="dd20f-116">View details of an investigation</span></span>

1. <span data-ttu-id="dd20f-117">Como administrador global do Office 365, administrador de segurança ou leitor de segurança, acesse [https://protection.office.com](https://protection.office.com) e entre.</span><span class="sxs-lookup"><span data-stu-id="dd20f-117">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="dd20f-118">Isso leva você para o centro de conformidade de & de segurança.</span><span class="sxs-lookup"><span data-stu-id="dd20f-118">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="dd20f-119">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="dd20f-119">Do one of the following:</span></span>

    - <span data-ttu-id="dd20f-120">Vá para o**painel**de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="dd20f-120">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="dd20f-121">Isso leva você para o [painel de segurança](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="dd20f-121">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="dd20f-122">Os widgets do AIR aparecem na parte superior do [painel de segurança](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="dd20f-122">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="dd20f-123">Selecione um widget, como o **Resumo de investigações**.</span><span class="sxs-lookup"><span data-stu-id="dd20f-123">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="dd20f-124">Vá para \*\*\*\* > **investigações**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="dd20f-124">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="dd20f-125">Qualquer um dos métodos o leva a uma lista de investigações.</span><span class="sxs-lookup"><span data-stu-id="dd20f-125">Either method takes you to a list of investigations.</span></span>

    ![Página de investigação principal para AIR](media/air-maininvestigationpage.png) 

3. <span data-ttu-id="dd20f-127">Na lista de investigações, selecione um item na coluna **ID** .</span><span class="sxs-lookup"><span data-stu-id="dd20f-127">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="dd20f-128">Isso abre a página detalhes da investigação, começando com o gráfico de investigação.</span><span class="sxs-lookup"><span data-stu-id="dd20f-128">This opens investigation details page, starting with the investigation graph.</span></span>

    ![Página de gráfico de investigação aérea](media/air-investigationgraphpage.png)

4. <span data-ttu-id="dd20f-130">Use as várias guias para saber mais sobre a investigação.</span><span class="sxs-lookup"><span data-stu-id="dd20f-130">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="dd20f-131">Revisar e aprovar ações</span><span class="sxs-lookup"><span data-stu-id="dd20f-131">Review and approve actions</span></span>

<span data-ttu-id="dd20f-132">No Office 365, as investigações automatizadas normalmente resultam em uma ou mais ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="dd20f-132">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="dd20f-133">No entanto, nenhuma ação será executada até que sejam aprovadas pela equipe de operações de segurança.</span><span class="sxs-lookup"><span data-stu-id="dd20f-133">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="dd20f-134">Use o procedimento a seguir para revisar e aprovar ações.</span><span class="sxs-lookup"><span data-stu-id="dd20f-134">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="dd20f-135">Como administrador global do Office 365, administrador de segurança ou leitor de segurança, acesse [https://protection.office.com](https://protection.office.com) e entre.</span><span class="sxs-lookup"><span data-stu-id="dd20f-135">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="dd20f-136">Vá para \*\*\*\* > **investigações**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="dd20f-136">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="dd20f-137">Na lista de investigações, selecione um item na coluna **ID** .</span><span class="sxs-lookup"><span data-stu-id="dd20f-137">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="dd20f-138">No modo de exibição detalhes da investigação, selecione a guia **ações** . Todas as ações que estão com aprovação pendente são listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="dd20f-138">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="dd20f-139">Selecione um item na lista.</span><span class="sxs-lookup"><span data-stu-id="dd20f-139">Select an item in the list.</span></span>

5. <span data-ttu-id="dd20f-140">Selecione **aprovar** para executar a ação recomendada (ou **rejeitar** para fechar a investigação sem executar a ação).</span><span class="sxs-lookup"><span data-stu-id="dd20f-140">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="dd20f-141">Exibir detalhes sobre um alerta relacionado a uma investigação</span><span class="sxs-lookup"><span data-stu-id="dd20f-141">View details about an alert related to an investigation</span></span>

<span data-ttu-id="dd20f-142">Determinados tipos de alertas disparam investigação automatizada no Office 365.</span><span class="sxs-lookup"><span data-stu-id="dd20f-142">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="dd20f-143">Para saber mais, confira [alertas](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="dd20f-143">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="dd20f-144">Use o procedimento a seguir para exibir detalhes sobre um alerta que está associado a uma investigação automatizada.</span><span class="sxs-lookup"><span data-stu-id="dd20f-144">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="dd20f-145">Como administrador global do Office 365, administrador de segurança ou leitor de segurança, acesse [https://protection.office.com](https://protection.office.com) e entre.</span><span class="sxs-lookup"><span data-stu-id="dd20f-145">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="dd20f-146">Isso leva você para o centro de conformidade de & de segurança.</span><span class="sxs-lookup"><span data-stu-id="dd20f-146">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="dd20f-147">Vá para \*\*\*\* > **investigações**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="dd20f-147">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="dd20f-148">Na lista de investigações, selecione um item na coluna **ID** .</span><span class="sxs-lookup"><span data-stu-id="dd20f-148">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="dd20f-149">Com detalhes de uma investigação aberta, selecione a guia **alertas** . Todos os alertas que dispararam a investigação estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="dd20f-149">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="dd20f-150">Selecione um item na lista.</span><span class="sxs-lookup"><span data-stu-id="dd20f-150">Select an item in the list.</span></span> <span data-ttu-id="dd20f-151">Um submenu abre, com detalhes sobre o alerta e links para informações adicionais e ações.</span><span class="sxs-lookup"><span data-stu-id="dd20f-151">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="dd20f-152">Revise as informações no submenu e, dependendo do alerta específico, execute uma ação, como **resolver**, **suprimir**ou **notificar os usuários**.</span><span class="sxs-lookup"><span data-stu-id="dd20f-152">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

    - <span data-ttu-id="dd20f-153">**Resolver** é equivalente a fechar um alerta</span><span class="sxs-lookup"><span data-stu-id="dd20f-153">**Resolve** is equivalent to closing an alert</span></span>
    
    - <span data-ttu-id="dd20f-154">**Supressão** faz com que uma política não acione alertas por um período de tempo especificado</span><span class="sxs-lookup"><span data-stu-id="dd20f-154">**Suppress** causes a policy to not trigger alerts for a specified period of time</span></span>
    
    - <span data-ttu-id="dd20f-155">**Notificar os usuários sobre** o início de um email com os endereços de email dos usuários já inseridos e permite que sua equipe de operações de segurança digite uma mensagem para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="dd20f-155">**Notify users** starts an email with users' email addresses already entered, and enables your security operations team to type a message to those users.</span></span> <span data-ttu-id="dd20f-156">(Isso é semelhante ao envio de uma mensagem para destinatários usando o [Explorador de ameaças](threat-explorer.md).)</span><span class="sxs-lookup"><span data-stu-id="dd20f-156">(This is similar to sending a message to recipients using [Threat Explorer](threat-explorer.md).)</span></span>  

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="dd20f-157">Usar a API de atividade de gerenciamento do Office 365 para soluções de relatórios personalizados ou de terceiros</span><span class="sxs-lookup"><span data-stu-id="dd20f-157">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="dd20f-158">Se sua organização estiver usando uma solução de relatórios personalizada ou de terceiros, você poderá exibir informações sobre investigações automatizadas nessa solução usando a API da atividade de gerenciamento do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dd20f-158">If your organization is using a custom or third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="dd20f-159">Use os seguintes recursos para configurar isso:</span><span class="sxs-lookup"><span data-stu-id="dd20f-159">Use the following resources to set this up:</span></span>

|<span data-ttu-id="dd20f-160">Resource</span><span class="sxs-lookup"><span data-stu-id="dd20f-160">Resource</span></span>  |<span data-ttu-id="dd20f-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd20f-161">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="dd20f-162">Visão geral das APIs de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-162">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="dd20f-163">A API da Atividade de Gerenciamento do Office 365 fornece informações sobre várias ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd20f-163">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="dd20f-164">Introdução às APIs de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-164">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="dd20f-165">A API de gerenciamento do Office 365 usa o Azure AD para fornecer serviços de autenticação para que seu aplicativo acesse os dados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dd20f-165">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="dd20f-166">Siga as etapas deste artigo para configurá-lo.</span><span class="sxs-lookup"><span data-stu-id="dd20f-166">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="dd20f-167">Referência da API da Atividade de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-167">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="dd20f-168">Você pode usar a API de atividade de gerenciamento do Office 365 para recuperar informações sobre ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dd20f-168">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="dd20f-169">Leia este artigo para saber mais sobre como isso funciona.</span><span class="sxs-lookup"><span data-stu-id="dd20f-169">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="dd20f-170">Esquema da API da Atividade de Gerenciamento do Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-170">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="dd20f-171">Obtenha uma visão geral do [esquema comum](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) e do [Office 365 ATP e o esquema de resposta](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) para conhecer os tipos específicos de dados disponíveis por meio da API de atividade de gerenciamento do Office 365.</span><span class="sxs-lookup"><span data-stu-id="dd20f-171">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="dd20f-172">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="dd20f-172">Next steps</span></span>

[<span data-ttu-id="dd20f-173">Saiba mais sobre os alertas</span><span class="sxs-lookup"><span data-stu-id="dd20f-173">Learn more about alerts</span></span>](alert-policies.md)

[<span data-ttu-id="dd20f-174">Encontre e investigue manualmente emails mal-intencionados que foram entregues no Office 365</span><span class="sxs-lookup"><span data-stu-id="dd20f-174">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="dd20f-175">Saiba mais sobre o AIR no Microsoft defender ATP</span><span class="sxs-lookup"><span data-stu-id="dd20f-175">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="dd20f-176">Visite o mapa do Microsoft 365 para ver o que está chegando em breve e distribuir</span><span class="sxs-lookup"><span data-stu-id="dd20f-176">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)