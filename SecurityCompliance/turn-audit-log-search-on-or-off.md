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
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Ativar e desativar a Pesquisa de log de auditoria do Office 365

Você (ou outro administrador) deverá ativar o log de auditoria antes de começar a pesquisar o log de auditoria do Office 365. Quando auditoria pesquisas de log no Office 365 Security &amp; Centro de conformidade está ativado, a atividade de administrador e usuário da sua organização é registrada no log de auditoria e mantida por 90 dias. No entanto, sua organização não talvez queira registrar e reter dados de log de auditoria. Ou você pode estar usando um aplicativo de gerenciamento (SIEM) de eventos e informações de segurança de terceiros para acessar seus dados de auditoria. Nesses casos, um administrador global pode desativar a pesquisa de log de auditoria no Office 365.
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ter a função Logs de auditoria no Exchange Online para ativar ou desativar a pesquisa de log de auditoria em sua organização do Office 365. Por padrão, essa função é atribuída aos grupos de função de gerenciamento de conformidade e gerenciamento da organização na página **permissões** no Centro de administração do Exchange. Administradores globais no Office 365 são membros do grupo de funções de gerenciamento da organização no Exchange Online. 
    
    > [!IMPORTANT]
    > Os usuários precisam ter permissões no Exchange Online para ativar ou desativar a pesquisa de log de auditoria. Se você atribuir usuários a função de Logs de auditoria na página **permissões** na segurança &amp; Centro de conformidade, eles não poderão ativar ou desativar a pesquisa de log de auditoria. Isso ocorre porque o cmdlet subjacente é um cmdlet do Exchange Online. 
  
- Se você desativar a pesquisa de log de auditoria no Office 365, você ainda pode usar a API de atividade de gerenciamento do Office 365 para acessar os dados de auditoria para sua organização. Desativando a pesquisa de log de auditoria, seguindo as etapas neste artigo significa que nenhum resultado será retornado quando você pesquisar o log de auditoria usando a segurança &amp; Centro de conformidade ou quando você executa o cmdlet **Search-UnifiedAuditLog** no Exchange Online PowerShell. No entanto, se você tiver autorizado qualquer aplicativo para acessar dados de auditoria de sua organização via a API de atividade de gerenciamento do Office 365, esses aplicativos continuarão a funcionar. 
    
- Para instruções passo a passo sobre o Office 365 de pesquisa em log de auditoria, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).
    
## <a name="turn-on-audit-log-search"></a>Ativar a pesquisa de log de auditoria

Você pode usar a segurança &amp; Centro de conformidade ou o PowerShell para ativar a pesquisa de log de auditoria no Office 365. Ela pode levar várias horas após ativar pesquisa de log de auditoria antes de você pode retornar resultados ao pesquisar o log de auditoria. Você precisa ter a função Logs de auditoria no Exchange Online para ativar a pesquisa de log de auditoria.
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a>Usar a segurança &amp; Centro de conformidade para ativar a pesquisa de log de auditoria

1. Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de log de auditoria**.
    
2. Clique em **Iniciar gravação atividades de administrador e usuário**.
    
    ![Clique em "Iniciar gravação de atividades do administrador e dos usuários" para habilitar a auditoria](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    Uma caixa de diálogo é exibida informando que a atividade de admin na sua organização e de usuário serão gravados no log de auditoria do Office 365 e disponíveis para exibição em um relatório. 
    
3. Clique em **Ativar**.
    
    Será exibida uma mensagem que informa que o log de auditoria está sendo preparado e que você pode executar uma pesquisa de duas horas após a preparação estiver concluída.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>Use o PowerShell para ativar a pesquisa de log de auditoria

1. [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Execute o seguinte comando do PowerShell para ativar a pesquisa de log de auditoria no Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    Será exibida uma mensagem informando que poderá levar até 60 minutos para que a alteração entre em vigor.
  
## <a name="turn-off-audit-log-search"></a>Desativar a pesquisa de log de auditoria

Você precisa usar o PowerShell remoto conectado à sua organização do Exchange Online para desativar a pesquisa de log de auditoria. Semelhante ao ativem a pesquisa de log de auditoria, você precisa ter a função Logs de auditoria no Exchange Online para desativar a pesquisa de log de auditoria.
  
1. [Conectar-se ao Exchange Online usando o PowerShell Remoto](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Execute o seguinte comando do PowerShell para desativar a pesquisa de log de auditoria no Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. Após algum tempo, verifique se essa pesquisa de log de auditoria está desativada (disabled). Há duas maneiras de fazer isso:
    
    - No PowerShell, execute o seguinte comando:

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        O valor da `False` para o _UnifiedAuditLogIngestionEnabled_ propriedade indica que pesquisa de log de auditoria está desativada. 
    
    - Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de log de auditoria**e clique em **Pesquisar**.
    
      Será exibida uma mensagem informando que a pesquisa de log de auditoria que não está ativada. 
    
      ![Uma mensagem é exibido se a auditoria estiver desativada](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
