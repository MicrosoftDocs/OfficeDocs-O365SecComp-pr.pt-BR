---
title: Usar o Explorer no centro &amp; de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection: M365-security-compliance
description: Saiba mais sobre o Explorer (também chamado de Gerenciador de ameaças &amp; ) no centro de conformidade de segurança.
ms.openlocfilehash: 439a7d53e185e12ddd5d2e19b9d88bd8c9b47dad
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218981"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="842ee-103">Usar o Explorer no centro &amp; de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="842ee-103">Use Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="842ee-p101">Se sua organização tiver o [Office 365 Threat Intelligence](office-365-ti.md)e você tiver as permissões necessárias, você poderá usar o Explorer para identificar e analisar ameaças. Por exemplo, você pode identificar e excluir emails mal-intencionados que foram entregues ou confira o malware que foi detectado pelos recursos de segurança do Office 365. O Explorer (também chamado de Gerenciador de ameaças) é um relatório avançado próximo a tempo real no centro &amp; de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="842ee-p101">If your organization has [Office 365 Threat Intelligence](office-365-ti.md), and you have the necessary permissions, you can use Explorer to identify and analyze threats. For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features. Explorer (also referred to as Threat Explorer) is a powerful near real-time report in the Security &amp; Compliance Center.</span></span>
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="842ee-108">Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="842ee-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="842ee-p102">A partir de fevereiro de 2019 e saindo dos próximos meses, o Office 365 Threat Intelligence está se tornando o Office 365 Advanced Threat Protection Plan 2, com recursos adicionais de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="842ee-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="842ee-111">Visão geral do Explorer</span><span class="sxs-lookup"><span data-stu-id="842ee-111">Explorer overview</span></span>

<span data-ttu-id="842ee-p103">O Explorer exibe informações sobre o malware suspeito em emails e arquivos no Office 365, bem como outras ameaças de segurança e riscos à sua organização. Quando você abre o Explorer pela primeira vez, o modo de exibição padrão mostra as detecções de malware do antivírus nos últimos sete dias. O Explorer também pode mostrar recursos de proteção de segurança no Office 365, incluindo [links seguros](atp-safe-links.md) e [anexos seguros](atp-safe-attachments.md) e pode ser modificado para mostrar dados nos últimos 30 dias.</span><span class="sxs-lookup"><span data-stu-id="842ee-p103">Explorer displays information about suspected malware in email and files in Office 365, as well as other security threats and risks to your organization. When you first open Explorer, the default view shows malware detections from antivirus for the past 7 days. Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span>
  
