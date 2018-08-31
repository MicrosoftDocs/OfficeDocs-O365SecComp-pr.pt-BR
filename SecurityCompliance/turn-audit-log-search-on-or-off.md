---
title: Ativar e desativar a Pesquisa de log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Você pode ativar o recurso de pesquisa de log de auditoria de segurança do Office 365 &amp; Centro de conformidade. Se você mudar de ideia, você pode transformar se desativa a qualquer momento. Quando pesquisa de log de auditoria está desativada, os administradores não podem pesquisar o log de auditoria do Office 365 para atividade de administrador e usuário em sua organização.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524070"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="feeba-105">Ativar e desativar a Pesquisa de log de auditoria do Office 365</span><span class="sxs-lookup"><span data-stu-id="feeba-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="feeba-p102">Você (ou outro administrador) deverá ativar o log de auditoria antes de começar a pesquisar o log de auditoria do Office 365. Quando auditoria pesquisas de log no Office 365 Security &amp; Centro de conformidade está ativado, a atividade de administrador e usuário da sua organização é registrada no log de auditoria e mantida por 90 dias. No entanto, sua organização não talvez queira registrar e reter dados de log de auditoria. Ou você pode estar usando um aplicativo de gerenciamento (SIEM) de eventos e informações de segurança de terceiros para acessar seus dados de auditoria. Nesses casos, um administrador global pode desativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="feeba-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="feeba-111">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="feeba-111">Before you begin</span></span>

- <span data-ttu-id="feeba-p103">Você precisa ter a função Logs de auditoria no Exchange Online para ativar ou desativar a pesquisa de log de auditoria em sua organização do Office 365. Por padrão, essa função é atribuída aos grupos de função de gerenciamento de conformidade e gerenciamento da organização na página **permissões** no Centro de administração do Exchange. Administradores globais no Office 365 são membros do grupo de funções de gerenciamento da organização no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="feeba-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="feeba-p104">Os usuários precisam ter permissões no Exchange Online para ativar ou desativar a pesquisa de log de auditoria. Se você atribuir usuários a função de Logs de auditoria na página **permissões** na segurança &amp; Centro de conformidade, eles não poderão ativar ou desativar a pesquisa de log de auditoria. Isso ocorre porque o cmdlet subjacente é um cmdlet do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="feeba-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="feeba-p105">Se você desativar a pesquisa de log de auditoria no Office 365, você ainda pode usar a API de atividade de gerenciamento do Office 365 para acessar os dados de auditoria para sua organização. Desativando a pesquisa de log de auditoria, seguindo as etapas neste artigo significa que nenhum resultado será retornado quando você pesquisar o log de auditoria usando a segurança &amp; Centro de conformidade ou quando você executa o cmdlet **Search-UnifiedAuditLog** no Exchange Online PowerShell. No entanto, se você tiver autorizado qualquer aplicativo para acessar dados de auditoria de sua organização via a API de atividade de gerenciamento do Office 365, esses aplicativos continuarão a funcionar.</span><span class="sxs-lookup"><span data-stu-id="feeba-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="feeba-121">Para instruções passo a passo sobre o Office 365 de pesquisa em log de auditoria, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="feeba-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="feeba-122">Ativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="feeba-122">Turn on audit log search</span></span>

<span data-ttu-id="feeba-p106">Você pode usar a segurança &amp; Centro de conformidade ou o PowerShell para ativar a pesquisa de log de auditoria no Office 365. Ela pode levar várias horas após ativar pesquisa de log de auditoria antes de você pode retornar resultados ao pesquisar o log de auditoria. Você precisa ter a função Logs de auditoria no Exchange Online para ativar a pesquisa de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="feeba-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="feeba-126">Usar a segurança &amp; Centro de conformidade para ativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="feeba-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="feeba-127">Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de log de auditoria**.</span><span class="sxs-lookup"><span data-stu-id="feeba-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="feeba-128">Clique em **Iniciar gravação atividades de administrador e usuário**.</span><span class="sxs-lookup"><span data-stu-id="feeba-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Clique em "Iniciar gravação de atividades do administrador e dos usuários" para habilitar a auditoria](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="feeba-130">Uma caixa de diálogo é exibida informando que a atividade de admin na sua organização e de usuário serão gravados no log de auditoria do Office 365 e disponíveis para exibição em um relatório.</span><span class="sxs-lookup"><span data-stu-id="feeba-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="feeba-131">Clique em **Ativar**.</span><span class="sxs-lookup"><span data-stu-id="feeba-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="feeba-132">Será exibida uma mensagem que informa que o log de auditoria está sendo preparado e que você pode executar uma pesquisa de duas horas após a preparação estiver concluída.</span><span class="sxs-lookup"><span data-stu-id="feeba-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="feeba-133">Use o PowerShell para ativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="feeba-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="feeba-134">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="feeba-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="feeba-135">Execute o seguinte comando do PowerShell para ativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="feeba-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="feeba-136">Será exibida uma mensagem informando que poderá levar até 60 minutos para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="feeba-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="feeba-137">Desativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="feeba-137">Turn off audit log search</span></span>

<span data-ttu-id="feeba-p107">Você precisa usar o PowerShell remoto conectado à sua organização do Exchange Online para desativar a pesquisa de log de auditoria. Semelhante ao ativem a pesquisa de log de auditoria, você precisa ter a função Logs de auditoria no Exchange Online para desativar a pesquisa de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="feeba-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="feeba-140">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="feeba-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="feeba-141">Execute o seguinte comando do PowerShell para desativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="feeba-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="feeba-p108">Após algum tempo, verifique se essa pesquisa de log de auditoria está desativada (disabled). Há duas maneiras de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="feeba-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="feeba-144">No PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="feeba-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="feeba-145">O valor da `False` para o _UnifiedAuditLogIngestionEnabled_ propriedade indica que pesquisa de log de auditoria está desativada.</span><span class="sxs-lookup"><span data-stu-id="feeba-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="feeba-146">Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de log de auditoria**e clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="feeba-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="feeba-147">Será exibida uma mensagem informando que a pesquisa de log de auditoria que não está ativada.</span><span class="sxs-lookup"><span data-stu-id="feeba-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Uma mensagem é exibido se a auditoria estiver desativada](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
