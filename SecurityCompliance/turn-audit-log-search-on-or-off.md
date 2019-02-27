---
title: Ativar e desativar a Pesquisa de log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Você pode ativar o recurso pesquisa de log de auditoria no centro de conformidade &amp; de segurança do Office 365. Se você mudar de ideia, poderá desativar se estiver desligado a qualquer momento. Quando a pesquisa de log de auditoria está desativada, os administradores não podem pesquisar o log de auditoria do Office 365 para atividades de usuário e administrador em sua organização.
ms.openlocfilehash: 17b98cce26054d073006fa78c55fe418b5f327d8
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295454"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="45c0e-105">Ativar e desativar a Pesquisa de log de auditoria do Office 365</span><span class="sxs-lookup"><span data-stu-id="45c0e-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="45c0e-p102">Você (ou outro administrador) deve ativar o log de auditoria antes de começar a pesquisar o log de auditoria do Office 365. Quando a pesquisa de log de auditoria no centro &amp; de conformidade de segurança do Office 365 está ativada, a atividade do usuário e do administrador de sua organização é registrada no log de auditoria e mantida por 90 dias. No enTanto, sua organização pode não querer gravar e reter dados de log de auditoria. Ou você pode estar usando um aplicativo de gerenciamento de eventos e informações de segurança (SIEM) de terceiros para acessar seus dados de auditoria. Nesses casos, um administrador global pode desativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="45c0e-111">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="45c0e-111">Before you begin</span></span>

- <span data-ttu-id="45c0e-p103">Você precisa receber a função de logs de auditoria no Exchange Online para ativar ou desativar a pesquisa de log de auditoria na sua organização do Office 365. Por padrão, essa função é atribuída aos grupos de função gerenciamento de conformidade e gerenciamento da organização na página **permissões** no centro de administração do Exchange. Os administradores globais no Office 365 são membros do grupo de funções Gerenciamento da organização no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="45c0e-p104">Os usuários precisam receber permissões no Exchange Online para ativar ou desativar a pesquisa de log de auditoria. Se você atribuir aos usuários a função logs de auditoria na página **permissões** no centro &amp; de conformidade de segurança, eles não poderão ativar ou desativar a pesquisa de log de auditoria. Isso ocorre porque o cmdlet subjacente é um cmdlet do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="45c0e-p105">Se você desativar a pesquisa de log de auditoria no Office 365, ainda poderá usar a API da atividade de gerenciamento do Office 365 para acessar os dados de auditoria da sua organização. DesAtivando a pesquisa de log de auditoria seguindo as etapas deste artigo significa que nenhum resultado será retornado quando você pesquisar o log de auditoria usando &amp; o centro de conformidade de segurança ou quando executar o cmdlet **Search-UnifiedAuditLog** no Exchange Online ™. No enTanto, se você tiver autorizado qualquer aplicativo para acessar os dados de auditoria da sua organização por meio da API de atividade de gerenciamento do Office 365, esses aplicativos continuarão a funcionar.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="45c0e-121">Para obter instruções detalhadas sobre como pesquisar o log de auditoria do Office 365, confira [Pesquisar o log de auditoria no centro de &amp; conformidade de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="45c0e-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="45c0e-122">Ativar pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="45c0e-122">Turn on audit log search</span></span>

<span data-ttu-id="45c0e-p106">Você pode usar o centro &amp; de conformidade de segurança ou o PowerShell para ativar a pesquisa de log de auditoria no Office 365. Pode levar várias horas após você ativar a pesquisa de log de auditoria antes de poder retornar os resultados ao pesquisar o log de auditoria. Você precisa receber a função de logs de auditoria no Exchange Online para ativar a pesquisa de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="45c0e-126">Usar o centro &amp; de conformidade de segurança para ativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="45c0e-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="45c0e-127">No centro de &amp; conformidade de segurança, vá para pesquisa pesquisa de log de \> **auditoria**de \*\* &amp; investigação\*\* .</span><span class="sxs-lookup"><span data-stu-id="45c0e-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="45c0e-128">Clique em **Iniciar gravação de atividades do usuário e do administrador**.</span><span class="sxs-lookup"><span data-stu-id="45c0e-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Clique em "Iniciar gravação de atividades do administrador e dos usuários" para habilitar a auditoria](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="45c0e-130">Uma caixa de diálogo é exibida informando que a atividade de usuário e administrador em sua organização será registrada no log de auditoria do Office 365 e disponível para exibição em um relatório.</span><span class="sxs-lookup"><span data-stu-id="45c0e-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="45c0e-131">Clique em **Ativar**.</span><span class="sxs-lookup"><span data-stu-id="45c0e-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="45c0e-132">Uma mensagem é exibida dizendo que o log de auditoria está sendo preparado e que você pode executar uma pesquisa em algumas horas após a conclusão da preparação.</span><span class="sxs-lookup"><span data-stu-id="45c0e-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="45c0e-133">Usar o PowerShell para ativar a pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="45c0e-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="45c0e-134">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="45c0e-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="45c0e-135">Execute o seguinte comando do PowerShell para ativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="45c0e-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="45c0e-136">Uma mensagem é exibida dizendo que pode levar até 60 minutos para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="45c0e-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="45c0e-137">Desativar pesquisa de log de auditoria</span><span class="sxs-lookup"><span data-stu-id="45c0e-137">Turn off audit log search</span></span>

<span data-ttu-id="45c0e-p107">Você precisa usar o PowerShell remoto conectado à sua organização do Exchange Online para desativar a pesquisa de log de auditoria. Semelhante à ativação da pesquisa de log de auditoria, você precisa ter atribuído a função de logs de auditoria no Exchange Online para desativar a pesquisa de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="45c0e-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="45c0e-140">Conectar-se ao Exchange Online usando o PowerShell Remoto</span><span class="sxs-lookup"><span data-stu-id="45c0e-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="45c0e-141">Execute o seguinte comando do PowerShell para desativar a pesquisa de log de auditoria no Office 365.</span><span class="sxs-lookup"><span data-stu-id="45c0e-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="45c0e-p108">Após um tempo, verifique se a pesquisa de log de auditoria está desativada (desabilitada). Há duas maneiras de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="45c0e-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="45c0e-144">No PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="45c0e-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="45c0e-145">O valor da `False` propriedade _UnifiedAuditLogIngestionEnabled_ indica que a pesquisa de log de auditoria está desativada.</span><span class="sxs-lookup"><span data-stu-id="45c0e-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="45c0e-146">No centro de &amp; conformidade de segurança, vá para pesquisa pesquisa de log de \> **auditoria**de \*\* &amp; investigação\*\* e clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="45c0e-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="45c0e-147">Uma mensagem é exibida dizendo que a pesquisa de log de auditoria não está ativada.</span><span class="sxs-lookup"><span data-stu-id="45c0e-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Uma mensagem é dispayed se A auditoria estiver desativada](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
