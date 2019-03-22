---
title: Investigação e resposta automatizadas (AIR) com inteligência contra ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Saiba mais sobre os recursos de investigação e resposta automatizados do Office 365 proteção avançada contra ameaças.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736199"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a><span data-ttu-id="aee99-103">Investigação e resposta automatizadas (AIR) com inteligência contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="aee99-103">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="aee99-104">A investigação e a resposta automatizadas (AIR) (em breve para os [recursos de investigação e resposta contra ameaças do Office 365](office-365-ti.md)) permitem que você execute investigação e correção automatizadas para ameaças conhecidas que existem atualmente.</span><span class="sxs-lookup"><span data-stu-id="aee99-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="aee99-105">Leia este artigo para obter uma visão geral do AIR e como ele pode ajudar sua organização a reduzir as ameaças com maior eficácia e eficiência.</span><span class="sxs-lookup"><span data-stu-id="aee99-105">Read this article to get an overview of AIR and how it can help your organization mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="aee99-106">Saiba mais sobre quando o AIR estará disponível, consulte o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="aee99-106">Tolearn more about when AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="aee99-107">Alertas</span><span class="sxs-lookup"><span data-stu-id="aee99-107">Alerts</span></span>

<span data-ttu-id="aee99-108">Os [alertas](alert-policies.md#viewing-alerts) representam disparadores de fluxos de trabalho da equipe de operações de segurança para resposta a incidentes.</span><span class="sxs-lookup"><span data-stu-id="aee99-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="aee99-109">Priorizar o conjunto certo de alertas para investigação e, ao mesmo tempo, garantir que nenhuma ameaça seja difícil.</span><span class="sxs-lookup"><span data-stu-id="aee99-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="aee99-110">Quando as investigações nos alertas são realizadas manualmente, as equipes de operações de segurança devem procurar e correlacionar as entidades (por exemplo, conteúdo, dispositivos e usuários) em risco de ameaças.</span><span class="sxs-lookup"><span data-stu-id="aee99-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="aee99-111">Essas tarefas e fluxos de trabalho são muito demorados e envolvem várias ferramentas e sistemas.</span><span class="sxs-lookup"><span data-stu-id="aee99-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="aee99-112">Com o AIR, a investigação e a resposta são automatizadas nos alertas importantes de segurança e gerenciamento de ameaças que acionam os guias estratégicos de resposta de segurança automaticamente.</span><span class="sxs-lookup"><span data-stu-id="aee99-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="aee99-113">para exibir alertas, no centro de conformidade do & de segurança do Office 365, escolha **alertas** > **exibir alertas**.</span><span class="sxs-lookup"><span data-stu-id="aee99-113">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span>

![Alertas que se vinculam a investigações](media/air-alerts-page-details.png) 

<span data-ttu-id="aee99-115">Selecione um alerta para exibir seus detalhes e, em seguida, use o link **Exibir investigação** para ir para a [investigação](#investigation-graph)correspondente.</span><span class="sxs-lookup"><span data-stu-id="aee99-115">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

## <a name="security-playbooks"></a><span data-ttu-id="aee99-116">Guias de segurança</span><span class="sxs-lookup"><span data-stu-id="aee99-116">Security playbooks</span></span>

<span data-ttu-id="aee99-117">Os guias de segurança são políticas de back-end que estão no coração da automação no Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="aee99-117">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="aee99-118">Os guias estratégicos de segurança fornecidos no AIR são baseados em cenários comuns de segurança do mundo real.</span><span class="sxs-lookup"><span data-stu-id="aee99-118">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="aee99-119">Um guia de segurança é iniciado automaticamente quando um alerta é disparado dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="aee99-119">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="aee99-120">Depois que o alerta é acionado, o manual associado é executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="aee99-120">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="aee99-121">O guia estratégico executa uma investigação, examinando todos os metadados associados (incluindo mensagens de email, usuários, assuntos, remetentes, etc.) e, com base em suas descobertas, recomenda um conjunto de ações que a equipe de segurança da sua organização pode executar para controlar e reduzir a ameaça.</span><span class="sxs-lookup"><span data-stu-id="aee99-121">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="aee99-122">Os guias de segurança que você receberá com o AIR são projetados para lidar com as ameaças mais frequentes que as organizações enfrentam hoje.</span><span class="sxs-lookup"><span data-stu-id="aee99-122">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="aee99-123">Eles são baseados na entrada de operações de segurança e em equipes de resposta a incidentes, incluindo aqueles que ajudam a defender ativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aee99-123">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="aee99-124">Os guias de segurança estão distribuindo em fases</span><span class="sxs-lookup"><span data-stu-id="aee99-124">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="aee99-125">Como parte do AIR, os guias de segurança são implantados em fases</span><span class="sxs-lookup"><span data-stu-id="aee99-125">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="aee99-126">**Fase 1 (abril de 2019)**: os guias estratégicos incluem recomendações que os administradores de segurança revisam e aprovam.</span><span class="sxs-lookup"><span data-stu-id="aee99-126">**Phase 1 (April 2019)**: Playbooks include recommendations that security administrators review and approve.</span></span> 

- <span data-ttu-id="aee99-127">**Fase 2 (junho de 2019)**: os administradores de segurança terão a opção de permitir que os guias estratégicos de segurança executem ações automaticamente, sem interação administrativa.</span><span class="sxs-lookup"><span data-stu-id="aee99-127">**Phase 2 (June 2019)**: Security administrators will have the option to allow security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="aee99-128">A fase 1 incluirá os seguintes guias estratégicos:</span><span class="sxs-lookup"><span data-stu-id="aee99-128">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="aee99-129">Mensagem de phishing relatada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="aee99-129">User-reported phish message</span></span>
- <span data-ttu-id="aee99-130">URL clique em veredicto Change e links seguros de ATP bloquear substituição</span><span class="sxs-lookup"><span data-stu-id="aee99-130">URL click verdict change and ATP Safe Links block override</span></span>
- <span data-ttu-id="aee99-131">ZAP de malware</span><span class="sxs-lookup"><span data-stu-id="aee99-131">Malware ZAP</span></span>
- <span data-ttu-id="aee99-132">Phish de phishing</span><span class="sxs-lookup"><span data-stu-id="aee99-132">Phish ZAP</span></span>
- <span data-ttu-id="aee99-133">Investigações manuais (usando o Explorer)</span><span class="sxs-lookup"><span data-stu-id="aee99-133">Manual investigations (using Explorer)</span></span>

<span data-ttu-id="aee99-134">Vários outros guias estratégicos estão planejados para a fase 2.</span><span class="sxs-lookup"><span data-stu-id="aee99-134">Several more playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="aee99-135">Os guias estratégicos incluem investigação e recomendações</span><span class="sxs-lookup"><span data-stu-id="aee99-135">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="aee99-136">Cada manual inclui:</span><span class="sxs-lookup"><span data-stu-id="aee99-136">Each playbook includes:</span></span> 
- <span data-ttu-id="aee99-137">uma investigação raiz,</span><span class="sxs-lookup"><span data-stu-id="aee99-137">a root investigation,</span></span> 
- <span data-ttu-id="aee99-138">etapas para procurar outras ameaças potenciais e</span><span class="sxs-lookup"><span data-stu-id="aee99-138">steps to hunt down other potential threats, and</span></span> 
- <span data-ttu-id="aee99-139">correção de ameaça recomendada.</span><span class="sxs-lookup"><span data-stu-id="aee99-139">recommended threat remediation.</span></span>

<span data-ttu-id="aee99-140">Cada etapa de alto nível inclui muitas subetapas executadas para fornecer uma resposta detalhada, detalhada e exaustiva às ameaças.</span><span class="sxs-lookup"><span data-stu-id="aee99-140">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="aee99-141">Exemplo: mensagem de phishing relatada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="aee99-141">Example: User-reported phish message</span></span>

<span data-ttu-id="aee99-142">Quando um usuário em sua organização envia uma mensagem de email e o relata à Microsoft usando o [suplemento de mensagem de relatório para Outlook ou Outlook Web Access](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="aee99-142">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="aee99-143">Isso aciona um alerta informativo baseado no sistema que inicia automaticamente o guia estratégico de investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-143">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="aee99-144">Durante a fase de investigação de raiz, vários aspectos do email são avaliados.</span><span class="sxs-lookup"><span data-stu-id="aee99-144">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="aee99-145">Eles incluem:</span><span class="sxs-lookup"><span data-stu-id="aee99-145">These include:</span></span>
- <span data-ttu-id="aee99-146">Uma determinação sobre o tipo de ameaça que ela pode ser;</span><span class="sxs-lookup"><span data-stu-id="aee99-146">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="aee99-147">Quem o enviou;</span><span class="sxs-lookup"><span data-stu-id="aee99-147">Who sent it;</span></span>
- <span data-ttu-id="aee99-148">De onde o email foi enviado (infraestrutura de envio);</span><span class="sxs-lookup"><span data-stu-id="aee99-148">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="aee99-149">Se outras instâncias do email foram entregues ou bloqueadas;</span><span class="sxs-lookup"><span data-stu-id="aee99-149">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="aee99-150">Uma avaliação de nossos analistas;</span><span class="sxs-lookup"><span data-stu-id="aee99-150">An assessment from our analysts;</span></span>
- <span data-ttu-id="aee99-151">Se o email está associado a qualquer campanha conhecida;</span><span class="sxs-lookup"><span data-stu-id="aee99-151">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="aee99-152">e muito mais.</span><span class="sxs-lookup"><span data-stu-id="aee99-152">and more.</span></span>

<span data-ttu-id="aee99-153">Após a conclusão da investigação raiz, o guia estratégico fornece uma lista de ações recomendadas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="aee99-153">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="aee99-154">Em seguida, várias etapas de busca são executadas:</span><span class="sxs-lookup"><span data-stu-id="aee99-154">Next, several hunting steps are executed:</span></span>

- <span data-ttu-id="aee99-155">Mensagens de email semelhantes em outros clusters de email são pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="aee99-155">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="aee99-156">O sinal é compartilhado com outras plataformas, como o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="aee99-156">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="aee99-157">É feita uma determinação sobre se algum usuário clicou na mensagem de email suspeita.</span><span class="sxs-lookup"><span data-stu-id="aee99-157">A determination is made on whether any users have clicked through on the suspicious email message.</span></span>
- <span data-ttu-id="aee99-158">Uma verificação é feita entre O Office 365 [EOP](eop/exchange-online-protection-eop.md) e a [ATP](office-365-atp.md) para ver se há outras mensagens semelhantes relatadas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="aee99-158">A check is done across Office 365 [EOP](eop/exchange-online-protection-eop.md) and [ATP](office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="aee99-159">Uma verificação é feita para ver se um usuário foi comprometido.</span><span class="sxs-lookup"><span data-stu-id="aee99-159">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="aee99-160">Esta verificação utiliza sinais no [Microsoft Cloud app Security](https://docs.microsoft.com/cloud-app-security) e no [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlacionando qualquer evento ou alerta relacionado.</span><span class="sxs-lookup"><span data-stu-id="aee99-160">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related events or alerts.</span></span> 

<span data-ttu-id="aee99-161">Durante a fase de caça, riscos e ameaças são atribuídos a várias etapas de busca.</span><span class="sxs-lookup"><span data-stu-id="aee99-161">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="aee99-162">Correção é a fase final do guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="aee99-162">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="aee99-163">Durante esta fase, as etapas de correção são tomadas, com base nas fases de investigação e busca.</span><span class="sxs-lookup"><span data-stu-id="aee99-163">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="aee99-164">Introdução</span><span class="sxs-lookup"><span data-stu-id="aee99-164">Getting started</span></span>

<span data-ttu-id="aee99-165">Para acessar suas investigações, como administrador global do Office 365 ou administrador de segurança, vá para o centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança do Office 365 () e entre.</span><span class="sxs-lookup"><span data-stu-id="aee99-165">To access your investigations, as an Office 365 global administrator or security administrator, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="aee99-166">Em seguida, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="aee99-166">Then, do one of the following:</span></span>

- <span data-ttu-id="aee99-167">No painel de navegação à esquerda, vá para**investigações**de **Gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="aee99-167">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="aee99-168">ou</span><span class="sxs-lookup"><span data-stu-id="aee99-168">or</span></span>

- <span data-ttu-id="aee99-169">Visite o painel de gerenciamento de ameaças (no centro de conformidade do & de segurança, vá para o**painel** **Gerenciamento** > de ameaças).</span><span class="sxs-lookup"><span data-stu-id="aee99-169">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![Widgets do AIR](media/air-widgets.png)

<span data-ttu-id="aee99-171">Seus widgets do AIR serão exibidos na parte superior do [painel de segurança](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="aee99-171">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="aee99-172">Selecione um widget para começar.</span><span class="sxs-lookup"><span data-stu-id="aee99-172">Select a widget to get started.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="aee99-173">Investigações automatizadas</span><span class="sxs-lookup"><span data-stu-id="aee99-173">Automated investigations</span></span>

<span data-ttu-id="aee99-174">A página de investigações automatizadas mostra as investigações da organização e seus Estados atuais.</span><span class="sxs-lookup"><span data-stu-id="aee99-174">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Página de investigação principal para AIR](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="aee99-176">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-176">You can:</span></span>
- <span data-ttu-id="aee99-177">Navegue diretamente para uma investigação (selecione uma **ID de investigação**).</span><span class="sxs-lookup"><span data-stu-id="aee99-177">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="aee99-178">Aplicar filtros.</span><span class="sxs-lookup"><span data-stu-id="aee99-178">Apply filters.</span></span> <span data-ttu-id="aee99-179">Escolha um **tipo de investigação**, **intervalo de tempo**, **status**ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="aee99-179">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="aee99-180">Exporte os dados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="aee99-180">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="aee99-181">Gráfico de investigação</span><span class="sxs-lookup"><span data-stu-id="aee99-181">Investigation graph</span></span>

<span data-ttu-id="aee99-182">Ao abrir uma investigação específica, você verá a página de gráfico de investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-182">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="aee99-183">Esta página mostra todas as diferentes entidades: mensagens de email, usuários (e suas atividades) e dispositivos que foram investigados automaticamente como parte do alerta que foi acionado.</span><span class="sxs-lookup"><span data-stu-id="aee99-183">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Página de gráfico de investigação aérea](media/air-investigationgraphpage.png)

<span data-ttu-id="aee99-185">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-185">You can:</span></span>
- <span data-ttu-id="aee99-186">Obtenha uma visão geral da investigação atual.</span><span class="sxs-lookup"><span data-stu-id="aee99-186">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="aee99-187">Exibir um resumo dos intervalos de investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-187">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="aee99-188">Selecione um nó na visualização para exibir detalhes desse nó.</span><span class="sxs-lookup"><span data-stu-id="aee99-188">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="aee99-189">Selecione uma guia na parte superior para exibir os detalhes dessa guia.</span><span class="sxs-lookup"><span data-stu-id="aee99-189">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="aee99-190">Investigação de alerta</span><span class="sxs-lookup"><span data-stu-id="aee99-190">Alert investigation</span></span>

<span data-ttu-id="aee99-191">Na guia **alertas** de uma investigação, você pode ver todos os alertas relevantes para a investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-191">On the **Alerts** tab for an investigation, you can see all of the alerts relevant to the investigation.</span></span> <span data-ttu-id="aee99-192">Os detalhes incluem o alerta que disparou a investigação e outros alertas, como entrada arriscada, download em massa, etc., que são correlacionados à investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-192">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="aee99-193">A partir dessa página, um analista de segurança também pode exibir detalhes adicionais sobre alertas individuais.</span><span class="sxs-lookup"><span data-stu-id="aee99-193">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Página alertas de ar](media/air-investigationalertspage.png)

<span data-ttu-id="aee99-195">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-195">You can:</span></span>
- <span data-ttu-id="aee99-196">Obtenha uma visão geral do alerta de acionamento atual e de todos os alertas associados.</span><span class="sxs-lookup"><span data-stu-id="aee99-196">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="aee99-197">Selecione um alerta na lista para abrir uma página de sobrevôo que mostre detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="aee99-197">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="aee99-198">Investigação de email</span><span class="sxs-lookup"><span data-stu-id="aee99-198">Email investigation</span></span>

<span data-ttu-id="aee99-199">Na guia **email** de uma investigação, você pode ver todos os clusters de email identificados como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-199">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="aee99-200">Dado o volume simples de email que os usuários de uma organização enviam e recebem, o processo de</span><span class="sxs-lookup"><span data-stu-id="aee99-200">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="aee99-201">agrupar mensagens de email com base em atributos semelhantes de um cabeçalho de mensagem, corpo, URL e anexo;</span><span class="sxs-lookup"><span data-stu-id="aee99-201">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="aee99-202">separar emails mal-intencionados do email em bom estado; e</span><span class="sxs-lookup"><span data-stu-id="aee99-202">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="aee99-203">executar ações em mensagens de email mal-intencionadas</span><span class="sxs-lookup"><span data-stu-id="aee99-203">taking action on malicious email messages</span></span> 

<span data-ttu-id="aee99-204">pode levar várias horas.</span><span class="sxs-lookup"><span data-stu-id="aee99-204">can take many hours.</span></span> <span data-ttu-id="aee99-205">Agora, o ar automatiza esse processo, poupando o tempo e esforço da equipe de segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="aee99-205">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="aee99-206">Por exemplo, considere a imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="aee99-206">As an example, consider the following image.</span></span> <span data-ttu-id="aee99-207">O primeiro cluster de três mensagens de email foi considerado como phishing.</span><span class="sxs-lookup"><span data-stu-id="aee99-207">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="aee99-208">Outro cluster de mensagens semelhantes com o mesmo IP e assunto foi encontrado e é considerado mal-intencionado, pois alguns deles foram identificados como phishing durante a detecção inicial.</span><span class="sxs-lookup"><span data-stu-id="aee99-208">Another cluster of similar messages with the same IP and subject was found and is considered to be malicious, as some of them were identified as phish during initial detection.</span></span> 

![Página investigação de emails de ar](media/air-investigationemailpage.png)

<span data-ttu-id="aee99-210">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-210">You can:</span></span>
- <span data-ttu-id="aee99-211">Obtenha uma visão geral das ameaças e dos resultados de agrupamento atuais encontrados.</span><span class="sxs-lookup"><span data-stu-id="aee99-211">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="aee99-212">Clique em uma entidade de cluster ou uma lista de ameaças para abrir uma página de saída que mostra os detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="aee99-212">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Email de investigação de ar com detalhes de submenu](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a><span data-ttu-id="aee99-214">Investigação de usuário</span><span class="sxs-lookup"><span data-stu-id="aee99-214">User investigation</span></span>

<span data-ttu-id="aee99-215">Na guia **usuários** , você pode ver todos os usuários identificados como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-215">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="aee99-216">Por exemplo, na imagem a seguir, o AIR identificou indicadores de comprometimento e anomalias com base em uma nova regra de caixa de entrada que foi criada.</span><span class="sxs-lookup"><span data-stu-id="aee99-216">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="aee99-217">Detalhes adicionais (evidência) da investigação estão disponíveis por meio de exibições detalhadas nesta guia.</span><span class="sxs-lookup"><span data-stu-id="aee99-217">Additional details (evidence) of the investigation are available through detailed views within this tab.</span></span>

![Página usuários de investigação aérea](media/air-investigationuserspage.png)

<span data-ttu-id="aee99-219">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-219">You can:</span></span>
- <span data-ttu-id="aee99-220">Obtenha uma visão geral dos resultados do usuário identificados e dos riscos encontrados.</span><span class="sxs-lookup"><span data-stu-id="aee99-220">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="aee99-221">Selecione um usuário para abrir uma página de sobrevôo que mostre os detalhes completos do alerta.</span><span class="sxs-lookup"><span data-stu-id="aee99-221">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="aee99-222">Investigação de máquina</span><span class="sxs-lookup"><span data-stu-id="aee99-222">Machine investigation</span></span>

<span data-ttu-id="aee99-223">Na guia **computadores** , você pode ver todas as máquinas identificadas como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-223">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Página da máquina de investigação de ar](media/air-investigationmachinepage.png)

<span data-ttu-id="aee99-225">Como parte da investigação, o AIR correlaciona ameaças de email a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aee99-225">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="aee99-226">Por exemplo, uma investigação passa um hash de arquivo para o [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) para investigar.</span><span class="sxs-lookup"><span data-stu-id="aee99-226">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="aee99-227">Isso permite a investigação automatizada de máquinas relevantes para seus usuários e ajuda a garantir que as ameaças sejam tratadas tanto na nuvem quanto em seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aee99-227">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="aee99-228">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-228">You can:</span></span>
- <span data-ttu-id="aee99-229">Obtenha uma visão geral das máquinas e ameaças atuais encontradas.</span><span class="sxs-lookup"><span data-stu-id="aee99-229">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="aee99-230">Selecione uma máquina para abrir um modo de exibição que nas [investigações ATP relacionadas do Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="aee99-230">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="aee99-231">Investigação de entidade</span><span class="sxs-lookup"><span data-stu-id="aee99-231">Entity investigation</span></span>

<span data-ttu-id="aee99-232">Na guia **entidades** , você pode ver todas as máquinas identificadas como parte da investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-232">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="aee99-233">Aqui, você pode ver as entidades investigadas.</span><span class="sxs-lookup"><span data-stu-id="aee99-233">Here, you can see the investigated entities.</span></span> <span data-ttu-id="aee99-234">Você pode ver detalhes dos tipos de entidades, como mensagens de email, clusters, endereços IP, usuários e muito mais.</span><span class="sxs-lookup"><span data-stu-id="aee99-234">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="aee99-235">Você também pode ver quantas entidades foram analisadas e as ameaças que foram associadas a cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="aee99-235">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Página de entidades de investigação aérea](media/air-investigationentitiespage.png)

<span data-ttu-id="aee99-237">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-237">You can:</span></span>
- <span data-ttu-id="aee99-238">Obtenha uma visão geral das entidades e ameaças de investigação encontradas.</span><span class="sxs-lookup"><span data-stu-id="aee99-238">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="aee99-239">Selecione uma entidade para abrir uma página de saída que mostre os detalhes relacionados da entidade.</span><span class="sxs-lookup"><span data-stu-id="aee99-239">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Detalhes das entidades de investigação aérea](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="aee99-241">Log do guia estratégico</span><span class="sxs-lookup"><span data-stu-id="aee99-241">Playbook log</span></span>

<span data-ttu-id="aee99-242">Na guia **log** , você pode ver todas as etapas do guia estratégico que ocorreram durante a investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-242">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="aee99-243">O log captura um inventário completo de todas as ações concluídas por recursos de inteligência de ameaças do Office 365 como parte do ar.</span><span class="sxs-lookup"><span data-stu-id="aee99-243">The log captures a complete inventory of all actions completed by Office 365 Threat Intelligence capabilities as part of AIR.</span></span> <span data-ttu-id="aee99-244">Ele fornece uma visão clara de todas as etapas executadas, incluindo a própria ação, uma descrição e a duração do real do início ao fim.</span><span class="sxs-lookup"><span data-stu-id="aee99-244">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Página de log de investigação de ar](media/air-investigationlogpage.png)

<span data-ttu-id="aee99-246">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-246">You can:</span></span>
- <span data-ttu-id="aee99-247">Obtenha uma visão geral das etapas do guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="aee99-247">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="aee99-248">Exportar os resultados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="aee99-248">Export the results to a CSV file.</span></span>
- <span data-ttu-id="aee99-249">Filtrar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="aee99-249">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="aee99-250">Ações recomendadas</span><span class="sxs-lookup"><span data-stu-id="aee99-250">Recommended actions</span></span>

<span data-ttu-id="aee99-251">Na guia **ações** , você pode ver todas as ações do guia estratégico que são recomendadas para correção após a conclusão da investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-251">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="aee99-252">As ações capturam uma lista completa de todas as etapas que a Microsoft recomenda que você faça no final de uma investigação.</span><span class="sxs-lookup"><span data-stu-id="aee99-252">Actions capture a complete list of all the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="aee99-253">Você pode realizar ações de correção aqui selecionando uma ou mais ações.</span><span class="sxs-lookup"><span data-stu-id="aee99-253">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="aee99-254">Clicar em **aprovar** permitirá que a correção seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="aee99-254">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="aee99-255">(As permissões apropriadas podem ser necessárias.</span><span class="sxs-lookup"><span data-stu-id="aee99-255">(Appropriate permissions might be required.</span></span> <span data-ttu-id="aee99-256">Por exemplo, um leitor de segurança pode exibir ações, mas não aprová-las.)</span><span class="sxs-lookup"><span data-stu-id="aee99-256">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Página de ação de investigações aéreas](media/air-investigationactionspage.png)

<span data-ttu-id="aee99-258">Você pode:</span><span class="sxs-lookup"><span data-stu-id="aee99-258">You can:</span></span>
- <span data-ttu-id="aee99-259">Obtenha uma visão geral das ações recomendadas para o guia estratégico.</span><span class="sxs-lookup"><span data-stu-id="aee99-259">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="aee99-260">Selecione uma única ação ou várias ações.</span><span class="sxs-lookup"><span data-stu-id="aee99-260">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="aee99-261">Aprovar ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="aee99-261">Approve recommended actions.</span></span> <span data-ttu-id="aee99-262">(Estes são iniciados imediatamente com comentários.)</span><span class="sxs-lookup"><span data-stu-id="aee99-262">(These are started immediately with comments.)</span></span>
- <span data-ttu-id="aee99-263">Exportar os resultados para um arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="aee99-263">Export the results to a CSV file.</span></span>
- <span data-ttu-id="aee99-264">Filtrar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="aee99-264">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="aee99-265">Como obter o AIR</span><span class="sxs-lookup"><span data-stu-id="aee99-265">How to get AIR</span></span>

<span data-ttu-id="aee99-266">No momento, o AIR está em visualização.</span><span class="sxs-lookup"><span data-stu-id="aee99-266">Currently, AIR is in preview.</span></span> <span data-ttu-id="aee99-267">Quando lançado, o ar será incluído nas seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="aee99-267">When released, AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="aee99-268">Microsoft 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="aee99-268">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="aee99-269">Office 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="aee99-269">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="aee99-270">Proteção contra ameaças da Microsoft</span><span class="sxs-lookup"><span data-stu-id="aee99-270">Microsoft Threat Protection</span></span>
- <span data-ttu-id="aee99-271">Office 365 plano avançado de proteção contra ameaças 2</span><span class="sxs-lookup"><span data-stu-id="aee99-271">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="aee99-272">Para saber mais sobre a disponibilidade de recursos, visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="aee99-272">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
