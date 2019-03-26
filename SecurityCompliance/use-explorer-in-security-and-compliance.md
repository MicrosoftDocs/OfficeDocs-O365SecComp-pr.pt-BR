---
title: Usar o explorador de ameaças no &amp; centro de conformidade de segurança
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
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Saiba mais sobre o Explorer (também chamado de Gerenciador de ameaças &amp; ) no centro de conformidade de segurança.
ms.openlocfilehash: 202898873bb9611c747aed335d295c749c7cd0fa
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732254"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="75f15-103">Usar o explorador de ameaças no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="75f15-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="75f15-104">Se sua organização tiver o [plano de proteção avançada contra ameaças do Office 365](office-365-ti.md)e tiver as permissões necessárias, você poderá usar o Gerenciador de ameaças para identificar e analisar ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="75f15-105">Por exemplo, você pode identificar e excluir emails mal-intencionados que foram entregues ou confira o malware que foi detectado pelos recursos de segurança do Office 365.</span><span class="sxs-lookup"><span data-stu-id="75f15-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="75f15-106">O Gerenciador de ameaças (também mencionado como Explorer) é uma poderosa ferramenta quase em tempo real para ajudar as equipes de operações de segurança a investigar e responder &amp; a ameaças no centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="75f15-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="75f15-108">Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75f15-109">O Office 365 Threat Intelligence é agora o Office 365 Advanced Threat Protection Plan 2, juntamente com outros recursos de proteção contra ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-109">Office 365 Threat Intelligence is now Office 365 Advanced Threat Protection Plan 2, along with additional threat protection capabilities.</span></span> <span data-ttu-id="75f15-110">Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="75f15-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="75f15-111">Visão geral do Explorer</span><span class="sxs-lookup"><span data-stu-id="75f15-111">Explorer overview</span></span>

<span data-ttu-id="75f15-112">Se sua organização tiver [recursos de investigação e resposta contra ameaças do Office 365](office-365-ti.md) (isso é incluído no plano ATP 2) e você tiver as permissões necessárias, poderá usar o explorador de ameaças (também chamado de Gerenciador) para identificar e analisar ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-112">If your organization has [Office 365 Threat investigation and response capabilities](office-365-ti.md) (this is included in ATP Plan 2), and you have the necessary permissions, you can use Threat Explorer (also referred to as Explorer) to identify and analyze threats.</span></span> <span data-ttu-id="75f15-113">(No centro de &amp; conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.)</span><span class="sxs-lookup"><span data-stu-id="75f15-113">(In the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.)</span></span>

