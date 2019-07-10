---
title: Ativar o Office 365 ATP para SharePoint, OneDrive e Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
description: Saiba como ativar a ATP para SharePoint, OneDrive e Teams, incluindo como definir alertas para arquivos detectados.
ms.openlocfilehash: c4146ce97f09723a8da543b84dc57bc522581001
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600277"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Ativar o Office 365 ATP para SharePoint, OneDrive e Microsoft Teams

> [!IMPORTANT]
> Este artigo destina-se a clientes corporativos com [proteção avançada contra ameaças do Office 365](office-365-atp.md). Se você for um usuário doméstico que procura informações sobre links seguros no Outlook, consulte [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

O [Office 365 ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) protege sua organização contra o compartilhamento inadvertidamente de arquivos mal-intencionados. Quando um arquivo mal-intencionado é detectado, esse arquivo é bloqueado para que ninguém possa abri-lo, copiá-lo ou compartilhá-lo até que outras ações sejam executadas pela equipe de segurança da organização. Leia este artigo para habilitar a ATP para o SharePoint, o OneDrive e o Microsoft Teams, configure os alertas a serem notificados sobre os arquivos detectados e execute suas próximas etapas. 
  
Para definir (ou editar) políticas ATP, você deve ter uma função apropriada atribuída. Alguns exemplos são descritos na tabela a seguir:

|Role  |Onde/como a atribuição  |
|---------|---------|
|Administrador global do Office 365 |Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global. (Confira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)         |
|Administrador de segurança |Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()|
|Gerenciamento da organização do Exchange Online |Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange () <br>ou <br>  Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Ative a ATP para SharePoint, OneDrive e Microsoft Teams

**Antes de iniciar esse procedimento, verifique se o log de auditoria já está ativado para o seu ambiente do Office 365**. Isso geralmente é feito por alguém que tenha a função de logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).
  
1. Vá até [https://protection.office.com](https://protection.office.com)e entre com sua conta corporativa ou de estudante.
    
2. No centro de conformidade com &amp; segurança do Office 365, no painel de navegação esquerdo, em **Gerenciamento de ameaças**, escolha **anexos seguros**de **política** \> . <br/>![No centro de &amp; conformidade de segurança, escolha política \> de gerenciamento de ameaças](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. Selecione **Ativar ATP para SharePoint, onedrive e Microsoft Teams**.<br/>![Ativar a proteção avançada contra ameaças para o SharePoint Online, o OneDrive for Business e o Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. Clique em **Salvar**.
    
5. Revise (e, conforme apropriado, edite) as [políticas de anexos seguros](set-up-atp-safe-attachments-policies.md) da sua organização e [as políticas de links seguros](set-up-atp-safe-links-policies.md).
    
6. Recomenda Como administrador global ou administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true*. <br/>
      - Definir o parâmetro como *true* bloqueia todas as ações (exceto excluir) para arquivos detectados. As pessoas não podem abrir, mover, copiar ou compartilhar arquivos detectados.
      - A definição do parâmetro como *false* bloqueia todas as ações, exceto excluir e baixar. As pessoas podem optar por aceitar o risco e baixar um arquivo detectado.  
   
7. Aguarde até 30 minutos para que as alterações se espalhem para todos os datacenters do Office 365.
    
8. Recomenda Vá para configurar alertas para arquivos detectados.
    
Para saber mais sobre como usar o PowerShell com o Office 365, confira [gerenciar o office 365 com o PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). 

Para saber mais sobre a experiência do usuário quando um arquivo foi detectado como mal-intencionado, confira [o que fazer quando um arquivo mal-intencionado é encontrado no SharePoint Online, no onedrive ou no Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2). 
  
## <a name="set-up-alerts-for-detected-files"></a>Configurar alertas para arquivos detectados

Para receber notificações quando um arquivo no SharePoint Online, no OneDrive for Business ou no Microsoft Teams foi identificado como mal-intencionado, você pode configurar um alerta.
  
1. No [centro de conformidade de &amp; segurança do Office 365](https://protection.office.com), escolha **alertas** \> **Gerenciar alertas**.
    
2. Escolha **nova política de alerta**.
    
3. Especifique um nome para o alerta. Por exemplo, você pode digitar arquivos mal-intencionados em bibliotecas.
    
4. Digite uma descrição para o alerta. Por exemplo, você pode digitar notifica os administradores quando arquivos mal-intencionados são detectados no SharePoint Online, no OneDrive ou no Microsoft Teams.
    
5. Na seção **Enviar este alerta quando...** , faça o seguinte: 
    
    a. Na lista **atividades** , escolha **malware detectado em arquivo**.
    
    b. Deixe o campo **usuários** vazio. 
    
6. Na seção **Enviar este alerta para...** , selecione um ou mais administradores globais, administradores de segurança ou leitores de segurança que devem receber notificações quando um arquivo mal-intencionado for detectado. 
    
7. Clique em **Salvar**.
    
Para saber mais sobre alertas, confira [criar alertas de atividade no centro de &amp; conformidade de segurança do Office 365](create-activity-alerts.md). 
  
## <a name="next-steps"></a>Próximas etapas

1. [Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365](manage-quarantined-messages-and-files.md)
    

  

