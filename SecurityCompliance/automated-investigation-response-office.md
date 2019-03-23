---
title: Investigação e resposta automatizadas (AIR) com o Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Saiba mais sobre os recursos de investigação e resposta automatizados do Office 365 proteção avançada contra ameaças.
ms.openlocfilehash: c6cfc03588e580382f673b2e9be8543bfcaf9ac1
ms.sourcegitcommit: f6073deec39a18581ed12abef18728417a52cdf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2019
ms.locfileid: "30747557"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a><span data-ttu-id="7b28d-103">Investigação e resposta automatizadas (AIR) com o Office 365</span><span class="sxs-lookup"><span data-stu-id="7b28d-103">Automated Investigation and Response (AIR) with Office 365</span></span>

<span data-ttu-id="7b28d-104">A investigação e a resposta automatizadas (AIR) (em breve para os [recursos de investigação e resposta contra ameaças do Office 365](office-365-ti.md)) permitem que você execute investigação e correção automatizadas para ameaças conhecidas que existem atualmente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="7b28d-105">Leia este artigo para obter uma visão geral do AIR e como ele pode ajudar sua organização e as equipes de operações de segurança a reduzir as ameaças de forma mais eficaz e eficiente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-105">Read this article to get an overview of AIR and how it can help your organization and security operations teams mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="7b28d-106">Para saber mais sobre quando recursos adicionais do AIR estarão disponíveis, consulte o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="7b28d-106">To learn more about when additional features in AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="7b28d-107">Alertas</span><span class="sxs-lookup"><span data-stu-id="7b28d-107">Alerts</span></span>

