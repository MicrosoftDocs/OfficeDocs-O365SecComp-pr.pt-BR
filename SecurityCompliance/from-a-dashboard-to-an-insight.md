---
title: Passo a passo – de um painel para um insight
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
description: Saiba como você pode ir de um painel para um insight com ações recomendadas na segurança &amp; Centro de conformidade.
ms.openlocfilehash: 933bf6e86bc1ddce9259d071b69654f68e4dd370
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706145"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="4e46a-103">Passo a passo – de um painel para um insight</span><span class="sxs-lookup"><span data-stu-id="4e46a-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="4e46a-104">Se estiver familiarizado com [relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md), ele pode ser útil para visualizar como você pode facilmente navegar de um painel para um insight e ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="4e46a-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="4e46a-p101">Essa é uma das diversas orientações para a segurança &amp; Centro de conformidade. Para ver as orientações adicionais, consulte a seção de [Tópicos relacionados](#related-topics) .</span><span class="sxs-lookup"><span data-stu-id="4e46a-p101">This is one of several walkthroughs for the Security &amp; Compliance Center. To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="4e46a-107">Passo a passo: de um painel para um insight</span><span class="sxs-lookup"><span data-stu-id="4e46a-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="4e46a-p102">Vamos examinar o fluxo de um painel para um relatório para um insight e a ação. (Isto é um exemplo breve [intelligence falso](learn-about-spoof-intelligence.md) ).</span><span class="sxs-lookup"><span data-stu-id="4e46a-p102">Let's walk through the flow from a dashboard to a report to an insight and action. (This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="4e46a-p103">Começamos com o painel de segurança no [segurança &amp; Centro de conformidade](https://security.microsoft.com). (Vá para **gerenciamento de ameaça** \> **Dashboard**.)</span><span class="sxs-lookup"><span data-stu-id="4e46a-p103">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://security.microsoft.com). (Go to **Threat management** \> **Dashboard**.)</span></span>
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciamento de ameaça \> painel](media/05a38660-eb13-4960-a266-11809c453d95.png)
  
2. <span data-ttu-id="4e46a-p104">Na linha **ideias** , podemos Observe um insight indicando que precisamos examinar alguns domínios que podem ser suspeitos. (Na linha **ideias** , clique **pares de domínio**).</span><span class="sxs-lookup"><span data-stu-id="4e46a-p104">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious. (In the **Insights** row, click **Domain pairs**.)</span></span>
    
    ![A linha Insights menções preocupações de falsificação potenciais](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)
  
3. <span data-ttu-id="4e46a-p105">Podemos obter uma lista de atividades relacionadas a falsificar intelligence. Estas são as instâncias onde as mensagens de email são enviadas que pareçam que eles provém de nossa organização, mas, na verdade, enviados a partir outra organização. O objetivo é determinar se as mensagens falsificadas estão autorizadas ou não.</span><span class="sxs-lookup"><span data-stu-id="4e46a-p105">We get a list of activities related to spoof intelligence. These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization. The goal is to determine whether the spoofed messages are authorized or not.</span></span>
    
    ![Realizar a falsificação ideias de inteligência de dados](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)
  
    <span data-ttu-id="4e46a-p106">Nesta lista, podemos classificar as informações por contagem de mensagem, data que última foi detectada a falsificação e mais. (Clique em títulos de coluna, **a contagem de mensagem** ou **visto pela última vez** para ver como classificação funciona).</span><span class="sxs-lookup"><span data-stu-id="4e46a-p106">In this list, we can sort the information by message count, date the spoofing was last detected, and more. (Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="4e46a-p107">Selecionar um item na lista abre um painel de detalhes, onde podemos ver informações adicionais, incluindo mensagens de email semelhantes que foram detectadas. (Clique em um item na lista e revise as informações e recomendações).</span><span class="sxs-lookup"><span data-stu-id="4e46a-p107">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected. (Click an item in the list, and review the information and recommendations.)</span></span>
    
    ![Selecionar um item é aberto um painel de detalhes](media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)
  
5. <span data-ttu-id="4e46a-p108">Observe que, na parte superior do painel, temos a opção para adicionar remetente à lista de remetentes permitidos da nossa organização. (Não selecione **lista de permissões de adicionar ao remetente 'AllowedtoSpoof'** até que você tiver certeza que deseja fazer isso. [Saiba mais sobre inteligência de falsificação](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="4e46a-p108">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list. (Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this. [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span>
    
    ![Você pode autorizar um remetente](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)
  
<span data-ttu-id="4e46a-129">Dessa maneira, é possível mover de um painel para ideias e ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="4e46a-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="4e46a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e46a-130">Related topics</span></span>

[<span data-ttu-id="4e46a-131">Passo a passo: a partir da perspectiva de um relatório detalhado</span><span class="sxs-lookup"><span data-stu-id="4e46a-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="4e46a-132">Passo a passo: de um relatório detalhado para um insight</span><span class="sxs-lookup"><span data-stu-id="4e46a-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

