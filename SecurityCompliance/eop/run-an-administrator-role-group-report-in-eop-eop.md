---
title: 'Executar um relatório de grupo de funções de administrador no EOP '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Quando um administrador adiciona ou remove membros dos grupos de função de administrador, o Microsoft Proteção do Exchange Online (EOP) registra cada ocorrência.
ms.openlocfilehash: 752def771d95fcfbb3f7cbe0bc86a33b3967716d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692710"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a><span data-ttu-id="b0b8d-103">Executar um relatório de grupo de funções de administrador no EOP</span><span class="sxs-lookup"><span data-stu-id="b0b8d-103">Run an administrator role group report in EOP</span></span> 

 <span data-ttu-id="b0b8d-p101">Quando um administrador adiciona ou remove membros dos grupos de função de administrador, o Microsoft Proteção do Exchange Online (EOP) registra cada ocorrência. Quando você executa um relatório de grupo de funções de administrador no Centro de administração do Exchange, as entradas são exibidas como resultados de pesquisa e incluem os grupos de função afetados, quem e quando alterou a associação do grupo de função, e quais atualizações de associação foram feitas. Use esse relatório para monitorar as alterações nas permissões administrativas atribuídas aos usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p101">When an administrator adds members to or removes members from administrator role groups, Microsoft Exchange Online Protection (EOP) logs each occurrence. When you run an administrator role group report in the Exchange admin center, entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made. Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b0b8d-107">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="b0b8d-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b0b8d-108">Tempo estimado para conclusão: 2 minutos</span><span class="sxs-lookup"><span data-stu-id="b0b8d-108">Estimated time to complete: 2 minutes</span></span>
    
- <span data-ttu-id="b0b8d-p102">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Seção "Relatórios" do tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Reports" section of the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="b0b8d-111">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-111">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="b0b8d-p103">Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p103">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="b0b8d-115">Usar o EAC para executar o relatório de grupo de funções de administrador</span><span class="sxs-lookup"><span data-stu-id="b0b8d-115">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="b0b8d-116">Execute o relatório de grupo de funções de administrador para encontrar as alterações nos grupos de função de gerenciamento em sua organização dentro de um período específico.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-116">Run the administrator role group report to find the changes to management role groups in your organization within a particular timeframe.</span></span>
  
1. <span data-ttu-id="b0b8d-117">No EAC, navegue até **Gerenciamento de conformidade** \> **Auditoria** e escolha **Executar o relatório do grupo de funções do administrador**.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-117">In the EAC, navigate to **Compliance management** \> **Auditing**, and choose **Run an administrator role group report**.</span></span>
    
2. <span data-ttu-id="b0b8d-p104">Escolha a **Data de início** e a **Data de término**. Por padrão, o relatório procura alterações feitas nos grupos de funções do administrador nas duas últimas semanas.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p104">Choose the **Start date** and **End date**. By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>
    
3. <span data-ttu-id="b0b8d-p105">Para exibir as alterações de um grupo de funções específico, clique em **Selecionar grupos de função**. Selecione o grupo de função (ou grupos) na caixa de diálogo subsequente e clique em **OK**. Você também pode deixar o campo em branco para encontrar todos os grupos de função alterados.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p105">To view the changes for a specific role group, click **Select role groups**. Select the role group (or groups) in the subsequent dialog box, and click **OK**. You can also leave the field blank to find all changed role groups.</span></span>
    
4. <span data-ttu-id="b0b8d-123">Clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-123">Click **Search**.</span></span>
    
<span data-ttu-id="b0b8d-p106">Se quaisquer alterações forem encontradas usando os critérios especificados, elas aparecerão no painel de resultados. Clique em um grupo de função nos resultados da pesquisa para ver as alterações no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p106">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="b0b8d-126">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="b0b8d-126">How do you know this worked?</span></span>

<span data-ttu-id="b0b8d-p107">Se você executou com sucesso um relatório de grupo de funções do administrador, os grupos de funções que foram alterados dentro do intervalo de datas serão exibidos no painel de resultados da pesquisa. Se não houver resultados, nenhuma alteração nos grupos de funções será executada dentro do intervalo de datas especificado. Se julgar que deveria haver resultados, altere o intervalo de dados e execute novamente o relatório.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p107">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>
  
## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="b0b8d-130">Monitorar alterações na associação de grupo de funções</span><span class="sxs-lookup"><span data-stu-id="b0b8d-130">Monitor changes to role group membership</span></span>

<span data-ttu-id="b0b8d-p108">Quando os membros são adicionados ou removidos de um grupo de funções, os resultados da pesquisa exibidos no painel de detalhes indicam que a associação de grupo de funções foi atualizada e lista os membros atuais. Os resultados não informam explicitamente qual usuário foi adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p108">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>
  
<span data-ttu-id="b0b8d-p109">Para determinar se um usuário foi adicionado ou removido, você terá que comparar duas entradas separadas no relatório. Por exemplo, vamos observar as entradas de log a seguir do grupo de funções de **HelpDesk**:</span><span class="sxs-lookup"><span data-stu-id="b0b8d-p109">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span> 
  
 <span data-ttu-id="b0b8d-135">**27/01/2013 16h43**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-135">**1/27/2013 4:43 PM**</span></span>
  
 <span data-ttu-id="b0b8d-136">**Administrador**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-136">**Administrator**</span></span>
  
 <span data-ttu-id="b0b8d-137">**Membros atualizados: Administrator;annb,florencef;pilarp**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-137">**Updated members: Administrator;annb,florencef;pilarp**</span></span>
  
 <span data-ttu-id="b0b8d-138">**06/02/2013 10h09**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-138">**2/06/2013 10:09 AM**</span></span>
  
 <span data-ttu-id="b0b8d-139">**Administrador**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-139">**Administrator**</span></span>
  
 <span data-ttu-id="b0b8d-140">**Membros atualizados: Administrator;annb;florencef;pilarp;tonip**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-140">**Updated members: Administrator;annb;florencef;pilarp;tonip**</span></span>
  
 <span data-ttu-id="b0b8d-141">**19/02/2013 14h12**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-141">**2/19/2013 2:12 PM**</span></span>
  
 <span data-ttu-id="b0b8d-142">**Administrador**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-142">**Administrator**</span></span>
  
 <span data-ttu-id="b0b8d-143">**Membros atualizados: Administrator;annb;florencef;tonip**</span><span class="sxs-lookup"><span data-stu-id="b0b8d-143">**Updated members: Administrator;annb;florencef;tonip**</span></span>
  
<span data-ttu-id="b0b8d-144">Nesse exemplo, a conta de usuário Administrador fez as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="b0b8d-144">In this example, the Administrator user account made the following changes:</span></span>
  
- <span data-ttu-id="b0b8d-145">Em 02/06/2013, ela adicionou o usuário tonip.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-145">On 2/06/2013, it added the user tonip.</span></span>
    
- <span data-ttu-id="b0b8d-146">Em 19/02/2013, ela removeu o usuário pilarp.</span><span class="sxs-lookup"><span data-stu-id="b0b8d-146">On 2/19/2013, it removed the user pilarp.</span></span>
    