<span data-ttu-id="7b28d-108">Os [alertas](alert-policies.md#viewing-alerts) representam disparadores de fluxos de trabalho da equipe de operações de segurança para resposta a incidentes.</span><span class="sxs-lookup"><span data-stu-id="7b28d-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="7b28d-109">Priorizar o conjunto certo de alertas para investigação e, ao mesmo tempo, garantir que nenhuma ameaça seja difícil.</span><span class="sxs-lookup"><span data-stu-id="7b28d-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="7b28d-110">Quando as investigações nos alertas são realizadas manualmente, as equipes de operações de segurança devem procurar e correlacionar as entidades (por exemplo, conteúdo, dispositivos e usuários) em risco de ameaças.</span><span class="sxs-lookup"><span data-stu-id="7b28d-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="7b28d-111">Essas tarefas e fluxos de trabalho são muito demorados e envolvem várias ferramentas e sistemas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="7b28d-112">Com o AIR, a investigação e a resposta são automatizadas nos alertas importantes de segurança e gerenciamento de ameaças que acionam os guias estratégicos de resposta de segurança automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="7b28d-113">Na versão inicial do AIR em abril de 2019, os alertas gerados a partir das políticas de alerta de eventos do único a seguir serão investigados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-113">In the initial release of AIR in April 2019, alerts generated from following singel events alert policies will be auto-investigated.</span></span> 

1. <span data-ttu-id="7b28d-114">Um clique em URL potencialmente mal-intencionado foi detectado</span><span class="sxs-lookup"><span data-stu-id="7b28d-114">A potentially malicious URL click was detected</span></span>
2. <span data-ttu-id="7b28d-115">Email relatado pelo usuário como Phish \*</span><span class="sxs-lookup"><span data-stu-id="7b28d-115">Email reported by user as phish\*</span></span>
3. <span data-ttu-id="7b28d-116">Mensagens de email contendo malware removidos após a entrega \*</span><span class="sxs-lookup"><span data-stu-id="7b28d-116">Email messages containing malware removed after delivery\*</span></span>
4. <span data-ttu-id="7b28d-117">Mensagens de email que contêm URLs de phishing removidos após a entrega \*</span><span class="sxs-lookup"><span data-stu-id="7b28d-117">Email messages containing phish URLs removed after delivery\*</span></span>

<span data-ttu-id="7b28d-118">\* Observação: esses alertas receberam uma severidade "inFormativa" nas respectivas políticas de alerta no centro de segurança e conformidade com as notificações de email desativadas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-118">\*Note: These alerts have been assigned an "Informational" severity in the respective alert policies within the Security and Compliance Center with email notifications turned off.</span></span> <span data-ttu-id="7b28d-119">Eles podem ser ativados por meio da configuração da política de alerta.</span><span class="sxs-lookup"><span data-stu-id="7b28d-119">These can be turned on through the Alert policy configuration.</span></span>

<span data-ttu-id="7b28d-120">para exibir alertas, no centro de conformidade do & de segurança do Office 365, escolha **alertas** > **exibir alertas**.</span><span class="sxs-lookup"><span data-stu-id="7b28d-120">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span> <span data-ttu-id="7b28d-121">Selecione um alerta para exibir seus detalhes e, em seguida, use o link **Exibir investigação** para ir para a [investigação](#investigation-graph)correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-121">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

![Alertas que se vinculam a investigações](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a><span data-ttu-id="7b28d-123">Guias de segurança</span><span class="sxs-lookup"><span data-stu-id="7b28d-123">Security playbooks</span></span>

<span data-ttu-id="7b28d-124">Os guias de segurança são políticas de back-end que estão no coração da automação no Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="7b28d-124">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="7b28d-125">Os guias estratégicos de segurança fornecidos no AIR são baseados em cenários comuns de segurança do mundo real.</span><span class="sxs-lookup"><span data-stu-id="7b28d-125">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="7b28d-126">Um guia de segurança é iniciado automaticamente quando um alerta é disparado dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="7b28d-126">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="7b28d-127">Depois que o alerta é acionado, o manual associado é executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b28d-127">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="7b28d-128">O guia estratégico executa uma investigação, examinando todos os metadados associados (incluindo mensagens de email, usuários, assuntos, remetentes, etc.) e, com base em suas descobertas, recomenda um conjunto de ações que a equipe de segurança da sua organização pode executar para controlar e reduzir a ameaça.</span><span class="sxs-lookup"><span data-stu-id="7b28d-128">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="7b28d-129">Os guias de segurança que você receberá com o AIR são projetados para lidar com as ameaças mais frequentes que as organizações enfrentam hoje.</span><span class="sxs-lookup"><span data-stu-id="7b28d-129">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="7b28d-130">Eles são baseados na entrada de operações de segurança e em equipes de resposta a incidentes, incluindo aqueles que ajudam a defender a Microsoft e seus ativos de clientes.</span><span class="sxs-lookup"><span data-stu-id="7b28d-130">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft and our customers assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="7b28d-131">Os guias de segurança estão distribuindo em fases</span><span class="sxs-lookup"><span data-stu-id="7b28d-131">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="7b28d-132">Como parte do AIR, os guias de segurança são implantados em fases</span><span class="sxs-lookup"><span data-stu-id="7b28d-132">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="7b28d-133">**Fase 1 (abril de 2019)**: os guias estratégicos incluem recomendações para ações que os administradores de segurança revisam e aprovam.</span><span class="sxs-lookup"><span data-stu-id="7b28d-133">**Phase 1 (April 2019)**: Playbooks include recommendations for actions that security administrators review and approve.</span></span> 

- <span data-ttu-id="7b28d-134">**Fase 2 (junho de 2019)**: os administradores de segurança terão a opção de configurar os guias estratégicos de segurança para executar a ação automaticamente, sem a interação administrativa.</span><span class="sxs-lookup"><span data-stu-id="7b28d-134">**Phase 2 (June 2019)**: Security administrators will have the option to configure security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="7b28d-135">A fase 1 incluirá os seguintes guias estratégicos:</span><span class="sxs-lookup"><span data-stu-id="7b28d-135">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="7b28d-136">Mensagem de phishing relatada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7b28d-136">User-reported phish message</span></span>
- <span data-ttu-id="7b28d-137">URL clique em alterar veredicto</span><span class="sxs-lookup"><span data-stu-id="7b28d-137">URL click verdict change</span></span> 
- <span data-ttu-id="7b28d-138">Malware detectado após a entrega (malware ZAP)</span><span class="sxs-lookup"><span data-stu-id="7b28d-138">Malware detected post-delivery (Malware ZAP)</span></span>
- <span data-ttu-id="7b28d-139">O phishing detectou o post-Delivery ZAP (Phish ZAP)</span><span class="sxs-lookup"><span data-stu-id="7b28d-139">Phish detected post-delivery ZAP (Phish ZAP)</span></span>
- <span data-ttu-id="7b28d-140">Investigações de email manuais (usando o explorador de ameaças)</span><span class="sxs-lookup"><span data-stu-id="7b28d-140">Manual e-mail investigations (using Threat Explorer)</span></span>

<span data-ttu-id="7b28d-141">Vários outros guias estratégicos estão planejados para a fase 2.</span><span class="sxs-lookup"><span data-stu-id="7b28d-141">Several other playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="7b28d-142">Os guias estratégicos incluem investigação e recomendações</span><span class="sxs-lookup"><span data-stu-id="7b28d-142">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="7b28d-143">Cada manual inclui:</span><span class="sxs-lookup"><span data-stu-id="7b28d-143">Each playbook includes:</span></span> 
- <span data-ttu-id="7b28d-144">uma investigação raiz,</span><span class="sxs-lookup"><span data-stu-id="7b28d-144">a root investigation,</span></span> 
- <span data-ttu-id="7b28d-145">etapas seguidas para identificar e correlacionar outras ameaças potenciais e</span><span class="sxs-lookup"><span data-stu-id="7b28d-145">steps taken to identify and correlate other potential threats, and</span></span> 
- <span data-ttu-id="7b28d-146">ações de correção de ameaças recomendadas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-146">recommended threat remediation actions.</span></span>

<span data-ttu-id="7b28d-147">Cada etapa de alto nível inclui muitas subetapas executadas para fornecer uma resposta detalhada, detalhada e exaustiva às ameaças.</span><span class="sxs-lookup"><span data-stu-id="7b28d-147">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="7b28d-148">Exemplo: mensagem de phishing relatada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7b28d-148">Example: User-reported phish message</span></span>

<span data-ttu-id="7b28d-149">Quando um usuário em sua organização envia uma mensagem de email e o relata à Microsoft usando o [suplemento de mensagem de relatório para Outlook ou Outlook Web Access](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="7b28d-149">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="7b28d-150">Isso aciona um alerta informativo baseado no sistema que inicia automaticamente o guia estratégico de investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-150">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="7b28d-151">Durante a fase de investigação de raiz, vários aspectos do email são avaliados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-151">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="7b28d-152">Eles incluem:</span><span class="sxs-lookup"><span data-stu-id="7b28d-152">These include:</span></span>
- <span data-ttu-id="7b28d-153">Uma determinação sobre o tipo de ameaça que ela pode ser;</span><span class="sxs-lookup"><span data-stu-id="7b28d-153">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="7b28d-154">Quem o enviou;</span><span class="sxs-lookup"><span data-stu-id="7b28d-154">Who sent it;</span></span>
- <span data-ttu-id="7b28d-155">De onde o email foi enviado (infraestrutura de envio);</span><span class="sxs-lookup"><span data-stu-id="7b28d-155">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="7b28d-156">Se outras instâncias do email foram entregues ou bloqueadas;</span><span class="sxs-lookup"><span data-stu-id="7b28d-156">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="7b28d-157">Uma avaliação de nossos analistas;</span><span class="sxs-lookup"><span data-stu-id="7b28d-157">An assessment from our analysts;</span></span>
- <span data-ttu-id="7b28d-158">Se o email está associado a qualquer campanha conhecida;</span><span class="sxs-lookup"><span data-stu-id="7b28d-158">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="7b28d-159">e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7b28d-159">and more.</span></span>

<span data-ttu-id="7b28d-160">Após a conclusão da investigação raiz, o guia estratégico fornece uma lista de ações recomendadas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-160">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="7b28d-161">Em seguida, várias etapas de investigação e busca de ameaças são executadas:</span><span class="sxs-lookup"><span data-stu-id="7b28d-161">Next, several threat investigation and hunting steps are executed:</span></span>

- <span data-ttu-id="7b28d-162">Mensagens de email semelhantes em outros clusters de email são pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-162">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="7b28d-163">O sinal é compartilhado com outras plataformas, como o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="7b28d-163">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="7b28d-164">É possível determinar se qualquer usuário clicou por qualquer link em mensagens de email suspeitas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-164">A determination is made on whether any users have clicked through any links in suspicious email messages.</span></span>
- <span data-ttu-id="7b28d-165">Uma verificação é feita entre O Office 365 proteção do Exchange Online ([EOP]) (EOP/Exchange-Online-Protection-EOP. MD) e o Office 365 Advanced Therat Protection ([ATP]) (Office-365-atp.md) para ver se há outras mensagens semelhantes relatadas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="7b28d-165">A check is done across Office 365 Exchange Online Protection ([EOP])(eop/exchange-online-protection-eop.md) and Office 365 Advanced Therat Protection ([ATP])(office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="7b28d-166">Uma verificação é feita para ver se um usuário foi comprometido.</span><span class="sxs-lookup"><span data-stu-id="7b28d-166">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="7b28d-167">Esta verificação utiliza sinais no [Microsoft Cloud app Security](https://docs.microsoft.com/cloud-app-security) e no [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlacionando qualquer anomalia de atividade do usuário relacionada.</span><span class="sxs-lookup"><span data-stu-id="7b28d-167">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related user activity anomalies.</span></span> 

<span data-ttu-id="7b28d-168">Durante a fase de caça, riscos e ameaças são atribuídos a várias etapas de busca.</span><span class="sxs-lookup"><span data-stu-id="7b28d-168">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="7b28d-169">Correção é a fase final do guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="7b28d-169">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="7b28d-170">Durante esta fase, as etapas de correção são tomadas, com base nas fases de investigação e busca.</span><span class="sxs-lookup"><span data-stu-id="7b28d-170">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="7b28d-171">Introdução</span><span class="sxs-lookup"><span data-stu-id="7b28d-171">Getting started</span></span>

<span data-ttu-id="7b28d-172">Para acessar suas investigações, como um administrador global do Office 365, administrador de segurança ou leitor de segurança, vá para o centro de conformidade do &[https://protection.office.com](https://protection.office.com)de segurança do Office 365 () e entre.</span><span class="sxs-lookup"><span data-stu-id="7b28d-172">To access your investigations, as an Office 365 global administrator, security administrator, or security reader, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="7b28d-173">Em seguida, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7b28d-173">Then, do one of the following:</span></span>

- <span data-ttu-id="7b28d-174">No painel de navegação à esquerda, vá para**investigações**de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="7b28d-174">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="7b28d-175">ou</span><span class="sxs-lookup"><span data-stu-id="7b28d-175">or</span></span>

- <span data-ttu-id="7b28d-176">Visite o painel de gerenciamento de ameaças (no centro de conformidade do & de segurança, vá para o**painel** **Gerenciamento** > de ameaças).</span><span class="sxs-lookup"><span data-stu-id="7b28d-176">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![Widgets do AIR](media/air-widgets.png)

<span data-ttu-id="7b28d-178">Seus widgets do AIR serão exibidos na parte superior do [painel de segurança](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="7b28d-178">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="7b28d-179">Selecione um widget para começar.</span><span class="sxs-lookup"><span data-stu-id="7b28d-179">Select a widget to get started.</span></span>

<span data-ttu-id="7b28d-180">Você também pode acessar um invesitgation diretamente dos alertas relacionados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-180">You may also access an invesitgation directly from the related Alerts.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="7b28d-181">Investigações automatizadas</span><span class="sxs-lookup"><span data-stu-id="7b28d-181">Automated investigations</span></span>

<span data-ttu-id="7b28d-182">A página de investigações automatizadas mostra as investigações da organização e seus Estados atuais.</span><span class="sxs-lookup"><span data-stu-id="7b28d-182">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Página de investigação principal para AIR](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="7b28d-184">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-184">You can:</span></span>
- <span data-ttu-id="7b28d-185">Navegue diretamente para uma investigação (selecione uma **ID de investigação**).</span><span class="sxs-lookup"><span data-stu-id="7b28d-185">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="7b28d-186">Aplicar filtros.</span><span class="sxs-lookup"><span data-stu-id="7b28d-186">Apply filters.</span></span> <span data-ttu-id="7b28d-187">Escolha um **tipo de investigação**, **intervalo de tempo**, **status**ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="7b28d-187">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="7b28d-188">Exporte os dados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="7b28d-188">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="7b28d-189">Gráfico de investigação</span><span class="sxs-lookup"><span data-stu-id="7b28d-189">Investigation graph</span></span>

<span data-ttu-id="7b28d-190">Ao abrir uma investigação específica, você verá a página de gráfico de investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-190">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="7b28d-191">Esta página mostra todas as diferentes entidades: mensagens de email, usuários (e suas atividades) e dispositivos que foram investigados automaticamente como parte do alerta que foi acionado.</span><span class="sxs-lookup"><span data-stu-id="7b28d-191">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Página de gráfico de investigação aérea](media/air-investigationgraphpage.png)

<span data-ttu-id="7b28d-193">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-193">You can:</span></span>
- <span data-ttu-id="7b28d-194">Obtenha uma visão geral da investigação atual.</span><span class="sxs-lookup"><span data-stu-id="7b28d-194">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="7b28d-195">Exibir um resumo dos intervalos de investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-195">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="7b28d-196">Selecione um nó na visualização para exibir detalhes desse nó.</span><span class="sxs-lookup"><span data-stu-id="7b28d-196">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="7b28d-197">Selecione uma guia na parte superior para exibir os detalhes dessa guia.</span><span class="sxs-lookup"><span data-stu-id="7b28d-197">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="7b28d-198">Investigação de alerta</span><span class="sxs-lookup"><span data-stu-id="7b28d-198">Alert investigation</span></span>

<span data-ttu-id="7b28d-199">Na guia **alertas** de uma investigação, você pode ver alertas relevantes para a investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-199">On the **Alerts** tab for an investigation, you can see alerts relevant to the investigation.</span></span> <span data-ttu-id="7b28d-200">Os detalhes incluem o alerta que disparou a investigação e outros alertas, como entrada arriscada, download em massa, etc., que são correlacionados à investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-200">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="7b28d-201">A partir dessa página, um analista de segurança também pode exibir detalhes adicionais sobre alertas individuais.</span><span class="sxs-lookup"><span data-stu-id="7b28d-201">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Página alertas de ar](media/air-investigationalertspage.png)

<span data-ttu-id="7b28d-203">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-203">You can:</span></span>
- <span data-ttu-id="7b28d-204">Obtenha uma visão geral do alerta de acionamento atual e de todos os alertas associados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-204">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="7b28d-205">Selecione um alerta na lista para abrir uma página de sobrevôo que mostre detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="7b28d-205">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="7b28d-206">Investigação de email</span><span class="sxs-lookup"><span data-stu-id="7b28d-206">Email investigation</span></span>

<span data-ttu-id="7b28d-207">Na guia **email** de uma investigação, você pode ver todos os clusters de email identificados como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-207">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="7b28d-208">Dado o volume simples de email que os usuários de uma organização enviam e recebem, o processo de</span><span class="sxs-lookup"><span data-stu-id="7b28d-208">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="7b28d-209">agrupar mensagens de email com base em atributos semelhantes de um cabeçalho de mensagem, corpo, URL e anexo;</span><span class="sxs-lookup"><span data-stu-id="7b28d-209">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="7b28d-210">separar emails mal-intencionados do email em bom estado; e</span><span class="sxs-lookup"><span data-stu-id="7b28d-210">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="7b28d-211">executar ações em mensagens de email mal-intencionadas</span><span class="sxs-lookup"><span data-stu-id="7b28d-211">taking action on malicious email messages</span></span> 

<span data-ttu-id="7b28d-212">pode levar várias horas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-212">can take many hours.</span></span> <span data-ttu-id="7b28d-213">Agora, o ar automatiza esse processo, poupando o tempo e esforço da equipe de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="7b28d-213">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="7b28d-214">Por exemplo, considere o cenário a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b28d-214">As an example, consider the following scenario.</span></span> <span data-ttu-id="7b28d-215">O primeiro cluster de três mensagens de email foi considerado como phishing.</span><span class="sxs-lookup"><span data-stu-id="7b28d-215">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="7b28d-216">Outro cluster de mensagens semelhantes com o mesmo IP e assunto foi encontrado e considerado mal-intencionado, pois alguns deles foram identificados como phishing durante a detecção inicial.</span><span class="sxs-lookup"><span data-stu-id="7b28d-216">Another cluster of similar messages with the same IP and subject was found and considered  malicious, as some of them were identified as phish during initial detection.</span></span> 

![Página investigação de emails de ar](media/air-investigationemailpage.png)

<span data-ttu-id="7b28d-218">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-218">You can:</span></span>
- <span data-ttu-id="7b28d-219">Obtenha uma visão geral das ameaças e dos resultados de agrupamento atuais encontrados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-219">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="7b28d-220">Clique em uma entidade de cluster ou uma lista de ameaças para abrir uma página de saída que mostra os detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="7b28d-220">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Email de investigação de ar com detalhes de submenu](media/air-investigationemailpageflyoutdetails.png)

<span data-ttu-id="7b28d-222">\* Observação: no contexto de email, você pode ver uma superfície de ameaça de anomalias de volume como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-222">\*Note: In the context of email, you may see a volume anomaly threat surface as part of the investigation.</span></span> <span data-ttu-id="7b28d-223">Uma anomalia de volume indica um pico em emails semelhantes em torno do tempo de evento de investigação em comparação aos prazos anteriores.</span><span class="sxs-lookup"><span data-stu-id="7b28d-223">A volume anomaly indicates a spike in similar emails around the investigation event time compared to earlier timeframes.</span></span> <span data-ttu-id="7b28d-224">Esse pico no tráfego de email com características semelhantes (por exemplo, domínio de assunto e remetente, semelhança de corpo e IP de remetente) é típico do início de campanhas ou ataques de email.</span><span class="sxs-lookup"><span data-stu-id="7b28d-224">This spike in email traffic with similar characteristics (e.g. subject and sender domain, body similarity and sender IP) is typical of the start of email campaigns or attacks.</span></span> <span data-ttu-id="7b28d-225">No enTanto, as campanhas de email em massa e spom em momentos também compartilham essas características.</span><span class="sxs-lookup"><span data-stu-id="7b28d-225">However, bulk and spom email campaigns at times also share these characteristics.</span></span> <span data-ttu-id="7b28d-226">As anomalias de volume representam uma possível ameaça e, portanto, podem ser menos graves em comparação às ameaças de malware ou phishing identificadas usando mecanismos antivírus, acionamento ou reputação mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-226">Volume anomalies represent a potential threat, and accordingly could be less severe compared to malware or phish threats that are identified using anti-virus engines, detonation or malicious reputation.</span></span>

### <a name="user-investigation"></a><span data-ttu-id="7b28d-227">Investigação de usuário</span><span class="sxs-lookup"><span data-stu-id="7b28d-227">User investigation</span></span>

<span data-ttu-id="7b28d-228">Na guia **usuários** , você pode ver todos os usuários identificados como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-228">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="7b28d-229">Por exemplo, na imagem a seguir, o AIR identificou indicadores de comprometimento e anomalias com base em uma nova regra de caixa de entrada que foi criada.</span><span class="sxs-lookup"><span data-stu-id="7b28d-229">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="7b28d-230">Detalhes adicionais (evidência) da investigação estão disponíveis por meio de exibições detalhadas nesta guia. os indicadores de comprometimento e anomalias também podem incluir detecções de anomalias do [Microsoft Cloud app Security](https://docs.microsoft.com/cloud-app-security).</span><span class="sxs-lookup"><span data-stu-id="7b28d-230">Additional details (evidence) of the investigation are available through detailed views within this tab. Indicators of compromise and anomalies may also include anomaly detections from [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span>

![Página usuários de investigação aérea](media/air-investigationuserspage.png)

<span data-ttu-id="7b28d-232">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-232">You can:</span></span>
- <span data-ttu-id="7b28d-233">Obtenha uma visão geral dos resultados do usuário identificados e dos riscos encontrados.</span><span class="sxs-lookup"><span data-stu-id="7b28d-233">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="7b28d-234">Selecione um usuário para abrir uma página de sobrevôo que mostre os detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="7b28d-234">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="7b28d-235">Investigação de máquina</span><span class="sxs-lookup"><span data-stu-id="7b28d-235">Machine investigation</span></span>

<span data-ttu-id="7b28d-236">Na guia **computadores** , você pode ver todas as máquinas identificadas como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-236">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Página da máquina de investigação de ar](media/air-investigationmachinepage.png)

<span data-ttu-id="7b28d-238">Como parte da investigação, o AIR correlaciona ameaças de email a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7b28d-238">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="7b28d-239">Por exemplo, uma investigação passa um hash de arquivo para o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) para investigar.</span><span class="sxs-lookup"><span data-stu-id="7b28d-239">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="7b28d-240">Isso permite a investigação automatizada de máquinas relevantes para seus usuários e ajuda a garantir que as ameaças sejam tratadas tanto na nuvem quanto em seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7b28d-240">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="7b28d-241">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-241">You can:</span></span>
- <span data-ttu-id="7b28d-242">Obtenha uma visão geral das máquinas e ameaças atuais encontradas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-242">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="7b28d-243">Selecione uma máquina para abrir um modo de exibição que nas [investigações ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) relacionadas do Windows Defender no centro de segurança ATP do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="7b28d-243">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) in the Windows Defender ATP Security Center.</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="7b28d-244">Investigação de entidade</span><span class="sxs-lookup"><span data-stu-id="7b28d-244">Entity investigation</span></span>

<span data-ttu-id="7b28d-245">Na guia **entidades** , você pode ver todas as máquinas identificadas como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-245">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="7b28d-246">Aqui, você pode ver as entidades investigadas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-246">Here, you can see the investigated entities.</span></span> <span data-ttu-id="7b28d-247">Você pode ver detalhes dos tipos de entidades, como mensagens de email, clusters, endereços IP, usuários e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7b28d-247">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="7b28d-248">Você também pode ver quantas entidades foram analisadas e as ameaças que foram associadas a cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-248">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Página de entidades de investigação aérea](media/air-investigationentitiespage.png)

<span data-ttu-id="7b28d-250">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-250">You can:</span></span>
- <span data-ttu-id="7b28d-251">Obtenha uma visão geral das entidades e ameaças de investigação encontradas.</span><span class="sxs-lookup"><span data-stu-id="7b28d-251">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="7b28d-252">Selecione uma entidade para abrir uma página de saída que mostre os detalhes relacionados da entidade.</span><span class="sxs-lookup"><span data-stu-id="7b28d-252">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Detalhes das entidades de investigação aérea](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="7b28d-254">Log do guia estratégico</span><span class="sxs-lookup"><span data-stu-id="7b28d-254">Playbook log</span></span>

<span data-ttu-id="7b28d-255">Na guia **log** , você pode ver todas as etapas do guia estratégico que ocorreram durante a investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-255">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="7b28d-256">O log captura um inventário completo de todas as ações concluídas pelos recursos de investigação automática do Office 365 como parte do ar.</span><span class="sxs-lookup"><span data-stu-id="7b28d-256">The log captures a complete inventory of all actions completed by Office 365 auto-investigation capabilities as part of AIR.</span></span> <span data-ttu-id="7b28d-257">Ele fornece uma visão clara de todas as etapas executadas, incluindo a própria ação, uma descrição e a duração do real do início ao fim.</span><span class="sxs-lookup"><span data-stu-id="7b28d-257">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Página de log de investigação de ar](media/air-investigationlogpage.png)

<span data-ttu-id="7b28d-259">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-259">You can:</span></span>
- <span data-ttu-id="7b28d-260">Obtenha uma visão geral das etapas do guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="7b28d-260">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="7b28d-261">Exportar os resultados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="7b28d-261">Export the results to a CSV file.</span></span>
- <span data-ttu-id="7b28d-262">Filtrar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="7b28d-262">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="7b28d-263">Ações recomendadas</span><span class="sxs-lookup"><span data-stu-id="7b28d-263">Recommended actions</span></span>

<span data-ttu-id="7b28d-264">Na guia **ações** , você pode ver todas as ações do guia estratégico que são recomendadas para correção após a conclusão da investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-264">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="7b28d-265">As ações capturam as etapas que a Microsoft recomenda que você faça no final de uma investigação.</span><span class="sxs-lookup"><span data-stu-id="7b28d-265">Actions capture the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="7b28d-266">Você pode realizar ações de correção aqui selecionando uma ou mais ações.</span><span class="sxs-lookup"><span data-stu-id="7b28d-266">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="7b28d-267">Clicar em **aprovar** permitirá que a correção seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="7b28d-267">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="7b28d-268">(As permissões apropriadas serão necessárias.</span><span class="sxs-lookup"><span data-stu-id="7b28d-268">(Appropriate permissions will be required.</span></span> <span data-ttu-id="7b28d-269">Por exemplo, um leitor de segurança pode exibir ações, mas não aprová-las.)</span><span class="sxs-lookup"><span data-stu-id="7b28d-269">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Página de ação de investigações aéreas](media/air-investigationactionspage.png)

<span data-ttu-id="7b28d-271">Você pode:</span><span class="sxs-lookup"><span data-stu-id="7b28d-271">You can:</span></span>
- <span data-ttu-id="7b28d-272">Obtenha uma visão geral das ações recomendadas para o guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="7b28d-272">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="7b28d-273">Selecione uma única ação ou várias ações.</span><span class="sxs-lookup"><span data-stu-id="7b28d-273">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="7b28d-274">Aprovar ou rejeitar ações recomendadas com comentários.</span><span class="sxs-lookup"><span data-stu-id="7b28d-274">Approve or reject recommended actions with comments.</span></span>
- <span data-ttu-id="7b28d-275">Exportar os resultados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="7b28d-275">Export the results to a CSV file.</span></span>
- <span data-ttu-id="7b28d-276">Filtrar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="7b28d-276">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="7b28d-277">Como obter o AIR</span><span class="sxs-lookup"><span data-stu-id="7b28d-277">How to get AIR</span></span>

<span data-ttu-id="7b28d-278">No momento, o Office 365 AIR está em visualização.</span><span class="sxs-lookup"><span data-stu-id="7b28d-278">Currently, Office 365 AIR is in preview.</span></span> <span data-ttu-id="7b28d-279">O Office 365 AIR será incluído nas seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="7b28d-279">Office 365 AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="7b28d-280">Microsoft 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="7b28d-280">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="7b28d-281">Office 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="7b28d-281">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="7b28d-282">Proteção contra ameaças da Microsoft</span><span class="sxs-lookup"><span data-stu-id="7b28d-282">Microsoft Threat Protection</span></span>
- <span data-ttu-id="7b28d-283">Office 365 plano avançado de proteção contra ameaças 2</span><span class="sxs-lookup"><span data-stu-id="7b28d-283">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="7b28d-284">Para saber mais sobre a disponibilidade de recursos, visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="7b28d-284">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