![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

<span data-ttu-id="75f15-115">Este artigo descreve algumas coisas que você pode fazer com o Explorer (há muito mais possibilidades):</span><span class="sxs-lookup"><span data-stu-id="75f15-115">This article describes a few things you can do with Explorer (there are many more possibilities):</span></span>

- <span data-ttu-id="75f15-116">[Veja quais tipos de malware foram detectados no email](#see-malware-detected-in-email-by-technology)e por tecnologia de proteção contra ameaças (proteção contra malware, anexos seguros de ATP etc.)</span><span class="sxs-lookup"><span data-stu-id="75f15-116">[See what kinds of malware were detected in email](#see-malware-detected-in-email-by-technology), and by threat protection technology (anti-malware protection, ATP Safe Attachments, etc.)</span></span>

- <span data-ttu-id="75f15-117">[Exibir dados sobre links de phishing (URLs)](#view-data-about-phishing-urls-and-click-verdict)e o que o verdicts de clique (URLs bloqueados, permitidos ou visitados apesar de avisos)</span><span class="sxs-lookup"><span data-stu-id="75f15-117">[View data about phishing links (URLs)](#view-data-about-phishing-urls-and-click-verdict), and what the click verdicts were (URLs blocked, allowed, or visited despite warnings)</span></span>

- <span data-ttu-id="75f15-118">[Revise mensagens de email relatadas como lixo eletrônico, não lixo eletrônico ou phishing](#review-email-messages-reported-by-users)e identifique as tendências (como um número maior do que o normal de mensagens relatadas como phishing)</span><span class="sxs-lookup"><span data-stu-id="75f15-118">[Review email messages that were reported as Junk, Not Junk, or Phishing](#review-email-messages-reported-by-users), and identify any trends (such as a larger than usual number of messages reported as Phish)</span></span> 

## <a name="see-malware-detected-in-email-by-technology"></a><span data-ttu-id="75f15-119">ConFira malware detectado em email por tecnologia</span><span class="sxs-lookup"><span data-stu-id="75f15-119">See malware detected in email by technology</span></span>

<span data-ttu-id="75f15-120">Suponha que você queira ver o malware detectado no email e por qual tecnologia no Office 365.</span><span class="sxs-lookup"><span data-stu-id="75f15-120">Suppose you want to see malware that was detected in email, and by what technology in Office 365.</span></span> <span data-ttu-id="75f15-121">Para fazer isso, use o [email _GT_ malware](threat-explorer-views.md#email--malware) View do Explorer.</span><span class="sxs-lookup"><span data-stu-id="75f15-121">To do this, use the [Email > Malware](threat-explorer-views.md#email--malware) view of Explorer.</span></span>

1. <span data-ttu-id="75f15-122">no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-122">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="75f15-123">No menu **Exibir** , escolha**malware**de **email** > .</span><span class="sxs-lookup"><span data-stu-id="75f15-123">In the **View** menu, choose **Email** > **Malware**.</span></span><br/><span data-ttu-id="75f15-124">![Menu Exibir para Explorer](media/ExplorerViewEmailMalwareMenu.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-124">![View menu for Explorer](media/ExplorerViewEmailMalwareMenu.png)</span></span><br/>
3. <span data-ttu-id="75f15-125">Clique em **remetente**e escolha**tecnologia de detecção** **básica** > .</span><span class="sxs-lookup"><span data-stu-id="75f15-125">Click **Sender**, and then choose **Basic** > **Detection technology**.</span></span><br/><span data-ttu-id="75f15-126">Agora, suas tecnologias de detecção estão disponíveis como filtros para o relatório.</span><span class="sxs-lookup"><span data-stu-id="75f15-126">Your detection technologies are now available as filters for the report.</span></span><br/><span data-ttu-id="75f15-127">![Tecnologias de detecção de malware](media/ExplorerEmailMalwareDetectionTech.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-127">![Malware detection technologies](media/ExplorerEmailMalwareDetectionTech.png)</span></span><br/> 
4. <span data-ttu-id="75f15-128">Selecione uma opção e, em seguida, clique no botão atualizar para aplicar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="75f15-128">Select an option, and then click the Refresh button to apply that filter.</span></span><br/>![Tecnologia de detecção selecionada](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

<span data-ttu-id="75f15-130">O relatório é atualizado para mostrar o malware de resultados detectado no email, usando a opção de tecnologia que você selecionou.</span><span class="sxs-lookup"><span data-stu-id="75f15-130">The report refreshes to show the results malware detected in email, using the technology option you selected.</span></span> <span data-ttu-id="75f15-131">A partir daqui, você pode realizar uma análise adicional.</span><span class="sxs-lookup"><span data-stu-id="75f15-131">From here, you can conduct further analysis.</span></span>

## <a name="view-data-about-phishing-urls-and-click-verdict"></a><span data-ttu-id="75f15-132">Exibir dados sobre URLs de phishing e clicar em veredicto</span><span class="sxs-lookup"><span data-stu-id="75f15-132">View data about phishing URLs and click verdict</span></span>

<span data-ttu-id="75f15-133">Suponha que você queira ver as tentativas de phishing por meio de URLs no email, incluindo uma lista de URLs que foram permitidas, bloqueadas e substituídas.</span><span class="sxs-lookup"><span data-stu-id="75f15-133">Suppose you want to see phishing attempts through URLs in email, including a list of URLs that were allowed, blocked, and overridden.</span></span> <span data-ttu-id="75f15-134">Para fazer isso, use o [E-mail _GT_ Phish](threat-explorer-views.md#email--phish) View do Explorer.</span><span class="sxs-lookup"><span data-stu-id="75f15-134">To do this, use the [Email > Phish](threat-explorer-views.md#email--phish) view of Explorer.</span></span>

1. <span data-ttu-id="75f15-135">no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-135">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="75f15-136">No menu **Exibir** , escolha**phishing**de **email** > .</span><span class="sxs-lookup"><span data-stu-id="75f15-136">In the **View** menu, choose **Email** > **Phish**.</span></span><br/><span data-ttu-id="75f15-137">![Menu Exibir para Explorer](media/ExplorerViewEmailPhishMenu.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-137">![View menu for Explorer](media/ExplorerViewEmailPhishMenu.png)</span></span><br/>
3. <span data-ttu-id="75f15-138">Clique em **remetente**e, em seguida, escolha **URLs** > **clique em veredicto**.</span><span class="sxs-lookup"><span data-stu-id="75f15-138">Click **Sender**, and then choose **URLs** > **Click verdict**.</span></span>
4. <span data-ttu-id="75f15-139">Selecione uma ou mais opções, como **bloqueado** e o **bloco substituído**, e clique no botão **Atualizar** para aplicar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="75f15-139">Select one or more options, such as **Blocked** and **Block overridden**, and then click the **Refresh** button to apply that filter.</span></span><br/><span data-ttu-id="75f15-140">![URLs e clique em verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-140">![URLs and click verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)</span></span><br/>

<span data-ttu-id="75f15-141">O relatório é atualizado para mostrar URLs de phishing detectadas em emails que foram bloqueados (ou visitados apesar de um aviso), junto com o status de entrega de email.</span><span class="sxs-lookup"><span data-stu-id="75f15-141">The report refreshes to show detected phishing URLs in email that were blocked (or visited despite a warning), along with email delivery status.</span></span> <span data-ttu-id="75f15-142">A partir daqui, você pode realizar uma análise adicional.</span><span class="sxs-lookup"><span data-stu-id="75f15-142">From here, you can conduct further analysis.</span></span> <span data-ttu-id="75f15-143">Por exemplo, abaixo do gráfico, você pode ver as principais URLs que foram bloqueadas no email da sua organização.</span><span class="sxs-lookup"><span data-stu-id="75f15-143">For example, below the chart, you can see the top URLs that were blocked in your organization's email.</span></span> 

![URLs do Explorer que foram bloqueadas](media/ExplorerPhishClickVerdictURLs.png) 

<span data-ttu-id="75f15-145">Selecione uma URL para exibir informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="75f15-145">Select a URL to view more detailed information.</span></span>

## <a name="review-email-messages-reported-by-users"></a><span data-ttu-id="75f15-146">Analisar mensagens de email relatadas por usuários</span><span class="sxs-lookup"><span data-stu-id="75f15-146">Review email messages reported by users</span></span>

<span data-ttu-id="75f15-147">Suponha que você queira ver as mensagens de email que os usuários em sua organização relataram como lixo eletrônico, não lixo eletrônico ou phishing usando o [suplemento de mensagem de relatório para o Outlook e o Outlook na Web](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="75f15-147">Suppose you want to see email messages that users in your organization have reported as Junk, Not Junk, or Phishing by using the [Report Message add-in for Outlook and Outlook on the web](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="75f15-148">Para fazer isso, use a exibição de [email > relatada pelo usuário](threat-explorer-views.md#email--user-reported) do Explorer.</span><span class="sxs-lookup"><span data-stu-id="75f15-148">To do this, use the [Email > User-reported](threat-explorer-views.md#email--user-reported) view of Explorer.</span></span>

1. <span data-ttu-id="75f15-149">no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.</span><span class="sxs-lookup"><span data-stu-id="75f15-149">In the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), choose **Threat management** > **Explorer**.</span></span>
2. <span data-ttu-id="75f15-150">No menu **Exibir** , escolha **email** > **reportado pelo usuário**.</span><span class="sxs-lookup"><span data-stu-id="75f15-150">In the **View** menu, choose **Email** > **User-reported**.</span></span><br/><span data-ttu-id="75f15-151">![Menu Exibir para Explorer](media/ExplorerViewMenuEmailUserReported.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-151">![View menu for Explorer](media/ExplorerViewMenuEmailUserReported.png)</span></span><br/>
3. <span data-ttu-id="75f15-152">Clique em **remetente**e, em seguida, escolha**tipo de relatório** **básico** > .</span><span class="sxs-lookup"><span data-stu-id="75f15-152">Click **Sender**, and then choose **Basic** > **Report type**.</span></span>
4. <span data-ttu-id="75f15-153">Selecione uma opção, como **Phish**, e clique no botão **Atualizar** .</span><span class="sxs-lookup"><span data-stu-id="75f15-153">Select an option, such as **Phish**, and then click the **Refresh** button.</span></span> <br/><span data-ttu-id="75f15-154">![Phishing relatado pelo usuário](media/EmailUserReportedReportType.png)</span><span class="sxs-lookup"><span data-stu-id="75f15-154">![User-reported phish](media/EmailUserReportedReportType.png)</span></span><br/> 

<span data-ttu-id="75f15-155">O relatório é atualizado para mostrar dados sobre mensagens de email que as pessoas em sua organização relataram como uma tentativa de phishing.</span><span class="sxs-lookup"><span data-stu-id="75f15-155">The report refreshes to show data about email messages that people in your organization have reported as a phishing attempt.</span></span> <span data-ttu-id="75f15-156">Você pode usar essas informações para realizar mais análises e, se necessário, ajustar as [políticas de anti-phishing da ATP](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="75f15-156">You can use this information to conduct further analysis, and if necessary, adjust your [ATP anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="theres-more"></a><span data-ttu-id="75f15-157">Há mais!</span><span class="sxs-lookup"><span data-stu-id="75f15-157">There's more!</span></span>

<span data-ttu-id="75f15-158">Além dos três cenários descritos neste artigo, você tem vários cenários de relatórios disponíveis no Explorer.</span><span class="sxs-lookup"><span data-stu-id="75f15-158">In addition to the three scenarios outlined in this article, you have many reporting scenarios available with Explorer.</span></span> <span data-ttu-id="75f15-159">Aqui estão alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="75f15-159">Here are a few more examples:</span></span>

- [<span data-ttu-id="75f15-160">Encontre e investigue emails mal-intencionados que foram entregues</span><span class="sxs-lookup"><span data-stu-id="75f15-160">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)

- [<span data-ttu-id="75f15-161">Exibir arquivos mal-intencionados detectados no SharePoint Online, no OneDrive e no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="75f15-161">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)

- [<span data-ttu-id="75f15-162">Obter uma visão geral dos modos de exibição no explorador de ameaças</span><span class="sxs-lookup"><span data-stu-id="75f15-162">Get an overview of the views in Threat Explorer</span></span>](threat-explorer-views.md)

## <a name="how-to-get-explorer"></a><span data-ttu-id="75f15-163">Como obter o Explorer</span><span class="sxs-lookup"><span data-stu-id="75f15-163">How to get Explorer</span></span>

<span data-ttu-id="75f15-164">O Explorer está incluído no [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="75f15-164">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="75f15-165">Para exibir e usar o Explorer, você deve ter as permissões apropriadas, como aquelas concedidas a um administrador de segurança ou leitor de segurança.</span><span class="sxs-lookup"><span data-stu-id="75f15-165">To view and use Explorer, you must have appropriate permissions, such as those granted to a security administrator or security reader.</span></span> 

- <span data-ttu-id="75f15-166">Para o centro &amp; de conformidade de segurança, você deve ter uma das seguintes funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="75f15-166">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="75f15-167">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="75f15-167">Organization Management</span></span>
    - <span data-ttu-id="75f15-168">Administrador de segurança (pode ser atribuído no centro[https://aad.portal.azure.com](https://aad.portal.azure.com)de administração do Azure Active Directory)</span><span class="sxs-lookup"><span data-stu-id="75f15-168">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="75f15-169">Leitor de segurança</span><span class="sxs-lookup"><span data-stu-id="75f15-169">Security Reader</span></span>

- <span data-ttu-id="75f15-170">Para o Exchange Online, você deve ter uma das seguintes funções atribuídas no centro de administração do Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() ou com cmdlets do PowerShell (Confira [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="75f15-170">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="75f15-171">Gerenciamento de Organização</span><span class="sxs-lookup"><span data-stu-id="75f15-171">Organization Management</span></span>
    - <span data-ttu-id="75f15-172">Gerenciamento de Organização Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="75f15-172">View-only Organization Management</span></span>
    - <span data-ttu-id="75f15-173">Função de Destinatários Somente para Exibição</span><span class="sxs-lookup"><span data-stu-id="75f15-173">View-Only Recipients role</span></span>
    - <span data-ttu-id="75f15-174">Gerenciamento de Conformidade</span><span class="sxs-lookup"><span data-stu-id="75f15-174">Compliance Management</span></span>

<span data-ttu-id="75f15-175">Para saber mais, confira os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="75f15-175">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="75f15-176">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="75f15-176">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="75f15-177">Permissões de recursos no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="75f15-177">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
## <a name="related-topics"></a><span data-ttu-id="75f15-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75f15-178">Related topics</span></span>

- [<span data-ttu-id="75f15-179">Investigação e resposta automatizadas (AIR)</span><span class="sxs-lookup"><span data-stu-id="75f15-179">Automated Investigation and Response (AIR)</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="75f15-180">Modos de exibição do Gerenciador de ameaças</span><span class="sxs-lookup"><span data-stu-id="75f15-180">Threat Explorer views</span></span>](threat-explorer-views.md)

- [<span data-ttu-id="75f15-181">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="75f15-181">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