![Explorer mostra informações sobre os principais malware e usuários direcionados](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="842ee-116">Use o menu Exibir para alterar as informações que são exibidas.</span><span class="sxs-lookup"><span data-stu-id="842ee-116">Use the View menu to change what information is displayed.</span></span>
  
![O menu Exibir do Explorer](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="842ee-p104">O Explorer tem vários recursos de filtragem e consulta que permitem detalhar detalhes, como os principais usuários direcionados, famílias de malware principais e muito mais. Cada tipo de relatório oferece várias maneiras de exibir e explorar dados.</span><span class="sxs-lookup"><span data-stu-id="842ee-p104">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, and more. Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="842ee-p105">Não use caracteres curinga, como um asterisco (\*) ou um ponto de interrogação (?), com o Explorer. Quando você pesquisar o campo assunto de mensagens de email, o Explorer executará a correspondência parcial e produzirá resultados similares a uma pesquisa curinga.</span><span class="sxs-lookup"><span data-stu-id="842ee-p105">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer. When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="842ee-122">Malware \> de email</span><span class="sxs-lookup"><span data-stu-id="842ee-122">Email \> Malware</span></span>

<span data-ttu-id="842ee-123">Este modo de exibição mostra mensagens de email identificadas como contendo malware.</span><span class="sxs-lookup"><span data-stu-id="842ee-123">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="842ee-124">Exibir informações no gráfico por família de malware, domínio do remetente, IP do remetente, status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365) e tecnologia de detecção (como o malware foi detectado).</span><span class="sxs-lookup"><span data-stu-id="842ee-124">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Exibir dados sobre malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="842ee-126">Abaixo do gráfico, veja detalhes sobre as principais famílias de malware, principais usuários direcionados e mais detalhes sobre mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="842ee-126">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="842ee-127">Phishing \> de email</span><span class="sxs-lookup"><span data-stu-id="842ee-127">Email \> Phish</span></span>

<span data-ttu-id="842ee-128">Este modo de exibição mostra mensagens de email identificadas como tentativas de phishing.</span><span class="sxs-lookup"><span data-stu-id="842ee-128">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="842ee-129">Exibir informações por domínio do remetente, IP do remetente e status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365).</span><span class="sxs-lookup"><span data-stu-id="842ee-129">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Exibir dados sobre email identificados como tentativas de phishing](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="842ee-131">Abaixo do gráfico, veja mais detalhes sobre mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="842ee-131">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="842ee-132">Emails \> relatados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="842ee-132">Email \> User-reported</span></span>

<span data-ttu-id="842ee-133">Este modo de exibição mostra o email que os usuários relataram como lixo eletrônico, não lixo eletrônico ou email de phishing.</span><span class="sxs-lookup"><span data-stu-id="842ee-133">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="842ee-134">Exibir informações por tipo de relatório (a determinação do usuário que o email era lixo eletrônico, não lixo eletrônico ou Phish) e por motivo de entrega (motivos pelos quais o email entrou em um local específico, como uma política de filtro de spam, uma regra de fluxo de emails, uma lista de remetentes bloqueados, uma lista de remetentes seguros, etc.).</span><span class="sxs-lookup"><span data-stu-id="842ee-134">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Exibir dados sobre usuários de email relatados como lixo eletrônico, não lixo eletrônico ou phishing](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="842ee-136">Abaixo do gráfico, veja mais detalhes sobre mensagens de email específicas, como a linha de assunto, o endereço IP do remetente, o usuário que informou a mensagem como lixo eletrônico, não lixo eletrônico ou Phish e muito mais.</span><span class="sxs-lookup"><span data-stu-id="842ee-136">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="842ee-137">Enviar \> todos os emails</span><span class="sxs-lookup"><span data-stu-id="842ee-137">Email \> All mail</span></span>

<span data-ttu-id="842ee-138">Este modo de exibição mostra uma visão detalhada da atividade de email, incluindo emails identificados como mal-intencionados devido a phishing ou malware, bem como todos os emails não-mal-intencionados (emails, spam e emails em massa normais).</span><span class="sxs-lookup"><span data-stu-id="842ee-138">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="842ee-139">Se você receber um erro que leia **muitos dados a serem exibidos**, adicione um filtro e, se necessário, restrinja o intervalo de datas que você está exibindo.</span><span class="sxs-lookup"><span data-stu-id="842ee-139">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="842ee-p106">Para aplicar um filtro, escolha **remetente**, selecione um item na lista e clique no botão atualizar. No nosso exemplo, usamos a **tecnologia de detecção** como um filtro (há várias opções disponíveis). Exibir informações por remetente, domínio do remetente, destinatários, assunto, nome do arquivo de anexo, família de malware, status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365), tecnologia de detecção (como o malware foi detectado) e adicionais.</span><span class="sxs-lookup"><span data-stu-id="842ee-p106">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button. In our example, we used **Detection technology** as a filter (there are several options available). View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Exibir dados sobre o email detectado por tecnologia de detecção](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="842ee-144">Abaixo do gráfico, veja mais detalhes sobre mensagens de email específicas, como linha de assunto, destinatário, remetente, status e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="842ee-144">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="842ee-145">Malware \> de conteúdo</span><span class="sxs-lookup"><span data-stu-id="842ee-145">Content \> Malware</span></span>

<span data-ttu-id="842ee-146">Este modo de exibição mostra arquivos que foram identificados como mal-intencionados no SharePoint Online, no OneDrive for Business e no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="842ee-146">This view shows files that were identified as malicious in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="842ee-147">Exibir informações pela família de malware, tecnologia de detecção (como o malware foi detectado) e carga de trabalho (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="842ee-147">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Exibir dados sobre malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="842ee-149">Abaixo do gráfico, veja mais detalhes sobre arquivos específicos, como o nome do arquivo anexo, carga de trabalho, tamanho do arquivo, que modificou o arquivo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="842ee-149">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="842ee-150">(Novo!) Recursos de clique para filtrar</span><span class="sxs-lookup"><span data-stu-id="842ee-150">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="842ee-p107">Novo no Explorer é a capacidade de clicar para filtrar. A partir do final de maio de 2018, quando você clica em um item na legenda, esse item se torna um filtro para o relatório. Por exemplo, vamos supor que estamos examinando o modo de exibição de malware no Explorer:</span><span class="sxs-lookup"><span data-stu-id="842ee-p107">New to Explorer is the ability to click to filter. Beginning in late May 2018, when you click an item in the legend, that item becomes a filter for the report. For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="842ee-155">Clicar em **acionamento ATP** neste gráfico resultará em um modo de exibição como este:</span><span class="sxs-lookup"><span data-stu-id="842ee-155">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer filtrado para exibir somente os resultados do ATO acionamento](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="842ee-p108">Neste modo de exibição, agora estamos examinando dados para arquivos que foram destruídodos por [anexos seguros do Office 365 ATP](atp-safe-attachments.md). Abaixo do gráfico, podemos ver detalhes sobre mensagens de email específicas que tinham anexos detectados por anexos seguros de ATP.</span><span class="sxs-lookup"><span data-stu-id="842ee-p108">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md). Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Detalhes específicos sobre mensagens de email com anexos detectados](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="842ee-160">Selecionar um ou mais itens ativa o menu **ações** , que oferece várias opções de escolha para os itens selecionados.</span><span class="sxs-lookup"><span data-stu-id="842ee-160">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Selecionar um item ativa o menu ações](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="842ee-162">A capacidade de filtrar em um clique e navegar para detalhes específicos pode poupar muito tempo na investigação de ameaças.</span><span class="sxs-lookup"><span data-stu-id="842ee-162">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="842ee-163">Como faço para obter o Explorer?</span><span class="sxs-lookup"><span data-stu-id="842ee-163">How do I get Explorer?</span></span>

<span data-ttu-id="842ee-164">O Explorer está incluído no [Office 365 Threat Intelligence](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="842ee-164">Explorer is included in [Office 365 Threat Intelligence](office-365-ti.md).</span></span> 

<span data-ttu-id="842ee-p109">Você deve ter permissões apropriadas, como aquelas concedidas a um administrador de segurança ou leitor de segurança para exibir e usar o Explorer. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="842ee-p109">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="842ee-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="842ee-167">Related topics</span></span>

[<span data-ttu-id="842ee-168">Relatórios e insights no centro de conformidade de &amp; segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="842ee-168">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="842ee-169">Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)</span><span class="sxs-lookup"><span data-stu-id="842ee-169">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="842ee-170">Proteção antispam e antimalware do Office 365</span><span class="sxs-lookup"><span data-stu-id="842ee-170">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

